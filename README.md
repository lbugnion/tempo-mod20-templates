# MOD20 

## Initial deployment

The deployment for this session is split in two parts:

- [Data source](#datasource): This deployment installs two virtual machines; a Linux VM running MongoDB for the shopping cart; and a Windows Server 2012 VM running SQL Server 2012 for the products. These VMs are the source of the migration.

- [Platform as a Service](#paas): This deployment installs the following services:
    - An Azure SQL server with two databases. The first database will be the target of the migration for the products. The second database is a backup that will be used during the demo in case the migration fails for any reason.
    - A CosmosDB database which will be used as the target of the migration for the shopping cart.
    - Another CosmosDB database as a backup that will be used during the demo in case the migration fails for any reason.
    - The front-end website connecting to the databases to show the catalog.
    - A storage account we'll use to configure advanced security features for the SQL database.
    - The Azure Database Migration Service we'll use for the demo.

The idea of the automated deployment is that you can deploy and delete the resources as often as you need.

<a id="datasource"></a>
### Data source (Virtual Machines, IaaS)

In order to install the virtual machines that will be used as the source of the migration for the demo, follow these steps:

1. Click on the button below to open the deployment page.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Flbugnion%2Ftempo-mod20-templates%2Fmaster%2Fazuredeploy-vms.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>

2. In the template page, enter the following information:

    - 

<a id="paas"></a>
### PaaS (website, Cosmos, Azure SQL, DMS)

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Flbugnion%2Ftempo-mod20-templates%2Fmaster%2Fazuredeploy-paas.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
