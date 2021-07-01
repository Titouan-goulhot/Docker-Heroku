# Docker-Heroku

### First of all...

=> you must create an account on = 
                                   -DockerHub
                                   -Heroku

=> You must 

## How to deploy an App 

`docker build -t + id_docker/nom_projet`

`heroku login` => connect to Heroku account

`heroku create` => creating the app + heroku give a name at  the applicaiton 

`heroku container:push web -a` + name_of_app_given_by_heroku

`heroku container:release web -a` + name_of_app_given_by_heroku
`heroku open` => Open Application in navigator 



### TIPS

`touch Dockerfile` => will creat an empty Dockerfile without any extension 
