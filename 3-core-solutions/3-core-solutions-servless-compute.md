- [Core Solutions - Serverless Computing](#core-solutions---serverless-computing)
  - [Product options](#product-options)
    - [Azure Functions](#azure-functions)
    - [Azure Logic Apps](#azure-logic-apps)
  - [pricing](#pricing)
  - [Decisions](#decisions)
# Core Solutions - Serverless Computing

term
* env is setup and managed for you
* specify the f()  or connect/configure components,
* triggers
* implement code
* no worries about deployment
* no hosting, no vm
* Cloud vendor manages, runs as needed
* per for resources used
* scalability
* no outages

2 ways
* azure functions
  * event driven
  * servless code
  * variable demand
* azure logic apps
  * low / no code 
  * orchestrate apps
  * visual dev



pre-req
* understand orchestration and workflows
* API
* MS Products like Dynamics and Office 365

## Product options

### Azure Functions
* host single method or f()
* any popular prog lang
  * C#, python, javascript, typscript, java, powershell
* events
  * ex: HTTP req
  * new message on queue
  * timer
* scale automatically
* durable functions - 
  * allow devs to chain functions together
  * maintain state
    * rem: Manish used durable function to hold onto a database connection

More
* ex: Product purhcases -> JSON messages sent to event hub
* allows other systems to be notified
* hub subscribers get messages and process
* Easier to take imperative lang app and break it up into servless functions than to go to an Azure Logic App

### Azure Logic Apps
* low-code/no-code
* automate and orchestrate tasks, bus proc, workflows
* integrate apps, data, sys, svc across orgs
* in cloud, on-premises, hybrid
* EAT and B2B integ
* 200+ connectors
  * ex: salesforce, SAP, oracle db, file shares
  * build own

## pricing
|svc|metric 1|metric 2|
|---|-|-|
|f()|# executions|runtime|
|apps|# executions|# connectors|

## Decisions
* f()
  * custom algs
  * imperative lang
  * Developers usually
* Apps
  * orchestration across well-known APIs
  * pref: IT Pros and Business Analysts

