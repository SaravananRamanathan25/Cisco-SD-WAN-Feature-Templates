# Cisco SD-WAN - FeatureTemplate (REST API)
The Cisco SD-WAN Solution (a.k.a Viptela) is a cloud-delivered overlay SD-WAN architecture that facilitates digital and cloud transformation for enterprises and communication service providers (CSP). It significantly reduces WAN costs and time to deploy new services.

Cisco SD-WAN builds a API based architecture that's crucial for enterprises and CSPs to do the configuration automation through their internal tools.

The configuration of edge devices requires following templates to be created and group them under one device template before the template can be attached to an edge device

* Feature Templates
* Local Policy Template
* Security Policy Template

# Feature Template creation - POSTMAN Collection
This postman collection provides some example of various APIs dealing with Feature Templates.

This POSTMAN environment and collection that can be used to interact with the Cisco SD-WAN powered by Viptela vManage REST API. You can edit the variables in the environment to point to your own vManage instance. The collection contains REST API calls to authenticate, create feature templates for various features such as (AAA/BGP/OMP/System/VPNInterface).  Please note that the username should have write permission for "Template Configuration" Feature for the usergroup that it is associated with.

# Steps to execute APIs in the Postman Collection
* Clone or Download the JSON files "CiscoSD-WAN-FeatureTemplate.postman_collection.json" and "Cisco-SD-WAN-Environment.postman_environment.json"  
* Import above files to the POSTMAN  
* In the POSTMAN, make sure you set the environment as "Cisco-SD-WAN-Environment" in the top right corner ![SelectEnvDetails](https://github.com/SaravananRamanathan25/CiscoSD-WAN-FeatureTemplate/tree/master/Images/SelectEnvDetails-Postman.png)
* Go to Environment options and edit the vmanage, j_username, j_password and port details as per your own vmanage environment ![EditEnvDetails](https://github.com/SaravananRamanathan25/CiscoSD-WAN-FeatureTemplate/tree/master/Images/UpdateEnvDetails_Postman.png)
* First Execute API under "Feature Template\1.Authentication\Authentication".  This will make sure that you have logged into the vManage for that session
* Execute "Feature Template\2a. To Create AAA Feature Template\To Create AAA Feature Template", which will create a AAA feature template called "TestTemplate-AAA" for the device type "vedge-100-B".  On successful execution, vManage will return Template ID.
* Execute "Feature Template\2b. To Create BGP Feature Template\To Create BGP Feature Template", which will create a BGP feature template called "TestTemplate-bgp" for the device type "vedge-1000".  On successful execution, vManage will return Template ID.
* Execute "Feature Template\2c. To Create OMP Feature Template\To Create OMP Feature Template", which will create a OMP feature template called "TestTemplate-OMP" for the device type "vedge-1000".  On successful execution, vManage will return Template ID.
* Execute "Feature Template\2d. To Create System Feature Template\To Create System Feature Template", which will create a System feature template called "TestTemplate-System" for the device type "vedge-1000".  On successful execution, vManage will return Template ID.
* Execute "Feature Template\2e. To Create VPN Interface Feature Template\To Create VPN Interface Feature Template", which will create a VPN Interface feature template called "TestTemplate-OMP" for the device type "vedge-100-B".  On successful execution, vManage will return Template ID.
