---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-sppendingupgradeactions
applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: Get-SPPendingUpgradeActions
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Get-SPPendingUpgradeActions

## SYNOPSIS

Displays pending upgrade actions.


## SYNTAX

```
Get-SPPendingUpgradeActions [-RootObject] <IUpgradable> [-AssignmentCollection <SPAssignmentCollection>]
 [-Recursive] [-SkipSiteUpgradeActionInfo] [<CommonParameters>]
```

## DESCRIPTION
Use the Get-SPPendingUpgradeActions cmdlet to display the current pending upgrade actions for the farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```
Get-SPFarm | Get-SPPendingUpgradeActions -Recursive
```

## PARAMETERS

### -RootObject

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies a SharePoint object where you check for which upgrade actions are outstanding for that object based on its current upgrade status.

This object must be inherited from IUpgradable.

```yaml
Type: IUpgradable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### -Recursive

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies whether to perform the same pending upgrade action checks on each IUpgradable object that occurs under the RootObject parameter that is specified.

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

### -SkipSiteUpgradeActionInfo

> Applicable: SharePoint Server 2016, SharePoint Server 2019

Specifies to not include pending upgrade actions for all child objects of a content database.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
