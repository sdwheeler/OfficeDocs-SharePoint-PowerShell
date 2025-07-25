---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-sposite
applicable: SharePoint Online
title: Get-SPOSite
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPOSite

## SYNOPSIS

Returns one or more site collections.

## SYNTAX

### ParamSet1 (Default)
```
Get-SPOSite [[-Identity] <SpoSitePipeBind>] [-Limit <String>] [-Detailed] [<CommonParameters>]
```

### ParamSet3
```
Get-SPOSite [-Identity] <SpoSitePipeBind> [-DisableSharingForNonOwnersStatus] [<CommonParameters>]
```

### ParamSet2
```
Get-SPOSite [-Filter <String>] [-Limit <String>] [-Detailed] [-Template <String>]
 [-IncludePersonalSite <Boolean>] [-GroupIdDefined <Boolean>] [-ArchiveStatus <ArchiveStatusFilterType>]
 [<CommonParameters>]
```

## DESCRIPTION

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see Cmdlet Parameter Sets.

The `Get-SPOSite` cmdlet retrieves and returns properties of all site collections that match the given criteria.

With version 5361 of the SharePoint Online Management Shell, you may experience the following:

Additional site collections are now displayed. For example, all group and video sites along with team sites will be displayed.

The Detailed parameter has been deprecated. It will continue to work with earlier versions

> [!NOTE]
> Site collections in the Recycle Bin will not be retrieved by using the `Get-SPOSite` cmdlet.
>
> Site redirects, like the ones created after [changing the SharePoint domain name](/sharepoint/change-your-sharepoint-domain-name) will be retrieved by using this cmdlet.

You need to be a SharePoint Online administrator and be a site collection administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

> [!NOTE]
> If Site Collection Storage Management is enabled for the tenant, you will not be able to set quota and will have a generic error returned. To workaround this issue, set the site collection storage management to "manual" temporarily, set your quotas and then set the site collection storage management setting back to its original setting.

> [!NOTE]
> If the Limit or Filter parameters are provided then the following site collection properties will not be populated and may contain a default value:
> AllowDownloadingNonWebViewableFiles, AllowEditing, AllowSelfServiceUpgrade, AnonymousLinkExpirationInDays, ConditionalAccessPolicy, DefaultLinkPermission, DefaultLinkToExistingAccess, DefaultSharingLinkType, DenyAddAndCustomizePages, DisableCompanyWideSharingLinks, ExternalUserExpirationInDays, InformationSegment, LimitedAccessFileType, OverrideTenantAnonymousLinkExpirationPolicy, OverrideTenantExternalUserExpirationPolicy, PWAEnabled, SandboxedCodeActivationCapability, SensitivityLabel, SharingAllowedDomainList, SharingBlockedDomainList, SharingCapability, SharingDomainRestrictionMode.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOSite
```

Example 1 returns all site collections.

### EXAMPLE 2

```powershell
Get-SPOSite -Identity https://contoso.sharepoint.com
```

Example 2 lists the site collection with detailed properties.

### EXAMPLE 3

```powershell
Get-SPOSite -Identity https://contoso.sharepoint.com -DisableSharingForNonOwnersStatus
```

Example 3 Updates status on if the non owners of a site collection can share the site collection (does not set this value).

### EXAMPLE 4

```powershell
Get-SPOSite -Template GROUP#0 -IncludePersonalSite:$false
```

This example enumerates Group Site Collections in a tenant.

### EXAMPLE 5

```powershell
Get-SPOSite -Identity https://contoso.sharepoint.com/sites/groupname -detailed |fl
```

This example gets quota details for a Group Site.

### EXAMPLE 6

```powershell
Get-SPOSite -Identity https://contoso.sharepoint.com/sites/research | Select InformationSegment
```

This example returns the InformationSegments associated with the site. It is applicable for tenants who have enabled Microsoft 365 Information barriers capability. Read [Learn about information barriers](/microsoft-365/compliance/information-barriers) to understand Information barriers in SharePoint Online.

**Note**: This property is available only in SharePoint Online Management Shell Version 16.0.19927.12000 or later.

### EXAMPLE 7

```powershell
Get-SPOSite -Filter { Url -like "contoso.sharepoint.com/sites/18" }
```

This example uses server side filtering to return sites matching 18.

### EXAMPLE 8

```powershell
Get-SPOSite -Limit ALL | ?{$_.IsTeamsConnected -eq $true}
```

This example uses client-side filtering to return a list of sites connected to Microsoft Teams.

### EXAMPLE 9

```powershell
Get-SPOSite -Limit ALL | ?{$_.IsTeamsChannelConnected -eq $true}
```

This example uses client-side filtering to return a list of sites connected to a Microsoft Teams Private or Shared channel.

### EXAMPLE 10

```powershell
Get-SPOSite -Limit ALL -GroupIdDefined $true
```
This example uses server-side filtering to return all sites that have an associated Microsoft 365 Group.

### EXAMPLE 11

```powershell
$userUPN="joe.healy@contoso.com"
Get-SPOSite -Filter "Owner -like '$($userUPN)'"
```
This example retrieves all sites filtering by the specified owner using a variable.

## PARAMETERS

### -ArchiveStatus

> Applicable: SharePoint Online

Displays sites of a specific archive status. For example, NotArchived, RecentlyArchived, FullyArchived, Archived, or Reactivating.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.ArchiveStatusFilterType
Parameter Sets: ParamSet2
Aliases:
Accepted values: NotArchived, FullyArchived, RecentlyArchived, Reactivating, Archived

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Detailed

> Applicable: SharePoint Online

Use this parameter to get additional property information on a site collection. You will notice a slower response time when the Detailed parameter is used.

The following properties are returned:

- ResourceUsageCurrent
- ResourceUsageAverage
- StorageUsageCurrent
- LockIssue
- WebsCount
- CompatibilityLevel
- AllowSelfServiceUpgrade
- SiteDefinedSharingCapability

Returns the stored value of the site policy.

- SharingCapability

Returns the effective access level, which is the site policy and the tenant policy combined.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParamSet1, ParamSet2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSharingForNonOwnersStatus

> Applicable: SharePoint Online

This parameter prevents non-owners from sharing.

> [!NOTE]
> This parameter is available only in SharePoint Online Management Shell Version 16.0.4613.1211 or later. DisableSharingForNonOwnersStatus is not a persisted setting but rather an analysis of the state of the site collection. The purpose of this is to get this setting, and it's not guaranteed that other settings returned are correct. To get other settings and values, use the Get-SPOSite without this parameter to ensure everything is displayed correctly.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParamSet3
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter

> Applicable: SharePoint Online

Specifies the script block of the server-side filter to apply. The type must be a valid filter name and value must be in the form `{ PropertyName <operator> "filterValue"}`. Valid operators are as follows: -eq, -ne, -like, -notlike.
 Currently, you can filter by these properties: Owner, Template (can be used to filter if it is the only property present in the filter), LockState, Url.
 Using the -or operator to include an additional filter is not supported.

Note: The operator values are case-sensitive.

```yaml
Type: System.String
Parameter Sets: ParamSet2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GroupIdDefined

> Applicable: SharePoint Online

Filters the list of sites returned to sites with a Group ID (ie: Sites connected to an Microsoft 365 Group) when the value is set to $true.  Filters the list of sites to only sites without a Group ID when the value is $false.

The values are **$true**, **$false**, and **not defined**. By default, the value is **not defined**, which means that the filter does not apply.

```yaml
Type: System.Boolean
Parameter Sets: ParamSet2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

> Applicable: SharePoint Online

Specifies the URL of the site collection.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind
Parameter Sets: ParamSet1, ParamSet3
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IncludePersonalSite

> Applicable: SharePoint Online

Displays personal sites when value is set to $true.

The values are $true and $false. By default, the value is $false which means no personal sites will be returned.

```yaml
Type: System.Boolean
Parameter Sets: ParamSet2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Limit

> Applicable: SharePoint Online

Specifies the maximum number of site collections to return. It can be any number. To retrieve all site collections, use ALL. The default value is 200. If this parameter is provided, then some site collection properties will not be populated and may contain a default value.

```yaml
Type: System.String
Parameter Sets: ParamSet1, ParamSet2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Template

> Applicable: SharePoint Online

Displays sites of a specific template. For example, STS, STS#0, STS#1, STS#3, GROUP#0, SRCHCEN#0 or SITEPAGEPUBLISHING#0.

```yaml
Type: System.String
Parameter Sets: ParamSet2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SpoSitePipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
