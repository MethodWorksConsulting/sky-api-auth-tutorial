# Blackbaud SKY API Authorization Code Flow Tutorial

Blackbaud SKY API Authroization Code Flow demo application.

## About

The Blackbaud SKY API currently supports the [Authorization Code Flow](https://apidocs.nxt.blackbaud-dev.com/docs/authorization/), which requires us to have a back-end server component where we're able to securely store the client secret.  For this code sample, we've implemented the server component using NodeJS.  

Feel free to leave feedback by filing an issue.

Be sure to read the associated [Auth Code Flow Tutorial](https://apidocs.nxt.blackbaud-dev.com/docs/authorization/auth-code-flow/tutorial/) within our documentation. 

## Run this app on your server

To run this application in your environment, you will need to complete the following steps:

### Prerequisites

0. A server, such as your local machine, capable of running [NodeJS](https://nodejs.org/en/).
0. A reliable internet connection for cloning the repo and installing this project's dependencies.
0. [Register your application](https://developer.nxt.blackbaud-dev.com/comingsoon) in order to obtain the **Application ID** (client id) and **Application secret** (client secret).  If you plan on running this sample on your local machine, be sure to supply a **Redirect URI** of `https://localhost:5000/auth/callback`.
0. [Signup (for free)](https://developer.nxt.blackbaud-dev.com/) for the Blackbaud SKY API developer program in order to obtain your **Subscription key**.  The subscription key represents an approved subscription to a specific Blackbaud SKY API product and is associated with your developer account. You can view your subscription keys within your [profile](https://developer.nxt.blackbaud-dev.com/developer). 
0. We assume you know how to clone a repo and use a command line interface (CLI) such as Terminal or the Windows Command Prompt.  

### Setup

Be sure to read the associated [Auth Code Flow Tutorial](https://apidocs.nxt.blackbaud-dev.com/docs/authorization/auth-code-flow/tutorial/) within our documentation. 

0. Fork or clone this repository.
0. Prepare environment:
  0. Copy the environment file named `.env.sample` as `.env`.
  0. Review the `.gitignore` file which specifies untracked files to ignore within git.  Note how the `.env` file is ignored. This prevents your registered application's keys from being exposed to everyone else on GitHub. 
  0. Update the `.env` file with the following values.
    * AUTH_CLIENT_ID = Your registered application's **Application ID**.  See [Managing your apps](https://apidocs.nxt.blackbaud-dev.com/docs/apps/).
    * AUTH_CLIENT_SECRET = Your registered application's **Application secret**.
    * AUTH_SUBSCRIPTION_KEY = Provide your **Subscription key**.  Use either the **primary key** or **secondary key**.  See your [profile](https://developer.nxt.blackbaud-dev.com/developer).
    * AUTH_REDIRECT_URI = One of your registered application's **Redirect URIs**. As you try out this sample locally, you will want to use something like `https://localhost:5000/auth/callback`.  See [Managing your apps](https://apidocs.nxt.blackbaud-dev.com/docs/apps/).

0. On your local machine:  
  0. Change to the working directory: `cd sky-api-auth-tutorial`.
  0. Run `npm install`.  **npm** is the package manager for **nodejs**.  `npm install` installs all modules that are listed within the **package.json** file and their dependencies into the local **node_modules** directory.  
  0. Run `source .env` to load the environment variables into your node app. 
  0. Run `node index.js` to start the app on localhost port 5000. 
  0. Open your browser to [https://localhost:5000/](https://localhost:5000/).
  
  ### TO DO
  
  Describe how to use app.  Currently its https://localhost:5000/auth/login to get token and https://localhost:5000/api/constituents/280 to pull down a constituent.