---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/remove-spwebapplicationappdomain
applicable: SharePoint Server Subscription Edition
title: Remove-SPWebApplicationAppDomain
schema: 2.0.0
---

# Remove-SPWebApplicationAppDomain

## SYNOPSIS
Deletes the AppDomain.

## SYNTAX

```
Remove-SPWebApplicationAppDomain [-Identity] <SPAppDomainPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Use the Remove-SPWebApplicationAppDomain cmdlet to delete the AppDomain for a specified zone or to delete all the app domains for the web application if no zone is specified.

This cmdlet also deletes the Internet Information Services (IIS) port binding if any was added for the WebApp/Zone combination.

## EXAMPLES

### EXAMPLE 1
```powershell
Remove-SPWebApplicationAppDomain -WebApplication https://www.contoso.com
```
Removes all of the app domains for the specified web application.

### EXAMPLE 2
```powershell
Remove-SPWebApplicationAppDomain -WebApplication https://www.contoso.com -Zone Internet
```
Removes the app domains for the internet zone for the specified web application.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the string of a domain name (that is, contoso.com) or a SPAppDomain object to remove.

```yaml
Type: SPAppDomainPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal. Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Server Subscription Edition

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Server Subscription Edition

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.SharePoint.Administration.SPAppCmdlets.SPAppDomainPipeBind
Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-SPWebApplicationAppDomain](Get-SPWebApplicationAppDomain.md)

[New-SPWebApplicationAppDomain](New-SPWebApplicationAppDomain.md)
