
! [Docker-Logo](https://s2.qwant.com/thumbr/0x380/5/6/0d4e0a2c7c8518b622644066cbce588e737b82401eabe634c435067b67b75d/dockerhero.jpg?u=https%3A%2F%2Ftr4.cbsistatic.com%2Fhub%2Fi%2Fr%2F2016%2F10%2F18%2F831f017c-ee68-4bd6-8a5c-ab31b4d35d6d%2Fresize%2F770x%2F1cedcf2f03388a9720835a628a8a9765%2Fdockerhero.jpg&q=0&b=1&p=0&a=0)

# Docker-Heroku

### First of all...

=> you must create an account on = 
                                   -DockerHub
                                   -Heroku

=> You must download & Install 
[Docker Desktop](https://hub.docker.com/)

#### Just to be sure Docker works fine...

you can run directly in you powerShell : 
`Docker` -> Will make appear a list of command 

&

` docker run hello-world` -> will execute your first container throught the image 

### Some commands 

`docker --version` -> pretty clear isn't it ?
`docker image ls` -> show your local image 
`docker run <image ID>` -> execute a container 
`docker image rm <image ID>` -> remove an image
`docker ps -a` -> List of your container
`docker start <container ID>` -> start a container which is stopped

## How to deploy an App 

`docker build -t + id_docker/nom_projet`

`heroku login` => connect to Heroku account

`heroku create` => creating the app + heroku give a name at  the applicaiton 

`heroku container:push web -a` + name_of_app_given_by_heroku

`heroku container:release web -a` + name_of_app_given_by_heroku
`heroku open` => Open Application in navigator 



### TIPS

`touch Dockerfile` => will creat an empty Dockerfile without any extension 
