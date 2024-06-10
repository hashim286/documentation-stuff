1. first check the current pihole instance is running <br/>`docker ps`
2. download latest image of pihole <br/>`docker pull pihole/pihole:latest`

3. Confirm the new image is on the device <br/>`docker image ls`

4. with new image on device, stop the old docker container <br/>`docker stop pihole`

5. remove the stopped container <br/>`docker rm pihole`

6. confirm container is gone <br/>`docker ps -a`

7. with container gone, remove the old image from the device<br/>`docker image ls` (copy image ID for pihole with tag of \<none>)<br/>`docker image rm (image ID)` 

8. rerun the pihole docker setup script located [here](https://github.com/pi-hole/docker-pi-hole/blob/master/examples/docker_run.sh)
