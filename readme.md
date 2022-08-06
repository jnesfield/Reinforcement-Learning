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
docker pull jxu305/openai_gym_docker:v1.0 <br>

docker run -p <local port>:8888 -it -v <local directory to mount>:<target directory> jxu305/openai_gym_docker:v1.0
```

