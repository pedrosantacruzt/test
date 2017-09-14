FROM anapsix/alpine-java
VOLUME /tmp
EXPOSE 8888
WORKDIR /opt/spring/deployment
WORKDIR /opt/spring/configuration
WORKDIR /opt/spring/logs
ADD /home/bse-application/builds/deployment/artifacts/eida/backend/microservices/process-apis-projects/batch-api/log4j2-spring.xml /opt/spring/configuration/log4j2-spring.xml
ADD /home/bse-application/builds/deployment/artifacts/eida/backend/microservices/process-apis-projects/batch-api/aepe-ecommerce-server-configuration.jar /opt/spring/deployment/aepe-ecommerce-server-configuration.jar
RUN sh -c 'touch /opt/spring/deployment/aepe-ecommerce-server-configuration.jar'
RUN chmod -R 777 /opt/spring
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Dspring.cloud.config.server.svn.uri=svn://subversion.aepenergy.com/repos/bluestarenergy-parent/ecommerce-projects/microservice-projects/configuration-projects/ecommerce-server-configuration/branches/spring-boot-demo/src/main/resources/repository/demo -Decommerce.svn.username=jwong -Decommerce.svn.password=ThasPU4850 -Decommerce.app.home.config=/opt/spring/configuration -jar /opt/spring/deployment/aepe-ecommerce-server-configuration.jar" ]
