# Iroha nodes for BSMD
Install four Iroha nodes for BSMD experiments or test. This guide is meant for Debian based systems (Ubuntu, 
Mint, Kali, etc.), but with a few modifications this will also work for Windows or macOS. 

The Iroha nodes run on four Docker containers. Visit the [Docker](https://www.docker.com/) web page to familiarize 
with the system. If you have never work with Docker I recommend the 
[Docker 101 tutorial](https://www.docker.com/101-tutorial) before continuing.   

# Pre-requisites
1. Install Docker by following the official [guide](https://docs.docker.com/engine/install/ubuntu/). Then, follow this
[guide](https://docs.docker.com/engine/install/linux-postinstall/) to make Docker run as non-root user

2. Install docker-compose with the following commands:
```commandline
curl -L "https://github.com/docker/compose/releases/download/1.26.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
```commandline
chmod +x /usr/local/bin/docker-compose
```
3. Test the installation with:
```commandline
docker-compose --version
```
# Install Iroha nodes
Run ```docker-compose up -d``` to install all the containers, wait about 1min for the process to finish.

To stop the blockckain simply run ```docker-compose down```.

If you want to start again the iroha nodes run ```docker-compose up -d```

To connect your project to the iroha blockchain use the ip address of the hosting machine one of the following ports: 
`50051`, `50052`, `50053` or `50054`. If you are running the blockchain on a cloud VM or outside a local network make 
sure the hosting machine acept TCP and UDP connections from the mentioned ports. If you are running the blockchain 
on a cloud VM or outside a local network make sure the hosting machine accept TCP and UDP connections from the ports:
`50051`, `50052`, `50053` or `50054`. 

# Install more than four Iroha nodes
TO-DO

## Built With
* [Hyperledger Iroha](https://github.com/hyperledger/iroha)
* [Docker](https://www.docker.com/)

## Authors
* **David Lopez** [mitrailer](https://github.com/mitrailer)

## Thanks
This guide use snipets from [Calvin Nguyen](https://levelup.gitconnected.com/the-easiest-docker-docker-compose-setup-on-compute-engine-ec171c09a29a)
and from the [Iroha docker project](https://github.com/hyperledger/iroha/tree/master/docker) 


## License

* Hyperledger Iroha is [licensed](https://github.com/hyperledger/iroha/blob/master/LICENSE) under the Apache License 2.0 
* This project is [licensed](LICENSE.md) under the Apache License 2.0