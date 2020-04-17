deploy-heroku
==========================

This folder contains Heroku cloud deployment steps.

The day i haved started using Github, i thinked about publishing my appications in an online cloud, that the application can be accessible from the network via an URL. 

Thus, i deciede to write this tutrial to describe Heroku, which i have found, the most awsome and easy cloud. 


![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/0/06/Heroku_suporte.png/800px-Heroku_suporte.png?uselang=en-gb "supported languages")

  For Java projects, you need a Heroku account and [Heroku CLI installed](https://devcenter.heroku.com/articles/heroku-cli). 
  
Heroku version <= 6

  Type this commande to install your war deployer API 
  
  ``
    heroku plugins:install java
   ``
   
 
 To deploy a war file, type
 
   ``
     heroku war:deploy war_file --app app_name
     ``
     
Heroku version >= 7

Imagine that you have a remote project called 'project'. Note that you should prepare two files according to the project nature; Spring MVC, Spring Boot, Python, NodeJS, etc. In this example, you find a file related to Spring MVC template.

 To deploy the project in the heroku cloud, type
 
 
  ``
      git init
      heroku git:remote -a project

      git add .
      git commit -am "initial commit"
      git push heroku master

      heroku git:remote -a project
     ``


