
# Comandos basicos de Docker

* Ver la version instalada de docker:
```
docker --version
```

* Listar las imagenes almacenadas localmente
```
docker images ls
```

* Buscar una imagine en dockerhub
```
docker search hello-world
```

* Descargar la imagen hello-world y hello-seattle
```
docker pull hello-world
```

```
docker pull hello-seattle
```
**Tip**: Las imagenes tambien pueden ser descargadas especificando el tag `<Docker Hub Id o Registro de docker>/<Repositorio de Docker>:<Nombre/Tag o version>`, ejemplo: `jperales29/static-site:latest`

* Crear un contener usando la imagen `hello-world`
```
docker run hello-world
```
**Tip**: Si la imagen no esta disponible localmente, docker intentara descargalo desde el registro

* Listar todos los contenedores
```
docker container ls -a
```

```
docker ps -a
```

* Listar todos los contenedores y su tamaño
```
docker container ls -a -s
```

```
docker ps -a -s
```

* Remover una imagen de docker usando su ID en este caso `515d5e66f68a`
```
docker rmi 515d5e66f68a
```
Tip: Pueden usar los primeros tres caracteres del id de la imagen para referirse a ella y borrarla `docker rmi 515` o su nombre

* Remover un contenedor usando su ID en este caso `515d5e66f68a`
```
docker container rm c159ba7ffa32
```
Tip: Pueden usar los primeros tres caracteres del id del para referirse a ella y borrarla `docker container rm c15`

## Operaciones sobre contenedores

* Despleguemos un contenedor llamado `web` usando la imagen oficial de nginx
```
docker container run -it -d -p 8080:80 --name web nginx
```

* **-d**: se utiliza por el comando Docker Run para arrancar en segundo plano, también conocido como background.

* **-p**: cumple la función de mapear puertos del host hacia el contenedor.
* **-it**: interactivo (stdin) + tty (pseudo terminal).
* **--name**: se utilizar para brindarle un nombre el contenedor, si no se indica docker le asignara uno autogenerado por defecto.**

**Tip**: Se puede agregar la opcion `-rm` para hacer que el contenedor sea eliminado una vez complete su ejecucion o sea detenido

* Detener el contenedor 
```
docker container stop 95e985a58fbf
```

* Iniciar el contenedor 
```
docker container start 95e985a58fbf
```

* Reiniciar el contenedor
```
docker container restart 95e985a58fbf
```

* Inspeccionar el contenedor
```
docker container inspect 95e985a58fbf
```

* Ver las estadisticas  del contenedor
```
docker container stats 95e985a58fbf
```
**Tip**: Este comando puede ser ejecutado sin identificar el contenedor para poder ver las estadisticas de todos los contenedores siendo ejecutados.

* Ver los logs del contenedor
```
docker container logs 95e985a58fbf
```





Recursos:

https://github.com/manjunath5496/Basic-Docker-Commands
