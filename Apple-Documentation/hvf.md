# hvf Documentation

Source: https://sosumi.ai/documentation/hvf

---
title: hvf
source: https://developer.apple.com/documentation/hvf
timestamp: 2026-02-13T18:57:54.980Z
---

## Classes

- [HVGLPartLoader](/documentation/hvf/hvglpartloader)

### Initializers

- [init?(hvglTable: UnsafeRawBufferPointer, hvpmTable: UnsafeRawBufferPointer?)](/documentation/hvf/hvglpartloader/init(hvgltable:hvpmtable:))

### Instance Properties

- [var glyphCount: Int](/documentation/hvf/hvglpartloader/glyphcount)
- [var partCount: Int](/documentation/hvf/hvglpartloader/partcount)
- [var tableVersion: (major: Int, minor: Int)](/documentation/hvf/hvglpartloader/tableversion)
- [PartRenderer](/documentation/hvf/partrenderer)

### Classes

- [PartRenderer.AxisValues](/documentation/hvf/partrenderer/axisvalues)

#### Instance Properties

- [var isNested: Bool](/documentation/hvf/partrenderer/axisvalues/isnested)

#### Instance Methods

- [func blendedValue(axis: Int) -> Double](/documentation/hvf/partrenderer/axisvalues/blendedvalue(axis:))
- [PartRenderer.PartParameters](/documentation/hvf/partrenderer/partparameters)

#### Instance Properties

- [var axisValues: PartRenderer.AxisValues](/documentation/hvf/partrenderer/partparameters/axisvalues)
- [var blendedRotation: Double](/documentation/hvf/partrenderer/partparameters/blendedrotation)
- [var blendedTranslation: PartRenderer.Translation](/documentation/hvf/partrenderer/partparameters/blendedtranslation)
- [let partIndex: Int](/documentation/hvf/partrenderer/partparameters/partindex)
- [var rotation: Double](/documentation/hvf/partrenderer/partparameters/rotation)
- [var subparts: PartRenderer.Subparts](/documentation/hvf/partrenderer/partparameters/subparts)
- [var translation: PartRenderer.Translation](/documentation/hvf/partrenderer/partparameters/translation)

### Structures

- [PartRenderer.Point](/documentation/hvf/partrenderer/point)

#### Initializers

- [init(x: Double, y: Double)](/documentation/hvf/partrenderer/point/init(x:y:))

#### Instance Properties

- [var x: Double](/documentation/hvf/partrenderer/point/x)
- [var y: Double](/documentation/hvf/partrenderer/point/y)
- [PartRenderer.Subparts](/documentation/hvf/partrenderer/subparts)
- [PartRenderer.Translation](/documentation/hvf/partrenderer/translation)

#### Initializers

- [init(dx: Double, dy: Double)](/documentation/hvf/partrenderer/translation/init(dx:dy:))

#### Instance Properties

- [var dx: Double](/documentation/hvf/partrenderer/translation/dx)
- [var dy: Double](/documentation/hvf/partrenderer/translation/dy)

### Initializers

- [init(custom: CustomPartLoader, reusable: Bool)](/documentation/hvf/partrenderer/init(custom:reusable:))
- [init(hvglLoader: HVGLPartLoader, reusable: Bool)](/documentation/hvf/partrenderer/init(hvglloader:reusable:))

### Instance Properties

- [var blendedAxisValueBounds: ClosedRange<Double>](/documentation/hvf/partrenderer/blendedaxisvaluebounds)
- [var parameters: PartRenderer.PartParameters](/documentation/hvf/partrenderer/parameters)
- [var partAxisCount: Int](/documentation/hvf/partrenderer/partaxiscount)
- [var partIndex: Int](/documentation/hvf/partrenderer/partindex)

### Instance Methods

- [func clearPartCache()](/documentation/hvf/partrenderer/clearpartcache())
- [func render(to: (PartRenderer.Instruction) -> PartRenderer.Action) -> Bool](/documentation/hvf/partrenderer/render(to:))

### Enumerations

- [PartRenderer.Action](/documentation/hvf/partrenderer/action)

#### Enumeration Cases

- [case `continue`](/documentation/hvf/partrenderer/action/continue)
- [case skip](/documentation/hvf/partrenderer/action/skip)
- [case stop](/documentation/hvf/partrenderer/action/stop)
- [PartRenderer.Instruction](/documentation/hvf/partrenderer/instruction)

#### Enumeration Cases

- [case addCubic(cp1: PartRenderer.Point, cp2: PartRenderer.Point, on: PartRenderer.Point)](/documentation/hvf/partrenderer/instruction/addcubic(cp1:cp2:on:))
- [case addLine(PartRenderer.Point)](/documentation/hvf/partrenderer/instruction/addline(_:))
- [case addPoint(PartRenderer.Point)](/documentation/hvf/partrenderer/instruction/addpoint(_:))
- [case addQuad(off: PartRenderer.Point, on: PartRenderer.Point)](/documentation/hvf/partrenderer/instruction/addquad(off:on:))
- [case beginPart(id: Int, name: String?)](/documentation/hvf/partrenderer/instruction/beginpart(id:name:))
- [case beginPath](/documentation/hvf/partrenderer/instruction/beginpath)
- [case closePath](/documentation/hvf/partrenderer/instruction/closepath)
- [case endPart(id: Int, name: String?)](/documentation/hvf/partrenderer/instruction/endpart(id:name:))
- [case endPath](/documentation/hvf/partrenderer/instruction/endpath)
- [case stop](/documentation/hvf/partrenderer/instruction/stop)

## Protocols

- [CompositeWriter](/documentation/hvf/compositewriter)

### Instance Properties

- [var axisCount: Int](/documentation/hvf/compositewriter/axiscount)
- [var extremumCSCAxisValues: [Float]](/documentation/hvf/compositewriter/extremumcscaxisvalues)
- [var extremumCSCColumnStarts: [UInt16]](/documentation/hvf/compositewriter/extremumcsccolumnstarts)
- [var extremumCSCRowIndices: [UInt16]](/documentation/hvf/compositewriter/extremumcscrowindices)
- [var extremumRotationIndices: [CompositeExtremumIndex]](/documentation/hvf/compositewriter/extremumrotationindices)
- [var extremumRotations: [Float]](/documentation/hvf/compositewriter/extremumrotations)
- [var extremumTranslationIndices: [CompositeExtremumIndex]](/documentation/hvf/compositewriter/extremumtranslationindices)
- [var extremumTranslations: [CompositeSubpartTranslation]](/documentation/hvf/compositewriter/extremumtranslations)
- [var masterCSCAxisValues: [Float]](/documentation/hvf/compositewriter/mastercscaxisvalues)
- [var masterCSCRowIndices: [UInt16]](/documentation/hvf/compositewriter/mastercscrowindices)
- [var masterRotationIndices: [UInt16]](/documentation/hvf/compositewriter/masterrotationindices)
- [var masterRotations: [Float]](/documentation/hvf/compositewriter/masterrotations)
- [var masterTranslationIndices: [UInt16]](/documentation/hvf/compositewriter/mastertranslationindices)
- [var masterTranslations: [CompositeSubpartTranslation]](/documentation/hvf/compositewriter/mastertranslations)
- [var maximumExtremumCount: Int](/documentation/hvf/compositewriter/maximumextremumcount)
- [var subpartCount: Int](/documentation/hvf/compositewriter/subpartcount)
- [var subparts: [CompositeSubpart]](/documentation/hvf/compositewriter/subparts)
- [var totalAxisCount: Int](/documentation/hvf/compositewriter/totalaxiscount)
- [var totalPartCount: Int](/documentation/hvf/compositewriter/totalpartcount)

### Instance Methods

- [func column(axis: Int, extremum: AxisExtremum) -> Int](/documentation/hvf/compositewriter/column(axis:extremum:))
- [func finalize() -> Bool](/documentation/hvf/compositewriter/finalize())
- [PartGenerator](/documentation/hvf/partgenerator)

### Instance Methods

- [func makeComposite(Int) -> any CompositeWriter](/documentation/hvf/partgenerator/makecomposite(_:))
- [func makeShape(Int) -> any ShapeWriter](/documentation/hvf/partgenerator/makeshape(_:))
- [ShapeWriter](/documentation/hvf/shapewriter)

### Instance Properties

- [var axisCount: Int](/documentation/hvf/shapewriter/axiscount)
- [var blendTypes: [SegmentBlendType]](/documentation/hvf/shapewriter/blendtypes)
- [var denseDeltaMatrix: [Double]](/documentation/hvf/shapewriter/densedeltamatrix)
- [var masterVector: [Double]](/documentation/hvf/shapewriter/mastervector)
- [var pathSizes: [UInt16]](/documentation/hvf/shapewriter/pathsizes)
- [var totalSegmentCount: Int](/documentation/hvf/shapewriter/totalsegmentcount)

### Instance Methods

- [func denseDeltaOffset(axis: Int, extremum: AxisExtremum, segment: Int, point: SegmentPoint, coordinate: PointCoordinate) -> Int](/documentation/hvf/shapewriter/densedeltaoffset(axis:extremum:segment:point:coordinate:))
- [func finalize() -> Bool](/documentation/hvf/shapewriter/finalize())
- [func masterOffset(segment: Int, point: SegmentPoint, coordinate: PointCoordinate) -> Int](/documentation/hvf/shapewriter/masteroffset(segment:point:coordinate:))

## Structures

- [CompositeExtremumIndex](/documentation/hvf/compositeextremumindex)

### Initializers

- [init(row: UInt16, column: UInt16)](/documentation/hvf/compositeextremumindex/init(row:column:))

### Instance Properties

- [var column: UInt16](/documentation/hvf/compositeextremumindex/column)
- [var row: UInt16](/documentation/hvf/compositeextremumindex/row)
- [CompositeSubpart](/documentation/hvf/compositesubpart)

### Initializers

- [init(partIndex: UInt32, treePartOffset: UInt16, treeAxisOffset: UInt16)](/documentation/hvf/compositesubpart/init(partindex:treepartoffset:treeaxisoffset:))

### Instance Properties

- [var partIndex: UInt32](/documentation/hvf/compositesubpart/partindex)
- [var treeAxisOffset: UInt16](/documentation/hvf/compositesubpart/treeaxisoffset)
- [var treePartOffset: UInt16](/documentation/hvf/compositesubpart/treepartoffset)
- [CompositeSubpartTranslation](/documentation/hvf/compositesubparttranslation)

### Initializers

- [init(dx: Float, dy: Float)](/documentation/hvf/compositesubparttranslation/init(dx:dy:))

### Instance Properties

- [var dx: Float](/documentation/hvf/compositesubparttranslation/dx)
- [var dy: Float](/documentation/hvf/compositesubparttranslation/dy)

## Variables

- [let hvfLibraryVersion: (major: Int, minor: Int, patch: Int)](/documentation/hvf/hvflibraryversion-swift.var)

## Type Aliases

- [CustomPartLoader](/documentation/hvf/custompartloader)

## Enumerations

- [AxisExtremum](/documentation/hvf/axisextremum)

### Enumeration Cases

- [case maximum](/documentation/hvf/axisextremum/maximum)
- [case minimum](/documentation/hvf/axisextremum/minimum)
- [PartResult](/documentation/hvf/partresult)

### Enumeration Cases

- [case composite(any CompositeWriter)](/documentation/hvf/partresult/composite(_:))
- [case notFound](/documentation/hvf/partresult/notfound)
- [case shape(any ShapeWriter)](/documentation/hvf/partresult/shape(_:))
- [PointCoordinate](/documentation/hvf/pointcoordinate)

### Enumeration Cases

- [case xOrParallel](/documentation/hvf/pointcoordinate/xorparallel)
- [case yOrZero](/documentation/hvf/pointcoordinate/yorzero)
- [SegmentBlendType](/documentation/hvf/segmentblendtype)

### Enumeration Cases

- [case corner](/documentation/hvf/segmentblendtype/corner)
- [case curve](/documentation/hvf/segmentblendtype/curve)
- [case tangent](/documentation/hvf/segmentblendtype/tangent)
- [case tangentTangent1](/documentation/hvf/segmentblendtype/tangenttangent1)
- [case tangentTangent2](/documentation/hvf/segmentblendtype/tangenttangent2)
- [SegmentPoint](/documentation/hvf/segmentpoint)

### Enumeration Cases

- [case off](/documentation/hvf/segmentpoint/off)
- [case on](/documentation/hvf/segmentpoint/on)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
