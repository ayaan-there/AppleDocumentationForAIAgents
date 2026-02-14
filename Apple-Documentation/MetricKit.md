# MetricKit Documentation

Source: https://sosumi.ai/documentation/metrickit

---
title: MetricKit
source: https://developer.apple.com/documentation/metrickit
timestamp: 2026-02-13T18:59:45.204Z
---

## Essentials

- [MXMetricManager](/documentation/metrickit/mxmetricmanager)

### Getting the shared metrics manager

- [class var shared: MXMetricManager](/documentation/metrickit/mxmetricmanager/shared)

### Subscribing to reports

- [func add(any MXMetricManagerSubscriber)](/documentation/metrickit/mxmetricmanager/add(_:))
- [func remove(any MXMetricManagerSubscriber)](/documentation/metrickit/mxmetricmanager/remove(_:))

### Retrieving previous reports

- [var pastPayloads: [MXMetricPayload]](/documentation/metrickit/mxmetricmanager/pastpayloads)
- [var pastDiagnosticPayloads: [MXDiagnosticPayload]](/documentation/metrickit/mxmetricmanager/pastdiagnosticpayloads)

### Creating custom metric logs

- [class func makeLogHandle(category: String) -> OSLog](/documentation/metrickit/mxmetricmanager/makeloghandle(category:))

### Measuring an extended launch

- [class func extendLaunchMeasurement(forTaskID: MXLaunchTaskID) throws](/documentation/metrickit/mxmetricmanager/extendlaunchmeasurement(fortaskid:))
- [class func finishExtendedLaunchMeasurement(forTaskID: MXLaunchTaskID) throws](/documentation/metrickit/mxmetricmanager/finishextendedlaunchmeasurement(fortaskid:))
- [MXLaunchTaskID](/documentation/metrickit/mxlaunchtaskid)

#### Creating a task identifier

- [init(String)](/documentation/metrickit/mxlaunchtaskid/init(_:))
- [init(rawValue: String)](/documentation/metrickit/mxlaunchtaskid/init(rawvalue:))
- [MXMetricPayload](/documentation/metrickit/mxmetricpayload)

### Reading battery metrics

- [var cellularConditionMetrics: MXCellularConditionMetric?](/documentation/metrickit/mxmetricpayload/cellularconditionmetrics)
- [var cpuMetrics: MXCPUMetric?](/documentation/metrickit/mxmetricpayload/cpumetrics)
- [var displayMetrics: MXDisplayMetric?](/documentation/metrickit/mxmetricpayload/displaymetrics)
- [var gpuMetrics: MXGPUMetric?](/documentation/metrickit/mxmetricpayload/gpumetrics)
- [var locationActivityMetrics: MXLocationActivityMetric?](/documentation/metrickit/mxmetricpayload/locationactivitymetrics)
- [var networkTransferMetrics: MXNetworkTransferMetric?](/documentation/metrickit/mxmetricpayload/networktransfermetrics)

### Reading performance metrics

- [var applicationExitMetrics: MXAppExitMetric?](/documentation/metrickit/mxmetricpayload/applicationexitmetrics)
- [var applicationTimeMetrics: MXAppRunTimeMetric?](/documentation/metrickit/mxmetricpayload/applicationtimemetrics)
- [var memoryMetrics: MXMemoryMetric?](/documentation/metrickit/mxmetricpayload/memorymetrics)

### Reading responsiveness metrics

- [var applicationLaunchMetrics: MXAppLaunchMetric?](/documentation/metrickit/mxmetricpayload/applicationlaunchmetrics)
- [var animationMetrics: MXAnimationMetric?](/documentation/metrickit/mxmetricpayload/animationmetrics)
- [var applicationResponsivenessMetrics: MXAppResponsivenessMetric?](/documentation/metrickit/mxmetricpayload/applicationresponsivenessmetrics)

### Reading disk access metrics

- [var diskIOMetrics: MXDiskIOMetric?](/documentation/metrickit/mxmetricpayload/diskiometrics)

### Reading custom metrics

- [var signpostMetrics: [MXSignpostMetric]?](/documentation/metrickit/mxmetricpayload/signpostmetrics)

### Generating a report

- [func jsonRepresentation() -> Data](/documentation/metrickit/mxmetricpayload/jsonrepresentation())
- [func dictionaryRepresentation() -> [AnyHashable : Any]](/documentation/metrickit/mxmetricpayload/dictionaryrepresentation())

### Reading information about the payload

- [var timeStampBegin: Date](/documentation/metrickit/mxmetricpayload/timestampbegin)
- [var timeStampEnd: Date](/documentation/metrickit/mxmetricpayload/timestampend)
- [var includesMultipleApplicationVersions: Bool](/documentation/metrickit/mxmetricpayload/includesmultipleapplicationversions)
- [var latestApplicationVersion: String](/documentation/metrickit/mxmetricpayload/latestapplicationversion)
- [var metaData: MXMetaData?](/documentation/metrickit/mxmetricpayload/metadata)

### Instance Properties

- [var diskSpaceUsageMetrics: MXDiskSpaceUsageMetric?](/documentation/metrickit/mxmetricpayload/diskspaceusagemetrics)
- [MXDiagnosticPayload](/documentation/metrickit/mxdiagnosticpayload)

### Reading performance metrics

- [var crashDiagnostics: [MXCrashDiagnostic]?](/documentation/metrickit/mxdiagnosticpayload/crashdiagnostics)
- [var cpuExceptionDiagnostics: [MXCPUExceptionDiagnostic]?](/documentation/metrickit/mxdiagnosticpayload/cpuexceptiondiagnostics)

### Reading responsiveness metrics

- [var appLaunchDiagnostics: [MXAppLaunchDiagnostic]?](/documentation/metrickit/mxdiagnosticpayload/applaunchdiagnostics)
- [var hangDiagnostics: [MXHangDiagnostic]?](/documentation/metrickit/mxdiagnosticpayload/hangdiagnostics)

### Reading disk access metrics

- [var diskWriteExceptionDiagnostics: [MXDiskWriteExceptionDiagnostic]?](/documentation/metrickit/mxdiagnosticpayload/diskwriteexceptiondiagnostics)

### Generating a report

- [func jsonRepresentation() -> Data](/documentation/metrickit/mxdiagnosticpayload/jsonrepresentation())
- [func dictionaryRepresentation() -> [AnyHashable : Any]](/documentation/metrickit/mxdiagnosticpayload/dictionaryrepresentation())

### Reading information about the payload

- [var timeStampBegin: Date](/documentation/metrickit/mxdiagnosticpayload/timestampbegin)
- [var timeStampEnd: Date](/documentation/metrickit/mxdiagnosticpayload/timestampend)
- [MXMetricManagerSubscriber](/documentation/metrickit/mxmetricmanagersubscriber)

### Receiving reports

- [func didReceive([MXMetricPayload])](/documentation/metrickit/mxmetricmanagersubscriber/didreceive(_:)-3zq5g)
- [func didReceive([MXDiagnosticPayload])](/documentation/metrickit/mxmetricmanagersubscriber/didreceive(_:)-9yd4u)

## Performance improvements

- [Improving your app’s performance](/documentation/xcode/improving-your-app-s-performance)

## Battery metrics

- [MXCellularConditionMetric](/documentation/metrickit/mxcellularconditionmetric)

### Viewing cellular connectivity metrics

- [var histogrammedCellularConditionTime: MXHistogram<MXUnitSignalBars>](/documentation/metrickit/mxcellularconditionmetric/histogrammedcellularconditiontime)
- [MXUnitSignalBars](/documentation/metrickit/mxunitsignalbars)

#### Measuring Connection Strength

- [class var bars: MXUnitSignalBars](/documentation/metrickit/mxunitsignalbars/bars)
- [MXCPUMetric](/documentation/metrickit/mxcpumetric)

### Reading CPU use

- [var cumulativeCPUTime: Measurement<UnitDuration>](/documentation/metrickit/mxcpumetric/cumulativecputime)
- [var cumulativeCPUInstructions: Measurement<Unit>](/documentation/metrickit/mxcpumetric/cumulativecpuinstructions)
- [MXDisplayMetric](/documentation/metrickit/mxdisplaymetric)

### Reading average active pixel use

- [var averagePixelLuminance: MXAverage<MXUnitAveragePixelLuminance>?](/documentation/metrickit/mxdisplaymetric/averagepixelluminance)
- [MXUnitAveragePixelLuminance](/documentation/metrickit/mxunitaveragepixelluminance)

#### Measuring Average Pixel Luminance

- [class var apl: MXUnitAveragePixelLuminance](/documentation/metrickit/mxunitaveragepixelluminance/apl)
- [MXGPUMetric](/documentation/metrickit/mxgpumetric)

### Reading GPU use

- [var cumulativeGPUTime: Measurement<UnitDuration>](/documentation/metrickit/mxgpumetric/cumulativegputime)
- [MXLocationActivityMetric](/documentation/metrickit/mxlocationactivitymetric)

### Reading location services use

- [var cumulativeBestAccuracyForNavigationTime: Measurement<UnitDuration>](/documentation/metrickit/mxlocationactivitymetric/cumulativebestaccuracyfornavigationtime)
- [var cumulativeBestAccuracyTime: Measurement<UnitDuration>](/documentation/metrickit/mxlocationactivitymetric/cumulativebestaccuracytime)
- [var cumulativeNearestTenMetersAccuracyTime: Measurement<UnitDuration>](/documentation/metrickit/mxlocationactivitymetric/cumulativenearesttenmetersaccuracytime)
- [var cumulativeHundredMetersAccuracyTime: Measurement<UnitDuration>](/documentation/metrickit/mxlocationactivitymetric/cumulativehundredmetersaccuracytime)
- [var cumulativeKilometerAccuracyTime: Measurement<UnitDuration>](/documentation/metrickit/mxlocationactivitymetric/cumulativekilometeraccuracytime)
- [var cumulativeThreeKilometersAccuracyTime: Measurement<UnitDuration>](/documentation/metrickit/mxlocationactivitymetric/cumulativethreekilometersaccuracytime)
- [MXNetworkTransferMetric](/documentation/metrickit/mxnetworktransfermetric)

### Reading wireless data use

- [var cumulativeCellularDownload: Measurement<UnitInformationStorage>](/documentation/metrickit/mxnetworktransfermetric/cumulativecellulardownload)
- [var cumulativeCellularUpload: Measurement<UnitInformationStorage>](/documentation/metrickit/mxnetworktransfermetric/cumulativecellularupload)
- [var cumulativeWifiDownload: Measurement<UnitInformationStorage>](/documentation/metrickit/mxnetworktransfermetric/cumulativewifidownload)
- [var cumulativeWifiUpload: Measurement<UnitInformationStorage>](/documentation/metrickit/mxnetworktransfermetric/cumulativewifiupload)
- [MXCPUExceptionDiagnostic](/documentation/metrickit/mxcpuexceptiondiagnostic)

### Viewing the call stack

- [var callStackTree: MXCallStackTree](/documentation/metrickit/mxcpuexceptiondiagnostic/callstacktree)

### Viewing app CPU time

- [var totalCPUTime: Measurement<UnitDuration>](/documentation/metrickit/mxcpuexceptiondiagnostic/totalcputime)
- [var totalSampledTime: Measurement<UnitDuration>](/documentation/metrickit/mxcpuexceptiondiagnostic/totalsampledtime)

## Performance metrics

- [MXAppLaunchDiagnostic](/documentation/metrickit/mxapplaunchdiagnostic)

### Reading app launch metrics

- [var callStackTree: MXCallStackTree](/documentation/metrickit/mxapplaunchdiagnostic/callstacktree)
- [var launchDuration: Measurement<UnitDuration>](/documentation/metrickit/mxapplaunchdiagnostic/launchduration)
- [MXAppExitMetric](/documentation/metrickit/mxappexitmetric)

### Reading the foreground exit data

- [var foregroundExitData: MXForegroundExitData](/documentation/metrickit/mxappexitmetric/foregroundexitdata)
- [MXForegroundExitData](/documentation/metrickit/mxforegroundexitdata)

#### Reading the Normal Exit Count

- [var cumulativeNormalAppExitCount: Int](/documentation/metrickit/mxforegroundexitdata/cumulativenormalappexitcount)

#### Reading the Abnormal Exit Count

- [var cumulativeAbnormalExitCount: Int](/documentation/metrickit/mxforegroundexitdata/cumulativeabnormalexitcount)

#### Reading the System Termination Count

- [var cumulativeAppWatchdogExitCount: Int](/documentation/metrickit/mxforegroundexitdata/cumulativeappwatchdogexitcount)
- [var cumulativeMemoryResourceLimitExitCount: Int](/documentation/metrickit/mxforegroundexitdata/cumulativememoryresourcelimitexitcount)

#### Reading the Crash Count

- [var cumulativeBadAccessExitCount: Int](/documentation/metrickit/mxforegroundexitdata/cumulativebadaccessexitcount)
- [var cumulativeIllegalInstructionExitCount: Int](/documentation/metrickit/mxforegroundexitdata/cumulativeillegalinstructionexitcount)

### Reading the background exit data

- [var backgroundExitData: MXBackgroundExitData](/documentation/metrickit/mxappexitmetric/backgroundexitdata)
- [MXBackgroundExitData](/documentation/metrickit/mxbackgroundexitdata)

#### Reading the Normal Exit Count

- [var cumulativeNormalAppExitCount: Int](/documentation/metrickit/mxbackgroundexitdata/cumulativenormalappexitcount)

#### Reading the Abnormal Exit Count

- [var cumulativeAbnormalExitCount: Int](/documentation/metrickit/mxbackgroundexitdata/cumulativeabnormalexitcount)

#### Reading the System Termination Count

- [var cumulativeAppWatchdogExitCount: Int](/documentation/metrickit/mxbackgroundexitdata/cumulativeappwatchdogexitcount)
- [var cumulativeCPUResourceLimitExitCount: Int](/documentation/metrickit/mxbackgroundexitdata/cumulativecpuresourcelimitexitcount)
- [var cumulativeMemoryResourceLimitExitCount: Int](/documentation/metrickit/mxbackgroundexitdata/cumulativememoryresourcelimitexitcount)
- [var cumulativeMemoryPressureExitCount: Int](/documentation/metrickit/mxbackgroundexitdata/cumulativememorypressureexitcount)
- [var cumulativeSuspendedWithLockedFileExitCount: Int](/documentation/metrickit/mxbackgroundexitdata/cumulativesuspendedwithlockedfileexitcount)

#### Reading the Crash Count

- [var cumulativeBadAccessExitCount: Int](/documentation/metrickit/mxbackgroundexitdata/cumulativebadaccessexitcount)
- [var cumulativeIllegalInstructionExitCount: Int](/documentation/metrickit/mxbackgroundexitdata/cumulativeillegalinstructionexitcount)

#### Reading the Timeout Count

- [var cumulativeBackgroundTaskAssertionTimeoutExitCount: Int](/documentation/metrickit/mxbackgroundexitdata/cumulativebackgroundtaskassertiontimeoutexitcount)
- [MXAppRunTimeMetric](/documentation/metrickit/mxappruntimemetric)

### Reading application run time

- [var cumulativeForegroundTime: Measurement<UnitDuration>](/documentation/metrickit/mxappruntimemetric/cumulativeforegroundtime)
- [var cumulativeBackgroundTime: Measurement<UnitDuration>](/documentation/metrickit/mxappruntimemetric/cumulativebackgroundtime)
- [var cumulativeBackgroundAudioTime: Measurement<UnitDuration>](/documentation/metrickit/mxappruntimemetric/cumulativebackgroundaudiotime)
- [var cumulativeBackgroundLocationTime: Measurement<UnitDuration>](/documentation/metrickit/mxappruntimemetric/cumulativebackgroundlocationtime)
- [MXMemoryMetric](/documentation/metrickit/mxmemorymetric)

### Measuring memory use

- [var averageSuspendedMemory: MXAverage<UnitInformationStorage>](/documentation/metrickit/mxmemorymetric/averagesuspendedmemory)
- [var peakMemoryUsage: Measurement<UnitInformationStorage>](/documentation/metrickit/mxmemorymetric/peakmemoryusage)
- [MXCrashDiagnostic](/documentation/metrickit/mxcrashdiagnostic)

### Viewing exception details

- [var exceptionType: NSNumber?](/documentation/metrickit/mxcrashdiagnostic/exceptiontype)
- [var exceptionCode: NSNumber?](/documentation/metrickit/mxcrashdiagnostic/exceptioncode)
- [var signal: NSNumber?](/documentation/metrickit/mxcrashdiagnostic/signal)
- [var exceptionReason: MXCrashDiagnosticObjectiveCExceptionReason?](/documentation/metrickit/mxcrashdiagnostic/exceptionreason)
- [var terminationReason: String?](/documentation/metrickit/mxcrashdiagnostic/terminationreason)
- [var virtualMemoryRegionInfo: String?](/documentation/metrickit/mxcrashdiagnostic/virtualmemoryregioninfo)

### Viewing the call stack

- [var callStackTree: MXCallStackTree](/documentation/metrickit/mxcrashdiagnostic/callstacktree)

## Responsiveness metrics

- [MXAnimationMetric](/documentation/metrickit/mxanimationmetric)

### Reading the ratio of scrolling hitch time

- [var scrollHitchTimeRatio: Measurement<Unit>](/documentation/metrickit/mxanimationmetric/scrollhitchtimeratio)

### Reading the ratio of hitch time

- [var hitchTimeRatio: Measurement<Unit>](/documentation/metrickit/mxanimationmetric/hitchtimeratio)
- [MXAppLaunchMetric](/documentation/metrickit/mxapplaunchmetric)

### Viewing app launch and resume time

- [var histogrammedOptimizedTimeToFirstDraw: MXHistogram<UnitDuration>](/documentation/metrickit/mxapplaunchmetric/histogrammedoptimizedtimetofirstdraw)
- [var histogrammedTimeToFirstDraw: MXHistogram<UnitDuration>](/documentation/metrickit/mxapplaunchmetric/histogrammedtimetofirstdraw)
- [var histogrammedApplicationResumeTime: MXHistogram<UnitDuration>](/documentation/metrickit/mxapplaunchmetric/histogrammedapplicationresumetime)
- [var histogrammedExtendedLaunch: MXHistogram<UnitDuration>](/documentation/metrickit/mxapplaunchmetric/histogrammedextendedlaunch)
- [MXAppResponsivenessMetric](/documentation/metrickit/mxappresponsivenessmetric)

### Viewing application unresponsive durations

- [var histogrammedApplicationHangTime: MXHistogram<UnitDuration>](/documentation/metrickit/mxappresponsivenessmetric/histogrammedapplicationhangtime)
- [MXHangDiagnostic](/documentation/metrickit/mxhangdiagnostic)

### Reading total app hang time

- [var hangDuration: Measurement<UnitDuration>](/documentation/metrickit/mxhangdiagnostic/hangduration)

### Viewing the call stack

- [var callStackTree: MXCallStackTree](/documentation/metrickit/mxhangdiagnostic/callstacktree)

## Disk usage metrics

- [MXDiskIOMetric](/documentation/metrickit/mxdiskiometric)

### Reading disk use

- [var cumulativeLogicalWrites: Measurement<UnitInformationStorage>](/documentation/metrickit/mxdiskiometric/cumulativelogicalwrites)
- [MXDiskSpaceUsageMetric](/documentation/metrickit/mxdiskspaceusagemetric)

### Reading file counts

- [var totalBinaryFileCount: Int](/documentation/metrickit/mxdiskspaceusagemetric/totalbinaryfilecount)
- [var totalDataFileCount: Int](/documentation/metrickit/mxdiskspaceusagemetric/totaldatafilecount)

### Reading file sizes

- [var totalBinaryFileSize: Measurement<UnitInformationStorage>](/documentation/metrickit/mxdiskspaceusagemetric/totalbinaryfilesize)
- [var totalCacheFolderSize: Measurement<UnitInformationStorage>](/documentation/metrickit/mxdiskspaceusagemetric/totalcachefoldersize)
- [var totalCloneSize: Measurement<UnitInformationStorage>](/documentation/metrickit/mxdiskspaceusagemetric/totalclonesize)
- [var totalDataFileSize: Measurement<UnitInformationStorage>](/documentation/metrickit/mxdiskspaceusagemetric/totaldatafilesize)

### Reading disk capacity and space

- [var totalDiskSpaceCapacity: Measurement<UnitInformationStorage>](/documentation/metrickit/mxdiskspaceusagemetric/totaldiskspacecapacity)
- [var totalDiskSpaceUsedSize: Measurement<UnitInformationStorage>](/documentation/metrickit/mxdiskspaceusagemetric/totaldiskspaceusedsize)
- [MXDiskWriteExceptionDiagnostic](/documentation/metrickit/mxdiskwriteexceptiondiagnostic)

### Reading total disk writes

- [var totalWritesCaused: Measurement<UnitInformationStorage>](/documentation/metrickit/mxdiskwriteexceptiondiagnostic/totalwritescaused)

### Viewing the call stack

- [var callStackTree: MXCallStackTree](/documentation/metrickit/mxdiskwriteexceptiondiagnostic/callstacktree)

## Custom metrics

- [MXSignpostMetric](/documentation/metrickit/mxsignpostmetric)

### Logging custom metrics

- [func mxSignpost(OSSignpostType, dso: UnsafeRawPointer, log: OSLog, name: StaticString, signpostID: OSSignpostID, StaticString, [any CVarArg])](/documentation/metrickit/mxsignpost(_:dso:log:name:signpostid:_:_:))
- [func mxSignpostAnimationIntervalBegin(dso: UnsafeRawPointer, log: OSLog, name: StaticString, signpostID: OSSignpostID, StaticString, [any CVarArg])](/documentation/metrickit/mxsignpostanimationintervalbegin(dso:log:name:signpostid:_:_:))

### Reading custom metric data

- [var signpostIntervalData: MXSignpostIntervalData?](/documentation/metrickit/mxsignpostmetric/signpostintervaldata)
- [MXSignpostIntervalData](/documentation/metrickit/mxsignpostintervaldata)

#### Reading Histogrammed Custom Metric Durations

- [var histogrammedSignpostDuration: MXHistogram<UnitDuration>](/documentation/metrickit/mxsignpostintervaldata/histogrammedsignpostduration)

#### Reading Power and Performance Information

- [var averageMemory: MXAverage<UnitInformationStorage>?](/documentation/metrickit/mxsignpostintervaldata/averagememory)
- [var cumulativeCPUTime: Measurement<UnitDuration>?](/documentation/metrickit/mxsignpostintervaldata/cumulativecputime)
- [var cumulativeLogicalWrites: Measurement<UnitInformationStorage>?](/documentation/metrickit/mxsignpostintervaldata/cumulativelogicalwrites)
- [var cumulativeHitchTimeRatio: Measurement<Unit>?](/documentation/metrickit/mxsignpostintervaldata/cumulativehitchtimeratio)

### Reading data about the custom metric

- [var signpostName: String](/documentation/metrickit/mxsignpostmetric/signpostname)
- [var signpostCategory: String](/documentation/metrickit/mxsignpostmetric/signpostcategory)
- [var totalCount: Int](/documentation/metrickit/mxsignpostmetric/totalcount)

## Data types

- [MXCallStackTree](/documentation/metrickit/mxcallstacktree)

### Generating a report

- [func jsonRepresentation() -> Data](/documentation/metrickit/mxcallstacktree/jsonrepresentation())
- [MXMetaData](/documentation/metrickit/mxmetadata)

### Reading data about a payload

- [var applicationBuildVersion: String](/documentation/metrickit/mxmetadata/applicationbuildversion)
- [var deviceType: String](/documentation/metrickit/mxmetadata/devicetype)
- [var isTestFlightApp: Bool](/documentation/metrickit/mxmetadata/istestflightapp)
- [var lowPowerModeEnabled: Bool](/documentation/metrickit/mxmetadata/lowpowermodeenabled)
- [var osVersion: String](/documentation/metrickit/mxmetadata/osversion)
- [var platformArchitecture: String](/documentation/metrickit/mxmetadata/platformarchitecture)
- [var regionFormat: String](/documentation/metrickit/mxmetadata/regionformat)
- [var pid: pid_t](/documentation/metrickit/mxmetadata/pid)

### Generating a report

- [func dictionaryRepresentation() -> [AnyHashable : Any]](/documentation/metrickit/mxmetadata/dictionaryrepresentation())
- [func jsonRepresentation() -> Data](/documentation/metrickit/mxmetadata/jsonrepresentation())

### Instance Properties

- [var bundleIdentifier: String](/documentation/metrickit/mxmetadata/bundleidentifier)
- [MXAverage](/documentation/metrickit/mxaverage)

### Reading the data

- [var averageMeasurement: Measurement<UnitType>](/documentation/metrickit/mxaverage/averagemeasurement)
- [var sampleCount: Int](/documentation/metrickit/mxaverage/samplecount)
- [var standardDeviation: Double](/documentation/metrickit/mxaverage/standarddeviation)
- [MXHistogram](/documentation/metrickit/mxhistogram)

### Reading the buckets

- [var bucketEnumerator: NSEnumerator](/documentation/metrickit/mxhistogram/bucketenumerator)
- [var totalBucketCount: Int](/documentation/metrickit/mxhistogram/totalbucketcount)
- [MXHistogramBucket](/documentation/metrickit/mxhistogrambucket)

#### Reading the Data

- [var bucketStart: Measurement<UnitType>](/documentation/metrickit/mxhistogrambucket/bucketstart)
- [var bucketEnd: Measurement<UnitType>](/documentation/metrickit/mxhistogrambucket/bucketend)
- [var bucketCount: Int](/documentation/metrickit/mxhistogrambucket/bucketcount)
- [MXDiagnostic](/documentation/metrickit/mxdiagnostic)

### Reading data About a diagnostic

- [var applicationVersion: String](/documentation/metrickit/mxdiagnostic/applicationversion)
- [var metaData: MXMetaData](/documentation/metrickit/mxdiagnostic/metadata)
- [var signpostData: [MXSignpostRecord]?](/documentation/metrickit/mxdiagnostic/signpostdata)

### Generating a report

- [func jsonRepresentation() -> Data](/documentation/metrickit/mxdiagnostic/jsonrepresentation())
- [func dictionaryRepresentation() -> [AnyHashable : Any]](/documentation/metrickit/mxdiagnostic/dictionaryrepresentation())
- [MXMetric](/documentation/metrickit/mxmetric)

### Generate a report

- [func dictionaryRepresentation() -> [AnyHashable : Any]](/documentation/metrickit/mxmetric/dictionaryrepresentation())
- [func jsonRepresentation() -> Data](/documentation/metrickit/mxmetric/jsonrepresentation())
- [MXError.Code](/documentation/metrickit/mxerror/code)

### Launch errors

- [case launchTaskDuplicated](/documentation/metrickit/mxerror/code/launchtaskduplicated)
- [case launchTaskInternalFailure](/documentation/metrickit/mxerror/code/launchtaskinternalfailure)
- [case launchTaskInvalidID](/documentation/metrickit/mxerror/code/launchtaskinvalidid)
- [case launchTaskMaxCount](/documentation/metrickit/mxerror/code/launchtaskmaxcount)
- [case launchTaskPastDeadline](/documentation/metrickit/mxerror/code/launchtaskpastdeadline)
- [case launchTaskUnknown](/documentation/metrickit/mxerror/code/launchtaskunknown)

### Initializers

- [init?(rawValue: Int)](/documentation/metrickit/mxerror/code/init(rawvalue:))
- [let MXErrorDomain: String](/documentation/metrickit/mxerrordomain)
- [MXError](/documentation/metrickit/mxerror)

### Getting the error properties

- [MXError.Code](/documentation/metrickit/mxerror/code)

#### Launch errors

- [case launchTaskDuplicated](/documentation/metrickit/mxerror/code/launchtaskduplicated)
- [case launchTaskInternalFailure](/documentation/metrickit/mxerror/code/launchtaskinternalfailure)
- [case launchTaskInvalidID](/documentation/metrickit/mxerror/code/launchtaskinvalidid)
- [case launchTaskMaxCount](/documentation/metrickit/mxerror/code/launchtaskmaxcount)
- [case launchTaskPastDeadline](/documentation/metrickit/mxerror/code/launchtaskpastdeadline)
- [case launchTaskUnknown](/documentation/metrickit/mxerror/code/launchtaskunknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/metrickit/mxerror/code/init(rawvalue:))
- [let MXErrorDomain: String](/documentation/metrickit/mxerrordomain)

### Getting the launch error properties

- [static var launchTaskDuplicated: MXError.Code](/documentation/metrickit/mxerror/launchtaskduplicated)
- [static var launchTaskInternalFailure: MXError.Code](/documentation/metrickit/mxerror/launchtaskinternalfailure)
- [static var launchTaskInvalidID: MXError.Code](/documentation/metrickit/mxerror/launchtaskinvalidid)
- [static var launchTaskMaxCount: MXError.Code](/documentation/metrickit/mxerror/launchtaskmaxcount)
- [static var launchTaskPastDeadline: MXError.Code](/documentation/metrickit/mxerror/launchtaskpastdeadline)
- [static var launchTaskUnknown: MXError.Code](/documentation/metrickit/mxerror/launchtaskunknown)
- [MXError.Code](/documentation/metrickit/mxerror/code)

#### Launch errors

- [case launchTaskDuplicated](/documentation/metrickit/mxerror/code/launchtaskduplicated)
- [case launchTaskInternalFailure](/documentation/metrickit/mxerror/code/launchtaskinternalfailure)
- [case launchTaskInvalidID](/documentation/metrickit/mxerror/code/launchtaskinvalidid)
- [case launchTaskMaxCount](/documentation/metrickit/mxerror/code/launchtaskmaxcount)
- [case launchTaskPastDeadline](/documentation/metrickit/mxerror/code/launchtaskpastdeadline)
- [case launchTaskUnknown](/documentation/metrickit/mxerror/code/launchtaskunknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/metrickit/mxerror/code/init(rawvalue:))
- [let MXErrorDomain: String](/documentation/metrickit/mxerrordomain)

### Type Properties

- [static var errorDomain: String](/documentation/metrickit/mxerror/errordomain)
- [MXCrashDiagnosticObjectiveCExceptionReason](/documentation/metrickit/mxcrashdiagnosticobjectivecexceptionreason)

### Generating a report

- [func dictionaryRepresentation() -> [AnyHashable : Any]](/documentation/metrickit/mxcrashdiagnosticobjectivecexceptionreason/dictionaryrepresentation())
- [func jsonRepresentation() -> Data](/documentation/metrickit/mxcrashdiagnosticobjectivecexceptionreason/jsonrepresentation())

### Reading the data

- [var arguments: [String]](/documentation/metrickit/mxcrashdiagnosticobjectivecexceptionreason/arguments)
- [var className: String](/documentation/metrickit/mxcrashdiagnosticobjectivecexceptionreason/classname)
- [var composedMessage: String](/documentation/metrickit/mxcrashdiagnosticobjectivecexceptionreason/composedmessage)
- [var exceptionName: String](/documentation/metrickit/mxcrashdiagnosticobjectivecexceptionreason/exceptionname)
- [var exceptionType: String](/documentation/metrickit/mxcrashdiagnosticobjectivecexceptionreason/exceptiontype)
- [var formatString: String](/documentation/metrickit/mxcrashdiagnosticobjectivecexceptionreason/formatstring)
- [MXSignpostRecord](/documentation/metrickit/mxsignpostrecord)

### Generating a report

- [func dictionaryRepresentation() -> [AnyHashable : Any]](/documentation/metrickit/mxsignpostrecord/dictionaryrepresentation())
- [func jsonRepresentation() -> Data](/documentation/metrickit/mxsignpostrecord/jsonrepresentation())

### Reading the data

- [var beginTimeStamp: Date](/documentation/metrickit/mxsignpostrecord/begintimestamp)
- [var category: String](/documentation/metrickit/mxsignpostrecord/category)
- [var duration: Measurement<UnitDuration>?](/documentation/metrickit/mxsignpostrecord/duration)
- [var endTimeStamp: Date?](/documentation/metrickit/mxsignpostrecord/endtimestamp)
- [var isInterval: Bool](/documentation/metrickit/mxsignpostrecord/isinterval)
- [var name: String](/documentation/metrickit/mxsignpostrecord/name)
- [var subsystem: String](/documentation/metrickit/mxsignpostrecord/subsystem)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
