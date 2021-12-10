# Simple-NodeJS-Server
This is a tutorial that shows how to create a simple NodeJS Server.

In this tutorial, you will learn how to create a simple server with node.js. Bellow is a brief definition of a Server and NodeJS.

**Server** is a computer program or device that provides a service to another computer program and its user, also known as the client.

**NodeJS** is simply an open source, cross-platform runtime environment that runs on a V8 engine for developing server-side, networking applications thereby allowing JavaScript to run outside the web.

The following technology will be used in the cause of this tutorial.
1. JavaScript (An object oriented programming language)
2. Node.js (A runtime environment)
3. VSCode (An Integrated Development Environment-IDE)
4. POSTMAN (A application to run our request)

Let's get started. 

## Initiating Node.js
To create a server on node.js, you must first launch the IDE of your choice (VSCode in my case), then you will need to run the command below:

```
npm init --y
```
**npm** is a short for Node Package Manager which helps to install node packages. Some packages will be installed as soon as you hit the enter key after entering the above command. see sample below.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/fyfuireynbm13hgl3l6s.PNG)

Now that we have successfully set up our node environment, the next thing is to create a server on this environment. 

## Creating a server
Create a new file and name it server.js at the left pane(Explorer) of VSCode. If all is done as directed, you will have a replica of the below sample image. 

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6bxp1fv81auw5qustb5r.PNG)

now that we have the server.js file created it does nothing because it is currently an empty file. Let dive in to the code base bellow.

First we install a package called "express" with the command 

```
npm i express.
```
OOPS!!! just remembered i haven't gave a brief on what express is. **Express** is a back end web application framework for Node.js.

```
const express = require('express');
const port = 2021;

const app = express();
app.get('/', (req, res) => {
    res.send('A Simple Node.js Server is Up and Running.......')
})
app.listen(port, ()=>{
    console.log(`Server is listening on port ${port}`)
});
```

First we imported the express module. After importing express, we set a port at which our server will run on, next created an instance of the express module imported. The essence of creating that instance is to help us utilize everything express has to offer us(say its functions).

We use the instance app created to fire our first request(GET METHOD) so as to look for a route that matches "/", after which a response follows up rendering the required content to our client/browser using the `res.send()` method.

Now that we have all our lines of code, we are left with running this application so as to completely confirm that our server is really up and running.

## Running the server
To run our server, we need to first lunch a terminal by clicking on the terminal option at the menu or use a shortcut (ctrl + j) then  enter the command below inside the terminal:

```
node server.js
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/yx8jl4xc3ow54v9u5ow7.PNG)

Once this is done, we would see a message on the terminal showing that our server is up running on port 2021 but the content of the response isn't displayed. This is because we only ran our server but haven't sent a request so if we are to see the response, we need to use either a Browser, POSTMAN or Thunder Client(an extension provided by VSCode) to send a request that is based on the endpoint created which is "/" in our case.

## Sending a request

- Lunch POSTMAN
- Enter this URL in the URL address bar: `http://localhost:2021/`
- Change the request method to GET
- Click on the SEND button.

This sample image shows that all is done and dusted as our server is running and our first response was gotten.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/1emop3pwubieju3y7e1l.PNG)

You can get my articles <a href="https://dev.to/callmefarad"> here </a>

Trust you've learnt how to create a simple server with node.js.

# From Installation to Running the Application
The complete process from installation to running the application can be found <a href="https://dev.to/callmefarad/simple-nodejs-server-1ee6">here </a>.</br>
Thanks for reading.</br>
See you!!!!
