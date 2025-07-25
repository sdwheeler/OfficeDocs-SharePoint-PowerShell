---
external help file: sharepointserver.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-fastsearchsecurityloglevel
applicable: FAST Server for SharePoint 2010
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
title: Set-FASTSearchSecurityLogLevel
---

# Set-FASTSearchSecurityLogLevel

## SYNOPSIS
Updates the log level general setting.

## SYNTAX

```
Set-FASTSearchSecurityLogLevel [[-GeneralSetting] <LogLevelSetting>] [-DebugNameSpaceLogLevel <String[]>]
 [-DefaultLogLevel <String>] [-ErrorNameSpaceLogLevel <String[]>] [-IncludeExceptionStack <Boolean>]
 [-InfoNameSpaceLogLevel <String[]>] [-WarningNameSpaceLogLevel <String[]>] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet updates the configuration information for the log level's general setting.
The log level controls the type of information that is logged by the security system.

For permissions and the most current information about FAST Search Server 2010 for SharePoint cmdlets, see the online documentation, (https://go.microsoft.com/fwlink/?LinkId=163227).

## EXAMPLES

### EXAMPLE 1 (FAST Server for SharePoint 2010)
```
Set-FASTSearchSecurityLogLevel -DefaultLogLevel debug -IncludeExceptionStack $True
```

This example sets the default log level to the "Debug" level and enables the setting to include the exception stack in the log.

### EXAMPLE 2 (FAST Server for SharePoint 2010)
```
Set-FASTSearchSecurityLogLevel -WarningNameSpaceLogLevel Microsoft
```

This example sets the log level setting for the "Microsoft" namespace to the "Warning" level.

## PARAMETERS

### -GeneralSetting

> Applicable: FAST Server for SharePoint 2010

A LogLevelSetting whose property values are used for the LogLevelSetting being updated.

```yaml
Type: LogLevelSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: 9999
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DebugNameSpaceLogLevel

> Applicable: FAST Server for SharePoint 2010

A list of C# namespaces.
Any class contained in that namespace logs all messages to the log.

A class can occur in only one namespace.
If you specify the same class in more than one name space log level, the log level that generates the most messages will be set.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultLogLevel

> Applicable: FAST Server for SharePoint 2010

Specifies the type of log messages that each class writes to the log, unless the class is contained in a namespace explicitly specified in ErrorLogLevelNameSpaces, WarningLogLevelNameSpaces, InfoLogLevelNameSpaces, and DebugLogLevelNameSpaces.

Valid values are:

-- Error
-- Warning
-- Info
-- Debug

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ErrorNameSpaceLogLevel

> Applicable: FAST Server for SharePoint 2010

A list of C# namespaces.
Any class included in the namespace only logs error messages.

A class can occur in only one namespace.
If you specify the same class in more than one namespace log level, the log level that generates the most messages will be set.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IncludeExceptionStack

> Applicable: FAST Server for SharePoint 2010

Whether or not to include the exception stack in the log.
Set to $True to include the exception stack.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InfoNameSpaceLogLevel

> Applicable: FAST Server for SharePoint 2010

A list of C# namespaces.
Any class contained in that namespace only logs error, warning, and info messages.

A class can occur in only one namespace.
If you specify the same class in more than one namespace log level, the log level that generates the most messages will be set.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WarningNameSpaceLogLevel

> Applicable: FAST Server for SharePoint 2010

A list of C# namespaces.
Any class included in the namespace only logs error and warning messages.

A class can occur in only one namespace.
If you specify the same class in more one than namespace log level, the log level that generates the most messages will be set.

```yaml
Type: String[]
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

[Get-FASTSearchSecurityLogLevel](Get-FASTSearchSecurityLogLevel.md)
