---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spdesignersettings
applicable: SharePoint Server Subscription Edition
title: Set-SPDesignerSettings
schema: 2.0.0
---

# Set-SPDesignerSettings

## SYNOPSIS
Sets SharePoint Designer features.

## SYNTAX

```
Set-SPDesignerSettings [-WebApplication] <SPWebApplicationPipeBind> [-AllowDesigner <Boolean>]
 [-AllowMasterPageEditing <Boolean>] [-AllowRevertFromTemplate <Boolean>]
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-ShowURLStructure <Boolean>] [-WhatIf]
 [-AllowCreateDeclarativeWorkflow <Boolean>] [-AllowSaveDeclarativeWorkflowAsTemplate <Boolean>]
 [-AllowSavePublishDeclarativeWorkflow <Boolean>] [-DesignerDownloadUrl <String>]
 [-RequiredDesignerVersion <String>] [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPDesignerSettings` cmdlet sets SharePoint Designer features on a specified Web application when the WebApplicaton is used.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Set-SPDesignerSettings -WebApplication https://contoso -AllowRevertFromTemplate $False -AllowMasterPageEditing $False
```

This example disables the ability to detach pages from existing site definitions and to edit master pages and page layouts.

## PARAMETERS

### -WebApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the Web application in which the settings will apply.

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -AllowDesigner

> Applicable: SharePoint Server Subscription Edition

Specifies whether to allow users to edit sites in a web application by using SharePoint Designer.
The default value is True

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

### -AllowMasterPageEditing

> Applicable: SharePoint Server Subscription Edition

Specifies whether to allow site administrators to customize master pages and layout pages using SharePoint Designer.
The default value is True.

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

### -AllowRevertFromTemplate

> Applicable: SharePoint Server Subscription Edition

Specifies whether to allow site administrators to detach pages from the original site definition using SharePoint Designer.
The default value is True.

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

### -Confirm

> Applicable: SharePoint Server Subscription Edition

Prompts you for confirmation before executing the command.
For more information, type the following command: `get-help about_commonparameters`

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowURLStructure

> Applicable: SharePoint Server Subscription Edition

Specifies whether to allow site administrators to manage the URL structure of their Web sites by using SharePoint Designer.
The default value is True.

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

### -WhatIf

> Applicable: SharePoint Server Subscription Edition

Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: `get-help about_commonparameters`

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowCreateDeclarativeWorkflow

> Applicable: SharePoint Server Subscription Edition

Allows the creation of declarative workflows.

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

### -AllowSaveDeclarativeWorkflowAsTemplate

> Applicable: SharePoint Server Subscription Edition

Allows saving declarative workflows as a template.

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

### -AllowSavePublishDeclarativeWorkflow

> Applicable: SharePoint Server Subscription Edition

Allows saving of published declarative workflows.

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

### -DesignerDownloadUrl

> Applicable: SharePoint Server Subscription Edition

Sets the URL to the SharePoint Designer download. The default value is:

https://go.microsoft.com/fwlink/?LinkId=328584

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

### -RequiredDesignerVersion

> Applicable: SharePoint Server Subscription Edition

Sets the required version of SharePoint Designer. The default value is

15.0.0.0

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
