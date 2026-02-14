# simd Documentation

Source: https://sosumi.ai/documentation/simd

---
title: simd
source: https://developer.apple.com/documentation/simd
timestamp: 2026-02-13T19:02:15.060Z
---

## Structures

- [simd_double2x2](/documentation/simd/simd_double2x2)

### Initializers

- [init()](/documentation/simd/simd_double2x2/init())
- [init(Double)](/documentation/simd/simd_double2x2/init(_:)-3kbjz)
- [init(diagonal: SIMD2<Double>)](/documentation/simd/simd_double2x2/init(diagonal:))
- [init([SIMD2<Double>])](/documentation/simd/simd_double2x2/init(_:)-6yq0z)
- [init(SIMD2<Double>, SIMD2<Double>)](/documentation/simd/simd_double2x2/init(_:_:))
- [init(columns: (simd_double2, simd_double2))](/documentation/simd/simd_double2x2/init(columns:))
- [init(rows: [SIMD2<Double>])](/documentation/simd/simd_double2x2/init(rows:))

### Matrix Constants

- [let matrix_identity_double2x2: simd_double2x2](/documentation/simd/matrix_identity_double2x2)

### Matrix Properties

- [var determinant: Double](/documentation/simd/simd_double2x2/determinant)
- [var inverse: simd_double2x2](/documentation/simd/simd_double2x2/inverse)
- [var transpose: double2x2](/documentation/simd/simd_double2x2/transpose)
- [var columns: (simd_double2, simd_double2)](/documentation/simd/simd_double2x2/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_double2, simd_double2) -> simd_double2x2](/documentation/simd/simd_matrix(_:_:)-938tb)
- [func simd_matrix_from_rows(simd_double2, simd_double2) -> simd_double2x2](/documentation/simd/simd_matrix_from_rows(_:_:)-368td)
- [func matrix_from_rows(SIMD2<Double>, SIMD2<Double>) -> simd_double2x2](/documentation/simd/matrix_from_rows(_:_:)-1w56v)

### Element Access

- [subscript(Int) -> SIMD2<Double>](/documentation/simd/simd_double2x2/subscript(_:))
- [subscript(Int, Int) -> Double](/documentation/simd/simd_double2x2/subscript(_:_:))

### Type Aliases

- [double2x2](/documentation/simd/double2x2)
- [matrix_double2x2](/documentation/simd/matrix_double2x2)

### Deprecated Symbols

- [func matrix_invert(simd_double2x2) -> simd_double2x2](/documentation/simd/matrix_invert(_:)-nkj5)
- [func matrix_equal(simd_double2x2, simd_double2x2) -> Bool](/documentation/simd/matrix_equal(_:_:)-4claa)
- [func matrix_from_diagonal(SIMD2<Double>) -> simd_double2x2](/documentation/simd/matrix_from_diagonal(_:)-7i8pm)
- [func matrix_determinant(simd_double2x2) -> Double](/documentation/simd/matrix_determinant(_:)-7kglv)
- [func matrix_from_columns(SIMD2<Double>, SIMD2<Double>) -> simd_double2x2](/documentation/simd/matrix_from_columns(_:_:)-37jug)
- [func matrix_transpose(simd_double2x2) -> double2x2](/documentation/simd/matrix_transpose(_:)-6qaez)
- [init(simd_double2x2)](/documentation/simd/simd_double2x2/init(_:)-9vxjx)
- [var cmatrix: simd_double2x2](/documentation/simd/simd_double2x2/cmatrix)

### Operators

- [static func * (simd_double2x2, Double) -> simd_double2x2](/documentation/simd/simd_double2x2/*(_:_:)-34mwe)
- [static func * (simd_double2x2, SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/simd_double2x2/*(_:_:)-4srge)
- [static func * (simd_double2x2, double2x2) -> double2x2](/documentation/simd/simd_double2x2/*(_:_:)-4x1rs)
- [static func * (simd_double2x2, double4x2) -> double4x2](/documentation/simd/simd_double2x2/*(_:_:)-6vah1)
- [static func * (simd_double2x2, double3x2) -> double3x2](/documentation/simd/simd_double2x2/*(_:_:)-86p1t)
- [static func * (SIMD2<Double>, simd_double2x2) -> SIMD2<Double>](/documentation/simd/simd_double2x2/*(_:_:)-mvy8)
- [static func * (Double, simd_double2x2) -> simd_double2x2](/documentation/simd/simd_double2x2/*(_:_:)-xb7z)
- [static func *= (inout simd_double2x2, Double)](/documentation/simd/simd_double2x2/*=(_:_:)-76lel)
- [static func *= (inout simd_double2x2, double2x2)](/documentation/simd/simd_double2x2/*=(_:_:)-99yuu)
- [static func + (simd_double2x2, simd_double2x2) -> simd_double2x2](/documentation/simd/simd_double2x2/+(_:_:))
- [static func += (inout simd_double2x2, simd_double2x2)](/documentation/simd/simd_double2x2/+=(_:_:))
- [static func - (simd_double2x2) -> simd_double2x2](/documentation/simd/simd_double2x2/-(_:))
- [static func - (simd_double2x2, simd_double2x2) -> simd_double2x2](/documentation/simd/simd_double2x2/-(_:_:))
- [static func -= (inout simd_double2x2, simd_double2x2)](/documentation/simd/simd_double2x2/-=(_:_:))
- [simd_double2x3](/documentation/simd/simd_double2x3)

### Initializers

- [init()](/documentation/simd/simd_double2x3/init())
- [init(Double)](/documentation/simd/simd_double2x3/init(_:)-6xclm)
- [init(diagonal: SIMD2<Double>)](/documentation/simd/simd_double2x3/init(diagonal:))
- [init([SIMD3<Double>])](/documentation/simd/simd_double2x3/init(_:)-6n7k)
- [init(SIMD3<Double>, SIMD3<Double>)](/documentation/simd/simd_double2x3/init(_:_:))
- [init(columns: (simd_double3, simd_double3))](/documentation/simd/simd_double2x3/init(columns:))
- [init(rows: [SIMD2<Double>])](/documentation/simd/simd_double2x3/init(rows:))

### Matrix Properties

- [var transpose: double3x2](/documentation/simd/simd_double2x3/transpose)
- [var columns: (simd_double3, simd_double3)](/documentation/simd/simd_double2x3/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_double3, simd_double3) -> simd_double2x3](/documentation/simd/simd_matrix(_:_:)-86soe)
- [func simd_matrix_from_rows(simd_double2, simd_double2, simd_double2) -> simd_double2x3](/documentation/simd/simd_matrix_from_rows(_:_:_:)-96jbn)
- [func matrix_from_rows(SIMD2<Double>, SIMD2<Double>, SIMD2<Double>) -> simd_double2x3](/documentation/simd/matrix_from_rows(_:_:_:)-2ar1l)

### Element Access

- [subscript(Int) -> SIMD3<Double>](/documentation/simd/simd_double2x3/subscript(_:))
- [subscript(Int, Int) -> Double](/documentation/simd/simd_double2x3/subscript(_:_:))

### Type Aliases

- [double2x3](/documentation/simd/double2x3)
- [matrix_double2x3](/documentation/simd/matrix_double2x3)

### Deprecated Symbols

- [func matrix_equal(simd_double2x3, simd_double2x3) -> Bool](/documentation/simd/matrix_equal(_:_:)-52vds)
- [func matrix_from_columns(SIMD3<Double>, SIMD3<Double>) -> simd_double2x3](/documentation/simd/matrix_from_columns(_:_:)-61w2n)
- [func matrix_transpose(simd_double3x2) -> double2x3](/documentation/simd/matrix_transpose(_:)-97k0o)
- [init(simd_double2x3)](/documentation/simd/simd_double2x3/init(_:)-98rcw)
- [var cmatrix: simd_double2x3](/documentation/simd/simd_double2x3/cmatrix)

### Operators

- [static func * (simd_double2x3, SIMD2<Double>) -> SIMD3<Double>](/documentation/simd/simd_double2x3/*(_:_:)-26bpe)
- [static func * (simd_double2x3, double3x2) -> double3x3](/documentation/simd/simd_double2x3/*(_:_:)-2qo9o)
- [static func * (simd_double2x3, Double) -> simd_double2x3](/documentation/simd/simd_double2x3/*(_:_:)-3li3r)
- [static func * (simd_double2x3, double2x2) -> double2x3](/documentation/simd/simd_double2x3/*(_:_:)-4bwlw)
- [static func * (Double, simd_double2x3) -> simd_double2x3](/documentation/simd/simd_double2x3/*(_:_:)-559m0)
- [static func * (SIMD3<Double>, simd_double2x3) -> SIMD2<Double>](/documentation/simd/simd_double2x3/*(_:_:)-8rxeu)
- [static func * (simd_double2x3, double4x2) -> double4x3](/documentation/simd/simd_double2x3/*(_:_:)-919bm)
- [static func *= (inout simd_double2x3, double2x2)](/documentation/simd/simd_double2x3/*=(_:_:)-3lbnh)
- [static func *= (inout simd_double2x3, Double)](/documentation/simd/simd_double2x3/*=(_:_:)-9b91z)
- [static func + (simd_double2x3, simd_double2x3) -> simd_double2x3](/documentation/simd/simd_double2x3/+(_:_:))
- [static func += (inout simd_double2x3, simd_double2x3)](/documentation/simd/simd_double2x3/+=(_:_:))
- [static func - (simd_double2x3) -> simd_double2x3](/documentation/simd/simd_double2x3/-(_:))
- [static func - (simd_double2x3, simd_double2x3) -> simd_double2x3](/documentation/simd/simd_double2x3/-(_:_:))
- [static func -= (inout simd_double2x3, simd_double2x3)](/documentation/simd/simd_double2x3/-=(_:_:))
- [simd_double2x4](/documentation/simd/simd_double2x4)

### Initializers

- [init()](/documentation/simd/simd_double2x4/init())
- [init(Double)](/documentation/simd/simd_double2x4/init(_:)-71dee)
- [init(diagonal: SIMD2<Double>)](/documentation/simd/simd_double2x4/init(diagonal:))
- [init([SIMD4<Double>])](/documentation/simd/simd_double2x4/init(_:)-6lqav)
- [init(SIMD4<Double>, SIMD4<Double>)](/documentation/simd/simd_double2x4/init(_:_:))
- [init(columns: (simd_double4, simd_double4))](/documentation/simd/simd_double2x4/init(columns:))
- [init(rows: [SIMD2<Double>])](/documentation/simd/simd_double2x4/init(rows:))

### Matrix Properties

- [var transpose: double4x2](/documentation/simd/simd_double2x4/transpose)
- [var columns: (simd_double4, simd_double4)](/documentation/simd/simd_double2x4/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_double4, simd_double4) -> simd_double2x4](/documentation/simd/simd_matrix(_:_:)-7hafe)
- [func simd_matrix_from_rows(simd_double2, simd_double2, simd_double2, simd_double2) -> simd_double2x4](/documentation/simd/simd_matrix_from_rows(_:_:_:_:)-851r7)
- [func matrix_from_rows(SIMD2<Double>, SIMD2<Double>, SIMD2<Double>, SIMD2<Double>) -> simd_double2x4](/documentation/simd/matrix_from_rows(_:_:_:_:)-897qw)

### Element Access

- [subscript(Int) -> SIMD4<Double>](/documentation/simd/simd_double2x4/subscript(_:))
- [subscript(Int, Int) -> Double](/documentation/simd/simd_double2x4/subscript(_:_:))

### Type Aliases

- [double2x4](/documentation/simd/double2x4)
- [matrix_double2x4](/documentation/simd/matrix_double2x4)

### Deprecated Symbols

- [func matrix_equal(simd_double2x4, simd_double2x4) -> Bool](/documentation/simd/matrix_equal(_:_:)-1dcgx)
- [func matrix_from_columns(SIMD4<Double>, SIMD4<Double>) -> simd_double2x4](/documentation/simd/matrix_from_columns(_:_:)-9q8xb)
- [func matrix_transpose(simd_double4x2) -> double2x4](/documentation/simd/matrix_transpose(_:)-bpqg)
- [init(simd_double2x4)](/documentation/simd/simd_double2x4/init(_:)-6ssjo)
- [var cmatrix: simd_double2x4](/documentation/simd/simd_double2x4/cmatrix)

### Operators

- [static func * (simd_double2x4, double3x2) -> double3x4](/documentation/simd/simd_double2x4/*(_:_:)-2rc47)
- [static func * (simd_double2x4, double2x2) -> double2x4](/documentation/simd/simd_double2x4/*(_:_:)-3croh)
- [static func * (simd_double2x4, SIMD2<Double>) -> SIMD4<Double>](/documentation/simd/simd_double2x4/*(_:_:)-4f5rx)
- [static func * (SIMD4<Double>, simd_double2x4) -> SIMD2<Double>](/documentation/simd/simd_double2x4/*(_:_:)-4iash)
- [static func * (simd_double2x4, Double) -> simd_double2x4](/documentation/simd/simd_double2x4/*(_:_:)-59wcu)
- [static func * (simd_double2x4, double4x2) -> double4x4](/documentation/simd/simd_double2x4/*(_:_:)-8judh)
- [static func * (Double, simd_double2x4) -> simd_double2x4](/documentation/simd/simd_double2x4/*(_:_:)-98679)
- [static func *= (inout simd_double2x4, Double)](/documentation/simd/simd_double2x4/*=(_:_:)-45oag)
- [static func *= (inout simd_double2x4, double2x2)](/documentation/simd/simd_double2x4/*=(_:_:)-57wbl)
- [static func + (simd_double2x4, simd_double2x4) -> simd_double2x4](/documentation/simd/simd_double2x4/+(_:_:))
- [static func += (inout simd_double2x4, simd_double2x4)](/documentation/simd/simd_double2x4/+=(_:_:))
- [static func - (simd_double2x4) -> simd_double2x4](/documentation/simd/simd_double2x4/-(_:))
- [static func - (simd_double2x4, simd_double2x4) -> simd_double2x4](/documentation/simd/simd_double2x4/-(_:_:))
- [static func -= (inout simd_double2x4, simd_double2x4)](/documentation/simd/simd_double2x4/-=(_:_:))
- [simd_double3x2](/documentation/simd/simd_double3x2)

### Initializers

- [init()](/documentation/simd/simd_double3x2/init())
- [init(Double)](/documentation/simd/simd_double3x2/init(_:)-6r1mr)
- [init(diagonal: SIMD2<Double>)](/documentation/simd/simd_double3x2/init(diagonal:))
- [init([SIMD2<Double>])](/documentation/simd/simd_double3x2/init(_:)-9euf0)
- [init(SIMD2<Double>, SIMD2<Double>, SIMD2<Double>)](/documentation/simd/simd_double3x2/init(_:_:_:))
- [init(columns: (simd_double2, simd_double2, simd_double2))](/documentation/simd/simd_double3x2/init(columns:))
- [init(rows: [SIMD3<Double>])](/documentation/simd/simd_double3x2/init(rows:))

### Matrix Properties

- [var transpose: double2x3](/documentation/simd/simd_double3x2/transpose)
- [var columns: (simd_double2, simd_double2, simd_double2)](/documentation/simd/simd_double3x2/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_double2, simd_double2, simd_double2) -> simd_double3x2](/documentation/simd/simd_matrix(_:_:_:)-59y1c)
- [func simd_matrix_from_rows(simd_double3, simd_double3) -> simd_double3x2](/documentation/simd/simd_matrix_from_rows(_:_:)-7mxf9)
- [func matrix_from_rows(SIMD3<Double>, SIMD3<Double>) -> simd_double3x2](/documentation/simd/matrix_from_rows(_:_:)-630eh)

### Element Access

- [subscript(Int) -> SIMD2<Double>](/documentation/simd/simd_double3x2/subscript(_:))
- [subscript(Int, Int) -> Double](/documentation/simd/simd_double3x2/subscript(_:_:))

### Type Aliases

- [double3x2](/documentation/simd/double3x2)
- [matrix_double3x2](/documentation/simd/matrix_double3x2)

### Deprecated Symbols

- [func matrix_equal(simd_double3x2, simd_double3x2) -> Bool](/documentation/simd/matrix_equal(_:_:)-3dnu)
- [func matrix_from_columns(SIMD2<Double>, SIMD2<Double>, SIMD2<Double>) -> simd_double3x2](/documentation/simd/matrix_from_columns(_:_:_:)-9wapk)
- [func matrix_transpose(simd_double2x3) -> double3x2](/documentation/simd/matrix_transpose(_:)-7ueg2)
- [init(simd_double3x2)](/documentation/simd/simd_double3x2/init(_:)-6yyfq)
- [var cmatrix: simd_double3x2](/documentation/simd/simd_double3x2/cmatrix)

### Operators

- [static func * (SIMD2<Double>, simd_double3x2) -> SIMD3<Double>](/documentation/simd/simd_double3x2/*(_:_:)-1hwgh)
- [static func * (Double, simd_double3x2) -> simd_double3x2](/documentation/simd/simd_double3x2/*(_:_:)-1i31n)
- [static func * (simd_double3x2, double3x3) -> double3x2](/documentation/simd/simd_double3x2/*(_:_:)-205gc)
- [static func * (simd_double3x2, double2x3) -> double2x2](/documentation/simd/simd_double3x2/*(_:_:)-55cki)
- [static func * (simd_double3x2, double4x3) -> double4x2](/documentation/simd/simd_double3x2/*(_:_:)-71omv)
- [static func * (simd_double3x2, Double) -> simd_double3x2](/documentation/simd/simd_double3x2/*(_:_:)-8b0gm)
- [static func * (simd_double3x2, SIMD3<Double>) -> SIMD2<Double>](/documentation/simd/simd_double3x2/*(_:_:)-8sxw1)
- [static func *= (inout simd_double3x2, Double)](/documentation/simd/simd_double3x2/*=(_:_:)-65soi)
- [static func *= (inout simd_double3x2, double3x3)](/documentation/simd/simd_double3x2/*=(_:_:)-7jk10)
- [static func + (simd_double3x2, simd_double3x2) -> simd_double3x2](/documentation/simd/simd_double3x2/+(_:_:))
- [static func += (inout simd_double3x2, simd_double3x2)](/documentation/simd/simd_double3x2/+=(_:_:))
- [static func - (simd_double3x2) -> simd_double3x2](/documentation/simd/simd_double3x2/-(_:))
- [static func - (simd_double3x2, simd_double3x2) -> simd_double3x2](/documentation/simd/simd_double3x2/-(_:_:))
- [static func -= (inout simd_double3x2, simd_double3x2)](/documentation/simd/simd_double3x2/-=(_:_:))
- [simd_double3x3](/documentation/simd/simd_double3x3)

### Initializers

- [init()](/documentation/simd/simd_double3x3/init())
- [init(Double)](/documentation/simd/simd_double3x3/init(_:)-6qq5k)
- [init(diagonal: SIMD3<Double>)](/documentation/simd/simd_double3x3/init(diagonal:))
- [init([SIMD3<Double>])](/documentation/simd/simd_double3x3/init(_:)-6kw2p)
- [init(simd_quatd)](/documentation/simd/simd_double3x3/init(_:)-9wyb6)
- [init(SIMD3<Double>, SIMD3<Double>, SIMD3<Double>)](/documentation/simd/simd_double3x3/init(_:_:_:))
- [init(columns: (simd_double3, simd_double3, simd_double3))](/documentation/simd/simd_double3x3/init(columns:))
- [init(rows: [SIMD3<Double>])](/documentation/simd/simd_double3x3/init(rows:))

### Matrix Constants

- [let matrix_identity_double3x3: simd_double3x3](/documentation/simd/matrix_identity_double3x3)

### Matrix Properties

- [var determinant: Double](/documentation/simd/simd_double3x3/determinant)
- [var inverse: simd_double3x3](/documentation/simd/simd_double3x3/inverse)
- [var transpose: double3x3](/documentation/simd/simd_double3x3/transpose)
- [var columns: (simd_double3, simd_double3, simd_double3)](/documentation/simd/simd_double3x3/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_double3, simd_double3, simd_double3) -> simd_double3x3](/documentation/simd/simd_matrix(_:_:_:)-5h0nl)
- [func simd_matrix_from_rows(simd_double3, simd_double3, simd_double3) -> simd_double3x3](/documentation/simd/simd_matrix_from_rows(_:_:_:)-48v9h)
- [func matrix_from_rows(SIMD3<Double>, SIMD3<Double>, SIMD3<Double>) -> simd_double3x3](/documentation/simd/matrix_from_rows(_:_:_:)-7a60t)
- [func simd_matrix3x3(simd_quatd) -> simd_double3x3](/documentation/simd/simd_matrix3x3(_:)-60dhx)

### Element Access

- [subscript(Int) -> SIMD3<Double>](/documentation/simd/simd_double3x3/subscript(_:))
- [subscript(Int, Int) -> Double](/documentation/simd/simd_double3x3/subscript(_:_:))

### Type Aliases

- [double3x3](/documentation/simd/double3x3)
- [matrix_double3x3](/documentation/simd/matrix_double3x3)

### Deprecated Symbols

- [func matrix_invert(simd_double3x3) -> simd_double3x3](/documentation/simd/matrix_invert(_:)-2lv98)
- [func matrix_from_columns(SIMD3<Double>, SIMD3<Double>, SIMD3<Double>) -> simd_double3x3](/documentation/simd/matrix_from_columns(_:_:_:)-4bc62)
- [func matrix_from_diagonal(SIMD3<Double>) -> simd_double3x3](/documentation/simd/matrix_from_diagonal(_:)-3jtgg)
- [func matrix_determinant(simd_double3x3) -> Double](/documentation/simd/matrix_determinant(_:)-4bxkm)
- [func matrix_equal(simd_double3x3, simd_double3x3) -> Bool](/documentation/simd/matrix_equal(_:_:)-9tdua)
- [func matrix_transpose(simd_double3x3) -> double3x3](/documentation/simd/matrix_transpose(_:)-3ectl)
- [init(simd_double3x3)](/documentation/simd/simd_double3x3/init(_:)-2o4jh)
- [var cmatrix: simd_double3x3](/documentation/simd/simd_double3x3/cmatrix)

### Operators

- [static func * (simd_double3x3, SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/simd_double3x3/*(_:_:)-11ff2)
- [static func * (Double, simd_double3x3) -> simd_double3x3](/documentation/simd/simd_double3x3/*(_:_:)-23oic)
- [static func * (simd_double3x3, double4x3) -> double4x3](/documentation/simd/simd_double3x3/*(_:_:)-2hizn)
- [static func * (simd_double3x3, double3x3) -> double3x3](/documentation/simd/simd_double3x3/*(_:_:)-2oy7n)
- [static func * (SIMD3<Double>, simd_double3x3) -> SIMD3<Double>](/documentation/simd/simd_double3x3/*(_:_:)-2yrlv)
- [static func * (simd_double3x3, double2x3) -> double2x3](/documentation/simd/simd_double3x3/*(_:_:)-38zoj)
- [static func * (simd_double3x3, Double) -> simd_double3x3](/documentation/simd/simd_double3x3/*(_:_:)-8r8se)
- [static func *= (inout simd_double3x3, double3x3)](/documentation/simd/simd_double3x3/*=(_:_:)-4dl51)
- [static func *= (inout simd_double3x3, Double)](/documentation/simd/simd_double3x3/*=(_:_:)-7vz3h)
- [static func + (simd_double3x3, simd_double3x3) -> simd_double3x3](/documentation/simd/simd_double3x3/+(_:_:))
- [static func += (inout simd_double3x3, simd_double3x3)](/documentation/simd/simd_double3x3/+=(_:_:))
- [static func - (simd_double3x3) -> simd_double3x3](/documentation/simd/simd_double3x3/-(_:))
- [static func - (simd_double3x3, simd_double3x3) -> simd_double3x3](/documentation/simd/simd_double3x3/-(_:_:))
- [static func -= (inout simd_double3x3, simd_double3x3)](/documentation/simd/simd_double3x3/-=(_:_:))
- [simd_double3x4](/documentation/simd/simd_double3x4)

### Initializers

- [init()](/documentation/simd/simd_double3x4/init())
- [init(Double)](/documentation/simd/simd_double3x4/init(_:)-11lc1)
- [init(diagonal: SIMD3<Double>)](/documentation/simd/simd_double3x4/init(diagonal:))
- [init([SIMD4<Double>])](/documentation/simd/simd_double3x4/init(_:)-74wu4)
- [init(SIMD4<Double>, SIMD4<Double>, SIMD4<Double>)](/documentation/simd/simd_double3x4/init(_:_:_:))
- [init(columns: (simd_double4, simd_double4, simd_double4))](/documentation/simd/simd_double3x4/init(columns:))
- [init(rows: [SIMD3<Double>])](/documentation/simd/simd_double3x4/init(rows:))

### Matrix Properties

- [var transpose: double4x3](/documentation/simd/simd_double3x4/transpose)
- [var columns: (simd_double4, simd_double4, simd_double4)](/documentation/simd/simd_double3x4/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_double4, simd_double4, simd_double4) -> simd_double3x4](/documentation/simd/simd_matrix(_:_:_:)-4o4n5)
- [func simd_matrix_from_rows(simd_double3, simd_double3, simd_double3, simd_double3) -> simd_double3x4](/documentation/simd/simd_matrix_from_rows(_:_:_:_:)-7j052)
- [func matrix_from_rows(SIMD3<Double>, SIMD3<Double>, SIMD3<Double>, SIMD3<Double>) -> simd_double3x4](/documentation/simd/matrix_from_rows(_:_:_:_:)-69xld)

### Element Access

- [subscript(Int) -> SIMD4<Double>](/documentation/simd/simd_double3x4/subscript(_:))
- [subscript(Int, Int) -> Double](/documentation/simd/simd_double3x4/subscript(_:_:))

### Type Aliases

- [double3x4](/documentation/simd/double3x4)
- [matrix_double3x4](/documentation/simd/matrix_double3x4)

### Deprecated Symbols

- [func matrix_equal(simd_double3x4, simd_double3x4) -> Bool](/documentation/simd/matrix_equal(_:_:)-4qog1)
- [func matrix_from_columns(SIMD4<Double>, SIMD4<Double>, SIMD4<Double>) -> simd_double3x4](/documentation/simd/matrix_from_columns(_:_:_:)-4no1k)
- [func matrix_transpose(simd_double4x3) -> double3x4](/documentation/simd/matrix_transpose(_:)-8am0o)
- [init(simd_double3x4)](/documentation/simd/simd_double3x4/init(_:)-2qvpe)
- [var cmatrix: simd_double3x4](/documentation/simd/simd_double3x4/cmatrix)

### Operators

- [static func * (simd_double3x4, double2x3) -> double2x4](/documentation/simd/simd_double3x4/*(_:_:)-15q5b)
- [static func * (Double, simd_double3x4) -> simd_double3x4](/documentation/simd/simd_double3x4/*(_:_:)-2qxoj)
- [static func * (SIMD4<Double>, simd_double3x4) -> SIMD3<Double>](/documentation/simd/simd_double3x4/*(_:_:)-3xyct)
- [static func * (simd_double3x4, SIMD3<Double>) -> SIMD4<Double>](/documentation/simd/simd_double3x4/*(_:_:)-4g9jd)
- [static func * (simd_double3x4, Double) -> simd_double3x4](/documentation/simd/simd_double3x4/*(_:_:)-4qzww)
- [static func * (simd_double3x4, double3x3) -> double3x4](/documentation/simd/simd_double3x4/*(_:_:)-6qa2j)
- [static func * (simd_double3x4, double4x3) -> double4x4](/documentation/simd/simd_double3x4/*(_:_:)-962p4)
- [static func *= (inout simd_double3x4, Double)](/documentation/simd/simd_double3x4/*=(_:_:)-62fjm)
- [static func *= (inout simd_double3x4, double3x3)](/documentation/simd/simd_double3x4/*=(_:_:)-sjb5)
- [static func + (simd_double3x4, simd_double3x4) -> simd_double3x4](/documentation/simd/simd_double3x4/+(_:_:))
- [static func += (inout simd_double3x4, simd_double3x4)](/documentation/simd/simd_double3x4/+=(_:_:))
- [static func - (simd_double3x4) -> simd_double3x4](/documentation/simd/simd_double3x4/-(_:))
- [static func - (simd_double3x4, simd_double3x4) -> simd_double3x4](/documentation/simd/simd_double3x4/-(_:_:))
- [static func -= (inout simd_double3x4, simd_double3x4)](/documentation/simd/simd_double3x4/-=(_:_:))
- [simd_double4x2](/documentation/simd/simd_double4x2)

### Initializers

- [init()](/documentation/simd/simd_double4x2/init())
- [init(Double)](/documentation/simd/simd_double4x2/init(_:)-3i3he)
- [init(diagonal: SIMD2<Double>)](/documentation/simd/simd_double4x2/init(diagonal:))
- [init([SIMD2<Double>])](/documentation/simd/simd_double4x2/init(_:)-9pvdm)
- [init(SIMD2<Double>, SIMD2<Double>, SIMD2<Double>, SIMD2<Double>)](/documentation/simd/simd_double4x2/init(_:_:_:_:))
- [init(columns: (simd_double2, simd_double2, simd_double2, simd_double2))](/documentation/simd/simd_double4x2/init(columns:))
- [init(rows: [SIMD4<Double>])](/documentation/simd/simd_double4x2/init(rows:))

### Matrix Properties

- [var transpose: double2x4](/documentation/simd/simd_double4x2/transpose)
- [var columns: (simd_double2, simd_double2, simd_double2, simd_double2)](/documentation/simd/simd_double4x2/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_double2, simd_double2, simd_double2, simd_double2) -> simd_double4x2](/documentation/simd/simd_matrix(_:_:_:_:)-6cze4)
- [func simd_matrix_from_rows(simd_double4, simd_double4) -> simd_double4x2](/documentation/simd/simd_matrix_from_rows(_:_:)-5xq2d)
- [func matrix_from_rows(SIMD4<Double>, SIMD4<Double>) -> simd_double4x2](/documentation/simd/matrix_from_rows(_:_:)-2rxkt)

### Element Access

- [subscript(Int) -> SIMD2<Double>](/documentation/simd/simd_double4x2/subscript(_:))
- [subscript(Int, Int) -> Double](/documentation/simd/simd_double4x2/subscript(_:_:))

### Type Aliases

- [double4x2](/documentation/simd/double4x2)
- [matrix_double4x2](/documentation/simd/matrix_double4x2)

### Deprecated Symbols

- [func matrix_from_columns(SIMD2<Double>, SIMD2<Double>, SIMD2<Double>, SIMD2<Double>) -> simd_double4x2](/documentation/simd/matrix_from_columns(_:_:_:_:)-6tb78)
- [func matrix_equal(simd_double4x2, simd_double4x2) -> Bool](/documentation/simd/matrix_equal(_:_:)-5v8g0)
- [func matrix_transpose(simd_double2x4) -> double4x2](/documentation/simd/matrix_transpose(_:)-7ttoe)
- [init(simd_double4x2)](/documentation/simd/simd_double4x2/init(_:)-hovz)
- [var cmatrix: simd_double4x2](/documentation/simd/simd_double4x2/cmatrix)

### Operators

- [static func * (simd_double4x2, Double) -> simd_double4x2](/documentation/simd/simd_double4x2/*(_:_:)-5166x)
- [static func * (SIMD2<Double>, simd_double4x2) -> SIMD4<Double>](/documentation/simd/simd_double4x2/*(_:_:)-64ht9)
- [static func * (simd_double4x2, SIMD4<Double>) -> SIMD2<Double>](/documentation/simd/simd_double4x2/*(_:_:)-73ixh)
- [static func * (Double, simd_double4x2) -> simd_double4x2](/documentation/simd/simd_double4x2/*(_:_:)-7fz5)
- [static func * (simd_double4x2, double4x4) -> double4x2](/documentation/simd/simd_double4x2/*(_:_:)-8tpc2)
- [static func * (simd_double4x2, double3x4) -> double3x2](/documentation/simd/simd_double4x2/*(_:_:)-mlrw)
- [static func * (simd_double4x2, double2x4) -> double2x2](/documentation/simd/simd_double4x2/*(_:_:)-qtns)
- [static func *= (inout simd_double4x2, double4x4)](/documentation/simd/simd_double4x2/*=(_:_:)-2s2r4)
- [static func *= (inout simd_double4x2, Double)](/documentation/simd/simd_double4x2/*=(_:_:)-9qlax)
- [static func + (simd_double4x2, simd_double4x2) -> simd_double4x2](/documentation/simd/simd_double4x2/+(_:_:))
- [static func += (inout simd_double4x2, simd_double4x2)](/documentation/simd/simd_double4x2/+=(_:_:))
- [static func - (simd_double4x2) -> simd_double4x2](/documentation/simd/simd_double4x2/-(_:))
- [static func - (simd_double4x2, simd_double4x2) -> simd_double4x2](/documentation/simd/simd_double4x2/-(_:_:))
- [static func -= (inout simd_double4x2, simd_double4x2)](/documentation/simd/simd_double4x2/-=(_:_:))
- [simd_double4x3](/documentation/simd/simd_double4x3)

### Initializers

- [init()](/documentation/simd/simd_double4x3/init())
- [init(Double)](/documentation/simd/simd_double4x3/init(_:)-lh76)
- [init(diagonal: SIMD3<Double>)](/documentation/simd/simd_double4x3/init(diagonal:))
- [init([SIMD3<Double>])](/documentation/simd/simd_double4x3/init(_:)-24exh)
- [init(SIMD3<Double>, SIMD3<Double>, SIMD3<Double>, SIMD3<Double>)](/documentation/simd/simd_double4x3/init(_:_:_:_:))
- [init(columns: (simd_double3, simd_double3, simd_double3, simd_double3))](/documentation/simd/simd_double4x3/init(columns:))
- [init(rows: [SIMD4<Double>])](/documentation/simd/simd_double4x3/init(rows:))
- [init(AffineTransform3DFloat)](/documentation/simd/simd_double4x3/init(_:)-8t58y)

### Matrix Properties

- [var transpose: double3x4](/documentation/simd/simd_double4x3/transpose)
- [var columns: (simd_double3, simd_double3, simd_double3, simd_double3)](/documentation/simd/simd_double4x3/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_double3, simd_double3, simd_double3, simd_double3) -> simd_double4x3](/documentation/simd/simd_matrix(_:_:_:_:)-4swfv)
- [func simd_matrix_from_rows(simd_double4, simd_double4, simd_double4) -> simd_double4x3](/documentation/simd/simd_matrix_from_rows(_:_:_:)-6525o)
- [func matrix_from_rows(SIMD4<Double>, SIMD4<Double>, SIMD4<Double>) -> simd_double4x3](/documentation/simd/matrix_from_rows(_:_:_:)-19j6n)

### Element Access

- [subscript(Int) -> SIMD3<Double>](/documentation/simd/simd_double4x3/subscript(_:))
- [subscript(Int, Int) -> Double](/documentation/simd/simd_double4x3/subscript(_:_:))

### Type Aliases

- [double4x3](/documentation/simd/double4x3)
- [matrix_double4x3](/documentation/simd/matrix_double4x3)

### Deprecated Symbols

- [func matrix_from_columns(SIMD3<Double>, SIMD3<Double>, SIMD3<Double>, SIMD3<Double>) -> simd_double4x3](/documentation/simd/matrix_from_columns(_:_:_:_:)-7g6mu)
- [func matrix_equal(simd_double4x3, simd_double4x3) -> Bool](/documentation/simd/matrix_equal(_:_:)-1x3ox)
- [func matrix_transpose(simd_double3x4) -> double4x3](/documentation/simd/matrix_transpose(_:)-23ibz)
- [init(simd_double4x3)](/documentation/simd/simd_double4x3/init(_:)-30jps)
- [var cmatrix: simd_double4x3](/documentation/simd/simd_double4x3/cmatrix)

### Operators

- [static func * (Double, simd_double4x3) -> simd_double4x3](/documentation/simd/simd_double4x3/*(_:_:)-13lud)
- [static func * (simd_double4x3, double4x4) -> double4x3](/documentation/simd/simd_double4x3/*(_:_:)-3vmls)
- [static func * (simd_double4x3, Double) -> simd_double4x3](/documentation/simd/simd_double4x3/*(_:_:)-4q5li)
- [static func * (simd_double4x3, double3x4) -> double3x3](/documentation/simd/simd_double4x3/*(_:_:)-61nnq)
- [static func * (simd_double4x3, SIMD4<Double>) -> SIMD3<Double>](/documentation/simd/simd_double4x3/*(_:_:)-6sw55)
- [static func * (SIMD3<Double>, simd_double4x3) -> SIMD4<Double>](/documentation/simd/simd_double4x3/*(_:_:)-7362q)
- [static func * (simd_double4x3, double2x4) -> double2x3](/documentation/simd/simd_double4x3/*(_:_:)-8ugfy)
- [static func *= (inout simd_double4x3, double4x4)](/documentation/simd/simd_double4x3/*=(_:_:)-2x6ni)
- [static func *= (inout simd_double4x3, Double)](/documentation/simd/simd_double4x3/*=(_:_:)-4o6cd)
- [static func + (simd_double4x3, simd_double4x3) -> simd_double4x3](/documentation/simd/simd_double4x3/+(_:_:))
- [static func += (inout simd_double4x3, simd_double4x3)](/documentation/simd/simd_double4x3/+=(_:_:))
- [static func - (simd_double4x3) -> simd_double4x3](/documentation/simd/simd_double4x3/-(_:))
- [static func - (simd_double4x3, simd_double4x3) -> simd_double4x3](/documentation/simd/simd_double4x3/-(_:_:))
- [static func -= (inout simd_double4x3, simd_double4x3)](/documentation/simd/simd_double4x3/-=(_:_:))
- [simd_double4x4](/documentation/simd/simd_double4x4)

### Initializers

- [init()](/documentation/simd/simd_double4x4/init())
- [init(Double)](/documentation/simd/simd_double4x4/init(_:)-184ad)
- [init(diagonal: SIMD4<Double>)](/documentation/simd/simd_double4x4/init(diagonal:))
- [init([SIMD4<Double>])](/documentation/simd/simd_double4x4/init(_:)-ahnn)
- [init(simd_quatd)](/documentation/simd/simd_double4x4/init(_:)-43z8y)
- [init(SCNMatrix4)](/documentation/simd/simd_double4x4/init(_:)-45usb)
- [init(SCNMatrix4)](/documentation/simd/simd_double4x4/init(_:)-vm0p)
- [init(SIMD4<Double>, SIMD4<Double>, SIMD4<Double>, SIMD4<Double>)](/documentation/simd/simd_double4x4/init(_:_:_:_:))
- [init(columns: (simd_double4, simd_double4, simd_double4, simd_double4))](/documentation/simd/simd_double4x4/init(columns:))
- [init(rows: [SIMD4<Double>])](/documentation/simd/simd_double4x4/init(rows:))
- [init(AffineTransform3DFloat)](/documentation/simd/simd_double4x4/init(_:)-1ara7)
- [init(Pose3DFloat)](/documentation/simd/simd_double4x4/init(_:)-818zf)
- [init(ProjectiveTransform3DFloat)](/documentation/simd/simd_double4x4/init(_:)-98553)

### Matrix Constants

- [let matrix_identity_double4x4: simd_double4x4](/documentation/simd/matrix_identity_double4x4)

### Matrix Properties

- [var determinant: Double](/documentation/simd/simd_double4x4/determinant)
- [var inverse: simd_double4x4](/documentation/simd/simd_double4x4/inverse)
- [var transpose: double4x4](/documentation/simd/simd_double4x4/transpose)
- [var columns: (simd_double4, simd_double4, simd_double4, simd_double4)](/documentation/simd/simd_double4x4/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_double4, simd_double4, simd_double4, simd_double4) -> simd_double4x4](/documentation/simd/simd_matrix(_:_:_:_:)-28at0)
- [func simd_matrix_from_rows(simd_double4, simd_double4, simd_double4, simd_double4) -> simd_double4x4](/documentation/simd/simd_matrix_from_rows(_:_:_:_:)-898tw)
- [func matrix_from_rows(SIMD4<Double>, SIMD4<Double>, SIMD4<Double>, SIMD4<Double>) -> simd_double4x4](/documentation/simd/matrix_from_rows(_:_:_:_:)-37t0w)
- [func simd_matrix4x4(simd_quatd) -> simd_double4x4](/documentation/simd/simd_matrix4x4(_:)-20mdz)

### Element Access

- [subscript(Int) -> SIMD4<Double>](/documentation/simd/simd_double4x4/subscript(_:))
- [subscript(Int, Int) -> Double](/documentation/simd/simd_double4x4/subscript(_:_:))

### Type Aliases

- [double4x4](/documentation/simd/double4x4)
- [matrix_double4x4](/documentation/simd/matrix_double4x4)

### Deprecated Symbols

- [func matrix_invert(simd_double4x4) -> simd_double4x4](/documentation/simd/matrix_invert(_:)-84fxh)
- [func matrix_from_columns(SIMD4<Double>, SIMD4<Double>, SIMD4<Double>, SIMD4<Double>) -> simd_double4x4](/documentation/simd/matrix_from_columns(_:_:_:_:)-61q4l)
- [func matrix_from_diagonal(SIMD4<Double>) -> simd_double4x4](/documentation/simd/matrix_from_diagonal(_:)-2r6tr)
- [func matrix_determinant(simd_double4x4) -> Double](/documentation/simd/matrix_determinant(_:)-2n34p)
- [func matrix_equal(simd_double4x4, simd_double4x4) -> Bool](/documentation/simd/matrix_equal(_:_:)-3jmfe)
- [func matrix_transpose(simd_double4x4) -> double4x4](/documentation/simd/matrix_transpose(_:)-66ecl)
- [init(simd_double4x4)](/documentation/simd/simd_double4x4/init(_:)-4fie3)
- [var cmatrix: simd_double4x4](/documentation/simd/simd_double4x4/cmatrix)

### Operators

- [static func * (simd_double4x4, double2x4) -> double2x4](/documentation/simd/simd_double4x4/*(_:_:)-17puk)
- [static func * (simd_double4x4, double4x4) -> double4x4](/documentation/simd/simd_double4x4/*(_:_:)-2wqm8)
- [static func * (simd_double4x4, SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/simd_double4x4/*(_:_:)-3jd3c)
- [static func * (Double, simd_double4x4) -> simd_double4x4](/documentation/simd/simd_double4x4/*(_:_:)-5459y)
- [static func * (simd_double4x4, double3x4) -> double3x4](/documentation/simd/simd_double4x4/*(_:_:)-5i8yr)
- [static func * (SIMD4<Double>, simd_double4x4) -> SIMD4<Double>](/documentation/simd/simd_double4x4/*(_:_:)-7cb0c)
- [static func * (simd_double4x4, Double) -> simd_double4x4](/documentation/simd/simd_double4x4/*(_:_:)-p402)
- [static func *= (inout simd_double4x4, double4x4)](/documentation/simd/simd_double4x4/*=(_:_:)-12w8l)
- [static func *= (inout simd_double4x4, Double)](/documentation/simd/simd_double4x4/*=(_:_:)-9llx)
- [static func + (simd_double4x4, simd_double4x4) -> simd_double4x4](/documentation/simd/simd_double4x4/+(_:_:))
- [static func += (inout simd_double4x4, simd_double4x4)](/documentation/simd/simd_double4x4/+=(_:_:))
- [static func - (simd_double4x4) -> simd_double4x4](/documentation/simd/simd_double4x4/-(_:))
- [static func - (simd_double4x4, simd_double4x4) -> simd_double4x4](/documentation/simd/simd_double4x4/-(_:_:))
- [static func -= (inout simd_double4x4, simd_double4x4)](/documentation/simd/simd_double4x4/-=(_:_:))
- [simd_float2x2](/documentation/simd/simd_float2x2)

### Initializers

- [init()](/documentation/simd/simd_float2x2/init())
- [init(Float)](/documentation/simd/simd_float2x2/init(_:)-55fda)
- [init(diagonal: SIMD2<Float>)](/documentation/simd/simd_float2x2/init(diagonal:))
- [init([SIMD2<Float>])](/documentation/simd/simd_float2x2/init(_:)-2mgex)
- [init(SIMD2<Float>, SIMD2<Float>)](/documentation/simd/simd_float2x2/init(_:_:))
- [init(columns: (simd_float2, simd_float2))](/documentation/simd/simd_float2x2/init(columns:))
- [init(rows: [SIMD2<Float>])](/documentation/simd/simd_float2x2/init(rows:))

### Matrix Constants

- [let matrix_identity_float2x2: simd_float2x2](/documentation/simd/matrix_identity_float2x2)

### Matrix Properties

- [var determinant: Float](/documentation/simd/simd_float2x2/determinant)
- [var inverse: simd_float2x2](/documentation/simd/simd_float2x2/inverse)
- [var transpose: float2x2](/documentation/simd/simd_float2x2/transpose)
- [var columns: (simd_float2, simd_float2)](/documentation/simd/simd_float2x2/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_float2, simd_float2) -> simd_float2x2](/documentation/simd/simd_matrix(_:_:)-1ftcm)
- [func simd_matrix_from_rows(simd_float2, simd_float2) -> simd_float2x2](/documentation/simd/simd_matrix_from_rows(_:_:)-3mqrr)
- [func matrix_from_rows(SIMD2<Float>, SIMD2<Float>) -> simd_float2x2](/documentation/simd/matrix_from_rows(_:_:)-2pi8i)

### Element Access

- [subscript(Int) -> SIMD2<Float>](/documentation/simd/simd_float2x2/subscript(_:))
- [subscript(Int, Int) -> Float](/documentation/simd/simd_float2x2/subscript(_:_:))

### Type Aliases

- [float2x2](/documentation/simd/float2x2)
- [matrix_float2x2](/documentation/simd/matrix_float2x2)

### Deprecated Symbols

- [func matrix_invert(simd_float2x2) -> simd_float2x2](/documentation/simd/matrix_invert(_:)-94e37)
- [func matrix_transpose(simd_float2x2) -> float2x2](/documentation/simd/matrix_transpose(_:)-77v7g)
- [func matrix_from_diagonal(SIMD2<Float>) -> simd_float2x2](/documentation/simd/matrix_from_diagonal(_:)-1v0zl)
- [func matrix_from_columns(SIMD2<Float>, SIMD2<Float>) -> simd_float2x2](/documentation/simd/matrix_from_columns(_:_:)-5urmx)
- [func matrix_determinant(simd_float2x2) -> Float](/documentation/simd/matrix_determinant(_:)-30k4n)
- [func matrix_equal(simd_float2x2, simd_float2x2) -> Bool](/documentation/simd/matrix_equal(_:_:)-88hz9)
- [init(simd_float2x2)](/documentation/simd/simd_float2x2/init(_:)-uyy7)
- [var cmatrix: simd_float2x2](/documentation/simd/simd_float2x2/cmatrix)

### Operators

- [static func * (simd_float2x2, float2x2) -> float2x2](/documentation/simd/simd_float2x2/*(_:_:)-2jwi9)
- [static func * (simd_float2x2, float3x2) -> float3x2](/documentation/simd/simd_float2x2/*(_:_:)-39xxb)
- [static func * (simd_float2x2, float4x2) -> float4x2](/documentation/simd/simd_float2x2/*(_:_:)-4h9qy)
- [static func * (simd_float2x2, SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/simd_float2x2/*(_:_:)-5fo9p)
- [static func * (simd_float2x2, Float) -> simd_float2x2](/documentation/simd/simd_float2x2/*(_:_:)-7begh)
- [static func * (Float, simd_float2x2) -> simd_float2x2](/documentation/simd/simd_float2x2/*(_:_:)-92stm)
- [static func * (SIMD2<Float>, simd_float2x2) -> SIMD2<Float>](/documentation/simd/simd_float2x2/*(_:_:)-98lyp)
- [static func *= (inout simd_float2x2, float2x2)](/documentation/simd/simd_float2x2/*=(_:_:)-2vg0e)
- [static func *= (inout simd_float2x2, Float)](/documentation/simd/simd_float2x2/*=(_:_:)-obw4)
- [static func + (simd_float2x2, simd_float2x2) -> simd_float2x2](/documentation/simd/simd_float2x2/+(_:_:))
- [static func += (inout simd_float2x2, simd_float2x2)](/documentation/simd/simd_float2x2/+=(_:_:))
- [static func - (simd_float2x2) -> simd_float2x2](/documentation/simd/simd_float2x2/-(_:))
- [static func - (simd_float2x2, simd_float2x2) -> simd_float2x2](/documentation/simd/simd_float2x2/-(_:_:))
- [static func -= (inout simd_float2x2, simd_float2x2)](/documentation/simd/simd_float2x2/-=(_:_:))
- [simd_float2x3](/documentation/simd/simd_float2x3)

### Initializers

- [init()](/documentation/simd/simd_float2x3/init())
- [init(Float)](/documentation/simd/simd_float2x3/init(_:)-9lk1g)
- [init(diagonal: SIMD2<Float>)](/documentation/simd/simd_float2x3/init(diagonal:))
- [init([SIMD3<Float>])](/documentation/simd/simd_float2x3/init(_:)-757nf)
- [init(SIMD3<Float>, SIMD3<Float>)](/documentation/simd/simd_float2x3/init(_:_:))
- [init(columns: (simd_float3, simd_float3))](/documentation/simd/simd_float2x3/init(columns:))
- [init(rows: [SIMD2<Float>])](/documentation/simd/simd_float2x3/init(rows:))

### Matrix Properties

- [var transpose: float3x2](/documentation/simd/simd_float2x3/transpose)
- [var columns: (simd_float3, simd_float3)](/documentation/simd/simd_float2x3/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_float3, simd_float3) -> simd_float2x3](/documentation/simd/simd_matrix(_:_:)-7qavs)
- [func simd_matrix_from_rows(simd_float2, simd_float2, simd_float2) -> simd_float2x3](/documentation/simd/simd_matrix_from_rows(_:_:_:)-9kksc)
- [func matrix_from_rows(SIMD2<Float>, SIMD2<Float>, SIMD2<Float>) -> simd_float2x3](/documentation/simd/matrix_from_rows(_:_:_:)-m0hw)

### Element Access

- [subscript(Int) -> SIMD3<Float>](/documentation/simd/simd_float2x3/subscript(_:))
- [subscript(Int, Int) -> Float](/documentation/simd/simd_float2x3/subscript(_:_:))

### Type Aliases

- [float2x3](/documentation/simd/float2x3)
- [matrix_float2x3](/documentation/simd/matrix_float2x3)

### Deprecated Symbols

- [func matrix_from_columns(SIMD3<Float>, SIMD3<Float>) -> simd_float2x3](/documentation/simd/matrix_from_columns(_:_:)-8tygq)
- [func matrix_equal(simd_float2x3, simd_float2x3) -> Bool](/documentation/simd/matrix_equal(_:_:)-he2l)
- [func matrix_transpose(simd_float2x3) -> float3x2](/documentation/simd/matrix_transpose(_:)-71xii)
- [init(simd_float2x3)](/documentation/simd/simd_float2x3/init(_:)-55t2w)
- [var cmatrix: simd_float2x3](/documentation/simd/simd_float2x3/cmatrix)

### Operators

- [static func * (simd_float2x3, Float) -> simd_float2x3](/documentation/simd/simd_float2x3/*(_:_:)-2hkqa)
- [static func * (simd_float2x3, float2x2) -> float2x3](/documentation/simd/simd_float2x3/*(_:_:)-4hssh)
- [static func * (Float, simd_float2x3) -> simd_float2x3](/documentation/simd/simd_float2x3/*(_:_:)-4pre4)
- [static func * (simd_float2x3, float4x2) -> float4x3](/documentation/simd/simd_float2x3/*(_:_:)-7vzog)
- [static func * (SIMD3<Float>, simd_float2x3) -> SIMD2<Float>](/documentation/simd/simd_float2x3/*(_:_:)-82e85)
- [static func * (simd_float2x3, float3x2) -> float3x3](/documentation/simd/simd_float2x3/*(_:_:)-84qqs)
- [static func * (simd_float2x3, SIMD2<Float>) -> SIMD3<Float>](/documentation/simd/simd_float2x3/*(_:_:)-955tc)
- [static func *= (inout simd_float2x3, Float)](/documentation/simd/simd_float2x3/*=(_:_:)-6hcqy)
- [static func *= (inout simd_float2x3, float2x2)](/documentation/simd/simd_float2x3/*=(_:_:)-7ohft)
- [static func + (simd_float2x3, simd_float2x3) -> simd_float2x3](/documentation/simd/simd_float2x3/+(_:_:))
- [static func += (inout simd_float2x3, simd_float2x3)](/documentation/simd/simd_float2x3/+=(_:_:))
- [static func - (simd_float2x3) -> simd_float2x3](/documentation/simd/simd_float2x3/-(_:))
- [static func - (simd_float2x3, simd_float2x3) -> simd_float2x3](/documentation/simd/simd_float2x3/-(_:_:))
- [static func -= (inout simd_float2x3, simd_float2x3)](/documentation/simd/simd_float2x3/-=(_:_:))
- [simd_float2x4](/documentation/simd/simd_float2x4)

### Initializers

- [init()](/documentation/simd/simd_float2x4/init())
- [init(Float)](/documentation/simd/simd_float2x4/init(_:)-smdg)
- [init(diagonal: SIMD2<Float>)](/documentation/simd/simd_float2x4/init(diagonal:))
- [init([SIMD4<Float>])](/documentation/simd/simd_float2x4/init(_:)-hvkr)
- [init(SIMD4<Float>, SIMD4<Float>)](/documentation/simd/simd_float2x4/init(_:_:))
- [init(columns: (simd_float4, simd_float4))](/documentation/simd/simd_float2x4/init(columns:))
- [init(rows: [SIMD2<Float>])](/documentation/simd/simd_float2x4/init(rows:))

### Matrix Properties

- [var transpose: float4x2](/documentation/simd/simd_float2x4/transpose)
- [var columns: (simd_float4, simd_float4)](/documentation/simd/simd_float2x4/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_float4, simd_float4) -> simd_float2x4](/documentation/simd/simd_matrix(_:_:)-7ayva)
- [func simd_matrix_from_rows(simd_float2, simd_float2, simd_float2, simd_float2) -> simd_float2x4](/documentation/simd/simd_matrix_from_rows(_:_:_:_:)-7s7pv)
- [func matrix_from_rows(SIMD2<Float>, SIMD2<Float>, SIMD2<Float>, SIMD2<Float>) -> simd_float2x4](/documentation/simd/matrix_from_rows(_:_:_:_:)-51dz4)

### Element Access

- [subscript(Int) -> SIMD4<Float>](/documentation/simd/simd_float2x4/subscript(_:))
- [subscript(Int, Int) -> Float](/documentation/simd/simd_float2x4/subscript(_:_:))

### Type Aliases

- [float2x4](/documentation/simd/float2x4)
- [matrix_float2x4](/documentation/simd/matrix_float2x4)

### Deprecated Symbols

- [func matrix_from_columns(SIMD4<Float>, SIMD4<Float>) -> simd_float2x4](/documentation/simd/matrix_from_columns(_:_:)-6tvfl)
- [func matrix_equal(simd_float2x4, simd_float2x4) -> Bool](/documentation/simd/matrix_equal(_:_:)-34fuu)
- [func matrix_transpose(simd_float4x2) -> float2x4](/documentation/simd/matrix_transpose(_:)-5ymlr)
- [init(simd_float2x4)](/documentation/simd/simd_float2x4/init(_:)-3teag)
- [var cmatrix: simd_float2x4](/documentation/simd/simd_float2x4/cmatrix)

### Operators

- [static func * (SIMD4<Float>, simd_float2x4) -> SIMD2<Float>](/documentation/simd/simd_float2x4/*(_:_:)-10gif)
- [static func * (simd_float2x4, float2x2) -> float2x4](/documentation/simd/simd_float2x4/*(_:_:)-239o8)
- [static func * (simd_float2x4, float4x2) -> float4x4](/documentation/simd/simd_float2x4/*(_:_:)-35xo4)
- [static func * (simd_float2x4, Float) -> simd_float2x4](/documentation/simd/simd_float2x4/*(_:_:)-3x5jg)
- [static func * (simd_float2x4, SIMD2<Float>) -> SIMD4<Float>](/documentation/simd/simd_float2x4/*(_:_:)-4clgl)
- [static func * (Float, simd_float2x4) -> simd_float2x4](/documentation/simd/simd_float2x4/*(_:_:)-7gnvu)
- [static func * (simd_float2x4, float3x2) -> float3x4](/documentation/simd/simd_float2x4/*(_:_:)-7ypgr)
- [static func *= (inout simd_float2x4, float2x2)](/documentation/simd/simd_float2x4/*=(_:_:)-6u2a)
- [static func *= (inout simd_float2x4, Float)](/documentation/simd/simd_float2x4/*=(_:_:)-jfkv)
- [static func + (simd_float2x4, simd_float2x4) -> simd_float2x4](/documentation/simd/simd_float2x4/+(_:_:))
- [static func += (inout simd_float2x4, simd_float2x4)](/documentation/simd/simd_float2x4/+=(_:_:))
- [static func - (simd_float2x4) -> simd_float2x4](/documentation/simd/simd_float2x4/-(_:))
- [static func - (simd_float2x4, simd_float2x4) -> simd_float2x4](/documentation/simd/simd_float2x4/-(_:_:))
- [static func -= (inout simd_float2x4, simd_float2x4)](/documentation/simd/simd_float2x4/-=(_:_:))
- [simd_float3x2](/documentation/simd/simd_float3x2)

### Initializers

- [init()](/documentation/simd/simd_float3x2/init())
- [init(Float)](/documentation/simd/simd_float3x2/init(_:)-8cvcd)
- [init(diagonal: SIMD2<Float>)](/documentation/simd/simd_float3x2/init(diagonal:))
- [init([SIMD2<Float>])](/documentation/simd/simd_float3x2/init(_:)-7ssoh)
- [init(SIMD2<Float>, SIMD2<Float>, SIMD2<Float>)](/documentation/simd/simd_float3x2/init(_:_:_:))
- [init(columns: (simd_float2, simd_float2, simd_float2))](/documentation/simd/simd_float3x2/init(columns:))
- [init(rows: [SIMD3<Float>])](/documentation/simd/simd_float3x2/init(rows:))

### Matrix Properties

- [var transpose: float2x3](/documentation/simd/simd_float3x2/transpose)
- [var columns: (simd_float2, simd_float2, simd_float2)](/documentation/simd/simd_float3x2/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_float2, simd_float2, simd_float2) -> simd_float3x2](/documentation/simd/simd_matrix(_:_:_:)-2oltj)
- [func simd_matrix_from_rows(simd_float3, simd_float3) -> simd_float3x2](/documentation/simd/simd_matrix_from_rows(_:_:)-48bjr)
- [func matrix_from_rows(SIMD3<Float>, SIMD3<Float>) -> simd_float3x2](/documentation/simd/matrix_from_rows(_:_:)-47wrn)

### Element Access

- [subscript(Int) -> SIMD2<Float>](/documentation/simd/simd_float3x2/subscript(_:))
- [subscript(Int, Int) -> Float](/documentation/simd/simd_float3x2/subscript(_:_:))

### Type Aliases

- [float3x2](/documentation/simd/float3x2)
- [matrix_float3x2](/documentation/simd/matrix_float3x2)

### Deprecated Symbols

- [func matrix_from_columns(SIMD2<Float>, SIMD2<Float>, SIMD2<Float>) -> simd_float3x2](/documentation/simd/matrix_from_columns(_:_:_:)-6ua0c)
- [func matrix_equal(simd_float3x2, simd_float3x2) -> Bool](/documentation/simd/matrix_equal(_:_:)-1kgro)
- [func matrix_transpose(simd_float3x2) -> float2x3](/documentation/simd/matrix_transpose(_:)-92iqd)
- [var cmatrix: simd_float3x2](/documentation/simd/simd_float3x2/cmatrix)
- [init(simd_float3x2)](/documentation/simd/simd_float3x2/init(_:)-323m3)

### Operators

- [static func * (simd_float3x2, float3x3) -> float3x2](/documentation/simd/simd_float3x2/*(_:_:)-2dgpn)
- [static func * (simd_float3x2, float2x3) -> float2x2](/documentation/simd/simd_float3x2/*(_:_:)-2raa3)
- [static func * (simd_float3x2, float4x3) -> float4x2](/documentation/simd/simd_float3x2/*(_:_:)-5obls)
- [static func * (simd_float3x2, Float) -> simd_float3x2](/documentation/simd/simd_float3x2/*(_:_:)-7x4bm)
- [static func * (SIMD2<Float>, simd_float3x2) -> SIMD3<Float>](/documentation/simd/simd_float3x2/*(_:_:)-83wp)
- [static func * (simd_float3x2, SIMD3<Float>) -> SIMD2<Float>](/documentation/simd/simd_float3x2/*(_:_:)-8l62c)
- [static func * (Float, simd_float3x2) -> simd_float3x2](/documentation/simd/simd_float3x2/*(_:_:)-9c2w1)
- [static func *= (inout simd_float3x2, float3x3)](/documentation/simd/simd_float3x2/*=(_:_:)-46fya)
- [static func *= (inout simd_float3x2, Float)](/documentation/simd/simd_float3x2/*=(_:_:)-6ojp8)
- [static func + (simd_float3x2, simd_float3x2) -> simd_float3x2](/documentation/simd/simd_float3x2/+(_:_:))
- [static func += (inout simd_float3x2, simd_float3x2)](/documentation/simd/simd_float3x2/+=(_:_:))
- [static func - (simd_float3x2) -> simd_float3x2](/documentation/simd/simd_float3x2/-(_:))
- [static func - (simd_float3x2, simd_float3x2) -> simd_float3x2](/documentation/simd/simd_float3x2/-(_:_:))
- [static func -= (inout simd_float3x2, simd_float3x2)](/documentation/simd/simd_float3x2/-=(_:_:))
- [simd_float3x3](/documentation/simd/simd_float3x3)

### Initializers

- [init()](/documentation/simd/simd_float3x3/init())
- [init(Float)](/documentation/simd/simd_float3x3/init(_:)-43ntv)
- [init(diagonal: SIMD3<Float>)](/documentation/simd/simd_float3x3/init(diagonal:))
- [init([SIMD3<Float>])](/documentation/simd/simd_float3x3/init(_:)-51tfs)
- [init(simd_quatf)](/documentation/simd/simd_float3x3/init(_:)-5wkmz)
- [init(SIMD3<Float>, SIMD3<Float>, SIMD3<Float>)](/documentation/simd/simd_float3x3/init(_:_:_:))
- [init(columns: (simd_float3, simd_float3, simd_float3))](/documentation/simd/simd_float3x3/init(columns:))
- [init(rows: [SIMD3<Float>])](/documentation/simd/simd_float3x3/init(rows:))

### Matrix Constants

- [let matrix_identity_float3x3: simd_float3x3](/documentation/simd/matrix_identity_float3x3)

### Matrix Properties

- [var determinant: Float](/documentation/simd/simd_float3x3/determinant)
- [var inverse: simd_float3x3](/documentation/simd/simd_float3x3/inverse)
- [var transpose: float3x3](/documentation/simd/simd_float3x3/transpose)
- [var columns: (simd_float3, simd_float3, simd_float3)](/documentation/simd/simd_float3x3/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_float3, simd_float3, simd_float3) -> simd_float3x3](/documentation/simd/simd_matrix(_:_:_:)-52z0s)
- [func simd_matrix_from_rows(simd_float3, simd_float3, simd_float3) -> simd_float3x3](/documentation/simd/simd_matrix_from_rows(_:_:_:)-1tn2x)
- [func matrix_from_rows(SIMD3<Float>, SIMD3<Float>, SIMD3<Float>) -> simd_float3x3](/documentation/simd/matrix_from_rows(_:_:_:)-15v2l)
- [func simd_matrix3x3(simd_quatf) -> simd_float3x3](/documentation/simd/simd_matrix3x3(_:)-60cx9)

### Element Access

- [subscript(Int) -> SIMD3<Float>](/documentation/simd/simd_float3x3/subscript(_:))
- [subscript(Int, Int) -> Float](/documentation/simd/simd_float3x3/subscript(_:_:))

### Type Aliases

- [float3x3](/documentation/simd/float3x3)
- [matrix_float3x3](/documentation/simd/matrix_float3x3)

### Deprecated Symbols

- [func matrix_invert(simd_float3x3) -> simd_float3x3](/documentation/simd/matrix_invert(_:)-15kif)
- [func matrix_from_diagonal(SIMD3<Float>) -> simd_float3x3](/documentation/simd/matrix_from_diagonal(_:)-61643)
- [func matrix_determinant(simd_float3x3) -> Float](/documentation/simd/matrix_determinant(_:)-2m4vm)
- [func matrix_equal(simd_float3x3, simd_float3x3) -> Bool](/documentation/simd/matrix_equal(_:_:)-14gko)
- [func matrix_from_columns(SIMD3<Float>, SIMD3<Float>, SIMD3<Float>) -> simd_float3x3](/documentation/simd/matrix_from_columns(_:_:_:)-4c7qb)
- [func matrix_transpose(simd_float3x3) -> float3x3](/documentation/simd/matrix_transpose(_:)-9pl1z)
- [init(simd_float3x3)](/documentation/simd/simd_float3x3/init(_:)-7ymye)
- [var cmatrix: simd_float3x3](/documentation/simd/simd_float3x3/cmatrix)

### Operators

- [static func * (Float, simd_float3x3) -> simd_float3x3](/documentation/simd/simd_float3x3/*(_:_:)-4x4d0)
- [static func * (simd_float3x3, float2x3) -> float2x3](/documentation/simd/simd_float3x3/*(_:_:)-69c2x)
- [static func * (SIMD3<Float>, simd_float3x3) -> SIMD3<Float>](/documentation/simd/simd_float3x3/*(_:_:)-6jkru)
- [static func * (simd_float3x3, float4x3) -> float4x3](/documentation/simd/simd_float3x3/*(_:_:)-6p68q)
- [static func * (simd_float3x3, Float) -> simd_float3x3](/documentation/simd/simd_float3x3/*(_:_:)-81cfn)
- [static func * (simd_float3x3, SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/simd_float3x3/*(_:_:)-8sd17)
- [static func * (simd_float3x3, float3x3) -> float3x3](/documentation/simd/simd_float3x3/*(_:_:)-9a517)
- [static func *= (inout simd_float3x3, Float)](/documentation/simd/simd_float3x3/*=(_:_:)-1iqf4)
- [static func *= (inout simd_float3x3, float3x3)](/documentation/simd/simd_float3x3/*=(_:_:)-744e6)
- [static func + (simd_float3x3, simd_float3x3) -> simd_float3x3](/documentation/simd/simd_float3x3/+(_:_:))
- [static func += (inout simd_float3x3, simd_float3x3)](/documentation/simd/simd_float3x3/+=(_:_:))
- [static func - (simd_float3x3) -> simd_float3x3](/documentation/simd/simd_float3x3/-(_:))
- [static func - (simd_float3x3, simd_float3x3) -> simd_float3x3](/documentation/simd/simd_float3x3/-(_:_:))
- [static func -= (inout simd_float3x3, simd_float3x3)](/documentation/simd/simd_float3x3/-=(_:_:))
- [simd_float3x4](/documentation/simd/simd_float3x4)

### Initializers

- [init()](/documentation/simd/simd_float3x4/init())
- [init(Float)](/documentation/simd/simd_float3x4/init(_:)-2os7r)
- [init(diagonal: SIMD3<Float>)](/documentation/simd/simd_float3x4/init(diagonal:))
- [init([SIMD4<Float>])](/documentation/simd/simd_float3x4/init(_:)-4w4et)
- [init(SIMD4<Float>, SIMD4<Float>, SIMD4<Float>)](/documentation/simd/simd_float3x4/init(_:_:_:))
- [init(columns: (simd_float4, simd_float4, simd_float4))](/documentation/simd/simd_float3x4/init(columns:))
- [init(rows: [SIMD3<Float>])](/documentation/simd/simd_float3x4/init(rows:))

### Matrix Properties

- [var transpose: float4x3](/documentation/simd/simd_float3x4/transpose)
- [var columns: (simd_float4, simd_float4, simd_float4)](/documentation/simd/simd_float3x4/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_float4, simd_float4, simd_float4) -> simd_float3x4](/documentation/simd/simd_matrix(_:_:_:)-1vwb0)
- [func simd_matrix_from_rows(simd_float3, simd_float3, simd_float3, simd_float3) -> simd_float3x4](/documentation/simd/simd_matrix_from_rows(_:_:_:_:)-6irzy)
- [func matrix_from_rows(SIMD3<Float>, SIMD3<Float>, SIMD3<Float>, SIMD3<Float>) -> simd_float3x4](/documentation/simd/matrix_from_rows(_:_:_:_:)-4bn2a)

### Element Access

- [subscript(Int) -> SIMD4<Float>](/documentation/simd/simd_float3x4/subscript(_:))
- [subscript(Int, Int) -> Float](/documentation/simd/simd_float3x4/subscript(_:_:))

### Type Aliases

- [float3x4](/documentation/simd/float3x4)
- [matrix_float3x4](/documentation/simd/matrix_float3x4)

### Deprecated Symbols

- [func matrix_equal(simd_float3x4, simd_float3x4) -> Bool](/documentation/simd/matrix_equal(_:_:)-6el88)
- [func matrix_from_columns(SIMD4<Float>, SIMD4<Float>, SIMD4<Float>) -> simd_float3x4](/documentation/simd/matrix_from_columns(_:_:_:)-5nhl4)
- [func matrix_transpose(simd_float4x3) -> float3x4](/documentation/simd/matrix_transpose(_:)-6ygo1)
- [init(simd_float3x4)](/documentation/simd/simd_float3x4/init(_:)-8fk31)
- [var cmatrix: simd_float3x4](/documentation/simd/simd_float3x4/cmatrix)

### Operators

- [static func * (Float, simd_float3x4) -> simd_float3x4](/documentation/simd/simd_float3x4/*(_:_:)-309ny)
- [static func * (simd_float3x4, float2x3) -> float2x4](/documentation/simd/simd_float3x4/*(_:_:)-39co8)
- [static func * (simd_float3x4, SIMD3<Float>) -> SIMD4<Float>](/documentation/simd/simd_float3x4/*(_:_:)-5hu83)
- [static func * (SIMD4<Float>, simd_float3x4) -> SIMD3<Float>](/documentation/simd/simd_float3x4/*(_:_:)-71y0j)
- [static func * (simd_float3x4, Float) -> simd_float3x4](/documentation/simd/simd_float3x4/*(_:_:)-7vkfz)
- [static func * (simd_float3x4, float4x3) -> float4x4](/documentation/simd/simd_float3x4/*(_:_:)-8gb9i)
- [static func * (simd_float3x4, float3x3) -> float3x4](/documentation/simd/simd_float3x4/*(_:_:)-ehb7)
- [static func *= (inout simd_float3x4, Float)](/documentation/simd/simd_float3x4/*=(_:_:)-4brfc)
- [static func *= (inout simd_float3x4, float3x3)](/documentation/simd/simd_float3x4/*=(_:_:)-8yuww)
- [static func + (simd_float3x4, simd_float3x4) -> simd_float3x4](/documentation/simd/simd_float3x4/+(_:_:))
- [static func += (inout simd_float3x4, simd_float3x4)](/documentation/simd/simd_float3x4/+=(_:_:))
- [static func - (simd_float3x4) -> simd_float3x4](/documentation/simd/simd_float3x4/-(_:))
- [static func - (simd_float3x4, simd_float3x4) -> simd_float3x4](/documentation/simd/simd_float3x4/-(_:_:))
- [static func -= (inout simd_float3x4, simd_float3x4)](/documentation/simd/simd_float3x4/-=(_:_:))
- [simd_float4x2](/documentation/simd/simd_float4x2)

### Initializers

- [init()](/documentation/simd/simd_float4x2/init())
- [init(Float)](/documentation/simd/simd_float4x2/init(_:)-4xu3o)
- [init(diagonal: SIMD2<Float>)](/documentation/simd/simd_float4x2/init(diagonal:))
- [init([SIMD2<Float>])](/documentation/simd/simd_float4x2/init(_:)-5k3p5)
- [init(SIMD2<Float>, SIMD2<Float>, SIMD2<Float>, SIMD2<Float>)](/documentation/simd/simd_float4x2/init(_:_:_:_:))
- [init(columns: (simd_float2, simd_float2, simd_float2, simd_float2))](/documentation/simd/simd_float4x2/init(columns:))
- [init(rows: [SIMD4<Float>])](/documentation/simd/simd_float4x2/init(rows:))

### Matrix Properties

- [var transpose: float2x4](/documentation/simd/simd_float4x2/transpose)
- [var columns: (simd_float2, simd_float2, simd_float2, simd_float2)](/documentation/simd/simd_float4x2/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_float2, simd_float2, simd_float2, simd_float2) -> simd_float4x2](/documentation/simd/simd_matrix(_:_:_:_:)-xobw)
- [func simd_matrix_from_rows(simd_float4, simd_float4) -> simd_float4x2](/documentation/simd/simd_matrix_from_rows(_:_:)-4lzrf)
- [func matrix_from_rows(SIMD4<Float>, SIMD4<Float>) -> simd_float4x2](/documentation/simd/matrix_from_rows(_:_:)-2ip8)

### Element Access

- [subscript(Int) -> SIMD2<Float>](/documentation/simd/simd_float4x2/subscript(_:))
- [subscript(Int, Int) -> Float](/documentation/simd/simd_float4x2/subscript(_:_:))

### Type Aliases

- [float4x2](/documentation/simd/float4x2)
- [matrix_float4x2](/documentation/simd/matrix_float4x2)

### Deprecated Symbols

- [func matrix_equal(simd_float4x2, simd_float4x2) -> Bool](/documentation/simd/matrix_equal(_:_:)-1izln)
- [func matrix_from_columns(SIMD2<Float>, SIMD2<Float>, SIMD2<Float>, SIMD2<Float>) -> simd_float4x2](/documentation/simd/matrix_from_columns(_:_:_:_:)-2u92u)
- [func matrix_transpose(simd_float2x4) -> float4x2](/documentation/simd/matrix_transpose(_:)-260wn)
- [var cmatrix: simd_float4x2](/documentation/simd/simd_float4x2/cmatrix)
- [init(simd_float4x2)](/documentation/simd/simd_float4x2/init(_:)-2e140)

### Operators

- [static func * (simd_float4x2, Float) -> simd_float4x2](/documentation/simd/simd_float4x2/*(_:_:)-3xkqa)
- [static func * (simd_float4x2, float3x4) -> float3x2](/documentation/simd/simd_float4x2/*(_:_:)-5f1f2)
- [static func * (simd_float4x2, float2x4) -> float2x2](/documentation/simd/simd_float4x2/*(_:_:)-85wgv)
- [static func * (simd_float4x2, float4x4) -> float4x2](/documentation/simd/simd_float4x2/*(_:_:)-93u9t)
- [static func * (Float, simd_float4x2) -> simd_float4x2](/documentation/simd/simd_float4x2/*(_:_:)-9kthx)
- [static func * (simd_float4x2, SIMD4<Float>) -> SIMD2<Float>](/documentation/simd/simd_float4x2/*(_:_:)-9wwew)
- [static func * (SIMD2<Float>, simd_float4x2) -> SIMD4<Float>](/documentation/simd/simd_float4x2/*(_:_:)-jxxr)
- [static func *= (inout simd_float4x2, Float)](/documentation/simd/simd_float4x2/*=(_:_:)-24lqw)
- [static func *= (inout simd_float4x2, float4x4)](/documentation/simd/simd_float4x2/*=(_:_:)-39csh)
- [static func + (simd_float4x2, simd_float4x2) -> simd_float4x2](/documentation/simd/simd_float4x2/+(_:_:))
- [static func += (inout simd_float4x2, simd_float4x2)](/documentation/simd/simd_float4x2/+=(_:_:))
- [static func - (simd_float4x2) -> simd_float4x2](/documentation/simd/simd_float4x2/-(_:))
- [static func - (simd_float4x2, simd_float4x2) -> simd_float4x2](/documentation/simd/simd_float4x2/-(_:_:))
- [static func -= (inout simd_float4x2, simd_float4x2)](/documentation/simd/simd_float4x2/-=(_:_:))
- [simd_float4x3](/documentation/simd/simd_float4x3)

### Initializers

- [init()](/documentation/simd/simd_float4x3/init())
- [init(Float)](/documentation/simd/simd_float4x3/init(_:)-4h0e8)
- [init(diagonal: SIMD3<Float>)](/documentation/simd/simd_float4x3/init(diagonal:))
- [init([SIMD3<Float>])](/documentation/simd/simd_float4x3/init(_:)-50uqp)
- [init(SIMD3<Float>, SIMD3<Float>, SIMD3<Float>, SIMD3<Float>)](/documentation/simd/simd_float4x3/init(_:_:_:_:))
- [init(columns: (simd_float3, simd_float3, simd_float3, simd_float3))](/documentation/simd/simd_float4x3/init(columns:))
- [init(rows: [SIMD4<Float>])](/documentation/simd/simd_float4x3/init(rows:))
- [init(AffineTransform3D)](/documentation/simd/simd_float4x3/init(_:)-3rlc3)
- [init(affineTransform: AffineTransform3D)](/documentation/simd/simd_float4x3/init(affinetransform:))

### Matrix Properties

- [var transpose: float3x4](/documentation/simd/simd_float4x3/transpose)
- [var columns: (simd_float3, simd_float3, simd_float3, simd_float3)](/documentation/simd/simd_float4x3/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_float3, simd_float3, simd_float3, simd_float3) -> simd_float4x3](/documentation/simd/simd_matrix(_:_:_:_:)-55qff)
- [func simd_matrix_from_rows(simd_float4, simd_float4, simd_float4) -> simd_float4x3](/documentation/simd/simd_matrix_from_rows(_:_:_:)-81rfz)
- [func matrix_from_rows(SIMD4<Float>, SIMD4<Float>, SIMD4<Float>) -> simd_float4x3](/documentation/simd/matrix_from_rows(_:_:_:)-ld0y)

### Element Access

- [subscript(Int) -> SIMD3<Float>](/documentation/simd/simd_float4x3/subscript(_:))
- [subscript(Int, Int) -> Float](/documentation/simd/simd_float4x3/subscript(_:_:))

### Type Aliases

- [float4x3](/documentation/simd/float4x3)
- [matrix_float4x3](/documentation/simd/matrix_float4x3)

### Deprecated Symbols

- [func matrix_equal(simd_float4x3, simd_float4x3) -> Bool](/documentation/simd/matrix_equal(_:_:)-2m44x)
- [func matrix_from_columns(SIMD3<Float>, SIMD3<Float>, SIMD3<Float>, SIMD3<Float>) -> simd_float4x3](/documentation/simd/matrix_from_columns(_:_:_:_:)-7tq9m)
- [func matrix_transpose(simd_float3x4) -> float4x3](/documentation/simd/matrix_transpose(_:)-2oa75)
- [var cmatrix: simd_float4x3](/documentation/simd/simd_float4x3/cmatrix)
- [init(simd_float4x3)](/documentation/simd/simd_float4x3/init(_:)-6f0m9)

### Operators

- [static func * (simd_float4x3, SIMD4<Float>) -> SIMD3<Float>](/documentation/simd/simd_float4x3/*(_:_:)-2x5u4)
- [static func * (SIMD3<Float>, simd_float4x3) -> SIMD4<Float>](/documentation/simd/simd_float4x3/*(_:_:)-3hma7)
- [static func * (simd_float4x3, float2x4) -> float2x3](/documentation/simd/simd_float4x3/*(_:_:)-3u8eq)
- [static func * (simd_float4x3, Float) -> simd_float4x3](/documentation/simd/simd_float4x3/*(_:_:)-3wqpi)
- [static func * (simd_float4x3, float4x4) -> float4x3](/documentation/simd/simd_float4x3/*(_:_:)-5if2f)
- [static func * (simd_float4x3, float3x4) -> float3x3](/documentation/simd/simd_float4x3/*(_:_:)-6s4w1)
- [static func * (Float, simd_float4x3) -> simd_float4x3](/documentation/simd/simd_float4x3/*(_:_:)-6v4mm)
- [static func *= (inout simd_float4x3, float4x4)](/documentation/simd/simd_float4x3/*=(_:_:)-5uxwu)
- [static func *= (inout simd_float4x3, Float)](/documentation/simd/simd_float4x3/*=(_:_:)-9icea)
- [static func + (simd_float4x3, simd_float4x3) -> simd_float4x3](/documentation/simd/simd_float4x3/+(_:_:))
- [static func += (inout simd_float4x3, simd_float4x3)](/documentation/simd/simd_float4x3/+=(_:_:))
- [static func - (simd_float4x3) -> simd_float4x3](/documentation/simd/simd_float4x3/-(_:))
- [static func - (simd_float4x3, simd_float4x3) -> simd_float4x3](/documentation/simd/simd_float4x3/-(_:_:))
- [static func -= (inout simd_float4x3, simd_float4x3)](/documentation/simd/simd_float4x3/-=(_:_:))
- [simd_float4x4](/documentation/simd/simd_float4x4)

### Initializers

- [init()](/documentation/simd/simd_float4x4/init())
- [init(Float)](/documentation/simd/simd_float4x4/init(_:)-6pc85)
- [init(diagonal: SIMD4<Float>)](/documentation/simd/simd_float4x4/init(diagonal:))
- [init([SIMD4<Float>])](/documentation/simd/simd_float4x4/init(_:)-50sjs)
- [init(simd_quatf)](/documentation/simd/simd_float4x4/init(_:)-7ig5g)
- [init(SCNMatrix4)](/documentation/simd/simd_float4x4/init(_:)-4jrbw)
- [init(SCNMatrix4)](/documentation/simd/simd_float4x4/init(_:)-q9z6)
- [init(SIMD4<Float>, SIMD4<Float>, SIMD4<Float>, SIMD4<Float>)](/documentation/simd/simd_float4x4/init(_:_:_:_:))
- [init(columns: (simd_float4, simd_float4, simd_float4, simd_float4))](/documentation/simd/simd_float4x4/init(columns:))
- [init(rows: [SIMD4<Float>])](/documentation/simd/simd_float4x4/init(rows:))
- [init(AffineTransform3D)](/documentation/simd/simd_float4x4/init(_:)-3op4b)
- [init(ProjectiveTransform3D)](/documentation/simd/simd_float4x4/init(_:)-9txnb)
- [init(Pose3D)](/documentation/simd/simd_float4x4/init(_:)-77vxr)
- [init(affineTransform: AffineTransform3D)](/documentation/simd/simd_float4x4/init(affinetransform:))
- [init(pose: Pose3D)](/documentation/simd/simd_float4x4/init(pose:))
- [init(projectiveTransform: ProjectiveTransform3D)](/documentation/simd/simd_float4x4/init(projectivetransform:))

### Matrix Constants

- [let matrix_identity_float4x4: simd_float4x4](/documentation/simd/matrix_identity_float4x4)

### Matrix Properties

- [var determinant: Float](/documentation/simd/simd_float4x4/determinant)
- [var inverse: simd_float4x4](/documentation/simd/simd_float4x4/inverse)
- [var transpose: float4x4](/documentation/simd/simd_float4x4/transpose)
- [var columns: (simd_float4, simd_float4, simd_float4, simd_float4)](/documentation/simd/simd_float4x4/columns)

### Matrix Creation Functions

- [func simd_matrix(simd_float4, simd_float4, simd_float4, simd_float4) -> simd_float4x4](/documentation/simd/simd_matrix(_:_:_:_:)-4p5ox)
- [func simd_matrix_from_rows(simd_float4, simd_float4, simd_float4, simd_float4) -> simd_float4x4](/documentation/simd/simd_matrix_from_rows(_:_:_:_:)-34hac)
- [func matrix_from_rows(SIMD4<Float>, SIMD4<Float>, SIMD4<Float>, SIMD4<Float>) -> simd_float4x4](/documentation/simd/matrix_from_rows(_:_:_:_:)-18jb3)
- [func simd_matrix4x4(simd_quatf) -> simd_float4x4](/documentation/simd/simd_matrix4x4(_:)-20lv7)

### Element Access

- [subscript(Int) -> SIMD4<Float>](/documentation/simd/simd_float4x4/subscript(_:))
- [subscript(Int, Int) -> Float](/documentation/simd/simd_float4x4/subscript(_:_:))

### Type Aliases

- [float4x4](/documentation/simd/float4x4)
- [matrix_float4x4](/documentation/simd/matrix_float4x4)

### Deprecated Symbols

- [func matrix_invert(simd_float4x4) -> simd_float4x4](/documentation/simd/matrix_invert(_:)-7fevy)
- [func matrix_from_diagonal(SIMD4<Float>) -> simd_float4x4](/documentation/simd/matrix_from_diagonal(_:)-71pds)
- [func matrix_determinant(simd_float4x4) -> Float](/documentation/simd/matrix_determinant(_:)-4yqoy)
- [func matrix_equal(simd_float4x4, simd_float4x4) -> Bool](/documentation/simd/matrix_equal(_:_:)-752xl)
- [func matrix_from_columns(SIMD4<Float>, SIMD4<Float>, SIMD4<Float>, SIMD4<Float>) -> simd_float4x4](/documentation/simd/matrix_from_columns(_:_:_:_:)-5d0yw)
- [func matrix_transpose(simd_float4x4) -> float4x4](/documentation/simd/matrix_transpose(_:)-8t44c)
- [var cmatrix: simd_float4x4](/documentation/simd/simd_float4x4/cmatrix)
- [init(simd_float4x4)](/documentation/simd/simd_float4x4/init(_:)-2ga0f)

### Operators

- [static func * (simd_float4x4, Float) -> simd_float4x4](/documentation/simd/simd_float4x4/*(_:_:)-1qmhs)
- [static func * (simd_float4x4, float2x4) -> float2x4](/documentation/simd/simd_float4x4/*(_:_:)-1qwyg)
- [static func * (simd_float4x4, float4x4) -> float4x4](/documentation/simd/simd_float4x4/*(_:_:)-6yrrr)
- [static func * (SIMD4<Float>, simd_float4x4) -> SIMD4<Float>](/documentation/simd/simd_float4x4/*(_:_:)-973nq)
- [static func * (simd_float4x4, float3x4) -> float3x4](/documentation/simd/simd_float4x4/*(_:_:)-97jjs)
- [static func * (simd_float4x4, SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/simd_float4x4/*(_:_:)-9bvh7)
- [static func * (Float, simd_float4x4) -> simd_float4x4](/documentation/simd/simd_float4x4/*(_:_:)-vr6m)
- [static func *= (inout simd_float4x4, float4x4)](/documentation/simd/simd_float4x4/*=(_:_:)-10057)
- [static func *= (inout simd_float4x4, Float)](/documentation/simd/simd_float4x4/*=(_:_:)-43syc)
- [static func + (simd_float4x4, simd_float4x4) -> simd_float4x4](/documentation/simd/simd_float4x4/+(_:_:))
- [static func += (inout simd_float4x4, simd_float4x4)](/documentation/simd/simd_float4x4/+=(_:_:))
- [static func - (simd_float4x4) -> simd_float4x4](/documentation/simd/simd_float4x4/-(_:))
- [static func - (simd_float4x4, simd_float4x4) -> simd_float4x4](/documentation/simd/simd_float4x4/-(_:_:))
- [static func -= (inout simd_float4x4, simd_float4x4)](/documentation/simd/simd_float4x4/-=(_:_:))
- [simd_half2x2](/documentation/simd/simd_half2x2)

### Initializers

- [init()](/documentation/simd/simd_half2x2/init())
- [init(columns: (simd_half2, simd_half2))](/documentation/simd/simd_half2x2/init(columns:))

### Matrix properties

- [var columns: (simd_half2, simd_half2)](/documentation/simd/simd_half2x2/columns)

### Matrix constants

- [let matrix_identity_half2x2: simd_half2x2](/documentation/simd/matrix_identity_half2x2)

### Matrix creation functions

- [func simd_matrix(simd_half2, simd_half2) -> simd_half2x2](/documentation/simd/simd_matrix(_:_:)-1w6b0)
- [func simd_matrix_from_rows(simd_half2, simd_half2) -> simd_half2x2](/documentation/simd/simd_matrix_from_rows(_:_:)-9lrpr)
- [simd_half2x3](/documentation/simd/simd_half2x3)

### Initializers

- [init()](/documentation/simd/simd_half2x3/init())
- [init(columns: (simd_half3, simd_half3))](/documentation/simd/simd_half2x3/init(columns:))

### Matrix properties

- [var columns: (simd_half3, simd_half3)](/documentation/simd/simd_half2x3/columns)

### Matrix creation functions

- [func simd_matrix(simd_half3, simd_half3) -> simd_half2x3](/documentation/simd/simd_matrix(_:_:)-33y1x)
- [func simd_matrix_from_rows(simd_half2, simd_half2, simd_half2) -> simd_half2x3](/documentation/simd/simd_matrix_from_rows(_:_:_:)-6y100)
- [simd_half2x4](/documentation/simd/simd_half2x4)

### Initializers

- [init()](/documentation/simd/simd_half2x4/init())
- [init(columns: (simd_half4, simd_half4))](/documentation/simd/simd_half2x4/init(columns:))

### Matrix properties

- [var columns: (simd_half4, simd_half4)](/documentation/simd/simd_half2x4/columns)

### Matrix creation functions

- [func simd_matrix(simd_half4, simd_half4) -> simd_half2x4](/documentation/simd/simd_matrix(_:_:)-3087y)
- [func simd_matrix_from_rows(simd_half2, simd_half2, simd_half2, simd_half2) -> simd_half2x4](/documentation/simd/simd_matrix_from_rows(_:_:_:_:)-76zte)
- [simd_half3x2](/documentation/simd/simd_half3x2)

### Initializers

- [init()](/documentation/simd/simd_half3x2/init())
- [init(columns: (simd_half2, simd_half2, simd_half2))](/documentation/simd/simd_half3x2/init(columns:))

### Matrix properties

- [var columns: (simd_half2, simd_half2, simd_half2)](/documentation/simd/simd_half3x2/columns)

### Matrix creation functions

- [func simd_matrix(simd_half2, simd_half2, simd_half2) -> simd_half3x2](/documentation/simd/simd_matrix(_:_:_:)-9lkar)
- [func simd_matrix_from_rows(simd_half3, simd_half3) -> simd_half3x2](/documentation/simd/simd_matrix_from_rows(_:_:)-6oc46)
- [simd_half3x3](/documentation/simd/simd_half3x3)

### Initializers

- [init()](/documentation/simd/simd_half3x3/init())
- [init(columns: (simd_half3, simd_half3, simd_half3))](/documentation/simd/simd_half3x3/init(columns:))

### Matrix properties

- [var columns: (simd_half3, simd_half3, simd_half3)](/documentation/simd/simd_half3x3/columns)

### Matrix constants

- [let matrix_identity_half3x3: simd_half3x3](/documentation/simd/matrix_identity_half3x3)

### Matrix creation functions

- [func simd_matrix(simd_half3, simd_half3, simd_half3) -> simd_half3x3](/documentation/simd/simd_matrix(_:_:_:)-2bbz7)
- [func simd_matrix_from_rows(simd_half3, simd_half3, simd_half3) -> simd_half3x3](/documentation/simd/simd_matrix_from_rows(_:_:_:)-60h5f)
- [simd_half3x4](/documentation/simd/simd_half3x4)

### Initializers

- [init()](/documentation/simd/simd_half3x4/init())
- [init(columns: (simd_half4, simd_half4, simd_half4))](/documentation/simd/simd_half3x4/init(columns:))

### Matrix properties

- [var columns: (simd_half4, simd_half4, simd_half4)](/documentation/simd/simd_half3x4/columns)

### Matrix creation functions

- [func simd_matrix(simd_half4, simd_half4, simd_half4) -> simd_half3x4](/documentation/simd/simd_matrix(_:_:_:)-5oh9m)
- [func simd_matrix_from_rows(simd_half3, simd_half3, simd_half3, simd_half3) -> simd_half3x4](/documentation/simd/simd_matrix_from_rows(_:_:_:_:)-9v9ky)
- [simd_half4x2](/documentation/simd/simd_half4x2)

### Initializers

- [init()](/documentation/simd/simd_half4x2/init())
- [init(columns: (simd_half2, simd_half2, simd_half2, simd_half2))](/documentation/simd/simd_half4x2/init(columns:))

### Matrix properties

- [var columns: (simd_half2, simd_half2, simd_half2, simd_half2)](/documentation/simd/simd_half4x2/columns)

### Matrix creation functions

- [func simd_matrix(simd_half2, simd_half2, simd_half2, simd_half2) -> simd_half4x2](/documentation/simd/simd_matrix(_:_:_:_:)-9nj2)
- [func simd_matrix_from_rows(simd_half4, simd_half4) -> simd_half4x2](/documentation/simd/simd_matrix_from_rows(_:_:)-74k)
- [simd_half4x3](/documentation/simd/simd_half4x3)

### Initializers

- [init()](/documentation/simd/simd_half4x3/init())
- [init(columns: (simd_half3, simd_half3, simd_half3, simd_half3))](/documentation/simd/simd_half4x3/init(columns:))

### Matrix properties

- [var columns: (simd_half3, simd_half3, simd_half3, simd_half3)](/documentation/simd/simd_half4x3/columns)

### Matrix creation functions

- [func simd_matrix(simd_half3, simd_half3, simd_half3, simd_half3) -> simd_half4x3](/documentation/simd/simd_matrix(_:_:_:_:)-6ene)
- [func simd_matrix_from_rows(simd_half4, simd_half4, simd_half4) -> simd_half4x3](/documentation/simd/simd_matrix_from_rows(_:_:_:)-7bb0v)
- [simd_half4x4](/documentation/simd/simd_half4x4)

### Initializers

- [init()](/documentation/simd/simd_half4x4/init())
- [init(columns: (simd_half4, simd_half4, simd_half4, simd_half4))](/documentation/simd/simd_half4x4/init(columns:))

### Matrix properties

- [var columns: (simd_half4, simd_half4, simd_half4, simd_half4)](/documentation/simd/simd_half4x4/columns)

### Matrix constants

- [let matrix_identity_half4x4: simd_half4x4](/documentation/simd/matrix_identity_half4x4)

### Matrix creation functions

- [func simd_matrix(simd_half4, simd_half4, simd_half4, simd_half4) -> simd_half4x4](/documentation/simd/simd_matrix(_:_:_:_:)-7ltt0)
- [func simd_matrix_from_rows(simd_half4, simd_half4, simd_half4, simd_half4) -> simd_half4x4](/documentation/simd/simd_matrix_from_rows(_:_:_:_:)-31gpp)
- [simd_quatd](/documentation/simd/simd_quatd)

### Initializing a quaternion

- [init()](/documentation/simd/simd_quatd/init())
- [init(vector: simd_double4)](/documentation/simd/simd_quatd/init(vector:))
- [init(simd_double3x3)](/documentation/simd/simd_quatd/init(_:)-791zk)
- [init(simd_double4x4)](/documentation/simd/simd_quatd/init(_:)-5vcd5)
- [init(angle: Double, axis: SIMD3<Double>)](/documentation/simd/simd_quatd/init(angle:axis:))
- [init(from: SIMD3<Double>, to: SIMD3<Double>)](/documentation/simd/simd_quatd/init(from:to:))
- [init(ix: Double, iy: Double, iz: Double, r: Double)](/documentation/simd/simd_quatd/init(ix:iy:iz:r:))
- [init(real: Double, imag: SIMD3<Double>)](/documentation/simd/simd_quatd/init(real:imag:))

### Querying a quaternion’s properties

- [var angle: Double](/documentation/simd/simd_quatd/angle)
- [var axis: SIMD3<Double>](/documentation/simd/simd_quatd/axis)
- [var conjugate: simd_quatd](/documentation/simd/simd_quatd/conjugate)
- [var imag: SIMD3<Double>](/documentation/simd/simd_quatd/imag)
- [var real: Double](/documentation/simd/simd_quatd/real)
- [var inverse: simd_quatd](/documentation/simd/simd_quatd/inverse)
- [var length: Double](/documentation/simd/simd_quatd/length)
- [var normalized: simd_quatd](/documentation/simd/simd_quatd/normalized)
- [var vector: simd_double4](/documentation/simd/simd_quatd/vector)

### Creating a quaternion from other data types

- [func simd_quaternion(Double, Double, Double, Double) -> simd_quatd](/documentation/simd/simd_quaternion(_:_:_:_:)-1adm9)
- [func simd_quaternion(Double, simd_double3) -> simd_quatd](/documentation/simd/simd_quaternion(_:_:)-2jzvc)
- [func simd_quaternion(UnsafePointer<Double>!) -> simd_quatd](/documentation/simd/simd_quaternion(_:)-8kl4p)
- [func simd_quaternion(simd_double3, simd_double3) -> simd_quatd](/documentation/simd/simd_quaternion(_:_:)-2yoqw)
- [func simd_quaternion(simd_double3x3) -> simd_quatd](/documentation/simd/simd_quaternion(_:)-7paor)
- [func simd_quaternion(simd_double4) -> simd_quatd](/documentation/simd/simd_quaternion(_:)-459vs)
- [func simd_quaternion(simd_double4x4) -> simd_quatd](/documentation/simd/simd_quaternion(_:)-8e0xf)

### Applying arithmetic operations to quaternions

- [func simd_add(simd_quatd, simd_quatd) -> simd_quatd](/documentation/simd/simd_add(_:_:)-6ohmq)
- [func simd_mul(simd_quatd, simd_quatd) -> simd_quatd](/documentation/simd/simd_mul(_:_:)-531pe)
- [func simd_mul(Double, simd_quatd) -> simd_quatd](/documentation/simd/simd_mul(_:_:)-8aedk)
- [func simd_mul(simd_quatd, Double) -> simd_quatd](/documentation/simd/simd_mul(_:_:)-8uidm)
- [func simd_sub(simd_quatd, simd_quatd) -> simd_quatd](/documentation/simd/simd_sub(_:_:)-87caf)
- [func exp(simd_quatd) -> simd_quatd](/documentation/simd/exp(_:)-9nl1f)
- [func log(simd_quatd) -> simd_quatd](/documentation/simd/log(_:)-77xdo)

### Applying geometric operations to quaternions

- [func simd_act(simd_quatd, simd_double3) -> simd_double3](/documentation/simd/simd_act(_:_:)-47h09)
- [func act(SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/simd_quatd/act(_:))
- [func simd_angle(simd_quatd) -> Double](/documentation/simd/simd_angle(_:)-zuvx)
- [func simd_axis(simd_quatd) -> simd_double3](/documentation/simd/simd_axis(_:)-56wf4)
- [func simd_bezier(simd_quatd, simd_quatd, simd_quatd, simd_quatd, Double) -> simd_quatd](/documentation/simd/simd_bezier(_:_:_:_:_:)-556xd)
- [func simd_conjugate(simd_quatd) -> simd_quatd](/documentation/simd/simd_conjugate(_:)-98awl)
- [func simd_imag(simd_quatd) -> simd_double3](/documentation/simd/simd_imag(_:)-2c7fz)
- [func simd_negate(simd_quatd) -> simd_quatd](/documentation/simd/simd_negate(_:)-3ysgu)
- [func simd_real(simd_quatd) -> Double](/documentation/simd/simd_real(_:)-75t5f)
- [func simd_slerp(simd_quatd, simd_quatd, Double) -> simd_quatd](/documentation/simd/simd_slerp(_:_:_:)-65dt5)
- [func simd_slerp_longest(simd_quatd, simd_quatd, Double) -> simd_quatd](/documentation/simd/simd_slerp_longest(_:_:_:)-8hbz2)
- [func simd_spline(simd_quatd, simd_quatd, simd_quatd, simd_quatd, Double) -> simd_quatd](/documentation/simd/simd_spline(_:_:_:_:_:)-19wbg)
- [func simd_dot(simd_quatd, simd_quatd) -> Double](/documentation/simd/simd_dot(_:_:)-2bnqp)
- [func dot(simd_quatd, simd_quatd) -> Double](/documentation/simd/dot(_:_:)-438xp)
- [func simd_length(simd_quatd) -> Double](/documentation/simd/simd_length(_:)-52o29)
- [func simd_normalize(simd_quatd) -> simd_quatd](/documentation/simd/simd_normalize(_:)-ud11)

### Inverting a quaternion

- [func simd_inverse(simd_quatd) -> simd_quatd](/documentation/simd/simd_inverse(_:)-3cvvi)

### Providing a hash value

- [func hash(into: inout Hasher)](/documentation/simd/simd_quatd/hash(into:))

### Operators

- [static func * (simd_quatd, simd_quatd) -> simd_quatd](/documentation/simd/simd_quatd/*(_:_:)-5wd9q)
- [static func * (simd_quatd, Double) -> simd_quatd](/documentation/simd/simd_quatd/*(_:_:)-5wtdl)
- [static func * (Double, simd_quatd) -> simd_quatd](/documentation/simd/simd_quatd/*(_:_:)-6yv0o)
- [static func *= (inout simd_quatd, Double)](/documentation/simd/simd_quatd/*=(_:_:)-66wf4)
- [static func *= (inout simd_quatd, simd_quatd)](/documentation/simd/simd_quatd/*=(_:_:)-9rhrs)
- [static func + (simd_quatd, simd_quatd) -> simd_quatd](/documentation/simd/simd_quatd/+(_:_:))
- [static func += (inout simd_quatd, simd_quatd)](/documentation/simd/simd_quatd/+=(_:_:))
- [static func - (simd_quatd) -> simd_quatd](/documentation/simd/simd_quatd/-(_:))
- [static func - (simd_quatd, simd_quatd) -> simd_quatd](/documentation/simd/simd_quatd/-(_:_:))
- [static func -= (inout simd_quatd, simd_quatd)](/documentation/simd/simd_quatd/-=(_:_:))
- [static func / (simd_quatd, Double) -> simd_quatd](/documentation/simd/simd_quatd/_(_:_:)-2ftmo)
- [static func / (simd_quatd, simd_quatd) -> simd_quatd](/documentation/simd/simd_quatd/_(_:_:)-dhx4)
- [static func /= (inout simd_quatd, simd_quatd)](/documentation/simd/simd_quatd/_=(_:_:)-40h2o)
- [static func /= (inout simd_quatd, Double)](/documentation/simd/simd_quatd/_=(_:_:)-4w1si)

### Initializers

- [init(Rotation3DFloat)](/documentation/simd/simd_quatd/init(_:)-3wkyg)

### Default Implementations

- [Hashable Implementations](/documentation/simd/simd_quatd/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/simd/simd_quatd/hash(into:))
- [simd_quatf](/documentation/simd/simd_quatf)

### Initializing a quaternion

- [init()](/documentation/simd/simd_quatf/init())
- [init(vector: simd_float4)](/documentation/simd/simd_quatf/init(vector:))
- [init(simd_float3x3)](/documentation/simd/simd_quatf/init(_:)-1hlsg)
- [init(simd_float4x4)](/documentation/simd/simd_quatf/init(_:)-3751)
- [init(angle: Float, axis: SIMD3<Float>)](/documentation/simd/simd_quatf/init(angle:axis:))
- [init(from: SIMD3<Float>, to: SIMD3<Float>)](/documentation/simd/simd_quatf/init(from:to:))
- [init(ix: Float, iy: Float, iz: Float, r: Float)](/documentation/simd/simd_quatf/init(ix:iy:iz:r:))
- [init(real: Float, imag: SIMD3<Float>)](/documentation/simd/simd_quatf/init(real:imag:))
- [init(Rotation3D)](/documentation/simd/simd_quatf/init(_:)-9rvr0)

### Querying a quaternion’s properties

- [var angle: Float](/documentation/simd/simd_quatf/angle)
- [var axis: SIMD3<Float>](/documentation/simd/simd_quatf/axis)
- [var conjugate: simd_quatf](/documentation/simd/simd_quatf/conjugate)
- [var imag: SIMD3<Float>](/documentation/simd/simd_quatf/imag)
- [var real: Float](/documentation/simd/simd_quatf/real)
- [var inverse: simd_quatf](/documentation/simd/simd_quatf/inverse)
- [var length: Float](/documentation/simd/simd_quatf/length)
- [var normalized: simd_quatf](/documentation/simd/simd_quatf/normalized)
- [var vector: simd_float4](/documentation/simd/simd_quatf/vector)

### Creating a quaternion from other data types

- [func simd_quaternion(Float, Float, Float, Float) -> simd_quatf](/documentation/simd/simd_quaternion(_:_:_:_:)-8aad4)
- [func simd_quaternion(Float, simd_float3) -> simd_quatf](/documentation/simd/simd_quaternion(_:_:)-5lqb)
- [func simd_quaternion(UnsafePointer<Float>!) -> simd_quatf](/documentation/simd/simd_quaternion(_:)-8kkih)
- [func simd_quaternion(simd_float3, simd_float3) -> simd_quatf](/documentation/simd/simd_quaternion(_:_:)-18t47)
- [func simd_quaternion(simd_float3x3) -> simd_quatf](/documentation/simd/simd_quaternion(_:)-2qm7k)
- [func simd_quaternion(simd_float4) -> simd_quatf](/documentation/simd/simd_quaternion(_:)-459a0)
- [func simd_quaternion(simd_float4x4) -> simd_quatf](/documentation/simd/simd_quaternion(_:)-69ido)

### Applying arithmetic operations to quaternions

- [func simd_add(simd_quatf, simd_quatf) -> simd_quatf](/documentation/simd/simd_add(_:_:)-7641g)
- [func simd_mul(simd_quatf, simd_quatf) -> simd_quatf](/documentation/simd/simd_mul(_:_:)-4a5hq)
- [func simd_mul(Float, simd_quatf) -> simd_quatf](/documentation/simd/simd_mul(_:_:)-391wq)
- [func simd_mul(simd_quatf, Float) -> simd_quatf](/documentation/simd/simd_mul(_:_:)-bqqq)
- [func simd_sub(simd_quatf, simd_quatf) -> simd_quatf](/documentation/simd/simd_sub(_:_:)-807rv)
- [func exp(simd_quatf) -> simd_quatf](/documentation/simd/exp(_:)-9q8na)
- [func log(simd_quatf) -> simd_quatf](/documentation/simd/log(_:)-xpx0)

### Applying geometric operations to quaternions

- [func simd_act(simd_quatf, simd_float3) -> simd_float3](/documentation/simd/simd_act(_:_:)-2liww)
- [func act(SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/simd_quatf/act(_:))
- [func simd_angle(simd_quatf) -> Float](/documentation/simd/simd_angle(_:)-zu9h)
- [func simd_axis(simd_quatf) -> simd_float3](/documentation/simd/simd_axis(_:)-56wzs)
- [func simd_bezier(simd_quatf, simd_quatf, simd_quatf, simd_quatf, Float) -> simd_quatf](/documentation/simd/simd_bezier(_:_:_:_:_:)-1z3gf)
- [func simd_conjugate(simd_quatf) -> simd_quatf](/documentation/simd/simd_conjugate(_:)-98bil)
- [func simd_imag(simd_quatf) -> simd_float3](/documentation/simd/simd_imag(_:)-2c837)
- [func simd_negate(simd_quatf) -> simd_quatf](/documentation/simd/simd_negate(_:)-3yt2y)
- [func simd_real(simd_quatf) -> Float](/documentation/simd/simd_real(_:)-75sl3)
- [func simd_slerp(simd_quatf, simd_quatf, Float) -> simd_quatf](/documentation/simd/simd_slerp(_:_:_:)-u2db)
- [func simd_slerp_longest(simd_quatf, simd_quatf, Float) -> simd_quatf](/documentation/simd/simd_slerp_longest(_:_:_:)-3qens)
- [func simd_spline(simd_quatf, simd_quatf, simd_quatf, simd_quatf, Float) -> simd_quatf](/documentation/simd/simd_spline(_:_:_:_:_:)-1ok51)
- [func simd_dot(simd_quatf, simd_quatf) -> Float](/documentation/simd/simd_dot(_:_:)-7frqx)
- [func dot(simd_quatf, simd_quatf) -> Float](/documentation/simd/dot(_:_:)-2en8e)
- [func simd_length(simd_quatf) -> Float](/documentation/simd/simd_length(_:)-52nf5)
- [func simd_normalize(simd_quatf) -> simd_quatf](/documentation/simd/simd_normalize(_:)-uch9)

### Inverting a quaternion

- [func simd_inverse(simd_quatf) -> simd_quatf](/documentation/simd/simd_inverse(_:)-3cvay)

### Providing a hash value

- [func hash(into: inout Hasher)](/documentation/simd/simd_quatf/hash(into:))

### Deprecated symbols

- [init(rotation: Rotation3D)](/documentation/simd/simd_quatf/init(rotation:))

### Operators

- [static func * (simd_quatf, Float) -> simd_quatf](/documentation/simd/simd_quatf/*(_:_:)-48x)
- [static func * (Float, simd_quatf) -> simd_quatf](/documentation/simd/simd_quatf/*(_:_:)-9tia3)
- [static func * (simd_quatf, simd_quatf) -> simd_quatf](/documentation/simd/simd_quatf/*(_:_:)-v1lb)
- [static func *= (inout simd_quatf, Float)](/documentation/simd/simd_quatf/*=(_:_:)-51ee0)
- [static func *= (inout simd_quatf, simd_quatf)](/documentation/simd/simd_quatf/*=(_:_:)-pcoc)
- [static func + (simd_quatf, simd_quatf) -> simd_quatf](/documentation/simd/simd_quatf/+(_:_:))
- [static func += (inout simd_quatf, simd_quatf)](/documentation/simd/simd_quatf/+=(_:_:))
- [static func - (simd_quatf) -> simd_quatf](/documentation/simd/simd_quatf/-(_:))
- [static func - (simd_quatf, simd_quatf) -> simd_quatf](/documentation/simd/simd_quatf/-(_:_:))
- [static func -= (inout simd_quatf, simd_quatf)](/documentation/simd/simd_quatf/-=(_:_:))
- [static func / (simd_quatf, simd_quatf) -> simd_quatf](/documentation/simd/simd_quatf/_(_:_:)-15qds)
- [static func / (simd_quatf, Float) -> simd_quatf](/documentation/simd/simd_quatf/_(_:_:)-1ba81)
- [static func /= (inout simd_quatf, Float)](/documentation/simd/simd_quatf/_=(_:_:)-2qypk)
- [static func /= (inout simd_quatf, simd_quatf)](/documentation/simd/simd_quatf/_=(_:_:)-5tm7m)

### Default Implementations

- [Hashable Implementations](/documentation/simd/simd_quatf/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/simd/simd_quatf/hash(into:))
- [simd_quath](/documentation/simd/simd_quath)

### Initializers

- [init()](/documentation/simd/simd_quath/init())
- [init(vector: simd_half4)](/documentation/simd/simd_quath/init(vector:))

### Instance Properties

- [var vector: simd_half4](/documentation/simd/simd_quath/vector)

## Variables

- [var SIMD_COMPILER_HAS_REQUIRED_FEATURES: Int32](/documentation/simd/simd_compiler_has_required_features)
- [var SIMD_CURRENT_LIBRARY_VERSION: Int32](/documentation/simd/simd_current_library_version)
- [var SIMD_LIBRARY_VERSION: Int32](/documentation/simd/simd_library_version)

## Functions

- [func abs(simd_half3) -> simd_half3](/documentation/simd/abs(_:)-1oaic)
- [func abs(simd_half8) -> simd_half8](/documentation/simd/abs(_:)-23x59)
- [func abs(simd_half4) -> simd_half4](/documentation/simd/abs(_:)-2sqwt)
- [func abs(simd_half32) -> simd_half32](/documentation/simd/abs(_:)-4qe6n)
- [func abs(simd_half2) -> simd_half2](/documentation/simd/abs(_:)-5f1om)
- [func abs(simd_half16) -> simd_half16](/documentation/simd/abs(_:)-5yvia)
- [func ceil(simd_half32) -> simd_half32](/documentation/simd/ceil(_:)-2mz12)
- [func ceil(simd_half2) -> simd_half2](/documentation/simd/ceil(_:)-2y927)
- [func ceil(simd_half8) -> simd_half8](/documentation/simd/ceil(_:)-3qezc)
- [func ceil(simd_half16) -> simd_half16](/documentation/simd/ceil(_:)-5zaxi)
- [func ceil(simd_half3) -> simd_half3](/documentation/simd/ceil(_:)-6phu2)
- [func ceil(simd_half4) -> simd_half4](/documentation/simd/ceil(_:)-6qwcw)
- [func floor(simd_half4) -> simd_half4](/documentation/simd/floor(_:)-2r68l)
- [func floor(simd_half16) -> simd_half16](/documentation/simd/floor(_:)-51eh3)
- [func floor(simd_half2) -> simd_half2](/documentation/simd/floor(_:)-5kj31)
- [func floor(simd_half32) -> simd_half32](/documentation/simd/floor(_:)-5yv9x)
- [func floor(simd_half8) -> simd_half8](/documentation/simd/floor(_:)-8noum)
- [func floor(simd_half3) -> simd_half3](/documentation/simd/floor(_:)-9w8kb)
- [func max(simd_half16, simd_half16) -> simd_half16](/documentation/simd/max(_:_:)-3ia66)
- [func max(simd_half16, Float16) -> simd_half16](/documentation/simd/max(_:_:)-3nrjh)
- [func max(simd_half32, simd_half32) -> simd_half32](/documentation/simd/max(_:_:)-51f8j)
- [func max(simd_half32, Float16) -> simd_half32](/documentation/simd/max(_:_:)-54mlg)
- [func max(simd_half3, Float16) -> simd_half3](/documentation/simd/max(_:_:)-6dcr1)
- [func max(simd_half3, simd_half3) -> simd_half3](/documentation/simd/max(_:_:)-6ityy)
- [func max(simd_half2, simd_half2) -> simd_half2](/documentation/simd/max(_:_:)-7kwai)
- [func max(simd_half2, Float16) -> simd_half2](/documentation/simd/max(_:_:)-7nw7d)
- [func max(simd_half8, simd_half8) -> simd_half8](/documentation/simd/max(_:_:)-8ukdb)
- [func max(simd_half8, Float16) -> simd_half8](/documentation/simd/max(_:_:)-8xrps)
- [func max(simd_half4, simd_half4) -> simd_half4](/documentation/simd/max(_:_:)-960b9)
- [func max(simd_half4, Float16) -> simd_half4](/documentation/simd/max(_:_:)-997qu)
- [func min(simd_half4, simd_half4) -> simd_half4](/documentation/simd/min(_:_:)-5rg96)
- [func min(simd_half4, Float16) -> simd_half4](/documentation/simd/min(_:_:)-5ul5l)
- [func min(simd_half16, simd_half16) -> simd_half16](/documentation/simd/min(_:_:)-67sp6)
- [func min(simd_half16, Float16) -> simd_half16](/documentation/simd/min(_:_:)-6b02l)
- [func min(simd_half2, simd_half2) -> simd_half2](/documentation/simd/min(_:_:)-735cl)
- [func min(simd_half2, Float16) -> simd_half2](/documentation/simd/min(_:_:)-76cpi)
- [func min(simd_half32, simd_half32) -> simd_half32](/documentation/simd/min(_:_:)-7bq1b)
- [func min(simd_half32, Float16) -> simd_half32](/documentation/simd/min(_:_:)-7ezvg)
- [func min(simd_half8, simd_half8) -> simd_half8](/documentation/simd/min(_:_:)-7vhsf)
- [func min(simd_half8, Float16) -> simd_half8](/documentation/simd/min(_:_:)-80p4s)
- [func min(simd_half3, Float16) -> simd_half3](/documentation/simd/min(_:_:)-qbr4)
- [func min(simd_half3, simd_half3) -> simd_half3](/documentation/simd/min(_:_:)-tj43)
- [func rint(simd_half4) -> simd_half4](/documentation/simd/rint(_:)-16itt)
- [func rint(simd_half16) -> simd_half16](/documentation/simd/rint(_:)-2g2hq)
- [func rint(simd_half32) -> simd_half32](/documentation/simd/rint(_:)-3p367)
- [func rint(simd_half3) -> simd_half3](/documentation/simd/rint(_:)-91msl)
- [func rint(simd_half2) -> simd_half2](/documentation/simd/rint(_:)-9zf0h)
- [func rint(simd_half8) -> simd_half8](/documentation/simd/rint(_:)-ryn3)
- [func simd_act(simd_quath, simd_half3) -> simd_half3](/documentation/simd/simd_act(_:_:)-17i5z)
- [func simd_add(simd_quath, simd_quath) -> simd_quath](/documentation/simd/simd_add(_:_:)-7ul9y)
- [func simd_angle(simd_quath) -> Float16](/documentation/simd/simd_angle(_:)-zylp)
- [func simd_axis(simd_quath) -> simd_half3](/documentation/simd/simd_axis(_:)-56smw)
- [func simd_bezier(simd_quath, simd_quath, simd_quath, simd_quath, Float16) -> simd_quath](/documentation/simd/simd_bezier(_:_:_:_:_:)-2cl6p)
- [func simd_clamp(simd_half16, simd_half16, simd_half16) -> simd_half16](/documentation/simd/simd_clamp(_:_:_:)-7ck0a)
- [func simd_conjugate(simd_quath) -> simd_quath](/documentation/simd/simd_conjugate(_:)-989np)
- [func simd_dot(simd_quath, simd_quath) -> Float16](/documentation/simd/simd_dot(_:_:)-2dt0z)
- [func simd_equal(simd_int3, simd_int3) -> simd_bool](/documentation/simd/simd_equal(_:_:)-29zmw)
- [func simd_imag(simd_quath) -> simd_half3](/documentation/simd/simd_imag(_:)-2c8in)
- [func simd_inverse(simd_quath) -> simd_quath](/documentation/simd/simd_inverse(_:)-3cumm)
- [func simd_length(simd_quath) -> Float16](/documentation/simd/simd_length(_:)-52pax)
- [func simd_matrix3x3(simd_quath) -> simd_half3x3](/documentation/simd/simd_matrix3x3(_:)-60esl)
- [func simd_matrix4x4(simd_quath) -> simd_half4x4](/documentation/simd/simd_matrix4x4(_:)-20inb)
- [func simd_mul(simd_quath, Float16) -> simd_quath](/documentation/simd/simd_mul(_:_:)-2u2df)
- [func simd_mul(Float16, simd_quath) -> simd_quath](/documentation/simd/simd_mul(_:_:)-428fx)
- [func simd_mul(simd_quath, simd_quath) -> simd_quath](/documentation/simd/simd_mul(_:_:)-765ay)
- [func simd_negate(simd_quath) -> simd_quath](/documentation/simd/simd_negate(_:)-3yw6m)
- [func simd_normalize(simd_quath) -> simd_quath](/documentation/simd/simd_normalize(_:)-ubut)
- [func simd_quaternion(simd_half3x3) -> simd_quath](/documentation/simd/simd_quaternion(_:)-2er3f)
- [func simd_quaternion(simd_half4) -> simd_quath](/documentation/simd/simd_quaternion(_:)-4565s)
- [func simd_quaternion(UnsafePointer<Float16>!) -> simd_quath](/documentation/simd/simd_quaternion(_:)-8kjw1)
- [func simd_quaternion(simd_half4x4) -> simd_quath](/documentation/simd/simd_quaternion(_:)-9c4np)
- [func simd_quaternion(simd_half3, simd_half3) -> simd_quath](/documentation/simd/simd_quaternion(_:_:)-59cuw)
- [func simd_quaternion(Float16, simd_half3) -> simd_quath](/documentation/simd/simd_quaternion(_:_:)-6a6gg)
- [func simd_quaternion(Float16, Float16, Float16, Float16) -> simd_quath](/documentation/simd/simd_quaternion(_:_:_:_:)-9u5ci)
- [func simd_real(simd_quath) -> Float16](/documentation/simd/simd_real(_:)-75wwb)
- [func simd_reduce_max(simd_int3) -> Int32](/documentation/simd/simd_reduce_max(_:)-4hctl)
- [func simd_slerp(simd_quath, simd_quath, Float16) -> simd_quath](/documentation/simd/simd_slerp(_:_:_:)-7vayy)
- [func simd_slerp_longest(simd_quath, simd_quath, Float16) -> simd_quath](/documentation/simd/simd_slerp_longest(_:_:_:)-816ko)
- [func simd_spline(simd_quath, simd_quath, simd_quath, simd_quath, Float16) -> simd_quath](/documentation/simd/simd_spline(_:_:_:_:_:)-4ojmq)
- [func simd_sub(simd_quath, simd_quath) -> simd_quath](/documentation/simd/simd_sub(_:_:)-47kxs)
- [func sqrt(simd_half3) -> simd_half3](/documentation/simd/sqrt(_:)-201lt)
- [func sqrt(simd_half16) -> simd_half16](/documentation/simd/sqrt(_:)-3tk46)
- [func sqrt(simd_half2) -> simd_half2](/documentation/simd/sqrt(_:)-5rag4)
- [func sqrt(simd_half4) -> simd_half4](/documentation/simd/sqrt(_:)-605ao)
- [func sqrt(simd_half8) -> simd_half8](/documentation/simd/sqrt(_:)-62r7j)
- [func sqrt(simd_half32) -> simd_half32](/documentation/simd/sqrt(_:)-85jg8)
- [func trunc(simd_half4) -> simd_half4](/documentation/simd/trunc(_:)-1ndoy)
- [func trunc(simd_half8) -> simd_half8](/documentation/simd/trunc(_:)-3i567)
- [func trunc(simd_half16) -> simd_half16](/documentation/simd/trunc(_:)-42bu2)
- [func trunc(simd_half3) -> simd_half3](/documentation/simd/trunc(_:)-6l2mm)
- [func trunc(simd_half32) -> simd_half32](/documentation/simd/trunc(_:)-8e59l)
- [func trunc(simd_half2) -> simd_half2](/documentation/simd/trunc(_:)-l3lk)

## Type Aliases

- [matrix_half2x2](/documentation/simd/matrix_half2x2)
- [matrix_half2x3](/documentation/simd/matrix_half2x3)
- [matrix_half2x4](/documentation/simd/matrix_half2x4)
- [matrix_half3x2](/documentation/simd/matrix_half3x2)
- [matrix_half3x3](/documentation/simd/matrix_half3x3)
- [matrix_half3x4](/documentation/simd/matrix_half3x4)
- [matrix_half4x2](/documentation/simd/matrix_half4x2)
- [matrix_half4x3](/documentation/simd/matrix_half4x3)
- [matrix_half4x4](/documentation/simd/matrix_half4x4)
- [simd_bool](/documentation/simd/simd_bool)
- [simd_char1](/documentation/simd/simd_char1)
- [simd_char16](/documentation/simd/simd_char16)

### Functions to Create Sixteen-Element Vectors From Other Vectors

- [func simd_make_char16(simd_char2) -> simd_char16](/documentation/simd/simd_make_char16(_:)-5aqmo)
- [func simd_make_char16(simd_char3) -> simd_char16](/documentation/simd/simd_make_char16(_:)-5e63t)
- [func simd_make_char16(simd_char4) -> simd_char16](/documentation/simd/simd_make_char16(_:)-54urm)
- [func simd_make_char16(simd_char8) -> simd_char16](/documentation/simd/simd_make_char16(_:)-4pte6)
- [func simd_make_char16(simd_char16) -> simd_char16](/documentation/simd/simd_make_char16(_:)-516bc)
- [func simd_make_char16(simd_char32) -> simd_char16](/documentation/simd/simd_make_char16(_:)-tfq4)
- [func simd_make_char16(simd_char64) -> simd_char16](/documentation/simd/simd_make_char16(_:)-2j94t)
- [func simd_make_char16(simd_char8, simd_char8) -> simd_char16](/documentation/simd/simd_make_char16(_:_:))
- [func simd_make_char16_undef(simd_char2) -> simd_char16](/documentation/simd/simd_make_char16_undef(_:)-5kb1b)
- [func simd_make_char16_undef(simd_char3) -> simd_char16](/documentation/simd/simd_make_char16_undef(_:)-5gvk6)
- [func simd_make_char16_undef(simd_char4) -> simd_char16](/documentation/simd/simd_make_char16_undef(_:)-5ddf1)
- [func simd_make_char16_undef(simd_char8) -> simd_char16](/documentation/simd/simd_make_char16_undef(_:)-4yci9)

### Functions to Create Sixteen-Element Vectors From Scalar Values

- [func simd_make_char16(CChar) -> simd_char16](/documentation/simd/simd_make_char16(_:)-9skzf)
- [func simd_make_char16_undef(CChar) -> simd_char16](/documentation/simd/simd_make_char16_undef(_:)-9uhre)

### Common Functions

- [func simd_abs(simd_char16) -> simd_char16](/documentation/simd/simd_abs(_:)-475ng)
- [func simd_clamp(simd_char16, simd_char16, simd_char16) -> simd_char16](/documentation/simd/simd_clamp(_:_:_:)-509lj)
- [func simd_equal(simd_char16, simd_char16) -> simd_bool](/documentation/simd/simd_equal(_:_:)-19z1a)

### Reduce Functions

- [func simd_reduce_min(simd_char16) -> CChar](/documentation/simd/simd_reduce_min(_:)-3crdj)
- [func simd_reduce_max(simd_char16) -> CChar](/documentation/simd/simd_reduce_max(_:)-8idj9)
- [func simd_reduce_add(simd_char16) -> CChar](/documentation/simd/simd_reduce_add(_:)-7mtzs)

### Extrema Functions

- [func simd_min(simd_char16, simd_char16) -> simd_char16](/documentation/simd/simd_min(_:_:)-3t06b)
- [func simd_max(simd_char16, simd_char16) -> simd_char16](/documentation/simd/simd_max(_:_:)-2pboz)

### Logic and Bitwise Functions

- [func simd_any(simd_char16) -> simd_bool](/documentation/simd/simd_any(_:)-92tuy)
- [func simd_all(simd_char16) -> simd_bool](/documentation/simd/simd_all(_:)-iajg)
- [func simd_bitselect(simd_char16, simd_char16, simd_char16) -> simd_char16](/documentation/simd/simd_bitselect(_:_:_:)-5uq86)

### Alternative Type Alias

- [vector_char16](/documentation/simd/vector_char16)
- [simd_char2](/documentation/simd/simd_char2)

### Functions to Create Two-Element Vectors From Other Vectors

- [func simd_make_char2(simd_char2) -> simd_char2](/documentation/simd/simd_make_char2(_:)-3yugv)
- [func simd_make_char2(simd_char3) -> simd_char2](/documentation/simd/simd_make_char2(_:)-3vcc6)
- [func simd_make_char2(simd_char4) -> simd_char2](/documentation/simd/simd_make_char2(_:)-3dx8l)
- [func simd_make_char2(simd_char8) -> simd_char2](/documentation/simd/simd_make_char2(_:)-2yw9d)
- [func simd_make_char2(simd_char16) -> simd_char2](/documentation/simd/simd_make_char2(_:)-2o33b)
- [func simd_make_char2(simd_char32) -> simd_char2](/documentation/simd/simd_make_char2(_:)-6vtvj)
- [func simd_make_char2(simd_char64) -> simd_char2](/documentation/simd/simd_make_char2(_:)-7bvq1)

### Functions to Create Two-Element Vectors From Scalar Values

- [func simd_make_char2(CChar) -> simd_char2](/documentation/simd/simd_make_char2(_:)-97vf3)
- [func simd_make_char2(CChar, CChar) -> simd_char2](/documentation/simd/simd_make_char2(_:_:))
- [func simd_make_char2_undef(CChar) -> simd_char2](/documentation/simd/simd_make_char2_undef(_:))

### Common Functions

- [func simd_abs(simd_char2) -> simd_char2](/documentation/simd/simd_abs(_:)-88i9q)
- [func simd_clamp(simd_char2, simd_char2, simd_char2) -> simd_char2](/documentation/simd/simd_clamp(_:_:_:)-5vl7)
- [func simd_equal(simd_char2, simd_char2) -> simd_bool](/documentation/simd/simd_equal(_:_:)-3n6nt)

### Reduce Functions

- [func simd_reduce_min(simd_char2) -> CChar](/documentation/simd/simd_reduce_min(_:)-49h4g)
- [func simd_reduce_max(simd_char2) -> CChar](/documentation/simd/simd_reduce_max(_:)-4krqw)
- [func simd_reduce_add(simd_char2) -> CChar](/documentation/simd/simd_reduce_add(_:)-2qb2i)

### Extrema Functions

- [func simd_min(simd_char2, simd_char2) -> simd_char2](/documentation/simd/simd_min(_:_:)-5di41)
- [func simd_max(simd_char2, simd_char2) -> simd_char2](/documentation/simd/simd_max(_:_:)-6op8l)

### Logic and Bitwise Functions

- [func simd_any(simd_char2) -> simd_bool](/documentation/simd/simd_any(_:)-64och)
- [func simd_all(simd_char2) -> simd_bool](/documentation/simd/simd_all(_:)-1d0nz)
- [func simd_bitselect(simd_char2, simd_char2, simd_char2) -> simd_char2](/documentation/simd/simd_bitselect(_:_:_:)-2nrwa)

### Alternative Type Alias

- [vector_char2](/documentation/simd/vector_char2)
- [simd_char3](/documentation/simd/simd_char3)

### Functions to Create Three-Element Vectors From Other Vectors

- [func simd_make_char3(simd_char2) -> simd_char3](/documentation/simd/simd_make_char3(_:)-7hn14)
- [func simd_make_char3(simd_char3) -> simd_char3](/documentation/simd/simd_make_char3(_:)-7l2ch)
- [func simd_make_char3(simd_char4) -> simd_char3](/documentation/simd/simd_make_char3(_:)-81dqq)
- [func simd_make_char3(simd_char8) -> simd_char3](/documentation/simd/simd_make_char3(_:)-6wpri)
- [func simd_make_char3(simd_char16) -> simd_char3](/documentation/simd/simd_make_char3(_:)-7kwml)
- [func simd_make_char3(simd_char32) -> simd_char3](/documentation/simd/simd_make_char3(_:)-5pt8h)
- [func simd_make_char3(simd_char64) -> simd_char3](/documentation/simd/simd_make_char3(_:)-2kabv)
- [func simd_make_char3_undef(simd_char2) -> simd_char3](/documentation/simd/simd_make_char3_undef(_:)-3pbpb)

### Functions to Create Three-Element Vectors From Scalar Values

- [func simd_make_char3(CChar) -> simd_char3](/documentation/simd/simd_make_char3(_:)-9zbpd)
- [func simd_make_char3(CChar, CChar, CChar) -> simd_char3](/documentation/simd/simd_make_char3(_:_:_:))
- [func simd_make_char3_undef(CChar) -> simd_char3](/documentation/simd/simd_make_char3_undef(_:)-866v6)

### Functions to Create Three-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_char3(CChar, simd_char2) -> simd_char3](/documentation/simd/simd_make_char3(_:_:)-5c5ds)
- [func simd_make_char3(simd_char2, CChar) -> simd_char3](/documentation/simd/simd_make_char3(_:_:)-9qv2s)

### Common Functions

- [func simd_abs(simd_char3) -> simd_char3](/documentation/simd/simd_abs(_:)-8d1l3)
- [func simd_clamp(simd_char3, simd_char3, simd_char3) -> simd_char3](/documentation/simd/simd_clamp(_:_:_:)-5xm9q)
- [func simd_equal(simd_char3, simd_char3) -> simd_bool](/documentation/simd/simd_equal(_:_:)-ymae)

### Reduce Functions

- [func simd_reduce_min(simd_char3) -> CChar](/documentation/simd/simd_reduce_min(_:)-461hl)
- [func simd_reduce_max(simd_char3) -> CChar](/documentation/simd/simd_reduce_max(_:)-4h9pt)
- [func simd_reduce_add(simd_char3) -> CChar](/documentation/simd/simd_reduce_add(_:)-2uwqb)

### Extrema Functions

- [func simd_min(simd_char3, simd_char3) -> simd_char3](/documentation/simd/simd_min(_:_:)-93d9y)
- [func simd_max(simd_char3, simd_char3) -> simd_char3](/documentation/simd/simd_max(_:_:)-5fzu7)

### Logic and Bitwise Functions

- [func simd_any(simd_char3) -> simd_bool](/documentation/simd/simd_any(_:)-69a7c)
- [func simd_all(simd_char3) -> simd_bool](/documentation/simd/simd_all(_:)-1aml2)
- [func simd_bitselect(simd_char3, simd_char3, simd_char3) -> simd_char3](/documentation/simd/simd_bitselect(_:_:_:)-4kbjh)

### Alternative Type Alias

- [vector_char3](/documentation/simd/vector_char3)
- [simd_char32](/documentation/simd/simd_char32)

### Functions to Create Thirty Two-Element Vectors From Other Vectors

- [func simd_make_char32(simd_char2) -> simd_char32](/documentation/simd/simd_make_char32(_:)-384hl)
- [func simd_make_char32(simd_char3) -> simd_char32](/documentation/simd/simd_make_char32(_:)-3bm80)
- [func simd_make_char32(simd_char4) -> simd_char32](/documentation/simd/simd_make_char32(_:)-2n9wz)
- [func simd_make_char32(simd_char8) -> simd_char32](/documentation/simd/simd_make_char32(_:)-2ag5j)
- [func simd_make_char32(simd_char16) -> simd_char32](/documentation/simd/simd_make_char32(_:)-3g5k3)
- [func simd_make_char32(simd_char32) -> simd_char32](/documentation/simd/simd_make_char32(_:)-8fqzf)
- [func simd_make_char32(simd_char64) -> simd_char32](/documentation/simd/simd_make_char32(_:)-6kn8l)
- [func simd_make_char32(simd_char16, simd_char16) -> simd_char32](/documentation/simd/simd_make_char32(_:_:))
- [func simd_make_char32_undef(simd_char2) -> simd_char32](/documentation/simd/simd_make_char32_undef(_:)-7t6qn)
- [func simd_make_char32_undef(simd_char3) -> simd_char32](/documentation/simd/simd_make_char32_undef(_:)-7poo6)
- [func simd_make_char32_undef(simd_char4) -> simd_char32](/documentation/simd/simd_make_char32_undef(_:)-7z0ct)
- [func simd_make_char32_undef(simd_char8) -> simd_char32](/documentation/simd/simd_make_char32_undef(_:)-6t8l5)
- [func simd_make_char32_undef(simd_char16) -> simd_char32](/documentation/simd/simd_make_char32_undef(_:)-3vq4m)

### Functions to Create Thirty Two-Element Vectors From Scalar Values

- [func simd_make_char32(CChar) -> simd_char32](/documentation/simd/simd_make_char32(_:)-20u7n)
- [func simd_make_char32_undef(CChar) -> simd_char32](/documentation/simd/simd_make_char32_undef(_:)-9nqa9)

### Common Functions

- [func simd_abs(simd_char32) -> simd_char32](/documentation/simd/simd_abs(_:)-2ca9r)
- [func simd_clamp(simd_char32, simd_char32, simd_char32) -> simd_char32](/documentation/simd/simd_clamp(_:_:_:)-2eiom)
- [func simd_equal(simd_char32, simd_char32) -> simd_bool](/documentation/simd/simd_equal(_:_:)-2iweh)

### Reduce Functions

- [func simd_reduce_min(simd_char32) -> CChar](/documentation/simd/simd_reduce_min(_:)-2au68)
- [func simd_reduce_max(simd_char32) -> CChar](/documentation/simd/simd_reduce_max(_:)-9j748)
- [func simd_reduce_add(simd_char32) -> CChar](/documentation/simd/simd_reduce_add(_:)-1uzk7)

### Extrema Functions

- [func simd_min(simd_char32, simd_char32) -> simd_char32](/documentation/simd/simd_min(_:_:)-2isjs)
- [func simd_max(simd_char32, simd_char32) -> simd_char32](/documentation/simd/simd_max(_:_:)-9ec8n)

### Logic and Bitwise Functions

- [func simd_any(simd_char32) -> simd_bool](/documentation/simd/simd_any(_:)-3az4l)
- [func simd_all(simd_char32) -> simd_bool](/documentation/simd/simd_all(_:)-1k7jn)
- [func simd_bitselect(simd_char32, simd_char32, simd_char32) -> simd_char32](/documentation/simd/simd_bitselect(_:_:_:)-2da13)

### Alternative Type Alias

- [vector_char32](/documentation/simd/vector_char32)
- [simd_char4](/documentation/simd/simd_char4)

### Functions to Create Four-Element Vectors From Other Vectors

- [func simd_make_char4(simd_char2) -> simd_char4](/documentation/simd/simd_make_char4(_:)-mdlt)
- [func simd_make_char4(simd_char3) -> simd_char4](/documentation/simd/simd_make_char4(_:)-k1u0)
- [func simd_make_char4(simd_char4) -> simd_char4](/documentation/simd/simd_make_char4(_:)-gjz7)
- [func simd_make_char4(simd_char8) -> simd_char4](/documentation/simd/simd_make_char4(_:)-1mbtb)
- [func simd_make_char4(simd_char16) -> simd_char4](/documentation/simd/simd_make_char4(_:)-4y0kh)
- [func simd_make_char4(simd_char32) -> simd_char4](/documentation/simd/simd_make_char4(_:)-3tnz9)
- [func simd_make_char4(simd_char64) -> simd_char4](/documentation/simd/simd_make_char4(_:)-69u9q)
- [func simd_make_char4(simd_char2, simd_char2) -> simd_char4](/documentation/simd/simd_make_char4(_:_:)-3vf4l)
- [func simd_make_char4_undef(simd_char2) -> simd_char4](/documentation/simd/simd_make_char4_undef(_:)-6zlek)
- [func simd_make_char4_undef(simd_char3) -> simd_char4](/documentation/simd/simd_make_char4_undef(_:)-73111)

### Functions to Create Four-Element Vectors From Scalar Values

- [func simd_make_char4(CChar) -> simd_char4](/documentation/simd/simd_make_char4(_:)-8kfe3)
- [func simd_make_char4(CChar, CChar, CChar, CChar) -> simd_char4](/documentation/simd/simd_make_char4(_:_:_:_:))
- [func simd_make_char4_undef(CChar) -> simd_char4](/documentation/simd/simd_make_char4_undef(_:)-99pql)

### Functions to Create Four-Element Vectors From Combinations of Vectors and Scalar Value

- [func simd_make_char4(simd_char2, CChar, CChar) -> simd_char4](/documentation/simd/simd_make_char4(_:_:_:)-82ftd)
- [func simd_make_char4(simd_char3, CChar) -> simd_char4](/documentation/simd/simd_make_char4(_:_:)-226qq)
- [func simd_make_char4(CChar, CChar, simd_char2) -> simd_char4](/documentation/simd/simd_make_char4(_:_:_:)-9mb46)
- [func simd_make_char4(CChar, simd_char2, CChar) -> simd_char4](/documentation/simd/simd_make_char4(_:_:_:)-94kun)
- [func simd_make_char4(CChar, simd_char3) -> simd_char4](/documentation/simd/simd_make_char4(_:_:)-76rpp)

### Common Functions

- [func simd_abs(simd_char4) -> simd_char4](/documentation/simd/simd_abs(_:)-81ics)
- [func simd_clamp(simd_char4, simd_char4, simd_char4) -> simd_char4](/documentation/simd/simd_clamp(_:_:_:)-1lm34)
- [func simd_equal(simd_char4, simd_char4) -> simd_bool](/documentation/simd/simd_equal(_:_:)-4x3vb)

### Reduce Functions

- [func simd_reduce_min(simd_char4) -> CChar](/documentation/simd/simd_reduce_min(_:)-4ue96)
- [func simd_reduce_max(simd_char4) -> CChar](/documentation/simd/simd_reduce_max(_:)-4ql9m)
- [func simd_reduce_add(simd_char4) -> CChar](/documentation/simd/simd_reduce_add(_:)-2yeuw)

### Extrema Functions

- [func simd_min(simd_char4, simd_char4) -> simd_char4](/documentation/simd/simd_min(_:_:)-2mbto)
- [func simd_max(simd_char4, simd_char4) -> simd_char4](/documentation/simd/simd_max(_:_:)-7qdak)

### Logic and Bitwise Functions

- [func simd_any(simd_char4) -> simd_bool](/documentation/simd/simd_any(_:)-6cs8j)
- [func simd_all(simd_char4) -> simd_bool](/documentation/simd/simd_all(_:)-1jxv1)
- [func simd_bitselect(simd_char4, simd_char4, simd_char4) -> simd_char4](/documentation/simd/simd_bitselect(_:_:_:)-4mvfw)

### Alternative Type Alias

- [vector_char4](/documentation/simd/vector_char4)
- [simd_char64](/documentation/simd/simd_char64)

### Functions to Create Sixty Four-Element Vectors From Other Vectors

- [func simd_make_char64(simd_char2) -> simd_char64](/documentation/simd/simd_make_char64(_:)-mo7n)
- [func simd_make_char64(simd_char3) -> simd_char64](/documentation/simd/simd_make_char64(_:)-kchm)
- [func simd_make_char64(simd_char4) -> simd_char64](/documentation/simd/simd_make_char64(_:)-18pa1)
- [func simd_make_char64(simd_char8) -> simd_char64](/documentation/simd/simd_make_char64(_:)-1mmet)
- [func simd_make_char64(simd_char16) -> simd_char64](/documentation/simd/simd_make_char64(_:)-kijk)
- [func simd_make_char64(simd_char32) -> simd_char64](/documentation/simd/simd_make_char64(_:)-747mj)
- [func simd_make_char64(simd_char64) -> simd_char64](/documentation/simd/simd_make_char64(_:)-v4n8)
- [func simd_make_char64(simd_char32, simd_char32) -> simd_char64](/documentation/simd/simd_make_char64(_:_:))
- [func simd_make_char64_undef(simd_char2) -> simd_char64](/documentation/simd/simd_make_char64_undef(_:)-9r2mn)
- [func simd_make_char64_undef(simd_char3) -> simd_char64](/documentation/simd/simd_make_char64_undef(_:)-9ui3q)
- [func simd_make_char64_undef(simd_char4) -> simd_char64](/documentation/simd/simd_make_char64_undef(_:)-cbyu)
- [func simd_make_char64_undef(simd_char8) -> simd_char64](/documentation/simd/simd_make_char64_undef(_:)-p5ey)
- [func simd_make_char64_undef(simd_char16) -> simd_char64](/documentation/simd/simd_make_char64_undef(_:)-ax60)
- [func simd_make_char64_undef(simd_char32) -> simd_char64](/documentation/simd/simd_make_char64_undef(_:)-5axfx)

### Functions to Create Sixty Four-Element Vectors From Scalar Values

- [func simd_make_char64(CChar) -> simd_char64](/documentation/simd/simd_make_char64(_:)-bvt7)
- [func simd_make_char64_undef(CChar) -> simd_char64](/documentation/simd/simd_make_char64_undef(_:)-2ljie)

### Common Functions

- [func simd_abs(simd_char64) -> simd_char64](/documentation/simd/simd_abs(_:)-1p85t)
- [func simd_clamp(simd_char64, simd_char64, simd_char64) -> simd_char64](/documentation/simd/simd_clamp(_:_:_:)-6jkxk)
- [func simd_equal(simd_char64, simd_char64) -> simd_bool](/documentation/simd/simd_equal(_:_:)-8ghe2)

### Reduce Functions

- [func simd_reduce_min(simd_char64) -> CChar](/documentation/simd/simd_reduce_min(_:)-jzf5)
- [func simd_reduce_max(simd_char64) -> CChar](/documentation/simd/simd_reduce_max(_:)-mshf)
- [func simd_reduce_add(simd_char64) -> CChar](/documentation/simd/simd_reduce_add(_:)-92wpk)

### Logic and Bitwise Functions

- [func simd_any(simd_char64) -> simd_bool](/documentation/simd/simd_any(_:)-jb9j)
- [func simd_all(simd_char64) -> simd_bool](/documentation/simd/simd_all(_:)-2mapx)
- [func simd_bitselect(simd_char64, simd_char64, simd_char64) -> simd_char64](/documentation/simd/simd_bitselect(_:_:_:)-2qkxa)

### Extrema Functions

- [func simd_min(simd_char64, simd_char64) -> simd_char64](/documentation/simd/simd_min(_:_:)-66xtr)
- [func simd_max(simd_char64, simd_char64) -> simd_char64](/documentation/simd/simd_max(_:_:)-4dt8v)
- [simd_char8](/documentation/simd/simd_char8)

### Functions to Create Eight-Element Vectors From Other Vectors

- [func simd_make_char8(simd_char2) -> simd_char8](/documentation/simd/simd_make_char8(_:)-3e9h4)
- [func simd_make_char8(simd_char3) -> simd_char8](/documentation/simd/simd_make_char8(_:)-39q4x)
- [func simd_make_char8(simd_char4) -> simd_char8](/documentation/simd/simd_make_char8(_:)-3y2oy)
- [func simd_make_char8(simd_char8) -> simd_char8](/documentation/simd/simd_make_char8(_:)-4c00u)
- [func simd_make_char8(simd_char16) -> simd_char8](/documentation/simd/simd_make_char8(_:)-497r7)
- [func simd_make_char8(simd_char32) -> simd_char8](/documentation/simd/simd_make_char8(_:)-tbln)
- [func simd_make_char8(simd_char64) -> simd_char8](/documentation/simd/simd_make_char8(_:)-4m1k5)
- [func simd_make_char8(simd_char4, simd_char4) -> simd_char8](/documentation/simd/simd_make_char8(_:_:))
- [func simd_make_char8_undef(simd_char2) -> simd_char8](/documentation/simd/simd_make_char8_undef(_:)-4zw8k)
- [func simd_make_char8_undef(simd_char3) -> simd_char8](/documentation/simd/simd_make_char8_undef(_:)-53bml)
- [func simd_make_char8_undef(simd_char4) -> simd_char8](/documentation/simd/simd_make_char8_undef(_:)-5kqwe)

### Functions to Create Eight-Element Vectors From Scalar Values

- [func simd_make_char8(CChar) -> simd_char8](/documentation/simd/simd_make_char8(_:)-2wraz)
- [func simd_make_char8_undef(CChar) -> simd_char8](/documentation/simd/simd_make_char8_undef(_:)-830qy)

### Common Functions

- [func simd_abs(simd_char8) -> simd_char8](/documentation/simd/simd_abs(_:)-7oowg)
- [func simd_clamp(simd_char8, simd_char8, simd_char8) -> simd_char8](/documentation/simd/simd_clamp(_:_:_:)-6t9ze)
- [func simd_equal(simd_char8, simd_char8) -> simd_bool](/documentation/simd/simd_equal(_:_:)-7xed4)

### Reduce Functions

- [func simd_reduce_min(simd_char8) -> CChar](/documentation/simd/simd_reduce_min(_:)-3omfa)
- [func simd_reduce_max(simd_char8) -> CChar](/documentation/simd/simd_reduce_max(_:)-55mb2)
- [func simd_reduce_add(simd_char8) -> CChar](/documentation/simd/simd_reduce_add(_:)-3b8ak)

### Extrema Functions

- [func simd_min(simd_char8, simd_char8) -> simd_char8](/documentation/simd/simd_min(_:_:)-66w6r)
- [func simd_max(simd_char8, simd_char8) -> simd_char8](/documentation/simd/simd_max(_:_:)-1zyht)

### Logic and Bitwise Functions

- [func simd_any(simd_char8) -> simd_bool](/documentation/simd/simd_any(_:)-6plnr)
- [func simd_all(simd_char8) -> simd_bool](/documentation/simd/simd_all(_:)-1yyw9)
- [func simd_bitselect(simd_char8, simd_char8, simd_char8) -> simd_char8](/documentation/simd/simd_bitselect(_:_:_:)-5bgc3)

### Alternative Type Alias

- [vector_char8](/documentation/simd/vector_char8)
- [simd_double1](/documentation/simd/simd_double1)

### Common Functions

- [func step(Double, edge: Double) -> Double](/documentation/simd/step(_:edge:)-382a5)
- [func simd_step(Double, Double) -> Double](/documentation/simd/simd_step(_:_:)-8mpre)
- [func simd_clamp(Double, Double, Double) -> Double](/documentation/simd/simd_clamp(_:_:_:)-1ktlk)
- [func simd_fract(Double) -> Double](/documentation/simd/simd_fract(_:)-1wsn4)
- [func sign(Double) -> Double](/documentation/simd/sign(_:)-iwmp)
- [func simd_sign(Double) -> Double](/documentation/simd/simd_sign(_:)-937ee)

### Interpolation Functions

- [func simd_smoothstep(Double, Double, Double) -> Double](/documentation/simd/simd_smoothstep(_:_:_:)-5839l)
- [func simd_mix(Double, Double, Double) -> Double](/documentation/simd/simd_mix(_:_:_:)-6aqwp)

### Extrema Functions

- [func min(SIMD4<Double>, Double) -> SIMD4<Double>](/documentation/simd/min(_:_:)-7rmn)
- [func simd_min(Double, Double) -> Double](/documentation/simd/simd_min(_:_:)-x4en)
- [func max(SIMD2<Double>, Double) -> SIMD2<Double>](/documentation/simd/max(_:_:)-3puhr)
- [func simd_max(Double, Double) -> Double](/documentation/simd/simd_max(_:_:)-9ibgs)

### Math Functions

- [func simd_muladd(Double, Double, Double) -> Double](/documentation/simd/simd_muladd(_:_:_:)-9hwx1)

### Reciprocal and Reciprocal Square Root Functions

- [func recip(Double) -> Double](/documentation/simd/recip(_:)-8b6ef)
- [func simd_recip(Double) -> Double](/documentation/simd/simd_recip(_:)-7ylz3)
- [func simd_fast_recip(Double) -> Double](/documentation/simd/simd_fast_recip(_:)-1h1e)
- [func simd_precise_recip(Double) -> Double](/documentation/simd/simd_precise_recip(_:)-6qb0h)
- [func rsqrt(Double) -> Double](/documentation/simd/rsqrt(_:)-7h0u6)
- [func simd_rsqrt(Double) -> Double](/documentation/simd/simd_rsqrt(_:)-4ygr4)
- [func simd_fast_rsqrt(Double) -> Double](/documentation/simd/simd_fast_rsqrt(_:)-43tvc)
- [func simd_precise_rsqrt(Double) -> Double](/documentation/simd/simd_precise_rsqrt(_:)-5fl9s)
- [simd_double2](/documentation/simd/simd_double2)

### Functions to Create Two-Element Vectors From Other Vectors

- [func simd_make_double2(simd_double2) -> simd_double2](/documentation/simd/simd_make_double2(_:)-3qby3)
- [func simd_make_double2(simd_double3) -> simd_double2](/documentation/simd/simd_make_double2(_:)-3tt38)
- [func simd_make_double2(simd_double4) -> simd_double2](/documentation/simd/simd_make_double2(_:)-3hpld)
- [func simd_make_double2(simd_double8) -> simd_double2](/documentation/simd/simd_make_double2(_:)-4o3ot)
- [func simd_make_double2(Double, Double) -> simd_double2](/documentation/simd/simd_make_double2(_:_:))

### Functions to Create Two-Element Vectors From Scalar Values

- [func simd_make_double2(Double) -> simd_double2](/documentation/simd/simd_make_double2(_:)-r6xz)
- [func simd_make_double2_undef(Double) -> simd_double2](/documentation/simd/simd_make_double2_undef(_:))

### Common Functions

- [func simd_abs(simd_double2) -> simd_double2](/documentation/simd/simd_abs(_:)-8869e)
- [func abs(SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/abs(_:)-1p8t7)
- [func simd_clamp(simd_double2, simd_double2, simd_double2) -> simd_double2](/documentation/simd/simd_clamp(_:_:_:)-6puwa)
- [func clamp(SIMD2<Double>, min: Double, max: Double) -> SIMD2<Double>](/documentation/simd/clamp(_:min:max:)-7n2jv)
- [func clamp(SIMD2<Double>, min: SIMD2<Double>, max: SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/clamp(_:min:max:)-6d1s7)
- [func simd_equal(simd_double2, simd_double2) -> simd_bool](/documentation/simd/simd_equal(_:_:)-vmn4)
- [func simd_fract(simd_double2) -> simd_double2](/documentation/simd/simd_fract(_:)-42i3r)
- [func fract(SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/fract(_:)-2gjrn)
- [func simd_sign(simd_double2) -> simd_double2](/documentation/simd/simd_sign(_:)-6jlx9)
- [func sign(SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/sign(_:)-5fczz)
- [func step(SIMD2<Double>, edge: SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/step(_:edge:)-2qauk)
- [func simd_step(simd_double2, simd_double2) -> simd_double2](/documentation/simd/simd_step(_:_:)-8jlf2)

### Reduce Functions

- [func simd_reduce_add(simd_double2) -> Double](/documentation/simd/simd_reduce_add(_:)-2q09i)
- [func reduce_add(SIMD2<Double>) -> Double](/documentation/simd/reduce_add(_:)-8iwo6)
- [func simd_reduce_max(simd_double2) -> Double](/documentation/simd/simd_reduce_max(_:)-4kinw)
- [func reduce_max(SIMD2<Double>) -> Double](/documentation/simd/reduce_max(_:)-3rmpx)
- [func simd_reduce_min(simd_double2) -> Double](/documentation/simd/simd_reduce_min(_:)-49t1o)
- [func reduce_min(SIMD2<Double>) -> Double](/documentation/simd/reduce_min(_:)-6mev7)

### Interpolation Functions

- [func simd_smoothstep(simd_double2, simd_double2, simd_double2) -> simd_double2](/documentation/simd/simd_smoothstep(_:_:_:)-e0ov)
- [func smoothstep(SIMD2<Double>, edge0: SIMD2<Double>, edge1: SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/smoothstep(_:edge0:edge1:)-2wqo9)
- [func simd_mix(simd_double2, simd_double2, simd_double2) -> simd_double2](/documentation/simd/simd_mix(_:_:_:)-v083)
- [func mix(SIMD2<Double>, SIMD2<Double>, t: Double) -> SIMD2<Double>](/documentation/simd/mix(_:_:t:)-7bjg5)
- [func mix(SIMD2<Double>, SIMD2<Double>, t: SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/mix(_:_:t:)-3hfwb)

### Extrema Functions

- [func simd_max(simd_double2, simd_double2) -> simd_double2](/documentation/simd/simd_max(_:_:)-1sy2n)
- [func max(SIMD2<Double>, Double) -> SIMD2<Double>](/documentation/simd/max(_:_:)-3puhr)
- [func max(SIMD2<Double>, SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/max(_:_:)-8a5p5)
- [func fmax(SIMD2<Double>, SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/fmax(_:_:)-15te9)
- [func simd_min(simd_double2, simd_double2) -> simd_double2](/documentation/simd/simd_min(_:_:)-9mraz)
- [func min(SIMD2<Double>, Double) -> SIMD2<Double>](/documentation/simd/min(_:_:)-4sdw0)
- [func min(SIMD2<Double>, SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/min(_:_:)-9yz9x)
- [func fmin(SIMD2<Double>, SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/fmin(_:_:)-39mes)

### Reciprocal and Reciprocal Square Root Functions

- [func recip(SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/recip(_:)-43mv7)
- [func simd_recip(simd_double2) -> simd_double2](/documentation/simd/simd_recip(_:)-8nekc)
- [func simd_fast_recip(simd_double2) -> simd_double2](/documentation/simd/simd_fast_recip(_:)-lm0t)
- [func simd_precise_recip(simd_double2) -> simd_double2](/documentation/simd/simd_precise_recip(_:)-66n8k)
- [func simd_rsqrt(simd_double2) -> simd_double2](/documentation/simd/simd_rsqrt(_:)-ok9s)
- [func rsqrt(SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/rsqrt(_:)-2k5rh)
- [func simd_fast_rsqrt(simd_double2) -> simd_double2](/documentation/simd/simd_fast_rsqrt(_:)-84dca)
- [func simd_precise_rsqrt(simd_double2) -> simd_double2](/documentation/simd/simd_precise_rsqrt(_:)-wrke)

### Exponential and Logarithmic Functions

- [func exp(simd_double2) -> simd_double2](/documentation/simd/exp(_:)-9nxip)
- [func exp2(simd_double2) -> simd_double2](/documentation/simd/exp2(_:)-4y2ne)
- [func exp10(simd_double2) -> simd_double2](/documentation/simd/exp10(_:)-4tdos)
- [func expm1(simd_double2) -> simd_double2](/documentation/simd/expm1(_:)-9aitr)
- [func log(simd_double2) -> simd_double2](/documentation/simd/log(_:)-2ieba)
- [func log2(simd_double2) -> simd_double2](/documentation/simd/log2(_:)-779eu)
- [func log10(simd_double2) -> simd_double2](/documentation/simd/log10(_:)-337zw)
- [func log1p(simd_double2) -> simd_double2](/documentation/simd/log1p(_:)-40mka)

### Geometry Functions

- [func cross(SIMD2<Double>, SIMD2<Double>) -> SIMD3<Double>](/documentation/simd/cross(_:_:)-916aw)
- [func dot(SIMD2<Double>, SIMD2<Double>) -> Double](/documentation/simd/dot(_:_:)-6ayky)
- [func normalize(SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/normalize(_:)-5mqhk)
- [func project(SIMD2<Double>, SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/project(_:_:)-kai1)
- [func reflect(SIMD2<Double>, n: SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/reflect(_:n:)-3rhgb)
- [func refract(SIMD2<Double>, n: SIMD2<Double>, eta: Double) -> SIMD2<Double>](/documentation/simd/refract(_:n:eta:)-1ghae)

### Vector Norm Functions

- [func norm_one(SIMD2<Double>) -> Double](/documentation/simd/norm_one(_:)-2uh74)
- [func norm_inf(SIMD2<Double>) -> Double](/documentation/simd/norm_inf(_:)-s3p1)

### Length and Distance Functions

- [func length(SIMD2<Double>) -> Double](/documentation/simd/length(_:)-4gxdk)
- [func length_squared(SIMD2<Double>) -> Double](/documentation/simd/length_squared(_:)-8gxz9)
- [func distance(SIMD2<Double>, SIMD2<Double>) -> Double](/documentation/simd/distance(_:_:)-1mnxv)
- [func distance_squared(SIMD2<Double>, SIMD2<Double>) -> Double](/documentation/simd/distance_squared(_:_:)-56tah)

### Hyperbolic Functions

- [func acosh(simd_double2) -> simd_double2](/documentation/simd/acosh(_:)-edu)
- [func asinh(simd_double2) -> simd_double2](/documentation/simd/asinh(_:)-nxaa)
- [func atanh(simd_double2) -> simd_double2](/documentation/simd/atanh(_:)-5l8ss)
- [func cosh(simd_double2) -> simd_double2](/documentation/simd/cosh(_:)-303ot)
- [func sinh(simd_double2) -> simd_double2](/documentation/simd/sinh(_:)-5gx9h)
- [func tanh(simd_double2) -> simd_double2](/documentation/simd/tanh(_:)-739hq)

### Logic Functions

- [func simd_select(simd_double2, simd_double2, simd_long2) -> simd_double2](/documentation/simd/simd_select(_:_:_:)-7sz6k)
- [func simd_bitselect(simd_double2, simd_double2, simd_long2) -> simd_double2](/documentation/simd/simd_bitselect(_:_:_:)-3ys1a)

### Math Functions

- [func cbrt(simd_double2) -> simd_double2](/documentation/simd/cbrt(_:)-75bqn)
- [func ceil(SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/ceil(_:)-cu6z)
- [func erf(simd_double2) -> simd_double2](/documentation/simd/erf(_:)-7tfrz)
- [func erfc(simd_double2) -> simd_double2](/documentation/simd/erfc(_:)-8i2r6)
- [func floor(SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/floor(_:)-21h1y)
- [func fma(simd_double2, simd_double2, simd_double2) -> simd_double2](/documentation/simd/fma(_:_:_:)-4fxau)
- [func fmod(simd_double2, simd_double2) -> simd_double2](/documentation/simd/fmod(_:_:)-81hr1)
- [func hypot(simd_double2, simd_double2) -> simd_double2](/documentation/simd/hypot(_:_:)-9ecpz)
- [func lgamma(simd_double2) -> simd_double2](/documentation/simd/lgamma(_:)-697vf)
- [func nextafter(simd_double2, simd_double2) -> simd_double2](/documentation/simd/nextafter(_:_:)-6qeuz)
- [func pow(simd_double2, simd_double2) -> simd_double2](/documentation/simd/pow(_:_:)-2ov0n)
- [func remainder(simd_double2, simd_double2) -> simd_double2](/documentation/simd/remainder(_:_:)-1l80m)
- [func round(simd_double2) -> simd_double2](/documentation/simd/round(_:)-1ith)
- [func simd_muladd(simd_double2, simd_double2, simd_double2) -> simd_double2](/documentation/simd/simd_muladd(_:_:_:)-o9lv)
- [func tgamma(simd_double2) -> simd_double2](/documentation/simd/tgamma(_:)-3id8t)
- [func trunc(SIMD2<Double>) -> SIMD2<Double>](/documentation/simd/trunc(_:)-1xvcu)

### Trigonometric Functions

- [func acos(simd_double2) -> simd_double2](/documentation/simd/acos(_:)-1hgv5)
- [func asin(simd_double2) -> simd_double2](/documentation/simd/asin(_:)-72orw)
- [func atan(simd_double2) -> simd_double2](/documentation/simd/atan(_:)-9onaa)
- [func atan2(simd_double2, simd_double2) -> simd_double2](/documentation/simd/atan2(_:_:)-6ogu4)
- [func cos(simd_double2) -> simd_double2](/documentation/simd/cos(_:)-3p9ym)
- [func cospi(simd_double2) -> simd_double2](/documentation/simd/cospi(_:)-57353)
- [func sin(simd_double2) -> simd_double2](/documentation/simd/sin(_:)-3p88b)
- [func sinpi(simd_double2) -> simd_double2](/documentation/simd/sinpi(_:)-4lgpo)
- [func sincos(simd_double2) -> (sin: simd_double2, cos: simd_double2)](/documentation/simd/sincos(_:)-9pa2l)
- [func sincospi(simd_double2) -> (sin: simd_double2, cos: simd_double2)](/documentation/simd/sincospi(_:)-3fwbj)
- [func tan(simd_double2) -> simd_double2](/documentation/simd/tan(_:)-5czlf)
- [func tanpi(simd_double2) -> simd_double2](/documentation/simd/tanpi(_:)-9z76)

### Classification Functions

- [func isfinite(simd_double2) -> simd_long2](/documentation/simd/isfinite(_:)-7d8q7)
- [func isinf(simd_double2) -> simd_long2](/documentation/simd/isinf(_:)-4wflm)
- [func isnan(simd_double2) -> simd_long2](/documentation/simd/isnan(_:)-9irpc)
- [func isnormal(simd_double2) -> simd_long2](/documentation/simd/isnormal(_:)-61nr1)

### Alternative Type Alias

- [vector_double2](/documentation/simd/vector_double2)
- [double2](/documentation/simd/double2)
- [simd_double3](/documentation/simd/simd_double3)

### Functions to Create Three-Element Vectors From Other Vectors

- [func simd_make_double3(simd_double2) -> simd_double3](/documentation/simd/simd_make_double3(_:)-5ti92)
- [func simd_make_double3(simd_double3) -> simd_double3](/documentation/simd/simd_make_double3(_:)-5qigh)
- [func simd_make_double3(simd_double4) -> simd_double3](/documentation/simd/simd_make_double3(_:)-5zuas)
- [func simd_make_double3(simd_double8) -> simd_double3](/documentation/simd/simd_make_double3(_:)-4tl5k)
- [func simd_make_double3_undef(simd_double2) -> simd_double3](/documentation/simd/simd_make_double3_undef(_:)-95a07)

### Functions to Create Three-Element Vectors From Scalar Values

- [func simd_make_double3(Double) -> simd_double3](/documentation/simd/simd_make_double3(_:)-3qbde)
- [func simd_make_double3(Double, Double, Double) -> simd_double3](/documentation/simd/simd_make_double3(_:_:_:))
- [func simd_make_double3_undef(Double) -> simd_double3](/documentation/simd/simd_make_double3_undef(_:)-38cg2)

### Functions to Create Three-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_double3(Double, simd_double2) -> simd_double3](/documentation/simd/simd_make_double3(_:_:)-2va6)
- [func simd_make_double3(simd_double2, Double) -> simd_double3](/documentation/simd/simd_make_double3(_:_:)-3b3z3)

### Common Functions

- [func simd_abs(simd_double3) -> simd_double3](/documentation/simd/simd_abs(_:)-8db3x)
- [func abs(SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/abs(_:)-8miv)
- [func simd_clamp(simd_double3, simd_double3, simd_double3) -> simd_double3](/documentation/simd/simd_clamp(_:_:_:)-2jao)
- [func clamp(SIMD3<Double>, min: Double, max: Double) -> SIMD3<Double>](/documentation/simd/clamp(_:min:max:)-5otf7)
- [func clamp(SIMD3<Double>, min: SIMD3<Double>, max: SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/clamp(_:min:max:)-6m2so)
- [func simd_equal(simd_double3, simd_double3) -> simd_bool](/documentation/simd/simd_equal(_:_:)-4v2cb)
- [func simd_fract(simd_double3) -> simd_double3](/documentation/simd/simd_fract(_:)-47n4w)
- [func fract(SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/fract(_:)-swov)
- [func simd_sign(simd_double3) -> simd_double3](/documentation/simd/simd_sign(_:)-6goju)
- [func sign(SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/sign(_:)-2qtea)
- [func simd_step(simd_double3, simd_double3) -> simd_double3](/documentation/simd/simd_step(_:_:)-2gbx7)
- [func step(SIMD3<Double>, edge: SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/step(_:edge:)-4azct)

### Reduce Functions

- [func simd_reduce_add(simd_double3) -> Double](/documentation/simd/simd_reduce_add(_:)-2v7l1)
- [func reduce_add(SIMD3<Double>) -> Double](/documentation/simd/reduce_add(_:)-3112d)
- [func simd_reduce_max(simd_double3) -> Double](/documentation/simd/simd_reduce_max(_:)-4gytr)
- [func reduce_max(SIMD3<Double>) -> Double](/documentation/simd/reduce_max(_:)-96cb3)
- [func simd_reduce_min(simd_double3) -> Double](/documentation/simd/simd_reduce_min(_:)-46by3)
- [func reduce_min(SIMD3<Double>) -> Double](/documentation/simd/reduce_min(_:)-9g9a6)

### Interpolation Functions

- [func simd_mix(simd_double3, simd_double3, simd_double3) -> simd_double3](/documentation/simd/simd_mix(_:_:_:)-46dv1)
- [func mix(SIMD3<Double>, SIMD3<Double>, t: Double) -> SIMD3<Double>](/documentation/simd/mix(_:_:t:)-1dp7m)
- [func mix(SIMD3<Double>, SIMD3<Double>, t: SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/mix(_:_:t:)-5ifg3)
- [func simd_smoothstep(simd_double3, simd_double3, simd_double3) -> simd_double3](/documentation/simd/simd_smoothstep(_:_:_:)-9hwr9)
- [func smoothstep(SIMD3<Double>, edge0: SIMD3<Double>, edge1: SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/smoothstep(_:edge0:edge1:)-5ih1o)

### Extrema Functions

- [func simd_min(simd_double3, simd_double3) -> simd_double3](/documentation/simd/simd_min(_:_:)-5xqg7)
- [func min(SIMD3<Double>, Double) -> SIMD3<Double>](/documentation/simd/min(_:_:)-7hm19)
- [func min(SIMD3<Double>, SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/min(_:_:)-32b0w)
- [func fmin(SIMD3<Double>, SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/fmin(_:_:)-6p9y)
- [func simd_max(simd_double3, simd_double3) -> simd_double3](/documentation/simd/simd_max(_:_:)-6ykq4)
- [func max(SIMD3<Double>, Double) -> SIMD3<Double>](/documentation/simd/max(_:_:)-1mzkc)
- [func max(SIMD3<Double>, SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/max(_:_:)-9e6ry)
- [func fmax(SIMD3<Double>, SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/fmax(_:_:)-4pce8)

### Reciprocal and Reciprocal Square Root Functions

- [func simd_recip(simd_double3) -> simd_double3](/documentation/simd/simd_recip(_:)-8jzqn)
- [func recip(SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/recip(_:)-6uvj7)
- [func simd_rsqrt(simd_double3) -> simd_double3](/documentation/simd/simd_rsqrt(_:)-rhpf)
- [func rsqrt(SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/rsqrt(_:)-6298y)
- [func simd_precise_recip(simd_double3) -> simd_double3](/documentation/simd/simd_precise_recip(_:)-61i77)
- [func simd_precise_rsqrt(simd_double3) -> simd_double3](/documentation/simd/simd_precise_rsqrt(_:)-zrh9)
- [func simd_fast_recip(simd_double3) -> simd_double3](/documentation/simd/simd_fast_recip(_:)-ogui)
- [func simd_fast_rsqrt(simd_double3) -> simd_double3](/documentation/simd/simd_fast_rsqrt(_:)-80w49)

### Exponential and Logarithmic Functions

- [func exp(simd_double3) -> simd_double3](/documentation/simd/exp(_:)-zash)
- [func exp2(simd_double3) -> simd_double3](/documentation/simd/exp2(_:)-26tvo)
- [func exp10(simd_double3) -> simd_double3](/documentation/simd/exp10(_:)-88dd5)
- [func expm1(simd_double3) -> simd_double3](/documentation/simd/expm1(_:)-2ag4r)
- [func log(simd_double3) -> simd_double3](/documentation/simd/log(_:)-70ujd)
- [func log2(simd_double3) -> simd_double3](/documentation/simd/log2(_:)-3p8ex)
- [func log10(simd_double3) -> simd_double3](/documentation/simd/log10(_:)-1eshe)
- [func log1p(simd_double3) -> simd_double3](/documentation/simd/log1p(_:)-50npd)

### Geometry Functions

- [func cross(SIMD3<Double>, SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/cross(_:_:)-7sd7t)
- [func dot(SIMD3<Double>, SIMD3<Double>) -> Double](/documentation/simd/dot(_:_:)-2sdb)
- [func normalize(SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/normalize(_:)-29n8k)
- [func project(SIMD3<Double>, SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/project(_:_:)-9jlig)
- [func reflect(SIMD3<Double>, n: SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/reflect(_:n:)-1vw0n)
- [func refract(SIMD3<Double>, n: SIMD3<Double>, eta: Double) -> SIMD3<Double>](/documentation/simd/refract(_:n:eta:)-13wsy)

### Vector Norm Functions

- [func norm_one(SIMD3<Double>) -> Double](/documentation/simd/norm_one(_:)-mrh)
- [func norm_inf(SIMD3<Double>) -> Double](/documentation/simd/norm_inf(_:)-7ga8i)

### Length and Distance Functions

- [func length(SIMD3<Double>) -> Double](/documentation/simd/length(_:)-907xq)
- [func length_squared(SIMD3<Double>) -> Double](/documentation/simd/length_squared(_:)-620zs)
- [func distance(SIMD3<Double>, SIMD3<Double>) -> Double](/documentation/simd/distance(_:_:)-57zfj)
- [func distance_squared(SIMD3<Double>, SIMD3<Double>) -> Double](/documentation/simd/distance_squared(_:_:)-4erc0)

### Hyperbolic Functions

- [func acosh(simd_double3) -> simd_double3](/documentation/simd/acosh(_:)-1e4qf)
- [func asinh(simd_double3) -> simd_double3](/documentation/simd/asinh(_:)-8b3vg)
- [func atanh(simd_double3) -> simd_double3](/documentation/simd/atanh(_:)-7z6qz)
- [func cosh(simd_double3) -> simd_double3](/documentation/simd/cosh(_:)-6f3bc)
- [func sinh(simd_double3) -> simd_double3](/documentation/simd/sinh(_:)-6glq8)
- [func tanh(simd_double3) -> simd_double3](/documentation/simd/tanh(_:)-4b44y)

### Logic Functions

- [func simd_select(simd_double3, simd_double3, simd_long3) -> simd_double3](/documentation/simd/simd_select(_:_:_:)-1aiih)
- [func simd_bitselect(simd_double3, simd_double3, simd_long3) -> simd_double3](/documentation/simd/simd_bitselect(_:_:_:)-mtv1)

### Math Functions

- [func cbrt(simd_double3) -> simd_double3](/documentation/simd/cbrt(_:)-38h14)
- [func ceil(SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/ceil(_:)-72yci)
- [func erf(simd_double3) -> simd_double3](/documentation/simd/erf(_:)-8eer2)
- [func erfc(simd_double3) -> simd_double3](/documentation/simd/erfc(_:)-7ux6y)
- [func floor(SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/floor(_:)-262rp)
- [func fma(simd_double3, simd_double3, simd_double3) -> simd_double3](/documentation/simd/fma(_:_:_:)-6w3jf)
- [func fmod(simd_double3, simd_double3) -> simd_double3](/documentation/simd/fmod(_:_:)-16oie)
- [func hypot(simd_double3, simd_double3) -> simd_double3](/documentation/simd/hypot(_:_:)-5z7ry)
- [func lgamma(simd_double3) -> simd_double3](/documentation/simd/lgamma(_:)-4lks7)
- [func nextafter(simd_double3, simd_double3) -> simd_double3](/documentation/simd/nextafter(_:_:)-7qi1e)
- [func pow(simd_double3, simd_double3) -> simd_double3](/documentation/simd/pow(_:_:)-6hgod)
- [func remainder(simd_double3, simd_double3) -> simd_double3](/documentation/simd/remainder(_:_:)-28w7v)
- [func round(simd_double3) -> simd_double3](/documentation/simd/round(_:)-3e7l9)
- [func simd_muladd(simd_double3, simd_double3, simd_double3) -> simd_double3](/documentation/simd/simd_muladd(_:_:_:)-74qpk)
- [func tgamma(simd_double3) -> simd_double3](/documentation/simd/tgamma(_:)-98alm)
- [func trunc(SIMD3<Double>) -> SIMD3<Double>](/documentation/simd/trunc(_:)-4p8mg)

### Trigonometric Functions

- [func acos(simd_double3) -> simd_double3](/documentation/simd/acos(_:)-76i0e)
- [func asin(simd_double3) -> simd_double3](/documentation/simd/asin(_:)-g6mp)
- [func atan(simd_double3) -> simd_double3](/documentation/simd/atan(_:)-2h77h)
- [func atan2(simd_double3, simd_double3) -> simd_double3](/documentation/simd/atan2(_:_:)-1zx4a)
- [func cos(simd_double3) -> simd_double3](/documentation/simd/cos(_:)-9hw4a)
- [func cospi(simd_double3) -> simd_double3](/documentation/simd/cospi(_:)-471sg)
- [func sin(simd_double3) -> simd_double3](/documentation/simd/sin(_:)-5dnnn)
- [func sinpi(simd_double3) -> simd_double3](/documentation/simd/sinpi(_:)-291vx)
- [func sincos(simd_double3) -> (sin: simd_double3, cos: simd_double3)](/documentation/simd/sincos(_:)-6572x)
- [func sincospi(simd_double3) -> (sin: simd_double3, cos: simd_double3)](/documentation/simd/sincospi(_:)-2t5q7)
- [func tan(simd_double3) -> simd_double3](/documentation/simd/tan(_:)-2tvur)
- [func tanpi(simd_double3) -> simd_double3](/documentation/simd/tanpi(_:)-42odv)

### Classification Functions

- [func isfinite(simd_double3) -> simd_long3](/documentation/simd/isfinite(_:)-1s3ji)
- [func isinf(simd_double3) -> simd_long3](/documentation/simd/isinf(_:)-6gve5)
- [func isnan(simd_double3) -> simd_long3](/documentation/simd/isnan(_:)-6l7v3)
- [func isnormal(simd_double3) -> simd_long3](/documentation/simd/isnormal(_:)-8k36k)

### Alternative Type Alias

- [vector_double3](/documentation/simd/vector_double3)
- [double3](/documentation/simd/double3)
- [simd_double4](/documentation/simd/simd_double4)

### Functions to Create Four-Element Vectors From Other Vectors

- [func simd_make_double4(simd_double2) -> simd_double4](/documentation/simd/simd_make_double4(_:)-3ft6m)
- [func simd_make_double4(simd_double3) -> simd_double4](/documentation/simd/simd_make_double4(_:)-3jd0t)
- [func simd_make_double4(simd_double4) -> simd_double4](/documentation/simd/simd_make_double4(_:)-3ofj0)
- [func simd_make_double4(simd_double8) -> simd_double4](/documentation/simd/simd_make_double4(_:)-41bao)
- [func simd_make_double4(simd_double2, simd_double2) -> simd_double4](/documentation/simd/simd_make_double4(_:_:)-68v0e)
- [func simd_make_double4_undef(simd_double2) -> simd_double4](/documentation/simd/simd_make_double4_undef(_:)-6brs0)
- [func simd_make_double4_undef(simd_double3) -> simd_double4](/documentation/simd/simd_make_double4_undef(_:)-68wqb)

### Functions to Create Four-Element Vectors From Scalar Values

- [func simd_make_double4(Double) -> simd_double4](/documentation/simd/simd_make_double4(_:)-2zeiq)
- [func simd_make_double4(Double, Double, Double, Double) -> simd_double4](/documentation/simd/simd_make_double4(_:_:_:_:))
- [func simd_make_double4_undef(Double) -> simd_double4](/documentation/simd/simd_make_double4_undef(_:)-22old)

### Functions to Create Four-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_double4(Double, Double, simd_double2) -> simd_double4](/documentation/simd/simd_make_double4(_:_:_:)-51v00)
- [func simd_make_double4(Double, simd_double2, Double) -> simd_double4](/documentation/simd/simd_make_double4(_:_:_:)-8f2vh)
- [func simd_make_double4(Double, simd_double3) -> simd_double4](/documentation/simd/simd_make_double4(_:_:)-1ifzl)
- [func simd_make_double4(simd_double2, Double, Double) -> simd_double4](/documentation/simd/simd_make_double4(_:_:_:)-8b5fy)
- [func simd_make_double4(simd_double3, Double) -> simd_double4](/documentation/simd/simd_make_double4(_:_:)-767qm)

### Common Functions

- [func simd_abs(simd_double4) -> simd_double4](/documentation/simd/simd_abs(_:)-81rjc)
- [func abs(SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/abs(_:)-63bb7)
- [func simd_clamp(simd_double4, simd_double4, simd_double4) -> simd_double4](/documentation/simd/simd_clamp(_:_:_:)-8skia)
- [func clamp(SIMD4<Double>, min: Double, max: Double) -> SIMD4<Double>](/documentation/simd/clamp(_:min:max:)-3iua3)
- [func clamp(SIMD4<Double>, min: SIMD4<Double>, max: SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/clamp(_:min:max:)-51jkt)
- [func simd_fract(simd_double4) -> simd_double4](/documentation/simd/simd_fract(_:)-3w3dh)
- [func fract(SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/fract(_:)-8mowg)
- [func simd_equal(simd_double4, simd_double4) -> simd_bool](/documentation/simd/simd_equal(_:_:)-6lpka)
- [func simd_sign(simd_double4) -> simd_double4](/documentation/simd/simd_sign(_:)-74z7b)
- [func sign(SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/sign(_:)-86tur)
- [func simd_step(simd_double4, simd_double4) -> simd_double4](/documentation/simd/simd_step(_:_:)-6nrf4)
- [func step(SIMD4<Double>, edge: SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/step(_:edge:)-641e1)

### Reduce Functions

- [func simd_reduce_add(simd_double4) -> Double](/documentation/simd/simd_reduce_add(_:)-2ymlg)
- [func reduce_add(SIMD4<Double>) -> Double](/documentation/simd/reduce_add(_:)-7psay)
- [func simd_reduce_max(simd_double4) -> Double](/documentation/simd/simd_reduce_max(_:)-4qv3y)
- [func reduce_max(SIMD4<Double>) -> Double](/documentation/simd/reduce_max(_:)-66smw)
- [func simd_reduce_min(simd_double4) -> Double](/documentation/simd/simd_reduce_min(_:)-4umgm)
- [func reduce_min(SIMD4<Double>) -> Double](/documentation/simd/reduce_min(_:)-4bbr)

### Interpolation Functions

- [func simd_smoothstep(simd_double4, simd_double4, simd_double4) -> simd_double4](/documentation/simd/simd_smoothstep(_:_:_:)-6idlb)
- [func smoothstep(SIMD4<Double>, edge0: SIMD4<Double>, edge1: SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/smoothstep(_:edge0:edge1:)-3gmrv)
- [func simd_mix(simd_double4, simd_double4, simd_double4) -> simd_double4](/documentation/simd/simd_mix(_:_:_:)-49aeg)
- [func mix(SIMD4<Double>, SIMD4<Double>, t: Double) -> SIMD4<Double>](/documentation/simd/mix(_:_:t:)-9jxxl)
- [func mix(SIMD4<Double>, SIMD4<Double>, t: SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/mix(_:_:t:)-92fbo)

### Extrema Functions

- [func simd_max(simd_double4, simd_double4) -> simd_double4](/documentation/simd/simd_max(_:_:)-72b4)
- [func max(SIMD4<Double>, Double) -> SIMD4<Double>](/documentation/simd/max(_:_:)-82ig0)
- [func max(SIMD4<Double>, SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/max(_:_:)-4pgdo)
- [func fmax(SIMD4<Double>, SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/fmax(_:_:)-60f6g)
- [func simd_min(simd_double4, simd_double4) -> simd_double4](/documentation/simd/simd_min(_:_:)-78g6s)
- [func min(SIMD4<Double>, Double) -> SIMD4<Double>](/documentation/simd/min(_:_:)-7rmn)
- [func min(SIMD4<Double>, SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/min(_:_:)-8m4sw)
- [func fmin(SIMD4<Double>, SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/fmin(_:_:)-4joph)

### Reciprocal and Reciprocal Square Root Functions

- [func simd_recip(simd_double4) -> simd_double4](/documentation/simd/simd_recip(_:)-8218m)
- [func recip(SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/recip(_:)-2zcya)
- [func simd_rsqrt(simd_double4) -> simd_double4](/documentation/simd/simd_rsqrt(_:)-i5ka)
- [func rsqrt(SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/rsqrt(_:)-8rb58)
- [func simd_precise_recip(simd_double4) -> simd_double4](/documentation/simd/simd_precise_recip(_:)-6pt5q)
- [func simd_precise_rsqrt(simd_double4) -> simd_double4](/documentation/simd/simd_precise_rsqrt(_:)-136bw)
- [func simd_fast_recip(simd_double4) -> simd_double4](/documentation/simd/simd_fast_recip(_:)-61j)
- [func simd_fast_rsqrt(simd_double4) -> simd_double4](/documentation/simd/simd_fast_rsqrt(_:)-8p6tk)

### Exponential and Logarithmic Functions

- [func exp(simd_double4) -> simd_double4](/documentation/simd/exp(_:)-92zj)
- [func exp2(simd_double4) -> simd_double4](/documentation/simd/exp2(_:)-6nz50)
- [func exp10(simd_double4) -> simd_double4](/documentation/simd/exp10(_:)-apfo)
- [func expm1(simd_double4) -> simd_double4](/documentation/simd/expm1(_:)-4osfq)
- [func log(simd_double4) -> simd_double4](/documentation/simd/log(_:)-54908)
- [func log2(simd_double4) -> simd_double4](/documentation/simd/log2(_:)-2m5uu)
- [func log10(simd_double4) -> simd_double4](/documentation/simd/log10(_:)-80x29)
- [func log1p(simd_double4) -> simd_double4](/documentation/simd/log1p(_:)-t4r0)

### Geometry Functions

- [func dot(SIMD4<Double>, SIMD4<Double>) -> Double](/documentation/simd/dot(_:_:)-5ifd)
- [func normalize(SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/normalize(_:)-3lhrd)
- [func project(SIMD4<Double>, SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/project(_:_:)-1uuxo)
- [func reflect(SIMD4<Double>, n: SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/reflect(_:n:)-1nabs)
- [func refract(SIMD4<Double>, n: SIMD4<Double>, eta: Double) -> SIMD4<Double>](/documentation/simd/refract(_:n:eta:)-2macj)

### Vector Norm Functions

- [func norm_one(SIMD4<Double>) -> Double](/documentation/simd/norm_one(_:)-1cwpd)
- [func norm_inf(SIMD4<Double>) -> Double](/documentation/simd/norm_inf(_:)-8zws7)

### Length and Distance Functions

- [func length(SIMD4<Double>) -> Double](/documentation/simd/length(_:)-79i68)
- [func length_squared(SIMD4<Double>) -> Double](/documentation/simd/length_squared(_:)-856uz)
- [func distance(SIMD4<Double>, SIMD4<Double>) -> Double](/documentation/simd/distance(_:_:)-559m9)
- [func distance_squared(SIMD4<Double>, SIMD4<Double>) -> Double](/documentation/simd/distance_squared(_:_:)-73nv3)

### Hyperbolic Functions

- [func acosh(simd_double4) -> simd_double4](/documentation/simd/acosh(_:)-2a3a)
- [func asinh(simd_double4) -> simd_double4](/documentation/simd/asinh(_:)-847y)
- [func atanh(simd_double4) -> simd_double4](/documentation/simd/atanh(_:)-17pza)
- [func cosh(simd_double4) -> simd_double4](/documentation/simd/cosh(_:)-8h0te)
- [func sinh(simd_double4) -> simd_double4](/documentation/simd/sinh(_:)-3rjw6)
- [func tanh(simd_double4) -> simd_double4](/documentation/simd/tanh(_:)-x8vt)

### Logic Functions

- [func simd_select(simd_double4, simd_double4, simd_long4) -> simd_double4](/documentation/simd/simd_select(_:_:_:)-tq6k)
- [func simd_bitselect(simd_double4, simd_double4, simd_long4) -> simd_double4](/documentation/simd/simd_bitselect(_:_:_:)-1mn6g)

### Math Functions

- [func cbrt(simd_double4) -> simd_double4](/documentation/simd/cbrt(_:)-7pm3s)
- [func ceil(SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/ceil(_:)-9s503)
- [func erf(simd_double4) -> simd_double4](/documentation/simd/erf(_:)-1yjjk)
- [func erfc(simd_double4) -> simd_double4](/documentation/simd/erfc(_:)-6rgzx)
- [func floor(SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/floor(_:)-3956i)
- [func fma(simd_double4, simd_double4, simd_double4) -> simd_double4](/documentation/simd/fma(_:_:_:)-6mqpv)
- [func fmod(simd_double4, simd_double4) -> simd_double4](/documentation/simd/fmod(_:_:)-92tjw)
- [func hypot(simd_double4, simd_double4) -> simd_double4](/documentation/simd/hypot(_:_:)-2exik)
- [func lgamma(simd_double4) -> simd_double4](/documentation/simd/lgamma(_:)-2frmv)
- [func nextafter(simd_double4, simd_double4) -> simd_double4](/documentation/simd/nextafter(_:_:)-oxq7)
- [func pow(simd_double4, simd_double4) -> simd_double4](/documentation/simd/pow(_:_:)-3jh7o)
- [func remainder(simd_double4, simd_double4) -> simd_double4](/documentation/simd/remainder(_:_:)-jw8b)
- [func round(simd_double4) -> simd_double4](/documentation/simd/round(_:)-5ytc6)
- [func simd_muladd(simd_double4, simd_double4, simd_double4) -> simd_double4](/documentation/simd/simd_muladd(_:_:_:)-6kpyx)
- [func tgamma(simd_double4) -> simd_double4](/documentation/simd/tgamma(_:)-2o8vo)
- [func trunc(SIMD4<Double>) -> SIMD4<Double>](/documentation/simd/trunc(_:)-9n2h5)

### Trigonometric Functions

- [func acos(simd_double4) -> simd_double4](/documentation/simd/acos(_:)-9cb48)
- [func asin(simd_double4) -> simd_double4](/documentation/simd/asin(_:)-70soc)
- [func atan(simd_double4) -> simd_double4](/documentation/simd/atan(_:)-5w6c7)
- [func atan2(simd_double4, simd_double4) -> simd_double4](/documentation/simd/atan2(_:_:)-19fnn)
- [func cos(simd_double4) -> simd_double4](/documentation/simd/cos(_:)-1leci)
- [func cospi(simd_double4) -> simd_double4](/documentation/simd/cospi(_:)-8cke2)
- [func sin(simd_double4) -> simd_double4](/documentation/simd/sin(_:)-67ulu)
- [func sinpi(simd_double4) -> simd_double4](/documentation/simd/sinpi(_:)-45nf0)
- [func sincos(simd_double4) -> (sin: simd_double4, cos: simd_double4)](/documentation/simd/sincos(_:)-9olep)
- [func sincospi(simd_double4) -> (sin: simd_double4, cos: simd_double4)](/documentation/simd/sincospi(_:)-40ymv)
- [func tan(simd_double4) -> simd_double4](/documentation/simd/tan(_:)-5zsp2)
- [func tanpi(simd_double4) -> simd_double4](/documentation/simd/tanpi(_:)-54qo6)

### Classification Functions

- [func isfinite(simd_double4) -> simd_long4](/documentation/simd/isfinite(_:)-1870d)
- [func isinf(simd_double4) -> simd_long4](/documentation/simd/isinf(_:)-4gutc)
- [func isnan(simd_double4) -> simd_long4](/documentation/simd/isnan(_:)-94v5c)
- [func isnormal(simd_double4) -> simd_long4](/documentation/simd/isnormal(_:)-35fxl)

### Alternative Type Alias

- [vector_double4](/documentation/simd/vector_double4)
- [double4](/documentation/simd/double4)
- [simd_double8](/documentation/simd/simd_double8)

### Functions to Create Eight-Element Vectors From Other Vectors

- [func simd_make_double8(simd_double2) -> simd_double8](/documentation/simd/simd_make_double8(_:)-3wn9q)
- [func simd_make_double8(simd_double3) -> simd_double8](/documentation/simd/simd_make_double8(_:)-40259)
- [func simd_make_double8(simd_double4) -> simd_double8](/documentation/simd/simd_make_double8(_:)-3br50)
- [func simd_make_double8(simd_double8) -> simd_double8](/documentation/simd/simd_make_double8(_:)-4i0aw)
- [func simd_make_double8(simd_double4, simd_double4) -> simd_double8](/documentation/simd/simd_make_double8(_:_:))
- [func simd_make_double8_undef(simd_double2) -> simd_double8](/documentation/simd/simd_make_double8_undef(_:)-7g0z0)
- [func simd_make_double8_undef(simd_double3) -> simd_double8](/documentation/simd/simd_make_double8_undef(_:)-7d127)
- [func simd_make_double8_undef(simd_double4) -> simd_double8](/documentation/simd/simd_make_double8_undef(_:)-7md0u)

### Functions to Create Eight-Element Vectors From Scalar Values

- [func simd_make_double8(Double) -> simd_double8](/documentation/simd/simd_make_double8(_:)-56g8y)
- [func simd_make_double8_undef(Double) -> simd_double8](/documentation/simd/simd_make_double8_undef(_:)-5rmk5)

### Common Functions

- [func simd_abs(simd_double8) -> simd_double8](/documentation/simd/simd_abs(_:)-7p0dw)
- [func simd_clamp(simd_double8, simd_double8, simd_double8) -> simd_double8](/documentation/simd/simd_clamp(_:_:_:)-q88m)
- [func simd_equal(simd_double8, simd_double8) -> simd_bool](/documentation/simd/simd_equal(_:_:)-8pk1m)
- [func simd_fract(simd_double8) -> simd_double8](/documentation/simd/simd_fract(_:)-3jcfd)
- [func simd_sign(simd_double8) -> simd_double8](/documentation/simd/simd_sign(_:)-7hb8r)
- [func simd_step(simd_double8, simd_double8) -> simd_double8](/documentation/simd/simd_step(_:_:)-1vckv)

### Reduce Functions

- [func simd_reduce_min(simd_double8) -> Double](/documentation/simd/simd_reduce_min(_:)-3ode2)
- [func simd_reduce_max(simd_double8) -> Double](/documentation/simd/simd_reduce_max(_:)-55eqq)
- [func simd_reduce_add(simd_double8) -> Double](/documentation/simd/simd_reduce_add(_:)-3aymg)

### Interpolation Functions

- [func simd_smoothstep(simd_double8, simd_double8, simd_double8) -> simd_double8](/documentation/simd/simd_smoothstep(_:_:_:)-99l4q)
- [func simd_mix(simd_double8, simd_double8, simd_double8) -> simd_double8](/documentation/simd/simd_mix(_:_:_:)-5afwd)

### Extrema Functions

- [func simd_min(simd_double8, simd_double8) -> simd_double8](/documentation/simd/simd_min(_:_:)-6beor)
- [func simd_max(simd_double8, simd_double8) -> simd_double8](/documentation/simd/simd_max(_:_:)-65po6)

### Reciprocal and Reciprocal Square Root Functions

- [func simd_recip(simd_double8) -> simd_double8](/documentation/simd/simd_recip(_:)-98afu)
- [func simd_fast_recip(simd_double8) -> simd_double8](/documentation/simd/simd_fast_recip(_:)-16f97)
- [func simd_precise_recip(simd_double8) -> simd_double8](/documentation/simd/simd_precise_recip(_:)-74cqq)
- [func simd_rsqrt(simd_double8) -> simd_double8](/documentation/simd/simd_rsqrt(_:)-1ojpy)
- [func simd_fast_rsqrt(simd_double8) -> simd_double8](/documentation/simd/simd_fast_rsqrt(_:)-922us)
- [func simd_precise_rsqrt(simd_double8) -> simd_double8](/documentation/simd/simd_precise_rsqrt(_:)-1hq00)

### Exponential and Logarithmic Functions

- [func exp(simd_double8) -> simd_double8](/documentation/simd/exp(_:)-69tin)
- [func exp2(simd_double8) -> simd_double8](/documentation/simd/exp2(_:)-4m3mb)
- [func exp10(simd_double8) -> simd_double8](/documentation/simd/exp10(_:)-39f7r)
- [func expm1(simd_double8) -> simd_double8](/documentation/simd/expm1(_:)-8nn5x)
- [func log(simd_double8) -> simd_double8](/documentation/simd/log(_:)-7649l)
- [func log2(simd_double8) -> simd_double8](/documentation/simd/log2(_:)-8k8nf)
- [func log10(simd_double8) -> simd_double8](/documentation/simd/log10(_:)-24ung)
- [func log1p(simd_double8) -> simd_double8](/documentation/simd/log1p(_:)-3fdfb)

### Hyperbolic Functions

- [func acosh(simd_double8) -> simd_double8](/documentation/simd/acosh(_:)-2zf9d)
- [func asinh(simd_double8) -> simd_double8](/documentation/simd/asinh(_:)-5vu4r)
- [func atanh(simd_double8) -> simd_double8](/documentation/simd/atanh(_:)-d3b3)
- [func cosh(simd_double8) -> simd_double8](/documentation/simd/cosh(_:)-1g57o)
- [func sinh(simd_double8) -> simd_double8](/documentation/simd/sinh(_:)-ip9w)
- [func tanh(simd_double8) -> simd_double8](/documentation/simd/tanh(_:)-1ag6z)

### Logic Functions

- [func simd_select(simd_double8, simd_double8, simd_long8) -> simd_double8](/documentation/simd/simd_select(_:_:_:)-8wti7)
- [func simd_bitselect(simd_double8, simd_double8, simd_long8) -> simd_double8](/documentation/simd/simd_bitselect(_:_:_:)-1yj5q)

### Math Functions

- [func cbrt(simd_double8) -> simd_double8](/documentation/simd/cbrt(_:)-9dsjc)
- [func erf(simd_double8) -> simd_double8](/documentation/simd/erf(_:)-293ey)
- [func erfc(simd_double8) -> simd_double8](/documentation/simd/erfc(_:)-vzkw)
- [func fma(simd_double8, simd_double8, simd_double8) -> simd_double8](/documentation/simd/fma(_:_:_:)-95vfo)
- [func fmod(simd_double8, simd_double8) -> simd_double8](/documentation/simd/fmod(_:_:)-7g7m)
- [func hypot(simd_double8, simd_double8) -> simd_double8](/documentation/simd/hypot(_:_:)-8vke8)
- [func lgamma(simd_double8) -> simd_double8](/documentation/simd/lgamma(_:)-7t6g8)
- [func nextafter(simd_double8, simd_double8) -> simd_double8](/documentation/simd/nextafter(_:_:)-2xerr)
- [func pow(simd_double8, simd_double8) -> simd_double8](/documentation/simd/pow(_:_:)-9xmzf)
- [func remainder(simd_double8, simd_double8) -> simd_double8](/documentation/simd/remainder(_:_:)-326ci)
- [func round(simd_double8) -> simd_double8](/documentation/simd/round(_:)-7t6q)
- [func simd_muladd(simd_double8, simd_double8, simd_double8) -> simd_double8](/documentation/simd/simd_muladd(_:_:_:)-2vs0c)
- [func tgamma(simd_double8) -> simd_double8](/documentation/simd/tgamma(_:)-8qiri)

### Trigonometric Functions

- [func acos(simd_double8) -> simd_double8](/documentation/simd/acos(_:)-2141m)
- [func asin(simd_double8) -> simd_double8](/documentation/simd/asin(_:)-78d03)
- [func atan(simd_double8) -> simd_double8](/documentation/simd/atan(_:)-7b52p)
- [func atan2(simd_double8, simd_double8) -> simd_double8](/documentation/simd/atan2(_:_:)-8pfg9)
- [func cos(simd_double8) -> simd_double8](/documentation/simd/cos(_:)-7bqey)
- [func cospi(simd_double8) -> simd_double8](/documentation/simd/cospi(_:)-8d55q)
- [func sin(simd_double8) -> simd_double8](/documentation/simd/sin(_:)-1joh9)
- [func sinpi(simd_double8) -> simd_double8](/documentation/simd/sinpi(_:)-9tdix)
- [func sincos(simd_double8) -> (sin: simd_double8, cos: simd_double8)](/documentation/simd/sincos(_:)-3iwed)
- [func sincospi(simd_double8) -> (sin: simd_double8, cos: simd_double8)](/documentation/simd/sincospi(_:)-5yfry)
- [func tan(simd_double8) -> simd_double8](/documentation/simd/tan(_:)-7a2xj)
- [func tanpi(simd_double8) -> simd_double8](/documentation/simd/tanpi(_:)-3lobh)

### Classification Functions

- [func isfinite(simd_double8) -> simd_long8](/documentation/simd/isfinite(_:)-9iwij)
- [func isinf(simd_double8) -> simd_long8](/documentation/simd/isinf(_:)-5i1uj)
- [func isnan(simd_double8) -> simd_long8](/documentation/simd/isnan(_:)-90lcg)
- [func isnormal(simd_double8) -> simd_long8](/documentation/simd/isnormal(_:)-7lk2x)

### Alternative Type Alias

- [vector_double8](/documentation/simd/vector_double8)
- [simd_float1](/documentation/simd/simd_float1)

### Common Functions

- [func step(Float, edge: Float) -> Float](/documentation/simd/step(_:edge:)-7md5f)
- [func simd_step(Float, Float) -> Float](/documentation/simd/simd_step(_:_:)-7127e)
- [func simd_clamp(Float, Float, Float) -> Float](/documentation/simd/simd_clamp(_:_:_:)-8f4ck)
- [func simd_fract(Float) -> Float](/documentation/simd/simd_fract(_:)-1ws2w)
- [func sign(Float) -> Float](/documentation/simd/sign(_:)-iw0p)
- [func simd_sign(Float) -> Float](/documentation/simd/simd_sign(_:)-9380i)

### Interpolation Functions

- [func simd_mix(Float, Float, Float) -> Float](/documentation/simd/simd_mix(_:_:_:)-3i6gv)
- [func simd_smoothstep(Float, Float, Float) -> Float](/documentation/simd/simd_smoothstep(_:_:_:)-993b1)

### Extrema Functions

- [func simd_min(Float, Float) -> Float](/documentation/simd/simd_min(_:_:)-8o17r)
- [func simd_max(Float, Float) -> Float](/documentation/simd/simd_max(_:_:)-7wj2s)

### Reciprocal and Reciprocal Square Root Functions

- [func recip(Float) -> Float](/documentation/simd/recip(_:)-8b743)
- [func simd_recip(Float) -> Float](/documentation/simd/simd_recip(_:)-7ylar)
- [func simd_fast_recip(Float) -> Float](/documentation/simd/simd_fast_recip(_:)-1hpi)
- [func simd_precise_recip(Float) -> Float](/documentation/simd/simd_precise_recip(_:)-6qbmp)
- [func rsqrt(Float) -> Float](/documentation/simd/rsqrt(_:)-7h1cq)
- [func simd_rsqrt(Float) -> Float](/documentation/simd/simd_rsqrt(_:)-4yg08)
- [func simd_fast_rsqrt(Float) -> Float](/documentation/simd/simd_fast_rsqrt(_:)-43uag)
- [func simd_precise_rsqrt(Float) -> Float](/documentation/simd/simd_precise_rsqrt(_:)-5flt4)

### Math Functions

- [func simd_muladd(Float, Float, Float) -> Float](/documentation/simd/simd_muladd(_:_:_:)-2pepd)
- [simd_float16](/documentation/simd/simd_float16)

### Functions to Create 16-Element Vectors From Other Vectors

- [func simd_make_float16(simd_float2) -> simd_float16](/documentation/simd/simd_make_float16(_:)-73rau)
- [func simd_make_float16(simd_float3) -> simd_float16](/documentation/simd/simd_make_float16(_:)-76ned)
- [func simd_make_float16(simd_float4) -> simd_float16](/documentation/simd/simd_make_float16(_:)-6v3h4)
- [func simd_make_float16(simd_float8) -> simd_float16](/documentation/simd/simd_make_float16(_:)-81hjg)
- [func simd_make_float16(simd_float16) -> simd_float16](/documentation/simd/simd_make_float16(_:)-5j0rl)
- [func simd_make_float16(simd_float8, simd_float8) -> simd_float16](/documentation/simd/simd_make_float16(_:_:))
- [func simd_make_float16_undef(simd_float2) -> simd_float16](/documentation/simd/simd_make_float16_undef(_:)-3f8p6)
- [func simd_make_float16_undef(simd_float3) -> simd_float16](/documentation/simd/simd_make_float16_undef(_:)-3bslp)
- [func simd_make_float16_undef(simd_float4) -> simd_float16](/documentation/simd/simd_make_float16_undef(_:)-38xrw)
- [func simd_make_float16_undef(simd_float8) -> simd_float16](/documentation/simd/simd_make_float16_undef(_:)-4f6xc)

### Functions to Create 16-Element Vectors From Scalar Values

- [func simd_make_float16(Float) -> simd_float16](/documentation/simd/simd_make_float16(_:)-4r3a8)
- [func simd_make_float16_undef(Float) -> simd_float16](/documentation/simd/simd_make_float16_undef(_:)-71tt7)

### Alternative Type Alias

- [vector_float16](/documentation/simd/vector_float16)

### Common Functions

- [func simd_abs(simd_float16) -> simd_float16](/documentation/simd/simd_abs(_:)-47h6g)
- [func simd_clamp(simd_float16, simd_float16, simd_float16) -> simd_float16](/documentation/simd/simd_clamp(_:_:_:)-92son)
- [func simd_equal(simd_float16, simd_float16) -> simd_bool](/documentation/simd/simd_equal(_:_:)-376kl)
- [func simd_fract(simd_float16) -> simd_float16](/documentation/simd/simd_fract(_:)-6v1ix)
- [func simd_sign(simd_float16) -> simd_float16](/documentation/simd/simd_sign(_:)-tc2v)
- [func simd_step(simd_float16, simd_float16) -> simd_float16](/documentation/simd/simd_step(_:_:)-14cn0)

### Reduce Functions

- [func simd_reduce_min(simd_float16) -> Float](/documentation/simd/simd_reduce_min(_:)-3d29t)
- [func simd_reduce_max(simd_float16) -> Float](/documentation/simd/simd_reduce_max(_:)-8iok7)
- [func simd_reduce_add(simd_float16) -> Float](/documentation/simd/simd_reduce_add(_:)-7n310)

### Interpolation Functions

- [func simd_smoothstep(simd_float16, simd_float16, simd_float16) -> simd_float16](/documentation/simd/simd_smoothstep(_:_:_:)-2q68m)
- [func simd_mix(simd_float16, simd_float16, simd_float16) -> simd_float16](/documentation/simd/simd_mix(_:_:_:)-1hgrq)

### Extrema Functions

- [func simd_min(simd_float16, simd_float16) -> simd_float16](/documentation/simd/simd_min(_:_:)-6clj9)
- [func simd_max(simd_float16, simd_float16) -> simd_float16](/documentation/simd/simd_max(_:_:)-90s23)

### Reciprocal and Reciprocal Square Root Functions

- [func simd_recip(simd_float16) -> simd_float16](/documentation/simd/simd_recip(_:)-5bwdz)
- [func simd_fast_recip(simd_float16) -> simd_float16](/documentation/simd/simd_fast_recip(_:)-mza9)
- [func simd_precise_recip(simd_float16) -> simd_float16](/documentation/simd/simd_precise_recip(_:)-5ic8t)
- [func simd_rsqrt(simd_float16) -> simd_float16](/documentation/simd/simd_rsqrt(_:)-76a19)
- [func simd_fast_rsqrt(simd_float16) -> simd_float16](/documentation/simd/simd_fast_rsqrt(_:)-6862g)
- [func simd_precise_rsqrt(simd_float16) -> simd_float16](/documentation/simd/simd_precise_rsqrt(_:)-6j35f)

### Exponential and Logarithmic Functions

- [func exp(simd_float16) -> simd_float16](/documentation/simd/exp(_:)-2ru57)
- [func exp2(simd_float16) -> simd_float16](/documentation/simd/exp2(_:)-271hg)
- [func exp10(simd_float16) -> simd_float16](/documentation/simd/exp10(_:)-165iq)
- [func expm1(simd_float16) -> simd_float16](/documentation/simd/expm1(_:)-90g3j)
- [func log(simd_float16) -> simd_float16](/documentation/simd/log(_:)-44j3q)
- [func log2(simd_float16) -> simd_float16](/documentation/simd/log2(_:)-8nusk)
- [func log10(simd_float16) -> simd_float16](/documentation/simd/log10(_:)-7eq4p)
- [func log1p(simd_float16) -> simd_float16](/documentation/simd/log1p(_:)-2uw4e)

### Hyperbolic Functions

- [func acosh(simd_float16) -> simd_float16](/documentation/simd/acosh(_:)-4w84k)
- [func asinh(simd_float16) -> simd_float16](/documentation/simd/asinh(_:)-6v4m)
- [func atanh(simd_float16) -> simd_float16](/documentation/simd/atanh(_:)-70pvm)
- [func cosh(simd_float16) -> simd_float16](/documentation/simd/cosh(_:)-9kvzr)
- [func sinh(simd_float16) -> simd_float16](/documentation/simd/sinh(_:)-1d6si)
- [func tanh(simd_float16) -> simd_float16](/documentation/simd/tanh(_:)-7sto5)

### Logic Functions

- [func simd_select(simd_float16, simd_float16, simd_int16) -> simd_float16](/documentation/simd/simd_select(_:_:_:)-41fgt)
- [func simd_bitselect(simd_float16, simd_float16, simd_int16) -> simd_float16](/documentation/simd/simd_bitselect(_:_:_:)-wjqf)

### Math Functions

- [func cbrt(simd_float16) -> simd_float16](/documentation/simd/cbrt(_:)-3cnri)
- [func erf(simd_float16) -> simd_float16](/documentation/simd/erf(_:)-7wkg3)
- [func erfc(simd_float16) -> simd_float16](/documentation/simd/erfc(_:)-20vsh)
- [func fma(simd_float16, simd_float16, simd_float16) -> simd_float16](/documentation/simd/fma(_:_:_:)-503dp)
- [func fmod(simd_float16, simd_float16) -> simd_float16](/documentation/simd/fmod(_:_:)-2bys0)
- [func hypot(simd_float16, simd_float16) -> simd_float16](/documentation/simd/hypot(_:_:)-265pt)
- [func lgamma(simd_float16) -> simd_float16](/documentation/simd/lgamma(_:)-1onkc)
- [func nextafter(simd_float16, simd_float16) -> simd_float16](/documentation/simd/nextafter(_:_:)-9kvo8)
- [func pow(simd_float16, simd_float16) -> simd_float16](/documentation/simd/pow(_:_:)-7mpyc)
- [func remainder(simd_float16, simd_float16) -> simd_float16](/documentation/simd/remainder(_:_:)-5dxqm)
- [func round(simd_float16) -> simd_float16](/documentation/simd/round(_:)-74w3c)
- [func simd_muladd(simd_float16, simd_float16, simd_float16) -> simd_float16](/documentation/simd/simd_muladd(_:_:_:)-8imv2)
- [func tgamma(simd_float16) -> simd_float16](/documentation/simd/tgamma(_:)-9r61k)

### Trigonometric Functions

- [func acos(simd_float16) -> simd_float16](/documentation/simd/acos(_:)-9k95t)
- [func asin(simd_float16) -> simd_float16](/documentation/simd/asin(_:)-52bly)
- [func atan(simd_float16) -> simd_float16](/documentation/simd/atan(_:)-7y100)
- [func atan2(simd_float16, simd_float16) -> simd_float16](/documentation/simd/atan2(_:_:)-5dweo)
- [func cos(simd_float16) -> simd_float16](/documentation/simd/cos(_:)-40gvn)
- [func cospi(simd_float16) -> simd_float16](/documentation/simd/cospi(_:)-7kfdh)
- [func sin(simd_float16) -> simd_float16](/documentation/simd/sin(_:)-7e17y)
- [func sinpi(simd_float16) -> simd_float16](/documentation/simd/sinpi(_:)-6d2hq)
- [func sincos(simd_float16) -> (sin: simd_float16, cos: simd_float16)](/documentation/simd/sincos(_:)-go67)
- [func sincospi(simd_float16) -> (sin: simd_float16, cos: simd_float16)](/documentation/simd/sincospi(_:)-h3av)
- [func tan(simd_float16) -> simd_float16](/documentation/simd/tan(_:)-5q9ad)
- [func tanpi(simd_float16) -> simd_float16](/documentation/simd/tanpi(_:)-2vht8)

### Classification Functions

- [func isfinite(simd_float16) -> simd_int16](/documentation/simd/isfinite(_:)-8bt9t)
- [func isinf(simd_float16) -> simd_int16](/documentation/simd/isinf(_:)-77t4f)
- [func isnan(simd_float16) -> simd_int16](/documentation/simd/isnan(_:)-3ek5k)
- [func isnormal(simd_float16) -> simd_int16](/documentation/simd/isnormal(_:)-86aj9)
- [simd_float2](/documentation/simd/simd_float2)

### Functions to Create Two-Element Vectors From Other Vectors

- [func simd_make_float2(simd_float2) -> simd_float2](/documentation/simd/simd_make_float2(_:)-3nphb)
- [func simd_make_float2(simd_float3) -> simd_float2](/documentation/simd/simd_make_float2(_:)-3kta4)
- [func simd_make_float2(simd_float4) -> simd_float2](/documentation/simd/simd_make_float2(_:)-32usp)
- [func simd_make_float2(simd_float8) -> simd_float2](/documentation/simd/simd_make_float2(_:)-493yd)
- [func simd_make_float2(simd_float16) -> simd_float2](/documentation/simd/simd_make_float2(_:)-4e6k3)

### Functions to Create Two-Element Vectors From Scalar Values

- [func simd_make_float2(Float) -> simd_float2](/documentation/simd/simd_make_float2(_:)-70ndk)
- [func simd_make_float2(Float, Float) -> simd_float2](/documentation/simd/simd_make_float2(_:_:))
- [func simd_make_float2_undef(Float) -> simd_float2](/documentation/simd/simd_make_float2_undef(_:))

### Common Functions

- [func simd_abs(simd_float2) -> simd_float2](/documentation/simd/simd_abs(_:)-886vq)
- [func abs(SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/abs(_:)-6ckob)
- [func simd_clamp(simd_float2, simd_float2, simd_float2) -> simd_float2](/documentation/simd/simd_clamp(_:_:_:)-9b6uf)
- [func clamp(SIMD2<Float>, min: Float, max: Float) -> SIMD2<Float>](/documentation/simd/clamp(_:min:max:)-5rthg)
- [func clamp(SIMD2<Float>, min: SIMD2<Float>, max: SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/clamp(_:min:max:)-3oo0f)
- [func simd_equal(simd_float2, simd_float2) -> simd_bool](/documentation/simd/simd_equal(_:_:)-9z8e8)
- [func simd_fract(simd_float2) -> simd_float2](/documentation/simd/simd_fract(_:)-42ipv)
- [func fract(SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/fract(_:)-7rplw)
- [func simd_sign(simd_float2) -> simd_float2](/documentation/simd/simd_sign(_:)-6jld1)
- [func sign(SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/sign(_:)-2e6do)
- [func simd_step(simd_float2, simd_float2) -> simd_float2](/documentation/simd/simd_step(_:_:)-9xjdc)
- [func step(SIMD2<Float>, edge: SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/step(_:edge:)-1pthr)

### Reduce Functions

- [func simd_reduce_add(simd_float2) -> Float](/documentation/simd/simd_reduce_add(_:)-2pzn6)
- [func reduce_add(SIMD2<Float>) -> Float](/documentation/simd/reduce_add(_:)-39n2m)
- [func simd_reduce_max(simd_float2) -> Float](/documentation/simd/simd_reduce_max(_:)-4kjh0)
- [func reduce_max(SIMD2<Float>) -> Float](/documentation/simd/reduce_max(_:)-4zzwq)
- [func simd_reduce_min(simd_float2) -> Float](/documentation/simd/simd_reduce_min(_:)-49sh0)
- [func reduce_min(SIMD2<Float>) -> Float](/documentation/simd/reduce_min(_:)-76co5)

### Interpolation Functions

- [func simd_mix(simd_float2, simd_float2, simd_float2) -> simd_float2](/documentation/simd/simd_mix(_:_:_:)-bvhh)
- [func mix(SIMD2<Float>, SIMD2<Float>, t: Float) -> SIMD2<Float>](/documentation/simd/mix(_:_:t:)-2z3yo)
- [func mix(SIMD2<Float>, SIMD2<Float>, t: SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/mix(_:_:t:)-14tli)
- [func simd_smoothstep(simd_float2, simd_float2, simd_float2) -> simd_float2](/documentation/simd/simd_smoothstep(_:_:_:)-7iziv)
- [func smoothstep(SIMD2<Float>, edge0: SIMD2<Float>, edge1: SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/smoothstep(_:edge0:edge1:)-43udr)

### Extrema Functions

- [func simd_max(simd_float2, simd_float2) -> simd_float2](/documentation/simd/simd_max(_:_:)-6uws6)
- [func max(SIMD2<Float>, Float) -> SIMD2<Float>](/documentation/simd/max(_:_:)-35pzn)
- [func max(SIMD2<Float>, SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/max(_:_:)-9ye2a)
- [func fmax(SIMD2<Float>, SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/fmax(_:_:)-3cz61)
- [func simd_min(simd_float2, simd_float2) -> simd_float2](/documentation/simd/simd_min(_:_:)-9xyee)
- [func min(SIMD2<Float>, Float) -> SIMD2<Float>](/documentation/simd/min(_:_:)-3eaa2)
- [func min(SIMD2<Float>, SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/min(_:_:)-6cnnq)
- [func fmin(SIMD2<Float>, SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/fmin(_:_:)-7jupb)

### Reciprocal and Reciprocal Square Root Functions

- [func simd_recip(simd_float2) -> simd_float2](/documentation/simd/simd_recip(_:)-8nf6c)
- [func recip(SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/recip(_:)-2opi)
- [func simd_rsqrt(simd_float2) -> simd_float2](/documentation/simd/simd_rsqrt(_:)-okw0)
- [func rsqrt(SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/rsqrt(_:)-1er1q)
- [func simd_precise_recip(simd_float2) -> simd_float2](/documentation/simd/simd_precise_recip(_:)-66mt8)
- [func simd_precise_rsqrt(simd_float2) -> simd_float2](/documentation/simd/simd_precise_rsqrt(_:)-wqzu)
- [func simd_fast_recip(simd_float2) -> simd_float2](/documentation/simd/simd_fast_recip(_:)-ll5x)
- [func simd_fast_rsqrt(simd_float2) -> simd_float2](/documentation/simd/simd_fast_rsqrt(_:)-84cs6)

### Exponential and Logarithmic Functions

- [func exp(simd_float2) -> simd_float2](/documentation/simd/exp(_:)-3pa97)
- [func exp2(simd_float2) -> simd_float2](/documentation/simd/exp2(_:)-6sez2)
- [func exp10(simd_float2) -> simd_float2](/documentation/simd/exp10(_:)-6ga3o)
- [func expm1(simd_float2) -> simd_float2](/documentation/simd/expm1(_:)-3bqf9)
- [func log(simd_float2) -> simd_float2](/documentation/simd/log(_:)-1zfuo)
- [func log2(simd_float2) -> simd_float2](/documentation/simd/log2(_:)-8x5g)
- [func log10(simd_float2) -> simd_float2](/documentation/simd/log10(_:)-4yb6z)
- [func log1p(simd_float2) -> simd_float2](/documentation/simd/log1p(_:)-15zc7)

### Geometry Functions

- [func cross(SIMD2<Float>, SIMD2<Float>) -> SIMD3<Float>](/documentation/simd/cross(_:_:)-53xk2)
- [func dot(SIMD2<Float>, SIMD2<Float>) -> Float](/documentation/simd/dot(_:_:)-1vb5g)
- [func normalize(SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/normalize(_:)-100kb)
- [func project(SIMD2<Float>, SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/project(_:_:)-9wt83)
- [func reflect(SIMD2<Float>, n: SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/reflect(_:n:)-6w80i)
- [func refract(SIMD2<Float>, n: SIMD2<Float>, eta: Float) -> SIMD2<Float>](/documentation/simd/refract(_:n:eta:)-5bv79)

### Vector Norm Functions

- [func norm_one(SIMD2<Float>) -> Float](/documentation/simd/norm_one(_:)-2y0m)
- [func norm_inf(SIMD2<Float>) -> Float](/documentation/simd/norm_inf(_:)-9lj66)

### Length and Distance Functions

- [func length(SIMD2<Float>) -> Float](/documentation/simd/length(_:)-6g7q5)
- [func length_squared(SIMD2<Float>) -> Float](/documentation/simd/length_squared(_:)-6tcxv)
- [func distance(SIMD2<Float>, SIMD2<Float>) -> Float](/documentation/simd/distance(_:_:)-1p8ae)
- [func distance_squared(SIMD2<Float>, SIMD2<Float>) -> Float](/documentation/simd/distance_squared(_:_:)-9nmpe)

### Hyperbolic Functions

- [func acosh(simd_float2) -> simd_float2](/documentation/simd/acosh(_:)-16wup)
- [func asinh(simd_float2) -> simd_float2](/documentation/simd/asinh(_:)-14lj8)
- [func atanh(simd_float2) -> simd_float2](/documentation/simd/atanh(_:)-3o0hv)
- [func cosh(simd_float2) -> simd_float2](/documentation/simd/cosh(_:)-4n03p)
- [func sinh(simd_float2) -> simd_float2](/documentation/simd/sinh(_:)-2ft5c)
- [func tanh(simd_float2) -> simd_float2](/documentation/simd/tanh(_:)-8avnx)

### Logic Functions

- [func simd_select(simd_float2, simd_float2, simd_int2) -> simd_float2](/documentation/simd/simd_select(_:_:_:)-9jdc0)
- [func simd_bitselect(simd_float2, simd_float2, simd_int2) -> simd_float2](/documentation/simd/simd_bitselect(_:_:_:)-5g70k)

### Math Functions

- [func cbrt(simd_float2) -> simd_float2](/documentation/simd/cbrt(_:)-1t3k)
- [func ceil(SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/ceil(_:)-8j6zo)
- [func erf(simd_float2) -> simd_float2](/documentation/simd/erf(_:)-1unjp)
- [func erfc(simd_float2) -> simd_float2](/documentation/simd/erfc(_:)-1hisg)
- [func floor(SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/floor(_:)-1e9me)
- [func fma(simd_float2, simd_float2, simd_float2) -> simd_float2](/documentation/simd/fma(_:_:_:)-69k8u)
- [func fmod(simd_float2, simd_float2) -> simd_float2](/documentation/simd/fmod(_:_:)-566aw)
- [func hypot(simd_float2, simd_float2) -> simd_float2](/documentation/simd/hypot(_:_:)-1zs4i)
- [func lgamma(simd_float2) -> simd_float2](/documentation/simd/lgamma(_:)-1ksbv)
- [func nextafter(simd_float2, simd_float2) -> simd_float2](/documentation/simd/nextafter(_:_:)-8mat0)
- [func pow(simd_float2, simd_float2) -> simd_float2](/documentation/simd/pow(_:_:)-15e0y)
- [func remainder(simd_float2, simd_float2) -> simd_float2](/documentation/simd/remainder(_:_:)-37wwd)
- [func round(simd_float2) -> simd_float2](/documentation/simd/round(_:)-608of)
- [func simd_muladd(simd_float2, simd_float2, simd_float2) -> simd_float2](/documentation/simd/simd_muladd(_:_:_:)-45h2k)
- [func tgamma(simd_float2) -> simd_float2](/documentation/simd/tgamma(_:)-2aqvi)
- [func trunc(SIMD2<Float>) -> SIMD2<Float>](/documentation/simd/trunc(_:)-6neoe)

### Trigonometric Functions

- [func acos(simd_float2) -> simd_float2](/documentation/simd/acos(_:)-1ya4v)
- [func asin(simd_float2) -> simd_float2](/documentation/simd/asin(_:)-4tbvj)
- [func atan(simd_float2) -> simd_float2](/documentation/simd/atan(_:)-5v3x)
- [func atan2(simd_float2, simd_float2) -> simd_float2](/documentation/simd/atan2(_:_:)-4dpoz)
- [func cos(simd_float2) -> simd_float2](/documentation/simd/cos(_:)-59waa)
- [func cospi(simd_float2) -> simd_float2](/documentation/simd/cospi(_:)-2cd9u)
- [func sin(simd_float2) -> simd_float2](/documentation/simd/sin(_:)-5k8vo)
- [func sinpi(simd_float2) -> simd_float2](/documentation/simd/sinpi(_:)-524r6)
- [func sincos(simd_float2) -> (sin: simd_float2, cos: simd_float2)](/documentation/simd/sincos(_:)-4uhuq)
- [func sincospi(simd_float2) -> (sin: simd_float2, cos: simd_float2)](/documentation/simd/sincospi(_:)-11sii)
- [func tan(simd_float2) -> simd_float2](/documentation/simd/tan(_:)-4rx9f)
- [func tanpi(simd_float2) -> simd_float2](/documentation/simd/tanpi(_:)-3a1w1)

### Classification Functions

- [func isfinite(simd_float2) -> simd_int2](/documentation/simd/isfinite(_:)-zthr)
- [func isinf(simd_float2) -> simd_int2](/documentation/simd/isinf(_:)-9bb5h)
- [func isnan(simd_float2) -> simd_int2](/documentation/simd/isnan(_:)-7diw7)
- [func isnormal(simd_float2) -> simd_int2](/documentation/simd/isnormal(_:)-3n6dc)

### Alternative Type Alias

- [vector_float2](/documentation/simd/vector_float2)
- [float2](/documentation/simd/float2)
- [simd_float3](/documentation/simd/simd_float3)

### Functions to Create Three-Element Vectors From Other Vectors

- [func simd_make_float3(simd_float2) -> simd_float3](/documentation/simd/simd_make_float3(_:)-6jup1)
- [func simd_make_float3(simd_float3) -> simd_float3](/documentation/simd/simd_make_float3(_:)-6nare)
- [func simd_make_float3(simd_float4) -> simd_float3](/documentation/simd/simd_make_float3(_:)-759bf)
- [func simd_make_float3(simd_float8) -> simd_float3](/documentation/simd/simd_make_float3(_:)-7i06n)
- [func simd_make_float3(simd_float16) -> simd_float3](/documentation/simd/simd_make_float3(_:)-8p6oi)
- [func simd_make_float3_undef(simd_float2) -> simd_float3](/documentation/simd/simd_make_float3_undef(_:)-9aafs)

### Functions to Create Three-Element Vectors From Scalar Values

- [func simd_make_float3(Float) -> simd_float3](/documentation/simd/simd_make_float3(_:)-1lvzk)
- [func simd_make_float3(Float, Float, Float) -> simd_float3](/documentation/simd/simd_make_float3(_:_:_:))
- [func simd_make_float3_undef(Float) -> simd_float3](/documentation/simd/simd_make_float3_undef(_:)-4yqj8)

### Functions to Create Three-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_float3(Float, simd_float2) -> simd_float3](/documentation/simd/simd_make_float3(_:_:)-2ke7j)
- [func simd_make_float3(simd_float2, Float) -> simd_float3](/documentation/simd/simd_make_float3(_:_:)-57oga)

### Common Functions

- [func simd_abs(simd_float3) -> simd_float3](/documentation/simd/simd_abs(_:)-8dafp)
- [func abs(SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/abs(_:)-6lc19)
- [func simd_clamp(simd_float3, simd_float3, simd_float3) -> simd_float3](/documentation/simd/simd_clamp(_:_:_:)-5szev)
- [func clamp(SIMD3<Float>, min: Float, max: Float) -> SIMD3<Float>](/documentation/simd/clamp(_:min:max:)-3esdw)
- [func clamp(SIMD3<Float>, min: SIMD3<Float>, max: SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/clamp(_:min:max:)-9eeiz)
- [func simd_equal(simd_float3, simd_float3) -> simd_bool](/documentation/simd/simd_equal(_:_:)-6i7q4)
- [func fract(SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/fract(_:)-3rsxo)
- [func simd_fract(simd_float3) -> simd_float3](/documentation/simd/simd_fract(_:)-47mh4)
- [func simd_sign(simd_float3) -> simd_float3](/documentation/simd/simd_sign(_:)-6gp3q)
- [func sign(SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/sign(_:)-9p5uo)
- [func simd_step(simd_float3, simd_float3) -> simd_float3](/documentation/simd/simd_step(_:_:)-9ygnw)
- [func step(SIMD3<Float>, edge: SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/step(_:edge:)-48vbr)

### Reduce Functions

- [func simd_reduce_add(simd_float3) -> Float](/documentation/simd/simd_reduce_add(_:)-2v85p)
- [func reduce_add(SIMD3<Float>) -> Float](/documentation/simd/reduce_add(_:)-3xuqf)
- [func simd_reduce_max(simd_float3) -> Float](/documentation/simd/simd_reduce_max(_:)-4gy97)
- [func reduce_max(SIMD3<Float>) -> Float](/documentation/simd/reduce_max(_:)-1u3hn)
- [func simd_reduce_min(simd_float3) -> Float](/documentation/simd/simd_reduce_min(_:)-46cif)
- [func reduce_min(SIMD3<Float>) -> Float](/documentation/simd/reduce_min(_:)-3myvw)

### Interpolation Functions

- [func simd_mix(simd_float3, simd_float3, simd_float3) -> simd_float3](/documentation/simd/simd_mix(_:_:_:)-6l1x8)
- [func mix(SIMD3<Float>, SIMD3<Float>, t: Float) -> SIMD3<Float>](/documentation/simd/mix(_:_:t:)-9o58r)
- [func mix(SIMD3<Float>, SIMD3<Float>, t: SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/mix(_:_:t:)-6c4d3)
- [func simd_smoothstep(simd_float3, simd_float3, simd_float3) -> simd_float3](/documentation/simd/simd_smoothstep(_:_:_:)-mz0x)
- [func smoothstep(SIMD3<Float>, edge0: SIMD3<Float>, edge1: SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/smoothstep(_:edge0:edge1:)-6m76x)

### Extrema Functions

- [func simd_min(simd_float3, simd_float3) -> simd_float3](/documentation/simd/simd_min(_:_:)-9ccbp)
- [func min(SIMD3<Float>, Float) -> SIMD3<Float>](/documentation/simd/min(_:_:)-2xilk)
- [func min(SIMD3<Float>, SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/min(_:_:)-7cjgj)
- [func fmin(SIMD3<Float>, SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/fmin(_:_:)-6jyy2)
- [func simd_max(simd_float3, simd_float3) -> simd_float3](/documentation/simd/simd_max(_:_:)-6x53b)
- [func max(SIMD3<Float>, Float) -> SIMD3<Float>](/documentation/simd/max(_:_:)-27ore)
- [func max(SIMD3<Float>, SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/max(_:_:)-7plm)
- [func fmax(SIMD3<Float>, SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/fmax(_:_:)-1yseu)

### Reciprocal and Reciprocal Square Root Functions

- [func simd_recip(simd_float3) -> simd_float3](/documentation/simd/simd_recip(_:)-8jz2r)
- [func recip(SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/recip(_:)-8p7rb)
- [func simd_fast_recip(simd_float3) -> simd_float3](/documentation/simd/simd_fast_recip(_:)-ohgm)
- [func simd_precise_recip(simd_float3) -> simd_float3](/documentation/simd/simd_precise_recip(_:)-61j27)
- [func simd_rsqrt(simd_float3) -> simd_float3](/documentation/simd/simd_rsqrt(_:)-rh1j)
- [func rsqrt(SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/rsqrt(_:)-6peaq)
- [func simd_fast_rsqrt(simd_float3) -> simd_float3](/documentation/simd/simd_fast_rsqrt(_:)-80wq1)
- [func simd_precise_rsqrt(simd_float3) -> simd_float3](/documentation/simd/simd_precise_rsqrt(_:)-zs51)

### Exponential and Logarithmic Functions

- [func exp(simd_float3) -> simd_float3](/documentation/simd/exp(_:)-5nqcd)
- [func exp2(simd_float3) -> simd_float3](/documentation/simd/exp2(_:)-85hb2)
- [func exp10(simd_float3) -> simd_float3](/documentation/simd/exp10(_:)-6da66)
- [func expm1(simd_float3) -> simd_float3](/documentation/simd/expm1(_:)-2r6sd)
- [func log(simd_float3) -> simd_float3](/documentation/simd/log(_:)-3290g)
- [func log2(simd_float3) -> simd_float3](/documentation/simd/log2(_:)-5mgme)
- [func log10(simd_float3) -> simd_float3](/documentation/simd/log10(_:)-39t0j)
- [func log1p(simd_float3) -> simd_float3](/documentation/simd/log1p(_:)-25ya0)

### Geometry Functions

- [func cross(SIMD3<Float>, SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/cross(_:_:)-8xu8k)
- [func dot(SIMD3<Float>, SIMD3<Float>) -> Float](/documentation/simd/dot(_:_:)-4gb9g)
- [func normalize(SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/normalize(_:)-ac7)
- [func project(SIMD3<Float>, SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/project(_:_:)-9ggyv)
- [func reflect(SIMD3<Float>, n: SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/reflect(_:n:)-64cgz)
- [func refract(SIMD3<Float>, n: SIMD3<Float>, eta: Float) -> SIMD3<Float>](/documentation/simd/refract(_:n:eta:)-7jv66)

### Vector Norm Functions

- [func norm_one(SIMD3<Float>) -> Float](/documentation/simd/norm_one(_:)-7w7u6)
- [func norm_inf(SIMD3<Float>) -> Float](/documentation/simd/norm_inf(_:)-6o26q)

### Length and Distance Functions

- [func length(SIMD3<Float>) -> Float](/documentation/simd/length(_:)-6t47g)
- [func length_squared(SIMD3<Float>) -> Float](/documentation/simd/length_squared(_:)-8odp0)
- [func distance(SIMD3<Float>, SIMD3<Float>) -> Float](/documentation/simd/distance(_:_:)-8t6ut)
- [func distance_squared(SIMD3<Float>, SIMD3<Float>) -> Float](/documentation/simd/distance_squared(_:_:)-87jjy)

### Hyperbolic Functions

- [func acosh(simd_float3) -> simd_float3](/documentation/simd/acosh(_:)-48wtu)
- [func asinh(simd_float3) -> simd_float3](/documentation/simd/asinh(_:)-5c50h)
- [func atanh(simd_float3) -> simd_float3](/documentation/simd/atanh(_:)-1y6z5)
- [func cosh(simd_float3) -> simd_float3](/documentation/simd/cosh(_:)-4k02l)
- [func sinh(simd_float3) -> simd_float3](/documentation/simd/sinh(_:)-15g8v)
- [func tanh(simd_float3) -> simd_float3](/documentation/simd/tanh(_:)-4rx8s)

### Logic Functions

- [func simd_select(simd_float3, simd_float3, simd_int3) -> simd_float3](/documentation/simd/simd_select(_:_:_:)-9gbqb)
- [func simd_bitselect(simd_float3, simd_float3, simd_int3) -> simd_float3](/documentation/simd/simd_bitselect(_:_:_:)-5j5g8)

### Math Functions

- [func cbrt(simd_float3) -> simd_float3](/documentation/simd/cbrt(_:)-6vcwl)
- [func ceil(SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/ceil(_:)-580ar)
- [func erf(simd_float3) -> simd_float3](/documentation/simd/erf(_:)-2fow4)
- [func erfc(simd_float3) -> simd_float3](/documentation/simd/erfc(_:)-7e6kk)
- [func floor(SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/floor(_:)-50q1o)
- [func fma(simd_float3, simd_float3, simd_float3) -> simd_float3](/documentation/simd/fma(_:_:_:)-22bjf)
- [func fmod(simd_float3, simd_float3) -> simd_float3](/documentation/simd/fmod(_:_:)-3x8lc)
- [func hypot(simd_float3, simd_float3) -> simd_float3](/documentation/simd/hypot(_:_:)-4xggy)
- [func lgamma(simd_float3) -> simd_float3](/documentation/simd/lgamma(_:)-7kgzo)
- [func nextafter(simd_float3, simd_float3) -> simd_float3](/documentation/simd/nextafter(_:_:)-ymwd)
- [func pow(simd_float3, simd_float3) -> simd_float3](/documentation/simd/pow(_:_:)-65mb9)
- [func remainder(simd_float3, simd_float3) -> simd_float3](/documentation/simd/remainder(_:_:)-7ij10)
- [func round(simd_float3) -> simd_float3](/documentation/simd/round(_:)-1tl5h)
- [func simd_muladd(simd_float3, simd_float3, simd_float3) -> simd_float3](/documentation/simd/simd_muladd(_:_:_:)-8a66m)
- [func tgamma(simd_float3) -> simd_float3](/documentation/simd/tgamma(_:)-6difz)
- [func trunc(SIMD3<Float>) -> SIMD3<Float>](/documentation/simd/trunc(_:)-9byjt)

### Trigonometric Functions

- [func acos(simd_float3) -> simd_float3](/documentation/simd/acos(_:)-8bwml)
- [func asin(simd_float3) -> simd_float3](/documentation/simd/asin(_:)-5t22r)
- [func atan(simd_float3) -> simd_float3](/documentation/simd/atan(_:)-3otbw)
- [func atan2(simd_float3, simd_float3) -> simd_float3](/documentation/simd/atan2(_:_:)-40z9)
- [func cos(simd_float3) -> simd_float3](/documentation/simd/cos(_:)-2d0cu)
- [func cospi(simd_float3) -> simd_float3](/documentation/simd/cospi(_:)-1ceix)
- [func sin(simd_float3) -> simd_float3](/documentation/simd/sin(_:)-78r0i)
- [func sinpi(simd_float3) -> simd_float3](/documentation/simd/sinpi(_:)-99o27)
- [func sincos(simd_float3) -> (sin: simd_float3, cos: simd_float3)](/documentation/simd/sincos(_:)-3330)
- [func sincospi(simd_float3) -> (sin: simd_float3, cos: simd_float3)](/documentation/simd/sincospi(_:)-98kdl)
- [func tan(simd_float3) -> simd_float3](/documentation/simd/tan(_:)-yv9u)
- [func tanpi(simd_float3) -> simd_float3](/documentation/simd/tanpi(_:)-3lzzx)

### Classification Functions

- [func isfinite(simd_float3) -> simd_int3](/documentation/simd/isfinite(_:)-57mgu)
- [func isinf(simd_float3) -> simd_int3](/documentation/simd/isinf(_:)-7fd4p)
- [func isnan(simd_float3) -> simd_int3](/documentation/simd/isnan(_:)-j9kr)
- [func isnormal(simd_float3) -> simd_int3](/documentation/simd/isnormal(_:)-6f7tq)

### Alternative Type Alias

- [vector_float3](/documentation/simd/vector_float3)
- [float3](/documentation/simd/float3)
- [simd_float4](/documentation/simd/simd_float4)

### Functions to Create Four-Element Vectors From Other Vectors

- [func simd_make_float4(simd_float2) -> simd_float4](/documentation/simd/simd_make_float4(_:)-iuxp)
- [func simd_make_float4(simd_float3) -> simd_float4](/documentation/simd/simd_make_float4(_:)-fyse)
- [func simd_make_float4(simd_float4) -> simd_float4](/documentation/simd/simd_make_float4(_:)-cjxn)
- [func simd_make_float4(simd_float8) -> simd_float4](/documentation/simd/simd_make_float4(_:)-9xll2)
- [func simd_make_float4(simd_float16) -> simd_float4](/documentation/simd/simd_make_float4(_:)-5sesp)
- [func simd_make_float4(simd_float2, simd_float2) -> simd_float4](/documentation/simd/simd_make_float4(_:_:)-51w3j)
- [func simd_make_float4_undef(simd_float2) -> simd_float4](/documentation/simd/simd_make_float4_undef(_:)-3brs5)
- [func simd_make_float4_undef(simd_float3) -> simd_float4](/documentation/simd/simd_make_float4_undef(_:)-3f7tu)

### Functions to Create Four-Element Vectors From Scalar Values

- [func simd_make_float4(Float) -> simd_float4](/documentation/simd/simd_make_float4(_:)-2ja7v)
- [func simd_make_float4(Float, Float, Float, Float) -> simd_float4](/documentation/simd/simd_make_float4(_:_:_:_:))
- [func simd_make_float4_undef(Float) -> simd_float4](/documentation/simd/simd_make_float4_undef(_:)-24y7o)

### Functions to Create Four-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_float4(Float, simd_float2, Float) -> simd_float4](/documentation/simd/simd_make_float4(_:_:_:)-5qr1r)
- [func simd_make_float4(Float, Float, simd_float2) -> simd_float4](/documentation/simd/simd_make_float4(_:_:_:)-2rgt8)
- [func simd_make_float4(Float, simd_float3) -> simd_float4](/documentation/simd/simd_make_float4(_:_:)-9ngva)
- [func simd_make_float4(simd_float2, Float, Float) -> simd_float4](/documentation/simd/simd_make_float4(_:_:_:)-2bmi8)
- [func simd_make_float4(simd_float3, Float) -> simd_float4](/documentation/simd/simd_make_float4(_:_:)-4911p)

### Common Functions

- [func simd_abs(simd_float4) -> simd_float4](/documentation/simd/simd_abs(_:)-81qo8)
- [func abs(SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/abs(_:)-1fzhv)
- [func simd_clamp(simd_float4, simd_float4, simd_float4) -> simd_float4](/documentation/simd/simd_clamp(_:_:_:)-6vmhh)
- [func clamp(SIMD4<Float>, min: Float, max: Float) -> SIMD4<Float>](/documentation/simd/clamp(_:min:max:)-46ay6)
- [func clamp(SIMD4<Float>, min: SIMD4<Float>, max: SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/clamp(_:min:max:)-19q7w)
- [func simd_equal(simd_float4, simd_float4) -> simd_bool](/documentation/simd/simd_equal(_:_:)-6sa26)
- [func simd_fract(simd_float4) -> simd_float4](/documentation/simd/simd_fract(_:)-3w2rh)
- [func fract(SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/fract(_:)-9s3df)
- [func simd_sign(simd_float4) -> simd_float4](/documentation/simd/simd_sign(_:)-74zwz)
- [func sign(SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/sign(_:)-167c1)
- [func simd_step(simd_float4, simd_float4) -> simd_float4](/documentation/simd/simd_step(_:_:)-1fxwh)
- [func step(SIMD4<Float>, edge: SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/step(_:edge:)-8we4c)

### Reduce Functions

- [func simd_reduce_add(simd_float4) -> Float](/documentation/simd/simd_reduce_add(_:)-2yn18)
- [func reduce_add(SIMD4<Float>) -> Float](/documentation/simd/reduce_add(_:)-8m4ir)
- [func simd_reduce_max(simd_float4) -> Float](/documentation/simd/simd_reduce_max(_:)-4qug2)
- [func reduce_max(SIMD4<Float>) -> Float](/documentation/simd/reduce_max(_:)-263wv)
- [func simd_reduce_min(simd_float4) -> Float](/documentation/simd/simd_reduce_min(_:)-4un1u)
- [func reduce_min(SIMD4<Float>) -> Float](/documentation/simd/reduce_min(_:)-1xt53)

### Interpolation Functions

- [func simd_mix(simd_float4, simd_float4, simd_float4) -> simd_float4](/documentation/simd/simd_mix(_:_:_:)-5fpv1)
- [func mix(SIMD4<Float>, SIMD4<Float>, t: Float) -> SIMD4<Float>](/documentation/simd/mix(_:_:t:)-2uufx)
- [func mix(SIMD4<Float>, SIMD4<Float>, t: SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/mix(_:_:t:)-8qz2g)
- [func simd_smoothstep(simd_float4, simd_float4, simd_float4) -> simd_float4](/documentation/simd/simd_smoothstep(_:_:_:)-33ugy)
- [func smoothstep(SIMD4<Float>, edge0: SIMD4<Float>, edge1: SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/smoothstep(_:edge0:edge1:)-3gx0q)

### Extrema Functions

- [func simd_max(simd_float4, simd_float4) -> simd_float4](/documentation/simd/simd_max(_:_:)-3mrbf)
- [func max(SIMD4<Float>, Float) -> SIMD4<Float>](/documentation/simd/max(_:_:)-8mn3g)
- [func max(SIMD4<Float>, SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/max(_:_:)-317vz)
- [func fmax(SIMD4<Float>, SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/fmax(_:_:)-7f29b)
- [func simd_min(simd_float4, simd_float4) -> simd_float4](/documentation/simd/simd_min(_:_:)-6upge)
- [func min(SIMD4<Float>, Float) -> SIMD4<Float>](/documentation/simd/min(_:_:)-2jw3s)
- [func min(SIMD4<Float>, SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/min(_:_:)-7wmdr)
- [func fmin(SIMD4<Float>, SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/fmin(_:_:)-47ii0)

### Reciprocal and Reciprocal Square Root Functions

- [func simd_recip(simd_float4) -> simd_float4](/documentation/simd/simd_recip(_:)-820ma)
- [func recip(SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/recip(_:)-3idnw)
- [func simd_rsqrt(simd_float4) -> simd_float4](/documentation/simd/simd_rsqrt(_:)-i4we)
- [func rsqrt(SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/rsqrt(_:)-3g5ej)
- [func simd_precise_recip(simd_float4) -> simd_float4](/documentation/simd/simd_precise_recip(_:)-6ptoq)
- [func simd_precise_rsqrt(simd_float4) -> simd_float4](/documentation/simd/simd_precise_rsqrt(_:)-136xw)
- [func simd_fast_recip(simd_float4) -> simd_float4](/documentation/simd/simd_fast_recip(_:)-6nf)
- [func simd_fast_rsqrt(simd_float4) -> simd_float4](/documentation/simd/simd_fast_rsqrt(_:)-8p7fk)

### Exponential and Logarithmic Functions

- [func exp(simd_float4) -> simd_float4](/documentation/simd/exp(_:)-8lp9u)
- [func exp2(simd_float4) -> simd_float4](/documentation/simd/exp2(_:)-4tmv0)
- [func exp10(simd_float4) -> simd_float4](/documentation/simd/exp10(_:)-7ddho)
- [func expm1(simd_float4) -> simd_float4](/documentation/simd/expm1(_:)-4f45)
- [func log(simd_float4) -> simd_float4](/documentation/simd/log(_:)-259z1)
- [func log2(simd_float4) -> simd_float4](/documentation/simd/log2(_:)-5gt2x)
- [func log10(simd_float4) -> simd_float4](/documentation/simd/log10(_:)-2lowj)
- [func log1p(simd_float4) -> simd_float4](/documentation/simd/log1p(_:)-77wue)

### Geometry Functions

- [func dot(SIMD4<Float>, SIMD4<Float>) -> Float](/documentation/simd/dot(_:_:)-47df)
- [func normalize(SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/normalize(_:)-6g9xc)
- [func project(SIMD4<Float>, SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/project(_:_:)-pdsh)
- [func reflect(SIMD4<Float>, n: SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/reflect(_:n:)-8i5cc)
- [func refract(SIMD4<Float>, n: SIMD4<Float>, eta: Float) -> SIMD4<Float>](/documentation/simd/refract(_:n:eta:)-8qo9c)

### Vector Norm Functions

- [func norm_one(SIMD4<Float>) -> Float](/documentation/simd/norm_one(_:)-jo3r)
- [func norm_inf(SIMD4<Float>) -> Float](/documentation/simd/norm_inf(_:)-8tppa)

### Length and Distance Functions

- [func length(SIMD4<Float>) -> Float](/documentation/simd/length(_:)-9i1zg)
- [func length_squared(SIMD4<Float>) -> Float](/documentation/simd/length_squared(_:)-80gxf)
- [func distance(SIMD4<Float>, SIMD4<Float>) -> Float](/documentation/simd/distance(_:_:)-39uat)
- [func distance_squared(SIMD4<Float>, SIMD4<Float>) -> Float](/documentation/simd/distance_squared(_:_:)-32wfg)

### Hyperbolic Functions

- [func acosh(simd_float4) -> simd_float4](/documentation/simd/acosh(_:)-7sio6)
- [func asinh(simd_float4) -> simd_float4](/documentation/simd/asinh(_:)-693z8)
- [func atanh(simd_float4) -> simd_float4](/documentation/simd/atanh(_:)-48wed)
- [func cosh(simd_float4) -> simd_float4](/documentation/simd/cosh(_:)-5k3hp)
- [func sinh(simd_float4) -> simd_float4](/documentation/simd/sinh(_:)-4eoxy)
- [func tanh(simd_float4) -> simd_float4](/documentation/simd/tanh(_:)-9p88r)

### Logic Functions

- [func simd_select(simd_float4, simd_float4, simd_int4) -> simd_float4](/documentation/simd/simd_select(_:_:_:)-7vjx6)
- [func simd_bitselect(simd_float4, simd_float4, simd_int4) -> simd_float4](/documentation/simd/simd_bitselect(_:_:_:)-7g1os)

### Math Functions

- [func cbrt(simd_float4) -> simd_float4](/documentation/simd/cbrt(_:)-5wdps)
- [func ceil(SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/ceil(_:)-2omh0)
- [func erf(simd_float4) -> simd_float4](/documentation/simd/erf(_:)-4zsot)
- [func erfc(simd_float4) -> simd_float4](/documentation/simd/erfc(_:)-7acqr)
- [func floor(SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/floor(_:)-56de3)
- [func fma(simd_float4, simd_float4, simd_float4) -> simd_float4](/documentation/simd/fma(_:_:_:)-1zefy)
- [func fmod(simd_float4, simd_float4) -> simd_float4](/documentation/simd/fmod(_:_:)-px8m)
- [func hypot(simd_float4, simd_float4) -> simd_float4](/documentation/simd/hypot(_:_:)-96sjx)
- [func lgamma(simd_float4) -> simd_float4](/documentation/simd/lgamma(_:)-3l63e)
- [func nextafter(simd_float4, simd_float4) -> simd_float4](/documentation/simd/nextafter(_:_:)-6sc0p)
- [func pow(simd_float4, simd_float4) -> simd_float4](/documentation/simd/pow(_:_:)-skyu)
- [func remainder(simd_float4, simd_float4) -> simd_float4](/documentation/simd/remainder(_:_:)-7o61f)
- [func round(simd_float4) -> simd_float4](/documentation/simd/round(_:)-8vqnv)
- [func simd_muladd(simd_float4, simd_float4, simd_float4) -> simd_float4](/documentation/simd/simd_muladd(_:_:_:)-3e79w)
- [func tgamma(simd_float4) -> simd_float4](/documentation/simd/tgamma(_:)-twdo)
- [func trunc(SIMD4<Float>) -> SIMD4<Float>](/documentation/simd/trunc(_:)-4xiyl)

### Trigonometric Functions

- [func acos(simd_float4) -> simd_float4](/documentation/simd/acos(_:)-2blze)
- [func asin(simd_float4) -> simd_float4](/documentation/simd/asin(_:)-87ban)
- [func atan(simd_float4) -> simd_float4](/documentation/simd/atan(_:)-8xa90)
- [func atan2(simd_float4, simd_float4) -> simd_float4](/documentation/simd/atan2(_:_:)-63ije)
- [func cos(simd_float4) -> simd_float4](/documentation/simd/cos(_:)-8qcj2)
- [func cospi(simd_float4) -> simd_float4](/documentation/simd/cospi(_:)-5chnf)
- [func sin(simd_float4) -> simd_float4](/documentation/simd/sin(_:)-80x4)
- [func sinpi(simd_float4) -> simd_float4](/documentation/simd/sinpi(_:)-71xz)
- [func sincos(simd_float4) -> (sin: simd_float4, cos: simd_float4)](/documentation/simd/sincos(_:)-8bfn1)
- [func sincospi(simd_float4) -> (sin: simd_float4, cos: simd_float4)](/documentation/simd/sincospi(_:)-84wzt)
- [func tan(simd_float4) -> simd_float4](/documentation/simd/tan(_:)-7uvy9)
- [func tanpi(simd_float4) -> simd_float4](/documentation/simd/tanpi(_:)-93eul)

### Classification Functions

- [func isfinite(simd_float4) -> simd_int4](/documentation/simd/isfinite(_:)-96ccc)
- [func isinf(simd_float4) -> simd_int4](/documentation/simd/isinf(_:)-4hqza)
- [func isnan(simd_float4) -> simd_int4](/documentation/simd/isnan(_:)-9epap)
- [func isnormal(simd_float4) -> simd_int4](/documentation/simd/isnormal(_:)-7428z)

### Alternative Type Alias

- [vector_float4](/documentation/simd/vector_float4)
- [float4](/documentation/simd/float4)
- [simd_float8](/documentation/simd/simd_float8)

### Functions to Create Eight-Element Vectors From Other Vectors

- [func simd_make_float8(simd_float2) -> simd_float8](/documentation/simd/simd_make_float8(_:)-9l23p)
- [func simd_make_float8(simd_float3) -> simd_float8](/documentation/simd/simd_make_float8(_:)-9i5x2)
- [func simd_make_float8(simd_float4) -> simd_float8](/documentation/simd/simd_make_float8(_:)-6v9s)
- [func simd_make_float8(simd_float8) -> simd_float8](/documentation/simd/simd_make_float8(_:)-907gf)
- [func simd_make_float8(simd_float16) -> simd_float8](/documentation/simd/simd_make_float8(_:)-9z6aw)
- [func simd_make_float8(simd_float4, simd_float4) -> simd_float8](/documentation/simd/simd_make_float8(_:_:))
- [func simd_make_float8_undef(simd_float2) -> simd_float8](/documentation/simd/simd_make_float8_undef(_:)-9njgo)
- [func simd_make_float8_undef(simd_float3) -> simd_float8](/documentation/simd/simd_make_float8_undef(_:)-9qfif)
- [func simd_make_float8_undef(simd_float4) -> simd_float8](/documentation/simd/simd_make_float8_undef(_:)-8sol)

### Functions to Create Eight-Element Vectors From Scalar Values

- [func simd_make_float8(Float) -> simd_float8](/documentation/simd/simd_make_float8(_:)-6hx2j)
- [func simd_make_float8_undef(Float) -> simd_float8](/documentation/simd/simd_make_float8_undef(_:)-8cuk5)

### Common Functions

- [func simd_abs(simd_float8) -> simd_float8](/documentation/simd/simd_abs(_:)-7ozws)
- [func simd_clamp(simd_float8, simd_float8, simd_float8) -> simd_float8](/documentation/simd/simd_clamp(_:_:_:)-14mzm)
- [func simd_equal(simd_float8, simd_float8) -> simd_bool](/documentation/simd/simd_equal(_:_:)-7of37)
- [func simd_fract(simd_float8) -> simd_float8](/documentation/simd/simd_fract(_:)-3jbrt)
- [func simd_sign(simd_float8) -> simd_float8](/documentation/simd/simd_sign(_:)-7hbzz)
- [func simd_step(simd_float8, simd_float8) -> simd_float8](/documentation/simd/simd_step(_:_:)-96e50)

### Reduce Functions

- [func simd_reduce_min(simd_float8) -> Float](/documentation/simd/simd_reduce_min(_:)-3odum)
- [func simd_reduce_max(simd_float8) -> Float](/documentation/simd/simd_reduce_max(_:)-55e32)
- [func simd_reduce_add(simd_float8) -> Float](/documentation/simd/simd_reduce_add(_:)-3az3s)

### Interpolation Functions

- [func simd_smoothstep(simd_float8, simd_float8, simd_float8) -> simd_float8](/documentation/simd/simd_smoothstep(_:_:_:)-845yk)
- [func simd_mix(simd_float8, simd_float8, simd_float8) -> simd_float8](/documentation/simd/simd_mix(_:_:_:)-4c4kn)

### Extrema Functions

- [func simd_min(simd_float8, simd_float8) -> simd_float8](/documentation/simd/simd_min(_:_:)-7n539)
- [func simd_max(simd_float8, simd_float8) -> simd_float8](/documentation/simd/simd_max(_:_:)-6m7z0)

### Reciprocal and Reciprocal Square Root Functions

- [func simd_recip(simd_float8) -> simd_float8](/documentation/simd/simd_recip(_:)-989se)
- [func simd_fast_recip(simd_float8) -> simd_float8](/documentation/simd/simd_fast_recip(_:)-16fz3)
- [func simd_precise_recip(simd_float8) -> simd_float8](/documentation/simd/simd_precise_recip(_:)-74deu)
- [func simd_rsqrt(simd_float8) -> simd_float8](/documentation/simd/simd_rsqrt(_:)-1oj3u)
- [func simd_fast_rsqrt(simd_float8) -> simd_float8](/documentation/simd/simd_fast_rsqrt(_:)-923f0)
- [func simd_precise_rsqrt(simd_float8) -> simd_float8](/documentation/simd/simd_precise_rsqrt(_:)-1hqkg)

### Exponential and Logarithmic Functions

- [func exp(simd_float8) -> simd_float8](/documentation/simd/exp(_:)-1pg0i)
- [func exp2(simd_float8) -> simd_float8](/documentation/simd/exp2(_:)-1n4s0)
- [func exp10(simd_float8) -> simd_float8](/documentation/simd/exp10(_:)-8kkzs)
- [func expm1(simd_float8) -> simd_float8](/documentation/simd/expm1(_:)-70odp)
- [func log(simd_float8) -> simd_float8](/documentation/simd/log(_:)-5bs8h)
- [func log2(simd_float8) -> simd_float8](/documentation/simd/log2(_:)-939d1)
- [func log10(simd_float8) -> simd_float8](/documentation/simd/log10(_:)-94fwu)
- [func log1p(simd_float8) -> simd_float8](/documentation/simd/log1p(_:)-7f7d8)

### Hyperbolic Functions

- [func acosh(simd_float8) -> simd_float8](/documentation/simd/acosh(_:)-5ye64)
- [func asinh(simd_float8) -> simd_float8](/documentation/simd/asinh(_:)-1uw5q)
- [func atanh(simd_float8) -> simd_float8](/documentation/simd/atanh(_:)-95265)
- [func cosh(simd_float8) -> simd_float8](/documentation/simd/cosh(_:)-6rb1l)
- [func sinh(simd_float8) -> simd_float8](/documentation/simd/sinh(_:)-43ijd)
- [func tanh(simd_float8) -> simd_float8](/documentation/simd/tanh(_:)-tpg5)

### Logic Functions

- [func simd_select(simd_float8, simd_float8, simd_int8) -> simd_float8](/documentation/simd/simd_select(_:_:_:)-5h243)
- [func simd_bitselect(simd_float8, simd_float8, simd_int8) -> simd_float8](/documentation/simd/simd_bitselect(_:_:_:)-66uzh)

### Math Functions

- [func cbrt(simd_float8) -> simd_float8](/documentation/simd/cbrt(_:)-3f2k2)
- [func erf(simd_float8) -> simd_float8](/documentation/simd/erf(_:)-5vzab)
- [func erfc(simd_float8) -> simd_float8](/documentation/simd/erfc(_:)-1csse)
- [func fma(simd_float8, simd_float8, simd_float8) -> simd_float8](/documentation/simd/fma(_:_:_:)-49crk)
- [func fmod(simd_float8, simd_float8) -> simd_float8](/documentation/simd/fmod(_:_:)-8fmuq)
- [func hypot(simd_float8, simd_float8) -> simd_float8](/documentation/simd/hypot(_:_:)-47t8e)
- [func lgamma(simd_float8) -> simd_float8](/documentation/simd/lgamma(_:)-9g2rk)
- [func nextafter(simd_float8, simd_float8) -> simd_float8](/documentation/simd/nextafter(_:_:)-sc7d)
- [func pow(simd_float8, simd_float8) -> simd_float8](/documentation/simd/pow(_:_:)-nk2t)
- [func remainder(simd_float8, simd_float8) -> simd_float8](/documentation/simd/remainder(_:_:)-7l2wd)
- [func round(simd_float8) -> simd_float8](/documentation/simd/round(_:)-1ffcx)
- [func simd_muladd(simd_float8, simd_float8, simd_float8) -> simd_float8](/documentation/simd/simd_muladd(_:_:_:)-3v5t5)
- [func tgamma(simd_float8) -> simd_float8](/documentation/simd/tgamma(_:)-6tafl)

### Trigonometric Functions

- [func acos(simd_float8) -> simd_float8](/documentation/simd/acos(_:)-7zw9c)
- [func asin(simd_float8) -> simd_float8](/documentation/simd/asin(_:)-476k0)
- [func atan(simd_float8) -> simd_float8](/documentation/simd/atan(_:)-al43)
- [func atan2(simd_float8, simd_float8) -> simd_float8](/documentation/simd/atan2(_:_:)-52zvp)
- [func cos(simd_float8) -> simd_float8](/documentation/simd/cos(_:)-6spt8)
- [func cospi(simd_float8) -> simd_float8](/documentation/simd/cospi(_:)-mwoe)
- [func sin(simd_float8) -> simd_float8](/documentation/simd/sin(_:)-8n720)
- [func sinpi(simd_float8) -> simd_float8](/documentation/simd/sinpi(_:)-5sfds)
- [func sincos(simd_float8) -> (sin: simd_float8, cos: simd_float8)](/documentation/simd/sincos(_:)-26uzx)
- [func sincospi(simd_float8) -> (sin: simd_float8, cos: simd_float8)](/documentation/simd/sincospi(_:)-3cme4)
- [func tan(simd_float8) -> simd_float8](/documentation/simd/tan(_:)-6t9p5)
- [func tanpi(simd_float8) -> simd_float8](/documentation/simd/tanpi(_:)-5w53i)

### Classification Functions

- [func isfinite(simd_float8) -> simd_int8](/documentation/simd/isfinite(_:)-285ek)
- [func isinf(simd_float8) -> simd_int8](/documentation/simd/isinf(_:)-9ud2k)
- [func isnan(simd_float8) -> simd_int8](/documentation/simd/isnan(_:)-8blhp)
- [func isnormal(simd_float8) -> simd_int8](/documentation/simd/isnormal(_:)-36pn2)

### Alternative Type Alias

- [vector_float8](/documentation/simd/vector_float8)
- [simd_half1](/documentation/simd/simd_half1)

### Common functions

- [func simd_clamp(Float16, Float16, Float16) -> Float16](/documentation/simd/simd_clamp(_:_:_:)-c4d6)
- [func simd_fract(Float16) -> Float16](/documentation/simd/simd_fract(_:)-1wwew)
- [func simd_sign(Float16) -> Float16](/documentation/simd/simd_sign(_:)-9365i)
- [func simd_step(Float16, Float16) -> Float16](/documentation/simd/simd_step(_:_:)-u24h)

### Interpolation functions

- [func simd_mix(Float16, Float16, Float16) -> Float16](/documentation/simd/simd_mix(_:_:_:)-3mcrj)
- [func simd_smoothstep(Float16, Float16, Float16) -> Float16](/documentation/simd/simd_smoothstep(_:_:_:)-6zp30)

### Extrema functions

- [func simd_max(Float16, Float16) -> Float16](/documentation/simd/simd_max(_:_:)-3f8z7)
- [func simd_min(Float16, Float16) -> Float16](/documentation/simd/simd_min(_:_:)-57wqc)

### Reciprocal and reciprocal square root functions

- [func simd_recip(Float16) -> Float16](/documentation/simd/simd_recip(_:)-7yi5r)
- [func simd_rsqrt(Float16) -> Float16](/documentation/simd/simd_rsqrt(_:)-4yfi0)
- [func simd_precise_recip(Float16) -> Float16](/documentation/simd/simd_precise_recip(_:)-6q9sp)
- [func simd_precise_rsqrt(Float16) -> Float16](/documentation/simd/simd_precise_rsqrt(_:)-5fjxk)
- [func simd_fast_recip(Float16) -> Float16](/documentation/simd/simd_fast_recip(_:)-1ibu)
- [func simd_fast_rsqrt(Float16) -> Float16](/documentation/simd/simd_fast_rsqrt(_:)-43sls)

### Math functions

- [func simd_muladd(Float16, Float16, Float16) -> Float16](/documentation/simd/simd_muladd(_:_:_:)-41x8n)
- [simd_half16](/documentation/simd/simd_half16)

### Functions to create 16-element vectors from other vectors

- [func simd_make_half16(simd_half2) -> simd_half16](/documentation/simd/simd_make_half16(_:)-7jegv)
- [func simd_make_half16(simd_half3) -> simd_half16](/documentation/simd/simd_make_half16(_:)-7fwvg)
- [func simd_make_half16(simd_half4) -> simd_half16](/documentation/simd/simd_make_half16(_:)-7czq5)
- [func simd_make_half16(simd_half8) -> simd_half16](/documentation/simd/simd_make_half16(_:)-8jb49)
- [func simd_make_half16(simd_half16) -> simd_half16](/documentation/simd/simd_make_half16(_:)-2eeq3)
- [func simd_make_half16(simd_half32) -> simd_half16](/documentation/simd/simd_make_half16(_:)-18zo3)
- [func simd_make_half16_undef(simd_half2) -> simd_half16](/documentation/simd/simd_make_half16_undef(_:)-nn1z)
- [func simd_make_half16_undef(simd_half3) -> simd_half16](/documentation/simd/simd_make_half16_undef(_:)-qkco)
- [func simd_make_half16_undef(simd_half4) -> simd_half16](/documentation/simd/simd_make_half16_undef(_:)-hd79)
- [func simd_make_half16_undef(simd_half8) -> simd_half16](/documentation/simd/simd_make_half16_undef(_:)-1lcb5)
- [func simd_make_half16(simd_half8, simd_half8) -> simd_half16](/documentation/simd/simd_make_half16(_:_:))

### Functions to create 16-element vectors from scalar values

- [func simd_make_half16(Float16) -> simd_half16](/documentation/simd/simd_make_half16(_:)-923w5)
- [func simd_make_half16_undef(Float16) -> simd_half16](/documentation/simd/simd_make_half16_undef(_:)-5x8m)

### Common functions

- [func simd_abs(simd_half16) -> simd_half16](/documentation/simd/simd_abs(_:)-47hrc)
- [func simd_clamp(simd_int16, simd_int16, simd_int16) -> simd_int16](/documentation/simd/simd_clamp(_:_:_:)-5xcny)
- [func simd_equal(simd_half16, simd_half16) -> simd_bool](/documentation/simd/simd_equal(_:_:)-9ijsx)
- [func simd_fract(simd_half16) -> simd_half16](/documentation/simd/simd_fract(_:)-6v27d)
- [func simd_sign(simd_half16) -> simd_half16](/documentation/simd/simd_sign(_:)-tcn7)
- [func simd_step(simd_half16, simd_half16) -> simd_half16](/documentation/simd/simd_step(_:_:)-7ryeb)

### Reduce functions

- [func simd_reduce_add(simd_half16) -> Float16](/documentation/simd/simd_reduce_add(_:)-7n2m4)
- [func simd_reduce_max(simd_half16) -> Float16](/documentation/simd/simd_reduce_max(_:)-8iq8z)
- [func simd_reduce_min(simd_half16) -> Float16](/documentation/simd/simd_reduce_min(_:)-3cxx5)

### Interpolation functions

- [func simd_mix(simd_half16, simd_half16, simd_half16) -> simd_half16](/documentation/simd/simd_mix(_:_:_:)-7hbla)
- [func simd_smoothstep(simd_half16, simd_half16, simd_half16) -> simd_half16](/documentation/simd/simd_smoothstep(_:_:_:)-4twuq)

### Extrema functions

- [func simd_max(simd_half16, simd_half16) -> simd_half16](/documentation/simd/simd_max(_:_:)-9p9g1)
- [func simd_min(simd_half16, simd_half16) -> simd_half16](/documentation/simd/simd_min(_:_:)-4gxfx)

### Reciprocal and reciprocal square root functions

- [func simd_recip(simd_half16) -> simd_half16](/documentation/simd/simd_recip(_:)-5bvrv)
- [func simd_rsqrt(simd_half16) -> simd_half16](/documentation/simd/simd_rsqrt(_:)-765rp)
- [func simd_precise_recip(simd_half16) -> simd_half16](/documentation/simd/simd_precise_recip(_:)-5icut)
- [func simd_precise_rsqrt(simd_half16) -> simd_half16](/documentation/simd/simd_precise_rsqrt(_:)-6j2jj)
- [func simd_fast_recip(simd_half16) -> simd_half16](/documentation/simd/simd_fast_recip(_:)-mw6p)
- [func simd_fast_rsqrt(simd_half16) -> simd_half16](/documentation/simd/simd_fast_rsqrt(_:)-686mo)

### Logic functions

- [func simd_select(simd_half16, simd_half16, simd_short16) -> simd_half16](/documentation/simd/simd_select(_:_:_:)-7d7xj)
- [func simd_bitselect(simd_half16, simd_half16, simd_short16) -> simd_half16](/documentation/simd/simd_bitselect(_:_:_:)-92kfc)

### Math functions

- [func simd_muladd(simd_half16, simd_half16, simd_half16) -> simd_half16](/documentation/simd/simd_muladd(_:_:_:)-8bkab)
- [simd_half2](/documentation/simd/simd_half2)

### Functions to create two-element vectors from other vectors

- [func simd_make_half2(simd_half2) -> simd_half2](/documentation/simd/simd_make_half2(_:)-1857c)
- [func simd_make_half2(simd_half3) -> simd_half2](/documentation/simd/simd_make_half2(_:)-1b2kr)
- [func simd_make_half2(simd_half4) -> simd_half2](/documentation/simd/simd_make_half2(_:)-1t11m)
- [func simd_make_half2(simd_half8) -> simd_half2](/documentation/simd/simd_make_half2(_:)-27x5a)
- [func simd_make_half2(simd_half16) -> simd_half2](/documentation/simd/simd_make_half2(_:)-9auhj)
- [func simd_make_half2(simd_half32) -> simd_half2](/documentation/simd/simd_make_half2(_:)-4bzdr)

### Functions to create two-element vectors from scalar values

- [func simd_make_half2(Float16) -> simd_half2](/documentation/simd/simd_make_half2(_:)-9q31)
- [func simd_make_half2(Float16, Float16) -> simd_half2](/documentation/simd/simd_make_half2(_:_:))
- [func simd_make_half2_undef(Float16) -> simd_half2](/documentation/simd/simd_make_half2_undef(_:))

### Common functions

- [func simd_abs(simd_half2) -> simd_half2](/documentation/simd/simd_abs(_:)-889zu)
- [func simd_clamp(simd_half2, simd_half2, simd_half2) -> simd_half2](/documentation/simd/simd_clamp(_:_:_:)-8crce)
- [func simd_equal(simd_half2, simd_half2) -> simd_bool](/documentation/simd/simd_equal(_:_:)-6mu96)
- [func simd_fract(simd_half2) -> simd_half2](/documentation/simd/simd_fract(_:)-42lx3)
- [func simd_sign(simd_half2) -> simd_half2](/documentation/simd/simd_sign(_:)-6jn8t)
- [func simd_step(simd_half2, simd_half2) -> simd_half2](/documentation/simd/simd_step(_:_:)-4dqzp)

### Reduce functions

- [func simd_reduce_add(simd_half2) -> Float16](/documentation/simd/simd_reduce_add(_:)-2q3zq)
- [func simd_reduce_max(simd_half2) -> Float16](/documentation/simd/simd_reduce_max(_:)-4kf4c)
- [func simd_reduce_min(simd_half2) -> Float16](/documentation/simd/simd_reduce_min(_:)-49pb0)

### Interpolation functions

- [func simd_mix(simd_half2, simd_half2, simd_half2) -> simd_half2](/documentation/simd/simd_mix(_:_:_:)-33iiq)
- [func simd_smoothstep(simd_half2, simd_half2, simd_half2) -> simd_half2](/documentation/simd/simd_smoothstep(_:_:_:)-9x0u5)

### Extrema functions

- [func simd_max(simd_half2, simd_half2) -> simd_half2](/documentation/simd/simd_max(_:_:)-3wsb8)
- [func simd_min(simd_half2, simd_half2) -> simd_half2](/documentation/simd/simd_min(_:_:)-6mo5o)

### Reciprocal and reciprocal square root functions

- [func simd_recip(simd_half2) -> simd_half2](/documentation/simd/simd_recip(_:)-8ni98)
- [func simd_rsqrt(simd_half2) -> simd_half2](/documentation/simd/simd_rsqrt(_:)-oj14)
- [func simd_precise_recip(simd_half2) -> simd_half2](/documentation/simd/simd_precise_recip(_:)-66ohg)
- [func simd_precise_rsqrt(simd_half2) -> simd_half2](/documentation/simd/simd_precise_rsqrt(_:)-wvby)
- [func simd_fast_recip(simd_half2) -> simd_half2](/documentation/simd/simd_fast_recip(_:)-ln7x)
- [func simd_fast_rsqrt(simd_half2) -> simd_half2](/documentation/simd/simd_fast_rsqrt(_:)-84ema)

### Logic functions

- [func simd_select(simd_half2, simd_half2, simd_short2) -> simd_half2](/documentation/simd/simd_select(_:_:_:)-472ze)
- [func simd_bitselect(simd_half2, simd_half2, simd_short2) -> simd_half2](/documentation/simd/simd_bitselect(_:_:_:)-3g1i8)

### Math functions

- [func simd_muladd(simd_half2, simd_half2, simd_half2) -> simd_half2](/documentation/simd/simd_muladd(_:_:_:)-30k16)
- [simd_half3](/documentation/simd/simd_half3)

### Functions to create three-element vectors from other vectors

- [func simd_make_half3(simd_half2) -> simd_half3](/documentation/simd/simd_make_half3(_:)-52gdy)
- [func simd_make_half3(simd_half3) -> simd_half3](/documentation/simd/simd_make_half3(_:)-4yz0x)
- [func simd_make_half3(simd_half4) -> simd_half3](/documentation/simd/simd_make_half3(_:)-4h0kc)
- [func simd_make_half3(simd_half8) -> simd_half3](/documentation/simd/simd_make_half3(_:)-5nca0)
- [func simd_make_half3(simd_half16) -> simd_half3](/documentation/simd/simd_make_half3(_:)-9063q)
- [func simd_make_half3(simd_half32) -> simd_half3](/documentation/simd/simd_make_half3(_:)-64v1)
- [func simd_make_half3_undef(simd_half2) -> simd_half3](/documentation/simd/simd_make_half3_undef(_:)-1frd1)

### Functions to create three-element vectors from scalar values

- [func simd_make_half3(Float16) -> simd_half3](/documentation/simd/simd_make_half3(_:)-9gqvo)
- [func simd_make_half3(Float16, Float16, Float16) -> simd_half3](/documentation/simd/simd_make_half3(_:_:_:))
- [func simd_make_half3(simd_half2, Float16) -> simd_half3](/documentation/simd/simd_make_half3(_:_:)-5wwpl)
- [func simd_make_half3(Float16, simd_half2) -> simd_half3](/documentation/simd/simd_make_half3(_:_:)-4svq0)
- [func simd_make_half3_undef(Float16) -> simd_half3](/documentation/simd/simd_make_half3_undef(_:)-6lcqp)

### Common functions

- [func simd_abs(simd_half3) -> simd_half3](/documentation/simd/simd_abs(_:)-8derx)
- [func simd_clamp(simd_half3, simd_half3, simd_half3) -> simd_half3](/documentation/simd/simd_clamp(_:_:_:)-2h8ov)
- [func simd_equal(simd_half3, simd_half3) -> simd_bool](/documentation/simd/simd_equal(_:_:)-9k8m9)
- [func simd_fract(simd_half3) -> simd_half3](/documentation/simd/simd_fract(_:)-47quw)
- [func simd_sign(simd_half3) -> simd_half3](/documentation/simd/simd_sign(_:)-6gppu)
- [func simd_step(simd_half3, simd_half3) -> simd_half3](/documentation/simd/simd_step(_:_:)-8w7e)

### Reduce functions

- [func simd_reduce_add(simd_half3) -> Float16](/documentation/simd/simd_reduce_add(_:)-2v3th)
- [func simd_reduce_max(simd_half3) -> Float16](/documentation/simd/simd_reduce_max(_:)-4h2m7)
- [func simd_reduce_min(simd_half3) -> Float16](/documentation/simd/simd_reduce_min(_:)-4685v)

### Interpolation functions

- [func simd_mix(simd_half3, simd_half3, simd_half3) -> simd_half3](/documentation/simd/simd_mix(_:_:_:)-4co2a)
- [func simd_smoothstep(simd_half3, simd_half3, simd_half3) -> simd_half3](/documentation/simd/simd_smoothstep(_:_:_:)-4rnii)

### Extrema functions

- [func simd_max(simd_half3, simd_half3) -> simd_half3](/documentation/simd/simd_max(_:_:)-1g1g7)
- [func simd_min(simd_half3, simd_half3) -> simd_half3](/documentation/simd/simd_min(_:_:)-4rmyw)

### Reciprocal and reciprocal square root functions

- [func simd_recip(simd_half3) -> simd_half3](/documentation/simd/simd_recip(_:)-8k0yn)
- [func simd_rsqrt(simd_half3) -> simd_half3](/documentation/simd/simd_rsqrt(_:)-rgh7)
- [func simd_precise_recip(simd_half3) -> simd_half3](/documentation/simd/simd_precise_recip(_:)-61jmz)
- [func simd_precise_rsqrt(simd_half3) -> simd_half3](/documentation/simd/simd_precise_rsqrt(_:)-znwt)
- [func simd_fast_recip(simd_half3) -> simd_half3](/documentation/simd/simd_fast_recip(_:)-okeq)
- [func simd_fast_rsqrt(simd_half3) -> simd_half3](/documentation/simd/simd_fast_rsqrt(_:)-80xc1)

### Logic functions

- [func simd_select(simd_half3, simd_half3, simd_short3) -> simd_half3](/documentation/simd/simd_select(_:_:_:)-2ljkl)
- [func simd_bitselect(simd_half3, simd_half3, simd_short3) -> simd_half3](/documentation/simd/simd_bitselect(_:_:_:)-6ne9u)

### Math functions

- [func simd_muladd(simd_half3, simd_half3, simd_half3) -> simd_half3](/documentation/simd/simd_muladd(_:_:_:)-582ze)
- [simd_half32](/documentation/simd/simd_half32)

### Functions to create 32-element vectors from other vectors

- [func simd_make_half32(simd_half2) -> simd_half32](/documentation/simd/simd_make_half32(_:)-8obpe)
- [func simd_make_half32(simd_half3) -> simd_half32](/documentation/simd/simd_make_half32(_:)-8kum5)
- [func simd_make_half32(simd_half4) -> simd_half32](/documentation/simd/simd_make_half32(_:)-82w1c)
- [func simd_make_half32(simd_half8) -> simd_half32](/documentation/simd/simd_make_half32(_:)-997h0)
- [func simd_make_half32(simd_half16) -> simd_half32](/documentation/simd/simd_make_half32(_:)-6xe53)
- [func simd_make_half32(simd_half32) -> simd_half32](/documentation/simd/simd_make_half32(_:)-80qof)
- [func simd_make_half32_undef(simd_half2) -> simd_half32](/documentation/simd/simd_make_half32_undef(_:)-3w7jb)
- [func simd_make_half32_undef(simd_half3) -> simd_half32](/documentation/simd/simd_make_half32_undef(_:)-3yzwk)
- [func simd_make_half32_undef(simd_half4) -> simd_half32](/documentation/simd/simd_make_half32_undef(_:)-42h8l)
- [func simd_make_half32_undef(simd_half8) -> simd_half32](/documentation/simd/simd_make_half32_undef(_:)-4gyi9)
- [func simd_make_half32_undef(simd_half16) -> simd_half32](/documentation/simd/simd_make_half32_undef(_:)-9hc0w)
- [func simd_make_half32(simd_half16, simd_half16) -> simd_half32](/documentation/simd/simd_make_half32(_:_:))

### Functions to create 32-element vectors from scalar values

- [func simd_make_half32(Float16) -> simd_half32](/documentation/simd/simd_make_half32(_:)-4hl1s)
- [func simd_make_half32_undef(Float16) -> simd_half32](/documentation/simd/simd_make_half32_undef(_:)-65xeg)

### Common functions

- [func simd_abs(simd_half32) -> simd_half32](/documentation/simd/simd_abs(_:)-2byol)
- [func simd_clamp(simd_half32, simd_half32, simd_half32) -> simd_half32](/documentation/simd/simd_clamp(_:_:_:)-868pk)
- [func simd_equal(simd_half32, simd_half32) -> simd_bool](/documentation/simd/simd_equal(_:_:)-5620v)
- [func simd_fract(simd_half32) -> simd_half32](/documentation/simd/simd_fract(_:)-4zj0y)
- [func simd_sign(simd_half32) -> simd_half32](/documentation/simd/simd_sign(_:)-9r24j)
- [func simd_step(simd_half32, simd_half32) -> simd_half32](/documentation/simd/simd_step(_:_:)-2kbac)

### Reduce functions

- [func simd_reduce_add(simd_half32) -> Float16](/documentation/simd/simd_reduce_add(_:)-1urk1)
- [func simd_reduce_max(simd_half32) -> Float16](/documentation/simd/simd_reduce_max(_:)-9itok)
- [func simd_reduce_min(simd_half32) -> Float16](/documentation/simd/simd_reduce_min(_:)-2b1zw)

### Interpolation functions

- [func simd_mix(simd_half32, simd_half32, simd_half32) -> simd_half32](/documentation/simd/simd_mix(_:_:_:)-4qwly)
- [func simd_smoothstep(simd_half32, simd_half32, simd_half32) -> simd_half32](/documentation/simd/simd_smoothstep(_:_:_:)-6nnf0)

### Extrema functions

- [func simd_max(simd_half32, simd_half32) -> simd_half32](/documentation/simd/simd_max(_:_:)-2y7nk)
- [func simd_min(simd_half32, simd_half32) -> simd_half32](/documentation/simd/simd_min(_:_:)-10jj2)

### Reciprocal and reciprocal square root functions

- [func simd_recip(simd_half32) -> simd_half32](/documentation/simd/simd_recip(_:)-6hfwj)
- [func simd_rsqrt(simd_half32) -> simd_half32](/documentation/simd/simd_rsqrt(_:)-60bll)
- [func simd_precise_recip(simd_half32) -> simd_half32](/documentation/simd/simd_precise_recip(_:)-22hxl)
- [func simd_precise_rsqrt(simd_half32) -> simd_half32](/documentation/simd/simd_precise_rsqrt(_:)-8ce7i)
- [func simd_fast_recip(simd_half32) -> simd_half32](/documentation/simd/simd_fast_recip(_:)-2i3al)
- [func simd_fast_rsqrt(simd_half32) -> simd_half32](/documentation/simd/simd_fast_rsqrt(_:)-2sbqs)

### Logic functions

- [func simd_select(simd_half32, simd_half32, simd_short32) -> simd_half32](/documentation/simd/simd_select(_:_:_:)-63scw)
- [func simd_bitselect(simd_half32, simd_half32, simd_short32) -> simd_half32](/documentation/simd/simd_bitselect(_:_:_:)-81xk8)

### Math functions

- [func simd_muladd(simd_half32, simd_half32, simd_half32) -> simd_half32](/documentation/simd/simd_muladd(_:_:_:)-bf1p)
- [simd_half4](/documentation/simd/simd_half4)

### Functions to create four-element vectors from other vectors

- [func simd_make_half4(simd_half2) -> simd_half4](/documentation/simd/simd_make_half4(_:)-fx5r)
- [func simd_make_half4(simd_half3) -> simd_half4](/documentation/simd/simd_make_half4(_:)-iuj0)
- [func simd_make_half4(simd_half4) -> simd_half4](/documentation/simd/simd_make_half4(_:)-9u2ra)
- [func simd_make_half4(simd_half8) -> simd_half4](/documentation/simd/simd_make_half4(_:)-10t2p)
- [func simd_make_half4(simd_half16) -> simd_half4](/documentation/simd/simd_make_half4(_:)-43737)
- [func simd_make_half4(simd_half32) -> simd_half4](/documentation/simd/simd_make_half4(_:)-60ltf)
- [func simd_make_half4(simd_half2, simd_half2) -> simd_half4](/documentation/simd/simd_make_half4(_:_:)-2ea2z)
- [func simd_make_half4_undef(simd_half2) -> simd_half4](/documentation/simd/simd_make_half4_undef(_:)-16ipv)
- [func simd_make_half4_undef(simd_half3) -> simd_half4](/documentation/simd/simd_make_half4_undef(_:)-136jo)

### Functions to create four-element vectors from scalar values

- [func simd_make_half4(Float16) -> simd_half4](/documentation/simd/simd_make_half4(_:)-6lkh9)
- [func simd_make_half4(Float16, Float16, Float16, Float16) -> simd_half4](/documentation/simd/simd_make_half4(_:_:_:_:))
- [func simd_make_half4_undef(Float16) -> simd_half4](/documentation/simd/simd_make_half4_undef(_:)-4axzi)
- [func simd_make_half4(Float16, simd_half3) -> simd_half4](/documentation/simd/simd_make_half4(_:_:)-2n13g)
- [func simd_make_half4(simd_half3, Float16) -> simd_half4](/documentation/simd/simd_make_half4(_:_:)-6uygn)
- [func simd_make_half4(Float16, simd_half2, Float16) -> simd_half4](/documentation/simd/simd_make_half4(_:_:_:)-43wuv)
- [func simd_make_half4(Float16, Float16, simd_half2) -> simd_half4](/documentation/simd/simd_make_half4(_:_:_:)-74ybg)
- [func simd_make_half4(simd_half2, Float16, Float16) -> simd_half4](/documentation/simd/simd_make_half4(_:_:_:)-6g0kb)

### Common functions

- [func simd_abs(simd_half4) -> simd_half4](/documentation/simd/simd_abs(_:)-81q3k)
- [func simd_clamp(simd_half4, simd_half4, simd_half4) -> simd_half4](/documentation/simd/simd_clamp(_:_:_:)-2vvpa)
- [func simd_equal(simd_half4, simd_half4) -> simd_bool](/documentation/simd/simd_equal(_:_:)-6nuuw)
- [func simd_fract(simd_half4) -> simd_half4](/documentation/simd/simd_fract(_:)-3w251)
- [func simd_sign(simd_half4) -> simd_half4](/documentation/simd/simd_sign(_:)-7533b)
- [func simd_step(simd_half4, simd_half4) -> simd_half4](/documentation/simd/simd_step(_:_:)-4knqw)

### Reduce functions

- [func simd_reduce_add(simd_half4) -> Float16](/documentation/simd/simd_reduce_add(_:)-2ylck)
- [func simd_reduce_max(simd_half4) -> Float16](/documentation/simd/simd_reduce_max(_:)-4qtu6)
- [func simd_reduce_min(simd_half4) -> Float16](/documentation/simd/simd_reduce_min(_:)-4ulc6)

### Interpolation functions

- [func simd_mix(simd_half4, simd_half4, simd_half4) -> simd_half4](/documentation/simd/simd_mix(_:_:_:)-4uou1)
- [func simd_smoothstep(simd_half4, simd_half4, simd_half4) -> simd_half4](/documentation/simd/simd_smoothstep(_:_:_:)-7gsfq)

### Extrema functions

- [func simd_max(simd_half4, simd_half4) -> simd_half4](/documentation/simd/simd_max(_:_:)-64l5l)
- [func simd_min(simd_half4, simd_half4) -> simd_half4](/documentation/simd/simd_min(_:_:)-1ep1a)

### Reciprocal and reciprocal square root functions

- [func simd_recip(simd_half4) -> simd_half4](/documentation/simd/simd_recip(_:)-822hi)
- [func simd_rsqrt(simd_half4) -> simd_half4](/documentation/simd/simd_rsqrt(_:)-i99u)
- [func simd_precise_recip(simd_half4) -> simd_half4](/documentation/simd/simd_precise_recip(_:)-6pwwe)
- [func simd_precise_rsqrt(simd_half4) -> simd_half4](/documentation/simd/simd_precise_rsqrt(_:)-13530)
- [func simd_fast_recip(simd_half4) -> simd_half4](/documentation/simd/simd_fast_recip(_:)-7d3)
- [func simd_fast_rsqrt(simd_half4) -> simd_half4](/documentation/simd/simd_fast_rsqrt(_:)-8pakw)

### Logic functions

- [func simd_select(simd_half4, simd_half4, simd_short4) -> simd_half4](/documentation/simd/simd_select(_:_:_:)-4vjt)
- [func simd_bitselect(simd_half4, simd_half4, simd_short4) -> simd_half4](/documentation/simd/simd_bitselect(_:_:_:)-6gy8u)

### Math functions

- [func simd_muladd(simd_half4, simd_half4, simd_half4) -> simd_half4](/documentation/simd/simd_muladd(_:_:_:)-99g6r)
- [simd_half8](/documentation/simd/simd_half8)

### Functions to create eight-element vectors from other vectors

- [func simd_make_half8(simd_half2) -> simd_half8](/documentation/simd/simd_make_half8(_:)-97ut4)
- [func simd_make_half8(simd_half3) -> simd_half8](/documentation/simd/simd_make_half8(_:)-9anaf)
- [func simd_make_half8(simd_half4) -> simd_half8](/documentation/simd/simd_make_half8(_:)-9e4ki)
- [func simd_make_half8(simd_half8) -> simd_half8](/documentation/simd/simd_make_half8(_:)-9slsm)
- [func simd_make_half8(simd_half16) -> simd_half8](/documentation/simd/simd_make_half8(_:)-4xf3n)
- [func simd_make_half8(simd_half32) -> simd_half8](/documentation/simd/simd_make_half8(_:)-94pmz)
- [func simd_make_half8_undef(simd_half2) -> simd_half8](/documentation/simd/simd_make_half8_undef(_:)-3on10)
- [func simd_make_half8_undef(simd_half3) -> simd_half8](/documentation/simd/simd_make_half8_undef(_:)-3l5sn)
- [func simd_make_half8_undef(simd_half4) -> simd_half8](/documentation/simd/simd_make_half8_undef(_:)-337am)
- [func simd_make_half8(simd_half4, simd_half4) -> simd_half8](/documentation/simd/simd_make_half8(_:_:))

### Functions to create eight-element vectors from scalar values

- [func simd_make_half8(Float16) -> simd_half8](/documentation/simd/simd_make_half8(_:)-ivna)
- [func simd_make_half8_undef(Float16) -> simd_half8](/documentation/simd/simd_make_half8_undef(_:)-4lqrh)

### Common functions

- [func simd_abs(simd_half8) -> simd_half8](/documentation/simd/simd_abs(_:)-7p1mc)
- [func simd_clamp(simd_half8, simd_half8, simd_half8) -> simd_half8](/documentation/simd/simd_clamp(_:_:_:)-7a090)
- [func simd_equal(simd_half8, simd_half8) -> simd_bool](/documentation/simd/simd_equal(_:_:)-8nejo)
- [func simd_fract(simd_half8) -> simd_half8](/documentation/simd/simd_fract(_:)-3jdnl)
- [func simd_sign(simd_half8) -> simd_half8](/documentation/simd/simd_sign(_:)-7hck3)
- [func simd_step(simd_half8, simd_half8) -> simd_half8](/documentation/simd/simd_step(_:_:)-5v3vi)

### Reduce functions

- [func simd_reduce_add(simd_half8) -> Float16](/documentation/simd/simd_reduce_add(_:)-3auqo)
- [func simd_reduce_max(simd_half8) -> Float16](/documentation/simd/simd_reduce_max(_:)-55ayy)
- [func simd_reduce_min(simd_half8) -> Float16](/documentation/simd/simd_reduce_min(_:)-3o9ia)

### Interpolation functions

- [func simd_mix(simd_half8, simd_half8, simd_half8) -> simd_half8](/documentation/simd/simd_mix(_:_:_:)-6gojc)
- [func simd_smoothstep(simd_half8, simd_half8, simd_half8) -> simd_half8](/documentation/simd/simd_smoothstep(_:_:_:)-96q78)

### Extrema functions

- [func simd_max(simd_half8, simd_half8) -> simd_half8](/documentation/simd/simd_max(_:_:)-ei84)
- [func simd_min(simd_half8, simd_half8) -> simd_half8](/documentation/simd/simd_min(_:_:)-55b3r)

### Reciprocal and reciprocal square root functions

- [func simd_recip(simd_half8) -> simd_half8](/documentation/simd/simd_recip(_:)-98e5u)
- [func simd_rsqrt(simd_half8) -> simd_half8](/documentation/simd/simd_rsqrt(_:)-1ofzq)
- [func simd_precise_recip(simd_half8) -> simd_half8](/documentation/simd/simd_precise_recip(_:)-74du2)
- [func simd_precise_rsqrt(simd_half8) -> simd_half8](/documentation/simd/simd_precise_rsqrt(_:)-1hm48)
- [func simd_fast_recip(simd_half8) -> simd_half8](/documentation/simd/simd_fast_recip(_:)-16ixv)
- [func simd_fast_rsqrt(simd_half8) -> simd_half8](/documentation/simd/simd_fast_rsqrt(_:)-923z8)

### Logic functions

- [func simd_select(simd_half8, simd_half8, simd_short8) -> simd_half8](/documentation/simd/simd_select(_:_:_:)-7qsat)
- [func simd_bitselect(simd_half8, simd_half8, simd_short8) -> simd_half8](/documentation/simd/simd_bitselect(_:_:_:)-1kwpu)

### Math functions

- [func simd_muladd(simd_half8, simd_half8, simd_half8) -> simd_half8](/documentation/simd/simd_muladd(_:_:_:)-1vfnf)
- [simd_int1](/documentation/simd/simd_int1)
- [simd_int16](/documentation/simd/simd_int16)

### Functions to Create Sixteen-Element Vectors From Other Vectors

- [func simd_make_int16(simd_int2) -> simd_int16](/documentation/simd/simd_make_int16(_:)-35atp)
- [func simd_make_int16(simd_int3) -> simd_int16](/documentation/simd/simd_make_int16(_:)-31p8k)
- [func simd_make_int16(simd_int4) -> simd_int16](/documentation/simd/simd_make_int16(_:)-3b5u3)
- [func simd_make_int16(simd_int8) -> simd_int16](/documentation/simd/simd_make_int16(_:)-25e3r)
- [func simd_make_int16(simd_int16) -> simd_int16](/documentation/simd/simd_make_int16(_:)-4wuqs)
- [func simd_make_int16(simd_int8, simd_int8) -> simd_int16](/documentation/simd/simd_make_int16(_:_:))
- [func simd_make_int16_undef(simd_int2) -> simd_int16](/documentation/simd/simd_make_int16_undef(_:)-3zkgc)
- [func simd_make_int16_undef(simd_int3) -> simd_int16](/documentation/simd/simd_make_int16_undef(_:)-431ed)
- [func simd_make_int16_undef(simd_int4) -> simd_int16](/documentation/simd/simd_make_int16_undef(_:)-3eopu)
- [func simd_make_int16_undef(simd_int8) -> simd_int16](/documentation/simd/simd_make_int16_undef(_:)-4lk92)

### Functions to Create Sixteen-Element Vectors From Scalar Values

- [func simd_make_int16(Int32) -> simd_int16](/documentation/simd/simd_make_int16(_:)-26gfd)
- [func simd_make_int16_undef(Int32) -> simd_int16](/documentation/simd/simd_make_int16_undef(_:)-6radb)

### Common Functions

- [func simd_abs(simd_int16) -> simd_int16](/documentation/simd/simd_abs(_:)-477j8)
- [func simd_clamp(simd_int16, simd_int16, simd_int16) -> simd_int16](/documentation/simd/simd_clamp(_:_:_:)-5xcny)
- [func simd_equal(simd_int16, simd_int16) -> simd_bool](/documentation/simd/simd_equal(_:_:)-5fwh2)

### Reduce Functions

- [func simd_reduce_min(simd_int16) -> Int32](/documentation/simd/simd_reduce_min(_:)-3coa3)
- [func simd_reduce_max(simd_int16) -> Int32](/documentation/simd/simd_reduce_max(_:)-8igr1)
- [func simd_reduce_add(simd_int16) -> Int32](/documentation/simd/simd_reduce_add(_:)-7msaw)

### Extrema Functions

- [func simd_min(simd_int16, simd_int16) -> simd_int16](/documentation/simd/simd_min(_:_:)-3f9xy)
- [func simd_max(simd_int16, simd_int16) -> simd_int16](/documentation/simd/simd_max(_:_:)-ybh4)

### Alternative Type Alias

- [vector_int16](/documentation/simd/vector_int16)

### Logic and Bitwise Functions

- [func simd_any(simd_int16) -> simd_bool](/documentation/simd/simd_any(_:)-92rsm)
- [func simd_all(simd_int16) -> simd_bool](/documentation/simd/simd_all(_:)-idpg)
- [func simd_bitselect(simd_int16, simd_int16, simd_int16) -> simd_int16](/documentation/simd/simd_bitselect(_:_:_:)-9fgtc)
- [simd_int2](/documentation/simd/simd_int2)

### Functions to Create Two-Element Vectors From Other Vectors

- [func simd_make_int2(simd_int2) -> simd_int2](/documentation/simd/simd_make_int2(_:)-1j0r7)
- [func simd_make_int2(simd_int3) -> simd_int2](/documentation/simd/simd_make_int2(_:)-1mclu)
- [func simd_make_int2(simd_int4) -> simd_int2](/documentation/simd/simd_make_int2(_:)-1qyb9)
- [func simd_make_int2(simd_int8) -> simd_int2](/documentation/simd/simd_make_int2(_:)-23rr5)
- [func simd_make_int2(simd_int16) -> simd_int2](/documentation/simd/simd_make_int2(_:)-4okip)

### Functions to Create Two-Element Vectors From Scalar Values

- [func simd_make_int2(Int32) -> simd_int2](/documentation/simd/simd_make_int2(_:)-3zby)
- [func simd_make_int2(Int32, Int32) -> simd_int2](/documentation/simd/simd_make_int2(_:_:))
- [func simd_make_int2_undef(Int32) -> simd_int2](/documentation/simd/simd_make_int2_undef(_:))

### Common Functions

- [func simd_abs(simd_int2) -> simd_int2](/documentation/simd/simd_abs(_:)-88kbu)
- [func abs(SIMD2<Int32>) -> SIMD2<Int32>](/documentation/simd/abs(_:)-770jg)
- [func simd_clamp(simd_int2, simd_int2, simd_int2) -> simd_int2](/documentation/simd/simd_clamp(_:_:_:)-9n2rx)
- [func clamp(SIMD2<Int32>, min: SIMD2<Int32>, max: SIMD2<Int32>) -> SIMD2<Int32>](/documentation/simd/clamp(_:min:max:)-y596)
- [func clamp(SIMD2<Int32>, min: Int32, max: Int32) -> SIMD2<Int32>](/documentation/simd/clamp(_:min:max:)-11cyt)
- [func simd_equal(simd_int2, simd_int2) -> simd_bool](/documentation/simd/simd_equal(_:_:)-8sg1t)

### Reduce Functions

- [func simd_reduce_min(simd_int2) -> Int32](/documentation/simd/simd_reduce_min(_:)-49f1c)
- [func reduce_min(SIMD2<Int32>) -> Int32](/documentation/simd/reduce_min(_:)-34ha7)
- [func simd_reduce_max(simd_int2) -> Int32](/documentation/simd/simd_reduce_max(_:)-4kojc)
- [func reduce_max(SIMD2<Int32>) -> Int32](/documentation/simd/reduce_max(_:)-6qw44)
- [func simd_reduce_add(simd_int2) -> Int32](/documentation/simd/simd_reduce_add(_:)-2qeam)
- [func reduce_add(SIMD2<Int32>) -> Int32](/documentation/simd/reduce_add(_:)-4edwc)

### Extrema Functions

- [func simd_max(simd_int2, simd_int2) -> simd_int2](/documentation/simd/simd_max(_:_:)-2xs4j)
- [func max(SIMD2<Int32>, SIMD2<Int32>) -> SIMD2<Int32>](/documentation/simd/max(_:_:)-9xpv0)
- [func max(SIMD2<Int32>, Int32) -> SIMD2<Int32>](/documentation/simd/max(_:_:)-9uijf)
- [func simd_min(simd_int2, simd_int2) -> simd_int2](/documentation/simd/simd_min(_:_:)-3focz)
- [func min(SIMD2<Int32>, SIMD2<Int32>) -> SIMD2<Int32>](/documentation/simd/min(_:_:)-jyi5)
- [func min(SIMD2<Int32>, Int32) -> SIMD2<Int32>](/documentation/simd/min(_:_:)-goji)

### Logic and Bitwise Functions

- [func simd_any(simd_int2) -> simd_bool](/documentation/simd/simd_any(_:)-64rh5)
- [func simd_all(simd_int2) -> simd_bool](/documentation/simd/simd_all(_:)-1cxjv)
- [func simd_bitselect(simd_int2, simd_int2, simd_int2) -> simd_int2](/documentation/simd/simd_bitselect(_:_:_:)-6p66c)

### Alternative Type Alias

- [int2](/documentation/simd/int2)
- [vector_int2](/documentation/simd/vector_int2)
- [simd_int3](/documentation/simd/simd_int3)

### Functions to Create Three-Element Vectors From Other Vectors

- [func simd_make_int3(simd_int2) -> simd_int3](/documentation/simd/simd_make_int3(_:)-2tix4)
- [func simd_make_int3(simd_int3) -> simd_int3](/documentation/simd/simd_make_int3(_:)-2r609)
- [func simd_make_int3(simd_int4) -> simd_int3](/documentation/simd/simd_make_int3(_:)-3fioe)
- [func simd_make_int3(simd_int8) -> simd_int3](/documentation/simd/simd_make_int3(_:)-28n96)
- [func simd_make_int3(simd_int16) -> simd_int3](/documentation/simd/simd_make_int3(_:)-4wbrt)
- [func simd_make_int3_undef(simd_int2) -> simd_int3](/documentation/simd/simd_make_int3_undef(_:)-5kpok)

### Functions to Create Three-Element Vectors From Scalar Values

- [func simd_make_int3(Int32) -> simd_int3](/documentation/simd/simd_make_int3(_:)-4pdxm)
- [func simd_make_int3(Int32, Int32, Int32) -> simd_int3](/documentation/simd/simd_make_int3(_:_:_:))
- [func simd_make_int3_undef(Int32) -> simd_int3](/documentation/simd/simd_make_int3_undef(_:)-5q1nf)

### Functions to Create Three-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_int3(simd_int2, Int32) -> simd_int3](/documentation/simd/simd_make_int3(_:_:)-7nox5)
- [func simd_make_int3(Int32, simd_int2) -> simd_int3](/documentation/simd/simd_make_int3(_:_:)-48lb0)

### Common Functions

- [func simd_abs(simd_int3) -> simd_int3](/documentation/simd/simd_abs(_:)-8d4m3)
- [func abs(SIMD3<Int32>) -> SIMD3<Int32>](/documentation/simd/abs(_:)-2m9bi)
- [func simd_clamp(simd_int3, simd_int3, simd_int3) -> simd_int3](/documentation/simd/simd_clamp(_:_:_:)-68p0z)
- [func clamp(SIMD3<Int32>, min: Int32, max: Int32) -> SIMD3<Int32>](/documentation/simd/clamp(_:min:max:)-7b2i)
- [func clamp(SIMD3<Int32>, min: SIMD3<Int32>, max: SIMD3<Int32>) -> SIMD3<Int32>](/documentation/simd/clamp(_:min:max:)-cim1)
- [func simd_equal(simd_float3, simd_float3) -> simd_bool](/documentation/simd/simd_equal(_:_:)-6i7q4)

### Reduce Functions

- [func simd_reduce_min(simd_int3) -> Int32](/documentation/simd/simd_reduce_min(_:)-45ygx)
- [func reduce_min(SIMD3<Int32>) -> Int32](/documentation/simd/reduce_min(_:)-3l43s)
- [func simd_reduce_max(simd_float3) -> Float](/documentation/simd/simd_reduce_max(_:)-4gy97)
- [func reduce_max(SIMD3<Int32>) -> Int32](/documentation/simd/reduce_max(_:)-5wvu6)
- [func simd_reduce_add(simd_int3) -> Int32](/documentation/simd/simd_reduce_add(_:)-2utmv)
- [func reduce_add(SIMD3<Int32>) -> Int32](/documentation/simd/reduce_add(_:)-9pjza)

### Extrema Functions

- [func simd_max(simd_int3, simd_int3) -> simd_int3](/documentation/simd/simd_max(_:_:)-93k3o)
- [func max(SIMD3<Int32>, Int32) -> SIMD3<Int32>](/documentation/simd/max(_:_:)-1zb5g)
- [func max(SIMD3<Int32>, SIMD3<Int32>) -> SIMD3<Int32>](/documentation/simd/max(_:_:)-1w3tf)
- [func simd_min(simd_int3, simd_int3) -> simd_int3](/documentation/simd/simd_min(_:_:)-2t446)
- [func min(SIMD3<Int32>, Int32) -> SIMD3<Int32>](/documentation/simd/min(_:_:)-8safl)
- [func min(SIMD3<Int32>, SIMD3<Int32>) -> SIMD3<Int32>](/documentation/simd/min(_:_:)-8p0ea)

### Logic and Bitwise Functions

- [func simd_any(simd_int3) -> simd_bool](/documentation/simd/simd_any(_:)-69748)
- [func simd_all(simd_int3) -> simd_bool](/documentation/simd/simd_all(_:)-1apey)
- [func simd_bitselect(simd_int3, simd_int3, simd_int3) -> simd_int3](/documentation/simd/simd_bitselect(_:_:_:)-78l7a)

### Alternative Type Alias

- [int3](/documentation/simd/int3)
- [vector_int3](/documentation/simd/vector_int3)
- [simd_int4](/documentation/simd/simd_int4)

### Functions to Create Four-Element Vectors From Other Vectors

- [func simd_make_int4(simd_int2) -> simd_int4](/documentation/simd/simd_make_int4(_:)-1suou)
- [func simd_make_int4(simd_int3) -> simd_int4](/documentation/simd/simd_make_int4(_:)-1wbev)
- [func simd_make_int4(simd_int4) -> simd_int4](/documentation/simd/simd_make_int4(_:)-1kx2w)
- [func simd_make_int4(simd_int8) -> simd_int4](/documentation/simd/simd_make_int4(_:)-2qk04)
- [func simd_make_int4(simd_int16) -> simd_int4](/documentation/simd/simd_make_int4(_:)-2rtb0)
- [func simd_make_int4(simd_int2, simd_int2) -> simd_int4](/documentation/simd/simd_make_int4(_:_:)-4phxy)
- [func simd_make_int4_undef(simd_int2) -> simd_int4](/documentation/simd/simd_make_int4_undef(_:)-5g92f)
- [func simd_make_int4_undef(simd_int3) -> simd_int4](/documentation/simd/simd_make_int4_undef(_:)-5dw9q)

### Functions to Create Four-Element Vectors From Scalar Values

- [func simd_make_int4(Int32) -> simd_int4](/documentation/simd/simd_make_int4(_:)-7vwve)
- [func simd_make_int4(Int32, Int32, Int32, Int32) -> simd_int4](/documentation/simd/simd_make_int4(_:_:_:_:))
- [func simd_make_int4_undef(Int32) -> simd_int4](/documentation/simd/simd_make_int4_undef(_:)-2wt72)

### Functions to Create Four-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_int4(simd_int2, Int32, Int32) -> simd_int4](/documentation/simd/simd_make_int4(_:_:_:)-7cjm7)
- [func simd_make_int4(simd_int3, Int32) -> simd_int4](/documentation/simd/simd_make_int4(_:_:)-7rrqd)
- [func simd_make_int4(Int32, Int32, simd_int2) -> simd_int4](/documentation/simd/simd_make_int4(_:_:_:)-9tjlm)
- [func simd_make_int4(Int32, simd_int2, Int32) -> simd_int4](/documentation/simd/simd_make_int4(_:_:_:)-8of8y)
- [func simd_make_int4(Int32, simd_int3) -> simd_int4](/documentation/simd/simd_make_int4(_:_:)-6p0ui)

### Common Functions

- [func simd_abs(simd_int4) -> simd_int4](/documentation/simd/simd_abs(_:)-81glw)
- [func abs(SIMD4<Int32>) -> SIMD4<Int32>](/documentation/simd/abs(_:)-1b3qo)
- [func simd_clamp(simd_int4, simd_int4, simd_int4) -> simd_int4](/documentation/simd/simd_clamp(_:_:_:)-50obl)
- [func clamp(SIMD4<Int32>, min: Int32, max: Int32) -> SIMD4<Int32>](/documentation/simd/clamp(_:min:max:)-5if3n)
- [func clamp(SIMD4<Int32>, min: SIMD4<Int32>, max: SIMD4<Int32>) -> SIMD4<Int32>](/documentation/simd/clamp(_:min:max:)-5f538)
- [func simd_equal(simd_int4, simd_int4) -> simd_bool](/documentation/simd/simd_equal(_:_:)-2rypj)

### Reduce Functions

- [func simd_reduce_min(simd_int4) -> Int32](/documentation/simd/simd_reduce_min(_:)-4uaza)
- [func reduce_min(SIMD4<Int32>) -> Int32](/documentation/simd/reduce_min(_:)-6npco)
- [func simd_reduce_max(simd_int4) -> Int32](/documentation/simd/simd_reduce_max(_:)-4qjkm)
- [func reduce_max(SIMD4<Int32>) -> Int32](/documentation/simd/reduce_max(_:)-5afy1)
- [func simd_reduce_add(simd_int4) -> Int32](/documentation/simd/simd_reduce_add(_:)-2ybq8)
- [func reduce_add(SIMD4<Int32>) -> Int32](/documentation/simd/reduce_add(_:)-89ptt)

### Extrema Functions

- [func simd_max(simd_int4, simd_int4) -> simd_int4](/documentation/simd/simd_max(_:_:)-51txy)
- [func max(SIMD4<Int32>, Int32) -> SIMD4<Int32>](/documentation/simd/max(_:_:)-696e3)
- [func max(SIMD4<Int32>, SIMD4<Int32>) -> SIMD4<Int32>](/documentation/simd/max(_:_:)-6cb9k)
- [func simd_min(simd_int4, simd_int4) -> simd_int4](/documentation/simd/simd_min(_:_:)-1m8ma)
- [func min(SIMD4<Int32>, Int32) -> SIMD4<Int32>](/documentation/simd/min(_:_:)-5uuf6)
- [func min(SIMD4<Int32>, SIMD4<Int32>) -> SIMD4<Int32>](/documentation/simd/min(_:_:)-5y1sd)

### Logic and Bitwise Functions

- [func simd_any(simd_int4) -> simd_bool](/documentation/simd/simd_any(_:)-6cp1b)
- [func simd_all(simd_int4) -> simd_bool](/documentation/simd/simd_all(_:)-1jw6t)
- [func simd_bitselect(simd_int4, simd_int4, simd_int4) -> simd_int4](/documentation/simd/simd_bitselect(_:_:_:)-27mh1)

### Alternative Type Alias

- [int4](/documentation/simd/int4)
- [vector_int4](/documentation/simd/vector_int4)
- [simd_int8](/documentation/simd/simd_int8)

### Functions to Create Eight-Element Vectors From Other Vectors

- [func simd_make_int8(simd_int2) -> simd_int8](/documentation/simd/simd_make_int8(_:)-9s1jp)
- [func simd_make_int8(simd_int3) -> simd_int8](/documentation/simd/simd_make_int8(_:)-9vi30)
- [func simd_make_int8(simd_int4) -> simd_int8](/documentation/simd/simd_make_int8(_:)-efr4)
- [func simd_make_int8(simd_int8) -> simd_int8](/documentation/simd/simd_make_int8(_:)-r4ak)
- [func simd_make_int8(simd_int16) -> simd_int8](/documentation/simd/simd_make_int8(_:)-3lu01)
- [func simd_make_int8(simd_int4, simd_int4) -> simd_int8](/documentation/simd/simd_make_int8(_:_:))
- [func simd_make_int8_undef(simd_int2) -> simd_int8](/documentation/simd/simd_make_int8_undef(_:)-57mj8)
- [func simd_make_int8_undef(simd_int3) -> simd_int8](/documentation/simd/simd_make_int8_undef(_:)-5324d)
- [func simd_make_int8_undef(simd_int4) -> simd_int8](/documentation/simd/simd_make_int8_undef(_:)-5rem2)

### Functions to Create Eight-Element Vectors From Scalar Values

- [func simd_make_int8(Int32) -> simd_int8](/documentation/simd/simd_make_int8(_:)-9srg8)
- [func simd_make_int8_undef(Int32) -> simd_int8](/documentation/simd/simd_make_int8_undef(_:)-2ce80)

### Common Functions

- [func simd_abs(simd_int8) -> simd_int8](/documentation/simd/simd_abs(_:)-7os48)
- [func simd_clamp(simd_int8, simd_int8, simd_int8) -> simd_int8](/documentation/simd/simd_clamp(_:_:_:)-4jo2y)
- [func simd_equal(simd_int8, simd_int8) -> simd_bool](/documentation/simd/simd_equal(_:_:)-ojy5)

### Reduce Functions

- [func simd_reduce_min(simd_int8) -> Int32](/documentation/simd/simd_reduce_min(_:)-3ojci)
- [func simd_reduce_max(simd_int8) -> Int32](/documentation/simd/simd_reduce_max(_:)-55kne)
- [func simd_reduce_add(simd_int8) -> Int32](/documentation/simd/simd_reduce_add(_:)-3b56c)

### Extrema Functions

- [func simd_min(simd_int8, simd_int8) -> simd_int8](/documentation/simd/simd_min(_:_:)-2fywl)
- [func simd_max(simd_int8, simd_int8) -> simd_int8](/documentation/simd/simd_max(_:_:)-5sjen)

### Logic and Bitwise Functions

- [func simd_any(simd_int8) -> simd_bool](/documentation/simd/simd_any(_:)-6pigr)
- [func simd_all(simd_int8) -> simd_bool](/documentation/simd/simd_all(_:)-1yx6x)
- [func simd_bitselect(simd_int8, simd_int8, simd_int8) -> simd_int8](/documentation/simd/simd_bitselect(_:_:_:)-361vz)

### Alternative Type Alias

- [vector_int8](/documentation/simd/vector_int8)
- [simd_long1](/documentation/simd/simd_long1)

### Alternative Type Alias

- [vector_long1](/documentation/simd/vector_long1)
- [simd_long2](/documentation/simd/simd_long2)

### Functions to Create Two-Element Vectors From Other Vectors

- [func simd_make_long2(simd_long2) -> simd_long2](/documentation/simd/simd_make_long2(_:)-96bn)
- [func simd_make_long2(simd_long3) -> simd_long2](/documentation/simd/simd_make_long2(_:)-5ou8)
- [func simd_make_long2(simd_long4) -> simd_long2](/documentation/simd/simd_make_long2(_:)-2abd)
- [func simd_make_long2(simd_long8) -> simd_long2](/documentation/simd/simd_make_long2(_:)-9ozpw)

### Functions to Create Two-Element Vectors From Scalar Values

- [func simd_make_long2(simd_long1) -> simd_long2](/documentation/simd/simd_make_long2(_:)-698vu)
- [func simd_make_long2(simd_long1, simd_long1) -> simd_long2](/documentation/simd/simd_make_long2(_:_:))
- [func simd_make_long2_undef(simd_long1) -> simd_long2](/documentation/simd/simd_make_long2_undef(_:))

### Common Functions

- [func simd_abs(simd_long2) -> simd_long2](/documentation/simd/simd_abs(_:)-88ipu)
- [func simd_clamp(simd_long2, simd_long2, simd_long2) -> simd_long2](/documentation/simd/simd_clamp(_:_:_:)-4sik)
- [func simd_equal(simd_long2, simd_long2) -> simd_bool](/documentation/simd/simd_equal(_:_:)-2qcs1)

### Reduce Functions

- [func simd_reduce_min(simd_long2) -> simd_long1](/documentation/simd/simd_reduce_min(_:)-49gjw)
- [func simd_reduce_max(simd_long2) -> simd_long1](/documentation/simd/simd_reduce_max(_:)-4kq58)
- [func simd_reduce_add(simd_long2) -> simd_long1](/documentation/simd/simd_reduce_add(_:)-2qco6)

### Extrema Functions

- [func simd_min(simd_long2, simd_long2) -> simd_long2](/documentation/simd/simd_min(_:_:)-5lq3f)
- [func simd_max(simd_long2, simd_long2) -> simd_long2](/documentation/simd/simd_max(_:_:)-439j5)

### Logic and Bitwise Functions

- [func simd_any(simd_long2) -> simd_bool](/documentation/simd/simd_any(_:)-64pz3)
- [func simd_all(simd_long2) -> simd_bool](/documentation/simd/simd_all(_:)-1cyyp)
- [func simd_bitselect(simd_long2, simd_long2, simd_long2) -> simd_long2](/documentation/simd/simd_bitselect(_:_:_:)-8ffoo)

### Alternative Type Alias

- [vector_long2](/documentation/simd/vector_long2)
- [simd_long3](/documentation/simd/simd_long3)

### Functions to Create Three-Element Vectors From Other Vectors

- [func simd_make_long3(simd_long2) -> simd_long3](/documentation/simd/simd_make_long3(_:)-4le1z)
- [func simd_make_long3(simd_long3) -> simd_long3](/documentation/simd/simd_make_long3(_:)-4osz8)
- [func simd_make_long3(simd_long4) -> simd_long3](/documentation/simd/simd_make_long3(_:)-40i9p)
- [func simd_make_long3(simd_long8) -> simd_long3](/documentation/simd/simd_make_long3(_:)-567hd)
- [func simd_make_long3_undef(simd_long2) -> simd_long3](/documentation/simd/simd_make_long3_undef(_:)-8anf9)

### Functions to Create Three-Element Vectors From Scalar Values

- [func simd_make_long3(simd_long1) -> simd_long3](/documentation/simd/simd_make_long3(_:)-1n0vi)
- [func simd_make_long3(simd_long1, simd_long1, simd_long1) -> simd_long3](/documentation/simd/simd_make_long3(_:_:_:))
- [func simd_make_long3_undef(simd_long1) -> simd_long3](/documentation/simd/simd_make_long3_undef(_:)-4ehx)

### Functions to Create Three-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_long3(simd_long1, simd_long2) -> simd_long3](/documentation/simd/simd_make_long3(_:_:)-3zz23)
- [func simd_make_long3(simd_long2, simd_long1) -> simd_long3](/documentation/simd/simd_make_long3(_:_:)-36pz0)

### Common Functions

- [func simd_abs(simd_long3) -> simd_long3](/documentation/simd/simd_abs(_:)-8d3rx)
- [func simd_clamp(simd_long3, simd_long3, simd_long3) -> simd_long3](/documentation/simd/simd_clamp(_:_:_:)-6yqku)
- [func simd_equal(simd_long3, simd_long3) -> simd_bool](/documentation/simd/simd_equal(_:_:)-1ikxk)

### Reduce Functions

- [func simd_reduce_min(simd_long3) -> simd_long1](/documentation/simd/simd_reduce_min(_:)-45zbv)
- [func simd_reduce_max(simd_long3) -> simd_long1](/documentation/simd/simd_reduce_max(_:)-4hb9r)
- [func simd_reduce_add(simd_long3) -> simd_long1](/documentation/simd/simd_reduce_add(_:)-2uv9x)

### Extrema Functions

- [func simd_min(simd_long3, simd_long3) -> simd_long3](/documentation/simd/simd_min(_:_:)-3a034)
- [func simd_max(simd_long3, simd_long3) -> simd_long3](/documentation/simd/simd_max(_:_:)-2hury)

### Logic and Bitwise Functions

- [func simd_any(simd_long3) -> simd_bool](/documentation/simd/simd_any(_:)-698ng)
- [func simd_all(simd_long3) -> simd_bool](/documentation/simd/simd_all(_:)-1ao6q)
- [func simd_bitselect(simd_long3, simd_long3, simd_long3) -> simd_long3](/documentation/simd/simd_bitselect(_:_:_:)-9hl4)

### Alternative Type Alias

- [vector_long3](/documentation/simd/vector_long3)
- [simd_long4](/documentation/simd/simd_long4)

### Functions to Create Four-Element Vectors From Other Vectors

- [func simd_make_long4(simd_long2) -> simd_long4](/documentation/simd/simd_make_long4(_:)-98er2)
- [func simd_make_long4(simd_long3) -> simd_long4](/documentation/simd/simd_make_long4(_:)-94zwx)
- [func simd_make_long4(simd_long4) -> simd_long4](/documentation/simd/simd_make_long4(_:)-8op7o)
- [func simd_make_long4(simd_long8) -> simd_long4](/documentation/simd/simd_make_long4(_:)-9tamg)
- [func simd_make_long4(simd_long2, simd_long2) -> simd_long4](/documentation/simd/simd_make_long4(_:_:)-51qs4)
- [func simd_make_long4_undef(simd_long2) -> simd_long4](/documentation/simd/simd_make_long4_undef(_:)-31uo1)
- [func simd_make_long4_undef(simd_long3) -> simd_long4](/documentation/simd/simd_make_long4_undef(_:)-345km)

### Functions to Create Four-Element Vectors From Scalar Values

- [func simd_make_long4(simd_long1) -> simd_long4](/documentation/simd/simd_make_long4(_:)-4ir93)
- [func simd_make_long4(simd_long1, simd_long1, simd_long1, simd_long1) -> simd_long4](/documentation/simd/simd_make_long4(_:_:_:_:))
- [func simd_make_long4_undef(simd_long1) -> simd_long4](/documentation/simd/simd_make_long4_undef(_:)-6bf3i)

### Functions to Create Four-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_long4(simd_long1, simd_long1, simd_long2) -> simd_long4](/documentation/simd/simd_make_long4(_:_:_:)-5o04d)
- [func simd_make_long4(simd_long1, simd_long2, simd_long1) -> simd_long4](/documentation/simd/simd_make_long4(_:_:_:)-1oyio)
- [func simd_make_long4(simd_long1, simd_long3) -> simd_long4](/documentation/simd/simd_make_long4(_:_:)-837pc)
- [func simd_make_long4(simd_long2, simd_long1, simd_long1) -> simd_long4](/documentation/simd/simd_make_long4(_:_:_:)-6ici1)
- [func simd_make_long4(simd_long3, simd_long1) -> simd_long4](/documentation/simd/simd_make_long4(_:_:)-270ke)

### Common Functions

- [func simd_abs(simd_long4) -> simd_long4](/documentation/simd/simd_abs(_:)-81f1k)
- [func simd_clamp(simd_long4, simd_long4, simd_long4) -> simd_long4](/documentation/simd/simd_clamp(_:_:_:)-69473)
- [func simd_equal(simd_long4, simd_long4) -> simd_bool](/documentation/simd/simd_equal(_:_:)-4wnv3)

### Reduce Functions

- [func simd_reduce_min(simd_long4) -> simd_long1](/documentation/simd/simd_reduce_min(_:)-4ua4m)
- [func simd_reduce_max(simd_long4) -> simd_long1](/documentation/simd/simd_reduce_max(_:)-4qin2)
- [func simd_reduce_add(simd_long4) -> simd_long1](/documentation/simd/simd_reduce_add(_:)-2ya50)

### Extrema Functions

- [func simd_min(simd_long4, simd_long4) -> simd_long4](/documentation/simd/simd_min(_:_:)-4y4aq)
- [func simd_max(simd_long4, simd_long4) -> simd_long4](/documentation/simd/simd_max(_:_:)-3enrf)

### Logic and Bitwise Functions

- [func simd_any(simd_long4) -> simd_bool](/documentation/simd/simd_any(_:)-6cnfh)
- [func simd_all(simd_long4) -> simd_bool](/documentation/simd/simd_all(_:)-1jv5n)
- [func simd_bitselect(simd_long4, simd_long4, simd_long4) -> simd_long4](/documentation/simd/simd_bitselect(_:_:_:)-9f5q6)

### Alternative Type Alias

- [vector_long4](/documentation/simd/vector_long4)
- [simd_long8](/documentation/simd/simd_long8)

### Functions to Create Eight-Element Vectors From Other Vectors

- [func simd_make_long8(simd_long2) -> simd_long8](/documentation/simd/simd_make_long8(_:)-7pzt7)
- [func simd_make_long8(simd_long3) -> simd_long8](/documentation/simd/simd_make_long8(_:)-7netg)
- [func simd_make_long8(simd_long4) -> simd_long8](/documentation/simd/simd_make_long8(_:)-7wvxt)
- [func simd_make_long8(simd_long8) -> simd_long8](/documentation/simd/simd_make_long8(_:)-6saal)
- [func simd_make_long8(simd_long4, simd_long4) -> simd_long8](/documentation/simd/simd_make_long8(_:_:))
- [func simd_make_long8_undef(simd_long2) -> simd_long8](/documentation/simd/simd_make_long8_undef(_:)-5uowh)
- [func simd_make_long8_undef(simd_long3) -> simd_long8](/documentation/simd/simd_make_long8_undef(_:)-5y3qm)
- [func simd_make_long8_undef(simd_long4) -> simd_long8](/documentation/simd/simd_make_long8_undef(_:)-59t0j)

### Functions to Create Eight-Element Vectors From Scalar Values

- [func simd_make_long8(simd_long1) -> simd_long8](/documentation/simd/simd_make_long8(_:)-2kqft)
- [func simd_make_long8_undef(simd_long1) -> simd_long8](/documentation/simd/simd_make_long8_undef(_:)-9h1v1)

### Common Functions

- [func simd_abs(simd_long8) -> simd_long8](/documentation/simd/simd_abs(_:)-7osxw)
- [func simd_clamp(simd_long8, simd_long8, simd_long8) -> simd_long8](/documentation/simd/simd_clamp(_:_:_:)-7h5og)
- [func simd_equal(simd_long8, simd_long8) -> simd_bool](/documentation/simd/simd_equal(_:_:)-1fygf)

### Reduce Functions

- [func simd_reduce_min(simd_long8) -> simd_long1](/documentation/simd/simd_reduce_min(_:)-3okve)
- [func simd_reduce_max(simd_long8) -> simd_long1](/documentation/simd/simd_reduce_max(_:)-55m7m)
- [func simd_reduce_add(simd_long8) -> simd_long1](/documentation/simd/simd_reduce_add(_:)-3b63s)

### Extrema Functions

- [func simd_min(simd_long8, simd_long8) -> simd_long8](/documentation/simd/simd_min(_:_:)-1z34d)
- [func simd_max(simd_long8, simd_long8) -> simd_long8](/documentation/simd/simd_max(_:_:)-4cbvp)

### Logic and Bitwise Functions

- [func simd_any(simd_long8) -> simd_bool](/documentation/simd/simd_any(_:)-6pjhd)
- [func simd_all(simd_long8) -> simd_bool](/documentation/simd/simd_all(_:)-1yys7)
- [func simd_bitselect(simd_long8, simd_long8, simd_long8) -> simd_long8](/documentation/simd/simd_bitselect(_:_:_:)-5k6g)

### Alternative Type Alias

- [vector_long8](/documentation/simd/vector_long8)
- [simd_packed_char16](/documentation/simd/simd_packed_char16)

### Alternative Type Alias

- [packed_char16](/documentation/simd/packed_char16)
- [simd_packed_char2](/documentation/simd/simd_packed_char2)

### Alternative Type Alias

- [packed_char2](/documentation/simd/packed_char2)
- [simd_packed_char32](/documentation/simd/simd_packed_char32)

### Alternative Type Alias

- [packed_char32](/documentation/simd/packed_char32)
- [simd_packed_char4](/documentation/simd/simd_packed_char4)

### Alternative Type Alias

- [packed_char4](/documentation/simd/packed_char4)
- [simd_packed_char64](/documentation/simd/simd_packed_char64)

### Alternative Type Alias

- [packed_char64](/documentation/simd/packed_char64)
- [simd_packed_char8](/documentation/simd/simd_packed_char8)

### Alternative Type Alias

- [packed_char8](/documentation/simd/packed_char8)
- [simd_packed_double2](/documentation/simd/simd_packed_double2)

### Alternative Type Alias

- [packed_double2](/documentation/simd/packed_double2)
- [simd_packed_double4](/documentation/simd/simd_packed_double4)

### Alternative Type Alias

- [packed_double4](/documentation/simd/packed_double4)
- [simd_packed_double8](/documentation/simd/simd_packed_double8)

### Alternative Type Alias

- [packed_double8](/documentation/simd/packed_double8)
- [simd_packed_float16](/documentation/simd/simd_packed_float16)

### Alternative Type Alias

- [packed_float16](/documentation/simd/packed_float16)
- [simd_packed_float2](/documentation/simd/simd_packed_float2)

### Alternative Type Alias

- [packed_float2](/documentation/simd/packed_float2)
- [simd_packed_float4](/documentation/simd/simd_packed_float4)

### Alternative Type Alias

- [packed_float4](/documentation/simd/packed_float4)
- [simd_packed_float8](/documentation/simd/simd_packed_float8)

### Alternative Type Alias

- [packed_float8](/documentation/simd/packed_float8)
- [simd_packed_half16](/documentation/simd/simd_packed_half16)
- [simd_packed_half2](/documentation/simd/simd_packed_half2)
- [simd_packed_half32](/documentation/simd/simd_packed_half32)
- [simd_packed_half4](/documentation/simd/simd_packed_half4)
- [simd_packed_half8](/documentation/simd/simd_packed_half8)
- [simd_packed_int16](/documentation/simd/simd_packed_int16)

### Alternative Type Alias

- [packed_int16](/documentation/simd/packed_int16)
- [simd_packed_int2](/documentation/simd/simd_packed_int2)

### Alternative Type Alias

- [packed_int2](/documentation/simd/packed_int2)
- [simd_packed_int4](/documentation/simd/simd_packed_int4)

### Alternative Type Alias

- [packed_int4](/documentation/simd/packed_int4)
- [simd_packed_int8](/documentation/simd/simd_packed_int8)

### Alternative Type Alias

- [packed_int8](/documentation/simd/packed_int8)
- [simd_packed_long2](/documentation/simd/simd_packed_long2)

### Alternative Type Alias

- [packed_long2](/documentation/simd/packed_long2)
- [simd_packed_long4](/documentation/simd/simd_packed_long4)

### Alternative Type Alias

- [packed_long4](/documentation/simd/packed_long4)
- [simd_packed_long8](/documentation/simd/simd_packed_long8)

### Alternative Type Alias

- [packed_long8](/documentation/simd/packed_long8)
- [simd_packed_short16](/documentation/simd/simd_packed_short16)

### Alternative Type Alias

- [packed_short16](/documentation/simd/packed_short16)
- [simd_packed_short2](/documentation/simd/simd_packed_short2)

### Alternative Type Alias

- [packed_short2](/documentation/simd/packed_short2)
- [simd_packed_short32](/documentation/simd/simd_packed_short32)

### Alternative Type Alias

- [packed_short32](/documentation/simd/packed_short32)
- [simd_packed_short4](/documentation/simd/simd_packed_short4)

### Alternative Type Alias

- [packed_short4](/documentation/simd/packed_short4)
- [simd_packed_short8](/documentation/simd/simd_packed_short8)

### Alternative Type Alias

- [packed_short8](/documentation/simd/packed_short8)
- [simd_packed_uchar16](/documentation/simd/simd_packed_uchar16)

### Alternative Type Alias

- [packed_uchar16](/documentation/simd/packed_uchar16)
- [simd_packed_uchar2](/documentation/simd/simd_packed_uchar2)

### Alternative Type Alias

- [packed_uchar2](/documentation/simd/packed_uchar2)
- [simd_packed_uchar32](/documentation/simd/simd_packed_uchar32)

### Alternative Type Alias

- [packed_uchar32](/documentation/simd/packed_uchar32)
- [simd_packed_uchar4](/documentation/simd/simd_packed_uchar4)

### Alternative Type Alias

- [packed_uchar4](/documentation/simd/packed_uchar4)
- [simd_packed_uchar64](/documentation/simd/simd_packed_uchar64)

### Alternative Type Alias

- [packed_uchar64](/documentation/simd/packed_uchar64)
- [simd_packed_uchar8](/documentation/simd/simd_packed_uchar8)

### Alternative Type Alias

- [packed_uchar8](/documentation/simd/packed_uchar8)
- [simd_packed_uint16](/documentation/simd/simd_packed_uint16)

### Alternative Type Alias

- [packed_uint16](/documentation/simd/packed_uint16)
- [simd_packed_uint2](/documentation/simd/simd_packed_uint2)

### Alternative Type Alias

- [packed_uint2](/documentation/simd/packed_uint2)
- [simd_packed_uint4](/documentation/simd/simd_packed_uint4)

### Alternative Type Alias

- [packed_uint4](/documentation/simd/packed_uint4)
- [simd_packed_uint8](/documentation/simd/simd_packed_uint8)

### Alternative Type Alias

- [packed_uint8](/documentation/simd/packed_uint8)
- [simd_packed_ulong2](/documentation/simd/simd_packed_ulong2)

### Alternative Type Alias

- [packed_ulong2](/documentation/simd/packed_ulong2)
- [simd_packed_ulong4](/documentation/simd/simd_packed_ulong4)

### Alternative Type Alias

- [packed_ulong4](/documentation/simd/packed_ulong4)
- [simd_packed_ulong8](/documentation/simd/simd_packed_ulong8)

### Alternative Type Alias

- [packed_ulong8](/documentation/simd/packed_ulong8)
- [simd_packed_ushort16](/documentation/simd/simd_packed_ushort16)

### Alternative Type Alias

- [packed_ushort16](/documentation/simd/packed_ushort16)
- [simd_packed_ushort2](/documentation/simd/simd_packed_ushort2)

### Alternative Type Alias

- [packed_ushort2](/documentation/simd/packed_ushort2)
- [simd_packed_ushort32](/documentation/simd/simd_packed_ushort32)

### Alternative Type Alias

- [packed_ushort32](/documentation/simd/packed_ushort32)
- [simd_packed_ushort4](/documentation/simd/simd_packed_ushort4)

### Alternative Type Alias

- [packed_ushort4](/documentation/simd/packed_ushort4)
- [simd_packed_ushort8](/documentation/simd/simd_packed_ushort8)

### Alternative Type Alias

- [packed_ushort8](/documentation/simd/packed_ushort8)
- [simd_short1](/documentation/simd/simd_short1)
- [simd_short16](/documentation/simd/simd_short16)

### Functions to Create Sixteen-Element Vectors From Other Vectors

- [func simd_make_short16(simd_short2) -> simd_short16](/documentation/simd/simd_make_short16(_:)-8892t)
- [func simd_make_short16(simd_short3) -> simd_short16](/documentation/simd/simd_make_short16(_:)-8bejg)
- [func simd_make_short16(simd_short4) -> simd_short16](/documentation/simd/simd_make_short16(_:)-82czr)
- [func simd_make_short16(simd_short8) -> simd_short16](/documentation/simd/simd_make_short16(_:)-984rv)
- [func simd_make_short16(simd_short16) -> simd_short16](/documentation/simd/simd_make_short16(_:)-5xtuv)
- [func simd_make_short16(simd_short32) -> simd_short16](/documentation/simd/simd_make_short16(_:)-4ubc7)
- [func simd_make_short16(simd_short8, simd_short8) -> simd_short16](/documentation/simd/simd_make_short16(_:_:))
- [func simd_make_short16_undef(simd_short2) -> simd_short16](/documentation/simd/simd_make_short16_undef(_:)-19u0l)
- [func simd_make_short16_undef(simd_short3) -> simd_short16](/documentation/simd/simd_make_short16_undef(_:)-150ws)
- [func simd_make_short16_undef(simd_short4) -> simd_short16](/documentation/simd/simd_make_short16_undef(_:)-11st3)
- [func simd_make_short16_undef(simd_short8) -> simd_short16](/documentation/simd/simd_make_short16_undef(_:)-27knv)

### Functions to Create Sixteen-Element Vectors From Scalar Values

- [func simd_make_short16(Int16) -> simd_short16](/documentation/simd/simd_make_short16(_:)-3x8mr)
- [func simd_make_short16_undef(Int16) -> simd_short16](/documentation/simd/simd_make_short16_undef(_:)-mhi)

### Common Functions

- [func simd_abs(simd_short16) -> simd_short16](/documentation/simd/simd_abs(_:)-47an0)
- [func simd_clamp(simd_short16, simd_short16, simd_short16) -> simd_short16](/documentation/simd/simd_clamp(_:_:_:)-9ykva)
- [func simd_equal(simd_short16, simd_short16) -> simd_bool](/documentation/simd/simd_equal(_:_:)-220xu)

### Reduce Functions

- [func simd_reduce_min(simd_short16) -> Int16](/documentation/simd/simd_reduce_min(_:)-3cwd3)
- [func simd_reduce_max(simd_short16) -> Int16](/documentation/simd/simd_reduce_max(_:)-8iihx)
- [func simd_reduce_add(simd_short16) -> Int16](/documentation/simd/simd_reduce_add(_:)-7mz6g)

### Extrema Functions

- [func simd_min(simd_short16, simd_short16) -> simd_short16](/documentation/simd/simd_min(_:_:)-9vjqx)
- [func simd_max(simd_short16, simd_short16) -> simd_short16](/documentation/simd/simd_max(_:_:)-9xf7i)

### Logic and Bitwise Functions

- [func simd_any(simd_short16) -> simd_bool](/documentation/simd/simd_any(_:)-92yq2)
- [func simd_all(simd_short16) -> simd_bool](/documentation/simd/simd_all(_:)-i5jw)
- [func simd_bitselect(simd_short16, simd_short16, simd_short16) -> simd_short16](/documentation/simd/simd_bitselect(_:_:_:)-3vpt5)

### Alternative Type Alias

- [vector_short16](/documentation/simd/vector_short16)
- [simd_short2](/documentation/simd/simd_short2)

### Functions to Create Two-Element Vectors From Other Vectors

- [func simd_make_short2(simd_short2) -> simd_short2](/documentation/simd/simd_make_short2(_:)-6juuy)
- [func simd_make_short2(simd_short3) -> simd_short2](/documentation/simd/simd_make_short2(_:)-6gmv7)
- [func simd_make_short2(simd_short4) -> simd_short2](/documentation/simd/simd_make_short2(_:)-5z7ps)
- [func simd_make_short2(simd_short8) -> simd_short2](/documentation/simd/simd_make_short2(_:)-74zg4)
- [func simd_make_short2(simd_short16) -> simd_short2](/documentation/simd/simd_make_short2(_:)-58qns)
- [func simd_make_short2(simd_short32) -> simd_short2](/documentation/simd/simd_make_short2(_:)-6bz90)

### Functions to Create Two-Element Vectors From Scalar Values

- [func simd_make_short2(Int16) -> simd_short2](/documentation/simd/simd_make_short2(_:)-222xa)
- [func simd_make_short2(Int16, Int16) -> simd_short2](/documentation/simd/simd_make_short2(_:_:))
- [func simd_make_short2_undef(Int16) -> simd_short2](/documentation/simd/simd_make_short2_undef(_:))

### Common Functions

- [func simd_abs(simd_short2) -> simd_short2](/documentation/simd/simd_abs(_:)-88dfi)
- [func simd_clamp(simd_short2, simd_short2, simd_short2) -> simd_short2](/documentation/simd/simd_clamp(_:_:_:)-5qqhe)
- [func simd_equal(simd_short2, simd_short2) -> simd_bool](/documentation/simd/simd_equal(_:_:)-6gad6)

### Reduce Functions

- [func simd_reduce_min(simd_short2) -> Int16](/documentation/simd/simd_reduce_min(_:)-49c4w)
- [func simd_reduce_max(simd_short2) -> Int16](/documentation/simd/simd_reduce_max(_:)-4kmuw)
- [func simd_reduce_add(simd_short2) -> Int16](/documentation/simd/simd_reduce_add(_:)-2q65m)

### Extrema Functions

- [func simd_min(simd_short2, simd_short2) -> simd_short2](/documentation/simd/simd_min(_:_:)-13ip4)
- [func simd_max(simd_short2, simd_short2) -> simd_short2](/documentation/simd/simd_max(_:_:)-6w9rg)

### Logic and Bitwise Functions

- [func simd_any(simd_short2) -> simd_bool](/documentation/simd/simd_any(_:)-64jj5)
- [func simd_all(simd_short2) -> simd_bool](/documentation/simd/simd_all(_:)-1d5nj)
- [func simd_bitselect(simd_short2, simd_short2, simd_short2) -> simd_short2](/documentation/simd/simd_bitselect(_:_:_:)-625jo)

### Alternative Type Alias

- [vector_short2](/documentation/simd/vector_short2)
- [simd_short3](/documentation/simd/simd_short3)

### Functions to Create Three-Element Vectors From Other Vectors

- [func simd_make_short3(simd_short2) -> simd_short3](/documentation/simd/simd_make_short3(_:)-c59z)
- [func simd_make_short3(simd_short3) -> simd_short3](/documentation/simd/simd_make_short3(_:)-gyam)
- [func simd_make_short3(simd_short4) -> simd_short3](/documentation/simd/simd_make_short3(_:)-x9n1)
- [func simd_make_short3(simd_short8) -> simd_short3](/documentation/simd/simd_make_short3(_:)-1capt)
- [func simd_make_short3(simd_short16) -> simd_short3](/documentation/simd/simd_make_short3(_:)-9l6v8)
- [func simd_make_short3(simd_short32) -> simd_short3](/documentation/simd/simd_make_short3(_:)-70om7)
- [func simd_make_short3_undef(simd_short2) -> simd_short3](/documentation/simd/simd_make_short3_undef(_:)-87ju7)

### Functions to Create Three-Element Vectors From Scalar Values

- [func simd_make_short3(Int16) -> simd_short3](/documentation/simd/simd_make_short3(_:)-2ux4i)
- [func simd_make_short3(Int16, Int16, Int16) -> simd_short3](/documentation/simd/simd_make_short3(_:_:_:))
- [func simd_make_short3_undef(Int16) -> simd_short3](/documentation/simd/simd_make_short3_undef(_:)-5n83n)

### Functions to Create Three-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_short3(simd_short2, Int16) -> simd_short3](/documentation/simd/simd_make_short3(_:_:)-7dmp4)
- [func simd_make_short3(Int16, simd_short2) -> simd_short3](/documentation/simd/simd_make_short3(_:_:)-9bk9v)

### Common Functions

- [func simd_abs(simd_short3) -> simd_short3](/documentation/simd/simd_abs(_:)-8d6jr)
- [func simd_clamp(simd_short3, simd_short3, simd_short3) -> simd_short3](/documentation/simd/simd_clamp(_:_:_:)-7wmh7)
- [func simd_equal(simd_short3, simd_short3) -> simd_bool](/documentation/simd/simd_equal(_:_:)-40ux3)

### Reduce Functions

- [func simd_reduce_min(simd_short3) -> Int16](/documentation/simd/simd_reduce_min(_:)-466g9)
- [func simd_reduce_max(simd_short3) -> Int16](/documentation/simd/simd_reduce_max(_:)-4hewh)
- [func simd_reduce_add(simd_short3) -> Int16](/documentation/simd/simd_reduce_add(_:)-2v1tf)

### Extrema Functions

- [func simd_min(simd_short3, simd_short3) -> simd_short3](/documentation/simd/simd_min(_:_:)-9vz62)
- [func simd_max(simd_short3, simd_short3) -> simd_short3](/documentation/simd/simd_max(_:_:)-8id6w)

### Logic and Bitwise Functions

- [func simd_any(simd_short3) -> simd_bool](/documentation/simd/simd_any(_:)-69f7s)
- [func simd_all(simd_short3) -> simd_bool](/documentation/simd/simd_all(_:)-1ahau)
- [func simd_bitselect(simd_short3, simd_short3, simd_short3) -> simd_short3](/documentation/simd/simd_bitselect(_:_:_:)-8m8ti)

### Alternative Type Alias

- [vector_short3](/documentation/simd/vector_short3)
- [simd_short32](/documentation/simd/simd_short32)

### Functions to Create Thirty Two-Element Vectors From Other Vectors

- [func simd_make_short32(simd_short2) -> simd_short32](/documentation/simd/simd_make_short32(_:)-ubpt)
- [func simd_make_short32(simd_short3) -> simd_short32](/documentation/simd/simd_make_short32(_:)-xjmw)
- [func simd_make_short32(simd_short4) -> simd_short32](/documentation/simd/simd_make_short32(_:)-9757)
- [func simd_make_short32(simd_short8) -> simd_short32](/documentation/simd/simd_make_short32(_:)-1eywv)
- [func simd_make_short32(simd_short16) -> simd_short32](/documentation/simd/simd_make_short32(_:)-9m5sz)
- [func simd_make_short32(simd_short32) -> simd_short32](/documentation/simd/simd_make_short32(_:)-94o20)
- [func simd_make_short32(simd_short16, simd_short16) -> simd_short32](/documentation/simd/simd_make_short32(_:_:))
- [func simd_make_short32_undef(simd_short2) -> simd_short32](/documentation/simd/simd_make_short32_undef(_:)-lops)
- [func simd_make_short32_undef(simd_short3) -> simd_short32](/documentation/simd/simd_make_short32_undef(_:)-hws9)
- [func simd_make_short32_undef(simd_short4) -> simd_short32](/documentation/simd/simd_make_short32_undef(_:)-ri8y)
- [func simd_make_short32_undef(simd_short8) -> simd_short32](/documentation/simd/simd_make_short32_undef(_:)-169di)
- [func simd_make_short32_undef(simd_short16) -> simd_short32](/documentation/simd/simd_make_short32_undef(_:)-435zw)

### Functions to Create Thirty Two-Element Vectors From Scalar Values

- [func simd_make_short32(Int16) -> simd_short32](/documentation/simd/simd_make_short32(_:)-8b798)
- [func simd_make_short32_undef(Int16) -> simd_short32](/documentation/simd/simd_make_short32_undef(_:)-94vzp)

### Common Functions

- [func simd_abs(simd_short32) -> simd_short32](/documentation/simd/simd_abs(_:)-2cf7j)
- [func simd_clamp(simd_short32, simd_short32, simd_short32) -> simd_short32](/documentation/simd/simd_clamp(_:_:_:)-v73)
- [func simd_equal(simd_short32, simd_short32) -> simd_bool](/documentation/simd/simd_equal(_:_:)-2cuv8)

### Reduce Functions

- [func simd_reduce_min(simd_short32) -> Int16](/documentation/simd/simd_reduce_min(_:)-2az34)
- [func simd_reduce_max(simd_short32) -> Int16](/documentation/simd/simd_reduce_max(_:)-9j1wo)
- [func simd_reduce_add(simd_short32) -> Int16](/documentation/simd/simd_reduce_add(_:)-1v4iv)

### Extrema Functions

- [func simd_min(simd_short32, simd_short32) -> simd_short32](/documentation/simd/simd_min(_:_:)-6joky)
- [func simd_max(simd_short32, simd_short32) -> simd_short32](/documentation/simd/simd_max(_:_:)-8macj)

### Logic and Bitwise Functions

- [func simd_any(simd_short32) -> simd_bool](/documentation/simd/simd_any(_:)-3b445)
- [func simd_all(simd_short32) -> simd_bool](/documentation/simd/simd_all(_:)-1kcj7)
- [func simd_bitselect(simd_short32, simd_short32, simd_short32) -> simd_short32](/documentation/simd/simd_bitselect(_:_:_:)-9so3n)

### Alternative Type Alias

- [vector_short32](/documentation/simd/vector_short32)
- [simd_short4](/documentation/simd/simd_short4)

### Functions to Create Four-Element Vectors From Other Vectors

- [func simd_make_short4(simd_short2) -> simd_short4](/documentation/simd/simd_make_short4(_:)-6bvw4)
- [func simd_make_short4(simd_short3) -> simd_short4](/documentation/simd/simd_make_short4(_:)-68qml)
- [func simd_make_short4(simd_short4) -> simd_short4](/documentation/simd/simd_make_short4(_:)-662gm)
- [func simd_make_short4(simd_short8) -> simd_short4](/documentation/simd/simd_make_short4(_:)-5rbcq)
- [func simd_make_short4(simd_short16) -> simd_short4](/documentation/simd/simd_make_short4(_:)-9muje)
- [func simd_make_short4(simd_short32) -> simd_short4](/documentation/simd/simd_make_short4(_:)-7tcxn)
- [func simd_make_short4(simd_short2, simd_short2) -> simd_short4](/documentation/simd/simd_make_short4(_:_:)-8h120)
- [func simd_make_short4_undef(simd_short2) -> simd_short4](/documentation/simd/simd_make_short4_undef(_:)-8g0xr)
- [func simd_make_short4_undef(simd_short3) -> simd_short4](/documentation/simd/simd_make_short4_undef(_:)-8imcm)

### Functions to Create Four-Element Vectors From Scalar Values

- [func simd_make_short4(Int16) -> simd_short4](/documentation/simd/simd_make_short4(_:)-1emve)
- [func simd_make_short4(Int16, Int16, Int16, Int16) -> simd_short4](/documentation/simd/simd_make_short4(_:_:_:_:))
- [func simd_make_short4_undef(Int16) -> simd_short4](/documentation/simd/simd_make_short4_undef(_:)-36i14)

### Functions to Create Four-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_short4(simd_short2, Int16, Int16) -> simd_short4](/documentation/simd/simd_make_short4(_:_:_:)-6v1lj)
- [func simd_make_short4(simd_short3, Int16) -> simd_short4](/documentation/simd/simd_make_short4(_:_:)-8tpr6)
- [func simd_make_short4(Int16, Int16, simd_short2) -> simd_short4](/documentation/simd/simd_make_short4(_:_:_:)-34dcj)
- [func simd_make_short4(Int16, simd_short2, Int16) -> simd_short4](/documentation/simd/simd_make_short4(_:_:_:)-21v12)
- [func simd_make_short4(Int16, simd_short3) -> simd_short4](/documentation/simd/simd_make_short4(_:_:)-46aby)

### Common Functions

- [func simd_abs(simd_short4) -> simd_short4](/documentation/simd/simd_abs(_:)-81n9o)
- [func simd_clamp(simd_short4, simd_short4, simd_short4) -> simd_short4](/documentation/simd/simd_clamp(_:_:_:)-3fip1)
- [func simd_equal(simd_short4, simd_short4) -> simd_bool](/documentation/simd/simd_equal(_:_:)-51wsu)

### Reduce Functions

- [func simd_reduce_min(simd_short4) -> Int16](/documentation/simd/simd_reduce_min(_:)-4uj62)
- [func simd_reduce_max(simd_short4) -> Int16](/documentation/simd/simd_reduce_max(_:)-4qgga)
- [func simd_reduce_add(simd_short4) -> Int16](/documentation/simd/simd_reduce_add(_:)-2y9o8)

### Extrema Functions

- [func simd_min(simd_short4, simd_short4) -> simd_short4](/documentation/simd/simd_min(_:_:)-3w6s9)
- [func simd_max(simd_short4, simd_short4) -> simd_short4](/documentation/simd/simd_max(_:_:)-7xxnr)

### Logic and Bitwise Functions

- [func simd_any(simd_short4) -> simd_bool](/documentation/simd/simd_any(_:)-6cn5f)
- [func simd_all(simd_short4) -> simd_bool](/documentation/simd/simd_all(_:)-1k2rx)
- [func simd_bitselect(simd_short4, simd_short4, simd_short4) -> simd_short4](/documentation/simd/simd_bitselect(_:_:_:)-u3k7)

### Alternative Type Alias

- [vector_short4](/documentation/simd/vector_short4)
- [simd_short8](/documentation/simd/simd_short8)

### Functions to Create Eight-Element Vectors From Other Vectors

- [func simd_make_short8(simd_short2) -> simd_short8](/documentation/simd/simd_make_short8(_:)-600rc)
- [func simd_make_short8(simd_short3) -> simd_short8](/documentation/simd/simd_make_short8(_:)-5wv29)
- [func simd_make_short8(simd_short4) -> simd_short8](/documentation/simd/simd_make_short8(_:)-6l7oy)
- [func simd_make_short8(simd_short8) -> simd_short8](/documentation/simd/simd_make_short8(_:)-5gjta)
- [func simd_make_short8(simd_short16) -> simd_short8](/documentation/simd/simd_make_short8(_:)-22n5y)
- [func simd_make_short8(simd_short32) -> simd_short8](/documentation/simd/simd_make_short8(_:)-8mc9h)
- [func simd_make_short8(simd_short4, simd_short4) -> simd_short8](/documentation/simd/simd_make_short8(_:_:))
- [func simd_make_short8_undef(simd_short2) -> simd_short8](/documentation/simd/simd_make_short8_undef(_:)-54hbi)
- [func simd_make_short8_undef(simd_short3) -> simd_short8](/documentation/simd/simd_make_short8_undef(_:)-57mlz)
- [func simd_make_short8_undef(simd_short4) -> simd_short8](/documentation/simd/simd_make_short8_undef(_:)-5ny5g)

### Functions to Create Eight-Element Vectors From Scalar Values

- [func simd_make_short8(Int16) -> simd_short8](/documentation/simd/simd_make_short8(_:)-1jz7f)
- [func simd_make_short8_undef(Int16) -> simd_short8](/documentation/simd/simd_make_short8_undef(_:)-7945n)

### Common Functions

- [func simd_abs(simd_short8) -> simd_short8](/documentation/simd/simd_abs(_:)-7otzk)
- [func simd_clamp(simd_short8, simd_short8, simd_short8) -> simd_short8](/documentation/simd/simd_clamp(_:_:_:)-3cc2g)
- [func simd_equal(simd_short8, simd_short8) -> simd_bool](/documentation/simd/simd_equal(_:_:)-4n1gi)

### Reduce Functions

- [func simd_reduce_min(simd_short8) -> Int16](/documentation/simd/simd_reduce_min(_:)-3ordy)
- [func simd_reduce_max(simd_short8) -> Int16](/documentation/simd/simd_reduce_max(_:)-55r7y)
- [func simd_reduce_add(simd_short8) -> Int16](/documentation/simd/simd_reduce_add(_:)-3bda4)

### Extrema Functions

- [func simd_min(simd_short8, simd_short8) -> simd_short8](/documentation/simd/simd_min(_:_:)-40hpn)
- [func simd_max(simd_short8, simd_short8) -> simd_short8](/documentation/simd/simd_max(_:_:)-1u1su)

### Logic and Bitwise Functions

- [func simd_any(simd_short8) -> simd_bool](/documentation/simd/simd_any(_:)-6pqh3)
- [func simd_all(simd_short8) -> simd_bool](/documentation/simd/simd_all(_:)-1ytzd)
- [func simd_bitselect(simd_short8, simd_short8, simd_short8) -> simd_short8](/documentation/simd/simd_bitselect(_:_:_:)-1vm6y)

### Alternative Type Alias

- [vector_short8](/documentation/simd/vector_short8)
- [simd_uchar1](/documentation/simd/simd_uchar1)
- [simd_uchar16](/documentation/simd/simd_uchar16)

### Functions to Create Sixteen-Element Vectors From Other Vectors

- [func simd_make_uchar16(simd_uchar2) -> simd_uchar16](/documentation/simd/simd_make_uchar16(_:)-3fz5p)
- [func simd_make_uchar16(simd_uchar3) -> simd_uchar16](/documentation/simd/simd_make_uchar16(_:)-3d3no)
- [func simd_make_uchar16(simd_uchar4) -> simd_uchar16](/documentation/simd/simd_make_uchar16(_:)-39lkf)
- [func simd_make_uchar16(simd_uchar8) -> simd_uchar16](/documentation/simd/simd_make_uchar16(_:)-2v4kz)
- [func simd_make_uchar16(simd_uchar16) -> simd_uchar16](/documentation/simd/simd_make_uchar16(_:)-3jakr)
- [func simd_make_uchar16(simd_uchar32) -> simd_uchar16](/documentation/simd/simd_make_uchar16(_:)-1q2p8)
- [func simd_make_uchar16(simd_uchar64) -> simd_uchar16](/documentation/simd/simd_make_uchar16(_:)-4u0bo)
- [func simd_make_uchar16(simd_uchar8, simd_uchar8) -> simd_uchar16](/documentation/simd/simd_make_uchar16(_:_:))
- [func simd_make_uchar16_undef(simd_uchar2) -> simd_uchar16](/documentation/simd/simd_make_uchar16_undef(_:)-7pk27)
- [func simd_make_uchar16_undef(simd_uchar3) -> simd_uchar16](/documentation/simd/simd_make_uchar16_undef(_:)-7sziu)
- [func simd_make_uchar16_undef(simd_uchar4) -> simd_uchar16](/documentation/simd/simd_make_uchar16_undef(_:)-7jo0t)
- [func simd_make_uchar16_undef(simd_uchar8) -> simd_uchar16](/documentation/simd/simd_make_uchar16_undef(_:)-74mxt)

### Functions to Create Sixteen-Element Vectors From Scalar Values

- [func simd_make_uchar16(UInt8) -> simd_uchar16](/documentation/simd/simd_make_uchar16(_:)-v6ux)
- [func simd_make_uchar16_undef(UInt8) -> simd_uchar16](/documentation/simd/simd_make_uchar16_undef(_:)-4x6v6)

### Common Functions

- [func simd_clamp(simd_uchar16, simd_uchar16, simd_uchar16) -> simd_uchar16](/documentation/simd/simd_clamp(_:_:_:)-1zlhc)
- [func simd_equal(simd_uchar16, simd_uchar16) -> simd_bool](/documentation/simd/simd_equal(_:_:)-6la77)

### Reduce Functions

- [func simd_reduce_min(simd_uchar16) -> UInt8](/documentation/simd/simd_reduce_min(_:)-3d193)
- [func simd_reduce_max(simd_uchar16) -> UInt8](/documentation/simd/simd_reduce_max(_:)-8inet)
- [func simd_reduce_add(simd_uchar16) -> UInt8](/documentation/simd/simd_reduce_add(_:)-7n460)

### Extrema Functions

- [func simd_min(simd_uchar16, simd_uchar16) -> simd_uchar16](/documentation/simd/simd_min(_:_:)-8haop)
- [func simd_max(simd_uchar16, simd_uchar16) -> simd_uchar16](/documentation/simd/simd_max(_:_:)-248h3)

### Logic and Bitwise Functions

- [func simd_any(simd_uchar16) -> simd_bool](/documentation/simd/simd_any(_:)-933sa)
- [func simd_all(simd_uchar16) -> simd_bool](/documentation/simd/simd_all(_:)-ikbg)
- [func simd_bitselect(simd_uchar16, simd_uchar16, simd_char16) -> simd_uchar16](/documentation/simd/simd_bitselect(_:_:_:)-9i5ku)

### Alternative Type Alias

- [vector_uchar16](/documentation/simd/vector_uchar16)
- [simd_uchar2](/documentation/simd/simd_uchar2)

### Functions to Create Two-Element Vectors From Other Vectors

- [func simd_make_uchar2(simd_uchar2) -> simd_uchar2](/documentation/simd/simd_make_uchar2(_:)-5a6cb)
- [func simd_make_uchar2(simd_uchar3) -> simd_uchar2](/documentation/simd/simd_make_uchar2(_:)-5dlsy)
- [func simd_make_uchar2(simd_uchar4) -> simd_uchar2](/documentation/simd/simd_make_uchar2(_:)-5vkwh)
- [func simd_make_uchar2(simd_uchar8) -> simd_uchar2](/documentation/simd/simd_make_uchar2(_:)-4p97x)
- [func simd_make_uchar2(simd_uchar16) -> simd_uchar2](/documentation/simd/simd_make_uchar2(_:)-6etds)
- [func simd_make_uchar2(simd_uchar32) -> simd_uchar2](/documentation/simd/simd_make_uchar2(_:)-4hies)
- [func simd_make_uchar2(simd_uchar64) -> simd_uchar2](/documentation/simd/simd_make_uchar2(_:)-1bfr0)

### Functions to Create Two-Element Vectors From Scalar Values

- [func simd_make_uchar2(UInt8) -> simd_uchar2](/documentation/simd/simd_make_uchar2(_:)-152cz)
- [func simd_make_uchar2(UInt8, UInt8) -> simd_uchar2](/documentation/simd/simd_make_uchar2(_:_:))
- [func simd_make_uchar2_undef(UInt8) -> simd_uchar2](/documentation/simd/simd_make_uchar2_undef(_:))

### Common Functions

- [func simd_clamp(simd_uchar2, simd_uchar2, simd_uchar2) -> simd_uchar2](/documentation/simd/simd_clamp(_:_:_:)-71hrv)
- [func simd_equal(simd_uchar2, simd_uchar2) -> simd_bool](/documentation/simd/simd_equal(_:_:)-7ujh6)

### Reduce Functions

- [func simd_reduce_min(simd_uchar2) -> UInt8](/documentation/simd/simd_reduce_min(_:)-49quo)
- [func simd_reduce_max(simd_uchar2) -> UInt8](/documentation/simd/simd_reduce_max(_:)-4khx4)
- [func simd_reduce_add(simd_uchar2) -> UInt8](/documentation/simd/simd_reduce_add(_:)-2q16y)

### Extrema Functions

- [func simd_min(simd_uchar2, simd_uchar2) -> simd_uchar2](/documentation/simd/simd_min(_:_:)-45w1z)
- [func simd_max(simd_uchar2, simd_uchar2) -> simd_uchar2](/documentation/simd/simd_max(_:_:)-8i357)

### Logic and Bitwise Functions

- [func simd_any(simd_uchar2) -> simd_bool](/documentation/simd/simd_any(_:)-64ekh)
- [func simd_all(simd_uchar2) -> simd_bool](/documentation/simd/simd_all(_:)-1dafz)
- [func simd_bitselect(simd_uchar2, simd_uchar2, simd_char2) -> simd_uchar2](/documentation/simd/simd_bitselect(_:_:_:)-2yxn9)

### Alternative Type Alias

- [vector_uchar2](/documentation/simd/vector_uchar2)
- [simd_uchar3](/documentation/simd/simd_uchar3)

### Functions to Create Three-Element Vectors From Other Vectors

- [func simd_make_uchar3(simd_uchar2) -> simd_uchar3](/documentation/simd/simd_make_uchar3(_:)-4qkxz)
- [func simd_make_uchar3(simd_uchar3) -> simd_uchar3](/documentation/simd/simd_make_uchar3(_:)-4nmxq)
- [func simd_make_uchar3(simd_uchar4) -> simd_uchar3](/documentation/simd/simd_make_uchar3(_:)-45nsd)
- [func simd_make_uchar3(simd_uchar8) -> simd_uchar3](/documentation/simd/simd_make_uchar3(_:)-3sucp)
- [func simd_make_uchar3(simd_uchar16) -> simd_uchar3](/documentation/simd/simd_make_uchar3(_:)-90ge7)
- [func simd_make_uchar3(simd_uchar32) -> simd_uchar3](/documentation/simd/simd_make_uchar3(_:)-38lno)
- [func simd_make_uchar3(simd_uchar64) -> simd_uchar3](/documentation/simd/simd_make_uchar3(_:)-3p7i8)
- [func simd_make_uchar3_undef(simd_uchar2) -> simd_uchar3](/documentation/simd/simd_make_uchar3_undef(_:)-99t25)

### Functions to Create Three-Element Vectors From Scalar Values

- [func simd_make_uchar3(UInt8) -> simd_uchar3](/documentation/simd/simd_make_uchar3(_:)-bybh)
- [func simd_make_uchar3(UInt8, UInt8, UInt8) -> simd_uchar3](/documentation/simd/simd_make_uchar3(_:_:_:))
- [func simd_make_uchar3_undef(UInt8) -> simd_uchar3](/documentation/simd/simd_make_uchar3_undef(_:)-562ub)

### Functions to Create Three-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_uchar3(simd_uchar2, UInt8) -> simd_uchar3](/documentation/simd/simd_make_uchar3(_:_:)-5tgih)
- [func simd_make_uchar3(UInt8, simd_uchar2) -> simd_uchar3](/documentation/simd/simd_make_uchar3(_:_:)-2m5x7)

### Common Functions

- [func simd_clamp(simd_uchar3, simd_uchar3, simd_uchar3) -> simd_uchar3](/documentation/simd/simd_clamp(_:_:_:)-6h8i3)
- [func simd_equal(simd_uchar3, simd_uchar3) -> simd_bool](/documentation/simd/simd_equal(_:_:)-8iga0)

### Reduce Functions

- [func simd_reduce_min(simd_uchar3) -> UInt8](/documentation/simd/simd_reduce_min(_:)-46bd5)
- [func simd_reduce_max(simd_uchar3) -> UInt8](/documentation/simd/simd_reduce_max(_:)-4gzsh)
- [func simd_reduce_add(simd_uchar3) -> UInt8](/documentation/simd/simd_reduce_add(_:)-2v6nn)

### Extrema Functions

- [func simd_min(simd_uchar3, simd_uchar3) -> simd_uchar3](/documentation/simd/simd_min(_:_:)-8h62y)
- [func simd_max(simd_uchar3, simd_uchar3) -> simd_uchar3](/documentation/simd/simd_max(_:_:)-8ylny)

### Logic and Bitwise Functions

- [func simd_any(simd_uchar3) -> simd_bool](/documentation/simd/simd_any(_:)-69k4o)
- [func simd_all(simd_uchar3) -> simd_bool](/documentation/simd/simd_all(_:)-1aceu)
- [func simd_bitselect(simd_uchar3, simd_uchar3, simd_char3) -> simd_uchar3](/documentation/simd/simd_bitselect(_:_:_:)-2syfj)

### Alternative Type Alias

- [vector_uchar3](/documentation/simd/vector_uchar3)
- [simd_uchar32](/documentation/simd/simd_uchar32)

### Functions to Create Thirty Two-Element Vectors From Other Vectors

- [func simd_make_uchar32(simd_uchar2) -> simd_uchar32](/documentation/simd/simd_make_uchar32(_:)-ycg1)
- [func simd_make_uchar32(simd_uchar3) -> simd_uchar32](/documentation/simd/simd_make_uchar32(_:)-uuk8)
- [func simd_make_uchar32(simd_uchar4) -> simd_uchar32](/documentation/simd/simd_make_uchar32(_:)-cvfv)
- [func simd_make_uchar32(simd_uchar8) -> simd_uchar32](/documentation/simd/simd_make_uchar32(_:)-lv3)
- [func simd_make_uchar32(simd_uchar16) -> simd_uchar32](/documentation/simd/simd_make_uchar32(_:)-94jec)
- [func simd_make_uchar32(simd_uchar32) -> simd_uchar32](/documentation/simd/simd_make_uchar32(_:)-3c53d)
- [func simd_make_uchar32(simd_uchar64) -> simd_uchar32](/documentation/simd/simd_make_uchar32(_:)-3tap7)
- [func simd_make_uchar32(simd_uchar16, simd_uchar16) -> simd_uchar32](/documentation/simd/simd_make_uchar32(_:_:))
- [func simd_make_uchar32_undef(simd_uchar2) -> simd_uchar32](/documentation/simd/simd_make_uchar32_undef(_:)-86jc5)
- [func simd_make_uchar32_undef(simd_uchar3) -> simd_uchar32](/documentation/simd/simd_make_uchar32_undef(_:)-89hb0)
- [func simd_make_uchar32_undef(simd_uchar4) -> simd_uchar32](/documentation/simd/simd_make_uchar32_undef(_:)-8emxj)
- [func simd_make_uchar32_undef(simd_uchar8) -> simd_uchar32](/documentation/simd/simd_make_uchar32_undef(_:)-78b83)
- [func simd_make_uchar32_undef(simd_uchar16) -> simd_uchar32](/documentation/simd/simd_make_uchar32_undef(_:)-9vswr)

### Functions to Create Thirty Two-Element Vectors From Scalar Values

- [func simd_make_uchar32(UInt8) -> simd_uchar32](/documentation/simd/simd_make_uchar32(_:)-8z2lu)
- [func simd_make_uchar32_undef(UInt8) -> simd_uchar32](/documentation/simd/simd_make_uchar32_undef(_:)-6klno)

### Common Functions

- [func simd_clamp(simd_uchar32, simd_uchar32, simd_uchar32) -> simd_uchar32](/documentation/simd/simd_clamp(_:_:_:)-3bfcx)
- [func simd_equal(simd_uchar32, simd_uchar32) -> simd_bool](/documentation/simd/simd_equal(_:_:)-qmif)

### Reduce Functions

- [func simd_reduce_min(simd_uchar32) -> UInt8](/documentation/simd/simd_reduce_min(_:)-2b45c)
- [func simd_reduce_max(simd_uchar32) -> UInt8](/documentation/simd/simd_reduce_max(_:)-9iwy0)
- [func simd_reduce_add(simd_uchar32) -> UInt8](/documentation/simd/simd_reduce_add(_:)-1updz)

### Extrema Functions

- [func simd_min(simd_uchar32, simd_uchar32) -> simd_uchar32](/documentation/simd/simd_min(_:_:)-4b2i2)
- [func simd_max(simd_uchar32, simd_uchar32) -> simd_uchar32](/documentation/simd/simd_max(_:_:)-xuo)

### Logic and Bitwise Functions

- [func simd_any(simd_uchar32) -> simd_bool](/documentation/simd/simd_any(_:)-3apcl)
- [func simd_all(simd_uchar32) -> simd_bool](/documentation/simd/simd_all(_:)-1khgz)
- [func simd_bitselect(simd_uchar32, simd_uchar32, simd_char32) -> simd_uchar32](/documentation/simd/simd_bitselect(_:_:_:)-49vzj)

### Alternative Type Alias

- [vector_uchar32](/documentation/simd/vector_uchar32)
- [simd_uchar4](/documentation/simd/simd_uchar4)

### Functions to Create Four-Element Vectors From Other Vectors

- [func simd_make_uchar4(simd_uchar2) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:)-4hwy4)
- [func simd_make_uchar4(simd_uchar3) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:)-4lf1x)
- [func simd_make_uchar4(simd_uchar4) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:)-3x2fa)
- [func simd_make_uchar4(simd_uchar8) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:)-3i1f6)
- [func simd_make_uchar4(simd_uchar16) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:)-174yg)
- [func simd_make_uchar4(simd_uchar32) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:)-6662s)
- [func simd_make_uchar4(simd_uchar64) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:)-4d9x4)
- [func simd_make_uchar4(simd_uchar2, simd_uchar2) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:_:)-29ka1)
- [func simd_make_uchar4_undef(simd_uchar2) -> simd_uchar4](/documentation/simd/simd_make_uchar4_undef(_:)-5we7j)
- [func simd_make_uchar4_undef(simd_uchar3) -> simd_uchar4](/documentation/simd/simd_make_uchar4_undef(_:)-5tfyu)

### Functions to Create Four-Element Vectors From Scalar Values

- [func simd_make_uchar4(UInt8) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:)-7gszj)
- [func simd_make_uchar4(UInt8, UInt8, UInt8, UInt8) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:_:_:_:))
- [func simd_make_uchar4_undef(UInt8) -> simd_uchar4](/documentation/simd/simd_make_uchar4_undef(_:)-7uno)

### Functions to Create Four-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_uchar4(simd_uchar2, UInt8, UInt8) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:_:_:)-5x9io)
- [func simd_make_uchar4(simd_uchar3, UInt8) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:_:)-3zlj2)
- [func simd_make_uchar4(UInt8, UInt8, simd_uchar2) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:_:_:)-9rqjk)
- [func simd_make_uchar4(UInt8, simd_uchar2, UInt8) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:_:_:)-53d7w)
- [func simd_make_uchar4(UInt8, simd_uchar3) -> simd_uchar4](/documentation/simd/simd_make_uchar4(_:_:)-4sdi7)

### Common Functions

- [func simd_clamp(simd_uchar4, simd_uchar4, simd_uchar4) -> simd_uchar4](/documentation/simd/simd_clamp(_:_:_:)-7gs2x)
- [func simd_equal(simd_uchar4, simd_uchar4) -> simd_bool](/documentation/simd/simd_equal(_:_:)-4wf8b)

### Reduce Functions

- [func simd_reduce_min(simd_uchar4) -> UInt8](/documentation/simd/simd_reduce_min(_:)-4uo6i)
- [func simd_reduce_max(simd_uchar4) -> UInt8](/documentation/simd/simd_reduce_max(_:)-4qv6y)
- [func simd_reduce_add(simd_uchar4) -> UInt8](/documentation/simd/simd_reduce_add(_:)-2yos8)

### Extrema Functions

- [func simd_min(simd_uchar4, simd_uchar4) -> simd_uchar4](/documentation/simd/simd_min(_:_:)-9muwy)
- [func simd_max(simd_uchar4, simd_uchar4) -> simd_uchar4](/documentation/simd/simd_max(_:_:)-2f249)

### Logic and Bitwise Functions

- [func simd_any(simd_uchar4) -> simd_bool](/documentation/simd/simd_any(_:)-6d22b)
- [func simd_all(simd_uchar4) -> simd_bool](/documentation/simd/simd_all(_:)-1jo4t)
- [func simd_bitselect(simd_uchar4, simd_uchar4, simd_char4) -> simd_uchar4](/documentation/simd/simd_bitselect(_:_:_:)-46k0t)

### Alternative Type Alias

- [vector_uchar4](/documentation/simd/vector_uchar4)
- [simd_uchar64](/documentation/simd/simd_uchar64)

### Functions to Create Sixty Four-Element Vectors From Other Vectors

- [func simd_make_uchar64(simd_uchar2) -> simd_uchar64](/documentation/simd/simd_make_uchar64(_:)-57u64)
- [func simd_make_uchar64(simd_uchar3) -> simd_uchar64](/documentation/simd/simd_make_uchar64(_:)-5apn9)
- [func simd_make_uchar64(simd_uchar4) -> simd_uchar64](/documentation/simd/simd_make_uchar64(_:)-51eby)
- [func simd_make_uchar64(simd_uchar8) -> simd_uchar64](/documentation/simd/simd_make_uchar64(_:)-65i5u)
- [func simd_make_uchar64(simd_uchar16) -> simd_uchar64](/documentation/simd/simd_make_uchar64(_:)-3wfeh)
- [func simd_make_uchar64(simd_uchar32) -> simd_uchar64](/documentation/simd/simd_make_uchar64(_:)-56lh8)
- [func simd_make_uchar64(simd_uchar64) -> simd_uchar64](/documentation/simd/simd_make_uchar64(_:)-1g5oc)
- [func simd_make_uchar64(simd_uchar32, simd_uchar32) -> simd_uchar64](/documentation/simd/simd_make_uchar64(_:_:))
- [func simd_make_uchar64_undef(simd_uchar2) -> simd_uchar64](/documentation/simd/simd_make_uchar64_undef(_:)-8lvix)
- [func simd_make_uchar64_undef(simd_uchar3) -> simd_uchar64](/documentation/simd/simd_make_uchar64_undef(_:)-8ig34)
- [func simd_make_uchar64_undef(simd_uchar4) -> simd_uchar64](/documentation/simd/simd_make_uchar64_undef(_:)-8fhu3)
- [func simd_make_uchar64_undef(simd_uchar8) -> simd_uchar64](/documentation/simd/simd_make_uchar64_undef(_:)-9jm47)
- [func simd_make_uchar64_undef(simd_uchar16) -> simd_uchar64](/documentation/simd/simd_make_uchar64_undef(_:)-p0tj)
- [func simd_make_uchar64_undef(simd_uchar32) -> simd_uchar64](/documentation/simd/simd_make_uchar64_undef(_:)-9ldf2)

### Functions to Create Sixty Four-Element Vectors From Scalar Values

- [func simd_make_uchar64(UInt8) -> simd_uchar64](/documentation/simd/simd_make_uchar64(_:)-9d1w7)
- [func simd_make_uchar64_undef(UInt8) -> simd_uchar64](/documentation/simd/simd_make_uchar64_undef(_:)-6vlwv)

### Reduce Functions

- [func simd_reduce_min(simd_uchar64) -> UInt8](/documentation/simd/simd_reduce_min(_:)-jpn5)
- [func simd_reduce_max(simd_uchar64) -> UInt8](/documentation/simd/simd_reduce_max(_:)-micz)
- [func simd_reduce_add(simd_uchar64) -> UInt8](/documentation/simd/simd_reduce_add(_:)-936l4)

### Extrema Functions

- [func simd_min(simd_uchar64, simd_uchar64) -> simd_uchar64](/documentation/simd/simd_min(_:_:)-ep1f)
- [func simd_max(simd_uchar64, simd_uchar64) -> simd_uchar64](/documentation/simd/simd_max(_:_:)-5la8o)

### Common Functions

- [func simd_clamp(simd_uchar64, simd_uchar64, simd_uchar64) -> simd_uchar64](/documentation/simd/simd_clamp(_:_:_:)-52h9h)
- [func simd_equal(simd_uchar64, simd_uchar64) -> simd_bool](/documentation/simd/simd_equal(_:_:)-494kp)

### Logic and Bitwise Functions

- [func simd_any(simd_uchar64) -> simd_bool](/documentation/simd/simd_any(_:)-jl1j)
- [func simd_all(simd_uchar64) -> simd_bool](/documentation/simd/simd_all(_:)-2m0jp)
- [func simd_bitselect(simd_uchar64, simd_uchar64, simd_char64) -> simd_uchar64](/documentation/simd/simd_bitselect(_:_:_:)-2bway)
- [simd_uchar8](/documentation/simd/simd_uchar8)

### Functions to Create Eight-Element Vectors From Other Vectors

- [func simd_make_uchar8(simd_uchar2) -> simd_uchar8](/documentation/simd/simd_make_uchar8(_:)-5zumf)
- [func simd_make_uchar8(simd_uchar3) -> simd_uchar8](/documentation/simd/simd_make_uchar8(_:)-62sn2)
- [func simd_make_uchar8(simd_uchar4) -> simd_uchar8](/documentation/simd/simd_make_uchar8(_:)-65qph)
- [func simd_make_uchar8(simd_uchar8) -> simd_uchar8](/documentation/simd/simd_make_uchar8(_:)-51mi9)
- [func simd_make_uchar8(simd_uchar16) -> simd_uchar8](/documentation/simd/simd_make_uchar8(_:)-5p2su)
- [func simd_make_uchar8(simd_uchar32) -> simd_uchar8](/documentation/simd/simd_make_uchar8(_:)-6svfy)
- [func simd_make_uchar8(simd_uchar64) -> simd_uchar8](/documentation/simd/simd_make_uchar8(_:)-75pea)
- [func simd_make_uchar8(simd_uchar4, simd_uchar4) -> simd_uchar8](/documentation/simd/simd_make_uchar8(_:_:))
- [func simd_make_uchar8_undef(simd_uchar2) -> simd_uchar8](/documentation/simd/simd_make_uchar8_undef(_:)-19t4r)
- [func simd_make_uchar8_undef(simd_uchar3) -> simd_uchar8](/documentation/simd/simd_make_uchar8_undef(_:)-14ngi)
- [func simd_make_uchar8_undef(simd_uchar4) -> simd_uchar8](/documentation/simd/simd_make_uchar8_undef(_:)-ovyp)

### Functions to Create Eight-Element Vectors From Scalar Values

- [func simd_make_uchar8(UInt8) -> simd_uchar8](/documentation/simd/simd_make_uchar8(_:)-9e791)
- [func simd_make_uchar8_undef(UInt8) -> simd_uchar8](/documentation/simd/simd_make_uchar8_undef(_:)-3cvtm)

### Common Functions

- [func simd_clamp(simd_uchar8, simd_uchar8, simd_uchar8) -> simd_uchar8](/documentation/simd/simd_clamp(_:_:_:)-1uiyw)
- [func simd_equal(simd_uchar8, simd_uchar8) -> simd_bool](/documentation/simd/simd_equal(_:_:)-5o6ip)

### Reduce Functions

- [func simd_reduce_min(simd_uchar8) -> UInt8](/documentation/simd/simd_reduce_min(_:)-3oc92)
- [func simd_reduce_max(simd_uchar8) -> UInt8](/documentation/simd/simd_reduce_max(_:)-55cku)
- [func simd_reduce_add(simd_uchar8) -> UInt8](/documentation/simd/simd_reduce_add(_:)-3ay64)

### Extrema Functions

- [func simd_min(simd_uchar8, simd_uchar8) -> simd_uchar8](/documentation/simd/simd_min(_:_:)-8ibca)
- [func simd_max(simd_uchar8, simd_uchar8) -> simd_uchar8](/documentation/simd/simd_max(_:_:)-7b9mk)

### Logic and Bitwise Functions

- [func simd_any(simd_uchar8) -> simd_bool](/documentation/simd/simd_any(_:)-6pbmv)
- [func simd_all(simd_uchar8) -> simd_bool](/documentation/simd/simd_all(_:)-1yp2h)
- [func simd_bitselect(simd_uchar8, simd_uchar8, simd_char8) -> simd_uchar8](/documentation/simd/simd_bitselect(_:_:_:)-9gyx6)

### Alternative Type Alias

- [vector_uchar8](/documentation/simd/vector_uchar8)
- [simd_uint1](/documentation/simd/simd_uint1)
- [simd_uint16](/documentation/simd/simd_uint16)

### Functions to Create Sixteen-Element Vectors From Other Vectors

- [func simd_make_uint16(simd_uint2) -> simd_uint16](/documentation/simd/simd_make_uint16(_:)-99aov)
- [func simd_make_uint16(simd_uint3) -> simd_uint16](/documentation/simd/simd_make_uint16(_:)-9efau)
- [func simd_make_uint16(simd_uint4) -> simd_uint16](/documentation/simd/simd_make_uint16(_:)-9u6t5)
- [func simd_make_uint16(simd_uint8) -> simd_uint16](/documentation/simd/simd_make_uint16(_:)-9hiq)
- [func simd_make_uint16(simd_uint16) -> simd_uint16](/documentation/simd/simd_make_uint16(_:)-9s9mg)
- [func simd_make_uint16(simd_uint8, simd_uint8) -> simd_uint16](/documentation/simd/simd_make_uint16(_:_:))
- [func simd_make_uint16_undef(simd_uint2) -> simd_uint16](/documentation/simd/simd_make_uint16_undef(_:)-9w2go)
- [func simd_make_uint16_undef(simd_uint3) -> simd_uint16](/documentation/simd/simd_make_uint16_undef(_:)-9slqx)
- [func simd_make_uint16_undef(simd_uint4) -> simd_uint16](/documentation/simd/simd_make_uint16_undef(_:)-hcyl)
- [func simd_make_uint16_undef(simd_uint8) -> simd_uint16](/documentation/simd/simd_make_uint16_undef(_:)-we1l)

### Functions to Create Sixteen-Element Vectors From Scalar Values

- [func simd_make_uint16(UInt32) -> simd_uint16](/documentation/simd/simd_make_uint16(_:)-3h7ip)
- [func simd_make_uint16_undef(UInt32) -> simd_uint16](/documentation/simd/simd_make_uint16_undef(_:)-6ss74)

### Common Functions

- [func simd_clamp(simd_uint16, simd_uint16, simd_uint16) -> simd_uint16](/documentation/simd/simd_clamp(_:_:_:)-226tg)
- [func simd_equal(simd_uint16, simd_uint16) -> simd_bool](/documentation/simd/simd_equal(_:_:)-35l8d)

### Reduce Functions

- [func simd_reduce_min(simd_uint16) -> UInt32](/documentation/simd/simd_reduce_min(_:)-3cy7f)
- [func simd_reduce_max(simd_uint16) -> UInt32](/documentation/simd/simd_reduce_max(_:)-8iqq5)
- [func simd_reduce_add(simd_uint16) -> UInt32](/documentation/simd/simd_reduce_add(_:)-7n22w)

### Extrema Functions

- [func simd_min(simd_uint16, simd_uint16) -> simd_uint16](/documentation/simd/simd_min(_:_:)-5plhb)
- [func simd_max(simd_uint16, simd_uint16) -> simd_uint16](/documentation/simd/simd_max(_:_:)-3cz8t)

### Logic and Bitwise Functions

- [func simd_any(simd_uint16) -> simd_bool](/documentation/simd/simd_any(_:)-931x2)
- [func simd_all(simd_uint16) -> simd_bool](/documentation/simd/simd_all(_:)-inj8)
- [func simd_bitselect(simd_uint16, simd_uint16, simd_int16) -> simd_uint16](/documentation/simd/simd_bitselect(_:_:_:)-35yra)

### Alternative Type Alias

- [vector_uint16](/documentation/simd/vector_uint16)
- [simd_uint2](/documentation/simd/simd_uint2)

### Functions to Create Two-Element Vectors From Other Vectors

- [func simd_make_uint2(simd_uint2) -> simd_uint2](/documentation/simd/simd_make_uint2(_:)-3fnd3)
- [func simd_make_uint2(simd_uint3) -> simd_uint2](/documentation/simd/simd_make_uint2(_:)-3cbr2)
- [func simd_make_uint2(simd_uint4) -> simd_uint2](/documentation/simd/simd_make_uint2(_:)-3m281)
- [func simd_make_uint2(simd_uint8) -> simd_uint2](/documentation/simd/simd_make_uint2(_:)-40jb1)
- [func simd_make_uint2(simd_uint16) -> simd_uint2](/documentation/simd/simd_make_uint2(_:)-9b05l)

### Functions to Create Two-Element Vectors From Scalar Values

- [func simd_make_uint2(UInt32) -> simd_uint2](/documentation/simd/simd_make_uint2(_:)-82fnu)
- [func simd_make_uint2(UInt32, UInt32) -> simd_uint2](/documentation/simd/simd_make_uint2(_:_:))
- [func simd_make_uint2_undef(UInt32) -> simd_uint2](/documentation/simd/simd_make_uint2_undef(_:))

### Common Functions

- [func simd_clamp(simd_uint2, simd_uint2, simd_uint2) -> simd_uint2](/documentation/simd/simd_clamp(_:_:_:)-5yp7)
- [func clamp(SIMD2<UInt32>, min: UInt32, max: UInt32) -> SIMD2<UInt32>](/documentation/simd/clamp(_:min:max:)-5cyx4)
- [func clamp(SIMD2<UInt32>, min: SIMD2<UInt32>, max: SIMD2<UInt32>) -> SIMD2<UInt32>](/documentation/simd/clamp(_:min:max:)-59rk7)
- [func simd_equal(simd_uint2, simd_uint2) -> simd_bool](/documentation/simd/simd_equal(_:_:)-2urgh)

### Reduce Functions

- [func simd_reduce_min(simd_uint2) -> UInt32](/documentation/simd/simd_reduce_min(_:)-49p5s)
- [func reduce_min(SIMD2<UInt32>) -> UInt32](/documentation/simd/reduce_min(_:)-2b4fr)
- [func simd_reduce_max(simd_uint2) -> UInt32](/documentation/simd/simd_reduce_max(_:)-4ket4)
- [func reduce_max(SIMD2<UInt32>) -> UInt32](/documentation/simd/reduce_max(_:)-5dxp4)
- [func simd_reduce_add(simd_uint2) -> UInt32](/documentation/simd/simd_reduce_add(_:)-2q44e)
- [func reduce_add(SIMD2<UInt32>) -> UInt32](/documentation/simd/reduce_add(_:)-5uvts)

### Extrema Functions

- [func simd_min(simd_uint2, simd_uint2) -> simd_uint2](/documentation/simd/simd_min(_:_:)-9b5n7)
- [func min(SIMD2<UInt32>, UInt32) -> SIMD2<UInt32>](/documentation/simd/min(_:_:)-6xef7)
- [func min(SIMD2<UInt32>, SIMD2<UInt32>) -> SIMD2<UInt32>](/documentation/simd/min(_:_:)-70ls4)
- [func simd_max(simd_uint2, simd_uint2) -> simd_uint2](/documentation/simd/simd_max(_:_:)-8931y)
- [func max(SIMD2<UInt32>, UInt32) -> SIMD2<UInt32>](/documentation/simd/max(_:_:)-9ch4d)
- [func max(SIMD2<UInt32>, SIMD2<UInt32>) -> SIMD2<UInt32>](/documentation/simd/max(_:_:)-9fm5e)

### Logic and Bitwise Functions

- [func simd_any(simd_uint2) -> simd_bool](/documentation/simd/simd_any(_:)-64hll)
- [func simd_all(simd_uint2) -> simd_bool](/documentation/simd/simd_all(_:)-1d7bv)
- [func simd_bitselect(simd_uint2, simd_uint2, simd_int2) -> simd_uint2](/documentation/simd/simd_bitselect(_:_:_:)-5dqwa)

### Alternative Type Alias

- [uint2](/documentation/simd/uint2)
- [vector_uint2](/documentation/simd/vector_uint2)
- [simd_uint3](/documentation/simd/simd_uint3)

### Functions to Create Three-Element Vectors From Other Vectors

- [func simd_make_uint3(simd_uint2) -> simd_uint3](/documentation/simd/simd_make_uint3(_:)-7e6jd)
- [func simd_make_uint3(simd_uint3) -> simd_uint3](/documentation/simd/simd_make_uint3(_:)-7h348)
- [func simd_make_uint3(simd_uint4) -> simd_uint3](/documentation/simd/simd_make_uint3(_:)-77mmf)
- [func simd_make_uint3(simd_uint8) -> simd_uint3](/documentation/simd/simd_make_uint3(_:)-6sqjv)
- [func simd_make_uint3(simd_uint16) -> simd_uint3](/documentation/simd/simd_make_uint3(_:)-6rqe9)
- [func simd_make_uint3_undef(simd_uint2) -> simd_uint3](/documentation/simd/simd_make_uint3_undef(_:)-3a81k)

### Functions to Create Three-Element Vectors From Scalar Values

- [func simd_make_uint3(UInt32) -> simd_uint3](/documentation/simd/simd_make_uint3(_:)-512r5)
- [func simd_make_uint3(UInt32, UInt32, UInt32) -> simd_uint3](/documentation/simd/simd_make_uint3(_:_:_:))
- [func simd_make_uint3_undef(UInt32) -> simd_uint3](/documentation/simd/simd_make_uint3_undef(_:)-1waea)

### Functions to Create Three-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_uint3(simd_uint2, UInt32) -> simd_uint3](/documentation/simd/simd_make_uint3(_:_:)-5y5kc)
- [func simd_make_uint3(UInt32, simd_uint2) -> simd_uint3](/documentation/simd/simd_make_uint3(_:_:)-210g2)

### Common Functions

- [func simd_clamp(simd_uint3, simd_uint3, simd_uint3) -> simd_uint3](/documentation/simd/simd_clamp(_:_:_:)-7ssi2)
- [func clamp(SIMD3<UInt32>, min: UInt32, max: UInt32) -> SIMD3<UInt32>](/documentation/simd/clamp(_:min:max:)-dhvg)
- [func clamp(SIMD3<UInt32>, min: SIMD3<UInt32>, max: SIMD3<UInt32>) -> SIMD3<UInt32>](/documentation/simd/clamp(_:min:max:)-gp7z)
- [func simd_equal(simd_uint3, simd_uint3) -> simd_bool](/documentation/simd/simd_equal(_:_:)-57xz1)

### Reduce Functions

- [func simd_reduce_min(simd_uint3) -> UInt32](/documentation/simd/simd_reduce_min(_:)-4688x)
- [func reduce_min(SIMD3<UInt32>) -> UInt32](/documentation/simd/reduce_min(_:)-1yst6)
- [func simd_reduce_max(simd_uint3) -> UInt32](/documentation/simd/simd_reduce_max(_:)-4h33d)
- [func reduce_max(SIMD3<UInt32>) -> UInt32](/documentation/simd/reduce_max(_:)-1h2j7)
- [func simd_reduce_add(simd_uint3) -> UInt32](/documentation/simd/simd_reduce_add(_:)-2v3pj)
- [func reduce_add(SIMD3<UInt32>) -> UInt32](/documentation/simd/reduce_add(_:)-7drmm)

### Extrema Functions

- [func simd_min(simd_uint3, simd_uint3) -> simd_uint3](/documentation/simd/simd_min(_:_:)-2sp22)
- [func min(SIMD3<UInt32>, UInt32) -> SIMD3<UInt32>](/documentation/simd/min(_:_:)-9iyne)
- [func min(SIMD3<UInt32>, SIMD3<UInt32>) -> SIMD3<UInt32>](/documentation/simd/min(_:_:)-9ftkl)
- [func simd_max(simd_uint3, simd_uint3) -> simd_uint3](/documentation/simd/simd_max(_:_:)-7a6cq)
- [func max(SIMD3<UInt32>, UInt32) -> SIMD3<UInt32>](/documentation/simd/max(_:_:)-703ka)
- [func max(SIMD3<UInt32>, SIMD3<UInt32>) -> SIMD3<UInt32>](/documentation/simd/max(_:_:)-6ww7t)

### Logic and Bitwise Functions

- [func simd_any(simd_uint3) -> simd_bool](/documentation/simd/simd_any(_:)-69h3c)
- [func simd_all(simd_uint3) -> simd_bool](/documentation/simd/simd_all(_:)-1afl6)
- [func simd_bitselect(simd_uint3, simd_uint3, simd_int3) -> simd_uint3](/documentation/simd/simd_bitselect(_:_:_:)-4hak)

### Alternative Type Alias

- [uint3](/documentation/simd/uint3)
- [vector_uint3](/documentation/simd/vector_uint3)
- [simd_uint4](/documentation/simd/simd_uint4)

### Functions to Create Four-Element Vectors From Other Vectors

- [func simd_make_uint4(simd_uint2) -> simd_uint4](/documentation/simd/simd_make_uint4(_:)-236jz)
- [func simd_make_uint4(simd_uint3) -> simd_uint4](/documentation/simd/simd_make_uint4(_:)-1zpti)
- [func simd_make_uint4(simd_uint4) -> simd_uint4](/documentation/simd/simd_make_uint4(_:)-2o2f5)
- [func simd_make_uint4(simd_uint8) -> simd_uint4](/documentation/simd/simd_make_uint4(_:)-333jp)
- [func simd_make_uint4(simd_uint16) -> simd_uint4](/documentation/simd/simd_make_uint4(_:)-4a98b)
- [func simd_make_uint4(simd_uint2, simd_uint2) -> simd_uint4](/documentation/simd/simd_make_uint4(_:_:)-14dxw)
- [func simd_make_uint4_undef(simd_uint2) -> simd_uint4](/documentation/simd/simd_make_uint4_undef(_:)-4iaj6)
- [func simd_make_uint4_undef(simd_uint3) -> simd_uint4](/documentation/simd/simd_make_uint4_undef(_:)-4lr3n)

### Functions to Create Four-Element Vectors From Scalar Values

- [func simd_make_uint4(UInt32) -> simd_uint4](/documentation/simd/simd_make_uint4(_:)-1vdsn)
- [func simd_make_uint4(UInt32, UInt32, UInt32, UInt32) -> simd_uint4](/documentation/simd/simd_make_uint4(_:_:_:_:))
- [func simd_make_uint4_undef(UInt32) -> simd_uint4](/documentation/simd/simd_make_uint4_undef(_:)-5wuto)

### Functions to Create Four-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_uint4(simd_uint2, UInt32, UInt32) -> simd_uint4](/documentation/simd/simd_make_uint4(_:_:_:)-5ftg3)
- [func simd_make_uint4(simd_uint3, UInt32) -> simd_uint4](/documentation/simd/simd_make_uint4(_:_:)-9arct)
- [func simd_make_uint4(UInt32, UInt32, simd_uint2) -> simd_uint4](/documentation/simd/simd_make_uint4(_:_:_:)-73ivt)
- [func simd_make_uint4(UInt32, simd_uint2, UInt32) -> simd_uint4](/documentation/simd/simd_make_uint4(_:_:_:)-45zbh)
- [func simd_make_uint4(UInt32, simd_uint3) -> simd_uint4](/documentation/simd/simd_make_uint4(_:_:)-4kh9u)

### Common Functions

- [func simd_clamp(simd_uint4, simd_uint4, simd_uint4) -> simd_uint4](/documentation/simd/simd_clamp(_:_:_:)-1y56u)
- [func clamp(SIMD4<UInt32>, min: UInt32, max: UInt32) -> SIMD4<UInt32>](/documentation/simd/clamp(_:min:max:)-6ix39)
- [func clamp(SIMD4<UInt32>, min: SIMD4<UInt32>, max: SIMD4<UInt32>) -> SIMD4<UInt32>](/documentation/simd/clamp(_:min:max:)-6fsdy)
- [func simd_equal(simd_uint4, simd_uint4) -> simd_bool](/documentation/simd/simd_equal(_:_:)-6tvg4)

### Reduce Functions

- [func simd_reduce_min(simd_uint4) -> UInt32](/documentation/simd/simd_reduce_min(_:)-4ukuu)
- [func reduce_min(SIMD4<UInt32>) -> UInt32](/documentation/simd/reduce_min(_:)-3yrpe)
- [func simd_reduce_max(simd_uint4) -> UInt32](/documentation/simd/simd_reduce_max(_:)-4qtcm)
- [func reduce_max(SIMD4<UInt32>) -> UInt32](/documentation/simd/reduce_max(_:)-ko69)
- [func simd_reduce_add(simd_uint4) -> UInt32](/documentation/simd/simd_reduce_add(_:)-2ylgg)
- [func reduce_add(SIMD4<UInt32>) -> UInt32](/documentation/simd/reduce_add(_:)-9xs7v)

### Extrema Functions

- [func simd_min(simd_uint4, simd_uint4) -> simd_uint4](/documentation/simd/simd_min(_:_:)-7hpr6)
- [func min(SIMD4<UInt32>, UInt32) -> SIMD4<UInt32>](/documentation/simd/min(_:_:)-7l4j0)
- [func min(SIMD4<UInt32>, SIMD4<UInt32>) -> SIMD4<UInt32>](/documentation/simd/min(_:_:)-7o4pn)
- [func simd_max(simd_uint4, simd_uint4) -> simd_uint4](/documentation/simd/simd_max(_:_:)-6870v)
- [func max(SIMD4<UInt32>, UInt32) -> SIMD4<UInt32>](/documentation/simd/max(_:_:)-2m7il)
- [func max(SIMD4<UInt32>, SIMD4<UInt32>) -> SIMD4<UInt32>](/documentation/simd/max(_:_:)-2pev2)

### Logic and Bitwise Functions

- [func simd_any(simd_uint4) -> simd_bool](/documentation/simd/simd_any(_:)-6cz27)
- [func simd_all(simd_uint4) -> simd_bool](/documentation/simd/simd_all(_:)-1jm2d)
- [func simd_bitselect(simd_uint4, simd_uint4, simd_int4) -> simd_uint4](/documentation/simd/simd_bitselect(_:_:_:)-1rrhy)

### Alternative Type Alias

- [uint4](/documentation/simd/uint4)
- [vector_uint4](/documentation/simd/vector_uint4)
- [simd_uint8](/documentation/simd/simd_uint8)

### Functions to Create Eight-Element Vectors From Other Vectors

- [func simd_make_uint8(simd_uint2) -> simd_uint8](/documentation/simd/simd_make_uint8(_:)-2vaoh)
- [func simd_make_uint8(simd_uint3) -> simd_uint8](/documentation/simd/simd_make_uint8(_:)-2rtxs)
- [func simd_make_uint8(simd_uint4) -> simd_uint8](/documentation/simd/simd_make_uint8(_:)-2ovzr)
- [func simd_make_uint8(simd_uint8) -> simd_uint8](/documentation/simd/simd_make_uint8(_:)-3sztf)
- [func simd_make_uint8(simd_uint16) -> simd_uint8](/documentation/simd/simd_make_uint8(_:)-64gkj)
- [func simd_make_uint8(simd_uint4, simd_uint4) -> simd_uint8](/documentation/simd/simd_make_uint8(_:_:))
- [func simd_make_uint8_undef(simd_uint2) -> simd_uint8](/documentation/simd/simd_make_uint8_undef(_:)-ck1m)
- [func simd_make_uint8_undef(simd_uint3) -> simd_uint8](/documentation/simd/simd_make_uint8_undef(_:)-hojv)
- [func simd_make_uint8_undef(simd_uint4) -> simd_uint8](/documentation/simd/simd_make_uint8_undef(_:)-6a8k)

### Functions to Create Eight-Element Vectors From Scalar Values

- [func simd_make_uint8(UInt32) -> simd_uint8](/documentation/simd/simd_make_uint8(_:)-7jqj3)
- [func simd_make_uint8_undef(UInt32) -> simd_uint8](/documentation/simd/simd_make_uint8_undef(_:)-8p5i8)

### Common Functions

- [func simd_clamp(simd_uint8, simd_uint8, simd_uint8) -> simd_uint8](/documentation/simd/simd_clamp(_:_:_:)-9evfi)
- [func simd_equal(simd_uint8, simd_uint8) -> simd_bool](/documentation/simd/simd_equal(_:_:)-1v1wn)

### Reduce Functions

- [func simd_reduce_min(simd_uint8) -> UInt32](/documentation/simd/simd_reduce_min(_:)-3o9f6)
- [func simd_reduce_max(simd_uint8) -> UInt32](/documentation/simd/simd_reduce_max(_:)-55ah6)
- [func simd_reduce_add(simd_uint8) -> UInt32](/documentation/simd/simd_reduce_add(_:)-3av90)

### Extrema Functions

- [func simd_min(simd_uint8, simd_uint8) -> simd_uint8](/documentation/simd/simd_min(_:_:)-873mx)
- [func simd_max(simd_uint8, simd_uint8) -> simd_uint8](/documentation/simd/simd_max(_:_:)-4l2k6)

### Logic and Bitwise Functions

- [func simd_any(simd_uint8) -> simd_bool](/documentation/simd/simd_any(_:)-6p8mz)
- [func simd_all(simd_uint8) -> simd_bool](/documentation/simd/simd_all(_:)-1ynbd)
- [func simd_bitselect(simd_uint8, simd_uint8, simd_int8) -> simd_uint8](/documentation/simd/simd_bitselect(_:_:_:)-803fj)

### Alternative Type Alias

- [vector_uint8](/documentation/simd/vector_uint8)
- [simd_ulong1](/documentation/simd/simd_ulong1)

### Alternative Type Alias

- [vector_ulong1](/documentation/simd/vector_ulong1)
- [simd_ulong2](/documentation/simd/simd_ulong2)

### Functions to Create Two-Element Vectors From Other Vectors

- [func simd_make_ulong2(simd_ulong2) -> simd_ulong2](/documentation/simd/simd_make_ulong2(_:)-oc6t)
- [func simd_make_ulong2(simd_ulong3) -> simd_ulong2](/documentation/simd/simd_make_ulong2(_:)-rr3e)
- [func simd_make_ulong2(simd_ulong4) -> simd_ulong2](/documentation/simd/simd_make_ulong2(_:)-ulyf)
- [func simd_make_ulong2(simd_ulong8) -> simd_ulong2](/documentation/simd/simd_make_ulong2(_:)-17hvf)

### Functions to Create Two-Element Vectors From Scalar Values

- [func simd_make_ulong2(simd_ulong1) -> simd_ulong2](/documentation/simd/simd_make_ulong2(_:)-14omj)
- [func simd_make_ulong2(simd_ulong1, simd_ulong1) -> simd_ulong2](/documentation/simd/simd_make_ulong2(_:_:))
- [func simd_make_ulong2_undef(simd_ulong1) -> simd_ulong2](/documentation/simd/simd_make_ulong2_undef(_:))

### Common Functions

- [func simd_clamp(simd_ulong2, simd_ulong2, simd_ulong2) -> simd_ulong2](/documentation/simd/simd_clamp(_:_:_:)-5y5rd)
- [func simd_equal(simd_ulong2, simd_ulong2) -> simd_bool](/documentation/simd/simd_equal(_:_:)-80jzi)

### Reduce Functions

- [func simd_reduce_min(simd_ulong2) -> simd_ulong1](/documentation/simd/simd_reduce_min(_:)-49qq4)
- [func simd_reduce_max(simd_ulong2) -> simd_ulong1](/documentation/simd/simd_reduce_max(_:)-4kgd8)
- [func simd_reduce_add(simd_ulong2) -> simd_ulong1](/documentation/simd/simd_reduce_add(_:)-2q2jq)

### Extrema Functions

- [func simd_min(simd_ulong2, simd_ulong2) -> simd_ulong2](/documentation/simd/simd_min(_:_:)-9be6)
- [func simd_max(simd_ulong2, simd_ulong2) -> simd_ulong2](/documentation/simd/simd_max(_:_:)-86a4g)

### Logic and Bitwise Functions

- [func simd_any(simd_ulong2) -> simd_bool](/documentation/simd/simd_any(_:)-64g1r)
- [func simd_all(simd_ulong2) -> simd_bool](/documentation/simd/simd_all(_:)-1d8u9)
- [func simd_bitselect(simd_ulong2, simd_ulong2, simd_long2) -> simd_ulong2](/documentation/simd/simd_bitselect(_:_:_:)-886h0)

### Alternative Type Alias

- [vector_ulong2](/documentation/simd/vector_ulong2)
- [simd_ulong3](/documentation/simd/simd_ulong3)

### Functions to Create Three-Element Vectors From Other Vectors

- [func simd_make_ulong3(simd_ulong2) -> simd_ulong3](/documentation/simd/simd_make_ulong3(_:)-5autj)
- [func simd_make_ulong3(simd_ulong3) -> simd_ulong3](/documentation/simd/simd_make_ulong3(_:)-57xdw)
- [func simd_make_ulong3(simd_ulong4) -> simd_ulong3](/documentation/simd/simd_make_ulong3(_:)-5w7y5)
- [func simd_make_ulong3(simd_ulong8) -> simd_ulong3](/documentation/simd/simd_make_ulong3(_:)-4pyq9)
- [func simd_make_ulong3_undef(simd_ulong2) -> simd_ulong3](/documentation/simd/simd_make_ulong3_undef(_:)-5oqlt)

### Functions to Create Three-Element Vectors From Scalar Values

- [func simd_make_ulong3(simd_ulong1) -> simd_ulong3](/documentation/simd/simd_make_ulong3(_:)-3eb9a)
- [func simd_make_ulong3(simd_ulong1, simd_ulong1, simd_ulong1) -> simd_ulong3](/documentation/simd/simd_make_ulong3(_:_:_:))
- [func simd_make_ulong3_undef(simd_ulong1) -> simd_ulong3](/documentation/simd/simd_make_ulong3_undef(_:)-7s0qh)

### Functions to Create Three-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_ulong3(simd_ulong1, simd_ulong2) -> simd_ulong3](/documentation/simd/simd_make_ulong3(_:_:)-3zpz6)
- [func simd_make_ulong3(simd_ulong2, simd_ulong1) -> simd_ulong3](/documentation/simd/simd_make_ulong3(_:_:)-3orcm)

### Common Functions

- [func simd_clamp(simd_ulong3, simd_ulong3, simd_ulong3) -> simd_ulong3](/documentation/simd/simd_clamp(_:_:_:)-5ce6)
- [func simd_equal(simd_ulong3, simd_ulong3) -> simd_bool](/documentation/simd/simd_equal(_:_:)-2p336)

### Reduce Functions

- [func simd_reduce_min(simd_ulong3) -> simd_ulong1](/documentation/simd/simd_reduce_min(_:)-4697f)
- [func simd_reduce_max(simd_ulong3) -> simd_ulong1](/documentation/simd/simd_reduce_max(_:)-4h1hr)
- [func simd_reduce_add(simd_ulong3) -> simd_ulong1](/documentation/simd/simd_reduce_add(_:)-2v51x)

### Extrema Functions

- [func simd_min(simd_ulong3, simd_ulong3) -> simd_ulong3](/documentation/simd/simd_min(_:_:)-914t0)
- [func simd_max(simd_ulong3, simd_ulong3) -> simd_ulong3](/documentation/simd/simd_max(_:_:)-765ec)

### Logic and Bitwise Functions

- [func simd_any(simd_ulong3) -> simd_bool](/documentation/simd/simd_any(_:)-69ij0)
- [func simd_all(simd_ulong3) -> simd_bool](/documentation/simd/simd_all(_:)-1adyq)
- [func simd_bitselect(simd_ulong3, simd_ulong3, simd_long3) -> simd_ulong3](/documentation/simd/simd_bitselect(_:_:_:)-600bp)

### Alternative Type Alias

- [vector_ulong3](/documentation/simd/vector_ulong3)
- [simd_ulong4](/documentation/simd/simd_ulong4)

### Functions to Create Four-Element Vectors From Other Vectors

- [func simd_make_ulong4(simd_ulong2) -> simd_ulong4](/documentation/simd/simd_make_ulong4(_:)-364ux)
- [func simd_make_ulong4(simd_ulong3) -> simd_ulong4](/documentation/simd/simd_make_ulong4(_:)-39may)
- [func simd_make_ulong4(simd_ulong4) -> simd_ulong4](/documentation/simd/simd_make_ulong4(_:)-2zv2b)
- [func simd_make_ulong4(simd_ulong8) -> simd_ulong4](/documentation/simd/simd_make_ulong4(_:)-43wof)
- [func simd_make_ulong4(simd_ulong2, simd_ulong2) -> simd_ulong4](/documentation/simd/simd_make_ulong4(_:_:)-9oy4u)
- [func simd_make_ulong4_undef(simd_ulong2) -> simd_ulong4](/documentation/simd/simd_make_ulong4_undef(_:)-o0j)
- [func simd_make_ulong4_undef(simd_ulong3) -> simd_ulong4](/documentation/simd/simd_make_ulong4_undef(_:)-9xbtd)

### Functions to Create Four-Element Vectors From Scalar Values

- [func simd_make_ulong4(simd_ulong1) -> simd_ulong4](/documentation/simd/simd_make_ulong4(_:)-6kawu)
- [func simd_make_ulong4(simd_ulong1, simd_ulong1, simd_ulong1, simd_ulong1) -> simd_ulong4](/documentation/simd/simd_make_ulong4(_:_:_:_:))
- [func simd_make_ulong4_undef(simd_ulong1) -> simd_ulong4](/documentation/simd/simd_make_ulong4_undef(_:)-jgtr)

### Functions to Create Four-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_ulong4(simd_ulong1, simd_ulong1, simd_ulong2) -> simd_ulong4](/documentation/simd/simd_make_ulong4(_:_:_:)-4du2m)
- [func simd_make_ulong4(simd_ulong1, simd_ulong2, simd_ulong1) -> simd_ulong4](/documentation/simd/simd_make_ulong4(_:_:_:)-8asm5)
- [func simd_make_ulong4(simd_ulong1, simd_ulong3) -> simd_ulong4](/documentation/simd/simd_make_ulong4(_:_:)-5mtth)
- [func simd_make_ulong4(simd_ulong2, simd_ulong1, simd_ulong1) -> simd_ulong4](/documentation/simd/simd_make_ulong4(_:_:_:)-8g4ch)
- [func simd_make_ulong4(simd_ulong3, simd_ulong1) -> simd_ulong4](/documentation/simd/simd_make_ulong4(_:_:)-cnt3)

### Common Functions

- [func simd_clamp(simd_ulong4, simd_ulong4, simd_ulong4) -> simd_ulong4](/documentation/simd/simd_clamp(_:_:_:)-5cuj3)
- [func simd_equal(simd_ulong4, simd_ulong4) -> simd_bool](/documentation/simd/simd_equal(_:_:)-8d8x)

### Reduce Functions

- [func simd_reduce_min(simd_ulong4) -> simd_ulong1](/documentation/simd/simd_reduce_min(_:)-4ujwm)
- [func simd_reduce_max(simd_ulong4) -> simd_ulong1](/documentation/simd/simd_reduce_max(_:)-4qsf2)
- [func simd_reduce_add(simd_ulong4) -> simd_ulong1](/documentation/simd/simd_reduce_add(_:)-2yjx0)

### Extrema Functions

- [func simd_min(simd_ulong4, simd_ulong4) -> simd_ulong4](/documentation/simd/simd_min(_:_:)-9meuw)
- [func simd_max(simd_ulong4, simd_ulong4) -> simd_ulong4](/documentation/simd/simd_max(_:_:)-6x9fu)

### Logic and Bitwise Functions

- [func simd_any(simd_ulong4) -> simd_bool](/documentation/simd/simd_any(_:)-6cxel)
- [func simd_all(simd_ulong4) -> simd_bool](/documentation/simd/simd_all(_:)-1jlbv)
- [func simd_bitselect(simd_ulong4, simd_ulong4, simd_long4) -> simd_ulong4](/documentation/simd/simd_bitselect(_:_:_:)-6gszc)

### Alternative Type Alias

- [vector_ulong4](/documentation/simd/vector_ulong4)
- [simd_ulong8](/documentation/simd/simd_ulong8)

### Functions to Create Eight-Element Vectors From Other Vectors

- [func simd_make_ulong8(simd_ulong2) -> simd_ulong8](/documentation/simd/simd_make_ulong8(_:)-5w0n4)
- [func simd_make_ulong8(simd_ulong3) -> simd_ulong8](/documentation/simd/simd_make_ulong8(_:)-5zhz7)
- [func simd_make_ulong8(simd_ulong4) -> simd_ulong8](/documentation/simd/simd_make_ulong8(_:)-6hggi)
- [func simd_make_ulong8(simd_ulong8) -> simd_ulong8](/documentation/simd/simd_make_ulong8(_:)-6wa2m)
- [func simd_make_ulong8(simd_ulong4, simd_ulong4) -> simd_ulong8](/documentation/simd/simd_make_ulong8(_:_:))
- [func simd_make_ulong8_undef(simd_ulong2) -> simd_ulong8](/documentation/simd/simd_make_ulong8_undef(_:)-9rdt9)
- [func simd_make_ulong8_undef(simd_ulong3) -> simd_ulong8](/documentation/simd/simd_make_ulong8_undef(_:)-9oge2)
- [func simd_make_ulong8_undef(simd_ulong4) -> simd_ulong8](/documentation/simd/simd_make_ulong8_undef(_:)-d5pk)

### Functions to Create Eight-Element Vectors From Scalar Values

- [func simd_make_ulong8(simd_ulong1) -> simd_ulong8](/documentation/simd/simd_make_ulong8(_:)-w5ee)
- [func simd_make_ulong8_undef(simd_ulong1) -> simd_ulong8](/documentation/simd/simd_make_ulong8_undef(_:)-73woc)

### Common Functions

- [func simd_clamp(simd_ulong8, simd_ulong8, simd_ulong8) -> simd_ulong8](/documentation/simd/simd_clamp(_:_:_:)-6mt76)
- [func simd_equal(simd_ulong8, simd_ulong8) -> simd_bool](/documentation/simd/simd_equal(_:_:)-4dws0)

### Reduce Functions

- [func simd_reduce_min(simd_ulong8) -> simd_ulong1](/documentation/simd/simd_reduce_min(_:)-3oaqy)
- [func simd_reduce_max(simd_ulong8) -> simd_ulong1](/documentation/simd/simd_reduce_max(_:)-55c36)
- [func simd_reduce_add(simd_ulong8) -> simd_ulong1](/documentation/simd/simd_reduce_add(_:)-3avzc)

### Extrema Functions

- [func simd_min(simd_ulong8, simd_ulong8) -> simd_ulong8](/documentation/simd/simd_min(_:_:)-1ynv5)
- [func simd_max(simd_ulong8, simd_ulong8) -> simd_ulong8](/documentation/simd/simd_max(_:_:)-9mj3u)

### Logic and Bitwise Functions

- [func simd_any(simd_ulong8) -> simd_bool](/documentation/simd/simd_any(_:)-6p9gh)
- [func simd_all(simd_ulong8) -> simd_bool](/documentation/simd/simd_all(_:)-1yolz)
- [func simd_bitselect(simd_ulong8, simd_ulong8, simd_long8) -> simd_ulong8](/documentation/simd/simd_bitselect(_:_:_:)-3xirg)

### Alternative Type Alias

- [vector_ulong8](/documentation/simd/vector_ulong8)
- [simd_ushort1](/documentation/simd/simd_ushort1)
- [simd_ushort16](/documentation/simd/simd_ushort16)

### Functions to Create Sixteen-Element Vectors From Other Vectors

- [func simd_make_ushort16(simd_ushort2) -> simd_ushort16](/documentation/simd/simd_make_ushort16(_:)-5h1oe)
- [func simd_make_ushort16(simd_ushort3) -> simd_ushort16](/documentation/simd/simd_make_ushort16(_:)-5dtrr)
- [func simd_make_ushort16(simd_ushort4) -> simd_ushort16](/documentation/simd/simd_make_ushort16(_:)-4vumc)
- [func simd_make_ushort16(simd_ushort8) -> simd_ushort16](/documentation/simd/simd_make_ushort16(_:)-4h3f4)
- [func simd_make_ushort16(simd_ushort16) -> simd_ushort16](/documentation/simd/simd_make_ushort16(_:)-43b0g)
- [func simd_make_ushort16(simd_ushort32) -> simd_ushort16](/documentation/simd/simd_make_ushort16(_:)-5wstb)
- [func simd_make_ushort16(simd_ushort8, simd_ushort8) -> simd_ushort16](/documentation/simd/simd_make_ushort16(_:_:))
- [func simd_make_ushort16_undef(simd_ushort2) -> simd_ushort16](/documentation/simd/simd_make_ushort16_undef(_:)-3jyo)
- [func simd_make_ushort16_undef(simd_ushort3) -> simd_ushort16](/documentation/simd/simd_make_ushort16_undef(_:)-8phl)
- [func simd_make_ushort16_undef(simd_ushort4) -> simd_ushort16](/documentation/simd/simd_make_ushort16_undef(_:)-bxgi)
- [func simd_make_ushort16_undef(simd_ushort8) -> simd_ushort16](/documentation/simd/simd_make_ushort16_undef(_:)-957cx)

### Functions to Create Sixteen-Element Vectors From Scalar Values

- [func simd_make_ushort16(UInt16) -> simd_ushort16](/documentation/simd/simd_make_ushort16(_:)-6sqah)
- [func simd_make_ushort16_undef(UInt16) -> simd_ushort16](/documentation/simd/simd_make_ushort16_undef(_:)-6iivl)

### Common Functions

- [func simd_clamp(simd_ushort16, simd_ushort16, simd_ushort16) -> simd_ushort16](/documentation/simd/simd_clamp(_:_:_:)-5hezy)
- [func simd_equal(simd_ushort16, simd_ushort16) -> simd_bool](/documentation/simd/simd_equal(_:_:)-9luz4)

### Reduce Functions

- [func simd_reduce_min(simd_ushort16) -> UInt16](/documentation/simd/simd_reduce_min(_:)-3d6c7)
- [func simd_reduce_max(simd_ushort16) -> UInt16](/documentation/simd/simd_reduce_max(_:)-8isf9)
- [func simd_reduce_add(simd_ushort16) -> UInt16](/documentation/simd/simd_reduce_add(_:)-7n920)

### Extrema Functions

- [func simd_min(simd_ushort16, simd_ushort16) -> simd_ushort16](/documentation/simd/simd_min(_:_:)-99clp)
- [func simd_max(simd_ushort16, simd_ushort16) -> simd_ushort16](/documentation/simd/simd_max(_:_:)-1332e)

### Logic and Bitwise Functions

- [func simd_any(simd_ushort16) -> simd_bool](/documentation/simd/simd_any(_:)-938p6)
- [func simd_all(simd_ushort16) -> simd_bool](/documentation/simd/simd_all(_:)-iffg)
- [func simd_bitselect(simd_ushort16, simd_ushort16, simd_short16) -> simd_ushort16](/documentation/simd/simd_bitselect(_:_:_:)-144l9)

### Alternative Type Alias

- [vector_ushort16](/documentation/simd/vector_ushort16)
- [simd_ushort2](/documentation/simd/simd_ushort2)

### Functions to Create Two-Element Vectors From Other Vectors

- [func simd_make_ushort2(simd_ushort2) -> simd_ushort2](/documentation/simd/simd_make_ushort2(_:)-2dkjj)
- [func simd_make_ushort2(simd_ushort3) -> simd_ushort2](/documentation/simd/simd_make_ushort2(_:)-2gsja)
- [func simd_make_ushort2(simd_ushort4) -> simd_ushort2](/documentation/simd/simd_make_ushort2(_:)-1sfxh)
- [func simd_make_ushort2(simd_ushort8) -> simd_ushort2](/documentation/simd/simd_make_ushort2(_:)-2yrlt)
- [func simd_make_ushort2(simd_ushort16) -> simd_ushort2](/documentation/simd/simd_make_ushort2(_:)-72vh1)
- [func simd_make_ushort2(simd_ushort32) -> simd_ushort2](/documentation/simd/simd_make_ushort2(_:)-8zwg1)

### Functions to Create Two-Element Vectors From Scalar Values

- [func simd_make_ushort2(UInt16) -> simd_ushort2](/documentation/simd/simd_make_ushort2(_:)-4i2ym)
- [func simd_make_ushort2(UInt16, UInt16) -> simd_ushort2](/documentation/simd/simd_make_ushort2(_:_:))
- [func simd_make_ushort2_undef(UInt16) -> simd_ushort2](/documentation/simd/simd_make_ushort2_undef(_:))

### Common Functions

- [func simd_clamp(simd_ushort2, simd_ushort2, simd_ushort2) -> simd_ushort2](/documentation/simd/simd_clamp(_:_:_:)-3o9ad)
- [func simd_equal(simd_ushort2, simd_ushort2) -> simd_bool](/documentation/simd/simd_equal(_:_:)-ktbu)

### Reduce Functions

- [func simd_reduce_min(simd_ushort2) -> UInt16](/documentation/simd/simd_reduce_min(_:)-49m28)
- [func simd_reduce_max(simd_ushort2) -> UInt16](/documentation/simd/simd_reduce_max(_:)-4kcqg)
- [func simd_reduce_add(simd_ushort2) -> UInt16](/documentation/simd/simd_reduce_add(_:)-2pw16)

### Extrema Functions

- [func simd_min(simd_ushort2, simd_ushort2) -> simd_ushort2](/documentation/simd/simd_min(_:_:)-717c8)
- [func simd_max(simd_ushort2, simd_ushort2) -> simd_ushort2](/documentation/simd/simd_max(_:_:)-27z7q)

### Logic and Bitwise Functions

- [func simd_any(simd_ushort2) -> simd_bool](/documentation/simd/simd_any(_:)-649i9)
- [func simd_all(simd_ushort2) -> simd_bool](/documentation/simd/simd_all(_:)-1dffj)
- [func simd_bitselect(simd_ushort2, simd_ushort2, simd_short2) -> simd_ushort2](/documentation/simd/simd_bitselect(_:_:_:)-9p6cd)

### Alternative Type Alias

- [vector_ushort2](/documentation/simd/vector_ushort2)
- [simd_ushort3](/documentation/simd/simd_ushort3)

### Functions to Create Three-Element Vectors From Other Vectors

- [func simd_make_ushort3(simd_ushort2) -> simd_ushort3](/documentation/simd/simd_make_ushort3(_:)-80g2g)
- [func simd_make_ushort3(simd_ushort3) -> simd_ushort3](/documentation/simd/simd_make_ushort3(_:)-7xag1)
- [func simd_make_ushort3(simd_ushort4) -> simd_ushort3](/documentation/simd/simd_make_ushort3(_:)-7u2h6)
- [func simd_make_ushort3(simd_ushort8) -> simd_ushort3](/documentation/simd/simd_make_ushort3(_:)-7fbo6)
- [func simd_make_ushort3(simd_ushort16) -> simd_ushort3](/documentation/simd/simd_make_ushort3(_:)-58w42)
- [func simd_make_ushort3(simd_ushort32) -> simd_ushort3](/documentation/simd/simd_make_ushort3(_:)-11fhu)
- [func simd_make_ushort3_undef(simd_ushort2) -> simd_ushort3](/documentation/simd/simd_make_ushort3_undef(_:)-6m2i9)

### Functions to Create Three-Element Vectors From Scalar Values

- [func simd_make_ushort3(UInt16) -> simd_ushort3](/documentation/simd/simd_make_ushort3(_:)-93msa)
- [func simd_make_ushort3(UInt16, UInt16, UInt16) -> simd_ushort3](/documentation/simd/simd_make_ushort3(_:_:_:))
- [func simd_make_ushort3_undef(UInt16) -> simd_ushort3](/documentation/simd/simd_make_ushort3_undef(_:)-6cyga)

### Functions to Create Three-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_ushort3(simd_ushort2, UInt16) -> simd_ushort3](/documentation/simd/simd_make_ushort3(_:_:)-3ap3r)
- [func simd_make_ushort3(UInt16, simd_ushort2) -> simd_ushort3](/documentation/simd/simd_make_ushort3(_:_:)-9h935)

### Common Functions

- [func simd_clamp(simd_ushort3, simd_ushort3, simd_ushort3) -> simd_ushort3](/documentation/simd/simd_clamp(_:_:_:)-4akg3)
- [func simd_equal(simd_ushort3, simd_ushort3) -> simd_bool](/documentation/simd/simd_equal(_:_:)-9b270)

### Reduce Functions

- [func simd_reduce_min(simd_ushort3) -> UInt16](/documentation/simd/simd_reduce_min(_:)-46gdl)
- [func simd_reduce_max(simd_ushort3) -> UInt16](/documentation/simd/simd_reduce_max(_:)-4h4s1)
- [func simd_reduce_add(simd_ushort3) -> UInt16](/documentation/simd/simd_reduce_add(_:)-2vbub)

### Extrema Function

- [func simd_min(simd_ushort3, simd_ushort3) -> simd_ushort3](/documentation/simd/simd_min(_:_:)-4jk8l)
- [func simd_max(simd_ushort3, simd_ushort3) -> simd_ushort3](/documentation/simd/simd_max(_:_:)-4fcp5)

### Logic and Bitwise Functions

- [func simd_any(simd_ushort3) -> simd_bool](/documentation/simd/simd_any(_:)-69p6w)
- [func simd_all(simd_ushort3) -> simd_bool](/documentation/simd/simd_all(_:)-1a7fa)
- [func simd_bitselect(simd_ushort3, simd_ushort3, simd_short3) -> simd_ushort3](/documentation/simd/simd_bitselect(_:_:_:)-7yglw)

### Alternative Type Alias

- [vector_ushort3](/documentation/simd/vector_ushort3)
- [simd_ushort32](/documentation/simd/simd_ushort32)

### Functions to Create Thirty Two-Element Vectors From Other Vectors

- [func simd_make_ushort32(simd_ushort2) -> simd_ushort32](/documentation/simd/simd_make_ushort32(_:)-359dc)
- [func simd_make_ushort32(simd_ushort3) -> simd_ushort32](/documentation/simd/simd_make_ushort32(_:)-323vt)
- [func simd_make_ushort32(simd_ushort4) -> simd_ushort32](/documentation/simd/simd_make_ushort32(_:)-2yvzm)
- [func simd_make_ushort32(simd_ushort8) -> simd_ushort32](/documentation/simd/simd_make_ushort32(_:)-2k4se)
- [func simd_make_ushort32(simd_ushort16) -> simd_ushort32](/documentation/simd/simd_make_ushort32(_:)-1y3a6)
- [func simd_make_ushort32(simd_ushort32) -> simd_ushort32](/documentation/simd/simd_make_ushort32(_:)-7o0fp)
- [func simd_make_ushort32(simd_ushort16, simd_ushort16) -> simd_ushort32](/documentation/simd/simd_make_ushort32(_:_:))
- [func simd_make_ushort32_undef(simd_ushort2) -> simd_ushort32](/documentation/simd/simd_make_ushort32_undef(_:)-5c9cc)
- [func simd_make_ushort32_undef(simd_ushort3) -> simd_ushort32](/documentation/simd/simd_make_ushort32_undef(_:)-5fet1)
- [func simd_make_ushort32_undef(simd_ushort4) -> simd_ushort32](/documentation/simd/simd_make_ushort32_undef(_:)-563cu)
- [func simd_make_ushort32_undef(simd_ushort8) -> simd_ushort32](/documentation/simd/simd_make_ushort32_undef(_:)-4r2aq)
- [func simd_make_ushort32_undef(simd_ushort16) -> simd_ushort32](/documentation/simd/simd_make_ushort32_undef(_:)-ie6m)

### Functions to Create Thirty Two-Element Vectors From Scalar Values

- [func simd_make_ushort32(UInt16) -> simd_ushort32](/documentation/simd/simd_make_ushort32(_:)-9so7l)
- [func simd_make_ushort32_undef(UInt16) -> simd_ushort32](/documentation/simd/simd_make_ushort32_undef(_:)-1kuiz)

### Common Functions

- [func simd_clamp(simd_ushort32, simd_ushort32, simd_ushort32) -> simd_ushort32](/documentation/simd/simd_clamp(_:_:_:)-8pjou)
- [func simd_equal(simd_ushort32, simd_ushort32) -> simd_bool](/documentation/simd/simd_equal(_:_:)-4rifl)

### Reduce Functions

- [func simd_reduce_min(simd_ushort32) -> UInt16](/documentation/simd/simd_reduce_min(_:)-2b90g)
- [func simd_reduce_max(simd_ushort32) -> UInt16](/documentation/simd/simd_reduce_max(_:)-9irzc)
- [func simd_reduce_add(simd_ushort32) -> UInt16](/documentation/simd/simd_reduce_add(_:)-1uuef)

### Extrema Functions

- [func simd_min(simd_ushort32, simd_ushort32) -> simd_ushort32](/documentation/simd/simd_min(_:_:)-4512d)
- [func simd_max(simd_ushort32, simd_ushort32) -> simd_ushort32](/documentation/simd/simd_max(_:_:)-3xzw5)

### Logic and Bitwise Functions

- [func simd_any(simd_ushort32) -> simd_bool](/documentation/simd/simd_any(_:)-3au8l)
- [func simd_all(simd_ushort32) -> simd_bool](/documentation/simd/simd_all(_:)-1kmnn)
- [func simd_bitselect(simd_ushort32, simd_ushort32, simd_short32) -> simd_ushort32](/documentation/simd/simd_bitselect(_:_:_:)-6mgti)

### Alternative Type Alias

- [vector_ushort32](/documentation/simd/vector_ushort32)
- [simd_ushort4](/documentation/simd/simd_ushort4)

### Functions to Create Four-Element Vectors From Other Vectors

- [func simd_make_ushort4(simd_ushort2) -> simd_ushort4](/documentation/simd/simd_make_ushort4(_:)-35tv2)
- [func simd_make_ushort4(simd_ushort3) -> simd_ushort4](/documentation/simd/simd_make_ushort4(_:)-38zbb)
- [func simd_make_ushort4(simd_ushort4) -> simd_ushort4](/documentation/simd/simd_make_ushort4(_:)-3qyfo)
- [func simd_make_ushort4(simd_ushort8) -> simd_ushort4](/documentation/simd/simd_make_ushort4(_:)-45zew)
- [func simd_make_ushort4(simd_ushort16) -> simd_ushort4](/documentation/simd/simd_make_ushort4(_:)-2aylo)
- [func simd_make_ushort4(simd_ushort32) -> simd_ushort4](/documentation/simd/simd_make_ushort4(_:)-7bisx)
- [func simd_make_ushort4(simd_ushort2, simd_ushort2) -> simd_ushort4](/documentation/simd/simd_make_ushort4(_:_:)-33b7a)
- [func simd_make_ushort4_undef(simd_ushort2) -> simd_ushort4](/documentation/simd/simd_make_ushort4_undef(_:)-263ji)
- [func simd_make_ushort4_undef(simd_ushort3) -> simd_ushort4](/documentation/simd/simd_make_ushort4_undef(_:)-22y87)

### Functions to Create Four-Element Vectors From Scalar Values

- [func simd_make_ushort4(UInt16) -> simd_ushort4](/documentation/simd/simd_make_ushort4(_:)-85y03)
- [func simd_make_ushort4(UInt16, UInt16, UInt16, UInt16) -> simd_ushort4](/documentation/simd/simd_make_ushort4(_:_:_:_:))
- [func simd_make_ushort4_undef(UInt16) -> simd_ushort4](/documentation/simd/simd_make_ushort4_undef(_:)-9xmiv)

### Functions to Create Four-Element Vectors From Combinations of Vectors and Scalar Values

- [func simd_make_ushort4(simd_ushort2, UInt16, UInt16) -> simd_ushort4](/documentation/simd/simd_make_ushort4(_:_:_:)-5tiuy)
- [func simd_make_ushort4(simd_ushort3, UInt16) -> simd_ushort4](/documentation/simd/simd_make_ushort4(_:_:)-44sd1)
- [func simd_make_ushort4(UInt16, UInt16, simd_ushort2) -> simd_ushort4](/documentation/simd/simd_make_ushort4(_:_:_:)-3yjly)
- [func simd_make_ushort4(UInt16, simd_ushort2, UInt16) -> simd_ushort4](/documentation/simd/simd_make_ushort4(_:_:_:)-53g72)
- [func simd_make_ushort4(UInt16, simd_ushort3) -> simd_ushort4](/documentation/simd/simd_make_ushort4(_:_:)-4t4aq)

### Common Functions

- [func simd_clamp(simd_ushort4, simd_ushort4, simd_ushort4) -> simd_ushort4](/documentation/simd/simd_clamp(_:_:_:)-72wjb)
- [func simd_equal(simd_ushort4, simd_ushort4) -> simd_bool](/documentation/simd/simd_equal(_:_:)-9613j)

### Reduce Functions

- [func simd_reduce_min(simd_ushort4) -> UInt16](/documentation/simd/simd_reduce_min(_:)-4usy2)
- [func simd_reduce_max(simd_ushort4) -> UInt16](/documentation/simd/simd_reduce_max(_:)-4qq8a)
- [func simd_reduce_add(simd_ushort4) -> UInt16](/documentation/simd/simd_reduce_add(_:)-2yjso)

### Extrema Functions

- [func simd_min(simd_ushort4, simd_ushort4) -> simd_ushort4](/documentation/simd/simd_min(_:_:)-9tvdl)
- [func simd_max(simd_ushort4, simd_ushort4) -> simd_ushort4](/documentation/simd/simd_max(_:_:)-64jwl)

### Logic and Bitwise Functions

- [func simd_any(simd_ushort4) -> simd_bool](/documentation/simd/simd_any(_:)-6cx6b)
- [func simd_all(simd_ushort4) -> simd_bool](/documentation/simd/simd_all(_:)-1jswd)
- [func simd_bitselect(simd_ushort4, simd_ushort4, simd_short4) -> simd_ushort4](/documentation/simd/simd_bitselect(_:_:_:)-ryof)

### Alternative Type Alias

- [vector_ushort4](/documentation/simd/vector_ushort4)
- [simd_ushort8](/documentation/simd/simd_ushort8)

### Functions to Create Eight-Element Vectors From Other Vectors

- [func simd_make_ushort8(simd_ushort2) -> simd_ushort8](/documentation/simd/simd_make_ushort8(_:)-1e906)
- [func simd_make_ushort8(simd_ushort3) -> simd_ushort8](/documentation/simd/simd_make_ushort8(_:)-1henz)
- [func simd_make_ushort8(simd_ushort4) -> simd_ushort8](/documentation/simd/simd_make_ushort8(_:)-17t38)
- [func simd_make_ushort8(simd_ushort8) -> simd_ushort8](/documentation/simd/simd_make_ushort8(_:)-2e4yw)
- [func simd_make_ushort8(simd_ushort16) -> simd_ushort8](/documentation/simd/simd_make_ushort8(_:)-5yzvk)
- [func simd_make_ushort8(simd_ushort32) -> simd_ushort8](/documentation/simd/simd_make_ushort8(_:)-4t9gk)
- [func simd_make_ushort8(simd_ushort4, simd_ushort4) -> simd_ushort8](/documentation/simd/simd_make_ushort8(_:_:))
- [func simd_make_ushort8_undef(simd_ushort2) -> simd_ushort8](/documentation/simd/simd_make_ushort8_undef(_:)-49rg0)
- [func simd_make_ushort8_undef(simd_ushort3) -> simd_ushort8](/documentation/simd/simd_make_ushort8_undef(_:)-46lw9)
- [func simd_make_ushort8_undef(simd_ushort4) -> simd_ushort8](/documentation/simd/simd_make_ushort8_undef(_:)-416aa)

### Functions to Create Eight-Element Vectors From Scalar Values

- [func simd_make_ushort8(UInt16) -> simd_ushort8](/documentation/simd/simd_make_ushort8(_:)-66ltd)
- [func simd_make_ushort8_undef(UInt16) -> simd_ushort8](/documentation/simd/simd_make_ushort8_undef(_:)-wluw)

### Common Functions

- [func simd_clamp(simd_ushort8, simd_ushort8, simd_ushort8) -> simd_ushort8](/documentation/simd/simd_clamp(_:_:_:)-81cik)
- [func simd_equal(simd_ushort8, simd_ushort8) -> simd_bool](/documentation/simd/simd_equal(_:_:)-3fkex)

### Reduce Functions

- [func simd_reduce_min(simd_ushort8) -> UInt16](/documentation/simd/simd_reduce_min(_:)-3oh9i)
- [func simd_reduce_max(simd_ushort8) -> UInt16](/documentation/simd/simd_reduce_max(_:)-55hce)
- [func simd_reduce_add(simd_ushort8) -> UInt16](/documentation/simd/simd_reduce_add(_:)-3b3cs)

### Extrema Functions

- [func simd_min(simd_ushort8, simd_ushort8) -> simd_ushort8](/documentation/simd/simd_min(_:_:)-2600d)
- [func simd_max(simd_ushort8, simd_ushort8) -> simd_ushort8](/documentation/simd/simd_max(_:_:)-30jsw)

### Logic and Bitwise Functions

- [func simd_any(simd_ushort8) -> simd_bool](/documentation/simd/simd_any(_:)-6pgp3)
- [func simd_all(simd_ushort8) -> simd_bool](/documentation/simd/simd_all(_:)-1yk7d)
- [func simd_bitselect(simd_ushort8, simd_ushort8, simd_short8) -> simd_ushort8](/documentation/simd/simd_bitselect(_:_:_:)-4yay5)

### Alternative Type Alias

- [vector_ushort8](/documentation/simd/vector_ushort8)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
