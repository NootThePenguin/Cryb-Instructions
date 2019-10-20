## Instructions for Web
-------------------------------------------------------------------------------------

Open up the web folder which you should have, if not download from here and put it in your cryb folder.

https://github.com/crybapp/web

![img1](https://i.imgur.com/e9cRdXe.png)

Your web folder should look like this

![img-2](https://i.imgur.com/SoME73m.png)

Shift + Right click to open up the powershell

![img2-5](https://i.imgur.com/ga8CgS7.png)

Type `npm install` and press enter

![img3](https://i.imgur.com/9Sw6hPG.png)

You should now have a new folder in your web folder called `node_modules` don't touch it

![img4](https://i.imgur.com/XD9eBHX.png)

Rename your .env.example to .env in your powershell prompt by typing `ren ".env.example" ".env"`

![img5](https://i.imgur.com/KIWP2R9.png)

Open up your .env, it should look like this

![img6](https://i.imgur.com/D77ywrE.png)

Change `NODE_ENV=` to `NODE_ENV=development`

Change `COOKIE_DOMAIN=` to `COOKIE_DOMAIN=localhost`

Your .env should look like this now

![img7](https://i.imgur.com/CZFOqUZ.png)

Now type `yarn dev` in your powershell

![img4](https://i.imgur.com/sPYvYOn.png)

Your web server is now running! Head over to your browser and type this url `localhost:3000/`

This should appear: ![img5](https://i.imgur.com/XJUEl9t.png)

Head over [here](03-portals.md) to setup the portals server now.
