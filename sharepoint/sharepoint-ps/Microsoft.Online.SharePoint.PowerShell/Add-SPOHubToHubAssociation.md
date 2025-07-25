---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/add-spohubtohubassociation
applicable: SharePoint Online
title: Add-SPOHubToHubAssociation
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Add-SPOHubToHubAssociation

## SYNOPSIS

Associates a hub site to a hub site.
Note: This feature is currently in preview and may not be available in your tenant.

## SYNTAX

```
Add-SPOHubToHubAssociation [-Source] <Guid> -Target <Guid> [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to associate a hub site to a hub site.

## EXAMPLES

### Example 1

```powershell
Add-SPOHubToHubAssociation -Source 7b6fd3a3-b029-4eb0-8e00-ba4a3949807d -Target 43a36572-37ec-45c3-9058-061a2db4cd26
```

This example associates the source hub site with the HubSiteId 7b6fd3a3-b029-4eb0-8e00-ba4a3949807d with the target hub site with the HubSiteId 43a36572-37ec-45c3-9058-061a2db4cd26.

## PARAMETERS

### -Source

> Applicable: SharePoint Online

HubSiteId of the Source Hub site to be associated with the Target Hub Site.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Target

> Applicable: SharePoint Online

HubSiteId of the Target Hub to associate the source Hub to.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### System.Guid

## OUTPUTS

### System.Object

## NOTES

SPOHubToHubAssociation is just a placeholder and not yet ready for production.

## RELATED LINKS

