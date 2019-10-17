## Instructions for API
-------------------------------------------------------------------------------------
We will be using the Terminal to do all the things related to Cryb. You can open this by searching for "Terminal" in Spotlight.

### Installing programs that is needed to run Cryb

In this case, it's Node.js, yarn, MongoDB, and Redis. We will be installing these tools using Homebrew.

#### Installing Homebrew

If you don't already have Homebrew installed, you will need to install it in order to get all the other programs. You can do that by running this command in your terminal program of choice.
```/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```
 
#### Installing the programs
 
We will now install all the necessary programs by running these commands in the terminal. Specifically:
     - Node.js `brew install node`.
     - Yarn `brew install yarn`.
     - MongoDB `brew tap mongodb/brew && brew install mongodb-community@4.2`.
     - Redis `brew install redis`.
 
### Installing the Cryb API

This is where the fun begins! 
 
We need a folder to house all of Cryb's source code. For this particular guide, we will be creating a folder named `cryb` on our Desktop.
 
In the command line/terminal, navigate to your Desktop, and make a new folder called `cryb`
```cd ~/Desktop
   mkdir cryb
   cd cryb```

After that, we can now download the API by running `git clone https://github.com/crybapp/api.git`. When that's done, a new folder called `api` should appear in your `cryb` folder.

<image goes here>

### Installing the required dependencies

Make sure you're still cd'd into your api folder, then run `yarn`

### Editing your ENV

To edit your ENV, go into finder and find your `cryb/api` folder.

When you're in the API folder, you'll see a file called `.env.example`. Rename it to just `.env`

Double click on your `.env` file. a TextEdit window should open up.

When you're in the file, the first thing you'll see is `NODE_ENV=` make it `NODE_ENV=development`

Then, you'll see `PORTALS_API_KEY=api-portals-key, APERTURE_WS_KEY=api-aperture-key,` and `APERTURE_WS_KEY=api-aperture-key` 
Make sure to **NOT** touch these values. 

Then, youll see `MONGO_URI=` change it to `MONGO_URI=mongodb://localhost:27017/cryb`

Then, you'll see `REDIS_URI=` **DO NOT** touch this value. Leave it blank.

Then you'll see many things discord-related. You'll want to go to discordapp.com and go to the developer portal.
In the developer portal, create an app and make the name "Cryb" and a logo of your choice. When it's created, copy the ID and put it in `DISCORD_CLIENT_ID=` 

Then, copy the Client Secret and put it in `DISCORD_CLIENT_SECRET=` **make sure theres no spaces between the = sign and ANY of the .env values.**

Here comes the hard part, on the side bar navigate to the "OAuth2" tab.

Then, you'll see redirects. Click on Add Redirect. type `http://localhost:3000/auth/discord` **MAKE SURE TO SAVE THIS**

Now, go back to your .env file and as `DISCORD_CALLBACK_URL=` put `http://localhost:3000/auth/discord` **make sure theres no spaces between the = sign and ANY of the .env values.**

**SAVE YOUR .ENV**

### Starting MongoDB and Redis

make sure you cd'd into cryb api folder

To start MongoDB and Redis, make sure your cd'd into your cryb api folder, and first run `redis-server --daemonize yes --port 6379` to start redis

If no errors formulate, redis is running.

To start mongoDB, create a folder inside your Cryb folder called "data"

then run `cd data`

run `mongod --dbpath <path to your cryb/data folder>` and a long thing of logs should formulate and mongodb is started, don't close the window.

### Running the API

To run your api, make sure you cd'd into cryb api folder, and run the command `yarn dev`

**make a new terminal window to not disrupt mongodb running**

Now, you have the Cryb API up and running!

_More coming soon._ Feel free to ask in the [Cryb Discord server](https://discord.gg/ShTATH4) meanwhile!
