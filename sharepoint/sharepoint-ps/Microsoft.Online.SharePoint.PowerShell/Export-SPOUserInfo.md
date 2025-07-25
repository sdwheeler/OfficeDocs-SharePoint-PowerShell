---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/export-spouserinfo
applicable: SharePoint Online
title: Export-SPOUserInfo
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Export-SPOUserInfo

## SYNOPSIS

Export user information from site user information list.

## SYNTAX

```
Export-SPOUserInfo -LoginName <String> -Site <SpoSitePipeBind> [-OutputFolder <String>] [<CommonParameters>]
```

## DESCRIPTION

Export user information from site user information list.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Export-SPOUserInfo -LoginName joe.healy@contoso.com -site https://contoso.sharepoint.com/sites/sc1 -OutputFolder "C:\users\admin\exportfolder"
```

Example 1 exports a user data who has the e-mail address joe.healy@contoso.com from the site collection <https://contoso.sharepoint.com/sites/sc1> to folder C:\users\admin\exportfolder.

### Example 2

```powershell
$sites = Get-SPOSite -IncludePersonalSite $true
$user = "joe.healy@contoso.com"
foreach ($site in $sites)
{
Export-SPOUserInfo -LoginName $user -site $site.Url -OutputFolder
"C:\users\admin\exportfolder"
}
```

Example 2 exports user data who has email address joe.healy@contoso.com from all site collections to folder C:\users\admin\exportfolder.

## PARAMETERS

### -LoginName

> Applicable: SharePoint Online

Specifies the login name of the user to export.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFolder

> Applicable: SharePoint Online

Target folder where the CSV file is generated.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Site

> Applicable: SharePoint Online

Specifies the URL of the site collection to which you want to export the user.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: (All)
Aliases:

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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[New-SPOSiteGroup](New-SPOSiteGroup.md)

[Get-SPOUser](Get-SPOUser.md)

[Set-SPOUser](Set-SPOUser.md)

[Remove-SPOUser](Remove-SPOUser.md)
