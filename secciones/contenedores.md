# Contenedores Docker

- Para saber si tenemos un contenedor corriendo actualmente:

`docker ps`
`docker ps -a`

- Para eliminar un contenedor:

`docker rm -fv name-container`

- Para crear un contenedor 

`docker run -d --name apache-centos name-image`

- Mapeo de puertos de maquina local a contenedor
 
`docker run -d --name apache-centos -p 80:80 apache-centos7:cmd`

- log de un contenedor

`docker logs name-image`

