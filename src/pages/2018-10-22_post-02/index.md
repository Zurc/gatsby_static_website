---
path: "/post-02"
date: "2018-10-22"
title: "Node - Create a 'Break Time' alarm"
author: "Cruz JT"
---

![alt text](https://www.mpnpokertour.com/wp-content/uploads/2018/07/shutterstock_157027796-1000x675-1.jpg)


Hi everyone!

Welcome to another episode of Cruz's code journey.

Today I'll write about a very handy tool for when we are coding, all day seated on the same chair...

before creating a bottom pattern I'll encourage you to take a break and stand up periodically (every X amount of hours) with this useful NodeJS program that opens your browser with your favourite youtube song or whatever video you'd like.

##1. Install Node (and npm) on your machine

This could be easy doing by [dowloading node](https://nodejs.org/en/download/) and install it (plenty of tutorials on this).

When you download Node.js, you automatically get npm installed on your computer.

To check if you have Node.js installed, run this command in your terminal:

```
node -v
```

To check if you have npm installed, run this command in your terminal:

```
npm -v
```

##3. Open your code editor and create your folder

In my case I'm using Visual Studio Code, and I called my folder "node-alarm"

Navigate where you'll create your folder, you can create it from your terminal.

```
mkdir node-alarm
```

mkdir (make directory) followed by your folder name.

##4. Generate your package.json file

from your terminal you can create your package.json file by running...

```
npm init -y
```

This will create your package.json file with the default options. You can change that options at any moment.

##5. install node packages required

This time I'll use to **opn** node package to open a website on your browser

```
npm install opn
```

##6. create your app.js file

Here we'll request our **opn** package

**setInterval** belong to the timer global API (built-in Node), so you don't need to require it to use the API.

setInterval Schedules repeated execution of a callback function (we'll use an anonymous function) every X delay time (in milliseconds).

Inside our anonymous function we call opn method to open the browser with the specified url

That's all folks! this is our code for app.js file. 

Play around with the delayed time and insert whatever url you like. 

Happy coding!


```javascript
const opn = require('opn');

setInterval(() => {

  opn('https://www.youtube.com/watch?v=d-diB65scQU');

}, 2 * 60 * 60 * 1000)  // break every two hours

```

If you are interested you can grab/see the [code from github](https://github.com/Zurc/node-breaktime)
