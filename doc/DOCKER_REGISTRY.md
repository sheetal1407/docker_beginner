# Steps to host your own Registry

* Requirements

  The Registry is only compatible with Docker engine version 1.6.0 or higher.

* Commands
  
i. To start your registry
````
docker run -d -p 5000:5000 --name registry registry:2
````

ii. Pull (or build) some image from the hub
````
docker pull ubuntu
````

iii. Tag the image so that it points to your registry
````
docker image tag ubuntu localhost:5000/myfirstimage
````
iv. Push it
````
docker push localhost:5000/myfirstimage
````
v. To pull it back
````
docker pull localhost:5000/myfirstimage
````
