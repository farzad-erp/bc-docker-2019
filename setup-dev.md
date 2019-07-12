

install-module navcontainerhelper -force

#create user/password

$credential =  (get-credential -credential $env:USERNAME)

#fjalali - Poupart123!


new-navcontainer `
    -accept_eula `
    -containerName "bsuserpass01" `
    -imageName "mcr.microsoft.com/businesscentral/onprem:gb" `
    -useBestContainerOS `
    -credential $credential `
    -memoryLimit 4G `
    -doNotExportObjectsToText `
    -auth UserPassword `
    -shortcuts Desktop `
    -updateHosts `
    -assignPremiumPlan `
    -includeCSide `
    -licenseFile "C:\NAV license file\5120769.flf" 


<#
  starting container
  hostname is bsuserpass01
  publicdnsname is bsuserpass01
  using navuserpassword authentication
  starting local sql server
  starting internet information server
  creating self signed certificate
  self signed certificate thumbprint e8466821ef49640267e1dfa9fa6c2ca2fcd59477
  modifying service tier config file with instance specific settings
  starting service tier
  registering event sources
  creating dotnetcore web server instance
  using license file 'c:\run\my\license.flf'
  import license
  creating http download site
  setting sa password and enabling sa
  creating fjalali as sql user and add to sysadmin
  creating super user
  assign premium plan for fjalali
  container ip address: 172.17.101.104
  container hostname  : bsuserpass01
  container dns name  : bsuserpass01
  web client          : http://bsuserpass01/nav/
  dev. server         : http://bsuserpass01
  dev. serverinstance : nav
  
  files:
  http://bsuserpass01:8080/al-3.0.124247.vsix
  
  initialization took 43 seconds
  ready for connections!
  reading customsettings.config from bsuserpass01
  creating desktop shortcuts for bsuserpass01
  container bsuserpass01 successfully created
 #>
