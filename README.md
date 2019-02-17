deploy-heroku
==========================

This folder contains Heroku cloud deployment steps.

The day i haved started using Github, i thinked aboout publishing my appications in an online cloud, that the application can be accessible from the network via an URL. 

Thus, i deciede to write this tutrial to relate my experince using Heroku, which i have found, the most awsome and easy cloud. 

![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/0/06/Heroku_suporte.png/800px-Heroku_suporte.png?uselang=en-gb "supported languages")

  For Java projects, you need a Heroku account and Heroku CLI installed.

  Type this commande to install your war deployer API 
  ``
    heroku plugins:install java
   ``
 
 To deploy a war file, type
 
   ``
     heroku war:deploy war_file --app app_name
     ``
