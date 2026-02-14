# InputMethodKit Documentation

Source: https://sosumi.ai/documentation/inputmethodkit

---
title: InputMethodKit
source: https://developer.apple.com/documentation/inputmethodkit
timestamp: 2026-02-13T18:58:12.824Z
---

## Classes

- [IMKCandidates](/documentation/inputmethodkit/imkcandidates)

### Initializing a Candidates Window

- [init!(server: IMKServer!, panelType: IMKCandidatePanelType)](/documentation/inputmethodkit/imkcandidates/init(server:paneltype:))

### Managing Selection Keys

- [func setSelectionKeys([Any]!)](/documentation/inputmethodkit/imkcandidates/setselectionkeys(_:))
- [func selectionKeys() -> [Any]!](/documentation/inputmethodkit/imkcandidates/selectionkeys())
- [func setSelectionKeysKeylayout(TISInputSource!)](/documentation/inputmethodkit/imkcandidates/setselectionkeyskeylayout(_:))
- [func selectionKeysKeylayout() -> Unmanaged<TISInputSource>!](/documentation/inputmethodkit/imkcandidates/selectionkeyskeylayout())

### Managing Window Visibility and Behavior

- [func show(IMKCandidatesLocationHint)](/documentation/inputmethodkit/imkcandidates/show(_:))
- [func hide()](/documentation/inputmethodkit/imkcandidates/hide())
- [func isVisible() -> Bool](/documentation/inputmethodkit/imkcandidates/isvisible())
- [func setDismissesAutomatically(Bool)](/documentation/inputmethodkit/imkcandidates/setdismissesautomatically(_:))
- [func dismissesAutomatically() -> Bool](/documentation/inputmethodkit/imkcandidates/dismissesautomatically())
- [func update()](/documentation/inputmethodkit/imkcandidates/update())

### Managing Window Type and Text Attributes

- [func panelType() -> IMKCandidatePanelType](/documentation/inputmethodkit/imkcandidates/paneltype())
- [func setPanelType(IMKCandidatePanelType)](/documentation/inputmethodkit/imkcandidates/setpaneltype(_:))
- [func setAttributes([AnyHashable : Any]!)](/documentation/inputmethodkit/imkcandidates/setattributes(_:))
- [func attributes() -> [AnyHashable : Any]!](/documentation/inputmethodkit/imkcandidates/attributes())

### Showing an Annotation Window

- [func showAnnotation(NSAttributedString!)](/documentation/inputmethodkit/imkcandidates/showannotation(_:))

### Constants

- [IMKCandidatePanelType](/documentation/inputmethodkit/imkcandidatepaneltype)

#### Constants

- [var kIMKSingleColumnScrollingCandidatePanel: Int](/documentation/inputmethodkit/kimksinglecolumnscrollingcandidatepanel)
- [var kIMKScrollingGridCandidatePanel: Int](/documentation/inputmethodkit/kimkscrollinggridcandidatepanel)
- [var kIMKSingleRowSteppingCandidatePanel: Int](/documentation/inputmethodkit/kimksinglerowsteppingcandidatepanel)
- [IMKCandidatesLocationHint](/documentation/inputmethodkit/imkcandidateslocationhint)

#### Constants

- [var kIMKLocateCandidatesAboveHint: Int](/documentation/inputmethodkit/kimklocatecandidatesabovehint)
- [var kIMKLocateCandidatesBelowHint: Int](/documentation/inputmethodkit/kimklocatecandidatesbelowhint)
- [var kIMKLocateCandidatesLeftHint: Int](/documentation/inputmethodkit/kimklocatecandidateslefthint)
- [var kIMKLocateCandidatesRightHint: Int](/documentation/inputmethodkit/kimklocatecandidatesrighthint)
- [let IMKCandidatesOpacityAttributeName: String](/documentation/inputmethodkit/imkcandidatesopacityattributename)

### Initializers

- [init!(server: IMKServer!, panelType: IMKCandidatePanelType, styleType: IMKStyleType)](/documentation/inputmethodkit/imkcandidates/init(server:paneltype:styletype:))

### Instance Methods

- [func attachChild(IMKCandidates!, toCandidate: Int, type: IMKStyleType)](/documentation/inputmethodkit/imkcandidates/attachchild(_:tocandidate:type:))
- [func candidateFrame() -> NSRect](/documentation/inputmethodkit/imkcandidates/candidateframe())
- [func candidateIdentifier(atLineNumber: Int) -> Int](/documentation/inputmethodkit/imkcandidates/candidateidentifier(atlinenumber:))
- [func candidateStringIdentifier(Any!) -> Int](/documentation/inputmethodkit/imkcandidates/candidatestringidentifier(_:))
- [func clearSelection()](/documentation/inputmethodkit/imkcandidates/clearselection())
- [func detachChild(Int)](/documentation/inputmethodkit/imkcandidates/detachchild(_:))
- [func hideChild()](/documentation/inputmethodkit/imkcandidates/hidechild())
- [func lineNumberForCandidate(withIdentifier: Int) -> Int](/documentation/inputmethodkit/imkcandidates/linenumberforcandidate(withidentifier:))
- [func selectCandidate(Int)](/documentation/inputmethodkit/imkcandidates/selectcandidate(_:))
- [func selectCandidate(withIdentifier: Int) -> Bool](/documentation/inputmethodkit/imkcandidates/selectcandidate(withidentifier:))
- [func selectedCandidate() -> Int](/documentation/inputmethodkit/imkcandidates/selectedcandidate())
- [func selectedCandidateString() -> NSAttributedString!](/documentation/inputmethodkit/imkcandidates/selectedcandidatestring())
- [func setCandidateData([Any]!)](/documentation/inputmethodkit/imkcandidates/setcandidatedata(_:))
- [func setCandidateFrameTopLeft(NSPoint)](/documentation/inputmethodkit/imkcandidates/setcandidateframetopleft(_:))
- [func show()](/documentation/inputmethodkit/imkcandidates/show())
- [func showChild()](/documentation/inputmethodkit/imkcandidates/showchild())
- [func showSublist([Any]!, subListDelegate: Any!)](/documentation/inputmethodkit/imkcandidates/showsublist(_:sublistdelegate:))
- [IMKInputController](/documentation/inputmethodkit/imkinputcontroller)

### Initializing an Input Controller

- [init!(server: IMKServer!, delegate: Any!, client: Any!)](/documentation/inputmethodkit/imkinputcontroller/init(server:delegate:client:))

### Working with Ranges

- [func compositionAttributes(at: NSRange) -> NSMutableDictionary!](/documentation/inputmethodkit/imkinputcontroller/compositionattributes(at:))
- [func selectionRange() -> NSRange](/documentation/inputmethodkit/imkinputcontroller/selectionrange())
- [func replacementRange() -> NSRange](/documentation/inputmethodkit/imkinputcontroller/replacementrange())
- [func mark(forStyle: Int, at: NSRange) -> [AnyHashable : Any]!](/documentation/inputmethodkit/imkinputcontroller/mark(forstyle:at:))

### Managing the Delegate

- [func delegate() -> Any!](/documentation/inputmethodkit/imkinputcontroller/delegate())
- [func setDelegate(Any!)](/documentation/inputmethodkit/imkinputcontroller/setdelegate(_:))

### Getting the Client and Server Objects

- [func server() -> IMKServer!](/documentation/inputmethodkit/imkinputcontroller/server())
- [func client() -> (any IMKTextInput & NSObjectProtocol)!](/documentation/inputmethodkit/imkinputcontroller/client())

### Tracking Selections

- [func annotationSelected(NSAttributedString!, forCandidate: NSAttributedString!)](/documentation/inputmethodkit/imkinputcontroller/annotationselected(_:forcandidate:))
- [func candidateSelectionChanged(NSAttributedString!)](/documentation/inputmethodkit/imkinputcontroller/candidateselectionchanged(_:))
- [func candidateSelected(NSAttributedString!)](/documentation/inputmethodkit/imkinputcontroller/candidateselected(_:))

### Managing Composition

- [func updateComposition()](/documentation/inputmethodkit/imkinputcontroller/updatecomposition())
- [func cancelComposition()](/documentation/inputmethodkit/imkinputcontroller/cancelcomposition())

### Hiding the User Interface

- [func hidePalettes()](/documentation/inputmethodkit/imkinputcontroller/hidepalettes())

### Working with Custom Commands

- [func doCommand(by: Selector!, command: [AnyHashable : Any]!)](/documentation/inputmethodkit/imkinputcontroller/docommand(by:command:))
- [func menu() -> NSMenu!](/documentation/inputmethodkit/imkinputcontroller/menu())

### Instance Methods

- [func inputControllerWillClose()](/documentation/inputmethodkit/imkinputcontroller/inputcontrollerwillclose())
- [IMKServer](/documentation/inputmethodkit/imkserver)

### Initializing a Server Object

- [init!(name: String!, bundleIdentifier: String!)](/documentation/inputmethodkit/imkserver/init(name:bundleidentifier:))
- [init!(name: String!, controllerClass: AnyClass!, delegateClass: AnyClass!)](/documentation/inputmethodkit/imkserver/init(name:controllerclass:delegateclass:))

### Getting a Bundle for the Input Method

- [func bundle() -> Bundle!](/documentation/inputmethodkit/imkserver/bundle())

### Constants

- [let IMKModeDictionary: String](/documentation/inputmethodkit/imkmodedictionary)
- [let IMKControllerClass: String](/documentation/inputmethodkit/imkcontrollerclass)
- [let IMKDelegateClass: String](/documentation/inputmethodkit/imkdelegateclass)

### Instance Methods

- [func lastKeyEventWasDeadKey() -> Bool](/documentation/inputmethodkit/imkserver/lastkeyeventwasdeadkey())
- [func paletteWillTerminate() -> Bool](/documentation/inputmethodkit/imkserver/palettewillterminate())

## Protocols

- [IMKMouseHandling](/documentation/inputmethodkit/imkmousehandling)

### Handling Mouse Events

- [func mouseDown(onCharacterIndex: Int, coordinate: NSPoint, withModifier: Int, continueTracking: UnsafeMutablePointer<ObjCBool>!, client: Any!) -> Bool](/documentation/inputmethodkit/imkmousehandling/mousedown(oncharacterindex:coordinate:withmodifier:continuetracking:client:))
- [func mouseUp(onCharacterIndex: Int, coordinate: NSPoint, withModifier: Int, client: Any!) -> Bool](/documentation/inputmethodkit/imkmousehandling/mouseup(oncharacterindex:coordinate:withmodifier:client:))
- [func mouseMoved(onCharacterIndex: Int, coordinate: NSPoint, withModifier: Int, client: Any!) -> Bool](/documentation/inputmethodkit/imkmousehandling/mousemoved(oncharacterindex:coordinate:withmodifier:client:))
- [IMKServerInput](/documentation/inputmethodkit/imkserverinput)

### Supporting Key Binding

- [func inputText(String!, client: Any!) -> Bool](/documentation/objectivec/nsobject/1385446-inputtext)
- [func didCommand(by: Selector!, client: Any!) -> Bool](/documentation/objectivec/nsobject/1385394-didcommand)

### Unpacking Text Data

- [func inputText(String!, key: Int, modifiers: Int, client: Any!) -> Bool](/documentation/objectivec/nsobject/1385436-inputtext)

### Receiving Events Directly from the Text Services Manager

- [func handle(NSEvent!, client: Any!) -> Bool](/documentation/objectivec/nsobject/1385363-handle)

### Committing a Composition

- [func commitComposition(Any!)](/documentation/objectivec/nsobject/1385539-commitcomposition)

### Getting Input Strings and Candidates

- [func composedString(Any!) -> Any!](/documentation/objectivec/nsobject/1385416-composedstring)
- [func originalString(Any!) -> NSAttributedString!](/documentation/objectivec/nsobject/1385400-originalstring)
- [func candidates(Any!) -> [Any]!](/documentation/objectivec/nsobject/1385360-candidates)

### Constants

- [Info Dictionary Keys](/documentation/inputmethodkit/info-dictionary-keys)

#### Constants

- [let kIMKCommandMenuItemName: String](/documentation/inputmethodkit/kimkcommandmenuitemname)
- [let kIMKCommandClientName: String](/documentation/inputmethodkit/kimkcommandclientname)
- [IMKStateSetting](/documentation/inputmethodkit/imkstatesetting)

### Activating and Deactivating the Server

- [func activateServer(Any!)](/documentation/inputmethodkit/imkstatesetting/activateserver(_:))
- [func deactivateServer(Any!)](/documentation/inputmethodkit/imkstatesetting/deactivateserver(_:))

### Showing a Preferences Window

- [func showPreferences(Any!)](/documentation/inputmethodkit/imkstatesetting/showpreferences(_:))

### Getting the Supported Events

- [func recognizedEvents(Any!) -> Int](/documentation/inputmethodkit/imkstatesetting/recognizedevents(_:))

### Getting the Mode Dictionary

- [func modes(Any!) -> [AnyHashable : Any]!](/documentation/inputmethodkit/imkstatesetting/modes(_:))

### Getting and Setting Values

- [func value(forTag: Int, client: Any!) -> Any!](/documentation/inputmethodkit/imkstatesetting/value(fortag:client:))
- [func setValue(Any!, forTag: Int, client: Any!)](/documentation/inputmethodkit/imkstatesetting/setvalue(_:fortag:client:))

## Reference

- [InputMethodKit Enumerations](/documentation/inputmethodkit/inputmethodkit-enumerations)

### Enumerations

- [Anonymous](/documentation/inputmethodkit/inputmethodkit-enumerations-1448298-anonymous)

#### Constants

- [var kIMKLocateCandidatesAboveHint: Int](/documentation/inputmethodkit/kimklocatecandidatesabovehint)
- [var kIMKLocateCandidatesBelowHint: Int](/documentation/inputmethodkit/kimklocatecandidatesbelowhint)
- [var kIMKLocateCandidatesLeftHint: Int](/documentation/inputmethodkit/kimklocatecandidateslefthint)
- [var kIMKLocateCandidatesRightHint: Int](/documentation/inputmethodkit/kimklocatecandidatesrighthint)
- [Anonymous](/documentation/inputmethodkit/inputmethodkit-enumerations-1448307-anonymous)

#### Constants

- [var kIMKScrollingGridCandidatePanel: Int](/documentation/inputmethodkit/kimkscrollinggridcandidatepanel)
- [var kIMKSingleColumnScrollingCandidatePanel: Int](/documentation/inputmethodkit/kimksinglecolumnscrollingcandidatepanel)
- [var kIMKSingleRowSteppingCandidatePanel: Int](/documentation/inputmethodkit/kimksinglerowsteppingcandidatepanel)
- [Anonymous](/documentation/inputmethodkit/inputmethodkit-enumerations-1448301-anonymous)

#### Constants

- [var kIMKAnnotation: Int](/documentation/inputmethodkit/kimkannotation)
- [var kIMKMain: Int](/documentation/inputmethodkit/kimkmain)
- [var kIMKSubList: Int](/documentation/inputmethodkit/kimksublist)
- [InputMethodKit Constants](/documentation/inputmethodkit/inputmethodkit-constants)

### Constants

- [let IMKCandidatesOpacityAttributeName: String](/documentation/inputmethodkit/imkcandidatesopacityattributename)
- [let IMKCandidatesSendServerKeyEventFirst: String](/documentation/inputmethodkit/imkcandidatessendserverkeyeventfirst)
- [let IMKControllerClass: String](/documentation/inputmethodkit/imkcontrollerclass)
- [let IMKDelegateClass: String](/documentation/inputmethodkit/imkdelegateclass)
- [let IMKModeDictionary: String](/documentation/inputmethodkit/imkmodedictionary)
- [InputMethodKit Data Types](/documentation/inputmethodkit/inputmethodkit-data_types)

### Data Types

- [IMKCandidatePanelType](/documentation/inputmethodkit/imkcandidatepaneltype)

#### Constants

- [var kIMKSingleColumnScrollingCandidatePanel: Int](/documentation/inputmethodkit/kimksinglecolumnscrollingcandidatepanel)
- [var kIMKScrollingGridCandidatePanel: Int](/documentation/inputmethodkit/kimkscrollinggridcandidatepanel)
- [var kIMKSingleRowSteppingCandidatePanel: Int](/documentation/inputmethodkit/kimksinglerowsteppingcandidatepanel)
- [IMKCandidatesLocationHint](/documentation/inputmethodkit/imkcandidateslocationhint)

#### Constants

- [var kIMKLocateCandidatesAboveHint: Int](/documentation/inputmethodkit/kimklocatecandidatesabovehint)
- [var kIMKLocateCandidatesBelowHint: Int](/documentation/inputmethodkit/kimklocatecandidatesbelowhint)
- [var kIMKLocateCandidatesLeftHint: Int](/documentation/inputmethodkit/kimklocatecandidateslefthint)
- [var kIMKLocateCandidatesRightHint: Int](/documentation/inputmethodkit/kimklocatecandidatesrighthint)
- [IMKStyleType](/documentation/inputmethodkit/imkstyletype)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
