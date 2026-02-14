# ShaderGraph Documentation

Source: https://sosumi.ai/documentation/shadergraph

---
title: ShaderGraph
source: https://developer.apple.com/documentation/shadergraph
timestamp: 2026-02-13T19:02:07.590Z
---

## Node Categories

- [2D-Procedural](/documentation/shadergraph/2d-procedural)

### Nodes

- [Ramp Horizontal](/documentation/shadergraph/2d-procedural/ramp-horizontal)
- [Ramp Vertical](/documentation/shadergraph/2d-procedural/ramp-vertical)
- [Ramp 4 Corners](/documentation/shadergraph/2d-procedural/ramp-4-corners)
- [Split Horizontal](/documentation/shadergraph/2d-procedural/split-horizontal)
- [Split Vertical](/documentation/shadergraph/2d-procedural/split-vertical)
- [Noise 2D](/documentation/shadergraph/2d-procedural/noise-2d)
- [Cellular Noise 2D](/documentation/shadergraph/2d-procedural/cellular-noise-2d)
- [Worley Noise 2D](/documentation/shadergraph/2d-procedural/worley-noise-2d)
- [2D-Texture](/documentation/shadergraph/2d-texture)

### Nodes

- [Image](/documentation/shadergraph/2d-texture/image)
- [Tiled Image](/documentation/shadergraph/2d-texture/tiled-image)
- [UV Texture](/documentation/shadergraph/2d-texture/uv-texture)
- [Transform 2D](/documentation/shadergraph/2d-texture/transform-2d)
- [3D-Procedural](/documentation/shadergraph/3d-procedural)

### Nodes

- [Noise 3D](/documentation/shadergraph/3d-procedural/noise-3d)
- [Fractal Noise 3D](/documentation/shadergraph/3d-procedural/fractal-noise-3d)
- [Cellular Noise 3D](/documentation/shadergraph/3d-procedural/cellular-noise-3d)
- [Worley Noise 3D](/documentation/shadergraph/3d-procedural/worley-noise-3d)
- [3D-Texture](/documentation/shadergraph/3d-texture)

### Nodes

- [Triplanar Projection](/documentation/shadergraph/3d-texture/triplanar-projection)
- [Adjustment](/documentation/shadergraph/adjustment)

### Nodes

- [Remap](/documentation/shadergraph/adjustment/remap)
- [Smooth Step](/documentation/shadergraph/adjustment/smooth-step)
- [Luminance](/documentation/shadergraph/adjustment/luminance)
- [RGB to HSV](/documentation/shadergraph/adjustment/rgb-to-hsv)
- [HSV to RGB](/documentation/shadergraph/adjustment/hsv-to-rgb)
- [Contrast](/documentation/shadergraph/adjustment/contrast)
- [Range](/documentation/shadergraph/adjustment/range)
- [HSV Adjust](/documentation/shadergraph/adjustment/hsv-adjust)
- [Saturate](/documentation/shadergraph/adjustment/saturate)
- [Step (RealityKit)](/documentation/shadergraph/adjustment/step-(realitykit))
- [Application](/documentation/shadergraph/application)

### Nodes

- [Time (float)](/documentation/shadergraph/application/time-(float))
- [Up Direction](/documentation/shadergraph/application/up-direction)
- [Compositing](/documentation/shadergraph/compositing)

### Nodes

- [Premultiply](/documentation/shadergraph/compositing/premultiply)
- [Unpremultiply](/documentation/shadergraph/compositing/unpremultiply)
- [Additive Mix](/documentation/shadergraph/compositing/additive-mix)
- [Subtractive Mix](/documentation/shadergraph/compositing/subtractive-mix)
- [Difference](/documentation/shadergraph/compositing/difference)
- [Burn](/documentation/shadergraph/compositing/burn)
- [Dodge](/documentation/shadergraph/compositing/dodge)
- [Screen](/documentation/shadergraph/compositing/screen)
- [Overlay](/documentation/shadergraph/compositing/overlay)
- [Disjoint Over](/documentation/shadergraph/compositing/disjoint-over)
- [In](/documentation/shadergraph/compositing/in)
- [Mask](/documentation/shadergraph/compositing/mask)
- [Matte](/documentation/shadergraph/compositing/matte)
- [Out](/documentation/shadergraph/compositing/out)
- [Over](/documentation/shadergraph/compositing/over)
- [Inside](/documentation/shadergraph/compositing/inside)
- [Outside](/documentation/shadergraph/compositing/outside)
- [Mix](/documentation/shadergraph/compositing/mix)
- [Data](/documentation/shadergraph/data)

### Nodes

- [Convert](/documentation/shadergraph/data/convert)
- [Swizzle](/documentation/shadergraph/data/swizzle)
- [Combine 2](/documentation/shadergraph/data/combine-2)
- [Combine 3](/documentation/shadergraph/data/combine-3)
- [Combine 4](/documentation/shadergraph/data/combine-4)
- [Extract](/documentation/shadergraph/data/extract)
- [Separate 2](/documentation/shadergraph/data/separate-2)
- [Separate 3](/documentation/shadergraph/data/separate-3)
- [Separate 4](/documentation/shadergraph/data/separate-4)
- [Primvar Reader](/documentation/shadergraph/data/primvar-reader)
- [Geometric](/documentation/shadergraph/geometric)

### Nodes

- [Position](/documentation/shadergraph/geometric/position)
- [Normal](/documentation/shadergraph/geometric/normal)
- [Tangent](/documentation/shadergraph/geometric/tangent)
- [Bitangent](/documentation/shadergraph/geometric/bitangent)
- [Texture Coordinates](/documentation/shadergraph/geometric/texture-coordinates)
- [Geometry Color](/documentation/shadergraph/geometric/geometry-color)
- [Geometric Property](/documentation/shadergraph/geometric/geometric-property)
- [Reflect (RealityKit)](/documentation/shadergraph/geometric/reflect-(realitykit))
- [Refract (RealityKit)](/documentation/shadergraph/geometric/refract-(realitykit))
- [Logic](/documentation/shadergraph/logic)

### Nodes

- [If Greater](/documentation/shadergraph/logic/if-greater)
- [If Greater Or Equal](/documentation/shadergraph/logic/if-greater-or-equal)
- [If Equal](/documentation/shadergraph/logic/if-equal)
- [Switch](/documentation/shadergraph/logic/switch)
- [And (RealityKit)](/documentation/shadergraph/logic/and-(realitykit))
- [Or (RealityKit)](/documentation/shadergraph/logic/or-(realitykit))
- [XOR (RealityKit)](/documentation/shadergraph/logic/xor-(realitykit))
- [Not (RealityKit)](/documentation/shadergraph/logic/not-(realitykit))
- [Select (RealityKit)](/documentation/shadergraph/logic/select-(realitykit))
- [Multiply Add 24 (RealityKit)](/documentation/shadergraph/realitykit/multiply-add-24-(realitykit))
- [Multiply 24 (RealityKit)](/documentation/shadergraph/realitykit/multiply-24-(realitykit))
- [Material](/documentation/shadergraph/material)

### Nodes

- [Node Graph](/documentation/shadergraph/material/node-graph)
- [Math](/documentation/shadergraph/math)

### Nodes

- [Add](/documentation/shadergraph/math/add)
- [Subtract](/documentation/shadergraph/math/subtract)
- [Multiply](/documentation/shadergraph/math/multiply)
- [Divide](/documentation/shadergraph/math/divide)
- [Modulo](/documentation/shadergraph/math/modulo)
- [Abs](/documentation/shadergraph/math/abs)
- [Floor](/documentation/shadergraph/math/floor)
- [Ceiling](/documentation/shadergraph/math/ceiling)
- [Power](/documentation/shadergraph/math/power)
- [Sin](/documentation/shadergraph/math/sin)
- [Cos](/documentation/shadergraph/math/cos)
- [Tan](/documentation/shadergraph/math/tan)
- [Asin](/documentation/shadergraph/math/asin)
- [Acos](/documentation/shadergraph/math/acos)
- [Atan2](/documentation/shadergraph/math/atan2)
- [Square Root](/documentation/shadergraph/math/square-root)
- [Natural Log](/documentation/shadergraph/math/natural-log)
- [Exp](/documentation/shadergraph/math/exp)
- [Sign](/documentation/shadergraph/math/sign)
- [Clamp](/documentation/shadergraph/math/clamp)
- [Min](/documentation/shadergraph/math/min)
- [Max](/documentation/shadergraph/math/max)
- [Normalize](/documentation/shadergraph/math/normalize)
- [Magnitude](/documentation/shadergraph/math/magnitude)
- [Dot Product](/documentation/shadergraph/math/dot-product)
- [Cross Product](/documentation/shadergraph/math/cross-product)
- [Transform Point](/documentation/shadergraph/math/transform-point)
- [Transform Vector](/documentation/shadergraph/math/transform-vector)
- [Transform Normal](/documentation/shadergraph/math/transform-normal)
- [Transform Matrix](/documentation/shadergraph/math/transform-matrix)
- [Transpose](/documentation/shadergraph/math/transpose)
- [Determinant](/documentation/shadergraph/math/determinant)
- [Invert Matrix](/documentation/shadergraph/math/invert-matrix)
- [Rotate 2D](/documentation/shadergraph/math/rotate-2d)
- [Rotate 3D](/documentation/shadergraph/math/rotate-3d)
- [Place 2D](/documentation/shadergraph/math/place-2d)
- [Round](/documentation/shadergraph/math/round)
- [Safe Power](/documentation/shadergraph/math/safe-power)
- [Normal Map](/documentation/shadergraph/math/normal-map)
- [Fractional (RealityKit)](/documentation/shadergraph/math/fractional-(realitykit))
- [One Minus (RealityKit)](/documentation/shadergraph/math/one-minus-(realitykit))
- [Normal Map Decode](/documentation/shadergraph/math/normal-map-decode)
- [Max3 (RealityKit)](/documentation/shadergraph/math/max3-(realitykit))
- [Min3 (RealityKit)](/documentation/shadergraph/math/min3-(realitykit))
- [Fractional (RealityKit)](/documentation/shadergraph/math/fractional-(realitykit))
- [Inverse Hyperbolic Cos](/documentation/shadergraph/math/inverse-hyperbolic-cos)
- [Inverse Hyperbolic Sin](/documentation/shadergraph/math/inverse-hyperbolic-sin)
- [Atan](/documentation/shadergraph/math/atan)
- [Inverse Hyperbolic Tan](/documentation/shadergraph/math/inverse-hyperbolic-tan)
- [Copy Sign (RealityKit)](/documentation/shadergraph/math/copy-sign-(realitykit))
- [Hyperbolic Cos](/documentation/shadergraph/math/hyperbolic-cos)
- [Cos Pi (RealityKit)](/documentation/shadergraph/math/cos-pi-(realitykit))
- [Exponential 2 (RealityKit)](/documentation/shadergraph/math/exponential-2-(realitykit))
- [Exponential 10 (RealityKit)](/documentation/shadergraph/math/exponential-10-(realitykit))

### Subscripts

- [Distance (RealityKit)](/documentation/shadergraph/math/distance-(realitykit))
- [Distance Square (RealityKit)](/documentation/shadergraph/math/distance-square-(realitykit))
- [Fused Multiply-Add (RealityKit)](/documentation/shadergraph/math/fused-multiply-add-(realitykit))
- [Hyperbolic Sin](/documentation/shadergraph/math/hyperbolic-sin)
- [Hyperbolic Tan](/documentation/shadergraph/math/hyperbolic-tan)
- [Log 10](/documentation/shadergraph/math/log-10)
- [Log 2](/documentation/shadergraph/math/log-2)
- [Magnitude Square (RealityKit)](/documentation/shadergraph/math/magnitude-square-(realitykit))
- [Median3 (RealityKit)](/documentation/shadergraph/math/median3-(realitykit))
- [Modulo (RealityKit)](/documentation/shadergraph/math/modulo-(realitykit))
- [Reciprocal Square Root (RealityKit)](/documentation/shadergraph/math/reciprocal-square-root-(realitykit))
- [Sin Pi (RealityKit)](/documentation/shadergraph/math/sin-pi-(realitykit))
- [Tan Pi (RealityKit)](/documentation/shadergraph/math/tan-pi-(realitykit))
- [Truncate (RealityKit)](/documentation/shadergraph/math/truncate-(realitykit))
- [Organization](/documentation/shadergraph/organization)

### Nodes

- [Dot](/documentation/shadergraph/organization/dot)
- [Procedural](/documentation/shadergraph/procedural)

### Nodes

- [Float](/documentation/shadergraph/procedural/float)
- [Color3 (Float)](/documentation/shadergraph/procedural/color3-(float))
- [Color4 (Float)](/documentation/shadergraph/procedural/color4-(float))
- [Vector2 (Float)](/documentation/shadergraph/procedural/vector2-(float))
- [Vector3 (Float)](/documentation/shadergraph/procedural/vector3-(float))
- [Vector4 (Float)](/documentation/shadergraph/procedural/vector4-(float))
- [Boolean](/documentation/shadergraph/procedural/boolean)
- [Integer](/documentation/shadergraph/procedural/integer)
- [Matrix3x3 (Float)](/documentation/shadergraph/procedural/matrix3x3-(float))
- [Matrix4x4 (Float)](/documentation/shadergraph/procedural/matrix4x4-(float))
- [String](/documentation/shadergraph/procedural/string)
- [Image File](/documentation/shadergraph/procedural/image-file)
- [Half](/documentation/shadergraph/procedural/half)
- [Vector2 (Half)](/documentation/shadergraph/procedural/vector2-(half))
- [Vector3 (Half)](/documentation/shadergraph/procedural/vector3-(half))
- [Vector4 (Half)](/documentation/shadergraph/procedural/vector4-(half))
- [Matrix2x2 (Float)](/documentation/shadergraph/procedural/matrix2x2-(float))
- [Integer2](/documentation/shadergraph/procedural/integer2)
- [Integer3](/documentation/shadergraph/procedural/integer3)
- [Integer4](/documentation/shadergraph/procedural/integer4)
- [RealityKit](/documentation/shadergraph/realitykit)

### Nodes

- [Unlit Surface (RealityKit)](/documentation/shadergraph/realitykit/unlit-surface-(realitykit))
- [PBR Surface (RealityKit)](/documentation/shadergraph/realitykit/pbr-surface-(realitykit))
- [Occlusion Surface (RealityKit)](/documentation/shadergraph/realitykit/occlusion-surface-(realitykit))
- [Shadow Receiving Occlusion Surface (RealityKit)](/documentation/shadergraph/realitykit/shadow-receiving-occlusion-surface-(realitykit))
- [View Direction (RealityKit)](/documentation/shadergraph/realitykit/view-direction-(realitykit))
- [Camera Position (RealityKit)](/documentation/shadergraph/realitykit/camera-position-(realitykit))
- [Geometry Modifier Model To World (RealityKit)](/documentation/shadergraph/realitykit/geometry-modifier-model-to-world-(realitykit))
- [Geometry Modifier World To Model (RealityKit)](/documentation/shadergraph/realitykit/geometry-modifier-world-to-model-(realitykit))
- [Geometry Modifier Normal To World (RealityKit)](/documentation/shadergraph/realitykit/geometry-modifier-normal-to-world-(realitykit))
- [Geometry Modifier Model To View (RealityKit)](/documentation/shadergraph/realitykit/geometry-modifier-model-to-view-(realitykit))
- [Geometry Modifier View To Projection (RealityKit)](/documentation/shadergraph/realitykit/geometry-modifier-view-to-projection-(realitykit))
- [Geometry Modifier Projection To View (RealityKit)](/documentation/shadergraph/realitykit/geometry-modifier-projection-to-view-(realitykit))
- [Geometry Modifier Vertex ID (RealityKit)](/documentation/shadergraph/realitykit/geometry-modifier-vertex-id-(realitykit))
- [Surface Model To World (RealityKit)](/documentation/shadergraph/realitykit/surface-model-to-world-(realitykit))
- [Surface Model To View (RealityKit)](/documentation/shadergraph/realitykit/surface-model-to-view-(realitykit))
- [Surface World To View (RealityKit)](/documentation/shadergraph/realitykit/surface-world-to-view-(realitykit))
- [Surface View To Projection (RealityKit)](/documentation/shadergraph/realitykit/surface-view-to-projection-(realitykit))
- [Surface Projection To View (RealityKit)](/documentation/shadergraph/realitykit/surface-projection-to-view-(realitykit))
- [Surface Screen Position (RealityKit)](/documentation/shadergraph/realitykit/surface-screen-position-(realitykit))
- [Surface View Direction (RealityKit)](/documentation/shadergraph/realitykit/surface-view-direction-(realitykit))
- [Environment Radiance (RealityKit)](/documentation/shadergraph/realitykit/environment-radiance-(realitykit))
- [Hover State (RealityKit)](/documentation/shadergraph/realitykit/hover-state-(realitykit))
- [Blurred Background (RealityKit)](/documentation/shadergraph/realitykit/blurred-background-(realitykit))
- [Geometry Modifier (RealityKit)](/documentation/shadergraph/realitykit/geometry-modifier-(realitykit))
- [Camera Index Switch (RealityKit)](/documentation/shadergraph/realitykit/camera-index-switch-(realitykit))
- [Image 2D (RealityKit)](/documentation/shadergraph/realitykit/image-2d-(realitykit))
- [Image 2D LOD (RealityKit)](/documentation/shadergraph/realitykit/image-2d-lod-(realitykit))
- [Image 2D Gradient (RealityKit)](/documentation/shadergraph/realitykit/image-2d-gradient-(realitykit))
- [Image 2D Pixel (RealityKit)](/documentation/shadergraph/realitykit/image-2d-pixel-(realitykit))
- [Image 2D LOD Pixel (RealityKit)](/documentation/shadergraph/realitykit/image-2d-lod-pixel-(realitykit))
- [Image 2D Gradient Pixel (RealityKit)](/documentation/shadergraph/realitykit/image-2d-gradient-pixel-(realitykit))
- [Cube Image (RealityKit)](/documentation/shadergraph/realitykit/cube-image-(realitykit))
- [Cube Image LOD (RealityKit)](/documentation/shadergraph/realitykit/cube-image-lod-(realitykit))
- [Cube Image Gradient (RealityKit)](/documentation/shadergraph/realitykit/cube-image-gradient-(realitykit))
- [Image 2D Read (RealityKit)](/documentation/shadergraph/realitykit/image-2d-read-(realitykit))
- [Image 3D (RealityKit)](/documentation/shadergraph/realitykit/image-3d-(realitykit))
- [Image 3D LOD (RealityKit)](/documentation/shadergraph/realitykit/image-3d-lod-(realitykit))
- [Image 3D Gradient (RealityKit)](/documentation/shadergraph/realitykit/image-3d-gradient-(realitykit))
- [Image 3D Pixel (RealityKit)](/documentation/shadergraph/realitykit/image-3d-pixel-(realitykit))
- [Image 3D LOD Pixel (RealityKit)](/documentation/shadergraph/realitykit/image-3d-lod-pixel-(realitykit))
- [Image 3D Gradient Pixel (RealityKit)](/documentation/shadergraph/realitykit/image-3d-gradient-pixel-(realitykit))
- [Image 2D Array (RealityKit)](/documentation/shadergraph/realitykit/image-2d-array-(realitykit))
- [Image 2D Array LOD (RealityKit)](/documentation/shadergraph/realitykit/image-2d-array-lod-(realitykit))
- [Image 2D Array Gradient (RealityKit)](/documentation/shadergraph/realitykit/image-2d-array-gradient-(realitykit))
- [Image 2D Array Pixel (RealityKit)](/documentation/shadergraph/realitykit/image-2d-array-pixel-(realitykit))
- [Image 2D Array LOD Pixel (RealityKit)](/documentation/shadergraph/realitykit/image-2d-array-lod-pixel-(realitykit))
- [Image 2D Array Gradient Pixel (RealityKit)](/documentation/shadergraph/realitykit/image-2d-array-gradient-pixel-(realitykit))
- [Image 2D Array Read (RealityKit)](/documentation/shadergraph/realitykit/image-2d-array-read-(realitykit))
- [Image 3D Read (RealityKit)](/documentation/shadergraph/realitykit/image-3d-read-(realitykit))
- [Screen-Space X Partial Derivative (RealityKit)](/documentation/shadergraph/realitykit/screen-space-x-partial-derivative-(realitykit))
- [Screen-Space Y Partial Derivative (RealityKit)](/documentation/shadergraph/realitykit/screen-space-y-partial-derivative-(realitykit))
- [Absolute Derivatives Sum (RealityKit)](/documentation/shadergraph/realitykit/absolute-derivatives-sum-(realitykit))
- [Power Positive (RealityKit)](/documentation/shadergraph/realitykit/power-positive-(realitykit))
- [Round Integral (RealityKit)](/documentation/shadergraph/realitykit/round-integral-(realitykit))
- [Reflection Diffuse (RealityKit)](/documentation/shadergraph/realitykit/reflection-diffuse-(realitykit))
- [Reflection Specular (RealityKit)](/documentation/shadergraph/realitykit/reflection-specular-(realitykit))
- [Fortran Difference and Minimum (RealityKit)](/documentation/shadergraph/realitykit/fortran-difference-and-minimum-(realitykit))
- [Is Finite (RealityKit)](/documentation/shadergraph/realitykit/is-finite-(realitykit))
- [Is Infinite (RealityKit)](/documentation/shadergraph/realitykit/is-infinite-(realitykit))
- [Is Not a Number (RealityKit)](/documentation/shadergraph/realitykit/is-not-a-number-(realitykit))
- [Is Normal (RealityKit)](/documentation/shadergraph/realitykit/is-normal-(realitykit))
- [Is Ordered (RealityKit)](/documentation/shadergraph/realitykit/is-ordered-(realitykit))
- [Is Unordered (RealityKit)](/documentation/shadergraph/realitykit/is-unordered-(realitykit))
- [Sign Bit (RealityKit)](/documentation/shadergraph/realitykit/sign-bit-(realitykit))

### Subscripts

- [Multiply 24 (RealityKit)](/documentation/shadergraph/realitykit/multiply-24-(realitykit))
- [Multiply Add 24 (RealityKit)](/documentation/shadergraph/realitykit/multiply-add-24-(realitykit))
- [Surface](/documentation/shadergraph/surface)

### Nodes

- [Preview Surface](/documentation/shadergraph/surface/preview-surface)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
