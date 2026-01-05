FROM tomcat:8.5.16-jre8-alpine
RUN rm -rf /usr/local/tomcat/webapps/*
COPY target/*.war /usr/local/tomcat/webapps
RUN chmod 777 /usr/local/tomcat/webapps/*.war
CMD ["catalina.sh", "run"]
