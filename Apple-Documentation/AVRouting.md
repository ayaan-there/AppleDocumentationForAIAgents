# AVRouting Documentation

Source: https://sosumi.ai/documentation/avrouting

---
title: AVRouting
source: https://developer.apple.com/documentation/avrouting
timestamp: 2026-02-13T18:54:18.184Z
---

## Media routing

- [AVCustomRoutingController](/documentation/avrouting/avcustomroutingcontroller)

### Managing authorization

- [var authorizedRoutes: [AVCustomDeviceRoute]](/documentation/avrouting/avcustomroutingcontroller/authorizedroutes)
- [class let authorizedRoutesDidChange: NSNotification.Name](/documentation/avrouting/avcustomroutingcontroller/authorizedroutesdidchange)
- [func invalidateAuthorization(for: AVCustomDeviceRoute)](/documentation/avrouting/avcustomroutingcontroller/invalidateauthorization(for:))

### Configuring route addresses

- [var knownRouteIPs: [AVCustomRoutingPartialIP]](/documentation/avrouting/avcustomroutingcontroller/knownrouteips)
- [AVCustomRoutingPartialIP](/documentation/avrouting/avcustomroutingpartialip)

#### Creating an IP fragment

- [init(address: Data, mask: Data)](/documentation/avrouting/avcustomroutingpartialip/init(address:mask:))

#### Inspecting the IP fragment

- [var address: Data](/documentation/avrouting/avcustomroutingpartialip/address)
- [var mask: Data](/documentation/avrouting/avcustomroutingpartialip/mask)

### Activating a route

- [func isRouteActive(AVCustomDeviceRoute) -> Bool](/documentation/avrouting/avcustomroutingcontroller/isrouteactive(_:))
- [func setActive(Bool, for: AVCustomDeviceRoute)](/documentation/avrouting/avcustomroutingcontroller/setactive(_:for:))

### Accessing the delegate

- [var delegate: (any AVCustomRoutingControllerDelegate)?](/documentation/avrouting/avcustomroutingcontroller/delegate)

### Customizing the user interface

- [var customActionItems: [AVCustomRoutingActionItem]](/documentation/avrouting/avcustomroutingcontroller/customactionitems)
- [AVCustomRoutingControllerDelegate](/documentation/avrouting/avcustomroutingcontrollerdelegate)

### Handling controller events

- [func customRoutingController(AVCustomRoutingController, handle: AVCustomRoutingEvent, completionHandler: (Bool) -> Void)](/documentation/avrouting/avcustomroutingcontrollerdelegate/customroutingcontroller(_:handle:completionhandler:))
- [func customRoutingController(AVCustomRoutingController, eventDidTimeOut: AVCustomRoutingEvent)](/documentation/avrouting/avcustomroutingcontrollerdelegate/customroutingcontroller(_:eventdidtimeout:))
- [func customRoutingController(AVCustomRoutingController, didSelect: AVCustomRoutingActionItem)](/documentation/avrouting/avcustomroutingcontrollerdelegate/customroutingcontroller(_:didselect:))
- [AVCustomRoutingEvent](/documentation/avrouting/avcustomroutingevent)

### Inspecting an event

- [var route: AVCustomDeviceRoute](/documentation/avrouting/avcustomroutingevent/route)
- [AVCustomDeviceRoute](/documentation/avrouting/avcustomdeviceroute)

#### Identifying routes

- [var bluetoothIdentifier: UUID?](/documentation/avrouting/avcustomdeviceroute/bluetoothidentifier)
- [var networkEndpoint: nw_endpoint_t?](/documentation/avrouting/avcustomdeviceroute/networkendpoint)
- [var reason: AVCustomRoutingEventReason](/documentation/avrouting/avcustomroutingevent/reason)
- [AVCustomRoutingEventReason](/documentation/avrouting/avcustomroutingeventreason)

#### Reasons

- [case activate](/documentation/avrouting/avcustomroutingeventreason/activate)
- [case deactivate](/documentation/avrouting/avcustomroutingeventreason/deactivate)
- [case reactivate](/documentation/avrouting/avcustomroutingeventreason/reactivate)

#### Initializers

- [init?(rawValue: Int)](/documentation/avrouting/avcustomroutingeventreason/init(rawvalue:))
- [AVCustomRoutingActionItem](/documentation/avrouting/avcustomroutingactionitem)

### Configuring an item

- [var type: UTType](/documentation/avrouting/avcustomroutingactionitem/type)
- [var overrideTitle: String?](/documentation/avrouting/avcustomroutingactionitem/overridetitle)

## Playback arbitration

- [AVRoutingPlaybackArbiter](/documentation/avrouting/avroutingplaybackarbiter)

### Instance Properties

- [var preferredParticipantForExternalPlayback: (any AVRoutingPlaybackParticipant)?](/documentation/avrouting/avroutingplaybackarbiter/preferredparticipantforexternalplayback)
- [var preferredParticipantForNonMixableAudioRoutes: (any AVRoutingPlaybackParticipant)?](/documentation/avrouting/avroutingplaybackarbiter/preferredparticipantfornonmixableaudioroutes)

### Type Methods

- [class func shared() -> AVRoutingPlaybackArbiter](/documentation/avrouting/avroutingplaybackarbiter/shared())
- [AVRoutingPlaybackParticipant](/documentation/avrouting/avroutingplaybackparticipant)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
