---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/remove-spsiteurl
applicable: SharePoint Server Subscription Edition
title: Remove-SPSiteURL
schema: 2.0.0
---

# Remove-SPSiteURL

## SYNOPSIS
Removes an URL mapping from the site.

## SYNTAX

```
Remove-SPSiteURL [-Url] <String> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
The `Remove-SPSiteUrl` cmdlet removes an URL mapping from the site.

The `Remove-SPSiteUrl` cmdlet only applies to the root site collection for a host name, that is, https://www.contoso.com.
This cmdlet cannot be directly run against a managed path site collection underneath the root, that is, https://www.contoso.com/sites/test.

You cannot remove the primary URL for a given site collection, which is typically defined as the first URL in the default zone.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Remove-SPSiteURL -Url https://contoso.sharepoint.com
```

This example removes the URL from the site collection, https://contoso.sharepoint.com.

## PARAMETERS

### -Url

> Applicable: SharePoint Server Subscription Edition

Specifies the URL to remove.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

[Get-SPSiteUrl](Get-SPSiteUrl.md)

[Set-SPSiteUrl](Set-SPSiteUrl.md)
