---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spenterprisesearchqueryspellingcorrection
applicable: SharePoint Server Subscription Edition
title: Get-SPEnterpriseSearchQuerySpellingCorrection
schema: 2.0.0
---

# Get-SPEnterpriseSearchQuerySpellingCorrection

## SYNOPSIS
Returns the object that exposes the Query Spelling Correction (QSC) configuration.

## SYNTAX

```
Get-SPEnterpriseSearchQuerySpellingCorrection [[-Identity] <QuerySpellingCorrectionPipeBind>]
 -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet returns the object that exposes the QSC configuration parameters.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication
Get-SPEnterpriseSearchQuerySpellingCorrection -SearchApplication $ssa
```

Returns the current configuration for the Query Spelling Correction component for the default search service application.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies an object that represents the current status for the query spelling correction.

```yaml
Type: QuerySpellingCorrectionPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the search service application that contains the query spelling correction parameters.

```yaml
Type: SearchServiceApplicationPipeBind
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
