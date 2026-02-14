# Paravirtualized Graphics Documentation

Source: https://sosumi.ai/documentation/paravirtualizedgraphics

---
title: Paravirtualized Graphics
source: https://developer.apple.com/documentation/paravirtualizedgraphics
timestamp: 2026-02-13T19:00:24.583Z
---

## PCI Device Characteristics

- [var PG_PCI_DEVICE_ID: Int32](/documentation/paravirtualizedgraphics/pg_pci_device_id)
- [var PG_PCI_VENDOR_ID: Int32](/documentation/paravirtualizedgraphics/pg_pci_vendor_id)
- [var PG_PCI_BAR_MMIO: Int32](/documentation/paravirtualizedgraphics/pg_pci_bar_mmio)
- [var PG_PCI_MAX_MSI_VECTORS: Int32](/documentation/paravirtualizedgraphics/pg_pci_max_msi_vectors)
- [func PGCopyOptionROMURL() -> URL](/documentation/paravirtualizedgraphics/pgcopyoptionromurl())

## Devices

- [func PGNewDeviceWithDescriptor(PGDeviceDescriptor) -> (any PGDevice)?](/documentation/paravirtualizedgraphics/pgnewdevicewithdescriptor(_:))
- [PGDeviceDescriptor](/documentation/paravirtualizedgraphics/pgdevicedescriptor)

### Specifying the GPU

- [var device: (any MTLDevice)?](/documentation/paravirtualizedgraphics/pgdevicedescriptor/device)

### Managing Tasks

- [var createTask: PGCreateTask?](/documentation/paravirtualizedgraphics/pgdevicedescriptor/createtask)
- [var destroyTask: PGDestroyTask?](/documentation/paravirtualizedgraphics/pgdevicedescriptor/destroytask)
- [PGCreateTask](/documentation/paravirtualizedgraphics/pgcreatetask)
- [PGDestroyTask](/documentation/paravirtualizedgraphics/pgdestroytask)

### Managing Memory Operations

- [var mapMemory: PGMapMemory?](/documentation/paravirtualizedgraphics/pgdevicedescriptor/mapmemory)
- [var unmapMemory: PGUnmapMemory?](/documentation/paravirtualizedgraphics/pgdevicedescriptor/unmapmemory)
- [var readMemory: PGReadMemory?](/documentation/paravirtualizedgraphics/pgdevicedescriptor/readmemory)
- [PGMapMemory](/documentation/paravirtualizedgraphics/pgmapmemory)
- [PGUnmapMemory](/documentation/paravirtualizedgraphics/pgunmapmemory)
- [PGReadMemory](/documentation/paravirtualizedgraphics/pgreadmemory)
- [PGPhysicalMemoryRange_s](/documentation/paravirtualizedgraphics/pgphysicalmemoryrange_s)

#### Creating a Memory Range

- [init()](/documentation/paravirtualizedgraphics/pgphysicalmemoryrange_s/init())
- [init(physicalAddress: UInt64, physicalLength: UInt64)](/documentation/paravirtualizedgraphics/pgphysicalmemoryrange_s/init(physicaladdress:physicallength:))

#### Inspecting Range Properties

- [var physicalAddress: UInt64](/documentation/paravirtualizedgraphics/pgphysicalmemoryrange_s/physicaladdress)
- [var physicalLength: UInt64](/documentation/paravirtualizedgraphics/pgphysicalmemoryrange_s/physicallength)

#### Type alias

- [PGPhysicalMemoryRange_t](/documentation/paravirtualizedgraphics/pgphysicalmemoryrange_t)

### Specifying Trace Behavior

- [var addTraceRange: PGAddTraceRange?](/documentation/paravirtualizedgraphics/pgdevicedescriptor/addtracerange)
- [var removeTraceRange: PGRemoveTraceRange?](/documentation/paravirtualizedgraphics/pgdevicedescriptor/removetracerange)
- [PGAddTraceRange](/documentation/paravirtualizedgraphics/pgaddtracerange)
- [PGRemoveTraceRange](/documentation/paravirtualizedgraphics/pgremovetracerange)
- [PGTraceRangeHandler](/documentation/paravirtualizedgraphics/pgtracerangehandler)

### Handling Interrupts

- [var raiseInterrupt: PGRaiseInterrupt?](/documentation/paravirtualizedgraphics/pgdevicedescriptor/raiseinterrupt)
- [PGRaiseInterrupt](/documentation/paravirtualizedgraphics/pgraiseinterrupt)

### Specifying Virtual Device Properties

- [var mmioLength: Int](/documentation/paravirtualizedgraphics/pgdevicedescriptor/mmiolength)

### Instance Properties

- [var displayPortCount: UInt32](/documentation/paravirtualizedgraphics/pgdevicedescriptor/displayportcount)
- [PGDevice](/documentation/paravirtualizedgraphics/pgdevice)

### Handling Memory-Mapped I/O

- [func mmioRead(atOffset: Int) -> UInt32](/documentation/paravirtualizedgraphics/pgdevice/mmioread(atoffset:))
- [func mmioWrite(atOffset: Int, value: UInt32)](/documentation/paravirtualizedgraphics/pgdevice/mmiowrite(atoffset:value:))

### Suspending and Resuming Graphics Processing

- [func willSuspend()](/documentation/paravirtualizedgraphics/pgdevice/willsuspend())
- [func finishSuspend() -> Data?](/documentation/paravirtualizedgraphics/pgdevice/finishsuspend())
- [func willResume(withSuspendState: Data, error: NSErrorPointer) -> Bool](/documentation/paravirtualizedgraphics/pgdevice/willresume(withsuspendstate:error:))
- [func didResume()](/documentation/paravirtualizedgraphics/pgdevice/didresume())
- [let PGResumeErrorDomain: String](/documentation/paravirtualizedgraphics/pgresumeerrordomain)
- [PGResumeErrorCode](/documentation/paravirtualizedgraphics/pgresumeerrorcode)

#### Errors

- [case incompatibleDevice](/documentation/paravirtualizedgraphics/pgresumeerrorcode/incompatibledevice)
- [case internalFault](/documentation/paravirtualizedgraphics/pgresumeerrorcode/internalfault)
- [case invalidContent](/documentation/paravirtualizedgraphics/pgresumeerrorcode/invalidcontent)
- [case invalidGuestVersion](/documentation/paravirtualizedgraphics/pgresumeerrorcode/invalidguestversion)
- [case invalidSuspendStateVersion](/documentation/paravirtualizedgraphics/pgresumeerrorcode/invalidsuspendstateversion)

#### Enumeration Cases

- [case invalidDisplayPortCount](/documentation/paravirtualizedgraphics/pgresumeerrorcode/invaliddisplayportcount)

#### Initializers

- [init?(rawValue: UInt)](/documentation/paravirtualizedgraphics/pgresumeerrorcode/init(rawvalue:))

### Managing Displays

- [func newDisplay(with: PGDisplayDescriptor, port: Int, serialNum: UInt32) -> (any PGDisplay)?](/documentation/paravirtualizedgraphics/pgdevice/newdisplay(with:port:serialnum:))

### Instance Methods

- [func pause()](/documentation/paravirtualizedgraphics/pgdevice/pause())
- [func reset()](/documentation/paravirtualizedgraphics/pgdevice/reset())
- [func stop()](/documentation/paravirtualizedgraphics/pgdevice/stop())
- [func unpause()](/documentation/paravirtualizedgraphics/pgdevice/unpause())

## Displays

- [PGDisplayDescriptor](/documentation/paravirtualizedgraphics/pgdisplaydescriptor)

### Specifying the Display Properties

- [var name: String?](/documentation/paravirtualizedgraphics/pgdisplaydescriptor/name)
- [var sizeInMillimeters: NSSize](/documentation/paravirtualizedgraphics/pgdisplaydescriptor/sizeinmillimeters)

### Setting the Dispatch Queue

- [var queue: dispatch_queue_t?](/documentation/paravirtualizedgraphics/pgdisplaydescriptor/queue)

### Managing Cursor Events

- [var cursorGlyphHandler: PGDisplayCursorGlyphHandler?](/documentation/paravirtualizedgraphics/pgdisplaydescriptor/cursorglyphhandler)
- [var cursorShowHandler: PGDisplayCursorShowHandler?](/documentation/paravirtualizedgraphics/pgdisplaydescriptor/cursorshowhandler)
- [PGDisplayCursorGlyphHandler](/documentation/paravirtualizedgraphics/pgdisplaycursorglyphhandler)
- [PGDisplayCursorShowHandler](/documentation/paravirtualizedgraphics/pgdisplaycursorshowhandler)

### Handling Mode Changes

- [var modeChangeHandler: PGDisplayModeChangeHandler?](/documentation/paravirtualizedgraphics/pgdisplaydescriptor/modechangehandler)
- [PGDisplayModeChangeHandler](/documentation/paravirtualizedgraphics/pgdisplaymodechangehandler)

### Handling Frame Events

- [var newFrameEventHandler: PGDisplayNewFrameEventHandler?](/documentation/paravirtualizedgraphics/pgdisplaydescriptor/newframeeventhandler)
- [PGDisplayNewFrameEventHandler](/documentation/paravirtualizedgraphics/pgdisplaynewframeeventhandler)

### Instance Properties

- [var cursorMoveHandler: PGDisplayCursorMoveHandler?](/documentation/paravirtualizedgraphics/pgdisplaydescriptor/cursormovehandler)
- [PGDisplay](/documentation/paravirtualizedgraphics/pgdisplay)

### Setting Display Modes

- [var modeList: [PGDisplayMode]](/documentation/paravirtualizedgraphics/pgdisplay/modelist)

### Getting the Guest Cursor Position

- [var cursorPosition: PGDisplayCoord_t](/documentation/paravirtualizedgraphics/pgdisplay/cursorposition)

### Handling Frame Updates

- [var guestPresentCount: Int](/documentation/paravirtualizedgraphics/pgdisplay/guestpresentcount)
- [var hostPresentCount: Int](/documentation/paravirtualizedgraphics/pgdisplay/hostpresentcount)
- [var minimumTextureUsage: MTLTextureUsage](/documentation/paravirtualizedgraphics/pgdisplay/minimumtextureusage)
- [func encodeCurrentFrame(to: any MTLCommandBuffer, texture: any MTLTexture, region: MTLRegion) -> Bool](/documentation/paravirtualizedgraphics/pgdisplay/encodecurrentframe(to:texture:region:))

### Inspecting Display Properties

- [var name: String?](/documentation/paravirtualizedgraphics/pgdisplay/name)
- [var serialNum: UInt32](/documentation/paravirtualizedgraphics/pgdisplay/serialnum)
- [var port: Int](/documentation/paravirtualizedgraphics/pgdisplay/port)
- [var sizeInMillimeters: NSSize](/documentation/paravirtualizedgraphics/pgdisplay/sizeinmillimeters)

### Inspecting the Display Handlers

- [var queue: dispatch_queue_t?](/documentation/paravirtualizedgraphics/pgdisplay/queue)
- [var cursorGlyphHandler: PGDisplayCursorGlyphHandler?](/documentation/paravirtualizedgraphics/pgdisplay/cursorglyphhandler)
- [var cursorShowHandler: PGDisplayCursorShowHandler?](/documentation/paravirtualizedgraphics/pgdisplay/cursorshowhandler)
- [var modeChangeHandler: PGDisplayModeChangeHandler?](/documentation/paravirtualizedgraphics/pgdisplay/modechangehandler)
- [var newFrameEventHandler: PGDisplayNewFrameEventHandler?](/documentation/paravirtualizedgraphics/pgdisplay/newframeeventhandler)

### Instance Properties

- [var cursorMoveHandler: PGDisplayCursorMoveHandler?](/documentation/paravirtualizedgraphics/pgdisplay/cursormovehandler)
- [PGDisplayMode](/documentation/paravirtualizedgraphics/pgdisplaymode)

### Creating a Display Mode

- [init?(sizeInPixels: PGDisplayCoord_t, refreshRateInHz: Double)](/documentation/paravirtualizedgraphics/pgdisplaymode/init(sizeinpixels:refreshrateinhz:))

### Inspecting Mode Properties

- [var sizeInPixels: PGDisplayCoord_t](/documentation/paravirtualizedgraphics/pgdisplaymode/sizeinpixels)
- [var refreshRate: Double](/documentation/paravirtualizedgraphics/pgdisplaymode/refreshrate)
- [PGDisplayCoord_t](/documentation/paravirtualizedgraphics/pgdisplaycoord_t)

### Creating Display Coordinates

- [init()](/documentation/paravirtualizedgraphics/pgdisplaycoord_t/init())
- [init(x: UInt16, y: UInt16)](/documentation/paravirtualizedgraphics/pgdisplaycoord_t/init(x:y:))

### Inspecting Coordinate Values

- [var x: UInt16](/documentation/paravirtualizedgraphics/pgdisplaycoord_t/x)
- [var y: UInt16](/documentation/paravirtualizedgraphics/pgdisplaycoord_t/y)

## Reference

- [ParavirtualizedGraphics Constants](/documentation/paravirtualizedgraphics/paravirtualizedgraphics-constants)

### Constants

- [var PG_SUPPORT_CURSOR_GLYPH_HANDLER2: Int32](/documentation/paravirtualizedgraphics/pg_support_cursor_glyph_handler2)
- [var PG_SUPPORT_DISPLAY_PORT_COUNT: Int32](/documentation/paravirtualizedgraphics/pg_support_display_port_count)
- [var PG_SUPPORT_DISPLAY_SLEEP: Int32](/documentation/paravirtualizedgraphics/pg_support_display_sleep)
- [var PG_SUPPORT_DISPLAY_SLEEP_HANDLER: Int32](/documentation/paravirtualizedgraphics/pg_support_display_sleep_handler)
- [var PG_SUPPORT_MODELIST_RESPONSIVENESS_HANDLER: Int32](/documentation/paravirtualizedgraphics/pg_support_modelist_responsiveness_handler)
- [var PG_SUPPORT_PAUSE_UNPAUSE: Int32](/documentation/paravirtualizedgraphics/pg_support_pause_unpause)
- [var PG_SUPPORT_RESET: Int32](/documentation/paravirtualizedgraphics/pg_support_reset)
- [var PG_SUPPORT_EFI: Int32](/documentation/paravirtualizedgraphics/pg_support_efi)
- [ParavirtualizedGraphics Functions](/documentation/paravirtualizedgraphics/paravirtualizedgraphics-functions)

### Functions

- [func PGMaxDisplayPortCount() -> UInt32](/documentation/paravirtualizedgraphics/pgmaxdisplayportcount())
- [ParavirtualizedGraphics Data Types](/documentation/paravirtualizedgraphics/paravirtualizedgraphics-data-types)

### Data Types

- [PGDisplayCursorMoveHandler](/documentation/paravirtualizedgraphics/pgdisplaycursormovehandler)

## Variables

- [var HAS_NS_BITMAP_HEADER: Int32](/documentation/paravirtualizedgraphics/has_ns_bitmap_header)
- [var PG_SUPPORT_CREATE_DEVICE: Int32](/documentation/paravirtualizedgraphics/pg_support_create_device)

## Functions

- [func PGCreateDeviceWithDescriptor(PGDeviceDescriptor) -> (any PGDevice)?](/documentation/paravirtualizedgraphics/pgcreatedevicewithdescriptor(_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
