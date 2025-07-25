---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spworkflowconfig
applicable: SharePoint Server Subscription Edition
title: Set-SPWorkflowConfig
schema: 2.0.0
---

# Set-SPWorkflowConfig

## SYNOPSIS
Configures the workflow settings for the specified Web application.

## SYNTAX

### SiteCollection
```
Set-SPWorkflowConfig [-SiteCollection] <SPSitePipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-DeclarativeWorkflowsEnabled <Boolean>] [-EmailNoPermissionParticipantsEnabled <Boolean>]
 [-SendDocumentToExternalParticipants <Boolean>] [-SingleWorkflowEpisodeTimeout <Int32>] [<CommonParameters>]
```

### WebApplication
```
Set-SPWorkflowConfig [-WebApplication] <SPWebApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-DeclarativeWorkflowsEnabled <Boolean>]
 [-EmailNoPermissionParticipantsEnabled <Boolean>] [-SendDocumentToExternalParticipants <Boolean>]
 [-SingleWorkflowEpisodeTimeout <Int32>] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet parameter sets](https://learn.microsoft.com/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

Use the `Set-SPWorkflowConfig` cmdlet to configure the workflow settings for the specified Web application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Set-SPWorkflowConfig -webapplication https://sitename DeclarativeWorkflowsEnabled $true -EmailNoPermissionParticipantsEnabled $true -SendDocumentToExternalParticipants $false
```

This example sets the workflow settings for the specified Web application to turn on declarative workflows, turn on e-mail to participants who do not have permissions to the site and turn off the functionality to send e-mail messages as attachments to external participants.

No return values.
Use the `Get-SPWorkflowConfig` cmdlet to see values.
To set farm-level workflow settings for event-delivery time-out and to postpone threshold and batch size, use `Set-SPFarmConfig`.

## PARAMETERS

### -SiteCollection

> Applicable: SharePoint Server Subscription Edition

Specifies the name or URL of the site collection.

The only other parameter that is used with the SiteCollection parameter is the DeclarativeWorkflowsEnabled parameter.
No other parameters are used.

```yaml
Type: SPSitePipeBind
Parameter Sets: SiteCollection
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WebApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the name or URL of the Web application.

The type must be a valid name or GUID, in the form WebApplication-1212, or a URL, in the form https://server_name/WebApplication-1212.

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: WebApplication
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -DeclarativeWorkflowsEnabled

> Applicable: SharePoint Server Subscription Edition

Sets whether declarative workflows are allowed to run in the Web application.

The type must be either 1 for True or 0 for False.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EmailNoPermissionParticipantsEnabled

> Applicable: SharePoint Server Subscription Edition

Sets whether workflows send task e-mail messages to users who do not have permissions to the site in which the workflows are running.

The type must be  either 1 for True or 0 for False.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendDocumentToExternalParticipants

> Applicable: SharePoint Server Subscription Edition

Sets whether workflows automatically send a copy of the document as an e-mail attachment to participants who do not have access to the site or who are not in any linked directory other than Active Directory Domain Services (AD DS).

The type must be either 1 for True or 0 for False.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SingleWorkflowEpisodeTimeout

> Applicable: SharePoint Server Subscription Edition

Amount of time in seconds given to the workflow to run.

```yaml
Type: Int32
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
