FROM openjdk:8-jre-slim
RUN apt-get update && apt-get -y upgrade && apt-get install -y unzip && apt-get install -y apt-utils && apt-get install -y iproute2 && apt-get install -y procps && apt-get install -y sysstat && mkdir /opt/appdynamics
ARG APPD_AGENT_VERSION = 4.3.5.13

RUN wget https://download.appdynamics.com/download/prox/download-file/machine/${APPD_AGENT_VERSION}/MachineAgent-${APPD_AGENT_VERSION}.zip
RUN unzip -oq MachineAgent-${APPD_AGENT_VERSION}.zip -d /opt/appdynamics

CMD ["sh", "-c", "java ${MACHINE_AGENT_PROPERTIES} -jar /opt/appdynamics/machineagent.jar"]
