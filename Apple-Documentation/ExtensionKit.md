# ExtensionKit Documentation

Source: https://sosumi.ai/documentation/extensionkit

---
title: ExtensionKit
source: https://developer.apple.com/documentation/extensionkit
timestamp: 2026-02-13T18:56:50.390Z
---

## Essentials

- [Including extension-based UI in your interface](/documentation/extensionkit/including-extension-based-ui-in-your-interface)

## UI definition

- [AppExtensionScene](/documentation/extensionkit/appextensionscene)

### Configuring the app extension

- [var body: Self.Body](/documentation/extensionkit/appextensionscene/body-swift.property)
- [Body](/documentation/extensionkit/appextensionscene/body-swift.associatedtype)
- [PrimitiveAppExtensionScene](/documentation/extensionkit/primitiveappextensionscene)

### Creating a primitive extension scene

- [init<Content>(id: String, content: () -> Content, onConnection: (NSXPCConnection) -> Bool)](/documentation/extensionkit/primitiveappextensionscene/init(id:content:onconnection:))

### Defining the scene contents

- [var body: Never](/documentation/extensionkit/primitiveappextensionscene/body)

### Describing the scene

- [var debugDescription: String](/documentation/extensionkit/primitiveappextensionscene/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/extensionkit/primitiveappextensionscene/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/extensionkit/primitiveappextensionscene/debugdescription)
- [AppExtensionSceneBuilder](/documentation/extensionkit/appextensionscenebuilder)

### Building the scene’s content

- [static func buildBlock<Content>(Content) -> some AppExtensionScene](/documentation/extensionkit/appextensionscenebuilder/buildblock(_:))
- [static func buildBlock<C0, C1>(C0, C1) -> some AppExtensionScene](/documentation/extensionkit/appextensionscenebuilder/buildblock(_:_:))
- [static func buildBlock<C0, C1, C2>(C0, C1, C2) -> some AppExtensionScene](/documentation/extensionkit/appextensionscenebuilder/buildblock(_:_:_:))
- [static func buildBlock<C0, C1, C2, C3>(C0, C1, C2, C3) -> some AppExtensionScene](/documentation/extensionkit/appextensionscenebuilder/buildblock(_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4>(C0, C1, C2, C3, C4) -> some AppExtensionScene](/documentation/extensionkit/appextensionscenebuilder/buildblock(_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5>(C0, C1, C2, C3, C4, C5) -> some AppExtensionScene](/documentation/extensionkit/appextensionscenebuilder/buildblock(_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6>(C0, C1, C2, C3, C4, C5, C6) -> some AppExtensionScene](/documentation/extensionkit/appextensionscenebuilder/buildblock(_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7>(C0, C1, C2, C3, C4, C5, C6, C7) -> some AppExtensionScene](/documentation/extensionkit/appextensionscenebuilder/buildblock(_:_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7, C8>(C0, C1, C2, C3, C4, C5, C6, C7, C8) -> some AppExtensionScene](/documentation/extensionkit/appextensionscenebuilder/buildblock(_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7, C8, C9>(C0, C1, C2, C3, C4, C5, C6, C7, C8, C9) -> some AppExtensionScene](/documentation/extensionkit/appextensionscenebuilder/buildblock(_:_:_:_:_:_:_:_:_:_:))

## App extension configuration

- [AppExtensionSceneConfiguration](/documentation/extensionkit/appextensionsceneconfiguration)

### Creating the configuration

- [init<Content>(@autoclosure () -> Content)](/documentation/extensionkit/appextensionsceneconfiguration/init(_:))
- [init<Content, Configuration>(@autoclosure () -> Content, configuration: Configuration?)](/documentation/extensionkit/appextensionsceneconfiguration/init(_:configuration:))

### Accepting a connection to the host app

- [func accept(connection: NSXPCConnection) -> Bool](/documentation/extensionkit/appextensionsceneconfiguration/accept(connection:))

## Host app presentation

- [Displaying the app extensions available to your app](/documentation/extensionkit/displaying-the-app-extensions-available-to-your-app)
- [EXHostViewController](/documentation/extensionkit/exhostviewcontroller)

### Configuring the view controller

- [var configuration: EXHostViewController.Configuration?](/documentation/extensionkit/exhostviewcontroller/configuration-swift.property)
- [EXHostViewController.Configuration](/documentation/extensionkit/exhostviewcontroller/configuration-swift.struct)

#### Creating a configuration type

- [init(appExtension: AppExtensionIdentity, sceneID: String)](/documentation/extensionkit/exhostviewcontroller/configuration-swift.struct/init(appextension:sceneid:))

#### Identifying the scene to display

- [var appExtension: AppExtensionIdentity](/documentation/extensionkit/exhostviewcontroller/configuration-swift.struct/appextension)
- [var sceneID: String](/documentation/extensionkit/exhostviewcontroller/configuration-swift.struct/sceneid)
- [var placeholderView: UIView](/documentation/extensionkit/exhostviewcontroller/placeholderview)

### Connecting to the app extension

- [func makeXPCConnection() throws -> NSXPCConnection](/documentation/extensionkit/exhostviewcontroller/makexpcconnection())

### Responding to activation and deactivation events

- [var delegate: (any EXHostViewControllerDelegate)?](/documentation/extensionkit/exhostviewcontroller/delegate)
- [EXHostViewControllerDelegate](/documentation/extensionkit/exhostviewcontrollerdelegate)

#### Responding to activation and deactivation events

- [func hostViewControllerDidActivate(EXHostViewController)](/documentation/extensionkit/exhostviewcontrollerdelegate/hostviewcontrollerdidactivate(_:))
- [func hostViewControllerWillDeactivate(EXHostViewController, error: (any Error)?)](/documentation/extensionkit/exhostviewcontrollerdelegate/hostviewcontrollerwilldeactivate(_:error:))
- [EXAppExtensionBrowserViewController](/documentation/extensionkit/exappextensionbrowserviewcontroller)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
