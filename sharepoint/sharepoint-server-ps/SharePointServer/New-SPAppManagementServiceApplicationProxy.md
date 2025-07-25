---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spappmanagementserviceapplicationproxy
applicable: SharePoint Server Subscription Edition
title: New-SPAppManagementServiceApplicationProxy
schema: 2.0.0
---

# New-SPAppManagementServiceApplicationProxy

## SYNOPSIS

Creates an App Management Service application proxy.


## SYNTAX

### ServiceApplication
```
New-SPAppManagementServiceApplicationProxy -ServiceApplication <SPServiceApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-Name <String>] [-UseDefaultProxyGroup] [-WhatIf]
 [<CommonParameters>]
```

### Uri
```
New-SPAppManagementServiceApplicationProxy -Uri <String> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-Name <String>] [-UseDefaultProxyGroup] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet parameter sets](https://learn.microsoft.com/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

Use the New-SPAppManagementServiceApplicationProxy cmdlet to create an App Management Service application proxy with the specified name for the specified App Management Service application or the specified endpoint.
Depending on the parameter value, it also adds the new proxy to the default proxy group.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$sa = New-SPAppManagementServiceApplication -Name AppManagement -DatabaseServer MyDatabaseServer -DatabaseName AppManagementDB -ApplicationPool MyServiceAppPool
New-SPAppManagementServiceApplicationProxy -Name AppManagementProxy -UseDefaultProxyGroup -ServiceApplication $sa
```

This example creates a new App Management Service application proxy named AppManagementProxy for the specified service application and adds the new App Management Service application proxy to the default proxy group.

## PARAMETERS

### -ServiceApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the App Management Service application for which you are creating the service application proxy.

```yaml
Type: SPServiceApplicationPipeBind
Parameter Sets: ServiceApplication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Uri

> Applicable: SharePoint Server Subscription Edition

Specifies the endpoint URI of the App Management Service application in which to create the service application proxy.

```yaml
Type: String
Parameter Sets: Uri
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

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the service application proxy to be created.
If a value is not provided, a default name is used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseDefaultProxyGroup

> Applicable: SharePoint Server Subscription Edition

Specifies whether to add the newly created service application proxy to the default proxy group.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

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

## OUTPUTS

## NOTES

## RELATED LINKS

[New-SPAppManagementServiceApplication](New-SPAppManagementServiceApplication.md)
