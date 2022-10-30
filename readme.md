# Reinforcement Learning

## started: 2/23/2022
## last edited: 7/28/2022

## By: James Nesfield

### PURPOSE: 
The purpose of this repo is to store and publicly display my exploratory work in reinforcement learning 

use docker<br>
build a new image using the dockerfile in this repo<br>
install docker and if needed nvidia packages so you may access gpu resources, this does not work in windows, so please google how to set that up:<br>
https://docs.nvidia.com/ai-enterprise/deployment-guide/dg-docker.html <br>
download the docker file and run this changing the user name and path to match your own set up:

```
sudo docker build  -f /home/james/docker_aigym/DockerFile /home/james/docker_aigym -t james_n_aigym:0.1
```
/home/james/docker_aigym/DockerFile is where the docker file is

/home/james/docker_aigym is the context

-t james_n_aigym:0.1 specifies the name you will use to run the image later thus:

```
docker run james_n_aigym:0.1
```

ideally use something like this to run

```
docker run -p 8888:8888 -it --gpus all -v <local directory to mount>:/tf/mystuff/ james_n_aigym:0.1
```
