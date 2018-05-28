FROM tomcat:8-jre8

MAINTAINER hiroshis <hiroshis.bamboo@gmail.com>

ADD postgresql-42.2.2.jar /usr/local/tomcat/lib/
ADD tomcat-users.xml /usr/local/tomcat/conf/
ADD catalina.properties /usr/local/tomcat/conf/
ADD context.xml /usr/local/tomcat/webapps/manager/META-INF/context.xml

CMD ["catalina.sh", "run"]
