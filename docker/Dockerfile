FROM amazoncorretto:11.0.18
ENV TZ=America/Asuncion
WORKDIR /root/
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
COPY ../target/*.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java","-jar","/app.jar"]
