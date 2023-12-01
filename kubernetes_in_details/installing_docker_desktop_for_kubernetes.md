# installing Docker Desktop for kubernetes

- `Docker Desktop` is a `commercial product` , its ok if we are the `single user or small organiazation` we can use `Docker Desktop` for `free`

- if we are `Big Organization` then you may need to `pay for the Docker Desktop` , we can check that `pricing section` of `docker.com`

- in this one we will `install the docker desktop` , in the next we will see `how to use kubernetes in docker desktop` 

- we can goto `Docker Desktop` by going to `https://docs.docker.com/desktop/install/ubuntu/` as below 

    
    ```bash
        sudo apt-get update
        sudo apt-get install ./docker-desktop-4.25.2-amd64.deb
        # we can launch the docker desktop by using the command as 
        systemctl --user start docker-desktop
        # we can also start the docker-desktop service as below 
        systemctl --user enable docker-desktop
        # this  will enable to the docker-desktop service in this case 

    ```

- we can then use the below command to validate that `docker-desktop` installed successfully

    ```bash
        
    
    
    
    
    
    ```

