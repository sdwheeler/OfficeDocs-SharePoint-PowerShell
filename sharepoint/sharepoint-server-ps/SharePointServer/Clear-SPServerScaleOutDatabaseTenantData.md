---
external help file: Microsoft.Office.Server.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/clear-spserverscaleoutdatabasetenantdata
applicable: SharePoint Server Subscription Edition
title: Clear-SPServerScaleOutDatabaseTenantData
schema: 2.0.0
---

# Clear-SPServerScaleOutDatabaseTenantData

## SYNOPSIS

Removes all data related to the specified site subscription.

## SYNTAX

```
Clear-SPServerScaleOutDatabaseTenantData -ServiceApplication <SPServiceApplicationPipeBind>
 -SiteSubscriptionId <Guid> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION

Use the Clear-SPServerScaleOutDatabaseTenantData cmdlet removes all data related to the specified site subscription from the specified service application.



## EXAMPLES

### EXAMPLE
```powershell
Clear-SPServerScaleOutDatabaseTenantData -ServiceApplication $serviceApplication -SiteSubscriptionId "5CAF2F99-A75F-4239-B9CD-7FE63D1CE904"
```

This example clears all data related to the site subscription with id 5CAF2F99-A75F-4239-B9CD-7FE63D1CE904 from the specified service application.

## PARAMETERS

### -ServiceApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the service application in which to clear data.

```yaml
Type: SPServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSubscriptionId

> Applicable: SharePoint Server Subscription Edition

Specifies the site subscription id of the site subscription in which to clear data.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

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

Prompts you for confirmation before executing the command.
For more information, type the following command: `get-help about_commonparameters`

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

Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: `get-help about_commonparameters`

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

### Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Export-SPServerScaleOutDatabaseTenantData](Export-SPServerScaleOutDatabaseTenantData.md)

[Import-SPServerScaleOutDatabaseTenantData](Import-SPServerScaleOutDatabaseTenantData.md)
