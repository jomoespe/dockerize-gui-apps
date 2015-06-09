# Dockerized Firefox

Ejemplo de [artículo sobre como ejecutar aplicaciones dentro de Docker](http://fabiorehm.com/blog/2014/09/11/running-gui-apps-with-docker/)

Ahora mismo hay un sólo caso, [Firefox](./firefox/)

## Firefox

Existen dos scripts (*build* y *run*) para construir la imagen del contenedor y ejecutar la imagen.

### Construir imagen del contenedor

    docker build -t firefox .


### Ejecutar imagen del contenedor

    docker run --rm=true -e DISPLAY -v $HOME/.Xauthority:/home/developer/.Xauthority --net=host firefox

    