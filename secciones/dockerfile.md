#Dockerfile

* FROM
* RUN
* COPY/ADD
* ENV
* WORKDIR
* EXPOSE
* LABEL
* USER
* VOLUME
* CMD


## FROM

El *FROM* es la imagen de sistema operativo de nuestra elección

## RUN

*RUN* se utiliza para ejecutar comandos de linux

## COPY/ADD

Se utiliza para copiar/descargar archivos hacia la imagen que queremos crear

`COPY initializr /var/www/html` *->* Copia de nuestra maquina local 
`ADD initializr /var/www/html`  *->* Copia o descarga(http)

## ENV

*ENV (ENVIROMENT)* Sirve para agregar variables de entorno

`ENV JAVA_PATH /dir1/dir2/dir3`
`RUN echo "$JAVA_PATH"`

## WORKDIR

*WORKDIR* indica el directorio en el que vamos a estar trabajando

`WORKDIR /var/www/html`
`COPY initializr .`

## EXPOSE

*EXPOSE* nos permite exponer puestos para posteriormente usarlo

## LABEL

*LABEL* es una etiqueta, va en cualquier nivel, por lo general va al inicio
y siirve para dar metadata a la imagen 

`LABEL version = 1.0`
`LABEL descripcion = "This is apache image"`
`LABEL vendor = yo`


## USER

*USER* Sirve para cambiar de usuario; a partir del cambio de usuario todas 
las instrucciones posteriores se ejecutaran con este nuevo usuario

## VOLUME

*VOLUME* sirve para declarar data persistente que no se borre cuando el
contenedor se elimine


## CMD

*CMD* Es lo que mantiene vivo al contenedor y tiene que ser un proceso en primer plano
y se puede conbinar con otros comandos para ejecutar un script en bash

## .dockerignore

*.dockerignore*  archivo que sirve para ignorar otros archivos dentro de nuestro
directorio





