# Cloud concepts

## Expanding set of services
* web svcs
* virtualized comps
* remote storage, database hosting, centralized account mgmt
* AI
* IOT

AZ-900 scoring
|Area|Percent|
|----|:-----:|
|Cloud Concepts|20-25|
|Azure core svcs|15-20|
|Core solutions and mgmt tools|10-15|
|general sec and network features|10-15|
|identity, governance, policy,compliance features|10-15|

## What is cloud computing?

Delivery of services over internet

Compute power
Storage

Backups
Software/OS up to date
Hardware maintained by cloud provider. 
Easy to upgrade to more memory, cpu, storage

## Why cheaper?
Pay as you go. Pay only for what you use.
* lower operating costs
* run infra more efficiently
* scale easily based on business needs

## Why move to cloud?
* faster delivery
* users expect richimmersive exp with their devices and sofwtare
* Nearly limitless pool of raw copute, storage, networking components
* speec recog, cog svcs, etc
* Analytics services deliver telemetry data from software and devs

## What is Azure

* SAAS
* PAAS
* IAAS

VMs running in cloud, databases, Machine learning, IOT, etc


blah blah
* build on your terms. open source, all langs and frameworks, how you want, where you want
* hybrid seamlessly. on-prem, cloud, at edge, . Integrate/manage all envs w tools ans svcs designed for hybrid 
* trust

Over 100 svcs
How does it work?

* private and public cloud platform
* Abstraction layer - Hypervisor
* Repeats abstraction in many regions, in mult data centers
* network switch provides connectivity between them. * * Fabric controller
* Orchestrator - reponsibility of coordining everything. via Web API and portal


## Azure portal
* build/manage/monitor everythin gfrom portal
* custom dashboards . org view of resources
* configure accessibility
* start/stop
* scale
* monitor
* track costs
* analyze peformance of apps
* create reports

## Azure Marketplace
8k plus listings
solution catalog

* VMs
* container platforms
* databases
* app build/deploy software
* etc

## Tour of services

10 main categories
1. Compute
2. networking
   1. connect cloud, on-prem infra
   2. vpns
   3. load balancing etc
3. Storage
   1. types: disk
      1. file
      2. blob
      3. archival
   2. scale in secure fashion
4. Mobile
   1. notifications
   2. xamarin
   3. cog services etc
5. databases
   1. cosmos db
   2. mysql
   3. postgresql more
6. web 
   1. build/deploy/manage/scale web apps
   2. geo spational context through maps
7. IOT
   1. management IOT assets
   2. sensor data analysis
   3. take action
8. Big data
   1. lg volumes of data
   2. run analytics at massive scale
9. AI 
   1.  use existing data to forecast 
   2.  machine learning - build/depoy
10. DevOps
    1.  people, process, tech
    2.  continuious delivery and deployment



### Compute
|Service name|function|
|------------|--------|
|VM|Windows or linux VMs hosted in azure|
|VM Scale Sets|scaling for Windows or Linux Vms hosted in azure|
|Kubernetes svc|cluster mgmt for VMs running containerized svcs|
|Service fabric|distrib sys platfgorm . runs in azure on-prem|
|Batch|Managed svc for parallel and high-perf comp apps|
|Container Instances|containerized apps run on azure w/o provisioning services or VMs|
|Functions|event-driven, serverless compute svc|

### Networking

|Service name|function|
|------------|--------|
|Virtual Network|Connect VMs to incoming VPN connections|
|Load balancer|balance inbound and outbound conn to apps or svc endpoints|
|App Gateway|Optimize app server farm delivery. Inc app sec|
|VPN Gateway|accesses azure virtual networks through high-perf VPN gateways|
|DNS|DNS high perf and high avail|
|CDN||
|DDoS protection|Protect Azure-hosted apps|
|Traffic Manager|distrib network traffic across regions|
|ExpressRoute|Azure over high-bandwidth dedicated secure conn|
|Network watcher|Monitor / dianose network issues by using scenario-bases analysis|
|Firewall|high sec, high avail, unlimited scale|
|Virtualn WAN|unified wide area network connect local and remote sites|

### Storage

|Service name|function|
|------------|--------|
|Blob|large objects, like video files or bitmaps|
|File|access/manage like file server|
|Queue|data store for queuing and reliably delivering msgs between apps|
|Table|non-relational, structured data (NOSQL). key/attribute store, schemaless|

Common characteristics
* durable
* secure
* managed
* accessible

## Mobile
mobile back-end svcs iOS, Android, windows
Sign-in, other resources
incl:
* offline data sync
* connectivity to on-prem data
* broadcasting push notifications
* autoscaling to match bu sneeds

### DBs
|Service name|function|
|------------|--------|
|CosmosDB|Global distrib DB, supports noSQL|
|SQL Database|Fully managed db, auto-scale, integral intell, robust sec|
|MySQL||
|PosgreSQL||
|SQL Server on Azure VMs|hosts enterprise SQL Server apps in cloud|
|Synapse Analytics|fully managed data warehouse. integral sec at every level of scale.|
|Database migration service|svc migrates dbs w no app code changes|
|Cache for Redis|fully managed. caches freq used and static data . reduce latency|
|Azure database for MariaDB|Fully managed. scalable MariaDB. high avail and sec|

### Web
|Service name|function|
|------------|--------|
|App svc|quickly create powerful cloud web-based apps|
|notification hubs|send push notif to any platform from any back-end|
|API Mgmt|Publish APIs to devs, partners, employees, securely, at scale|
|Cog search|deploy fully managed search as service|
|Web Apps feature of Azure App Service|create/deploy mission critical web apps at scale|
|SigalR Service|add real-time web f() easily|


### IoT
|Service name|function|
|------------|--------|
|IOT Central|Fully managed global IOT SAAS. connect, monitor, manage at scale|
|IoT Hub|msg hub. provides secure comm between and monitoring millions of IoT devices|
|IoT Edge|Fully managed. allows data analysis models to be pushed to Iot devices. Edge devices don't have to consult cloud-based AI models|

### Big Data
|Service name|function|
|------------|--------|
|Synapse analytics|massive scale. clouse-based enterprise data warehouse. massively parallel processing for complex queries. petabytes of data|
|HDInsight|Massive blah blah with managed Hadoop clusters|
|Databricks|Integrate collab Apache Spark-based analytics service with other big data services in azure|

### AI
|Service name|function|
|------------|--------|
|ML svc|cloud-based env. use to dev, train, test, deploy, manage , track ML models. Auto-gen model and auto-tune. Start on local machine, scale|
|ML Studio|Collab visually. prebuilt ML algorithms and data-handling modules|

closely related cog svcs
|Service name|function|
|------------|--------|
|Vision|ident captuion,index, moderate pics and videos|
|Speech|audio into text, use voice for verfication, speach recognition|
|Knowledge mapping|complex info and data mapping for ex intelligent recommeditations and semantic search|
|Big search|search API usage|
|NLP|allow apps to do NLP, eval sentiment, learn recog what users want|

### DevOps
|Service name|function|
|------------|--------|
|DevOps|use dev collab tools, high perf pipelines, free private git repos, kanban boards, automated/cloud based load testing, etc. aka VS Team Services|
|DevTest Labs|create on-demand win/linux envs to test or demo apps from deployment pipelines|

## accounts

* accounts
  * subscriptions
    * resource groups
      * resources
  