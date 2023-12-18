## Evaluation 

### Notes

1. Azure Event hub usage and cost needs to be tracked 
1. Disable Application insights and hence no new entries in AZ Log analytics 
1. Any services or reporting build on top of Log analytics will be broken 
1. Duplicate Persistant of logs is not a valid concerns 
1.  if you want to send resource and activity logs you can run the automated install form here to automatically set up an event hub in your Azure account to collect these logs and have them forwarded to DD.
https://docs.datadoghq.com/logs/guide/azure-logging-guide/?tab=automatedinstallation
This will give further info on the Web Apps/Functions themselves from an infrastructure perspective
1. Need to have organization’s tag policies https://docs.datadoghq.com/monitors/settings/#tag-policies

### Azure integration for enabling APM

[<img width="40px" src="../image/az-dd-trace-arch.png">](https://docs.datadoghq.com/serverless/azure_app_services/azure_app_services_windows/?tab=net#programmatic-management)

### Status of features enable

<iframe src="https://cyncly-my.sharepoint.com/:x:/r/personal/jestha_wangkheirakpam_cyncly_com/Documents/Enabling%20dd%20in%20ADEO%20instance%20-%20timeline.xlsx?d=wf794fe771d784fa0bab1eb1ecfca27d1&csf=1&web=1&e=pyusVA&nav=MTVfezJBNjcwMkQ4LUVDMjktNDY2Ni1COEFBLUU5OTg1Rjg5M0U1MX0" title="status report"></iframe>