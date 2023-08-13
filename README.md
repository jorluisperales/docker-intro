
# Comandos basicos de Docker

* Ver la version instalada de docker:
```
docker --version
```

* Listar las imagenes almacenadas localmente
```
docker images ls
```

* Descargar la imagen hello-world
```
docker pull hello-world
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