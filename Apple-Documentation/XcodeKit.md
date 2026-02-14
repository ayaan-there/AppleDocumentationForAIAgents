# XcodeKit Documentation

Source: https://sosumi.ai/documentation/xcodekit

---
title: XcodeKit
source: https://developer.apple.com/documentation/xcodekit
timestamp: 2026-02-13T19:04:29.091Z
---

## Essentials

- [Creating a Source Editor Extension](/documentation/xcodekit/creating-a-source-editor-extension)
- [Testing Your Source Editor Extension](/documentation/xcodekit/testing-your-source-editor-extension)
- [XCSourceEditorExtension](/documentation/xcodekit/xcsourceeditorextension)

### Defining Extension Commands

- [var commandDefinitions: [[XCSourceEditorCommandDefinitionKey : Any]]](/documentation/xcodekit/xcsourceeditorextension/commanddefinitions)

### Handling Extension Launches

- [func extensionDidFinishLaunching()](/documentation/xcodekit/xcsourceeditorextension/extensiondidfinishlaunching())

## Editor Commands

- [XCSourceEditorCommand](/documentation/xcodekit/xcsourceeditorcommand)

### Defining Editor Commands

- [XCSourceEditorCommandDefinitionKey](/documentation/xcodekit/xcsourceeditorcommanddefinitionkey)

#### Populating a Command Definition Dictionary

- [static let classNameKey: XCSourceEditorCommandDefinitionKey](/documentation/xcodekit/xcsourceeditorcommanddefinitionkey/classnamekey)
- [static let identifierKey: XCSourceEditorCommandDefinitionKey](/documentation/xcodekit/xcsourceeditorcommanddefinitionkey/identifierkey)
- [static let nameKey: XCSourceEditorCommandDefinitionKey](/documentation/xcodekit/xcsourceeditorcommanddefinitionkey/namekey)

#### Creating a Key Using a Raw String

- [init(rawValue: String)](/documentation/xcodekit/xcsourceeditorcommanddefinitionkey/init(rawvalue:))

#### Type Properties

- [static let systemSymbolNameKey: XCSourceEditorCommandDefinitionKey](/documentation/xcodekit/xcsourceeditorcommanddefinitionkey/systemsymbolnamekey)

### Handling Editor Commands

- [func perform(with: XCSourceEditorCommandInvocation, completionHandler: ((any Error)?) -> Void)](/documentation/xcodekit/xcsourceeditorcommand/perform(with:completionhandler:))
- [XCSourceEditorCommandInvocation](/documentation/xcodekit/xcsourceeditorcommandinvocation)

### Responding to Commands

- [var buffer: XCSourceTextBuffer](/documentation/xcodekit/xcsourceeditorcommandinvocation/buffer)
- [var commandIdentifier: String](/documentation/xcodekit/xcsourceeditorcommandinvocation/commandidentifier)

### Responding to Cancelled Commands

- [var cancellationHandler: () -> Void](/documentation/xcodekit/xcsourceeditorcommandinvocation/cancellationhandler)

## Source Text

- [XCSourceTextBuffer](/documentation/xcodekit/xcsourcetextbuffer)

### Accessing Source Text

- [var completeBuffer: String](/documentation/xcodekit/xcsourcetextbuffer/completebuffer)
- [var contentUTI: String](/documentation/xcodekit/xcsourcetextbuffer/contentuti)

### Editing Source Text

- [var lines: NSMutableArray](/documentation/xcodekit/xcsourcetextbuffer/lines)
- [var selections: NSMutableArray](/documentation/xcodekit/xcsourcetextbuffer/selections)

### Configuring Source Editor Indentation

- [var indentationWidth: Int](/documentation/xcodekit/xcsourcetextbuffer/indentationwidth)
- [var usesTabsForIndentation: Bool](/documentation/xcodekit/xcsourcetextbuffer/usestabsforindentation)
- [var tabWidth: Int](/documentation/xcodekit/xcsourcetextbuffer/tabwidth)
- [XCSourceTextPosition](/documentation/xcodekit/xcsourcetextposition)

### Creating Source Text Positions

- [init()](/documentation/xcodekit/xcsourcetextposition/init())
- [init(line: Int, column: Int)](/documentation/xcodekit/xcsourcetextposition/init(line:column:))

### Inspecting Source Text Positions

- [var column: Int](/documentation/xcodekit/xcsourcetextposition/column)
- [var line: Int](/documentation/xcodekit/xcsourcetextposition/line)
- [XCSourceTextRange](/documentation/xcodekit/xcsourcetextrange)

### Creating Source Text Ranges

- [init(start: XCSourceTextPosition, end: XCSourceTextPosition)](/documentation/xcodekit/xcsourcetextrange/init(start:end:))

### Getting the Bounds of Source Text Ranges

- [var start: XCSourceTextPosition](/documentation/xcodekit/xcsourcetextrange/start)
- [var end: XCSourceTextPosition](/documentation/xcodekit/xcsourcetextrange/end)

## XcodeKit Constants

- [XcodeKit Version Constants](/documentation/xcodekit/xcodekit-version-constants)

### XcodeKit Versions

- [var XCXcodeKitVersionNumber: Double](/documentation/xcodekit/xcxcodekitversionnumber)
- [var XCXcodeKitVersionNumber_Xcode_8_0: Double](/documentation/xcodekit/xcxcodekitversionnumber_xcode_8_0)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
