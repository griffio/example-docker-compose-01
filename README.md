# docker-compose-01

Example for Nginx/Java with Spring Boot 

[docker-compose](https://docs.docker.com/compose/)

Launch two containers - for nginx, JVM; that can be configured for local and production use.

Required docker configuration files:

~~~
/docker-compose-base.yml - Shared config that can be extended 
/docker-compose-devl.yml - Localhost deploy 
/docker-compose-prod.yml - Cloud provider deploy 
/nginx/DockerFile 
/spring-boot/DockerFile 
~~~

---

docker-compose.yml is the default filename when --file is not specified.

~~~
docker-compose --file docker-compose-devl.yml build
docker-compose --file docker-compose-devl.yml up
~~~
