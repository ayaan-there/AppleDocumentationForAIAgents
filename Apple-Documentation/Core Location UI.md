# Core Location UI Documentation

Source: https://sosumi.ai/documentation/corelocationui

---
title: CoreLocationUI
source: https://developer.apple.com/documentation/corelocationui
timestamp: 2026-02-13T18:55:24.713Z
---

## Location authorization

- [Sharing Your Location to Find a Park](/documentation/corelocationui/sharing-your-location-to-find-a-park)
- [LocationButton](/documentation/corelocationui/locationbutton)

### Creating a location button

- [init(LocationButton.Title?, action: () -> Void)](/documentation/corelocationui/locationbutton/init(_:action:))
- [LocationButton.Title](/documentation/corelocationui/locationbutton/title)

#### Customizing title styles

- [static let currentLocation: LocationButton.Title](/documentation/corelocationui/locationbutton/title/currentlocation)
- [static let sendCurrentLocation: LocationButton.Title](/documentation/corelocationui/locationbutton/title/sendcurrentlocation)
- [static let sendMyCurrentLocation: LocationButton.Title](/documentation/corelocationui/locationbutton/title/sendmycurrentlocation)
- [static let shareCurrentLocation: LocationButton.Title](/documentation/corelocationui/locationbutton/title/sharecurrentlocation)
- [static let shareMyCurrentLocation: LocationButton.Title](/documentation/corelocationui/locationbutton/title/sharemycurrentlocation)
- [CLLocationButton](/documentation/corelocationui/cllocationbutton)

### Customizing the icon style

- [var icon: CLLocationButtonIcon](/documentation/corelocationui/cllocationbutton/icon)

### Customizing the label text

- [var label: CLLocationButtonLabel](/documentation/corelocationui/cllocationbutton/label)

### Customizing the button appearance

- [var cornerRadius: CGFloat](/documentation/corelocationui/cllocationbutton/cornerradius)
- [var fontSize: CGFloat](/documentation/corelocationui/cllocationbutton/fontsize)

## Button customization

- [CLLocationButtonIcon](/documentation/corelocationui/cllocationbuttonicon)

### Customizing icon styles

- [case none](/documentation/corelocationui/cllocationbuttonicon/none)
- [case arrowFilled](/documentation/corelocationui/cllocationbuttonicon/arrowfilled)
- [case arrowOutline](/documentation/corelocationui/cllocationbuttonicon/arrowoutline)

### Initializers

- [init?(rawValue: Int)](/documentation/corelocationui/cllocationbuttonicon/init(rawvalue:))
- [CLLocationButtonLabel](/documentation/corelocationui/cllocationbuttonlabel)

### Customizing label styles

- [case none](/documentation/corelocationui/cllocationbuttonlabel/none)
- [case currentLocation](/documentation/corelocationui/cllocationbuttonlabel/currentlocation)
- [case sendCurrentLocation](/documentation/corelocationui/cllocationbuttonlabel/sendcurrentlocation)
- [case sendMyCurrentLocation](/documentation/corelocationui/cllocationbuttonlabel/sendmycurrentlocation)
- [case shareCurrentLocation](/documentation/corelocationui/cllocationbuttonlabel/sharecurrentlocation)
- [case shareMyCurrentLocation](/documentation/corelocationui/cllocationbuttonlabel/sharemycurrentlocation)

### Initializers

- [init?(rawValue: Int)](/documentation/corelocationui/cllocationbuttonlabel/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
