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

