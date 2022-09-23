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

<br>

## Data & Volumes
- docker run -v /path/in/container IMAGE : Create an Anonymous Volume inside a
Container

<br>

- docker run -v some-name:/path/in/container IMAGE : Create a Named Volume (named
some-name ) inside a Container

<br>

- docker run -v /path/on/your/host/machine:path/in/container IMAGE : Create a Bind
Mount and connect a local path on your host machine to some path in the Container


<br>

- docker volume ls : List all currently active / stored Volumes (by all Containers)


<br>

- docker volume create VOL_NAME : Create a new (Named) Volume named VOL_NAME . You
typically don't need to do that, since Docker creates them automatically for you if they don't
exist when running a container

<br>

- docker volume rm VOL_NAME : Remove a Volume by it's name (or ID)

<br>

- docker volume prune : Remove all unused Volumes (i.e. not connected to a currently
running or stopped container)

<br>

