# Docker
# What is a container?
* A way to package application with all the neceesary dependencies and configuration
* Portiable artifact, easily shared and moved around
* Makes development and deployment more efficient
* Technically, Layers of images which is mostly Linux Based Image(alpine:3.10), because small in size with application image on top(postgres:10.10)
# Where do containers live?
* Container Repository 
* Public Repository for docker(DockerHub)
# Before Containers?
* Installation process different on each OS environment
* Many steps where something could go wrong
* Configuration on the server needed
* Dependency version conflicts
* Textual guide of deployment which ultimately leads to misunderstandings

![Screenshot 2023-06-08 134607](https://github.com/Sinha321/Docker/assets/116704941/d745303d-65f0-44f2-8112-0b56cc983785)

# After Containers?
* Own isolated environment
* Packaged with all needed configuration
* One command to install the application
* Run same application with two different versions
* Developers and Operations work together to package the application in a container 
* No environmental configuration needed on server-except Docker Runtime

![Screenshot 2023-06-08 135259](https://github.com/Sinha321/Docker/assets/116704941/f05dee4b-84cf-4287-8ecd-c1121e612221)
# Docker Image 
* Actual Package
* Artifact that can be moved around 
* Not running
# Docker Container
* Actually start the application
* Container is a running environment for image
* virtual file system
* port binded: talk to application running inside of container (port:5000)
* application image: postgres,redis,mongo...
* Container is when the image is pulled to the local machine and starts the application and the container environment is created
* Running
# Docker vs Virtualmachine
Operating system has two layers
* OS Kernel (the part which communicates with the hardware component)
* Application layer (run on the kernel layer)
* Docker virtualizes the application layer. When a docker image is downloaded it actually contains the application layer of the OS and uses the kernel of the host because it dosen't have its own kernel.
* The size of the docker image is much smaller because they just ahve to implement one layer (megabytes)
* Docker containers start and run much fast
* Linux based docker image might not be compatible with the windows kernel. A technology called Docker Toolbox is installed which abstracts away the kernel to make it possible for your hosts to run different docker images.
* On the other ahnd , the virtual machine has the applicattions layer and it's own kernel.So it virtualizes the complete operating system.
* Size is of few gigabytes
* VM of any OS can run on any OS host
# Terms:
* Docker Engine -to run docker containers on the laptop
* Docker CLI -to execute some docker commands
* Docker compose -technology to orchestrate if there are multiple containers
# Main docker commands 
1. docker –version
* This command is used to get the currently installed version of docker
2. docker pull
* Usage: docker pull <image name>
* This command is used to pull images from the docker repository(hub.docker.com)
3. docker run
* Usage: docker run -it -d <image name>
* Usage: docker run  -d <image name> -starts a new container with a command(detached mode)
* This command is used to create a container from an image. Docker run command pulls the image and starts container
4. docker ps
* This command is used to list the running containers
5. docker ps -a
* This command is used to show all the running and stopped containers
6. docker exec
* Usage: docker exec -it <container id> bash
* This command is used to access the running container
7. docker stop
* Usage: docker stop <container id>
* This command stops a running container
8. docker kill
* Usage: docker kill <container id>
* This command kills the container by stopping its execution immediately. The difference between ‘docker kill’ and ‘docker stop’ is that ‘docker stop’ gives the container time to shutdown gracefully, in situations when it is taking too much time for getting the container to stop, one can opt to kill it
9. docker commit
* Usage: docker commit <conatainer id> <username/imagename>
* This command creates a new image of an edited container on the local system
10. docker login
* This command is used to login to the docker hub repository
11. docker push
* Usage: docker push <username/image name>
* This command is used to push an image to the docker hub repository
12.  docker images
* This command lists all the locally stored docker images
13. docker rm
* Usage: docker rm <container id>
* This command is used to delete a stopped container
14. docker rmi
* Usage: docker rmi <image-id>
* This command is used to delete an image from local storage
15. docker build
* Usage: docker build <path to docker file>
* This command is used to build an image from a specified docker file
16. docker start <container id>
* Start the container with its id by doind docker ps
# Container Port vs Host Port
* Multiple containers can run on your host machine as container is just the virtual environment running on the host.
  * Your laptop has only certain ports available
  * How is the binding between the port that the host machine has and the container
  * Conflict when same port on host machine
  * Two containers say 3000 and 3001 can listen to same port 3000 when it is binded to two different ports from the host amchine. Once the binding between the host and the container is done , we can actually connect to the running container using the port of the host.
  
  
