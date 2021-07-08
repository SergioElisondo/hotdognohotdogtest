# Install

`npm install`
`npm i multer`
`npm i axios`

***IN HEROKU: MUST INCLUDE CONFIG VARS!!! There will be a handfull of KEYS and VALUES such as:
CLOUD_NAME
CLOUD_API_KEY
MS_COMPUTER_VISION_SUBSCRIPTION_KEY
etc...
include all of them!

****IN HEROKU: make sure under DEPLOY to change to proper URL


***FIX HEADER NAME -- was "HOT DOG NOT HOT DOG... etc"

****must change to URL friendly header such as: 'hotdognothotdog'

****add node version to package.json (place underneath "version": "1.0.0",) would look like this below:

"engines": {
    "node": "14.11.1"
  },

---



# Things to add

- Create a config folder with a `.env` file and add the following as `key = value`
  - PORT = 2121 (can be any port example: 3000)
  - CLOUD_NAME = `your cloudinary cloud name`
  - CLOUD_API_KEY = `your cloudinary api key`
  - CLOUD_API_SECRET = `your cloudinary api secret`
  - MS_COMPUTER_VISION_SUBSCRIPTION_KEY = `your Microsoft Subscription Key`
  - MS_COMPUTER_VISION_ENDPOINT = `your Microsoft Computer Vision Endpoint`
  - MS_FACE_ENDPOINT = `your Microsoft Face Endpoint`
  - MS_FACE_SUB_KEY = `your Microsoft Face Key`

---

# Run

`npm start`



---
---
-EXTRA NOTES-
YOU MUST RUN THESE STEPS!!

-npm install
(OPTIONAL)-heroku authorizations:create (in case you're out of date...)
-npm install -g heroku  (in the proper directory)
-heroku login -i (if this one doesn't work due to MFA extra security, use the one below to sign in via browser)
-heroku login
(if email already there yellow, just hit ENTER -- then do password)
-heroku create 'name-of-the-project'
(make sure it's like this with dashes and '')

-echo "web:node server.js" > Procfile
-git add . 
-git commit -m "changes"
-git push heroku main


BEFORE YOU UPLOAD
1. "Config Vars" -- add your DB string OR credentials from cloudinary / azure within heroku: 
-go to your app
-go to settings
-go to Config Vars
-add string like this:
DB_STRING  
(left is first box, no equal sign right box is string) 
mongodb+srv://username:password@cluster0.qkej8.mongodb.net/todo?retryWrites=true&w=majority

2. IF using mongoDB, "Whitelist" the IP address in MongoDB -- in other words, "allow all":
-in mongoDB, make sure you're in correct project
-go to Network Access
-go to Edit next to IP Address
-set to either "allow all" or 0.0.0.0/0