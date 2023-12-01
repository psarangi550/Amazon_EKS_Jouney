# Installing eksctl CLI

- For windows and linux OS, you can refer below documentation link.
    
- Reference: [eksctl CLI](https://docs.aws.amazon.com/eks/latest/userguide/eksctl.html#installing-eksctl)

- we can refer the link as [eksctl.io](https://eksctl.io/installation/) with below steps

    
    
    ```bash
        # forchecking the Archirecture we can use the command as 
        uname -m
        # the output can be AMD64 (x86_64) or ARM64 (aarch64)
        #based on that we can perform the below steps in here 
        # for ARM systems, set ARCH to: `arm64`, `armv6` or `armv7`
        ARCH=amd64
        PLATFORM=$(uname -s)_$ARCH

        curl -sLO "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$PLATFORM.tar.gz"

        # (Optional) Verify checksum
        curl -sL "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_checksums.txt" | grep $PLATFORM | sha256sum --check

        tar -xzf eksctl_$PLATFORM.tar.gz -C /tmp && rm eksctl_$PLATFORM.tar.gz

        sudo mv /tmp/eksctl /usr/local/bin

    ```


- we can validate the `eksctl version` that being installed using the command as 

    
    ```bash
        eksctl version
        # this will show the eksctl version in this case 
        0.165.0 # which is 0.165.0 for this case
    
    ```