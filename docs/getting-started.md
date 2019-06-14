# Getting started

## .gitignore
* Create a file called ```.gitignore``` in the project directory and past everything from this link

```https://github.com/github/gitignore/blob/master/Python.gitignore```

## Using Docker
### Installation
https://hub.docker.com/editions/community/docker-ce-desktop-windows
https://hub.docker.com/editions/community/docker-ce-desktop-mac

### Running the app
* Now, the app and everything else you might need for development can be started with one simple command line code in the project directory!

```docker-compose up```

### Closing the app 
* The app can be stopped with CTRL + C (Or whatever appropriate command on your OS) then just run the code below to stop and remove the other containers if desired

```docker-compose down```

### Tools
* Sometimes you might want to nuke all your docker images and containers. Copy the following script and save it as a .bat file and run it to do so

```
@echo off
FOR /f "tokens=*" %%i IN ('docker ps -aq') DO docker rm %%i
FOR /f "tokens=*" %%i IN ('docker images --format "{{.ID}}"') DO docker rmi %%i
```