# ACCOUNT FOR APPDYNAMICS
testing.jtimon@yopmail.com /// testing

# LOGIN PAGE FOR COOKIES
https://login.appdynamics.com/sso/authenticate/?site=download_serverusername=testing.jtimon@yopmail.com&password=testing
username=testing.jtimon@yopmail.com&password=testing
https://download.appdynamics.com/download/
https://download.appdynamics.com/download/prox/download-file/machine/4.3.5.13/MachineAgent-4.3.5.13.zip

# INFO 

oc new-build https://github.com/juantimonescalona/appdynamics-docker-images.git --context-dir=appd-machine --allow-missing-images --name=appdynamicsmachineagent

oc new-app appdynamics-docker-images/appd-machine --env-file /appd-machine/appdynamics.env

# Documentacion
https://docs.appdynamics.com/display/PRO43/Integrated+Docker+Visibility
https://docs.appdynamics.com/display/PRO43/Configuring+Docker+Visibility
https://docs.appdynamics.com/display/PRO42/Java+Agent+Configuration+Properties
https://download.appdynamics.com/download/prox/download-file/machine/4.3.5.13/MachineAgent-4.3.5.13.zip
