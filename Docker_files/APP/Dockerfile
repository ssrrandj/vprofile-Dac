FROM openjdk:11 AS war_build
RUN apt update && apt install maven git -y
RUN git clone https://github.com/ssrrandj/vprofile-Dac.git
RUN cd vprofile-Dac && mvn install

FROM tomcat
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=war_build vprofile-Dac/target/*.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8081
CMD ["catalina.sh","run"]