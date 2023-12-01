# Installing Kubernetes

- `kubernetes` is designed to `manage` the `cluster of computer` which been running on `cloud`

- its been designed for the `ground up` and it takes a lot of `complecated responsibilty`

- we need to install `kubernetes` on the `single computer` when we are learning `kubernetes basics`

- even if we are `experienced on kubernetes` we need to install `kubernetes` locally 
  
  - maybe we are starting a `new development`
  
  - if we are woking on the `subsystem` of the `main system`
  
  - there are lot of scenario where we need to run `kubernetes locally`

- by far the best way of `running kubernetes` is by using the `using a specialized version of kubernetes which is a cut-down version of kubernetes` i.e `kubectl`

- it is `a version of kubernetes` where the `un-necessary feature been removed` , `Anything which is not required` for a `single machine installation` also been `removed`

- the `kubernetes` we will be running `in some form of a virtual machine`


- **kubectl**

- if we are going to the `kubernetes official docs` [official Docs](https://kubernetes.io/docs/tasks/tools/) the `first tool` we will looking in here known as `kubectl`
  
- `kubectl` is the `command line tool` that allow us to `run the command` against `kubernetes cluster`

- it does not matter a `cut down local version of kubertnetes cluster` or `massive production scale kubernetes cluster` , either way we have to use this tool called `kubectl`

- it is a `production ready standard tool` for `working with kubernetes`


- there are `3 more additional tools` , i.e `3 alternative tools` which will help in `running` `kubernetes locally`
  
  - `kind`
  
  - `minikube`
  
  - `kubeadm` 


- **Kind**
  
  - `kind` lets you `run Kubernetes` `on your local computer`
  
  - `This tool requires that you have either Docker or Podman installed and configure`


- **minikube**
  
  - Like `kind`, `minikube` is a `tool` that lets you `run Kubernetes locally`
  
  - `minikube` `runs` an `all-in-one or a multi-node local Kubernetes cluster` on your `personal computer` (including Windows, macOS and Linux PCs) so that you can `try out Kubernetes, or for daily development work`
  
  - it can be difficult to run 

- **Kubeadm**
  
  - `You can use the kubeadm tool to create and manage Kubernetes clusters`
  
  - `It performs the actions necessary to get a minimum viable, secure cluster up and running in a user friendly way.` 


# Running kubernetes locally

- there are `2 ways` that supported `for running kubernetes locally`
  
  - `Docker Desktop (prefered)`
    
    - for the last couple of version the `docker desktop` been ship with embeded `implementation of kubernetes` inside it
    
    - its very easy to `switch on` and `start with kubernetes` using the `docker desktop`
    
    - if we have the `Docker Desktop` then we have the `kubernetes` installed ,l we need to turn that on  
    
    - `docker basically is a linux tool` , but if we install `docker desktop on linux` then we can work on `kubernetes out of the box`
  
  <br/>
  
  - `minikube`

    - there might be `some reason that we are unable to run` the `docker desktop`
    
    - `docker desktop` is not a `open source free software` , if we are running the `enterprize` , the company have to pay for `docker desktop`
    
    - if not docker desktop , then we need to install `minikube` for the `backup choice`  
