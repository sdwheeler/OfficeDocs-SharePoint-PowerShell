---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spenterprisesearchcrawlmapping
applicable: SharePoint Server Subscription Edition
title: New-SPEnterpriseSearchCrawlMapping
schema: 2.0.0
---

# New-SPEnterpriseSearchCrawlMapping

## SYNOPSIS
Creates a crawl mapping rule for a shared search application.

## SYNTAX

```
New-SPEnterpriseSearchCrawlMapping [-Url] <String> -SearchApplication <SearchServiceApplicationPipeBind>
 -Target <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION

The New-SPEnterpriseSearchCrawlMapping cmdlet is run when the search functionality is initially configured, and when access is changed through a different mechanism to create the crawl mapping rule; for example, when a rule is changed to use file:\\\\ rather than  http://.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).


## EXAMPLES

### EXAMPLE
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication
New-SPEnterpriseSearchCrawlMapping -SearchApplication $ssa -Url "file://location1" -Target "https://location2"
```

This example will change the query results link from the file share where the item was crawled to the Web site location from which the item can be browsed.

## PARAMETERS

### -Url

> Applicable: SharePoint Server Subscription Edition

Specifies the source URI for the crawl mapping.

The type must be a valid URL, in the form https://server_name.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the search application that contains the crawl mapping collection.

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

### -Target

> Applicable: SharePoint Server Subscription Edition

Specifies the target URI for the crawl mapping to get.

The type must be a valid URI; for example, file:\\\\ server_name\sitedocs.

```yaml
Type: String
Parameter Sets: (All)
Aliases: t

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

## OUTPUTS

## NOTES

## RELATED LINKS
