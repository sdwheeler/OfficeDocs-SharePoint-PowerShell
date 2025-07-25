---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spenterprisesearchcrawlextension
applicable: SharePoint Server Subscription Edition
title: Get-SPEnterpriseSearchCrawlExtension
schema: 2.0.0
---

# Get-SPEnterpriseSearchCrawlExtension

## SYNOPSIS
Returns the file types to be included in the content index.

## SYNTAX

```
Get-SPEnterpriseSearchCrawlExtension [[-Identity] <ExtensionPipeBind>]
 -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [<CommonParameters>]
```

## DESCRIPTION
The Get-SPEnterpriseSearchCrawlExtension cmdlet returns any or all file extensions in the index for a search application.

Run this cmdlet at the initial search configuration, and after any new IFilter interface is added to read the rule when you create, update, or delete the extension rule.
If the Identity parameter is not specified, this cmdlet returns the crawl extension collection for the specified search application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### Add code example.
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication 'Search Service Application'
Get-SPEnterpriseSearchCrawlExtension -Identity 'pdf' -SearchApplication $ssa
```

This example checks whether the pdf file type is included in the file types to be included in the content index.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the file name extension to get.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid file name extension (for example, .xml); or an instance of a valid CrawlExtension object.

```yaml
Type: ExtensionPipeBind
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

Specifies the search application that contains the extension collection.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
