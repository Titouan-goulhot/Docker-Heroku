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
