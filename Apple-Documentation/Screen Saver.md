# Screen Saver Documentation

Source: https://sosumi.ai/documentation/screensaver

---
title: Screen Saver
source: https://developer.apple.com/documentation/screensaver
timestamp: 2026-02-13T19:01:37.213Z
---

## Interface

- [ScreenSaverView](/documentation/screensaver/screensaverview)

### Creating a screen saver view

- [init?(frame: NSRect, isPreview: Bool)](/documentation/screensaver/screensaverview/init(frame:ispreview:))

### Getting the preferred window behavior

- [class func backingStoreType() -> NSWindow.BackingStoreType](/documentation/screensaver/screensaverview/backingstoretype())
- [class func performGammaFade() -> Bool](/documentation/screensaver/screensaverview/performgammafade())

### Setting and getting the animation time interval

- [var animationTimeInterval: TimeInterval](/documentation/screensaver/screensaverview/animationtimeinterval)

### Animating the screen saver

- [func startAnimation()](/documentation/screensaver/screensaverview/startanimation())
- [func animateOneFrame()](/documentation/screensaver/screensaverview/animateoneframe())
- [func stopAnimation()](/documentation/screensaver/screensaverview/stopanimation())
- [var isAnimating: Bool](/documentation/screensaver/screensaverview/isanimating)

### Drawing the view

- [func draw(NSRect)](/documentation/screensaver/screensaverview/draw(_:))
- [var isPreview: Bool](/documentation/screensaver/screensaverview/ispreview)

### Accessing the configuration sheet

- [var hasConfigureSheet: Bool](/documentation/screensaver/screensaverview/hasconfiguresheet)
- [var configureSheet: NSWindow?](/documentation/screensaver/screensaverview/configuresheet)
- [ScreenSaverDefaults](/documentation/screensaver/screensaverdefaults)

### Creating the screen saver defaults

- [convenience init?(forModuleWithName: String)](/documentation/screensaver/screensaverdefaults/init(formodulewithname:))

## Utilities

- [func SSRandomIntBetween(Int32, Int32) -> Int32](/documentation/screensaver/ssrandomintbetween(_:_:))
- [func SSRandomFloatBetween(CGFloat, CGFloat) -> CGFloat](/documentation/screensaver/ssrandomfloatbetween(_:_:))
- [func SSRandomPointForSizeWithinRect(NSSize, NSRect) -> NSPoint](/documentation/screensaver/ssrandompointforsizewithinrect(_:_:))
- [func SSCenteredRectInRect(NSRect, NSRect) -> NSRect](/documentation/screensaver/sscenteredrectinrect(_:_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
