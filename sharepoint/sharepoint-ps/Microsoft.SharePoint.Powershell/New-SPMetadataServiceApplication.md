---
external help file: Microsoft.SharePoint.Taxonomy.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spmetadataserviceapplication
applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: New-SPMetadataServiceApplication
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# New-SPMetadataServiceApplication

## SYNOPSIS
Creates a new managed metadata service application.

## SYNTAX

### NoQuota
```
New-SPMetadataServiceApplication -Name <String> [-AdministratorAccount <String>]
 -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-CacheTimeCheckInterval <Int32>] [-Confirm] [-DatabaseCredentials <PSCredential>] [-DatabaseName <String>]
 [-DatabaseServer <String>] [-FailoverDatabaseServer <String>] [-FullAccessAccount <String>] [-HubUri <String>]
 [-MaxChannelCache <Int32>] [-PartitionMode] [-ReadAccessAccount <String>] [-RestrictedAccount <String>]
 [-SyndicationErrorReportEnabled] [-WhatIf] [-DisablePartitionQuota] [-DeferUpgradeActions]
 [<CommonParameters>]
```

### Quota
```
New-SPMetadataServiceApplication -Name <String> [-AdministratorAccount <String>]
 -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-CacheTimeCheckInterval <Int32>] [-Confirm] [-DatabaseCredentials <PSCredential>] [-DatabaseName <String>]
 [-DatabaseServer <String>] [-FailoverDatabaseServer <String>] [-FullAccessAccount <String>] [-HubUri <String>]
 [-MaxChannelCache <Int32>] [-PartitionMode] [-ReadAccessAccount <String>] [-RestrictedAccount <String>]
 [-SyndicationErrorReportEnabled] [-WhatIf] -GroupsPerPartition <Int32> -LabelsPerPartition <Int32>
 -PropertiesPerPartition <Int32> -TermSetsPerPartition <Int32> -TermsPerPartition <Int32>
 [-DeferUpgradeActions] [<CommonParameters>]
```

## DESCRIPTION
Use the `New-SPMetadataServiceApplication` cmdlet to create a new managed metadata service application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```
New-SPMetadataServiceApplication -Name "MetadataServiceApp1" -ApplicationPool "AppPool1" -DatabaseName "MetadataDB1"
```

This example creates a new managed metadata service application.

### EXAMPLE 2
```
New-SPMetadataServiceApplication -Name "MetadataServiceApp2" -ApplicationPool "AppPool1" -DatabaseName "MetadataDB2" -HubUri "https://sitename" -SyndicationErrorReportEnabled
```

This example creates a new managed metadata service application and specifies a content type hub to be used for syndication.
It also enables error reporting during syndication.

### EXAMPLE 3
```
New-SPMetadataServiceApplication -Name "MetadataServiceApp3" -ApplicationPool "AppPool1" -DatabaseName "MetadataDB3" -PartitionMode
```

This example creates a new managed metadata service application that is partitioned, for use by sites in a subscription.

## PARAMETERS

### -Name

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the name of the service application to create.
The name can contain a maximum of 128 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -AdministratorAccount

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

A comma-separated list of user accounts or service accounts in the format \<domain\>\\\<account\> that may create and run the service application.
The accounts must already exist.

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

### -ApplicationPool

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies an existing IIS application pool in which to run the new managed metadata service application.

The value must be a GUID that is the identity of an SPServiceApplicationPool object; the name of an existing application pool, or an instance of an SPServiceApplicationPool object.

```yaml
Type: SPIisWebServiceApplicationPoolPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### -CacheTimeCheckInterval

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies an interval, in seconds, that a front-end Web Server should wait before asking the application server for changes.
This value is set per timer job, client application, or Web application.

The mininum value is 1, and there is no maximum value.
The default value is 10.

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

### -Confirm

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### -DatabaseCredentials

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the PSCredential object that contains the user name and password to be used for database SQL authentication.

If SQL authentication is to be used, either DatabaseCredentials must be specified or both the DatabaseUserName and DatabasePassword parameters must be set.

The type must be a valid PSCredential object.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the name of the database to create for the new managed metadata service application.

The type must be a valid name of a SQL Server database; for example MeatadataDB1.

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

### -DatabaseServer

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the name of the host server for the database specified in DatabaseName.

The type must be a valid name of a SQL Server database; for example SqlServerHost1.

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

### -FailoverDatabaseServer

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the name of the host server for the failover database server.

The type must be a valid SQL Server host name; for example, SQLServerHost1.

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

### -FullAccessAccount

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies a comma-separated set of application pool accounts in the format \<domain\>\\\<account\> that will be given read/write permission to the managed metadata service's term store and content type gallery.
The accounts must already exist.

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

### -HubUri

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the fully qualified URL of the site collection that contains the content type gallery that the service will provide access to.

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

### -MaxChannelCache

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the maximum number of Windows Communication Foundation (WCF) channels that a front-end Web server should hold open to the application server.

This value is set per timer job, client application, or Web application.

The minimum value is 0, and there is no maximum value. The default value is 4.

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

### -PartitionMode

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies that the service application restrict data by subscription.

Note This property cannot be changed after the service application has been created.

This property has no effect on SharePoint Server 2019.

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

### -ReadAccessAccount

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies a comma-separated set of application pool accounts in the format \<domain\>\\\<account\> that will be given read-only permission to the managed metadata service's term store and content type gallery.

The accounts must already exist.

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

### -RestrictedAccount

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies a comma-separated set of application pool accounts in the format \<domain\>\\\<account\> that will be given permission to read the managed metadata service's term store and content type gallery; and permission to write to open term sets and local term sets and to create new enterprise keywords.

The accounts must already exist.

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

### -SyndicationErrorReportEnabled

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Enables reporting of errors when content types are imported.

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

### -WhatIf

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### -DisablePartitionQuota

> Applicable: SharePoint Server 2016, SharePoint Server 2019

Disables partition quotas.

```yaml
Type: SwitchParameter
Parameter Sets: NoQuota
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GroupsPerPartition

> Applicable: SharePoint Server 2016, SharePoint Server 2019

Sets the maximum number of Term Groups per partition.

```yaml
Type: Int32
Parameter Sets: Quota
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LabelsPerPartition

> Applicable: SharePoint Server 2016, SharePoint Server 2019

Sets the maximum number of Labels per partition.

```yaml
Type: Int32
Parameter Sets: Quota
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertiesPerPartition

> Applicable: SharePoint Server 2016, SharePoint Server 2019

Sets the maximum number of Properties per partition.

```yaml
Type: Int32
Parameter Sets: Quota
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TermSetsPerPartition

> Applicable: SharePoint Server 2016, SharePoint Server 2019

Sets the maximum number of Term Sets per partition.

```yaml
Type: Int32
Parameter Sets: Quota
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TermsPerPartition

> Applicable: SharePoint Server 2016, SharePoint Server 2019

Sets the maximum number of Terms per partition.
```yaml
Type: Int32
Parameter Sets: Quota
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeferUpgradeActions

> Applicable: SharePoint Server 2016, SharePoint Server 2019

Specifies if the upgrade process is to be deferred and manually completed.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
