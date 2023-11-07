FROM openjdk:8-jre

RUN mkdir -p /usr/local/app

#copiar el .jar del servicio a la imagen
COPY drop/*.jar /usr/local/app

#copiar script que se ejecutara al lanzar el contenedir
COPY drop/run.sh /usr/local/app/run.sh

#cuando lancemos una pila de servicios con docker, la ip de mongodb no se puede descubrir al menos que se la pasemos en un archivo de propiedades
COPY drop/application.properties application.properties

EXPOSE 8080

ENTRYPOINT sh /usr/local/app/run.sh
