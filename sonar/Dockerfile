FROM sonarqube:latest

WORKDIR $SONARQUBE_HOME/extensions/plugins

RUN set -x \
&& curl -fSL -o sonar-cxx-plugin-0.9.7.jar https://github.com/SonarOpenCommunity/sonar-cxx/releases/download/cxx-0.9.7/sonar-cxx-plugin-0.9.7.jar

VOLUME ["$SONARQUBE_HOME/data", "$SONARQUBE_HOME/extensions"]

WORKDIR $SONARQUBE_HOME

ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]