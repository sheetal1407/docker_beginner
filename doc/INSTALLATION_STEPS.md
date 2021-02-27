# Steps to install Docker

This is my first time working on Docker. Please follow the steps below to install Docker.

* To install Docker Engine, you need the 64-bit version of one of these Ubuntu versions:

  *Ubuntu Groovy 20.10
  *Ubuntu Focal 20.04 (LTS)
  *Ubuntu Bionic 18.04 (LTS)
  *Ubuntu Xenial 16.04 (LTS)
  
Installing using Repositories

1. Update the apt package index and install packages to allow apt to use a repository over HTTPS:

````
$ sudo apt-get update

$ sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
````
2. Adding Docker's GPG Key

````
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
````
Verify that you now have the key with the fingerprint 
, by searching for the last 8 characters of the fingerprint.

````
9DC8 5822 9FC7 DD38 854A  E2D8 8D81 803C 0EBF CD88
````
````
$ sudo apt-key fingerprint 0EBFCD88

pub   rsa4096 2017-02-22 [SCEA]
      9DC8 5822 9FC7 DD38 854A  E2D8 8D81 803C 0EBF CD88
uid           [ unknown] Docker Release (CE deb) <docker@docker.com>
sub   rsa4096 2017-02-22 [S]
````
3. Use the following command to set up the stable repository.
````
$ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
````
Install Docker Engine

1. Update the apt package index
````
 $ sudo apt-get update
 $ sudo apt-get install docker-ce docker-ce-cli containerd.io
````
2. To install a specific version of Docker Engine, list the available versions in the repo, then select and install:

Install a specific version using the version string from the available versions in the repo:
````
$ sudo apt-get install docker-ce=<VERSION_STRING> docker-ce-cli=<VERSION_STRING> containerd.io
````
3. Verifying if the docker engine is installed in a right manner by running the hello-world image:
````
$ sudo docker run hello-world
````

