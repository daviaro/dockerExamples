## Ejercicio 4 con DockerFile

Se crea el directorio cowsay4 en el cual se agrega el Dockerfile y en el se configura la  descarga de la imagen de debian y la instalacion de cowsay y fortune.
pero se generan unas lineas adicionales; ENTRYPOINT y MAITAINER

```
FROM debian:wheezy
MAINTAINER David Aroca <daviaro@gmail.com>
RUN apt-get update && apt-get install -y cowsay fortune
COPY entrypoint.sh /
ENTRYPOINT ["/entrypoint.sh"]
```

En MAINTAINER el nombre y correo de un contacto.
En ENTRYPOINT se invoca el archivo entrypoint.sh el cual contiene un script que invoca las funciones cowsay y fortune de acuerdo a unas condiciones.

Este ejercicio se realiza para probar el cargue de imagenes a docker hub en la cuenta.
