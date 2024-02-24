To see the number of docker images : ```docker images```
TO run the docker file fromm a local directory 
````
docker run -d --volume 'path_from_local_directory':'path_to_mount_in_docker' docker_image_ID sleep infinity 
````
* -d : detach mode 
* --volume  : volume flag 
* sleep infinity : dwill run for infinity 

```
sample command : docker run -d --volume /home/tgadmin:workspace image sleep infinity 

```

Get the stauts of the container : ````docker ps````


Checking for docker :

````docker exec -it container_id sh````

Come out of a docker container 
````
ctl + p and then ctl + q
````

Docker provides a single command that will clean up any resources — images, containers, volumes, and networks — that are dangling (not associated with a container):
```
docker system prune
```
To additionally remove any stopped containers and all unused images (not just dangling images), add the -a flag to the command:
```
docker system prune -a
```
