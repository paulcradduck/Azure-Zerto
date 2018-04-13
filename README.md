
[![Deploy to Azure](https://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fpaulcradduck%2FSplunk-Azure%2Fmaster%2Fazuredeploy.json)

This template deploys a single Zerto Appliance along with two subnets and one NSG. Once the deployment is complete, you will need to finish the Zerto Virtual Replication 6.0 setup and link it to your secondary site.

Below is the list of template parameters:

| Name   | Required | Description |
|:--- |:--- |:---|
| location | :heavy_check_mark: | Location where Azure resources will be created |
| storageAccountType | | Storage account type which determines data redundancy and underlying drive type. Defaults to `Standard_LRS` |
| adminUsername | :heavy_check_mark: | Admin username for the Zerto Appliance |
| adminPassword | :heavy_check_mark: | Admin password for the Zerto Appliance |
| virtualNetworkNewOrExisting | | Identifies whether to use new or existing Virtual Network. Allowed values: `new` (Default), `existing` 
| virtualNetworkName | :heavy_check_mark: | Name of the virtual network to be used |
| virtualNetworkAddressPrefix | | Virtual network address CIDR |
| subnet1Name | | Subnet for the Search Head |
| subnet2Name | | Subnet for the Indexers |
| subnet1Prefix | | Search Head subnet CIDR |
| subnet2Prefix | | Indexer subnet CIDR |
| subnet1StartAddress | | Search Head subnet start address |
| subnet2StartAddress | | Indexer subnet start address |
| publicIPName | | Name of the Search Head public IP address. Default: splunksh-publicip |



