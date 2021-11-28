React Template
==========================

A set of steps to deploy in the heroku cloud v7.

Unlike Spring Boot, in a React project you need a specific configuration.

Type the following commands : 
 
  ```
heroku login -i  
heroku create
```

  Then you need to create your project with react buildpack


  ```
 
heroku create name --buildpack mars/create-react-app
```

  Commit your project and add the heroku remote project, and push it.Thus, Heroku will build it.
  
  ```
git init
git add .
git commit -m "comm"
git git remote add heroku URL
git push heroku master
```
