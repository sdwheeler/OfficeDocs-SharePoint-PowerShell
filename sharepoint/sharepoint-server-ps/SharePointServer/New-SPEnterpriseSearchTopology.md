---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spenterprisesearchtopology
applicable: SharePoint Server Subscription Edition
title: New-SPEnterpriseSearchTopology
schema: 2.0.0
---

# New-SPEnterpriseSearchTopology

## SYNOPSIS
Creates a new search topology in the given search service application.

## SYNTAX

```
New-SPEnterpriseSearchTopology -SearchApplication <SearchServiceApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Clone] [-Confirm]
 [-SearchTopology <SearchTopologyPipeBind>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet creates a new, inactive search topology in the given search service application.
If the Clone switch is used, a cloned topology is created.
Otherwise, an empty topology is created.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication
New-SPEnterpriseSearchTopology -SearchApplication $ssa
```

This example creates a new, empty search topology in the search service application referenced by $ssa.

### EXAMPLE 2
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication
$topology = Get-SPEnterpriseSearchTopology -SearchApplication $ssa
New-SPEnterpriseSearchTopology -SearchApplication $ssa -Clone -SearchTopology $topology
```

This example creates a new search topology in the search service application referenced by $ssa by cloning the existing topology referenced by $topology.

## PARAMETERS

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the search application to which the search topology will belong.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
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

### -Clone

> Applicable: SharePoint Server Subscription Edition

Specifies that the new search topology is to be created by cloning an existing search topology.

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

### -Confirm

> Applicable: SharePoint Server Subscription Edition

Specifies that the new search topology is to be created by cloning an existing search topology.

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

### -SearchTopology

> Applicable: SharePoint Server Subscription Edition

Specifies the existing search topology of which the new topology will be a clone.

```yaml
Type: SearchTopologyPipeBind
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

[Get-SPEnterpriseSearchTopology](Get-SPEnterpriseSearchTopology.md)

[Set-SPEnterpriseSearchTopology](Set-SPEnterpriseSearchTopology.md)

[Remove-SPEnterpriseSearchTopology](Remove-SPEnterpriseSearchTopology.md)
