Private Virtual Server VPS
==========================

A set of steps to deploy a private virtual server in the heroku cloud v7.


Type the following commands : 
 
  ```
git clone https://github.com/0x77dev/docker-novnc  
cd docker-novnc-master
```

  Then update docker-compose.yml file and set PORT to "80:80"

   ```
nano docker-compose.yml
```

  After that deploy the dockerfile to Heroku

  
  ```
heroku create
heroku app:rename -app *** name  
heroku container:push web --app ****
heroku container:release web --app ****
heroku open --app ****
```

 When you open the project, you will find some links. So click on the vnc.html link.