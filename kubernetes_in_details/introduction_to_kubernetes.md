# Introduction to Kubernetes orchestrations

- `container` are the `becoming popular` to `deploying system` , by far the `most popular` one is of `docker`

- we can deploy `individual part of the system`  as `containers` and assure some `gurantee` that ` those docker container` will run `in an identical environment`

- but if we are deploying `nontrivial system` such as `microservice architecture` then we might have the `problem` that we have a lot of `docker container` to manage

- lets suppose we have `10 docker container` to `manage` , which will be a `pretty small deployment`

- managing the `system with 10 container` can be `very difficult` , whatif the `container crashes`

- if the `system administrator` can watch `terminal` in order to `deploy the restart the container` when the `container crashes`

- but thats not good `if the container` fails on `3AM` and angry customer will `msg` regarding the `failure` for `help`

- google running in the region `2 billion container` in a `single week` , we can't manage `those number of container` manually 

- Eventhough we are managing the `small microservice` with `5/6 container` we need `some type of automation help` in order to `manage the containers`

- thats where the `orchestration` term comes in 

# What is Orchestration 

- `Orchestration` is the generally means `some type of automated service` for `arrangement, coordination and management of computer system and middleware and service`

- here we are talking about the `orchestration system` for `container` whether we have the `6 contains` or `6 billion container` , we need the `automatic management` for the same

- in an `orchestration system` we will be defining the `series of text file` known as `manifests`

- the `manifests` will going to capture `our entire system architecture`

  - it will allow us to `describe` what `containers` we will be running 
  
  - it will also describe `what infrastructure we will be running` such as `hard-disk or node`
  
  - it also allow us to make the system robust such as `there is always one or more instances of the container` that will be `running` at `any particular time`
  
  - Even incase of `catastrophy` which means `contains been crashed` , the `orchestration` system will be responsible to `restoring the system back` to `healthy state` without any ` manual interventation` from `administrator`
  
  - here we will be working on `cloud` which bring `its own complecation` such as 
    
  - we need things like 
    
    - external harddrive
    
    - load-balancer
    
    - security configuration
    
  - this all can be handled by `manifests` file in the `orchestration`    
  
  - we will be taking the `manifests` file `we have developed locally` and `transfering` them `onto the cloud`
  
  - we can `run the orchestration` in `any cloud` such as `AWS/Azure/GCP/Bare Metal Local env`
  


- kubernetes is one `example` of the `container` orchestration tool , which is most popular `container orchestration tool` 

- its been originated from `google` , manage the `multi billion container deployment`

- `kubernetes` now being `independent of google` and being managed by `cloud native computing foundation` organization


# Differencce Bettween Docker Swarm and Kubernetes 

- `Docker Swarm` is the `built-in` container orchestration system

- we dn't have to do `anything special` in order to install the `Docker Swarm` , it just comes integrated with `Docker Engine`

- **Why to use Kubernetes instead of Docker Swarm**
  
  - the `Advantage` of `Docker Swarm` is `built-in` with the `docker engine`
  
  - `Docker Swarm` is a little-bit simpler as compared to `kubernetes`  , `kubernetes` learning curve is a bit `steep`
  
  - on the `other side` kubernetes is `more richer` than the `docker-swarm` , we can do a `lot` in `kubernetes`
  
  - we can take the `manifests` and `deploy` them to `different cloud providers` such as `Amazon/Azure/GCP` , `kubernetes can configure those environments`
  
  - we can `abstracting away` the `low level details` for the `underlying cloud platform`
  
  - we don't have to `start any image` , we can just `run the scripts` and all the `load balancer` , `hard-disk` and `instances` will be `automatically be created`
  
  - we need to perform  a lot of `manual setup in cloud` in order to `run the orchestration using docker swarm`
  

# Setup Required 

- we need to `setup` the `manifest` locally , we need the `local version of kubernetes` which is called `minikube`

- installing `minikube` can be `very difficult` hence we will address that in the coming lectures
-  