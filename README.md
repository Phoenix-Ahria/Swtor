![fancy logo I stole from somewhere else](http://vignette3.wikia.nocookie.net/starwars/images/6/6d/SWTOR.jpg/revision/latest?cb=20081023010731)
Star Wars: The Old Republic bot powered by AI.

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
- https://github.com/theoephraim/node-google-spreadsheet
- https://mariadb.org/

The bots are powered by the following open source projects:
- Telegram: https://github.com/yagop/node-telegram-bot-api
- Discord: https://discord.js.org
- IRC: https://github.com/martynsmith/node-irc

The data for the bot is provided by:
- http://swtordata.com/
- http://swtorcalendar.com/ (via Google Calendar API)
- http://www.torstatus.net/
- https://www.reddit.com/r/swtor/wiki/upcoming_events
- https://docs.google.com/spreadsheets/d/1aI6kFuRlDxwjJXsq0HybhwdeluEm0JtxHZ20LdxVUsM/ (via Google Drive API)

Database by ~~https://firebase.google.com/~~ _migrating to a local solution_.  
Analytics by https://bot-metrics.com/  

Special Thanks
- [swtor conquest](https://www.reddit.com/user/swtor_conquest) for support on his incredible APIs.
- Eymas & Hess for trying really hard to break the bot for testing purposes.
- [Kaypin_Mayor](https://www.reddit.com/user/Kaypin_Mayor) for providing the Google spreadsheet used for daily operations and cxp bonus activity

## Official Links
[Official Discord Server](https://discord.gg/nNCPzj6) - I will provide support, update details and status changes here.  
[Official Changelog](http://changelog.swtorbot.xyz/) - Constantly updated with everything you need to know, and even things you don't!  
[Official Site](https://swtorbot.xyz/)


## Legacy 
This is not utterly useless. A manual is coming shortly. You'll love it better than double chocolate cake.. not quite as good as tripple though.
