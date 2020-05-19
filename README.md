deploy-heroku
==========================

This folder contains Heroku cloud deployment steps.

The day i haved started using Github, i thinked about publishing my appications in an online cloud, that the application can be accessible from the network via an URL. 

Thus, i deciede to write this tutrial to describe Heroku, which i have found, the most awsome and easy cloud. Your project will be hosted in a heroku Dyno.

Cloud Dyno Hardware Specifications
- [x] Available processors (cores): 8 
- [x] Free memory (Mb): 213.773 
- [x] Maximum memory (Mb): 267.0 
- [x] Total memory available to JVM (Mb): 232.0 
- [x] Name of the OS: Linux 
- [x] Version of the OS: 4.4.0-1062-aws 
- [x] Architecture of THe OS: amd64 
- [x] Total space (Mb): 2298.25 
- [x] Free space (Mb): 1788.629 
- [x] Usable space (Mb): 1764.629


![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/0/06/Heroku_suporte.png/800px-Heroku_suporte.png?uselang=en-gb "supported languages")



  
  
  
  What You need
- [x] Heroku account
- [x] Heroku CLI

For Java projects, you need a Heroku account and [Heroku CLI installed](https://devcenter.heroku.com/articles/heroku-cli). 
  
Heroku version <= 6

  Type this commande to install your war deployer API 
  
  ``
    heroku plugins:install java
   ``
   
 
 Imagine that you have a remote project called 'project', to deploy a war file, type
 
   ``
     heroku war:deploy war_file --app project
     ``
     
Heroku version >= 7

Imagine that you have a remote project called 'project'. Note that you should prepare two files according to the project nature; Spring MVC, Spring Boot, Python, NodeJS, etc. In this example, you find a file related to Spring MVC, Boot templates.

 To deploy the project in the heroku cloud, type
 
 
  ``
  
      git init
      
      heroku git:remote -a project
      
      git add .
      
      git commit -am "initial commit"
      
      git push heroku master
      
      heroku git:remote -a project
     ``


