---
external help file: Microsoft.Office.Server.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/mount-spstateservicedatabase
applicable: SharePoint Server Subscription Edition
title: Mount-SPStateServiceDatabase
schema: 2.0.0
---

# Mount-SPStateServiceDatabase

## SYNOPSIS
Attaches an existing state service database to the farm.

## SYNTAX

```
Mount-SPStateServiceDatabase [-Name] <String> [-AssignmentCollection <SPAssignmentCollection>]
 [-DatabaseCredentials <PSCredential>] [-DatabaseServer <String>]
 [-ServiceApplication <SPStateServiceApplicationPipeBind>] [-Weight <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The Mount-SPStateServiceDatabase cmdlet attaches an existing state service database to the farm.
If the session state database schema is not installed in the state service database, use the Initialize-SPStateServiceDatabase cmdlet to install the schema after the state service database has been mounted.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Mount-SPStateServiceDatabase -Name "statedata1" -DatabaseServer "localhost"
```

This example associates a SharePoint Server farm with a SQL Server database.

This example is used in least privilege scenarios when an administrator cannot create databases in SQL.
The database must already exist and be empty.
The database cannot be used until the Initialize-SPStateServiceDatabase cmdlet is run, so errors could occur with this example.

### EXAMPLE 2
```powershell
Mount-SPStateServiceDatabase -Name "statedata1" -DatabaseServer "localhost" -ServiceApplication "ServiceApp1" -Weight 10 | Initialize-SPStateServiceDatabase
```

This example associates a SharePoint Server farm with a SQL Server database, at the same time that it also associates the database with a service application and gives a weight of 10.
The result is immediately piped to the Initialize-SPStateServiceDatabase cmdlet so that the database can be used.

## PARAMETERS

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the database name that is created in the SQL Server database.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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

### -DatabaseCredentials

> Applicable: SharePoint Server Subscription Edition

Specifies the database credentials for SQL Authentication used to access the state service database.
If this parameter is not specified, Windows authentication is used.

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

### -DatabaseServer

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the host server for the state service database.

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

### -ServiceApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the state service application to which to add the state database.

The type must be a valid name of a state service application (for example, StateServiceApp1); a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an instance of a valid SPStateServiceApplication object.

```yaml
Type: SPStateServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Weight

> Applicable: SharePoint Server Subscription Edition

Specifies the weight for the state database used to load balance the allocation of new data.
The default value is 1.

The type must be a valid integer in the range of 1 to 10.

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
