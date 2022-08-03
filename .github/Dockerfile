FROM openjdk:8-jre-alpine
MAINTAINER lksun.cn

ADD ./target/*.jar root.jar


ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/${TZ} /etc/localtime && echo ${TZ} > /etc/timezone
RUN mkdir "/logs"

EXPOSE 8080

ENTRYPOINT [ "java", "-Djava.security.egd=file:/dev/./urandom ","-Ddruid.mysql.usePingMethod=false",  "-jar" ,"/root.jar"]
