FROM openjdk:8-jre-slim

RUN apt-get update && apt-get -y upgrade && apt-get install -y wget && apt-get install -y unzip && apt-get install -y apt-utils && apt-get install -y iproute2 && apt-get install -y procps && apt-get install -y sysstat && mkdir /opt/appdynamics

ENV APPD_AGENT_VERSION=4.3.5.13
#ENV APPDYNAMICS_AGENT_ACCOUNT_ACCESS_KEY
#ENV APPDYNAMICS_CONTROLLER_HOST_NAME
#ENV APPDYNAMICS_CONTROLLER_SSL_ENABLED
#ENV APPDYNAMICS_CONTROLLER_PORT
ENV MACHINE_AGENT_PROPERTIES=-Dappdynamics.sim.enabled=true -Dappdynamics.docker.enabled=true

ARG APPDYNAMICS_AGENT_ACCOUNT_ACCESS_KEY
ARG APPDYNAMICS_CONTROLLER_HOST_NAME
ARG APPDYNAMICS_CONTROLLER_SSL_ENABLED
ARG APPDYNAMICS_CONTROLLER_PORT
ARG MACHINE_AGENT_PROPERTIES

RUN wget -O /tmp/MachineAgent-${APPD_AGENT_VERSION}.zip https://download.appdynamics.com/download/prox/download-file/machine/${APPD_AGENT_VERSION}/MachineAgent-${APPD_AGENT_VERSION}.zip
RUN unzip -oq /tmp/MachineAgent-${APPD_AGENT_VERSION}.zip -d /opt/appdynamics

CMD ["sh", "-c", "java ${MACHINE_AGENT_PROPERTIES} -jar /opt/appdynamics/machineagent.jar"]
