# Introduction and Understand AWS EKS Cluster

- `How EKS cluster going to work`

- What are the `core objects` of `EKS` cluster

- `More details` about the `core objects` of the `EKS cluster`

- `EKS Cluster` have 4 `core objects`
  
  - `EKS Control plane`
  
  - `Worker Nodes` and `Node Groups`
  
  - `Fargate Profile`
  
  - `VPC`   

- `EKS Control plane`:- 

    - `EKS control plane` is nothing but the `master node` in the `regular kubernetes architure`
    
    - which means it will host below inside the `EKS control plane`
      
      - `etcd`
      
      - `kube-apiserver`
      
      - `kube-controller`
      
    - in `regular kubernetes`  we need to maintain the `master node` , but when it comes to `cloud`  the entire `EKS control plane` managed by `AWS` 
    
    - so we don't have to bother about the `high avaiblability` of `etcd` , `kube-apiserver` , `kube-controller`
    
    - `whatever the object` present in the `master node` , all those objects will be managed by `AWS EKS control plane`
    
    - which is a `complete managed service by AWS` in case of `AWS EKS control plane`

    - `our responsibility ` `starts` with `provisioning the EKS cluster` and `Provisioning the worker node which is nothing but node groups`


- `Worker Nodes` and `Node Groups`
  
  - `worker node` is nothing but the `group of EC2 instance` where we want to run the `application workload`
  
  - we will `provision the EC2 instance here` and then we need to `deploy the kubernetes application` into those `EC2 instance`
  
  -   