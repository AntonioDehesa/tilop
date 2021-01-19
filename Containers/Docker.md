# Docker

## Installation

So, first, we need to install it. We could simply follow the installation guide in the Docker page, but I had some troubles with it. So, at the end, these are the commands I had to run to correctly install it. 
```bash
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu xenial stable"
sudo apt update
apt-cache search docker-ce
sudo apt update
sudo apt upgrade
sudo apt install docker-ce
```

## First Launch

```bash
docker run -d -p 80:80 docker/getting-started
```
So, this would allow us to pull the image "docker/getting-started". 
Tags: 
* -d: Will run the image in "detached mode"
* -p: Allows us to map the ports. In this case, it will map the port 80 of the local machine, on the left side, to port 80 of the docker image, on the right side. 
* -t: Tags. We can name our image. 

After testing the docker installation with the "getting-started", we will run the next step of the guide, which will be running a node [application on docker](https://github.com/docker/getting-started/tree/master/app). 

```docker
 FROM node:12-alpine
 WORKDIR /app
 COPY . .
 RUN yarn install --production
 CMD ["node", "src/index.js"]
```
For that, we clone the project, and in the "/app" directory, we create a Dockerfile, which HAS NO EXTENSION. 

Keywords: 
* FROM: Base image where everything else will be running. It includes a node installation
* WORKDIR: Sets the PWD to /app
* COPY . .: Will copy the files in our local system to the PWD of the docker. 
* RUN: It will, well, run the following command. 
* CMD: It will allow us to run command line instructions. 

```bash
 docker build -t getting-started .
```
Once we write this file, we build our image. 

Afterwards, we can run our image. 
```bash
 docker run -dp 3000:3000 getting-started
```


## Updating the image
To update our image, we simply change our application, and then we build the image again. 
