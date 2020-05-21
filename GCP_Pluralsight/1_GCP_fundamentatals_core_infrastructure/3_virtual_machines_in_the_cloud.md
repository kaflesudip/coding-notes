# Virtual machines in the cloud

## 1. Introduction

- How google compute engine works

## 2. VPC Network:

- Virtual Private Cloud
- segment networks, use firewall rules
- VPC have global scope
  - can have subnets in any GCP region worldwide
  - Subnets can span zones that make up region
  - resouces in different zones in same subnet

## 3. Compute Engine

- virtual machine on Google infrastructures
- use console or gcloud command line tool
- pick memory, cpu and GPU if you want.
- 2 kinds of persistant disks
  - SSD
  - Standard
  - local SSD for scratch space
- Boot image: Linux or windows
- startup scripts
- durable snapshots of disk
- **Preemptible VM**: Compute engine given permission to terminate if resources needed somewhere else.
- **Autoscale** scale out



## 4. Important VPC capabilities

- VPC have routing capabilities like physical networks

- Buit-in routing table

- firewall to control what network traffic is allowed

  - e.g. create web server rule with web tag.

- **VPC belongs to GCP projects**

- pairing relation between two VPC

- also, shared VPC

- Google cloud CDN

  - CDN interconnect partner program

    

## 5 Demonstrate VPC in Qwiklab

