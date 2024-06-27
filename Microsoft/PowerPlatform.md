[https://admin.microsoft.com/Adminportal/Home#/licenses](https://admin.microsoft.com/Adminportal/Home#/licenses) 

[https://admin.powerplatform.microsoft.com/ext/DataGateways](https://admin.powerplatform.microsoft.com/ext/DataGateways) 

[https://www.office.com/?auth=2](https://www.office.com/?auth=2) 

[https://home.dynamics.com/](https://home.dynamics.com/) 

1. Dynamics 365:-  
    
2. Power Automates: - [https://admin.flow.microsoft.com/environments](https://admin.flow.microsoft.com/environments) 
    
3. Power Apps: [https://admin.powerapps.com/environments](https://admin.powerapps.com/environments) 
    
4. PowerBI : [https://app.powerbi.com/admin-portal/capacities](https://app.powerbi.com/admin-portal/capacities) 
    

[https://outlook.office365.com/ecp/](https://outlook.office365.com/ecp/) 

[https://protection.office.com/homepage](https://protection.office.com/homepage) 

[https://devicemanagement.microsoft.com/](https://devicemanagement.microsoft.com/) 

[https://security.microsoft.com/homepage](https://security.microsoft.com/homepage)

[https://powerapps.microsoft.com/en-us/blog/gdpr-admin-powershell-cmdlets/](https://powerapps.microsoft.com/en-us/blog/gdpr-admin-powershell-cmdlets/)

[https://docs.microsoft.com/en-us/graph/tutorials/angular](https://docs.microsoft.com/en-us/graph/tutorials/angular) 

[Build Angular SPA's with Microsoft Graph - June 2019](https://www.youtube.com/watch?time_continue=673&v=KUPRTTOUzz8&feature=emb_logo)

https://www.youtube.com/watch?v=jT3bDt2qrHQ


[https://aad.portal.azure.com/](https://aad.portal.azure.com/) 

[https://docs.microsoft.com/en-us/graph/tutorials/angular?tutorial-step=1](https://docs.microsoft.com/en-us/graph/tutorials/angular?tutorial-step=1) 

[https://docs.microsoft.com/en-us/office/dev/add-ins/develop/sso-in-office-add-ins](https://docs.microsoft.com/en-us/office/dev/add-ins/develop/sso-in-office-add-ins) 

```
npm install -g office-toolbox 
```

[https://docs.microsoft.com/en-us/office/dev/add-ins/concepts/add-in-development-best-practices](https://docs.microsoft.com/en-us/office/dev/add-ins/concepts/add-in-development-best-practices) 

[https://github.com/officedev/office-add-in-nodejs-sso](https://github.com/officedev/office-add-in-nodejs-sso)

[https://azure.microsoft.com/en-us/status/](https://azure.microsoft.com/en-us/status/) 

[https://docs.microsoft.com/en-us/azure/app-service/app-service-web-get-started-nodejs](https://docs.microsoft.com/en-us/azure/app-service/app-service-web-get-started-nodejs) 

[https://docs.microsoft.com/en-us/azure/virtual-machines/windows/tutorial-manage-vm](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/tutorial-manage-vm) 

[https://docs.microsoft.com/en-us/learn/modules/principles-cloud-computing/3-benefits-of-cloud-computing](https://docs.microsoft.com/en-us/learn/modules/principles-cloud-computing/3-benefits-of-cloud-computing)





[https://docs.microsoft.com/en-us/learn/modules/welcome-to-azure/4-create-a-vm?pivots=windows-cloud](https://docs.microsoft.com/en-us/learn/modules/welcome-to-azure/4-create-a-vm?pivots=windows-cloud) 

az group create 

From <[https://docs.microsoft.com/en-us/learn/modules/welcome-to-azure/4-create-a-vm?pivots=windows-cloud](https://docs.microsoft.com/en-us/learn/modules/welcome-to-azure/4-create-a-vm?pivots=windows-cloud)>  

USERNAME=azureuser 

PASSWORD=$(openssl rand -base64 32) 

az vm create \ 

  --name myVM \ 

  --resource-group dc240593-69d7-40c1-878e-2a8d97f26ef8 \ 

  --image Win2016Datacenter \ 

  --size Standard_DS2_v2 \ 

  --location eastus \ 

  --admin-username $USERNAME \ 

  --admin-password $PASSWORD 

az vm get-instance-view \ 

  --name myVM \ 

  --resource-group dc240593-69d7-40c1-878e-2a8d97f26ef8 \ 

  --output table 

What's the Custom Script Extension? 

The Custom Script Extension is an easy way to download and run scripts on your Azure VMs.  

[https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-iis.ps1](https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-iis.ps1)? 

[https://docs.microsoft.com/en-us/learn/modules/welcome-to-azure/6-scale-up?pivots=windows-cloud](https://docs.microsoft.com/en-us/learn/modules/welcome-to-azure/6-scale-up?pivots=windows-cloud) 

Scaling up, or vertical scaling, means to increase the memory, storage, or compute power on an existing virtual machine. 

Scaling out, or horizontal scaling, means to add extra virtual machines to power your application.  

The cloud is elastic. You can scale down or scale in your deployment if you needed to scale up or scale out only temporarily. Scaling down or scaling in can help you save money.