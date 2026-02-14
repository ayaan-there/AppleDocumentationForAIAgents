# Dispatch Documentation

Source: https://sosumi.ai/documentation/dispatch

---
title: Dispatch
source: https://developer.apple.com/documentation/dispatch
timestamp: 2026-02-13T18:56:22.348Z
---

## Queues and Tasks

- [DispatchQueue](/documentation/dispatch/dispatchqueue)

### Creating a Dispatch Queue

- [class var main: DispatchQueue](/documentation/dispatch/dispatchqueue/main)
- [class func global(qos: DispatchQoS.QoSClass) -> DispatchQueue](/documentation/dispatch/dispatchqueue/global(qos:))
- [convenience init(label: String, qos: DispatchQoS, attributes: DispatchQueue.Attributes, autoreleaseFrequency: DispatchQueue.AutoreleaseFrequency, target: DispatchQueue?)](/documentation/dispatch/dispatchqueue/init(label:qos:attributes:autoreleasefrequency:target:))
- [DispatchQoS.QoSClass](/documentation/dispatch/dispatchqos/qosclass-swift.enum)

#### Getting the Quality-of-Service Class

- [case userInteractive](/documentation/dispatch/dispatchqos/qosclass-swift.enum/userinteractive)
- [case userInitiated](/documentation/dispatch/dispatchqos/qosclass-swift.enum/userinitiated)
- [case `default`](/documentation/dispatch/dispatchqos/qosclass-swift.enum/default)
- [case utility](/documentation/dispatch/dispatchqos/qosclass-swift.enum/utility)
- [case background](/documentation/dispatch/dispatchqos/qosclass-swift.enum/background)
- [case unspecified](/documentation/dispatch/dispatchqos/qosclass-swift.enum/unspecified)

#### Initializing the Type

- [init?(rawValue: qos_class_t)](/documentation/dispatch/dispatchqos/qosclass-swift.enum/init(rawvalue:))
- [var rawValue: qos_class_t](/documentation/dispatch/dispatchqos/qosclass-swift.enum/rawvalue)
- [DispatchQueue.Attributes](/documentation/dispatch/dispatchqueue/attributes)

#### Attributes

- [static let concurrent: DispatchQueue.Attributes](/documentation/dispatch/dispatchqueue/attributes/concurrent)
- [static let initiallyInactive: DispatchQueue.Attributes](/documentation/dispatch/dispatchqueue/attributes/initiallyinactive)
- [DispatchQueue.AutoreleaseFrequency](/documentation/dispatch/dispatchqueue/autoreleasefrequency)

#### Autorelease Frequencies

- [case inherit](/documentation/dispatch/dispatchqueue/autoreleasefrequency/inherit)
- [case workItem](/documentation/dispatch/dispatchqueue/autoreleasefrequency/workitem)
- [case never](/documentation/dispatch/dispatchqueue/autoreleasefrequency/never)
- [OS_dispatch_queue_main](/documentation/dispatch/os_dispatch_queue_main-swift.class)
- [OS_dispatch_queue_global](/documentation/dispatch/os_dispatch_queue_global-swift.class)
- [DispatchSerialQueue](/documentation/dispatch/dispatchserialqueue)

#### Structures

- [DispatchSerialQueue.Attributes](/documentation/dispatch/dispatchserialqueue/attributes)

##### Type Properties

- [static let initiallyInactive: DispatchSerialQueue.Attributes](/documentation/dispatch/dispatchserialqueue/attributes/initiallyinactive)

#### Initializers

- [convenience init(label: String, qos: DispatchQoS, attributes: DispatchSerialQueue.Attributes, autoreleaseFrequency: DispatchQueue.AutoreleaseFrequency, target: DispatchQueue?)](/documentation/dispatch/dispatchserialqueue/init(label:qos:attributes:autoreleasefrequency:target:))
- [DispatchConcurrentQueue](/documentation/dispatch/dispatchconcurrentqueue)

#### Structures

- [DispatchConcurrentQueue.Attributes](/documentation/dispatch/dispatchconcurrentqueue/attributes)

##### Type Properties

- [static let initiallyInactive: DispatchConcurrentQueue.Attributes](/documentation/dispatch/dispatchconcurrentqueue/attributes/initiallyinactive)

#### Initializers

- [convenience init(label: String, qos: DispatchQoS, attributes: DispatchConcurrentQueue.Attributes, autoreleaseFrequency: DispatchQueue.AutoreleaseFrequency, target: DispatchQueue?)](/documentation/dispatch/dispatchconcurrentqueue/init(label:qos:attributes:autoreleasefrequency:target:))
- [dispatch_queue_main_t](/documentation/dispatch/dispatch_queue_main_t)
- [dispatch_queue_global_t](/documentation/dispatch/dispatch_queue_global_t)
- [dispatch_queue_serial_t](/documentation/dispatch/dispatch_queue_serial_t)
- [dispatch_queue_concurrent_t](/documentation/dispatch/dispatch_queue_concurrent_t)

### Executing Tasks Asynchronously

- [func async(execute: DispatchWorkItem)](/documentation/dispatch/dispatchqueue/async(execute:))
- [func asyncAfter(deadline: DispatchTime, execute: DispatchWorkItem)](/documentation/dispatch/dispatchqueue/asyncafter(deadline:execute:))
- [func asyncAfter(deadline: DispatchTime, qos: DispatchQoS, flags: DispatchWorkItemFlags, execute: () -> Void)](/documentation/dispatch/dispatchqueue/asyncafter(deadline:qos:flags:execute:))
- [func asyncAfter(wallDeadline: DispatchWallTime, execute: DispatchWorkItem)](/documentation/dispatch/dispatchqueue/asyncafter(walldeadline:execute:))
- [func asyncAfter(wallDeadline: DispatchWallTime, qos: DispatchQoS, flags: DispatchWorkItemFlags, execute: () -> Void)](/documentation/dispatch/dispatchqueue/asyncafter(walldeadline:qos:flags:execute:))

### Executing Tasks Synchronously

- [func sync(execute: DispatchWorkItem)](/documentation/dispatch/dispatchqueue/sync(execute:)-2fzvo)
- [func sync(execute: () -> Void)](/documentation/dispatch/dispatchqueue/sync(execute:)-3segw)
- [func sync<T>(execute: () throws -> T) rethrows -> T](/documentation/dispatch/dispatchqueue/sync(execute:)-20xby)
- [func sync<T>(flags: DispatchWorkItemFlags, execute: () throws -> T) rethrows -> T](/documentation/dispatch/dispatchqueue/sync(flags:execute:))
- [func asyncAndWait(execute: () -> Void)](/documentation/dispatch/dispatchqueue/asyncandwait(execute:)-1udeu)

### Executing a Task in Parallel

- [class func concurrentPerform(iterations: Int, execute: (Int) -> Void)](/documentation/dispatch/dispatchqueue/concurrentperform(iterations:execute:))

### Dispatching Work to Groups

- [func async(group: DispatchGroup, execute: DispatchWorkItem)](/documentation/dispatch/dispatchqueue/async(group:execute:))
- [func async(group: DispatchGroup?, qos: DispatchQoS, flags: DispatchWorkItemFlags, execute: () -> Void)](/documentation/dispatch/dispatchqueue/async(group:qos:flags:execute:))

### Managing Queue Attributes

- [var label: String](/documentation/dispatch/dispatchqueue/label)
- [var qos: DispatchQoS](/documentation/dispatch/dispatchqueue/qos)
- [func setTarget(queue: dispatch_queue_t?)](/documentation/dispatch/dispatchobject/settarget(queue:))

### Getting and Setting Contextual Data

- [func setSpecific<T>(key: DispatchSpecificKey<T>, value: T?)](/documentation/dispatch/dispatchqueue/setspecific(key:value:))
- [func getSpecific<T>(key: DispatchSpecificKey<T>) -> T?](/documentation/dispatch/dispatchqueue/getspecific(key:)-swift.method)
- [class func getSpecific<T>(key: DispatchSpecificKey<T>) -> T?](/documentation/dispatch/dispatchqueue/getspecific(key:)-swift.type.method)
- [DispatchSpecificKey](/documentation/dispatch/dispatchspecifickey)

#### Creating a Key

- [init()](/documentation/dispatch/dispatchspecifickey/init())

### Managing the Main Dispatch Queue

- [func dispatchMain() -> Never](/documentation/dispatch/dispatchmain())

### Scheduling Combine Publishers

- [DispatchQueue.SchedulerTimeType](/documentation/dispatch/dispatchqueue/schedulertimetype)

#### Creating Scheduler Times

- [init(DispatchTime)](/documentation/dispatch/dispatchqueue/schedulertimetype/init(_:))

#### Working with Scheduler Time Intervals

- [func advanced(by: DispatchQueue.SchedulerTimeType.Stride) -> DispatchQueue.SchedulerTimeType](/documentation/dispatch/dispatchqueue/schedulertimetype/advanced(by:))
- [func distance(to: DispatchQueue.SchedulerTimeType) -> DispatchQueue.SchedulerTimeType.Stride](/documentation/dispatch/dispatchqueue/schedulertimetype/distance(to:))

#### Inspecting Scheduler Time Properties

- [var dispatchTime: DispatchTime](/documentation/dispatch/dispatchqueue/schedulertimetype/dispatchtime)
- [DispatchQueue.SchedulerOptions](/documentation/dispatch/dispatchqueue/scheduleroptions)

#### Creating Dispatch Queue Scheduler Options

- [init(qos: DispatchQoS, flags: DispatchWorkItemFlags, group: DispatchGroup?)](/documentation/dispatch/dispatchqueue/scheduleroptions/init(qos:flags:group:))

#### Inspecting Scheduler Options

- [var qos: DispatchQoS](/documentation/dispatch/dispatchqueue/scheduleroptions/qos)
- [var flags: DispatchWorkItemFlags](/documentation/dispatch/dispatchqueue/scheduleroptions/flags)
- [var group: DispatchGroup?](/documentation/dispatch/dispatchqueue/scheduleroptions/group)

### Deprecated

- [class func global(priority: DispatchQueue.GlobalQueuePriority) -> DispatchQueue](/documentation/dispatch/dispatchqueue/global(priority:))
- [DispatchQueue.GlobalQueuePriority](/documentation/dispatch/dispatchqueue/globalqueuepriority)

#### Priorities

- [case `default`](/documentation/dispatch/dispatchqueue/globalqueuepriority/default)
- [case high](/documentation/dispatch/dispatchqueue/globalqueuepriority/high)
- [case low](/documentation/dispatch/dispatchqueue/globalqueuepriority/low)
- [case background](/documentation/dispatch/dispatchqueue/globalqueuepriority/background)

### Instance Methods

- [func asyncAfterUnsafe(deadline: DispatchTime, qos: DispatchQoS, flags: DispatchWorkItemFlags, execute: () -> Void)](/documentation/dispatch/dispatchqueue/asyncafterunsafe(deadline:qos:flags:execute:))
- [func asyncAfterUnsafe(wallDeadline: DispatchWallTime, qos: DispatchQoS, flags: DispatchWorkItemFlags, execute: () -> Void)](/documentation/dispatch/dispatchqueue/asyncafterunsafe(walldeadline:qos:flags:execute:))
- [func asyncAndWait<T>(execute: () throws -> T) rethrows -> T](/documentation/dispatch/dispatchqueue/asyncandwait(execute:)-52p9n)
- [func asyncAndWait(execute: DispatchWorkItem)](/documentation/dispatch/dispatchqueue/asyncandwait(execute:)-pfxy)
- [func asyncAndWait<T>(flags: DispatchWorkItemFlags, execute: () throws -> T) rethrows -> T](/documentation/dispatch/dispatchqueue/asyncandwait(flags:execute:))
- [func asyncUnsafe(group: DispatchGroup?, qos: DispatchQoS, flags: DispatchWorkItemFlags, execute: () -> Void)](/documentation/dispatch/dispatchqueue/asyncunsafe(group:qos:flags:execute:))

### Default Implementations

- [Scheduler Implementations](/documentation/dispatch/dispatchqueue/scheduler-implementations)

#### Structures

- [DispatchQueue.SchedulerOptions](/documentation/dispatch/dispatchqueue/scheduleroptions)

##### Creating Dispatch Queue Scheduler Options

- [init(qos: DispatchQoS, flags: DispatchWorkItemFlags, group: DispatchGroup?)](/documentation/dispatch/dispatchqueue/scheduleroptions/init(qos:flags:group:))

##### Inspecting Scheduler Options

- [var qos: DispatchQoS](/documentation/dispatch/dispatchqueue/scheduleroptions/qos)
- [var flags: DispatchWorkItemFlags](/documentation/dispatch/dispatchqueue/scheduleroptions/flags)
- [var group: DispatchGroup?](/documentation/dispatch/dispatchqueue/scheduleroptions/group)
- [DispatchQueue.SchedulerTimeType](/documentation/dispatch/dispatchqueue/schedulertimetype)

##### Creating Scheduler Times

- [init(DispatchTime)](/documentation/dispatch/dispatchqueue/schedulertimetype/init(_:))

##### Working with Scheduler Time Intervals

- [func advanced(by: DispatchQueue.SchedulerTimeType.Stride) -> DispatchQueue.SchedulerTimeType](/documentation/dispatch/dispatchqueue/schedulertimetype/advanced(by:))
- [func distance(to: DispatchQueue.SchedulerTimeType) -> DispatchQueue.SchedulerTimeType.Stride](/documentation/dispatch/dispatchqueue/schedulertimetype/distance(to:))

##### Inspecting Scheduler Time Properties

- [var dispatchTime: DispatchTime](/documentation/dispatch/dispatchqueue/schedulertimetype/dispatchtime)
- [DispatchWorkItem](/documentation/dispatch/dispatchworkitem)

### Creating a Work Item

- [init(qos: DispatchQoS, flags: DispatchWorkItemFlags, block: () -> Void)](/documentation/dispatch/dispatchworkitem/init(qos:flags:block:))
- [DispatchWorkItemFlags](/documentation/dispatch/dispatchworkitemflags)

#### Work Item Flags

- [static let assignCurrentContext: DispatchWorkItemFlags](/documentation/dispatch/dispatchworkitemflags/assigncurrentcontext)
- [static let barrier: DispatchWorkItemFlags](/documentation/dispatch/dispatchworkitemflags/barrier)
- [static let detached: DispatchWorkItemFlags](/documentation/dispatch/dispatchworkitemflags/detached)
- [static let enforceQoS: DispatchWorkItemFlags](/documentation/dispatch/dispatchworkitemflags/enforceqos)
- [static let inheritQoS: DispatchWorkItemFlags](/documentation/dispatch/dispatchworkitemflags/inheritqos)
- [static let noQoS: DispatchWorkItemFlags](/documentation/dispatch/dispatchworkitemflags/noqos)

### Executing the Work Item

- [func perform()](/documentation/dispatch/dispatchworkitem/perform())

### Adding a Completion Handler

- [func notify(queue: DispatchQueue, execute: DispatchWorkItem)](/documentation/dispatch/dispatchworkitem/notify(queue:execute:))
- [func notify(qos: DispatchQoS, flags: DispatchWorkItemFlags, queue: DispatchQueue, execute: () -> Void)](/documentation/dispatch/dispatchworkitem/notify(qos:flags:queue:execute:))

### Waiting for the Completion of a Work Item

- [func wait()](/documentation/dispatch/dispatchworkitem/wait())
- [func wait(timeout: DispatchTime) -> DispatchTimeoutResult](/documentation/dispatch/dispatchworkitem/wait(timeout:))
- [func wait(wallTimeout: DispatchWallTime) -> DispatchTimeoutResult](/documentation/dispatch/dispatchworkitem/wait(walltimeout:))
- [DispatchTime](/documentation/dispatch/dispatchtime)

#### Getting Well-Known Times

- [static func now() -> DispatchTime](/documentation/dispatch/dispatchtime/now())
- [static let distantFuture: DispatchTime](/documentation/dispatch/dispatchtime/distantfuture)

#### Creating a Dispatch Time Object

- [init(uptimeNanoseconds: UInt64)](/documentation/dispatch/dispatchtime/init(uptimenanoseconds:))

#### Getting the Time

- [let rawValue: dispatch_time_t](/documentation/dispatch/dispatchtime/rawvalue)
- [var uptimeNanoseconds: UInt64](/documentation/dispatch/dispatchtime/uptimenanoseconds)

#### Modifying the Value

- [func advanced(by: DispatchTimeInterval) -> DispatchTime](/documentation/dispatch/dispatchtime/advanced(by:))
- [func distance(to: DispatchTime) -> DispatchTimeInterval](/documentation/dispatch/dispatchtime/distance(to:))

#### Operator Functions

- [func + (DispatchTime, Double) -> DispatchTime](/documentation/dispatch/+(_:_:)-6fmcc)
- [func + (DispatchTime, DispatchTimeInterval) -> DispatchTime](/documentation/dispatch/+(_:_:)-2dcrq)
- [func - (DispatchTime, Double) -> DispatchTime](/documentation/dispatch/-(_:_:)-5l4yh)
- [func - (DispatchTime, DispatchTimeInterval) -> DispatchTime](/documentation/dispatch/-(_:_:)-8usj3)
- [DispatchWallTime](/documentation/dispatch/dispatchwalltime)

#### Getting Well-Known Times

- [static func now() -> DispatchWallTime](/documentation/dispatch/dispatchwalltime/now())
- [static let distantFuture: DispatchWallTime](/documentation/dispatch/dispatchwalltime/distantfuture)

#### Creating a Dispatch Wall Time Object

- [init(timespec: timespec)](/documentation/dispatch/dispatchwalltime/init(timespec:))

#### Getting the Time

- [let rawValue: dispatch_time_t](/documentation/dispatch/dispatchwalltime/rawvalue)

#### Operator Functions

- [func + (DispatchWallTime, DispatchTimeInterval) -> DispatchWallTime](/documentation/dispatch/+(_:_:)-8ylhk)
- [func + (DispatchWallTime, Double) -> DispatchWallTime](/documentation/dispatch/+(_:_:)-8pe6k)
- [func - (DispatchWallTime, Double) -> DispatchWallTime](/documentation/dispatch/-(_:_:)-6jk71)
- [func - (DispatchWallTime, DispatchTimeInterval) -> DispatchWallTime](/documentation/dispatch/-(_:_:)-50bxr)

### Canceling a Work Item

- [func cancel()](/documentation/dispatch/dispatchworkitem/cancel())
- [var isCancelled: Bool](/documentation/dispatch/dispatchworkitem/iscancelled)

### Initializers

- [init(flags: DispatchWorkItemFlags, block: () -> Void)](/documentation/dispatch/dispatchworkitem/init(flags:block:))
- [DispatchGroup](/documentation/dispatch/dispatchgroup)

### Creating a Dispatch Group

- [init()](/documentation/dispatch/dispatchgroup/init())

### Adding a Completion Handler

- [func notify(qos: DispatchQoS, flags: DispatchWorkItemFlags, queue: DispatchQueue, execute: () -> Void)](/documentation/dispatch/dispatchgroup/notify(qos:flags:queue:execute:))
- [func notify(queue: DispatchQueue, work: DispatchWorkItem)](/documentation/dispatch/dispatchgroup/notify(queue:work:))

### Waiting for Tasks to Finish Executing

- [func wait()](/documentation/dispatch/dispatchgroup/wait())
- [func wait(timeout: DispatchTime) -> DispatchTimeoutResult](/documentation/dispatch/dispatchgroup/wait(timeout:))
- [func wait(wallTimeout: DispatchWallTime) -> DispatchTimeoutResult](/documentation/dispatch/dispatchgroup/wait(walltimeout:))

### Updating the Group Manually

- [func enter()](/documentation/dispatch/dispatchgroup/enter())
- [func leave()](/documentation/dispatch/dispatchgroup/leave())
- [Dispatch Queue](/documentation/dispatch/dispatch-queue)

### Creating a Dispatch Queue

- [dispatch_queue_t](/documentation/dispatch/dispatch_queue_t)
- [dispatch_queue_main_t](/documentation/dispatch/dispatch_queue_main_t)
- [dispatch_queue_global_t](/documentation/dispatch/dispatch_queue_global_t)
- [dispatch_queue_serial_t](/documentation/dispatch/dispatch_queue_serial_t)
- [dispatch_queue_concurrent_t](/documentation/dispatch/dispatch_queue_concurrent_t)

### Configuring Queue Execution Parameters

- [dispatch_queue_attr_t](/documentation/dispatch/dispatch_queue_attr_t)

### Executing Tasks Synchronously

- [func sync(execute: () -> Void)](/documentation/dispatch/dispatchqueue/sync(execute:)-3segw)
- [func asyncAndWait(execute: () -> Void)](/documentation/dispatch/dispatchqueue/asyncandwait(execute:)-1udeu)

### Managing Queue Attributes

- [func setTarget(queue: dispatch_queue_t?)](/documentation/dispatch/dispatchobject/settarget(queue:))

### Managing the Main Dispatch Queue

- [func dispatchMain() -> Never](/documentation/dispatch/dispatchmain())
- [Dispatch Work Item](/documentation/dispatch/dispatch-work-item)
- [Dispatch Group](/documentation/dispatch/dispatch-group)

### Creating a Dispatch Group

- [init()](/documentation/dispatch/dispatchgroup/init())
- [dispatch_group_t](/documentation/dispatch/dispatch_group_t)

### Updating the Group Manually

- [func enter()](/documentation/dispatch/dispatchgroup/enter())
- [func leave()](/documentation/dispatch/dispatchgroup/leave())
- [Workloop](/documentation/dispatch/workloop)

### Creating a Dispatch Workloop

- [dispatch_workloop_t](/documentation/dispatch/dispatch_workloop_t)

### Executing Tasks Synchronously

- [func sync(execute: () -> Void)](/documentation/dispatch/dispatchqueue/sync(execute:)-3segw)
- [func asyncAndWait(execute: () -> Void)](/documentation/dispatch/dispatchqueue/asyncandwait(execute:)-1udeu)

### Managing Queue Attributes

- [func setTarget(queue: dispatch_queue_t?)](/documentation/dispatch/dispatchobject/settarget(queue:))

## Thread Scheduling

- [DispatchQoS](/documentation/dispatch/dispatchqos)

### Getting the Predefined QoS Objects

- [static let userInteractive: DispatchQoS](/documentation/dispatch/dispatchqos/userinteractive)
- [static let userInitiated: DispatchQoS](/documentation/dispatch/dispatchqos/userinitiated)
- [static let `default`: DispatchQoS](/documentation/dispatch/dispatchqos/default)
- [static let utility: DispatchQoS](/documentation/dispatch/dispatchqos/utility)
- [static let background: DispatchQoS](/documentation/dispatch/dispatchqos/background)
- [static let unspecified: DispatchQoS](/documentation/dispatch/dispatchqos/unspecified)

### Creating a QoS Structure

- [init(qosClass: DispatchQoS.QoSClass, relativePriority: Int)](/documentation/dispatch/dispatchqos/init(qosclass:relativepriority:))
- [DispatchQoS.QoSClass](/documentation/dispatch/dispatchqos/qosclass-swift.enum)

#### Getting the Quality-of-Service Class

- [case userInteractive](/documentation/dispatch/dispatchqos/qosclass-swift.enum/userinteractive)
- [case userInitiated](/documentation/dispatch/dispatchqos/qosclass-swift.enum/userinitiated)
- [case `default`](/documentation/dispatch/dispatchqos/qosclass-swift.enum/default)
- [case utility](/documentation/dispatch/dispatchqos/qosclass-swift.enum/utility)
- [case background](/documentation/dispatch/dispatchqos/qosclass-swift.enum/background)
- [case unspecified](/documentation/dispatch/dispatchqos/qosclass-swift.enum/unspecified)

#### Initializing the Type

- [init?(rawValue: qos_class_t)](/documentation/dispatch/dispatchqos/qosclass-swift.enum/init(rawvalue:))
- [var rawValue: qos_class_t](/documentation/dispatch/dispatchqos/qosclass-swift.enum/rawvalue)

### Getting the QoS Attributes

- [let qosClass: DispatchQoS.QoSClass](/documentation/dispatch/dispatchqos/qosclass-swift.property)
- [let relativePriority: Int](/documentation/dispatch/dispatchqos/relativepriority)

## System Event Monitoring

- [DispatchSource](/documentation/dispatch/dispatchsource)

### Managing Common Dispatch Source Properties

- [DispatchSourceProtocol](/documentation/dispatch/dispatchsourceprotocol)

#### Activating, Suspending, and Resuming a Source

- [func activate()](/documentation/dispatch/dispatchsourceprotocol/activate())
- [func suspend()](/documentation/dispatch/dispatchsourceprotocol/suspend())
- [func resume()](/documentation/dispatch/dispatchsourceprotocol/resume())

#### Canceling a Dispatch Source

- [func cancel()](/documentation/dispatch/dispatchsourceprotocol/cancel())
- [var isCancelled: Bool](/documentation/dispatch/dispatchsourceprotocol/iscancelled)
- [func setCancelHandler(handler: DispatchWorkItem)](/documentation/dispatch/dispatchsourceprotocol/setcancelhandler(handler:))
- [func setCancelHandler(qos: DispatchQoS, flags: DispatchWorkItemFlags, handler: Self.DispatchSourceHandler?)](/documentation/dispatch/dispatchsourceprotocol/setcancelhandler(qos:flags:handler:))

#### Installing Event Handlers

- [func setEventHandler(handler: DispatchWorkItem)](/documentation/dispatch/dispatchsourceprotocol/seteventhandler(handler:))
- [func setEventHandler(qos: DispatchQoS, flags: DispatchWorkItemFlags, handler: Self.DispatchSourceHandler?)](/documentation/dispatch/dispatchsourceprotocol/seteventhandler(qos:flags:handler:))
- [func setRegistrationHandler(handler: DispatchWorkItem)](/documentation/dispatch/dispatchsourceprotocol/setregistrationhandler(handler:))
- [func setRegistrationHandler(qos: DispatchQoS, flags: DispatchWorkItemFlags, handler: Self.DispatchSourceHandler?)](/documentation/dispatch/dispatchsourceprotocol/setregistrationhandler(qos:flags:handler:))
- [DispatchSourceProtocol.DispatchSourceHandler](/documentation/dispatch/dispatchsourceprotocol/dispatchsourcehandler)

#### Getting the Dispatch Source Attributes

- [var handle: UInt](/documentation/dispatch/dispatchsourceprotocol/handle)
- [var data: UInt](/documentation/dispatch/dispatchsourceprotocol/data)
- [var mask: UInt](/documentation/dispatch/dispatchsourceprotocol/mask)

### Creating a Timer Source

- [class func makeTimerSource(flags: DispatchSource.TimerFlags, queue: DispatchQueue?) -> any DispatchSourceTimer](/documentation/dispatch/dispatchsource/maketimersource(flags:queue:))
- [DispatchSourceTimer](/documentation/dispatch/dispatchsourcetimer)

#### Scheduling the Timer Trigger Conditions

- [func schedule(deadline: DispatchTime, repeating: DispatchTimeInterval, leeway: DispatchTimeInterval)](/documentation/dispatch/dispatchsourcetimer/schedule(deadline:repeating:leeway:)-hvhp)
- [func schedule(deadline: DispatchTime, repeating: Double, leeway: DispatchTimeInterval)](/documentation/dispatch/dispatchsourcetimer/schedule(deadline:repeating:leeway:)-24w9r)
- [func schedule(wallDeadline: DispatchWallTime, repeating: DispatchTimeInterval, leeway: DispatchTimeInterval)](/documentation/dispatch/dispatchsourcetimer/schedule(walldeadline:repeating:leeway:)-7c4d7)
- [func schedule(wallDeadline: DispatchWallTime, repeating: Double, leeway: DispatchTimeInterval)](/documentation/dispatch/dispatchsourcetimer/schedule(walldeadline:repeating:leeway:)-21bay)

#### Deprecated

- [func scheduleOneshot(deadline: DispatchTime, leeway: DispatchTimeInterval)](/documentation/dispatch/dispatchsourcetimer/scheduleoneshot(deadline:leeway:))
- [func scheduleOneshot(wallDeadline: DispatchWallTime, leeway: DispatchTimeInterval)](/documentation/dispatch/dispatchsourcetimer/scheduleoneshot(walldeadline:leeway:))
- [func scheduleRepeating(deadline: DispatchTime, interval: DispatchTimeInterval, leeway: DispatchTimeInterval)](/documentation/dispatch/dispatchsourcetimer/schedulerepeating(deadline:interval:leeway:)-3k199)
- [func scheduleRepeating(deadline: DispatchTime, interval: Double, leeway: DispatchTimeInterval)](/documentation/dispatch/dispatchsourcetimer/schedulerepeating(deadline:interval:leeway:)-4wtot)
- [func scheduleRepeating(wallDeadline: DispatchWallTime, interval: Double, leeway: DispatchTimeInterval)](/documentation/dispatch/dispatchsourcetimer/schedulerepeating(walldeadline:interval:leeway:)-6fiox)
- [func scheduleRepeating(wallDeadline: DispatchWallTime, interval: DispatchTimeInterval, leeway: DispatchTimeInterval)](/documentation/dispatch/dispatchsourcetimer/schedulerepeating(walldeadline:interval:leeway:)-942p7)
- [DispatchSource.TimerFlags](/documentation/dispatch/dispatchsource/timerflags)

#### Timer Flags

- [static let strict: DispatchSource.TimerFlags](/documentation/dispatch/dispatchsource/timerflags/strict)

### Creating a File System Source

- [class func makeReadSource(fileDescriptor: Int32, queue: DispatchQueue?) -> any DispatchSourceRead](/documentation/dispatch/dispatchsource/makereadsource(filedescriptor:queue:))
- [class func makeWriteSource(fileDescriptor: Int32, queue: DispatchQueue?) -> any DispatchSourceWrite](/documentation/dispatch/dispatchsource/makewritesource(filedescriptor:queue:))
- [class func makeFileSystemObjectSource(fileDescriptor: Int32, eventMask: DispatchSource.FileSystemEvent, queue: DispatchQueue?) -> any DispatchSourceFileSystemObject](/documentation/dispatch/dispatchsource/makefilesystemobjectsource(filedescriptor:eventmask:queue:))
- [DispatchSourceRead](/documentation/dispatch/dispatchsourceread)
- [DispatchSourceWrite](/documentation/dispatch/dispatchsourcewrite)
- [DispatchSourceFileSystemObject](/documentation/dispatch/dispatchsourcefilesystemobject)

#### Getting the Data Handle

- [var handle: Int32](/documentation/dispatch/dispatchsourcefilesystemobject/handle)

#### Getting the Event Data

- [var data: DispatchSource.FileSystemEvent](/documentation/dispatch/dispatchsourcefilesystemobject/data)
- [var mask: DispatchSource.FileSystemEvent](/documentation/dispatch/dispatchsourcefilesystemobject/mask)
- [DispatchSource.FileSystemEvent](/documentation/dispatch/dispatchsource/filesystemevent)

#### File System Event Flags

- [static let all: DispatchSource.FileSystemEvent](/documentation/dispatch/dispatchsource/filesystemevent/all)
- [static let attrib: DispatchSource.FileSystemEvent](/documentation/dispatch/dispatchsource/filesystemevent/attrib)
- [static let delete: DispatchSource.FileSystemEvent](/documentation/dispatch/dispatchsource/filesystemevent/delete)
- [static let extend: DispatchSource.FileSystemEvent](/documentation/dispatch/dispatchsource/filesystemevent/extend)
- [static let funlock: DispatchSource.FileSystemEvent](/documentation/dispatch/dispatchsource/filesystemevent/funlock)
- [static let link: DispatchSource.FileSystemEvent](/documentation/dispatch/dispatchsource/filesystemevent/link)
- [static let rename: DispatchSource.FileSystemEvent](/documentation/dispatch/dispatchsource/filesystemevent/rename)
- [static let revoke: DispatchSource.FileSystemEvent](/documentation/dispatch/dispatchsource/filesystemevent/revoke)
- [static let write: DispatchSource.FileSystemEvent](/documentation/dispatch/dispatchsource/filesystemevent/write)

### Creating a Process Source

- [class func makeProcessSource(identifier: pid_t, eventMask: DispatchSource.ProcessEvent, queue: DispatchQueue?) -> any DispatchSourceProcess](/documentation/dispatch/dispatchsource/makeprocesssource(identifier:eventmask:queue:))
- [DispatchSourceProcess](/documentation/dispatch/dispatchsourceprocess)

#### Getting the Process ID

- [var handle: pid_t](/documentation/dispatch/dispatchsourceprocess/handle)

#### Getting the Event Data

- [var data: DispatchSource.ProcessEvent](/documentation/dispatch/dispatchsourceprocess/data)
- [var mask: DispatchSource.ProcessEvent](/documentation/dispatch/dispatchsourceprocess/mask)
- [DispatchSource.ProcessEvent](/documentation/dispatch/dispatchsource/processevent)

#### Process Event Flags

- [static let all: DispatchSource.ProcessEvent](/documentation/dispatch/dispatchsource/processevent/all)
- [static let exec: DispatchSource.ProcessEvent](/documentation/dispatch/dispatchsource/processevent/exec)
- [static let exit: DispatchSource.ProcessEvent](/documentation/dispatch/dispatchsource/processevent/exit)
- [static let fork: DispatchSource.ProcessEvent](/documentation/dispatch/dispatchsource/processevent/fork)
- [static let signal: DispatchSource.ProcessEvent](/documentation/dispatch/dispatchsource/processevent/signal)

### Creating a Memory Pressure Source

- [class func makeMemoryPressureSource(eventMask: DispatchSource.MemoryPressureEvent, queue: DispatchQueue?) -> any DispatchSourceMemoryPressure](/documentation/dispatch/dispatchsource/makememorypressuresource(eventmask:queue:))
- [DispatchSourceMemoryPressure](/documentation/dispatch/dispatchsourcememorypressure)

#### Getting the Event Data

- [var data: DispatchSource.MemoryPressureEvent](/documentation/dispatch/dispatchsourcememorypressure/data)
- [var mask: DispatchSource.MemoryPressureEvent](/documentation/dispatch/dispatchsourcememorypressure/mask)
- [DispatchSource.MemoryPressureEvent](/documentation/dispatch/dispatchsource/memorypressureevent)

#### Memory Pressure Event Flags

- [static let all: DispatchSource.MemoryPressureEvent](/documentation/dispatch/dispatchsource/memorypressureevent/all)
- [static let normal: DispatchSource.MemoryPressureEvent](/documentation/dispatch/dispatchsource/memorypressureevent/normal)
- [static let warning: DispatchSource.MemoryPressureEvent](/documentation/dispatch/dispatchsource/memorypressureevent/warning)
- [static let critical: DispatchSource.MemoryPressureEvent](/documentation/dispatch/dispatchsource/memorypressureevent/critical)

### Creating a Signal Source

- [class func makeSignalSource(signal: Int32, queue: DispatchQueue?) -> any DispatchSourceSignal](/documentation/dispatch/dispatchsource/makesignalsource(signal:queue:))
- [DispatchSourceSignal](/documentation/dispatch/dispatchsourcesignal)

### Creating a Mach Port Source

- [class func makeMachReceiveSource(port: mach_port_t, queue: DispatchQueue?) -> any DispatchSourceMachReceive](/documentation/dispatch/dispatchsource/makemachreceivesource(port:queue:))
- [class func makeMachSendSource(port: mach_port_t, eventMask: DispatchSource.MachSendEvent, queue: DispatchQueue?) -> any DispatchSourceMachSend](/documentation/dispatch/dispatchsource/makemachsendsource(port:eventmask:queue:))
- [DispatchSourceMachReceive](/documentation/dispatch/dispatchsourcemachreceive)

#### Getting the Mach Port Handle

- [var handle: mach_port_t](/documentation/dispatch/dispatchsourcemachreceive/handle)
- [DispatchSourceMachSend](/documentation/dispatch/dispatchsourcemachsend)

#### Getting the Mach Port Handle

- [var handle: mach_port_t](/documentation/dispatch/dispatchsourcemachsend/handle)

#### Getting the Event Data

- [var data: DispatchSource.MachSendEvent](/documentation/dispatch/dispatchsourcemachsend/data)
- [var mask: DispatchSource.MachSendEvent](/documentation/dispatch/dispatchsourcemachsend/mask)
- [DispatchSource.MachSendEvent](/documentation/dispatch/dispatchsource/machsendevent)

#### Mach Event Flags

- [static let dead: DispatchSource.MachSendEvent](/documentation/dispatch/dispatchsource/machsendevent/dead)

### Creating a Custom Source

- [class func makeUserDataAddSource(queue: DispatchQueue?) -> any DispatchSourceUserDataAdd](/documentation/dispatch/dispatchsource/makeuserdataaddsource(queue:))
- [class func makeUserDataOrSource(queue: DispatchQueue?) -> any DispatchSourceUserDataOr](/documentation/dispatch/dispatchsource/makeuserdataorsource(queue:))
- [class func makeUserDataReplaceSource(queue: DispatchQueue?) -> any DispatchSourceUserDataReplace](/documentation/dispatch/dispatchsource/makeuserdatareplacesource(queue:))
- [DispatchSourceUserDataAdd](/documentation/dispatch/dispatchsourceuserdataadd)

#### Getting the Event Data

- [func add(data: UInt)](/documentation/dispatch/dispatchsourceuserdataadd/add(data:))
- [DispatchSourceUserDataOr](/documentation/dispatch/dispatchsourceuserdataor)

#### Getting the Event Data

- [func or(data: UInt)](/documentation/dispatch/dispatchsourceuserdataor/or(data:))
- [DispatchSourceUserDataReplace](/documentation/dispatch/dispatchsourceuserdatareplace)

#### Getting the Event Data

- [func replace(data: UInt)](/documentation/dispatch/dispatchsourceuserdatareplace/replace(data:))
- [Dispatch Source](/documentation/dispatch/dispatch-source)

### Creating a Dispatch Source

- [dispatch_source_t](/documentation/dispatch/dispatch_source_t)

### Getting Dispatch Source Attributes

- [dispatch_source_mach_recv_flags_t](/documentation/dispatch/dispatch_source_mach_recv_flags_t)
- [DispatchIO](/documentation/dispatch/dispatchio)

### Creating a Dispatch I/O Object

- [convenience init(type: DispatchIO.StreamType, fileDescriptor: Int32, queue: DispatchQueue, cleanupHandler: (Int32) -> Void)](/documentation/dispatch/dispatchio/init(type:filedescriptor:queue:cleanuphandler:))
- [convenience init?(type: DispatchIO.StreamType, path: UnsafePointer<Int8>, oflag: Int32, mode: mode_t, queue: DispatchQueue, cleanupHandler: (Int32) -> Void)](/documentation/dispatch/dispatchio/init(type:path:oflag:mode:queue:cleanuphandler:)-50rb0)
- [convenience init(type: DispatchIO.StreamType, io: DispatchIO, queue: DispatchQueue, cleanupHandler: (Int32) -> Void)](/documentation/dispatch/dispatchio/init(type:io:queue:cleanuphandler:))
- [DispatchIO.StreamType](/documentation/dispatch/dispatchio/streamtype)

#### Stream Types

- [case stream](/documentation/dispatch/dispatchio/streamtype/stream)
- [case random](/documentation/dispatch/dispatchio/streamtype/random)

#### Initializing the Type

- [var DISPATCH_IO_RANDOM: Int32](/documentation/dispatch/dispatch_io_random)
- [var DISPATCH_IO_STREAM: Int32](/documentation/dispatch/dispatch_io_stream)

### Reading from the File

- [func read(offset: off_t, length: Int, queue: DispatchQueue, ioHandler: (Bool, DispatchData?, Int32) -> Void)](/documentation/dispatch/dispatchio/read(offset:length:queue:iohandler:))
- [class func read(fromFileDescriptor: Int32, maxLength: Int, runningHandlerOn: DispatchQueue, handler: (DispatchData, Int32) -> Void)](/documentation/dispatch/dispatchio/read(fromfiledescriptor:maxlength:runninghandleron:handler:))

### Writing to the File

- [func write(offset: off_t, data: DispatchData, queue: DispatchQueue, ioHandler: (Bool, DispatchData?, Int32) -> Void)](/documentation/dispatch/dispatchio/write(offset:data:queue:iohandler:))
- [class func write(toFileDescriptor: Int32, data: DispatchData, runningHandlerOn: DispatchQueue, handler: (DispatchData?, Int32) -> Void)](/documentation/dispatch/dispatchio/write(tofiledescriptor:data:runninghandleron:handler:))

### Closing the File

- [func close(flags: DispatchIO.CloseFlags)](/documentation/dispatch/dispatchio/close(flags:))
- [DispatchIO.CloseFlags](/documentation/dispatch/dispatchio/closeflags)

#### Close Flags

- [static let stop: DispatchIO.CloseFlags](/documentation/dispatch/dispatchio/closeflags/stop)

#### Initializing the Type

- [var DISPATCH_IO_STOP: Int32](/documentation/dispatch/dispatch_io_stop)

### Managing the File Descriptor

- [var fileDescriptor: Int32](/documentation/dispatch/dispatchio/filedescriptor)
- [func setLimit(highWater: Int)](/documentation/dispatch/dispatchio/setlimit(highwater:))
- [func setLimit(lowWater: Int)](/documentation/dispatch/dispatchio/setlimit(lowwater:))
- [func setInterval(interval: DispatchTimeInterval, flags: DispatchIO.IntervalFlags)](/documentation/dispatch/dispatchio/setinterval(interval:flags:))
- [DispatchIO.IntervalFlags](/documentation/dispatch/dispatchio/intervalflags)

#### Interval Flags

- [static let strictInterval: DispatchIO.IntervalFlags](/documentation/dispatch/dispatchio/intervalflags/strictinterval)
- [var DISPATCH_IO_STRICT_INTERVAL: Int32](/documentation/dispatch/dispatch_io_strict_interval)

#### Initializing the Type

- [init(nilLiteral: ())](/documentation/dispatch/dispatchio/intervalflags/init(nilliteral:))

### Synchronizing File Operations

- [func barrier(execute: () -> Void)](/documentation/dispatch/dispatchio/barrier(execute:))

### Initializers

- [convenience init(type: DispatchIO.StreamType, path: UnsafePointer<Int8>, oflag: Int32, mode: mode_t, queue: DispatchQueue, cleanupHandler: (Int32) -> Void)](/documentation/dispatch/dispatchio/init(type:path:oflag:mode:queue:cleanuphandler:)-25rlb)
- [DispatchData](/documentation/dispatch/dispatchdata)

### Creating a Dispatch Data Structure

- [init(bytes: UnsafeRawBufferPointer)](/documentation/dispatch/dispatchdata/init(bytes:)-9lrd)
- [init(bytesNoCopy: UnsafeRawBufferPointer, deallocator: DispatchData.Deallocator)](/documentation/dispatch/dispatchdata/init(bytesnocopy:deallocator:)-vfoe)
- [func withUnsafeBytes<Result, ContentType>(body: (UnsafePointer<ContentType>) throws -> Result) rethrows -> Result](/documentation/dispatch/dispatchdata/withunsafebytes(body:))
- [DispatchData.Deallocator](/documentation/dispatch/dispatchdata/deallocator)

#### Deallocators

- [case free](/documentation/dispatch/dispatchdata/deallocator/free)
- [case unmap](/documentation/dispatch/dispatchdata/deallocator/unmap)
- [case custom(DispatchQueue?, () -> Void)](/documentation/dispatch/dispatchdata/deallocator/custom(_:_:))
- [static let empty: DispatchData](/documentation/dispatch/dispatchdata/empty)

### Appending Data to the Buffer

- [func append(DispatchData)](/documentation/dispatch/dispatchdata/append(_:)-3bvdr)
- [func append<SourceType>(UnsafeBufferPointer<SourceType>)](/documentation/dispatch/dispatchdata/append(_:)-9sgkq)
- [func append(UnsafeRawBufferPointer)](/documentation/dispatch/dispatchdata/append(_:)-1m94x)

### Copying Bytes

- [func copyBytes(to: UnsafeMutableRawBufferPointer, count: Int)](/documentation/dispatch/dispatchdata/copybytes(to:count:)-3j0qx)
- [func copyBytes<DestinationType>(to: UnsafeMutableBufferPointer<DestinationType>, from: Range<DispatchData.Index>?) -> Int](/documentation/dispatch/dispatchdata/copybytes(to:from:)-7zz4y)
- [func copyBytes(to: UnsafeMutableRawBufferPointer, from: Range<DispatchData.Index>)](/documentation/dispatch/dispatchdata/copybytes(to:from:)-60yai)

### Accessing Buffer Data

- [subscript(DispatchData.Index) -> UInt8](/documentation/dispatch/dispatchdata/subscript(_:))
- [func region(location: Int) -> (data: DispatchData, offset: Int)](/documentation/dispatch/dispatchdata/region(location:))
- [DispatchData.Region](/documentation/dispatch/dispatchdata/region)

#### Accessing the Region

- [subscript(DispatchData.Index) -> UInt8](/documentation/dispatch/dispatchdata/subscript(_:))

### Iterating Over the Buffer Contents

- [func makeIterator() -> DispatchData.Iterator](/documentation/dispatch/dispatchdata/makeiterator())
- [func enumerateBytes((UnsafeBufferPointer<UInt8>, Int, inout Bool) -> Void)](/documentation/dispatch/dispatchdata/enumeratebytes(_:))

### Retrieving Buffer Subsequences

- [func subdata(in: Range<DispatchData.Index>) -> DispatchData](/documentation/dispatch/dispatchdata/subdata(in:))

### Combining Sequence Elements

- [func append(DispatchData)](/documentation/dispatch/dispatchdata/append(_:)-3bvdr)
- [func append<SourceType>(UnsafeBufferPointer<SourceType>)](/documentation/dispatch/dispatchdata/append(_:)-9sgkq)
- [func append(UnsafeRawBufferPointer)](/documentation/dispatch/dispatchdata/append(_:)-1m94x)
- [func append(UnsafePointer<UInt8>, count: Int)](/documentation/dispatch/dispatchdata/append(_:count:))
- [func copyBytes(to: UnsafeMutablePointer<UInt8>, count: Int)](/documentation/dispatch/dispatchdata/copybytes(to:count:)-4ffyj)
- [func copyBytes(to: UnsafeMutableRawBufferPointer, count: Int)](/documentation/dispatch/dispatchdata/copybytes(to:count:)-3j0qx)
- [func copyBytes<DestinationType>(to: UnsafeMutableBufferPointer<DestinationType>, from: Range<DispatchData.Index>?) -> Int](/documentation/dispatch/dispatchdata/copybytes(to:from:)-7zz4y)
- [func copyBytes(to: UnsafeMutablePointer<UInt8>, from: Range<DispatchData.Index>)](/documentation/dispatch/dispatchdata/copybytes(to:from:)-6ztcb)
- [func copyBytes(to: UnsafeMutableRawBufferPointer, from: Range<DispatchData.Index>)](/documentation/dispatch/dispatchdata/copybytes(to:from:)-60yai)
- [func enumerateBytes((UnsafeBufferPointer<UInt8>, Int, inout Bool) -> Void)](/documentation/dispatch/dispatchdata/enumeratebytes(_:))
- [func makeIterator() -> DispatchData.Iterator](/documentation/dispatch/dispatchdata/makeiterator())
- [func region(location: Int) -> (data: DispatchData, offset: Int)](/documentation/dispatch/dispatchdata/region(location:))
- [func subdata(in: Range<DispatchData.Index>) -> DispatchData](/documentation/dispatch/dispatchdata/subdata(in:))
- [func withUnsafeBytes<Result, ContentType>(body: (UnsafePointer<ContentType>) throws -> Result) rethrows -> Result](/documentation/dispatch/dispatchdata/withunsafebytes(body:))

### Deprecated

- [init(bytes: UnsafeBufferPointer<UInt8>)](/documentation/dispatch/dispatchdata/init(bytes:)-mkbp)
- [init(bytesNoCopy: UnsafeBufferPointer<UInt8>, deallocator: DispatchData.Deallocator)](/documentation/dispatch/dispatchdata/init(bytesnocopy:deallocator:)-7h08w)
- [func append(UnsafePointer<UInt8>, count: Int)](/documentation/dispatch/dispatchdata/append(_:count:))
- [func copyBytes(to: UnsafeMutablePointer<UInt8>, count: Int)](/documentation/dispatch/dispatchdata/copybytes(to:count:)-4ffyj)
- [func copyBytes(to: UnsafeMutablePointer<UInt8>, from: Range<DispatchData.Index>)](/documentation/dispatch/dispatchdata/copybytes(to:from:)-6ztcb)

### Instance Methods

- [func enumerateBytes(block: (UnsafeBufferPointer<UInt8>, Int, inout Bool) -> Void)](/documentation/dispatch/dispatchdata/enumeratebytes(block:))
- [DispatchDataIterator](/documentation/dispatch/dispatchdataiterator)

### Iterating Over a Sequence’s Elements

- [func next() -> DispatchData.Element?](/documentation/dispatch/dispatchdataiterator/next())
- [Dispatch I/O](/documentation/dispatch/dispatch-i-o)

### Creating a Dispatch I/O Object

- [dispatch_io_t](/documentation/dispatch/dispatch_io_t)

### Managing the File Descriptor

- [var fileDescriptor: Int32](/documentation/dispatch/dispatchio/filedescriptor)
- [func setLimit(lowWater: Int)](/documentation/dispatch/dispatchio/setlimit(lowwater:))
- [func setLimit(highWater: Int)](/documentation/dispatch/dispatchio/setlimit(highwater:))

### Synchronizing File Operations

- [func barrier(execute: () -> Void)](/documentation/dispatch/dispatchio/barrier(execute:))
- [Dispatch Data](/documentation/dispatch/dispatch-data)

### Creating a Dispatch Data Object

- [dispatch_data_t](/documentation/dispatch/dispatch_data_t)
- [DispatchSourceProtocol](/documentation/dispatch/dispatchsourceprotocol)

### Activating, Suspending, and Resuming a Source

- [func activate()](/documentation/dispatch/dispatchsourceprotocol/activate())
- [func suspend()](/documentation/dispatch/dispatchsourceprotocol/suspend())
- [func resume()](/documentation/dispatch/dispatchsourceprotocol/resume())

### Canceling a Dispatch Source

- [func cancel()](/documentation/dispatch/dispatchsourceprotocol/cancel())
- [var isCancelled: Bool](/documentation/dispatch/dispatchsourceprotocol/iscancelled)
- [func setCancelHandler(handler: DispatchWorkItem)](/documentation/dispatch/dispatchsourceprotocol/setcancelhandler(handler:))
- [func setCancelHandler(qos: DispatchQoS, flags: DispatchWorkItemFlags, handler: Self.DispatchSourceHandler?)](/documentation/dispatch/dispatchsourceprotocol/setcancelhandler(qos:flags:handler:))

### Installing Event Handlers

- [func setEventHandler(handler: DispatchWorkItem)](/documentation/dispatch/dispatchsourceprotocol/seteventhandler(handler:))
- [func setEventHandler(qos: DispatchQoS, flags: DispatchWorkItemFlags, handler: Self.DispatchSourceHandler?)](/documentation/dispatch/dispatchsourceprotocol/seteventhandler(qos:flags:handler:))
- [func setRegistrationHandler(handler: DispatchWorkItem)](/documentation/dispatch/dispatchsourceprotocol/setregistrationhandler(handler:))
- [func setRegistrationHandler(qos: DispatchQoS, flags: DispatchWorkItemFlags, handler: Self.DispatchSourceHandler?)](/documentation/dispatch/dispatchsourceprotocol/setregistrationhandler(qos:flags:handler:))
- [DispatchSourceProtocol.DispatchSourceHandler](/documentation/dispatch/dispatchsourceprotocol/dispatchsourcehandler)

### Getting the Dispatch Source Attributes

- [var handle: UInt](/documentation/dispatch/dispatchsourceprotocol/handle)
- [var data: UInt](/documentation/dispatch/dispatchsourceprotocol/data)
- [var mask: UInt](/documentation/dispatch/dispatchsourceprotocol/mask)

## Task Synchronization

- [DispatchSemaphore](/documentation/dispatch/dispatchsemaphore)

### Creating a Semaphore

- [init(value: Int)](/documentation/dispatch/dispatchsemaphore/init(value:))

### Signaling the Semaphore

- [func signal() -> Int](/documentation/dispatch/dispatchsemaphore/signal())

### Blocking on the Semaphore

- [func wait()](/documentation/dispatch/dispatchsemaphore/wait())
- [func wait(timeout: DispatchTime) -> DispatchTimeoutResult](/documentation/dispatch/dispatchsemaphore/wait(timeout:))
- [func wait(wallTimeout: DispatchWallTime) -> DispatchTimeoutResult](/documentation/dispatch/dispatchsemaphore/wait(walltimeout:))
- [Dispatch Semaphore](/documentation/dispatch/dispatch-semaphore)

### Creating a Semaphore

- [init(value: Int)](/documentation/dispatch/dispatchsemaphore/init(value:))
- [dispatch_semaphore_t](/documentation/dispatch/dispatch_semaphore_t)
- [Dispatch Barrier](/documentation/dispatch/dispatch-barrier)

## Time Constructs

- [DispatchTime](/documentation/dispatch/dispatchtime)

### Getting Well-Known Times

- [static func now() -> DispatchTime](/documentation/dispatch/dispatchtime/now())
- [static let distantFuture: DispatchTime](/documentation/dispatch/dispatchtime/distantfuture)

### Creating a Dispatch Time Object

- [init(uptimeNanoseconds: UInt64)](/documentation/dispatch/dispatchtime/init(uptimenanoseconds:))

### Getting the Time

- [let rawValue: dispatch_time_t](/documentation/dispatch/dispatchtime/rawvalue)
- [var uptimeNanoseconds: UInt64](/documentation/dispatch/dispatchtime/uptimenanoseconds)

### Modifying the Value

- [func advanced(by: DispatchTimeInterval) -> DispatchTime](/documentation/dispatch/dispatchtime/advanced(by:))
- [func distance(to: DispatchTime) -> DispatchTimeInterval](/documentation/dispatch/dispatchtime/distance(to:))

### Operator Functions

- [func + (DispatchTime, Double) -> DispatchTime](/documentation/dispatch/+(_:_:)-6fmcc)
- [func + (DispatchTime, DispatchTimeInterval) -> DispatchTime](/documentation/dispatch/+(_:_:)-2dcrq)
- [func - (DispatchTime, Double) -> DispatchTime](/documentation/dispatch/-(_:_:)-5l4yh)
- [func - (DispatchTime, DispatchTimeInterval) -> DispatchTime](/documentation/dispatch/-(_:_:)-8usj3)
- [DispatchWallTime](/documentation/dispatch/dispatchwalltime)

### Getting Well-Known Times

- [static func now() -> DispatchWallTime](/documentation/dispatch/dispatchwalltime/now())
- [static let distantFuture: DispatchWallTime](/documentation/dispatch/dispatchwalltime/distantfuture)

### Creating a Dispatch Wall Time Object

- [init(timespec: timespec)](/documentation/dispatch/dispatchwalltime/init(timespec:))

### Getting the Time

- [let rawValue: dispatch_time_t](/documentation/dispatch/dispatchwalltime/rawvalue)

### Operator Functions

- [func + (DispatchWallTime, DispatchTimeInterval) -> DispatchWallTime](/documentation/dispatch/+(_:_:)-8ylhk)
- [func + (DispatchWallTime, Double) -> DispatchWallTime](/documentation/dispatch/+(_:_:)-8pe6k)
- [func - (DispatchWallTime, Double) -> DispatchWallTime](/documentation/dispatch/-(_:_:)-6jk71)
- [func - (DispatchWallTime, DispatchTimeInterval) -> DispatchWallTime](/documentation/dispatch/-(_:_:)-50bxr)
- [DispatchTimeInterval](/documentation/dispatch/dispatchtimeinterval)

### Enumeration Cases

- [case seconds(Int)](/documentation/dispatch/dispatchtimeinterval/seconds(_:))
- [case milliseconds(Int)](/documentation/dispatch/dispatchtimeinterval/milliseconds(_:))
- [case microseconds(Int)](/documentation/dispatch/dispatchtimeinterval/microseconds(_:))
- [case nanoseconds(Int)](/documentation/dispatch/dispatchtimeinterval/nanoseconds(_:))
- [case never](/documentation/dispatch/dispatchtimeinterval/never)
- [DispatchTimeoutResult](/documentation/dispatch/dispatchtimeoutresult)

### Enumeration Cases

- [case success](/documentation/dispatch/dispatchtimeoutresult/success)
- [case timedOut](/documentation/dispatch/dispatchtimeoutresult/timedout)
- [dispatch_time_t](/documentation/dispatch/dispatch_time_t)

### Well-Defined Times

- [var DISPATCH_TIME_NOW: UInt64](/documentation/dispatch/dispatch_time_now)
- [var DISPATCH_TIME_FOREVER: UInt64](/documentation/dispatch/dispatch_time_forever)

### Time Multiplier Constants

- [var USEC_PER_SEC: UInt64](/documentation/dispatch/usec_per_sec)
- [var NSEC_PER_SEC: UInt64](/documentation/dispatch/nsec_per_sec)
- [var NSEC_PER_MSEC: UInt64](/documentation/dispatch/nsec_per_msec)
- [var NSEC_PER_USEC: UInt64](/documentation/dispatch/nsec_per_usec)
- [var DISPATCH_WALLTIME_NOW: UInt](/documentation/dispatch/dispatch_walltime_now)
- [Wall Time Constants](/documentation/dispatch/2963138-wall-time-constants)

### Times

- [var DISPATCH_WALLTIME_NOW: UInt](/documentation/dispatch/dispatch_walltime_now)

## Dispatch Objects

- [DispatchObject](/documentation/dispatch/dispatchobject)

### Activating, Suspending, and Resuming

- [func activate()](/documentation/dispatch/dispatchobject/activate())
- [func resume()](/documentation/dispatch/dispatchobject/resume())
- [func suspend()](/documentation/dispatch/dispatchobject/suspend())

### Changing the Assigned Target Queue

- [func setTarget(queue: dispatch_queue_t?)](/documentation/dispatch/dispatchobject/settarget(queue:))
- [DispatchPredicate](/documentation/dispatch/dispatchpredicate)

### Predicates

- [case onQueue(DispatchQueue)](/documentation/dispatch/dispatchpredicate/onqueue(_:))
- [case onQueueAsBarrier(DispatchQueue)](/documentation/dispatch/dispatchpredicate/onqueueasbarrier(_:))
- [case notOnQueue(DispatchQueue)](/documentation/dispatch/dispatchpredicate/notonqueue(_:))
- [func dispatchPrecondition(condition: @autoclosure () -> DispatchPredicate)](/documentation/dispatch/dispatchprecondition(condition:))
- [Dispatch Objects](/documentation/dispatch/dispatch-objects)

### Activating, Suspending, and Resuming the Object

- [func activate()](/documentation/dispatch/dispatchobject/activate())
- [func suspend()](/documentation/dispatch/dispatchobject/suspend())
- [func resume()](/documentation/dispatch/dispatchobject/resume())
- [dispatch_object_t](/documentation/dispatch/dispatch_object_t)

### Changing the Assigned Target Queue

- [func setTarget(queue: dispatch_queue_t?)](/documentation/dispatch/dispatchobject/settarget(queue:))

## Deprecated

- [Deprecated Symbols](/documentation/dispatch/deprecated-symbols)

### Functions

- [func dispatch_get_current_queue() -> dispatch_queue_t](/documentation/dispatch/dispatch_get_current_queue())
- [func dispatch_debugv(dispatch_object_t, UnsafePointer<CChar>, CVaListPointer)](/documentation/dispatch/dispatch_debugv(_:_:_:))

## Classes

- [DispatchWorkloop](/documentation/dispatch/dispatchworkloop)

### Structures

- [DispatchWorkloop.Attributes](/documentation/dispatch/dispatchworkloop/attributes)

### Initializers

- [convenience init(label: String, attributes: DispatchWorkloop.Attributes, autoreleaseFrequency: DispatchQueue.AutoreleaseFrequency, osWorkgroup: WorkGroup?)](/documentation/dispatch/dispatchworkloop/init(label:attributes:autoreleasefrequency:osworkgroup:))

## Reference

- [Dispatch Constants](/documentation/dispatch/dispatch-constants)

### Constants

- [var DISPATCH_API_VERSION: Int32](/documentation/dispatch/dispatch_api_version)
- [var DISPATCH_APPLY_AUTO_AVAILABLE: Int32](/documentation/dispatch/dispatch_apply_auto_available)
- [var DISPATCH_ONCE_INLINE_FASTPATH: Int32](/documentation/dispatch/dispatch_once_inline_fastpath)
- [var DISPATCH_SWIFT3_OVERLAY: Int32](/documentation/dispatch/dispatch_swift3_overlay)
- [var MSEC_PER_SEC: UInt64](/documentation/dispatch/msec_per_sec)
- [Dispatch Data Types](/documentation/dispatch/dispatch-data-types)

### Data Types

- [dispatch_group_t](/documentation/dispatch/dispatch_group_t)
- [dispatch_io_t](/documentation/dispatch/dispatch_io_t)
- [dispatch_object_t](/documentation/dispatch/dispatch_object_t)
- [dispatch_queue_attr_t](/documentation/dispatch/dispatch_queue_attr_t)
- [dispatch_queue_serial_executor_t](/documentation/dispatch/dispatch_queue_serial_executor_t)
- [dispatch_queue_t](/documentation/dispatch/dispatch_queue_t)
- [dispatch_semaphore_t](/documentation/dispatch/dispatch_semaphore_t)
- [Dispatch Functions](/documentation/dispatch/dispatch-functions)

### Functions

- [func dispatch_allow_send_signals(Int32) -> Int32](/documentation/dispatch/dispatch_allow_send_signals(_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
