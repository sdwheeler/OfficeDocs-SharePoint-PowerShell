---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spenterprisesearchlanguageresourcephrase
applicable: SharePoint Server Subscription Edition
title: Get-SPEnterpriseSearchLanguageResourcePhrase
schema: 2.0.0
---

# Get-SPEnterpriseSearchLanguageResourcePhrase

## SYNOPSIS
Returns a language resource phrase.

## SYNTAX

```
Get-SPEnterpriseSearchLanguageResourcePhrase [-AssignmentCollection <SPAssignmentCollection>]
 [-Identity <LanguageResourcePhrasePipeBind>] [-Language <String>] [-Mapping <String>]
 -Owner <SearchObjectOwner> -SearchApplication <SearchServiceApplicationPipeBind> [-SourceId <Guid>]
 [-Type <LanguageResourceType>] [<CommonParameters>]
```

## DESCRIPTION
The Get-SPEnterpriseSearchLanguageResourcePhrase cmdlet reads a LanguageResourcePhrase object when the language resource phrase is created or deleted.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication 'Search Service Application'
Get-SPEnterpriseSearchLanguageResourcePhrase -SearchApplication $ssa -Language 'en-us' -Type QuerySuggestionBlockList
```

This example returns all language resource entries for the en-us language in the QuerySuggestionBlockList type.

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

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the language resource phrase to get.

The type must be a string; a valid name of a language resource phrase (for example, LanguageResourcePhrase1); or an instance of a valid LanguageResourcePhrase object.


```yaml
Type: LanguageResourcePhrasePipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Language

> Applicable: SharePoint Server Subscription Edition

Filters to return phrases of a specified source language.

The type must be a valid name of a language; for example, en-us or ja-jp.


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

### -Mapping

> Applicable: SharePoint Server Subscription Edition

Allows a term or phrase to be mapped to another term or phrase.
For example, the nickname "John" could be mapped to "Jonathan".

This parameter only applies to nicknames and substitutions.


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

### -Owner

> Applicable: SharePoint Server Subscription Edition

Specifies the search object owner that defines the scope at which the corresponding LanguageResourcePhrase is created.

The owner must be one of the following valid levels:

- Search Service Application
- Site Subscription
- Site Collection
- Site


```yaml
Type: SearchObjectOwner
Parameter Sets: (All)
Aliases: o

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the search application that contains the language resources.

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

### -SourceId

> Applicable: SharePoint Server Subscription Edition

Identifies the search result source for which the LanguageResourcePhrase applies to.


```yaml
Type: Guid
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

Filters to return phrases of a specified type.

The type must be one of the following valid types of phrases:

- QuerySuggestionBlockList
- QuerySuggestionAlwaysSuggest
- Nickname
- QuerySuggestionSubstitution


```yaml
Type: LanguageResourceType
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
