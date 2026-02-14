# Background Assets Documentation

Source: https://sosumi.ai/documentation/backgroundassets

---
title: Background Assets
source: https://developer.apple.com/documentation/backgroundassets
timestamp: 2026-02-13T18:54:20.176Z
---

## Essentials

- [Creating managed asset packs](/documentation/backgroundassets/creating-managed-asset-packs)
- [Downloading Apple-hosted asset packs](/documentation/backgroundassets/downloading-apple-hosted-asset-packs)
- [Testing asset packs locally](/documentation/backgroundassets/testing-asset-packs-locally)

## Managed asset packs

- [BAAssetPack](/documentation/backgroundassets/assetpack)

### Identifying assets


### Accessing asset details


### Downloading assets

- [BAAssetPackManager](/documentation/backgroundassets/assetpackmanager)

### Getting the shared manager


### Tracking downloads


### Accessing asset packs


### Managing asset packs

- [ManagedDownloaderExtension](/documentation/backgroundassets/manageddownloaderextension)

### Downloading assets

- [func shouldDownload(AssetPack) -> Bool](/documentation/backgroundassets/manageddownloaderextension/shoulddownload(_:))
- [BAAppGroupID](/documentation/bundleresources/information-property-list/baappgroupid)
- [BAHasManagedAssetPacks](/documentation/bundleresources/information-property-list/bahasmanagedassetpacks)

## Apple-hosted managed asset packs

- [BAUsesAppleHosting](/documentation/bundleresources/information-property-list/bausesapplehosting)

## Self-hosted unmanaged asset packs

- [BAAssetPackManifest](/documentation/backgroundassets/assetpackmanifest)

### Creating an asset pack manifest


### Accessing downloads


### Getting asset packs


## Unmanaged asset downloads

- [Configuring an unmanaged Background Assets project](/documentation/backgroundassets/configuring-an-unmanaged-background-assets-project)
- [Downloading essential assets in the background](/documentation/backgroundassets/downloading-essential-assets-in-the-background)
- [BAManifestURL](/documentation/bundleresources/information-property-list/bamanifesturl)
- [BAInitialDownloadRestrictions](/documentation/bundleresources/information-property-list/bainitialdownloadrestrictions)
- [BAEssentialMaxInstallSize](/documentation/bundleresources/information-property-list/baessentialmaxinstallsize)
- [BAMaxInstallSize](/documentation/bundleresources/information-property-list/bamaxinstallsize)
- [BADownloadManager](/documentation/backgroundassets/badownloadmanager)

### Accessing the download manager

- [class var shared: BADownloadManager](/documentation/backgroundassets/badownloadmanager/shared)

### Managing downloads

- [func scheduleDownload(BADownload) throws](/documentation/backgroundassets/badownloadmanager/scheduledownload(_:))
- [func startForegroundDownload(BADownload) throws](/documentation/backgroundassets/badownloadmanager/startforegrounddownload(_:))
- [func cancel(BADownload) throws](/documentation/backgroundassets/badownloadmanager/cancel(_:))

### Monitoring downloads

- [var delegate: (any BADownloadManagerDelegate)?](/documentation/backgroundassets/badownloadmanager/delegate)
- [BADownloadManagerDelegate](/documentation/backgroundassets/badownloadmanagerdelegate)

#### Reacting to download events

- [func downloadDidBegin(BADownload)](/documentation/backgroundassets/badownloadmanagerdelegate/downloaddidbegin(_:))
- [func download(BADownload, didReceive: URLAuthenticationChallenge, completionHandler: (URLSession.AuthChallengeDisposition, URLCredential?) -> Void)](/documentation/backgroundassets/badownloadmanagerdelegate/download(_:didreceive:completionhandler:))
- [func download(BADownload, didWriteBytes: Int64, totalBytesWritten: Int64, totalBytesExpectedToWrite: Int64)](/documentation/backgroundassets/badownloadmanagerdelegate/download(_:didwritebytes:totalbyteswritten:totalbytesexpectedtowrite:))
- [func downloadDidPause(BADownload)](/documentation/backgroundassets/badownloadmanagerdelegate/downloaddidpause(_:))

#### Processing concluded downloads

- [func download(BADownload, finishedWithFileURL: URL)](/documentation/backgroundassets/badownloadmanagerdelegate/download(_:finishedwithfileurl:))
- [func download(BADownload, failedWithError: any Error)](/documentation/backgroundassets/badownloadmanagerdelegate/download(_:failedwitherror:))

### Fetching in-progress downloads

- [func fetchCurrentDownloads() throws -> [BADownload]](/documentation/backgroundassets/badownloadmanager/fetchcurrentdownloads())
- [func fetchCurrentDownloads(completionHandler: ([BADownload], (any Error)?) -> Void)](/documentation/backgroundassets/badownloadmanager/fetchcurrentdownloads(completionhandler:))

### Synchronizing manager access

- [func withExclusiveControl((Bool, (any Error)?) -> Void)](/documentation/backgroundassets/badownloadmanager/withexclusivecontrol(_:))
- [func withExclusiveControl(beforeDate: Date, perform: (Bool, (any Error)?) -> Void)](/documentation/backgroundassets/badownloadmanager/withexclusivecontrol(beforedate:perform:))
- [BADownloaderExtension](/documentation/backgroundassets/badownloaderextension-qwaw)

### Processing downloads

- [func backgroundDownload(BADownload, didReceive: URLAuthenticationChallenge) async -> (URLSession.AuthChallengeDisposition, URLCredential?)](/documentation/backgroundassets/badownloaderextension-qwaw/backgrounddownload(_:didreceive:))
- [func backgroundDownload(BADownload, finishedWithFileURL: URL)](/documentation/backgroundassets/badownloaderextension-qwaw/backgrounddownload(_:finishedwithfileurl:))
- [func backgroundDownload(BADownload, failedWithError: any Error)](/documentation/backgroundassets/badownloaderextension-qwaw/backgrounddownload(_:failedwitherror:))

### Checking for asset updates

- [func downloads(for: BAContentRequest, manifestURL: URL, extensionInfo: BAAppExtensionInfo) -> Set<BADownload>](/documentation/backgroundassets/badownloaderextension-qwaw/downloads(for:manifesturl:extensioninfo:))
- [BAContentRequest](/documentation/backgroundassets/bacontentrequest)

#### Content request types

- [case install](/documentation/backgroundassets/bacontentrequest/install)
- [case periodic](/documentation/backgroundassets/bacontentrequest/periodic)
- [case update](/documentation/backgroundassets/bacontentrequest/update)

#### Initializers

- [init?(rawValue: Int)](/documentation/backgroundassets/bacontentrequest/init(rawvalue:))
- [BAAppExtensionInfo](/documentation/backgroundassets/baappextensioninfo)

#### Getting the size of the remaining downloads

- [var restrictedEssentialDownloadSizeRemaining: Int?](/documentation/backgroundassets/baappextensioninfo/restrictedessentialdownloadsizeremaining-5r8v0)
- [var restrictedDownloadSizeRemaining: Int?](/documentation/backgroundassets/baappextensioninfo/restricteddownloadsizeremaining-4hea4)

### Reacting to extension events

- [func extensionWillTerminate()](/documentation/backgroundassets/badownloaderextension-qwaw/extensionwillterminate()-236ac)

### Instance Methods

- [func extensionWillTerminate()](/documentation/backgroundassets/badownloaderextension-qwaw/extensionwillterminate())
- [BADownloaderExtensionConfiguration](/documentation/backgroundassets/badownloaderextensionconfiguration)
- [BAURLDownload](/documentation/backgroundassets/baurldownload)

### Creating a download

- [init(identifier: String, request: URLRequest, essential: Bool, fileSize: Int, applicationGroupIdentifier: String, priority: BADownload.Priority)](/documentation/backgroundassets/baurldownload/init(identifier:request:essential:filesize:applicationgroupidentifier:priority:))
- [convenience init(identifier: String, request: URLRequest, fileSize: Int, applicationGroupIdentifier: String)](/documentation/backgroundassets/baurldownload/init(identifier:request:filesize:applicationgroupidentifier:))
- [convenience init(identifier: String, request: URLRequest, applicationGroupIdentifier: String)](/documentation/backgroundassets/baurldownload/init(identifier:request:applicationgroupidentifier:))
- [convenience init(identifier: String, request: URLRequest, applicationGroupIdentifier: String, priority: BADownload.Priority)](/documentation/backgroundassets/baurldownload/init(identifier:request:applicationgroupidentifier:priority:))
- [BADownload](/documentation/backgroundassets/badownload)

### Getting the identity

- [var identifier: String](/documentation/backgroundassets/badownload/identifier)
- [var uniqueIdentifier: String](/documentation/backgroundassets/badownload/uniqueidentifier)

### Determining the priority

- [var isEssential: Bool](/documentation/backgroundassets/badownload/isessential)
- [var priority: BADownload.Priority](/documentation/backgroundassets/badownload/priority-swift.property)
- [BADownload.Priority](/documentation/backgroundassets/badownload/priority-swift.struct)

#### Creating a priority

- [init(Int)](/documentation/backgroundassets/badownload/priority-swift.struct/init(_:))
- [init(rawValue: Int)](/documentation/backgroundassets/badownload/priority-swift.struct/init(rawvalue:))

#### Getting system priorities

- [static let `default`: BADownload.Priority](/documentation/backgroundassets/badownload/priority-swift.struct/default)
- [static let min: BADownload.Priority](/documentation/backgroundassets/badownload/priority-swift.struct/min)
- [static let max: BADownload.Priority](/documentation/backgroundassets/badownload/priority-swift.struct/max)

### Getting the current state

- [var state: BADownload.State](/documentation/backgroundassets/badownload/state-swift.property)
- [BADownload.State](/documentation/backgroundassets/badownload/state-swift.enum)

#### Download states

- [case created](/documentation/backgroundassets/badownload/state-swift.enum/created)
- [case waiting](/documentation/backgroundassets/badownload/state-swift.enum/waiting)
- [case downloading](/documentation/backgroundassets/badownload/state-swift.enum/downloading)
- [case finished](/documentation/backgroundassets/badownload/state-swift.enum/finished)
- [case failed](/documentation/backgroundassets/badownload/state-swift.enum/failed)

#### Initializers

- [init?(rawValue: Int)](/documentation/backgroundassets/badownload/state-swift.enum/init(rawvalue:))

### Downloading nonessential assets

- [func removingEssential() -> Self](/documentation/backgroundassets/badownload/removingessential())

## Errors

- [ManagedBackgroundAssetsError](/documentation/backgroundassets/managedbackgroundassetserror)

### Errors

- [case assetPackNotFound(withID: String)](/documentation/backgroundassets/managedbackgroundassetserror/assetpacknotfound(withid:))
- [case fileNotFound(at: FilePath)](/documentation/backgroundassets/managedbackgroundassetserror/filenotfound(at:))
- [let BAErrorDomain: String](/documentation/backgroundassets/baerrordomain)
- [BAErrorCode](/documentation/backgroundassets/baerrorcode)

### Error codes

- [case callFromExtensionNotAllowed](/documentation/backgroundassets/baerrorcode/callfromextensionnotallowed)
- [case callFromInactiveProcessNotAllowed](/documentation/backgroundassets/baerrorcode/callfrominactiveprocessnotallowed)
- [case callerConnectionInvalid](/documentation/backgroundassets/baerrorcode/callerconnectioninvalid)
- [case callerConnectionNotAccepted](/documentation/backgroundassets/baerrorcode/callerconnectionnotaccepted)
- [case downloadAlreadyFailed](/documentation/backgroundassets/baerrorcode/downloadalreadyfailed)
- [case downloadAlreadyScheduled](/documentation/backgroundassets/baerrorcode/downloadalreadyscheduled)
- [case downloadBackgroundActivityProhibited](/documentation/backgroundassets/baerrorcode/downloadbackgroundactivityprohibited)
- [case downloadEssentialDownloadNotPermitted](/documentation/backgroundassets/baerrorcode/downloadessentialdownloadnotpermitted)
- [case downloadFailedToStart](/documentation/backgroundassets/baerrorcode/downloadfailedtostart)
- [case downloadInvalid](/documentation/backgroundassets/baerrorcode/downloadinvalid)
- [case downloadNotScheduled](/documentation/backgroundassets/baerrorcode/downloadnotscheduled)
- [case downloadWouldExceedAllowance](/documentation/backgroundassets/baerrorcode/downloadwouldexceedallowance)
- [case sessionDownloadAllowanceExceeded](/documentation/backgroundassets/baerrorcode/sessiondownloadallowanceexceeded)
- [case sessionDownloadDisallowedByAllowance](/documentation/backgroundassets/baerrorcode/sessiondownloaddisallowedbyallowance)
- [case sessionDownloadDisallowedByDomain](/documentation/backgroundassets/baerrorcode/sessiondownloaddisallowedbydomain)
- [case sessionDownloadNotPermittedBeforeAppLaunch](/documentation/backgroundassets/baerrorcode/sessiondownloadnotpermittedbeforeapplaunch)

### Initializers

- [init?(rawValue: Int)](/documentation/backgroundassets/baerrorcode/init(rawvalue:))

### Enumeration Cases

- [case downloadDoesNotExist](/documentation/backgroundassets/baerrorcode/downloaddoesnotexist)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
