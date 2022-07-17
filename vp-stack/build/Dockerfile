FROM maven:3.8.6-openjdk-8
LABEL Author=DevOps
WORKDIR /app
RUN git clone -b local-setup https://github.com/devopshydclub/vprofile-project.git
WORKDIR /app/vprofile-project
COPY ./application.properties ./src/main/resources/application.properties
COPY ./settings.xml .
RUN mvn -U -s ./settings.xml clean install
RUN ls -lrt ./target/
RUN mvn -U -s ./settings.xml deploy:deploy-file -DgroupId=container -DartifactId=vprofile -Dversion=v2 -DgeneratePom=true -Dpackaging=war -DrepositoryId=internet-mirror -Durl=http://epc.australiaeast.cloudapp.azure.com:9089/repository/maven-releases -Dfile=/app/vprofile-project/target/vprofile-v2.war
