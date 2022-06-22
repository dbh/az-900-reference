- [Azure Security - Azure Security Center](#azure-security---azure-security-center)
  - [Security Center](#security-center)
    - [Secure score](#secure-score)
    - [Protect against threats](#protect-against-threats)
    - [Respond to sec alerts](#respond-to-sec-alerts)
  - [Azure Sentinel](#azure-sentinel)
    - [Connect data sources](#connect-data-sources)
    - [Detect threats](#detect-threats)
    - [Investigate / respond](#investigate--respond)
    - [Azure Monitor Workbooks](#azure-monitor-workbooks)
  - [Key Vault](#key-vault)
    - [Access via](#access-via)
# Azure Security - Azure Security Center

## Security Center
* monitor sec settings
* auto apply required sec settings to new resources
* sec recommentations
* monitor 
* ML to detect/block malware on VMs and resources
* adaptive app controls
* detect / analyze inbound attacks. post-greach activity analysis
* JIT controls

### Secure score
* measurement of org sec's posture
* based on sec controls, groups of rel sec recommentations etc

### Protect against threats
* JIT VM access
* adaptive app controls
* adaptive network hardening
* file integrity monitoring

### Respond to sec alerts
* centralized view of sec alerts
* dismiss false
* remediate alerts manual
* automated responses w workflow auto

## Azure Sentinel

* SIEM - security Info and Event Management
* agg sec data via logging 
* capability for threat detection and response
* capas
  * Collect cloud data at scale
  * Detect prev undtected threats
  * investgiate threats w AI
  * Respond to incidents rapidly

### Connect data sources
* MS Solutions connectors
  * MS Threat Prot
  * MS 365, azure AD, WIndows Defender FW
* other services and solutions
  * AWS CloudTrail, Citrix Analytics, Sophos, VMWare stuff, Okta SSO etc
* industry standard data sources
  * Common event format (CEF)
  * syslog
  * REST APi

### Detect threats
* built in analytics
* custom analytics



### Investigate / respond
* Azure Sential detects events
* investigation graph
* help w investigation

### Azure Monitor Workbooks
* Automate responses
* on some alert triggered.... 
  * open ticket
  * send message
  * send all info, etc , to network admin etc
  * block / ignore

## Key Vault
* Centralized cloud service
* store app keys
* manage secrets, encryption keys, certs, etc
* hardware sec modules (HSMs). 
* secure by 
  * software 
  * or FIPS 140-2 Level 2 validated HSMs
* access monitoring and control
* simplify admin
* integ with other azure svcs

### Access via 
* portal
* CLI
* Powershell
* 