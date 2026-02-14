# Symbols Documentation

Source: https://sosumi.ai/documentation/symbols

---
title: Symbols
source: https://developer.apple.com/documentation/symbols
timestamp: 2026-02-13T19:02:46.225Z
---

## Symbol effects

- [static var appear: AppearSymbolEffect](/documentation/symbols/symboleffect/appear)
- [static var bounce: BounceSymbolEffect](/documentation/symbols/symboleffect/bounce)
- [static var disappear: DisappearSymbolEffect](/documentation/symbols/symboleffect/disappear)
- [static var pulse: PulseSymbolEffect](/documentation/symbols/symboleffect/pulse)
- [static var scale: ScaleSymbolEffect](/documentation/symbols/symboleffect/scale)
- [static var variableColor: VariableColorSymbolEffect](/documentation/symbols/symboleffect/variablecolor)

## Symbol content transitions

- [static var replace: ReplaceSymbolEffect](/documentation/symbols/symboleffect/replace)
- [static var automatic: AutomaticSymbolEffect](/documentation/symbols/symboleffect/automatic)

## Symbol effect types

- [NSSymbolAppearEffect](/documentation/symbols/appearsymboleffect)

### Accessing symbol effects


### Determining effect scope

- [NSSymbolAutomaticContentTransition](/documentation/symbols/automaticsymboleffect)

### Accessing symbol effects

- [NSSymbolBounceEffect](/documentation/symbols/bouncesymboleffect)

### Accessing symbol effects


### Determining effect scope

- [NSSymbolDisappearEffect](/documentation/symbols/disappearsymboleffect)

### Accessing symbol effects


### Determining effect scope

- [PulseSymbolEffect](/documentation/symbols/pulsesymboleffect)

### Determining effect scope

- [var byLayer: PulseSymbolEffect](/documentation/symbols/pulsesymboleffect/bylayer)
- [var wholeSymbol: PulseSymbolEffect](/documentation/symbols/pulsesymboleffect/wholesymbol)

### Accessing the configuration

- [var configuration: SymbolEffectConfiguration](/documentation/symbols/pulsesymboleffect/configuration)
- [ReplaceSymbolEffect](/documentation/symbols/replacesymboleffect)

### Accessing symbol effects

- [var downUp: ReplaceSymbolEffect](/documentation/symbols/replacesymboleffect/downup-swift.property)
- [var offUp: ReplaceSymbolEffect](/documentation/symbols/replacesymboleffect/offup-swift.property)
- [var upUp: ReplaceSymbolEffect](/documentation/symbols/replacesymboleffect/upup-swift.property)

### Determining effect scope

- [var byLayer: ReplaceSymbolEffect](/documentation/symbols/replacesymboleffect/bylayer)
- [var wholeSymbol: ReplaceSymbolEffect](/documentation/symbols/replacesymboleffect/wholesymbol)

### Accessing the configuration

- [var configuration: SymbolEffectConfiguration](/documentation/symbols/replacesymboleffect/configuration)

### Structures

- [ReplaceSymbolEffect.MagicReplace](/documentation/symbols/replacesymboleffect/magicreplace)

#### Instance Properties

- [var configuration: SymbolEffectConfiguration](/documentation/symbols/replacesymboleffect/magicreplace/configuration)

### Instance Methods

- [func magic(fallback: ReplaceSymbolEffect) -> ReplaceSymbolEffect.MagicReplace](/documentation/symbols/replacesymboleffect/magic(fallback:))

### Type Properties

- [static var downUp: ReplaceSymbolEffect](/documentation/symbols/replacesymboleffect/downup-swift.type.property)
- [static var offUp: ReplaceSymbolEffect](/documentation/symbols/replacesymboleffect/offup-swift.type.property)
- [static var upUp: ReplaceSymbolEffect](/documentation/symbols/replacesymboleffect/upup-swift.type.property)
- [ScaleSymbolEffect](/documentation/symbols/scalesymboleffect)

### Accessing symbol effects

- [var down: ScaleSymbolEffect](/documentation/symbols/scalesymboleffect/down)
- [var up: ScaleSymbolEffect](/documentation/symbols/scalesymboleffect/up)

### Determining effect scope

- [var byLayer: ScaleSymbolEffect](/documentation/symbols/scalesymboleffect/bylayer)
- [var wholeSymbol: ScaleSymbolEffect](/documentation/symbols/scalesymboleffect/wholesymbol)

### Accessing the configuration

- [var configuration: SymbolEffectConfiguration](/documentation/symbols/scalesymboleffect/configuration)
- [VariableColorSymbolEffect](/documentation/symbols/variablecolorsymboleffect)

### Controlling fill style

- [var cumulative: VariableColorSymbolEffect](/documentation/symbols/variablecolorsymboleffect/cumulative)
- [var iterative: VariableColorSymbolEffect](/documentation/symbols/variablecolorsymboleffect/iterative)

### Changing playback style

- [var nonReversing: VariableColorSymbolEffect](/documentation/symbols/variablecolorsymboleffect/nonreversing)
- [var reversing: VariableColorSymbolEffect](/documentation/symbols/variablecolorsymboleffect/reversing)

### Affecting inactive layers

- [var dimInactiveLayers: VariableColorSymbolEffect](/documentation/symbols/variablecolorsymboleffect/diminactivelayers)
- [var hideInactiveLayers: VariableColorSymbolEffect](/documentation/symbols/variablecolorsymboleffect/hideinactivelayers)

### Accessing the configuration

- [var configuration: SymbolEffectConfiguration](/documentation/symbols/variablecolorsymboleffect/configuration)
- [NSSymbolBreatheEffect](/documentation/symbols/breathesymboleffect)

### Instance Methods


### Type Methods

- [RotateSymbolEffect](/documentation/symbols/rotatesymboleffect)

### Instance Properties

- [var byLayer: RotateSymbolEffect](/documentation/symbols/rotatesymboleffect/bylayer)
- [var clockwise: RotateSymbolEffect](/documentation/symbols/rotatesymboleffect/clockwise)
- [var configuration: SymbolEffectConfiguration](/documentation/symbols/rotatesymboleffect/configuration)
- [var counterClockwise: RotateSymbolEffect](/documentation/symbols/rotatesymboleffect/counterclockwise)
- [var wholeSymbol: RotateSymbolEffect](/documentation/symbols/rotatesymboleffect/wholesymbol)
- [WiggleSymbolEffect](/documentation/symbols/wigglesymboleffect)

### Instance Properties

- [var backward: WiggleSymbolEffect](/documentation/symbols/wigglesymboleffect/backward)
- [var byLayer: WiggleSymbolEffect](/documentation/symbols/wigglesymboleffect/bylayer)
- [var clockwise: WiggleSymbolEffect](/documentation/symbols/wigglesymboleffect/clockwise)
- [var configuration: SymbolEffectConfiguration](/documentation/symbols/wigglesymboleffect/configuration)
- [var counterClockwise: WiggleSymbolEffect](/documentation/symbols/wigglesymboleffect/counterclockwise)
- [var down: WiggleSymbolEffect](/documentation/symbols/wigglesymboleffect/down)
- [var forward: WiggleSymbolEffect](/documentation/symbols/wigglesymboleffect/forward)
- [var left: WiggleSymbolEffect](/documentation/symbols/wigglesymboleffect/left)
- [var right: WiggleSymbolEffect](/documentation/symbols/wigglesymboleffect/right)
- [var up: WiggleSymbolEffect](/documentation/symbols/wigglesymboleffect/up)
- [var wholeSymbol: WiggleSymbolEffect](/documentation/symbols/wigglesymboleffect/wholesymbol)

### Instance Methods

- [func custom(angle: Angle) -> WiggleSymbolEffect](/documentation/symbols/wigglesymboleffect/custom(angle:)-1f09q)
- [func custom(angle: Double) -> WiggleSymbolEffect](/documentation/symbols/wigglesymboleffect/custom(angle:)-cqpf)

## Symbol effect options

- [SymbolEffectOptions](/documentation/symbols/symboleffectoptions)

### Accessing effect options

- [static var `default`: SymbolEffectOptions](/documentation/symbols/symboleffectoptions/default)

### Configuring repeating effects

- [var repeating: SymbolEffectOptions](/documentation/symbols/symboleffectoptions/repeating-swift.property)
- [static var repeating: SymbolEffectOptions](/documentation/symbols/symboleffectoptions/repeating-swift.type.property)
- [var nonRepeating: SymbolEffectOptions](/documentation/symbols/symboleffectoptions/nonrepeating-swift.property)
- [static var nonRepeating: SymbolEffectOptions](/documentation/symbols/symboleffectoptions/nonrepeating-swift.type.property)
- [func `repeat`(Int?) -> SymbolEffectOptions](/documentation/symbols/symboleffectoptions/repeat(_:)-314sv)
- [static func `repeat`(Int?) -> SymbolEffectOptions](/documentation/symbols/symboleffectoptions/repeat(_:)-33816)

### Configuring effect speed

- [func speed(Double) -> SymbolEffectOptions](/documentation/symbols/symboleffectoptions/speed(_:)-swift.method)
- [static func speed(Double) -> SymbolEffectOptions](/documentation/symbols/symboleffectoptions/speed(_:)-swift.type.method)

### Structures

- [SymbolEffectOptions.RepeatBehavior](/documentation/symbols/symboleffectoptions/repeatbehavior)

#### Type Properties

- [static var continuous: SymbolEffectOptions.RepeatBehavior](/documentation/symbols/symboleffectoptions/repeatbehavior/continuous)
- [static var periodic: SymbolEffectOptions.RepeatBehavior](/documentation/symbols/symboleffectoptions/repeatbehavior/periodic)

#### Type Methods

- [static func periodic(Int?, delay: Double?) -> SymbolEffectOptions.RepeatBehavior](/documentation/symbols/symboleffectoptions/repeatbehavior/periodic(_:delay:))

### Instance Methods

- [func `repeat`(SymbolEffectOptions.RepeatBehavior) -> SymbolEffectOptions](/documentation/symbols/symboleffectoptions/repeat(_:)-316cr)

### Type Methods

- [static func `repeat`(SymbolEffectOptions.RepeatBehavior) -> SymbolEffectOptions](/documentation/symbols/symboleffectoptions/repeat(_:)-3klm2)

## Symbol effect protocols

- [SymbolEffect](/documentation/symbols/symboleffect)

### Effects

- [static var appear: AppearSymbolEffect](/documentation/symbols/symboleffect/appear)
- [static var bounce: BounceSymbolEffect](/documentation/symbols/symboleffect/bounce)
- [static var disappear: DisappearSymbolEffect](/documentation/symbols/symboleffect/disappear)
- [static var pulse: PulseSymbolEffect](/documentation/symbols/symboleffect/pulse)
- [static var scale: ScaleSymbolEffect](/documentation/symbols/symboleffect/scale)
- [static var variableColor: VariableColorSymbolEffect](/documentation/symbols/symboleffect/variablecolor)
- [static var breathe: BreatheSymbolEffect](/documentation/symbols/symboleffect/breathe)
- [static var rotate: RotateSymbolEffect](/documentation/symbols/symboleffect/rotate)
- [static var wiggle: WiggleSymbolEffect](/documentation/symbols/symboleffect/wiggle)

### Accessing the configuration

- [var configuration: SymbolEffectConfiguration](/documentation/symbols/symboleffect/configuration)
- [SymbolEffectConfiguration](/documentation/symbols/symboleffectconfiguration)

### Type Properties

- [static var automatic: AutomaticSymbolEffect](/documentation/symbols/symboleffect/automatic)
- [static var drawOff: DrawOffSymbolEffect](/documentation/symbols/symboleffect/drawoff)
- [static var drawOn: DrawOnSymbolEffect](/documentation/symbols/symboleffect/drawon)
- [static var replace: ReplaceSymbolEffect](/documentation/symbols/symboleffect/replace)
- [DiscreteSymbolEffect](/documentation/symbols/discretesymboleffect)
- [IndefiniteSymbolEffect](/documentation/symbols/indefinitesymboleffect)
- [NSSymbolContentTransition](/documentation/symbols/contenttransitionsymboleffect)
- [TransitionSymbolEffect](/documentation/symbols/transitionsymboleffect)

## Structures

- [DrawOffSymbolEffect](/documentation/symbols/drawoffsymboleffect)

### Instance Properties

- [var byLayer: DrawOffSymbolEffect](/documentation/symbols/drawoffsymboleffect/bylayer)
- [var configuration: SymbolEffectConfiguration](/documentation/symbols/drawoffsymboleffect/configuration)
- [var individually: DrawOffSymbolEffect](/documentation/symbols/drawoffsymboleffect/individually)
- [var nonReversed: DrawOffSymbolEffect](/documentation/symbols/drawoffsymboleffect/nonreversed)
- [var reversed: DrawOffSymbolEffect](/documentation/symbols/drawoffsymboleffect/reversed)
- [var wholeSymbol: DrawOffSymbolEffect](/documentation/symbols/drawoffsymboleffect/wholesymbol)
- [DrawOnSymbolEffect](/documentation/symbols/drawonsymboleffect)

### Instance Properties

- [var byLayer: DrawOnSymbolEffect](/documentation/symbols/drawonsymboleffect/bylayer)
- [var configuration: SymbolEffectConfiguration](/documentation/symbols/drawonsymboleffect/configuration)
- [var individually: DrawOnSymbolEffect](/documentation/symbols/drawonsymboleffect/individually)
- [var wholeSymbol: DrawOnSymbolEffect](/documentation/symbols/drawonsymboleffect/wholesymbol)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
