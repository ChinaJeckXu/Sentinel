FROM registry.cn-hangzhou.aliyuncs.com/chinajeckxu/jdk-ubuntu:21.0.10
LABEL maintainer="chinajeckxu <chinajeckxu@163.com>"

# 复制本地已经存在的 JAR 文件
COPY target/sentinel-dashboard.jar /home/sentinel-dashboard.jar

ENV JAVA_OPTS '-Xms256M -Xmx512M -Dserver.port=8870 -Dcsp.sentinel.api.port=8719 -Dproject.name=Magical-Sentinel-Dashboard -Dsentinel.dashboard.auth.username=magical -Dsentinel.dashboard.auth.password=magical -Dcsp.sentinel.dashboard.server=localhost:8870 -Dserver.servlet.session.timeout=7200'

RUN chmod -R +x /home/sentinel-dashboard.jar

EXPOSE 8870

CMD java ${JAVA_OPTS} -jar /home/sentinel-dashboard.jar

