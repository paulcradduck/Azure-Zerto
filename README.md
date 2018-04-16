[![Deploy to Azure](https://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fpaulcradduck%2FAzure-Zerto%2Fmaster%2Fazuredeploy.json)

This template deploys a single Zerto Appliance along with two subnets and one NSG. Once the deployment is complete, you will need to finish the Zerto Virtual Replication 6.0 setup and link it to your secondary site.

Below is the list of template parameters:

| Name   | Required | Description |
|:--- |:--- |:---|
| location | :heavy_check_mark: | Location where Azure resources will be created |
| adminUsername | :heavy_check_mark: | Admin username for the Zerto Appliance |
| adminPassword | :heavy_check_mark: | Admin password for the Zerto Appliance |
| virtualNetworkName | :heavy_check_mark: | Name of the virtual network to be used |
| virtualNetworkAddressPrefix | :heavy_check_mark: | Virtual network address CIDR |
| subnet1Name | :heavy_check_mark: | Subnet for the Zerto Virtual Appliance |
| subnet2Name | :heavy_check_mark: | Subnet for VMs to be recovered into |
| subnet1Prefix |:heavy_check_mark: | Zerto Virtual Appliance Head subnet CIDR |
| subnet2Prefix |:heavy_check_mark: | Recovery subnet CIDR |
| publicIPName | :heavy_check_mark: | Name of the Zerto Virtual Appliance public IP address. Default: zvm-publicIp |
| SourceIP | | This is the IP address that will be allowed to access the Zerto Appliance over the internet via RDP on 3389 |



