---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spbusinessdatacatalogentitynotificationweb
applicable: SharePoint Server Subscription Edition
title: Get-SPBusinessDataCatalogEntityNotificationWeb
schema: 2.0.0
---

# Get-SPBusinessDataCatalogEntityNotificationWeb

## SYNOPSIS

Returns the entity notification site.


## SYNTAX

```
Get-SPBusinessDataCatalogEntityNotificationWeb -ServiceContext <SPServiceContextPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

## DESCRIPTION
Use the Get-SPBusinessDataCatalogEntityNotificationWeb cmdlet to return the entity notification site that can receive and forward external system notifications.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Get-SPBusinessDataCatalogEntityNotificationWeb -ServiceContext "http://contoso"
```

This example returns the entity notification site for the site collection at http://contoso.

## PARAMETERS

### -ServiceContext

> Applicable: SharePoint Server Subscription Edition

Specifies the service context for which the entity notification web has to be returned.

```yaml
Type: SPServiceContextPipeBind
Parameter Sets: (All)
Aliases:

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Clear-SPBusinessDataCatalogEntityNotificationWeb](Clear-SPBusinessDataCatalogEntityNotificationWeb.md)

[Set-SPBusinessDataCatalogEntityNotificationWeb](Set-SPBusinessDataCatalogEntityNotificationWeb.md)
