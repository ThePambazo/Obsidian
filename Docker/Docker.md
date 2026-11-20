## Compose
Compose es una herramienta que corre dos contenedores al mismo tiempo. Puedes encontrar el ejemplo en clonando el siguiente repositorio:

`git clone https://github.com/docker/multi-container-app`

el archivo compose.yaml le dice a Docker las instrucciones sobre cómo correr la aplicación. Ejemplo:


``` python
# Comments are provided throughout this file to help you get started.

# If you need more help, visit the Docker compose reference guide at

# https://docs.docker.com/compose/compose-file/

  

# Here the instructions define your application as two services called "todo-app" and “todo-database”

# The service “todo-app” is built from the Dockerfile in the /app directory,

# and the service “todo-database” uses the official MongoDB image

# from Docker Hub - https://hub.docker.com/_/mongo.

# You can add other services your application may depend on here.

  

services:

  todo-app:

    build:

      context: ./app

    depends_on:

      - todo-database

    environment:

      NODE_ENV: production

    ports:

      - 3000:3000

      - 35729:35729

    develop:

      watch:

        - path: ./app/package.json

          action: rebuild

        - path: ./app

          target: /usr/src/app

          action: sync

  

  todo-database:

    image: mongo:6

    #volumes:

    #  - database:/data/db

    ports:

      - 27017:27017

  

#volumes:

  #database:
  ```
  