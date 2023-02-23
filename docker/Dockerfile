FROM amazoncorretto:11.0.18
ENV TZ=America/Asuncion
ENV TAGETDIR=target
ENV PORT=8080
WORKDIR /root/
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
COPY $TAGETDIR/*.jar app.jar
EXPOSE $PORT
ENTRYPOINT ["java","-jar","/app.jar"]
