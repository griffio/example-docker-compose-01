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
/application/build/docker/DockerFile 
~~~

* Docker Gradle plugin task [com.bmuschko.gradle.docker.tasks.image.Dockerfile] generates a DockerFile.
* The build jar is copied to DockerFile context location.
 * Local files can only be added to container from Docker build context location.

application/build.gradle

~~~
./gradlew createDockerFile
~~~

---

docker-compose.yml is the default filename when --file is not specified.

~~~
docker-compose --file docker-compose-devl.yml build
docker-compose --file docker-compose-devl.yml up
~~~
