# SmartGlass
---
### This is an unofficial NodeJS client implementation of Microsoft's Xbox One SmartGlass protocol.

This project is in its early development stages and as such has limited functionality.

*Installation*

```
yarn add smartglass
```

*Basic Usage*
Super simple promise based api
```js
import smartglass from 'smartglass'

// authenticate
const Console = await smartglass.authenticate('user@email.com', 'password')

// discover consoles on the network and set the first as the default - also returns an array of discovered consoles via a promise:
Console.discover()

// Set the currently selected console by ip address
Console.select("10.0.0.241")

// Power on/off console
Console.on()
Console.off()

// Gamepad input
Console.A()
Console.B()
Console.X()
Console.Y()

Console.Up()
Console.Down()
Console.Left()
Console.Right()

Console.Home()
Console.View()
Console.Menu()

// Text input - Send text input to console when a textfield is opened
Console.Text('some text')
```

*Planned and implemented features*

- [ ] Microsoft Xbox Live Authentication
- [ ] Console Discovery
- [ ] Power console on/off
- [ ] Gamepad input
- [ ] Text input
- [ ] Title launch

*Known issues*
* Initial implementation of this module consumes some python scripts (for sending the packets) but v2 is planned for a pure node implementation.
* Log em bugs as ya find em

*Contribute*
* Report bugs/suggest features
* Add/update docs

*Huge thanks to*
- @tuxuser - for pointing me to the [smartglass-documentation](https://openxbox.org/smartglass-documentation/)
- [OpenXbox](https://github.com/OpenXbox) - for all their work