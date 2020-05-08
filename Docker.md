Docker Template
==========================

A set of steps to deploy in the heroku cloud v7.

Unlike Spring MVC, in  Docker you don't need a specific configuration.

Type the following commands : 
 
  ```
heroku plugins:install heroku-container-registry
heroku container:login 
heroku create
```

  Then you will get the new Heroku app name, so rename it.


  ```
 
git app:rename -app *** name
```

  Add a Dockerfile and commit your project. Thus, Heroku will build the docker image in the remote container.
  
  ```
git init
git add .
git commit -m "comm"
heroku container:push web --app ****
heroku container:release web --app ****
heroku open --app ****
```