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

