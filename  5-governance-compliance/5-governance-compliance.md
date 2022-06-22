- [Azure Governance](#azure-governance)
  - [Azure role-based access control](#azure-role-based-access-control)
    - [Roles and Scopes](#roles-and-scopes)
    - [When to use](#when-to-use)
    - [How enforced](#how-enforced)
    - [Applies to](#applies-to)
    - [Access Control](#access-control)
  - [Resource locks](#resource-locks)
  - [Azure Blueprints](#azure-blueprints)
  - [Org Resources w Tags](#org-resources-w-tags)
  - [Azure Policy](#azure-policy)
    - [Policy Initiatives](#policy-initiatives)
  - [Azure Blueprints](#azure-blueprints-1)
  - [Cloud Adoption Framework](#cloud-adoption-framework)
    - [Create sub gov strategy](#create-sub-gov-strategy)

# Azure Governance 

## Azure role-based access control
* RBAC
* built-in roles for common access rules
* define own roles

### Roles and Scopes
* Roles
  * Reader
  * Resource specific
  * Custom
  * Contributor
  * Owner
    * Admins
* Scopes
  * Management group
  * subscription
  * resource group
  * Resource

### When to use
* one user to mng VMs in sub. Another to manage virt networks
* allow db admin group to manage sql dbs in sub
* allow user to manage all resources in a resource group
* allow app to access all resources in resource group

### How enforced
* any action iniatiated against resource going through Azure Resource Manager
* Resource Manager accessed through Portal, cloud shell, pwoershell, cli
* RBAC is allow model

### Applies to
* person or group
* other special identity
* Teams might align with a RBAC based resource group 

### Access Control
* permissions
* who has access to what scope and what roles apply

## Resource locks
* Prevent accidental deletes or changes
* access from po rtal, powershell, CLI, or ARM template
* add a lock to a resource
  * CanNotDelete
  * ReadyOnly
  * Combine w Azure Blueprints

## Azure Blueprints
* enables define set of std Azure resources org requires
* can enforce that a certain resource lock must exist

## Org Resources w Tags
* Resource management
* cost management and optimization
* Operations management
  * criticality and SLAs
* Security
  * pub
  * confidential etc
* Governance and reg compliance
  * ex: ISO 27001
* Workload optimization and automation
* access through
  * CLI
  * ARM templte
  * REST API
  * Azure Portal
* manage tags also by
  * azure policy


## Azure Policy
* define individual policies and groups of pol (initiatives)
* eval resources and shows which aren't compliant
* can prevent non-compliant resources
* built-in pol for
  * storage, networking, copute, security center, monitoring
* can remediate
* CI w azure devops and pipeline policies

In action
* create
* Assign def to resources
* Review and eval


### Policy Initiatives
* groups of policies
* ex: 
  * Enable Monitoring in Azure Security Center
    * monitor unecrypted SQL DB in Sec Center
    * Monitor OS vuln in Sec Center
    * monitor missing endpoint prot in Sec Center
* have a scope of a management group, sub, or resource group
* explore pre def policies
  * Policy -> Authoring -> definitions
  * Types:
    * SKU
    * Location


## Azure Blueprints
* Repeatable 
* Scales beyond sub
* Orchestrate deployment of 
  * Role Assignments
  * policy assignments
  * azur eresource manager templates
  * resource groups

## Cloud Adoption Framework
* Proven guidance on adoption
* create/impl bus and tech strategies

stages
1. Define strategy
   1. motivations
   2. bus outcomes
   3. eval fin considerations
   4. understand tech considerations
2. Make a plan
   1. digital estate
   2. initial org alignment
   3. skills readiness plan
   4. cloud adoption plan
3. Ready the org
   1. azure setup guide
   2. landing zone
   3. expand landing zone
   4. best practices
4. adopt the cloud
   1. migrate 1st workload
   2. migration scenarious
   3. best practices
   4. process improvements
   5. innovate
      1. bus val consenus
      2. azure innovation guide
      3. best practices
      4. feedback loops
5. Gov and manage cloud env
   1. gov
      1. Methodology
      2. Benchmark
      3. Init gov foundaiton
      4. improve init gov foundation
   2. manage
      1. estab mgmt baseline
      2. def bus commitments
      3. expand mgmt baseline
      4. advanced ops and design principles


### Create sub gov strategy
* Billing
  * ex: create 1 billing report per sub
  * ex: group based on department or project
* Resource tagging can help
* access control
  * sub is a deployment boundary for resources
  * each sub assoc w azure AD tenant
  * Tenant admins provide ability set granular access w RBAC
  * Design sub architecture. Consider deployment boundary factor
    * need separate sub for diff environments?
    * Sub limits?
      * ex: Azure ExpressRoute circutes - max 10 per sub