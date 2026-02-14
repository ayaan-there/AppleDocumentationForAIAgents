# ExtensionFoundation Documentation

Source: https://sosumi.ai/documentation/extensionfoundation

---
title: ExtensionFoundation
source: https://developer.apple.com/documentation/extensionfoundation
timestamp: 2026-02-13T18:56:48.313Z
---

## Essentials

- [Adding support for app extensions to your app](/documentation/extensionfoundation/adding-support-for-app-extensions-to-your-app)

## App-extension setup

- [Building an app extension to support a host app](/documentation/extensionfoundation/building-an-app-extension-to-support-a-host-app)
- [AppExtension](/documentation/extensionfoundation/appextension)

### Creating an app extension

- [init()](/documentation/extensionfoundation/appextension/init())

### Configuring the app extension

- [var configuration: Self.Configuration](/documentation/extensionfoundation/appextension/configuration-swift.property)
- [Configuration](/documentation/extensionfoundation/appextension/configuration-swift.associatedtype)

### Running the main event loop

- [static func main() throws](/documentation/extensionfoundation/appextension/main()-5zfjx)
- [static func main() throws](/documentation/extensionfoundation/appextension/main()-w0u9)

### Instance Properties

- [var extensionPoint: AppExtensionPoint](/documentation/extensionfoundation/appextension/extensionpoint)

### Type Aliases

- [AppExtension.Bind](/documentation/extensionfoundation/appextension/bind)
- [AppExtension.Identifier](/documentation/extensionfoundation/appextension/identifier)
- [AppExtension.Implementing](/documentation/extensionfoundation/appextension/implementing)

### Default Implementations

- [AppExtension Implementations](/documentation/extensionfoundation/appextension/appextension-implementations)

#### Type Methods

- [static func main() throws](/documentation/extensionfoundation/appextension/main()-w0u9)
- [AppExtensionConfiguration](/documentation/extensionfoundation/appextensionconfiguration)

### Accepting a connection to the host app

- [func accept(connection: NSXPCConnection) -> Bool](/documentation/extensionfoundation/appextensionconfiguration/accept(connection:))
- [ConnectionHandler](/documentation/extensionfoundation/connectionhandler)

### Initializing the connection handler

- [init(onConnection: (NSXPCConnection) -> Bool)](/documentation/extensionfoundation/connectionhandler/init(onconnection:))
- [init(onSessionRequest: (XPCListener.IncomingSessionRequest) -> XPCListener.IncomingSessionRequest.Decision)](/documentation/extensionfoundation/connectionhandler/init(onsessionrequest:))

## Host-app configuration

- [Discovering app extensions from your app](/documentation/extensionfoundation/discovering-app-extensions-from-your-app)
- [AppExtensionProcess](/documentation/extensionfoundation/appextensionprocess)

### Creating the app-extension process

- [init(configuration: AppExtensionProcess.Configuration) throws](/documentation/extensionfoundation/appextensionprocess/init(configuration:)-2g0cy)
- [init(configuration: AppExtensionProcess.Configuration) async throws](/documentation/extensionfoundation/appextensionprocess/init(configuration:)-38zf)
- [AppExtensionProcess.Configuration](/documentation/extensionfoundation/appextensionprocess/configuration)

#### Creating the configuration structure

- [init(appExtensionIdentity: AppExtensionIdentity, onInterruption: () -> Void)](/documentation/extensionfoundation/appextensionprocess/configuration/init(appextensionidentity:oninterruption:))

#### Responding to process interruptions

- [var onInterruption: () -> Void](/documentation/extensionfoundation/appextensionprocess/configuration/oninterruption)

#### Getting the app-extension details

- [var appExtensionIdentity: AppExtensionIdentity](/documentation/extensionfoundation/appextensionprocess/configuration/appextensionidentity)

### Connecting to the app extension

- [func makeXPCConnection() throws -> NSXPCConnection](/documentation/extensionfoundation/appextensionprocess/makexpcconnection())
- [func makeXPCSession() throws -> XPCSession](/documentation/extensionfoundation/appextensionprocess/makexpcsession())

### Invalidating the app-extension connection

- [func invalidate()](/documentation/extensionfoundation/appextensionprocess/invalidate())
- [AppExtensionIdentity](/documentation/extensionfoundation/appextensionidentity)

### Identifying the process

- [var bundleIdentifier: String](/documentation/extensionfoundation/appextensionidentity/bundleidentifier)
- [var extensionPointIdentifier: String](/documentation/extensionfoundation/appextensionidentity/extensionpointidentifier)
- [var localizedName: String](/documentation/extensionfoundation/appextensionidentity/localizedname)

### Comparing app extensions

- [func hash(into: inout Hasher)](/documentation/extensionfoundation/appextensionidentity/hash(into:))
- [static func == (AppExtensionIdentity, AppExtensionIdentity) -> Bool](/documentation/extensionfoundation/appextensionidentity/==(_:_:))

### Deprecated

- [AppExtensionIdentity.Availability](/documentation/extensionfoundation/appextensionidentity/availability)

#### Creating an Availability Object

- [init()](/documentation/extensionfoundation/appextensionidentity/availability/init())

#### Accessing Availability Information

- [var description: String](/documentation/extensionfoundation/appextensionidentity/availability/description)
- [var totalCount: Int](/documentation/extensionfoundation/appextensionidentity/availability/totalcount)
- [let disabledCount: Int](/documentation/extensionfoundation/appextensionidentity/availability/disabledcount)
- [let enabledCount: Int](/documentation/extensionfoundation/appextensionidentity/availability/enabledcount)
- [let unapprovedCount: Int](/documentation/extensionfoundation/appextensionidentity/availability/unapprovedcount)
- [static var availabilityUpdates: AsyncStream<AppExtensionIdentity.Availability>](/documentation/extensionfoundation/appextensionidentity/availabilityupdates)
- [static func matching(appExtensionPointIDs: String...) throws -> AppExtensionIdentity.Identities](/documentation/extensionfoundation/appextensionidentity/matching(appextensionpointids:))
- [AppExtensionIdentity.Identities](/documentation/extensionfoundation/appextensionidentity/identities)

#### Iterating the Sequence

- [func next() async -> [AppExtensionIdentity]?](/documentation/extensionfoundation/appextensionidentity/identities/asynciterator/next())
- [AppExtensionIdentity.Identities.AsyncIterator](/documentation/extensionfoundation/appextensionidentity/identities/asynciterator)

##### Iterating Extensions

- [AppExtensionIdentity.Identities.Element](/documentation/extensionfoundation/appextensionidentity/identities/element)
- [func next() async -> [AppExtensionIdentity]?](/documentation/extensionfoundation/appextensionidentity/identities/asynciterator/next())
- [AppExtensionIdentity.Identities.Element](/documentation/extensionfoundation/appextensionidentity/identities/element)
- [func makeAsyncIterator() -> AppExtensionIdentity.Identities.AsyncIterator](/documentation/extensionfoundation/appextensionidentity/identities/makeasynciterator())

## Extension-point management

- [AppExtensionPoint](/documentation/extensionfoundation/appextensionpoint)

### Creating an app-extension point

- [init(identifier: StaticString) throws](/documentation/extensionfoundation/appextensionpoint/init(identifier:))

### Declaring an extension point

- [AppExtensionPoint.Definition](/documentation/extensionfoundation/appextensionpoint/definition)

#### Wrapping the type

- [static func buildBlock<each T>(AppExtensionPoint.Name, repeat each T) -> AppExtensionPoint](/documentation/extensionfoundation/appextensionpoint/definition/buildblock(_:_:))
- [AppExtensionPoint.Name](/documentation/extensionfoundation/appextensionpoint/name)

#### Creating a name attribute

- [init(StaticString)](/documentation/extensionfoundation/appextensionpoint/name/init(_:))
- [AppExtensionPoint.UserInterface](/documentation/extensionfoundation/appextensionpoint/userinterface)

#### Creating a user-interface attribute

- [init(Bool)](/documentation/extensionfoundation/appextensionpoint/userinterface/init(_:))

#### Getting the value

- [let value: Bool](/documentation/extensionfoundation/appextensionpoint/userinterface/value)
- [AppExtensionPoint.EnhancedSecurity](/documentation/extensionfoundation/appextensionpoint/enhancedsecurity)

#### Creating a security attribute

- [init(Bool)](/documentation/extensionfoundation/appextensionpoint/enhancedsecurity/init(_:))
- [AppExtensionPoint.Scope](/documentation/extensionfoundation/appextensionpoint/scope)

#### Creating a scope attribute

- [init(restriction: AppExtensionPoint.Scope.Restriction)](/documentation/extensionfoundation/appextensionpoint/scope/init(restriction:))
- [AppExtensionPoint.Scope.Restriction](/documentation/extensionfoundation/appextensionpoint/scope/restriction)

##### Getting the restriction types

- [case none](/documentation/extensionfoundation/appextensionpoint/scope/restriction/none)
- [case application](/documentation/extensionfoundation/appextensionpoint/scope/restriction/application)
- [AppExtensionPoint.Attribute](/documentation/extensionfoundation/appextensionpoint/attribute)

### Binding to an extension point

- [AppExtensionPoint.Bind](/documentation/extensionfoundation/appextensionpoint/bind)

#### Annotating a binding

- [static func buildBlock(AppExtensionPoint.Identifier) -> AppExtensionPoint](/documentation/extensionfoundation/appextensionpoint/bind/buildblock(_:))
- [AppExtensionPoint.Identifier](/documentation/extensionfoundation/appextensionpoint/identifier)

#### Creating an identifier attribute

- [init(StaticString)](/documentation/extensionfoundation/appextensionpoint/identifier/init(_:))
- [init(host: StaticString, name: StaticString)](/documentation/extensionfoundation/appextensionpoint/identifier/init(host:name:))

### Detecting app extensions

- [AppExtensionPoint.Monitor](/documentation/extensionfoundation/appextensionpoint/monitor)

#### Creating a monitor

- [init()](/documentation/extensionfoundation/appextensionpoint/monitor/init())
- [convenience init(appExtensionPoint: AppExtensionPoint) async throws](/documentation/extensionfoundation/appextensionpoint/monitor/init(appextensionpoint:))

#### Adding and removing extension points

- [func addAppExtensionPoint(AppExtensionPoint) async throws](/documentation/extensionfoundation/appextensionpoint/monitor/addappextensionpoint(_:))
- [func removeAppExtensionPoint(AppExtensionPoint) async throws](/documentation/extensionfoundation/appextensionpoint/monitor/removeappextensionpoint(_:))

#### Getting the available app extensions

- [var identities: [AppExtensionIdentity]](/documentation/extensionfoundation/appextensionpoint/monitor/identities)

#### Getting the monitor state

- [var state: AppExtensionPoint.Monitor.State](/documentation/extensionfoundation/appextensionpoint/monitor/state-swift.property)
- [AppExtensionPoint.Monitor.State](/documentation/extensionfoundation/appextensionpoint/monitor/state-swift.struct)

##### Getting the app extension status

- [var identities: [AppExtensionIdentity]](/documentation/extensionfoundation/appextensionpoint/monitor/state-swift.struct/identities)
- [var disabledCount: Int](/documentation/extensionfoundation/appextensionpoint/monitor/state-swift.struct/disabledcount)
- [var unapprovedCount: Int](/documentation/extensionfoundation/appextensionpoint/monitor/state-swift.struct/unapprovedcount)

### Getting error codes

- [AppExtensionPoint.Error](/documentation/extensionfoundation/appextensionpoint/error)

#### Getting the error codes

- [case hostMustBeApplicationOrAppExtension](/documentation/extensionfoundation/appextensionpoint/error/hostmustbeapplicationorappextension)
- [case hostMustDefineAppExtensionPoint(String)](/documentation/extensionfoundation/appextensionpoint/error/hostmustdefineappextensionpoint(_:))
- [case hostMustHaveBundleIdentifier](/documentation/extensionfoundation/appextensionpoint/error/hostmusthavebundleidentifier)
- [case invalidAppExtensionPoint](/documentation/extensionfoundation/appextensionpoint/error/invalidappextensionpoint)
- [case unspecifiedAppExtensionPointName](/documentation/extensionfoundation/appextensionpoint/error/unspecifiedappextensionpointname)

### Protocols

- [AppExtensionPoint.Capability](/documentation/extensionfoundation/appextensionpoint/capability)

### Structures

- [AppExtensionPoint.Capabilities](/documentation/extensionfoundation/appextensionpoint/capabilities)

#### Structures

- [AppExtensionPoint.Capabilities.Builder](/documentation/extensionfoundation/appextensionpoint/capabilities/builder)

##### Type Methods

- [static func buildBlock<each T>(repeat each T) -> AppExtensionPoint.Capabilities](/documentation/extensionfoundation/appextensionpoint/capabilities/builder/buildblock(_:))

#### Initializers

- [init(() -> AppExtensionPoint.Capabilities)](/documentation/extensionfoundation/appextensionpoint/capabilities/init(_:))
- [ExtensionPointDefining](/documentation/extensionfoundation/extensionpointdefining)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
