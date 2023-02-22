FROM amazoncorretto:11.0.18
ENV TZ=America/Asuncion
ENV SNAP=procedure-ueno-0.0.1-SNAPSHOT
ENV TAGETDIR=target
ENV PORT=8080
WORKDIR /root/
RUN apk add --no-cache tzdata
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
COPY $TAGETDIR/$SNAP.jar app.jar
EXPOSE $PORT
ENTRYPOINT ["java","-jar","/app.jar"]
