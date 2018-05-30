FROM websphere-liberty:kernel
COPY server.xml /config/
RUN installUtility install --acceptLicense defaultServer
WORKDIR /opt/ibm/wlp/lib/
RUN wget https://repo1.maven.org/maven2/mysql/mysql-connector-java/5.1.34/mysql-connector-java-5.1.34.jar
