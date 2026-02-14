# Spatial Documentation

Source: https://sosumi.ai/documentation/spatial

---
title: Spatial
source: https://developer.apple.com/documentation/spatial
timestamp: 2026-02-13T19:02:29.575Z
---

## Data structures

- [Vector3D](/documentation/spatial/vector3d)

### Creating a vector

- [init()](/documentation/spatial/vector3d/init())
- [init(x: Double, y: Double, z: Double)](/documentation/spatial/vector3d/init(x:y:z:)-2ejxw)
- [init<T>(x: T, y: T, z: T)](/documentation/spatial/vector3d/init(x:y:z:)-29hwg)
- [init(simd_float3)](/documentation/spatial/vector3d/init(_:)-73gdm)
- [init(simd_double3)](/documentation/spatial/vector3d/init(_:)-1a9i3)
- [init(vector: simd_double3)](/documentation/spatial/vector3d/init(vector:))
- [init(RotationAxis3D)](/documentation/spatial/vector3d/init(_:)-3br9h)
- [init(Point3D)](/documentation/spatial/vector3d/init(_:)-8vcph)
- [init(Size3D)](/documentation/spatial/vector3d/init(_:)-8egfs)
- [init(SphericalCoordinates3D)](/documentation/spatial/vector3d/init(_:)-9ker1)

### Inspecting a vector’s properties

- [var x: Double](/documentation/spatial/vector3d/x)
- [var y: Double](/documentation/spatial/vector3d/y)
- [var z: Double](/documentation/spatial/vector3d/z)
- [var vector: simd_double3](/documentation/spatial/vector3d/vector)

### Checking characteristics

- [func rotation(to: Vector3D) -> Rotation3D](/documentation/spatial/vector3d/rotation(to:))

### Geometry functions

- [func cross(Vector3D) -> Vector3D](/documentation/spatial/vector3d/cross(_:))
- [func dot(Vector3D) -> Double](/documentation/spatial/vector3d/dot(_:))
- [var length: Double](/documentation/spatial/vector3d/length)
- [var lengthSquared: Double](/documentation/spatial/vector3d/lengthsquared)
- [func normalize()](/documentation/spatial/vector3d/normalize())
- [var normalized: Vector3D](/documentation/spatial/vector3d/normalized)
- [func projected(Vector3D) -> Vector3D](/documentation/spatial/vector3d/projected(_:))
- [func reflected(Vector3D) -> Vector3D](/documentation/spatial/vector3d/reflected(_:))

### Transforming a vector

- [func applying(AffineTransform3D) -> Vector3D](/documentation/spatial/vector3d/applying(_:)-1d0mh)
- [func applying(ProjectiveTransform3D) -> Vector3D](/documentation/spatial/vector3d/applying(_:)-5y3xb)
- [func applying(Pose3D) -> Vector3D](/documentation/spatial/vector3d/applying(_:)-4k2qi)
- [func unapplying(AffineTransform3D) -> Vector3D](/documentation/spatial/vector3d/unapplying(_:)-6vl3o)
- [func unapplying(ProjectiveTransform3D) -> Vector3D](/documentation/spatial/vector3d/unapplying(_:)-8ookb)
- [func unapplying(Pose3D) -> Vector3D](/documentation/spatial/vector3d/unapplying(_:)-1gzyd)
- [func rotated(by: Rotation3D) -> Vector3D](/documentation/spatial/vector3d/rotated(by:)-2gcq4)
- [func rotated(by: simd_quatd) -> Vector3D](/documentation/spatial/vector3d/rotated(by:)-8bwna)
- [func scaled(by: Size3D) -> Vector3D](/documentation/spatial/vector3d/scaled(by:))
- [func scaledBy(x: Double, y: Double, z: Double) -> Vector3D](/documentation/spatial/vector3d/scaledby(x:y:z:))
- [func uniformlyScaled(by: Double) -> Vector3D](/documentation/spatial/vector3d/uniformlyscaled(by:))
- [func sheared(AxisWithFactors) -> Vector3D](/documentation/spatial/vector3d/sheared(_:))
- [func applying(ScaledPose3D) -> Vector3D](/documentation/spatial/vector3d/applying(_:)-8fn6a)
- [func unapplying(ScaledPose3D) -> Vector3D](/documentation/spatial/vector3d/unapplying(_:)-4uxr2)

### Comparing values

- [static func == (Vector3D, Vector3D) -> Bool](/documentation/spatial/vector3d/==(_:_:))

### Encoding and decoding a vector

- [init(from: any Decoder) throws](/documentation/spatial/vector3d/init(from:))
- [func encode(to: any Encoder) throws](/documentation/spatial/vector3d/encode(to:))

### Type properties

- [static let forward: Vector3D](/documentation/spatial/vector3d/forward)
- [static let right: Vector3D](/documentation/spatial/vector3d/right)
- [static let up: Vector3D](/documentation/spatial/vector3d/up)

### Applying arithmetic operations

- [static func * (Vector3D, Double) -> Vector3D](/documentation/spatial/vector3d/*(_:_:)-dcwn)
- [static func * (Double, Vector3D) -> Vector3D](/documentation/spatial/vector3d/*(_:_:)-64lzt)
- [static func * (AffineTransform3D, Vector3D) -> Vector3D](/documentation/spatial/vector3d/*(_:_:)-6rxsr)
- [static func * (ProjectiveTransform3D, Vector3D) -> Vector3D](/documentation/spatial/vector3d/*(_:_:)-3dpli)
- [static func * (Pose3D, Vector3D) -> Vector3D](/documentation/spatial/vector3d/*(_:_:)-8y7xq)
- [static func + (Vector3D, Vector3D) -> Vector3D](/documentation/spatial/vector3d/+(_:_:)-7gbcj)
- [static func + (Vector3D, Size3D) -> Size3D](/documentation/spatial/vector3d/+(_:_:)-9xfxv)
- [static func + (Size3D, Vector3D) -> Size3D](/documentation/spatial/vector3d/+(_:_:)-1xufx)
- [static func + (Vector3D, Point3D) -> Point3D](/documentation/spatial/vector3d/+(_:_:)-1bq1m)
- [static func + (Point3D, Vector3D) -> Point3D](/documentation/spatial/vector3d/+(_:_:)-4rsou)
- [static func - (Vector3D) -> Vector3D](/documentation/spatial/vector3d/-(_:))
- [static func - (Vector3D, Vector3D) -> Vector3D](/documentation/spatial/vector3d/-(_:_:)-6zam)
- [static func - (Vector3D, Size3D) -> Size3D](/documentation/spatial/vector3d/-(_:_:)-6lui1)
- [static func - (Size3D, Vector3D) -> Size3D](/documentation/spatial/vector3d/-(_:_:)-3qpww)
- [static func - (Vector3D, Point3D) -> Point3D](/documentation/spatial/vector3d/-(_:_:)-1nz82)
- [static func - (Point3D, Vector3D) -> Point3D](/documentation/spatial/vector3d/-(_:_:)-8sgai)
- [static func *= (inout Vector3D, Double)](/documentation/spatial/vector3d/*=(_:_:))
- [static func += (inout Vector3D, Vector3D)](/documentation/spatial/vector3d/+=(_:_:))
- [static func -= (inout Vector3D, Vector3D)](/documentation/spatial/vector3d/-=(_:_:))
- [static func / (Vector3D, Double) -> Vector3D](/documentation/spatial/vector3d/_(_:_:))
- [static func /= (inout Vector3D, Double)](/documentation/spatial/vector3d/_=(_:_:))

### Initializers

- [init(simd_packed_double4)](/documentation/spatial/vector3d/init(_:)-23qst)
- [init(Vector3DFloat)](/documentation/spatial/vector3d/init(_:)-272sg)

### Type Methods

- [static func lerp(from: Vector3D, to: Vector3D, t: Vector3D) -> Vector3D](/documentation/spatial/vector3d/lerp(from:to:t:))
- [static func smoothstep(edge0: Vector3D, edge1: Vector3D, x: Vector3D) -> Vector3D](/documentation/spatial/vector3d/smoothstep(edge0:edge1:x:))

### Default Implementations

- [AdditiveArithmetic Implementations](/documentation/spatial/vector3d/additivearithmetic-implementations)

#### Operators

- [static func + (Vector3D, Vector3D) -> Vector3D](/documentation/spatial/vector3d/+(_:_:)-7gbcj)
- [static func += (inout Vector3D, Vector3D)](/documentation/spatial/vector3d/+=(_:_:))
- [static func - (Vector3D, Vector3D) -> Vector3D](/documentation/spatial/vector3d/-(_:_:)-6zam)
- [static func -= (inout Vector3D, Vector3D)](/documentation/spatial/vector3d/-=(_:_:))
- [CustomReflectable Implementations](/documentation/spatial/vector3d/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/vector3d/custommirror)
- [Decodable Implementations](/documentation/spatial/vector3d/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/vector3d/init(from:))
- [Encodable Implementations](/documentation/spatial/vector3d/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/vector3d/encode(to:))
- [Equatable Implementations](/documentation/spatial/vector3d/equatable-implementations)

#### Operators

- [static func == (Vector3D, Vector3D) -> Bool](/documentation/spatial/vector3d/==(_:_:))
- [Hashable Implementations](/documentation/spatial/vector3d/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/vector3d/hash(into:))
- [Primitive3DProtocol Implementations](/documentation/spatial/vector3d/primitive3dprotocol-implementations)

#### Instance Methods

- [func applying(AffineTransform3D) -> Vector3D](/documentation/spatial/vector3d/applying(_:)-1d0mh)
- [func applying(Pose3D) -> Vector3D](/documentation/spatial/vector3d/applying(_:)-4k2qi)
- [func unapplying(Pose3D) -> Vector3D](/documentation/spatial/vector3d/unapplying(_:)-1gzyd)
- [func unapplying(AffineTransform3D) -> Vector3D](/documentation/spatial/vector3d/unapplying(_:)-6vl3o)
- [func unapplying(ProjectiveTransform3D) -> Vector3D](/documentation/spatial/vector3d/unapplying(_:)-8ookb)
- [ProjectiveTransformable3D Implementations](/documentation/spatial/vector3d/projectivetransformable3d-implementations)

#### Instance Methods

- [func applying(ProjectiveTransform3D) -> Vector3D](/documentation/spatial/vector3d/applying(_:)-5y3xb)
- [Rotatable3DProtocol Implementations](/documentation/spatial/vector3d/rotatable3dprotocol-implementations)

#### Instance Methods

- [func rotated(by: Rotation3D) -> Vector3D](/documentation/spatial/vector3d/rotated(by:)-2gcq4)
- [func rotated(by: simd_quatd) -> Vector3D](/documentation/spatial/vector3d/rotated(by:)-8bwna)
- [Scalable3DProtocol Implementations](/documentation/spatial/vector3d/scalable3dprotocol-implementations)

#### Instance Methods

- [func scaled(by: Size3D) -> Vector3D](/documentation/spatial/vector3d/scaled(by:))
- [func scaledBy(x: Double, y: Double, z: Double) -> Vector3D](/documentation/spatial/vector3d/scaledby(x:y:z:))
- [func uniformlyScaled(by: Double) -> Vector3D](/documentation/spatial/vector3d/uniformlyscaled(by:))
- [Shearable3D Implementations](/documentation/spatial/vector3d/shearable3d-implementations)

#### Instance Methods

- [func sheared(AxisWithFactors) -> Vector3D](/documentation/spatial/vector3d/sheared(_:))
- [Vector3DFloat](/documentation/spatial/vector3dfloat)

### Operators

- [static func * (Pose3DFloat, Vector3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/*(_:_:)-1nqw7)
- [static func * (ProjectiveTransform3DFloat, Vector3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/*(_:_:)-39da3)
- [static func * (Vector3DFloat, Float) -> Vector3DFloat](/documentation/spatial/vector3dfloat/*(_:_:)-5f6x6)
- [static func * (Float, Vector3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/*(_:_:)-77n9y)
- [static func * (AffineTransform3DFloat, Vector3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/*(_:_:)-86gx9)
- [static func *= (inout Vector3DFloat, Float)](/documentation/spatial/vector3dfloat/*=(_:_:))
- [static func + (Point3DFloat, Vector3DFloat) -> Point3DFloat](/documentation/spatial/vector3dfloat/+(_:_:)-1l8zf)
- [static func + (Vector3DFloat, Point3DFloat) -> Point3DFloat](/documentation/spatial/vector3dfloat/+(_:_:)-1wtkv)
- [static func + (Size3DFloat, Vector3DFloat) -> Size3DFloat](/documentation/spatial/vector3dfloat/+(_:_:)-2l7re)
- [static func + (Vector3DFloat, Size3DFloat) -> Size3DFloat](/documentation/spatial/vector3dfloat/+(_:_:)-94qrx)
- [static func - (Vector3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/-(_:))
- [static func - (Vector3DFloat, Size3DFloat) -> Size3DFloat](/documentation/spatial/vector3dfloat/-(_:_:)-115el)
- [static func - (Size3DFloat, Vector3DFloat) -> Size3DFloat](/documentation/spatial/vector3dfloat/-(_:_:)-5qy45)
- [static func - (Vector3DFloat, Point3DFloat) -> Point3DFloat](/documentation/spatial/vector3dfloat/-(_:_:)-7h9bz)
- [static func - (Point3DFloat, Vector3DFloat) -> Point3DFloat](/documentation/spatial/vector3dfloat/-(_:_:)-8k83d)
- [static func / (Vector3DFloat, Float) -> Vector3DFloat](/documentation/spatial/vector3dfloat/_(_:_:))
- [static func /= (inout Vector3DFloat, Float)](/documentation/spatial/vector3dfloat/_=(_:_:))

### Initializers

- [init()](/documentation/spatial/vector3dfloat/init())
- [init(RotationAxis3DFloat)](/documentation/spatial/vector3dfloat/init(_:)-13p20)
- [init(simd_packed_float4)](/documentation/spatial/vector3dfloat/init(_:)-1w9o5)
- [init(Point3DFloat)](/documentation/spatial/vector3dfloat/init(_:)-217dp)
- [init(simd_double3)](/documentation/spatial/vector3dfloat/init(_:)-2qtq8)
- [init(simd_float3)](/documentation/spatial/vector3dfloat/init(_:)-3c8f6)
- [init(SphericalCoordinates3DFloat)](/documentation/spatial/vector3dfloat/init(_:)-4svr4)
- [init(Vector3D)](/documentation/spatial/vector3dfloat/init(_:)-538j2)
- [init(Size3DFloat)](/documentation/spatial/vector3dfloat/init(_:)-7y4t0)
- [init(vector: simd_float3)](/documentation/spatial/vector3dfloat/init(vector:))
- [init<T>(x: T, y: T, z: T)](/documentation/spatial/vector3dfloat/init(x:y:z:)-1h79g)
- [init(x: Float, y: Float, z: Float)](/documentation/spatial/vector3dfloat/init(x:y:z:)-8dkie)

### Instance Properties

- [var length: Float](/documentation/spatial/vector3dfloat/length)
- [var lengthSquared: Float](/documentation/spatial/vector3dfloat/lengthsquared)
- [var normalized: Vector3DFloat](/documentation/spatial/vector3dfloat/normalized)
- [var vector: simd_float3](/documentation/spatial/vector3dfloat/vector)
- [var x: Float](/documentation/spatial/vector3dfloat/x)
- [var y: Float](/documentation/spatial/vector3dfloat/y)
- [var z: Float](/documentation/spatial/vector3dfloat/z)

### Instance Methods

- [func applying(ScaledPose3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/applying(_:)-3mahk)
- [func cross(Vector3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/cross(_:))
- [func dot(Vector3DFloat) -> Float](/documentation/spatial/vector3dfloat/dot(_:))
- [func normalize()](/documentation/spatial/vector3dfloat/normalize())
- [func projected(Vector3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/projected(_:))
- [func reflected(Vector3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/reflected(_:))
- [func rotation(to: Vector3DFloat) -> Rotation3DFloat](/documentation/spatial/vector3dfloat/rotation(to:))
- [func sheared(AxisWithFactors) -> Vector3DFloat](/documentation/spatial/vector3dfloat/sheared(_:))
- [func unapplying(ScaledPose3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/unapplying(_:)-9dwm2)

### Type Properties

- [static let forward: Vector3DFloat](/documentation/spatial/vector3dfloat/forward)
- [static let right: Vector3DFloat](/documentation/spatial/vector3dfloat/right)
- [static let up: Vector3DFloat](/documentation/spatial/vector3dfloat/up)

### Type Methods

- [static func lerp(from: Vector3DFloat, to: Vector3DFloat, t: Vector3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/lerp(from:to:t:))
- [static func smoothstep(edge0: Vector3DFloat, edge1: Vector3DFloat, x: Vector3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/smoothstep(edge0:edge1:x:))

### Default Implementations

- [AdditiveArithmetic Implementations](/documentation/spatial/vector3dfloat/additivearithmetic-implementations)

#### Operators

- [static func + (Vector3DFloat, Vector3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/+(_:_:)-5a0s0)
- [static func += (inout Vector3DFloat, Vector3DFloat)](/documentation/spatial/vector3dfloat/+=(_:_:))
- [static func - (Vector3DFloat, Vector3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/-(_:_:)-87qbd)
- [static func -= (inout Vector3DFloat, Vector3DFloat)](/documentation/spatial/vector3dfloat/-=(_:_:))
- [CustomReflectable Implementations](/documentation/spatial/vector3dfloat/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/vector3dfloat/custommirror)
- [Decodable Implementations](/documentation/spatial/vector3dfloat/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/vector3dfloat/init(from:))
- [Encodable Implementations](/documentation/spatial/vector3dfloat/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/vector3dfloat/encode(to:))
- [Equatable Implementations](/documentation/spatial/vector3dfloat/equatable-implementations)

#### Operators

- [static func == (Vector3DFloat, Vector3DFloat) -> Bool](/documentation/spatial/vector3dfloat/==(_:_:))
- [Hashable Implementations](/documentation/spatial/vector3dfloat/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/vector3dfloat/hash(into:))
- [Primitive3DProtocol Implementations](/documentation/spatial/vector3dfloat/primitive3dprotocol-implementations)

#### Instance Methods

- [func applying(AffineTransform3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/applying(_:)-1a8xg)
- [func applying(ProjectiveTransform3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/applying(_:)-6hw8r)
- [func applying(Pose3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/applying(_:)-81zwt)
- [func unapplying(AffineTransform3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/unapplying(_:)-2n7h2)
- [func unapplying(Pose3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/unapplying(_:)-4xdju)
- [func unapplying(ProjectiveTransform3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/unapplying(_:)-wz3i)
- [Rotatable3DProtocol Implementations](/documentation/spatial/vector3dfloat/rotatable3dprotocol-implementations)

#### Instance Methods

- [func rotated(by: simd_quatf) -> Vector3DFloat](/documentation/spatial/vector3dfloat/rotated(by:)-56jvg)
- [func rotated(by: Rotation3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/rotated(by:)-7v04s)
- [Scalable3DProtocol Implementations](/documentation/spatial/vector3dfloat/scalable3dprotocol-implementations)

#### Instance Methods

- [func scaled(by: Size3DFloat) -> Vector3DFloat](/documentation/spatial/vector3dfloat/scaled(by:))
- [func scaledBy(x: Float, y: Float, z: Float) -> Vector3DFloat](/documentation/spatial/vector3dfloat/scaledby(x:y:z:))
- [func uniformlyScaled(by: Float) -> Vector3DFloat](/documentation/spatial/vector3dfloat/uniformlyscaled(by:))
- [Axis3D](/documentation/spatial/axis3d)

### Constants

- [static var x: Axis3D](/documentation/spatial/axis3d/x)
- [static var y: Axis3D](/documentation/spatial/axis3d/y)
- [static var z: Axis3D](/documentation/spatial/axis3d/z)

### Initializers

- [init(UInt32)](/documentation/spatial/axis3d/init(_:))
- [init(rawValue: UInt32)](/documentation/spatial/axis3d/init(rawvalue:))

### Inspecting the axis

- [var rawValue: UInt32](/documentation/spatial/axis3d/rawvalue)

### Default Implementations

- [Decodable Implementations](/documentation/spatial/axis3d/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/axis3d/init(from:))
- [Encodable Implementations](/documentation/spatial/axis3d/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/axis3d/encode(to:))
- [Hashable Implementations](/documentation/spatial/axis3d/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/axis3d/hash(into:))

## 2D primitives

- [Angle2D](/documentation/spatial/angle2d)

### Creating an angle structure

- [init()](/documentation/spatial/angle2d/init())
- [init(radians: Double)](/documentation/spatial/angle2d/init(radians:)-3zcwo)
- [init(radians: Double)](/documentation/spatial/angle2d/init(radians:)-6s7o6)
- [init<T>(radians: T)](/documentation/spatial/angle2d/init(radians:)-74ym2)
- [init<T>(degrees: T)](/documentation/spatial/angle2d/init(degrees:)-2obd)
- [init(degrees: Double)](/documentation/spatial/angle2d/init(degrees:)-7y9lb)
- [static func degrees(Double) -> Angle2D](/documentation/spatial/angle2d/degrees(_:))
- [static func radians(Double) -> Angle2D](/documentation/spatial/angle2d/radians(_:))

### Inspecting an angle’s properties

- [var degrees: Double](/documentation/spatial/angle2d/degrees)
- [var radians: Double](/documentation/spatial/angle2d/radians)

### Geometry functions

- [static func acos(Double) -> Angle2D](/documentation/spatial/angle2d/acos(_:))
- [static func acosh(Double) -> Angle2D](/documentation/spatial/angle2d/acosh(_:))
- [static func asin(Double) -> Angle2D](/documentation/spatial/angle2d/asin(_:))
- [static func asinh(Double) -> Angle2D](/documentation/spatial/angle2d/asinh(_:))
- [static func atan(Double) -> Angle2D](/documentation/spatial/angle2d/atan(_:))
- [static func atan2(y: Double, x: Double) -> Angle2D](/documentation/spatial/angle2d/atan2(y:x:))
- [static func atanh(Double) -> Angle2D](/documentation/spatial/angle2d/atanh(_:))
- [var normalized: Angle2D](/documentation/spatial/angle2d/normalized)

### Comparing values

- [static func == (Angle2D, Angle2D) -> Bool](/documentation/spatial/angle2d/==(_:_:))

### Encoding and decoding an angle structure

- [init(from: any Decoder) throws](/documentation/spatial/angle2d/init(from:))
- [func encode(to: any Encoder) throws](/documentation/spatial/angle2d/encode(to:))

### Applying arithmetic operations

- [static func + (Angle2D) -> Angle2D](/documentation/spatial/angle2d/+(_:))
- [static func + (Angle2D, Angle2D) -> Angle2D](/documentation/spatial/angle2d/+(_:_:))
- [static func += (inout Angle2D, Angle2D)](/documentation/spatial/angle2d/+=(_:_:))
- [static func - (Angle2D) -> Angle2D](/documentation/spatial/angle2d/-(_:))
- [static func - (Angle2D, Angle2D) -> Angle2D](/documentation/spatial/angle2d/-(_:_:))
- [static func -= (inout Angle2D, Angle2D)](/documentation/spatial/angle2d/-=(_:_:))

### Initializers

- [init(Angle)](/documentation/spatial/angle2d/init(_:)-44cs8)
- [init(Angle2DFloat)](/documentation/spatial/angle2d/init(_:)-7nf6j)

### Default Implementations

- [AdditiveArithmetic Implementations](/documentation/spatial/angle2d/additivearithmetic-implementations)

#### Operators

- [static func + (Angle2D, Angle2D) -> Angle2D](/documentation/spatial/angle2d/+(_:_:))
- [static func += (inout Angle2D, Angle2D)](/documentation/spatial/angle2d/+=(_:_:))
- [static func - (Angle2D, Angle2D) -> Angle2D](/documentation/spatial/angle2d/-(_:_:))
- [static func -= (inout Angle2D, Angle2D)](/documentation/spatial/angle2d/-=(_:_:))
- [Comparable Implementations](/documentation/spatial/angle2d/comparable-implementations)

#### Operators

- [static func < (Angle2D, Angle2D) -> Bool](/documentation/spatial/angle2d/_(_:_:))
- [CustomReflectable Implementations](/documentation/spatial/angle2d/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/angle2d/custommirror)
- [Decodable Implementations](/documentation/spatial/angle2d/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/angle2d/init(from:))
- [Encodable Implementations](/documentation/spatial/angle2d/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/angle2d/encode(to:))
- [Equatable Implementations](/documentation/spatial/angle2d/equatable-implementations)

#### Operators

- [static func == (Angle2D, Angle2D) -> Bool](/documentation/spatial/angle2d/==(_:_:))
- [Hashable Implementations](/documentation/spatial/angle2d/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/angle2d/hash(into:))
- [Angle2DFloat](/documentation/spatial/angle2dfloat)

### Operators

- [static func + (Angle2DFloat) -> Angle2DFloat](/documentation/spatial/angle2dfloat/+(_:))
- [static func - (Angle2DFloat) -> Angle2DFloat](/documentation/spatial/angle2dfloat/-(_:))

### Initializers

- [init()](/documentation/spatial/angle2dfloat/init())
- [init(Angle2D)](/documentation/spatial/angle2dfloat/init(_:))
- [init<T>(degrees: T)](/documentation/spatial/angle2dfloat/init(degrees:)-2mulz)
- [init(degrees: Float)](/documentation/spatial/angle2dfloat/init(degrees:)-56b20)
- [init(radians: Float)](/documentation/spatial/angle2dfloat/init(radians:)-4uwyj)
- [init<T>(radians: T)](/documentation/spatial/angle2dfloat/init(radians:)-9r8ja)
- [init(radians: Float)](/documentation/spatial/angle2dfloat/init(radians:)-9ri4z)

### Instance Properties

- [var degrees: Float](/documentation/spatial/angle2dfloat/degrees)
- [var normalized: Angle2DFloat](/documentation/spatial/angle2dfloat/normalized)
- [var radians: Float](/documentation/spatial/angle2dfloat/radians)

### Type Methods

- [static func acos(Float) -> Angle2DFloat](/documentation/spatial/angle2dfloat/acos(_:))
- [static func acosh(Float) -> Angle2DFloat](/documentation/spatial/angle2dfloat/acosh(_:))
- [static func asin(Float) -> Angle2DFloat](/documentation/spatial/angle2dfloat/asin(_:))
- [static func asinh(Float) -> Angle2DFloat](/documentation/spatial/angle2dfloat/asinh(_:))
- [static func atan(Float) -> Angle2DFloat](/documentation/spatial/angle2dfloat/atan(_:))
- [static func atan2(y: Float, x: Float) -> Angle2DFloat](/documentation/spatial/angle2dfloat/atan2(y:x:))
- [static func atanh(Float) -> Angle2DFloat](/documentation/spatial/angle2dfloat/atanh(_:))
- [static func degrees(Float) -> Angle2DFloat](/documentation/spatial/angle2dfloat/degrees(_:))
- [static func radians(Float) -> Angle2DFloat](/documentation/spatial/angle2dfloat/radians(_:))

### Default Implementations

- [AdditiveArithmetic Implementations](/documentation/spatial/angle2dfloat/additivearithmetic-implementations)

#### Operators

- [static func + (Angle2DFloat, Angle2DFloat) -> Angle2DFloat](/documentation/spatial/angle2dfloat/+(_:_:))
- [static func += (inout Angle2DFloat, Angle2DFloat)](/documentation/spatial/angle2dfloat/+=(_:_:))
- [static func - (Angle2DFloat, Angle2DFloat) -> Angle2DFloat](/documentation/spatial/angle2dfloat/-(_:_:))
- [static func -= (inout Angle2DFloat, Angle2DFloat)](/documentation/spatial/angle2dfloat/-=(_:_:))
- [Comparable Implementations](/documentation/spatial/angle2dfloat/comparable-implementations)

#### Operators

- [static func < (Angle2DFloat, Angle2DFloat) -> Bool](/documentation/spatial/angle2dfloat/_(_:_:))
- [CustomReflectable Implementations](/documentation/spatial/angle2dfloat/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/angle2dfloat/custommirror)
- [Decodable Implementations](/documentation/spatial/angle2dfloat/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/angle2dfloat/init(from:))
- [Encodable Implementations](/documentation/spatial/angle2dfloat/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/angle2dfloat/encode(to:))
- [Equatable Implementations](/documentation/spatial/angle2dfloat/equatable-implementations)

#### Operators

- [static func == (Angle2DFloat, Angle2DFloat) -> Bool](/documentation/spatial/angle2dfloat/==(_:_:))
- [Hashable Implementations](/documentation/spatial/angle2dfloat/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/angle2dfloat/hash(into:))

## 3D primitives

- [Point3D](/documentation/spatial/point3d)

### Creating a 3D point structure

- [init()](/documentation/spatial/point3d/init())
- [init(x: Double, y: Double, z: Double)](/documentation/spatial/point3d/init(x:y:z:)-3lary)
- [init<T>(x: T, y: T, z: T)](/documentation/spatial/point3d/init(x:y:z:)-28jhw)
- [init(vector: simd_double3)](/documentation/spatial/point3d/init(vector:))
- [init(Size3D)](/documentation/spatial/point3d/init(_:)-1f1ha)
- [init(simd_float3)](/documentation/spatial/point3d/init(_:)-1kved)
- [init(Vector3D)](/documentation/spatial/point3d/init(_:)-34plj)
- [init(simd_double3)](/documentation/spatial/point3d/init(_:)-4gu20)
- [init(SphericalCoordinates3D)](/documentation/spatial/point3d/init(_:)-50tw4)

### Inspecting a 3D point’s properties

- [x](/documentation/spatial/point3d/x)
- [y](/documentation/spatial/point3d/y)
- [z](/documentation/spatial/point3d/z)
- [var vector: simd_double3](/documentation/spatial/point3d/vector)
- [var magnitudeSquared: Double](/documentation/spatial/point3d/magnitudesquared)

### Checking characteristics

- [func distance(to: Point3D) -> Double](/documentation/spatial/point3d/distance(to:))

### Transforming a 3D point structure

- [func applying(ScaledPose3D) -> Point3D](/documentation/spatial/point3d/applying(_:)-1f4em)
- [func applying(ScaledPose3D) -> Point3D](/documentation/spatial/point3d/applying(_:)-1f4em)
- [func applying(Pose3D) -> Point3D](/documentation/spatial/point3d/applying(_:)-7ulww)
- [func clamp(to: Rect3D)](/documentation/spatial/point3d/clamp(to:))
- [func scale(by: Double)](/documentation/spatial/point3d/scale(by:))
- [func rotated(by: Rotation3D, around: Point3D) -> Point3D](/documentation/spatial/point3d/rotated(by:around:)-4tmfq)
- [func rotated(by: simd_quatd, around: Point3D) -> Point3D](/documentation/spatial/point3d/rotated(by:around:)-chuy)
- [func unapplying(Pose3D) -> Point3D](/documentation/spatial/point3d/unapplying(_:)-5hk6t)
- [func unapplying(ScaledPose3D) -> Point3D](/documentation/spatial/point3d/unapplying(_:)-7wdtv)
- [func unapplying(ScaledPose3D) -> Point3D](/documentation/spatial/point3d/unapplying(_:)-7wdtv)

### Comparing values

- [static func == (Point3D, Point3D) -> Bool](/documentation/spatial/point3d/==(_:_:))
- [func isApproximatelyEqual(to: Point3D, tolerance: Double) -> Bool](/documentation/spatial/point3d/isapproximatelyequal(to:tolerance:))

### Applying arithmetic operations

- [static func * (Point3D, Double) -> Point3D](/documentation/spatial/point3d/*(_:_:)-9rqvh)
- [static func * (Double, Point3D) -> Point3D](/documentation/spatial/point3d/*(_:_:)-9w7dk)
- [static func * (AffineTransform3D, Point3D) -> Point3D](/documentation/spatial/point3d/*(_:_:)-8ewep)
- [static func * (ProjectiveTransform3D, Point3D) -> Point3D](/documentation/spatial/point3d/*(_:_:)-9ak06)
- [static func * (Pose3D, Point3D) -> Point3D](/documentation/spatial/point3d/*(_:_:)-8wgkb)
- [static func + (Point3D, Size3D) -> Point3D](/documentation/spatial/point3d/+(_:_:)-5v6x4)
- [static func + (Size3D, Point3D) -> Point3D](/documentation/spatial/point3d/+(_:_:)-4g55)
- [static func - (Point3D) -> Point3D](/documentation/spatial/point3d/-(_:))
- [static func - (Point3D, Size3D) -> Point3D](/documentation/spatial/point3d/-(_:_:)-6om9g)
- [static func - (Point3D, Point3D) -> Vector3D](/documentation/spatial/point3d/-(_:_:)-9l6rn)
- [static func - (Size3D, Point3D) -> Point3D](/documentation/spatial/point3d/-(_:_:)-5t01r)
- [static func += (inout Point3D, Vector3D)](/documentation/spatial/point3d/+=(_:_:)-80hjz)
- [static func += (inout Point3D, Size3D)](/documentation/spatial/point3d/+=(_:_:)-3v0zk)
- [static func -= (inout Point3D, Vector3D)](/documentation/spatial/point3d/-=(_:_:)-23bow)
- [static func -= (inout Point3D, Size3D)](/documentation/spatial/point3d/-=(_:_:)-9xu2)
- [static func *= (inout Point3D, Double)](/documentation/spatial/point3d/*=(_:_:))
- [static func / (Point3D, Double) -> Point3D](/documentation/spatial/point3d/_(_:_:))
- [static func /= (inout Point3D, Double)](/documentation/spatial/point3d/_=(_:_:))

### Deprecated symbols

- [func rotation(to: Point3D) -> Rotation3D](/documentation/spatial/point3d/rotation(to:))
- [var origin: Point3D](/documentation/spatial/point3d/origin)
- [var simd: simd_double3](/documentation/spatial/point3d/simd)

### Initializers

- [init(Point3DFloat)](/documentation/spatial/point3d/init(_:)-7wgtj)
- [init(simd_packed_double4)](/documentation/spatial/point3d/init(_:)-8r7om)

### Default Implementations

- [Animatable Implementations](/documentation/spatial/point3d/animatable-implementations)

#### Instance Properties

- [var animatableData: Vector3D](/documentation/spatial/point3d/animatabledata)
- [ClampableWithinRectProtocol Implementations](/documentation/spatial/point3d/clampablewithinrectprotocol-implementations)

#### Instance Methods

- [func clamp(to: Rect3D)](/documentation/spatial/point3d/clamp(to:))
- [CustomReflectable Implementations](/documentation/spatial/point3d/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/point3d/custommirror)
- [Decodable Implementations](/documentation/spatial/point3d/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/point3d/init(from:))
- [Encodable Implementations](/documentation/spatial/point3d/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/point3d/encode(to:))
- [Equatable Implementations](/documentation/spatial/point3d/equatable-implementations)

#### Operators

- [static func == (Point3D, Point3D) -> Bool](/documentation/spatial/point3d/==(_:_:))
- [Hashable Implementations](/documentation/spatial/point3d/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/point3d/hash(into:))
- [Primitive3D Implementations](/documentation/spatial/point3d/primitive3d-implementations)

#### Instance Methods

- [func applying(Pose3D) -> Point3D](/documentation/spatial/point3d/applying(_:)-7ulww)
- [func unapplying(Pose3D) -> Point3D](/documentation/spatial/point3d/unapplying(_:)-5hk6t)
- [Point3DFloat](/documentation/spatial/point3dfloat)

### Operators

- [static func * (Pose3DFloat, Point3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/*(_:_:)-1r8dj)
- [static func * (ProjectiveTransform3DFloat, Point3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/*(_:_:)-22247)
- [static func * (AffineTransform3DFloat, Point3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/*(_:_:)-3doxu)
- [static func * (Float, Point3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/*(_:_:)-5k7wl)
- [static func * (Point3DFloat, Float) -> Point3DFloat](/documentation/spatial/point3dfloat/*(_:_:)-8ug4a)
- [static func *= (inout Point3DFloat, Float)](/documentation/spatial/point3dfloat/*=(_:_:))
- [static func + (Size3DFloat, Point3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/+(_:_:)-1t1gn)
- [static func + (Point3DFloat, Size3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/+(_:_:)-6ihv8)
- [static func += (inout Point3DFloat, Vector3DFloat)](/documentation/spatial/point3dfloat/+=(_:_:)-1x97i)
- [static func += (inout Point3DFloat, Size3DFloat)](/documentation/spatial/point3dfloat/+=(_:_:)-83599)
- [static func - (Point3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/-(_:))
- [static func - (Size3DFloat, Point3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/-(_:_:)-46bqa)
- [static func - (Point3DFloat, Point3DFloat) -> Vector3DFloat](/documentation/spatial/point3dfloat/-(_:_:)-5jrc)
- [static func - (Point3DFloat, Size3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/-(_:_:)-5rz8s)
- [static func -= (inout Point3DFloat, Size3DFloat)](/documentation/spatial/point3dfloat/-=(_:_:)-7r1d1)
- [static func -= (inout Point3DFloat, Vector3DFloat)](/documentation/spatial/point3dfloat/-=(_:_:)-8fp0l)
- [static func / (Point3DFloat, Float) -> Point3DFloat](/documentation/spatial/point3dfloat/_(_:_:))
- [static func /= (inout Point3DFloat, Float)](/documentation/spatial/point3dfloat/_=(_:_:))

### Initializers

- [init()](/documentation/spatial/point3dfloat/init())
- [init(Size3DFloat)](/documentation/spatial/point3dfloat/init(_:)-1h5vt)
- [init(Vector3DFloat)](/documentation/spatial/point3dfloat/init(_:)-4sdjs)
- [init(simd_packed_float4)](/documentation/spatial/point3dfloat/init(_:)-4uwq7)
- [init(simd_double3)](/documentation/spatial/point3dfloat/init(_:)-5fcqk)
- [init(Point3D)](/documentation/spatial/point3dfloat/init(_:)-5g1ob)
- [init(SphericalCoordinates3DFloat)](/documentation/spatial/point3dfloat/init(_:)-8c02t)
- [init(simd_float3)](/documentation/spatial/point3dfloat/init(_:)-8dj77)
- [init(vector: simd_float3)](/documentation/spatial/point3dfloat/init(vector:))
- [init<T>(x: T, y: T, z: T)](/documentation/spatial/point3dfloat/init(x:y:z:)-3hzkg)
- [init(x: Float, y: Float, z: Float)](/documentation/spatial/point3dfloat/init(x:y:z:)-59uqs)

### Instance Properties

- [var vector: simd_float3](/documentation/spatial/point3dfloat/vector)
- [var x: Float](/documentation/spatial/point3dfloat/x)
- [var y: Float](/documentation/spatial/point3dfloat/y)
- [var z: Float](/documentation/spatial/point3dfloat/z)

### Instance Methods

- [func applying(ScaledPose3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/applying(_:)-2dhmf)
- [func distance(to: Point3DFloat) -> Float](/documentation/spatial/point3dfloat/distance(to:))
- [func isApproximatelyEqual(to: Point3DFloat, tolerance: Float) -> Bool](/documentation/spatial/point3dfloat/isapproximatelyequal(to:tolerance:))
- [func rotated(by: simd_quatf, around: Point3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/rotated(by:around:)-1ejmw)
- [func rotated(by: Rotation3DFloat, around: Point3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/rotated(by:around:)-5xwwi)
- [func unapplying(ScaledPose3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/unapplying(_:)-93yzx)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/point3dfloat/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/point3dfloat/custommirror)
- [Decodable Implementations](/documentation/spatial/point3dfloat/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/point3dfloat/init(from:))
- [Encodable Implementations](/documentation/spatial/point3dfloat/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/point3dfloat/encode(to:))
- [Equatable Implementations](/documentation/spatial/point3dfloat/equatable-implementations)

#### Operators

- [static func == (Point3DFloat, Point3DFloat) -> Bool](/documentation/spatial/point3dfloat/==(_:_:))
- [Hashable Implementations](/documentation/spatial/point3dfloat/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/point3dfloat/hash(into:))
- [Primitive3DProtocol Implementations](/documentation/spatial/point3dfloat/primitive3dprotocol-implementations)

#### Instance Methods

- [func applying(Pose3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/applying(_:)-q5w)
- [func unapplying(Pose3DFloat) -> Point3DFloat](/documentation/spatial/point3dfloat/unapplying(_:)-16e4o)
- [Size3D](/documentation/spatial/size3d)

### Creating a 3D size structure

- [init()](/documentation/spatial/size3d/init())
- [init(width: Double, height: Double, depth: Double)](/documentation/spatial/size3d/init(width:height:depth:)-4j9bk)
- [init<T>(width: T, height: T, depth: T)](/documentation/spatial/size3d/init(width:height:depth:)-4kscw)
- [init(simd_float3)](/documentation/spatial/size3d/init(_:)-2ibhr)
- [init(simd_double3)](/documentation/spatial/size3d/init(_:)-3y7nr)
- [init(vector: simd_double3)](/documentation/spatial/size3d/init(vector:))
- [init(Point3D)](/documentation/spatial/size3d/init(_:)-7kyp0)
- [init(Vector3D)](/documentation/spatial/size3d/init(_:)-6nss1)

### Inspecting a 3D size’s properties

- [width](/documentation/spatial/size3d/width)
- [height](/documentation/spatial/size3d/height)
- [depth](/documentation/spatial/size3d/depth)
- [var size: Size3D](/documentation/spatial/size3d/size)
- [var vector: simd_double3](/documentation/spatial/size3d/vector)

### Transforming a 3D size structure

- [func applying(Pose3D) -> Size3D](/documentation/spatial/size3d/applying(_:)-85mlm)
- [func applying(ScaledPose3D) -> Size3D](/documentation/spatial/size3d/applying(_:)-7e2pf)
- [func applying(Pose3D) -> Size3D](/documentation/spatial/size3d/applying(_:)-85mlm)
- [func unapplying(AffineTransform3D) -> Size3D](/documentation/spatial/size3d/unapplying(_:)-7qam3)
- [func unapplying(ProjectiveTransform3D) -> Size3D](/documentation/spatial/size3d/unapplying(_:)-yock)
- [func unapplying(Pose3D) -> Size3D](/documentation/spatial/size3d/unapplying(_:)-3ip2e)
- [func sheared(AxisWithFactors) -> Size3D](/documentation/spatial/size3d/sheared(_:))
- [func applying(ScaledPose3D) -> Size3D](/documentation/spatial/size3d/applying(_:)-7e2pf)
- [func unapplying(ScaledPose3D) -> Size3D](/documentation/spatial/size3d/unapplying(_:)-42rsa)

### Checking characteristics

- [func contains(anyOf: [Point3D]) -> Bool](/documentation/spatial/size3d/contains(anyof:))

### Creating derived 3D sizes

- [func intersection(Size3D) -> Size3D?](/documentation/spatial/size3d/intersection(_:))

### Comparing values

- [static func == (Size3D, Size3D) -> Bool](/documentation/spatial/size3d/==(_:_:))

### 3D size constants

- [static let one: Size3D](/documentation/spatial/size3d/one)

### Applying arithmetic operations

- [static func * (Size3D, Double) -> Size3D](/documentation/spatial/size3d/*(_:_:)-751dt)
- [static func * (Double, Size3D) -> Size3D](/documentation/spatial/size3d/*(_:_:)-8zb5j)
- [static func * (AffineTransform3D, Size3D) -> Size3D](/documentation/spatial/size3d/*(_:_:)-4qpgt)
- [static func * (ProjectiveTransform3D, Size3D) -> Size3D](/documentation/spatial/size3d/*(_:_:)-52miz)
- [static func * (Pose3D, Size3D) -> Size3D](/documentation/spatial/size3d/*(_:_:)-5bb1n)
- [static func + (Size3D, Size3D) -> Size3D](/documentation/spatial/size3d/+(_:_:))
- [static func - (Size3D) -> Size3D](/documentation/spatial/size3d/-(_:))
- [static func - (Size3D, Size3D) -> Size3D](/documentation/spatial/size3d/-(_:_:))
- [static func *= (inout Size3D, Double)](/documentation/spatial/size3d/*=(_:_:))
- [static func += (inout Size3D, Size3D)](/documentation/spatial/size3d/+=(_:_:)-75tn3)
- [static func += (inout Size3D, Vector3D)](/documentation/spatial/size3d/+=(_:_:)-7yrej)
- [static func -= (inout Size3D, Size3D)](/documentation/spatial/size3d/-=(_:_:)-8t5kg)
- [static func -= (inout Size3D, Vector3D)](/documentation/spatial/size3d/-=(_:_:)-3te52)
- [static func / (Size3D, Double) -> Size3D](/documentation/spatial/size3d/_(_:_:))
- [static func /= (inout Size3D, Double)](/documentation/spatial/size3d/_=(_:_:))

### Deprecated symbols

- [var simd: simd_double3](/documentation/spatial/size3d/simd)
- [func containsAny(of: [Point3D]) -> Bool](/documentation/spatial/size3d/containsany(of:))

### Initializers

- [init(simd_packed_double4)](/documentation/spatial/size3d/init(_:)-25dft)
- [init(Size3DFloat)](/documentation/spatial/size3d/init(_:)-2jfoh)

### Default Implementations

- [AdditiveArithmetic Implementations](/documentation/spatial/size3d/additivearithmetic-implementations)

#### Operators

- [static func + (Size3D, Size3D) -> Size3D](/documentation/spatial/size3d/+(_:_:))
- [static func += (inout Size3D, Size3D)](/documentation/spatial/size3d/+=(_:_:)-75tn3)
- [static func - (Size3D, Size3D) -> Size3D](/documentation/spatial/size3d/-(_:_:))
- [static func -= (inout Size3D, Size3D)](/documentation/spatial/size3d/-=(_:_:)-8t5kg)
- [CustomReflectable Implementations](/documentation/spatial/size3d/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/size3d/custommirror)
- [Decodable Implementations](/documentation/spatial/size3d/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/size3d/init(from:))
- [Encodable Implementations](/documentation/spatial/size3d/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/size3d/encode(to:))
- [Equatable Implementations](/documentation/spatial/size3d/equatable-implementations)

#### Operators

- [static func == (Size3D, Size3D) -> Bool](/documentation/spatial/size3d/==(_:_:))
- [Hashable Implementations](/documentation/spatial/size3d/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/size3d/hash(into:))
- [Primitive3DProtocol Implementations](/documentation/spatial/size3d/primitive3dprotocol-implementations)

#### Instance Methods

- [func applying(Pose3D) -> Size3D](/documentation/spatial/size3d/applying(_:)-85mlm)
- [func unapplying(Pose3D) -> Size3D](/documentation/spatial/size3d/unapplying(_:)-3ip2e)
- [func unapplying(AffineTransform3D) -> Size3D](/documentation/spatial/size3d/unapplying(_:)-7qam3)
- [func unapplying(ProjectiveTransform3D) -> Size3D](/documentation/spatial/size3d/unapplying(_:)-yock)
- [Scalable3DProtocol Implementations](/documentation/spatial/size3d/scalable3dprotocol-implementations)

#### Instance Methods

- [func scaledBy(x: Double, y: Double, z: Double) -> Size3D](/documentation/spatial/size3d/scaledby(x:y:z:))
- [Shearable3D Implementations](/documentation/spatial/size3d/shearable3d-implementations)

#### Instance Methods

- [func sheared(AxisWithFactors) -> Size3D](/documentation/spatial/size3d/sheared(_:))
- [Volumetric Implementations](/documentation/spatial/size3d/volumetric-implementations)

#### Instance Methods

- [func containsAny(of: [Point3D]) -> Bool](/documentation/spatial/size3d/containsany(of:))
- [VolumetricProtocol Implementations](/documentation/spatial/size3d/volumetricprotocol-implementations)

#### Instance Properties

- [var size: Size3D](/documentation/spatial/size3d/size)

#### Instance Methods

- [func contains(anyOf: [Point3D]) -> Bool](/documentation/spatial/size3d/contains(anyof:))
- [func intersection(Size3D) -> Size3D?](/documentation/spatial/size3d/intersection(_:))
- [Size3DFloat](/documentation/spatial/size3dfloat)

### Operators

- [static func * (Float, Size3DFloat) -> Size3DFloat](/documentation/spatial/size3dfloat/*(_:_:)-124fk)
- [static func * (Size3DFloat, Float) -> Size3DFloat](/documentation/spatial/size3dfloat/*(_:_:)-544n3)
- [static func * (ProjectiveTransform3DFloat, Size3DFloat) -> Size3DFloat](/documentation/spatial/size3dfloat/*(_:_:)-57yj1)
- [static func * (Pose3DFloat, Size3DFloat) -> Size3DFloat](/documentation/spatial/size3dfloat/*(_:_:)-61lpp)
- [static func * (AffineTransform3DFloat, Size3DFloat) -> Size3DFloat](/documentation/spatial/size3dfloat/*(_:_:)-7txph)
- [static func *= (inout Size3DFloat, Float)](/documentation/spatial/size3dfloat/*=(_:_:))
- [static func += (inout Size3DFloat, Vector3DFloat)](/documentation/spatial/size3dfloat/+=(_:_:)-6yxe6)
- [static func - (Size3DFloat) -> Size3DFloat](/documentation/spatial/size3dfloat/-(_:))
- [static func -= (inout Size3DFloat, Vector3DFloat)](/documentation/spatial/size3dfloat/-=(_:_:)-4iec2)
- [static func / (Size3DFloat, Float) -> Size3DFloat](/documentation/spatial/size3dfloat/_(_:_:))
- [static func /= (inout Size3DFloat, Float)](/documentation/spatial/size3dfloat/_=(_:_:))

### Initializers

- [init()](/documentation/spatial/size3dfloat/init())
- [init(simd_float3)](/documentation/spatial/size3dfloat/init(_:)-208lc)
- [init(Vector3DFloat)](/documentation/spatial/size3dfloat/init(_:)-3z2u6)
- [init(Point3DFloat)](/documentation/spatial/size3dfloat/init(_:)-4eoby)
- [init(Size3D)](/documentation/spatial/size3dfloat/init(_:)-4r1ha)
- [init(simd_double3)](/documentation/spatial/size3dfloat/init(_:)-6y249)
- [init(simd_packed_float4)](/documentation/spatial/size3dfloat/init(_:)-8nzza)
- [init(vector: simd_float3)](/documentation/spatial/size3dfloat/init(vector:))
- [init<T>(width: T, height: T, depth: T)](/documentation/spatial/size3dfloat/init(width:height:depth:)-8h26f)
- [init(width: Float, height: Float, depth: Float)](/documentation/spatial/size3dfloat/init(width:height:depth:)-9u3g4)

### Instance Properties

- [var depth: Float](/documentation/spatial/size3dfloat/depth)
- [var height: Float](/documentation/spatial/size3dfloat/height)
- [var vector: simd_float3](/documentation/spatial/size3dfloat/vector)
- [var width: Float](/documentation/spatial/size3dfloat/width)

### Instance Methods

- [func applying(ScaledPose3DFloat) -> Size3DFloat](/documentation/spatial/size3dfloat/applying(_:)-4x5w1)
- [func sheared(AxisWithFactors) -> Size3DFloat](/documentation/spatial/size3dfloat/sheared(_:))
- [func unapplying(ScaledPose3DFloat) -> Size3DFloat](/documentation/spatial/size3dfloat/unapplying(_:)-9dyaz)

### Type Properties

- [static let one: Size3DFloat](/documentation/spatial/size3dfloat/one)

### Default Implementations

- [AdditiveArithmetic Implementations](/documentation/spatial/size3dfloat/additivearithmetic-implementations)

#### Operators

- [static func + (Size3DFloat, Size3DFloat) -> Size3DFloat](/documentation/spatial/size3dfloat/+(_:_:))
- [static func += (inout Size3DFloat, Size3DFloat)](/documentation/spatial/size3dfloat/+=(_:_:)-7eiud)
- [static func - (Size3DFloat, Size3DFloat) -> Size3DFloat](/documentation/spatial/size3dfloat/-(_:_:))
- [static func -= (inout Size3DFloat, Size3DFloat)](/documentation/spatial/size3dfloat/-=(_:_:)-9s57n)
- [CustomReflectable Implementations](/documentation/spatial/size3dfloat/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/size3dfloat/custommirror)
- [Decodable Implementations](/documentation/spatial/size3dfloat/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/size3dfloat/init(from:))
- [Encodable Implementations](/documentation/spatial/size3dfloat/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/size3dfloat/encode(to:))
- [Equatable Implementations](/documentation/spatial/size3dfloat/equatable-implementations)

#### Operators

- [static func == (Size3DFloat, Size3DFloat) -> Bool](/documentation/spatial/size3dfloat/==(_:_:))
- [Hashable Implementations](/documentation/spatial/size3dfloat/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/size3dfloat/hash(into:))
- [Primitive3DProtocol Implementations](/documentation/spatial/size3dfloat/primitive3dprotocol-implementations)

#### Instance Methods

- [func applying(Pose3DFloat) -> Size3DFloat](/documentation/spatial/size3dfloat/applying(_:)-44ilq)
- [func unapplying(Pose3DFloat) -> Size3DFloat](/documentation/spatial/size3dfloat/unapplying(_:)-1jw2r)
- [func unapplying(AffineTransform3DFloat) -> Size3DFloat](/documentation/spatial/size3dfloat/unapplying(_:)-2tlsj)
- [func unapplying(ProjectiveTransform3DFloat) -> Size3DFloat](/documentation/spatial/size3dfloat/unapplying(_:)-6i1g6)
- [Scalable3DProtocol Implementations](/documentation/spatial/size3dfloat/scalable3dprotocol-implementations)

#### Instance Methods

- [func scaledBy(x: Float, y: Float, z: Float) -> Size3DFloat](/documentation/spatial/size3dfloat/scaledby(x:y:z:))
- [VolumetricProtocol Implementations](/documentation/spatial/size3dfloat/volumetricprotocol-implementations)

#### Instance Properties

- [var size: Size3DFloat](/documentation/spatial/size3dfloat/size)

#### Instance Methods

- [func contains(anyOf: [Point3DFloat]) -> Bool](/documentation/spatial/size3dfloat/contains(anyof:))
- [func intersection(Size3DFloat) -> Size3DFloat?](/documentation/spatial/size3dfloat/intersection(_:))
- [Rect3D](/documentation/spatial/rect3d)

### Creating a 3D rectangle structure

- [init()](/documentation/spatial/rect3d/init())
- [init(center: Point3D, size: Size3D)](/documentation/spatial/rect3d/init(center:size:)-133fy)
- [init(center: simd_double3, size: simd_double3)](/documentation/spatial/rect3d/init(center:size:)-77l0z)
- [init(center: Vector3D, size: Vector3D)](/documentation/spatial/rect3d/init(center:size:)-9cfq7)
- [init(center: simd_float3, size: simd_float3)](/documentation/spatial/rect3d/init(center:size:)-zr2x)
- [init(origin: simd_double3, size: simd_double3)](/documentation/spatial/rect3d/init(origin:size:)-5xyrs)
- [init(origin: simd_float3, size: simd_float3)](/documentation/spatial/rect3d/init(origin:size:)-7fnuf)
- [init(origin: Vector3D, size: Vector3D)](/documentation/spatial/rect3d/init(origin:size:)-7o8ad)
- [init(origin: Point3D, size: Size3D)](/documentation/spatial/rect3d/init(origin:size:)-7v73)
- [init(origin: Point3D, size: Size3D)](/documentation/spatial/rect3d/init(origin:size:)-9a089)
- [init(points: [Point3D])](/documentation/spatial/rect3d/init(points:))

### Inspecting a 3D rectangle’s properties

- [var center: Point3D](/documentation/spatial/rect3d/center)
- [var cornerPoints: [Point3D]](/documentation/spatial/rect3d/cornerpoints)
- [var max: Point3D](/documentation/spatial/rect3d/max)
- [var min: Point3D](/documentation/spatial/rect3d/min)
- [var origin: Point3D](/documentation/spatial/rect3d/origin)

### Transforming a 3D rectangle structure

- [func applying(Pose3D) -> Rect3D](/documentation/spatial/rect3d/applying(_:)-3qdiy)
- [func applying(ScaledPose3D) -> Rect3D](/documentation/spatial/rect3d/applying(_:)-5hnif)
- [func applying(ScaledPose3D) -> Rect3D](/documentation/spatial/rect3d/applying(_:)-5hnif)
- [func rotated(by: Rotation3D, around: Point3D) -> Rect3D](/documentation/spatial/rect3d/rotated(by:around:)-3ih62)
- [func rotated(by: simd_quatd, around: Point3D) -> Rect3D](/documentation/spatial/rect3d/rotated(by:around:)-8g1c9)
- [func scaledBy(x: Double, y: Double, z: Double) -> Rect3D](/documentation/spatial/rect3d/scaledby(x:y:z:))
- [func sheared(AxisWithFactors) -> Rect3D](/documentation/spatial/rect3d/sheared(_:))
- [func unapplying(ProjectiveTransform3D) -> Rect3D](/documentation/spatial/rect3d/unapplying(_:)-1j6g7)
- [func unapplying(ScaledPose3D) -> Rect3D](/documentation/spatial/rect3d/unapplying(_:)-1pbfn)
- [func unapplying(Pose3D) -> Rect3D](/documentation/spatial/rect3d/unapplying(_:)-2he5i)
- [func unapplying(AffineTransform3D) -> Rect3D](/documentation/spatial/rect3d/unapplying(_:)-7eglq)

### Checking characteristics

- [func contains(anyOf: [Point3D]) -> Bool](/documentation/spatial/rect3d/contains(anyof:))
- [func intersects(Rect3D) -> Bool](/documentation/spatial/rect3d/intersects(_:))
- [var isEmpty: Bool](/documentation/spatial/rect3d/isempty)

### Creating derived 3D rectangles

- [var integral: Rect3D](/documentation/spatial/rect3d/integral)
- [func formInset(by: Size3D)](/documentation/spatial/rect3d/forminset(by:))
- [func inset(by: Size3D) -> Rect3D](/documentation/spatial/rect3d/inset(by:))
- [func intersection(Rect3D) -> Rect3D?](/documentation/spatial/rect3d/intersection(_:))
- [var standardized: Rect3D](/documentation/spatial/rect3d/standardized)

### Comparing values

- [static func == (Rect3D, Rect3D) -> Bool](/documentation/spatial/rect3d/==(_:_:))

### Applying arithmetic operations

- [static func * (AffineTransform3D, Rect3D) -> Rect3D](/documentation/spatial/rect3d/*(_:_:)-8710d)
- [static func * (ProjectiveTransform3D, Rect3D) -> Rect3D](/documentation/spatial/rect3d/*(_:_:)-8vu0)
- [static func * (Pose3D, Rect3D) -> Rect3D](/documentation/spatial/rect3d/*(_:_:)-5lqdv)

### Deprecated symbols

- [func distance(to: Rect3D) -> Double](/documentation/spatial/rect3d/distance(to:))
- [func containsAny(of: [Point3D]) -> Bool](/documentation/spatial/rect3d/containsany(of:))
- [func rotation(to: Rect3D) -> Rotation3D](/documentation/spatial/rect3d/rotation(to:))
- [var maxX: Double](/documentation/spatial/rect3d/maxx)
- [var maxY: Double](/documentation/spatial/rect3d/maxy)
- [var maxZ: Double](/documentation/spatial/rect3d/maxz)
- [var midX: Double](/documentation/spatial/rect3d/midx)
- [var midY: Double](/documentation/spatial/rect3d/midy)
- [var midZ: Double](/documentation/spatial/rect3d/midz)
- [var minX: Double](/documentation/spatial/rect3d/minx)
- [var minY: Double](/documentation/spatial/rect3d/miny)
- [var minZ: Double](/documentation/spatial/rect3d/minz)

### Initializers

- [init(Rect3DFloat)](/documentation/spatial/rect3d/init(_:)-3wm4y)
- [init(BoundingBox)](/documentation/spatial/rect3d/init(_:)-b16k)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/rect3d/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/rect3d/custommirror)
- [Decodable Implementations](/documentation/spatial/rect3d/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/rect3d/init(from:))
- [Encodable Implementations](/documentation/spatial/rect3d/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/rect3d/encode(to:))
- [Equatable Implementations](/documentation/spatial/rect3d/equatable-implementations)

#### Operators

- [static func == (Rect3D, Rect3D) -> Bool](/documentation/spatial/rect3d/==(_:_:))
- [Hashable Implementations](/documentation/spatial/rect3d/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/rect3d/hash(into:))
- [Primitive3DProtocol Implementations](/documentation/spatial/rect3d/primitive3dprotocol-implementations)

#### Instance Methods

- [func applying(Pose3D) -> Rect3D](/documentation/spatial/rect3d/applying(_:)-3qdiy)
- [func unapplying(ProjectiveTransform3D) -> Rect3D](/documentation/spatial/rect3d/unapplying(_:)-1j6g7)
- [func unapplying(Pose3D) -> Rect3D](/documentation/spatial/rect3d/unapplying(_:)-2he5i)
- [func unapplying(AffineTransform3D) -> Rect3D](/documentation/spatial/rect3d/unapplying(_:)-7eglq)
- [Scalable3DProtocol Implementations](/documentation/spatial/rect3d/scalable3dprotocol-implementations)

#### Instance Methods

- [func scaledBy(x: Double, y: Double, z: Double) -> Rect3D](/documentation/spatial/rect3d/scaledby(x:y:z:))
- [Shearable3D Implementations](/documentation/spatial/rect3d/shearable3d-implementations)

#### Instance Methods

- [func sheared(AxisWithFactors) -> Rect3D](/documentation/spatial/rect3d/sheared(_:))
- [Volumetric Implementations](/documentation/spatial/rect3d/volumetric-implementations)

#### Instance Methods

- [func containsAny(of: [Point3D]) -> Bool](/documentation/spatial/rect3d/containsany(of:))
- [VolumetricProtocol Implementations](/documentation/spatial/rect3d/volumetricprotocol-implementations)

#### Instance Methods

- [func contains(anyOf: [Point3D]) -> Bool](/documentation/spatial/rect3d/contains(anyof:))
- [func intersection(Rect3D) -> Rect3D?](/documentation/spatial/rect3d/intersection(_:))
- [Rect3DFloat](/documentation/spatial/rect3dfloat)

### Operators

- [static func * (ProjectiveTransform3DFloat, Rect3DFloat) -> Rect3DFloat](/documentation/spatial/rect3dfloat/*(_:_:)-1iaiz)
- [static func * (Pose3DFloat, Rect3DFloat) -> Rect3DFloat](/documentation/spatial/rect3dfloat/*(_:_:)-1xai0)
- [static func * (AffineTransform3DFloat, Rect3DFloat) -> Rect3DFloat](/documentation/spatial/rect3dfloat/*(_:_:)-2fdne)

### Initializers

- [init()](/documentation/spatial/rect3dfloat/init())
- [init(Rect3D)](/documentation/spatial/rect3dfloat/init(_:))
- [init(center: simd_double3, size: simd_double3)](/documentation/spatial/rect3dfloat/init(center:size:)-1gsbj)
- [init(center: simd_float3, size: simd_float3)](/documentation/spatial/rect3dfloat/init(center:size:)-2c8oz)
- [init(center: Vector3DFloat, size: Vector3DFloat)](/documentation/spatial/rect3dfloat/init(center:size:)-92ay9)
- [init(center: Point3DFloat, size: Size3DFloat)](/documentation/spatial/rect3dfloat/init(center:size:)-e8la)
- [init(origin: simd_float3, size: simd_float3)](/documentation/spatial/rect3dfloat/init(origin:size:)-27)
- [init(origin: Point3DFloat, size: Size3DFloat)](/documentation/spatial/rect3dfloat/init(origin:size:)-8tqau)
- [init(origin: Point3DFloat, size: Size3DFloat)](/documentation/spatial/rect3dfloat/init(origin:size:)-9his9)
- [init(origin: simd_double3, size: simd_double3)](/documentation/spatial/rect3dfloat/init(origin:size:)-uw6h)
- [init(origin: Vector3DFloat, size: Vector3DFloat)](/documentation/spatial/rect3dfloat/init(origin:size:)-ywzp)
- [init(points: [Point3DFloat])](/documentation/spatial/rect3dfloat/init(points:))

### Instance Properties

- [var center: Point3DFloat](/documentation/spatial/rect3dfloat/center)
- [var cornerPoints: [Point3DFloat]](/documentation/spatial/rect3dfloat/cornerpoints)
- [var integral: Rect3DFloat](/documentation/spatial/rect3dfloat/integral)
- [var isEmpty: Bool](/documentation/spatial/rect3dfloat/isempty)
- [var isNull: Bool](/documentation/spatial/rect3dfloat/isnull)
- [var max: Point3DFloat](/documentation/spatial/rect3dfloat/max)
- [var min: Point3DFloat](/documentation/spatial/rect3dfloat/min)
- [var origin: Point3DFloat](/documentation/spatial/rect3dfloat/origin)
- [var standardized: Rect3DFloat](/documentation/spatial/rect3dfloat/standardized)

### Instance Methods

- [func applying(ScaledPose3DFloat) -> Rect3DFloat](/documentation/spatial/rect3dfloat/applying(_:)-7i8x5)
- [func formInset(by: Size3DFloat)](/documentation/spatial/rect3dfloat/forminset(by:))
- [func inset(by: Size3DFloat) -> Rect3DFloat](/documentation/spatial/rect3dfloat/inset(by:))
- [func intersects(Rect3DFloat) -> Bool](/documentation/spatial/rect3dfloat/intersects(_:))
- [func rotated(by: Rotation3DFloat, around: Point3DFloat) -> Rect3DFloat](/documentation/spatial/rect3dfloat/rotated(by:around:)-1g90c)
- [func rotated(by: simd_quatf, around: Point3DFloat) -> Rect3DFloat](/documentation/spatial/rect3dfloat/rotated(by:around:)-9yw64)
- [func sheared(AxisWithFactors) -> Rect3DFloat](/documentation/spatial/rect3dfloat/sheared(_:))
- [func unapplying(ScaledPose3DFloat) -> Rect3DFloat](/documentation/spatial/rect3dfloat/unapplying(_:)-4dm1d)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/rect3dfloat/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/rect3dfloat/custommirror)
- [Decodable Implementations](/documentation/spatial/rect3dfloat/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/rect3dfloat/init(from:))
- [Encodable Implementations](/documentation/spatial/rect3dfloat/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/rect3dfloat/encode(to:))
- [Equatable Implementations](/documentation/spatial/rect3dfloat/equatable-implementations)

#### Operators

- [static func == (Rect3DFloat, Rect3DFloat) -> Bool](/documentation/spatial/rect3dfloat/==(_:_:))
- [Hashable Implementations](/documentation/spatial/rect3dfloat/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/rect3dfloat/hash(into:))
- [Primitive3DProtocol Implementations](/documentation/spatial/rect3dfloat/primitive3dprotocol-implementations)

#### Instance Methods

- [func applying(Pose3DFloat) -> Rect3DFloat](/documentation/spatial/rect3dfloat/applying(_:)-9tknk)
- [func unapplying(ProjectiveTransform3DFloat) -> Rect3DFloat](/documentation/spatial/rect3dfloat/unapplying(_:)-31d5i)
- [func unapplying(AffineTransform3DFloat) -> Rect3DFloat](/documentation/spatial/rect3dfloat/unapplying(_:)-32dls)
- [func unapplying(Pose3DFloat) -> Rect3DFloat](/documentation/spatial/rect3dfloat/unapplying(_:)-7w0uc)
- [Scalable3DProtocol Implementations](/documentation/spatial/rect3dfloat/scalable3dprotocol-implementations)

#### Instance Methods

- [func scaledBy(x: Float, y: Float, z: Float) -> Rect3DFloat](/documentation/spatial/rect3dfloat/scaledby(x:y:z:))
- [VolumetricProtocol Implementations](/documentation/spatial/rect3dfloat/volumetricprotocol-implementations)

#### Instance Methods

- [func contains(anyOf: [Point3DFloat]) -> Bool](/documentation/spatial/rect3dfloat/contains(anyof:))
- [func intersection(Rect3DFloat) -> Rect3DFloat?](/documentation/spatial/rect3dfloat/intersection(_:))
- [Rotation3D](/documentation/spatial/rotation3d)

### Creating a 3D rotation structure

- [init()](/documentation/spatial/rotation3d/init()-2uz53)
- [init()](/documentation/spatial/rotation3d/init()-krpj)
- [init(eulerAngles: EulerAngles)](/documentation/spatial/rotation3d/init(eulerangles:))
- [init(eulerAngles: EulerAngles)](/documentation/spatial/rotation3d/init(eulerangles:))
- [EulerAngles](/documentation/spatial/eulerangles)

#### Initializers

- [init()](/documentation/spatial/eulerangles/init())
- [init(angles: simd_float3, order: EulerAngles.Order)](/documentation/spatial/eulerangles/init(angles:order:)-44rv1)
- [init(angles: simd_double3, order: __SPEulerAngleOrder)](/documentation/spatial/eulerangles/init(angles:order:)-93mu1)
- [init(x: Angle2D, y: Angle2D, z: Angle2D, order: EulerAngles.Order)](/documentation/spatial/eulerangles/init(x:y:z:order:))
- [init(Angle2D, Angle2D, Angle2D, order: EulerAngles.Order)](/documentation/spatial/eulerangles/init(_:_:_:order:))

#### Instance properties

- [var angles: simd_double3](/documentation/spatial/eulerangles/angles)
- [var order: __SPEulerAngleOrder](/documentation/spatial/eulerangles/order-swift.property)
- [var angles: simd_double3](/documentation/spatial/eulerangles/angles)
- [var order: __SPEulerAngleOrder](/documentation/spatial/eulerangles/order-swift.property)

#### Supporting types

- [EulerAngles.Order](/documentation/spatial/eulerangles/order-swift.typealias)
- [init(quaternion: simd_quatd)](/documentation/spatial/rotation3d/init(quaternion:)-2c79y)
- [init(simd_quatd)](/documentation/spatial/rotation3d/init(_:)-8z2bn)
- [init(simd_quatf)](/documentation/spatial/rotation3d/init(_:)-829qb)
- [init(angle: Angle2D, axis: RotationAxis3D)](/documentation/spatial/rotation3d/init(angle:axis:))
- [init(position: Point3D, target: Point3D, up: Vector3D)](/documentation/spatial/rotation3d/init(position:target:up:))
- [init(forward: Vector3D)](/documentation/spatial/rotation3d/init(forward:))
- [init(forward: Vector3D, up: Vector3D)](/documentation/spatial/rotation3d/init(forward:up:))
- [init(forward: Vector3D, up: Vector3D)](/documentation/spatial/rotation3d/init(forward:up:))

### Inspecting a 3D rotation’s properties

- [var angle: Angle2D](/documentation/spatial/rotation3d/angle)
- [var axis: RotationAxis3D](/documentation/spatial/rotation3d/axis)
- [func eulerAngles(order: __SPEulerAngleOrder) -> EulerAngles](/documentation/spatial/rotation3d/eulerangles(order:))
- [EulerAngles](/documentation/spatial/eulerangles)

#### Initializers

- [init()](/documentation/spatial/eulerangles/init())
- [init(angles: simd_float3, order: EulerAngles.Order)](/documentation/spatial/eulerangles/init(angles:order:)-44rv1)
- [init(angles: simd_double3, order: __SPEulerAngleOrder)](/documentation/spatial/eulerangles/init(angles:order:)-93mu1)
- [init(x: Angle2D, y: Angle2D, z: Angle2D, order: EulerAngles.Order)](/documentation/spatial/eulerangles/init(x:y:z:order:))
- [init(Angle2D, Angle2D, Angle2D, order: EulerAngles.Order)](/documentation/spatial/eulerangles/init(_:_:_:order:))

#### Instance properties

- [var angles: simd_double3](/documentation/spatial/eulerangles/angles)
- [var order: __SPEulerAngleOrder](/documentation/spatial/eulerangles/order-swift.property)
- [var angles: simd_double3](/documentation/spatial/eulerangles/angles)
- [var order: __SPEulerAngleOrder](/documentation/spatial/eulerangles/order-swift.property)

#### Supporting types

- [EulerAngles.Order](/documentation/spatial/eulerangles/order-swift.typealias)
- [var quaternion: simd_quatd](/documentation/spatial/rotation3d/quaternion)
- [vector](/documentation/spatial/rotation3d/vector)

### Transforming a 3D rotation structure

- [static func slerp(from: Rotation3D, to: Rotation3D, t: Double, along: Rotation3D.SlerpPath) -> Rotation3D](/documentation/spatial/rotation3d/slerp(from:to:t:along:))
- [Rotation3D.SlerpPath](/documentation/spatial/rotation3d/slerppath)

#### Enumeration Cases

- [case automatic](/documentation/spatial/rotation3d/slerppath/automatic)
- [case shortest](/documentation/spatial/rotation3d/slerppath/shortest)
- [case longest](/documentation/spatial/rotation3d/slerppath/longest)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/rotation3d/hash(into:))

#### Operator Functions

- [static func == (Rotation3D, Rotation3D) -> Bool](/documentation/spatial/rotation3d/==(_:_:))
- [var inverse: Rotation3D](/documentation/spatial/rotation3d/inverse)
- [static let identity: Rotation3D](/documentation/spatial/rotation3d/identity)

### Decomposing a 3D rotation structure

- [func swing(twistAxis: RotationAxis3D) -> Rotation3D](/documentation/spatial/rotation3d/swing(twistaxis:))
- [func twist(twistAxis: RotationAxis3D) -> Rotation3D](/documentation/spatial/rotation3d/twist(twistaxis:))
- [func swingTwist(twistAxis: RotationAxis3D) -> (swing: Rotation3D, twist: Rotation3D)](/documentation/spatial/rotation3d/swingtwist(twistaxis:))
- [func swing(twistAxis: RotationAxis3D) -> Rotation3D](/documentation/spatial/rotation3d/swing(twistaxis:))
- [func twist(twistAxis: RotationAxis3D) -> Rotation3D](/documentation/spatial/rotation3d/twist(twistaxis:))

### Checking characteristics

- [var isIdentity: Bool](/documentation/spatial/rotation3d/isidentity)
- [var isIdentity: Bool](/documentation/spatial/rotation3d/isidentity)

### Comparing values

- [func isApproximatelyEqual(to: Rotation3D, tolerance: Double) -> Bool](/documentation/spatial/rotation3d/isapproximatelyequal(to:tolerance:))
- [static func == (Rotation3D, Rotation3D) -> Bool](/documentation/spatial/rotation3d/==(_:_:))

### Applying arithmetic operations

- [static func * (Rotation3D, Rotation3D) -> Rotation3D](/documentation/spatial/rotation3d/*(_:_:)-1tc8f)
- [static func * (Rotation3D, Double) -> Rotation3D](/documentation/spatial/rotation3d/*(_:_:)-5dxqv)
- [static func * (Double, Rotation3D) -> Rotation3D](/documentation/spatial/rotation3d/*(_:_:)-9t389)
- [func * <T>(Rotation3D, T) -> T](/documentation/spatial/*(_:_:))
- [static func *= (inout Rotation3D, Rotation3D)](/documentation/spatial/rotation3d/*=(_:_:))

### Interpolating a 3D rotation structure

- [static func spline(leftEndpoint: Rotation3D, from: Rotation3D, to: Rotation3D, rightEndpoint: Rotation3D, t: Double) -> Rotation3D](/documentation/spatial/rotation3d/spline(leftendpoint:from:to:rightendpoint:t:))

### Deprecated symbols

- [init(Angle2D, Angle2D, Angle2D, order: EulerAngles.Order)](/documentation/spatial/eulerangles/init(_:_:_:order:))
- [init(eye: Point3D, target: Point3D, up: Vector3D)](/documentation/spatial/rotation3d/init(eye:target:up:))
- [init(axis: RotationAxis3D, angle: Angle2D)](/documentation/spatial/rotation3d/init(axis:angle:))
- [init(quaternion: simd_quatf)](/documentation/spatial/rotation3d/init(quaternion:)-6ajmn)
- [static let zero: Rotation3D](/documentation/spatial/rotation3d/zero)
- [var isZero: Bool](/documentation/spatial/rotation3d/iszero)

### Initializers

- [init(Rotation3DFloat)](/documentation/spatial/rotation3d/init(_:)-1r1iq)
- [init(simd_packed_double4)](/documentation/spatial/rotation3d/init(_:)-9yxln)
- [init(quaternion: simd_quatd)](/documentation/spatial/rotation3d/init(quaternion:)-500aq)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/rotation3d/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/rotation3d/custommirror)
- [Decodable Implementations](/documentation/spatial/rotation3d/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/rotation3d/init(from:))
- [Encodable Implementations](/documentation/spatial/rotation3d/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/rotation3d/encode(to:))
- [Equatable Implementations](/documentation/spatial/rotation3d/equatable-implementations)

#### Operators

- [static func == (Rotation3D, Rotation3D) -> Bool](/documentation/spatial/rotation3d/==(_:_:))
- [Hashable Implementations](/documentation/spatial/rotation3d/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/rotation3d/hash(into:))
- [Rotation3DFloat](/documentation/spatial/rotation3dfloat)

### Operators

- [static func * (Rotation3DFloat, Float) -> Rotation3DFloat](/documentation/spatial/rotation3dfloat/*(_:_:)-2mmaj)
- [static func * (Rotation3DFloat, Rotation3DFloat) -> Rotation3DFloat](/documentation/spatial/rotation3dfloat/*(_:_:)-30js8)
- [static func * (Float, Rotation3DFloat) -> Rotation3DFloat](/documentation/spatial/rotation3dfloat/*(_:_:)-99umr)
- [static func *= (inout Rotation3DFloat, Rotation3DFloat)](/documentation/spatial/rotation3dfloat/*=(_:_:))

### Initializers

- [init()](/documentation/spatial/rotation3dfloat/init()-4vjiv)
- [init()](/documentation/spatial/rotation3dfloat/init()-4y09q)
- [init(simd_quatf)](/documentation/spatial/rotation3dfloat/init(_:)-140am)
- [init(simd_quatd)](/documentation/spatial/rotation3dfloat/init(_:)-20sue)
- [init(Rotation3D)](/documentation/spatial/rotation3dfloat/init(_:)-5vfv0)
- [init(simd_packed_float4)](/documentation/spatial/rotation3dfloat/init(_:)-7mhwz)
- [init(angle: Angle2DFloat, axis: RotationAxis3DFloat)](/documentation/spatial/rotation3dfloat/init(angle:axis:))
- [init(eulerAngles: EulerAnglesFloat)](/documentation/spatial/rotation3dfloat/init(eulerangles:))
- [init(forward: Vector3DFloat)](/documentation/spatial/rotation3dfloat/init(forward:))
- [init(forward: Vector3DFloat, up: Vector3DFloat)](/documentation/spatial/rotation3dfloat/init(forward:up:))
- [init(position: Point3DFloat, target: Point3DFloat, up: Vector3DFloat)](/documentation/spatial/rotation3dfloat/init(position:target:up:))
- [init(quaternion: simd_quatf)](/documentation/spatial/rotation3dfloat/init(quaternion:))

### Instance Properties

- [var angle: Angle2DFloat](/documentation/spatial/rotation3dfloat/angle)
- [var axis: RotationAxis3DFloat](/documentation/spatial/rotation3dfloat/axis)
- [var inverse: Rotation3DFloat](/documentation/spatial/rotation3dfloat/inverse)
- [var isIdentity: Bool](/documentation/spatial/rotation3dfloat/isidentity)
- [var quaternion: simd_quatf](/documentation/spatial/rotation3dfloat/quaternion)
- [var vector: simd_float4](/documentation/spatial/rotation3dfloat/vector)

### Instance Methods

- [func eulerAngles(order: __SPEulerAngleOrder) -> EulerAnglesFloat](/documentation/spatial/rotation3dfloat/eulerangles(order:))
- [func isApproximatelyEqual(to: Rotation3DFloat, tolerance: Float) -> Bool](/documentation/spatial/rotation3dfloat/isapproximatelyequal(to:tolerance:))
- [func swing(twistAxis: RotationAxis3DFloat) -> Rotation3DFloat](/documentation/spatial/rotation3dfloat/swing(twistaxis:))
- [func swingTwist(twistAxis: RotationAxis3DFloat) -> (swing: Rotation3DFloat, twist: Rotation3DFloat)](/documentation/spatial/rotation3dfloat/swingtwist(twistaxis:))
- [func twist(twistAxis: RotationAxis3DFloat) -> Rotation3DFloat](/documentation/spatial/rotation3dfloat/twist(twistaxis:))

### Type Properties

- [static let identity: Rotation3DFloat](/documentation/spatial/rotation3dfloat/identity)

### Type Methods

- [static func slerp(from: Rotation3DFloat, to: Rotation3DFloat, t: Float, along: Rotation3D.SlerpPath) -> Rotation3DFloat](/documentation/spatial/rotation3dfloat/slerp(from:to:t:along:))
- [static func spline(leftEndpoint: Rotation3DFloat, from: Rotation3DFloat, to: Rotation3DFloat, rightEndpoint: Rotation3DFloat, t: Float) -> Rotation3DFloat](/documentation/spatial/rotation3dfloat/spline(leftendpoint:from:to:rightendpoint:t:))

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/rotation3dfloat/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/rotation3dfloat/custommirror)
- [Decodable Implementations](/documentation/spatial/rotation3dfloat/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/rotation3dfloat/init(from:))
- [Encodable Implementations](/documentation/spatial/rotation3dfloat/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/rotation3dfloat/encode(to:))
- [Equatable Implementations](/documentation/spatial/rotation3dfloat/equatable-implementations)

#### Operators

- [static func == (Rotation3DFloat, Rotation3DFloat) -> Bool](/documentation/spatial/rotation3dfloat/==(_:_:))
- [Hashable Implementations](/documentation/spatial/rotation3dfloat/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/rotation3dfloat/hash(into:))
- [RotationAxis3D](/documentation/spatial/rotationaxis3d)

### Creating a 3D rotation axis structure

- [init()](/documentation/spatial/rotationaxis3d/init())
- [init(simd_float3)](/documentation/spatial/rotationaxis3d/init(_:)-96si4)
- [init(simd_double3)](/documentation/spatial/rotationaxis3d/init(_:)-804sx)
- [init(vector: simd_double3)](/documentation/spatial/rotationaxis3d/init(vector:))
- [init(Vector3D)](/documentation/spatial/rotationaxis3d/init(_:)-2zdal)
- [init(x: Double, y: Double, z: Double)](/documentation/spatial/rotationaxis3d/init(x:y:z:)-3z5nm)
- [init<T>(x: T, y: T, z: T)](/documentation/spatial/rotationaxis3d/init(x:y:z:)-1x93q)

### Checking characteristics

- [var x: Double](/documentation/spatial/rotationaxis3d/x-swift.property)
- [var y: Double](/documentation/spatial/rotationaxis3d/y-swift.property)
- [var z: Double](/documentation/spatial/rotationaxis3d/z-swift.property)
- [var vector: simd_double3](/documentation/spatial/rotationaxis3d/vector)
- [var isZero: Bool](/documentation/spatial/rotationaxis3d/iszero)

### Constants

- [static let x: RotationAxis3D](/documentation/spatial/rotationaxis3d/x-swift.type.property)
- [static let y: RotationAxis3D](/documentation/spatial/rotationaxis3d/y-swift.type.property)
- [static let z: RotationAxis3D](/documentation/spatial/rotationaxis3d/z-swift.type.property)
- [static let xy: RotationAxis3D](/documentation/spatial/rotationaxis3d/xy)
- [static let yz: RotationAxis3D](/documentation/spatial/rotationaxis3d/yz)
- [static let xz: RotationAxis3D](/documentation/spatial/rotationaxis3d/xz)
- [static let xyz: RotationAxis3D](/documentation/spatial/rotationaxis3d/xyz)
- [static let zero: RotationAxis3D](/documentation/spatial/rotationaxis3d/zero)

### Deprecated symbols

- [var simd: simd_double3](/documentation/spatial/rotationaxis3d/simd)

### Initializers

- [init(simd_packed_double4)](/documentation/spatial/rotationaxis3d/init(_:)-ctks)
- [init(RotationAxis3DFloat)](/documentation/spatial/rotationaxis3d/init(_:)-lvvq)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/rotationaxis3d/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/rotationaxis3d/custommirror)
- [Decodable Implementations](/documentation/spatial/rotationaxis3d/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/rotationaxis3d/init(from:))
- [Encodable Implementations](/documentation/spatial/rotationaxis3d/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/rotationaxis3d/encode(to:))
- [Equatable Implementations](/documentation/spatial/rotationaxis3d/equatable-implementations)

#### Operators

- [static func == (RotationAxis3D, RotationAxis3D) -> Bool](/documentation/spatial/rotationaxis3d/==(_:_:))
- [Hashable Implementations](/documentation/spatial/rotationaxis3d/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/rotationaxis3d/hash(into:))
- [RotationAxis3DFloat](/documentation/spatial/rotationaxis3dfloat)

### Initializers

- [init()](/documentation/spatial/rotationaxis3dfloat/init())
- [init(simd_float3)](/documentation/spatial/rotationaxis3dfloat/init(_:)-3r5wd)
- [init(simd_double3)](/documentation/spatial/rotationaxis3dfloat/init(_:)-4n1ej)
- [init(Vector3DFloat)](/documentation/spatial/rotationaxis3dfloat/init(_:)-4q4aa)
- [init(RotationAxis3D)](/documentation/spatial/rotationaxis3dfloat/init(_:)-6c919)
- [init(simd_packed_float4)](/documentation/spatial/rotationaxis3dfloat/init(_:)-72zxm)
- [init(vector: simd_float3)](/documentation/spatial/rotationaxis3dfloat/init(vector:))
- [init(x: Float, y: Float, z: Float)](/documentation/spatial/rotationaxis3dfloat/init(x:y:z:)-273jp)
- [init<T>(x: T, y: T, z: T)](/documentation/spatial/rotationaxis3dfloat/init(x:y:z:)-hx2)

### Instance Properties

- [var vector: simd_float3](/documentation/spatial/rotationaxis3dfloat/vector)
- [var x: Float](/documentation/spatial/rotationaxis3dfloat/x-swift.property)
- [var y: Float](/documentation/spatial/rotationaxis3dfloat/y-swift.property)
- [var z: Float](/documentation/spatial/rotationaxis3dfloat/z-swift.property)

### Type Properties

- [static let x: RotationAxis3DFloat](/documentation/spatial/rotationaxis3dfloat/x-swift.type.property)
- [static let xy: RotationAxis3DFloat](/documentation/spatial/rotationaxis3dfloat/xy)
- [static let xyz: RotationAxis3DFloat](/documentation/spatial/rotationaxis3dfloat/xyz)
- [static let xz: RotationAxis3DFloat](/documentation/spatial/rotationaxis3dfloat/xz)
- [static let y: RotationAxis3DFloat](/documentation/spatial/rotationaxis3dfloat/y-swift.type.property)
- [static let yz: RotationAxis3DFloat](/documentation/spatial/rotationaxis3dfloat/yz)
- [static let z: RotationAxis3DFloat](/documentation/spatial/rotationaxis3dfloat/z-swift.type.property)
- [static let zero: RotationAxis3DFloat](/documentation/spatial/rotationaxis3dfloat/zero)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/rotationaxis3dfloat/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/rotationaxis3dfloat/custommirror)
- [Decodable Implementations](/documentation/spatial/rotationaxis3dfloat/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/rotationaxis3dfloat/init(from:))
- [Encodable Implementations](/documentation/spatial/rotationaxis3dfloat/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/rotationaxis3dfloat/encode(to:))
- [Equatable Implementations](/documentation/spatial/rotationaxis3dfloat/equatable-implementations)

#### Operators

- [static func == (RotationAxis3DFloat, RotationAxis3DFloat) -> Bool](/documentation/spatial/rotationaxis3dfloat/==(_:_:))
- [Hashable Implementations](/documentation/spatial/rotationaxis3dfloat/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/rotationaxis3dfloat/hash(into:))
- [Pose3D](/documentation/spatial/pose3d)

### Creating a 3D pose structure

- [init()](/documentation/spatial/pose3d/init())
- [init?(simd_float4x4)](/documentation/spatial/pose3d/init(_:)-8njy6)
- [init?(simd_double4x4)](/documentation/spatial/pose3d/init(_:)-9xspz)
- [init(forward: Vector3D, up: Vector3D)](/documentation/spatial/pose3d/init(forward:up:))
- [init(position: simd_float3, rotation: simd_quatf)](/documentation/spatial/pose3d/init(position:rotation:)-1gu7k)
- [init(position: Point3D, rotation: Rotation3D)](/documentation/spatial/pose3d/init(position:rotation:)-5afaf)
- [init(position: Point3D, rotation: Rotation3D)](/documentation/spatial/pose3d/init(position:rotation:)-5vswy)
- [init(position: simd_double3, rotation: simd_quatd)](/documentation/spatial/pose3d/init(position:rotation:)-zc2j)
- [init(position: Point3D, target: Point3D, up: Vector3D)](/documentation/spatial/pose3d/init(position:target:up:))
- [init?(transform: AffineTransform3D)](/documentation/spatial/pose3d/init(transform:)-2sey4)
- [init?(transform: ProjectiveTransform3D)](/documentation/spatial/pose3d/init(transform:)-4go9c)

### Constants

- [static var identity: Pose3D](/documentation/spatial/pose3d/identity)

### Inspecting a 3D pose’s properties

- [var matrix: simd_double4x4](/documentation/spatial/pose3d/matrix)
- [var position: Point3D](/documentation/spatial/pose3d/position)
- [var rotation: Rotation3D](/documentation/spatial/pose3d/rotation)
- [var inverse: Pose3D](/documentation/spatial/pose3d/inverse)

### Transforming a 3D pose structure

- [func concatenating(ScaledPose3D) -> ScaledPose3D](/documentation/spatial/pose3d/concatenating(_:)-4esra)
- [func concatenating(Pose3D) -> Pose3D](/documentation/spatial/pose3d/concatenating(_:)-6dd2s)
- [func flip(along: Axis3D)](/documentation/spatial/pose3d/flip(along:))
- [func flipped(along: Axis3D) -> Pose3D](/documentation/spatial/pose3d/flipped(along:))
- [func rotated(by: simd_quatd) -> Pose3D](/documentation/spatial/pose3d/rotated(by:)-10k2a)
- [func rotated(by: Rotation3D) -> Pose3D](/documentation/spatial/pose3d/rotated(by:)-377u)

### Checking characteristics

- [var isIdentity: Bool](/documentation/spatial/pose3d/isidentity)

### Comparing values

- [func isApproximatelyEqual(to: Pose3D, tolerance: Double) -> Bool](/documentation/spatial/pose3d/isapproximatelyequal(to:tolerance:))
- [static func == (Pose3D, Pose3D) -> Bool](/documentation/spatial/pose3d/==(_:_:))

### Applying arithmetic operations

- [static func * (Pose3D, Pose3D) -> Pose3D](/documentation/spatial/pose3d/*(_:_:))
- [static func *= (inout Pose3D, Pose3D)](/documentation/spatial/pose3d/*=(_:_:))

### Deprecated symbols

- [init?(matrix: simd_float4x4)](/documentation/spatial/pose3d/init(matrix:)-63uwf)
- [init?(matrix: simd_double4x4)](/documentation/spatial/pose3d/init(matrix:)-6698w)

### Initializers

- [init(Pose3DFloat)](/documentation/spatial/pose3d/init(_:)-6u9lt)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/pose3d/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/pose3d/custommirror)
- [Decodable Implementations](/documentation/spatial/pose3d/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/pose3d/init(from:))
- [Encodable Implementations](/documentation/spatial/pose3d/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/pose3d/encode(to:))
- [Equatable Implementations](/documentation/spatial/pose3d/equatable-implementations)

#### Operators

- [static func == (Pose3D, Pose3D) -> Bool](/documentation/spatial/pose3d/==(_:_:))
- [Hashable Implementations](/documentation/spatial/pose3d/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/pose3d/hash(into:))
- [Rotatable3D Implementations](/documentation/spatial/pose3d/rotatable3d-implementations)

#### Instance Methods

- [func rotated(by: simd_quatd) -> Pose3D](/documentation/spatial/pose3d/rotated(by:)-10k2a)
- [func rotated(by: Rotation3D) -> Pose3D](/documentation/spatial/pose3d/rotated(by:)-377u)
- [Pose3DFloat](/documentation/spatial/pose3dfloat)

### Operators

- [static func * (Pose3DFloat, Pose3DFloat) -> Pose3DFloat](/documentation/spatial/pose3dfloat/*(_:_:))
- [static func *= (inout Pose3DFloat, Pose3DFloat)](/documentation/spatial/pose3dfloat/*=(_:_:))

### Initializers

- [init()](/documentation/spatial/pose3dfloat/init())
- [init?(simd_float4x4)](/documentation/spatial/pose3dfloat/init(_:)-6yai5)
- [init(Pose3D)](/documentation/spatial/pose3dfloat/init(_:)-91dxh)
- [init(forward: Vector3DFloat, up: Vector3DFloat)](/documentation/spatial/pose3dfloat/init(forward:up:))
- [init(position: simd_float3, rotation: simd_quatf)](/documentation/spatial/pose3dfloat/init(position:rotation:)-1r25j)
- [init(position: Point3DFloat, rotation: Rotation3DFloat)](/documentation/spatial/pose3dfloat/init(position:rotation:)-6979c)
- [init(position: Point3DFloat, rotation: Rotation3DFloat)](/documentation/spatial/pose3dfloat/init(position:rotation:)-9nvnb)
- [init(position: Point3DFloat, target: Point3DFloat, up: Vector3DFloat)](/documentation/spatial/pose3dfloat/init(position:target:up:))
- [init?(transform: AffineTransform3DFloat)](/documentation/spatial/pose3dfloat/init(transform:)-7bffd)
- [init?(transform: ProjectiveTransform3DFloat)](/documentation/spatial/pose3dfloat/init(transform:)-94kwr)

### Instance Properties

- [var inverse: Pose3DFloat](/documentation/spatial/pose3dfloat/inverse)
- [var isIdentity: Bool](/documentation/spatial/pose3dfloat/isidentity)
- [var matrix: simd_float4x4](/documentation/spatial/pose3dfloat/matrix)
- [var position: Point3DFloat](/documentation/spatial/pose3dfloat/position)
- [var rotation: Rotation3DFloat](/documentation/spatial/pose3dfloat/rotation)

### Instance Methods

- [func concatenating(Pose3DFloat) -> Pose3DFloat](/documentation/spatial/pose3dfloat/concatenating(_:)-2kbxs)
- [func concatenating(ScaledPose3DFloat) -> ScaledPose3DFloat](/documentation/spatial/pose3dfloat/concatenating(_:)-3anuw)
- [func flip(along: Axis3D)](/documentation/spatial/pose3dfloat/flip(along:))
- [func flipped(along: Axis3D) -> Pose3DFloat](/documentation/spatial/pose3dfloat/flipped(along:))
- [func isApproximatelyEqual(to: Pose3DFloat, tolerance: Float) -> Bool](/documentation/spatial/pose3dfloat/isapproximatelyequal(to:tolerance:))

### Type Properties

- [static var identity: Pose3DFloat](/documentation/spatial/pose3dfloat/identity)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/pose3dfloat/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/pose3dfloat/custommirror)
- [Decodable Implementations](/documentation/spatial/pose3dfloat/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/pose3dfloat/init(from:))
- [Encodable Implementations](/documentation/spatial/pose3dfloat/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/pose3dfloat/encode(to:))
- [Equatable Implementations](/documentation/spatial/pose3dfloat/equatable-implementations)

#### Operators

- [static func == (Pose3DFloat, Pose3DFloat) -> Bool](/documentation/spatial/pose3dfloat/==(_:_:))
- [Hashable Implementations](/documentation/spatial/pose3dfloat/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/pose3dfloat/hash(into:))
- [Rotatable3DProtocol Implementations](/documentation/spatial/pose3dfloat/rotatable3dprotocol-implementations)

#### Instance Methods

- [func rotated(by: Rotation3DFloat) -> Pose3DFloat](/documentation/spatial/pose3dfloat/rotated(by:)-16eh)
- [func rotated(by: simd_quatf) -> Pose3DFloat](/documentation/spatial/pose3dfloat/rotated(by:)-6s426)
- [ScaledPose3D](/documentation/spatial/scaledpose3d)

### Creating a 3D scaled-pose structure

- [init()](/documentation/spatial/scaledpose3d/init())
- [init?(simd_float4x4)](/documentation/spatial/scaledpose3d/init(_:)-v6ox)
- [init?(simd_double4x4)](/documentation/spatial/scaledpose3d/init(_:)-4izkj)
- [init(forward: Vector3D, scale: Double, up: Vector3D)](/documentation/spatial/scaledpose3d/init(forward:scale:up:))
- [init(position: simd_float3, rotation: simd_quatf, scale: Float)](/documentation/spatial/scaledpose3d/init(position:rotation:scale:)-8ndo4)
- [init(position: simd_double3, rotation: simd_quatd, scale: Double)](/documentation/spatial/scaledpose3d/init(position:rotation:scale:)-6fom1)
- [init(position: Point3D, target: Point3D, scale: Double, up: Vector3D)](/documentation/spatial/scaledpose3d/init(position:target:scale:up:))
- [init(position: Point3D, rotation: Rotation3D, scale: Double)](/documentation/spatial/scaledpose3d/init(position:rotation:scale:)-7ya6f)
- [init(position: Point3D, rotation: Rotation3D, scale: Double)](/documentation/spatial/scaledpose3d/init(position:rotation:scale:)-8fyu0)
- [init?(transform: AffineTransform3D)](/documentation/spatial/scaledpose3d/init(transform:)-oogv)
- [init?(transform: ProjectiveTransform3D)](/documentation/spatial/scaledpose3d/init(transform:)-9s08k)

### Inspecting a 3D scaled pose’s properties

- [var matrix: simd_double4x4](/documentation/spatial/scaledpose3d/matrix)
- [var position: Point3D](/documentation/spatial/scaledpose3d/position)
- [var rotation: Rotation3D](/documentation/spatial/scaledpose3d/rotation)
- [var scale: Double](/documentation/spatial/scaledpose3d/scale)
- [var inverse: ScaledPose3D](/documentation/spatial/scaledpose3d/inverse)
- [var customMirror: Mirror](/documentation/spatial/scaledpose3d/custommirror)
- [static var identity: ScaledPose3D](/documentation/spatial/scaledpose3d/identity)

### Transforming a 3D scaled-pose structure

- [func flip(along: Axis3D)](/documentation/spatial/scaledpose3d/flip(along:))
- [func flipped(along: Axis3D) -> ScaledPose3D](/documentation/spatial/scaledpose3d/flipped(along:))
- [func rotated(by: simd_quatd) -> ScaledPose3D](/documentation/spatial/scaledpose3d/rotated(by:)-5mxbl)
- [func rotated(by: Rotation3D) -> ScaledPose3D](/documentation/spatial/scaledpose3d/rotated(by:)-x75b)
- [func concatenating(ScaledPose3D) -> ScaledPose3D](/documentation/spatial/scaledpose3d/concatenating(_:)-c38k)
- [func concatenating(Pose3D) -> ScaledPose3D](/documentation/spatial/scaledpose3d/concatenating(_:)-2xzgs)

### Checking characteristics

- [var isIdentity: Bool](/documentation/spatial/scaledpose3d/isidentity)

### Comparing values

- [func isApproximatelyEqual(to: ScaledPose3D, tolerance: Double) -> Bool](/documentation/spatial/scaledpose3d/isapproximatelyequal(to:tolerance:))
- [static func == (ScaledPose3D, ScaledPose3D) -> Bool](/documentation/spatial/scaledpose3d/==(_:_:))

### Applying arithmetic operations

- [static func * (ScaledPose3D, ScaledPose3D) -> ScaledPose3D](/documentation/spatial/scaledpose3d/*(_:_:)-6nx9h)
- [static func * (ScaledPose3D, Pose3D) -> ScaledPose3D](/documentation/spatial/scaledpose3d/*(_:_:)-93yyr)
- [static func * (Pose3D, ScaledPose3D) -> ScaledPose3D](/documentation/spatial/scaledpose3d/*(_:_:)-179zu)
- [static func *= (inout ScaledPose3D, ScaledPose3D)](/documentation/spatial/scaledpose3d/*=(_:_:))

### Initializers

- [init(ScaledPose3DFloat)](/documentation/spatial/scaledpose3d/init(_:)-3fa9n)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/scaledpose3d/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/scaledpose3d/custommirror)
- [Decodable Implementations](/documentation/spatial/scaledpose3d/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/scaledpose3d/init(from:))
- [Encodable Implementations](/documentation/spatial/scaledpose3d/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/scaledpose3d/encode(to:))
- [Equatable Implementations](/documentation/spatial/scaledpose3d/equatable-implementations)

#### Operators

- [static func == (ScaledPose3D, ScaledPose3D) -> Bool](/documentation/spatial/scaledpose3d/==(_:_:))
- [Hashable Implementations](/documentation/spatial/scaledpose3d/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/scaledpose3d/hash(into:))
- [Rotatable3D Implementations](/documentation/spatial/scaledpose3d/rotatable3d-implementations)

#### Instance Methods

- [func rotated(by: simd_quatd) -> ScaledPose3D](/documentation/spatial/scaledpose3d/rotated(by:)-5mxbl)
- [func rotated(by: Rotation3D) -> ScaledPose3D](/documentation/spatial/scaledpose3d/rotated(by:)-x75b)
- [ScaledPose3DFloat](/documentation/spatial/scaledpose3dfloat)

### Operators

- [static func * (ScaledPose3DFloat, ScaledPose3DFloat) -> ScaledPose3DFloat](/documentation/spatial/scaledpose3dfloat/*(_:_:)-2wclg)
- [static func * (ScaledPose3DFloat, Pose3DFloat) -> ScaledPose3DFloat](/documentation/spatial/scaledpose3dfloat/*(_:_:)-5qwyl)
- [static func * (Pose3DFloat, ScaledPose3DFloat) -> ScaledPose3DFloat](/documentation/spatial/scaledpose3dfloat/*(_:_:)-9z6s)
- [static func *= (inout ScaledPose3DFloat, ScaledPose3DFloat)](/documentation/spatial/scaledpose3dfloat/*=(_:_:))

### Initializers

- [init()](/documentation/spatial/scaledpose3dfloat/init())
- [init?(simd_float4x4)](/documentation/spatial/scaledpose3dfloat/init(_:)-4hh5z)
- [init(ScaledPose3D)](/documentation/spatial/scaledpose3dfloat/init(_:)-7zqj3)
- [init(forward: Vector3DFloat, scale: Float, up: Vector3DFloat)](/documentation/spatial/scaledpose3dfloat/init(forward:scale:up:))
- [init(position: Point3DFloat, rotation: Rotation3DFloat, scale: Float)](/documentation/spatial/scaledpose3dfloat/init(position:rotation:scale:)-1j1mg)
- [init(position: Point3DFloat, rotation: Rotation3DFloat, scale: Float)](/documentation/spatial/scaledpose3dfloat/init(position:rotation:scale:)-1xgkl)
- [init(position: simd_float3, rotation: simd_quatf, scale: Float)](/documentation/spatial/scaledpose3dfloat/init(position:rotation:scale:)-3l2fe)
- [init(position: Point3DFloat, target: Point3DFloat, scale: Float, up: Vector3DFloat)](/documentation/spatial/scaledpose3dfloat/init(position:target:scale:up:))
- [init?(transform: AffineTransform3DFloat)](/documentation/spatial/scaledpose3dfloat/init(transform:)-1m87a)
- [init?(transform: ProjectiveTransform3DFloat)](/documentation/spatial/scaledpose3dfloat/init(transform:)-xeog)

### Instance Properties

- [var inverse: ScaledPose3DFloat](/documentation/spatial/scaledpose3dfloat/inverse)
- [var isIdentity: Bool](/documentation/spatial/scaledpose3dfloat/isidentity)
- [var matrix: simd_float4x4](/documentation/spatial/scaledpose3dfloat/matrix)
- [var position: Point3DFloat](/documentation/spatial/scaledpose3dfloat/position)
- [var rotation: Rotation3DFloat](/documentation/spatial/scaledpose3dfloat/rotation)
- [var scale: Float](/documentation/spatial/scaledpose3dfloat/scale)

### Instance Methods

- [func concatenating(ScaledPose3DFloat) -> ScaledPose3DFloat](/documentation/spatial/scaledpose3dfloat/concatenating(_:)-3pywy)
- [func concatenating(Pose3DFloat) -> ScaledPose3DFloat](/documentation/spatial/scaledpose3dfloat/concatenating(_:)-7ol75)
- [func flip(along: Axis3D)](/documentation/spatial/scaledpose3dfloat/flip(along:))
- [func flipped(along: Axis3D) -> ScaledPose3DFloat](/documentation/spatial/scaledpose3dfloat/flipped(along:))
- [func isApproximatelyEqual(to: ScaledPose3DFloat, tolerance: Float) -> Bool](/documentation/spatial/scaledpose3dfloat/isapproximatelyequal(to:tolerance:))

### Type Properties

- [static var identity: ScaledPose3DFloat](/documentation/spatial/scaledpose3dfloat/identity)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/scaledpose3dfloat/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/scaledpose3dfloat/custommirror)
- [Decodable Implementations](/documentation/spatial/scaledpose3dfloat/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/scaledpose3dfloat/init(from:))
- [Encodable Implementations](/documentation/spatial/scaledpose3dfloat/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/scaledpose3dfloat/encode(to:))
- [Equatable Implementations](/documentation/spatial/scaledpose3dfloat/equatable-implementations)

#### Operators

- [static func == (ScaledPose3DFloat, ScaledPose3DFloat) -> Bool](/documentation/spatial/scaledpose3dfloat/==(_:_:))
- [Hashable Implementations](/documentation/spatial/scaledpose3dfloat/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/scaledpose3dfloat/hash(into:))
- [Rotatable3DProtocol Implementations](/documentation/spatial/scaledpose3dfloat/rotatable3dprotocol-implementations)

#### Instance Methods

- [func rotated(by: simd_quatf) -> ScaledPose3DFloat](/documentation/spatial/scaledpose3dfloat/rotated(by:)-8d0z0)
- [func rotated(by: Rotation3DFloat) -> ScaledPose3DFloat](/documentation/spatial/scaledpose3dfloat/rotated(by:)-8oxh1)
- [SphericalCoordinates3D](/documentation/spatial/sphericalcoordinates3d)

### Creating a spherical coordinates structure

- [init()](/documentation/spatial/sphericalcoordinates3d/init())
- [init(Vector3D)](/documentation/spatial/sphericalcoordinates3d/init(_:)-2eoox)
- [init(Point3D)](/documentation/spatial/sphericalcoordinates3d/init(_:)-45qdy)
- [init(simd_double3)](/documentation/spatial/sphericalcoordinates3d/init(_:)-1xzjz)
- [init(radius: Double, inclination: Angle2D, azimuth: Angle2D)](/documentation/spatial/sphericalcoordinates3d/init(radius:inclination:azimuth:))
- [init(vector: simd_double3)](/documentation/spatial/sphericalcoordinates3d/init(vector:))
- [init(x: Double, y: Double, z: Double)](/documentation/spatial/sphericalcoordinates3d/init(x:y:z:))

### Inspecting a spherical coordinates structure’s properties

- [azimuth](/documentation/spatial/sphericalcoordinates3d/azimuth)
- [inclination](/documentation/spatial/sphericalcoordinates3d/inclination)
- [radius](/documentation/spatial/sphericalcoordinates3d/radius)
- [var vector: simd_double3](/documentation/spatial/sphericalcoordinates3d/vector)
- [var customMirror: Mirror](/documentation/spatial/sphericalcoordinates3d/custommirror)

### Initializers

- [init(SphericalCoordinates3DFloat)](/documentation/spatial/sphericalcoordinates3d/init(_:)-1hxjg)
- [init(simd_packed_double4)](/documentation/spatial/sphericalcoordinates3d/init(_:)-91oq0)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/sphericalcoordinates3d/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/sphericalcoordinates3d/custommirror)
- [Decodable Implementations](/documentation/spatial/sphericalcoordinates3d/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/sphericalcoordinates3d/init(from:))
- [Encodable Implementations](/documentation/spatial/sphericalcoordinates3d/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/sphericalcoordinates3d/encode(to:))
- [Equatable Implementations](/documentation/spatial/sphericalcoordinates3d/equatable-implementations)

#### Operators

- [static func == (SphericalCoordinates3D, SphericalCoordinates3D) -> Bool](/documentation/spatial/sphericalcoordinates3d/==(_:_:))
- [Hashable Implementations](/documentation/spatial/sphericalcoordinates3d/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/sphericalcoordinates3d/hash(into:))
- [SphericalCoordinates3DFloat](/documentation/spatial/sphericalcoordinates3dfloat)

### Initializers

- [init()](/documentation/spatial/sphericalcoordinates3dfloat/init())
- [init(Vector3DFloat)](/documentation/spatial/sphericalcoordinates3dfloat/init(_:)-4t1io)
- [init(simd_float3)](/documentation/spatial/sphericalcoordinates3dfloat/init(_:)-6dp94)
- [init(SphericalCoordinates3D)](/documentation/spatial/sphericalcoordinates3dfloat/init(_:)-6lfdm)
- [init(Point3DFloat)](/documentation/spatial/sphericalcoordinates3dfloat/init(_:)-8zaur)
- [init(simd_packed_float4)](/documentation/spatial/sphericalcoordinates3dfloat/init(_:)-99axl)
- [init(radius: Float, inclination: Angle2DFloat, azimuth: Angle2DFloat)](/documentation/spatial/sphericalcoordinates3dfloat/init(radius:inclination:azimuth:))
- [init(vector: simd_float3)](/documentation/spatial/sphericalcoordinates3dfloat/init(vector:))
- [init(x: Float, y: Float, z: Float)](/documentation/spatial/sphericalcoordinates3dfloat/init(x:y:z:))

### Instance Properties

- [var azimuth: Angle2DFloat](/documentation/spatial/sphericalcoordinates3dfloat/azimuth)
- [var inclination: Angle2DFloat](/documentation/spatial/sphericalcoordinates3dfloat/inclination)
- [var radius: Float](/documentation/spatial/sphericalcoordinates3dfloat/radius)
- [var vector: simd_float3](/documentation/spatial/sphericalcoordinates3dfloat/vector)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/sphericalcoordinates3dfloat/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/sphericalcoordinates3dfloat/custommirror)
- [Decodable Implementations](/documentation/spatial/sphericalcoordinates3dfloat/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/sphericalcoordinates3dfloat/init(from:))
- [Encodable Implementations](/documentation/spatial/sphericalcoordinates3dfloat/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/sphericalcoordinates3dfloat/encode(to:))
- [Equatable Implementations](/documentation/spatial/sphericalcoordinates3dfloat/equatable-implementations)

#### Operators

- [static func == (SphericalCoordinates3DFloat, SphericalCoordinates3DFloat) -> Bool](/documentation/spatial/sphericalcoordinates3dfloat/==(_:_:))
- [Hashable Implementations](/documentation/spatial/sphericalcoordinates3dfloat/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/sphericalcoordinates3dfloat/hash(into:))
- [Ray3D](/documentation/spatial/ray3d)

### Creating a 3D ray structure

- [init()](/documentation/spatial/ray3d/init())
- [init(origin: Point3D, direction: Vector3D)](/documentation/spatial/ray3d/init(origin:direction:)-5sxkl)
- [init(origin: simd_float3, direction: simd_float3)](/documentation/spatial/ray3d/init(origin:direction:)-3gfcj)
- [init(origin: simd_double3, direction: simd_double3)](/documentation/spatial/ray3d/init(origin:direction:)-47w1c)

### Inspecting a 3D ray’s properties

- [var origin: Point3D](/documentation/spatial/ray3d/origin)
- [var direction: Vector3D](/documentation/spatial/ray3d/direction)

### Transforming a 3D ray structure

- [func apply(Pose3D)](/documentation/spatial/ray3d/apply(_:))
- [func applying(AffineTransform3D) -> Ray3D](/documentation/spatial/ray3d/applying(_:)-337n0)
- [func applying(ProjectiveTransform3D) -> Ray3D](/documentation/spatial/ray3d/applying(_:)-2aom9)
- [func applying(Pose3D) -> Ray3D](/documentation/spatial/ray3d/applying(_:)-34rqi)
- [func unapplying(AffineTransform3D) -> Ray3D](/documentation/spatial/ray3d/unapplying(_:)-7bc37)
- [func unapplying(ProjectiveTransform3D) -> Ray3D](/documentation/spatial/ray3d/unapplying(_:)-6tj2w)
- [func unapplying(Pose3D) -> Ray3D](/documentation/spatial/ray3d/unapplying(_:)-928o9)
- [func rotated(by: Rotation3D) -> Ray3D](/documentation/spatial/ray3d/rotated(by:)-qxp0)
- [func rotated(by: simd_quatd) -> Ray3D](/documentation/spatial/ray3d/rotated(by:)-81glv)
- [func rotated(by: simd_quatd, around: Point3D) -> Ray3D](/documentation/spatial/ray3d/rotated(by:around:)-uzon)
- [func rotated(by: Rotation3D, around: Point3D) -> Ray3D](/documentation/spatial/ray3d/rotated(by:around:)-7h43)
- [func applying(ScaledPose3D) -> Ray3D](/documentation/spatial/ray3d/applying(_:)-6hfqw)
- [func unapplying(ScaledPose3D) -> Ray3D](/documentation/spatial/ray3d/unapplying(_:)-9x164)

### Checking characteristics

- [var isFinite: Bool](/documentation/spatial/ray3d/isfinite)
- [var isNaN: Bool](/documentation/spatial/ray3d/isnan)
- [var isZero: Bool](/documentation/spatial/ray3d/iszero)
- [func intersects(Rect3D) -> Bool](/documentation/spatial/ray3d/intersects(_:))
- [func intersects(sphereOrigin: Point3D, sphereRadius: Double) -> Bool](/documentation/spatial/ray3d/intersects(sphereorigin:sphereradius:))

### Comparing values

- [static func == (Ray3D, Ray3D) -> Bool](/documentation/spatial/ray3d/==(_:_:))

### Applying arithmetic operations

- [static func * (Pose3D, Ray3D) -> Ray3D](/documentation/spatial/ray3d/*(_:_:))

### Initializers

- [init(Ray3DFloat)](/documentation/spatial/ray3d/init(_:))
- [init(origin: Point3D, direction: Vector3D)](/documentation/spatial/ray3d/init(origin:direction:)-63yk4)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/ray3d/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/ray3d/custommirror)
- [Decodable Implementations](/documentation/spatial/ray3d/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/ray3d/init(from:))
- [Encodable Implementations](/documentation/spatial/ray3d/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/ray3d/encode(to:))
- [Equatable Implementations](/documentation/spatial/ray3d/equatable-implementations)

#### Operators

- [static func == (Ray3D, Ray3D) -> Bool](/documentation/spatial/ray3d/==(_:_:))
- [Hashable Implementations](/documentation/spatial/ray3d/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/ray3d/hash(into:))
- [Primitive3DProtocol Implementations](/documentation/spatial/ray3d/primitive3dprotocol-implementations)

#### Instance Properties

- [var isFinite: Bool](/documentation/spatial/ray3d/isfinite)
- [var isNaN: Bool](/documentation/spatial/ray3d/isnan)
- [var isZero: Bool](/documentation/spatial/ray3d/iszero)

#### Instance Methods

- [func apply(Pose3D)](/documentation/spatial/ray3d/apply(_:))
- [func applying(AffineTransform3D) -> Ray3D](/documentation/spatial/ray3d/applying(_:)-337n0)
- [func applying(Pose3D) -> Ray3D](/documentation/spatial/ray3d/applying(_:)-34rqi)
- [func unapplying(ProjectiveTransform3D) -> Ray3D](/documentation/spatial/ray3d/unapplying(_:)-6tj2w)
- [func unapplying(AffineTransform3D) -> Ray3D](/documentation/spatial/ray3d/unapplying(_:)-7bc37)
- [func unapplying(Pose3D) -> Ray3D](/documentation/spatial/ray3d/unapplying(_:)-928o9)
- [ProjectiveTransformable3D Implementations](/documentation/spatial/ray3d/projectivetransformable3d-implementations)

#### Instance Methods

- [func applying(ProjectiveTransform3D) -> Ray3D](/documentation/spatial/ray3d/applying(_:)-2aom9)
- [Rotatable3DProtocol Implementations](/documentation/spatial/ray3d/rotatable3dprotocol-implementations)

#### Instance Methods

- [func rotated(by: simd_quatd) -> Ray3D](/documentation/spatial/ray3d/rotated(by:)-81glv)
- [func rotated(by: Rotation3D) -> Ray3D](/documentation/spatial/ray3d/rotated(by:)-qxp0)
- [Ray3DFloat](/documentation/spatial/ray3dfloat)

### Operators

- [static func * (Pose3DFloat, Ray3DFloat) -> Ray3DFloat](/documentation/spatial/ray3dfloat/*(_:_:))

### Initializers

- [init()](/documentation/spatial/ray3dfloat/init())
- [init(Ray3D)](/documentation/spatial/ray3dfloat/init(_:))
- [init(origin: Point3DFloat, direction: Vector3DFloat)](/documentation/spatial/ray3dfloat/init(origin:direction:)-2oe8j)
- [init(origin: Point3DFloat, direction: Vector3DFloat)](/documentation/spatial/ray3dfloat/init(origin:direction:)-32dzt)
- [init(origin: simd_float3, direction: simd_float3)](/documentation/spatial/ray3dfloat/init(origin:direction:)-6g59d)

### Instance Properties

- [var direction: Vector3DFloat](/documentation/spatial/ray3dfloat/direction)
- [var origin: Point3DFloat](/documentation/spatial/ray3dfloat/origin)

### Instance Methods

- [func applying(ScaledPose3DFloat) -> Ray3DFloat](/documentation/spatial/ray3dfloat/applying(_:)-9e23e)
- [func intersects(Rect3DFloat) -> Bool](/documentation/spatial/ray3dfloat/intersects(_:))
- [func intersects(sphereOrigin: Point3DFloat, sphereRadius: Float) -> Bool](/documentation/spatial/ray3dfloat/intersects(sphereorigin:sphereradius:))
- [func rotated(by: simd_quatf, around: Point3DFloat) -> Ray3DFloat](/documentation/spatial/ray3dfloat/rotated(by:around:)-4etjl)
- [func rotated(by: Rotation3DFloat, around: Point3DFloat) -> Ray3DFloat](/documentation/spatial/ray3dfloat/rotated(by:around:)-7tmtq)
- [func unapplying(ScaledPose3DFloat) -> Ray3DFloat](/documentation/spatial/ray3dfloat/unapplying(_:)-3zk38)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/ray3dfloat/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/ray3dfloat/custommirror)
- [Decodable Implementations](/documentation/spatial/ray3dfloat/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/ray3dfloat/init(from:))
- [Encodable Implementations](/documentation/spatial/ray3dfloat/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/ray3dfloat/encode(to:))
- [Equatable Implementations](/documentation/spatial/ray3dfloat/equatable-implementations)

#### Operators

- [static func == (Ray3DFloat, Ray3DFloat) -> Bool](/documentation/spatial/ray3dfloat/==(_:_:))
- [Hashable Implementations](/documentation/spatial/ray3dfloat/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/ray3dfloat/hash(into:))
- [Primitive3DProtocol Implementations](/documentation/spatial/ray3dfloat/primitive3dprotocol-implementations)

#### Instance Properties

- [var isFinite: Bool](/documentation/spatial/ray3dfloat/isfinite)
- [var isNaN: Bool](/documentation/spatial/ray3dfloat/isnan)
- [var isZero: Bool](/documentation/spatial/ray3dfloat/iszero)

#### Instance Methods

- [func apply(Pose3DFloat)](/documentation/spatial/ray3dfloat/apply(_:))
- [func applying(Pose3DFloat) -> Ray3DFloat](/documentation/spatial/ray3dfloat/applying(_:)-3spgk)
- [func applying(ProjectiveTransform3DFloat) -> Ray3DFloat](/documentation/spatial/ray3dfloat/applying(_:)-6phxw)
- [func applying(AffineTransform3DFloat) -> Ray3DFloat](/documentation/spatial/ray3dfloat/applying(_:)-7miic)
- [func unapplying(Pose3DFloat) -> Ray3DFloat](/documentation/spatial/ray3dfloat/unapplying(_:)-2ouak)
- [func unapplying(ProjectiveTransform3DFloat) -> Ray3DFloat](/documentation/spatial/ray3dfloat/unapplying(_:)-6pcxp)
- [func unapplying(AffineTransform3DFloat) -> Ray3DFloat](/documentation/spatial/ray3dfloat/unapplying(_:)-9mbz3)
- [Rotatable3DProtocol Implementations](/documentation/spatial/ray3dfloat/rotatable3dprotocol-implementations)

#### Instance Methods

- [func rotated(by: simd_quatf) -> Ray3DFloat](/documentation/spatial/ray3dfloat/rotated(by:)-3vmkj)
- [func rotated(by: Rotation3DFloat) -> Ray3DFloat](/documentation/spatial/ray3dfloat/rotated(by:)-4p712)

## Affine and projective transforms

- [AffineTransform3D](/documentation/spatial/affinetransform3d)

### Creating a 3D affine transform structure

- [init()](/documentation/spatial/affinetransform3d/init()-2uqjl)
- [init()](/documentation/spatial/affinetransform3d/init()-6ntm3)
- [init(simd_float4x3)](/documentation/spatial/affinetransform3d/init(_:)-52vpb)
- [init(simd_double4x3)](/documentation/spatial/affinetransform3d/init(_:)-722a2)
- [init(Transform)](/documentation/spatial/affinetransform3d/init(_:)-e2xx)
- [init(matrix: simd_double4x3)](/documentation/spatial/affinetransform3d/init(matrix:)-2inci)
- [init(pose: Pose3D)](/documentation/spatial/affinetransform3d/init(pose:))
- [init(scale: Size3D, rotation: Rotation3D, translation: Vector3D)](/documentation/spatial/affinetransform3d/init(scale:rotation:translation:)-3somu)
- [init(scaledPose: ScaledPose3D)](/documentation/spatial/affinetransform3d/init(scaledpose:))
- [init(shear: AxisWithFactors)](/documentation/spatial/affinetransform3d/init(shear:))
- [init(truncating: ProjectiveTransform3D)](/documentation/spatial/affinetransform3d/init(truncating:)-40nzj)
- [init(truncating: simd_float4x4)](/documentation/spatial/affinetransform3d/init(truncating:)-5wjxy)
- [init(truncating: simd_double4x4)](/documentation/spatial/affinetransform3d/init(truncating:)-9fd9g)

### Transforming a 3D affine transform structure

- [Axis3D](/documentation/spatial/axis3d)

#### Constants

- [static var x: Axis3D](/documentation/spatial/axis3d/x)
- [static var y: Axis3D](/documentation/spatial/axis3d/y)
- [static var z: Axis3D](/documentation/spatial/axis3d/z)

#### Initializers

- [init(UInt32)](/documentation/spatial/axis3d/init(_:))
- [init(rawValue: UInt32)](/documentation/spatial/axis3d/init(rawvalue:))

#### Inspecting the axis

- [var rawValue: UInt32](/documentation/spatial/axis3d/rawvalue)

#### Default Implementations

- [Decodable Implementations](/documentation/spatial/axis3d/decodable-implementations)

##### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/axis3d/init(from:))
- [Encodable Implementations](/documentation/spatial/axis3d/encodable-implementations)

##### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/axis3d/encode(to:))
- [Hashable Implementations](/documentation/spatial/axis3d/hashable-implementations)

##### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/axis3d/hash(into:))
- [AxisWithFactors](/documentation/spatial/axiswithfactors)

#### Enumeration cases

- [case xAxis(yShearFactor: Double, zShearFactor: Double)](/documentation/spatial/axiswithfactors/xaxis(yshearfactor:zshearfactor:))
- [case yAxis(xShearFactor: Double, zShearFactor: Double)](/documentation/spatial/axiswithfactors/yaxis(xshearfactor:zshearfactor:))
- [case zAxis(xShearFactor: Double, yShearFactor: Double)](/documentation/spatial/axiswithfactors/zaxis(xshearfactor:yshearfactor:))
- [func changeBasis(from: AffineTransform3D, to: AffineTransform3D) -> AffineTransform3D?](/documentation/spatial/affinetransform3d/changebasis(from:to:))
- [func flip(along: Axis3D)](/documentation/spatial/affinetransform3d/flip(along:))
- [func flipped(along: Axis3D) -> AffineTransform3D](/documentation/spatial/affinetransform3d/flipped(along:))
- [var inverse: AffineTransform3D?](/documentation/spatial/affinetransform3d/inverse)
- [func scaledBy(x: Double, y: Double, z: Double) -> AffineTransform3D](/documentation/spatial/affinetransform3d/scaledby(x:y:z:))
- [func sheared(AxisWithFactors) -> AffineTransform3D](/documentation/spatial/affinetransform3d/sheared(_:))

### Decomposing a 3D affine transform

- [var rotation: Rotation3D?](/documentation/spatial/affinetransform3d/rotation)
- [var scale: Size3D](/documentation/spatial/affinetransform3d/scale)
- [var translation: Vector3D](/documentation/spatial/affinetransform3d/translation)

### Checking characteristics

- [Dimension3DSet](/documentation/spatial/dimension3dset)

#### Type properties

- [static let all: Dimension3DSet](/documentation/spatial/dimension3dset/all)
- [static let x: Dimension3DSet](/documentation/spatial/dimension3dset/x)
- [static let y: Dimension3DSet](/documentation/spatial/dimension3dset/y)
- [static let z: Dimension3DSet](/documentation/spatial/dimension3dset/z)

#### Instance properties

- [let rawValue: Int](/documentation/spatial/dimension3dset/rawvalue)

#### Initializers

- [init(rawValue: Int)](/documentation/spatial/dimension3dset/init(rawvalue:))
- [var isInvertible: Bool](/documentation/spatial/affinetransform3d/isinvertible)
- [func isUniform(overDimensions: Dimension3DSet) -> Bool](/documentation/spatial/affinetransform3d/isuniform(overdimensions:))
- [var matrix: simd_double4x3](/documentation/spatial/affinetransform3d/matrix)
- [var matrix3x3: simd_double3x3](/documentation/spatial/affinetransform3d/matrix3x3)
- [var matrix4x4: simd_double4x4](/documentation/spatial/affinetransform3d/matrix4x4)

### Comparing values

- [static func == (AffineTransform3D, AffineTransform3D) -> Bool](/documentation/spatial/affinetransform3d/==(_:_:))
- [func isApproximatelyEqual(to: AffineTransform3D, tolerance: Double) -> Bool](/documentation/spatial/affinetransform3d/isapproximatelyequal(to:tolerance:))

### Applying arithmetic operations

- [static func * (AffineTransform3D, AffineTransform3D) -> AffineTransform3D](/documentation/spatial/affinetransform3d/*(_:_:))
- [static func *= (inout AffineTransform3D, AffineTransform3D)](/documentation/spatial/affinetransform3d/*=(_:_:))

### Deprecated symbols

- [init?(simd_float4x4)](/documentation/spatial/affinetransform3d/init(_:)-41dx7)
- [init?(simd_double4x4)](/documentation/spatial/affinetransform3d/init(_:)-6bm4k)
- [init?(matrix: simd_double4x4)](/documentation/spatial/affinetransform3d/init(matrix:)-2tgp8)
- [init(matrix: simd_float4x3)](/documentation/spatial/affinetransform3d/init(matrix:)-6icxq)
- [init?(matrix: simd_float4x4)](/documentation/spatial/affinetransform3d/init(matrix:)-82rxz)
- [init?(projectiveTransform: ProjectiveTransform3D)](/documentation/spatial/affinetransform3d/init(projectivetransform:))
- [init(scale: Size3D, rotation: Rotation3D, translation: Size3D)](/documentation/spatial/affinetransform3d/init(scale:rotation:translation:)-40dow)
- [init(translation: Size3D)](/documentation/spatial/affinetransform3d/init(translation:))
- [func inverted() -> AffineTransform3D?](/documentation/spatial/affinetransform3d/inverted())
- [var offset: Vector3D](/documentation/spatial/affinetransform3d/offset)

### Initializers

- [init(AffineTransform3DFloat)](/documentation/spatial/affinetransform3d/init(_:)-7eksa)

### Instance Properties

- [var columns: (Vector3D, Vector3D, Vector3D, Vector3D)](/documentation/spatial/affinetransform3d/columns)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/affinetransform3d/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/affinetransform3d/custommirror)
- [Decodable Implementations](/documentation/spatial/affinetransform3d/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/affinetransform3d/init(from:))
- [Encodable Implementations](/documentation/spatial/affinetransform3d/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/affinetransform3d/encode(to:))
- [Equatable Implementations](/documentation/spatial/affinetransform3d/equatable-implementations)

#### Operators

- [static func == (AffineTransform3D, AffineTransform3D) -> Bool](/documentation/spatial/affinetransform3d/==(_:_:))
- [Hashable Implementations](/documentation/spatial/affinetransform3d/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/affinetransform3d/hash(into:))
- [Scalable3DProtocol Implementations](/documentation/spatial/affinetransform3d/scalable3dprotocol-implementations)

#### Instance Methods

- [func scaledBy(x: Double, y: Double, z: Double) -> AffineTransform3D](/documentation/spatial/affinetransform3d/scaledby(x:y:z:))
- [Shearable3DProtocol Implementations](/documentation/spatial/affinetransform3d/shearable3dprotocol-implementations)

#### Instance Methods

- [func sheared(AxisWithFactors) -> AffineTransform3D](/documentation/spatial/affinetransform3d/sheared(_:))
- [Transform3DProtocol Implementations](/documentation/spatial/affinetransform3d/transform3dprotocol-implementations)

#### Initializers

- [init(scale: Size3D, rotation: Rotation3D, translation: Vector3D)](/documentation/spatial/affinetransform3d/init(scale:rotation:translation:)-3somu)
- [init(shear: AxisWithFactors)](/documentation/spatial/affinetransform3d/init(shear:))

#### Instance Properties

- [var inverse: AffineTransform3D?](/documentation/spatial/affinetransform3d/inverse)
- [var rotation: Rotation3D?](/documentation/spatial/affinetransform3d/rotation)
- [var translation: Vector3D](/documentation/spatial/affinetransform3d/translation)

#### Instance Methods

- [func flip(along: Axis3D)](/documentation/spatial/affinetransform3d/flip(along:))
- [func flipped(along: Axis3D) -> AffineTransform3D](/documentation/spatial/affinetransform3d/flipped(along:))
- [func isApproximatelyEqual(to: AffineTransform3D, tolerance: Double) -> Bool](/documentation/spatial/affinetransform3d/isapproximatelyequal(to:tolerance:))
- [func isUniform(overDimensions: Dimension3DSet) -> Bool](/documentation/spatial/affinetransform3d/isuniform(overdimensions:))
- [AffineTransform3DFloat](/documentation/spatial/affinetransform3dfloat)

### Operators

- [static func * (AffineTransform3DFloat, AffineTransform3DFloat) -> AffineTransform3DFloat](/documentation/spatial/affinetransform3dfloat/*(_:_:))
- [static func *= (inout AffineTransform3DFloat, AffineTransform3DFloat)](/documentation/spatial/affinetransform3dfloat/*=(_:_:))

### Initializers

- [init()](/documentation/spatial/affinetransform3dfloat/init()-6ek9q)
- [init()](/documentation/spatial/affinetransform3dfloat/init()-8li4c)
- [init(AffineTransform3D)](/documentation/spatial/affinetransform3dfloat/init(_:)-2c2os)
- [init(simd_double4x3)](/documentation/spatial/affinetransform3dfloat/init(_:)-3a23d)
- [init(simd_float4x3)](/documentation/spatial/affinetransform3dfloat/init(_:)-5ajh4)
- [init(matrix: simd_float4x3)](/documentation/spatial/affinetransform3dfloat/init(matrix:))
- [init(pose: Pose3DFloat)](/documentation/spatial/affinetransform3dfloat/init(pose:))
- [init(scaledPose: ScaledPose3DFloat)](/documentation/spatial/affinetransform3dfloat/init(scaledpose:))
- [init(truncating: ProjectiveTransform3DFloat)](/documentation/spatial/affinetransform3dfloat/init(truncating:)-1jfno)
- [init(truncating: simd_double4x4)](/documentation/spatial/affinetransform3dfloat/init(truncating:)-7vabe)
- [init(truncating: simd_float4x4)](/documentation/spatial/affinetransform3dfloat/init(truncating:)-8jfn6)

### Instance Properties

- [var columns: (Vector3DFloat, Vector3DFloat, Vector3DFloat, Vector3DFloat)](/documentation/spatial/affinetransform3dfloat/columns)
- [var isInvertible: Bool](/documentation/spatial/affinetransform3dfloat/isinvertible)
- [var matrix: simd_float4x3](/documentation/spatial/affinetransform3dfloat/matrix)
- [var matrix3x3: simd_float3x3](/documentation/spatial/affinetransform3dfloat/matrix3x3)
- [var matrix4x4: simd_float4x4](/documentation/spatial/affinetransform3dfloat/matrix4x4)
- [var scale: Size3DFloat](/documentation/spatial/affinetransform3dfloat/scale)

### Instance Methods

- [func changeBasis(from: AffineTransform3DFloat, to: AffineTransform3DFloat) -> AffineTransform3DFloat?](/documentation/spatial/affinetransform3dfloat/changebasis(from:to:))

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/affinetransform3dfloat/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/affinetransform3dfloat/custommirror)
- [Decodable Implementations](/documentation/spatial/affinetransform3dfloat/decodable-implementations)

#### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/affinetransform3dfloat/init(from:))
- [Encodable Implementations](/documentation/spatial/affinetransform3dfloat/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/affinetransform3dfloat/encode(to:))
- [Equatable Implementations](/documentation/spatial/affinetransform3dfloat/equatable-implementations)

#### Operators

- [static func == (AffineTransform3DFloat, AffineTransform3DFloat) -> Bool](/documentation/spatial/affinetransform3dfloat/==(_:_:))
- [Hashable Implementations](/documentation/spatial/affinetransform3dfloat/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/affinetransform3dfloat/hash(into:))
- [Scalable3DProtocol Implementations](/documentation/spatial/affinetransform3dfloat/scalable3dprotocol-implementations)

#### Instance Methods

- [func scaledBy(x: Float, y: Float, z: Float) -> AffineTransform3DFloat](/documentation/spatial/affinetransform3dfloat/scaledby(x:y:z:))
- [Shearable3DProtocol Implementations](/documentation/spatial/affinetransform3dfloat/shearable3dprotocol-implementations)

#### Instance Methods

- [func sheared(AxisWithFactorsFloat) -> AffineTransform3DFloat](/documentation/spatial/affinetransform3dfloat/sheared(_:))
- [Transform3DProtocol Implementations](/documentation/spatial/affinetransform3dfloat/transform3dprotocol-implementations)

#### Initializers

- [init(scale: Size3DFloat, rotation: Rotation3DFloat, translation: Vector3DFloat)](/documentation/spatial/affinetransform3dfloat/init(scale:rotation:translation:))
- [init(shear: AxisWithFactorsFloat)](/documentation/spatial/affinetransform3dfloat/init(shear:))

#### Instance Properties

- [var inverse: AffineTransform3DFloat?](/documentation/spatial/affinetransform3dfloat/inverse)
- [var rotation: Rotation3DFloat?](/documentation/spatial/affinetransform3dfloat/rotation)
- [var translation: Vector3DFloat](/documentation/spatial/affinetransform3dfloat/translation)

#### Instance Methods

- [func flip(along: Axis3D)](/documentation/spatial/affinetransform3dfloat/flip(along:))
- [func flipped(along: Axis3D) -> AffineTransform3DFloat](/documentation/spatial/affinetransform3dfloat/flipped(along:))
- [func isApproximatelyEqual(to: AffineTransform3DFloat, tolerance: Float) -> Bool](/documentation/spatial/affinetransform3dfloat/isapproximatelyequal(to:tolerance:))
- [func isUniform(overDimensions: Dimension3DSet) -> Bool](/documentation/spatial/affinetransform3dfloat/isuniform(overdimensions:))
- [ProjectiveTransform3D](/documentation/spatial/projectivetransform3d)

### Creating a 3D projective transform structure

- [init()](/documentation/spatial/projectivetransform3d/init()-1clia)
- [init()](/documentation/spatial/projectivetransform3d/init()-6c4f4)
- [init(simd_float4x4)](/documentation/spatial/projectivetransform3d/init(_:)-7b2bq)
- [init(simd_double4x4)](/documentation/spatial/projectivetransform3d/init(_:)-6g88l)
- [init(matrix: simd_double4x4)](/documentation/spatial/projectivetransform3d/init(matrix:)-8eg5x)
- [init(AffineTransform3D)](/documentation/spatial/projectivetransform3d/init(_:)-9t2jh)
- [init(pose: Pose3D)](/documentation/spatial/projectivetransform3d/init(pose:))
- [init(scale: Size3D, rotation: Rotation3D, translation: Vector3D)](/documentation/spatial/projectivetransform3d/init(scale:rotation:translation:)-4h5wm)
- [init(shear: AxisWithFactors)](/documentation/spatial/projectivetransform3d/init(shear:))
- [init(leftTangent: Double, rightTangent: Double, topTangent: Double, bottomTangent: Double, nearZ: Double, farZ: Double, reverseZ: Bool)](/documentation/spatial/projectivetransform3d/init(lefttangent:righttangent:toptangent:bottomtangent:nearz:farz:reversez:))
- [init(fovY: Angle2D, aspectRatio: Double, nearZ: Double, farZ: Double)](/documentation/spatial/projectivetransform3d/init(fovy:aspectratio:nearz:farz:))
- [init(fovY: Angle2D, aspectRatio: Double, nearZ: Double, farZ: Double, reverseZ: Bool)](/documentation/spatial/projectivetransform3d/init(fovy:aspectratio:nearz:farz:reversez:))
- [init(scaledPose: ScaledPose3D)](/documentation/spatial/projectivetransform3d/init(scaledpose:))

### Inspecting a 3D projective transform’s properties

- [var inverse: ProjectiveTransform3D?](/documentation/spatial/projectivetransform3d/inverse)
- [var scaleComponent: Size3D](/documentation/spatial/projectivetransform3d/scalecomponent)
- [var translation: Vector3D](/documentation/spatial/projectivetransform3d/translation)
- [var matrix: simd_double4x4](/documentation/spatial/projectivetransform3d/matrix)

### Transforming a 3D projective transform structure

- [func sheared(AxisWithFactors) -> ProjectiveTransform3D](/documentation/spatial/projectivetransform3d/sheared(_:))
- [AxisWithFactors](/documentation/spatial/axiswithfactors)

#### Enumeration cases

- [case xAxis(yShearFactor: Double, zShearFactor: Double)](/documentation/spatial/axiswithfactors/xaxis(yshearfactor:zshearfactor:))
- [case yAxis(xShearFactor: Double, zShearFactor: Double)](/documentation/spatial/axiswithfactors/yaxis(xshearfactor:zshearfactor:))
- [case zAxis(xShearFactor: Double, yShearFactor: Double)](/documentation/spatial/axiswithfactors/zaxis(xshearfactor:yshearfactor:))
- [Axis3D](/documentation/spatial/axis3d)

#### Constants

- [static var x: Axis3D](/documentation/spatial/axis3d/x)
- [static var y: Axis3D](/documentation/spatial/axis3d/y)
- [static var z: Axis3D](/documentation/spatial/axis3d/z)

#### Initializers

- [init(UInt32)](/documentation/spatial/axis3d/init(_:))
- [init(rawValue: UInt32)](/documentation/spatial/axis3d/init(rawvalue:))

#### Inspecting the axis

- [var rawValue: UInt32](/documentation/spatial/axis3d/rawvalue)

#### Default Implementations

- [Decodable Implementations](/documentation/spatial/axis3d/decodable-implementations)

##### Initializers

- [init(from: any Decoder) throws](/documentation/spatial/axis3d/init(from:))
- [Encodable Implementations](/documentation/spatial/axis3d/encodable-implementations)

##### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/spatial/axis3d/encode(to:))
- [Hashable Implementations](/documentation/spatial/axis3d/hashable-implementations)

##### Instance Methods

- [func hash(into: inout Hasher)](/documentation/spatial/axis3d/hash(into:))
- [func flip(along: Axis3D)](/documentation/spatial/projectivetransform3d/flip(along:))
- [func flipped(along: Axis3D) -> ProjectiveTransform3D](/documentation/spatial/projectivetransform3d/flipped(along:))

### Decomposing a 3D projective transform

- [var rotation: Rotation3D?](/documentation/spatial/projectivetransform3d/rotation)

### Checking characteristics

- [func is3DProjection() -> Bool](/documentation/spatial/projectivetransform3d/is3dprojection())
- [func isUniform(overDimensions: Dimension3DSet) -> Bool](/documentation/spatial/projectivetransform3d/isuniform(overdimensions:))
- [var isAffine: Bool](/documentation/spatial/projectivetransform3d/isaffine)
- [var isInvertible: Bool](/documentation/spatial/projectivetransform3d/isinvertible)

### Comparing values

- [func isApproximatelyEqual(to: ProjectiveTransform3D, tolerance: Double) -> Bool](/documentation/spatial/projectivetransform3d/isapproximatelyequal(to:tolerance:))

### Applying arithmetic operations

- [static func * (ProjectiveTransform3D, ProjectiveTransform3D) -> ProjectiveTransform3D](/documentation/spatial/projectivetransform3d/*(_:_:))
- [static func *= (inout ProjectiveTransform3D, ProjectiveTransform3D)](/documentation/spatial/projectivetransform3d/*=(_:_:))

### Deprecated symbols

- [var offset: Vector3D](/documentation/spatial/projectivetransform3d/offset)
- [var scale: Size3D?](/documentation/spatial/projectivetransform3d/scale)
- [func inverted() -> ProjectiveTransform3D?](/documentation/spatial/projectivetransform3d/inverted())
- [init(matrix: simd_float4x4)](/documentation/spatial/projectivetransform3d/init(matrix:)-zfb)
- [init(scale: Size3D, rotation: Rotation3D, translation: Size3D)](/documentation/spatial/projectivetransform3d/init(scale:rotation:translation:)-8qxxq)
- [init(fovyRadians: Double, aspectRatio: Double, nearZ: Double, farZ: Double, reverseZ: Bool)](/documentation/spatial/projectivetransform3d/init(fovyradians:aspectratio:nearz:farz:reversez:))
- [init(translation: Size3D)](/documentation/spatial/projectivetransform3d/init(translation:))
- [init(fovyRadians: Double, aspectRatio: Double, nearZ: Double, farZ: Double)](/documentation/spatial/projectivetransform3d/init(fovyradians:aspectratio:nearz:farz:))

### Initializers

- [init(ProjectiveTransform3DFloat)](/documentation/spatial/projectivetransform3d/init(_:)-7nv9f)

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/projectivetransform3d/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/projectivetransform3d/custommirror)
- [Scalable3DProtocol Implementations](/documentation/spatial/projectivetransform3d/scalable3dprotocol-implementations)

#### Instance Methods

- [func scaledBy(x: Double, y: Double, z: Double) -> ProjectiveTransform3D](/documentation/spatial/projectivetransform3d/scaledby(x:y:z:))
- [Shearable3DProtocol Implementations](/documentation/spatial/projectivetransform3d/shearable3dprotocol-implementations)

#### Instance Methods

- [func sheared(AxisWithFactors) -> ProjectiveTransform3D](/documentation/spatial/projectivetransform3d/sheared(_:))
- [Transform3DProtocol Implementations](/documentation/spatial/projectivetransform3d/transform3dprotocol-implementations)

#### Initializers

- [init(scale: Size3D, rotation: Rotation3D, translation: Vector3D)](/documentation/spatial/projectivetransform3d/init(scale:rotation:translation:)-4h5wm)
- [init(shear: AxisWithFactors)](/documentation/spatial/projectivetransform3d/init(shear:))

#### Instance Properties

- [var inverse: ProjectiveTransform3D?](/documentation/spatial/projectivetransform3d/inverse)
- [var rotation: Rotation3D?](/documentation/spatial/projectivetransform3d/rotation)
- [var translation: Vector3D](/documentation/spatial/projectivetransform3d/translation)

#### Instance Methods

- [func flip(along: Axis3D)](/documentation/spatial/projectivetransform3d/flip(along:))
- [func flipped(along: Axis3D) -> ProjectiveTransform3D](/documentation/spatial/projectivetransform3d/flipped(along:))
- [func isApproximatelyEqual(to: ProjectiveTransform3D, tolerance: Double) -> Bool](/documentation/spatial/projectivetransform3d/isapproximatelyequal(to:tolerance:))
- [func isUniform(overDimensions: Dimension3DSet) -> Bool](/documentation/spatial/projectivetransform3d/isuniform(overdimensions:))
- [ProjectiveTransform3DFloat](/documentation/spatial/projectivetransform3dfloat)

### Operators

- [static func * (ProjectiveTransform3DFloat, ProjectiveTransform3DFloat) -> ProjectiveTransform3DFloat](/documentation/spatial/projectivetransform3dfloat/*(_:_:))
- [static func *= (inout ProjectiveTransform3DFloat, ProjectiveTransform3DFloat)](/documentation/spatial/projectivetransform3dfloat/*=(_:_:))

### Initializers

- [init()](/documentation/spatial/projectivetransform3dfloat/init()-89m3y)
- [init()](/documentation/spatial/projectivetransform3dfloat/init()-c35e)
- [init(simd_double4x4)](/documentation/spatial/projectivetransform3dfloat/init(_:)-43p4e)
- [init(simd_float4x4)](/documentation/spatial/projectivetransform3dfloat/init(_:)-56itt)
- [init(AffineTransform3DFloat)](/documentation/spatial/projectivetransform3dfloat/init(_:)-6ffxa)
- [init(ProjectiveTransform3D)](/documentation/spatial/projectivetransform3dfloat/init(_:)-9r5ov)
- [init(fovY: Angle2DFloat, aspectRatio: Float, nearZ: Float, farZ: Float)](/documentation/spatial/projectivetransform3dfloat/init(fovy:aspectratio:nearz:farz:))
- [init(fovY: Angle2DFloat, aspectRatio: Float, nearZ: Float, farZ: Float, reverseZ: Bool)](/documentation/spatial/projectivetransform3dfloat/init(fovy:aspectratio:nearz:farz:reversez:))
- [init(leftTangent: Float, rightTangent: Float, topTangent: Float, bottomTangent: Float, nearZ: Float, farZ: Float, reverseZ: Bool)](/documentation/spatial/projectivetransform3dfloat/init(lefttangent:righttangent:toptangent:bottomtangent:nearz:farz:reversez:))
- [init(matrix: simd_float4x4)](/documentation/spatial/projectivetransform3dfloat/init(matrix:))
- [init(pose: Pose3DFloat)](/documentation/spatial/projectivetransform3dfloat/init(pose:))
- [init(scaledPose: ScaledPose3DFloat)](/documentation/spatial/projectivetransform3dfloat/init(scaledpose:))

### Instance Properties

- [var isAffine: Bool](/documentation/spatial/projectivetransform3dfloat/isaffine)
- [var isInvertible: Bool](/documentation/spatial/projectivetransform3dfloat/isinvertible)
- [var matrix: simd_float4x4](/documentation/spatial/projectivetransform3dfloat/matrix)
- [var scaleComponent: Size3DFloat](/documentation/spatial/projectivetransform3dfloat/scalecomponent)

### Instance Methods

- [func is3DFloatProjection() -> Bool](/documentation/spatial/projectivetransform3dfloat/is3dfloatprojection())

### Default Implementations

- [CustomReflectable Implementations](/documentation/spatial/projectivetransform3dfloat/customreflectable-implementations)

#### Instance Properties

- [var customMirror: Mirror](/documentation/spatial/projectivetransform3dfloat/custommirror)
- [Scalable3DProtocol Implementations](/documentation/spatial/projectivetransform3dfloat/scalable3dprotocol-implementations)

#### Instance Methods

- [func scaledBy(x: Float, y: Float, z: Float) -> ProjectiveTransform3DFloat](/documentation/spatial/projectivetransform3dfloat/scaledby(x:y:z:))
- [Shearable3DProtocol Implementations](/documentation/spatial/projectivetransform3dfloat/shearable3dprotocol-implementations)

#### Instance Methods

- [func sheared(AxisWithFactorsFloat) -> ProjectiveTransform3DFloat](/documentation/spatial/projectivetransform3dfloat/sheared(_:))
- [Transform3DProtocol Implementations](/documentation/spatial/projectivetransform3dfloat/transform3dprotocol-implementations)

#### Initializers

- [init(scale: Size3DFloat, rotation: Rotation3DFloat, translation: Vector3DFloat)](/documentation/spatial/projectivetransform3dfloat/init(scale:rotation:translation:))
- [init(shear: AxisWithFactorsFloat)](/documentation/spatial/projectivetransform3dfloat/init(shear:))

#### Instance Properties

- [var inverse: ProjectiveTransform3DFloat?](/documentation/spatial/projectivetransform3dfloat/inverse)
- [var rotation: Rotation3DFloat?](/documentation/spatial/projectivetransform3dfloat/rotation)
- [var translation: Vector3DFloat](/documentation/spatial/projectivetransform3dfloat/translation)

#### Instance Methods

- [func flip(along: Axis3D)](/documentation/spatial/projectivetransform3dfloat/flip(along:))
- [func flipped(along: Axis3D) -> ProjectiveTransform3DFloat](/documentation/spatial/projectivetransform3dfloat/flipped(along:))
- [func isApproximatelyEqual(to: ProjectiveTransform3DFloat, tolerance: Float) -> Bool](/documentation/spatial/projectivetransform3dfloat/isapproximatelyequal(to:tolerance:))
- [func isUniform(overDimensions: Dimension3DSet) -> Bool](/documentation/spatial/projectivetransform3dfloat/isuniform(overdimensions:))

## Converting between coordinate spaces

- [CoordinateSpace3D](/documentation/spatial/coordinatespace3d)

### Associated Types

- [AncestorCoordinateSpace](/documentation/spatial/coordinatespace3d/ancestorcoordinatespace)

### Instance Properties

- [var ancestorSpace: Self.AncestorCoordinateSpace?](/documentation/spatial/coordinatespace3d/ancestorspace)

### Instance Methods

- [func ancestorFromSpaceTransform() throws -> ProjectiveTransform3D](/documentation/spatial/coordinatespace3d/ancestorfromspacetransform())
- [func convert<T>(value: T, from: Self) throws -> T](/documentation/spatial/coordinatespace3d/convert(value:from:)-3zi9f)
- [func convert<T, Space>(value: T, from: Space) throws -> T](/documentation/spatial/coordinatespace3d/convert(value:from:)-7og5p)
- [func convert<T, Space>(value: T, to: Space) throws -> T](/documentation/spatial/coordinatespace3d/convert(value:to:)-2i668)
- [func convert<T>(value: T, to: Self) throws -> T](/documentation/spatial/coordinatespace3d/convert(value:to:)-u2a0)
- [func transform(from: Self) throws -> ProjectiveTransform3D](/documentation/spatial/coordinatespace3d/transform(from:))
- [func transformSpace((Self) -> ProjectiveTransform3D) -> some CoordinateSpace3D](/documentation/spatial/coordinatespace3d/transformspace(_:))

### Type Properties

- [static var worldReference: WorldReferenceCoordinateSpace](/documentation/spatial/coordinatespace3d/worldreference)
- [CoordinateSpace3DFloat](/documentation/spatial/coordinatespace3dfloat)

### Instance Methods

- [func ancestorFromSpaceTransformFloat() throws -> ProjectiveTransform3DFloat](/documentation/spatial/coordinatespace3dfloat/ancestorfromspacetransformfloat())
- [func convert<T, Space>(value: T, from: Space) throws -> T](/documentation/spatial/coordinatespace3dfloat/convert(value:from:))
- [func convert<T, Space>(value: T, to: Space) throws -> T](/documentation/spatial/coordinatespace3dfloat/convert(value:to:))
- [func transformSpace((Self) -> ProjectiveTransform3DFloat) -> some CoordinateSpace3DFloat](/documentation/spatial/coordinatespace3dfloat/transformspace(_:))
- [CoordinateSpaceValue3D](/documentation/spatial/coordinatespacevalue3d)

### Associated Types

- [Value](/documentation/spatial/coordinatespacevalue3d/value)

### Instance Methods

- [func resolve<Space>(in: Space) throws -> Self.Value](/documentation/spatial/coordinatespacevalue3d/resolve(in:))
- [ProjectiveTransformable3D](/documentation/spatial/projectivetransformable3d)

### Instance Methods

- [func applying(ProjectiveTransform3D) -> Self](/documentation/spatial/projectivetransformable3d/applying(_:))
- [ProjectiveTransformable3DFloat](/documentation/spatial/projectivetransformable3dfloat)

### Instance Methods

- [func applying(ProjectiveTransform3DFloat) -> Self](/documentation/spatial/projectivetransformable3dfloat/applying(_:))
- [WorldReferenceCoordinateSpace](/documentation/spatial/worldreferencecoordinatespace)

## Applying trigonometric functions

- [func cos(Angle2D) -> Double](/documentation/spatial/cos(_:)-609v4)
- [func cos(Angle2DFloat) -> Float](/documentation/spatial/cos(_:)-79fxe)
- [func cosh(Angle2D) -> Double](/documentation/spatial/cosh(_:)-6cg6v)
- [func cosh(Angle2DFloat) -> Float](/documentation/spatial/cosh(_:)-9mmhn)
- [func sin(Angle2DFloat) -> Float](/documentation/spatial/sin(_:)-46su7)
- [func sin(Angle2D) -> Double](/documentation/spatial/sin(_:)-5tddt)
- [func sinh(Angle2D) -> Double](/documentation/spatial/sinh(_:)-4m7ds)
- [func sinh(Angle2DFloat) -> Float](/documentation/spatial/sinh(_:)-8kigy)
- [func tan(Angle2D) -> Double](/documentation/spatial/tan(_:)-1sjgu)
- [func tan(Angle2DFloat) -> Float](/documentation/spatial/tan(_:)-9x99s)
- [func tanh(Angle2D) -> Double](/documentation/spatial/tanh(_:)-1f341)
- [func tanh(Angle2DFloat) -> Float](/documentation/spatial/tanh(_:)-5yozs)

## Protocols

- [Primitive3D](/documentation/spatial/primitive3d)

### Instance properties

- [var isFinite: Bool](/documentation/spatial/primitive3d/isfinite)
- [var isNaN: Bool](/documentation/spatial/primitive3d/isnan)
- [var isZero: Bool](/documentation/spatial/primitive3d/iszero)

### Type properties

- [static var infinity: Self](/documentation/spatial/primitive3d/infinity)
- [static var zero: Self](/documentation/spatial/primitive3d/zero)

### Transforming primitives

- [func apply(AffineTransform3D)](/documentation/spatial/primitive3d/apply(_:)-1nv9y)
- [func apply(ProjectiveTransform3D)](/documentation/spatial/primitive3d/apply(_:)-64cgp)
- [func applying(AffineTransform3D) -> Self](/documentation/spatial/primitive3d/applying(_:)-6264n)
- [func applying(ProjectiveTransform3D) -> Self](/documentation/spatial/primitive3d/applying(_:)-6icvg)
- [func apply(Pose3D)](/documentation/spatial/primitive3d/apply(_:)-4ic73)
- [func applying(Pose3D) -> Self](/documentation/spatial/primitive3d/applying(_:)-5yia)
- [func unapply(AffineTransform3D)](/documentation/spatial/primitive3d/unapply(_:)-4z6og)
- [func unapply(ProjectiveTransform3D)](/documentation/spatial/primitive3d/unapply(_:)-5haxp)
- [func unapplying(AffineTransform3D) -> Self](/documentation/spatial/primitive3d/unapplying(_:)-8ihh5)
- [func unapplying(ProjectiveTransform3D) -> Self](/documentation/spatial/primitive3d/unapplying(_:)-5ppqi)
- [func unapply(Pose3D)](/documentation/spatial/primitive3d/unapply(_:)-2992s)
- [func unapplying(Pose3D) -> Self](/documentation/spatial/primitive3d/unapplying(_:)-37fbg)
- [Rotatable3D](/documentation/spatial/rotatable3d)

### Instance methods

- [func rotate(by: simd_quatd)](/documentation/spatial/rotatable3d/rotate(by:)-usrg)
- [func rotate(by: Rotation3D)](/documentation/spatial/rotatable3d/rotate(by:)-1g3rl)
- [func rotated(by: simd_quatd) -> Self](/documentation/spatial/rotatable3d/rotated(by:)-4gdqe)
- [func rotated(by: Rotation3D) -> Self](/documentation/spatial/rotatable3d/rotated(by:)-7bx4w)
- [Scalable3D](/documentation/spatial/scalable3d)

### Instance methods

- [func scale(by: Size3D)](/documentation/spatial/scalable3d/scale(by:))
- [func scaleBy(x: Double, y: Double, z: Double)](/documentation/spatial/scalable3d/scaleby(x:y:z:))
- [func scaled(by: Size3D) -> Self](/documentation/spatial/scalable3d/scaled(by:))
- [func scaledBy(x: Double, y: Double, z: Double) -> Self](/documentation/spatial/scalable3d/scaledby(x:y:z:))
- [func uniformlyScale(by: Double)](/documentation/spatial/scalable3d/uniformlyscale(by:))
- [func uniformlyScaled(by: Double) -> Self](/documentation/spatial/scalable3d/uniformlyscaled(by:))
- [Shearable3D](/documentation/spatial/shearable3d)

### Instance methods

- [func shear(AxisWithFactors)](/documentation/spatial/shearable3d/shear(_:))
- [func sheared(AxisWithFactors) -> Self](/documentation/spatial/shearable3d/sheared(_:))
- [Translatable3D](/documentation/spatial/translatable3d)

### Instance methods

- [func translate(by: Vector3D)](/documentation/spatial/translatable3d/translate(by:)-6dj5o)
- [func translated(by: Vector3D) -> Self](/documentation/spatial/translatable3d/translated(by:)-5h847)

### Deprecated methods

- [func translate(by: Size3D)](/documentation/spatial/translatable3d/translate(by:)-86nwy)
- [func translated(by: Size3D) -> Self](/documentation/spatial/translatable3d/translated(by:)-9ndur)
- [Volumetric](/documentation/spatial/volumetric)

### Instance properties

- [var size: Size3D](/documentation/spatial/volumetric/size)

### Instance methods

- [func contains(Self) -> Bool](/documentation/spatial/volumetric/contains(_:))
- [func contains(point: Point3D) -> Bool](/documentation/spatial/volumetric/contains(point:))
- [func contains(anyOf: [Point3D]) -> Bool](/documentation/spatial/volumetric/contains(anyof:))
- [func formIntersection(Self)](/documentation/spatial/volumetric/formintersection(_:))
- [func formUnion(Self)](/documentation/spatial/volumetric/formunion(_:))
- [func intersection(Self) -> Self?](/documentation/spatial/volumetric/intersection(_:))
- [func union(Self) -> Self](/documentation/spatial/volumetric/union(_:))

### Deprecated methods

- [func containsAny(of: [Point3D]) -> Bool](/documentation/spatial/volumetric/containsany(of:))
- [ClampableWithinRectProtocol](/documentation/spatial/clampablewithinrectprotocol)

### Instance Methods

- [func clamp(to: Self.Rect)](/documentation/spatial/clampablewithinrectprotocol/clamp(to:))
- [func clamped(to: Self.Rect) -> Self](/documentation/spatial/clampablewithinrectprotocol/clamped(to:))
- [Primitive3DProtocol](/documentation/spatial/primitive3dprotocol)

### Instance Properties

- [var isFinite: Bool](/documentation/spatial/primitive3dprotocol/isfinite)
- [var isNaN: Bool](/documentation/spatial/primitive3dprotocol/isnan)
- [var isZero: Bool](/documentation/spatial/primitive3dprotocol/iszero)

### Instance Methods

- [func apply(Self.Pose)](/documentation/spatial/primitive3dprotocol/apply(_:)-1qcu6)
- [func apply(Self.ProjectiveTransform)](/documentation/spatial/primitive3dprotocol/apply(_:)-3bne6)
- [func apply(Self.AffineTransform)](/documentation/spatial/primitive3dprotocol/apply(_:)-6b1fd)
- [func applying(Self.AffineTransform) -> Self](/documentation/spatial/primitive3dprotocol/applying(_:)-1tt2b)
- [func applying(Self.Pose) -> Self](/documentation/spatial/primitive3dprotocol/applying(_:)-4ylq8)
- [func applying(Self.ProjectiveTransform) -> Self](/documentation/spatial/primitive3dprotocol/applying(_:)-690k5)
- [func unapply(Self.ProjectiveTransform)](/documentation/spatial/primitive3dprotocol/unapply(_:)-22esh)
- [func unapply(Self.AffineTransform)](/documentation/spatial/primitive3dprotocol/unapply(_:)-34afa)
- [func unapply(Self.Pose)](/documentation/spatial/primitive3dprotocol/unapply(_:)-5dfj2)
- [func unapplying(Self.ProjectiveTransform) -> Self](/documentation/spatial/primitive3dprotocol/unapplying(_:)-1px2q)
- [func unapplying(Self.AffineTransform) -> Self](/documentation/spatial/primitive3dprotocol/unapplying(_:)-53rsn)
- [func unapplying(Self.Pose) -> Self](/documentation/spatial/primitive3dprotocol/unapplying(_:)-5fmf2)

### Type Properties

- [static var infinity: Self](/documentation/spatial/primitive3dprotocol/infinity)
- [static var zero: Self](/documentation/spatial/primitive3dprotocol/zero)
- [Rotatable3DProtocol](/documentation/spatial/rotatable3dprotocol)

### Operators

- [static func * (Self.Rotation, Self) -> Self](/documentation/spatial/rotatable3dprotocol/*(_:_:))

### Instance Methods

- [func rotate(by: Self.Quaternion)](/documentation/spatial/rotatable3dprotocol/rotate(by:)-66sot)
- [func rotate(by: Self.Rotation)](/documentation/spatial/rotatable3dprotocol/rotate(by:)-7waub)
- [func rotated(by: Self.Rotation) -> Self](/documentation/spatial/rotatable3dprotocol/rotated(by:)-3xjsw)
- [func rotated(by: Self.Quaternion) -> Self](/documentation/spatial/rotatable3dprotocol/rotated(by:)-4mye4)
- [Scalable3DProtocol](/documentation/spatial/scalable3dprotocol)

### Instance Methods

- [func scale(by: Self.Size)](/documentation/spatial/scalable3dprotocol/scale(by:))
- [func scaleBy(x: Self.Scalar, y: Self.Scalar, z: Self.Scalar)](/documentation/spatial/scalable3dprotocol/scaleby(x:y:z:))
- [func scaled(by: Self.Size) -> Self](/documentation/spatial/scalable3dprotocol/scaled(by:))
- [func scaledBy(x: Self.Scalar, y: Self.Scalar, z: Self.Scalar) -> Self](/documentation/spatial/scalable3dprotocol/scaledby(x:y:z:))
- [func uniformlyScale(by: Self.Scalar)](/documentation/spatial/scalable3dprotocol/uniformlyscale(by:))
- [func uniformlyScaled(by: Self.Scalar) -> Self](/documentation/spatial/scalable3dprotocol/uniformlyscaled(by:))
- [Shearable3DProtocol](/documentation/spatial/shearable3dprotocol)

### Instance Methods

- [func shear(Self.AxisEnumeration)](/documentation/spatial/shearable3dprotocol/shear(_:))
- [func sheared(Self.AxisEnumeration) -> Self](/documentation/spatial/shearable3dprotocol/sheared(_:))
- [SpatialTypeProtocol](/documentation/spatial/spatialtypeprotocol)

### Associated Types

- [AffineTransform](/documentation/spatial/spatialtypeprotocol/affinetransform)
- [AxisEnumeration](/documentation/spatial/spatialtypeprotocol/axisenumeration)
- [Point](/documentation/spatial/spatialtypeprotocol/point)
- [Pose](/documentation/spatial/spatialtypeprotocol/pose)
- [ProjectiveTransform](/documentation/spatial/spatialtypeprotocol/projectivetransform)
- [Quaternion](/documentation/spatial/spatialtypeprotocol/quaternion)
- [Rect](/documentation/spatial/spatialtypeprotocol/rect)
- [Rotation](/documentation/spatial/spatialtypeprotocol/rotation)
- [Scalar](/documentation/spatial/spatialtypeprotocol/scalar)
- [Size](/documentation/spatial/spatialtypeprotocol/size)
- [Vector](/documentation/spatial/spatialtypeprotocol/vector)
- [Transform3DProtocol](/documentation/spatial/transform3dprotocol)

### Initializers

- [init(rotation: Self.Rotation)](/documentation/spatial/transform3dprotocol/init(rotation:))
- [init(scale: Self.Size)](/documentation/spatial/transform3dprotocol/init(scale:))
- [init(scale: Self.Size, rotation: Self.Rotation, translation: Self.Vector)](/documentation/spatial/transform3dprotocol/init(scale:rotation:translation:))
- [init(shear: Self.AxisEnumeration)](/documentation/spatial/transform3dprotocol/init(shear:))
- [init(translation: Self.Vector)](/documentation/spatial/transform3dprotocol/init(translation:))

### Instance Properties

- [var inverse: Self?](/documentation/spatial/transform3dprotocol/inverse)
- [var isIdentity: Bool](/documentation/spatial/transform3dprotocol/isidentity)
- [var isRectilinear: Bool](/documentation/spatial/transform3dprotocol/isrectilinear)
- [var isTranslation: Bool](/documentation/spatial/transform3dprotocol/istranslation)
- [var isUniform: Bool](/documentation/spatial/transform3dprotocol/isuniform)
- [var rotation: Self.Rotation?](/documentation/spatial/transform3dprotocol/rotation)
- [var translation: Self.Vector](/documentation/spatial/transform3dprotocol/translation)

### Instance Methods

- [func concatenating(Self) -> Self](/documentation/spatial/transform3dprotocol/concatenating(_:))
- [func flip(along: Axis3D)](/documentation/spatial/transform3dprotocol/flip(along:))
- [func flipped(along: Axis3D) -> Self](/documentation/spatial/transform3dprotocol/flipped(along:))
- [func isApproximatelyEqual(to: Self, tolerance: Self.Scalar) -> Bool](/documentation/spatial/transform3dprotocol/isapproximatelyequal(to:tolerance:))
- [func isUniform(overDimensions: Dimension3DSet) -> Bool](/documentation/spatial/transform3dprotocol/isuniform(overdimensions:))

### Type Properties

- [static var identity: Self](/documentation/spatial/transform3dprotocol/identity)
- [Translatable3DProtocol](/documentation/spatial/translatable3dprotocol)

### Instance Methods

- [func translate(by: Self.Vector)](/documentation/spatial/translatable3dprotocol/translate(by:))
- [func translated(by: Self.Vector) -> Self](/documentation/spatial/translatable3dprotocol/translated(by:))
- [VolumetricProtocol](/documentation/spatial/volumetricprotocol)

### Instance Properties

- [var size: Self.Size](/documentation/spatial/volumetricprotocol/size)

### Instance Methods

- [func contains(Self) -> Bool](/documentation/spatial/volumetricprotocol/contains(_:))
- [func contains(anyOf: [Self.Point]) -> Bool](/documentation/spatial/volumetricprotocol/contains(anyof:))
- [func contains(point: Self.Point) -> Bool](/documentation/spatial/volumetricprotocol/contains(point:))
- [func formIntersection(Self)](/documentation/spatial/volumetricprotocol/formintersection(_:))
- [func formUnion(Self)](/documentation/spatial/volumetricprotocol/formunion(_:))
- [func intersection(Self) -> Self?](/documentation/spatial/volumetricprotocol/intersection(_:))
- [func union(Self) -> Self](/documentation/spatial/volumetricprotocol/union(_:))

## Macros

- [Macros & Global Variables](/documentation/spatial/spatial-macros)

### Deprecated global variables

- [let x: Axis3D](/documentation/spatial/x)
- [let y: Axis3D](/documentation/spatial/y)
- [let z: Axis3D](/documentation/spatial/z)

## Structures

- [EulerAnglesFloat](/documentation/spatial/euleranglesfloat)

### Initializers

- [init()](/documentation/spatial/euleranglesfloat/init())
- [init(angles: simd_float3, order: __SPEulerAngleOrder)](/documentation/spatial/euleranglesfloat/init(angles:order:))
- [init(x: Angle2DFloat, y: Angle2DFloat, z: Angle2DFloat, order: EulerAngles.Order)](/documentation/spatial/euleranglesfloat/init(x:y:z:order:))

### Instance Properties

- [var angles: simd_float3](/documentation/spatial/euleranglesfloat/angles)
- [var order: __SPEulerAngleOrder](/documentation/spatial/euleranglesfloat/order)

## Enumerations

- [AxisWithFactorsFloat](/documentation/spatial/axiswithfactorsfloat)

### Enumeration Cases

- [case xAxis(yShearFactor: Float, zShearFactor: Float)](/documentation/spatial/axiswithfactorsfloat/xaxis(yshearfactor:zshearfactor:))
- [case yAxis(xShearFactor: Float, zShearFactor: Float)](/documentation/spatial/axiswithfactorsfloat/yaxis(xshearfactor:zshearfactor:))
- [case zAxis(xShearFactor: Float, yShearFactor: Float)](/documentation/spatial/axiswithfactorsfloat/zaxis(xshearfactor:yshearfactor:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
