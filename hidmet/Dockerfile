FROM maven:latest as mavenbuild
WORKDIR /usr/src/
RUN git clone https://github.com/ivanristic/hidmet.git
WORKDIR /usr/src/hidmet/hidmetrest/
RUN mvn -B -s /usr/share/maven/ref/settings-docker.xml package -DskipTests -DserverName=cloud

FROM 127.0.0.1:5000/liberty-server AS production
WORKDIR /opt/ibm/wlp/usr/servers/defaultServer/dropins/
COPY --from=mavenbuild /usr/src/hidmet/hidmetrest/target/ROOT.war hidmet.war
