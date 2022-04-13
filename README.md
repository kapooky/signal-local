On-Premise/local Signal-Server(v2.92) Installation (Work in Progress)
=================

#### Alert: This project has been deprecated. You will be required to manually agree to the Oracle Licensing Agreement when you build the Android APK. While such a task can be automated, it opens the door for legal consequences. 

Documentation
-------------
As of this moment, The Signal Foundation does not provide an official guide to build and deploy their server. This has unfortunately left many people to turn to unofficial guides, which tend to have their own problems such as being outdated and hard to follow. 

My goal of this project is to reduce the learning curve required to build and run the server by making it very easy to deploy. T

To make it easy to deploy, I will be required to remove out most of the cloud dependencies so the user won't have to sign up to these services. 



Automation
------------
Docker-compose will be used to automate the provisioning and orchestration of containers. You can scale each service(voicecall/video) individually by adding more containers to that respective service. 
Load balancing of containers can be accomplished using NGINX. For more information, check out the docker-compose directory. 

---------------------

Faq
------------
Why did I use v2.92?
The current version of Signal is v7.6. 

A: 2.92, to my knowledge, is the only signal-server that can be succesfully run AND where CDS(Content Discovery Service) is optional. CDS requires special hardware computer processors for confidental computing. 

Problems:
----------
A list of problems that I need to sort out: 

- APN (Apple Push Notifications) requires a yearly membership of $120. Remove APN? 
- Remove Google Recaptcha?
- NginX load balance video/call servers 
- Run the server on localhost? or on a domain?

Progress
-------------
- 70% finished building and running signal-server
- 70% docker-compose file 
