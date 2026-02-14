# IOSurface Documentation

Source: https://sosumi.ai/documentation/iosurface

---
title: IOSurface
source: https://developer.apple.com/documentation/iosurface
timestamp: 2026-02-13T18:58:25.178Z
---

## Classes

- [IOSurface](/documentation/iosurface/iosurface)

### Initializers

- [init?(properties: [IOSurfacePropertyKey : any Sendable])](/documentation/iosurface/iosurface/init(properties:))
- [init(IOSurfaceRef)](/documentation/iosurface/iosurface/init(_:))

### Instance Properties

- [var allocationSize: Int](/documentation/iosurface/iosurface/allocationsize)
- [var allowsPixelSizeCasting: Bool](/documentation/iosurface/iosurface/allowspixelsizecasting)
- [var baseAddress: UnsafeMutableRawPointer](/documentation/iosurface/iosurface/baseaddress)
- [var bytesPerElement: Int](/documentation/iosurface/iosurface/bytesperelement)
- [var bytesPerRow: Int](/documentation/iosurface/iosurface/bytesperrow)
- [var elementHeight: Int](/documentation/iosurface/iosurface/elementheight)
- [var elementWidth: Int](/documentation/iosurface/iosurface/elementwidth)
- [var height: Int](/documentation/iosurface/iosurface/height)
- [var isInUse: Bool](/documentation/iosurface/iosurface/isinuse)
- [var localUseCount: Int32](/documentation/iosurface/iosurface/localusecount)
- [var pixelFormat: OSType](/documentation/iosurface/iosurface/pixelformat)
- [var planeCount: Int](/documentation/iosurface/iosurface/planecount)
- [var seed: UInt32](/documentation/iosurface/iosurface/seed)
- [var width: Int](/documentation/iosurface/iosurface/width)
- [var surfaceID: UInt32](/documentation/iosurface/iosurface/surfaceid)

### Instance Methods

- [func allAttachments() -> [String : any Sendable]?](/documentation/iosurface/iosurface/allattachments())
- [func attachment(forKey: String) -> (any Sendable)?](/documentation/iosurface/iosurface/attachment(forkey:))
- [func baseAddressOfPlane(at: Int) -> UnsafeMutableRawPointer](/documentation/iosurface/iosurface/baseaddressofplane(at:))
- [func bytesPerElementOfPlane(at: Int) -> Int](/documentation/iosurface/iosurface/bytesperelementofplane(at:))
- [func bytesPerRowOfPlane(at: Int) -> Int](/documentation/iosurface/iosurface/bytesperrowofplane(at:))
- [func decrementUseCount()](/documentation/iosurface/iosurface/decrementusecount())
- [func elementHeightOfPlane(at: Int) -> Int](/documentation/iosurface/iosurface/elementheightofplane(at:))
- [func elementWidthOfPlane(at: Int) -> Int](/documentation/iosurface/iosurface/elementwidthofplane(at:))
- [func heightOfPlane(at: Int) -> Int](/documentation/iosurface/iosurface/heightofplane(at:))
- [func incrementUseCount()](/documentation/iosurface/iosurface/incrementusecount())
- [func lock(options: IOSurfaceLockOptions, seed: UnsafeMutablePointer<UInt32>?) -> kern_return_t](/documentation/iosurface/iosurface/lock(options:seed:))
- [func removeAllAttachments()](/documentation/iosurface/iosurface/removeallattachments())
- [func removeAttachment(forKey: String)](/documentation/iosurface/iosurface/removeattachment(forkey:))
- [func setAllAttachments([String : any Sendable])](/documentation/iosurface/iosurface/setallattachments(_:))
- [func setAttachment(any Sendable, forKey: String)](/documentation/iosurface/iosurface/setattachment(_:forkey:))
- [func setPurgeable(IOSurfacePurgeabilityState, oldState: UnsafeMutablePointer<IOSurfacePurgeabilityState>?) -> kern_return_t](/documentation/iosurface/iosurface/setpurgeable(_:oldstate:))
- [func unlock(options: IOSurfaceLockOptions, seed: UnsafeMutablePointer<UInt32>?) -> kern_return_t](/documentation/iosurface/iosurface/unlock(options:seed:))
- [func widthOfPlane(at: Int) -> Int](/documentation/iosurface/iosurface/widthofplane(at:))
- [IOSurfaceRef](/documentation/iosurface/iosurfaceref)

### Initializers

- [init(IOSurface)](/documentation/iosurface/iosurfaceref/init(_:))

## Structures

- [IOSurfaceLockOptions](/documentation/iosurface/iosurfacelockoptions)

### Initializers

- [init(rawValue: UInt32)](/documentation/iosurface/iosurfacelockoptions/init(rawvalue:))

### Options

- [static var avoidSync: IOSurfaceLockOptions](/documentation/iosurface/iosurfacelockoptions/avoidsync)
- [static var readOnly: IOSurfaceLockOptions](/documentation/iosurface/iosurfacelockoptions/readonly)
- [IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey)

### Initializers

- [init(rawValue: String)](/documentation/iosurface/iosurfacepropertykey/init(rawvalue:))

### Type Properties

- [static let allocSizeKey: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/allocsizekey)
- [static let bytesPerElement: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/bytesperelement)
- [static let bytesPerRow: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/bytesperrow)
- [static let cacheMode: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/cachemode)
- [static let elementHeight: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/elementheight)
- [static let elementWidth: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/elementwidth)
- [static let height: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/height)
- [static let offset: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/offset)
- [static let pixelFormat: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/pixelformat)
- [static let pixelSizeCastingAllowed: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/pixelsizecastingallowed)
- [static let planeBase: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/planebase)
- [static let planeBytesPerElement: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/planebytesperelement)
- [static let planeBytesPerRow: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/planebytesperrow)
- [static let planeElementHeight: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/planeelementheight)
- [static let planeElementWidth: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/planeelementwidth)
- [static let planeHeight: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/planeheight)
- [static let planeInfo: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/planeinfo)
- [static let planeOffset: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/planeoffset)
- [static let planeSize: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/planesize)
- [static let planeWidth: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/planewidth)
- [static let width: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/width)
- [static let allocSize: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/allocsize)
- [static let name: IOSurfacePropertyKey](/documentation/iosurface/iosurfacepropertykey/name)
- [IOSurfacePurgeabilityState](/documentation/iosurface/iosurfacepurgeabilitystate)

### Initializers

- [init(rawValue: UInt32)](/documentation/iosurface/iosurfacepurgeabilitystate/init(rawvalue:))

### Type Properties

- [static var purgeableEmpty: IOSurfacePurgeabilityState](/documentation/iosurface/iosurfacepurgeabilitystate/purgeableempty)
- [static var purgeableKeepCurrent: IOSurfacePurgeabilityState](/documentation/iosurface/iosurfacepurgeabilitystate/purgeablekeepcurrent)
- [static var purgeableVolatile: IOSurfacePurgeabilityState](/documentation/iosurface/iosurfacepurgeabilitystate/purgeablevolatile)

## Reference

- [IOSurface Structures](/documentation/iosurface/iosurface-structures)

### Structures

- [IOSurfaceMemoryLedgerFlags](/documentation/iosurface/iosurfacememoryledgerflags)

#### Type Properties

- [static var noFootprint: IOSurfaceMemoryLedgerFlags](/documentation/iosurface/iosurfacememoryledgerflags/nofootprint)

#### Initializers

- [init(rawValue: UInt32)](/documentation/iosurface/iosurfacememoryledgerflags/init(rawvalue:))
- [IOSurfaceRef](/documentation/iosurface/iosurfaceref)

#### Initializers

- [init(IOSurface)](/documentation/iosurface/iosurfaceref/init(_:))
- [IOSurface Constants](/documentation/iosurface/iosurface-constants)

### Constants

- [let kIOSurfaceAllocSize: CFString](/documentation/iosurface/kiosurfaceallocsize)
- [let kIOSurfaceBytesPerElement: CFString](/documentation/iosurface/kiosurfacebytesperelement)
- [let kIOSurfaceBytesPerRow: CFString](/documentation/iosurface/kiosurfacebytesperrow)
- [let kIOSurfaceCacheMode: CFString](/documentation/iosurface/kiosurfacecachemode)
- [let kIOSurfaceColorSpace: CFString](/documentation/iosurface/kiosurfacecolorspace)
- [let kIOSurfaceElementHeight: CFString](/documentation/iosurface/kiosurfaceelementheight)
- [let kIOSurfaceElementWidth: CFString](/documentation/iosurface/kiosurfaceelementwidth)
- [let kIOSurfaceHeight: CFString](/documentation/iosurface/kiosurfaceheight)
- [let kIOSurfaceICCProfile: CFString](/documentation/iosurface/kiosurfaceiccprofile)
- [let kIOSurfaceIsGlobal: CFString](/documentation/iosurface/kiosurfaceisglobal)
- [let kIOSurfaceName: CFString](/documentation/iosurface/kiosurfacename)
- [let kIOSurfaceOffset: CFString](/documentation/iosurface/kiosurfaceoffset)
- [let kIOSurfacePixelFormat: CFString](/documentation/iosurface/kiosurfacepixelformat)
- [let kIOSurfacePixelSizeCastingAllowed: CFString](/documentation/iosurface/kiosurfacepixelsizecastingallowed)
- [let kIOSurfacePlaneBase: CFString](/documentation/iosurface/kiosurfaceplanebase)
- [let kIOSurfacePlaneBitsPerElement: CFString](/documentation/iosurface/kiosurfaceplanebitsperelement)
- [let kIOSurfacePlaneBytesPerElement: CFString](/documentation/iosurface/kiosurfaceplanebytesperelement)
- [let kIOSurfacePlaneBytesPerRow: CFString](/documentation/iosurface/kiosurfaceplanebytesperrow)
- [let kIOSurfacePlaneComponentBitDepths: CFString](/documentation/iosurface/kiosurfaceplanecomponentbitdepths)
- [let kIOSurfacePlaneComponentBitOffsets: CFString](/documentation/iosurface/kiosurfaceplanecomponentbitoffsets)
- [let kIOSurfacePlaneComponentNames: CFString](/documentation/iosurface/kiosurfaceplanecomponentnames)
- [let kIOSurfacePlaneComponentRanges: CFString](/documentation/iosurface/kiosurfaceplanecomponentranges)
- [let kIOSurfacePlaneComponentTypes: CFString](/documentation/iosurface/kiosurfaceplanecomponenttypes)
- [let kIOSurfacePlaneElementHeight: CFString](/documentation/iosurface/kiosurfaceplaneelementheight)
- [let kIOSurfacePlaneElementWidth: CFString](/documentation/iosurface/kiosurfaceplaneelementwidth)
- [let kIOSurfacePlaneHeight: CFString](/documentation/iosurface/kiosurfaceplaneheight)
- [let kIOSurfacePlaneInfo: CFString](/documentation/iosurface/kiosurfaceplaneinfo)
- [let kIOSurfacePlaneOffset: CFString](/documentation/iosurface/kiosurfaceplaneoffset)
- [let kIOSurfacePlaneSize: CFString](/documentation/iosurface/kiosurfaceplanesize)
- [let kIOSurfacePlaneWidth: CFString](/documentation/iosurface/kiosurfaceplanewidth)
- [let kIOSurfaceSubsampling: CFString](/documentation/iosurface/kiosurfacesubsampling)
- [var kIOSurfaceSuccess: Int32](/documentation/iosurface/kiosurfacesuccess)
- [let kIOSurfaceWidth: CFString](/documentation/iosurface/kiosurfacewidth)
- [IOSurface Functions](/documentation/iosurface/iosurface-functions)

### Functions

- [func IOSurfaceAlignProperty(CFString, Int) -> Int](/documentation/iosurface/iosurfacealignproperty(_:_:))
- [func IOSurfaceAllowsPixelSizeCasting(IOSurfaceRef) -> Bool](/documentation/iosurface/iosurfaceallowspixelsizecasting(_:))
- [func IOSurfaceCopyAllValues(IOSurfaceRef) -> CFDictionary?](/documentation/iosurface/iosurfacecopyallvalues(_:))
- [func IOSurfaceCopyValue(IOSurfaceRef, CFString) -> CFTypeRef?](/documentation/iosurface/iosurfacecopyvalue(_:_:))
- [func IOSurfaceCreate(CFDictionary) -> IOSurfaceRef?](/documentation/iosurface/iosurfacecreate(_:))
- [func IOSurfaceCreateMachPort(IOSurfaceRef) -> mach_port_t](/documentation/iosurface/iosurfacecreatemachport(_:))
- [func IOSurfaceCreateXPCObject(IOSurfaceRef) -> xpc_object_t](/documentation/iosurface/iosurfacecreatexpcobject(_:))
- [func IOSurfaceDecrementUseCount(IOSurfaceRef)](/documentation/iosurface/iosurfacedecrementusecount(_:))
- [func IOSurfaceGetAllocSize(IOSurfaceRef) -> Int](/documentation/iosurface/iosurfacegetallocsize(_:))
- [func IOSurfaceGetBaseAddress(IOSurfaceRef) -> UnsafeMutableRawPointer](/documentation/iosurface/iosurfacegetbaseaddress(_:))
- [func IOSurfaceGetBaseAddressOfPlane(IOSurfaceRef, Int) -> UnsafeMutableRawPointer](/documentation/iosurface/iosurfacegetbaseaddressofplane(_:_:))
- [func IOSurfaceGetBitDepthOfComponentOfPlane(IOSurfaceRef, Int, Int) -> Int](/documentation/iosurface/iosurfacegetbitdepthofcomponentofplane(_:_:_:))
- [func IOSurfaceGetBitOffsetOfComponentOfPlane(IOSurfaceRef, Int, Int) -> Int](/documentation/iosurface/iosurfacegetbitoffsetofcomponentofplane(_:_:_:))
- [func IOSurfaceGetBytesPerElement(IOSurfaceRef) -> Int](/documentation/iosurface/iosurfacegetbytesperelement(_:))
- [func IOSurfaceGetBytesPerElementOfPlane(IOSurfaceRef, Int) -> Int](/documentation/iosurface/iosurfacegetbytesperelementofplane(_:_:))
- [func IOSurfaceGetBytesPerRow(IOSurfaceRef) -> Int](/documentation/iosurface/iosurfacegetbytesperrow(_:))
- [func IOSurfaceGetBytesPerRowOfPlane(IOSurfaceRef, Int) -> Int](/documentation/iosurface/iosurfacegetbytesperrowofplane(_:_:))
- [func IOSurfaceGetElementHeight(IOSurfaceRef) -> Int](/documentation/iosurface/iosurfacegetelementheight(_:))
- [func IOSurfaceGetElementHeightOfPlane(IOSurfaceRef, Int) -> Int](/documentation/iosurface/iosurfacegetelementheightofplane(_:_:))
- [func IOSurfaceGetElementWidth(IOSurfaceRef) -> Int](/documentation/iosurface/iosurfacegetelementwidth(_:))
- [func IOSurfaceGetElementWidthOfPlane(IOSurfaceRef, Int) -> Int](/documentation/iosurface/iosurfacegetelementwidthofplane(_:_:))
- [func IOSurfaceGetHeight(IOSurfaceRef) -> Int](/documentation/iosurface/iosurfacegetheight(_:))
- [func IOSurfaceGetHeightOfPlane(IOSurfaceRef, Int) -> Int](/documentation/iosurface/iosurfacegetheightofplane(_:_:))
- [func IOSurfaceGetID(IOSurfaceRef) -> IOSurfaceID](/documentation/iosurface/iosurfacegetid(_:))
- [func IOSurfaceGetNameOfComponentOfPlane(IOSurfaceRef, Int, Int) -> IOSurfaceComponentName](/documentation/iosurface/iosurfacegetnameofcomponentofplane(_:_:_:))
- [func IOSurfaceGetNumberOfComponentsOfPlane(IOSurfaceRef, Int) -> Int](/documentation/iosurface/iosurfacegetnumberofcomponentsofplane(_:_:))
- [func IOSurfaceGetPixelFormat(IOSurfaceRef) -> OSType](/documentation/iosurface/iosurfacegetpixelformat(_:))
- [func IOSurfaceGetPlaneCount(IOSurfaceRef) -> Int](/documentation/iosurface/iosurfacegetplanecount(_:))
- [func IOSurfaceGetPropertyAlignment(CFString) -> Int](/documentation/iosurface/iosurfacegetpropertyalignment(_:))
- [func IOSurfaceGetPropertyMaximum(CFString) -> Int](/documentation/iosurface/iosurfacegetpropertymaximum(_:))
- [func IOSurfaceGetRangeOfComponentOfPlane(IOSurfaceRef, Int, Int) -> IOSurfaceComponentRange](/documentation/iosurface/iosurfacegetrangeofcomponentofplane(_:_:_:))
- [func IOSurfaceGetSeed(IOSurfaceRef) -> UInt32](/documentation/iosurface/iosurfacegetseed(_:))
- [func IOSurfaceGetSubsampling(IOSurfaceRef) -> IOSurfaceSubsampling](/documentation/iosurface/iosurfacegetsubsampling(_:))
- [func IOSurfaceGetTypeID() -> CFTypeID](/documentation/iosurface/iosurfacegettypeid())
- [func IOSurfaceGetTypeOfComponentOfPlane(IOSurfaceRef, Int, Int) -> IOSurfaceComponentType](/documentation/iosurface/iosurfacegettypeofcomponentofplane(_:_:_:))
- [func IOSurfaceGetUseCount(IOSurfaceRef) -> Int32](/documentation/iosurface/iosurfacegetusecount(_:))
- [func IOSurfaceGetWidth(IOSurfaceRef) -> Int](/documentation/iosurface/iosurfacegetwidth(_:))
- [func IOSurfaceGetWidthOfPlane(IOSurfaceRef, Int) -> Int](/documentation/iosurface/iosurfacegetwidthofplane(_:_:))
- [func IOSurfaceIncrementUseCount(IOSurfaceRef)](/documentation/iosurface/iosurfaceincrementusecount(_:))
- [func IOSurfaceIsInUse(IOSurfaceRef) -> Bool](/documentation/iosurface/iosurfaceisinuse(_:))
- [func IOSurfaceLock(IOSurfaceRef, IOSurfaceLockOptions, UnsafeMutablePointer<UInt32>?) -> kern_return_t](/documentation/iosurface/iosurfacelock(_:_:_:))
- [func IOSurfaceLookup(IOSurfaceID) -> IOSurfaceRef?](/documentation/iosurface/iosurfacelookup(_:))
- [func IOSurfaceLookupFromMachPort(mach_port_t) -> IOSurfaceRef?](/documentation/iosurface/iosurfacelookupfrommachport(_:))
- [func IOSurfaceLookupFromXPCObject(xpc_object_t) -> IOSurfaceRef?](/documentation/iosurface/iosurfacelookupfromxpcobject(_:))
- [func IOSurfaceRemoveAllValues(IOSurfaceRef)](/documentation/iosurface/iosurfaceremoveallvalues(_:))
- [func IOSurfaceRemoveValue(IOSurfaceRef, CFString)](/documentation/iosurface/iosurfaceremovevalue(_:_:))
- [func IOSurfaceSetOwnershipIdentity(IOSurfaceRef, task_id_token_t, Int32, UInt32) -> kern_return_t](/documentation/iosurface/iosurfacesetownershipidentity(_:_:_:_:))
- [func IOSurfaceSetPurgeable(IOSurfaceRef, UInt32, UnsafeMutablePointer<UInt32>?) -> kern_return_t](/documentation/iosurface/iosurfacesetpurgeable(_:_:_:))
- [func IOSurfaceSetValue(IOSurfaceRef, CFString, CFTypeRef)](/documentation/iosurface/iosurfacesetvalue(_:_:_:))
- [func IOSurfaceSetValues(IOSurfaceRef, CFDictionary)](/documentation/iosurface/iosurfacesetvalues(_:_:))
- [func IOSurfaceUnlock(IOSurfaceRef, IOSurfaceLockOptions, UnsafeMutablePointer<UInt32>?) -> kern_return_t](/documentation/iosurface/iosurfaceunlock(_:_:_:))

## Variables

- [let kIOSurfaceContentHeadroom: CFString](/documentation/iosurface/kiosurfacecontentheadroom)
- [var kIOSurfaceCopybackCache: Int](/documentation/iosurface/kiosurfacecopybackcache)
- [var kIOSurfaceCopybackInnerCache: Int](/documentation/iosurface/kiosurfacecopybackinnercache)
- [var kIOSurfaceDefaultCache: Int](/documentation/iosurface/kiosurfacedefaultcache)
- [var kIOSurfaceInhibitCache: Int](/documentation/iosurface/kiosurfaceinhibitcache)
- [var kIOSurfaceMapCacheShift: Int](/documentation/iosurface/kiosurfacemapcacheshift)
- [var kIOSurfaceMapCopybackCache: Int](/documentation/iosurface/kiosurfacemapcopybackcache)
- [var kIOSurfaceMapCopybackInnerCache: Int](/documentation/iosurface/kiosurfacemapcopybackinnercache)
- [var kIOSurfaceMapDefaultCache: Int](/documentation/iosurface/kiosurfacemapdefaultcache)
- [var kIOSurfaceMapInhibitCache: Int](/documentation/iosurface/kiosurfacemapinhibitcache)
- [var kIOSurfaceMapWriteCombineCache: Int](/documentation/iosurface/kiosurfacemapwritecombinecache)
- [var kIOSurfaceMapWriteThruCache: Int](/documentation/iosurface/kiosurfacemapwritethrucache)
- [var kIOSurfaceWriteCombineCache: Int](/documentation/iosurface/kiosurfacewritecombinecache)
- [var kIOSurfaceWriteThruCache: Int](/documentation/iosurface/kiosurfacewritethrucache)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
