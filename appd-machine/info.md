# INFO 

oc new-build https://github.com/juantimonescalona/appdynamics-docker-images.git --context-dir=appd-machine --allow-missing-images --name=evobank/appdynamics-machine-agent

oc new-app appdynamics-docker-images/appd-machine --env-file /appd-machine/appdynamics.env

# Documentacion
https://docs.appdynamics.com/display/PRO43/Integrated+Docker+Visibility
https://docs.appdynamics.com/display/PRO43/Configuring+Docker+Visibility
https://docs.appdynamics.com/display/PRO42/Java+Agent+Configuration+Properties
https://download.appdynamics.com/download/prox/download-file/machine/4.3.5.13/MachineAgent-4.3.5.13.zip
