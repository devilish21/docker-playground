FROM tomcat:8-jre11
RUN rm -rf /usr/local/tomcat/webapps/ROOT* &&\
    rm -rf /usr/local/tomcat/webapps.dist/ROOT* &&\
curl -u admin:admin -X GET http://epc.australiaeast.cloudapp.azure.com:9089/repository/maven-releases/container/vprofile/v2/vprofile-v2.war --output vprofile-v2.war
RUN cp vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war && cp vprofile-v2.war /usr/local/tomcat/webapps.dist/ROOT.war