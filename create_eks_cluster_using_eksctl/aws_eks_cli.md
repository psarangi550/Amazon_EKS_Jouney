# AWS EKS Cluster CLI

- there are `3 types` of `CLI` required for the `AWS EKS` cluster

- to manage the `application workload` over the `eks cluster` we need `3 type` of `CLI` to be installed 
  
  - `AWSCLI`
  
  - `kubectl`
  
  - `eksctl`
 

- `AWS CLI`
  
  - we can `control multiple AWS Service from the command line` and `automate them through Scripts` 
  
  - why we need the `AWS CLI` :-
    
    - for eks cluster
    
    - once we install the `AWS CLI` and `configure the security credetials` on the `local desktop` using the `AWS CLI`
    
    - then we can use the `kubectl` and `eksctl` we can `manage` `our cluster` and `cluster object` and `also application on kubernetes cluster`
    
    - for all this above , `AWS CLI` behave as the `underlying base` 


- `kubectl`
  
  - we can handle `kubernetes clusters` and `objects` using the `kubectl`
  
  - most of the time under this course we will doing everything with `kubectl`  


- `eksctl`
  
  - `eksctl` used for `creating` and `deleting` `cluster` on `AWS EKS` i.e `AWS Elastic Kubernetes Service`
  
  - `eksctl` is used for `managing the AWS Elastic Kubernetes Service Cluster ` 
  
  - we even have the `AWS Management Console` where we can perform 
    
    - creating the `EKS CLuster`
    
    - create the `Node Group`
    
    - crate the `control plane`  
  
  - `eksctl` is a better tool compare to the `AWS Management Console`    
  
  - we can also `create` , `autoscale` and `delete` `node group` using the `eksctl`
  
  - we can also create the `AWS Fargate Profile` using the `eksctl`
  
  - it is a `very powerful tool` for managing the `EKS cluster` on `AWS`


# Installing CLI for managing Elastic Kubernetes Service 

- we can goto [stacksimplify/aws-eks-kubernetes-masterclass Github](https://github.com/stacksimplify/aws-eks-kubernetes-masterclass) &rarr; `goto 01-01-Install-CLIs`

- we can go to the Reference-1: [AWS CLI Install](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html) in order to install the `AWS CLI`

- we can use the command as below for the same 

  
  
  ```bash
      curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" # downloading the AWS CLI ZIP in this case
      unzip awscliv2.zip # unziping the downloaded package in here
      sudo ./aws/install # installing the AWS CLi in here
 
  ```

- Verify the installation

  
  ```bash
      aws --version # which will show the AW CLi version in this case out in here 
      #here will be the output for the same 
      aws-cli/2.14.4 Python/3.11.6 Linux/6.2.0-37-generic exe/x86_64.ubuntu.22 prompt/off

      # WE CAN SEE WHERE THE aws cli LOCATED BY USING THE COMMAND AS 
      which aws
      # this will show the output as below 
      /usr/local/bin/aws
  
  ```

# Configure AWS Command Line using Security Credentials


  - Go to AWS Management Console --> Services --> IAM
  
  - Select the IAM User: pratik or create the user with appropriate security policy as Administrator Access
  
  - Important Note: Use only IAM user to generate Security Credentials. Never ever use Root User. (Highly not recommended)
    
  - Click on Security credentials tab
    
  - Click on Create access key
    
  - Copy Access ID and Secret access key
    
  -Go to command line and provide the required details

  - then we need to configure the `AWS CLI` as below 

  
    ```bash
        aws configure # this will configure the AWS CLI tool with the Access Key and Security Key 
        # which will display the below output for configuring the security credetials
        AWS Access Key ID [None]: ABCDEFGHIAZBERTUCNGG  (Replace your creds when prompted)
        AWS Secret Access Key [None]: uMe7fumK1IdDB094q2sGFhM5Bqt3HQRw3IHZzBDTm  (Replace your creds when prompted)
        Default region name [None]: us-east-1
        Default output format [None]: json
  
    ```

  - once configured we can validate that got `successfully configured` by using the below command as 

    
    ```bash
        aws ec2 describe-vpcs
        # which will show the default VPC info for the AWS 
        # we will be getyting the output as below in this case 
        {
        "Vpcs": [
            {
                "CidrBlock": "172.31.0.0/16",
                "DhcpOptionsId": "dopt-0b4ec680b0dc3c5b4",
                "State": "available",
                "VpcId": "vpc-08ac0f824179beb37",
                "OwnerId": "520668085636",
                "InstanceTenancy": "default",
                "CidrBlockAssociationSet": [
                    {
                        "AssociationId": "vpc-cidr-assoc-0316289a65472c668",
                        "CidrBlock": "172.31.0.0/16",
                        "CidrBlockState": {
                            "State": "associated"
                        }
                    }
                ],
                "IsDefault": true
            }
        ]
        }
    
    ```