# GameSave Documentation

Source: https://sosumi.ai/documentation/gamesave

---
title: GameSave
source: https://developer.apple.com/documentation/gamesave
timestamp: 2026-02-13T18:57:36.410Z
---

## Synced directory

- [GameSaveSyncedDirectory](/documentation/gamesave/gamesavesynceddirectory)

### Accessing a directory

- [class func openDirectory(containerIdentifier: String?) -> GameSaveSyncedDirectory](/documentation/gamesave/gamesavesynceddirectory/opendirectory(containeridentifier:))
- [GameSaveSyncedDirectory.State](/documentation/gamesave/gamesavesynceddirectory/state-swift.enum)

#### Directory states

- [case closed](/documentation/gamesave/gamesavesynceddirectory/state-swift.enum/closed)
- [case conflicted(versions: [GameSaveSyncedDirectory.Version])](/documentation/gamesave/gamesavesynceddirectory/state-swift.enum/conflicted(versions:))
- [case error(any Error)](/documentation/gamesave/gamesavesynceddirectory/state-swift.enum/error(_:))
- [case local(URL)](/documentation/gamesave/gamesavesynceddirectory/state-swift.enum/local(_:))
- [case offline(URL)](/documentation/gamesave/gamesavesynceddirectory/state-swift.enum/offline(_:))
- [case ready(URL)](/documentation/gamesave/gamesavesynceddirectory/state-swift.enum/ready(_:))
- [case syncing](/documentation/gamesave/gamesavesynceddirectory/state-swift.enum/syncing)
- [var state: GameSaveSyncedDirectory.State](/documentation/gamesave/gamesavesynceddirectory/state-swift.property)

### Syncing a directory

- [func finishSyncing() async](/documentation/gamesave/gamesavesynceddirectory/finishsyncing())
- [func finishSyncing(statusDisplay: NSWindow) async](/documentation/gamesave/gamesavesynceddirectory/finishsyncing(statusdisplay:)-309nq)
- [func finishSyncing(statusDisplay: UIWindow) async](/documentation/gamesave/gamesavesynceddirectory/finishsyncing(statusdisplay:)-500el)

### Resolving conflicts

- [GameSaveSyncedDirectory.Version](/documentation/gamesave/gamesavesynceddirectory/version)

#### Accessing saved game state

- [var url: URL](/documentation/gamesave/gamesavesynceddirectory/version/url)
- [var isLocal: Bool](/documentation/gamesave/gamesavesynceddirectory/version/islocal)

#### Comparing versions

- [var localizedNameOfSavingComputer: String](/documentation/gamesave/gamesavesynceddirectory/version/localizednameofsavingcomputer)
- [var modifiedDate: Date](/documentation/gamesave/gamesavesynceddirectory/version/modifieddate)
- [func resolveConflicts(with: GameSaveSyncedDirectory.Version)](/documentation/gamesave/gamesavesynceddirectory/resolveconflicts(with:))

### Finishing with a directory

- [func triggerPendingUpload() async -> Bool](/documentation/gamesave/gamesavesynceddirectory/triggerpendingupload())
- [func close()](/documentation/gamesave/gamesavesynceddirectory/close())

## Error domain

- [let GameSaveErrorDomain: String](/documentation/gamesave/gamesaveerrordomain)

## Synced directory (Objective-C)

- [GSSyncedDirectory](/documentation/gamesave/gssynceddirectory)

### Accessing a directory

- [class func open(forContainerIdentifier: String?) -> GSSyncedDirectory](/documentation/gamesave/gssynceddirectory/open(forcontaineridentifier:))
- [var directoryState: GSSyncedDirectoryState](/documentation/gamesave/gssynceddirectory/directorystate)
- [GSSyncedDirectoryState](/documentation/gamesave/gssynceddirectorystate)

#### Directory state information

- [GSSyncState](/documentation/gamesave/gssyncstate)

##### Directory states

- [case closed](/documentation/gamesave/gssyncstate/closed)
- [case conflicted](/documentation/gamesave/gssyncstate/conflicted)
- [case error](/documentation/gamesave/gssyncstate/error)
- [case local](/documentation/gamesave/gssyncstate/local)
- [case offline](/documentation/gamesave/gssyncstate/offline)
- [case ready](/documentation/gamesave/gssyncstate/ready)
- [case syncing](/documentation/gamesave/gssyncstate/syncing)

##### Creating a directory state

- [init?(rawValue: Int)](/documentation/gamesave/gssyncstate/init(rawvalue:))
- [var state: GSSyncState](/documentation/gamesave/gssynceddirectorystate/state)
- [var conflictedVersions: [GSSyncedDirectoryVersion]?](/documentation/gamesave/gssynceddirectorystate/conflictedversions)
- [var error: (any Error)?](/documentation/gamesave/gssynceddirectorystate/error)
- [var url: URL?](/documentation/gamesave/gssynceddirectorystate/url)

### Syncing a directory

- [func finishSyncing(UIWindow, completionHandler: () -> Void)](/documentation/gamesave/gssynceddirectory/finishsyncing(_:completionhandler:))
- [func finishSyncing(completionHandler: () -> Void)](/documentation/gamesave/gssynceddirectory/finishsyncing(completionhandler:))

### Resolving conflicts

- [GSSyncedDirectoryVersion](/documentation/gamesave/gssynceddirectoryversion)

#### Instance Properties

- [var description: String](/documentation/gamesave/gssynceddirectoryversion/description)
- [var isLocal: Bool](/documentation/gamesave/gssynceddirectoryversion/islocal)
- [var localizedNameOfSavingComputer: String](/documentation/gamesave/gssynceddirectoryversion/localizednameofsavingcomputer)
- [var modifiedDate: Date](/documentation/gamesave/gssynceddirectoryversion/modifieddate)
- [var url: URL](/documentation/gamesave/gssynceddirectoryversion/url)
- [func resolveConflicts(with: GSSyncedDirectoryVersion)](/documentation/gamesave/gssynceddirectory/resolveconflicts(with:))

### Finishing with a directory

- [func triggerPendingUpload(completionHandler: (Bool) -> Void)](/documentation/gamesave/gssynceddirectory/triggerpendingupload(completionhandler:))
- [func close()](/documentation/gamesave/gssynceddirectory/close())

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
