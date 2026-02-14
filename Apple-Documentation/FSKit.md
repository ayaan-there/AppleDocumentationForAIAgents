# FSKit Documentation

Source: https://sosumi.ai/documentation/fskit

---
title: FSKit
source: https://developer.apple.com/documentation/fskit
timestamp: 2026-02-13T18:57:13.181Z
---

## Essentials

- [Building a passthrough file system](/documentation/fskit/building-a-passthrough-file-system)

## App extensions

- [UnaryFileSystemExtension](/documentation/fskit/unaryfilesystemextension)

### Declaring the implemented file system

- [var fileSystem: Self.FileSystem](/documentation/fskit/unaryfilesystemextension/filesystem-swift.property)
- [FileSystem](/documentation/fskit/unaryfilesystemextension/filesystem-swift.associatedtype)

## File systems

- [FSUnaryFileSystem](/documentation/fskit/fsunaryfilesystem)

### Implementing operations

- [FSUnaryFileSystemOperations](/documentation/fskit/fsunaryfilesystemoperations)

#### Loading and unloading resources

- [func loadResource(resource: FSResource, options: FSTaskOptions, replyHandler: (FSVolume?, (any Error)?) -> Void)](/documentation/fskit/fsunaryfilesystemoperations/loadresource(resource:options:replyhandler:))
- [func unloadResource(resource: FSResource, options: FSTaskOptions, replyHandler: ((any Error)?) -> Void)](/documentation/fskit/fsunaryfilesystemoperations/unloadresource(resource:options:replyhandler:))
- [func didFinishLoading()](/documentation/fskit/fsunaryfilesystemoperations/didfinishloading())

#### Probing resources

- [func probeResource(resource: FSResource, replyHandler: (FSProbeResult?, (any Error)?) -> Void)](/documentation/fskit/fsunaryfilesystemoperations/proberesource(resource:replyhandler:))
- [FSProbeResult](/documentation/fskit/fsproberesult)

##### Working with results

- [class func recognized(name: String, containerID: FSContainerIdentifier) -> Self](/documentation/fskit/fsproberesult/recognized(name:containerid:))
- [class func usable(name: String, containerID: FSContainerIdentifier) -> Self](/documentation/fskit/fsproberesult/usable(name:containerid:))
- [class func usableButLimited(name: String, containerID: FSContainerIdentifier) -> Self](/documentation/fskit/fsproberesult/usablebutlimited(name:containerid:))
- [class var usableButLimited: FSProbeResult](/documentation/fskit/fsproberesult/usablebutlimited)
- [class var notRecognized: FSProbeResult](/documentation/fskit/fsproberesult/notrecognized)

##### Working with result properties

- [var containerID: FSContainerIdentifier?](/documentation/fskit/fsproberesult/containerid)
- [var name: String?](/documentation/fskit/fsproberesult/name)
- [var result: FSMatchResult](/documentation/fskit/fsproberesult/result)
- [FSMatchResult](/documentation/fskit/fsmatchresult)

###### Working with match results

- [case usable](/documentation/fskit/fsmatchresult/usable)
- [case usableButLimited](/documentation/fskit/fsmatchresult/usablebutlimited)
- [case recognized](/documentation/fskit/fsmatchresult/recognized)
- [case notRecognized](/documentation/fskit/fsmatchresult/notrecognized)

###### Working with raw values

- [init?(rawValue: Int)](/documentation/fskit/fsmatchresult/init(rawvalue:))
- [FSFileSystemBase](/documentation/fskit/fsfilesystembase)

### Implementing essential functionality

- [var containerStatus: FSContainerStatus](/documentation/fskit/fsfilesystembase/containerstatus)
- [func wipe(FSBlockDeviceResource, completionHandler: ((any Error)?) -> Void)](/documentation/fskit/fsfilesystembase/wipe(_:completionhandler:))
- [FSFileName](/documentation/fskit/fsfilename)

### Creating a filename

- [convenience init(bytes: UnsafeBufferPointer<CChar>)](/documentation/fskit/fsfilename/init(bytes:))
- [convenience init(cString: UnsafeBufferPointer<CChar>)](/documentation/fskit/fsfilename/init(cstring:))
- [convenience init(data: Data)](/documentation/fskit/fsfilename/init(data:))
- [convenience init(string: String)](/documentation/fskit/fsfilename/init(string:))

### Accessing filename properties

- [var data: Data](/documentation/fskit/fsfilename/data)
- [var string: String?](/documentation/fskit/fsfilename/string)
- [var debugDescription: String](/documentation/fskit/fsfilename/debugdescription)

## Containers

- [FSContainerIdentifier](/documentation/fskit/fscontaineridentifier)

### Accessing identifier properties

- [var volumeIdentifier: FSVolume.Identifier](/documentation/fskit/fscontaineridentifier/volumeidentifier)
- [FSContainerStatus](/documentation/fskit/fscontainerstatus)

### Creating a container status instance

- [class func active(status: any Error) -> Self](/documentation/fskit/fscontainerstatus/active(status:))
- [class func blocked(status: any Error) -> Self](/documentation/fskit/fscontainerstatus/blocked(status:))
- [class func notReady(status: any Error) -> Self](/documentation/fskit/fscontainerstatus/notready(status:))
- [class func ready(status: any Error) -> Self](/documentation/fskit/fscontainerstatus/ready(status:))

### Inspecting status properties

- [var state: FSContainerState](/documentation/fskit/fscontainerstatus/state)
- [FSContainerState](/documentation/fskit/fscontainerstate)

#### Container states

- [case notReady](/documentation/fskit/fscontainerstate/notready)
- [case blocked](/documentation/fskit/fscontainerstate/blocked)
- [case ready](/documentation/fskit/fscontainerstate/ready)
- [case active](/documentation/fskit/fscontainerstate/active)

#### Working with raw values

- [init?(rawValue: Int)](/documentation/fskit/fscontainerstate/init(rawvalue:))
- [var status: (any Error)?](/documentation/fskit/fscontainerstatus/status)

### Using common status values

- [class var active: FSContainerStatus](/documentation/fskit/fscontainerstatus/active)
- [class var ready: FSContainerStatus](/documentation/fskit/fscontainerstatus/ready)

## Resources

- [FSResource](/documentation/fskit/fsresource)

### Creating proxies

- [func makeProxy() -> Self](/documentation/fskit/fsresource/makeproxy())

### Revoking the resource

- [func revoke()](/documentation/fskit/fsresource/revoke())
- [var isRevoked: Bool](/documentation/fskit/fsresource/isrevoked)
- [FSBlockDeviceResource](/documentation/fskit/fsblockdeviceresource)

### Accessing resource properties

- [var bsdName: String](/documentation/fskit/fsblockdeviceresource/bsdname)
- [var isWritable: Bool](/documentation/fskit/fsblockdeviceresource/iswritable)
- [var blockCount: UInt64](/documentation/fskit/fsblockdeviceresource/blockcount)
- [var blockSize: UInt64](/documentation/fskit/fsblockdeviceresource/blocksize)
- [var physicalBlockSize: UInt64](/documentation/fskit/fsblockdeviceresource/physicalblocksize)

### Reading and writing data

- [func read(into: UnsafeMutableRawBufferPointer, startingAt: off_t, length: Int) throws -> Int](/documentation/fskit/fsblockdeviceresource/read(into:startingat:length:)-4ax6s)
- [func read(into: UnsafeMutableRawBufferPointer, startingAt: off_t, length: Int) async throws -> Int](/documentation/fskit/fsblockdeviceresource/read(into:startingat:length:)-5yozi)
- [func read(into: UnsafeMutableRawBufferPointer, startingAt: off_t, length: Int, completionHandler: (Int, (any Error)?) -> Void)](/documentation/fskit/fsblockdeviceresource/read(into:startingat:length:completionhandler:))
- [func write(from: UnsafeRawBufferPointer, startingAt: off_t, length: Int) throws -> Int](/documentation/fskit/fsblockdeviceresource/write(from:startingat:length:)-2fmgt)
- [func write(from: UnsafeRawBufferPointer, startingAt: off_t, length: Int) async throws -> Int](/documentation/fskit/fsblockdeviceresource/write(from:startingat:length:)-9oa1x)
- [func write(from: UnsafeRawBufferPointer, startingAt: off_t, length: Int, completionHandler: (Int, (any Error)?) -> Void)](/documentation/fskit/fsblockdeviceresource/write(from:startingat:length:completionhandler:))

### Reading and writing data with kernel buffer cache

- [func metadataRead(into: UnsafeMutableRawBufferPointer, startingAt: off_t, length: Int) throws](/documentation/fskit/fsblockdeviceresource/metadataread(into:startingat:length:))
- [func metadataWrite(from: UnsafeRawBufferPointer, startingAt: off_t, length: Int) throws](/documentation/fskit/fsblockdeviceresource/metadatawrite(from:startingat:length:))
- [func delayedMetadataWrite(from: UnsafeRawBufferPointer, startingAt: off_t, length: Int) throws](/documentation/fskit/fsblockdeviceresource/delayedmetadatawrite(from:startingat:length:))
- [func metadataFlush() throws](/documentation/fskit/fsblockdeviceresource/metadataflush())
- [func asynchronousMetadataFlush() throws](/documentation/fskit/fsblockdeviceresource/asynchronousmetadataflush())
- [func metadataClear([FSMetadataRange], withDelayedWrites: Bool) throws](/documentation/fskit/fsblockdeviceresource/metadataclear(_:withdelayedwrites:))
- [func metadataPurge([FSMetadataRange]) throws](/documentation/fskit/fsblockdeviceresource/metadatapurge(_:))
- [FSMetadataRange](/documentation/fskit/fsmetadatarange)

#### Creating a metadata range

- [init(offset: off_t, segmentLength: UInt64, segmentCount: UInt64)](/documentation/fskit/fsmetadatarange/init(offset:segmentlength:segmentcount:))

#### Accessing range properties

- [var startOffset: off_t](/documentation/fskit/fsmetadatarange/startoffset)
- [var segmentLength: UInt64](/documentation/fskit/fsmetadatarange/segmentlength)
- [var segmentCount: UInt64](/documentation/fskit/fsmetadatarange/segmentcount)
- [FSPathURLResource](/documentation/fskit/fspathurlresource)

### Creating a path URL resource

- [init(url: URL, writable: Bool)](/documentation/fskit/fspathurlresource/init(url:writable:))

### Accessing resource properties

- [var url: URL](/documentation/fskit/fspathurlresource/url)
- [var isWritable: Bool](/documentation/fskit/fspathurlresource/iswritable)
- [FSGenericURLResource](/documentation/fskit/fsgenericurlresource)

### Creating a generic URL resource

- [init(url: URL)](/documentation/fskit/fsgenericurlresource/init(url:))

### Accessing resource properties

- [var url: URL](/documentation/fskit/fsgenericurlresource/url)

## Volumes

- [FSVolume](/documentation/fskit/fsvolume)

### Creating a volume

- [init(volumeID: FSVolume.Identifier, volumeName: FSFileName)](/documentation/fskit/fsvolume/init(volumeid:volumename:))
- [FSVolume.Identifier](/documentation/fskit/fsvolume/identifier)
- [FSFileName](/documentation/fskit/fsfilename)

#### Creating a filename

- [convenience init(bytes: UnsafeBufferPointer<CChar>)](/documentation/fskit/fsfilename/init(bytes:))
- [convenience init(cString: UnsafeBufferPointer<CChar>)](/documentation/fskit/fsfilename/init(cstring:))
- [convenience init(data: Data)](/documentation/fskit/fsfilename/init(data:))
- [convenience init(string: String)](/documentation/fskit/fsfilename/init(string:))

#### Accessing filename properties

- [var data: Data](/documentation/fskit/fsfilename/data)
- [var string: String?](/documentation/fskit/fsfilename/string)
- [var debugDescription: String](/documentation/fskit/fsfilename/debugdescription)

### Accessing volume properties

- [var volumeID: FSVolume.Identifier](/documentation/fskit/fsvolume/volumeid)
- [var name: FSFileName](/documentation/fskit/fsvolume/name)

### Implementing required operations

- [FSVolume.Operations](/documentation/fskit/fsvolume/operations)

#### Handling activation and deactivation

- [func activate(options: FSTaskOptions, replyHandler: (FSItem?, (any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/activate(options:replyhandler:))
- [FSItem](/documentation/fskit/fsitem)

##### Identifying an item

- [FSItem.Identifier](/documentation/fskit/fsitem/identifier)

###### Working with special identifiers

- [case invalid](/documentation/fskit/fsitem/identifier/invalid)
- [case parentOfRoot](/documentation/fskit/fsitem/identifier/parentofroot)
- [case rootDirectory](/documentation/fskit/fsitem/identifier/rootdirectory)

###### Working with raw values

- [init?(rawValue: UInt64)](/documentation/fskit/fsitem/identifier/init(rawvalue:))
- [FSItem.ItemType](/documentation/fskit/fsitem/itemtype)

###### Working with item types

- [case file](/documentation/fskit/fsitem/itemtype/file)
- [case directory](/documentation/fskit/fsitem/itemtype/directory)
- [case symlink](/documentation/fskit/fsitem/itemtype/symlink)
- [case fifo](/documentation/fskit/fsitem/itemtype/fifo)
- [case charDevice](/documentation/fskit/fsitem/itemtype/chardevice)
- [case blockDevice](/documentation/fskit/fsitem/itemtype/blockdevice)
- [case socket](/documentation/fskit/fsitem/itemtype/socket)
- [case unknown](/documentation/fskit/fsitem/itemtype/unknown)

###### Working with raw values

- [init?(rawValue: Int)](/documentation/fskit/fsitem/itemtype/init(rawvalue:))

##### Working with attributes

- [FSItem.Attributes](/documentation/fskit/fsitem/attributes)

###### Validating and invalidating attributes

- [func isValid(FSItem.Attribute) -> Bool](/documentation/fskit/fsitem/attributes/isvalid(_:))
- [func invalidateAllProperties()](/documentation/fskit/fsitem/attributes/invalidateallproperties())

###### Working with identifier attributes

- [var fileID: FSItem.Identifier](/documentation/fskit/fsitem/attributes/fileid)
- [var parentID: FSItem.Identifier](/documentation/fskit/fsitem/attributes/parentid)

###### Working with metadata attributes

- [var type: FSItem.ItemType](/documentation/fskit/fsitem/attributes/type)
- [var mode: UInt32](/documentation/fskit/fsitem/attributes/mode)
- [var linkCount: UInt32](/documentation/fskit/fsitem/attributes/linkcount)
- [var uid: UInt32](/documentation/fskit/fsitem/attributes/uid)
- [var gid: UInt32](/documentation/fskit/fsitem/attributes/gid)
- [var flags: UInt32](/documentation/fskit/fsitem/attributes/flags)
- [var size: UInt64](/documentation/fskit/fsitem/attributes/size)
- [var allocSize: UInt64](/documentation/fskit/fsitem/attributes/allocsize)
- [var supportsLimitedXAttrs: Bool](/documentation/fskit/fsitem/attributes/supportslimitedxattrs)
- [var inhibitKernelOffloadedIO: Bool](/documentation/fskit/fsitem/attributes/inhibitkerneloffloadedio)

###### Working with time attributes

- [var accessTime: timespec](/documentation/fskit/fsitem/attributes/accesstime)
- [var modifyTime: timespec](/documentation/fskit/fsitem/attributes/modifytime)
- [var changeTime: timespec](/documentation/fskit/fsitem/attributes/changetime)
- [var birthTime: timespec](/documentation/fskit/fsitem/attributes/birthtime)
- [var backupTime: timespec](/documentation/fskit/fsitem/attributes/backuptime)
- [var addedTime: timespec](/documentation/fskit/fsitem/attributes/addedtime)
- [FSItem.GetAttributesRequest](/documentation/fskit/fsitem/getattributesrequest)

###### Inspecting requested attributes

- [var wantedAttributes: FSItem.Attribute](/documentation/fskit/fsitem/getattributesrequest/wantedattributes)
- [func isAttributeWanted(FSItem.Attribute) -> Bool](/documentation/fskit/fsitem/getattributesrequest/isattributewanted(_:))
- [FSItem.Attribute](/documentation/fskit/fsitem/attribute)

###### Working with identifier attributes

- [static var fileID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/fileid)
- [static var parentID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/parentid)

###### Working with metadata attributes

- [static var type: FSItem.Attribute](/documentation/fskit/fsitem/attribute/type)
- [static var mode: FSItem.Attribute](/documentation/fskit/fsitem/attribute/mode)
- [static var linkCount: FSItem.Attribute](/documentation/fskit/fsitem/attribute/linkcount)
- [static var uid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/uid)
- [static var gid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/gid)
- [static var flags: FSItem.Attribute](/documentation/fskit/fsitem/attribute/flags)
- [static var size: FSItem.Attribute](/documentation/fskit/fsitem/attribute/size)
- [static var allocSize: FSItem.Attribute](/documentation/fskit/fsitem/attribute/allocsize)
- [static var supportsLimitedXAttrs: FSItem.Attribute](/documentation/fskit/fsitem/attribute/supportslimitedxattrs)
- [static var inhibitKernelOffloadedIO: FSItem.Attribute](/documentation/fskit/fsitem/attribute/inhibitkerneloffloadedio)

###### Working with time attributes

- [static var accessTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/accesstime)
- [static var modifyTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/modifytime)
- [static var changeTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/changetime)
- [static var birthTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/birthtime)
- [static var backupTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/backuptime)
- [static var addedTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/addedtime)

###### Working with raw values

- [init(rawValue: Int)](/documentation/fskit/fsitem/attribute/init(rawvalue:))
- [FSItem.SetAttributesRequest](/documentation/fskit/fsitem/setattributesrequest)

###### Inspecting used attributes

- [var consumedAttributes: FSItem.Attribute](/documentation/fskit/fsitem/setattributesrequest/consumedattributes)
- [func wasAttributeConsumed(FSItem.Attribute) -> Bool](/documentation/fskit/fsitem/setattributesrequest/wasattributeconsumed(_:))
- [FSItem.Attribute](/documentation/fskit/fsitem/attribute)

###### Working with identifier attributes

- [static var fileID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/fileid)
- [static var parentID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/parentid)

###### Working with metadata attributes

- [static var type: FSItem.Attribute](/documentation/fskit/fsitem/attribute/type)
- [static var mode: FSItem.Attribute](/documentation/fskit/fsitem/attribute/mode)
- [static var linkCount: FSItem.Attribute](/documentation/fskit/fsitem/attribute/linkcount)
- [static var uid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/uid)
- [static var gid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/gid)
- [static var flags: FSItem.Attribute](/documentation/fskit/fsitem/attribute/flags)
- [static var size: FSItem.Attribute](/documentation/fskit/fsitem/attribute/size)
- [static var allocSize: FSItem.Attribute](/documentation/fskit/fsitem/attribute/allocsize)
- [static var supportsLimitedXAttrs: FSItem.Attribute](/documentation/fskit/fsitem/attribute/supportslimitedxattrs)
- [static var inhibitKernelOffloadedIO: FSItem.Attribute](/documentation/fskit/fsitem/attribute/inhibitkerneloffloadedio)

###### Working with time attributes

- [static var accessTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/accesstime)
- [static var modifyTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/modifytime)
- [static var changeTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/changetime)
- [static var birthTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/birthtime)
- [static var backupTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/backuptime)
- [static var addedTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/addedtime)

###### Working with raw values

- [init(rawValue: Int)](/documentation/fskit/fsitem/attribute/init(rawvalue:))
- [func deactivate(options: FSDeactivateOptions, replyHandler: ((any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/deactivate(options:replyhandler:))
- [FSDeactivateOptions](/documentation/fskit/fsdeactivateoptions)

##### Deactivation options

- [static var force: FSDeactivateOptions](/documentation/fskit/fsdeactivateoptions/force)

##### Working with raw values

- [init(rawValue: Int)](/documentation/fskit/fsdeactivateoptions/init(rawvalue:))

#### Mounting and unmounting

- [func mount(options: FSTaskOptions, replyHandler: ((any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/mount(options:replyhandler:))
- [func unmount(replyHandler: () -> Void)](/documentation/fskit/fsvolume/operations/unmount(replyhandler:))

#### Working with items

- [func createItem(named: FSFileName, type: FSItem.ItemType, inDirectory: FSItem, attributes: FSItem.SetAttributesRequest, replyHandler: (FSItem?, FSFileName?, (any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/createitem(named:type:indirectory:attributes:replyhandler:))
- [FSFileName](/documentation/fskit/fsfilename)

##### Creating a filename

- [convenience init(bytes: UnsafeBufferPointer<CChar>)](/documentation/fskit/fsfilename/init(bytes:))
- [convenience init(cString: UnsafeBufferPointer<CChar>)](/documentation/fskit/fsfilename/init(cstring:))
- [convenience init(data: Data)](/documentation/fskit/fsfilename/init(data:))
- [convenience init(string: String)](/documentation/fskit/fsfilename/init(string:))

##### Accessing filename properties

- [var data: Data](/documentation/fskit/fsfilename/data)
- [var string: String?](/documentation/fskit/fsfilename/string)
- [var debugDescription: String](/documentation/fskit/fsfilename/debugdescription)
- [FSItem.ItemType](/documentation/fskit/fsitem/itemtype)

##### Working with item types

- [case file](/documentation/fskit/fsitem/itemtype/file)
- [case directory](/documentation/fskit/fsitem/itemtype/directory)
- [case symlink](/documentation/fskit/fsitem/itemtype/symlink)
- [case fifo](/documentation/fskit/fsitem/itemtype/fifo)
- [case charDevice](/documentation/fskit/fsitem/itemtype/chardevice)
- [case blockDevice](/documentation/fskit/fsitem/itemtype/blockdevice)
- [case socket](/documentation/fskit/fsitem/itemtype/socket)
- [case unknown](/documentation/fskit/fsitem/itemtype/unknown)

##### Working with raw values

- [init?(rawValue: Int)](/documentation/fskit/fsitem/itemtype/init(rawvalue:))
- [FSItem.SetAttributesRequest](/documentation/fskit/fsitem/setattributesrequest)

##### Inspecting used attributes

- [var consumedAttributes: FSItem.Attribute](/documentation/fskit/fsitem/setattributesrequest/consumedattributes)
- [func wasAttributeConsumed(FSItem.Attribute) -> Bool](/documentation/fskit/fsitem/setattributesrequest/wasattributeconsumed(_:))
- [FSItem.Attribute](/documentation/fskit/fsitem/attribute)

###### Working with identifier attributes

- [static var fileID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/fileid)
- [static var parentID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/parentid)

###### Working with metadata attributes

- [static var type: FSItem.Attribute](/documentation/fskit/fsitem/attribute/type)
- [static var mode: FSItem.Attribute](/documentation/fskit/fsitem/attribute/mode)
- [static var linkCount: FSItem.Attribute](/documentation/fskit/fsitem/attribute/linkcount)
- [static var uid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/uid)
- [static var gid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/gid)
- [static var flags: FSItem.Attribute](/documentation/fskit/fsitem/attribute/flags)
- [static var size: FSItem.Attribute](/documentation/fskit/fsitem/attribute/size)
- [static var allocSize: FSItem.Attribute](/documentation/fskit/fsitem/attribute/allocsize)
- [static var supportsLimitedXAttrs: FSItem.Attribute](/documentation/fskit/fsitem/attribute/supportslimitedxattrs)
- [static var inhibitKernelOffloadedIO: FSItem.Attribute](/documentation/fskit/fsitem/attribute/inhibitkerneloffloadedio)

###### Working with time attributes

- [static var accessTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/accesstime)
- [static var modifyTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/modifytime)
- [static var changeTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/changetime)
- [static var birthTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/birthtime)
- [static var backupTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/backuptime)
- [static var addedTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/addedtime)

###### Working with raw values

- [init(rawValue: Int)](/documentation/fskit/fsitem/attribute/init(rawvalue:))
- [func lookupItem(named: FSFileName, inDirectory: FSItem, replyHandler: (FSItem?, FSFileName?, (any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/lookupitem(named:indirectory:replyhandler:))
- [func removeItem(FSItem, named: FSFileName, fromDirectory: FSItem, replyHandler: ((any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/removeitem(_:named:fromdirectory:replyhandler:))
- [func renameItem(FSItem, inDirectory: FSItem, named: FSFileName, to: FSFileName, inDirectory: FSItem, overItem: FSItem?, replyHandler: (FSFileName?, (any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/renameitem(_:indirectory:named:to:indirectory:overitem:replyhandler:))
- [func reclaimItem(FSItem, replyHandler: ((any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/reclaimitem(_:replyhandler:))

#### Working with links

- [func createLink(to: FSItem, named: FSFileName, inDirectory: FSItem, replyHandler: (FSFileName?, (any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/createlink(to:named:indirectory:replyhandler:))
- [func createSymbolicLink(named: FSFileName, inDirectory: FSItem, attributes: FSItem.SetAttributesRequest, linkContents: FSFileName, replyHandler: (FSItem?, FSFileName?, (any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/createsymboliclink(named:indirectory:attributes:linkcontents:replyhandler:))
- [func readSymbolicLink(FSItem, replyHandler: (FSFileName?, (any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/readsymboliclink(_:replyhandler:))

#### Working with attributes

- [func getAttributes(FSItem.GetAttributesRequest, of: FSItem, replyHandler: (FSItem.Attributes?, (any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/getattributes(_:of:replyhandler:))
- [FSItem.GetAttributesRequest](/documentation/fskit/fsitem/getattributesrequest)

##### Inspecting requested attributes

- [var wantedAttributes: FSItem.Attribute](/documentation/fskit/fsitem/getattributesrequest/wantedattributes)
- [func isAttributeWanted(FSItem.Attribute) -> Bool](/documentation/fskit/fsitem/getattributesrequest/isattributewanted(_:))
- [FSItem.Attribute](/documentation/fskit/fsitem/attribute)

###### Working with identifier attributes

- [static var fileID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/fileid)
- [static var parentID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/parentid)

###### Working with metadata attributes

- [static var type: FSItem.Attribute](/documentation/fskit/fsitem/attribute/type)
- [static var mode: FSItem.Attribute](/documentation/fskit/fsitem/attribute/mode)
- [static var linkCount: FSItem.Attribute](/documentation/fskit/fsitem/attribute/linkcount)
- [static var uid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/uid)
- [static var gid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/gid)
- [static var flags: FSItem.Attribute](/documentation/fskit/fsitem/attribute/flags)
- [static var size: FSItem.Attribute](/documentation/fskit/fsitem/attribute/size)
- [static var allocSize: FSItem.Attribute](/documentation/fskit/fsitem/attribute/allocsize)
- [static var supportsLimitedXAttrs: FSItem.Attribute](/documentation/fskit/fsitem/attribute/supportslimitedxattrs)
- [static var inhibitKernelOffloadedIO: FSItem.Attribute](/documentation/fskit/fsitem/attribute/inhibitkerneloffloadedio)

###### Working with time attributes

- [static var accessTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/accesstime)
- [static var modifyTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/modifytime)
- [static var changeTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/changetime)
- [static var birthTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/birthtime)
- [static var backupTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/backuptime)
- [static var addedTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/addedtime)

###### Working with raw values

- [init(rawValue: Int)](/documentation/fskit/fsitem/attribute/init(rawvalue:))
- [func setAttributes(FSItem.SetAttributesRequest, on: FSItem, replyHandler: (FSItem.Attributes?, (any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/setattributes(_:on:replyhandler:))
- [FSItem.SetAttributesRequest](/documentation/fskit/fsitem/setattributesrequest)

##### Inspecting used attributes

- [var consumedAttributes: FSItem.Attribute](/documentation/fskit/fsitem/setattributesrequest/consumedattributes)
- [func wasAttributeConsumed(FSItem.Attribute) -> Bool](/documentation/fskit/fsitem/setattributesrequest/wasattributeconsumed(_:))
- [FSItem.Attribute](/documentation/fskit/fsitem/attribute)

###### Working with identifier attributes

- [static var fileID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/fileid)
- [static var parentID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/parentid)

###### Working with metadata attributes

- [static var type: FSItem.Attribute](/documentation/fskit/fsitem/attribute/type)
- [static var mode: FSItem.Attribute](/documentation/fskit/fsitem/attribute/mode)
- [static var linkCount: FSItem.Attribute](/documentation/fskit/fsitem/attribute/linkcount)
- [static var uid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/uid)
- [static var gid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/gid)
- [static var flags: FSItem.Attribute](/documentation/fskit/fsitem/attribute/flags)
- [static var size: FSItem.Attribute](/documentation/fskit/fsitem/attribute/size)
- [static var allocSize: FSItem.Attribute](/documentation/fskit/fsitem/attribute/allocsize)
- [static var supportsLimitedXAttrs: FSItem.Attribute](/documentation/fskit/fsitem/attribute/supportslimitedxattrs)
- [static var inhibitKernelOffloadedIO: FSItem.Attribute](/documentation/fskit/fsitem/attribute/inhibitkerneloffloadedio)

###### Working with time attributes

- [static var accessTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/accesstime)
- [static var modifyTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/modifytime)
- [static var changeTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/changetime)
- [static var birthTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/birthtime)
- [static var backupTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/backuptime)
- [static var addedTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/addedtime)

###### Working with raw values

- [init(rawValue: Int)](/documentation/fskit/fsitem/attribute/init(rawvalue:))

#### Inspecting directory contents

- [func enumerateDirectory(FSItem, startingAt: FSDirectoryCookie, verifier: FSDirectoryVerifier, attributes: FSItem.GetAttributesRequest?, packer: FSDirectoryEntryPacker, replyHandler: (FSDirectoryVerifier, (any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/enumeratedirectory(_:startingat:verifier:attributes:packer:replyhandler:))
- [FSDirectoryCookie](/documentation/fskit/fsdirectorycookie)

##### Initializing a cookie

- [init(UInt64)](/documentation/fskit/fsdirectorycookie/init(_:))
- [init(rawValue: UInt64)](/documentation/fskit/fsdirectorycookie/init(rawvalue:))

##### Using defined cookie values

- [static let initial: FSDirectoryCookie](/documentation/fskit/fsdirectorycookie/initial)
- [FSDirectoryCookie](/documentation/fskit/fsdirectorycookie)

##### Initializing a cookie

- [init(UInt64)](/documentation/fskit/fsdirectorycookie/init(_:))
- [init(rawValue: UInt64)](/documentation/fskit/fsdirectorycookie/init(rawvalue:))

##### Using defined cookie values

- [static let initial: FSDirectoryCookie](/documentation/fskit/fsdirectorycookie/initial)
- [FSDirectoryVerifier](/documentation/fskit/fsdirectoryverifier)

##### Initializing a verifier

- [init(UInt64)](/documentation/fskit/fsdirectoryverifier/init(_:))
- [init(rawValue: UInt64)](/documentation/fskit/fsdirectoryverifier/init(rawvalue:))

##### Using defined verifier values

- [static let initial: FSDirectoryVerifier](/documentation/fskit/fsdirectoryverifier/initial)
- [FSDirectoryVerifier](/documentation/fskit/fsdirectoryverifier)

##### Initializing a verifier

- [init(UInt64)](/documentation/fskit/fsdirectoryverifier/init(_:))
- [init(rawValue: UInt64)](/documentation/fskit/fsdirectoryverifier/init(rawvalue:))

##### Using defined verifier values

- [static let initial: FSDirectoryVerifier](/documentation/fskit/fsdirectoryverifier/initial)
- [FSDirectoryEntryPacker](/documentation/fskit/fsdirectoryentrypacker)

##### Packing entries

- [func packEntry(name: FSFileName, itemType: FSItem.ItemType, itemID: FSItem.Identifier, nextCookie: FSDirectoryCookie, attributes: FSItem.Attributes?) -> Bool](/documentation/fskit/fsdirectoryentrypacker/packentry(name:itemtype:itemid:nextcookie:attributes:))
- [FSItem.ItemType](/documentation/fskit/fsitem/itemtype)

###### Working with item types

- [case file](/documentation/fskit/fsitem/itemtype/file)
- [case directory](/documentation/fskit/fsitem/itemtype/directory)
- [case symlink](/documentation/fskit/fsitem/itemtype/symlink)
- [case fifo](/documentation/fskit/fsitem/itemtype/fifo)
- [case charDevice](/documentation/fskit/fsitem/itemtype/chardevice)
- [case blockDevice](/documentation/fskit/fsitem/itemtype/blockdevice)
- [case socket](/documentation/fskit/fsitem/itemtype/socket)
- [case unknown](/documentation/fskit/fsitem/itemtype/unknown)

###### Working with raw values

- [init?(rawValue: Int)](/documentation/fskit/fsitem/itemtype/init(rawvalue:))
- [FSItem.Identifier](/documentation/fskit/fsitem/identifier)

###### Working with special identifiers

- [case invalid](/documentation/fskit/fsitem/identifier/invalid)
- [case parentOfRoot](/documentation/fskit/fsitem/identifier/parentofroot)
- [case rootDirectory](/documentation/fskit/fsitem/identifier/rootdirectory)

###### Working with raw values

- [init?(rawValue: UInt64)](/documentation/fskit/fsitem/identifier/init(rawvalue:))
- [FSDirectoryCookie](/documentation/fskit/fsdirectorycookie)

###### Initializing a cookie

- [init(UInt64)](/documentation/fskit/fsdirectorycookie/init(_:))
- [init(rawValue: UInt64)](/documentation/fskit/fsdirectorycookie/init(rawvalue:))

###### Using defined cookie values

- [static let initial: FSDirectoryCookie](/documentation/fskit/fsdirectorycookie/initial)
- [FSDirectoryCookie](/documentation/fskit/fsdirectorycookie)

###### Initializing a cookie

- [init(UInt64)](/documentation/fskit/fsdirectorycookie/init(_:))
- [init(rawValue: UInt64)](/documentation/fskit/fsdirectorycookie/init(rawvalue:))

###### Using defined cookie values

- [static let initial: FSDirectoryCookie](/documentation/fskit/fsdirectorycookie/initial)
- [FSItem.Attributes](/documentation/fskit/fsitem/attributes)

###### Validating and invalidating attributes

- [func isValid(FSItem.Attribute) -> Bool](/documentation/fskit/fsitem/attributes/isvalid(_:))
- [func invalidateAllProperties()](/documentation/fskit/fsitem/attributes/invalidateallproperties())

###### Working with identifier attributes

- [var fileID: FSItem.Identifier](/documentation/fskit/fsitem/attributes/fileid)
- [var parentID: FSItem.Identifier](/documentation/fskit/fsitem/attributes/parentid)

###### Working with metadata attributes

- [var type: FSItem.ItemType](/documentation/fskit/fsitem/attributes/type)
- [var mode: UInt32](/documentation/fskit/fsitem/attributes/mode)
- [var linkCount: UInt32](/documentation/fskit/fsitem/attributes/linkcount)
- [var uid: UInt32](/documentation/fskit/fsitem/attributes/uid)
- [var gid: UInt32](/documentation/fskit/fsitem/attributes/gid)
- [var flags: UInt32](/documentation/fskit/fsitem/attributes/flags)
- [var size: UInt64](/documentation/fskit/fsitem/attributes/size)
- [var allocSize: UInt64](/documentation/fskit/fsitem/attributes/allocsize)
- [var supportsLimitedXAttrs: Bool](/documentation/fskit/fsitem/attributes/supportslimitedxattrs)
- [var inhibitKernelOffloadedIO: Bool](/documentation/fskit/fsitem/attributes/inhibitkerneloffloadedio)

###### Working with time attributes

- [var accessTime: timespec](/documentation/fskit/fsitem/attributes/accesstime)
- [var modifyTime: timespec](/documentation/fskit/fsitem/attributes/modifytime)
- [var changeTime: timespec](/documentation/fskit/fsitem/attributes/changetime)
- [var birthTime: timespec](/documentation/fskit/fsitem/attributes/birthtime)
- [var backupTime: timespec](/documentation/fskit/fsitem/attributes/backuptime)
- [var addedTime: timespec](/documentation/fskit/fsitem/attributes/addedtime)

#### Synchronizing with a resource

- [func synchronize(flags: FSSyncFlags, replyHandler: ((any Error)?) -> Void)](/documentation/fskit/fsvolume/operations/synchronize(flags:replyhandler:))
- [FSSyncFlags](/documentation/fskit/fssyncflags)

##### Declaring synchronization behaviors

- [case wait](/documentation/fskit/fssyncflags/wait)
- [case noWait](/documentation/fskit/fssyncflags/nowait)
- [case dWait](/documentation/fskit/fssyncflags/dwait)

##### Initializers

- [init?(rawValue: Int)](/documentation/fskit/fssyncflags/init(rawvalue:))

#### Inspecting volume properties

- [var supportedVolumeCapabilities: FSVolume.SupportedCapabilities](/documentation/fskit/fsvolume/operations/supportedvolumecapabilities)
- [FSVolume.SupportedCapabilities](/documentation/fskit/fsvolume/supportedcapabilities)

##### Declaring identifier capabilities

- [var supportsPersistentObjectIDs: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supportspersistentobjectids)
- [var supports64BitObjectIDs: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supports64bitobjectids)
- [var supportsDocumentID: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supportsdocumentid)

##### Declaring linking capabilities

- [var supportsSymbolicLinks: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supportssymboliclinks)
- [var supportsHardLinks: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supportshardlinks)

##### Declaring journaling capabilities

- [var supportsJournal: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supportsjournal)
- [var supportsActiveJournal: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supportsactivejournal)

##### Declaring root capabilites

- [var doesNotSupportRootTimes: Bool](/documentation/fskit/fsvolume/supportedcapabilities/doesnotsupportroottimes)

##### Declaring file capabilities

- [var supportsSparseFiles: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supportssparsefiles)
- [var supportsZeroRuns: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supportszeroruns)
- [var supportsFastStatFS: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supportsfaststatfs)
- [var supports2TBFiles: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supports2tbfiles)
- [var supportsOpenDenyModes: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supportsopendenymodes)
- [var supportsHiddenFiles: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supportshiddenfiles)
- [var doesNotSupportImmutableFiles: Bool](/documentation/fskit/fsvolume/supportedcapabilities/doesnotsupportimmutablefiles)
- [var doesNotSupportSettingFilePermissions: Bool](/documentation/fskit/fsvolume/supportedcapabilities/doesnotsupportsettingfilepermissions)

##### Declaring volume capabilities

- [var supportsSharedSpace: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supportssharedspace)
- [var supportsVolumeGroups: Bool](/documentation/fskit/fsvolume/supportedcapabilities/supportsvolumegroups)
- [var doesNotSupportVolumeSizes: Bool](/documentation/fskit/fsvolume/supportedcapabilities/doesnotsupportvolumesizes)

##### Working with case sensitivity

- [var caseFormat: FSVolume.CaseFormat](/documentation/fskit/fsvolume/supportedcapabilities/caseformat)
- [FSVolume.CaseFormat](/documentation/fskit/fsvolume/caseformat)

###### Declaring case formats

- [case sensitive](/documentation/fskit/fsvolume/caseformat/sensitive)
- [case insensitive](/documentation/fskit/fsvolume/caseformat/insensitive)
- [case insensitiveCasePreserving](/documentation/fskit/fsvolume/caseformat/insensitivecasepreserving)

###### Initializers

- [init?(rawValue: Int)](/documentation/fskit/fsvolume/caseformat/init(rawvalue:))
- [var volumeStatistics: FSStatFSResult](/documentation/fskit/fsvolume/operations/volumestatistics)
- [FSStatFSResult](/documentation/fskit/fsstatfsresult)

##### Initializers

- [init(fileSystemTypeName: String)](/documentation/fskit/fsstatfsresult/init(filesystemtypename:))

##### Instance Properties

- [var availableBlocks: UInt64](/documentation/fskit/fsstatfsresult/availableblocks)
- [var availableBytes: UInt64](/documentation/fskit/fsstatfsresult/availablebytes)
- [var blockSize: Int](/documentation/fskit/fsstatfsresult/blocksize)
- [var fileSystemSubType: Int](/documentation/fskit/fsstatfsresult/filesystemsubtype)
- [var fileSystemTypeName: String](/documentation/fskit/fsstatfsresult/filesystemtypename)
- [var freeBlocks: UInt64](/documentation/fskit/fsstatfsresult/freeblocks)
- [var freeBytes: UInt64](/documentation/fskit/fsstatfsresult/freebytes)
- [var freeFiles: UInt64](/documentation/fskit/fsstatfsresult/freefiles)
- [var ioSize: Int](/documentation/fskit/fsstatfsresult/iosize)
- [var totalBlocks: UInt64](/documentation/fskit/fsstatfsresult/totalblocks)
- [var totalBytes: UInt64](/documentation/fskit/fsstatfsresult/totalbytes)
- [var totalFiles: UInt64](/documentation/fskit/fsstatfsresult/totalfiles)
- [var usedBlocks: UInt64](/documentation/fskit/fsstatfsresult/usedblocks)
- [var usedBytes: UInt64](/documentation/fskit/fsstatfsresult/usedbytes)

#### Instance Properties

- [var enableOpenUnlinkEmulation: Bool](/documentation/fskit/fsvolume/operations/enableopenunlinkemulation)
- [FSVolume.PathConfOperations](/documentation/fskit/fsvolume/pathconfoperations)

#### Checking limits and configurations

- [var maximumLinkCount: Int](/documentation/fskit/fsvolume/pathconfoperations/maximumlinkcount)
- [var maximumNameLength: Int](/documentation/fskit/fsvolume/pathconfoperations/maximumnamelength)
- [var restrictsOwnershipChanges: Bool](/documentation/fskit/fsvolume/pathconfoperations/restrictsownershipchanges)
- [var truncatesLongNames: Bool](/documentation/fskit/fsvolume/pathconfoperations/truncateslongnames)
- [var maximumFileSize: UInt64](/documentation/fskit/fsvolume/pathconfoperations/maximumfilesize)
- [var maximumFileSizeInBits: Int](/documentation/fskit/fsvolume/pathconfoperations/maximumfilesizeinbits)
- [var maximumXattrSize: Int](/documentation/fskit/fsvolume/pathconfoperations/maximumxattrsize)
- [var maximumXattrSizeInBits: Int](/documentation/fskit/fsvolume/pathconfoperations/maximumxattrsizeinbits)

### Implementing optional operations

- [FSVolume.OpenCloseOperations](/documentation/fskit/fsvolume/opencloseoperations)

#### Opening and closing

- [func openItem(FSItem, modes: FSVolume.OpenModes, replyHandler: ((any Error)?) -> Void)](/documentation/fskit/fsvolume/opencloseoperations/openitem(_:modes:replyhandler:))
- [func closeItem(FSItem, modes: FSVolume.OpenModes, replyHandler: ((any Error)?) -> Void)](/documentation/fskit/fsvolume/opencloseoperations/closeitem(_:modes:replyhandler:))
- [FSVolume.OpenModes](/documentation/fskit/fsvolume/openmodes)

##### Declaring open modes

- [static var read: FSVolume.OpenModes](/documentation/fskit/fsvolume/openmodes/read)
- [static var write: FSVolume.OpenModes](/documentation/fskit/fsvolume/openmodes/write)

##### Working with raw values

- [init(rawValue: UInt)](/documentation/fskit/fsvolume/openmodes/init(rawvalue:))

#### Inspecting volume properties

- [var isOpenCloseInhibited: Bool](/documentation/fskit/fsvolume/opencloseoperations/isopencloseinhibited)
- [FSVolume.ReadWriteOperations](/documentation/fskit/fsvolume/readwriteoperations)

#### Reading and writing

- [func read(from: FSItem, at: off_t, length: Int, into: FSMutableFileDataBuffer, replyHandler: (Int, (any Error)?) -> Void)](/documentation/fskit/fsvolume/readwriteoperations/read(from:at:length:into:replyhandler:))
- [FSMutableFileDataBuffer](/documentation/fskit/fsmutablefiledatabuffer)

##### Accessing buffer properties

- [func withUnsafeMutableBytes<R, E>((UnsafeMutableRawBufferPointer) throws(E) -> R) throws(E) -> R](/documentation/fskit/fsmutablefiledatabuffer/withunsafemutablebytes(_:))
- [var length: Int](/documentation/fskit/fsmutablefiledatabuffer/length)
- [func write(contents: Data, to: FSItem, at: off_t, replyHandler: (Int, (any Error)?) -> Void)](/documentation/fskit/fsvolume/readwriteoperations/write(contents:to:at:replyhandler:))
- [FSVolume.AccessCheckOperations](/documentation/fskit/fsvolume/accesscheckoperations)

#### Checking access

- [func checkAccess(to: FSItem, requestedAccess: FSVolume.AccessMask, replyHandler: (Bool, (any Error)?) -> Void)](/documentation/fskit/fsvolume/accesscheckoperations/checkaccess(to:requestedaccess:replyhandler:))
- [FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask)

##### Declaring read and write access

- [static var readData: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/readdata)
- [static var writeData: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/writedata)

##### Declaring directory access

- [static var listDirectory: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/listdirectory)
- [static var addFile: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/addfile)
- [static var addSubdirectory: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/addsubdirectory)
- [static var deleteChild: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/deletechild)
- [static var search: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/search)

##### Declaring file maniulation access

- [static var execute: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/execute)
- [static var delete: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/delete)
- [static var appendData: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/appenddata)

##### Declaring attribute access

- [static var readAttributes: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/readattributes)
- [static var writeAttributes: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/writeattributes)
- [static var readXattr: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/readxattr)
- [static var writeXattr: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/writexattr)
- [static var readSecurity: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/readsecurity)
- [static var writeSecurity: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/writesecurity)

##### Ownership access

- [static var takeOwnership: FSVolume.AccessMask](/documentation/fskit/fsvolume/accessmask/takeownership)

##### Working with raw values

- [init(rawValue: UInt)](/documentation/fskit/fsvolume/accessmask/init(rawvalue:))

#### Inspecting volume properties

- [var isAccessCheckInhibited: Bool](/documentation/fskit/fsvolume/accesscheckoperations/isaccesscheckinhibited)
- [FSVolume.RenameOperations](/documentation/fskit/fsvolume/renameoperations)

#### Renaming the volume

- [func setVolumeName(FSFileName, replyHandler: (FSFileName?, (any Error)?) -> Void)](/documentation/fskit/fsvolume/renameoperations/setvolumename(_:replyhandler:))

#### Inspecting volume properties

- [var isVolumeRenameInhibited: Bool](/documentation/fskit/fsvolume/renameoperations/isvolumerenameinhibited)
- [FSVolumeKernelOffloadedIOOperations](/documentation/fskit/fsvolumekerneloffloadediooperations)

#### Performing mapped I/O

- [func blockmapFile(FSItem, offset: off_t, length: Int, flags: FSBlockmapFlags, operationID: FSOperationID, packer: FSExtentPacker, replyHandler: ((any Error)?) -> Void)](/documentation/fskit/fsvolumekerneloffloadediooperations/blockmapfile(_:offset:length:flags:operationid:packer:replyhandler:))
- [FSBlockmapFlags](/documentation/fskit/fsblockmapflags)

##### Declaring block map behaviors

- [static var read: FSBlockmapFlags](/documentation/fskit/fsblockmapflags/read)
- [static var write: FSBlockmapFlags](/documentation/fskit/fsblockmapflags/write)

##### Working with raw values

- [init(rawValue: UInt)](/documentation/fskit/fsblockmapflags/init(rawvalue:))
- [func completeIO(for: FSItem, offset: off_t, length: Int, status: any Error, flags: FSCompleteIOFlags, operationID: FSOperationID, replyHandler: ((any Error)?) -> Void)](/documentation/fskit/fsvolumekerneloffloadediooperations/completeio(for:offset:length:status:flags:operationid:replyhandler:))
- [FSCompleteIOFlags](/documentation/fskit/fscompleteioflags)

##### Declaring I/O completion behaviors

- [static var read: FSCompleteIOFlags](/documentation/fskit/fscompleteioflags/read)
- [static var write: FSCompleteIOFlags](/documentation/fskit/fscompleteioflags/write)
- [static var async: FSCompleteIOFlags](/documentation/fskit/fscompleteioflags/async)

##### Working with raw values

- [init(rawValue: UInt)](/documentation/fskit/fscompleteioflags/init(rawvalue:))

#### Working with items

- [func createFile(name: FSFileName, in: FSItem, attributes: FSItem.SetAttributesRequest, packer: FSExtentPacker, replyHandler: (FSItem?, FSFileName?, (any Error)?) -> Void)](/documentation/fskit/fsvolumekerneloffloadediooperations/createfile(name:in:attributes:packer:replyhandler:))
- [FSItem.SetAttributesRequest](/documentation/fskit/fsitem/setattributesrequest)

##### Inspecting used attributes

- [var consumedAttributes: FSItem.Attribute](/documentation/fskit/fsitem/setattributesrequest/consumedattributes)
- [func wasAttributeConsumed(FSItem.Attribute) -> Bool](/documentation/fskit/fsitem/setattributesrequest/wasattributeconsumed(_:))
- [FSItem.Attribute](/documentation/fskit/fsitem/attribute)

###### Working with identifier attributes

- [static var fileID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/fileid)
- [static var parentID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/parentid)

###### Working with metadata attributes

- [static var type: FSItem.Attribute](/documentation/fskit/fsitem/attribute/type)
- [static var mode: FSItem.Attribute](/documentation/fskit/fsitem/attribute/mode)
- [static var linkCount: FSItem.Attribute](/documentation/fskit/fsitem/attribute/linkcount)
- [static var uid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/uid)
- [static var gid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/gid)
- [static var flags: FSItem.Attribute](/documentation/fskit/fsitem/attribute/flags)
- [static var size: FSItem.Attribute](/documentation/fskit/fsitem/attribute/size)
- [static var allocSize: FSItem.Attribute](/documentation/fskit/fsitem/attribute/allocsize)
- [static var supportsLimitedXAttrs: FSItem.Attribute](/documentation/fskit/fsitem/attribute/supportslimitedxattrs)
- [static var inhibitKernelOffloadedIO: FSItem.Attribute](/documentation/fskit/fsitem/attribute/inhibitkerneloffloadedio)

###### Working with time attributes

- [static var accessTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/accesstime)
- [static var modifyTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/modifytime)
- [static var changeTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/changetime)
- [static var birthTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/birthtime)
- [static var backupTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/backuptime)
- [static var addedTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/addedtime)

###### Working with raw values

- [init(rawValue: Int)](/documentation/fskit/fsitem/attribute/init(rawvalue:))
- [func lookupItem(name: FSFileName, in: FSItem, packer: FSExtentPacker, replyHandler: (FSItem?, FSFileName?, (any Error)?) -> Void)](/documentation/fskit/fsvolumekerneloffloadediooperations/lookupitem(name:in:packer:replyhandler:))
- [func preallocateSpace(for: FSItem, at: off_t, length: Int, flags: FSVolume.PreallocateFlags, packer: FSExtentPacker, replyHandler: (Int, (any Error)?) -> Void)](/documentation/fskit/fsvolumekerneloffloadediooperations/preallocatespace(for:at:length:flags:packer:replyhandler:))
- [FSVolume.PreallocateFlags](/documentation/fskit/fsvolume/preallocateflags)

##### Declaring preallocation behaviors

- [static var contiguous: FSVolume.PreallocateFlags](/documentation/fskit/fsvolume/preallocateflags/contiguous)
- [static var all: FSVolume.PreallocateFlags](/documentation/fskit/fsvolume/preallocateflags/all)
- [static var persist: FSVolume.PreallocateFlags](/documentation/fskit/fsvolume/preallocateflags/persist)
- [static var fromEOF: FSVolume.PreallocateFlags](/documentation/fskit/fsvolume/preallocateflags/fromeof)

##### Working with raw values

- [init(rawValue: UInt)](/documentation/fskit/fsvolume/preallocateflags/init(rawvalue:))

#### Mapping file extents

- [FSExtentPacker](/documentation/fskit/fsextentpacker)

##### Packing extents

- [func packExtent(resource: FSBlockDeviceResource, type: FSExtentType, logicalOffset: off_t, physicalOffset: off_t, length: Int) -> Bool](/documentation/fskit/fsextentpacker/packextent(resource:type:logicaloffset:physicaloffset:length:))
- [FSExtentType](/documentation/fskit/fsextenttype)

###### Working with extent types

- [case data](/documentation/fskit/fsextenttype/data)
- [case zeroFill](/documentation/fskit/fsextenttype/zerofill)

###### Working with raw values

- [init?(rawValue: Int)](/documentation/fskit/fsextenttype/init(rawvalue:))
- [FSVolume.PreallocateOperations](/documentation/fskit/fsvolume/preallocateoperations)

#### Preallocating space

- [func preallocateSpace(for: FSItem, at: off_t, length: Int, flags: FSVolume.PreallocateFlags, replyHandler: (Int, (any Error)?) -> Void)](/documentation/fskit/fsvolume/preallocateoperations/preallocatespace(for:at:length:flags:replyhandler:))
- [FSVolume.PreallocateFlags](/documentation/fskit/fsvolume/preallocateflags)

##### Declaring preallocation behaviors

- [static var contiguous: FSVolume.PreallocateFlags](/documentation/fskit/fsvolume/preallocateflags/contiguous)
- [static var all: FSVolume.PreallocateFlags](/documentation/fskit/fsvolume/preallocateflags/all)
- [static var persist: FSVolume.PreallocateFlags](/documentation/fskit/fsvolume/preallocateflags/persist)
- [static var fromEOF: FSVolume.PreallocateFlags](/documentation/fskit/fsvolume/preallocateflags/fromeof)

##### Working with raw values

- [init(rawValue: UInt)](/documentation/fskit/fsvolume/preallocateflags/init(rawvalue:))

#### Inspecting volume properties

- [var isPreallocateInhibited: Bool](/documentation/fskit/fsvolume/preallocateoperations/ispreallocateinhibited)
- [FSVolume.XattrOperations](/documentation/fskit/fsvolume/xattroperations)

#### Reading and writing

- [func getXattr(named: FSFileName, of: FSItem, replyHandler: (Data?, (any Error)?) -> Void)](/documentation/fskit/fsvolume/xattroperations/getxattr(named:of:replyhandler:))
- [func listXattrs(of: FSItem, replyHandler: ([FSFileName]?, (any Error)?) -> Void)](/documentation/fskit/fsvolume/xattroperations/listxattrs(of:replyhandler:))
- [func setXattr(named: FSFileName, to: Data?, on: FSItem, policy: FSVolume.SetXattrPolicy, replyHandler: ((any Error)?) -> Void)](/documentation/fskit/fsvolume/xattroperations/setxattr(named:to:on:policy:replyhandler:))
- [FSVolume.SetXattrPolicy](/documentation/fskit/fsvolume/setxattrpolicy)

##### Declaring a policy

- [case alwaysSet](/documentation/fskit/fsvolume/setxattrpolicy/alwaysset)
- [case mustCreate](/documentation/fskit/fsvolume/setxattrpolicy/mustcreate)
- [case mustReplace](/documentation/fskit/fsvolume/setxattrpolicy/mustreplace)
- [case delete](/documentation/fskit/fsvolume/setxattrpolicy/delete)

##### Initializers

- [init?(rawValue: UInt)](/documentation/fskit/fsvolume/setxattrpolicy/init(rawvalue:))
- [func supportedXattrNames(for: FSItem) -> [FSFileName]](/documentation/fskit/fsvolume/xattroperations/supportedxattrnames(for:))

#### Inspecting volume properties

- [var xattrOperationsInhibited: Bool](/documentation/fskit/fsvolume/xattroperations/xattroperationsinhibited)
- [FSVolume.ItemDeactivation](/documentation/fskit/fsvolume/itemdeactivation)

#### Deactivating an item

- [func deactivateItem(FSItem, replyHandler: ((any Error)?) -> Void)](/documentation/fskit/fsvolume/itemdeactivation/deactivateitem(_:replyhandler:))

#### Setting deactivation policy

- [var itemDeactivationPolicy: FSVolume.ItemDeactivationOptions](/documentation/fskit/fsvolume/itemdeactivation/itemdeactivationpolicy)
- [FSVolume.ItemDeactivationOptions](/documentation/fskit/fsvolume/itemdeactivationoptions)

##### Declaring deactivation options

- [static var forRemovedItems: FSVolume.ItemDeactivationOptions](/documentation/fskit/fsvolume/itemdeactivationoptions/forremoveditems)
- [static var forPreallocatedItems: FSVolume.ItemDeactivationOptions](/documentation/fskit/fsvolume/itemdeactivationoptions/forpreallocateditems)
- [static var always: FSVolume.ItemDeactivationOptions](/documentation/fskit/fsvolume/itemdeactivationoptions/always)

##### Working with raw values

- [init(rawValue: UInt)](/documentation/fskit/fsvolume/itemdeactivationoptions/init(rawvalue:))

## Items

- [FSItem](/documentation/fskit/fsitem)

### Identifying an item

- [FSItem.Identifier](/documentation/fskit/fsitem/identifier)

#### Working with special identifiers

- [case invalid](/documentation/fskit/fsitem/identifier/invalid)
- [case parentOfRoot](/documentation/fskit/fsitem/identifier/parentofroot)
- [case rootDirectory](/documentation/fskit/fsitem/identifier/rootdirectory)

#### Working with raw values

- [init?(rawValue: UInt64)](/documentation/fskit/fsitem/identifier/init(rawvalue:))
- [FSItem.ItemType](/documentation/fskit/fsitem/itemtype)

#### Working with item types

- [case file](/documentation/fskit/fsitem/itemtype/file)
- [case directory](/documentation/fskit/fsitem/itemtype/directory)
- [case symlink](/documentation/fskit/fsitem/itemtype/symlink)
- [case fifo](/documentation/fskit/fsitem/itemtype/fifo)
- [case charDevice](/documentation/fskit/fsitem/itemtype/chardevice)
- [case blockDevice](/documentation/fskit/fsitem/itemtype/blockdevice)
- [case socket](/documentation/fskit/fsitem/itemtype/socket)
- [case unknown](/documentation/fskit/fsitem/itemtype/unknown)

#### Working with raw values

- [init?(rawValue: Int)](/documentation/fskit/fsitem/itemtype/init(rawvalue:))

### Working with attributes

- [FSItem.Attributes](/documentation/fskit/fsitem/attributes)

#### Validating and invalidating attributes

- [func isValid(FSItem.Attribute) -> Bool](/documentation/fskit/fsitem/attributes/isvalid(_:))
- [func invalidateAllProperties()](/documentation/fskit/fsitem/attributes/invalidateallproperties())

#### Working with identifier attributes

- [var fileID: FSItem.Identifier](/documentation/fskit/fsitem/attributes/fileid)
- [var parentID: FSItem.Identifier](/documentation/fskit/fsitem/attributes/parentid)

#### Working with metadata attributes

- [var type: FSItem.ItemType](/documentation/fskit/fsitem/attributes/type)
- [var mode: UInt32](/documentation/fskit/fsitem/attributes/mode)
- [var linkCount: UInt32](/documentation/fskit/fsitem/attributes/linkcount)
- [var uid: UInt32](/documentation/fskit/fsitem/attributes/uid)
- [var gid: UInt32](/documentation/fskit/fsitem/attributes/gid)
- [var flags: UInt32](/documentation/fskit/fsitem/attributes/flags)
- [var size: UInt64](/documentation/fskit/fsitem/attributes/size)
- [var allocSize: UInt64](/documentation/fskit/fsitem/attributes/allocsize)
- [var supportsLimitedXAttrs: Bool](/documentation/fskit/fsitem/attributes/supportslimitedxattrs)
- [var inhibitKernelOffloadedIO: Bool](/documentation/fskit/fsitem/attributes/inhibitkerneloffloadedio)

#### Working with time attributes

- [var accessTime: timespec](/documentation/fskit/fsitem/attributes/accesstime)
- [var modifyTime: timespec](/documentation/fskit/fsitem/attributes/modifytime)
- [var changeTime: timespec](/documentation/fskit/fsitem/attributes/changetime)
- [var birthTime: timespec](/documentation/fskit/fsitem/attributes/birthtime)
- [var backupTime: timespec](/documentation/fskit/fsitem/attributes/backuptime)
- [var addedTime: timespec](/documentation/fskit/fsitem/attributes/addedtime)
- [FSItem.GetAttributesRequest](/documentation/fskit/fsitem/getattributesrequest)

#### Inspecting requested attributes

- [var wantedAttributes: FSItem.Attribute](/documentation/fskit/fsitem/getattributesrequest/wantedattributes)
- [func isAttributeWanted(FSItem.Attribute) -> Bool](/documentation/fskit/fsitem/getattributesrequest/isattributewanted(_:))
- [FSItem.Attribute](/documentation/fskit/fsitem/attribute)

##### Working with identifier attributes

- [static var fileID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/fileid)
- [static var parentID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/parentid)

##### Working with metadata attributes

- [static var type: FSItem.Attribute](/documentation/fskit/fsitem/attribute/type)
- [static var mode: FSItem.Attribute](/documentation/fskit/fsitem/attribute/mode)
- [static var linkCount: FSItem.Attribute](/documentation/fskit/fsitem/attribute/linkcount)
- [static var uid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/uid)
- [static var gid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/gid)
- [static var flags: FSItem.Attribute](/documentation/fskit/fsitem/attribute/flags)
- [static var size: FSItem.Attribute](/documentation/fskit/fsitem/attribute/size)
- [static var allocSize: FSItem.Attribute](/documentation/fskit/fsitem/attribute/allocsize)
- [static var supportsLimitedXAttrs: FSItem.Attribute](/documentation/fskit/fsitem/attribute/supportslimitedxattrs)
- [static var inhibitKernelOffloadedIO: FSItem.Attribute](/documentation/fskit/fsitem/attribute/inhibitkerneloffloadedio)

##### Working with time attributes

- [static var accessTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/accesstime)
- [static var modifyTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/modifytime)
- [static var changeTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/changetime)
- [static var birthTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/birthtime)
- [static var backupTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/backuptime)
- [static var addedTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/addedtime)

##### Working with raw values

- [init(rawValue: Int)](/documentation/fskit/fsitem/attribute/init(rawvalue:))
- [FSItem.SetAttributesRequest](/documentation/fskit/fsitem/setattributesrequest)

#### Inspecting used attributes

- [var consumedAttributes: FSItem.Attribute](/documentation/fskit/fsitem/setattributesrequest/consumedattributes)
- [func wasAttributeConsumed(FSItem.Attribute) -> Bool](/documentation/fskit/fsitem/setattributesrequest/wasattributeconsumed(_:))
- [FSItem.Attribute](/documentation/fskit/fsitem/attribute)

##### Working with identifier attributes

- [static var fileID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/fileid)
- [static var parentID: FSItem.Attribute](/documentation/fskit/fsitem/attribute/parentid)

##### Working with metadata attributes

- [static var type: FSItem.Attribute](/documentation/fskit/fsitem/attribute/type)
- [static var mode: FSItem.Attribute](/documentation/fskit/fsitem/attribute/mode)
- [static var linkCount: FSItem.Attribute](/documentation/fskit/fsitem/attribute/linkcount)
- [static var uid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/uid)
- [static var gid: FSItem.Attribute](/documentation/fskit/fsitem/attribute/gid)
- [static var flags: FSItem.Attribute](/documentation/fskit/fsitem/attribute/flags)
- [static var size: FSItem.Attribute](/documentation/fskit/fsitem/attribute/size)
- [static var allocSize: FSItem.Attribute](/documentation/fskit/fsitem/attribute/allocsize)
- [static var supportsLimitedXAttrs: FSItem.Attribute](/documentation/fskit/fsitem/attribute/supportslimitedxattrs)
- [static var inhibitKernelOffloadedIO: FSItem.Attribute](/documentation/fskit/fsitem/attribute/inhibitkerneloffloadedio)

##### Working with time attributes

- [static var accessTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/accesstime)
- [static var modifyTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/modifytime)
- [static var changeTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/changetime)
- [static var birthTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/birthtime)
- [static var backupTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/backuptime)
- [static var addedTime: FSItem.Attribute](/documentation/fskit/fsitem/attribute/addedtime)

##### Working with raw values

- [init(rawValue: Int)](/documentation/fskit/fsitem/attribute/init(rawvalue:))

## Maintenance and management

- [FSManageableResourceMaintenanceOperations](/documentation/fskit/fsmanageableresourcemaintenanceoperations)

### Checking the file system

- [func startCheck(task: FSTask, options: FSTaskOptions) throws -> Progress](/documentation/fskit/fsmanageableresourcemaintenanceoperations/startcheck(task:options:))

### Formatting the file system

- [func startFormat(task: FSTask, options: FSTaskOptions) throws -> Progress](/documentation/fskit/fsmanageableresourcemaintenanceoperations/startformat(task:options:))

## Operations

- [FSOperationID](/documentation/fskit/fsoperationid)

### Creating an operation ID

- [init(Int)](/documentation/fskit/fsoperationid/init(_:))

### Working with defined operations

- [static let unspecified: FSOperationID](/documentation/fskit/fsoperationid/unspecified)

### Working with raw values

- [init(rawValue: Int)](/documentation/fskit/fsoperationid/init(rawvalue:))

## Tasks

- [FSTask](/documentation/fskit/fstask)

### Logging

- [func logMessage(String)](/documentation/fskit/fstask/logmessage(_:))

### Sending completion messages

- [func didComplete(error: (any Error)?)](/documentation/fskit/fstask/didcomplete(error:))

### Handling task cancellation

- [var cancellationHandler: (() -> (any Error)?)?](/documentation/fskit/fstask/cancellationhandler)
- [FSTaskOptions](/documentation/fskit/fstaskoptions)

### Retrieving task options

- [var taskOptions: [String]](/documentation/fskit/fstaskoptions/taskoptions)

### Retrieving task option URLs

- [func url(forOption: String) -> URL?](/documentation/fskit/fstaskoptions/url(foroption:))

## Errors and logging

- [func fs_errorForCocoaError(Int32) -> any Error](/documentation/fskit/fs_errorforcocoaerror(_:))
- [func fs_errorForMachError(Int32) -> any Error](/documentation/fskit/fs_errorformacherror(_:))
- [func fs_errorForPOSIXError(Int32) -> any Error](/documentation/fskit/fs_errorforposixerror(_:))
- [FSError](/documentation/fskit/fserror)

### Identifying errors

- [static var invalidDirectoryCookie: FSError.Code](/documentation/fskit/fserror/invaliddirectorycookie)
- [static var moduleLoadFailed: FSError.Code](/documentation/fskit/fserror/moduleloadfailed)
- [static var resourceDamaged: FSError.Code](/documentation/fskit/fserror/resourcedamaged)
- [static var resourceUnrecognized: FSError.Code](/documentation/fskit/fserror/resourceunrecognized)
- [static var resourceUnusable: FSError.Code](/documentation/fskit/fserror/resourceunusable)
- [static var statusOperationInProgress: FSError.Code](/documentation/fskit/fserror/statusoperationinprogress)
- [static var statusOperationPaused: FSError.Code](/documentation/fskit/fserror/statusoperationpaused)

### Identifying the error domain

- [static var errorDomain: String](/documentation/fskit/fserror/errordomain)
- [FSError.Code](/documentation/fskit/fserror/code)

### Identifying errors

- [case invalidDirectoryCookie](/documentation/fskit/fserror/code/invaliddirectorycookie)
- [case moduleLoadFailed](/documentation/fskit/fserror/code/moduleloadfailed)
- [case resourceDamaged](/documentation/fskit/fserror/code/resourcedamaged)
- [case resourceUnrecognized](/documentation/fskit/fserror/code/resourceunrecognized)
- [case resourceUnusable](/documentation/fskit/fserror/code/resourceunusable)
- [case statusOperationInProgress](/documentation/fskit/fserror/code/statusoperationinprogress)
- [case statusOperationPaused](/documentation/fskit/fserror/code/statusoperationpaused)

### Working with raw values

- [init?(rawValue: Int)](/documentation/fskit/fserror/code/init(rawvalue:))
- [let FSKitErrorDomain: String](/documentation/fskit/fskiterrordomain)

## FSKit interactions

- [FSClient](/documentation/fskit/fsclient)

### Obtaining the shared instance

- [class var shared: FSClient](/documentation/fskit/fsclient/shared)

### Discovering installed extensions

- [func fetchInstalledExtensions(completionHandler: ([FSModuleIdentity]?, (any Error)?) -> Void)](/documentation/fskit/fsclient/fetchinstalledextensions(completionhandler:))
- [FSModuleIdentity](/documentation/fskit/fsmoduleidentity)

#### Accessing module properties

- [var bundleIdentifier: String](/documentation/fskit/fsmoduleidentity/bundleidentifier)
- [var url: URL](/documentation/fskit/fsmoduleidentity/url)
- [var isEnabled: Bool](/documentation/fskit/fsmoduleidentity/isenabled)

## Supporting types

- [FSBlockmapFlags](/documentation/fskit/fsblockmapflags)

### Declaring block map behaviors

- [static var read: FSBlockmapFlags](/documentation/fskit/fsblockmapflags/read)
- [static var write: FSBlockmapFlags](/documentation/fskit/fsblockmapflags/write)

### Working with raw values

- [init(rawValue: UInt)](/documentation/fskit/fsblockmapflags/init(rawvalue:))
- [FSCompleteIOFlags](/documentation/fskit/fscompleteioflags)

### Declaring I/O completion behaviors

- [static var read: FSCompleteIOFlags](/documentation/fskit/fscompleteioflags/read)
- [static var write: FSCompleteIOFlags](/documentation/fskit/fscompleteioflags/write)
- [static var async: FSCompleteIOFlags](/documentation/fskit/fscompleteioflags/async)

### Working with raw values

- [init(rawValue: UInt)](/documentation/fskit/fscompleteioflags/init(rawvalue:))
- [FSEntityIdentifier](/documentation/fskit/fsentityidentifier)

### Creating an entity identifier

- [init()](/documentation/fskit/fsentityidentifier/init())
- [init(uuid: UUID)](/documentation/fskit/fsentityidentifier/init(uuid:))
- [init(uuid: UUID, data: Data)](/documentation/fskit/fsentityidentifier/init(uuid:data:))
- [init(uuid: UUID, qualifier: UInt64)](/documentation/fskit/fsentityidentifier/init(uuid:qualifier:))

### Inspecting identifier properties

- [var uuid: UUID](/documentation/fskit/fsentityidentifier/uuid)
- [var qualifier: Data?](/documentation/fskit/fsentityidentifier/qualifier)
- [FSExtentPacker](/documentation/fskit/fsextentpacker)

### Packing extents

- [func packExtent(resource: FSBlockDeviceResource, type: FSExtentType, logicalOffset: off_t, physicalOffset: off_t, length: Int) -> Bool](/documentation/fskit/fsextentpacker/packextent(resource:type:logicaloffset:physicaloffset:length:))
- [FSExtentType](/documentation/fskit/fsextenttype)

#### Working with extent types

- [case data](/documentation/fskit/fsextenttype/data)
- [case zeroFill](/documentation/fskit/fsextenttype/zerofill)

#### Working with raw values

- [init?(rawValue: Int)](/documentation/fskit/fsextenttype/init(rawvalue:))
- [FSExtentType](/documentation/fskit/fsextenttype)

### Working with extent types

- [case data](/documentation/fskit/fsextenttype/data)
- [case zeroFill](/documentation/fskit/fsextenttype/zerofill)

### Working with raw values

- [init?(rawValue: Int)](/documentation/fskit/fsextenttype/init(rawvalue:))
- [FSMatchResult](/documentation/fskit/fsmatchresult)

### Working with match results

- [case usable](/documentation/fskit/fsmatchresult/usable)
- [case usableButLimited](/documentation/fskit/fsmatchresult/usablebutlimited)
- [case recognized](/documentation/fskit/fsmatchresult/recognized)
- [case notRecognized](/documentation/fskit/fsmatchresult/notrecognized)

### Working with raw values

- [init?(rawValue: Int)](/documentation/fskit/fsmatchresult/init(rawvalue:))
- [FSMetadataRange](/documentation/fskit/fsmetadatarange)

### Creating a metadata range

- [init(offset: off_t, segmentLength: UInt64, segmentCount: UInt64)](/documentation/fskit/fsmetadatarange/init(offset:segmentlength:segmentcount:))

### Accessing range properties

- [var startOffset: off_t](/documentation/fskit/fsmetadatarange/startoffset)
- [var segmentLength: UInt64](/documentation/fskit/fsmetadatarange/segmentlength)
- [var segmentCount: UInt64](/documentation/fskit/fsmetadatarange/segmentcount)
- [FSProbeResult](/documentation/fskit/fsproberesult)

### Working with results

- [class func recognized(name: String, containerID: FSContainerIdentifier) -> Self](/documentation/fskit/fsproberesult/recognized(name:containerid:))
- [class func usable(name: String, containerID: FSContainerIdentifier) -> Self](/documentation/fskit/fsproberesult/usable(name:containerid:))
- [class func usableButLimited(name: String, containerID: FSContainerIdentifier) -> Self](/documentation/fskit/fsproberesult/usablebutlimited(name:containerid:))
- [class var usableButLimited: FSProbeResult](/documentation/fskit/fsproberesult/usablebutlimited)
- [class var notRecognized: FSProbeResult](/documentation/fskit/fsproberesult/notrecognized)

### Working with result properties

- [var containerID: FSContainerIdentifier?](/documentation/fskit/fsproberesult/containerid)
- [var name: String?](/documentation/fskit/fsproberesult/name)
- [var result: FSMatchResult](/documentation/fskit/fsproberesult/result)
- [FSMatchResult](/documentation/fskit/fsmatchresult)

#### Working with match results

- [case usable](/documentation/fskit/fsmatchresult/usable)
- [case usableButLimited](/documentation/fskit/fsmatchresult/usablebutlimited)
- [case recognized](/documentation/fskit/fsmatchresult/recognized)
- [case notRecognized](/documentation/fskit/fsmatchresult/notrecognized)

#### Working with raw values

- [init?(rawValue: Int)](/documentation/fskit/fsmatchresult/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
