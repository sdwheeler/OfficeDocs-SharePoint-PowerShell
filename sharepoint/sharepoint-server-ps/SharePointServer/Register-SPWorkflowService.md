---
external help file: Microsoft.SharePoint.WorkflowServices.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/register-spworkflowservice
applicable: SharePoint Server Subscription Edition
title: Register-SPWorkflowService
schema: 2.0.0
---

# Register-SPWorkflowService

## SYNOPSIS
Registers a Workflow Manager farm with the SharePoint farm.

## SYNTAX

```
Register-SPWorkflowService [-AllowOAuthHttp] [-AssignmentCollection <SPAssignmentCollection>] [-Force]
 [-PartitionMode] -SPSite <SPSitePipeBind> [-ScopeName <String>] -WorkflowHostUri <String> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet registers a Workflow Manager farm with the SharePoint farm in order to allow users to leverage SharePoint 2013 workflows.

## EXAMPLES

### EXAMPLE
```powershell
Register-SPWorkflowService -SPSite https://site_name -WorkflowHostUri https://workflow.contoso.com:12290 -ScopeName SharePoint
```
Registers the Workflow Manager farm located at https://workflow.contoso.com:12290 with the SharePoint farm using https://site_name as a reference. A custom Scope named 'SharePoint' is used.

## PARAMETERS

### -AllowOAuthHttp

> Applicable: SharePoint Server Subscription Edition

Allows connecting to Workflow Manager using HTTP rather than HTTPS. This is not recommended for security.

```yaml
Type: SwitchParameter
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

### -Force

> Applicable: SharePoint Server Subscription Edition

Forces the registration, even if previously registered. Will overwrite the existing Scope.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionMode

> Applicable: SharePoint Server Subscription Edition

Specifies to use a SharePoint multi-tenancy features when registering Workflow Manager.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SPSite

> Applicable: SharePoint Server Subscription Edition

The Site Collection used as a reference to register Workflow Manager with the SharePoint farm.

```yaml
Type: SPSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScopeName

> Applicable: SharePoint Server Subscription Edition

The name of the scope in Workflow Manager to use. if not specified, the default Scope will be used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkflowHostUri

> Applicable: SharePoint Server Subscription Edition

The URI on which the Workflow Manager is hosted.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
