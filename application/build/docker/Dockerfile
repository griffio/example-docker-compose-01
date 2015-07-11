FROM azul/zulu-openjdk-centos:8
MAINTAINER griffio@users.noreply.github.com
RUN bash -c 'touch /main.jar'
ADD /home/griffio/IdeaProjects/spring-compose-01/application/build/libs/griffio-app-0.1.0.jar main.jar
ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "-jar", "/main.jar"]
VOLUME ["/tmp"]
