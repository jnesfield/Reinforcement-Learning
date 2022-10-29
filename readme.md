# Reinforcement Learning

## started: 2/23/2022
## last edited: 7/28/2022

## By: James Nesfield

### PURPOSE: 
The purpose of this repo is to store and publicly display my exploratory work in reinforcement learning 

There is homebrew environment set ups and also application in gym package now too...

### set up env in ubuntu:<br>
#### get ubuntu 18.04 lts
sudo apt-get update<br>
sudo apt-get install python3.7<br>
sudo apt install python3-pip<br>
sudo apt-get -y install cmake<br>
sudo apt install zlib1g-dev<br>
sudo apt-get install p7zip-full<br>
pip3 install numpy<br>
pip3 install sklearn<br>
pip3 install gym==0.19.0<br>
pip3 install gym[Box2D]<br>
pip3 install scikit-build<br>
pip3 install opencv-python==4.0.0.21<br>
pip3 install gym[atari]==0.19.0 --no-cache-dir<br>
pip3 install matplotlib<br>

or just not be silly and use a docker image that already works:<br>
```
docker pull jxu305/openai_gym_docker:v1.0 

docker run -p <local port>:8888 -it -v <local directory to mount>:<target directory> jxu305/openai_gym_docker:v1.0

docker run -p 8889:8888 -it jxu305/openai_gym_docker:v1.0
```

consider using ubuntu 18.04 lts instead of windows os... windows does not let you pass along gpu access to docker without complicated steps....

to install docker with nvidia gpu support first install the right driver then docker with the nvidia tool kit
- https://www.cyberciti.biz/faq/ubuntu-linux-install-nvidia-driver-latest-proprietary-driver/
- https://docs.nvidia.com/ai-enterprise/deployment-guide/dg-docker.html

but the originally referenced does not allow you to use gpu resouces.... fail


thus build a new image using the dockerfile here<br>
download the docker file and run this:

```
sudo docker build  -f /home/james/docker_aigym/DockerFile /home/james/docker_aigym -t james_n_aigym:0.1
```
/home/james/docker_aigym/DockerFile is where the docker file is

/home/james/docker_aigym is the context

-t james_n_aigym:0.1 specifies the name you will use to run the image later thus:

docker run james_n_aigym:0.1

ideally use something like this to run

docker run -p 8888:8888 -it --gpus all -v <local directory to mount>:/tf/mystuff/ james_n_aigym:0.1

