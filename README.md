<img src="https://cdn.discordapp.com/attachments/780245027212492812/780245250382757930/TwitchJS.png">
<p>
  <a href="https://discord.gg/26KFSUbVFe"><img src="https://img.shields.io/discord/773920681246851083?color=7289da&logo=discord&logoColor=FFFF55"/></a>
  <a href="https://www.npmjs.com/package/@twitchapis/twitch.js"><img src="https://img.shields.io/npm/v/@twitchapis/twitch.js.svg?maxAge=3600"/></a>
  <a href="https://www.npmjs.com/package/@twitchapis/twitch.js"><img src="https://img.shields.io/npm/dt/@twitchapis/twitch.js.svg?maxAge=3600"/></a>
  <a href="https://github.com/twitchapis/twitch.js"><img src="https://github.com/twitchapis/twitch.js/workflows/Testing/badge.svg"/></a>
  <a href="https://github.com/twitchapis/twitch.js"><img src="https://img.shields.io/david/twitchapis/twitch.js.svg?maxAge=3600"/></a>
</p>
<img src="https://nodei.co/npm/@twitchapis/twitch.js.png?downloads=true&stars=true">

## Summary

- [TODO](#todo)
- [About](#about)
- [Installing](#installing)
  - [npm](#npm)
  - [yarn](#yarn)
- [Example Usage](#example-usage)
- [contributors](#contributors)

## TODO

- [X] Beauty logger. (**DON'T TOUCH HIM**)
- [X] Stabilize a websocket connection with Twitchᵀⱽ.
- [X] Create easy functions to interact with Twitchᵀⱽ.
- [ ] Create onReady event.
- [ ] Create all easy interact functions to Twitchᵀⱽ.
- [ ] Create event dispatchers to the actions.

## About

Twitchʲˢ is a [unnoficial] powerful [Node.js](https://nodejs.org) module that allows you to easily interact with the
[Twitchᵀⱽ](https://twitch.tv) making easy the way to make a Twitchᵀⱽ bot, for a custom chat overlay for you [OBS](https://obsproject.com/), or a moderation bot for you chat, or you just want a easy interface to Twitchᵀⱽ.

- Object-oriented
- Predictable abstractions
- Performant

## installing

**Node.js 12.0.0 or newer is required.**  

#### npm: 
```bat
npm i @twitchapis/twitch.js
```  
#### yarn: 
```bat
yarn add @twitchapis/twitch.js
```  

## example-usage

```javascript
  const Twitch = require('@twitchapis/twitch.js');

  const Client = new Twitch.Client({
      autoLogEnd: true,
      channels: ['space_interprise', 'lobometalurgico'],
      debug: true
  });

  Client.on('message', msg => {
      if (msg.toString().toLowerCase().includes('hello')) {
          msg.reply('World');
      }
      if (msg.toString().toLowerCase() === 'leave space_interprise channel') {
        msg.channel.send('Ok, goodbye ;-;')
        Client.leave('space_interprise');
      }
  });

  Client.login('MyFabolousBotUserName', 'MyFabolousBotToken🤫').then(() => {
      Twitch.logger.info('YAY, i am connected with twitch!');
  });
```

## contributors

- [Lobo Metalurgico](https://github.com/LoboMetalurgico)
- [Space_Interprise](https://github.com/emanuelfranklyn)
