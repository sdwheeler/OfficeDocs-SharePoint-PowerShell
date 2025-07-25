---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/deny-spotenantserviceprincipalpermissionrequest
applicable: SharePoint Online
title: Deny-SPOTenantServicePrincipalPermissionRequest
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Deny-SPOTenantServicePrincipalPermissionRequest

## SYNOPSIS

Denies a permission request for the current tenant's "SharePoint Online Client" service principal

## SYNTAX

```
Deny-SPOTenantServicePrincipalPermissionRequest -RequestId <Guid> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Denies a permission request for the current tenant's "SharePoint Online Client" service principal

Denying a permission request removes that request from the list of permission requests.

## EXAMPLES

### EXAMPLE 1

```powershell
$requests = Get-SPOTenantServicePrincipalPermissionRequests
$requestToDeny = $requests | ? { $_.Resource -eq 'Office 365 SharePoint Online' -and $_.Scope -eq 'MyFiles.Read' } | Select-Object -First 1

if ($requestToDeny -ne $null)
{
    Deny-SPOTenantServicePrincipalPermissionRequest -RequestId $requestToDeny.Id
}
```

Denies the permission request for the 'Office 365 SharePoint Online' resource with scope claim 'MyFiles.Read'.
If there is no request with those properties, then no deny action will be taken.

## PARAMETERS

### -RequestId

The ID of the permission request to deny

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

### -Confirm
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

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
