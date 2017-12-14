# APPDYNAMICS
testing.jtimon@yopmail.com /// testing
https://download.appdynamics.com/download/prox/download-file/machine/4.3.5.13/MachineAgent-4.3.5.13.zip

# INFO BUILD 

oc new-build https://github.com/juantimonescalona/appdynamics-docker-images.git --context-dir=appd-machine --allow-missing-images --name=appdynamicsmachineagent

oc new-app appdynamicsmachineagent

Falta los volumenes -v /:/hostroot:ro -v /var/run/docker.sock:/var/run/docker.sock \


# Documentacion
https://docs.appdynamics.com/display/PRO43/Integrated+Docker+Visibility
https://docs.appdynamics.com/display/PRO43/Configuring+Docker+Visibility
https://docs.appdynamics.com/display/PRO42/Java+Agent+Configuration+Properties
https://download.appdynamics.com/download/prox/download-file/machine/4.3.5.13/MachineAgent-4.3.5.13.zip
