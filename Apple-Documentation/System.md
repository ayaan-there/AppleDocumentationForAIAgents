# System Documentation

Source: https://sosumi.ai/documentation/system

---
title: System
source: https://developer.apple.com/documentation/system
timestamp: 2026-02-13T19:02:50.019Z
---

## Adopting System

- [Adopting Swift File Operations](/documentation/system/adopting-file-operations)
- [Adopting Swift File Options](/documentation/system/adopting-file-options)
- [Adopting Swift Error Constants](/documentation/system/adopting-errno)

## Files

- [FileDescriptor](/documentation/system/filedescriptor)

### Creating a File Descriptor

- [init(rawValue: CInt)](/documentation/system/filedescriptor/init(rawvalue:))
- [let rawValue: CInt](/documentation/system/filedescriptor/rawvalue)

### Opening a File

- [static func open(FilePath, FileDescriptor.AccessMode, options: FileDescriptor.OpenOptions, permissions: FilePermissions?, retryOnInterrupt: Bool) throws -> FileDescriptor](/documentation/system/filedescriptor/open(_:_:options:permissions:retryoninterrupt:)-4ql4b)
- [static func open(UnsafePointer<CChar>, FileDescriptor.AccessMode, options: FileDescriptor.OpenOptions, permissions: FilePermissions?, retryOnInterrupt: Bool) throws -> FileDescriptor](/documentation/system/filedescriptor/open(_:_:options:permissions:retryoninterrupt:)-5t3xn)
- [FileDescriptor.AccessMode](/documentation/system/filedescriptor/accessmode)

#### Creating an Access Mode

- [static var readOnly: FileDescriptor.AccessMode](/documentation/system/filedescriptor/accessmode/readonly)
- [static var readWrite: FileDescriptor.AccessMode](/documentation/system/filedescriptor/accessmode/readwrite)
- [static var writeOnly: FileDescriptor.AccessMode](/documentation/system/filedescriptor/accessmode/writeonly)

#### Debugging

- [var description: String](/documentation/system/filedescriptor/accessmode/description)
- [var debugDescription: String](/documentation/system/filedescriptor/accessmode/debugdescription)

#### Working with C APIs

- [init(rawValue: CInt)](/documentation/system/filedescriptor/accessmode/init(rawvalue:))
- [var rawValue: CInt](/documentation/system/filedescriptor/accessmode/rawvalue)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/system/filedescriptor/accessmode/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/system/filedescriptor/accessmode/debugdescription)
- [CustomStringConvertible Implementations](/documentation/system/filedescriptor/accessmode/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/system/filedescriptor/accessmode/description)
- [FileDescriptor.OpenOptions](/documentation/system/filedescriptor/openoptions)

#### Specifying Options

- [static var append: FileDescriptor.OpenOptions](/documentation/system/filedescriptor/openoptions/append)
- [static var closeOnExec: FileDescriptor.OpenOptions](/documentation/system/filedescriptor/openoptions/closeonexec)
- [static var create: FileDescriptor.OpenOptions](/documentation/system/filedescriptor/openoptions/create)
- [static var eventOnly: FileDescriptor.OpenOptions](/documentation/system/filedescriptor/openoptions/eventonly)
- [static var exclusiveCreate: FileDescriptor.OpenOptions](/documentation/system/filedescriptor/openoptions/exclusivecreate)
- [static var exclusiveLock: FileDescriptor.OpenOptions](/documentation/system/filedescriptor/openoptions/exclusivelock)
- [static var noFollow: FileDescriptor.OpenOptions](/documentation/system/filedescriptor/openoptions/nofollow)
- [static var nonBlocking: FileDescriptor.OpenOptions](/documentation/system/filedescriptor/openoptions/nonblocking)
- [static var sharedLock: FileDescriptor.OpenOptions](/documentation/system/filedescriptor/openoptions/sharedlock)
- [static var symlink: FileDescriptor.OpenOptions](/documentation/system/filedescriptor/openoptions/symlink)
- [static var truncate: FileDescriptor.OpenOptions](/documentation/system/filedescriptor/openoptions/truncate)

#### Interacting with C APIs

- [init(rawValue: CInt)](/documentation/system/filedescriptor/openoptions/init(rawvalue:))
- [var rawValue: CInt](/documentation/system/filedescriptor/openoptions/rawvalue)

#### Debugging

- [var description: String](/documentation/system/filedescriptor/openoptions/description)
- [var debugDescription: String](/documentation/system/filedescriptor/openoptions/debugdescription)

#### Type Properties

- [static var directory: FileDescriptor.OpenOptions](/documentation/system/filedescriptor/openoptions/directory)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/system/filedescriptor/openoptions/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/system/filedescriptor/openoptions/debugdescription)
- [CustomStringConvertible Implementations](/documentation/system/filedescriptor/openoptions/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/system/filedescriptor/openoptions/description)

### Reading From a File

- [func read(into: UnsafeMutableRawBufferPointer, retryOnInterrupt: Bool) throws -> Int](/documentation/system/filedescriptor/read(into:retryoninterrupt:))
- [func read(fromAbsoluteOffset: Int64, into: UnsafeMutableRawBufferPointer, retryOnInterrupt: Bool) throws -> Int](/documentation/system/filedescriptor/read(fromabsoluteoffset:into:retryoninterrupt:))

### Changing a File’s Offset

- [func seek(offset: Int64, from: FileDescriptor.SeekOrigin) throws -> Int64](/documentation/system/filedescriptor/seek(offset:from:))
- [FileDescriptor.SeekOrigin](/documentation/system/filedescriptor/seekorigin)

#### Creating a Seek Origin

- [static var current: FileDescriptor.SeekOrigin](/documentation/system/filedescriptor/seekorigin/current)
- [static var end: FileDescriptor.SeekOrigin](/documentation/system/filedescriptor/seekorigin/end)
- [static var nextHole: FileDescriptor.SeekOrigin](/documentation/system/filedescriptor/seekorigin/nexthole)
- [static var nextData: FileDescriptor.SeekOrigin](/documentation/system/filedescriptor/seekorigin/nextdata)
- [static var start: FileDescriptor.SeekOrigin](/documentation/system/filedescriptor/seekorigin/start)

#### Debugging

- [var description: String](/documentation/system/filedescriptor/seekorigin/description)
- [var debugDescription: String](/documentation/system/filedescriptor/seekorigin/debugdescription)

#### Working with C APIs

- [init(rawValue: CInt)](/documentation/system/filedescriptor/seekorigin/init(rawvalue:))
- [var rawValue: CInt](/documentation/system/filedescriptor/seekorigin/rawvalue)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/system/filedescriptor/seekorigin/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/system/filedescriptor/seekorigin/debugdescription)
- [CustomStringConvertible Implementations](/documentation/system/filedescriptor/seekorigin/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/system/filedescriptor/seekorigin/description)

### Writing To A File

- [func write(UnsafeRawBufferPointer, retryOnInterrupt: Bool) throws -> Int](/documentation/system/filedescriptor/write(_:retryoninterrupt:))
- [func write(toAbsoluteOffset: Int64, UnsafeRawBufferPointer, retryOnInterrupt: Bool) throws -> Int](/documentation/system/filedescriptor/write(toabsoluteoffset:_:retryoninterrupt:))
- [func writeAll<S>(S) throws -> Int](/documentation/system/filedescriptor/writeall(_:))
- [func writeAll<S>(toAbsoluteOffset: Int64, S) throws -> Int](/documentation/system/filedescriptor/writeall(toabsoluteoffset:_:))

### Closing a File

- [func close() throws](/documentation/system/filedescriptor/close())
- [func closeAfter<R>(() throws -> R) throws -> R](/documentation/system/filedescriptor/closeafter(_:))

### Instance Methods

- [func duplicate(as: FileDescriptor?, retryOnInterrupt: Bool) throws -> FileDescriptor](/documentation/system/filedescriptor/duplicate(as:retryoninterrupt:))
- [func resize(to: Int64, retryOnInterrupt: Bool) throws](/documentation/system/filedescriptor/resize(to:retryoninterrupt:))

### Type Properties

- [static var standardError: FileDescriptor](/documentation/system/filedescriptor/standarderror)
- [static var standardInput: FileDescriptor](/documentation/system/filedescriptor/standardinput)
- [static var standardOutput: FileDescriptor](/documentation/system/filedescriptor/standardoutput)

### Type Methods

- [static func pipe() throws -> (readEnd: FileDescriptor, writeEnd: FileDescriptor)](/documentation/system/filedescriptor/pipe())
- [FilePath](/documentation/system/filepath)

### Creating a File Path

- [init()](/documentation/system/filepath/init())
- [init(stringLiteral: String)](/documentation/system/filepath/init(stringliteral:))

### Working with File Paths

- [var length: Int](/documentation/system/filepath/length)
- [var description: String](/documentation/system/filepath/description)
- [var debugDescription: String](/documentation/system/filepath/debugdescription)

### Interacting with C APIs

- [func withCString<Result>((UnsafePointer<CChar>) throws -> Result) rethrows -> Result](/documentation/system/filepath/withcstring(_:))

### Structures

- [FilePath.Component](/documentation/system/filepath/component)

#### Initializers

- [init?(String)](/documentation/system/filepath/component/init(_:))
- [init?(platformString: [CInterop.PlatformChar])](/documentation/system/filepath/component/init(platformstring:)-2tz4)
- [init?(platformString: inout CInterop.PlatformChar)](/documentation/system/filepath/component/init(platformstring:)-3mzo3)
- [init?(platformString: String)](/documentation/system/filepath/component/init(platformstring:)-8kixy)
- [init?(platformString: UnsafePointer<CInterop.PlatformChar>)](/documentation/system/filepath/component/init(platformstring:)-9a3qq)

#### Instance Properties

- [var `extension`: String?](/documentation/system/filepath/component/extension)
- [var kind: FilePath.Component.Kind](/documentation/system/filepath/component/kind-swift.property)
- [var stem: String](/documentation/system/filepath/component/stem)
- [var string: String](/documentation/system/filepath/component/string)

#### Instance Methods

- [func withPlatformString<Result>((UnsafePointer<CInterop.PlatformChar>) throws -> Result) rethrows -> Result](/documentation/system/filepath/component/withplatformstring(_:))

#### Enumerations

- [FilePath.Component.Kind](/documentation/system/filepath/component/kind-swift.enum)

##### Enumeration Cases

- [case currentDirectory](/documentation/system/filepath/component/kind-swift.enum/currentdirectory)
- [case parentDirectory](/documentation/system/filepath/component/kind-swift.enum/parentdirectory)
- [case regular](/documentation/system/filepath/component/kind-swift.enum/regular)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/system/filepath/component/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/system/filepath/component/debugdescription)
- [CustomStringConvertible Implementations](/documentation/system/filepath/component/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/system/filepath/component/description)
- [ExpressibleByStringLiteral Implementations](/documentation/system/filepath/component/expressiblebystringliteral-implementations)

##### Initializers

- [init(stringLiteral: String)](/documentation/system/filepath/component/init(stringliteral:))
- [FilePath.ComponentView](/documentation/system/filepath/componentview)
- [FilePath.Root](/documentation/system/filepath/root-swift.struct)

#### Initializers

- [init?(String)](/documentation/system/filepath/root-swift.struct/init(_:))
- [init?(platformString: [CInterop.PlatformChar])](/documentation/system/filepath/root-swift.struct/init(platformstring:)-3s0ol)
- [init?(platformString: String)](/documentation/system/filepath/root-swift.struct/init(platformstring:)-4twb4)
- [init?(platformString: UnsafePointer<CInterop.PlatformChar>)](/documentation/system/filepath/root-swift.struct/init(platformstring:)-5j1fu)
- [init?(platformString: inout CInterop.PlatformChar)](/documentation/system/filepath/root-swift.struct/init(platformstring:)-8hwtb)

#### Instance Properties

- [var string: String](/documentation/system/filepath/root-swift.struct/string)

#### Instance Methods

- [func withPlatformString<Result>((UnsafePointer<CInterop.PlatformChar>) throws -> Result) rethrows -> Result](/documentation/system/filepath/root-swift.struct/withplatformstring(_:))

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/system/filepath/root-swift.struct/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/system/filepath/root-swift.struct/debugdescription)
- [CustomStringConvertible Implementations](/documentation/system/filepath/root-swift.struct/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/system/filepath/root-swift.struct/description)
- [ExpressibleByStringLiteral Implementations](/documentation/system/filepath/root-swift.struct/expressiblebystringliteral-implementations)

##### Initializers

- [init(stringLiteral: String)](/documentation/system/filepath/root-swift.struct/init(stringliteral:))

### Initializers

- [init?(URL)](/documentation/system/filepath/init(_:)-2gkpw)
- [init(String)](/documentation/system/filepath/init(_:)-61dsw)
- [init(cString: [CChar])](/documentation/system/filepath/init(cstring:)-2hetg)
- [init(cString: String)](/documentation/system/filepath/init(cstring:)-3xw0n)
- [init(cString: UnsafePointer<CChar>)](/documentation/system/filepath/init(cstring:)-5igtz)
- [init(cString: inout CChar)](/documentation/system/filepath/init(cstring:)-8d3vx)
- [init(platformString: inout CInterop.PlatformChar)](/documentation/system/filepath/init(platformstring:)-4b3o6)
- [init(platformString: UnsafePointer<CInterop.PlatformChar>)](/documentation/system/filepath/init(platformstring:)-5o7oh)
- [init(platformString: String)](/documentation/system/filepath/init(platformstring:)-6i5cc)
- [init(platformString: [CInterop.PlatformChar])](/documentation/system/filepath/init(platformstring:)-8amn5)
- [init<C>(root: FilePath.Root?, C)](/documentation/system/filepath/init(root:_:)-19uu0)
- [init(root: FilePath.Root?, FilePath.ComponentView.SubSequence)](/documentation/system/filepath/init(root:_:)-19xzy)
- [init(root: FilePath.Root?, components: FilePath.Component...)](/documentation/system/filepath/init(root:components:))

### Instance Properties

- [var components: FilePath.ComponentView](/documentation/system/filepath/components)
- [var `extension`: String?](/documentation/system/filepath/extension)
- [var isAbsolute: Bool](/documentation/system/filepath/isabsolute)
- [var isEmpty: Bool](/documentation/system/filepath/isempty)
- [var isLexicallyNormal: Bool](/documentation/system/filepath/islexicallynormal)
- [var isRelative: Bool](/documentation/system/filepath/isrelative)
- [var lastComponent: FilePath.Component?](/documentation/system/filepath/lastcomponent)
- [var root: FilePath.Root?](/documentation/system/filepath/root-swift.property)
- [var stem: String?](/documentation/system/filepath/stem)
- [var string: String](/documentation/system/filepath/string)

### Instance Methods

- [func append<C>(C)](/documentation/system/filepath/append(_:)-66nkr)
- [func append(String)](/documentation/system/filepath/append(_:)-7ttzp)
- [func append(FilePath.Component)](/documentation/system/filepath/append(_:)-8f41n)
- [func appending(String) -> FilePath](/documentation/system/filepath/appending(_:)-1dtn3)
- [func appending(FilePath.Component) -> FilePath](/documentation/system/filepath/appending(_:)-24s87)
- [func appending<C>(C) -> FilePath](/documentation/system/filepath/appending(_:)-60fwk)
- [func ends(with: FilePath) -> Bool](/documentation/system/filepath/ends(with:))
- [func lexicallyNormalize()](/documentation/system/filepath/lexicallynormalize())
- [func lexicallyNormalized() -> FilePath](/documentation/system/filepath/lexicallynormalized())
- [func lexicallyResolving(FilePath) -> FilePath?](/documentation/system/filepath/lexicallyresolving(_:))
- [func push(FilePath)](/documentation/system/filepath/push(_:))
- [func pushing(FilePath) -> FilePath](/documentation/system/filepath/pushing(_:))
- [func removeAll(keepingCapacity: Bool)](/documentation/system/filepath/removeall(keepingcapacity:))
- [func removeLastComponent() -> Bool](/documentation/system/filepath/removelastcomponent())
- [func removePrefix(FilePath) -> Bool](/documentation/system/filepath/removeprefix(_:))
- [func removingLastComponent() -> FilePath](/documentation/system/filepath/removinglastcomponent())
- [func removingRoot() -> FilePath](/documentation/system/filepath/removingroot())
- [func reserveCapacity(Int)](/documentation/system/filepath/reservecapacity(_:))
- [func starts(with: FilePath) -> Bool](/documentation/system/filepath/starts(with:))
- [func withPlatformString<Result>((UnsafePointer<CInterop.PlatformChar>) throws -> Result) rethrows -> Result](/documentation/system/filepath/withplatformstring(_:))

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/system/filepath/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/system/filepath/debugdescription)
- [CustomStringConvertible Implementations](/documentation/system/filepath/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/system/filepath/description)
- [ExpressibleByStringLiteral Implementations](/documentation/system/filepath/expressiblebystringliteral-implementations)

#### Initializers

- [init(stringLiteral: String)](/documentation/system/filepath/init(stringliteral:))
- [FilePermissions](/documentation/system/filepermissions)

### Owner Permissions

- [static var ownerRead: FilePermissions](/documentation/system/filepermissions/ownerread)
- [static var ownerWrite: FilePermissions](/documentation/system/filepermissions/ownerwrite)
- [static var ownerExecute: FilePermissions](/documentation/system/filepermissions/ownerexecute)
- [static var ownerReadWrite: FilePermissions](/documentation/system/filepermissions/ownerreadwrite)
- [static var ownerReadExecute: FilePermissions](/documentation/system/filepermissions/ownerreadexecute)
- [static var ownerWriteExecute: FilePermissions](/documentation/system/filepermissions/ownerwriteexecute)
- [static var ownerReadWriteExecute: FilePermissions](/documentation/system/filepermissions/ownerreadwriteexecute)

### Group Permissions

- [static var groupRead: FilePermissions](/documentation/system/filepermissions/groupread)
- [static var groupWrite: FilePermissions](/documentation/system/filepermissions/groupwrite)
- [static var groupExecute: FilePermissions](/documentation/system/filepermissions/groupexecute)
- [static var groupReadWrite: FilePermissions](/documentation/system/filepermissions/groupreadwrite)
- [static var groupReadExecute: FilePermissions](/documentation/system/filepermissions/groupreadexecute)
- [static var groupWriteExecute: FilePermissions](/documentation/system/filepermissions/groupwriteexecute)
- [static var groupReadWriteExecute: FilePermissions](/documentation/system/filepermissions/groupreadwriteexecute)

### Other Permissions

- [static var otherRead: FilePermissions](/documentation/system/filepermissions/otherread)
- [static var otherWrite: FilePermissions](/documentation/system/filepermissions/otherwrite)
- [static var otherExecute: FilePermissions](/documentation/system/filepermissions/otherexecute)
- [static var otherReadWrite: FilePermissions](/documentation/system/filepermissions/otherreadwrite)
- [static var otherReadExecute: FilePermissions](/documentation/system/filepermissions/otherreadexecute)
- [static var otherWriteExecute: FilePermissions](/documentation/system/filepermissions/otherwriteexecute)
- [static var otherReadWriteExecute: FilePermissions](/documentation/system/filepermissions/otherreadwriteexecute)

### Special Permissions

- [static var setUserID: FilePermissions](/documentation/system/filepermissions/setuserid)
- [static var setGroupID: FilePermissions](/documentation/system/filepermissions/setgroupid)
- [static var saveText: FilePermissions](/documentation/system/filepermissions/savetext)

### Interacting with C APIs

- [init(rawValue: CModeT)](/documentation/system/filepermissions/init(rawvalue:))
- [let rawValue: CModeT](/documentation/system/filepermissions/rawvalue)
- [CModeT](/documentation/system/cmodet)

### Debugging

- [var description: String](/documentation/system/filepermissions/description)
- [var debugDescription: String](/documentation/system/filepermissions/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/system/filepermissions/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/system/filepermissions/debugdescription)
- [CustomStringConvertible Implementations](/documentation/system/filepermissions/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/system/filepermissions/description)

## Errors

- [Errno](/documentation/system/errno)

### File and Directory Errors

- [static var attributeNotFound: Errno](/documentation/system/errno/attributenotfound)
- [static var badFileDescriptor: Errno](/documentation/system/errno/badfiledescriptor)
- [static var fileExists: Errno](/documentation/system/errno/fileexists)
- [static var fileTooLarge: Errno](/documentation/system/errno/filetoolarge)
- [static var improperLink: Errno](/documentation/system/errno/improperlink)
- [static var isDirectory: Errno](/documentation/system/errno/isdirectory)
- [static var noLocks: Errno](/documentation/system/errno/nolocks)
- [static var noSuchFileOrDirectory: Errno](/documentation/system/errno/nosuchfileordirectory)
- [static var notDirectory: Errno](/documentation/system/errno/notdirectory)
- [static var permissionDenied: Errno](/documentation/system/errno/permissiondenied)
- [static var textFileBusy: Errno](/documentation/system/errno/textfilebusy)

### File System Errors

- [static var badFileTypeOrFormat: Errno](/documentation/system/errno/badfiletypeorformat)
- [static var directoryNotEmpty: Errno](/documentation/system/errno/directorynotempty)
- [static var diskQuotaExceeded: Errno](/documentation/system/errno/diskquotaexceeded)
- [static var noSpace: Errno](/documentation/system/errno/nospace)
- [static var readOnlyFileSystem: Errno](/documentation/system/errno/readonlyfilesystem)
- [static var tooManyLinks: Errno](/documentation/system/errno/toomanylinks)
- [static var tooManyOpenFilesInSystem: Errno](/documentation/system/errno/toomanyopenfilesinsystem)
- [static var tooManyOpenFiles: Errno](/documentation/system/errno/toomanyopenfiles)

### NFS Errors

- [static var authenticationError: Errno](/documentation/system/errno/authenticationerror)
- [static var needAuthenticator: Errno](/documentation/system/errno/needauthenticator)
- [static var staleNFSFileHandle: Errno](/documentation/system/errno/stalenfsfilehandle)

### Device Errors

- [static var deviceError: Errno](/documentation/system/errno/deviceerror)
- [static var devicePowerIsOff: Errno](/documentation/system/errno/devicepowerisoff)
- [static var inappropriateIOCTLForDevice: Errno](/documentation/system/errno/inappropriateioctlfordevice)
- [static var ioError: Errno](/documentation/system/errno/ioerror)
- [static var noSuchAddressOrDevice: Errno](/documentation/system/errno/nosuchaddressordevice)
- [static var notBlockDevice: Errno](/documentation/system/errno/notblockdevice)
- [static var operationNotSupportedByDevice: Errno](/documentation/system/errno/operationnotsupportedbydevice)

### Path Errors

- [static var fileNameTooLong: Errno](/documentation/system/errno/filenametoolong)
- [static var tooManyRemoteLevels: Errno](/documentation/system/errno/toomanyremotelevels)
- [static var tooManySymbolicLinkLevels: Errno](/documentation/system/errno/toomanysymboliclinklevels)

### Pipe Errors

- [static var brokenPipe: Errno](/documentation/system/errno/brokenpipe)
- [static var illegalSeek: Errno](/documentation/system/errno/illegalseek)

### Runtime Errors

- [static var deadlock: Errno](/documentation/system/errno/deadlock)
- [static var noMemory: Errno](/documentation/system/errno/nomemory)
- [static var wouldBlock: Errno](/documentation/system/errno/wouldblock)

### Math Errors

- [static var outOfDomain: Errno](/documentation/system/errno/outofdomain)
- [static var outOfRange: Errno](/documentation/system/errno/outofrange)
- [static var overflow: Errno](/documentation/system/errno/overflow)

### Executable File Errors

- [static var badCPUType: Errno](/documentation/system/errno/badcputype)
- [static var badExecutable: Errno](/documentation/system/errno/badexecutable)
- [static var execFormatError: Errno](/documentation/system/errno/execformaterror)
- [static var malformedMachO: Errno](/documentation/system/errno/malformedmacho)
- [static var sharedLibraryVersionMismatch: Errno](/documentation/system/errno/sharedlibraryversionmismatch)

### Network Errors

- [static var connectionAbort: Errno](/documentation/system/errno/connectionabort)
- [static var connectionRefused: Errno](/documentation/system/errno/connectionrefused)
- [static var connectionReset: Errno](/documentation/system/errno/connectionreset)
- [static var hostIsDown: Errno](/documentation/system/errno/hostisdown)
- [static var messageTooLong: Errno](/documentation/system/errno/messagetoolong)
- [static var networkDown: Errno](/documentation/system/errno/networkdown)
- [static var networkReset: Errno](/documentation/system/errno/networkreset)
- [static var networkUnreachable: Errno](/documentation/system/errno/networkunreachable)
- [static var noBufferSpace: Errno](/documentation/system/errno/nobufferspace)
- [static var noRouteToHost: Errno](/documentation/system/errno/noroutetohost)
- [static var notSupported: Errno](/documentation/system/errno/notsupported)
- [static var timedOut: Errno](/documentation/system/errno/timedout)

### Network Protocol Errors

- [static var protocolError: Errno](/documentation/system/errno/protocolerror)
- [static var protocolFamilyNotSupported: Errno](/documentation/system/errno/protocolfamilynotsupported)
- [static var protocolNotAvailable: Errno](/documentation/system/errno/protocolnotavailable)
- [static var protocolNotSupported: Errno](/documentation/system/errno/protocolnotsupported)
- [static var protocolWrongTypeForSocket: Errno](/documentation/system/errno/protocolwrongtypeforsocket)

### Network Address Errors

- [static var addressFamilyNotSupported: Errno](/documentation/system/errno/addressfamilynotsupported)
- [static var addressInUse: Errno](/documentation/system/errno/addressinuse)
- [static var addressNotAvailable: Errno](/documentation/system/errno/addressnotavailable)
- [static var addressRequired: Errno](/documentation/system/errno/addressrequired)

### Network Socket Errors

- [static var notSocket: Errno](/documentation/system/errno/notsocket)
- [static var notSupportedOnSocket: Errno](/documentation/system/errno/notsupportedonsocket)
- [static var socketIsConnected: Errno](/documentation/system/errno/socketisconnected)
- [static var socketNotConnected: Errno](/documentation/system/errno/socketnotconnected)
- [static var socketShutdown: Errno](/documentation/system/errno/socketshutdown)
- [static var socketTypeNotSupported: Errno](/documentation/system/errno/sockettypenotsupported)

### RPC Errors

- [static var rpcProcedureUnavailable: Errno](/documentation/system/errno/rpcprocedureunavailable)
- [static var rpcProgramUnavailable: Errno](/documentation/system/errno/rpcprogramunavailable)
- [static var rpcProgramVersionMismatch: Errno](/documentation/system/errno/rpcprogramversionmismatch)
- [static var rpcUnsuccessful: Errno](/documentation/system/errno/rpcunsuccessful)
- [static var rpcVersionMismatch: Errno](/documentation/system/errno/rpcversionmismatch)

### Process Errors

- [static var argListTooLong: Errno](/documentation/system/errno/arglisttoolong)
- [static var identifierRemoved: Errno](/documentation/system/errno/identifierremoved)
- [static var noChildProcess: Errno](/documentation/system/errno/nochildprocess)
- [static var noSuchProcess: Errno](/documentation/system/errno/nosuchprocess)
- [static var previousOwnerDied: Errno](/documentation/system/errno/previousownerdied)
- [static var tooManyProcesses: Errno](/documentation/system/errno/toomanyprocesses)

### System Call Errors

- [static var alreadyInProcess: Errno](/documentation/system/errno/alreadyinprocess)
- [static var badAddress: Errno](/documentation/system/errno/badaddress)
- [static var interrupted: Errno](/documentation/system/errno/interrupted)
- [static var invalidArgument: Errno](/documentation/system/errno/invalidargument)
- [static var noFunction: Errno](/documentation/system/errno/nofunction)
- [static var nowInProgress: Errno](/documentation/system/errno/nowinprogress)
- [static var resourceBusy: Errno](/documentation/system/errno/resourcebusy)
- [static var resourceTemporarilyUnavailable: Errno](/documentation/system/errno/resourcetemporarilyunavailable)

### General Errors

- [static var badMessage: Errno](/documentation/system/errno/badmessage)
- [static var canceled: Errno](/documentation/system/errno/canceled)
- [static var illegalByteSequence: Errno](/documentation/system/errno/illegalbytesequence)
- [static var noData: Errno](/documentation/system/errno/nodata)
- [static var noMessage: Errno](/documentation/system/errno/nomessage)
- [static var noSuchPolicy: Errno](/documentation/system/errno/nosuchpolicy)
- [static var notPermitted: Errno](/documentation/system/errno/notpermitted)
- [static var notRecoverable: Errno](/documentation/system/errno/notrecoverable)
- [static var outputQueueFull: Errno](/documentation/system/errno/outputqueuefull)
- [static var tooManyReferences: Errno](/documentation/system/errno/toomanyreferences)
- [static var tooManyUsers: Errno](/documentation/system/errno/toomanyusers)

### Reserved

- [static var lastErrnoValue: Errno](/documentation/system/errno/lasterrnovalue)
- [static var multiHop: Errno](/documentation/system/errno/multihop)
- [static var noLink: Errno](/documentation/system/errno/nolink)
- [static var noStreamResources: Errno](/documentation/system/errno/nostreamresources)
- [static var notStream: Errno](/documentation/system/errno/notstream)
- [static var notUsed: Errno](/documentation/system/errno/notused)
- [static var timeout: Errno](/documentation/system/errno/timeout)

### Interacting with C APIs

- [init(rawValue: CInt)](/documentation/system/errno/init(rawvalue:))
- [let rawValue: CInt](/documentation/system/errno/rawvalue)

### Debugging

- [var description: String](/documentation/system/errno/description)
- [var debugDescription: String](/documentation/system/errno/debugdescription)

### Comparing Errors

- [static func ~= (Errno, any Error) -> Bool](/documentation/system/errno/~=(_:_:))

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/system/errno/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/system/errno/debugdescription)
- [CustomStringConvertible Implementations](/documentation/system/errno/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/system/errno/description)

## Protocols

- [MachPortRight](/documentation/system/machportright)

## Enumerations

- [CInterop](/documentation/system/cinterop)

### Type Aliases

- [CInterop.Char](/documentation/system/cinterop/char)
- [CInterop.Mode](/documentation/system/cinterop/mode)
- [CInterop.PlatformChar](/documentation/system/cinterop/platformchar)
- [CInterop.PlatformUnicodeEncoding](/documentation/system/cinterop/platformunicodeencoding)
- [Mach](/documentation/system/mach)

### Structures

- [Mach.Port](/documentation/system/mach/port)

#### Initializers

- [init()](/documentation/system/mach/port/init())
- [init(name: mach_port_name_t)](/documentation/system/mach/port/init(name:))
- [init(name: mach_port_name_t, context: mach_port_context_t)](/documentation/system/mach/port/init(name:context:)-14mp9)
- [init(name: mach_port_name_t, context: mach_port_context_t)](/documentation/system/mach/port/init(name:context:)-oyjl)

#### Instance Properties

- [var makeSendCount: mach_port_mscount_t](/documentation/system/mach/port/makesendcount)

#### Instance Methods

- [func copySendRight() throws -> Mach.Port<Mach.SendRight>](/documentation/system/mach/port/copysendright())
- [func makeSendOnceRight() -> Mach.Port<Mach.SendOnceRight>](/documentation/system/mach/port/makesendonceright())
- [func makeSendRight() -> Mach.Port<Mach.SendRight>](/documentation/system/mach/port/makesendright())
- [func relinquish() -> mach_port_name_t](/documentation/system/mach/port/relinquish()-241tg)
- [func relinquish() -> (name: mach_port_name_t, context: mach_port_context_t)](/documentation/system/mach/port/relinquish()-70vbe)
- [func relinquish() -> mach_port_name_t](/documentation/system/mach/port/relinquish()-74amu)
- [func relinquish() -> (name: mach_port_name_t, context: mach_port_context_t)](/documentation/system/mach/port/relinquish()-9lm56)
- [func unguardAndRelinquish() -> mach_port_name_t](/documentation/system/mach/port/unguardandrelinquish())
- [func withBorrowedName<ReturnType>(body: (mach_port_name_t, mach_port_context_t) -> ReturnType) -> ReturnType](/documentation/system/mach/port/withborrowedname(body:)-4d4iq)
- [func withBorrowedName<ReturnType>(body: (mach_port_name_t, mach_port_context_t) -> ReturnType) -> ReturnType](/documentation/system/mach/port/withborrowedname(body:)-8402i)
- [func withBorrowedName<ReturnType>(body: (mach_port_name_t) -> ReturnType) -> ReturnType](/documentation/system/mach/port/withborrowedname(body:)-9v68k)
- [Mach.ReceiveRight](/documentation/system/mach/receiveright)
- [Mach.SendOnceRight](/documentation/system/mach/sendonceright)
- [Mach.SendRight](/documentation/system/mach/sendright)

### Enumerations

- [Mach.PortRightError](/documentation/system/mach/portrighterror)

#### Enumeration Cases

- [case deadName](/documentation/system/mach/portrighterror/deadname)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
