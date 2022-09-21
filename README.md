# docker_study

### Key Docker Commands

- docker build . : Build a Dockerfile and create your own Image based on the file
  - -t NAME:TAG : Assign a NAME and a TAG to an image

<br>

- docker run IMAGE_NAME : Create and start a new container based on image IMAGENAME (or
use the image id)
  - --name NAME : Assign a NAME to the container. The name can be used for stopping and
removing etc.
  - -d : Run the container in detached mode - i.e. output printed by the container is not
visible, the command prompt / terminal does NOT wait for the container to stop
  - -it : Run the container in "interactive" mode - the container / application is then
prepared to receive input via the command prompt / terminal. You can stop the
container with CTRL + C when using the -it flag
  - --rm : Automatically remove the container when it's stopped
  
<br>

- docker ps : List all running containers
  - -a : List all containers - including stopped ones

<br>

- docker images : List all locally stored images

<br>

- docker rm CONTAINER : Remove a container with name CONTAINER (you can also use the
container id)

<br>

- docker rmi IMAGE : Remove an image by name / id

<br>

- docker container prune : Remove all stopped containers

<br>

- docker image prune : Remove all dangling images (untagged images)
  - -a : Remove all locally stored images
<br>

- docker push IMAGE : Push an image to DockerHub (or another registry) - the image name/
tag must include the repository name/ url

<br>

- docker pull IMAGE : Pull (download) an image from DockerHub (or another registry) - this
is done automatically if you just docker run IMAGE and the image wasn't pulled before
