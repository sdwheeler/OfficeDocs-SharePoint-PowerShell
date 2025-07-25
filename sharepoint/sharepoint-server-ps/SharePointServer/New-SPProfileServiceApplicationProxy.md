---
external help file: Microsoft.Office.Server.UserProfiles.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spprofileserviceapplicationproxy
applicable: SharePoint Server Subscription Edition
title: New-SPProfileServiceApplicationProxy
schema: 2.0.0
---

# New-SPProfileServiceApplicationProxy

## SYNOPSIS
Creates a User Profile Service application proxy on the local farm.

## SYNTAX

### Application
```
New-SPProfileServiceApplicationProxy -ServiceApplication <SPServiceApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-DefaultProxyGroup] [-Name <String>]
 [-PartitionMode] [-WhatIf] [<CommonParameters>]
```

### Uri
```
New-SPProfileServiceApplicationProxy -Uri <Uri> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-DefaultProxyGroup] [-Name <String>] [-PartitionMode] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet parameter sets](https://learn.microsoft.com/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

The `New-SPProfileServiceApplicationProxy` creates a User Profile Service application proxy on the local farm.
The proxy is added to the default proxy group for the local farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$sa = New-SPProfileServiceApplication -Name 'User Profile Service Application' -ApplicationPool 'SharePoint Web Services Default' -ProfileDBName Profile -SocialDBName Social -ProfileSyncDBname Sync
New-SPProfileServiceApplicationProxy -Name 'User Profile Service Application Proxy' -ServiceApplication $sa -DefaultProxyGroup
```

This example creates a new User Profile Service application proxy.

## PARAMETERS

### -ServiceApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the local User Profile Service application that is associated with the new proxy.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a subscription User Profile Service application (for example, ProfileSvcApp1); or an instance of a valid SPServiceApplication object.

```yaml
Type: SPServiceApplicationPipeBind
Parameter Sets: Application
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Uri

> Applicable: SharePoint Server Subscription Edition

The URI of the remote user profile service application this proxy should communicate with.
This value is required only if you plan to connect a User Profile Service application from a remote farm.

```yaml
Type: Uri
Parameter Sets: Uri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the `Stop-SPAssignment` command, an out-of-memory scenario can occur.

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

### -DefaultProxyGroup

> Applicable: SharePoint Server Subscription Edition

Specifies that the User Profile Service application proxy be added to the default proxy group for the local farm.

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

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the display name for the new User Profile Service application.
The name that you use must be a unique name of a User Profile Service application in this farm.
The name can be a maximum of 128 characters.

The type must be a name of a valid User Profile Service application proxy; for example, UserProfileSvcProxy1.

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

### -PartitionMode

> Applicable: SharePoint Server Subscription Edition

Specifies that the service application restrict data by site group.
After the PartitionMode parameter is set and the service application is created, it cannot be changed.

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
