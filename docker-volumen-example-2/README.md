# Volumenes en docker

## Comandos claves

```sh

docker volumen --help
docker volumen ls
docker volume rm <nombre volumen>

```

## Ejemplo

1. Crear imagen
```sh

docker build . -t demo-1 -f dockerfile-1

```

2. Ejecutar imagen y ver que pasa cuando se hace el ls en el directorio

```sh

docker run -it -v /myvol demo-1 bash

```

3. Crear imagen
```sh

docker build . -t demo-1 -f dockerfile-1

```

4. Ejecutar imagen y ver que pasa cuando se hace el ls en el directorio

```sh

docker run -it -v /demo/volumen:/myvol demo-1 bash

```


5. Crear imagen
```sh

docker build . -t demo-2 -f dockerfile-2

```

6. Ejecutar imagen y ver que pasa cuando se hace el ls en el directorio

```sh

docker run -it -v /myvol demo-2 bash

```