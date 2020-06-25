# Networking en docker

1. Crear contenedores
   
   ```sh

    docker run -dit --name c1 alpine sh
    docker run -dit --name c2 alpine sh

   ```

2. Ver ip de la pc
   
   ```sh

    ifconfig -a

   ```
3. Ver ip de los contenedores

    ```sh

    docker inspect c1
    docker inspect c2

    ```

4. Otros ejemplos

    ```sh

    docker run -dit --name c1 alpine sh
    docker run -dit --name c2 --link c1 alpine sh

    docker attach c2

    ```