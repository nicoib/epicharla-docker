# Dockerfile example 1

Ejemplo de un dockerfile simple, donde solamente se copia una aplicación y se ejecuta

```sh
#Se descarga una imagen de nginx desde dockerhub

FROM nginx:1.17.1-alpine 

LABEL author="Nicolas Ibarra"

#Se copia la configuración de nginx
COPY nginx.conf /etc/nginx/nginx.conf

#Se copia la aplicación para que sea ejecutada
COPY /dist/dockerfile1 /usr/share/nginx/html

```

Para ejecutar la imagen creada se debe ejecutar el siguiente comando:

```sh
docker build . -t <<Nombre imagen>>
docker run -p 8080:80 <<Nombre imagen>>
```