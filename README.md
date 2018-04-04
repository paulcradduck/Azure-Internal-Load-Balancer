# Create 2 Virtual Machines under an Internal Load balancer and configures Load Balancing rules for the VMs

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fpaulcradduck%2FAzure-Internal-Load-Balancer%2Fmaster%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>

This Template Deploys an Internal Load balancer

This template also deploys a Storage Account, Virtual Network, Availability Set and Network Interfaces.

**Steps to deploy manually**

- Create a resource group: New-AzureResourceGroup -Name "ILB-DemoRG" -Location "West US"

- Modify the 2VMsinVnetWithILB-parameters file to update your subscriptionId and change naming convention

- Deploy: New-AzureResourceGroupDeployment –Name IPDep1 -ResourceGroupName ILB-DemoRG -TemplateFile 2VMsinVnetWithILB.json -TemplateParameterFile 2VMsinVnetWithILB-parameters.json
