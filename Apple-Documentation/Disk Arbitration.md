# Disk Arbitration Documentation

Source: https://sosumi.ai/documentation/diskarbitration

---
title: Disk Arbitration
source: https://developer.apple.com/documentation/diskarbitration
timestamp: 2026-02-13T18:56:20.790Z
---

## Reference

- [DADisk.h](/documentation/diskarbitration/dadisk-h)

### Miscellaneous

- [func DADiskCopyDescription(DADisk) -> CFDictionary?](/documentation/diskarbitration/dadiskcopydescription(_:))
- [func DADiskCopyIOMedia(DADisk) -> io_service_t](/documentation/diskarbitration/dadiskcopyiomedia(_:))
- [func DADiskCopyWholeDisk(DADisk) -> DADisk?](/documentation/diskarbitration/dadiskcopywholedisk(_:))
- [func DADiskCreateFromBSDName(CFAllocator?, DASession, UnsafePointer<CChar>) -> DADisk?](/documentation/diskarbitration/dadiskcreatefrombsdname(_:_:_:))
- [func DADiskCreateFromIOMedia(CFAllocator?, DASession, io_service_t) -> DADisk?](/documentation/diskarbitration/dadiskcreatefromiomedia(_:_:_:))
- [func DADiskCreateFromVolumePath(CFAllocator?, DASession, CFURL) -> DADisk?](/documentation/diskarbitration/dadiskcreatefromvolumepath(_:_:_:))
- [func DADiskGetBSDName(DADisk) -> UnsafePointer<CChar>?](/documentation/diskarbitration/dadiskgetbsdname(_:))
- [func DADiskGetTypeID() -> CFTypeID](/documentation/diskarbitration/dadiskgettypeid())

### Data Types

- [DADisk](/documentation/diskarbitration/dadisk)
- [DADissenter.h](/documentation/diskarbitration/dadissenter-h)

### Miscellaneous

- [func DADissenterCreate(CFAllocator?, DAReturn, CFString?) -> DADissenter](/documentation/diskarbitration/dadissentercreate(_:_:_:))
- [func DADissenterGetStatus(DADissenter) -> DAReturn](/documentation/diskarbitration/dadissentergetstatus(_:))
- [func DADissenterGetStatusString(DADissenter) -> CFString?](/documentation/diskarbitration/dadissentergetstatusstring(_:))

### Data Types

- [DADissenter](/documentation/diskarbitration/dadissenter)
- [DASession.h](/documentation/diskarbitration/dasession-h)

### Miscellaneous

- [func DASessionCreate(CFAllocator?) -> DASession?](/documentation/diskarbitration/dasessioncreate(_:))
- [func DASessionGetTypeID() -> CFTypeID](/documentation/diskarbitration/dasessiongettypeid())
- [func DASessionScheduleWithRunLoop(DASession, CFRunLoop, CFString)](/documentation/diskarbitration/dasessionschedulewithrunloop(_:_:_:))
- [func DASessionSetDispatchQueue(DASession, dispatch_queue_t?)](/documentation/diskarbitration/dasessionsetdispatchqueue(_:_:))
- [func DASessionUnscheduleFromRunLoop(DASession, CFRunLoop, CFString)](/documentation/diskarbitration/dasessionunschedulefromrunloop(_:_:_:))

### Data Types

- [DASession](/documentation/diskarbitration/dasession)
- [DiskArbitration.h](/documentation/diskarbitration/diskarbitration-h)

### Miscellaneous

- [func DADiskClaim(DADisk, DADiskClaimOptions, DADiskClaimReleaseCallback?, UnsafeMutableRawPointer?, DADiskClaimCallback?, UnsafeMutableRawPointer?)](/documentation/diskarbitration/dadiskclaim(_:_:_:_:_:_:))
- [func DADiskEject(DADisk, DADiskEjectOptions, DADiskEjectCallback?, UnsafeMutableRawPointer?)](/documentation/diskarbitration/dadiskeject(_:_:_:_:))
- [func DADiskGetOptions(DADisk) -> DADiskOptions](/documentation/diskarbitration/dadiskgetoptions(_:))
- [func DADiskIsClaimed(DADisk) -> Bool](/documentation/diskarbitration/dadiskisclaimed(_:))
- [func DADiskMount(DADisk, CFURL?, DADiskMountOptions, DADiskMountCallback?, UnsafeMutableRawPointer?)](/documentation/diskarbitration/dadiskmount(_:_:_:_:_:))
- [func DADiskMountWithArguments(DADisk, CFURL?, DADiskMountOptions, DADiskMountCallback?, UnsafeMutableRawPointer?, UnsafeMutablePointer<Unmanaged<CFString>?>?)](/documentation/diskarbitration/dadiskmountwitharguments(_:_:_:_:_:_:))
- [func DADiskRename(DADisk, CFString, DADiskRenameOptions, DADiskRenameCallback?, UnsafeMutableRawPointer?)](/documentation/diskarbitration/dadiskrename(_:_:_:_:_:))
- [func DADiskSetOptions(DADisk, DADiskOptions, Bool) -> DAReturn](/documentation/diskarbitration/dadisksetoptions(_:_:_:))
- [func DADiskUnclaim(DADisk)](/documentation/diskarbitration/dadiskunclaim(_:))
- [func DADiskUnmount(DADisk, DADiskUnmountOptions, DADiskUnmountCallback?, UnsafeMutableRawPointer?)](/documentation/diskarbitration/dadiskunmount(_:_:_:_:))
- [func DARegisterDiskAppearedCallback(DASession, CFDictionary?, DADiskAppearedCallback, UnsafeMutableRawPointer?)](/documentation/diskarbitration/daregisterdiskappearedcallback(_:_:_:_:))
- [func DARegisterDiskDescriptionChangedCallback(DASession, CFDictionary?, CFArray?, DADiskDescriptionChangedCallback, UnsafeMutableRawPointer?)](/documentation/diskarbitration/daregisterdiskdescriptionchangedcallback(_:_:_:_:_:))
- [func DARegisterDiskDisappearedCallback(DASession, CFDictionary?, DADiskDisappearedCallback, UnsafeMutableRawPointer?)](/documentation/diskarbitration/daregisterdiskdisappearedcallback(_:_:_:_:))
- [func DARegisterDiskEjectApprovalCallback(DASession, CFDictionary?, DADiskEjectApprovalCallback, UnsafeMutableRawPointer?)](/documentation/diskarbitration/daregisterdiskejectapprovalcallback(_:_:_:_:))
- [func DARegisterDiskMountApprovalCallback(DASession, CFDictionary?, DADiskMountApprovalCallback, UnsafeMutableRawPointer?)](/documentation/diskarbitration/daregisterdiskmountapprovalcallback(_:_:_:_:))
- [func DARegisterDiskPeekCallback(DASession, CFDictionary?, CFIndex, DADiskPeekCallback, UnsafeMutableRawPointer?)](/documentation/diskarbitration/daregisterdiskpeekcallback(_:_:_:_:_:))
- [func DARegisterDiskUnmountApprovalCallback(DASession, CFDictionary?, DADiskUnmountApprovalCallback, UnsafeMutableRawPointer?)](/documentation/diskarbitration/daregisterdiskunmountapprovalcallback(_:_:_:_:))
- [func DAUnregisterCallback(DASession, UnsafeMutableRawPointer, UnsafeMutableRawPointer?)](/documentation/diskarbitration/daunregistercallback(_:_:_:))

### Callbacks

- [DADiskAppearedCallback](/documentation/diskarbitration/dadiskappearedcallback)
- [DADiskClaimCallback](/documentation/diskarbitration/dadiskclaimcallback)
- [DADiskClaimReleaseCallback](/documentation/diskarbitration/dadiskclaimreleasecallback)
- [DADiskDescriptionChangedCallback](/documentation/diskarbitration/dadiskdescriptionchangedcallback)
- [DADiskDisappearedCallback](/documentation/diskarbitration/dadiskdisappearedcallback)
- [DADiskEjectApprovalCallback](/documentation/diskarbitration/dadiskejectapprovalcallback)
- [DADiskEjectCallback](/documentation/diskarbitration/dadiskejectcallback)
- [DADiskMountApprovalCallback](/documentation/diskarbitration/dadiskmountapprovalcallback)
- [DADiskMountCallback](/documentation/diskarbitration/dadiskmountcallback)
- [DADiskPeekCallback](/documentation/diskarbitration/dadiskpeekcallback)
- [DADiskRenameCallback](/documentation/diskarbitration/dadiskrenamecallback)
- [DADiskUnmountApprovalCallback](/documentation/diskarbitration/dadiskunmountapprovalcallback)
- [DADiskUnmountCallback](/documentation/diskarbitration/dadiskunmountcallback)

### Constants

- [Global Variables](/documentation/diskarbitration/global-variables)

#### Constants

- [var kDADiskDescriptionMatchMediaUnformatted: Unmanaged<CFDictionary>](/documentation/diskarbitration/kdadiskdescriptionmatchmediaunformatted)
- [var kDADiskDescriptionMatchMediaWhole: Unmanaged<CFDictionary>](/documentation/diskarbitration/kdadiskdescriptionmatchmediawhole)
- [var kDADiskDescriptionMatchVolumeMountable: Unmanaged<CFDictionary>](/documentation/diskarbitration/kdadiskdescriptionmatchvolumemountable)
- [var kDADiskDescriptionMatchVolumeUnrecognized: Unmanaged<CFDictionary>](/documentation/diskarbitration/kdadiskdescriptionmatchvolumeunrecognized)
- [var kDADiskDescriptionWatchVolumeName: Unmanaged<CFArray>](/documentation/diskarbitration/kdadiskdescriptionwatchvolumename)
- [var kDADiskDescriptionWatchVolumePath: Unmanaged<CFArray>](/documentation/diskarbitration/kdadiskdescriptionwatchvolumepath)
- [DADiskClaimOptions](/documentation/diskarbitration/dadiskclaimoptions)

#### Constants

- [var kDADiskClaimOptionDefault: Int](/documentation/diskarbitration/kdadiskclaimoptiondefault)
- [DADiskEjectOptions](/documentation/diskarbitration/dadiskejectoptions)
- [DADiskMountOptions](/documentation/diskarbitration/dadiskmountoptions)

#### Constants

- [var kDADiskMountOptionWhole: Int](/documentation/diskarbitration/kdadiskmountoptionwhole)
- [DADiskRenameOptions](/documentation/diskarbitration/dadiskrenameoptions)

#### Constants

- [var kDADiskRenameOptionDefault: Int](/documentation/diskarbitration/kdadiskrenameoptiondefault)
- [DADiskUnmountOptions](/documentation/diskarbitration/dadiskunmountoptions)

#### Constants

- [var kDADiskUnmountOptionForce: Int](/documentation/diskarbitration/kdadiskunmountoptionforce)
- [var kDADiskUnmountOptionWhole: Int](/documentation/diskarbitration/kdadiskunmountoptionwhole)
- [DiskArbitration Enumerations](/documentation/diskarbitration/diskarbitration-enumerations)

### Enumerations

- [Anonymous](/documentation/diskarbitration/anonymous-kdadiskunmountoptions)

#### Constants

- [var kDADiskUnmountOptionDefault: Int](/documentation/diskarbitration/kdadiskunmountoptiondefault)
- [var kDADiskUnmountOptionForce: Int](/documentation/diskarbitration/kdadiskunmountoptionforce)
- [var kDADiskUnmountOptionWhole: Int](/documentation/diskarbitration/kdadiskunmountoptionwhole)
- [Anonymous](/documentation/diskarbitration/anonymous-kdadiskmountoptions)

#### Constants

- [var kDADiskMountOptionDefault: Int](/documentation/diskarbitration/kdadiskmountoptiondefault)
- [var kDADiskMountOptionWhole: Int](/documentation/diskarbitration/kdadiskmountoptionwhole)
- [Anonymous](/documentation/diskarbitration/anonymous-kdadiskoptions)

#### Constants

- [var kDADiskOptionDefault: Int](/documentation/diskarbitration/kdadiskoptiondefault)
- [DiskArbitration Constants](/documentation/diskarbitration/diskarbitration-constants)

### Constants

- [let kDADiskDescriptionBusNameKey: CFString](/documentation/diskarbitration/kdadiskdescriptionbusnamekey)
- [let kDADiskDescriptionBusPathKey: CFString](/documentation/diskarbitration/kdadiskdescriptionbuspathkey)
- [let kDADiskDescriptionDeviceGUIDKey: CFString](/documentation/diskarbitration/kdadiskdescriptiondeviceguidkey)
- [let kDADiskDescriptionDeviceInternalKey: CFString](/documentation/diskarbitration/kdadiskdescriptiondeviceinternalkey)
- [let kDADiskDescriptionDeviceModelKey: CFString](/documentation/diskarbitration/kdadiskdescriptiondevicemodelkey)
- [let kDADiskDescriptionDevicePathKey: CFString](/documentation/diskarbitration/kdadiskdescriptiondevicepathkey)
- [let kDADiskDescriptionDeviceProtocolKey: CFString](/documentation/diskarbitration/kdadiskdescriptiondeviceprotocolkey)
- [let kDADiskDescriptionDeviceRevisionKey: CFString](/documentation/diskarbitration/kdadiskdescriptiondevicerevisionkey)
- [let kDADiskDescriptionDeviceUnitKey: CFString](/documentation/diskarbitration/kdadiskdescriptiondeviceunitkey)
- [let kDADiskDescriptionDeviceVendorKey: CFString](/documentation/diskarbitration/kdadiskdescriptiondevicevendorkey)
- [let kDADiskDescriptionMediaBSDMajorKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediabsdmajorkey)
- [let kDADiskDescriptionMediaBSDMinorKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediabsdminorkey)
- [let kDADiskDescriptionMediaBSDNameKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediabsdnamekey)
- [let kDADiskDescriptionMediaBSDUnitKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediabsdunitkey)
- [let kDADiskDescriptionMediaBlockSizeKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediablocksizekey)
- [let kDADiskDescriptionMediaContentKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediacontentkey)
- [let kDADiskDescriptionMediaEjectableKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediaejectablekey)
- [let kDADiskDescriptionMediaIconKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediaiconkey)
- [let kDADiskDescriptionMediaKindKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediakindkey)
- [let kDADiskDescriptionMediaLeafKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmedialeafkey)
- [let kDADiskDescriptionMediaNameKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmedianamekey)
- [let kDADiskDescriptionMediaPathKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediapathkey)
- [let kDADiskDescriptionMediaRemovableKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediaremovablekey)
- [let kDADiskDescriptionMediaSizeKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediasizekey)
- [let kDADiskDescriptionMediaTypeKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediatypekey)
- [let kDADiskDescriptionMediaUUIDKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediauuidkey)
- [let kDADiskDescriptionMediaWholeKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediawholekey)
- [let kDADiskDescriptionMediaWritableKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediawritablekey)
- [let kDADiskDescriptionVolumeKindKey: CFString](/documentation/diskarbitration/kdadiskdescriptionvolumekindkey)
- [let kDADiskDescriptionVolumeMountableKey: CFString](/documentation/diskarbitration/kdadiskdescriptionvolumemountablekey)
- [let kDADiskDescriptionVolumeNameKey: CFString](/documentation/diskarbitration/kdadiskdescriptionvolumenamekey)
- [let kDADiskDescriptionVolumeNetworkKey: CFString](/documentation/diskarbitration/kdadiskdescriptionvolumenetworkkey)
- [let kDADiskDescriptionVolumePathKey: CFString](/documentation/diskarbitration/kdadiskdescriptionvolumepathkey)
- [let kDADiskDescriptionVolumeTypeKey: CFString](/documentation/diskarbitration/kdadiskdescriptionvolumetypekey)
- [let kDADiskDescriptionVolumeUUIDKey: CFString](/documentation/diskarbitration/kdadiskdescriptionvolumeuuidkey)
- [let kDADiskDescriptionDeviceTDMLockedKey: CFString](/documentation/diskarbitration/kdadiskdescriptiondevicetdmlockedkey)
- [let kDADiskDescriptionMediaEncryptedKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediaencryptedkey)
- [let kDADiskDescriptionMediaEncryptionDetailKey: CFString](/documentation/diskarbitration/kdadiskdescriptionmediaencryptiondetailkey)
- [DiskArbitration Data Types](/documentation/diskarbitration/diskarbitration-data-types)

### Data Types

- [DADiskClaimOptions](/documentation/diskarbitration/dadiskclaimoptions)

#### Constants

- [var kDADiskClaimOptionDefault: Int](/documentation/diskarbitration/kdadiskclaimoptiondefault)
- [DADiskEjectOptions](/documentation/diskarbitration/dadiskejectoptions)
- [DADiskMountOptions](/documentation/diskarbitration/dadiskmountoptions)

#### Constants

- [var kDADiskMountOptionWhole: Int](/documentation/diskarbitration/kdadiskmountoptionwhole)
- [DADiskOptions](/documentation/diskarbitration/dadiskoptions)
- [DADiskRenameOptions](/documentation/diskarbitration/dadiskrenameoptions)

#### Constants

- [var kDADiskRenameOptionDefault: Int](/documentation/diskarbitration/kdadiskrenameoptiondefault)
- [DADiskUnmountOptions](/documentation/diskarbitration/dadiskunmountoptions)

#### Constants

- [var kDADiskUnmountOptionForce: Int](/documentation/diskarbitration/kdadiskunmountoptionforce)
- [var kDADiskUnmountOptionWhole: Int](/documentation/diskarbitration/kdadiskunmountoptionwhole)
- [DAReturn](/documentation/diskarbitration/dareturn)

## Articles

- [DAReturn](/documentation/diskarbitration/enum_(unnamed)-3ky11)

### Constants

- [var kDAReturnBadArgument: Int](/documentation/diskarbitration/kdareturnbadargument)
- [var kDAReturnBusy: Int](/documentation/diskarbitration/kdareturnbusy)
- [var kDAReturnError: Int](/documentation/diskarbitration/kdareturnerror)
- [var kDAReturnExclusiveAccess: Int](/documentation/diskarbitration/kdareturnexclusiveaccess)
- [var kDAReturnNoResources: Int](/documentation/diskarbitration/kdareturnnoresources)
- [var kDAReturnNotFound: Int](/documentation/diskarbitration/kdareturnnotfound)
- [var kDAReturnNotMounted: Int](/documentation/diskarbitration/kdareturnnotmounted)
- [var kDAReturnNotPermitted: Int](/documentation/diskarbitration/kdareturnnotpermitted)
- [var kDAReturnNotPrivileged: Int](/documentation/diskarbitration/kdareturnnotprivileged)
- [var kDAReturnNotReady: Int](/documentation/diskarbitration/kdareturnnotready)
- [var kDAReturnNotWritable: Int](/documentation/diskarbitration/kdareturnnotwritable)
- [var kDAReturnSuccess: Int](/documentation/diskarbitration/kdareturnsuccess)
- [var kDAReturnUnsupported: Int](/documentation/diskarbitration/kdareturnunsupported)
- [kDADiskOptionEjectUponLogout](/documentation/diskarbitration/kdadiskoptionejectuponlogout)
- [kDADiskOptionMountAutomatic](/documentation/diskarbitration/kdadiskoptionmountautomatic)
- [kDADiskOptionMountAutomaticNoDefer](/documentation/diskarbitration/kdadiskoptionmountautomaticnodefer)
- [kDADiskOptionPrivate](/documentation/diskarbitration/kdadiskoptionprivate)

## Variables

- [let kDADiskDescriptionFSKitPrefix: CFString](/documentation/diskarbitration/kdadiskdescriptionfskitprefix)
- [let kDADiskDescriptionRepairRunningKey: CFString](/documentation/diskarbitration/kdadiskdescriptionrepairrunningkey)
- [var kDADiskMountOptionNoFollow: Int](/documentation/diskarbitration/kdadiskmountoptionnofollow)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
