Setting up web files
-

Open up the web folder which you should have if not download from here and put it in your cryb folder

https://github.com/crybapp/web

![img1](https://imgur.com/e9cRdXe)


Rename your .env.example to .env in your powershell prompt by typing ren ".env.example" ".env"

![img1-5](https://i.imgur.com/KIWP2R9.png)

Change `NODE_ENV=` to `NODE_ENV=development`

Change `COOKIE_DOMAIN=` to `COOKIE_DOMAIN=localhost`

![img2](https://i.imgur.com/CZFOqUZ.png)

Shift + Right click to open up the powershell

Type `npm install` and press enter (More should appear then the image below)

![img3](https://i.imgur.com/hUUgurB.png)

Now type `yarn dev` in your powershell

![img4](https://i.imgur.com/sPYvYOn.png)

Your web server is now running! Head over to your browser and type this url localhost:3000/

This should appear: ![img5](https://i.imgur.com/XJUEl9t.png)






