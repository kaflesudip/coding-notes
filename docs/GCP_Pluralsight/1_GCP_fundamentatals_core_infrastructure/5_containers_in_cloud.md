# Containers in the cloud

## 1. Containers, Kubernetes and Kubernetes cloud

- IaaS lets you share resource.
  - each VM has own OS
  - flexibility but with cost.
- PaaS like App engine
  - access to services instead of VM
  - scales rapidly
  - but give up control of underlying server architecture
  - container come there (in between)
- Containers
  - OS and hardware as black box
  - Kubernetes helps to orchestrate many containers

## 2 Kubernetes and GKE

- Kubernetes cluster with gcloud
  - `gcloud container clusters create k1`
- Pod: smallest unit in kubernetes