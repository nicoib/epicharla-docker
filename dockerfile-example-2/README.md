# Dockerfile example 2

Ejemplo de un dockerfile multicapa, donde el codigo fuente de la aplicación, se compila y se corre

```sh
#Stage 1
FROM mhart/alpine-node:11 AS builder

WORKDIR /app

COPY . .

RUN yarn install
RUN yarn run build

#Stage 2
FROM nginx:1.16.0-alpine

COPY --from=builder /app/build /usr/share/nginx/html

RUN rm /etc/nginx/conf.d/default.conf

COPY nginx.conf /etc/nginx/conf.d

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]

```

Para ejecutar la imagen creada se debe ejecutar el siguiente comando:

```sh
docker build . -t <<Nombre imagen>>
docker run -p 8080:80 <<Nombre imagen>>
```