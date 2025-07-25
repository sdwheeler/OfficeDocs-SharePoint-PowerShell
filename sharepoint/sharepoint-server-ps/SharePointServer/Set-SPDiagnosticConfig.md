---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spdiagnosticconfig
applicable: SharePoint Server Subscription Edition
title: Set-SPDiagnosticConfig
schema: 2.0.0
---

# Set-SPDiagnosticConfig

## SYNOPSIS
Sets diagnostic configuration settings on the farm.

## SYNTAX

```
Set-SPDiagnosticConfig [-AllowLegacyTraceProviders] [-AppAnalyticsAutomaticUploadEnabled]
 [-AssignmentCollection <SPAssignmentCollection>] [-CustomerExperienceImprovementProgramEnabled]
 [-DaysToKeepLogs <Int32>] [-DownloadErrorReportingUpdatesEnabled] [-ErrorReportingAutomaticUploadEnabled]
 [-ErrorReportingEnabled] [-EventLogFloodProtectionEnabled] [-EventLogFloodProtectionNotifyInterval <Int32>]
 [-EventLogFloodProtectionQuietPeriod <Int32>] [-EventLogFloodProtectionThreshold <Int32>]
 [-EventLogFloodProtectionTriggerPeriod <Int32>] [-InputObject <PSObject>] [-LogCutInterval <Int32>]
 [-LogDiskSpaceUsageGB <Int32>] [-LogLocation <String>] [-LogMaxDiskSpaceUsageEnabled]
 [-ScriptErrorReportingDelay <Int32>] [-ScriptErrorReportingEnabled] [-ScriptErrorReportingRequireAuth]
 [<CommonParameters>]
```

## DESCRIPTION
Use the `Set-SPDiagnosticConfig` cmdlet to set diagnostic configuration settings on the entire farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Set-SPDiagnosticConfig -ErrorReportingEnabled -DownloadErrorReportingUpdatesEnabled:$false -DaysToKeepLog 60
```

This example enables ErrorReporting, disables DownloadErrorReportingUpdatesEnable and sets DaysToKeepLog to 60.

### EXAMPLE 2
```powershell
$config = Get-SPDiagnosticConfig
$config.CustomerExperienceImprovementProgramEnabled = $false
$config.LogCutInterval = 60
$config | Set-SPDiagnosticConfig
```

This example disables CEIP and sets LogCutInterval to 60 minutes.

## PARAMETERS

### -AllowLegacyTraceProviders

> Applicable: SharePoint Server Subscription Edition

Specifies that trace providers built for previous versions of SharePoint Products and Technologies can write to the trace session for SharePoint Products.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AppAnalyticsAutomaticUploadEnabled

> Applicable: SharePoint Server Subscription Edition

Specifies whether aggregated app usage data is automatically uploaded to Microsoft.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -CustomerExperienceImprovementProgramEnabled

> Applicable: SharePoint Server Subscription Edition

Specifies whether participation in the Customer Experience Improvement Program (CEIP) is enabled.

The CEIP is designed to improve the quality, reliability, and performance of Microsoft products and technologies.
With your permission, anonymous information about your server is sent to Microsoft to help improve SharePoint Products.

The type must be either of the following values:

- $True
- $False

The default value is $True.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DaysToKeepLogs

> Applicable: SharePoint Server Subscription Edition

Specifies the number of days to keep trace log files.
The type must be a valid number between 1 and 366.
The default value is 14 days.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DownloadErrorReportingUpdatesEnabled

> Applicable: SharePoint Server Subscription Edition

Specifies whether the error reporting remote control file is downloaded.

The type must be either of the following values:

- $True
- $False

The default value is $True.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ErrorReportingAutomaticUploadEnabled

> Applicable: SharePoint Server Subscription Edition

Specifies whether error reports are uploaded to Microsoft automatically.

Error reports include the following: information regarding the condition of the server when a problem occurs; the operating system version and computer hardware in use; and the digital product ID, which can be used to identify your license.
The IP address of your computer is also sent because you are connecting to an online service to send error reports; however, the IP address is used only to generate aggregate statistics.

The type must be either of the following values:

- $True
- $False

The default value is $True.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ErrorReportingEnabled

> Applicable: SharePoint Server Subscription Edition

Specifies whether collection of error reports is enabled.

Error reports are created when your system encounters hardware or software problems.
Microsoft and its partners actively use these reports to improve the reliability of the software.
Error reports include the following: information regarding the condition of the server when the problem occurs; the operating system version and computer hardware in use; and the digital product ID, which can be used to identify your license.
The IP address of your computer is also sent because you are connecting to an online service to send error reports; however, the IP address is used only to generate aggregate statistics.

The type must be either of the following values:

- $True
- $False

The default value is $True.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventLogFloodProtectionEnabled

> Applicable: SharePoint Server Subscription Edition

Specifies whether the Event log flood protection feature is enabled.

If multiple similar events are written to the event log, some duplicate messages are suppressed.
Then, after a period of time, a summary message is written that shows how many events were suppressed.

The type must be either of the following values:

- $True
- $False

The default value is $True.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventLogFloodProtectionNotifyInterval

> Applicable: SharePoint Server Subscription Edition

Specifies in minutes how often to write a summary event indicating how many events were suppressed due to flood protection.

The integer range is between 1 and 1440.
The default value is 5.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventLogFloodProtectionQuietPeriod

> Applicable: SharePoint Server Subscription Edition

Specifies in minutes how much time must pass without an event firing to exit flood protection.

The integer range is between 1 and 1440.
The default value is 2.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventLogFloodProtectionThreshold

> Applicable: SharePoint Server Subscription Edition

Specifies the number of events allowed in a given timeframe before an event is considered to be flooding the event log.

The integer range is between 1 and 100.
The default value is 5.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventLogFloodProtectionTriggerPeriod

> Applicable: SharePoint Server Subscription Edition

Specifies in minutes the timeframe to watch for events that may be flooding.

The integer range is between 1 and 1440.
The default value is 2.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject

> Applicable: SharePoint Server Subscription Edition

Use the result from the `Get-SPDiagnosticConfig` cmdlet, make modifications and then pipeline the object into `Set-SPDiagnosticConfig` cmdlet to update the content database.

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LogCutInterval

> Applicable: SharePoint Server Subscription Edition

Specifies the number of minutes between log file rollovers.

The value must be a valid integer between 0 and 1440.

The default value is 30.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogDiskSpaceUsageGB

> Applicable: SharePoint Server Subscription Edition

Specifies the maximum amount of storage to use for trace log files, in gigabytes (GB).

The default value is 1000 and only takes effect when the LogMaxDiskSpaceusageEnabled cmdlet is set to True.

The type must be a valid number between 1 and 1000.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogLocation

> Applicable: SharePoint Server Subscription Edition

Specifies the path of where to log files will reside.

The type must be a valid path, in the form C:\Logs.

The default location is %CommonProgramFiles%\Microsoft Shared\Web Server Extensions\14\Logs.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogMaxDiskSpaceUsageEnabled

> Applicable: SharePoint Server Subscription Edition

Specifies whether to restrict the maximum space to use for trace log files.

The type must be either of the following values:

- $True
- $False

The default value is $False.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScriptErrorReportingDelay

> Applicable: SharePoint Server Subscription Edition

Specifies the time (in minutes) between script error reports.

The type must be a valid integer between 0 and 1440.
The value is specified in minutes.

The default value is 30.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScriptErrorReportingEnabled

> Applicable: SharePoint Server Subscription Edition

Specifies whether error reporting is enabled for client script errors.

The type must be either of the following values:

- $True
- $False

The default value is $True.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScriptErrorReportingRequireAuth

> Applicable: SharePoint Server Subscription Edition

Specifies whether script error reporting requires authentication.

The type must be either of the following values:

- $True
- $False

The default value is $True.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
