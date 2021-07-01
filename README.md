
![Docker-Logo](https://s2.qwant.com/thumbr/0x380/5/6/0d4e0a2c7c8518b622644066cbce588e737b82401eabe634c435067b67b75d/dockerhero.jpg?u=https%3A%2F%2Ftr4.cbsistatic.com%2Fhub%2Fi%2Fr%2F2016%2F10%2F18%2F831f017c-ee68-4bd6-8a5c-ab31b4d35d6d%2Fresize%2F770x%2F1cedcf2f03388a9720835a628a8a9765%2Fdockerhero.jpg&q=0&b=1&p=0&a=0)

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

## Work on Linux 

You can work on a Linux Interface from your pc using a container. 

Execute 

`docker run -it ubuntu bash` -> In that way you can work with a classical  terminal bash Linux... In a container ! 

Let's have some fun
-------------------

From your terminal bash Linux : 

` apt update`
 `apt install figlet`
`figlet hello campus!`



## Create your own picture with *Dockerfile

"Docker can build images automatically by reading the instructions from a Dockerfile. A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image. Using docker build users can create an automated build that executes several command-line instructions in succession." -Not from me.


1. In an empty repository, creat a file named "Dockerfile" 
    *tips -> you can also (from your Powershel & in the right repository in your machine) execute this command `touch Dockerfile`
2. Edit your file with this code 
`FROM  alpine
LABEL maintainer="DockerGeeK"
CMD ["echo", “Conversation depuis l’intérieur de la baleine"]`
3. Now you can create a picture from this Dockerfile (after you named your picture) with : 
`docker build -t name_picture .` 
4. Then you can "run" it : 
`docker run name_picture`

**How to create a Dockerfile**

* **FROM**  : will define the source of the picture
* **RUN** : will execute some command in your container
* **ADD** : will add (no kidding) some files in your container
* **WORKDIR** : will define your work repository
* **EXPOSE** : ~~I don't know how to traduce that in english~~
* **VOLUME** : ~~Same problem...~~
* **CMD** : Define the command by default when you execute a container.

## How to deploy an App 

**First** you need to read [this](https://expressjs.com/fr/starter/hello-world.html), [this](https://devcenter.heroku.com/articles/container-registry-and-runtime), & [that](http://www.goring.org/resources/NodeandDocker.html)... See you later !


`docker build -t + id_docker/nom_projet`

`heroku login` => connect to Heroku account

`heroku create` => creating the app + heroku give a name at  the applicaiton 

`heroku container:push web -a` + name_of_app_given_by_heroku

`heroku container:release web -a` + name_of_app_given_by_heroku
`heroku open` => Open Application in navigator 



### TIPS

`touch Dockerfile` => will creat an empty Dockerfile without any extension 
