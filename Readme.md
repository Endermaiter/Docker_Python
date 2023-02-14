# Docker + Python

---

# Creamos un contenedor sencillo de python

Comando: 

`$ docker run -it --rm --name my-running-script -v "$PWD":/usr/src/myapp -w /usr/src/myapp python:3 python your-daemon-or-script.py`

Descripción del comando:

- `docker:` el comando base, es el daemon
- `run:` crear el contenedor
- `-it:` dos opciones que me valen para interactuar con la terminal del contenedor
- `--rm:` borra el contenedor cuando finaliza la opción
- `-v:` define el mapeo del volumen a continuacion
  * `"$SPWD":` el directorio donde estamos
  * `/usr/src/myapp:` el directorio dentro del contenedor
- `-w:` el directorio de trabajo (workdir)
- `python:3:` la imagen de la que se creará el contenedor
- `python script.py:` el script que debe ejecutarse en el contenedor

Para ejecutar un script de pyhton con el comando, debemos darselo en la última opcion:

`$ docker run -it --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp python:3 python main.py`