#Posh-NVS
##Description
PowerShell v3 Module for intearcting with one or more Tenable Nessus Vulnerability Scanner Servers.

## Installation 
The module is written for PowerShell v3. This version of PowerShell is only available for:

* Windows 7
* Windows 2008  R2
* Windows 8
* Windows 2012

.Net Framework 4.0 must be installed before installing PSv3:

[http://www.microsoft.com/en-us/download/details.aspx?id=17718](http://www.microsoft.com/en-us/download/details.aspx?id=17718 ".Net Framework 4 installer")

PowerShell v3 is part of the latest Windows Management Framework:

[http://www.microsoft.com/en-us/download/details.aspx?id=34595](http://www.microsoft.com/en-us/download/details.aspx?id=34595)

Since the code is not signed the execution policy should be RemoteSigned to be able to run the module. From a PowerShell Session running as administrator run:
```
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Force
```
To install a module folder:

* Create a Modules directory for the current user if one does not exist. To create a Modules directory, type:

```
New-Item -Type Directory -Path $home\Documents\WindowsPowerShell\Modules
```

* Copy the entire module folder into the Modules directory.

The module can be loaded by executing the command:
```
Import-Module posh-nessus -Verbose -Force
```
It should print all the functions as they are loaded. You can make changes to the code and reload the module using the same command.

## ChangeLog

* Added Encryption type selection when configuring the mail server.
* Scan folder manipulation (Listing, Creation, Rename and Delete).
* Migrated to Get-NessusScan for scan listing and filtering.
* Moving a specied scan to a folder.
* Get MultiScanner Info
