## Instructions for API
-------------------------------------------------------------------------------------
### Installing Node.js/npm

Follow the installer on [this link](https://nodejs.org/dist/v12.12.0/node-v12.12.0.pkg).

### Installing Homebrew (skip if already installed)

Run `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` in terminal/your command line of choice.
 
 
### Installing yarn
 
Run `brew install yarn`.
 
 
### Installing the Cryb API on your machine
 
Create a folder wherever you desire, and call it "Cryb"
 
In the command line/terminal, run `cd {path to your folder}`.

Then in the command line/terminal, run `git clone https://github.com/crybapp/api.git`.

When that is done, you should see a new folder called api in your cryb folder.


### Installing MongoDB and Redis (databases)

If you're already cd'd into your cryb folder, run `cd api`.
If you aren't, run `cd {path to your cryb folder}/api`.

Now, we're going to "tap" mongoDB, run `brew tap mongodb/brew`

Now, we're going to install mongoDB, run `brew install mongodb-community@4.2`

When you have mongoDB installed, run `brew install redis` to install Redis.

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
