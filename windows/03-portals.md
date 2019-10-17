## Instructions for Portals
-------------------------------------------------------------------------------------

Download the Cryb Portals files [here](https://github.com/crybapp/portals)

Move the folder to the cryb folder you've made before it should look like this

![img1](https://i.imgur.com/69vEwiG.png)

In this case I'm going to rename portals-master to portals for simplicity 

![img2](https://i.imgur.com/fgMNlFo.png)

Open your portals folder it should look like this

![img3](https://i.imgur.com/F1rqz8R.png)

Reopen your powershell prompt do this by Shift+Right clicking on the folder

![img4](https://i.imgur.com/Hd98Y0U.png)

Type in `npm install` in the powershell

![img5](https://i.imgur.com/NiOfgB0.png)

A new folder should appear now called `node_modules` don't touch it

![img6](https://i.imgur.com/la5uL1g.png)

Now we are going to be editting your .env file!

Rename your .env.example to .env in your powershell prompt by typing `ren ".env.example" ".env"`

![img7](https://i.imgur.com/QAolmTO.png)

Your file should now be renamed .env

![img8](https://i.imgur.com/M1uLNEk.png)

Open your .env file with notepad++ or notepad doesn't matter

![img9](https://i.imgur.com/rky4WcG.png)

Set `NODE_ENV=` to development so it should look like `NODE_ENV=development`

Set `MONGO_URI=` to `MONGO_URI=mongodb://localhost:27017/cryb`

Set `REDIS_URI` to `REDIS_URI=redis://localhost:6379`

Your .env file should look something like this

![img10](https://i.imgur.com/2H5unDo.png)

Now type `yarn dev` in the powershell

![img11](https://i.imgur.com/AHl7U9Q.png)

The end result should be this

![img12](https://i.imgur.com/m8WKggm.png)

Head over [here](04-aperture.md) to setup the aperture server now.