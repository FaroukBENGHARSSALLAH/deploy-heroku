Angular Template
==========================

A set of steps to deploy in the heroku cloud v7.

In an angular project you have a specific configuration. But, you have to use the latest nodeJS and Angular cli version

To begin, create a server.js file in root folderfile with the following content : 

  ```
function requireHTTPS(req, res, next) {
    // The 'x-forwarded-proto' check is for Heroku
    if (!req.secure && req.get('x-forwarded-proto') !== 'https') {
        return res.redirect('https://' + req.get('host') + req.url);
    }
    next();
}

const express = require('express');
const path = require('path');
const app = express();

app.use(requireHTTPS);
// built in middleware to serve static content just as images, css, html etc
app.use(express.static(path.join(__dirname, 'dist')));

app.get('/*', async (req, res) => {
    res.sendFile(path.resolve(__dirname, 'dist', 'index.html'));
});

app.listen(process.env.PORT || 8080);
```

Then modify the scripts parts in package.json file : 

  ```
"scripts": {
    "ng": "ng",
    "start": "node server.js",
    "build": "ng build",
    "test": "ng test",
    "lint": "ng lint",
    "e2e": "ng e2e"
```

And continue with the same usual commands : 
 
  ```
heroku login -i  
heroku create
```

  Then you will get the new Heroku app name, so rename it.


  ```
 
heroku app:rename -app *** name
```

  Commit your project and add the heroku remote project, and push it.Thus, Heroku will build it.
  
  ```
git init
git add .
git commit -m "comm"
git git remote add heroku URL
git push heroku master
```
