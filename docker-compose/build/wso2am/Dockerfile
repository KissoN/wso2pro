FROM dhr.thprom.ru:5000/java-oracle-perf:8u66

RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

RUN wget --no-verbose --no-check-certificate http://nexus.egron.net:8081/nexus/service/local/repositories/thirdparty/content/org/wso2/wso2am/2.0.0/wso2am-2.0.0.zip -O /tmp/wso2am.zip
#COPY wso2am-2.0.0.zip /tmp/wso2am.zip
RUN sudo apt-get update && sudo apt-get install unzip && unzip /tmp/wso2am.zip -d /opt &&\
    rm -f /tmp/wso2am.zip

EXPOSE 9443

CMD ["/opt/wso2am-2.0.0/bin/wso2server.sh"]