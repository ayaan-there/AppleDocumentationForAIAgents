# Playground Support Documentation

Source: https://sosumi.ai/documentation/playgroundsupport

---
title: Playground Support
source: https://developer.apple.com/documentation/playgroundsupport
timestamp: 2026-02-13T19:00:43.755Z
---

## Playground Pages

- [PlaygroundPage](/documentation/playgroundsupport/playgroundpage)

### Configuring Live Views

- [static let current: PlaygroundPage](/documentation/playgroundsupport/playgroundpage/1964509-current)
- [func setLiveView<IncomingView>(IncomingView)](/documentation/playgroundsupport/playgroundpage/3375751-setliveview)
- [func setLiveView<IncomingView>(IncomingView)](/documentation/playgroundsupport/playgroundpage/3375752-setliveview)
- [var liveView: (any PlaygroundLiveViewable)?](/documentation/playgroundsupport/playgroundpage/1964506-liveview)

### Configuring Execution

- [var executionMode: PlaygroundPage.ExecutionMode](/documentation/playgroundsupport/playgroundpage/3029561-executionmode)
- [PlaygroundPage.ExecutionMode](/documentation/playgroundsupport/playgroundpage/executionmode)

#### Controlling Execution Speed

- [case run](/documentation/playgroundsupport/playgroundpage/executionmode/run)
- [case runFaster](/documentation/playgroundsupport/playgroundpage/executionmode/runfaster)
- [case runFastest](/documentation/playgroundsupport/playgroundpage/executionmode/runfastest)

#### Stepping Through Code

- [case step](/documentation/playgroundsupport/playgroundpage/executionmode/step)
- [case stepSlowly](/documentation/playgroundsupport/playgroundpage/executionmode/stepslowly)

#### Comparing Modes

- [static func != (PlaygroundPage.ExecutionMode, PlaygroundPage.ExecutionMode) -> Bool](/documentation/playgroundsupport/playgroundpage/executionmode/3029554)
- [var needsIndefiniteExecution: Bool](/documentation/playgroundsupport/playgroundpage/1964501-needsindefiniteexecution)
- [func finishExecution() -> Never](/documentation/playgroundsupport/playgroundpage/1964505-finishexecution)

### Assessing Progress

- [var assessmentStatus: PlaygroundPage.AssessmentStatus?](/documentation/playgroundsupport/playgroundpage/3029560-assessmentstatus)
- [PlaygroundPage.AssessmentStatus](/documentation/playgroundsupport/playgroundpage/assessmentstatus)

#### Passing

- [case pass(message: String?)](/documentation/playgroundsupport/playgroundpage/assessmentstatus/pass_message)

#### Failing

- [case fail(hints: [String], solution: String?)](/documentation/playgroundsupport/playgroundpage/assessmentstatus/fail_hints_solution)

### Inspecting Page Data

- [var text: String](/documentation/playgroundsupport/playgroundpage/3029563-text)
- [var keyValueStore: PlaygroundKeyValueStore](/documentation/playgroundsupport/playgroundpage/3029562-keyvaluestore)

### Displaying Touch Bar Items

- [var liveTouchBar: NSTouchBar?](/documentation/playgroundsupport/playgroundpage/2919769-livetouchbar)

### Instance Properties

- [var userModuleNames: [String]](/documentation/playgroundsupport/playgroundpage/3919480-usermodulenames)
- [var wantsFullScreenLiveView: Bool](/documentation/playgroundsupport/playgroundpage/3074093-wantsfullscreenliveview)

### Instance Methods

- [func getText(forSourceFile: String, inUserModule: String) -> String?](/documentation/playgroundsupport/playgroundpage/3919478-gettext)
- [func listSourceFiles(inUserModule: String) -> [String]](/documentation/playgroundsupport/playgroundpage/3919479-listsourcefiles)
- [func navigateTo(page: PlaygroundPage.PageNavigation)](/documentation/playgroundsupport/playgroundpage/3239065-navigateto)
- [func openApplication(withBundleIdentifier: String, iTunesItemIdentifier: Int?)](/documentation/playgroundsupport/playgroundpage/3239066-openapplication)
- [func openPlayground(withContentIdentifier: String, toPageAtIndex: Int?)](/documentation/playgroundsupport/playgroundpage/3239067-openplayground)
- [func showGlossaryEntry(named: String, at: CGRect?, in: UIView?)](/documentation/playgroundsupport/playgroundpage/3239068-showglossaryentry)

### Enumerations

- [PlaygroundPage.PageNavigation](/documentation/playgroundsupport/playgroundpage/pagenavigation)

#### Enumeration Cases

- [case next](/documentation/playgroundsupport/playgroundpage/pagenavigation/next)
- [case pageReference(reference: String)](/documentation/playgroundsupport/playgroundpage/pagenavigation/pagereference_reference)
- [case previous](/documentation/playgroundsupport/playgroundpage/pagenavigation/previous)

## Live Views

- [PlaygroundLiveViewable](/documentation/playgroundsupport/playgroundliveviewable)

### Displaying Types

- [var playgroundLiveViewRepresentation: PlaygroundLiveViewRepresentation](/documentation/playgroundsupport/playgroundliveviewable/1978828-playgroundliveviewrepresentation)
- [PlaygroundLiveViewRepresentation](/documentation/playgroundsupport/playgroundliveviewrepresentation)

### Displaying UIKit Views

- [case view(UIView)](/documentation/playgroundsupport/playgroundliveviewrepresentation/view)
- [case viewController(UIViewController)](/documentation/playgroundsupport/playgroundliveviewrepresentation/viewcontroller)

### Displaying AppKit Views

- [case view(NSView)](/documentation/playgroundsupport/playgroundliveviewrepresentation/view-ues)
- [case viewController(NSViewController)](/documentation/playgroundsupport/playgroundliveviewrepresentation/viewcontroller-uej)
- [PlaygroundLiveViewSafeAreaContainer](/documentation/playgroundsupport/playgroundliveviewsafeareacontainer)

### Accessing the Layout Guide

- [var liveViewSafeAreaGuide: UILayoutGuide](/documentation/playgroundsupport/playgroundliveviewsafeareacontainer/3029546-liveviewsafeareaguide)

## Page-View Communication

- [Messaging Between a Playground Page and the Always-On Live View](/documentation/playgroundsupport/messaging_between_a_playground_page_and_the_always-on_live_view)
- [PlaygroundRemoteLiveViewProxy](/documentation/playgroundsupport/playgroundremoteliveviewproxy)

### Sending Messages

- [func send(PlaygroundValue)](/documentation/playgroundsupport/playgroundremoteliveviewproxy/3029570-send)

### Receiving Messages

- [var delegate: PlaygroundRemoteLiveViewProxyDelegate?](/documentation/playgroundsupport/playgroundremoteliveviewproxy/3029565-delegate)
- [func receive(PlaygroundValue)](/documentation/playgroundsupport/playgroundremoteliveviewproxy/3029569-receive)

### Handling Connection Changes

- [func liveViewMessageConnectionOpened()](/documentation/playgroundsupport/playgroundremoteliveviewproxy/3029567-liveviewmessageconnectionopened)
- [func liveViewMessageConnectionClosed()](/documentation/playgroundsupport/playgroundremoteliveviewproxy/3029566-liveviewmessageconnectionclosed)

### Inspecting Live View Proxies

- [var playgroundLiveViewRepresentation: PlaygroundLiveViewRepresentation](/documentation/playgroundsupport/playgroundremoteliveviewproxy/3029568-playgroundliveviewrepresentation)
- [PlaygroundRemoteLiveViewProxyDelegate](/documentation/playgroundsupport/playgroundremoteliveviewproxydelegate)

### Receiving Messages

- [func remoteLiveViewProxy(PlaygroundRemoteLiveViewProxy, received: PlaygroundValue)](/documentation/playgroundsupport/playgroundremoteliveviewproxydelegate/3029572-remoteliveviewproxy)

### Handling Connection Changes

- [func remoteLiveViewProxyConnectionClosed(PlaygroundRemoteLiveViewProxy)](/documentation/playgroundsupport/playgroundremoteliveviewproxydelegate/3029573-remoteliveviewproxyconnectionclo)
- [PlaygroundLiveViewMessageHandler](/documentation/playgroundsupport/playgroundliveviewmessagehandler)

### Sending Messages

- [func send(PlaygroundValue)](/documentation/playgroundsupport/playgroundliveviewmessagehandler/3029542-send)

### Receiving Messages

- [func receive(PlaygroundValue)](/documentation/playgroundsupport/playgroundliveviewmessagehandler/3029540-receive)

### Handling Connection Changes

- [func liveViewMessageConnectionOpened()](/documentation/playgroundsupport/playgroundliveviewmessagehandler/3029538-liveviewmessageconnectionopened)
- [func liveViewMessageConnectionClosed()](/documentation/playgroundsupport/playgroundliveviewmessagehandler/3029536-liveviewmessageconnectionclosed)

## Data Persistence

- [PlaygroundKeyValueStore](/documentation/playgroundsupport/playgroundkeyvaluestore)

### Persisting Data

- [static let current: PlaygroundKeyValueStore](/documentation/playgroundsupport/playgroundkeyvaluestore/3029533-current)
- [subscript(String) -> PlaygroundValue?](/documentation/playgroundsupport/playgroundkeyvaluestore/3029534-subscript)
- [PlaygroundValue](/documentation/playgroundsupport/playgroundvalue)

### Representing Data

- [case boolean(Bool)](/documentation/playgroundsupport/playgroundvalue/boolean)
- [case data(Data)](/documentation/playgroundsupport/playgroundvalue/data)
- [case date(Date)](/documentation/playgroundsupport/playgroundvalue/date)
- [case floatingPoint(Double)](/documentation/playgroundsupport/playgroundvalue/floatingpoint)
- [case integer(Int)](/documentation/playgroundsupport/playgroundvalue/integer)
- [case string(String)](/documentation/playgroundsupport/playgroundvalue/string)

### Representing Data Collections

- [case array([PlaygroundValue])](/documentation/playgroundsupport/playgroundvalue/array)
- [case dictionary([String : PlaygroundValue])](/documentation/playgroundsupport/playgroundvalue/dictionary)
- [let playgroundSharedDataDirectory: URL](/documentation/playgroundsupport/playgroundshareddatadirectory)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
