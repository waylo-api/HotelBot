# HotelBot built using the Waylo API

You can clone this repo to create your own hotel booking Facebook Messenger chatbot in less than 10 minutes. The hotel bookings are provided by [Waylo API](http://thewaylo.com/dev) and you earn a share of the revenue.

If you want to test out a HotelBot first, try [Waylo Bot](https://m.me/thewaylo)

# Build Your Hotel Booking Bot and Monetize

Creating this version will give you a Facebook Messenger chat bot. 

![Demo](http://i.imgur.com/I9MgSI8.gif)

## Get Started

### *Build the server*

1. Create an app on heroku.com or your favorite server

    ![Heroku](http://nicelydone.club/wp-content/uploads/2016/08/nicelydone-heroku-create.png)
Take note of the server URL.

2. Create a new folder Hotelbot and clone this repo

    ```
    sudo git clone https://github.com/waylo-api/HotelBot.git
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
    git commit --message "first commit"
    git push heroku master    
    ``` 

### *Setup the Facebook App*

1. Create or configure a Facebook App here https://developers.facebook.com/apps/. Take note of the App Secret.

2. In the app go to Messenger tab then click Setup Webhook. Here you will put in the URL of your Heroku server and a token in Step 5 of *Build the server*. Make sure to check all the subscription fields.

3. Create a Facebook Page and subscribe it to the App. 

4. Get a Page Access Token and save this somewhere. 

    ![Page Access Token](https://abhaykashyap.com/media/ckeditor/2016/11/30/fb_token_generation.png)

5. Add config parameters

   Edit config/default.json and add the following parameters

   ```
   "appSecret": ,
   "pageAccessToken" : ,
   ```

   "appSecret" is your FB App Secret in Step 1 of "Setup the Facebook App". "pageAccessToken" is the Page Access Token you noted in the previous step. 
    ```

### *Get Waylo Hotel API key*

1. First, sign up for a free account at [Waylo developer account](http://thewaylo.com/dev/register)

You'll need the Page Access Token in Step 4 of *Setup the Facebook App*

2. Note the API key and add config parameters

 Edit config/default.json and add the following parameters

   ```
   "wayloKey": <WAYLO API KEY>
   ```
3. Commit all changes to Heroku

    ```
    git add .
    git commit --message "first commit"
    git push heroku master    
    ``` 
4. You should be all set. Open your Facebook page  and start chatting with your new hotel booking bot! Remember you that earn on every hotel booking made through your bot.


## License

See the LICENSE file in the root directory of this source tree. Feel free to use and modify the code.


#BAB - Build Awesome Bots