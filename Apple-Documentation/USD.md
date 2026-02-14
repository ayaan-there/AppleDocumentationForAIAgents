# USD Documentation

Source: https://sosumi.ai/documentation/usd

---
title: USD
source: https://developer.apple.com/documentation/usd
timestamp: 2026-02-13T19:03:31.294Z
---

## Essentials

- [OpenUSD schemas for AR](/documentation/usd/usd-schemas-for-ar)

### Animation

- [autoPlay](/documentation/usd/autoplay)
- [playbackMode](/documentation/usd/playbackmode)

### Anchoring

- [Placing a prim in the real world](/documentation/usd/placing-a-prim-in-the-real-world)
- [Preliminary_AnchoringAPI](/documentation/usd/preliminary-anchoringapi)

#### Properties

- [preliminary:anchoring:type](/documentation/usd/preliminary-anchoring-type)
- [preliminary:planeAnchoring:alignment](/documentation/usd/preliminary-planeanchoring-alignment)
- [preliminary:imageAnchoring:referenceImage](/documentation/usd/preliminary-imageanchoring-referenceimage)
- [Preliminary_ReferenceImage](/documentation/usd/preliminary-referenceimage)

#### Properties

- [image](/documentation/usd/image)
- [physicalWidth](/documentation/usd/physicalwidth)

### Behaviors

- [Actions and triggers](/documentation/usd/actions-and-triggers)

#### Essentials

- [Preliminary_Behavior](/documentation/usd/preliminary-behavior)

##### Properties

- [triggers](/documentation/usd/triggers)
- [actions](/documentation/usd/actions)
- [exclusive](/documentation/usd/exclusive)

#### Triggers

- [Preliminary_Trigger](/documentation/usd/preliminary-trigger)

##### Properties

- [info:id](/documentation/usd/info-id)
- [CollideTrigger](/documentation/usd/collidetrigger)

##### Properties

- [info:id](/documentation/usd/info-id)
- [affectedObjects](/documentation/usd/affectedobjects)
- [colliders](/documentation/usd/colliders)
- [ProximityToCameraTrigger](/documentation/usd/proximitytocameratrigger)

##### Properties

- [info:id](/documentation/usd/info-id)
- [affectedObjects](/documentation/usd/affectedobjects)
- [distance](/documentation/usd/distance)
- [SceneTransitionTrigger](/documentation/usd/scenetransitiontrigger)

##### Properties

- [info:id](/documentation/usd/info-id)
- [type](/documentation/usd/type)
- [TapGestureTrigger](/documentation/usd/tapgesturetrigger)

##### Properties

- [info:id](/documentation/usd/info-id)
- [affectedObjects](/documentation/usd/affectedobjects)
- [NotificationTrigger](/documentation/usd/notificationtrigger)

##### Properties

- [info:id](/documentation/usd/info-id)
- [identifier](/documentation/usd/identifier)

#### Actions

- [Preliminary_Action](/documentation/usd/preliminary-action)

##### Properties

- [info:id](/documentation/usd/info-id)
- [multiplePerformOperation](/documentation/usd/multipleperformoperation)
- [AudioAction](/documentation/usd/audioaction)

##### Properties

- [info:id](/documentation/usd/info-id)
- [affectedObjects](/documentation/usd/affectedobjects)
- [audio](/documentation/usd/audio)
- [type](/documentation/usd/type)
- [gain](/documentation/usd/gain)
- [auralMode](/documentation/usd/auralmode)
- [ChangeSceneAction](/documentation/usd/changesceneaction)

##### Properties

- [info:id](/documentation/usd/info-id)
- [scene](/documentation/usd/scene)
- [EmphasizeAction](/documentation/usd/emphasizeaction)

##### Properties

- [info:id](/documentation/usd/info-id)
- [affectedObjects](/documentation/usd/affectedobjects)
- [duration](/documentation/usd/duration)
- [style](/documentation/usd/style)
- [motionType](/documentation/usd/motiontype)
- [GroupAction](/documentation/usd/groupaction)

##### Properties

- [info:id](/documentation/usd/info-id)
- [type](/documentation/usd/type)
- [loops](/documentation/usd/loops)
- [performCount](/documentation/usd/performcount)
- [actions](/documentation/usd/actions)
- [ImpulseAction](/documentation/usd/impulseaction)

##### Properties

- [info:id](/documentation/usd/info-id)
- [affectedObjects](/documentation/usd/affectedobjects)
- [velocity](/documentation/usd/velocity)
- [LookAtCameraAction](/documentation/usd/lookatcameraaction)

##### Properties

- [info:id](/documentation/usd/info-id)
- [affectedObjects](/documentation/usd/affectedobjects)
- [duration](/documentation/usd/duration)
- [front](/documentation/usd/front)
- [upVector](/documentation/usd/upvector)
- [OrbitAction](/documentation/usd/orbitaction)

##### Properties

- [info:id](/documentation/usd/info-id)
- [affectedObjects](/documentation/usd/affectedobjects)
- [center](/documentation/usd/center)
- [duration](/documentation/usd/duration)
- [revolutions](/documentation/usd/revolutions)
- [axis](/documentation/usd/axis)
- [alignToPath](/documentation/usd/aligntopath)
- [SpinAction](/documentation/usd/spinaction)

##### Properties

- [info:id](/documentation/usd/info-id)
- [affectedObjects](/documentation/usd/affectedobjects)
- [duration](/documentation/usd/duration)
- [revolutions](/documentation/usd/revolutions)
- [axis](/documentation/usd/axis)
- [StartAnimationAction](/documentation/usd/startanimationaction)

##### Properties

- [info:id](/documentation/usd/info-id)
- [affectedObjects](/documentation/usd/affectedobjects)
- [start](/documentation/usd/start)
- [duration](/documentation/usd/duration)
- [reversed](/documentation/usd/reversed)
- [animationSpeed](/documentation/usd/animationspeed)
- [reverses](/documentation/usd/reverses)
- [TransformAction](/documentation/usd/transformaction)

##### Properties

- [info:id](/documentation/usd/info-id)
- [affectedObjects](/documentation/usd/affectedobjects)
- [xformTarget](/documentation/usd/xformtarget)
- [duration](/documentation/usd/duration)
- [type](/documentation/usd/type)
- [easeType](/documentation/usd/easetype)
- [TransformAnimationAction](/documentation/usd/transformanimationaction)

##### Properties

- [info:id](/documentation/usd/info-id)
- [affectedObjects](/documentation/usd/affectedobjects)
- [animation](/documentation/usd/animation)
- [VisibilityAction](/documentation/usd/visibilityaction)

##### Properties

- [info:id](/documentation/usd/info-id)
- [affectedObjects](/documentation/usd/affectedobjects)
- [type](/documentation/usd/type)
- [style](/documentation/usd/style)
- [motionType](/documentation/usd/motiontype)
- [easeType](/documentation/usd/easetype)
- [moveDistance](/documentation/usd/movedistance)
- [WaitAction](/documentation/usd/waitaction)

##### Properties

- [info:id](/documentation/usd/info-id)
- [duration](/documentation/usd/duration)
- [NotificationAction](/documentation/usd/notificationaction)

##### Properties

- [info:id](/documentation/usd/info-id)
- [affectedObjects](/documentation/usd/affectedobjects)
- [identifier](/documentation/usd/identifier)

### Text

- [Preliminary_Text](/documentation/usd/preliminary-text)

#### Properties

- [content](/documentation/usd/content)
- [font](/documentation/usd/font)
- [pointSize](/documentation/usd/pointsize)
- [width](/documentation/usd/width)
- [height](/documentation/usd/height)
- [depth](/documentation/usd/depth)
- [wrapMode](/documentation/usd/wrapmode)
- [horizontalAlignment](/documentation/usd/horizontalalignment)
- [verticalAlignment](/documentation/usd/verticalalignment)

### Scenes and lighting

- [Specifying a lighting environment in AR Quick Look](/documentation/arkit/specifying-a-lighting-environment-in-ar-quick-look)
- [preferredIblVersion](/documentation/usd/preferrediblversion)
- [sceneLibrary](/documentation/usd/scenelibrary)

### Digital content creation

- [Schema definitions for third-party DCCs](/documentation/usd/schema-definitions-for-third-party-dccs)
- [Schema definitions for third-party DCCs](/documentation/usd/schema-definitions-for-third-party-dccs)
- [Creating USD files for Apple devices](/documentation/usd/creating-usd-files-for-apple-devices)

### Validating USD feature support

- [Validating feature support for USD files](/documentation/usd/validating-usd-files)
- [Validating feature support for USD files](/documentation/usd/validating-usd-files)
- [Placing a prim in the real world](/documentation/usd/placing-a-prim-in-the-real-world)
- [Previewing a Model with AR Quick Look](/documentation/arkit/previewing-a-model-with-ar-quick-look)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
