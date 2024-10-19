1. first check the current instance is running <br/>`docker ps`
2. download latest image for the container <br/>`docker pull (image name):latest`
    - usually if you do a docker ps it will list the image name, to get the latest append the :latest tag on the end
      - e.g. for pihole the name is pihole/pihole:latest
3. confirm the new image is on the device <br/>`docker image ls`

4. with new image on device, stop the old docker container <br/>`docker stop (container prefix)`
   - usually this is the first part of the image name, if the image name is portainer/portainer-ce then you would run <br/> `docker stop portainer`

5. remove the stopped container <br/>`docker rm (container prefix)`

6. confirm container is gone <br/>`docker ps -a`

7. with container gone, remove the old image from the device<br/>`docker image ls` (copy image ID for pihole with tag of \<none>)<br/>`docker image rm (image ID)` 

8. if there is a setup script to run then rerun the setup script
9. if you run into problem where bind address is in use, then run following command to check what is using the ports<br/>`sudo netstat -tulpn | grep LISTEN` <br/> sometimes a process for the container will still be around even if the container is dead so you may need to kill the process with <br/> `sudo killall (process name or number)`
