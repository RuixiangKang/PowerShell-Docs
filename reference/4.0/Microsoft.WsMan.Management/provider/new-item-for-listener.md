---
ms.date:  2017-06-09
schema:  2.0.0
locale:  en-us
keywords:  powershell,cmdlet
title:  New-Item for Listener
---

# New-Item for Listener
Creates a new item.  
  
## Syntax  
  
```  
New-Item -Address <string> -Transport <string> [-Hostname <string>] [-Enabled] [-URLPrefix <string>] [-CertificateThumbprint <string>] [-Confirm] [-WhatIf] [<CommonParameters>]  
  
```  
  
## Description  
 The [New-Item](../../microsoft.powershell.management/new-item.md) cmdlet creates a new item and sets its value. The types of items that can be created depend upon the location of the item. For example, in the file system, [New-Item](../../microsoft.powershell.management/new-item.md) is used to create files and folders. In the registry, [New-Item](../../microsoft.powershell.management/new-item.md) creates registry keys and entries.  
  
 New-Item can also set the value of the items that it creates. For example, when creating a new file, [New-Item](../../microsoft.powershell.management/new-item.md) can add initial content to the file.  
  
## Parameters  
  
### -Address <string\>  
 Specifies the address for which this listener was created. The value can be one of the following:  
  
 --The literal string "*". (The wildcard character (\*) makes the command bind all the IP addresses on all the network adapters.)  
  
 --The literal string "IP:" followed by a valid IP address in either IPv4 dotted-decimal format or in IPv6 cloned-hexadecimal format.  
  
 --The literal string "MAC:" followed by the MAC address of an adapter. For example: MAC:32-a3-58-90-be-cc.  
  
|||  
|-|-|  
|Required?|true|  
|Position?|named|  
|Default Value||  
|Accept Pipeline Input?|false|  
|Accept Wildcard Characters?|false|  
  
### -Transport <string\>  
 Specifies the transport to use to send and receive WS-Management protocol requests and responses. The value must be either HTTP or HTTPS.  
  
|||  
|-|-|  
|Required?|true|  
|Position?|named|  
|Default Value||  
|Accept Pipeline Input?|false|  
|Accept Wildcard Characters?|false|  
  
### -Hostname <string\>  
 Specifies the host name of the computer on which the WS-Management (WinRM) service is running. The value must be a fully qualified domain name, an IPv4 or IPv6 literal string, or a wildcard character.  
  
|||  
|-|-|  
|Required?|false|  
|Position?|named|  
|Default Value||  
|Accept Pipeline Input?|false|  
|Accept Wildcard Characters?|false|  
  
### -Enabled  
 Specifies whether the listener is enabled or disabled. The default is True.  
  
|||  
|-|-|  
|Required?|false|  
|Position?|named|  
|Default Value||  
|Accept Pipeline Input?|false|  
|Accept Wildcard Characters?|false|  
  
### -URLPrefix <string\>  
 A URL prefix on which to accept HTTP or HTTPS requests. This is a string containing only the characters a-z, A-Z, 9-0, underscore (_) and backslash (/). The string must not start with or end with a backslash (/). For example, if the computer name is SampleMachine, the WS-Management client would specify http://SampleMachine/URLPrefix in the destination address.  
  
|||  
|-|-|  
|Required?|false|  
|Position?|named|  
|Default Value||  
|Accept Pipeline Input?|false|  
|Accept Wildcard Characters?|false|  
  
### -CertificateThumbprint <string\>  
 Specifies the thumbprint of the service certificate.  
  
 This value represents the string of two-digit hexadecimal values in the Thumbprint field of the certificate. It specifies the digital public key certificate (X509) of a user account that has permission to perform this action. Certificates are used in client certificate-based authentication. They can be mapped only to local user accounts, and they do not work with domain accounts. To get a certificate thumbprint, use the [Get-Item](../../microsoft.powershell.management/get-item.md) or [Get-ChildItem](../../microsoft.powershell.management/get-childitem.md) cmdlets in the Windows PowerShell Cert: drive.  
  
|||  
|-|-|  
|Required?|false|  
|Position?|named|  
|Default Value||  
|Accept Pipeline Input?|false|  
|Accept Wildcard Characters?|false|  
  
### -Confirm  
 Prompts you for confirmation before executing the command.  
  
|||  
|-|-|  
|Required?|false|  
|Position?|named|  
|Default Value||  
|Accept Pipeline Input?|false|  
|Accept Wildcard Characters?|false|  
  
### -WhatIf  
 Describes what would happen if you executed the command without actually executing the command.  
  
|||  
|-|-|  
|Required?|false|  
|Position?|named|  
|Default Value||  
|Accept Pipeline Input?|false|  
|Accept Wildcard Characters?|false|  
  
### <CommonParameters\>  
 This cmdlet supports the common parameters: -Verbose, -Debug, -ErrorAction, -ErrorVariable, -OutBuffer, and -OutVariable. For more information, see [about_CommonParameters](../../microsoft.powershell.core/about/about_commonparameters.md).  
  
## Inputs and Outputs  
 The input type is the type of the objects that you can pipe to the cmdlet. The return type is the type of the objects that the cmdlet returns.  
  
|||  
|-|-|  
|Inputs|System.Object<br /><br /> You can pipe a value for the new item to the New-Item cmdlet.|  
|Outputs|Any|  
  
## Notes  
 The [New-Item](../../microsoft.powershell.management/new-item.md) cmdlet is designed to work with the data exposed by any provider. To list the providers available in your session, type "Get-PsProvider". For more information, see About_Providers.  
  
## Example 1  
  
```  
C:\PS>New-Item -Path WSMan:\localhost\Listener -Address * -Transport HTTP -force  
  
This command creates an HTTP listener on any IP address on the computer.  
  
```  
  
## See Also  
 [about_Providers](../../microsoft.powershell.core/about/about_providers.md)   
 [Get-Item](../../microsoft.powershell.management/get-item.md)   
 [Set-Item](../../microsoft.powershell.management/set-item.md)   
 [Remove-Item](../../microsoft.powershell.management/remove-item.md)   
 [Clear-Item](../../microsoft.powershell.management/clear-item.md)   
 [Invoke-Item](../../microsoft.powershell.management/invoke-item.md)   
 [Rename-Item](../../microsoft.powershell.management/rename-item.md)   
 [Move-Item](../../microsoft.powershell.management/move-item.md)   
 [Copy-Item](../../microsoft.powershell.management/copy-item.md)

