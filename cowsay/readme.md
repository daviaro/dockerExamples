## Ejercicio 1 con DockerFile

Se crea el directorio cowsay en el cual se agrega el Dockerfile en la cual se genera la descarga de la imagen de debia y la instalacion de cowsay y fortune.

```
FROM debian:wheezy
RUN apt-get update && apt-get install -y cowsay fortune
``` 
