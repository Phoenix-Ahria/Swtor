![fancy logo I stole from somewhere else](http://vignette3.wikia.nocookie.net/starwars/images/6/6d/SWTOR.jpg/revision/latest?cb=20081023010731)
Star Wars: The Old Republic bot powered by AI.

![Updated weekly](https://img.shields.io/badge/Discord-100-7289DA.png?colorA=7289DA&colorB=2C2F33&style=plastic) ![Updated weekly](https://img.shields.io/badge/Version-5.3-red.png?style=plastic) ![Updated weekly](https://img.shields.io/badge/Avg.%20daily%20messages-624-blue.png?style=plastic)
---
The bot is backed by NLP, or Natural Language Processing, the same technology behind Apple's Siri, Amazon's Alexa, and Google's... well everything. The bot is able to understand contextual information and process the intent of your messages as well as keep a conversation for follow up information. 

This project was more of an experiment for me to push my terrible programming abilities to their limits and beyond. I like to think it turned out pretty nicely but I might be a bit biased. The current implementation of the bot is entirely still experimental but 7.83/10 times the bot will get the job done right without any keyboard smashing. It's able to do a few early functions like lookup in-game events, dark v. light alignment statuses, server population, crafting and item information, and server status. The bot is currently being released for public testing on two platforms initially with plans down the road for more.

Before I get into the fun little details I want to give credit to the real people make this thing work, the developers of the open source projects that make it all possible.

The entire project is built on [Node.js](https://nodejs.org/en/).

The following open source projects were used in this project:
- http://underscorejs.org/
- https://github.com/wit-ai/node-wit
- http://socket.io/
- https://epeli.github.io/underscore.string/
- https://github.com/winstonjs/winston
- https://github.com/request/request
- http://momentjs.com/
- https://github.com/mnort9/node-botmetrics  
- https://lodash.com/  
- https://github.com/mysqljs/mysql
- https://www.npmjs.com/package/uws
- https://github.com/hammerandchisel/erlpack
- https://github.com/yagop/node-telegram-bot-api
- https://discord.js.org
- https://github.com/martynsmith/node-irc
- https://github.com/desmondmorris/node-twitter
- https://github.com/sentientwaffle/feed-read
- https://github.com/chriso/validator.js
- http://expressjs.com/
- https://www.npmjs.com/package/express-ipfilter
- https://www.npmjs.com/package/express-rate-limit
- https://github.com/expressjs/body-parser
- https://github.com/omnidan/node-emoji
- https://github.com/keymetrics/pmx

The data for the bot is provided by:
- http://swtordata.com/
- http://swtorcalendar.com/ (via Google Calendar API)
- http://www.torstatus.net/
- https://www.reddit.com/r/swtor/wiki/upcoming_events

Database powered by [MariaDB](https://mariadb.org/)  
Analytics by [bot-metrics](https://bot-metrics.com/)  
App Monitoring by [Keymetrics](https://keymetrics.io/)  
Web services secured by [Cloudflare](https://www.cloudflare.com/)  
Hosted on [Vultr](https://www.vultr.com/) and [OVH](https://www.ovh.com)

Special Thanks
- [swtor conquest](https://www.reddit.com/user/swtor_conquest) for support on his incredible APIs.
- Eymas for trying really hard to break the bot for testing purposes.  
- Hess for also trying really hard to break the bot, and design / graphic help.
- [Kaypin_Mayor](https://www.reddit.com/user/Kaypin_Mayor) for providing the Google spreadsheet originally used for daily operations and cxp bonus activity

## Official Links
[Official Discord Server](https://discord.gg/nNCPzj6) - I will provide support, update details and status changes here.  
[Official Changelog](http://changelog.swtorbot.xyz/) - Constantly updated with everything you need to know, and even things you don't!  
[Official Site](https://swtorbot.xyz/)  
[Official Examples & HowTo](https://swtorbot.xyz/how-to/) - Work in progress

## Contribute
I have open sourced some of the local data sources the bot uses. Feel free to make a pull request to contribute. Or don't. I really don't care. Please list sources.

## Don't sue me
This service is not endorsed by or affiliated with LucasArts, BioWare, or Electronic Arts.

Trademarks are the property of their respective owners. LucasArts, the LucasArts logo, Star Wars and related properties are trademarks in the United States and/or in other countries of Lucasfilm Ltd. and/or its affiliates. © 2008-2011 Lucasfilm Entertainment Company Ltd. or Lucasfilm Ltd. All Rights Reserved. BioWare and the BioWare logo are trademarks or registered trademarks of EA International (Studio and Publishing) Ltd. You may not copy any images, videos or sound clips found on this site or ‘deep link’ to any image, video or sound clip directly.

Game content and materials copyright LICENSOR. All Rights Reserved.
