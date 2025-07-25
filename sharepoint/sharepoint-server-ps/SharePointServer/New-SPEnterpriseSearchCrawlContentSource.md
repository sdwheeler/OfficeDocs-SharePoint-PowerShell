---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spenterprisesearchcrawlcontentsource
applicable: SharePoint Server Subscription Edition
title: New-SPEnterpriseSearchCrawlContentSource
schema: 2.0.0
---

# New-SPEnterpriseSearchCrawlContentSource

## SYNOPSIS
Creates a content source for a Search service application.

## SYNTAX

```
New-SPEnterpriseSearchCrawlContentSource [-AssignmentCollection <SPAssignmentCollection>]
 [-BDCApplicationProxyGroup <SPServiceApplicationProxyGroupPipeBind>] [-Confirm]
 [-CrawlPriority <CrawlPriority>] [-CustomProtocol <String>] [-LOBSystemSet <String[]>]
 [-MaxPageEnumerationDepth <Int32>] [-MaxSiteEnumerationDepth <Int32>] -Name <String>
 -SearchApplication <SearchServiceApplicationPipeBind> [-SharePointCrawlBehavior <SharePointCrawlBehavior>]
 [-StartAddresses <String>] [-Tag <String>] -Type <ContentSourceType> [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The New-SPEnterpriseSearchCrawlContentSource cmdlet creates a new content source.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication
New-SPEnterpriseSearchCrawlContentSource -SearchApplication $ssa -Type File -name FileServer -StartAddresses file://someserver/public
```

This example creates a new content source of type file to crawl a file system.

## PARAMETERS

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

### -BDCApplicationProxyGroup

> Applicable: SharePoint Server Subscription Edition

Specifies the proxy to use for a business type content source.
This proxy group must contain a default Business Data Connectivity Metadata Store proxy.


```yaml
Type: SPServiceApplicationProxyGroupPipeBind
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

### -CrawlPriority

> Applicable: SharePoint Server Subscription Edition

Specifies the priority of this content source.

The value must be one of the following integers: 1= Normal, 2=High.


```yaml
Type: CrawlPriority
Parameter Sets: (All)
Aliases: p

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomProtocol

> Applicable: SharePoint Server Subscription Edition

Specifies the custom protocol, handled by the custom connector, to use for this content source.


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

### -LOBSystemSet

> Applicable: SharePoint Server Subscription Edition

Specifies a comma-separated list of Business Data Connectivity metadata store system names and system instance names for a business type content source.


```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPageEnumerationDepth

> Applicable: SharePoint Server Subscription Edition

Specifies, for a web or custom type content source, the number of page hops that the crawler can make from the start address to a content item.


```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSiteEnumerationDepth

> Applicable: SharePoint Server Subscription Edition

Specifies, for a web or custom type content source, the number of site hops that the crawler can take from the start address to a content item.


```yaml
Type: Int32
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

Specifies the name of the content source to create.

The type must be a valid name of a ContentSource object (for example, ContentSource1).


```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the search application that contains the content source.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid Search service application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.


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

### -SharePointCrawlBehavior

> Applicable: SharePoint Server Subscription Edition

Specifies crawl behavior for a sharepoint type content source.
The behavior can be either:

CrawlSites to crawl only particular site collections.

CrawlVirtualServers to crawl the entire server and all site collections on the server.


```yaml
Type: SharePointCrawlBehavior
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartAddresses

> Applicable: SharePoint Server Subscription Edition

Specifies the comma-separated list of URLs at which to start a crawl for this content source.

The type must be a valid URL, in the form https://server_name.


```yaml
Type: String
Parameter Sets: (All)
Aliases: s

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag

> Applicable: SharePoint Server Subscription Edition

Specifies the URL for the page to modify the settings for a custom content source.
The string that specifies the URL can contain a maximum of 1,024 characters.

The type must be a valid URL, in the form https://server_name.


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

### -Type

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the content source type.
The value Business is for the Business Data Connectivity metadata store.
The value Exchange is for Microsoft Exchange public folders.
The value Custom is for a custom content source type.

The type must be the valid name of a content source type; for example, custom.


```yaml
Type: ContentSourceType
Parameter Sets: (All)
Aliases: t

Required: True
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
