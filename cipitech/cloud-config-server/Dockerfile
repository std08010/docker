ARG project_version=1.1.0-SNAPSHOT

FROM openjdk:8-jre
LABEL maintainer="Altin Cipi <haris.tsipis@gmail.com>"

WORKDIR /usr/src

VOLUME [ "/data/bootstrap" ]

COPY cipitech-cloud-config-server-1.1.0-SNAPSHOT.jar cipitech-cloud-config-server.jar

#ADD http://URL_TO_JAR_LOCATION_ON_NEXUS cipitech-cloud-config-server.jar

EXPOSE 8888
EXPOSE 8887

#Remember to mount the /data/bootstrap folder from the machine that runs docker
CMD ["java", "-jar", "-Dspring.config.additional-location=/data/bootstrap/sensitive.properties", "-Dspring.profiles.include=dev,docker", "cipitech-cloud-config-server.jar"]