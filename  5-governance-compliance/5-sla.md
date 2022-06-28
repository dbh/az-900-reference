- [Azure SLAs](#azure-slas)
  - [Comparison](#comparison)
  - [Service Credits](#service-credits)
  - [Azure status page](#azure-status-page)
  - [Your homework](#your-homework)
    - [Define App SLA](#define-app-sla)
      - [Bus impact](#bus-impact)
      - [Usage patterns](#usage-patterns)
      - [Team decision?](#team-decision)
    - [Design app to meet your SLA](#design-app-to-meet-your-sla)
      - [Ident Workloads](#ident-workloads)
      - [Combine SLAs to compute composite SLA](#combine-slas-to-compute-composite-sla)
    - [Doesn't fit / meet needs?](#doesnt-fit--meet-needs)
      - [customize options](#customize-options)
    - [Build avail requirements into design](#build-avail-requirements-into-design)
    - [Include redundancy to increase avail](#include-redundancy-to-increase-avail)
    - [very high perf difficult to achieve](#very-high-perf-difficult-to-achieve)

# Azure SLAs


SLA ~ Uptime

## Comparison
99%, 1.68 hours / week, 7.2 hrs over a month
99.9%, 10 min per week, or ... 43 min per mo
99.95, 5 min, 21.6 min
99.99, 1.01 min, 4.32 min
99.999, 6 sec, 25.9 sec

## Service Credits
* fees paid are credited back if SLA not met
* subject to claim approval process
* request from CSP 

## Azure status page
* visit to see global view of Azure svc and regions

## Your homework
### Define App SLA
#### Bus impact
#### Usage patterns
#### Team decision?
### Design app to meet your SLA
#### Ident Workloads
#### Combine SLAs to compute composite SLA
* multiple percentage uptimes together
### Doesn't fit / meet needs?
#### customize options
* disks
  * HDD Std managed
  * SSD Std Managed
  * Premium SSD
  * Ultradisk
* tiers
  * free
  * std
  ### Build avail requirements into design
  ### Include redundancy to increase avail
  ### very high perf difficult to achieve