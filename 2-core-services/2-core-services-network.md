- [Virtual Network](#virtual-network)
- [Creating a virt network](#creating-a-virt-network)
- [VPN Gateway](#vpn-gateway)
  - [Policy based](#policy-based)
  - [Route based](#route-based)
- [ExpresRoute](#expresroute)

## Virtual Network
enable cross over between on-prem and azure in cloud
allow resources to talk w each other

ex:
* VMs, web apps, databases


capabilities
* Isolation and segmentation
* internet comm
* between azure resources
* comm w on-prem resources
* route network traffic
* filter network traffic
* connect virtual networks

Whens setting up a virt network
* define private IP address , 
* specify public or private IP address ranges
* Public IP only accessible on the virt network
* Divide IP address space into subnets and allocate part to each defined subnet

DNS 
* Azure DNS for name resolution or external DNS server

An azure VM can connect to internet by default
Enable incoming connections by assign pub IP or place behind pub load balancer

mgmt
* CLI
* RDP
* Secure shell

comm between azure resources
* virt networks
* service endpoints
  * can link mult azure resources to virt networks - improve security and provide optimal routing

comm to on-prem
* Point-to-site VPN
* site-to-site VPN
* azure express route


route network traffic
* route tables
* border gateway protocol
  * works with azure VPN gateways , azure route server, or expressroute to propagate on-prem BGP routes to azure virtual networks

  connect virt networks
  * peering
  * can be in sep regions
  * user defined routes UDR - greater control over network traffic flow
  
  ## Creating a virt network
  Must specify
  * subscription
    * resource group
  * instance details
    * name
    * region
Also
* address space
* subnet name
* subnet(s)
* service endpoints 
  * ex: acure cosmos db, sb, key vault, ...
* NAT Gateway

Security
* Bastion host
  * disable/enable
* bastion name
* azure bastion subnet address
* public IP address
* DDoS protection std 
  * enable/disable
  * premium svc
* DDOS prot plan
* firewall
  * disable/enable
  * name
  * subnet address space
* public ip

Bastion Host let's you seamless RDP/SSH into the VMs directly in the azure portal over ssl


## VPN Gateway
Connect 2 or more trusted private networks

Uses
* on-prem data centers to virtual networks - site-to-site
* individual devices to virt networks - point-to-site
* virt entworks to virt networks - network-to-network

VPN type
* policy-based
* route-based

both use pre-shared key for auth
bothuse IKE v 1 or 2
IPSec
IKE = Internet key exchange

### Policy based
* IKE v1 only
* static routing
* source and test of tunneled networks specified
  * doesn't need to be specified in routing tables
* must be used in specific scenarious, like for compat with legacy on-prem VPN


### Route based
* modeled as an interface or virt tunnel interface
* IP routing (static or dynamic) decides which tunnel interface to use
* preferred conn method for on-prem devices

use route-based VPN gateway if
* conn between virt networks
* point-to-site
* multisite conn
* coexistence w azure express gateway

key features
* IKEv2 support
* any-t-any wildcard traffic selectores
* can use dyn routing protocols

gateway sizes
* basic recommended only for dev/test. Cannot be migrated
* based on SKU
* diff max number of tunnels (site-to-site)
  * 10 to 100
* agg througput
  * 100 Mbps -> 10 Gbps
* BGP support
  * basic no
  * all other yes

need: 
* virt network
* gateway subnet
* public ip
* local network gateway
* virt network gateway
* connection

for on-prem resources
* VPN device
* public facing IPv4 address

modes
* active/standby
  * disruption, but brief
* active/active 
  * uses BGP
* express ourte failover
* zone-redundant gateways

## ExpresRoute

modes
* from
  * any-to-any (IP VON) network
  * point to point
  * virtual cross connection

Don't go over public internet
faster

OSI
* Layer 2 - data link layer
  * node to node
* layer 3 - network layer
  * addressing, routing between nodes on multi-node network

add-on: 
* express route global reach
  * allow data from multiple customer owned data centers or sites to flow over the MS express route

connection
* Service Provider model
  * CloudExchange colo
  * Point to point ethernet connection
  * Any to any (IPVPN) connection
* direct
  * Express Route site