---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spotenantcdnenabled
applicable: SharePoint Online
title: Get-SPOTenantCdnEnabled
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPOTenantCdnEnabled

## SYNOPSIS

Returns whether Public content delivery network (CDN) or Private CDN is enabled on the tenant level. Requires Tenant administrator permissions.

## SYNTAX

```
Get-SPOTenantCdnEnabled -CdnType <SPOTenantCdnType> [<CommonParameters>]
```

## DESCRIPTION

Returns whether Public content delivery network (CDN) or Private CDN is enabled on the tenant level.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOTenantCdnEnabled -CdnType Public
```

The example returns a CDN with a type of public.

## PARAMETERS

### -CdnType

> Applicable: SharePoint Online

Specifies the CDN type. The valid values are Public or Private.

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SPOTenantCdnType
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
