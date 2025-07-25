---
external help file: Microsoft.SharePoint.PowerShell.SSOUpgrade-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spsecurestoreapplication
applicable: SharePoint Server Subscription Edition
title: New-SPSecureStoreApplication
schema: 2.0.0
---

# New-SPSecureStoreApplication

## SYNOPSIS
Creates a new Secure Store application.

## SYNTAX

```
New-SPSecureStoreApplication -ServiceContext <SPServiceContextPipeBind> -TargetApplication <TargetApplication>
 [-Administrator <SPClaim[]>] [-AssignmentCollection <SPAssignmentCollection>]
 [-CredentialsOwnerGroup <SPClaim[]>] -Fields <TargetApplicationField[]> [-TicketRedeemer <SPClaim[]>]
 [<CommonParameters>]
```

## DESCRIPTION
The `New-SPSecureStoreApplication` cmdlet creates a new Secure Store application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$usernameField = New-SPSecureStoreApplicationField -Name "UserName" -Type WindowsUserName -Masked:$false
$passwordField = New-SPSecureStoreApplicationField -Name "Password" -Type WindowsPassword -Masked:$true
$fields = $usernameField,$passwordField
$userClaim = New-SPClaimsPrincipal -Identity "CONTOSO\janedoe" -IdentityType WindowsSamAccountName
$contosoTargetApp = New-SPSecureStoreTargetApplication -Name "ContosoTargetApplication" -FriendlyName "Contoso Target Application" -ApplicationType Group
New-SPSecureStoreApplication -ServiceContext http://contoso -TargetApplication $contosoTargetApp -Fields $fields -Administrator $userClaim
```

This example creates a new group target application ContosoTargetApplication and then a new application for that target application. This new application has two fields; UserName of type WindowsUserName and Password of type WindowsPassword. The user with identity janedoe on the CONTOSO domain is set as the target application administrator.

## PARAMETERS

### -ServiceContext

> Applicable: SharePoint Server Subscription Edition

Specifies the service context for the target application.

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

### -TargetApplication

> Applicable: SharePoint Server Subscription Edition

Specifies information about the target application.
For example, the TargetApplication object includes data values for application name, display name, contact info, enable ticketing flag and URL address to set the credential.
The schema for the TargetApplication object is defined in the ISecureSToreProviderExtended interface that exposes the target application metadata.

```yaml
Type: TargetApplication
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Administrator

> Applicable: SharePoint Server Subscription Edition

Specifies the administrator of the new Secure Store application.

```yaml
Type: SPClaim[]
Parameter Sets: (All)
Aliases:

Required: False
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

### -CredentialsOwnerGroup

> Applicable: SharePoint Server Subscription Edition

Specifies the claims object for the groups that own the group credentials.

```yaml
Type: SPClaim[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fields

> Applicable: SharePoint Server Subscription Edition

Specifies the field information for the application.
The default fields are username and password.

```yaml
Type: TargetApplicationField[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TicketRedeemer

> Applicable: SharePoint Server Subscription Edition

Specifies the ticket redeemer claim value.

```yaml
Type: SPClaim[]
Parameter Sets: (All)
Aliases:

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
