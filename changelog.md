# Changelog
All notable changes to this project will be documented in this file.


## 2019-12-06

### API Key

In the configuration file, a API Key is now available to be added. This will allow Audit Logs to be pulled from each 
server in the configuration file. 

Please see the following example:

    [cbdefense1]
    api_connector_id = GO5M953111
    api_key = BYCRM7BRNSH0CXZR5V1Y3111

> **Note**: These fields are not optional and must be present in the config file. If no API Key is needed, please 
leave the field blank as shown below:

    [cbdefense1]
    api_connector_id = 
    api_key = 


### Audit Logs

Audit Logs are now available to be pulled from the Syslog Connector. To set up the program to pull Audit Logs, please 
see the API Key section above. When the Syslog Connector is executing, the program will grab the Audit Logs that have 
been generated since the last time the Connector was run. The following file formats are compatible with Audit Logs: 
CEF,LEEF, JSON

> **Note**: All events types will be pulled from the Syslog Connector. As of now, no additional filtering is 
compatible for Audit Logs.


### ThreatHunter

ThreatHunter notifications are now available to be pulled from the Syslog Connector. To set up the Connector to pull 
ThreatHunter notifications you need to add the API Key as shown below in the configuration file: 


    cbdefense1]
    siem_connector_id = UEUWR4U111
    siem_api_key = XNS5UKWZXZMCC3CYC7DFM111


The file formats that are compatible with ThreatHunter Notifications are: LEEF, CEF, JSON. Just like with Audit Logs, the 
program will grab only the notifications that have been generated since the last time the Connector was run. 

> **Note**: All events types will be pulled from the Syslog Connector. As of now, no additional filtering is 
compatible for the ThreatHunter Notifications.



