# Volumenes en docker

## Comandos claves

```sh

docker volumen --help
docker volumen ls
docker volume rm <nombre volumen>

```

## Ejemplo

1. Ejecutar la imagen sin montar el volumen
```sh

docker run -d -p 8080:80 -v /usr/share/nginx/html nginx:alpine

```

2. Mostar el contenedor

```sh

docker inspect <id>

```


3. Ejecutar la imagen montandole el index.html

```sh

docker run -d -p 8080:80 -v $(pwd):/usr/share/nginx/html nginx:alpine

```
