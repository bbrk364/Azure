# ![azureautomation2](https://cloud.githubusercontent.com/assets/6964549/17082193/9aade278-517d-11e6-8db1-1f04fb786e81.png)Microsoft Azure PowerShell Repo

### SCRIPTS

|No|Script|Description|
|----|----|----|
|1|[<b>Deploy-AzureVm.ps1</b>](https://github.com/rgel/Azure/blob/master/Deploy-AzureVm.ps1)|Deploy multiple Azure Iaas VM from [JSON](https://github.com/rgel/Azure/tree/master/JSON) templates|
|2|[<b>New-SecureCred.ps1</b>](https://github.com/rgel/Azure/blob/master/New-SecureCred.ps1)|Create file that contains encrypted password for Azure VM local admin account. The `adminPassword` parameter from [JSON](https://github.com/rgel/Azure/tree/master/JSON) templates|
|3|[<b>Apply-AzVmPowerStatePolicy.ps1</b>](https://github.com/rgel/Azure/blob/master/Apply-AzVmPowerStatePolicy.ps1)|[Start/Stop](https://ps1code.com/2017/06/28/stop-start-azure-vm-schedule) Azure VM in parallel on schedule based on two VM Tags (`PowerOn`/`PowerOff`)|

##
### MODULES

### [<ins>Az-Module</ins>](https://github.com/rgel/Azure/tree/master/Az-Module) Azure Automation PowerShell Module

<ins>Requirements:</ins> PowerShell 5 or above. To check, type the following command: `$PSVersionTable.PSVersion.Major`.

To install this module, drop the entire '<b>Az-Module</b>' folder into one of your module directories.

The default PowerShell module paths are listed in the `$env:PSModulePath` environment variable.

To make it look better, split the paths in this manner: `$env:PSModulePath -split ';'`

The default per-user module path is: `"$env:HOMEDRIVE$env:HOMEPATH\Documents\WindowsPowerShell\Modules"`.

The default computer-level module path is: `"$env:windir\System32\WindowsPowerShell\v1.0\Modules"`.

To use the module, type following command: `Import-Module Az-Module -Force -Verbose`.

To see the commands imported, type `Get-Command -Module Az-Module`.

For help on each individual cmdlet or function, run `Get-Help CmdletName -Full [-Online][-Examples]`.

To start using the module functions:

+ Install <b>Azure Resource Manager Module</b> module from Microsoft PSGallery by `Install-Module AzureRm`.
+ Connect to your Azure account by `Login-AzureRmAccount` cmdlet.
+ Optionally, select your target subscription by `Select-AzSubscription` function.

|No|Function|Description|
|----|----|----|
|1|<b>Select-AzSubscription</b>|Interactively select Azure Subscription|
|2|[<b>Select-AzResourceGroup</b>](https://ps1code.com/2017/06/29/azure-vm-tags)|Interactively select Azure ResourceGroup name|
|3|<b>Select-AzLocation</b>|Interactively select Azure Location|
|4|[<b>Select-AzObject</b>](https://ps1code.com/2017/06/29/azure-vm-tags)|Interactively select an Azure object (`VM`, `StorageAccount`, `VNET`, `AvailabilitySet`)|
|5|[<b>New-AzCredProfile</b>](https://ps1code.com/2017/07/05/login-to-azure-automatically)|Set your PowerShell session to automatically login to the Azure|
|6|[<b>Get-AzOrphanedVhd</b>](https://ps1code.com/2017/07/05/azure-orphaned-vhd)|Find Azure orphaned `*.VHD` files|
|7|[<b>Get-AzSubnet</b>](https://ps1code.com/2017/10/30/azure-ipam-powershell)|Get busy IP in Azure Subnets|
|8|<b>Get-AzVmPowerState</b>|Get Azure VM Power State|
|9|[<b>Get-AzVmTag / Add-AzVmTag</b>](https://ps1code.com/2017/06/29/azure-vm-tags)|Get/Add/Set Azure VM Resource Tag(s)|
|10|[<b>Get-AzVmDisk</b>](https://ps1code.com/2017/07/05/azure-vm-add-data-disk)|Get Azure VM Virtual Disks (`OSDisk`, `DataDisk`, `All`)|
|11|[<b>New-AzVmDisk</b>](https://ps1code.com/2017/07/05/azure-vm-add-data-disk)|Add a new `DataDisk` to an Azure VM|
|12|[<b>Expand-AzVmDisk</b>](https://ps1code.com/2017/10/24/azure-vm-increase-disk)|Increase Azure VM disks|
|13|[<b>New-AzParamsJson</b>](https://ps1code.com/2018/02/01/azure-json-parameter-files)|Create Azure JSON parameter files|

##
Stay tuned for the updates!
