- [Core Solutions - Azure Architectural Components](#core-solutions---azure-architectural-components)
  - [buzzwords](#buzzwords)
  - [Structure / terms](#structure--terms)
    - [resources](#resources)
    - [Resource groups](#resource-groups)
    - [Subscriptions](#subscriptions)
    - [management groups](#management-groups)
  - [Regions/avail zones, pairs](#regionsavail-zones-pairs)
  - [Availability Zones](#availability-zones)
  - [Regional Pairs](#regional-pairs)
  - [Azure resource Groups](#azure-resource-groups)
    - [Logical groups](#logical-groups)
  - [Azure Resource Manager](#azure-resource-manager)
  - [Azure Subscription](#azure-subscription)
  - [Azure Management Groups](#azure-management-groups)

# Core Solutions - Azure Architectural Components

## buzzwords
* regions, region pairs, avail zones
* resources, groups, azure resource manager
* subscriptions and management groups

## Structure / terms

* management groups
  * subscriptions
    * resource groups
      * resources
        * ex: SQL Db


### resources
* instances of svc
  * vm, storage, SQL db etc
### Resource groups
* act as logical container for ex: web app, db, storage account etc
### Subscriptions
* groups together user accounts and resources
* limits or quotas
* manage costs and resources created by users/teams/projects
### management groups
* manage access, policy, compliance for mult subscriptiions
* all subs inherit conditions applied to mgmt group

## Regions/avail zones, pairs

* data centers around globe
* not exposed to users directly
* organized into regions
* region
  * geographical area 
  * one or more data centers
  * networked together
  * low latency
  * azure controls resources. balancing workloads
  * some svc or Vm features limited to certain regions
    * ex: VM sized or storage types
* some services not region specificd
  * AD
  * Traffic manager
  * DNS

why
* closer to users
* scalability
* redundancy
* data residency

special regions
* US DoD Central, US Gov Virginia, US Gov Iowa... 
* China East, China North, ... 

## Availability Zones
* within a region
* redundancy
* create duplicate hw env 
* high availability
* phys sep data centers within a region
* isolation boundary
* data centers connected w high speed, private fiber optic networks
* Apps
  * can use availabiity zones
  * mision critical and high avail
  * co-locating compute, storage, networking, data resources within zone
  * replicatin gin other zones
* Category
  * Zonal svc
    * VM
    * Managed disk
    * IP
  * zone redundant svc
    * ex: zone-redundant storage, SQL Db
  * non-regional svc

## Regional Pairs    
* Region pairs
  * Regions within same geo
  * at least 300 mi apart
  * prevents distruptions that could affect an entire region
    * ex: US West and US East

## Azure resource Groups
* logical container for resources
* resources can be moved between resource groups
* cannot be nested
* must exist before creating a resource
### Logical groups
* sim usage, type, or loc
* order and org to resources
* life cycle
* auth
  * scoped for applying role-based access (RBAC) perms
  * also admin and limit access to allow only what is needed


## Azure Resource Manager
* mgmt layer
* Create,Update, Delete resources in acct
* manage features like access control, locks, tags to secure and organize
* user request -> Azure tool/API/SDK -> Resource manager. 
  * Resource mgr authenticates req.
  * sends to azure svc
* Benefits
  * declarative templates instead of scripts
  * deploy, manage, monitor resources as a group
  * redeploy solution in consistent state
  * access control to all svc (RBAC)
  * apply tags
  * clartify org billing by group of resources w same tag

## Azure Subscription
* in some account
* subscription provides authenticate and authorized access to prod and svc
* allows provision resources
* logical grouping ex
  * dev
  * test
  * prod
* Billing boundary
* Access Control Boundary
* possible uses
  * Environments
  * Org structures
  * Billing
* Subscription limits
  * max # of expre route circuits is 10
* Customized billing
  * diff subs can be in diff invoice sections
  * multiple invoices within same billing account. w billing profiles
  * structure
    * Billing account
      * Billing profile
        * Invoice
        * Payment methods
        * Invoice Section
          * azure sub(s)

## Azure Management Groups
* level of scope above subscriptions
* can be used to manage access,policies, compliance for subs
* hierarchy of groups and subscriptions
* can create hierarchy which applies policy
* 10k mgmt groups supported in 1 dir
* six levels deep max
* at most 1 parent
* can have children
* a subs and mgmt groups are within single hierarchy in each dir