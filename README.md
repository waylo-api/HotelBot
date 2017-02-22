# HotelBot built using the Waylo API

You can clone this repo to create your own hotel booking Facebook Messenger chatbot in 10 minutes. The hotel bookings are provided by [Waylo API](http://dev.thewaylo.com) and you earn a share of the revenue.

If you want to test out a HotelBot first, try [Waylo Bot](https://m.me/thewaylo)

# Build Your Hotel Booking Bot and Monetize

Creating this version will give you a Facebook Messenger chat bot. 

![Demo](http://i.imgur.com/I9MgSI8.gif)

You can read our [FAQ](http://dev.thewaylo.com/faq.html) to learn more about the monetization. The average earnings per booking from your bot is ~ USD 10.

# How is this possible in 10 minutes?

This is an example of bot to bot communcation. You only set up a simple FB bot with a button. Waylo's API takes care of the Natural Language Understanding, getting access to inventory and handling payments. 

# Requirements

Edit 5 parameters in config/default.json.

    ```
    {
    "appSecret": "<Add your appSecret>",
    "pageAccessToken" : "<Add your pageAccessToken>",
    "validationToken": "<Add your validationToken>",
    "serverURL": "<Add your server URL(eg https://<example>.herokuapp.com)",
    "wayloKey": "<Add your waylo API KEY>"
    }
    ```
    
 If you have set up a few bots, create a FB app, page and head over to [Waylo Developer site](http://dev.thewaylo.com) and create your API key. You should be good to go. If not, you can follow the steps outlined here.
 
 You can see the API request [Here](https://github.com/waylo-api/HotelBot/blob/master/app.js#L348-375)
 
You would need node, npm and git installed to follow along.

## Get Started

### *Build the server*

1. Create an app on [heroku.com](https://www.heroku.com/) or your favorite server

    ![Heroku](http://nicelydone.club/wp-content/uploads/2016/08/nicelydone-heroku-create.png)
Take note of the server URL.

2. Create a new folder Hotelbot and clone this repo

    ```
    git clone https://github.com/waylo-api/HotelBot.git
    ```

3. Add heroku remote 

    ```
    git remote add heroku git@heroku.com:<project>.git
    ```

    where <project> is the name of your Heroku app in Step 1.

4. Install dependencies

    ```
    npm install
    ```
5. Add config parameters

   Edit config/default.json and add the following parameters

   ```
   "validationToken": "",
   "serverURL": "",
   ```

   Add any string as your validation token.
   "serverURL" is the server URL in Step 1. Leave others blank for now.

6. Commit all code to Heroku

    ```
    git add .
    git commit -am "first commit"
    git push heroku master    
    ``` 

### *Setup the Facebook App*

1. Create or configure a Facebook App here https://developers.facebook.com/apps/. Take note of the App Secret in the App Dashboard.

    ![App Dashboard](http://i.imgur.com/l5ly27B.jpg)

2. In the app go to Messenger tab (or add product and then add Messenger) and click Setup Webhook. Here you will put in the URL of your Heroku server(Typically https://<Heroku project>.herokuapp.com/webhook) and a token in Step 5 of *Build the server*. Make sure to check all the subscription fields.

3. [Create a Facebook Page](https://www.facebook.com/pages/create/)

4. Get a Page Access Token and save this somewhere. 

    ![Page Access Token](https://abhaykashyap.com/media/ckeditor/2016/11/30/fb_token_generation.png)
    
5. [Subscribe your page to the App](http://imgur.com/a/PPL5t). 

6. Add config parameters

   Edit config/default.json and add the following parameters

   ```
   "appSecret": ,
   "pageAccessToken" : ,
   ```

   "appSecret" is your FB App Secret in Step 1 of "Setup the Facebook App". "pageAccessToken" is the Page Access Token you noted in the previous step. 
    

### *Get Waylo Hotel API key*

1. First, sign up for a free account at [Waylo developer account](http://dev.thewaylo.com)

You'll need the Page Access Token in Step 4 of *Setup the Facebook App*

2. Note the API key and add config parameters

 Edit config/default.json and add the following parameters

   ```
   "wayloKey": <WAYLO API KEY>
   ```
3. Commit all changes to Heroku

    ```
    git add .
    git commit -am "Waylo API first commit"
    git push heroku master    
    ``` 
4. You should be all set. Open your Facebook page  and start chatting with your new hotel booking bot! Congrats you have just enabled bot monetization.


## License

See the LICENSE file in the root directory of this source tree. Feel free to use and modify the code.


#BAB - Build Awesome Bots
