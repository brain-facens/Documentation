# DOCKER DOCUMENTATION (BRAIN FACENS)
<br>

------------------------------------------

<br>

## **INSTALL DOCKER IMAGE LOCALLY**
### Load the Image:
```
$ sudo docker load -i {Name_file_image.tar}
```

### Verify the images in docker:
```
$ sudo docker images
```

### Command to video setup be able to containers:
```
$ xhost +si:localuser:root
```
<br>

- OBS: You can add the command above to .bashrc, because it must be executed always when the computer is inicializated.

<br>

### Execute for the first time the container:
```
$ sudo docker run --gpus all -it --name {Name} --runtime nvidia --privileged -e DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix {Image}
```
<br>

------------------------------------------

<br>

## **USEGE ROTA DOCKER IMAGE**
### Start the container:
```
$ sudo docker start {Container ID}
```
<br>

- OBS: You can see the Container ID with the command: ```sudo docker ps -a```

<br>

### Verify if the container is UP:
```
$ sudo docker ps -a
```

### Enter in container:
```
$ sudo docker exec -it {Container ID} bash
```

### Exit container:
```
# ^D (ctrl+D)
```

### Turn off container:
```
$ sudo docker stop {Container ID}
```