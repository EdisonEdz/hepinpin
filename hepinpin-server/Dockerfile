FROM java:11
#作者
MAINTAINER EdisonZhang
#声明一个挂载点，容器内此路径会对应宿主机的某个文件夹
VOLUME /tmp
#复制上下文目录下的target/hepinpin-server-1.0-SNAPSHOT.jar 到容器里
COPY target/hepinpin-server-0.0.1-SNAPSHOT.jar hepinpin-server-0.0.1-SNAPSHOT.jar

#bash方式执行，使hepinpin-server-1.0-SNAPSHOT.jar可访问
#RUN新建立一层，在其上执行这些命令，执行结束后， commit 这一层的修改，构成新的镜像。
RUN bash -c "touch /hepinpin-server-0.0.1-SNAPSHOT.jar"

#声明运行时容器提供服务端口，这只是一个声明，在运行时并不会因为这个声明应用就会开启这个端口的服务
EXPOSE 8070

#指定容器启动程序及参数   <ENTRYPOINT> "<CMD>"
ENTRYPOINT ["java","-jar","hepinpin-server-0.0.1-SNAPSHOT.jar" ]
