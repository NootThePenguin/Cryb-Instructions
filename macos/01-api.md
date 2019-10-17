## Instructions for API
-------------------------------------------------------------------------------------
We will be using the Terminal to do all the things related to Cryb. You can open this by searching for "Terminal" in Spotlight.

### Installing programs that is needed to run Cryb
In this case, it's Node.js, yarn, MongoDB, and Redis. We will be installing these tools using Homebrew.

#### Installing Homebrew
If you don't already have Homebrew installed, you will need to install it in order to get all the other programs. You can do that by running this command in your terminal program of choice.
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
 
#### Installing the programs
We will now install all the necessary programs by running these commands in the terminal. Specifically:

* Node.js `brew install node`.
* Yarn `brew install yarn`.
* MongoDB `brew tap mongodb/brew && brew install mongodb-community@4.2`.
* Redis `brew install redis`.
 
### Installing the Cryb API
This is where the fun begins! 
 
We need a folder to house all of Cryb's source code. For this particular guide, we will be creating a folder named `cryb` on our Desktop.
In the command line/terminal, navigate to your Desktop, and make a new folder called `cryb`
```
cd ~/Desktop
mkdir cryb
cd cryb
```
After that, we can now download the API by running `git clone https://github.com/crybapp/api.git`. When that's done, a new folder called `api` should appear in your `cryb` folder.

### Editing your Environment file
The environment file will have all the necessary information for the API to function correctly. 
Start by going in to the `api` folder, and making a copy of your example environment file:
```
cd api
cp .env.example .env
```
Now that you have a copy, you can start editing the file in TextEdit by running `open -a TextEdit .env` in the terminal.
Let's start editing:

* Set `NODE_ENV=` to `development` so it should look like `NODE_ENV=development`
* Set `JWT_KEY=` to something complicated, like `JWT_KEY=jiwriouwrehasflkwejrf`
* Set `MONGO_URI=` to `MONGO_URI=mongodb://localhost:27017/cryb`
* Set `REDIS_URI=` to `REDIS_URI=redis://localhost:6379`

Now onto the discord stuff! (Courtesy of NootThePenguin's Windows guide)

Head over to https://discordapp.com/developers/applications and click on New Application and name it whatever you want

![img14](https://i.imgur.com/tZ1m6Ba.png)

Make sure you are on the General Information tab and get your "CLIENT ID" from there, click copy.
Paste it into `DISCORD_CLIENT_ID=<Your client ID here>`
  
Get your client secret (DO NOT SHARE!!) from the same page and click copy
Paste it into `DISCORD_CLIENT_SECRET=<Your client secret here> `
  
For now set DISCORD_CALLBACK_URL to
`DISCORD_CALLBACK_URL=http://localhost:3000/auth/discord`

We will set this up right now

Head over to the OAuth2 tab and make these Redirects

![img15](https://i.imgur.com/ZpZOdka.png)

Now for the last line! 
`DISCORD_OAUTH_ORIGINS=`
Here your going to want to paste all the redirect URLS you made (with commas and no spaces so heres an example)
`DISCORD_OAUTH_ORIGINS=http://localhost:3000`

You should have a file that looks similar to this:

![envExample](https://i.imgur.com/HgWf1Ii.png)

Now you can save the environment file and close TextEdit

**REMEMBER TO SAVE YOUR .ENV FILE**

### Starting MongoDB and Redis
Make sure you're still in Cryb's API folder. If you're lost, simply navigate back to it using `cd ~/Desktop/cryb/api`

Start Redis using this command: `redis-server --daemonize yes --port 6379`
In order to start MongoDB, we would need to setup some folders:

* Make a folder called `data`: `mkdir data`
* Run MongoDB: `mongod --dbpath ~/Desktop/cryb/api/data`
* You should see a bunch of text scrolling. Don't panic, this means that MongoDB is now running. Keep that terminal window open.

### Running the API
It's the final ~~countdown~~ stretch. It's time to start up the API
In a separate terminal window, navigate to the API folder and install the API: 
```
cd ~/Desktop/cryb/api
npm install && yarn
```
After that's complete, run the API using the command `yarn dev`
If everything is in order, you should see a very friendly house in the terminal window.

![apiRunning](https://i.imgur.com/8PZwtd2.png)

_More coming soon._ Feel free to ask in the [Cryb Discord server](https://discord.gg/ShTATH4) meanwhile!
