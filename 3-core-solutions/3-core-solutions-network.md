- [3-core-solutions-network-connectivity](#3-core-solutions-network-connectivity)
  - [Goals](#goals)
  - [Defense in depth](#defense-in-depth)
    - [phys sec](#phys-sec)
    - [ident and access](#ident-and-access)
    - [perimeter](#perimeter)
    - [network](#network)
    - [compute](#compute)
    - [app](#app)
    - [data](#data)
  - [Security posture](#security-posture)
  - [Azure Firewall](#azure-firewall)
  - [DDoS prot](#ddos-prot)
  - [Network security groups](#network-security-groups)
    - [Props](#props)
  - [Combine azure svcs to create complete network sec sol](#combine-azure-svcs-to-create-complete-network-sec-sol)

# 3-core-solutions-network-connectivity

## Goals
* ident defense in depth strategy
* azure firewall - control traffic allowed on network
* config network sec gruops to filter network traffic to/from
* Explaine DDOS Prot

## Defense in depth
### phys sec
* 1st LOD
* protect hardware in data center
* access to buildings
### ident and access
* access to infra and change control
* SSO
* Audit events and changes
### perimeter
* uses DDoS prot to filter attaches before DDoS for users
* firewalls
### network
* limit comm between resources through seg and access control
* deny by default
### compute
* sec access to VMs
* endpoint prot
### app
* apps secure and free of sec vuln
* secrets storage
* security design
### data
* access to bus and cust data 

## Security posture
* confidentiality
  * least priv principle
* integrity
  * prevent unauth changes to info
    * at rest
    * in transit
* availability
  * DDoS


## Azure Firewall
* stateful
* high avail
* unrestricted cloud avail
* inbound / outbound filtering
* inbound dest network address trans (DNAT)
* azure monitor logging
* App rules
  * define FQDNs which can be accessed from subnet
  * define source addr, proto, dest port, dest address, 
  * NAT rules
* Azure app gateway - 
  * also provides firewall
  * web app firewall (WAF)
    * centralized inbound prot for web apps


## DDoS prot
* Standard tier 
* uses scale and elasticity 
* analyzed and discards DDoS trafic and azure network edge
* also helps manage cloud consumption
* tiers
  * basic
    * free
    * auto enabled
    * traffic monitoring and real-time mitigation comon network level attacks
    * protects azure infra
  * standard
    * prots also Azure Virtual Network resources
    * policies tuned through dedicated traffic mon and machine learning alg
    * applied to public IPs, assoc w resources in virt networks like azure load balancer and app gateway


Std tier can prevent
* volumetric attacks
* protocol attacks
  * l3 and l4
* resource layer (app layer) attacks
  * only w web app firewall
  * l7

## Network security groups
* filter network traffic to/from resources within azure virt network
* ~ internal firewall
* mult inbound and outbound sec rules

### Props
* name
* priority 100-4096
* src/dst ip or range, or tag, or app sec group
* protocol
* direction
* port range
* action

## Combine azure svcs to create complete network sec sol
* Secure perim
  * Azure DDoS
  * Perim firewall with azure firewall to ident and alert on malicious attacks on network
* sec network layer
* Combine
  * Network sec groups and firewall
  * app gateway web app firewall and azure firewall
    * WAF is feature of App Gateway
    * Azure firewall
      * Inbound non-HTTP/S (like RDP, SSH, FTP)
      * Outbound network level prot all ports and proto
      * app level prot for outbound https
  * 