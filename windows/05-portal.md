Instructions for Portal
-

Sign up for docker & verify email

[Click here for Docker Sign up](https://hub.docker.com/signup)

![img1](https://i.imgur.com/5LIZbUW.png)

Download Docker Desktop for Windows

[Click here to download Docker](https://hub.docker.com/?overlay=onboarding)

![img2](https://i.imgur.com/ybCMBk5.png)

Open it up and it should install after clicking on yes/ok

![img3](https://i.imgur.com/7NM3pJ0.png)
![img4](https://i.imgur.com/mLQa3rp.png)

##### `IF FOR WHATEVER REASON YOU CAN'T USE THIS DOCKER PLEASE FOLLOW THIS GUIDE LINKED BELOW IF THE DOCKER ABOVE WORKS FOR YOU, YOU CAN CONTINUE WITH THE GUIDE`

[Install Docker ToolBox Instructions](https://docs.docker.com/toolbox/toolbox_install_windows/#step-2-install-docker-toolbox)

Upon clicking `Close and logout` you'll be logged out of your computer so you'll have to resign in

![img5](https://i.imgur.com/ZEJOy6G.png)

You should get a notification bottom right saying docker is running, if you get this click yes and your computer should restart

![img6](https://i.imgur.com/2za2lDf.png)

Click the little up arrow bottom right of your task bar

![img7](https://i.imgur.com/GQU1R4P.png)

It should say the Docker Desktop is running

![img8](https://i.imgur.com/P7V0lyA.png)



Thats it for dockers for now!


Installing Portal
-

Download the Cryb Portal files 
[here](https://github.com/crybapp/portal)

Move the folder to the cryb folder you've made from the start it should look like this

![img9](https://i.imgur.com/9wILewr.png)

In this case I'm going to rename portal-master to portal for simplicity

![img10](https://i.imgur.com/VTwdsAR.png)

Open your portal folder it should look like this

![img11](https://i.imgur.com/CVweoeE.png)

Reopen your powershell prompt do this by Shift+Right clicking on the folder

![img12](https://i.imgur.com/cC2B8qk.png)

Type in npm install in the powershell and press enter

![img13](https://i.imgur.com/M2pZwfC.png)

A new folder should appear in this directory called node_modules don't touch it

![img14](https://i.imgur.com/aDhlA3l.png)

Editing your .env file
-

Rename your .env.example to .env in your powershell prompt by typing ren ".env.example" ".env"

![img15](https://i.imgur.com/dSy25NN.png)

Your file should now be renamed .env

![img16](https://i.imgur.com/DdtCKNM.png)

Open your .env file with notepad++ or notepad doesn't matter

![img17](https://i.imgur.com/kYRFyKv.png)


Set `NODE_ENV=` to development so it should look like `NODE_ENV=development`

Set `PORTALS_WS_URL=` to `PORTALS_WS_URL=ws://host.docker.internal:1337`

Set `PORTALS_KEY=` to `PORTALS_KEY=portals-portal-key`

Set `APERTURE_URL=` to `APERTURE_URL=http://host.docker.internal:9000`

##### `IGNORE THIS IF YOU DIDN'T DOWNLOAD DOCKER TOOL`
##### `IF YOU'RE USING DOCKER TOOL PORTALS_WS_URL=<YOUR IP> AND APERTURE_URL=<YOUR IP>`
##### [CLICK HERE TO GET YOUR IP](https://whatismyipaddress.com/)

Set `APERTURE_KEY=` to `APERTURE_KEY=api-aperture-key`

Set `VIDEO_WIDTH=` to `VIDEO_WIDTH=1280`

Set `VIDEO_HEIGHT=` to `VIDEO_HEIGHT=720`

Your .env file should look something like this

![img18](https://i.imgur.com/uo4Nozy.png)

Getting Portal to work
-

Make sure you have everything but portal running (Aperture, Api, Web, Portals) including redis-server/mongodb

![img19](https://i.imgur.com/QRVylOE.png)

Don't forget you can check if Mongo is running by checking your task-manager
![img20](https://i.imgur.com/OiPjLez.png)

Open up your browser and head over to `http://localhost:3000/` and login

![img21](https://i.imgur.com/DGURjQI.jpg)

Click create a room and name it what ever you desire

![img22](https://i.imgur.com/80f3dh0.png)

Once you enter your room it should look like this

![img23](https://i.imgur.com/2G7YJwc.jpg)

Notice how top right it says `Portal ID: N/A` and `Portal Status: waiting` you need to make an alternative discord account so this changes

![img24](https://i.imgur.com/v3s4ZLp.png)

Make a quick discord account

[Click here to go to the registration page](https://discordapp.com/register)

Once you created another discord account, open up incognito mode (Press CTRL+SHIFT+N at the same time)

Great you got incognito open should look like this (if your using chrome)

![img25](https://i.imgur.com/PhXbo2h.png)

Now head over to the same website where your main account is, so go here `http://localhost:3000/` and login 

Once you logged in click `Join room` instead of create room 

![img26](https://i.imgur.com/JcejZmG.png)

Head on back over to the non-incognito browser and click the URL where it saids Copy and share this link with your friends

![img27](https://i.imgur.com/3C37zeo.jpg)

Once that link is copied head back to the incognito browser and paste that where it asks for an invite code and join

![img28](https://i.imgur.com/uWjuZ6J.png)

You should now see values for `Portal ID:` and how `Portal Status:` changed
![img29](https://i.imgur.com/FmwQ6Yb.jpg)

Open up your portals powershell which should be running and notice how it saids `yarn docker:dev --portalId <Your portal id here>`
you will need this to run portal 

Head back to your Portal folder and open up the powershell 

![img30](https://i.imgur.com/E28YhUK.png)

Copy the `yarn docker:dev --portalId <Your portal id here>` and paste it in your Portal powershell
  
![img31](https://i.imgur.com/bGVdOje.png)

Press enter and it should look something like this 

![img32](https://i.imgur.com/KrZzxEz.png)

Head back to your browser for a surprise!

![img33](https://i.imgur.com/oKIhRwQ.png)

Grats you got it working! Currently there is no sound but there will be a fix for that very soon!

_More coming soon._ Feel free to ask in the [Cryb Discord server](https://discord.gg/ShTATH4) meanwhile!
