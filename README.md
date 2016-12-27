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

The bots are powered by the following open source projects:
- Telegram: https://github.com/yagop/node-telegram-bot-api
- Discord: https://discord.js.org

The data for the bot is provided by:
- http://swtordata.com/
- http://swtorcalendar.com/ (via Google Calendar API)
- http://www.torstatus.net/
- https://www.reddit.com/r/swtor/wiki/upcoming_events

Database by https://firebase.google.com/  
Analytics by https://bot-metrics.com/  

Special Thanks
- [swtor conquest](https://www.reddit.com/user/swtor_conquest) for support on his incredible APIs.
- Eymas & Hess for trying really hard to break the bot for testing purposes.

## Examples
_All examples are from actual conversations with the bot. They are not simulated or theoretical mumbo jumbo to make it all shiny and pretty. Though some responses might vary due to improvements in wordiness and grammar are made._ 

### Dark v. Light Alignment status
**Conversational example:**
>You: What is the DvL status?  
Bot: For which server?  
You: Mantle  
Bot: Mantle of the Force is at light 5.

_As you can see here the bot was able to understand 'Mantle' is really 'Mantle of the Force'. While it's been trained (as a ninja) to understand a lot of aliases, it'll get better overtime as new aliases are trained._

**Another example:**
>You: What is the current alignment of The Ebon Hawk?  
Bot: The Ebon Hawk is at dark 4.

**Advanced Conversational Example:**
>You: What is the DvL status?  
Bot: For which server?  
You: Harbinger  
Bot: The Harbinger is at dark 1.  
You: When was it updated?  
Bot: The Harbinger status was updated 23 minutes ago.

_Obviously there's no server called it, but the bot was able to remember what server you were talking about and continue the conversation. Pretty sure this means it's memory is better than Grandma's!_

### Server Status
**Conversational example:**
>You: What is the status?  
Bot: For which server?  
You: Begeren  
Bot: Begeren Colony is currently online.

**Another Example:**
>You: What is the status of Begeren?  
Bot: Begeren Colony is currently online.

### Server population status 
**Conversational Example:**
>You: What is the current population?  
Bot: For which server?  
You: Jung  
Bot: Jung Ma currently has a light population load.

**Another example:**
>You: How active is Ebon Hawk?  
Bot: The Ebon Hawk currently has a standard population load.

### Server events
_A fair warning: due to the way time works sometimes the bot gets confused when a day ends. I'll fix this, pinky promise_
**Examples:**
>You: What is going on today?  
Bot: I found the following events:  
Bounty Contract Week  
Conquest: Death Mark

>You: What events are on Wednesday??  
Bot: I found the following events:  
Conquest: Total Galactic War

### Items and Crafting
_This is an experimental feature which frequently causes smashings of the keyboard. It allows you to ask what materials are needed to craft a particular item. You can also look up what the value of the item is for a vendor. This uses a third party search algorithm, so please be as specific as you can with the item names for optimal results._

**Crafting**
>You: What do I need to make Advanced Anodyne Versatile Stim?  
Bot: You will need: 2 Hemostatic Gel 1 Autoimmune Regulator 2 Anodyne Cell Graft to craft 1 Advanced Anodyne Versatile Stim with at least 480 in Biochem

**Items**
>You: What's the vendor price for Outlander Boltblaster's Belt MK-6?  
Bot: You should be able to sell Outlander Boltblaster's Belt MK-6 for 1,550 credits to a vendor.

### Event Subscriptions (DvL Alignment)
This feature is highly experimental. Use at own risk of insanity.  

_Set an alert for The Ebon Hawk_
>You: Alert me when The Ebon Hawk is dark 4.

This way you can now quickly jump on to get those Dark Side Tokens nobody ever gets because, the light side always wins _#Rigged_. Private conversations for Discord supporting this will be avilable shortly. This feature is only available on the Telegram platform today.

_Cancel the alert_
>You: Cancel my alignment alerts

**Note**: As of right now you can only have one alert active (per platform).

#### Important Note  

As of this publication the bot is not yet able to process conversational follow ups for the date, and it rarely also thinks it serves more than one game, and occasionally asks you to specify a game. If this happens simply type "swtor" or "star wars".  This will be fixed shortly, another pinky promise.

## Getting Started

Currently the bot is only available on two platforms but if you ignore all of this and scroll down you can see plans to expand to support more platforms in the future.

### Telegram
1) Add [@Swtor_Bot](http://telegram.me/Swtor_Bot) to Telegram.  
2) Ask a question!

**Note**:
The bot only works in private conversations and will not receive any messages from group chats. Sorry, we can't spy on you and your friends sharing dank memes.

### Discord
**Server Administrator/Manager Directions**  
1) Make sure you have permission to add bots to the server. In all honesty I have no idea what the permission is... probably `Manage Server`. _"Okay Google, remind me later to look this up"._  
2) Click [this link](https://discordapp.com/oauth2/authorize?client_id=251931589515280385&scope=bot) to login and authorize the bot to access the server. _The bot doesn't require any additional permissions besides reading and writing to channel's where it should be allowed to operate._  
3) Ask a question!

**Don't have permission or don't have a server?**  
Worry not! You can message the bot directly `SWTOR-BOT#8698` at any time even if you have no servers in common with T2.

**Note**:
- The bot will only process server/guild messages in which it has been @mentioned. All private messages are processed.
- The bot does not support `conversation mode` in guild channels. This feature only works in private discussions.

## What's next?

Somewhere down the yellow brick road is support for the following platforms:
- Amazon Alexa (definitely)  
- Google Assistant (definitely)  
- Facebook Messenger (definitely, maybe)  
- Skype (likely)  
- Twitter (shorta kindaish)  
- Slack, so your co-workers know you have no life outside of work.
- A mobile app that you can talk to awkwardly while waiting for your train. Yes, those people looking at you while you do it are judging you. 
- ~~Snapchat~~ this was a joke.

The additional bots take maybe an hour to setup and configure but my main focus is now the pinky promises I am legally and morally bound to and cleaning up the existing code.

**Additional future plans**:
>You: How many cartel coins is a scavenger pack?  
Bot: Whatever the answer is because this isn't even close to being written.

>You: Alert me when the next Bounty Contract Week is.  
Bot: Okay, I'll let you know when that begins next!

**Got a suggestion?**
You can use GitHub issues here to leave suggestions for the bot. As Lil Wayne once said, the sky is the limit. I'm pretty sure someone else important said that first... but he said it too. Now that I think about that is pretty wrong since spac... not a good place for a debate.

**Do you offer a SWTOR service?**  
If you offer a website or other service related to SWTOR and want to offer integration please do let me know... I am pretty flexible, I do yoga. Not really. Not ever.

## Privacy

All messages that you send to the bot are subject to a few things:

- Depending on the platform, the platform provider may store the messages on their servers. Please refer to the platform's Privacy Policy (available below) for more information how they handle your privacy.  
- The AI provider (wit.ai) uses all input to improve the overall accuracy of the system. Our project is private so the data isn't public but it is kept and accessible by myself and the provider. I do personally review the bot's inner thinkings to make sure it's learning correctly, as is providing the best possible service. It's privacy policy has been included below. 
- I use a bot analytic service called BotMetrics. They receive a copy of every incoming and outgoing message that the bot has processed. They do not receive any personal information about you.  
- I do not save any logs of messages on our servers, however I do store extensive amount of debugging data for improving the bot overall. This debugging data includes the intent of messages (as determined by AI), contextual entities (such as server, date/time, etc.), timestamps (to cross reference AI logs), session information (which includes your unique user id for Telegram, and Discord's channel ID) and the response given.

[Discord's Privacy Policy](https://discordapp.com/privacy)  
[Telegram's Privacy Policy](https://telegram.org/privacy)  
[Wit.ai's Privacy Policy](https://wit.ai/privacy)  
[BotMetric's Privacy Policy](https://bot-metrics.com/privacy)

## Thanks & Support
Thanks for reading this poorly written document which is really just me rambling on. If you decide to help in this inital public test, thanks I love you. In all seriousness it means a lot.

I will be providing support here on GitHub (via issues) or via Reddit if I catch a message. I have no idea where I'll publish a changelog, I'll figure that out once I make changes worth noting.

## Don't sue me
This service is not endorsed by or affiliated with LucasArts, BioWare, or Electronic Arts.

Trademarks are the property of their respective owners. LucasArts, the LucasArts logo, Star Wars and related properties are trademarks in the United States and/or in other countries of Lucasfilm Ltd. and/or its affiliates. © 2008-2011 Lucasfilm Entertainment Company Ltd. or Lucasfilm Ltd. All Rights Reserved. BioWare and the BioWare logo are trademarks or registered trademarks of EA International (Studio and Publishing) Ltd. You may not copy any images, videos or sound clips found on this site or ‘deep link’ to any image, video or sound clip directly.

Game content and materials copyright LICENSOR. All Rights Reserved.
