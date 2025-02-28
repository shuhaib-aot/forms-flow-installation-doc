---
layout: default
title: Download and Installation
nav_order: 2
---

# Download and Installation
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}
----
In the following document, we’ll describe the different project dependencies and the installation options being supported.

## Prerequisites
 - Admin access to a local or remote server (can be local Windows PC or Mac provided it is 64-bit with at least 16GB RAM and 25GB HDD).
 - For Docker-based installation [Docker](https://www.docker.com/) (supports Docker version above 4.0.0) needs to be installed
 - For Mac, make sure the [docker for mac](https://docs.docker.com/desktop/install/mac-install/) memory allocation is set to at least 16GB.

## Download formsflow.ai
 To download and set up, follow the installation guide, where you will find step-by-step instructions to download and install.  
 Clone this github repo: [https://github.com/AOT-Technologies/forms-flow-ai](https://github.com/AOT-Technologies/forms-flow-ai).



Folder structure will look like below:
![Download installation](../../assets/downloadandinstall.png)


### Project Dependencies
- [Keycloak](https://www.keycloak.org/) (included under ../.forms-flow-idm/keycloak).
- [Form.io](https://www.form.io/opensource) (included under ../.forms-flow-forms).
- [Camunda](https://camunda.com/) (included under ../.forms-flow-bpm).
- [Redash](https://redash.io/) (included under ../.forms-flow-analytics).
- [Python](https://www.python.org/) (included under ../.forms-flow-api).
- Optional: nginx (included under ./deployment/nginx).  

## Formsflow-ai user credentials  


Default User credentials are generated when keycloak started for the first time, you can modify the values on your keycloak service.   

| User Role    | User Name            | Password | User Group         |
|:-------------|:------------------   |:------   |:---------------    |
| Designer     | formsflow-designer   | changeme | formsflow-designer |
| client       | formsflow-client     | changeme | formsflow-client   |
| Reviewer     | formsflow-reviewer   | changeme | formsflow-reviewer |
| Clerk        | formsflow-clerk      | changeme | formsflow-reviewer |
| Approver     | formsflow-approver   | changeme | formsflow-reviewer |  



> NOTE: All the default configurations are imported to keycloak during the startup, so no manual changes are required at this stage. Redirect uri's are configured as localhost in the default setup, you can configure the ip address (if required) as the redirect uri for the clients by logging into Keycloak.
{: .fw-700    } 

---

  *Copyright© [formsflow.ai](https://formsflow.ai/)*   
  {: .text-center .mt-8}