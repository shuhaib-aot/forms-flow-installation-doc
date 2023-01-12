---
layout: default
title: Docker Full Deployment
nav_order: 2
parent : Docker based installation
---

## Docker Full Deployment
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}
### Installation Steps
\
Following steps are required to complete the installation and setup of formsflow.ai solution:  


1. Keycloak setup
2. forms-flow-analytics setup
3. forms-flow-forms ,forms-flow-web, forms-flow-bpm, forms-flow-api setup  


> *Make sure you have a Docker machine up and running*.  
{: .bg-grey-lt-000 .p-2}


###  Keycloak Setup.
  Keycloak is an open source software product to allow single sign-on with identity and access management aimed at modern applications and services.

  To install Keycloak follow the instructions given <a  href="/forms-flow-installation-doc/Pages/Docker_Based/SetUp/KeycloakSetup.html"  target="_blank" > here</a>.

###  forms-flow-analytics Setup.  
Redash is used to build analytics dashboards. The analytics server can be started by following the instructions given
 <a href="/forms-flow-installation-doc/Pages/Docker_Based/SetUp/Analytics.html" target="_blank" >here</a>.

###  forms-flow-forms, forms-flow-web, forms-flow-bpm, forms-flow-api & forms-flow-documents Setup. 
 
 To setup forms-flow-forms, forms-flow-web, forms-flow-bpm & forms-flow-api follow the below instructions .  
  - Make sure your current working directory `is /forms-flow-ai/deployment/docker` .  
  - Modify the environment variables inside the .env file if needed. Environment variables are given below.  

NOTE :{your-ip-address} given inside the .env file should be changed to your host system IP address. Please take special care to identify the correct IP address if your system has multiple network cards.
{: .fw-700 .ml-5    } 

 ![env var](../../assets//DockerFull/clientsecret.png)
 {: .ml-5}
 

 KEYCLOAK_BPM_CLIENT_SECRET provided in the **sample.env** is the default one.To generate new secret click 
 <a href="/forms-flow-installation-doc/Pages/Docker_Based/SetUp/Bpm.html#get-the-keycloak-bpm-client-secret" target="_blank" >here</a>.

![analytics var](../../assets//DockerFull/analytics%20var.png)
 {: .ml-5}

To get the redash API key click <a href="/forms-flow-installation-doc/Pages/Docker_Based/SetUp/Analytics.html#get-the-redash-api-key" target="_blank" >here</a>.

![analytics var](../../assets//DockerFull/variables2.png)
![analytics var](../../assets//DockerFull/variables3.png)
![analytics var](../../assets//DockerFull/variables4.png)
![analytics var](../../assets//DockerFull/variables5.png)
![analytics var](../../assets//DockerFull/variables6.png)
{: .ml-5}

### Running the application  
- Run `docker-compose up -d` to start.  

![analytics var](../../assets/DockerFull/dockerrunning.png)
{: .ml-5}

#### To stop the application
- Run `docker-compose stop` to stop.

### Health Check
- Analytics should be up and available for use at port defaulted to 7000 i.e. [http://localhost:7000/](http://localhost:7000/).
- Business Process Engine should be up and available for use at port defaulted to 8000 i.e. [http://localhost:8000/camunda/](http://localhost:7000/).
- FormIO should be up and available for use at port defaulted to 3001 i.e. [http://localhost:3001/](http://localhost:7000/).
- formsflow.ai Rest API should be up and available for use at port defaulted to 5000 i.e. [http://localhost:5000/checkpoint](http://localhost:5000/checkpoint).
- formsflow.ai web application should be up and available for use at port defaulted to 3000 i.e. [http://localhost:3000/](http://localhost:3000/).
- formsflow.ai documents API for use at port defaulted to 5006 i.e. [http://localhost:5006/checkpoint](http://localhost:5006/).
- Default user credentials are provided <a href="/forms-flow-installation-doc/Pages/Download_and_install/Download.html#formsflow-ai-user-credentials">here</a>.  

Installation is successfully completed now.

--- 


 [Prev](/forms-flow-installation-doc/Pages/Docker_Based/QuickInstallation.html){: .btn .float-left }
 [Next](/forms-flow-installation-doc/Pages/Docker_Based/IndividualService.html){: .btn .float-right }  
  
  
  *Copyright© [formsflow.ai](https://formsflow.ai/)*   
  {: .text-center .mt-8 .pt-8}
