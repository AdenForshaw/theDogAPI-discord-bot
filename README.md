# A Doggy Discord Bot
Example of how to make a Discord bot using theDogAPI.com or theCatAPI.com in NodeJs. Simple app you can experiment with yourself.
An issues hit me up - http://twitter.com/adenforshaw

The Dog API & Cat API use exactly the same REST API schema, so code built for one will work with the other - all you need is an API key for each.


![The Dog API packshot](docs/packshot.png)

# Setup
- Get your [API Key](https://thedogapi.com/signup) (it'll be emailed to you immediately)
- Setup a [Discord App](https://discordapp.com/developers/applications/me/create) & create a Bot user - save the TOKEN it gives you
- Clone the repo 'git clone https://github.com/AdenForshaw/theDogAPI-discord-bot'
- Change 'DOG_API_KEY' and 'DISCORD_TOKEN' in the 'index.js' file for the values you from above.
- Run 'npm install' in the cloned folder to install the libraries
- Run 'node index.js' to start the application
- In the Discord channel you added the Bot send the message 'woof'
- Enjoy the Dog image!

# How it should look in the Discord Client
![Discord Message Example](docs/discord-example.png)

# How does it work?
![Flow Diagram](docs/flow-diagram.png)
- Once the app is connected to Discord it stays alive via a websocket connection
- It listens to every message in the channel, 
- when someone says 'woof' it makes a request to TheDogAPI for a random image
- it the uses the 'url' and 'breed' values of the returned image, and sends it to the channel

# Where next?
- You could have the Bot 'always-on' by putting it on the cloud with the [AWS free tier using Elastic Beanstalk](https://aws.amazon.com/free/)
- Expand more commands to send back different breed of dogs, or different categories.
