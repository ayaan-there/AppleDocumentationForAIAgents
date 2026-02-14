# ImageCaptureCore Documentation

Source: https://sosumi.ai/documentation/imagecapturecore

---
title: ImageCaptureCore
source: https://developer.apple.com/documentation/imagecapturecore
timestamp: 2026-02-13T18:58:08.773Z
---

## Essentials

- [ICDeviceBrowser](/documentation/imagecapturecore/icdevicebrowser)

### Creating a Device Browser

- [init()](/documentation/imagecapturecore/icdevicebrowser/1507596-init)

### Managing Device Browsing

- [var delegate: (any ICDeviceBrowserDelegate)?](/documentation/imagecapturecore/icdevicebrowser/1508148-delegate)
- [ICDeviceBrowserDelegate](/documentation/imagecapturecore/icdevicebrowserdelegate)

#### Adding and Removing Devices

- [func deviceBrowser(ICDeviceBrowser, didAdd: ICDevice, moreComing: Bool)](/documentation/imagecapturecore/icdevicebrowserdelegate/1507732-devicebrowser)
- [func deviceBrowser(ICDeviceBrowser, didRemove: ICDevice, moreGoing: Bool)](/documentation/imagecapturecore/icdevicebrowserdelegate/1507686-devicebrowser)
- [func deviceBrowserDidEnumerateLocalDevices(ICDeviceBrowser)](/documentation/imagecapturecore/icdevicebrowserdelegate/1507983-devicebrowserdidenumeratelocalde)

#### Responding to Device Changes

- [func deviceBrowser(ICDeviceBrowser, requestsSelect: ICDevice)](/documentation/imagecapturecore/icdevicebrowserdelegate/1507647-devicebrowser)
- [func deviceBrowser(ICDeviceBrowser, deviceDidChangeName: ICDevice)](/documentation/imagecapturecore/icdevicebrowserdelegate/1507673-devicebrowser)
- [func deviceBrowser(ICDeviceBrowser, deviceDidChangeSharingState: ICDevice)](/documentation/imagecapturecore/icdevicebrowserdelegate/1507914-devicebrowser)

#### Instance Methods

- [func deviceBrowserDidCancelSuspendOperations(ICDeviceBrowser)](/documentation/imagecapturecore/icdevicebrowserdelegate/3650396-devicebrowserdidcancelsuspendope)
- [func deviceBrowserDidResumeOperations(ICDeviceBrowser)](/documentation/imagecapturecore/icdevicebrowserdelegate/3650397-devicebrowserdidresumeoperations)
- [func deviceBrowserDidSuspendOperations(ICDeviceBrowser)](/documentation/imagecapturecore/icdevicebrowserdelegate/3650398-devicebrowserdidsuspendoperation)
- [func deviceBrowserWillSuspendOperations(ICDeviceBrowser)](/documentation/imagecapturecore/icdevicebrowserdelegate/3650399-devicebrowserwillsuspendoperatio)

### Browsing Devices

- [var isBrowsing: Bool](/documentation/imagecapturecore/icdevicebrowser/1507627-isbrowsing)
- [var devices: [ICDevice]?](/documentation/imagecapturecore/icdevicebrowser/1507765-devices)
- [ICDevice](/documentation/imagecapturecore/icdevice)

#### Identifying a Device

- [var name: String?](/documentation/imagecapturecore/icdevice/1507989-name)
- [var productKind: String?](/documentation/imagecapturecore/icdevice/3142912-productkind)
- [var icon: CGImage?](/documentation/imagecapturecore/icdevice/1507860-icon)
- [var uuidString: String?](/documentation/imagecapturecore/icdevice/1507999-uuidstring)
- [var persistentIDString: String?](/documentation/imagecapturecore/icdevice/1507918-persistentidstring)
- [var serialNumberString: String?](/documentation/imagecapturecore/icdevice/1508137-serialnumberstring)

#### Inspecting a Device’s Type and Location

- [var type: ICDeviceType](/documentation/imagecapturecore/icdevice/1507909-type)
- [ICDeviceType](/documentation/imagecapturecore/icdevicetype)

##### Enumeration Cases

- [case camera](/documentation/imagecapturecore/icdevicetype/camera)
- [case scanner](/documentation/imagecapturecore/icdevicetype/scanner)
- [ICDeviceTypeMask](/documentation/imagecapturecore/icdevicetypemask)

##### Enumeration Cases

- [case camera](/documentation/imagecapturecore/icdevicetypemask/camera)
- [case scanner](/documentation/imagecapturecore/icdevicetypemask/scanner)
- [var locationDescription: String?](/documentation/imagecapturecore/icdevice/1507717-locationdescription)
- [var modulePath: String](/documentation/imagecapturecore/icdevice/1507800-modulepath)
- [var moduleVersion: String?](/documentation/imagecapturecore/icdevice/1507835-moduleversion)
- [ICDeviceLocationType](/documentation/imagecapturecore/icdevicelocationtype)

##### Enumeration Cases

- [case bluetooth](/documentation/imagecapturecore/icdevicelocationtype/bluetooth)
- [case bonjour](/documentation/imagecapturecore/icdevicelocationtype/bonjour)
- [case local](/documentation/imagecapturecore/icdevicelocationtype/local)
- [case shared](/documentation/imagecapturecore/icdevicelocationtype/shared)
- [ICDeviceLocationTypeMask](/documentation/imagecapturecore/icdevicelocationtypemask)

##### Enumeration Cases

- [case bluetooth](/documentation/imagecapturecore/icdevicelocationtypemask/bluetooth)
- [case bonjour](/documentation/imagecapturecore/icdevicelocationtypemask/bonjour)
- [case local](/documentation/imagecapturecore/icdevicelocationtypemask/local)
- [case remote](/documentation/imagecapturecore/icdevicelocationtypemask/remote)
- [case shared](/documentation/imagecapturecore/icdevicelocationtypemask/shared)
- [ICDeviceLocationOptions](/documentation/imagecapturecore/icdevicelocationoptions)

##### Creating Location Options

- [init(rawValue: String)](/documentation/imagecapturecore/icdevicelocationoptions/3192075-init)

##### Determining a Location

- [static let descriptionBluetooth: ICDeviceLocationOptions](/documentation/imagecapturecore/icdevicelocationoptions/1507599-descriptionbluetooth)
- [static let descriptionFireWire: ICDeviceLocationOptions](/documentation/imagecapturecore/icdevicelocationoptions/1508166-descriptionfirewire)
- [static let descriptionMassStorage: ICDeviceLocationOptions](/documentation/imagecapturecore/icdevicelocationoptions/1507831-descriptionmassstorage)
- [static let descriptionUSB: ICDeviceLocationOptions](/documentation/imagecapturecore/icdevicelocationoptions/1507694-descriptionusb)
- [var usbLocationID: Int32](/documentation/imagecapturecore/icdevice/1507614-usblocationid)
- [var usbProductID: Int32](/documentation/imagecapturecore/icdevice/1507716-usbproductid)
- [var usbVendorID: Int32](/documentation/imagecapturecore/icdevice/1507787-usbvendorid)

#### Inspecting a Device’s Transport Type

- [var transportType: String?](/documentation/imagecapturecore/icdevice/1507904-transporttype)
- [ICDeviceTransport](/documentation/imagecapturecore/icdevicetransport)

##### Initializers

- [init(rawValue: String)](/documentation/imagecapturecore/icdevicetransport/3143740-init)

##### Type Properties

- [static let transportTypeBluetooth: ICDeviceTransport](/documentation/imagecapturecore/icdevicetransport/1508035-transporttypebluetooth)
- [static let transportTypeExFAT: ICDeviceTransport](/documentation/imagecapturecore/icdevicetransport/3183648-transporttypeexfat)
- [static let transportTypeFireWire: ICDeviceTransport](/documentation/imagecapturecore/icdevicetransport/1507767-transporttypefirewire)
- [static let transportTypeMassStorage: ICDeviceTransport](/documentation/imagecapturecore/icdevicetransport/1507883-transporttypemassstorage)
- [static let transportTypeProximity: ICDeviceTransport](/documentation/imagecapturecore/icdevicetransport/4168399-transporttypeproximity)
- [static let transportTypeTCPIP: ICDeviceTransport](/documentation/imagecapturecore/icdevicetransport/1507947-transporttypetcpip)
- [static let transportTypeUSB: ICDeviceTransport](/documentation/imagecapturecore/icdevicetransport/1508049-transporttypeusb)

#### Inspecting a Device’s Capabilities

- [var capabilities: [String]](/documentation/imagecapturecore/icdevice/1507594-capabilities)
- [ICDeviceCapability](/documentation/imagecapturecore/icdevicecapability)

##### Creating Device Capabilities

- [init(rawValue: String)](/documentation/imagecapturecore/icdevicecapability/3143725-init)

##### Taking Pictures

- [static let cameraDeviceCanTakePicture: ICDeviceCapability](/documentation/imagecapturecore/icdevicecapability/1507939-cameradevicecantakepicture)
- [static let cameraDeviceCanTakePictureUsingShutterReleaseOnCamera: ICDeviceCapability](/documentation/imagecapturecore/icdevicecapability/1508150-cameradevicecantakepictureusings)

##### Deleting Files

- [static let cameraDeviceCanDeleteOneFile: ICDeviceCapability](/documentation/imagecapturecore/icdevicecapability/1508131-cameradevicecandeleteonefile)
- [static let cameraDeviceCanDeleteAllFiles: ICDeviceCapability](/documentation/imagecapturecore/icdevicecapability/1507766-cameradevicecandeleteallfiles)

##### Uploading Files

- [static let cameraDeviceCanReceiveFile: ICDeviceCapability](/documentation/imagecapturecore/icdevicecapability/1507851-cameradevicecanreceivefile)

##### Synchronizing the Clock

- [static let cameraDeviceCanSyncClock: ICDeviceCapability](/documentation/imagecapturecore/icdevicecapability/1508135-cameradevicecansyncclock)

##### Sending PTP Commands

- [static let cameraDeviceCanAcceptPTPCommands: ICDeviceCapability](/documentation/imagecapturecore/icdevicecapability/1508076-cameradevicecanacceptptpcommands)

##### Disconnecting

- [static let canEjectOrDisconnect: ICDeviceCapability](/documentation/imagecapturecore/icdevicecapability/1507814-canejectordisconnect)

##### Type Properties

- [static let cameraDeviceSupportsHEIF: ICDeviceCapability](/documentation/imagecapturecore/icdevicecapability/3601136-cameradevicesupportsheif)
- [ICSessionOptions](/documentation/imagecapturecore/icsessionoptions)

##### Initializers

- [init(rawValue: String)](/documentation/imagecapturecore/icsessionoptions/3143808-init)

##### Type Properties

- [static let enumerationChronologicalOrder: ICSessionOptions](/documentation/imagecapturecore/icsessionoptions/3142921-enumerationchronologicalorder)

#### Subscribing to Device Status Notifications

- [ICDeviceStatus](/documentation/imagecapturecore/icdevicestatus)

##### Initializers

- [init(rawValue: String)](/documentation/imagecapturecore/icdevicestatus/3143739-init)

##### Type Properties

- [static let localizedStatusNotificationKey: ICDeviceStatus](/documentation/imagecapturecore/icdevicestatus/1507718-localizedstatusnotificationkey)
- [static let statusCodeKey: ICDeviceStatus](/documentation/imagecapturecore/icdevicestatus/1508044-statuscodekey)
- [static let statusNotificationKey: ICDeviceStatus](/documentation/imagecapturecore/icdevicestatus/1507705-statusnotificationkey)

#### Managing a Device

- [var delegate: (any ICDeviceDelegate)?](/documentation/imagecapturecore/icdevice/1507701-delegate)
- [ICDeviceDelegate](/documentation/imagecapturecore/icdevicedelegate)

##### Responding to Device Events

- [func device(ICDevice, didOpenSessionWithError: (any Error)?)](/documentation/imagecapturecore/icdevicedelegate/1508020-device)
- [func device(ICDevice, didCloseSessionWithError: (any Error)?)](/documentation/imagecapturecore/icdevicedelegate/1507874-device)
- [func didRemove(ICDevice)](/documentation/imagecapturecore/icdevicedelegate/1507872-didremove)
- [func deviceDidBecomeReady(ICDevice)](/documentation/imagecapturecore/icdevicedelegate/1507769-devicedidbecomeready)
- [func device(ICDevice, didReceiveStatusInformation: [ICDeviceStatus : Any])](/documentation/imagecapturecore/icdevicedelegate/1507689-device)
- [func device(ICDevice, didEncounterError: (any Error)?)](/documentation/imagecapturecore/icdevicedelegate/1507568-device)
- [func device(ICDevice, didEjectWithError: (any Error)?)](/documentation/imagecapturecore/icdevicedelegate/3142918-device)

##### Responding to Device Changes

- [func deviceDidChangeName(ICDevice)](/documentation/imagecapturecore/icdevicedelegate/1507937-devicedidchangename)
- [func deviceDidChangeSharingState(ICDevice)](/documentation/imagecapturecore/icdevicedelegate/1507794-devicedidchangesharingstate)
- [var hasOpenSession: Bool](/documentation/imagecapturecore/icdevice/1507615-hasopensession)
- [func requestOpenSession()](/documentation/imagecapturecore/icdevice/1507649-requestopensession)
- [func requestOpenSession(options: [ICSessionOptions : Any]?, completion: ((any Error)?) -> Void)](/documentation/imagecapturecore/icdevice/3142916-requestopensession)
- [func requestSendMessage(UInt32, outData: Data, maxReturnedDataSize: UInt32, sendMessageDelegate: Any, didSendMessageSelector: Selector, contextInfo: UnsafeMutableRawPointer?)](/documentation/imagecapturecore/icdevice/1508006-requestsendmessage)
- [func requestCloseSession()](/documentation/imagecapturecore/icdevice/1507882-requestclosesession)
- [func requestCloseSession(options: [ICSessionOptions : Any]?, completion: ((any Error)?) -> Void)](/documentation/imagecapturecore/icdevice/3142913-requestclosesession)
- [func requestEject()](/documentation/imagecapturecore/icdevice/3142914-requesteject)
- [func requestEject(completion: ((any Error)?) -> Void)](/documentation/imagecapturecore/icdevice/3142915-requesteject)

#### Configuring a Device’s Characteristics

- [var userData: NSMutableDictionary?](/documentation/imagecapturecore/icdevice/1507676-userdata)
- [var autolaunchApplicationPath: String?](/documentation/imagecapturecore/icdevice/1507829-autolaunchapplicationpath)
- [var isRemote: Bool](/documentation/imagecapturecore/icdevice/1508075-isremote)

#### Deprecated Symbols

- [func requestEjectOrDisconnect()](/documentation/imagecapturecore/icdevice/1507862-requestejectordisconnect)
- [func requestYield()](/documentation/imagecapturecore/icdevice/1507720-requestyield)
- [var moduleExecutableArchitecture: Int32](/documentation/imagecapturecore/icdevice/1507795-moduleexecutablearchitecture)

#### Instance Properties

- [var systemSymbolName: String?](/documentation/imagecapturecore/icdevice/3571394-systemsymbolname)
- [var browsedDeviceTypeMask: ICDeviceTypeMask](/documentation/imagecapturecore/icdevicebrowser/1507613-browseddevicetypemask)
- [func start()](/documentation/imagecapturecore/icdevicebrowser/1508087-start)
- [func stop()](/documentation/imagecapturecore/icdevicebrowser/1508085-stop)

### Setting a Preferred Device

- [var preferredDevice: ICDevice?](/documentation/imagecapturecore/icdevicebrowser/1507781-preferreddevice)

### Instance Properties

- [var contentsAuthorizationStatus: ICAuthorizationStatus](/documentation/imagecapturecore/icdevicebrowser/3650391-contentsauthorizationstatus)
- [var controlAuthorizationStatus: ICAuthorizationStatus](/documentation/imagecapturecore/icdevicebrowser/3650392-controlauthorizationstatus)
- [var isSuspended: Bool](/documentation/imagecapturecore/icdevicebrowser/3650395-issuspended)

### Instance Methods

- [func requestContentsAuthorization(completion: (ICAuthorizationStatus) -> Void)](/documentation/imagecapturecore/icdevicebrowser/3650393-requestcontentsauthorization)
- [func requestControlAuthorization(completion: (ICAuthorizationStatus) -> Void)](/documentation/imagecapturecore/icdevicebrowser/3650394-requestcontrolauthorization)
- [func resetContentsAuthorization(completion: (ICAuthorizationStatus) -> Void)](/documentation/imagecapturecore/icdevicebrowser/3778550-resetcontentsauthorization)
- [func resetControlAuthorization(completion: (ICAuthorizationStatus) -> Void)](/documentation/imagecapturecore/icdevicebrowser/3778551-resetcontrolauthorization)
- [com.apple.security.personal-information.photos-library](/documentation/bundleresources/entitlements/com.apple.security.personal-information.photos-library)
- [NSCameraUsageDescription](/documentation/bundleresources/information-property-list/nscamerausagedescription)

## Cameras

- [ICCameraDevice](/documentation/imagecapturecore/iccameradevice)

### Reading Files

- [var contents: [ICCameraItem]?](/documentation/imagecapturecore/iccameradevice/1508088-contents)
- [var mediaFiles: [ICCameraItem]?](/documentation/imagecapturecore/iccameradevice/1507811-mediafiles)
- [var contentCatalogPercentCompleted: Int](/documentation/imagecapturecore/iccameradevice/1507899-contentcatalogpercentcompleted)
- [func files(ofType: String) -> [String]?](/documentation/imagecapturecore/iccameradevice/1508121-files)
- [func requestReadData(from: ICCameraFile, atOffset: off_t, length: off_t, readDelegate: Any, didReadDataSelector: Selector, contextInfo: UnsafeMutableRawPointer?)](/documentation/imagecapturecore/iccameradevice/1508079-requestreaddata)

### Uploading Files

- [ICUploadOption](/documentation/imagecapturecore/icuploadoption)

#### Initializers

- [init(rawValue: String)](/documentation/imagecapturecore/icuploadoption/3143809-init)
- [func requestUploadFile(URL, options: [ICUploadOption : Any], uploadDelegate: Any, didUploadSelector: Selector, contextInfo: UnsafeMutableRawPointer?)](/documentation/imagecapturecore/iccameradevice/1508047-requestuploadfile)

### Downloading Files

- [ICDownloadOption](/documentation/imagecapturecore/icdownloadoption)

#### Download Options

- [static let downloadsDirectoryURL: ICDownloadOption](/documentation/imagecapturecore/icdownloadoption/1507924-downloadsdirectoryurl)
- [static let saveAsFilename: ICDownloadOption](/documentation/imagecapturecore/icdownloadoption/1507966-saveasfilename)
- [static let savedFilename: ICDownloadOption](/documentation/imagecapturecore/icdownloadoption/1507651-savedfilename)
- [static let savedAncillaryFiles: ICDownloadOption](/documentation/imagecapturecore/icdownloadoption/1507987-savedancillaryfiles)
- [static let overwrite: ICDownloadOption](/documentation/imagecapturecore/icdownloadoption/1507789-overwrite)
- [static let deleteAfterSuccessfulDownload: ICDownloadOption](/documentation/imagecapturecore/icdownloadoption/1508081-deleteaftersuccessfuldownload)
- [static let sidecarFiles: ICDownloadOption](/documentation/imagecapturecore/icdownloadoption/1507858-sidecarfiles)

#### Initializers

- [init(rawValue: String)](/documentation/imagecapturecore/icdownloadoption/3143741-init)

#### Type Properties

- [static let truncateAfterSuccessfulDownload: ICDownloadOption](/documentation/imagecapturecore/icdownloadoption/3601140-truncateaftersuccessfuldownload)
- [func cancelDownload()](/documentation/imagecapturecore/iccameradevice/1507628-canceldownload)
- [func requestDownloadFile(ICCameraFile, options: [ICDownloadOption : Any], downloadDelegate: any ICCameraDeviceDownloadDelegate, didDownloadSelector: Selector, contextInfo: UnsafeMutableRawPointer?)](/documentation/imagecapturecore/iccameradevice/1507818-requestdownloadfile)
- [ICCameraDeviceDownloadDelegate](/documentation/imagecapturecore/iccameradevicedownloaddelegate)

#### Responding to Download Status

- [func didDownloadFile(ICCameraFile, error: (any Error)?, options: [String : Any], contextInfo: UnsafeMutableRawPointer?)](/documentation/imagecapturecore/iccameradevicedownloaddelegate/1507902-diddownloadfile)
- [func didReceiveDownloadProgress(for: ICCameraFile, downloadedBytes: off_t, maxBytes: off_t)](/documentation/imagecapturecore/iccameradevicedownloaddelegate/1507666-didreceivedownloadprogress)

### Deleting Files

- [var isLocked: Bool](/documentation/imagecapturecore/iccameradevice/3142892-islocked)
- [ICDeleteResult](/documentation/imagecapturecore/icdeleteresult)

#### Creating a Deletion Result

- [init(rawValue: String)](/documentation/imagecapturecore/icdeleteresult/3143724-init)

#### Reading a Deletion Result

- [static let canceled: ICDeleteResult](/documentation/imagecapturecore/icdeleteresult/3152422-canceled)
- [static let failed: ICDeleteResult](/documentation/imagecapturecore/icdeleteresult/3142902-failed)
- [static let successful: ICDeleteResult](/documentation/imagecapturecore/icdeleteresult/3142904-successful)
- [ICDeleteError](/documentation/imagecapturecore/icdeleteerror)

#### Creating a Deletion Error

- [init(rawValue: String)](/documentation/imagecapturecore/icdeleteerror/3143723-init)

#### Reading a Deletion Error

- [static let canceled: ICDeleteError](/documentation/imagecapturecore/icdeleteerror/3152423-canceled)
- [static let deviceMissing: ICDeleteError](/documentation/imagecapturecore/icdeleteerror/3142899-devicemissing)
- [static let fileMissing: ICDeleteError](/documentation/imagecapturecore/icdeleteerror/3142900-filemissing)
- [static let readOnly: ICDeleteError](/documentation/imagecapturecore/icdeleteerror/3142901-readonly)
- [func requestDeleteFiles([ICCameraItem])](/documentation/imagecapturecore/iccameradevice/1507921-requestdeletefiles)
- [func requestDeleteFiles([ICCameraItem], deleteFailed: ([ICDeleteError : ICCameraItem]) -> Void, completion: ([ICDeleteResult : [ICCameraItem]], (any Error)?) -> Void) -> Progress?](/documentation/imagecapturecore/iccameradevice/3142893-requestdeletefiles)
- [func cancelDelete()](/documentation/imagecapturecore/iccameradevice/1507931-canceldelete)

### Taking Pictures

- [var tetheredCaptureEnabled: Bool](/documentation/imagecapturecore/iccameradevice/1508004-tetheredcaptureenabled)
- [var ptpEventHandler: (Data) -> Void](/documentation/imagecapturecore/iccameradevice/3393297-ptpeventhandler)
- [func requestEnableTethering()](/documentation/imagecapturecore/iccameradevice/1508172-requestenabletethering)
- [func requestTakePicture()](/documentation/imagecapturecore/iccameradevice/1507903-requesttakepicture)
- [func requestSendPTPCommand(Data, outData: Data?, sendCommandDelegate: Any, didSendCommand: Selector, contextInfo: UnsafeMutableRawPointer?)](/documentation/imagecapturecore/iccameradevice/1507967-requestsendptpcommand)
- [func requestSendPTPCommand(Data, outData: Data?, completion: (Data, Data, (any Error)?) -> Void)](/documentation/imagecapturecore/iccameradevice/3393298-requestsendptpcommand)
- [func requestDisableTethering()](/documentation/imagecapturecore/iccameradevice/1507577-requestdisabletethering)

### Inspecting the Battery Charge Level

- [var batteryLevelAvailable: Bool](/documentation/imagecapturecore/iccameradevice/1508053-batterylevelavailable)
- [var batteryLevel: Int](/documentation/imagecapturecore/iccameradevice/1508043-batterylevel)

### Synchronizing the Clock

- [var timeOffset: TimeInterval](/documentation/imagecapturecore/iccameradevice/1507878-timeoffset)
- [func requestSyncClock()](/documentation/imagecapturecore/iccameradevice/1508062-requestsyncclock)

### Detecting Apple Devices

- [var isAccessRestrictedAppleDevice: Bool](/documentation/imagecapturecore/iccameradevice/1507742-isaccessrestrictedappledevice)
- [var iCloudPhotosEnabled: Bool](/documentation/imagecapturecore/iccameradevice/3142891-icloudphotosenabled)

### Detecting Mass Storage Devices

- [var mountPoint: String?](/documentation/imagecapturecore/iccameradevice/1507897-mountpoint)

### Removing a Device

- [var isEjectable: Bool](/documentation/imagecapturecore/iccameradevice/3142890-isejectable)

### Instance Properties

- [var mediaPresentation: ICMediaPresentation](/documentation/imagecapturecore/iccameradevice/3601135-mediapresentation)
- [ICCameraDeviceDelegate](/documentation/imagecapturecore/iccameradevicedelegate)

### Determining Device Readiness

- [func deviceDidBecomeReady(withCompleteContentCatalog: ICCameraDevice)](/documentation/imagecapturecore/iccameradevicedelegate/1508008-devicedidbecomeready)

### Adding Objects

- [func cameraDevice(ICCameraDevice, didAdd: [ICCameraItem])](/documentation/imagecapturecore/iccameradevicedelegate/1507996-cameradevice)
- [func cameraDevice(ICCameraDevice, didAdd: ICCameraItem)](/documentation/imagecapturecore/iccameradevicedelegate/1507819-cameradevice)

### Removing Objects

- [func cameraDevice(ICCameraDevice, didRemove: [ICCameraItem])](/documentation/imagecapturecore/iccameradevicedelegate/1508058-cameradevice)
- [func cameraDevice(ICCameraDevice, didCompleteDeleteFilesWithError: (any Error)?)](/documentation/imagecapturecore/iccameradevicedelegate/1507977-cameradevice)
- [func cameraDevice(ICCameraDevice, didRemove: ICCameraItem)](/documentation/imagecapturecore/iccameradevicedelegate/1507735-cameradevice)

### Renaming Objects

- [func cameraDevice(ICCameraDevice, didRenameItems: [ICCameraItem])](/documentation/imagecapturecore/iccameradevicedelegate/1507699-cameradevice)

### Receiving Metadata

- [func cameraDevice(ICCameraDevice, didReceiveMetadata: [AnyHashable : Any]?, for: ICCameraItem, error: (any Error)?)](/documentation/imagecapturecore/iccameradevicedelegate/3142894-cameradevice)
- [func cameraDevice(ICCameraDevice, shouldGetMetadataOf: ICCameraItem) -> Bool](/documentation/imagecapturecore/iccameradevicedelegate/1507926-cameradevice)
- [func cameraDevice(ICCameraDevice, didReceiveMetadataFor: ICCameraItem)](/documentation/imagecapturecore/iccameradevicedelegate/1507675-cameradevice)

### Receiving Thumbnails

- [func cameraDevice(ICCameraDevice, didReceiveThumbnail: CGImage?, for: ICCameraItem, error: (any Error)?)](/documentation/imagecapturecore/iccameradevicedelegate/3142895-cameradevice)
- [func cameraDevice(ICCameraDevice, didReceiveThumbnailFor: ICCameraItem)](/documentation/imagecapturecore/iccameradevicedelegate/1507941-cameradevice)
- [func cameraDevice(ICCameraDevice, shouldGetThumbnailOf: ICCameraItem) -> Bool](/documentation/imagecapturecore/iccameradevicedelegate/1507885-cameradevice)

### Responding to Capability Changes

- [func cameraDeviceDidChangeCapability(ICCameraDevice)](/documentation/imagecapturecore/iccameradevicedelegate/1507871-cameradevicedidchangecapability)

### Responding to Access Restrictions

- [func cameraDeviceDidEnableAccessRestriction(ICDevice)](/documentation/imagecapturecore/iccameradevicedelegate/3142896-cameradevicedidenableaccessrestr)
- [func cameraDeviceDidRemoveAccessRestriction(ICDevice)](/documentation/imagecapturecore/iccameradevicedelegate/3142897-cameradevicedidremoveaccessrestr)

### Responding to PTP Events

- [func cameraDevice(ICCameraDevice, didReceivePTPEvent: Data)](/documentation/imagecapturecore/iccameradevicedelegate/1507957-cameradevice)
- [ICCameraItem](/documentation/imagecapturecore/iccameraitem)

### Inspecting an Item’s Name and Type

- [var uti: String?](/documentation/imagecapturecore/iccameraitem/1388977-uti)
- [var name: String?](/documentation/imagecapturecore/iccameraitem/1389011-name)
- [var ptpObjectHandle: UInt32](/documentation/imagecapturecore/iccameraitem/1388997-ptpobjecthandle)
- [var isRaw: Bool](/documentation/imagecapturecore/iccameraitem/1389021-israw)

### Determining an Item’s Change Dates

- [var creationDate: Date?](/documentation/imagecapturecore/iccameraitem/1388989-creationdate)
- [var modificationDate: Date?](/documentation/imagecapturecore/iccameraitem/1388979-modificationdate)
- [var wasAddedAfterContentCatalogCompleted: Bool](/documentation/imagecapturecore/iccameraitem/1389015-wasaddedaftercontentcatalogcompl)

### Locating an Item

- [var device: ICCameraDevice?](/documentation/imagecapturecore/iccameraitem/1389019-device)
- [var fileSystemPath: String?](/documentation/imagecapturecore/iccameraitem/1388999-filesystempath)
- [var parentFolder: ICCameraFolder?](/documentation/imagecapturecore/iccameraitem/1388978-parentfolder)
- [var isInTemporaryStore: Bool](/documentation/imagecapturecore/iccameraitem/1388987-isintemporarystore)

### Requesting Metadata

- [func requestMetadata()](/documentation/imagecapturecore/iccameraitem/3131480-requestmetadata)
- [var metadata: [AnyHashable : Any]?](/documentation/imagecapturecore/iccameraitem/3131479-metadata)
- [var metadataIfAvailable: [String : Any]?](/documentation/imagecapturecore/iccameraitem/1388985-metadataifavailable)
- [func flushMetadataCache()](/documentation/imagecapturecore/iccameraitem/3131477-flushmetadatacache)
- [ICCameraItemMetadataOption](/documentation/imagecapturecore/iccameraitemmetadataoption)

#### Initializers

- [init(rawValue: String)](/documentation/imagecapturecore/iccameraitemmetadataoption/3143721-init)

### Requesting Thumbnails

- [func requestThumbnail()](/documentation/imagecapturecore/iccameraitem/3131481-requestthumbnail)
- [var thumbnail: CGImage?](/documentation/imagecapturecore/iccameraitem/3131482-thumbnail)
- [var thumbnailIfAvailable: CGImage?](/documentation/imagecapturecore/iccameraitem/1389001-thumbnailifavailable)
- [var largeThumbnailIfAvailable: CGImage?](/documentation/imagecapturecore/iccameraitem/1388995-largethumbnailifavailable)
- [func flushThumbnailCache()](/documentation/imagecapturecore/iccameraitem/3131478-flushthumbnailcache)
- [ICCameraItemThumbnailOption](/documentation/imagecapturecore/iccameraitemthumbnailoption)

#### Initializers

- [init(rawValue: String)](/documentation/imagecapturecore/iccameraitemthumbnailoption/3143722-init)

#### Type Properties

- [static let imageSourceShouldCache: ICCameraItemThumbnailOption](/documentation/imagecapturecore/iccameraitemthumbnailoption/3142910-imagesourceshouldcache)
- [static let imageSourceThumbnailMaxPixelSize: ICCameraItemThumbnailOption](/documentation/imagecapturecore/iccameraitemthumbnailoption/3142911-imagesourcethumbnailmaxpixelsize)

### Accessing a Protected Item

- [var isLocked: Bool](/documentation/imagecapturecore/iccameraitem/1389017-islocked)

### Storing Information

- [var userData: NSMutableDictionary?](/documentation/imagecapturecore/iccameraitem/1389009-userdata)
- [ICCameraFile](/documentation/imagecapturecore/iccamerafile)

### Requesting Metadata

- [func requestMetadataDictionary(options: [ICCameraItemMetadataOption : Any]?, completion: ([AnyHashable : Any]?, (any Error)?) -> Void)](/documentation/imagecapturecore/iccamerafile/3131468-requestmetadatadictionary)

### Requesting Thumbnails

- [func requestThumbnailData(options: [ICCameraItemThumbnailOption : Any]?, completion: (Data?, (any Error)?) -> Void)](/documentation/imagecapturecore/iccamerafile/3131471-requestthumbnaildata)

### Requesting Downloads

- [func requestDownload(options: [ICDownloadOption : Any]?, completion: (String?, (any Error)?) -> Void) -> Progress?](/documentation/imagecapturecore/iccamerafile/3142906-requestdownload)

### Requesting Data

- [func requestReadData(atOffset: off_t, length: off_t, completion: (Data?, (any Error)?) -> Void)](/documentation/imagecapturecore/iccamerafile/3131470-requestreaddata)

### Inspecting a File’s Name

- [var originalFilename: String?](/documentation/imagecapturecore/iccamerafile/3131463-originalfilename)
- [var createdFilename: String?](/documentation/imagecapturecore/iccamerafile/3131453-createdfilename)

### Inspecting a File's Identity

- [var groupUUID: String?](/documentation/imagecapturecore/iccamerafile/3131460-groupuuid)
- [var relatedUUID: String?](/documentation/imagecapturecore/iccamerafile/3131466-relateduuid)
- [var originatingAssetID: String?](/documentation/imagecapturecore/iccamerafile/3131464-originatingassetid)

### Determining When a File Was Created or Modified

- [var fileCreationDate: Date?](/documentation/imagecapturecore/iccamerafile/3131456-filecreationdate)
- [var fileModificationDate: Date?](/documentation/imagecapturecore/iccamerafile/3131457-filemodificationdate)

### Inspecting a File’s Size

- [var fileSize: off_t](/documentation/imagecapturecore/iccamerafile/1389013-filesize)

### Inspecting a File’s Dimensions

- [var width: Int](/documentation/imagecapturecore/iccamerafile/3131474-width)
- [var height: Int](/documentation/imagecapturecore/iccamerafile/3131461-height)

### Inspecting a File’s EXIF Data

- [var orientation: ICEXIFOrientationType](/documentation/imagecapturecore/iccamerafile/1388983-orientation)
- [ICEXIFOrientationType](/documentation/imagecapturecore/icexiforientationtype)

#### Enumeration Cases

- [case orientation1](/documentation/imagecapturecore/icexiforientationtype/orientation1)
- [case orientation2](/documentation/imagecapturecore/icexiforientationtype/orientation2)
- [case orientation3](/documentation/imagecapturecore/icexiforientationtype/orientation3)
- [case orientation4](/documentation/imagecapturecore/icexiforientationtype/orientation4)
- [case orientation5](/documentation/imagecapturecore/icexiforientationtype/orientation5)
- [case orientation6](/documentation/imagecapturecore/icexiforientationtype/orientation6)
- [case orientation7](/documentation/imagecapturecore/icexiforientationtype/orientation7)
- [case orientation8](/documentation/imagecapturecore/icexiforientationtype/orientation8)
- [var exifCreationDate: Date?](/documentation/imagecapturecore/iccamerafile/3131454-exifcreationdate)
- [var exifModificationDate: Date?](/documentation/imagecapturecore/iccamerafile/3131455-exifmodificationdate)

### Identifying a File’s Location

- [var gpsString: String?](/documentation/imagecapturecore/iccamerafile/3131459-gpsstring)

### Inspecting a File in a Burst

- [var firstPicked: Bool](/documentation/imagecapturecore/iccamerafile/3131458-firstpicked)
- [var burstUUID: String?](/documentation/imagecapturecore/iccamerafile/3131452-burstuuid)
- [var burstFavorite: Bool](/documentation/imagecapturecore/iccamerafile/3131450-burstfavorite)
- [var burstPicked: Bool](/documentation/imagecapturecore/iccamerafile/3131451-burstpicked)

### Inspecting Video Properties

- [var duration: Double](/documentation/imagecapturecore/iccamerafile/1388981-duration)
- [var highFramerate: Bool](/documentation/imagecapturecore/iccamerafile/3131462-highframerate)
- [var timeLapse: Bool](/documentation/imagecapturecore/iccamerafile/3131473-timelapse)

### Identifying Related Files

- [var sidecarFiles: [ICCameraItem]?](/documentation/imagecapturecore/iccamerafile/1389003-sidecarfiles)
- [var pairedRawImage: ICCameraFile?](/documentation/imagecapturecore/iccamerafile/3131465-pairedrawimage)

### Instance Properties

- [var fingerprint: String?](/documentation/imagecapturecore/iccamerafile/4359697-fingerprint)

### Instance Methods

- [func requestFingerprint(completion: (String?, (any Error)?) -> Void)](/documentation/imagecapturecore/iccamerafile/4359699-requestfingerprint)
- [func requestSecurityScopedURL(completion: (URL?, (any Error)?) -> Void)](/documentation/imagecapturecore/iccamerafile/4149740-requestsecurityscopedurl)

### Type Methods

- [class func fingerprintForFile(at: URL) -> String?](/documentation/imagecapturecore/iccamerafile/4359698-fingerprintforfile)
- [ICCameraFolder](/documentation/imagecapturecore/iccamerafolder)

### Inspecting a Folder’s Contents

- [var contents: [ICCameraItem]?](/documentation/imagecapturecore/iccamerafolder/1389005-contents)

## Scanners

- [ICScannerDevice](/documentation/imagecapturecore/icscannerdevice)

### Selecting a Functional Unit

- [var availableFunctionalUnitTypes: [NSNumber]](/documentation/imagecapturecore/icscannerdevice/1507679-availablefunctionalunittypes)
- [var selectedFunctionalUnit: ICScannerFunctionalUnit](/documentation/imagecapturecore/icscannerdevice/1508000-selectedfunctionalunit)
- [func requestSelect(ICScannerFunctionalUnitType)](/documentation/imagecapturecore/icscannerdevice/1507654-requestselect)
- [ICScannerFunctionalUnitType](/documentation/imagecapturecore/icscannerfunctionalunittype)

#### Enumeration Cases

- [case documentFeeder](/documentation/imagecapturecore/icscannerfunctionalunittype/documentfeeder)
- [case flatbed](/documentation/imagecapturecore/icscannerfunctionalunittype/flatbed)
- [case negativeTransparency](/documentation/imagecapturecore/icscannerfunctionalunittype/negativetransparency)
- [case positiveTransparency](/documentation/imagecapturecore/icscannerfunctionalunittype/positivetransparency)
- [ICScannerFunctionalUnitState](/documentation/imagecapturecore/icscannerfunctionalunitstate)

#### Enumeration Cases

- [case ready](/documentation/imagecapturecore/icscannerfunctionalunitstate/ready)
- [case overviewScanInProgress](/documentation/imagecapturecore/icscannerfunctionalunitstate/overviewscaninprogress)
- [case scanInProgress](/documentation/imagecapturecore/icscannerfunctionalunitstate/scaninprogress)

### Performing a Scan

- [func requestOpenSession(withCredentials: String, password: String)](/documentation/imagecapturecore/icscannerdevice/2881931-requestopensession)
- [func requestOverviewScan()](/documentation/imagecapturecore/icscannerdevice/1507646-requestoverviewscan)
- [func requestScan()](/documentation/imagecapturecore/icscannerdevice/1508117-requestscan)
- [func cancelScan()](/documentation/imagecapturecore/icscannerdevice/1507771-cancelscan)
- [var documentName: String](/documentation/imagecapturecore/icscannerdevice/1507879-documentname)
- [var documentUTI: String](/documentation/imagecapturecore/icscannerdevice/1507955-documentuti)
- [var downloadsDirectory: URL](/documentation/imagecapturecore/icscannerdevice/1508025-downloadsdirectory)
- [var transferMode: ICScannerTransferMode](/documentation/imagecapturecore/icscannerdevice/1507698-transfermode)
- [var maxMemoryBandSize: UInt32](/documentation/imagecapturecore/icscannerdevice/1508156-maxmemorybandsize)

### Logging into a Protected Device

- [var defaultUsername: String](/documentation/imagecapturecore/icscannerdevice/2881932-defaultusername)
- [ICScannerDeviceDelegate](/documentation/imagecapturecore/icscannerdevicedelegate)

### Determining Scanner Availability

- [func scannerDeviceDidBecomeAvailable(ICScannerDevice)](/documentation/imagecapturecore/icscannerdevicedelegate/1507590-scannerdevicedidbecomeavailable)

### Selecting a Functional Unit

- [func scannerDevice(ICScannerDevice, didSelect: ICScannerFunctionalUnit, error: (any Error)?)](/documentation/imagecapturecore/icscannerdevicedelegate/1507589-scannerdevice)

### Performing a Scan

- [func scannerDevice(ICScannerDevice, didCompleteOverviewScanWithError: (any Error)?)](/documentation/imagecapturecore/icscannerdevicedelegate/1507631-scannerdevice)
- [func scannerDevice(ICScannerDevice, didCompleteScanWithError: (any Error)?)](/documentation/imagecapturecore/icscannerdevicedelegate/1507932-scannerdevice)
- [func scannerDevice(ICScannerDevice, didScanTo: ICScannerBandData)](/documentation/imagecapturecore/icscannerdevicedelegate/1507845-scannerdevice)
- [func scannerDevice(ICScannerDevice, didScanTo: URL)](/documentation/imagecapturecore/icscannerdevicedelegate/1507655-scannerdevice)
- [Scanner Configuration](/documentation/imagecapturecore/scanner_configuration)

### Band Data

- [ICScannerBandData](/documentation/imagecapturecore/icscannerbanddata)

#### Instance Properties

- [var bitsPerComponent: Int](/documentation/imagecapturecore/icscannerbanddata/1507671-bitspercomponent)
- [var bitsPerPixel: Int](/documentation/imagecapturecore/icscannerbanddata/1507886-bitsperpixel)
- [var bytesPerRow: Int](/documentation/imagecapturecore/icscannerbanddata/1507751-bytesperrow)
- [var colorSyncProfilePath: String?](/documentation/imagecapturecore/icscannerbanddata/1507730-colorsyncprofilepath)
- [var dataBuffer: Data?](/documentation/imagecapturecore/icscannerbanddata/1507888-databuffer)
- [var dataNumRows: Int](/documentation/imagecapturecore/icscannerbanddata/1507714-datanumrows)
- [var dataSize: Int](/documentation/imagecapturecore/icscannerbanddata/1507877-datasize)
- [var dataStartRow: Int](/documentation/imagecapturecore/icscannerbanddata/1508005-datastartrow)
- [var fullImageHeight: Int](/documentation/imagecapturecore/icscannerbanddata/1507667-fullimageheight)
- [var fullImageWidth: Int](/documentation/imagecapturecore/icscannerbanddata/1507632-fullimagewidth)
- [var isBigEndian: Bool](/documentation/imagecapturecore/icscannerbanddata/1507710-isbigendian)
- [var numComponents: Int](/documentation/imagecapturecore/icscannerbanddata/1507728-numcomponents)
- [var pixelDataType: ICScannerPixelDataType](/documentation/imagecapturecore/icscannerbanddata/1507776-pixeldatatype)

### Bit Depth

- [ICScannerBitDepth](/documentation/imagecapturecore/icscannerbitdepth)

#### Enumeration Cases

- [case depth16Bits](/documentation/imagecapturecore/icscannerbitdepth/depth16bits)
- [case depth1Bit](/documentation/imagecapturecore/icscannerbitdepth/depth1bit)
- [case depth8Bits](/documentation/imagecapturecore/icscannerbitdepth/depth8bits)

### Color Formats

- [ICScannerColorDataFormatType](/documentation/imagecapturecore/icscannercolordataformattype)

#### Enumeration Cases

- [case chunky](/documentation/imagecapturecore/icscannercolordataformattype/chunky)
- [case planar](/documentation/imagecapturecore/icscannercolordataformattype/planar)

### Document Sizes

- [ICScannerDocumentType](/documentation/imagecapturecore/icscannerdocumenttype)

#### Enumeration Cases

- [case type10](/documentation/imagecapturecore/icscannerdocumenttype/type10)
- [case type10R](/documentation/imagecapturecore/icscannerdocumenttype/type10r)
- [case type110](/documentation/imagecapturecore/icscannerdocumenttype/type110)
- [case type11R](/documentation/imagecapturecore/icscannerdocumenttype/type11r)
- [case type12R](/documentation/imagecapturecore/icscannerdocumenttype/type12r)
- [case type135](/documentation/imagecapturecore/icscannerdocumenttype/type135)
- [case type2A0](/documentation/imagecapturecore/icscannerdocumenttype/type2a0)
- [case type3R](/documentation/imagecapturecore/icscannerdocumenttype/type3r)
- [case type4A0](/documentation/imagecapturecore/icscannerdocumenttype/type4a0)
- [case type4R](/documentation/imagecapturecore/icscannerdocumenttype/type4r)
- [case type5R](/documentation/imagecapturecore/icscannerdocumenttype/type5r)
- [case type6R](/documentation/imagecapturecore/icscannerdocumenttype/type6r)
- [case type8R](/documentation/imagecapturecore/icscannerdocumenttype/type8r)
- [case typeA0](/documentation/imagecapturecore/icscannerdocumenttype/typea0)
- [case typeA1](/documentation/imagecapturecore/icscannerdocumenttype/typea1)
- [case typeA2](/documentation/imagecapturecore/icscannerdocumenttype/typea2)
- [case typeA3](/documentation/imagecapturecore/icscannerdocumenttype/typea3)
- [case typeA4](/documentation/imagecapturecore/icscannerdocumenttype/typea4)
- [case typeA5](/documentation/imagecapturecore/icscannerdocumenttype/typea5)
- [case typeA6](/documentation/imagecapturecore/icscannerdocumenttype/typea6)
- [case typeA7](/documentation/imagecapturecore/icscannerdocumenttype/typea7)
- [case typeA8](/documentation/imagecapturecore/icscannerdocumenttype/typea8)
- [case typeA9](/documentation/imagecapturecore/icscannerdocumenttype/typea9)
- [case typeAPSC](/documentation/imagecapturecore/icscannerdocumenttype/typeapsc)
- [case typeAPSH](/documentation/imagecapturecore/icscannerdocumenttype/typeapsh)
- [case typeAPSP](/documentation/imagecapturecore/icscannerdocumenttype/typeapsp)
- [case typeB5](/documentation/imagecapturecore/icscannerdocumenttype/typeb5)
- [case typeBusinessCard](/documentation/imagecapturecore/icscannerdocumenttype/typebusinesscard)
- [case typeC0](/documentation/imagecapturecore/icscannerdocumenttype/typec0)
- [case typeC1](/documentation/imagecapturecore/icscannerdocumenttype/typec1)
- [case typeC10](/documentation/imagecapturecore/icscannerdocumenttype/typec10)
- [case typeC2](/documentation/imagecapturecore/icscannerdocumenttype/typec2)
- [case typeC3](/documentation/imagecapturecore/icscannerdocumenttype/typec3)
- [case typeC4](/documentation/imagecapturecore/icscannerdocumenttype/typec4)
- [case typeC5](/documentation/imagecapturecore/icscannerdocumenttype/typec5)
- [case typeC6](/documentation/imagecapturecore/icscannerdocumenttype/typec6)
- [case typeC7](/documentation/imagecapturecore/icscannerdocumenttype/typec7)
- [case typeC8](/documentation/imagecapturecore/icscannerdocumenttype/typec8)
- [case typeC9](/documentation/imagecapturecore/icscannerdocumenttype/typec9)
- [case typeDefault](/documentation/imagecapturecore/icscannerdocumenttype/typedefault)
- [case typeE](/documentation/imagecapturecore/icscannerdocumenttype/typee)
- [case typeISOB0](/documentation/imagecapturecore/icscannerdocumenttype/typeisob0)
- [case typeISOB1](/documentation/imagecapturecore/icscannerdocumenttype/typeisob1)
- [case typeISOB10](/documentation/imagecapturecore/icscannerdocumenttype/typeisob10)
- [case typeISOB2](/documentation/imagecapturecore/icscannerdocumenttype/typeisob2)
- [case typeISOB3](/documentation/imagecapturecore/icscannerdocumenttype/typeisob3)
- [case typeISOB4](/documentation/imagecapturecore/icscannerdocumenttype/typeisob4)
- [case typeISOB5](/documentation/imagecapturecore/icscannerdocumenttype/typeisob5)
- [case typeISOB6](/documentation/imagecapturecore/icscannerdocumenttype/typeisob6)
- [case typeISOB7](/documentation/imagecapturecore/icscannerdocumenttype/typeisob7)
- [case typeISOB8](/documentation/imagecapturecore/icscannerdocumenttype/typeisob8)
- [case typeISOB9](/documentation/imagecapturecore/icscannerdocumenttype/typeisob9)
- [case typeJISB0](/documentation/imagecapturecore/icscannerdocumenttype/typejisb0)
- [case typeJISB1](/documentation/imagecapturecore/icscannerdocumenttype/typejisb1)
- [case typeJISB10](/documentation/imagecapturecore/icscannerdocumenttype/typejisb10)
- [case typeJISB2](/documentation/imagecapturecore/icscannerdocumenttype/typejisb2)
- [case typeJISB3](/documentation/imagecapturecore/icscannerdocumenttype/typejisb3)
- [case typeJISB4](/documentation/imagecapturecore/icscannerdocumenttype/typejisb4)
- [case typeJISB6](/documentation/imagecapturecore/icscannerdocumenttype/typejisb6)
- [case typeJISB7](/documentation/imagecapturecore/icscannerdocumenttype/typejisb7)
- [case typeJISB8](/documentation/imagecapturecore/icscannerdocumenttype/typejisb8)
- [case typeJISB9](/documentation/imagecapturecore/icscannerdocumenttype/typejisb9)
- [case typeLF](/documentation/imagecapturecore/icscannerdocumenttype/typelf)
- [case typeMF](/documentation/imagecapturecore/icscannerdocumenttype/typemf)
- [case typeS10R](/documentation/imagecapturecore/icscannerdocumenttype/types10r)
- [case typeS12R](/documentation/imagecapturecore/icscannerdocumenttype/types12r)
- [case typeS8R](/documentation/imagecapturecore/icscannerdocumenttype/types8r)
- [case typeUSExecutive](/documentation/imagecapturecore/icscannerdocumenttype/typeusexecutive)
- [case typeUSLedger](/documentation/imagecapturecore/icscannerdocumenttype/typeusledger)
- [case typeUSLegal](/documentation/imagecapturecore/icscannerdocumenttype/typeuslegal)
- [case typeUSLetter](/documentation/imagecapturecore/icscannerdocumenttype/typeusletter)
- [case typeUSStatement](/documentation/imagecapturecore/icscannerdocumenttype/typeusstatement)
- [ICScannerMeasurementUnit](/documentation/imagecapturecore/icscannermeasurementunit)

#### Enumeration Cases

- [case centimeters](/documentation/imagecapturecore/icscannermeasurementunit/centimeters)
- [case inches](/documentation/imagecapturecore/icscannermeasurementunit/inches)
- [case picas](/documentation/imagecapturecore/icscannermeasurementunit/picas)
- [case pixels](/documentation/imagecapturecore/icscannermeasurementunit/pixels)
- [case points](/documentation/imagecapturecore/icscannermeasurementunit/points)
- [case twips](/documentation/imagecapturecore/icscannermeasurementunit/twips)

### Features

- [ICScannerFeature](/documentation/imagecapturecore/icscannerfeature)

#### Instance Properties

- [var humanReadableName: String?](/documentation/imagecapturecore/icscannerfeature/1508051-humanreadablename)
- [var internalName: String?](/documentation/imagecapturecore/icscannerfeature/1508021-internalname)
- [var tooltip: String?](/documentation/imagecapturecore/icscannerfeature/1507600-tooltip)
- [var type: ICScannerFeatureType](/documentation/imagecapturecore/icscannerfeature/1507807-type)
- [ICScannerFeatureBoolean](/documentation/imagecapturecore/icscannerfeatureboolean)

#### Instance Properties

- [var value: Bool](/documentation/imagecapturecore/icscannerfeatureboolean/1507884-value)
- [ICScannerFeatureEnumeration](/documentation/imagecapturecore/icscannerfeatureenumeration)

#### Instance Properties

- [var currentValue: AnyObject](/documentation/imagecapturecore/icscannerfeatureenumeration/1507864-currentvalue)
- [var defaultValue: Any](/documentation/imagecapturecore/icscannerfeatureenumeration/1507821-defaultvalue)
- [var menuItemLabels: [String]](/documentation/imagecapturecore/icscannerfeatureenumeration/1507712-menuitemlabels)
- [var menuItemLabelsTooltips: [String]](/documentation/imagecapturecore/icscannerfeatureenumeration/1507843-menuitemlabelstooltips)
- [var values: [NSNumber]](/documentation/imagecapturecore/icscannerfeatureenumeration/1508144-values)
- [ICScannerFeatureRange](/documentation/imagecapturecore/icscannerfeaturerange)

#### Instance Properties

- [var currentValue: CGFloat](/documentation/imagecapturecore/icscannerfeaturerange/1507778-currentvalue)
- [var defaultValue: CGFloat](/documentation/imagecapturecore/icscannerfeaturerange/1508018-defaultvalue)
- [var maxValue: CGFloat](/documentation/imagecapturecore/icscannerfeaturerange/1507839-maxvalue)
- [var minValue: CGFloat](/documentation/imagecapturecore/icscannerfeaturerange/1507774-minvalue)
- [var stepSize: CGFloat](/documentation/imagecapturecore/icscannerfeaturerange/1507697-stepsize)
- [ICScannerFeatureTemplate](/documentation/imagecapturecore/icscannerfeaturetemplate)

#### Instance Properties

- [var targets: [NSMutableArray]](/documentation/imagecapturecore/icscannerfeaturetemplate/1508048-targets)
- [ICScannerFeatureType](/documentation/imagecapturecore/icscannerfeaturetype)

#### Enumeration Cases

- [case boolean](/documentation/imagecapturecore/icscannerfeaturetype/boolean)
- [case enumeration](/documentation/imagecapturecore/icscannerfeaturetype/enumeration)
- [case range](/documentation/imagecapturecore/icscannerfeaturetype/range)
- [case template](/documentation/imagecapturecore/icscannerfeaturetype/template)

### Functional Units

- [ICScannerFunctionalUnit](/documentation/imagecapturecore/icscannerfunctionalunit)

#### Instance Properties

- [var acceptsThresholdForBlackAndWhiteScanning: Bool](/documentation/imagecapturecore/icscannerfunctionalunit/1507881-acceptsthresholdforblackandwhite)
- [var bitDepth: ICScannerBitDepth](/documentation/imagecapturecore/icscannerfunctionalunit/1507954-bitdepth)
- [var canPerformOverviewScan: Bool](/documentation/imagecapturecore/icscannerfunctionalunit/1507998-canperformoverviewscan)
- [var defaultThresholdForBlackAndWhiteScanning: UInt8](/documentation/imagecapturecore/icscannerfunctionalunit/1507900-defaultthresholdforblackandwhite)
- [var measurementUnit: ICScannerMeasurementUnit](/documentation/imagecapturecore/icscannerfunctionalunit/1507832-measurementunit)
- [var nativeXResolution: Int](/documentation/imagecapturecore/icscannerfunctionalunit/1508170-nativexresolution)
- [var nativeYResolution: Int](/documentation/imagecapturecore/icscannerfunctionalunit/1508168-nativeyresolution)
- [var overviewImage: CGImage?](/documentation/imagecapturecore/icscannerfunctionalunit/1507637-overviewimage)
- [var overviewResolution: Int](/documentation/imagecapturecore/icscannerfunctionalunit/1508054-overviewresolution)
- [var overviewScanInProgress: Bool](/documentation/imagecapturecore/icscannerfunctionalunit/1507709-overviewscaninprogress)
- [var physicalSize: NSSize](/documentation/imagecapturecore/icscannerfunctionalunit/1508033-physicalsize)
- [var pixelDataType: ICScannerPixelDataType](/documentation/imagecapturecore/icscannerfunctionalunit/1507901-pixeldatatype)
- [var preferredResolutions: IndexSet](/documentation/imagecapturecore/icscannerfunctionalunit/1507635-preferredresolutions)
- [var preferredScaleFactors: IndexSet](/documentation/imagecapturecore/icscannerfunctionalunit/1507734-preferredscalefactors)
- [var resolution: Int](/documentation/imagecapturecore/icscannerfunctionalunit/1508082-resolution)
- [var scaleFactor: Int](/documentation/imagecapturecore/icscannerfunctionalunit/1507928-scalefactor)
- [var scanArea: NSRect](/documentation/imagecapturecore/icscannerfunctionalunit/1508107-scanarea)
- [var scanAreaOrientation: ICEXIFOrientationType](/documentation/imagecapturecore/icscannerfunctionalunit/1507849-scanareaorientation)
- [var scanInProgress: Bool](/documentation/imagecapturecore/icscannerfunctionalunit/1507566-scaninprogress)
- [var scanProgressPercentDone: CGFloat](/documentation/imagecapturecore/icscannerfunctionalunit/1507754-scanprogresspercentdone)
- [var state: ICScannerFunctionalUnitState](/documentation/imagecapturecore/icscannerfunctionalunit/1507853-state)
- [var supportedBitDepths: IndexSet](/documentation/imagecapturecore/icscannerfunctionalunit/1507910-supportedbitdepths)
- [var supportedMeasurementUnits: IndexSet](/documentation/imagecapturecore/icscannerfunctionalunit/1507833-supportedmeasurementunits)
- [var supportedResolutions: IndexSet](/documentation/imagecapturecore/icscannerfunctionalunit/1507913-supportedresolutions)
- [var supportedScaleFactors: IndexSet](/documentation/imagecapturecore/icscannerfunctionalunit/1507919-supportedscalefactors)
- [var templates: [ICScannerFeatureTemplate]](/documentation/imagecapturecore/icscannerfunctionalunit/1508141-templates)
- [var thresholdForBlackAndWhiteScanning: UInt8](/documentation/imagecapturecore/icscannerfunctionalunit/1507975-thresholdforblackandwhitescannin)
- [var type: ICScannerFunctionalUnitType](/documentation/imagecapturecore/icscannerfunctionalunit/1508014-type)
- [var usesThresholdForBlackAndWhiteScanning: Bool](/documentation/imagecapturecore/icscannerfunctionalunit/1508028-usesthresholdforblackandwhitesca)
- [var vendorFeatures: [ICScannerFeature]?](/documentation/imagecapturecore/icscannerfunctionalunit/1507905-vendorfeatures)
- [ICScannerFunctionalUnitDocumentFeeder](/documentation/imagecapturecore/icscannerfunctionalunitdocumentfeeder)

#### Instance Properties

- [var documentLoaded: Bool](/documentation/imagecapturecore/icscannerfunctionalunitdocumentfeeder/1507825-documentloaded)
- [var documentSize: NSSize](/documentation/imagecapturecore/icscannerfunctionalunitdocumentfeeder/1508074-documentsize)
- [var documentType: ICScannerDocumentType](/documentation/imagecapturecore/icscannerfunctionalunitdocumentfeeder/1507783-documenttype)
- [var duplexScanningEnabled: Bool](/documentation/imagecapturecore/icscannerfunctionalunitdocumentfeeder/1507592-duplexscanningenabled)
- [var evenPageOrientation: ICEXIFOrientationType](/documentation/imagecapturecore/icscannerfunctionalunitdocumentfeeder/1508090-evenpageorientation)
- [var oddPageOrientation: ICEXIFOrientationType](/documentation/imagecapturecore/icscannerfunctionalunitdocumentfeeder/1507739-oddpageorientation)
- [var reverseFeederPageOrder: Bool](/documentation/imagecapturecore/icscannerfunctionalunitdocumentfeeder/1507908-reversefeederpageorder)
- [var supportedDocumentTypes: IndexSet](/documentation/imagecapturecore/icscannerfunctionalunitdocumentfeeder/1507584-supporteddocumenttypes)
- [var supportsDuplexScanning: Bool](/documentation/imagecapturecore/icscannerfunctionalunitdocumentfeeder/1507588-supportsduplexscanning)
- [ICScannerFunctionalUnitFlatbed](/documentation/imagecapturecore/icscannerfunctionalunitflatbed)

#### Instance Properties

- [var documentSize: NSSize](/documentation/imagecapturecore/icscannerfunctionalunitflatbed/1507971-documentsize)
- [var documentType: ICScannerDocumentType](/documentation/imagecapturecore/icscannerfunctionalunitflatbed/1507793-documenttype)
- [var supportedDocumentTypes: IndexSet](/documentation/imagecapturecore/icscannerfunctionalunitflatbed/1508067-supporteddocumenttypes)
- [ICScannerFunctionalUnitNegativeTransparency](/documentation/imagecapturecore/icscannerfunctionalunitnegativetransparency)

#### Instance Properties

- [var documentSize: NSSize](/documentation/imagecapturecore/icscannerfunctionalunitnegativetransparency/1507816-documentsize)
- [var documentType: ICScannerDocumentType](/documentation/imagecapturecore/icscannerfunctionalunitnegativetransparency/1508012-documenttype)
- [var supportedDocumentTypes: IndexSet](/documentation/imagecapturecore/icscannerfunctionalunitnegativetransparency/1507868-supporteddocumenttypes)
- [ICScannerFunctionalUnitPositiveTransparency](/documentation/imagecapturecore/icscannerfunctionalunitpositivetransparency)

#### Instance Properties

- [var documentSize: NSSize](/documentation/imagecapturecore/icscannerfunctionalunitpositivetransparency/1507652-documentsize)
- [var documentType: ICScannerDocumentType](/documentation/imagecapturecore/icscannerfunctionalunitpositivetransparency/1507591-documenttype)
- [var supportedDocumentTypes: IndexSet](/documentation/imagecapturecore/icscannerfunctionalunitpositivetransparency/1508152-supporteddocumenttypes)
- [ICScannerTransferMode](/documentation/imagecapturecore/icscannertransfermode)

#### Enumeration Cases

- [case fileBased](/documentation/imagecapturecore/icscannertransfermode/filebased)
- [case memoryBased](/documentation/imagecapturecore/icscannertransfermode/memorybased)

### Pixel Data Types

- [ICScannerPixelDataType](/documentation/imagecapturecore/icscannerpixeldatatype)

#### Enumeration Cases

- [case BW](/documentation/imagecapturecore/icscannerpixeldatatype/bw)
- [case CIEXYZ](/documentation/imagecapturecore/icscannerpixeldatatype/ciexyz)
- [case CMY](/documentation/imagecapturecore/icscannerpixeldatatype/cmy)
- [case CMYK](/documentation/imagecapturecore/icscannerpixeldatatype/cmyk)
- [case gray](/documentation/imagecapturecore/icscannerpixeldatatype/gray)
- [case palette](/documentation/imagecapturecore/icscannerpixeldatatype/palette)
- [case RGB](/documentation/imagecapturecore/icscannerpixeldatatype/rgb)
- [case YUV](/documentation/imagecapturecore/icscannerpixeldatatype/yuv)
- [case YUVK](/documentation/imagecapturecore/icscannerpixeldatatype/yuvk)

### Scanner States

- [let ICScannerStatusRequestsOverviewScan: String](/documentation/imagecapturecore/icscannerstatusrequestsoverviewscan)
- [let ICScannerStatusWarmingUp: String](/documentation/imagecapturecore/icscannerstatuswarmingup)
- [let ICScannerStatusWarmUpDone: String](/documentation/imagecapturecore/icscannerstatuswarmupdone)

### Buttons

- [let ICButtonTypeCopy: String](/documentation/imagecapturecore/icbuttontypecopy)
- [let ICButtonTypeMail: String](/documentation/imagecapturecore/icbuttontypemail)
- [let ICButtonTypePrint: String](/documentation/imagecapturecore/icbuttontypeprint)
- [let ICButtonTypeScan: String](/documentation/imagecapturecore/icbuttontypescan)
- [let ICButtonTypeTransfer: String](/documentation/imagecapturecore/icbuttontypetransfer)
- [let ICButtonTypeWeb: String](/documentation/imagecapturecore/icbuttontypeweb)

## Errors

- [ICReturn](/documentation/imagecapturecore/icreturn)

### Error Details

- [var errorCode: Int](/documentation/imagecapturecore/icreturn/3143766-errorcode)
- [var errorUserInfo: [String : Any]](/documentation/imagecapturecore/icreturn/3143768-erroruserinfo)
- [var localizedDescription: String](/documentation/imagecapturecore/icreturn/3143775-localizeddescription)

### Error Domain

- [static var errorDomain: String](/documentation/imagecapturecore/icreturn/3143767-errordomain)
- [let ICErrorDomain: String](/documentation/imagecapturecore/icerrordomain)

### Error Codes

- [static var communicationTimedOut: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143744-communicationtimedout)
- [static var deleteFilesCanceled: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143745-deletefilescanceled)
- [static var deleteFilesFailed: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143746-deletefilesfailed)
- [static var deviceCommandGeneralFailure: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143747-devicecommandgeneralfailure)
- [static var deviceCouldNotPair: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143748-devicecouldnotpair)
- [static var deviceCouldNotUnpair: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143749-devicecouldnotunpair)
- [static var deviceFailedToCloseSession: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143750-devicefailedtoclosesession)
- [static var deviceFailedToCompleteTransfer: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143751-devicefailedtocompletetransfer)
- [static var deviceFailedToOpenSession: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143752-devicefailedtoopensession)
- [static var deviceFailedToSendData: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143753-devicefailedtosenddata)
- [static var deviceFailedToTakePicture: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143754-devicefailedtotakepicture)
- [static var deviceIsBusyEnumerating: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143755-deviceisbusyenumerating)
- [static var deviceIsPasscodeLocked: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143756-deviceispasscodelocked)
- [static var deviceNeedsCredentials: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143757-deviceneedscredentials)
- [static var deviceSoftwareInstallationCanceled: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143758-devicesoftwareinstallationcancel)
- [static var deviceSoftwareInstallationCompleted: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143759-devicesoftwareinstallationcomple)
- [static var deviceSoftwareInstallationFailed: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143760-devicesoftwareinstallationfailed)
- [static var deviceSoftwareIsBeingInstalled: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143761-devicesoftwareisbeinginstalled)
- [static var deviceSoftwareNotAvailable: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143762-devicesoftwarenotavailable)
- [static var deviceSoftwareNotInstalled: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143763-devicesoftwarenotinstalled)
- [static var downloadCanceled: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143764-downloadcanceled)
- [static var downloadFailed: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143765-downloadfailed)
- [static var exFATVolumeInvalid: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143769-exfatvolumeinvalid)
- [static var failedToCompletePassThroughCommand: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143770-failedtocompletepassthroughcomma)
- [static var failedToCompleteSendMessageRequest: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143771-failedtocompletesendmessagereque)
- [static var failedToDisabeTethering: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143772-failedtodisabetethering)
- [static var failedToEnabeTethering: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143773-failedtoenabetethering)
- [static var invalidParam: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143774-invalidparam)
- [static var multiErrorDictionary: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143776-multierrordictionary)
- [static var receivedUnsolicitedScannerErrorInfo: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143777-receivedunsolicitedscannererrori)
- [static var receivedUnsolicitedScannerStatusInfo: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143778-receivedunsolicitedscannerstatus)
- [static var scanOperationCanceled: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143779-scanoperationcanceled)
- [static var scannerFailedToCompleteOverviewScan: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143780-scannerfailedtocompleteoverviews)
- [static var scannerFailedToCompleteScan: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143781-scannerfailedtocompletescan)
- [static var scannerFailedToSelectFunctionalUnit: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143782-scannerfailedtoselectfunctionalu)
- [static var scannerInUseByLocalUser: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143783-scannerinusebylocaluser)
- [static var scannerInUseByRemoteUser: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143784-scannerinusebyremoteuser)
- [static var sessionNotOpened: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143785-sessionnotopened)
- [static var success: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143786-success)
- [static var uploadFailed: ICReturn.Code](/documentation/imagecapturecore/icreturn/3143787-uploadfailed)
- [ICReturn.Code](/documentation/imagecapturecore/icreturn/code)

#### Enumeration Cases

- [case communicationTimedOut](/documentation/imagecapturecore/icreturn/code/communicationtimedout)
- [case deleteFilesCanceled](/documentation/imagecapturecore/icreturn/code/deletefilescanceled)
- [case deleteFilesFailed](/documentation/imagecapturecore/icreturn/code/deletefilesfailed)
- [case deviceCouldNotPair](/documentation/imagecapturecore/icreturn/code/devicecouldnotpair)
- [case deviceCouldNotUnpair](/documentation/imagecapturecore/icreturn/code/devicecouldnotunpair)
- [case deviceFailedToCloseSession](/documentation/imagecapturecore/icreturn/code/devicefailedtoclosesession)
- [case deviceFailedToOpenSession](/documentation/imagecapturecore/icreturn/code/devicefailedtoopensession)
- [case deviceFailedToTakePicture](/documentation/imagecapturecore/icreturn/code/devicefailedtotakepicture)
- [case deviceIsPasscodeLocked](/documentation/imagecapturecore/icreturn/code/deviceispasscodelocked)
- [case deviceNeedsCredentials](/documentation/imagecapturecore/icreturn/code/deviceneedscredentials)
- [case deviceSoftwareInstallationCanceled](/documentation/imagecapturecore/icreturn/code/devicesoftwareinstallationcanceled)
- [case deviceSoftwareInstallationCompleted](/documentation/imagecapturecore/icreturn/code/devicesoftwareinstallationcompleted)
- [case deviceSoftwareInstallationFailed](/documentation/imagecapturecore/icreturn/code/devicesoftwareinstallationfailed)
- [case deviceSoftwareIsBeingInstalled](/documentation/imagecapturecore/icreturn/code/devicesoftwareisbeinginstalled)
- [case deviceSoftwareNotAvailable](/documentation/imagecapturecore/icreturn/code/devicesoftwarenotavailable)
- [case deviceSoftwareNotInstalled](/documentation/imagecapturecore/icreturn/code/devicesoftwarenotinstalled)
- [case downloadCanceled](/documentation/imagecapturecore/icreturn/code/downloadcanceled)
- [case downloadFailed](/documentation/imagecapturecore/icreturn/code/downloadfailed)
- [case failedToCompletePassThroughCommand](/documentation/imagecapturecore/icreturn/code/failedtocompletepassthroughcommand)
- [case failedToCompleteSendMessageRequest](/documentation/imagecapturecore/icreturn/code/failedtocompletesendmessagerequest)
- [case failedToDisabeTethering](/documentation/imagecapturecore/icreturn/code/failedtodisabetethering)
- [case failedToEnabeTethering](/documentation/imagecapturecore/icreturn/code/failedtoenabetethering)
- [case invalidParam](/documentation/imagecapturecore/icreturn/code/invalidparam)
- [case receivedUnsolicitedScannerErrorInfo](/documentation/imagecapturecore/icreturn/code/receivedunsolicitedscannererrorinfo)
- [case receivedUnsolicitedScannerStatusInfo](/documentation/imagecapturecore/icreturn/code/receivedunsolicitedscannerstatusinfo)
- [case scanOperationCanceled](/documentation/imagecapturecore/icreturn/code/scanoperationcanceled)
- [case scannerFailedToCompleteOverviewScan](/documentation/imagecapturecore/icreturn/code/scannerfailedtocompleteoverviewscan)
- [case scannerFailedToCompleteScan](/documentation/imagecapturecore/icreturn/code/scannerfailedtocompletescan)
- [case scannerFailedToSelectFunctionalUnit](/documentation/imagecapturecore/icreturn/code/scannerfailedtoselectfunctionalunit)
- [case scannerInUseByLocalUser](/documentation/imagecapturecore/icreturn/code/scannerinusebylocaluser)
- [case scannerInUseByRemoteUser](/documentation/imagecapturecore/icreturn/code/scannerinusebyremoteuser)
- [case success](/documentation/imagecapturecore/icreturn/code/success)
- [case uploadFailed](/documentation/imagecapturecore/icreturn/code/uploadfailed)
- [case deviceIsBusyEnumerating](/documentation/imagecapturecore/icreturn/code/deviceisbusyenumerating)
- [case deviceCommandGeneralFailure](/documentation/imagecapturecore/icreturn/code/devicecommandgeneralfailure)
- [case deviceFailedToCompleteTransfer](/documentation/imagecapturecore/icreturn/code/devicefailedtocompletetransfer)
- [case deviceFailedToSendData](/documentation/imagecapturecore/icreturn/code/devicefailedtosenddata)
- [case exFATVolumeInvalid](/documentation/imagecapturecore/icreturn/code/exfatvolumeinvalid)
- [case multiErrorDictionary](/documentation/imagecapturecore/icreturn/code/multierrordictionary)
- [case sessionNotOpened](/documentation/imagecapturecore/icreturn/code/sessionnotopened)
- [ICReturnCodeOffset](/documentation/imagecapturecore/icreturncodeoffset)

#### Enumeration Cases

- [case deleteOffset](/documentation/imagecapturecore/icreturncodeoffset/deleteoffset)
- [case deviceConnection](/documentation/imagecapturecore/icreturncodeoffset/deviceconnection)
- [case deviceOffset](/documentation/imagecapturecore/icreturncodeoffset/deviceoffset)
- [case downloadOffset](/documentation/imagecapturecore/icreturncodeoffset/downloadoffset)
- [case exFATOffset](/documentation/imagecapturecore/icreturncodeoffset/exfatoffset)
- [case metadataOffset](/documentation/imagecapturecore/icreturncodeoffset/metadataoffset)
- [case objectOffset](/documentation/imagecapturecore/icreturncodeoffset/objectoffset)
- [case ptpOffset](/documentation/imagecapturecore/icreturncodeoffset/ptpoffset)
- [case systemOffset](/documentation/imagecapturecore/icreturncodeoffset/systemoffset)
- [case thumbnailOffset](/documentation/imagecapturecore/icreturncodeoffset/thumbnailoffset)

### Comparison Operator

- [static func != (ICReturn, ICReturn) -> Bool](/documentation/imagecapturecore/icreturn/3143743)

### Initializers

- [init(Code, userInfo: [String : Any])](/documentation/imagecapturecore/icreturn/3727579-init)

### Instance Properties

- [var code: Code](/documentation/imagecapturecore/icreturn/3727576-code)
- [var hashValue: Int](/documentation/imagecapturecore/icreturn/3727578-hashvalue)
- [var userInfo: [String : Any]](/documentation/imagecapturecore/icreturn/3727580-userinfo)

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/imagecapturecore/icreturn/3727577-hash)

### Operator Functions

- [static func == (ICReturn, ICReturn) -> Bool](/documentation/imagecapturecore/icreturn/3727575)
- [ICLegacyReturn](/documentation/imagecapturecore/iclegacyreturn)

### Error Details

- [var errorCode: Int](/documentation/imagecapturecore/iclegacyreturn/3152830-errorcode)
- [var errorUserInfo: [String : Any]](/documentation/imagecapturecore/iclegacyreturn/3152832-erroruserinfo)
- [var localizedDescription: String](/documentation/imagecapturecore/iclegacyreturn/3152841-localizeddescription)

### Error Domain

- [static var errorDomain: String](/documentation/imagecapturecore/iclegacyreturn/3152831-errordomain)
- [let ICErrorDomain: String](/documentation/imagecapturecore/icerrordomain)

### Error Codes

- [static var cannotYieldDevice: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152817-cannotyielddevice)
- [static var communicationErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152818-communicationerr)
- [static var dataTypeNotFoundErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152819-datatypenotfounderr)
- [static var deviceAlreadyOpenErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152820-devicealreadyopenerr)
- [static var deviceGUIDNotFoundErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152821-deviceguidnotfounderr)
- [static var deviceIOServicePathNotFoundErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152822-deviceioservicepathnotfounderr)
- [static var deviceInternalErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152823-deviceinternalerr)
- [static var deviceInvalidParamErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152824-deviceinvalidparamerr)
- [static var deviceLocationIDNotFoundErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152825-devicelocationidnotfounderr)
- [static var deviceMemoryAllocationErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152826-devicememoryallocationerr)
- [static var deviceNotFoundErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152827-devicenotfounderr)
- [static var deviceNotOpenErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152828-devicenotopenerr)
- [static var deviceUnsupportedErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152829-deviceunsupportederr)
- [static var extensionInternalErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152833-extensioninternalerr)
- [static var fileCorruptedErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152834-filecorruptederr)
- [static var frameworkInternalErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152835-frameworkinternalerr)
- [static var indexOutOfRangeErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152836-indexoutofrangeerr)
- [static var invalidObjectErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152837-invalidobjecterr)
- [static var invalidPropertyErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152838-invalidpropertyerr)
- [static var invalidSessionErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152839-invalidsessionerr)
- [static var ioPendingErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152840-iopendingerr)
- [static var propertyTypeNotFoundErr: ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/3152842-propertytypenotfounderr)
- [ICLegacyReturn.Code](/documentation/imagecapturecore/iclegacyreturn/code)

#### Enumeration Cases

- [case cannotYieldDevice](/documentation/imagecapturecore/iclegacyreturn/code/cannotyielddevice)
- [case communicationErr](/documentation/imagecapturecore/iclegacyreturn/code/communicationerr)
- [case dataTypeNotFoundErr](/documentation/imagecapturecore/iclegacyreturn/code/datatypenotfounderr)
- [case deviceAlreadyOpenErr](/documentation/imagecapturecore/iclegacyreturn/code/devicealreadyopenerr)
- [case deviceGUIDNotFoundErr](/documentation/imagecapturecore/iclegacyreturn/code/deviceguidnotfounderr)
- [case deviceIOServicePathNotFoundErr](/documentation/imagecapturecore/iclegacyreturn/code/deviceioservicepathnotfounderr)
- [case deviceInternalErr](/documentation/imagecapturecore/iclegacyreturn/code/deviceinternalerr)
- [case deviceInvalidParamErr](/documentation/imagecapturecore/iclegacyreturn/code/deviceinvalidparamerr)
- [case deviceLocationIDNotFoundErr](/documentation/imagecapturecore/iclegacyreturn/code/devicelocationidnotfounderr)
- [case deviceMemoryAllocationErr](/documentation/imagecapturecore/iclegacyreturn/code/devicememoryallocationerr)
- [case deviceNotFoundErr](/documentation/imagecapturecore/iclegacyreturn/code/devicenotfounderr)
- [case deviceNotOpenErr](/documentation/imagecapturecore/iclegacyreturn/code/devicenotopenerr)
- [case deviceUnsupportedErr](/documentation/imagecapturecore/iclegacyreturn/code/deviceunsupportederr)
- [case extensionInternalErr](/documentation/imagecapturecore/iclegacyreturn/code/extensioninternalerr)
- [case fileCorruptedErr](/documentation/imagecapturecore/iclegacyreturn/code/filecorruptederr)
- [case frameworkInternalErr](/documentation/imagecapturecore/iclegacyreturn/code/frameworkinternalerr)
- [case indexOutOfRangeErr](/documentation/imagecapturecore/iclegacyreturn/code/indexoutofrangeerr)
- [case invalidObjectErr](/documentation/imagecapturecore/iclegacyreturn/code/invalidobjecterr)
- [case invalidPropertyErr](/documentation/imagecapturecore/iclegacyreturn/code/invalidpropertyerr)
- [case invalidSessionErr](/documentation/imagecapturecore/iclegacyreturn/code/invalidsessionerr)
- [case ioPendingErr](/documentation/imagecapturecore/iclegacyreturn/code/iopendingerr)
- [case propertyTypeNotFoundErr](/documentation/imagecapturecore/iclegacyreturn/code/propertytypenotfounderr)

### Comparison Operator

- [static func != (ICLegacyReturn, ICLegacyReturn) -> Bool](/documentation/imagecapturecore/iclegacyreturn/3152816)

### Initializers

- [init(Code, userInfo: [String : Any])](/documentation/imagecapturecore/iclegacyreturn/3727573-init)

### Instance Properties

- [var code: Code](/documentation/imagecapturecore/iclegacyreturn/3727570-code)
- [var hashValue: Int](/documentation/imagecapturecore/iclegacyreturn/3727572-hashvalue)
- [var userInfo: [String : Any]](/documentation/imagecapturecore/iclegacyreturn/3727574-userinfo)

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/imagecapturecore/iclegacyreturn/3727571-hash)

### Operator Functions

- [static func == (ICLegacyReturn, ICLegacyReturn) -> Bool](/documentation/imagecapturecore/iclegacyreturn/3727569)
- [ICReturnConnectionError](/documentation/imagecapturecore/icreturnconnectionerror)

### Error Details

- [var errorCode: Int](/documentation/imagecapturecore/icreturnconnectionerror/3152849-errorcode)
- [var errorUserInfo: [String : Any]](/documentation/imagecapturecore/icreturnconnectionerror/3152851-erroruserinfo)
- [var localizedDescription: String](/documentation/imagecapturecore/icreturnconnectionerror/3152854-localizeddescription)

### Error Domain

- [static var errorDomain: String](/documentation/imagecapturecore/icreturnconnectionerror/3152850-errordomain)
- [let ICErrorDomain: String](/documentation/imagecapturecore/icerrordomain)

### Error Codes

- [static var closedSessionSuddenly: ICReturnConnectionError.Code](/documentation/imagecapturecore/icreturnconnectionerror/3152845-closedsessionsuddenly)
- [static var driverExited: ICReturnConnectionError.Code](/documentation/imagecapturecore/icreturnconnectionerror/3152846-driverexited)
- [static var ejectFailed: ICReturnConnectionError.Code](/documentation/imagecapturecore/icreturnconnectionerror/3152847-ejectfailed)
- [static var ejectedSuddenly: ICReturnConnectionError.Code](/documentation/imagecapturecore/icreturnconnectionerror/3152848-ejectedsuddenly)
- [static var failedToOpen: ICReturnConnectionError.Code](/documentation/imagecapturecore/icreturnconnectionerror/3152852-failedtoopen)
- [static var failedToOpenDevice: ICReturnConnectionError.Code](/documentation/imagecapturecore/icreturnconnectionerror/3152853-failedtoopendevice)
- [static var sessionAlreadyOpen: ICReturnConnectionError.Code](/documentation/imagecapturecore/icreturnconnectionerror/3152855-sessionalreadyopen)
- [ICReturnConnectionError.Code](/documentation/imagecapturecore/icreturnconnectionerror/code)

#### Error Cases

- [case closedSessionSuddenly](/documentation/imagecapturecore/icreturnconnectionerror/code/closedsessionsuddenly)
- [case driverExited](/documentation/imagecapturecore/icreturnconnectionerror/code/driverexited)
- [case ejectedSuddenly](/documentation/imagecapturecore/icreturnconnectionerror/code/ejectedsuddenly)
- [case ejectFailed](/documentation/imagecapturecore/icreturnconnectionerror/code/ejectfailed)
- [case failedToOpen](/documentation/imagecapturecore/icreturnconnectionerror/code/failedtoopen)
- [case failedToOpenDevice](/documentation/imagecapturecore/icreturnconnectionerror/code/failedtoopendevice)
- [case sessionAlreadyOpen](/documentation/imagecapturecore/icreturnconnectionerror/code/sessionalreadyopen)

#### Enumeration Cases

- [case notAuthorizedToOpenDevice](/documentation/imagecapturecore/icreturnconnectionerror/code/notauthorizedtoopendevice)

### Comparison Operator

- [static func != (ICReturnConnectionError, ICReturnConnectionError) -> Bool](/documentation/imagecapturecore/icreturnconnectionerror/3152844)

### Initializers

- [init(Code, userInfo: [String : Any])](/documentation/imagecapturecore/icreturnconnectionerror/3727585-init)

### Instance Properties

- [var code: Code](/documentation/imagecapturecore/icreturnconnectionerror/3727582-code)
- [var hashValue: Int](/documentation/imagecapturecore/icreturnconnectionerror/3727584-hashvalue)
- [var userInfo: [String : Any]](/documentation/imagecapturecore/icreturnconnectionerror/3727586-userinfo)

### Type Properties

- [static var notAuthorizedToOpenDevice: ICReturnConnectionError.Code](/documentation/imagecapturecore/icreturnconnectionerror/3650431-notauthorizedtoopendevice)

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/imagecapturecore/icreturnconnectionerror/3727583-hash)

### Operator Functions

- [static func == (ICReturnConnectionError, ICReturnConnectionError) -> Bool](/documentation/imagecapturecore/icreturnconnectionerror/3727581)
- [ICReturnDownloadError](/documentation/imagecapturecore/icreturndownloaderror)

### Error Details

- [var errorCode: Int](/documentation/imagecapturecore/icreturndownloaderror/3393315-errorcode)
- [var errorUserInfo: [String : Any]](/documentation/imagecapturecore/icreturndownloaderror/3393317-erroruserinfo)
- [var localizedDescription: String](/documentation/imagecapturecore/icreturndownloaderror/3393319-localizeddescription)

### Error Domain

- [static var errorDomain: String](/documentation/imagecapturecore/icreturndownloaderror/3393316-errordomain)
- [let ICErrorDomain: String](/documentation/imagecapturecore/icerrordomain)

### Error Codes

- [static var fileWritable: ICReturnDownloadError.Code](/documentation/imagecapturecore/icreturndownloaderror/3393318-filewritable)
- [static var pathInvalid: ICReturnDownloadError.Code](/documentation/imagecapturecore/icreturndownloaderror/3393320-pathinvalid)
- [ICReturnDownloadError.Code](/documentation/imagecapturecore/icreturndownloaderror/code)

#### Enumeration Cases

- [case fileWritable](/documentation/imagecapturecore/icreturndownloaderror/code/filewritable)
- [case pathInvalid](/documentation/imagecapturecore/icreturndownloaderror/code/pathinvalid)

### Comparison Operator

- [static func != (ICReturnDownloadError, ICReturnDownloadError) -> Bool](/documentation/imagecapturecore/icreturndownloaderror/3393314)

### Initializers

- [init(Code, userInfo: [String : Any])](/documentation/imagecapturecore/icreturndownloaderror/3727591-init)

### Instance Properties

- [var code: Code](/documentation/imagecapturecore/icreturndownloaderror/3727588-code)
- [var hashValue: Int](/documentation/imagecapturecore/icreturndownloaderror/3727590-hashvalue)
- [var userInfo: [String : Any]](/documentation/imagecapturecore/icreturndownloaderror/3727592-userinfo)

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/imagecapturecore/icreturndownloaderror/3727589-hash)

### Operator Functions

- [static func == (ICReturnDownloadError, ICReturnDownloadError) -> Bool](/documentation/imagecapturecore/icreturndownloaderror/3727587)
- [ICReturnMetadataError](/documentation/imagecapturecore/icreturnmetadataerror)

### Error Details

- [var errorCode: Int](/documentation/imagecapturecore/icreturnmetadataerror/3143792-errorcode)
- [var errorUserInfo: [String : Any]](/documentation/imagecapturecore/icreturnmetadataerror/3143794-erroruserinfo)
- [var localizedDescription: String](/documentation/imagecapturecore/icreturnmetadataerror/3143796-localizeddescription)

### Error Domain

- [static var errorDomain: String](/documentation/imagecapturecore/icreturnmetadataerror/3143793-errordomain)
- [let ICErrorDomain: String](/documentation/imagecapturecore/icerrordomain)

### Error Codes

- [static var alreadyFetching: ICReturnMetadataError.Code](/documentation/imagecapturecore/icreturnmetadataerror/3143790-alreadyfetching)
- [static var canceled: ICReturnMetadataError.Code](/documentation/imagecapturecore/icreturnmetadataerror/3143791-canceled)
- [static var invalid: ICReturnMetadataError.Code](/documentation/imagecapturecore/icreturnmetadataerror/3143795-invalid)
- [static var notAvailable: ICReturnMetadataError.Code](/documentation/imagecapturecore/icreturnmetadataerror/3143797-notavailable)
- [ICReturnMetadataError.Code](/documentation/imagecapturecore/icreturnmetadataerror/code)

#### Error Cases

- [case alreadyFetching](/documentation/imagecapturecore/icreturnmetadataerror/code/alreadyfetching)
- [case canceled](/documentation/imagecapturecore/icreturnmetadataerror/code/canceled)
- [case invalid](/documentation/imagecapturecore/icreturnmetadataerror/code/invalid)
- [case notAvailable](/documentation/imagecapturecore/icreturnmetadataerror/code/notavailable)

### Comparison Operator

- [static func != (ICReturnMetadataError, ICReturnMetadataError) -> Bool](/documentation/imagecapturecore/icreturnmetadataerror/3143789)

### Initializers

- [init(Code, userInfo: [String : Any])](/documentation/imagecapturecore/icreturnmetadataerror/3727597-init)

### Instance Properties

- [var code: Code](/documentation/imagecapturecore/icreturnmetadataerror/3727594-code)
- [var hashValue: Int](/documentation/imagecapturecore/icreturnmetadataerror/3727596-hashvalue)
- [var userInfo: [String : Any]](/documentation/imagecapturecore/icreturnmetadataerror/3727598-userinfo)

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/imagecapturecore/icreturnmetadataerror/3727595-hash)

### Operator Functions

- [static func == (ICReturnMetadataError, ICReturnMetadataError) -> Bool](/documentation/imagecapturecore/icreturnmetadataerror/3727593)
- [ICReturnObjectError](/documentation/imagecapturecore/icreturnobjecterror)

### Error Details

- [var errorCode: Int](/documentation/imagecapturecore/icreturnobjecterror/3393327-errorcode)
- [var errorUserInfo: [String : Any]](/documentation/imagecapturecore/icreturnobjecterror/3393329-erroruserinfo)
- [var localizedDescription: String](/documentation/imagecapturecore/icreturnobjecterror/3393330-localizeddescription)

### Error Domain

- [static var errorDomain: String](/documentation/imagecapturecore/icreturnobjecterror/3393328-errordomain)
- [let ICErrorDomain: String](/documentation/imagecapturecore/icerrordomain)

### Error Codes

- [static var codeObjectDoesNotExist: ICReturnObjectError.Code](/documentation/imagecapturecore/icreturnobjecterror/3393326-codeobjectdoesnotexist)
- [static var codeObjectDataOffsetInvalid: ICReturnObjectError.Code](/documentation/imagecapturecore/icreturnobjecterror/3393325-codeobjectdataoffsetinvalid)
- [static var codeObjectCouldNotBeRead: ICReturnObjectError.Code](/documentation/imagecapturecore/icreturnobjecterror/3393323-codeobjectcouldnotberead)
- [static var codeObjectDataEmpty: ICReturnObjectError.Code](/documentation/imagecapturecore/icreturnobjecterror/3393324-codeobjectdataempty)
- [ICReturnObjectError.Code](/documentation/imagecapturecore/icreturnobjecterror/code)

#### Enumeration Cases

- [case codeObjectCouldNotBeRead](/documentation/imagecapturecore/icreturnobjecterror/code/codeobjectcouldnotberead)
- [case codeObjectDataEmpty](/documentation/imagecapturecore/icreturnobjecterror/code/codeobjectdataempty)
- [case codeObjectDataOffsetInvalid](/documentation/imagecapturecore/icreturnobjecterror/code/codeobjectdataoffsetinvalid)
- [case codeObjectDataRequestTooLarge](/documentation/imagecapturecore/icreturnobjecterror/code/codeobjectdatarequesttoolarge)
- [case codeObjectDoesNotExist](/documentation/imagecapturecore/icreturnobjecterror/code/codeobjectdoesnotexist)

### Comparison Operator

- [static func != (ICReturnObjectError, ICReturnObjectError) -> Bool](/documentation/imagecapturecore/icreturnobjecterror/3393322)

### Initializers

- [init(Code, userInfo: [String : Any])](/documentation/imagecapturecore/icreturnobjecterror/3727603-init)

### Instance Properties

- [var code: Code](/documentation/imagecapturecore/icreturnobjecterror/3727600-code)
- [var hashValue: Int](/documentation/imagecapturecore/icreturnobjecterror/3727602-hashvalue)
- [var userInfo: [String : Any]](/documentation/imagecapturecore/icreturnobjecterror/3727604-userinfo)

### Type Properties

- [static var codeObjectDataRequestTooLarge: ICReturnObjectError.Code](/documentation/imagecapturecore/icreturnobjecterror/3528220-codeobjectdatarequesttoolarge)

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/imagecapturecore/icreturnobjecterror/3727601-hash)

### Operator Functions

- [static func == (ICReturnObjectError, ICReturnObjectError) -> Bool](/documentation/imagecapturecore/icreturnobjecterror/3727599)
- [ICReturnPTPDeviceError](/documentation/imagecapturecore/icreturnptpdeviceerror)

### Error Details

- [var errorCode: Int](/documentation/imagecapturecore/icreturnptpdeviceerror/3393333-errorcode)
- [var errorUserInfo: [String : Any]](/documentation/imagecapturecore/icreturnptpdeviceerror/3393335-erroruserinfo)
- [var localizedDescription: String](/documentation/imagecapturecore/icreturnptpdeviceerror/3393337-localizeddescription)

### Error Domain

- [static var errorDomain: String](/documentation/imagecapturecore/icreturnptpdeviceerror/3393334-errordomain)
- [let ICErrorDomain: String](/documentation/imagecapturecore/icerrordomain)

### Error Codes

- [static var failedToSendCommand: ICReturnPTPDeviceError.Code](/documentation/imagecapturecore/icreturnptpdeviceerror/3393336-failedtosendcommand)
- [ICReturnPTPDeviceError.Code](/documentation/imagecapturecore/icreturnptpdeviceerror/code)

#### Enumeration Cases

- [case failedToSendCommand](/documentation/imagecapturecore/icreturnptpdeviceerror/code/failedtosendcommand)
- [case notAuthorizedToSendCommand](/documentation/imagecapturecore/icreturnptpdeviceerror/code/notauthorizedtosendcommand)

### Comparison Operator

- [static func != (ICReturnPTPDeviceError, ICReturnPTPDeviceError) -> Bool](/documentation/imagecapturecore/icreturnptpdeviceerror/3393332)

### Initializers

- [init(Code, userInfo: [String : Any])](/documentation/imagecapturecore/icreturnptpdeviceerror/3727609-init)

### Instance Properties

- [var code: Code](/documentation/imagecapturecore/icreturnptpdeviceerror/3727606-code)
- [var hashValue: Int](/documentation/imagecapturecore/icreturnptpdeviceerror/3727608-hashvalue)
- [var userInfo: [String : Any]](/documentation/imagecapturecore/icreturnptpdeviceerror/3727610-userinfo)

### Type Properties

- [static var notAuthorizedToSendCommand: ICReturnPTPDeviceError.Code](/documentation/imagecapturecore/icreturnptpdeviceerror/3528221-notauthorizedtosendcommand)

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/imagecapturecore/icreturnptpdeviceerror/3727607-hash)

### Operator Functions

- [static func == (ICReturnPTPDeviceError, ICReturnPTPDeviceError) -> Bool](/documentation/imagecapturecore/icreturnptpdeviceerror/3727605)
- [ICReturnThumbnailError](/documentation/imagecapturecore/icreturnthumbnailerror)

### Error Details

- [var errorCode: Int](/documentation/imagecapturecore/icreturnthumbnailerror/3143802-errorcode)
- [var errorUserInfo: [String : Any]](/documentation/imagecapturecore/icreturnthumbnailerror/3143804-erroruserinfo)
- [var localizedDescription: String](/documentation/imagecapturecore/icreturnthumbnailerror/3143806-localizeddescription)

### Error Domain

- [static var errorDomain: String](/documentation/imagecapturecore/icreturnthumbnailerror/3143803-errordomain)
- [let ICErrorDomain: String](/documentation/imagecapturecore/icerrordomain)

### Error Codes

- [static var alreadyFetching: ICReturnThumbnailError.Code](/documentation/imagecapturecore/icreturnthumbnailerror/3143800-alreadyfetching)
- [static var canceled: ICReturnThumbnailError.Code](/documentation/imagecapturecore/icreturnthumbnailerror/3143801-canceled)
- [static var invalid: ICReturnThumbnailError.Code](/documentation/imagecapturecore/icreturnthumbnailerror/3143805-invalid)
- [static var notAvailable: ICReturnThumbnailError.Code](/documentation/imagecapturecore/icreturnthumbnailerror/3143807-notavailable)
- [ICReturnThumbnailError.Code](/documentation/imagecapturecore/icreturnthumbnailerror/code)

#### Error Cases

- [case alreadyFetching](/documentation/imagecapturecore/icreturnthumbnailerror/code/alreadyfetching)
- [case canceled](/documentation/imagecapturecore/icreturnthumbnailerror/code/canceled)
- [case invalid](/documentation/imagecapturecore/icreturnthumbnailerror/code/invalid)
- [case notAvailable](/documentation/imagecapturecore/icreturnthumbnailerror/code/notavailable)

### Comparison Operator

- [static func != (ICReturnThumbnailError, ICReturnThumbnailError) -> Bool](/documentation/imagecapturecore/icreturnthumbnailerror/3143799)

### Initializers

- [init(Code, userInfo: [String : Any])](/documentation/imagecapturecore/icreturnthumbnailerror/3727615-init)

### Instance Properties

- [var code: Code](/documentation/imagecapturecore/icreturnthumbnailerror/3727612-code)
- [var hashValue: Int](/documentation/imagecapturecore/icreturnthumbnailerror/3727614-hashvalue)
- [var userInfo: [String : Any]](/documentation/imagecapturecore/icreturnthumbnailerror/3727616-userinfo)

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/imagecapturecore/icreturnthumbnailerror/3727613-hash)

### Operator Functions

- [static func == (ICReturnThumbnailError, ICReturnThumbnailError) -> Bool](/documentation/imagecapturecore/icreturnthumbnailerror/3727611)

## Legacy Symbols

- [let ICRunLoopMode: String](/documentation/imagecapturecore/icrunloopmode)

## Reference

- [ImageCaptureCore Enumerations](/documentation/imagecapturecore/imagecapturecore_enumerations)

### Enumerations

- [ICMediaPresentation](/documentation/imagecapturecore/icmediapresentation)

#### Enumeration Cases

- [case convertedAssets](/documentation/imagecapturecore/icmediapresentation/convertedassets)
- [case originalAssets](/documentation/imagecapturecore/icmediapresentation/originalassets)
- [ImageCaptureCore Constants](/documentation/imagecapturecore/imagecapturecore_constants)

### Constants

- [let ICErrorDomain: String](/documentation/imagecapturecore/icerrordomain)
- [ImageCaptureCore Data Types](/documentation/imagecapturecore/imagecapturecore_data_types)

### Data Types

- [ICAuthorizationStatus](/documentation/imagecapturecore/icauthorizationstatus)

#### Initializers

- [init(rawValue: String)](/documentation/imagecapturecore/icauthorizationstatus/3650430-init)

#### Type Properties

- [static let authorized: ICAuthorizationStatus](/documentation/imagecapturecore/icauthorizationstatus/3650387-authorized)
- [static let denied: ICAuthorizationStatus](/documentation/imagecapturecore/icauthorizationstatus/3650388-denied)
- [static let notDetermined: ICAuthorizationStatus](/documentation/imagecapturecore/icauthorizationstatus/3650389-notdetermined)
- [static let restricted: ICAuthorizationStatus](/documentation/imagecapturecore/icauthorizationstatus/3650390-restricted)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
