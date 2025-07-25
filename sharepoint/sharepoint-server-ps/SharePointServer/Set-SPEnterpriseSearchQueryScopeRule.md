---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spenterprisesearchqueryscoperule
applicable: SharePoint Server Subscription Edition
title: Set-SPEnterpriseSearchQueryScopeRule
schema: 2.0.0
---

# Set-SPEnterpriseSearchQueryScopeRule

## SYNOPSIS
Sets the properties of a shared scope rule for a query scope.

## SYNTAX

```
Set-SPEnterpriseSearchQueryScopeRule [-Identity] <ScopeRulePipeBind> -Url <Uri>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-FilterBehavior <String>]
 [-ManagedPropertyName <String>] [-MatchingString <String>] [-PropertyValue <String>] [-Scope <ScopePipeBind>]
 [-SearchApplication <SearchServiceApplicationPipeBind>] [-UrlScopeRuleType <String>] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
After you upgrade a Search service application SharePoint Server, you can view shared scopes, but you cannot create, update, or delete them.
Therefore, you cannot use this cmdlet for shared scopes after upgrade.
However, you can convert shared scopes to result sources, which serve a similar purpose.
Similarly, after you upgrade a SharePoint Server site collection to SharePoint Server mode, you can view local scopes, but you cannot create, update, or delete them.
Therefore, you cannot use this cmdlet for local scopes after you upgrade a site collection.
However, you can convert local scopes to result sources, which serve a similar purpose.

The `Set-SPEnterpriseSearchQueryScopeRule` cmdlet updates the properties of a query scope.
SPEnterpriseSearchQueryScopeRule represents a query results scope rule that can be applied to a scope.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication
$scope = Get-SPEnterpriseSearchQueryScope -Identity MustCrawl -SearchApplication $ssa
Get-SPEnterpriseSearchQueryScopeRule -Scope $scope -Url https://criticalSite | Set-SPEnterpriseSearchQueryScopeRule -Url https://criticalSite -UrlScopeRuleType Url
```

This example gets a reference to a scope rule for the URL https://criticalSite and sets its rule type to Url.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the scope rule to update.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a scope rule (for example, ScopeRule1); or an instance a valid ScopeRule object.

```yaml
Type: ScopeRulePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Url

> Applicable: SharePoint Server Subscription Edition

Specifies the results URL that is associated with the query scope rule.

The type must be a valid URL, in the form https://server_name.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: u

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

### -FilterBehavior

> Applicable: SharePoint Server Subscription Edition

Specifies the type of scope rule to create for the query scope.

The type must be one of the following values: Exclude, Include, or Require.

```yaml
Type: String
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedPropertyName

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the managed property to use for the PropertyQuery scope rule.

The type must be a valid name of a managed property; for example, ManagedProp1.

```yaml
Type: String
Parameter Sets: (All)
Aliases: mname

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MatchingString

> Applicable: SharePoint Server Subscription Edition

Specifies the string to use when matching the URL rule type.

```yaml
Type: String
Parameter Sets: (All)
Aliases: text

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertyValue

> Applicable: SharePoint Server Subscription Edition

Specifies the property value to use when matching the PropertyQuery rule type.

```yaml
Type: String
Parameter Sets: (All)
Aliases: value

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope

> Applicable: SharePoint Server Subscription Edition

Applies the query scope rule to the specified scope.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a scope (for example, Scope1); or an instance of a valid Scope object.

```yaml
Type: ScopePipeBind
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the search application that contains the query scope rule collection.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UrlScopeRuleType

> Applicable: SharePoint Server Subscription Edition

Specifies the value to use when matching the URL rule type.

The type must be one of the following values: Folder, HostName, or Domain.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ut

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
