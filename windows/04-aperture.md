## Instructions for Aperture
-------------------------------------------------------------------------------------
#### Setting up Aperture

Download the Cryb Aperture files [here](https://github.com/crybapp/aperture).

Move the folder to the cryb folder you've made before it should look like this

![img1](https://i.imgur.com/d2cKiTC.png)

In this case I'm going to rename aperture-master to aperture for simplicity

![img2](https://i.imgur.com/W4XfYOw.png)

Open your aperture folder it should look like this

![img3](https://i.imgur.com/AOZ8qht.png)

Reopen your powershell prompt do this by Shift+Right clicking on the folder

![img4](https://i.imgur.com/vpXNGsZ.png)

Type in `npm install` in the powershell and press enter

![img5](https://i.imgur.com/Rv304KQ.png)

A new folder should appear now called node_modules don't touch it

![img6](https://i.imgur.com/Q2DppbT.png)

#### Editting your .env file

Rename your .env.example to .env in your powershell prompt by typing `ren ".env.example" ".env"`

![img7](https://i.imgur.com/Xq3Dl1d.png)

Your file should now be renamed .env

![img8](https://i.imgur.com/MuKRFdO.png)

Open your .env file with notepad++ or notepad doesn't matter

![img9](https://i.imgur.com/xPVkC36.png)

Set `NODE_ENV=` to development so it should look like `NODE_ENV=development`

Set `MONGO_URI=` to `MONGO_URI=mongodb://localhost:27017/cryb`

For now leave as is `APERTURE_KEY=api-aperture-key` we will edit this step 6 maybe

Your .env file should look something like this

![img10](https://i.imgur.com/sdeHSCc.png)

#### Wrapping things up with Powershell

Now type `yarn start` in powershell and press enter

![img11](https://i.imgur.com/LxZ3Z1k.png)

Head over [here](05-portal.md) to setup the portal now.
