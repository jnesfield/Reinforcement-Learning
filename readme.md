# Reinforcement Learning

## started: 2/23/2022
## last edited: 10/30/2022

## By: James Nesfield

### PURPOSE: 
The purpose of this repo is to store and publicly display my exploratory work in reinforcement learning 

## use docker in ubuntu:

- install ubuntu 18.04 lts as an operating system : 
  - https://ubuntu.com/download/desktop <br>
- update ubuntu and install proper nvidia drivers using apt-get: 
  - https://www.cyberciti.biz/faq/ubuntu-linux-install-nvidia-driver-latest-proprietary-driver/ <br>
- install docker and if needed nvidia packages so you may access gpu resources: 
  - https://docs.nvidia.com/ai-enterprise/deployment-guide/dg-docker.html <br>
- build a new image using the dockerfile in this repo: 
  -  https://raw.githubusercontent.com/jnesfield/Reinforcement-Learning/main/DockerFile <br>

- download the docker file and run this changing the user name and path to match your own set up:

```
sudo docker build  -f /home/james/docker_aigym/DockerFile /home/james/docker_aigym -t james_n_aigym:0.1
```
- /home/james/docker_aigym/DockerFile is where the docker file is

- /home/james/docker_aigym is the context

- -t james_n_aigym:0.1 specifies the name you will use to run the image later thus:

```
docker run james_n_aigym:0.1
```

- ideally use something like this to run

```
docker run -p 8888:8888 -it --gpus all -v <local directory to mount>:/tf/mystuff/ james_n_aigym:0.1
```

# good luck!
