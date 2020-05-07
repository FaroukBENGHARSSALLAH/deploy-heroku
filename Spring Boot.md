Spring Boot Template
==========================

A set of steps to deploy in the heroku cloud v7.

Unlike Spring MVC, in a spring boot you don't need a specific configuration.

Type the following commands : 
 
  ```
  
git create
```

  Then you will get the new Heroku app name, so rename it.


  ```
 
git app:rename -app *** name
```

  Commit your project and add the heroku remote project, and push it.Thus, Heroku will build it.
  
  ```
git init
git add .
git commit -m "comm"
git git remote add heroku URL
git push heroku master
```