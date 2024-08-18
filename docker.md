# DOCKER [Servers for Hackers](https://serversforhackers.com/t/containers)

# Docker commands

1. `docker image ls` lists the docker images in the folder
2. `docker-compose up -d` starts the containers
3. `docker-compose down -d` stops the containers
4. `docker run --rm -d -v $(pwd)/application:/var/www/html -p 8080:80 shippingdocker/phpapp`
   - `--rm` destroys the container after running it
   - `-d` runs in the background
   - `-v` shares cource directory called $(pwd)/application
   - `:/var/www/html` is the target directory
   - `-p 8080:80` specifies the port
   - `shippingdocker/phpapp` is the docker image
5. `docker image ls -q` lists the container ids for all the images
6. `docker image rm $(docker image ls -q)` removes all the docker images in the docker instance

# Docker concepts

1. An image is like a class.
2. Running a container from an image is like instantiating a class object.

# Goals

1. Run a dev environment in docker
   - Nginx/PHP
   - MySQL
   - Redis
2. Create a `Docker file` to build a nginx/php image
3. Re-use existing docker images of MySQl and Redis that someone else has already created
