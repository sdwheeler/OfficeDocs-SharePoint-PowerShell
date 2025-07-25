---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spocontainertype
applicable: SharePoint Online
title: Get-SPOContainerType
schema: 2.0.0
author: ShreyasSar26
ms.author: shsaravanan
ms.reviewer:
---

# Get-SPOContainerType

## SYNOPSIS

Returns one or more container types created in the tenant.

## SYNTAX

### ParamSet1

```
Get-SPOContainerType [[-ContainerTypeId] <Guid>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet returns all the container types present in the tenant or details of a specific container
type when paired with the `ContainerTypeId` parameter.

You must be a SharePoint Embedded Administrator to run the cmdlet.

While the basic information of container types is displayed to all administrators running this
cmdlet, the billing information about a container type is only visible to administrators who also
have owner or contributor access on the billing subscription attached to the container type.

For permissions and the most current information about Windows PowerShell for SharePoint Embedded
Containers, see the documentation at
[Intro to SharePoint Embedded Containers Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### Example 1

```powershell
Get-SPOContainerType
```

Example 1 retrieves all the container types present in the tenant and displays container type specific information.

### Example 2

```powershell
Get-SPOContainerType -ContainerTypeId 4f0af585
```

Example 2 returns the detailed properties of container type 4f0af585.

## PARAMETERS

### -ContainerTypeId

> Applicable: SharePoint Online

This parameter specifies the ID of the container type corresponding to the SharePoint Embedded application.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
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

[New-SPOContainerType](./New-SPOContainerType.md)

[Set-SPOContainerType](./Set-SPOContainerType.md)

[Remove-SPOContainerType](./Remove-SPOContainerType.md)
