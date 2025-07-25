---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spserver
applicable: SharePoint Server Subscription Edition
title: Get-SPServer
schema: 2.0.0
---

# Get-SPServer

## SYNOPSIS
Returns the server or servers in the farm that match the given identity.

## SYNTAX

```
Get-SPServer [[-Identity] <SPServerPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
 [<CommonParameters>]
```

## DESCRIPTION
The Get-SPServer cmdlet returns the SPServer object for the given identity (if it exists in the farm).
If no parameters are specified, the cmdlet returns all servers in the farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Get-SPServer
```

This example returns all servers in the local farm in a list.

### EXAMPLE 2
```powershell
Get-SPServer | Where{ $_.NeedsUpgrade -eq $TRUE}
```

This example returns a list of all servers in the farm that need an upgrade.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the address of the server to return.

```yaml
Type: SPServerPipeBind
Parameter Sets: (All)
Aliases: Address

Required: False
Position: 1
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
