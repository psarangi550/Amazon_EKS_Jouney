# install Kubectl CLI

- `AWS` provide the `EKS Vendor kubectl binary`

- if we are using the `EKS Clusters` then we need to install the `AWS EKS Vendor kubectl binary` in order to avoid the issues

- based on the `kubernetes cluster version` we can install the `kubectl cli` after refering to [reference Docs](https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html)

- we can use the below command in order to install the `AWS EKS supported Kubectl` as
  
    
    
    ```bash
        mkdir kubectlbinary # creating the b inary mnamed as kubectlbinary
        cd kubectlbinary # moving to the kubectlbinary folder in here
        # here we are using the eks-1.28 for the version upgrade
        curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.28.3/2023-11-14/bin/linux/amd64/kubectl
        # Provide execute permissions
        chmod +x ./kubectl
        mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$PATH:$HOME/bin
        # creating the bin folder and copying the kubectl to the bin folder and add it to the PATH 
        echo 'export PATH=$PATH:$HOME/bin' >> ~/.bashrc
        # adding that to the bashrc file so that shell will be updated with it

    ```

- we can validate which version of `kubectl` been installed with respect to `EKS` we can see  as 

    
    ```bash
        kubectl version --client
        # this will provide the kubectl version in this case out here 
        Client Version: v1.28.3-eks-e71965b
        Kustomize Version: v5.0.4-0.20230601165947-6ce0bf390ce3
        # getting the eks version in this case out in here where we are checking for kubectl
    
    ```

