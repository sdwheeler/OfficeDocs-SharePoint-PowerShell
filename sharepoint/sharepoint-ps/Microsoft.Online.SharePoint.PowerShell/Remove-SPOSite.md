---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-sposite
applicable: SharePoint Online
title: Remove-SPOSite
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Remove-SPOSite

## SYNOPSIS

Sends a SharePoint Online site collection to the SharePoint Online Recycle Bin.

## SYNTAX

```
Remove-SPOSite -Identity <SpoSitePipeBind> [-NoWait] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The `Remove-SPOSite` cmdlet does not delete a site collection from the site collections list permanently.
Instead, the removed site collection is moved to the Recycle Bin.
You can use the `Restore-SPODeletedSite`cmdlet to restore a site collection from the Recycle Bin.
To delete a site collection permanently, first move the site collection to the Recycle Bin by using the `Remove-SPOSite` cmdlet and then delete it from the Recycle Bin by using the `Remove-SPODeletedSite` cmdlet.

You must be at least a SharePoint Online administrator and be a site collection administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### EXAMPLE 1

```powershell
Remove-SPOSite -Identity https://contoso.sharepoint.com/sites/site1 -NoWait
```

This example immediately removes the site collection named <https://contoso.sharepoint.com/sites/site1> from the site collections list and moves it to the Recycle Bin.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

Specifies the URL of the site collection to remove.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoWait

> Applicable: SharePoint Online

Specifies to continue executing script immediately.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Online

Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Online

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Remove-SPODeletedSite](Remove-SPODeletedSite.md)

[Restore-SPODeletedSite](Restore-SPODeletedSite.md)
