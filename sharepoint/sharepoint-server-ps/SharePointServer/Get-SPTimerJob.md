---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-sptimerjob
applicable: SharePoint Server Subscription Edition
title: Get-SPTimerJob
schema: 2.0.0
---

# Get-SPTimerJob

## SYNOPSIS

Returns timer jobs.

## SYNTAX

```
Get-SPTimerJob [[-Identity] <SPTimerJobPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
 [-Type <String>] [-WebApplication <SPWebApplicationPipeBind>] [<CommonParameters>]
```

## DESCRIPTION
The Get-SPTimerJob cmdlet reads a specified timer job, timer jobs of a specified type, or timer jobs defined for a specified scope.

If no parameters are specified, this cmdlet returns all timer job definitions for the farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES
### EXAMPLE 01
```powershell
Get-SPTimerJob -WebApplication "https://servername" | select Name, DisplayName
```

This example displays all timer jobs for a specified Web application.

### EXAMPLE 02
```powershell
Get-SPTimerJob | select -ExpandProperty HistoryEntries
```
The above example will show you timer job run history

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the timer job to get.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a timer job (for example, TimerJob1); or an instance of a valid SPTimerJob object.

```yaml
Type: SPTimerJobPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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

### -Type

> Applicable: SharePoint Server Subscription Edition

Filters to return timer jobs of a specified type.

The type must be a name of a valid timer job type; for example, TimerJob1.

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

### -WebApplication

> Applicable: SharePoint Server Subscription Edition

Filters to return timer jobs defined for the scope of a specified SharePoint Web application.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint Web application (for example, MyOfficeApp1); or an instance of a valid SPWebApplication object.

```yaml
Type: SPWebApplicationPipeBind
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
