
# Comandos basicos de Docker

* Ver la version instalada de docker:
```
docker --version
```

* Listar las imagenes almacenadas localmente
```
docker images ls
```

* Descargar la imagen hello-world y hello-seattle
```
docker pull hello-world
```

```
docker pull hello-seattle
```

* Crear un contener usando la imagen `hello-world`
```
docker run hello-world
```

* Listar todos los contenedores
```
docker container ls -a
```

* Listar todos los contenedores y su tamaño
```
docker container ls -a -s
```

* Remover una imagen de docker usando su ID en este caso `515d5e66f68a`
```
docker rmi 515d5e66f68a
```
Tip: Pueden usar los primeros tres caracteres del id de la imagen para referirse a ella y borrarla `docker rmi 515`

* Remover un contenedor usando su ID en este caso `515d5e66f68a`
```
docker container rm c159ba7ffa32
```
Tip: Pueden usar los primeros tres caracteres del id del para referirse a ella y borrarla `docker container rm c15`

## Operaciones sobre contenedores

* Despleguemos un contenedor llamado `web` usando la imagen oficial de nginx
```
docker run -it --rm -d -p 8080:80 --name web nginx
```
* **-d**: se utiliza por el comando Docker Run para arrancar en segundo plano, también conocido como background.
* **–rm**: para destruir el docker al terminar su ejecución.
* **-p**: cumple la función de mapear puertos del host hacia el contenedor.
* **-it**: interactivo (stdin) + tty (pseudo terminal).
* **--name**: se utilizar para brindarle un nombre el contenedor, si no se indica docker le asignara uno autogenerado por defecto.**
