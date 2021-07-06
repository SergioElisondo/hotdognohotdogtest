# Install

`npm install`
`npm i multer`

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
