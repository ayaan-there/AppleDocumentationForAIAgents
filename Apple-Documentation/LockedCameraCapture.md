# LockedCameraCapture Documentation

Source: https://sosumi.ai/documentation/lockedcameracapture

---
title: LockedCameraCapture
source: https://developer.apple.com/documentation/lockedcameracapture
timestamp: 2026-02-13T18:58:53.222Z
---

## Essentials

- [Creating a camera experience for the Lock Screen](/documentation/lockedcameracapture/creating-a-camera-experience-for-the-lock-screen)

## Capture and launch

- [LockedCameraCaptureUIScene](/documentation/lockedcameracapture/lockedcameracaptureuiscene)

### Initializers

- [init(content: (LockedCameraCaptureSession) -> Content)](/documentation/lockedcameracapture/lockedcameracaptureuiscene/init(content:))

### Instance Properties

- [var body: some AppExtensionScene](/documentation/lockedcameracapture/lockedcameracaptureuiscene/body)
- [let session: LockedCameraCaptureSession](/documentation/lockedcameracapture/lockedcameracaptureuiscene/session)
- [LockedCameraCaptureSession](/documentation/lockedcameracapture/lockedcameracapturesession)

### Instance Properties

- [var sessionContentURL: URL](/documentation/lockedcameracapture/lockedcameracapturesession/sessioncontenturl)

### Instance Methods

- [func invalidateSessionContent() async throws](/documentation/lockedcameracapture/lockedcameracapturesession/invalidatesessioncontent())
- [func openApplication(for: NSUserActivity) async throws](/documentation/lockedcameracapture/lockedcameracapturesession/openapplication(for:))

### Enumerations

- [LockedCameraCaptureSession.ApplicationLaunchError](/documentation/lockedcameracapture/lockedcameracapturesession/applicationlauncherror)

#### Enumeration Cases

- [case applicationNotFound](/documentation/lockedcameracapture/lockedcameracapturesession/applicationlauncherror/applicationnotfound)
- [case authenticationFailed](/documentation/lockedcameracapture/lockedcameracapturesession/applicationlauncherror/authenticationfailed)
- [case unknown](/documentation/lockedcameracapture/lockedcameracapturesession/applicationlauncherror/unknown)

#### Instance Properties

- [var errorCode: Int](/documentation/lockedcameracapture/lockedcameracapturesession/applicationlauncherror/errorcode)
- [var failureReason: String?](/documentation/lockedcameracapture/lockedcameracapturesession/applicationlauncherror/failurereason)

#### Type Properties

- [static var errorDomain: String](/documentation/lockedcameracapture/lockedcameracapturesession/applicationlauncherror/errordomain)

## App integration

- [LockedCameraCaptureManager](/documentation/lockedcameracapture/lockedcameracapturemanager)

### Instance Properties

- [var sessionContentURLs: [URL]](/documentation/lockedcameracapture/lockedcameracapturemanager/sessioncontenturls)
- [var sessionContentUpdates: some AsyncSequence<LockedCameraCaptureManager.SessionContentUpdate, Never>](/documentation/lockedcameracapture/lockedcameracapturemanager/sessioncontentupdates)

### Instance Methods

- [func beginDelayingAppearance()](/documentation/lockedcameracapture/lockedcameracapturemanager/begindelayingappearance())
- [func endDelayingAppearance()](/documentation/lockedcameracapture/lockedcameracapturemanager/enddelayingappearance())
- [func invalidateSessionContent(at: URL) async throws](/documentation/lockedcameracapture/lockedcameracapturemanager/invalidatesessioncontent(at:))

### Type Properties

- [static let shared: LockedCameraCaptureManager](/documentation/lockedcameracapture/lockedcameracapturemanager/shared)

### Enumerations

- [LockedCameraCaptureManager.SessionContentUpdate](/documentation/lockedcameracapture/lockedcameracapturemanager/sessioncontentupdate)

#### Enumeration Cases

- [case added(url: URL)](/documentation/lockedcameracapture/lockedcameracapturemanager/sessioncontentupdate/added(url:))
- [case initial(urls: [URL])](/documentation/lockedcameracapture/lockedcameracapturemanager/sessioncontentupdate/initial(urls:))
- [case removed(url: URL)](/documentation/lockedcameracapture/lockedcameracapturemanager/sessioncontentupdate/removed(url:))
- [let NSUserActivityTypeLockedCameraCapture: String](/documentation/lockedcameracapture/nsuseractivitytypelockedcameracapture)

## Extension

- [LockedCameraCaptureExtension](/documentation/lockedcameracapture/lockedcameracaptureextension)

### Associated Types

- [Body](/documentation/lockedcameracapture/lockedcameracaptureextension/body-swift.associatedtype)

### Instance Properties

- [var body: Self.Body](/documentation/lockedcameracapture/lockedcameracaptureextension/body-swift.property)
- [LockedCameraCaptureExtensionScene](/documentation/lockedcameracapture/lockedcameracaptureextensionscene)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
