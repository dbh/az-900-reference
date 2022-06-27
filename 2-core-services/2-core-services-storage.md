
- [Types](#types)
- [tiers](#tiers)
- [Creating azure storage account](#creating-azure-storage-account)
- [Blob](#blob)
  - [Blob access tiers](#blob-access-tiers)
- [Disk storage fundamentals](#disk-storage-fundamentals)
- [Azure Files fundamentals](#azure-files-fundamentals)
# Types

* azure blob
  * massive amounts of unstructured data
  * audio, video
* file shared / storage 
* disk storage (for VMs and apps)
* azure data storage 
  * semi-structured
  * petabytes
* Queue storage
  * async messagging

SSD and conventional HDs for less 

# tiers
* hot
  * data accessed frequently
* cool
  * accessed every 30 days
  * slower access
* archive
  * long term backups
  * stored for at least 180 days

# Creating azure storage account

need
* subscription
  * resource group
* instance details
  * storage account name
  * location/region
  * performance 
    * std/premium
  * account kind
  * replication
  * blob acceess tier (hot or cool)


# Blob

hiearchy
* account
  * container
    * blob

example
|Account|Container|Bob|
|--|--|--|
|sally|pictures|img001.jpg|
|sally|pictures|img002.jpg|
|sally|movies|mov1.avi|

Points
* storage account provides unique namespace for your azure storage data
* accessible from anywhere 
* via HTTP or HTTPS
* secure, highly avail, durable, scalable

## Blob access tiers

* hot
* cool
* archive

|tier|account level|retention|latency|
|-|-|-|-|
|hot|y|indefinite|low|
|cool|y|>=30 days|med|
|archive|n|>=180 days|slow|

# Disk storage fundamentals
Used by VM or App
SSD or HDD

disks are IAAS

# Azure Files fundamentals

Available via 
* SMB
* NFS (preview)

Can be mounted on
* Win
* Linux 
* macos

Points
* any number of apps,VMs, roles can access the same Azure files simutaneously
* many on-prem apps use file shares. easy migration to azure
* Store config files on a file share and access from multi vms
* write data to file share, process, analyze data later

