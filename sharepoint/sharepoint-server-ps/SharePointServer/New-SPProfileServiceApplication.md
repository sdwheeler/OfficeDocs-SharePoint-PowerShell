---
external help file: Microsoft.Office.Server.UserProfiles.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spprofileserviceapplication
applicable: SharePoint Server Subscription Edition
title: New-SPProfileServiceApplication
schema: 2.0.0
---

# New-SPProfileServiceApplication

## SYNOPSIS
Adds a User Profile Service Application to a farm.

## SYNTAX

### Default
```
New-SPProfileServiceApplication -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> [-Name <String>]
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-MySiteHostLocation <SPSitePipeBind>]
 [-PartitionMode] [-ProfileDBCredentials <PSCredential>] [-ProfileDBName <String>] [-ProfileDBServer <String>]
 [-ProfileSyncDBCredentials <PSCredential>] [-ProfileDBFailoverServer <String>] [-ProfileSyncDBName <String>]
 [-ProfileSyncDBServer <String>] [-ProfileSyncDBFailoverServer <String>] [-SocialDBCredentials <PSCredential>]
 [-SocialDBName <String>] [-SocialDBServer <String>] [-SocialDBFailoverServer <String>] [-WhatIf]
 [-DeferUpgradeActions] [<CommonParameters>]
```

### MySiteSettings
```
New-SPProfileServiceApplication -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> [-Name <String>]
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] -MySiteHostLocation <SPSitePipeBind>
 [-MySiteManagedPath <SPPrefixPipeBind>] [-PartitionMode] [-ProfileDBCredentials <PSCredential>]
 [-ProfileDBName <String>] [-ProfileDBServer <String>] [-ProfileSyncDBCredentials <PSCredential>]
 [-ProfileDBFailoverServer <String>] [-ProfileSyncDBName <String>] [-ProfileSyncDBServer <String>]
 [-ProfileSyncDBFailoverServer <String>] [-SiteNamingConflictResolution <String>]
 [-SocialDBCredentials <PSCredential>] [-SocialDBName <String>] [-SocialDBServer <String>]
 [-SocialDBFailoverServer <String>] [-WhatIf] [-DeferUpgradeActions] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.

You may only use parameters from one parameter set and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet parameter sets](https://learn.microsoft.com/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

The `New-SPProfileServiceApplication` cmdlet adds and creates a new profile service application, or creates an instance of a profile service.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
New-SPProfileServiceApplication -Name 'User Profile Service Application' -ApplicationPool 'SharePoint Web Services Default' -ProfileDBName Profile -SocialDBName Social -ProfileSyncDBname Sync
```

This example creates a new User Profile Service application.

## PARAMETERS

### -ApplicationPool

> Applicable: SharePoint Server Subscription Edition

Specifies the existing IIS application pool in which to run the Web service for the service application.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of an application pool (for example, AppPoolName1); or an instance of a valid IISWebServiceApplicationPool object.

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

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the display name for the new User Profile Service application.
The name must be a unique name of a User Profile Service application in this farm.
The name can be a maximum of 64 characters.

The type must be a valid name of a service application; for example, UserProfileSvcApp1.

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

### -MySiteHostLocation

> Applicable: SharePoint Server Subscription Edition

Specifies the site collection where the My Site will be created.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or a valid URL, in the form https://server_name; or an instance of a valid SPSite object.

```yaml
Type: SPSitePipeBind
Parameter Sets: Default, MySiteSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MySiteManagedPath

> Applicable: SharePoint Server Subscription Edition

Specifies the managed path where personal sites will be created.

The type must be a valid URL, in the form https://server_name.

```yaml
Type: SPPrefixPipeBind
Parameter Sets: MySiteSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PartitionMode

> Applicable: SharePoint Server Subscription Edition

Specifies that the service application restrict data by site group.
After the PartitionMode parameter is set and the service application is created, it cannot be changed.

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

### -ProfileDBCredentials

> Applicable: SharePoint Server Subscription Edition

Specifies the set of security credentials, such as a user name and a password, that is used to connect to the User Profile database that this cmdlet creates.

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

### -ProfileDBName

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the database where the User Profile database is created.

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

### -ProfileDBServer

> Applicable: SharePoint Server Subscription Edition

Specifies the database where the User Profile database will be created.

The type must be a valid name of a SQL Server database; for example, ProfileAppDB1.

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

### -ProfileSyncDBCredentials

> Applicable: SharePoint Server Subscription Edition

Specifies the set of security credentials, such as a user name and a password, that will be used to connect to the Profile Sync database that is specified in the ProfileSyncDBName parameter.

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

### -ProfileDBFailoverServer

> Applicable: SharePoint Server Subscription Edition

Associates a content database with a specific failover server that is used in conjunction with SQL Server database mirroring.
The server name is the required value.

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

### -ProfileSyncDBName

> Applicable: SharePoint Server Subscription Edition

Specifies the database where the Profile Sync database will be created.

The type must be a valid name of a SQL Server database; for example, ProfileSyncAppDB1.

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

### -ProfileSyncDBServer

> Applicable: SharePoint Server Subscription Edition

Specifies the database server that will host the Profile Sync database that is specified in the ProfileSyncDBName parameter.

The type must be a valid name of a SQL Server host; for example, SQLServerProfileSyncHost1.

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

### -ProfileSyncDBFailoverServer

> Applicable: SharePoint Server Subscription Edition

Associates a Profile Sync database with a specific failover server that is used in conjunction with SQL Server database mirroring.
The server name is the required value.

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

### -SiteNamingConflictResolution

> Applicable: SharePoint Server Subscription Edition

Specifies the format to use to name personal sites.

Use one of the following integer values:

1   Personal site collections are to be based on user names without any conflict resolution.
For example, https://portal_site/location/username/

2   Personal site collections are to be based on user names with conflict resolution by using domain names.
For example, .../username/ or .../domain_username/

3   Personal site collections are to be named by using domain and user name always, to avoid any conflicts.
For example, https://portal_site/location/domain_username/

The default value is 1 (do not resolve conflicts).

```yaml
Type: String
Parameter Sets: MySiteSettings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SocialDBCredentials

> Applicable: SharePoint Server Subscription Edition

The set of security credentials, including a user name and a password, that is used to connect to the Social database that this cmdlet creates.

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

### -SocialDBName

> Applicable: SharePoint Server Subscription Edition

Specifies the database where the Social database will be created.

The type must be a valid name of a SQL Server host; for example, SQLServerSocialHost1.

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

### -SocialDBServer

> Applicable: SharePoint Server Subscription Edition

Specifies the database server that will host the Social database that is specified in SocialDBName.

The type must be a valid name of a SQL Server host; for example, SQLServerSocialHost1.

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

### -SocialDBFailoverServer

> Applicable: SharePoint Server Subscription Edition

Associates a Social database with a specific failover server that is used in conjunction with SQL Server database mirroring.
The server name is the required value.

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

### -DeferUpgradeActions

> Applicable: SharePoint Server Subscription Edition

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
