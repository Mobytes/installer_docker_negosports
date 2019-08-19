## INSTALADOR DOCKER WINDOWS
Este manual es para poder instalar el software de negosports con docker en windows.

### Version
V0.4

### Tecnologias

* [DockerToolbox](https://drive.google.com/file/d/1ebWirBtiEBDf7JVL4utbmAH9ktqH0j8y/view?usp=sharing)
* [Git](https://git-scm.com)
* [PgAdmin4](https://www.pgadmin.org/)

Antes de configurar el software tenemos que localizar 

### Configuracion

* Verificamos la distribucion de los directorios
```
sistema/
├─ docker-compose.yml
├─ production.yml
├─ README.md
├─ .env
├─ nginx/
│  ├─ Dockerfile
│  └─ nginx.conf
├─ app/
│  ├─ booking/
│  ├─ Dockerfile
│  ├─ Gulpfile.js
│  ├─ package.json
│  └─ ...
```

### Instalacion
Todos los comandos de docker tienen que ser lanzados dentro de la carpeta del proyecto de `docker`

### Situarnos en la carpeta system/
```sh
$ cd sistema/
```

### Creamos los servicios
```sh
$ docker-compose build
```

### Inciamos los servicios
```sh
$ docker-compose up -d
```

### Restauramos la base de datos 
Restauramos la base de datos con el pgadmin

## Comandos adicionales
* Listar servicios de docker
```sh
$ docker ps
```

* Reniciar servicios de docker
```sh
$ docker-compose up -d --no-deps --build </service>
```

* Entrar en el contenedor
```sh
$ docker exec -i -t [name-container] /bin/bash
```

* Eliminar todos los contenedores detenidos, 
```sh
$ docker system prune
```

* Eliminar volumenes detenidos.
```sh
$ docker system prune --volumes
```

* Remove one or more containers
```sh
$ docker container ls -a
$ docker container rm cc3f2ff51cab cd20b396a061
```
