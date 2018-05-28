FROM sonarqube:7.1

ARG PROXY_HOST
ARG PROXY_PORT
ARG PROXY_USER
ARG PROXY_PASSWORD

# for Proxy Basic Authentication
RUN sed -i -e "s/jdk.http.auth.tunneling.disabledSchemes=Basic/#jdk.http.auth.tunneling.disabledSchemes=Basic/g" /etc/java-8-openjdk/net.properties
RUN sed -i -e "s/#http.proxyHost=/http.proxyHost=$PROXY_HOST/g" /opt/sonarqube/conf/sonar.properties
RUN sed -i -e "s/#http.proxyPort=/http.proxyPort=$PROXY_PORT/g" /opt/sonarqube/conf/sonar.properties
RUN sed -i -e "s/#http.proxyUser=/http.proxyUser=$PROXY_USER/g" /opt/sonarqube/conf/sonar.properties
RUN sed -i -e "s/#http.proxyPassword=/http.proxyPassword=$PROXY_PASSWORD/g" /opt/sonarqube/conf/sonar.properties
