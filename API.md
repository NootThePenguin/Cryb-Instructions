# CrybAPI-Instructions 
Windows and Mac 

https://github.com/crybapp

Cryb was created by William

Windows guide by Noot

Mac guide by lolaustin


I apologies in advanced if the instructions are unclear but if you need help feel free to contact me on discord Noot#0420
## Windows (scroll down for mac)
-------------------------------------------------------------------------------------
#### Installing NPM (nodejs)


Link to install (unfortunately can't really give instructions on this but should be straight forward)

Go through the installer when completed

https://nodejs.org/dist/v10.16.3/node-v10.16.3-x64.msi

-------------------------------------------------------------------------------------
#### Installing MongoDB


First off we are going to install mongodb (windows)

https://www.mongodb.com/dr/fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.0-signed.msi/download

Go through the installer, accept agreement and click complete and install mongodb as a service
https://i.imgur.com/QuiMM1n.png

You dont need to install mongo-compass so you uncheck that and let it install

Once install head over to the directory path installed in this case mine was

C:\Program Files\MongoDB\Server\4.2\bin

https://i.imgur.com/L8FqBj1.png

Click mongod to launch the service a cmd prompt should appear and disappear
Open up taskmanager and check if its running in this case it is

https://i.imgur.com/0An6wIn.png

-------------------------------------------------------------------------------------
#### Installing redis-server

Now we are going to install redis-server

https://github.com/downloads/dmajkic/redis/redis-2.4.5-win32-win64.zip

Make a new folder on your desktop call it redis-server 

https://i.imgur.com/ONM4pMm.png

Drag the files onto that new folder

https://i.imgur.com/PU9iCf7.png

Click on the 64bit (assuming you have a 64 bit computer) and click redis-server.exe and allow access

https://i.imgur.com/NRJbua3.png

-------------------------------------------------------------------------------------
#### Installing yarn

Head over to this website to install yarn on your windows computer

https://yarnpkg.com/latest.msi

Go through the installer, click next etc.


-------------------------------------------------------------------------------------
#### Downloading and setting up cryb API

Download zips (you could also do git commands but w/e)

https://github.com/crybapp/api

https://github.com/crybapp/web

Make a folder named "cryb" (name can be w/e)
Move the folders into cryb like this: https://i.imgur.com/nMEVyUu.png

In this case I'm going to rename api-master and web-master folder to api and web 

https://i.imgur.com/e9cRdXe.png

Open up the api folder

https://i.imgur.com/pRDaiHT.png

Shift + Right click and click Open PowerShell window here

https://i.imgur.com/XnTQnZm.png

Type "npm install" in Windows PowerShell

https://i.imgur.com/9yr6j98.png

You should now have a new folder in your api folder called "node_modules" don't touch it

https://i.imgur.com/wVnEoho.png


For now close your powershell.

-------------------------------------------------------------------------------------
#### Editting your .env file

Rename your .env.example folder to .env

https://i.imgur.com/EKpEnBE.png

Now open your .env file with notepad++ or notepad doesn't matter

https://i.imgur.com/DHbJ57m.png

Set NODE_ENV= to development so it should look like NODE_ENV=development

Set the JWT_KEY to anything, example -> "km93m8c928ma90!mif" so JWT_KEY=km93m8c928ma90!mif (make it something complicated) or get something from random.org

Set MONGO_URI= to MONGO_URI=mongodb://localhost:27017/cryb

Leave REDIS_URI= blank as it should connect to localhost 

Now onto the discord stuff!

Head over to https://discordapp.com/developers/applications and click on New Application and name it whatever you want

https://i.imgur.com/tZ1m6Ba.png

Make sure you are on the General Information tab and get your "CLIENT ID" from there, click copy.
Paste it into DISCORD_CLIENT_ID=<Your client ID here>
  
Get your client secret (DO NOT SHARE!!) from the same page and click copy
Paste it into DISCORD_CLIENT_SECRET=<Your client secret here> 
  
For now set DISCORD_CALLBACK_URL to
DISCORD_CALLBACK_URL=http://localhost:3000/auth/discord

We will set this up right now

Head over to the OAuth2 tab and make these Redirects

https://i.imgur.com/ZpZOdka.png

Now for the last line! 
DISCORD_OAUTH_ORIGINS=
Here your going to want to paste all the redirect URLS you made (with commas and no spaces so heres an example)
DISCORD_OAUTH_ORIGINS=http://localhost:3000/auth/discord,http://localhost:4000/auth/discord,http://localhost/auth/discord

Your all set with the .env file it should look like this (My client-id, secret-client is random and should be different from yours):

https://i.imgur.com/3hmVkbU.png

-------------------------------------------------------------------------------------
#### Wrapping things up with the powershell

If you closed your powershell open it again (look above for reference)

Type yarn to confirm the installation of yarn

https://i.imgur.com/4N50QVz.png

Now type "yarn dev" and press enter this should appear

https://i.imgur.com/NeRqPqB.png

Head over to here to setup the web server now

https://github.com/NootThePenguin/Cryb-Instructions/blob/master/Web-Installation.md

------

## Mac 
by lolaustin


### Installing Node

Follow the installer on this link - https://nodejs.org/dist/v12.12.0/node-v12.12.0.pkg

### Installing Homebrew (skip if already installed)

 run `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` in terminal/your command line of choice.
 
 
 ### Installing yarn
 
 run `brew install yarn`
 
 
 ### Installing the Cryb API on your machine
 
 Create a folder wherever you desire, and call it "Cryb"
 
In the command line/terminal, run `cd {path to your folder}`

Then in the command line/terminal, run `https://github.com/crybapp/api.git`

When that is done, you should see a new folder called api in your cryb folder.


### Installing MongoDB and Redis (databases)

If you're already cd'd into your cryb folder, run `cd api`
If you aren't, run `cd {path to your cryb folder}/api`

Now, we're going to "tap" mongoDB, run `brew tap mongodb/brew`

Now, we're going to install mongoDB, run `brew install mongodb-community@4.2`

When you have mongoDB installed, run `brew install redis` to install redis.

and run `npm install redis-server` to install redis-server

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

Then, you'll see redirects. Click on Add Redirect. type `http://localhost:3000/auth/discord` Then add another redirect, type `http://localhost:4000/auth/discord` **MAKE SURE TO SAVE THIS**

Now, go back to your .env file and as `DISCORD_CALLBACK_URL=` put `http://localhost:3000/auth/discord` **make sure theres no spaces between the = sign and ANY of the .env values.**

**SAVE YOUR .ENV**

### Starting MongoDB and Redis

make sure you cd'd into cryb api folder

To start MongoDB and Redis, make sure your cd'd into your cryb api folder, and first run `redis-server --daemonize yes --port 6379` to start redis

If no errors formulate, redis is running.

To start mongoDB, create a folder in cryb api folder called "data" and inside of that create a folder called "db"

then run `cd`

run `mongod --dbpath <path to your cryb/api/data/db folder>` and a long thing of logs should formulate and mongodb is started, don't close the window.


### Running the API

To run your api, make sure you cd'd into cryb api folder, and run the command `yarn dev`

**make a new terminal window to not disrupt mongodb running**

Now, you have the Cryb API up and running!
