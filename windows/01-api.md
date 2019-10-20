## Instructions for API
-------------------------------------------------------------------------------------
#### Installing Node.js/npm

Download and install Node.js from [here](https://nodejs.org/en/). LTS works well.

-------------------------------------------------------------------------------------
#### Installing MongoDB

We also need to install MongoDB. Community Server is fine, which you can get [here](https://www.mongodb.com/download-center/community).

Go through the installer, accept agreement and click complete. Keep on mind to install MongoDB as a service.

![img](https://i.imgur.com/QuiMM1n.png)

You don't need to install mongo-compass so it's no problem if you uncheck that.

Once installed, head over to the directory path where it was installed. For example, in the case of this guide, `C:\Program Files\MongoDB\Server\4.2\bin`.

![img2](https://i.imgur.com/L8FqBj1.png)

Click MongoDB to launch the service. A command prompt should appear and disappear.
Open up Task Manager and check if it's running:

![img3](https://i.imgur.com/0An6wIn.png)

-------------------------------------------------------------------------------------
#### Installing redis-server

Now we are going to install redis-server, which you can get [here](https://github.com/downloads/dmajkic/redis/redis-2.4.5-win32-win64.zip).

Make a new folder on your desktop call it redis-server:

![img4](https://i.imgur.com/ONM4pMm.png)

Drag the files onto that new folder, then go to the 64bit folder (assuming you have a 64 bits computer)
and start redis-server.exe, allowing access in the Windows Firewall.

![img6](https://i.imgur.com/NRJbua3.png)

-------------------------------------------------------------------------------------
#### Installing yarn

Head over to [this](https://yarnpkg.com/latest.msi) to install yarn then go through the installer.


-------------------------------------------------------------------------------------
#### Downloading and setting up cryb API

Download zips (you could also do git commands but w/e)

https://github.com/crybapp/api

https://github.com/crybapp/web

Make a folder named "cryb" (name can be w/e)
Move the folders into cryb like this: ![img7](https://i.imgur.com/nMEVyUu.png)

In this case I'm going to rename api-master and web-master folder to api and web 

![img8](https://i.imgur.com/e9cRdXe.png)

Open up the api folder

![img9](https://i.imgur.com/967QrrJ.png)

Shift + Right click and click Open PowerShell window here

![img10](https://i.imgur.com/gcEC8X5.png)

Type `npm install` in Windows PowerShell

![img10-5](https://i.imgur.com/dj8jJs2.png)

You should now have a new folder in your api folder called `node_modules` don't touch it

![img11](https://i.imgur.com/LPrAClV.png)


-------------------------------------------------------------------------------------
#### Editting your .env file

Rename your .env.example to .env in your powershell prompt by typing `ren ".env.example" ".env"`

![img11-5](https://i.imgur.com/KIWP2R9.png)

Your file should now be renamed to .env

![img12](https://i.imgur.com/7rdGtB5.png)

Now open your .env file with notepad++ or notepad doesn't matter

![img13](https://i.imgur.com/NpzVD1s.png)

Set `NODE_ENV=` to development so it should look like `NODE_ENV=development`

Leave `PORT=4000` as default

Set `JWT_KEY=` to anything example, "km93m8c928ma90!mif" so `JWT_KEY=km93m8c928ma90!mif` (make it something complicated) or get something from random.org

Set `MONGO_URI=` to `MONGO_URI=mongodb://localhost:27017/cryb`

Set `REDIS_URI=` to `REDIS_URI=redis://localhost:6379`

Now onto the discord stuff!

Head over to https://discordapp.com/developers/applications and click on New Application and name it whatever you want

![img14](https://i.imgur.com/tZ1m6Ba.png)

Make sure you are on the General Information tab and get your "CLIENT ID" from there, click copy.
Paste it into `DISCORD_CLIENT_ID=<Your client ID here>`
  
Get your client secret (DO NOT SHARE!!) from the same page and click copy
Paste it into `DISCORD_CLIENT_SECRET=<Your client secret here> `  

We will set this up right now

Head over to the OAuth2 tab and make these Redirects

![img15](https://i.imgur.com/ZpZOdka.png)

Your all set with the .env file it should look like this (My client-id, secret-client is random and should be different from yours):

![img16](https://i.imgur.com/owkfb9u.png)

-------------------------------------------------------------------------------------
#### Wrapping things up with the powershell

If you closed your powershell open it again (look above for reference)

Type `yarn` to confirm the installation of yarn

![img17](https://i.imgur.com/4N50QVz.png)

Now type `yarn dev` and press enter this should appear

![img18](https://i.imgur.com/NeRqPqB.png)

Head over [here](02-web.md) to setup the web server now.
