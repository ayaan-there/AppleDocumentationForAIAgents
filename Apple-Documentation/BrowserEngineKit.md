# BrowserEngineKit Documentation

Source: https://sosumi.ai/documentation/browserenginekit

---
title: BrowserEngineKit
source: https://developer.apple.com/documentation/browserenginekit
timestamp: 2026-02-13T18:54:28.335Z
---

## Essentials

- [Developing a browser app that uses an alternative browser engine](/documentation/browserenginekit/developing-a-browser-app-that-uses-an-alternative-browser-engine)
- [Designing your browser architecture](/documentation/browserenginekit/designing-your-browser-architecture)
- [Preparing your app to be the default web browser](/documentation/xcode/preparing-your-app-to-be-the-default-browser)

## Browser extensions

- [Creating browser extensions in Xcode](/documentation/browserenginekit/creating-browser-extensions-in-xcode)
- [Extension lifecycle](/documentation/browserenginekit/extension-lifecycle)

### Essentials

- [Managing the browser extension life cycle](/documentation/browserenginekit/managing-the-browser-extension-lifecycle)
- [Using XPC to communicate with browser extensions](/documentation/browserenginekit/using-xpc-to-communicate-with-browser-extensions)

### Browser extensions

- [WebContentExtension](/documentation/browserenginekit/webcontentextension)

#### Handling incoming XPC connections

- [func handle(xpcConnection: xpc_connection_t)](/documentation/browserenginekit/webcontentextension/handle(xpcconnection:))
- [WebContentExtensionConfiguration](/documentation/browserenginekit/webcontentextensionconfiguration)
- [NetworkingExtension](/documentation/browserenginekit/networkingextension)

#### Handling incoming XPC connections

- [func handle(xpcConnection: xpc_connection_t)](/documentation/browserenginekit/networkingextension/handle(xpcconnection:))
- [NetworkingExtensionConfiguration](/documentation/browserenginekit/networkingextensionconfiguration)
- [RenderingExtension](/documentation/browserenginekit/renderingextension)

#### Handling incoming XPC connections

- [func handle(xpcConnection: xpc_connection_t)](/documentation/browserenginekit/renderingextension/handle(xpcconnection:))

#### Instance Methods

- [func enableFeature(RenderingExtensionFeature)](/documentation/browserenginekit/renderingextension/enablefeature(_:))
- [RenderingExtensionConfiguration](/documentation/browserenginekit/renderingextensionconfiguration)

### Host app representations

- [WebContentProcess](/documentation/browserenginekit/webcontentprocess)

#### Creating and invalidating extension processes

- [init(bundleIdentifier: String?, onInterruption: () -> Void) async throws](/documentation/browserenginekit/webcontentprocess/init(bundleidentifier:oninterruption:))
- [func invalidate()](/documentation/browserenginekit/webcontentprocess/invalidate())

#### Creating XPC connections

- [func makeLibXPCConnection() throws -> xpc_connection_t](/documentation/browserenginekit/webcontentprocess/makelibxpcconnection())

#### Coordinating processes

- [func grantCapability(ProcessCapability) throws -> ProcessCapability.Grant](/documentation/browserenginekit/webcontentprocess/grantcapability(_:))
- [func grantCapability(ProcessCapability, invalidationHandler: () -> Void) throws -> ProcessCapability.Grant](/documentation/browserenginekit/webcontentprocess/grantcapability(_:invalidationhandler:))
- [func createVisibilityPropagationInteraction() -> any UIInteraction](/documentation/browserenginekit/webcontentprocess/createvisibilitypropagationinteraction())
- [NetworkingProcess](/documentation/browserenginekit/networkingprocess)

#### Creating and invalidating extension processes

- [init(bundleIdentifier: String?, onInterruption: () -> Void) async throws](/documentation/browserenginekit/networkingprocess/init(bundleidentifier:oninterruption:))
- [func invalidate()](/documentation/browserenginekit/networkingprocess/invalidate())

#### Creating XPC connections

- [func makeLibXPCConnection() throws -> xpc_connection_t](/documentation/browserenginekit/networkingprocess/makelibxpcconnection())

#### Coordinating processes

- [func grantCapability(ProcessCapability) throws -> ProcessCapability.Grant](/documentation/browserenginekit/networkingprocess/grantcapability(_:))
- [func grantCapability(ProcessCapability, invalidationHandler: () -> Void) throws -> ProcessCapability.Grant](/documentation/browserenginekit/networkingprocess/grantcapability(_:invalidationhandler:))
- [RenderingProcess](/documentation/browserenginekit/renderingprocess)

#### Creating and invalidating extension processes

- [init(bundleIdentifier: String?, onInterruption: () -> Void) async throws](/documentation/browserenginekit/renderingprocess/init(bundleidentifier:oninterruption:))
- [func invalidate()](/documentation/browserenginekit/renderingprocess/invalidate())

#### Creating XPC connections

- [func makeLibXPCConnection() throws -> xpc_connection_t](/documentation/browserenginekit/renderingprocess/makelibxpcconnection())

#### Coordinating processes

- [func grantCapability(ProcessCapability) throws -> ProcessCapability.Grant](/documentation/browserenginekit/renderingprocess/grantcapability(_:))
- [func grantCapability(ProcessCapability, invalidationHandler: () -> Void) throws -> ProcessCapability.Grant](/documentation/browserenginekit/renderingprocess/grantcapability(_:invalidationhandler:))
- [func createVisibilityPropagationInteraction() -> any UIInteraction](/documentation/browserenginekit/renderingprocess/createvisibilitypropagationinteraction())

### Extension capabilities

- [ProcessCapability](/documentation/browserenginekit/processcapability)

#### Granting capabilities to browser extension processes

- [case background](/documentation/browserenginekit/processcapability/background)
- [case foreground](/documentation/browserenginekit/processcapability/foreground)
- [case suspended](/documentation/browserenginekit/processcapability/suspended)
- [case mediaPlaybackAndCapture(environment: MediaEnvironment)](/documentation/browserenginekit/processcapability/mediaplaybackandcapture(environment:))
- [ProcessCapability.Grant](/documentation/browserenginekit/processcapability/grant)

##### Testing and changing validity

- [var isValid: Bool](/documentation/browserenginekit/processcapability/grant/isvalid)
- [func invalidate()](/documentation/browserenginekit/processcapability/grant/invalidate())
- [MediaEnvironment](/documentation/browserenginekit/mediaenvironment)

#### Creating a media environment

- [init(webPage: URL)](/documentation/browserenginekit/mediaenvironment/init(webpage:))
- [init(xpcRepresentation: xpc_object_t) throws](/documentation/browserenginekit/mediaenvironment/init(xpcrepresentation:))

#### Sending media environments over XPC connections

- [func createXPCRepresentation() -> xpc_object_t](/documentation/browserenginekit/mediaenvironment/createxpcrepresentation())

#### Capturing media streams

- [func activate() throws](/documentation/browserenginekit/mediaenvironment/activate())
- [func makeCaptureSession() throws -> AVCaptureSession](/documentation/browserenginekit/mediaenvironment/makecapturesession())
- [func suspend() throws](/documentation/browserenginekit/mediaenvironment/suspend())
- [Extension resources](/documentation/browserenginekit/extension-resources)

### Access control

- [Limiting resource access in web content extensions](/documentation/browserenginekit/limiting-resource-access-in-content-extensions)
- [Accessing files in browser extensions](/documentation/browserenginekit/accessing-files-in-browser-extensions)
- [Attributing memory to a content extension](/documentation/browserenginekit/attributing-memory-to-a-content-extension)
- [RestrictedSandboxAppliable](/documentation/browserenginekit/restrictedsandboxappliable)

#### Applying sandbox restrictions

- [func applyRestrictedSandbox(revision: RestrictedSandboxRevision)](/documentation/browserenginekit/restrictedsandboxappliable/applyrestrictedsandbox(revision:))
- [RestrictedSandboxRevision](/documentation/browserenginekit/restrictedsandboxrevision)

##### Sandbox restriction revisions

- [case revision1](/documentation/browserenginekit/restrictedsandboxrevision/revision1)

##### Enumeration Cases

- [case revision2](/documentation/browserenginekit/restrictedsandboxrevision/revision2)
- [RestrictedSandboxRevision](/documentation/browserenginekit/restrictedsandboxrevision)

#### Sandbox restriction revisions

- [case revision1](/documentation/browserenginekit/restrictedsandboxrevision/revision1)

#### Enumeration Cases

- [case revision2](/documentation/browserenginekit/restrictedsandboxrevision/revision2)

## Web content

- [View coordination](/documentation/browserenginekit/view-coordination)

### Layer hosting

- [Hosting browser view layers in the rendering extension](/documentation/browserenginekit/hosting-browser-view-layers-in-the-rendering-extension)
- [LayerHierarchy](/documentation/browserenginekit/layerhierarchy)

#### Creating and invalidating a layer hierarchy

- [init() throws](/documentation/browserenginekit/layerhierarchy/init())
- [func invalidate()](/documentation/browserenginekit/layerhierarchy/invalidate())

#### Setting the layer

- [var layer: CALayer?](/documentation/browserenginekit/layerhierarchy/layer)

#### Getting a handle

- [var handle: LayerHierarchyHandle](/documentation/browserenginekit/layerhierarchy/handle)
- [LayerHierarchyHostingView](/documentation/browserenginekit/layerhierarchyhostingview)

#### Identifying remote layer hierarchy

- [var handle: LayerHierarchyHandle?](/documentation/browserenginekit/layerhierarchyhostingview/handle)
- [LayerHierarchyHostingTransactionCoordinator](/documentation/browserenginekit/layerhierarchyhostingtransactioncoordinator)

#### Creating a transaction coordinator

- [init() throws](/documentation/browserenginekit/layerhierarchyhostingtransactioncoordinator/init())

#### Interprocess communication

- [init?(coder: NSCoder)](/documentation/browserenginekit/layerhierarchyhostingtransactioncoordinator/init(coder:))
- [init(xpcRepresentation: xpc_object_t?) throws](/documentation/browserenginekit/layerhierarchyhostingtransactioncoordinator/init(xpcrepresentation:))
- [func createXPCRepresentation() -> xpc_object_t](/documentation/browserenginekit/layerhierarchyhostingtransactioncoordinator/createxpcrepresentation())

#### Synchronize transactions

- [func add(LayerHierarchyHostingView)](/documentation/browserenginekit/layerhierarchyhostingtransactioncoordinator/add(_:)-7day0)
- [func add(LayerHierarchy)](/documentation/browserenginekit/layerhierarchyhostingtransactioncoordinator/add(_:)-i66q)
- [func commit()](/documentation/browserenginekit/layerhierarchyhostingtransactioncoordinator/commit())

#### Initializers

- [init(port: mach_port_t, data: Data) throws](/documentation/browserenginekit/layerhierarchyhostingtransactioncoordinator/init(port:data:))

#### Instance Methods

- [func encode((mach_port_t, Data) -> Void)](/documentation/browserenginekit/layerhierarchyhostingtransactioncoordinator/encode(_:))
- [LayerHierarchyHandle](/documentation/browserenginekit/layerhierarchyhandle)

#### Interprocess communication

- [init?(coder: NSCoder)](/documentation/browserenginekit/layerhierarchyhandle/init(coder:))
- [init(xpcRepresentation: xpc_object_t?) throws](/documentation/browserenginekit/layerhierarchyhandle/init(xpcrepresentation:))
- [func createXPCRepresentation() -> xpc_object_t](/documentation/browserenginekit/layerhierarchyhandle/createxpcrepresentation())

#### Initializers

- [init(port: mach_port_t, data: Data) throws](/documentation/browserenginekit/layerhierarchyhandle/init(port:data:))

#### Instance Methods

- [func encode((mach_port_t, Data) -> Void)](/documentation/browserenginekit/layerhierarchyhandle/encode(_:))

### Visibility propagation

- [Propagating view visibility information to extension processes](/documentation/browserenginekit/propagating-view-visibility-information-to-browser-extensions)
- [func createVisibilityPropagationInteraction() -> any UIInteraction](/documentation/browserenginekit/renderingprocess/createvisibilitypropagationinteraction())
- [func createVisibilityPropagationInteraction() -> any UIInteraction](/documentation/browserenginekit/webcontentprocess/createvisibilitypropagationinteraction())
- [Text interaction](/documentation/browserenginekit/text-interaction)

### Custom text views

- [Integrating custom browser text views with UIKit](/documentation/browserenginekit/integrating-custom-browser-text-views-with-uikit)
- [Supporting extended text interactions](/documentation/browserenginekit/support-extended-text-interactions)
- [BETextInput](/documentation/browserenginekit/betextinput)

#### Updating the text system

- [var asyncInputDelegate: (any BETextInputDelegate)?](/documentation/browserenginekit/betextinput/asyncinputdelegate)
- [func canPerformAction(Selector, withSender: Any?) -> Bool](/documentation/browserenginekit/betextinput/canperformaction(_:withsender:))

#### Handling text input

- [var isEditable: Bool](/documentation/browserenginekit/betextinput/iseditable)
- [func handleKeyEntry(BEKeyEntry, completionHandler: (BEKeyEntry, Bool) -> Void)](/documentation/browserenginekit/betextinput/handlekeyentry(_:completionhandler:))
- [func shiftKeyStateChanged(fromState: BEKeyModifierFlags, toState: BEKeyModifierFlags)](/documentation/browserenginekit/betextinput/shiftkeystatechanged(fromstate:tostate:))
- [func text(in: UITextRange) -> String?](/documentation/browserenginekit/betextinput/text(in:))
- [func offset(from: UITextPosition, to: UITextPosition) -> Int](/documentation/browserenginekit/betextinput/offset(from:to:))
- [func setBaseWritingDirection(NSWritingDirection, for: UITextRange)](/documentation/browserenginekit/betextinput/setbasewritingdirection(_:for:))
- [func delete(in: UITextStorageDirection, to: UITextGranularity)](/documentation/browserenginekit/betextinput/delete(in:to:))

#### Editing and correcting text

- [func transposeCharactersAroundSelection()](/documentation/browserenginekit/betextinput/transposecharactersaroundselection())
- [func replaceText(String, withText: String, options: BETextReplacementOptions, completionHandler: ([UITextSelectionRect]) -> Void)](/documentation/browserenginekit/betextinput/replacetext(_:withtext:options:completionhandler:))
- [func requestTextContextForAutocorrection(completionHandler: (BETextDocumentContext) -> Void)](/documentation/browserenginekit/betextinput/requesttextcontextforautocorrection(completionhandler:))
- [func requestTextRects(for: String, withCompletionHandler: ([UITextSelectionRect]) -> Void)](/documentation/browserenginekit/betextinput/requesttextrects(for:withcompletionhandler:))
- [var automaticallyPresentEditMenu: Bool](/documentation/browserenginekit/betextinput/automaticallypresenteditmenu)
- [func requestPreferredArrowDirectionForEditMenu(completionHandler: (UIEditMenuArrowDirection) -> Void)](/documentation/browserenginekit/betextinput/requestpreferredarrowdirectionforeditmenu(completionhandler:))
- [func systemWillPresentEditMenu(withAnimator: any UIEditMenuInteractionAnimating)](/documentation/browserenginekit/betextinput/systemwillpresenteditmenu(withanimator:))
- [func systemWillDismissEditMenu(withAnimator: any UIEditMenuInteractionAnimating)](/documentation/browserenginekit/betextinput/systemwilldismisseditmenu(withanimator:))

#### Input traits

- [var extendedTextInputTraits: (any BEExtendedTextInputTraits)?](/documentation/browserenginekit/betextinput/extendedtextinputtraits)
- [func textStyling(at: UITextPosition, in: UITextStorageDirection) -> [NSAttributedString.Key : Any]?](/documentation/browserenginekit/betextinput/textstyling(at:in:))

#### Replacing text

- [var isReplaceAllowed: Bool](/documentation/browserenginekit/betextinput/isreplaceallowed)
- [func replaceSelectedText(String, withText: String)](/documentation/browserenginekit/betextinput/replaceselectedtext(_:withtext:))

#### Handling text gestures

- [func updateCurrentSelection(to: CGPoint, from: BEGestureType, in: UIGestureRecognizer.State)](/documentation/browserenginekit/betextinput/updatecurrentselection(to:from:in:))
- [func setSelection(from: CGPoint, to: CGPoint, gesture: BEGestureType, state: UIGestureRecognizer.State)](/documentation/browserenginekit/betextinput/setselection(from:to:gesture:state:))
- [func adjustSelectionBoundary(to: CGPoint, touchPhase: BESelectionTouchPhase, baseIsStart: Bool, flags: BESelectionFlags)](/documentation/browserenginekit/betextinput/adjustselectionboundary(to:touchphase:baseisstart:flags:))
- [func textInteractionGesture(BEGestureType, shouldBeginAt: CGPoint) -> Bool](/documentation/browserenginekit/betextinput/textinteractiongesture(_:shouldbeginat:))

#### Selecting text

- [var selectedText: String?](/documentation/browserenginekit/betextinput/selectedtext)
- [var selectedTextRange: UITextRange?](/documentation/browserenginekit/betextinput/selectedtextrange)
- [var isSelectionAtDocumentStart: Bool](/documentation/browserenginekit/betextinput/isselectionatdocumentstart)
- [func caretRect(for: UITextPosition) -> CGRect](/documentation/browserenginekit/betextinput/caretrect(for:))
- [func selectionRects(for: UITextRange) -> [UITextSelectionRect]](/documentation/browserenginekit/betextinput/selectionrects(for:))
- [func selectWordForReplacement()](/documentation/browserenginekit/betextinput/selectwordforreplacement())
- [func updateSelection(extent: CGPoint, boundary: UITextGranularity, completionHandler: (Bool) -> Void)](/documentation/browserenginekit/betextinput/updateselection(extent:boundary:completionhandler:))
- [func selectText(in: UITextGranularity, at: CGPoint, completionHandler: () -> Void)](/documentation/browserenginekit/betextinput/selecttext(in:at:completionhandler:))
- [func selectPosition(at: CGPoint, completionHandler: () -> Void)](/documentation/browserenginekit/betextinput/selectposition(at:completionhandler:))
- [func selectPosition(at: CGPoint, for: BETextDocumentRequest, completionHandler: (BETextDocumentContext) -> Void)](/documentation/browserenginekit/betextinput/selectposition(at:for:completionhandler:))
- [func adjustSelection(by: BEDirectionalTextRange, completionHandler: () -> Void)](/documentation/browserenginekit/betextinput/adjustselection(by:completionhandler:))
- [func move(byOffset: Int)](/documentation/browserenginekit/betextinput/move(byoffset:))
- [func moveSelection(atBoundary: UITextGranularity, in: UITextStorageDirection, completionHandler: () -> Void)](/documentation/browserenginekit/betextinput/moveselection(atboundary:in:completionhandler:))
- [func selectTextForEditMenuWithLocation(inView: CGPoint, completionHandler: (Bool, String?, NSRange) -> Void)](/documentation/browserenginekit/betextinput/selecttextforeditmenuwithlocation(inview:completionhandler:))

#### Marking text

- [var markedText: String?](/documentation/browserenginekit/betextinput/markedtext)
- [var attributedMarkedText: NSAttributedString?](/documentation/browserenginekit/betextinput/attributedmarkedtext)
- [var markedTextRange: UITextRange?](/documentation/browserenginekit/betextinput/markedtextrange)
- [var hasMarkedText: Bool](/documentation/browserenginekit/betextinput/hasmarkedtext)
- [func setMarkedText(String?, selectedRange: NSRange)](/documentation/browserenginekit/betextinput/setmarkedtext(_:selectedrange:))
- [func setAttributedMarkedText(NSAttributedString?, selectedRange: NSRange)](/documentation/browserenginekit/betextinput/setattributedmarkedtext(_:selectedrange:))
- [func unmarkText()](/documentation/browserenginekit/betextinput/unmarktext())
- [func isPointNearMarkedText(CGPoint) -> Bool](/documentation/browserenginekit/betextinput/ispointnearmarkedtext(_:))

#### Document context

- [func requestDocumentContext(BETextDocumentRequest, completionHandler: (BETextDocumentContext) -> Void)](/documentation/browserenginekit/betextinput/requestdocumentcontext(_:completionhandler:))

#### Dictation

- [func willInsertFinalDictationResult()](/documentation/browserenginekit/betextinput/willinsertfinaldictationresult())
- [func replaceDictatedText(String, withText: String)](/documentation/browserenginekit/betextinput/replacedictatedtext(_:withtext:))
- [func didInsertFinalDictationResult()](/documentation/browserenginekit/betextinput/didinsertfinaldictationresult())

#### Text alternatives

- [func alternativesForSelectedText() -> [BETextAlternatives]?](/documentation/browserenginekit/betextinput/alternativesforselectedtext())
- [func add(BETextAlternatives)](/documentation/browserenginekit/betextinput/add(_:))
- [func insert(BETextAlternatives)](/documentation/browserenginekit/betextinput/insert(_:)-6x7hd)

#### Text placeholders

- [func insertTextPlaceholder(size: CGSize, completionHandler: (UITextPlaceholder) -> Void)](/documentation/browserenginekit/betextinput/inserttextplaceholder(size:completionhandler:))
- [func remove(UITextPlaceholder, willInsertText: Bool, completionHandler: () -> Void)](/documentation/browserenginekit/betextinput/remove(_:willinserttext:completionhandler:))

#### Text suggestions

- [func insert(BETextSuggestion)](/documentation/browserenginekit/betextinput/insert(_:)-5iryn)

#### Geometry

- [var textInputView: UIView](/documentation/browserenginekit/betextinput/textinputview)
- [var textFirstRect: CGRect](/documentation/browserenginekit/betextinput/textfirstrect)
- [var textLastRect: CGRect](/documentation/browserenginekit/betextinput/textlastrect)
- [var unobscuredContentRect: CGRect](/documentation/browserenginekit/betextinput/unobscuredcontentrect)
- [var unscaledView: UIView](/documentation/browserenginekit/betextinput/unscaledview)
- [var selectionClipRect: CGRect](/documentation/browserenginekit/betextinput/selectioncliprect)
- [func autoscroll(to: CGPoint)](/documentation/browserenginekit/betextinput/autoscroll(to:))
- [func cancelAutoscroll()](/documentation/browserenginekit/betextinput/cancelautoscroll())

#### Instance Properties

- [var selectionContainerViewAboveText: UIView?](/documentation/browserenginekit/betextinput/selectioncontainerviewabovetext)
- [var selectionContainerViewBelowText: UIView?](/documentation/browserenginekit/betextinput/selectioncontainerviewbelowtext)

#### Instance Methods

- [func keyboardWillDismiss()](/documentation/browserenginekit/betextinput/keyboardwilldismiss())
- [func removeTextAlternatives()](/documentation/browserenginekit/betextinput/removetextalternatives())
- [BETextInputDelegate](/documentation/browserenginekit/betextinputdelegate)

#### Text selection

- [func selectionWillChange(for: any BETextInput)](/documentation/browserenginekit/betextinputdelegate/selectionwillchange(for:))
- [func selectionDidChange(for: any BETextInput)](/documentation/browserenginekit/betextinputdelegate/selectiondidchange(for:))

#### Deferring actions to the text system

- [func shouldDeferEventHandlingToSystem(for: any BETextInput, context: BEKeyEntryContext) -> Bool](/documentation/browserenginekit/betextinputdelegate/shoulddefereventhandlingtosystem(for:context:))
- [func textInput(any BETextInput, deferReplaceTextActionToSystem: Any)](/documentation/browserenginekit/betextinputdelegate/textinput(_:deferreplacetextactiontosystem:))

#### Providing completion suggestions

- [func textInput(any BETextInput, setCandidateSuggestions: [BETextSuggestion]?)](/documentation/browserenginekit/betextinputdelegate/textinput(_:setcandidatesuggestions:))

#### Removing stored context information

- [func invalidateTextEntryContext(for: any BETextInput)](/documentation/browserenginekit/betextinputdelegate/invalidatetextentrycontext(for:))

### Interaction responses

- [BETextInteraction](/documentation/browserenginekit/betextinteraction)

#### Text selection

- [var delegate: (any BETextInteractionDelegate)?](/documentation/browserenginekit/betextinteraction/delegate)
- [BETextInteractionDelegate](/documentation/browserenginekit/betextinteractiondelegate)

##### Text selection changes

- [func systemWillChangeSelection(for: BETextInteraction)](/documentation/browserenginekit/betextinteractiondelegate/systemwillchangeselection(for:))
- [func systemDidChangeSelection(for: BETextInteraction)](/documentation/browserenginekit/betextinteractiondelegate/systemdidchangeselection(for:))
- [var textSelectionDisplayInteraction: UITextSelectionDisplayInteraction](/documentation/browserenginekit/betextinteraction/textselectiondisplayinteraction)
- [func selectionBoundaryAdjusted(to: CGPoint, touchPhase: BESelectionTouchPhase, flags: BESelectionFlags)](/documentation/browserenginekit/betextinteraction/selectionboundaryadjusted(to:touchphase:flags:))
- [func selectionChangedWithGesture(at: CGPoint, gesture: BEGestureType, state: UIGestureRecognizer.State, flags: BESelectionFlags)](/documentation/browserenginekit/betextinteraction/selectionchangedwithgesture(at:gesture:state:flags:))

#### Menus

- [func presentEditMenuForSelection()](/documentation/browserenginekit/betextinteraction/presenteditmenuforselection())
- [func dismissEditMenuForSelection()](/documentation/browserenginekit/betextinteraction/dismisseditmenuforselection())
- [var contextMenuInteraction: UIContextMenuInteraction](/documentation/browserenginekit/betextinteraction/contextmenuinteraction)
- [var contextMenuInteractionDelegate: (any UIContextMenuInteractionDelegate)?](/documentation/browserenginekit/betextinteraction/contextmenuinteractiondelegate)

#### Text replacements

- [func addShortcut(forText: String, from: CGRect)](/documentation/browserenginekit/betextinteraction/addshortcut(fortext:from:))
- [func showReplacements(forText: String)](/documentation/browserenginekit/betextinteraction/showreplacements(fortext:))

#### Sharing and defining text

- [func share(text: String, from: CGRect)](/documentation/browserenginekit/betextinteraction/share(text:from:))
- [func showDictionary(forTextInContext: String, definingTextInRange: NSRange, from: CGRect)](/documentation/browserenginekit/betextinteraction/showdictionary(fortextincontext:definingtextinrange:from:))

#### Translation and transliteration

- [func translate(text: String, from: CGRect)](/documentation/browserenginekit/betextinteraction/translate(text:from:))
- [func transliterateChinese(forText: String)](/documentation/browserenginekit/betextinteraction/transliteratechinese(fortext:))

#### UI updates

- [func editabilityChanged()](/documentation/browserenginekit/betextinteraction/editabilitychanged())
- [func refreshKeyboardUI()](/documentation/browserenginekit/betextinteraction/refreshkeyboardui())
- [BETextInteractionDelegate](/documentation/browserenginekit/betextinteractiondelegate)

#### Text selection changes

- [func systemWillChangeSelection(for: BETextInteraction)](/documentation/browserenginekit/betextinteractiondelegate/systemwillchangeselection(for:))
- [func systemDidChangeSelection(for: BETextInteraction)](/documentation/browserenginekit/betextinteractiondelegate/systemdidchangeselection(for:))
- [BEResponderEditActions](/documentation/browserenginekit/berespondereditactions)

#### Finding and replacing text

- [func findSelected(Any?)](/documentation/browserenginekit/berespondereditactions/findselected(_:))
- [func promptForReplace(Any?)](/documentation/browserenginekit/berespondereditactions/promptforreplace(_:))
- [func replace(Any?)](/documentation/browserenginekit/berespondereditactions/replace(_:))
- [func addShortcut(Any?)](/documentation/browserenginekit/berespondereditactions/addshortcut(_:))

#### Defining and sharing text

- [func lookup(Any?)](/documentation/browserenginekit/berespondereditactions/lookup(_:))
- [func share(Any?)](/documentation/browserenginekit/berespondereditactions/share(_:))

#### Translating and transliterating text

- [func translate(Any?)](/documentation/browserenginekit/berespondereditactions/translate(_:))
- [func transliterateChinese(Any?)](/documentation/browserenginekit/berespondereditactions/transliteratechinese(_:))
- [BEGestureType](/documentation/browserenginekit/begesturetype)

#### Enumeration Cases

- [case doubleTap](/documentation/browserenginekit/begesturetype/doubletap)
- [case doubleTapAndHold](/documentation/browserenginekit/begesturetype/doubletapandhold)
- [case forceTouch](/documentation/browserenginekit/begesturetype/forcetouch)
- [case imPhraseBoundaryDrag](/documentation/browserenginekit/begesturetype/imphraseboundarydrag)
- [case loupe](/documentation/browserenginekit/begesturetype/loupe)
- [case oneFingerDoubleTap](/documentation/browserenginekit/begesturetype/onefingerdoubletap)
- [case oneFingerTap](/documentation/browserenginekit/begesturetype/onefingertap)
- [case oneFingerTripleTap](/documentation/browserenginekit/begesturetype/onefingertripletap)
- [case twoFingerRangedSelectGesture](/documentation/browserenginekit/begesturetype/twofingerrangedselectgesture)
- [case twoFingerSingleTap](/documentation/browserenginekit/begesturetype/twofingersingletap)

#### Initializers

- [init?(rawValue: Int)](/documentation/browserenginekit/begesturetype/init(rawvalue:))
- [BEResponderEditActions](/documentation/browserenginekit/berespondereditactions)

#### Finding and replacing text

- [func findSelected(Any?)](/documentation/browserenginekit/berespondereditactions/findselected(_:))
- [func promptForReplace(Any?)](/documentation/browserenginekit/berespondereditactions/promptforreplace(_:))
- [func replace(Any?)](/documentation/browserenginekit/berespondereditactions/replace(_:))
- [func addShortcut(Any?)](/documentation/browserenginekit/berespondereditactions/addshortcut(_:))

#### Defining and sharing text

- [func lookup(Any?)](/documentation/browserenginekit/berespondereditactions/lookup(_:))
- [func share(Any?)](/documentation/browserenginekit/berespondereditactions/share(_:))

#### Translating and transliterating text

- [func translate(Any?)](/documentation/browserenginekit/berespondereditactions/translate(_:))
- [func transliterateChinese(Any?)](/documentation/browserenginekit/berespondereditactions/transliteratechinese(_:))

### Text selection

- [BETextSelectionDirectionNavigation](/documentation/browserenginekit/betextselectiondirectionnavigation)

#### Instance Methods

- [func extend(in: UITextLayoutDirection)](/documentation/browserenginekit/betextselectiondirectionnavigation/extend(in:))
- [func extend(in: UITextStorageDirection, by: UITextGranularity)](/documentation/browserenginekit/betextselectiondirectionnavigation/extend(in:by:))
- [func move(in: UITextLayoutDirection)](/documentation/browserenginekit/betextselectiondirectionnavigation/move(in:))
- [func move(in: UITextStorageDirection, by: UITextGranularity)](/documentation/browserenginekit/betextselectiondirectionnavigation/move(in:by:))
- [BESelectionFlags](/documentation/browserenginekit/beselectionflags)

#### Initializers

- [init(rawValue: UInt)](/documentation/browserenginekit/beselectionflags/init(rawvalue:))

#### Type Properties

- [static var phraseBoundaryChanged: BESelectionFlags](/documentation/browserenginekit/beselectionflags/phraseboundarychanged)
- [static var selectionFlipped: BESelectionFlags](/documentation/browserenginekit/beselectionflags/selectionflipped)
- [static var wordIsNearTap: BESelectionFlags](/documentation/browserenginekit/beselectionflags/wordisneartap)
- [BESelectionTouchPhase](/documentation/browserenginekit/beselectiontouchphase)

#### Enumeration Cases

- [case ended](/documentation/browserenginekit/beselectiontouchphase/ended)
- [case endedMovingBackward](/documentation/browserenginekit/beselectiontouchphase/endedmovingbackward)
- [case endedMovingForward](/documentation/browserenginekit/beselectiontouchphase/endedmovingforward)
- [case endedNotMoving](/documentation/browserenginekit/beselectiontouchphase/endednotmoving)
- [case moved](/documentation/browserenginekit/beselectiontouchphase/moved)
- [case started](/documentation/browserenginekit/beselectiontouchphase/started)

#### Initializers

- [init?(rawValue: Int)](/documentation/browserenginekit/beselectiontouchphase/init(rawvalue:))

### Keyboard input

- [BEKeyEntry](/documentation/browserenginekit/bekeyentry)

#### Identifying the key

- [var key: UIKey](/documentation/browserenginekit/bekeyentry/key)

#### Getting information about the keypress

- [var state: BEKeyEntry.KeyPressState](/documentation/browserenginekit/bekeyentry/state)
- [BEKeyEntry.KeyPressState](/documentation/browserenginekit/bekeyentry/keypressstate)

##### Key states

- [case down](/documentation/browserenginekit/bekeyentry/keypressstate/down)
- [case up](/documentation/browserenginekit/bekeyentry/keypressstate/up)

##### Creating a key-press state

- [init?(rawValue: Int)](/documentation/browserenginekit/bekeyentry/keypressstate/init(rawvalue:))
- [var isKeyRepeating: Bool](/documentation/browserenginekit/bekeyentry/iskeyrepeating)
- [var timestamp: TimeInterval](/documentation/browserenginekit/bekeyentry/timestamp)
- [BEKeyEntryContext](/documentation/browserenginekit/bekeyentrycontext)

#### Creating a key entry context

- [init(keyEntry: BEKeyEntry)](/documentation/browserenginekit/bekeyentrycontext/init(keyentry:))

#### Getting the information about the key event

- [var keyEntry: BEKeyEntry](/documentation/browserenginekit/bekeyentrycontext/keyentry)
- [var shouldInsertCharacter: Bool](/documentation/browserenginekit/bekeyentrycontext/shouldinsertcharacter)
- [var shouldEvaluateForInputSystemHandling: Bool](/documentation/browserenginekit/bekeyentrycontext/shouldevaluateforinputsystemhandling)

#### Getting information about the text document

- [var isDocumentEditable: Bool](/documentation/browserenginekit/bekeyentrycontext/isdocumenteditable)
- [BEKeyModifierFlags](/documentation/browserenginekit/bekeymodifierflags)

#### Getting caps-shift information

- [case capsLock](/documentation/browserenginekit/bekeymodifierflags/capslock)
- [case shift](/documentation/browserenginekit/bekeymodifierflags/shift)
- [case none](/documentation/browserenginekit/bekeymodifierflags/none)

#### Initializing the flags

- [init?(rawValue: Int)](/documentation/browserenginekit/bekeymodifierflags/init(rawvalue:))

### Replacements and AutoFill

- [BEAutoFillTextSuggestion](/documentation/browserenginekit/beautofilltextsuggestion)

#### Instance Properties

- [var contents: [UITextContentType : String]](/documentation/browserenginekit/beautofilltextsuggestion/contents)
- [BETextAlternatives](/documentation/browserenginekit/betextalternatives)

#### Instance Properties

- [var alternativeStrings: [String]](/documentation/browserenginekit/betextalternatives/alternativestrings)
- [var primaryString: String](/documentation/browserenginekit/betextalternatives/primarystring)
- [BETextDocumentContext](/documentation/browserenginekit/betextdocumentcontext)

#### Creating a text document context

- [init(attributedSelectedText: NSAttributedString?, contextBefore: NSAttributedString?, contextAfter: NSAttributedString?, markedText: NSAttributedString?, selectedRangeInMarkedText: NSRange)](/documentation/browserenginekit/betextdocumentcontext/init(attributedselectedtext:contextbefore:contextafter:markedtext:selectedrangeinmarkedtext:))
- [init(selectedText: String?, contextBefore: String?, contextAfter: String?, markedText: String?, selectedRangeInMarkedText: NSRange)](/documentation/browserenginekit/betextdocumentcontext/init(selectedtext:contextbefore:contextafter:markedtext:selectedrangeinmarkedtext:))

#### Getting information about the selected range

- [var autocorrectedRanges: [NSValue]](/documentation/browserenginekit/betextdocumentcontext/autocorrectedranges)

#### Adding text rectangles

- [func addTextRect(CGRect, forCharacterRange: NSRange)](/documentation/browserenginekit/betextdocumentcontext/addtextrect(_:forcharacterrange:))
- [BETextDocumentRequest](/documentation/browserenginekit/betextdocumentrequest)

#### Instance Properties

- [var granularityCount: Int](/documentation/browserenginekit/betextdocumentrequest/granularitycount)
- [var options: BETextDocumentRequest.Options](/documentation/browserenginekit/betextdocumentrequest/options-swift.property)
- [var surroundingGranularity: UITextGranularity](/documentation/browserenginekit/betextdocumentrequest/surroundinggranularity)
- [BETextDocumentRequest.Options](/documentation/browserenginekit/betextdocumentrequest/options-swift.struct)

#### Initializers

- [init(rawValue: Int)](/documentation/browserenginekit/betextdocumentrequest/options-swift.struct/init(rawvalue:))

#### Type Properties

- [static var attributedText: BETextDocumentRequest.Options](/documentation/browserenginekit/betextdocumentrequest/options-swift.struct/attributedtext)
- [static var autocorrectedRanges: BETextDocumentRequest.Options](/documentation/browserenginekit/betextdocumentrequest/options-swift.struct/autocorrectedranges)
- [static var markedTextRects: BETextDocumentRequest.Options](/documentation/browserenginekit/betextdocumentrequest/options-swift.struct/markedtextrects)
- [static var text: BETextDocumentRequest.Options](/documentation/browserenginekit/betextdocumentrequest/options-swift.struct/text)
- [static var textRects: BETextDocumentRequest.Options](/documentation/browserenginekit/betextdocumentrequest/options-swift.struct/textrects)
- [BETextSuggestion](/documentation/browserenginekit/betextsuggestion)

#### Creating a text suggestion

- [init(inputText: String)](/documentation/browserenginekit/betextsuggestion/init(inputtext:))

#### Getting the suggested text

- [var inputText: String](/documentation/browserenginekit/betextsuggestion/inputtext)
- [BETextReplacementOptions](/documentation/browserenginekit/betextreplacementoptions)

#### Initializers

- [init(rawValue: UInt)](/documentation/browserenginekit/betextreplacementoptions/init(rawvalue:))

#### Type Properties

- [static var addUnderline: BETextReplacementOptions](/documentation/browserenginekit/betextreplacementoptions/addunderline)

### Information about text

- [BEExtendedTextInputTraits](/documentation/browserenginekit/beextendedtextinputtraits)

#### Instance Properties

- [var insertionPointColor: UIColor?](/documentation/browserenginekit/beextendedtextinputtraits/insertionpointcolor)
- [var isSingleLineDocument: Bool](/documentation/browserenginekit/beextendedtextinputtraits/issinglelinedocument)
- [var isTypingAdaptationEnabled: Bool](/documentation/browserenginekit/beextendedtextinputtraits/istypingadaptationenabled)
- [var selectionHandleColor: UIColor?](/documentation/browserenginekit/beextendedtextinputtraits/selectionhandlecolor)
- [var selectionHighlightColor: UIColor?](/documentation/browserenginekit/beextendedtextinputtraits/selectionhighlightcolor)
- [BEDirectionalTextRange](/documentation/browserenginekit/bedirectionaltextrange)

#### Initializers

- [init()](/documentation/browserenginekit/bedirectionaltextrange/init())
- [init(offset: Int, length: Int)](/documentation/browserenginekit/bedirectionaltextrange/init(offset:length:))

#### Instance Properties

- [var length: Int](/documentation/browserenginekit/bedirectionaltextrange/length)
- [var offset: Int](/documentation/browserenginekit/bedirectionaltextrange/offset)
- [BEWebAppManifest](/documentation/browserenginekit/bewebappmanifest)

### Creating a web app manifest

- [init?(JSONData: Data, manifestURL: URL)](/documentation/browserenginekit/bewebappmanifest/init(jsondata:manifesturl:)-4zjpz)
- [init?(jsonData: Data, manifestURL: URL)](/documentation/browserenginekit/bewebappmanifest/init(jsondata:manifesturl:))

### Getting manifest information

- [var jsonData: Data](/documentation/browserenginekit/bewebappmanifest/jsondata)
- [var manifestURL: URL](/documentation/browserenginekit/bewebappmanifest/manifesturl)

## Scroll view interaction

- [BEScrollView](/documentation/browserenginekit/bescrollview)

### Responding to scroll updates

- [var delegate: (any BEScrollViewDelegate)?](/documentation/browserenginekit/bescrollview/delegate)
- [BEScrollViewScrollUpdate](/documentation/browserenginekit/bescrollviewscrollupdate)

### Retrieving scroll state information

- [var timestamp: TimeInterval](/documentation/browserenginekit/bescrollviewscrollupdate/timestamp)
- [var phase: BEScrollViewScrollUpdate.Phase](/documentation/browserenginekit/bescrollviewscrollupdate/phase-swift.property)
- [BEScrollViewScrollUpdate.Phase](/documentation/browserenginekit/bescrollviewscrollupdate/phase-swift.enum)

#### Enumeration Cases

- [case began](/documentation/browserenginekit/bescrollviewscrollupdate/phase-swift.enum/began)
- [case cancelled](/documentation/browserenginekit/bescrollviewscrollupdate/phase-swift.enum/cancelled)
- [case changed](/documentation/browserenginekit/bescrollviewscrollupdate/phase-swift.enum/changed)
- [case ended](/documentation/browserenginekit/bescrollviewscrollupdate/phase-swift.enum/ended)

#### Initializers

- [init?(rawValue: Int)](/documentation/browserenginekit/bescrollviewscrollupdate/phase-swift.enum/init(rawvalue:))

### Transforming coordinates

- [func location(in: UIView?) -> CGPoint](/documentation/browserenginekit/bescrollviewscrollupdate/location(in:))
- [func translation(in: UIView?) -> CGPoint](/documentation/browserenginekit/bescrollviewscrollupdate/translation(in:))
- [BEScrollViewDelegate](/documentation/browserenginekit/bescrollviewdelegate)

### Nesting sibling scroll views

- [func parentScrollView(for: BEScrollView) -> BEScrollView?](/documentation/browserenginekit/bescrollviewdelegate/parentscrollview(for:))

### Handling scroll events

- [func scrollView(BEScrollView, handle: BEScrollViewScrollUpdate, completion: (Bool) -> Void)](/documentation/browserenginekit/bescrollviewdelegate/scrollview(_:handle:completion:))

## Drag interaction

- [BEDragInteraction](/documentation/browserenginekit/bedraginteraction)

### Creating a drag interaction

- [init(delegate: any BEDragInteractionDelegate)](/documentation/browserenginekit/bedraginteraction/init(delegate:))

### Handling drag gestures

- [var delegate: (any BEDragInteractionDelegate)?](/documentation/browserenginekit/bedraginteraction/delegate)
- [BEDragInteractionDelegate](/documentation/browserenginekit/bedraginteractiondelegate)

#### Participating in drag gestures

- [func dragInteraction(BEDragInteraction, prepare: any UIDragSession, completion: () -> Bool)](/documentation/browserenginekit/bedraginteractiondelegate/draginteraction(_:prepare:completion:))
- [func dragInteraction(BEDragInteraction, itemsForAddingTo: any UIDragSession, forTouchAt: CGPoint, completion: ([UIDragItem]) -> Bool)](/documentation/browserenginekit/bedraginteractiondelegate/draginteraction(_:itemsforaddingto:fortouchat:completion:))
- [BEDragInteractionDelegate](/documentation/browserenginekit/bedraginteractiondelegate)

### Participating in drag gestures

- [func dragInteraction(BEDragInteraction, prepare: any UIDragSession, completion: () -> Bool)](/documentation/browserenginekit/bedraginteractiondelegate/draginteraction(_:prepare:completion:))
- [func dragInteraction(BEDragInteraction, itemsForAddingTo: any UIDragSession, forTouchAt: CGPoint, completion: ([UIDragItem]) -> Bool)](/documentation/browserenginekit/bedraginteractiondelegate/draginteraction(_:itemsforaddingto:fortouchat:completion:))

## Context menus

- [BEContextMenuConfiguration](/documentation/browserenginekit/becontextmenuconfiguration)

### Creating a context menu configuration

- [init()](/documentation/browserenginekit/becontextmenuconfiguration/init())

### Fulfilling the configuration

- [func fulfill(using: UIContextMenuConfiguration?) -> Bool](/documentation/browserenginekit/becontextmenuconfiguration/fulfill(using:))

## Accessibility

- [BEAccessibilityTextMarkerSupport](/documentation/browserenginekit/beaccessibilitytextmarkersupport)

### Text positions

- [func accessibilityNextTextMarker(BEAccessibilityTextMarker) -> BEAccessibilityTextMarker?](/documentation/browserenginekit/beaccessibilitytextmarkersupport/accessibilitynexttextmarker(_:))
- [func accessibilityPreviousTextMarker(BEAccessibilityTextMarker) -> BEAccessibilityTextMarker?](/documentation/browserenginekit/beaccessibilitytextmarkersupport/accessibilityprevioustextmarker(_:))
- [func accessibilityLineStartMarker(for: BEAccessibilityTextMarker) -> BEAccessibilityTextMarker?](/documentation/browserenginekit/beaccessibilitytextmarkersupport/accessibilitylinestartmarker(for:))
- [func accessibilityLineEndMarker(for: BEAccessibilityTextMarker) -> BEAccessibilityTextMarker?](/documentation/browserenginekit/beaccessibilitytextmarkersupport/accessibilitylineendmarker(for:))
- [func accessibilityMarker(for: CGPoint) -> BEAccessibilityTextMarker?](/documentation/browserenginekit/beaccessibilitytextmarkersupport/accessibilitymarker(for:))
- [func accessibilityTextMarker(forPosition: Int) -> BEAccessibilityTextMarker?](/documentation/browserenginekit/beaccessibilitytextmarkersupport/accessibilitytextmarker(forposition:))
- [BEAccessibilityTextMarker](/documentation/browserenginekit/beaccessibilitytextmarker)

### Text ranges

- [func accessibilityBounds(for: BEAccessibilityTextMarker.Range) -> CGRect](/documentation/browserenginekit/beaccessibilitytextmarkersupport/accessibilitybounds(for:))
- [func accessibilityTextMarkerRange() -> BEAccessibilityTextMarker.Range](/documentation/browserenginekit/beaccessibilitytextmarkersupport/accessibilitytextmarkerrange())
- [func accessibilityTextMarkerRangeForCurrentSelection() -> BEAccessibilityTextMarker.Range?](/documentation/browserenginekit/beaccessibilitytextmarkersupport/accessibilitytextmarkerrangeforcurrentselection())
- [func accessibilityTextMarkerRange(for: NSRange) -> BEAccessibilityTextMarker.Range?](/documentation/browserenginekit/beaccessibilitytextmarkersupport/accessibilitytextmarkerrange(for:))
- [func accessibilityRange(for: BEAccessibilityTextMarker.Range) -> NSRange](/documentation/browserenginekit/beaccessibilitytextmarkersupport/accessibilityrange(for:))
- [BEAccessibilityTextMarker.Range](/documentation/browserenginekit/beaccessibilitytextmarker/range)

#### Range boundaries

- [var startMarker: BEAccessibilityTextMarker](/documentation/browserenginekit/beaccessibilitytextmarker/range/startmarker)
- [var endMarker: BEAccessibilityTextMarker](/documentation/browserenginekit/beaccessibilitytextmarker/range/endmarker)

### Instance Methods

- [func accessibilityContent(for: BEAccessibilityTextMarker.Range) -> String?](/documentation/browserenginekit/beaccessibilitytextmarkersupport/accessibilitycontent(for:))
- [static var valueChangedNotification: UIAccessibility.Notification](/documentation/browserenginekit/beaccessibility/valuechangednotification)
- [static var selectionChangedNotification: UIAccessibility.Notification](/documentation/browserenginekit/beaccessibility/selectionchangednotification)
- [BEAccessibilityContainerType](/documentation/browserenginekit/beaccessibilitycontainertype)

### Container types

- [static var landmark: BEAccessibilityContainerType](/documentation/browserenginekit/beaccessibilitycontainertype/landmark)
- [static var table: BEAccessibilityContainerType](/documentation/browserenginekit/beaccessibilitycontainertype/table)
- [static var list: BEAccessibilityContainerType](/documentation/browserenginekit/beaccessibilitycontainertype/list)
- [static var fieldset: BEAccessibilityContainerType](/documentation/browserenginekit/beaccessibilitycontainertype/fieldset)
- [static var dialog: BEAccessibilityContainerType](/documentation/browserenginekit/beaccessibilitycontainertype/dialog)
- [static var tree: BEAccessibilityContainerType](/documentation/browserenginekit/beaccessibilitycontainertype/tree)
- [static var frame: BEAccessibilityContainerType](/documentation/browserenginekit/beaccessibilitycontainertype/frame)
- [static var article: BEAccessibilityContainerType](/documentation/browserenginekit/beaccessibilitycontainertype/article)
- [static var semanticGroup: BEAccessibilityContainerType](/documentation/browserenginekit/beaccessibilitycontainertype/semanticgroup)
- [static var scrollArea: BEAccessibilityContainerType](/documentation/browserenginekit/beaccessibilitycontainertype/scrollarea)
- [static var alert: BEAccessibilityContainerType](/documentation/browserenginekit/beaccessibilitycontainertype/alert)
- [static var descriptionList: BEAccessibilityContainerType](/documentation/browserenginekit/beaccessibilitycontainertype/descriptionlist)

### Initializers

- [init(rawValue: UInt)](/documentation/browserenginekit/beaccessibilitycontainertype/init(rawvalue:))
- [BEAccessibilityPressedState](/documentation/browserenginekit/beaccessibilitypressedstate)

### Element states

- [case `false`](/documentation/browserenginekit/beaccessibilitypressedstate/false)
- [case `true`](/documentation/browserenginekit/beaccessibilitypressedstate/true)
- [case mixed](/documentation/browserenginekit/beaccessibilitypressedstate/mixed)
- [case undefined](/documentation/browserenginekit/beaccessibilitypressedstate/undefined)

### Initializers

- [init?(rawValue: Int)](/documentation/browserenginekit/beaccessibilitypressedstate/init(rawvalue:))
- [static var menuItem: UIAccessibilityTraits](/documentation/browserenginekit/beaccessibility/menuitem)
- [static var popUpButton: UIAccessibilityTraits](/documentation/browserenginekit/beaccessibility/popupbutton)
- [static var radioButton: UIAccessibilityTraits](/documentation/browserenginekit/beaccessibility/radiobutton)
- [static var readOnly: UIAccessibilityTraits](/documentation/browserenginekit/beaccessibility/readonly)
- [static var visited: UIAccessibilityTraits](/documentation/browserenginekit/beaccessibility/visited)

## Just-in-time code compilation

- [Protecting code compiled just in time](/documentation/browserenginekit/protecting-code-compiled-just-in-time)
- [Improving control flow integrity with pointer authentication](/documentation/apple-silicon/improving-control-flow-integrity-with-pointer-authentication)
- [var BE_JIT_WRITE_PROTECT_TAG: Int](/documentation/browserenginecore/be_jit_write_protect_tag)

## Downloads

- [Downloading files in a web browser with an alternative browser engine](/documentation/browserenginekit/downloading-files-in-a-web-browser)
- [BEDownloadMonitor](/documentation/browserenginekit/bedownloadmonitor-9bwls)

### Creating a download monitor

- [init(sourceURL: URL, destinationURL: URL, observedProgress: Progress, liveActivityAccessToken: Data)](/documentation/browserenginekit/bedownloadmonitor-9bwls/init(sourceurl:destinationurl:observedprogress:liveactivityaccesstoken:))
- [static func createAccessToken() -> Data?](/documentation/browserenginekit/bedownloadmonitor-9bwls/createaccesstoken())

### Creating a download placeholder

- [func useDownloadsFolder(placeholderType: UTType?, finalFileCreatedHandler: (BEDownloadMonitor.Location?) -> Void)](/documentation/browserenginekit/bedownloadmonitor-9bwls/usedownloadsfolder(placeholdertype:finalfilecreatedhandler:))
- [BEDownloadMonitor.Location](/documentation/browserenginekit/bedownloadmonitor-9bwls/location)

#### Getting information about a location

- [let url: URL](/documentation/browserenginekit/bedownloadmonitor-9bwls/location/url)
- [let bookmarkData: Data](/documentation/browserenginekit/bedownloadmonitor-9bwls/location/bookmarkdata)

### Reporting progress to the system

- [func beginMonitoring() async throws -> BEDownloadMonitor.Location?](/documentation/browserenginekit/bedownloadmonitor-9bwls/beginmonitoring())
- [func resumeMonitoring(placeholderURL: URL) async throws](/documentation/browserenginekit/bedownloadmonitor-9bwls/resumemonitoring(placeholderurl:))

### Getting information about a download

- [let sourceURL: URL](/documentation/browserenginekit/bedownloadmonitor-9bwls/sourceurl)
- [let destinationURL: URL](/documentation/browserenginekit/bedownloadmonitor-9bwls/destinationurl)

## Classes

- [BEAccessibilityRemoteElement](/documentation/browserenginekit/beaccessibilityremoteelement)

### Initializers

- [init(identifier: String, hostPid: pid_t)](/documentation/browserenginekit/beaccessibilityremoteelement/init(identifier:hostpid:))
- [BEAccessibilityRemoteHostElement](/documentation/browserenginekit/beaccessibilityremotehostelement)

### Initializers

- [init(identifier: String, remotePid: pid_t)](/documentation/browserenginekit/beaccessibilityremotehostelement/init(identifier:remotepid:))

### Instance Properties

- [var accessibilityContainer: AnyObject?](/documentation/browserenginekit/beaccessibilityremotehostelement/accessibilitycontainer)
- [BEMediaEnvironment](/documentation/browserenginekit/bemediaenvironment-15xci)
- [BEProcessCapability](/documentation/browserenginekit/beprocesscapability-76ijx)
- [BEWebContentFilter](/documentation/browserenginekit/bewebcontentfilter)

### Instance Methods

- [func allow(URL, completionHandler: (Bool, (any Error)?) -> Void)](/documentation/browserenginekit/bewebcontentfilter/allow(_:completionhandler:))
- [func evaluateURL(URL, completionHandler: (Bool, Data?) -> Void)](/documentation/browserenginekit/bewebcontentfilter/evaluateurl(_:completionhandler:))

### Type Properties

- [class var shouldEvaluateURLs: Bool](/documentation/browserenginekit/bewebcontentfilter/shouldevaluateurls)

## Protocols

- [BEExtensionProcess](/documentation/browserenginekit/beextensionprocess)

### Instance Methods

- [func invalidate()](/documentation/browserenginekit/beextensionprocess/invalidate())
- [func makeLibXPCConnectionError() throws -> xpc_connection_t](/documentation/browserenginekit/beextensionprocess/makelibxpcconnectionerror())

## Structures

- [BEAccessibility](/documentation/browserenginekit/beaccessibility)

## Enumerations

- [RenderingExtensionFeature](/documentation/browserenginekit/renderingextensionfeature)

### Enumeration Cases

- [case coreML](/documentation/browserenginekit/renderingextensionfeature/coreml)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
