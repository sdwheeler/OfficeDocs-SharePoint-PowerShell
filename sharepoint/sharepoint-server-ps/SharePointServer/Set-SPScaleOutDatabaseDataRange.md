---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spscaleoutdatabasedatarange
applicable: SharePoint Server Subscription Edition
title: Set-SPScaleOutDatabaseDataRange
schema: 2.0.0
---

# Set-SPScaleOutDatabaseDataRange

## SYNOPSIS
Extends the range of a specified scale-out database.

## SYNTAX

```
Set-SPScaleOutDatabaseDataRange -Database <SPDatabasePipeBind> -IsUpperSubRange <Boolean>
 -Range <SPScaleOutDataRange> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-NewRangePoint <Byte[]>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Use the `Set-SPScaleOutDatabaseDataRange` cmdlet to extend the range of a specified scale-out database towards a specified direction.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$databases = Get-SPScaleOutDatabase -ServiceApplication $serviceApplication
$database = $databases[0]
$state = Get-SPScaleOutDatabaseDataState -Database $database
Set-SPScaleOutDatabaseDataRange -Database $database -Range $state.Range -NewRangePoint $null -IsUpperSubRange $true
```

This example extends the data range end point of the first database in the specified service application up to the maximum range point.

## PARAMETERS

### -Database

> Applicable: SharePoint Server Subscription Edition

Specifies the scale-out database to which to extend the data range.

```yaml
Type: SPDatabasePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsUpperSubRange

> Applicable: SharePoint Server Subscription Edition

Specifies whether to set the start or the end point of the data range with the specified value in the NewRangePoint parameter.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Range

> Applicable: SharePoint Server Subscription Edition

Specifies the expected data range of the scale-out database.

```yaml
Type: SPScaleOutDataRange
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

### -NewRangePoint

> Applicable: SharePoint Server Subscription Edition

Specifies the new start or end point of the database.

The maximum value is NULL.

```yaml
Type: Byte[]
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

[Set-SPScaleOutDatabaseDataSubRange](Set-SPScaleOutDatabaseDataSubRange.md)

[Get-SPScaleOutDatabase](Get-SPScaleOutDatabase.md)

[Get-SPScaleOutDatabaseDataState](Get-SPScaleOutDatabaseDataState.md)
