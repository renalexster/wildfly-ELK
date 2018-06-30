FROM jboss/wildfly:10.1.0.Final

USER root

COPY modules/* /opt/jboss/wildfly/modules/org/jboss/logmanager/ext/main/

COPY standalone.xml /opt/jboss/wildfly/standalone/configuration

COPY modules/jboss-logmanager-ext-1.0.0.Alpha3.jar /opt/jboss/wildfly/standalone/deployments/jboss-logmanager-ext-1.0.0.Alpha3.jar

RUN chown -R jboss.jboss /opt/jboss

USER jboss

CMD ["/opt/jboss/wildfly/bin/standalone.sh", "-b0.0.0.0", "-bmanagement=0.0.0.0"]