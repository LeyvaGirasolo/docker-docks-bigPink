#Docker Images

## Descargar imagenes de contenedores

### Para descargar imagenes oficiales [Docker Hub](https://hub.docker.com/ "Docker Hub") inline link.

- Para listar las imagenes actuales en tu maquina local

`docker images`
`docker images | grep centos`



- Para descargar una imagen a tu local
		
`docker pull name-image` -> latest
`docker pull name-image:tag` -> para espesificar una versison 

### Creando nuestras propias imagenes

Las imagenes en Docker se crean a partir de un Dockerfile que contiene todas 
las instrucciones que Docker debe de ejecutar para preparar la imagen; tanto
el SO como todo el software que debe de tener instalado.

`FROM centos:7`
`RUN yum -y install httpd`
`CMD apachectl -DFOREGROUND`


*DockerFile reference [Dockerfile](https://docs.docker.com/engine/reference/builder/ "DockerFile")*

Una vez terminado tu Dockerfile se hace un Build del mismo para agregarlo como
imagen en tu maquina local

`docker build --tag name-image:tag .`
`docker build -t name-image:tag -f my-dockerfile .`

Podemos ver el hisotorial de nuestra imagen creada

`docker history -H apache-centos7:latest`


