# Metal Performance Shaders Documentation

Source: https://sosumi.ai/documentation/metalperformanceshaders

---
title: Metal Performance Shaders
source: https://developer.apple.com/documentation/metalperformanceshaders
timestamp: 2026-02-13T18:59:36.369Z
---

## Fundamentals

- [The MPSKernel Class](/documentation/metalperformanceshaders/the_mpskernel_class)
- [Tuning Hints](/documentation/metalperformanceshaders/tuning_hints)

## Device Support

- [func MPSSupportsMTLDevice((any MTLDevice)?) -> Bool](/documentation/metalperformanceshaders/1618849-mpssupportsmtldevice)

## Image Filters

- [Image Filters](/documentation/metalperformanceshaders/image_filters)

### Morphological Image Filters

- [MPSImageAreaMax](/documentation/metalperformanceshaders/mpsimageareamax)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimageareamax/2866327-init)

#### Methods

- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int)](/documentation/metalperformanceshaders/mpsimageareamax/1618281-init)

#### Properties

- [var kernelHeight: Int](/documentation/metalperformanceshaders/mpsimageareamax/1618277-kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshaders/mpsimageareamax/1618282-kernelwidth)
- [MPSImageDilate](/documentation/metalperformanceshaders/mpsimagedilate)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagedilate/2866325-init)

#### Methods

- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int, values: UnsafePointer<Float>)](/documentation/metalperformanceshaders/mpsimagedilate/1618285-init)

#### Properties

- [var kernelHeight: Int](/documentation/metalperformanceshaders/mpsimagedilate/1618280-kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshaders/mpsimagedilate/1618279-kernelwidth)
- [MPSImageAreaMin](/documentation/metalperformanceshaders/mpsimageareamin)
- [MPSImageErode](/documentation/metalperformanceshaders/mpsimageerode)

### Convolution Image Filters

- [MPSImageConvolution](/documentation/metalperformanceshaders/mpsimageconvolution)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimageconvolution/2866148-init)

#### Methods

- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int, weights: UnsafePointer<Float>)](/documentation/metalperformanceshaders/mpsimageconvolution/1618902-init)

#### Properties

- [var kernelHeight: Int](/documentation/metalperformanceshaders/mpsimageconvolution/1618842-kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshaders/mpsimageconvolution/1618868-kernelwidth)
- [var bias: Float](/documentation/metalperformanceshaders/mpsimageconvolution/1618841-bias)
- [MPSImageMedian](/documentation/metalperformanceshaders/mpsimagemedian)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagemedian/2865529-init)

#### Methods

- [init(device: any MTLDevice, kernelDiameter: Int)](/documentation/metalperformanceshaders/mpsimagemedian/1618837-init)
- [class func maxKernelDiameter() -> Int](/documentation/metalperformanceshaders/mpsimagemedian/1618830-maxkerneldiameter)
- [class func minKernelDiameter() -> Int](/documentation/metalperformanceshaders/mpsimagemedian/1618864-minkerneldiameter)

#### Properties

- [var kernelDiameter: Int](/documentation/metalperformanceshaders/mpsimagemedian/1618909-kerneldiameter)
- [MPSImageBox](/documentation/metalperformanceshaders/mpsimagebox)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagebox/2866153-init)

#### Methods

- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int)](/documentation/metalperformanceshaders/mpsimagebox/1618789-init)

#### Properties

- [var kernelHeight: Int](/documentation/metalperformanceshaders/mpsimagebox/1618739-kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshaders/mpsimagebox/1618834-kernelwidth)
- [MPSImageTent](/documentation/metalperformanceshaders/mpsimagetent)
- [MPSImageGaussianBlur](/documentation/metalperformanceshaders/mpsimagegaussianblur)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagegaussianblur/2866150-init)

#### Methods

- [init(device: any MTLDevice, sigma: Float)](/documentation/metalperformanceshaders/mpsimagegaussianblur/1618813-init)

#### Properties

- [var sigma: Float](/documentation/metalperformanceshaders/mpsimagegaussianblur/1618850-sigma)
- [MPSImageGaussianPyramid](/documentation/metalperformanceshaders/mpsimagegaussianpyramid)
- [MPSImageSobel](/documentation/metalperformanceshaders/mpsimagesobel)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagesobel/2866152-init)

#### Methods

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagesobel/1618843-init)
- [init(device: any MTLDevice, linearGrayColorTransform: UnsafePointer<Float>)](/documentation/metalperformanceshaders/mpsimagesobel/1618899-init)

#### Properties

- [var colorTransform: UnsafePointer<Float>](/documentation/metalperformanceshaders/mpsimagesobel/1618777-colortransform)
- [MPSImageLaplacian](/documentation/metalperformanceshaders/mpsimagelaplacian)

#### Properties

- [var bias: Float](/documentation/metalperformanceshaders/mpsimagelaplacian/1648929-bias)
- [MPSImageLaplacianPyramid](/documentation/metalperformanceshaders/mpsimagelaplacianpyramid)

#### Instance Properties

- [var laplacianBias: Float](/documentation/metalperformanceshaders/mpsimagelaplacianpyramid/2966645-laplacianbias)
- [var laplacianScale: Float](/documentation/metalperformanceshaders/mpsimagelaplacianpyramid/2966646-laplacianscale)
- [MPSImageLaplacianPyramidAdd](/documentation/metalperformanceshaders/mpsimagelaplacianpyramidadd)
- [MPSImageLaplacianPyramidSubtract](/documentation/metalperformanceshaders/mpsimagelaplacianpyramidsubtract)
- [MPSImagePyramid](/documentation/metalperformanceshaders/mpsimagepyramid)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagepyramid/2866151-init)

#### Methods

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagepyramid/1648935-init)
- [init(device: any MTLDevice, centerWeight: Float)](/documentation/metalperformanceshaders/mpsimagepyramid/1648889-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int, weights: UnsafePointer<Float>)](/documentation/metalperformanceshaders/mpsimagepyramid/1648821-init)

#### Properties

- [var kernelWidth: Int](/documentation/metalperformanceshaders/mpsimagepyramid/1648842-kernelwidth)
- [var kernelHeight: Int](/documentation/metalperformanceshaders/mpsimagepyramid/1648863-kernelheight)

### Histogram Image Filters

- [MPSImageHistogram](/documentation/metalperformanceshaders/mpsimagehistogram)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagehistogram/2867090-init)

#### Methods

- [init(device: any MTLDevice, histogramInfo: UnsafePointer<MPSImageHistogramInfo>)](/documentation/metalperformanceshaders/mpsimagehistogram/1618910-init)
- [MPSImageHistogramInfo](/documentation/metalperformanceshaders/mpsimagehistograminfo)

##### Initializers

- [init()](/documentation/metalperformanceshaders/mpsimagehistograminfo/1618769-init)
- [init(numberOfHistogramEntries: Int, histogramForAlpha: ObjCBool, minPixelValue: vector_float4, maxPixelValue: vector_float4)](/documentation/metalperformanceshaders/mpsimagehistograminfo/1618832-init)

##### Instance Properties

- [var histogramForAlpha: ObjCBool](/documentation/metalperformanceshaders/mpsimagehistograminfo/1618840-histogramforalpha)
- [var maxPixelValue: vector_float4](/documentation/metalperformanceshaders/mpsimagehistograminfo/1618847-maxpixelvalue)
- [var minPixelValue: vector_float4](/documentation/metalperformanceshaders/mpsimagehistograminfo/1618749-minpixelvalue)
- [var numberOfHistogramEntries: Int](/documentation/metalperformanceshaders/mpsimagehistograminfo/1618805-numberofhistogramentries)
- [func encode(to: any MTLCommandBuffer, sourceTexture: any MTLTexture, histogram: any MTLBuffer, histogramOffset: Int)](/documentation/metalperformanceshaders/mpsimagehistogram/1618853-encode)
- [func histogramSize(forSourceFormat: MTLPixelFormat) -> Int](/documentation/metalperformanceshaders/mpsimagehistogram/1618839-histogramsize)

#### Properties

- [var clipRectSource: MTLRegion](/documentation/metalperformanceshaders/mpsimagehistogram/1618765-cliprectsource)
- [var zeroHistogram: Bool](/documentation/metalperformanceshaders/mpsimagehistogram/1618891-zerohistogram)
- [var histogramInfo: MPSImageHistogramInfo](/documentation/metalperformanceshaders/mpsimagehistogram/1618844-histograminfo)
- [var minPixelThresholdValue: vector_float4](/documentation/metalperformanceshaders/mpsimagehistogram/2867008-minpixelthresholdvalue)
- [MPSImageHistogramEqualization](/documentation/metalperformanceshaders/mpsimagehistogramequalization)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagehistogramequalization/2866993-init)

#### Methods

- [init(device: any MTLDevice, histogramInfo: UnsafePointer<MPSImageHistogramInfo>)](/documentation/metalperformanceshaders/mpsimagehistogramequalization/1618856-init)
- [func encodeTransform(to: any MTLCommandBuffer, sourceTexture: any MTLTexture, histogram: any MTLBuffer, histogramOffset: Int)](/documentation/metalperformanceshaders/mpsimagehistogramequalization/1618746-encodetransform)

#### Properties

- [var histogramInfo: MPSImageHistogramInfo](/documentation/metalperformanceshaders/mpsimagehistogramequalization/1618775-histograminfo)
- [MPSImageHistogramSpecification](/documentation/metalperformanceshaders/mpsimagehistogramspecification)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagehistogramspecification/2867143-init)

#### Methods

- [init(device: any MTLDevice, histogramInfo: UnsafePointer<MPSImageHistogramInfo>)](/documentation/metalperformanceshaders/mpsimagehistogramspecification/1618907-init)
- [func encodeTransform(to: any MTLCommandBuffer, sourceTexture: any MTLTexture, sourceHistogram: any MTLBuffer, sourceHistogramOffset: Int, desiredHistogram: any MTLBuffer, desiredHistogramOffset: Int)](/documentation/metalperformanceshaders/mpsimagehistogramspecification/1618854-encodetransform)

#### Properties

- [var histogramInfo: MPSImageHistogramInfo](/documentation/metalperformanceshaders/mpsimagehistogramspecification/1618810-histograminfo)

### Image Threshold Filters

- [MPSImageThresholdBinary](/documentation/metalperformanceshaders/mpsimagethresholdbinary)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagethresholdbinary/2865668-init)

#### Methods

- [init(device: any MTLDevice, thresholdValue: Float, maximumValue: Float, linearGrayColorTransform: UnsafePointer<Float>?)](/documentation/metalperformanceshaders/mpsimagethresholdbinary/1618855-init)

#### Properties

- [var thresholdValue: Float](/documentation/metalperformanceshaders/mpsimagethresholdbinary/1618851-thresholdvalue)
- [var maximumValue: Float](/documentation/metalperformanceshaders/mpsimagethresholdbinary/1618852-maximumvalue)
- [var transform: UnsafePointer<Float>](/documentation/metalperformanceshaders/mpsimagethresholdbinary/1618744-transform)
- [MPSImageThresholdBinaryInverse](/documentation/metalperformanceshaders/mpsimagethresholdbinaryinverse)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagethresholdbinaryinverse/2865666-init)

#### Methods

- [init(device: any MTLDevice, thresholdValue: Float, maximumValue: Float, linearGrayColorTransform: UnsafePointer<Float>?)](/documentation/metalperformanceshaders/mpsimagethresholdbinaryinverse/1618903-init)

#### Properties

- [var thresholdValue: Float](/documentation/metalperformanceshaders/mpsimagethresholdbinaryinverse/1618845-thresholdvalue)
- [var maximumValue: Float](/documentation/metalperformanceshaders/mpsimagethresholdbinaryinverse/1618906-maximumvalue)
- [var transform: UnsafePointer<Float>](/documentation/metalperformanceshaders/mpsimagethresholdbinaryinverse/1618904-transform)
- [MPSImageThresholdToZero](/documentation/metalperformanceshaders/mpsimagethresholdtozero)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagethresholdtozero/2865665-init)

#### Methods

- [init(device: any MTLDevice, thresholdValue: Float, linearGrayColorTransform: UnsafePointer<Float>?)](/documentation/metalperformanceshaders/mpsimagethresholdtozero/1618865-init)

#### Properties

- [var thresholdValue: Float](/documentation/metalperformanceshaders/mpsimagethresholdtozero/1618767-thresholdvalue)
- [var transform: UnsafePointer<Float>](/documentation/metalperformanceshaders/mpsimagethresholdtozero/1618823-transform)
- [MPSImageThresholdToZeroInverse](/documentation/metalperformanceshaders/mpsimagethresholdtozeroinverse)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagethresholdtozeroinverse/2865667-init)

#### New Methods

- [init(device: any MTLDevice, thresholdValue: Float, linearGrayColorTransform: UnsafePointer<Float>?)](/documentation/metalperformanceshaders/mpsimagethresholdtozeroinverse/1618911-init)

#### Properties

- [var thresholdValue: Float](/documentation/metalperformanceshaders/mpsimagethresholdtozeroinverse/1618914-thresholdvalue)
- [var transform: UnsafePointer<Float>](/documentation/metalperformanceshaders/mpsimagethresholdtozeroinverse/1618828-transform)
- [MPSImageThresholdTruncate](/documentation/metalperformanceshaders/mpsimagethresholdtruncate)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagethresholdtruncate/2865664-init)

#### Methods

- [init(device: any MTLDevice, thresholdValue: Float, linearGrayColorTransform: UnsafePointer<Float>?)](/documentation/metalperformanceshaders/mpsimagethresholdtruncate/1618818-init)

#### Properties

- [var thresholdValue: Float](/documentation/metalperformanceshaders/mpsimagethresholdtruncate/1618882-thresholdvalue)
- [var transform: UnsafePointer<Float>](/documentation/metalperformanceshaders/mpsimagethresholdtruncate/1618787-transform)

### Image Integral Filters

- [MPSImageIntegral](/documentation/metalperformanceshaders/mpsimageintegral)
- [MPSImageIntegralOfSquares](/documentation/metalperformanceshaders/mpsimageintegralofsquares)

### Image Manipulation Filters

- [MPSImageConversion](/documentation/metalperformanceshaders/mpsimageconversion)

#### Methods

- [init(device: any MTLDevice, srcAlpha: MPSAlphaType, destAlpha: MPSAlphaType, backgroundColor: UnsafeMutablePointer<CGFloat>?, conversionInfo: CGColorConversionInfo?)](/documentation/metalperformanceshaders/mpsimageconversion/2206722-init)
- [MPSAlphaType](/documentation/metalperformanceshaders/mpsalphatype)

##### Constants

- [case nonPremultiplied](/documentation/metalperformanceshaders/mpsalphatype/nonpremultiplied)
- [case alphaIsOne](/documentation/metalperformanceshaders/mpsalphatype/alphaisone)
- [case premultiplied](/documentation/metalperformanceshaders/mpsalphatype/premultiplied)

#### Properties

- [var sourceAlpha: MPSAlphaType](/documentation/metalperformanceshaders/mpsimageconversion/1648518-sourcealpha)
- [var destinationAlpha: MPSAlphaType](/documentation/metalperformanceshaders/mpsimageconversion/1648515-destinationalpha)
- [MPSImageScale](/documentation/metalperformanceshaders/mpsimagescale)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagescale/2881187-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagescale/2881186-init)

#### Instance Properties

- [var scaleTransform: UnsafePointer<MPSScaleTransform>?](/documentation/metalperformanceshaders/mpsimagescale/2881183-scaletransform)
- [MPSImageLanczosScale](/documentation/metalperformanceshaders/mpsimagelanczosscale)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagelanczosscale/2867140-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagelanczosscale/2867001-init)

#### Properties

- [MPSScaleTransform](/documentation/metalperformanceshaders/mpsscaletransform)

##### Initializers

- [init()](/documentation/metalperformanceshaders/mpsscaletransform/1618820-init)
- [init(scaleX: Double, scaleY: Double, translateX: Double, translateY: Double)](/documentation/metalperformanceshaders/mpsscaletransform/1618862-init)

##### Instance Properties

- [var scaleX: Double](/documentation/metalperformanceshaders/mpsscaletransform/1618773-scalex)
- [var scaleY: Double](/documentation/metalperformanceshaders/mpsscaletransform/1618785-scaley)
- [var translateX: Double](/documentation/metalperformanceshaders/mpsscaletransform/1618795-translatex)
- [var translateY: Double](/documentation/metalperformanceshaders/mpsscaletransform/1618872-translatey)
- [MPSImageBilinearScale](/documentation/metalperformanceshaders/mpsimagebilinearscale)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagebilinearscale/2881188-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagebilinearscale/2881184-init)
- [MPSImageTranspose](/documentation/metalperformanceshaders/mpsimagetranspose)

### Image Statistics Filters

- [MPSImageStatisticsMean](/documentation/metalperformanceshaders/mpsimagestatisticsmean)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagestatisticsmean/2867124-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagestatisticsmean/2867156-init)

#### Instance Properties

- [var clipRectSource: MTLRegion](/documentation/metalperformanceshaders/mpsimagestatisticsmean/2867093-cliprectsource)
- [MPSImageStatisticsMeanAndVariance](/documentation/metalperformanceshaders/mpsimagestatisticsmeanandvariance)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagestatisticsmeanandvariance/2867044-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagestatisticsmeanandvariance/2867165-init)

#### Instance Properties

- [var clipRectSource: MTLRegion](/documentation/metalperformanceshaders/mpsimagestatisticsmeanandvariance/2867131-cliprectsource)
- [MPSImageStatisticsMinAndMax](/documentation/metalperformanceshaders/mpsimagestatisticsminandmax)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagestatisticsminandmax/2867026-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagestatisticsminandmax/2867125-init)

#### Instance Properties

- [var clipRectSource: MTLRegion](/documentation/metalperformanceshaders/mpsimagestatisticsminandmax/2867045-cliprectsource)

### Image Reduction Filters

- [MPSImageReduceRowMax](/documentation/metalperformanceshaders/mpsimagereducerowmax)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagereducerowmax/2942328-init)
- [MPSImageReduceRowMin](/documentation/metalperformanceshaders/mpsimagereducerowmin)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagereducerowmin/2942325-init)
- [MPSImageReduceRowSum](/documentation/metalperformanceshaders/mpsimagereducerowsum)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagereducerowsum/2942334-init)
- [MPSImageReduceRowMean](/documentation/metalperformanceshaders/mpsimagereducerowmean)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagereducerowmean/2942322-init)
- [MPSImageReduceColumnMax](/documentation/metalperformanceshaders/mpsimagereducecolumnmax)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagereducecolumnmax/2942318-init)
- [MPSImageReduceColumnMin](/documentation/metalperformanceshaders/mpsimagereducecolumnmin)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagereducecolumnmin/2942333-init)
- [MPSImageReduceColumnSum](/documentation/metalperformanceshaders/mpsimagereducecolumnsum)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagereducecolumnsum/2942321-init)
- [MPSImageReduceColumnMean](/documentation/metalperformanceshaders/mpsimagereducecolumnmean)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagereducecolumnmean/2942331-init)
- [MPSImageReduceUnary](/documentation/metalperformanceshaders/mpsimagereduceunary)

#### Instance Properties

- [var clipRectSource: MTLRegion](/documentation/metalperformanceshaders/mpsimagereduceunary/2942332-cliprectsource)

### Image Arithmetic Filters

- [MPSImageAdd](/documentation/metalperformanceshaders/mpsimageadd)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimageadd/2866610-init)
- [MPSImageSubtract](/documentation/metalperformanceshaders/mpsimagesubtract)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagesubtract/2866613-init)
- [MPSImageMultiply](/documentation/metalperformanceshaders/mpsimagemultiply)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagemultiply/2866600-init)
- [MPSImageDivide](/documentation/metalperformanceshaders/mpsimagedivide)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagedivide/2866606-init)
- [MPSImageArithmetic](/documentation/metalperformanceshaders/mpsimagearithmetic)

#### Instance Properties

- [var bias: Float](/documentation/metalperformanceshaders/mpsimagearithmetic/2866609-bias)
- [var primaryScale: Float](/documentation/metalperformanceshaders/mpsimagearithmetic/2866602-primaryscale)
- [var primaryStrideInPixels: MTLSize](/documentation/metalperformanceshaders/mpsimagearithmetic/2889864-primarystrideinpixels)
- [var secondaryScale: Float](/documentation/metalperformanceshaders/mpsimagearithmetic/2866601-secondaryscale)
- [var secondaryStrideInPixels: MTLSize](/documentation/metalperformanceshaders/mpsimagearithmetic/2889865-secondarystrideinpixels)
- [var maximumValue: Float](/documentation/metalperformanceshaders/mpsimagearithmetic/2942356-maximumvalue)
- [var minimumValue: Float](/documentation/metalperformanceshaders/mpsimagearithmetic/2942357-minimumvalue)

### Euclidean Distance Transform Filter

- [MPSImageEuclideanDistanceTransform](/documentation/metalperformanceshaders/mpsimageeuclideandistancetransform)

#### Creating a Euclidean distance transform

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimageeuclideandistancetransform/2953973-init)
- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimageeuclideandistancetransform/2953972-init)

#### Limiting the search for nonzero pixels

- [var searchLimitRadius: Float](/documentation/metalperformanceshaders/mpsimageeuclideandistancetransform/3547977-searchlimitradius)

### Fast Guided Filter

- [MPSImageGuidedFilter](/documentation/metalperformanceshaders/mpsimageguidedfilter)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimageguidedfilter/2951903-init)
- [init(device: any MTLDevice, kernelDiameter: Int)](/documentation/metalperformanceshaders/mpsimageguidedfilter/2951910-init)

#### Instance Properties

- [var epsilon: Float](/documentation/metalperformanceshaders/mpsimageguidedfilter/2951908-epsilon)
- [var kernelDiameter: Int](/documentation/metalperformanceshaders/mpsimageguidedfilter/2951909-kerneldiameter)
- [var reconstructOffset: Float](/documentation/metalperformanceshaders/mpsimageguidedfilter/2953079-reconstructoffset)
- [var reconstructScale: Float](/documentation/metalperformanceshaders/mpsimageguidedfilter/2953078-reconstructscale)

#### Instance Methods

- [func encodeReconstruction(commandBuffer: any MTLCommandBuffer, guidance: any MTLTexture, coefficientsA: any MTLTexture, coefficientsB: any MTLTexture, destination: any MTLTexture)](/documentation/metalperformanceshaders/mpsimageguidedfilter/3516398-encodereconstruction)
- [func encodeReconstruction(to: any MTLCommandBuffer, guidanceTexture: any MTLTexture, coefficientsTexture: any MTLTexture, destinationTexture: any MTLTexture)](/documentation/metalperformanceshaders/mpsimageguidedfilter/2951906-encodereconstruction)
- [func encodeRegression(commandBuffer: any MTLCommandBuffer, source: any MTLTexture, guidance: any MTLTexture, weights: (any MTLTexture)?, destinationCoefficientsA: any MTLTexture, destinationCoefficientsB: any MTLTexture)](/documentation/metalperformanceshaders/mpsimageguidedfilter/3516399-encoderegression)
- [func encodeRegression(to: any MTLCommandBuffer, sourceTexture: any MTLTexture, guidanceTexture: any MTLTexture, weightsTexture: (any MTLTexture)?, destinationCoefficientsTexture: any MTLTexture)](/documentation/metalperformanceshaders/mpsimageguidedfilter/2951907-encoderegression)

### Keypoints

- [MPSImageFindKeypoints](/documentation/metalperformanceshaders/mpsimagefindkeypoints)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagefindkeypoints/2873306-init)
- [init(device: any MTLDevice, info: UnsafePointer<MPSImageKeypointRangeInfo>)](/documentation/metalperformanceshaders/mpsimagefindkeypoints/2873309-init)

#### Instance Properties

- [var keypointRangeInfo: MPSImageKeypointRangeInfo](/documentation/metalperformanceshaders/mpsimagefindkeypoints/2873310-keypointrangeinfo)

#### Instance Methods

- [func encode(to: any MTLCommandBuffer, sourceTexture: any MTLTexture, regions: UnsafePointer<MTLRegion>, numberOfRegions: Int, keypointCount: any MTLBuffer, keypointCountBufferOffset: Int, keypointDataBuffer: any MTLBuffer, keypointDataBufferOffset: Int)](/documentation/metalperformanceshaders/mpsimagefindkeypoints/2873307-encode)
- [MPSImageKeypointData](/documentation/metalperformanceshaders/mpsimagekeypointdata)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsimagekeypointdata/2873395-init)
- [init(keypointCoordinate: vector_ushort2, keypointColorValue: Float)](/documentation/metalperformanceshaders/mpsimagekeypointdata/3204129-init)

#### Instance Properties

- [var keypointColorValue: Float](/documentation/metalperformanceshaders/mpsimagekeypointdata/2873303-keypointcolorvalue)
- [var keypointCoordinate: vector_ushort2](/documentation/metalperformanceshaders/mpsimagekeypointdata/2873311-keypointcoordinate)
- [MPSImageKeypointRangeInfo](/documentation/metalperformanceshaders/mpsimagekeypointrangeinfo)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsimagekeypointrangeinfo/2873389-init)
- [init(maximumKeypoints: Int, minimumThresholdValue: Float)](/documentation/metalperformanceshaders/mpsimagekeypointrangeinfo/2878286-init)

#### Instance Properties

- [var maximumKeypoints: Int](/documentation/metalperformanceshaders/mpsimagekeypointrangeinfo/2873308-maximumkeypoints)
- [var minimumThresholdValue: Float](/documentation/metalperformanceshaders/mpsimagekeypointrangeinfo/2873302-minimumthresholdvalue)

### Image Filter Base Classes

- [MPSUnaryImageKernel](/documentation/metalperformanceshaders/mpsunaryimagekernel)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsunaryimagekernel/2866329-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsunaryimagekernel/2866332-init)

#### Methods

- [func encode(commandBuffer: any MTLCommandBuffer, inPlaceTexture: UnsafeMutablePointer<any MTLTexture>, fallbackCopyAllocator: MPSCopyAllocator?) -> Bool](/documentation/metalperformanceshaders/mpsunaryimagekernel/1618873-encode)
- [MPSCopyAllocator](/documentation/metalperformanceshaders/mpscopyallocator)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, destinationImage: MPSImage)](/documentation/metalperformanceshaders/mpsunaryimagekernel/2866328-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceTexture: any MTLTexture, destinationTexture: any MTLTexture)](/documentation/metalperformanceshaders/mpsunaryimagekernel/1618741-encode)
- [func sourceRegion(destinationSize: MTLSize) -> MPSRegion](/documentation/metalperformanceshaders/mpsunaryimagekernel/1618754-sourceregion)

#### Properties

- [var offset: MPSOffset](/documentation/metalperformanceshaders/mpsunaryimagekernel/1618884-offset)
- [MPSOffset](/documentation/metalperformanceshaders/mpsoffset)

##### Initializers

- [init()](/documentation/metalperformanceshaders/mpsoffset/1618896-init)
- [init(x: Int, y: Int, z: Int)](/documentation/metalperformanceshaders/mpsoffset/1618740-init)

##### Instance Properties

- [var x: Int](/documentation/metalperformanceshaders/mpsoffset/1618861-x)
- [var y: Int](/documentation/metalperformanceshaders/mpsoffset/1618846-y)
- [var z: Int](/documentation/metalperformanceshaders/mpsoffset/1618881-z)
- [var clipRect: MTLRegion](/documentation/metalperformanceshaders/mpsunaryimagekernel/1618859-cliprect)
- [MPSRegion](/documentation/metalperformanceshaders/mpsregion)

##### Initializers

- [init()](/documentation/metalperformanceshaders/mpsregion/1618892-init)
- [init(origin: MPSOrigin, size: MPSSize)](/documentation/metalperformanceshaders/mpsregion/1618860-init)

##### Instance Properties

- [var origin: MPSOrigin](/documentation/metalperformanceshaders/mpsregion/1618897-origin)
- [MPSOrigin](/documentation/metalperformanceshaders/mpsorigin)

###### Initializers

- [init()](/documentation/metalperformanceshaders/mpsorigin/1618866-init)
- [init(x: Double, y: Double, z: Double)](/documentation/metalperformanceshaders/mpsorigin/1618888-init)

###### Instance Properties

- [var x: Double](/documentation/metalperformanceshaders/mpsorigin/1618870-x)
- [var y: Double](/documentation/metalperformanceshaders/mpsorigin/1618793-y)
- [var z: Double](/documentation/metalperformanceshaders/mpsorigin/1618833-z)
- [var size: MPSSize](/documentation/metalperformanceshaders/mpsregion/1618858-size)
- [MPSSize](/documentation/metalperformanceshaders/mpssize)

###### Initializers

- [init()](/documentation/metalperformanceshaders/mpssize/1618801-init)
- [init(width: Double, height: Double, depth: Double)](/documentation/metalperformanceshaders/mpssize/1618905-init)

###### Instance Properties

- [var depth: Double](/documentation/metalperformanceshaders/mpssize/1618886-depth)
- [var height: Double](/documentation/metalperformanceshaders/mpssize/1618874-height)
- [var width: Double](/documentation/metalperformanceshaders/mpssize/1618898-width)
- [var edgeMode: MPSImageEdgeMode](/documentation/metalperformanceshaders/mpsunaryimagekernel/1618812-edgemode)
- [MPSImageEdgeMode](/documentation/metalperformanceshaders/mpsimageedgemode)

##### Constants

- [case zero](/documentation/metalperformanceshaders/mpsimageedgemode/zero)
- [case clamp](/documentation/metalperformanceshaders/mpsimageedgemode/clamp)

##### Enumeration Cases

- [case constant](/documentation/metalperformanceshaders/mpsimageedgemode/constant)
- [case mirror](/documentation/metalperformanceshaders/mpsimageedgemode/mirror)
- [case mirrorWithEdge](/documentation/metalperformanceshaders/mpsimageedgemode/mirrorwithedge)
- [MPSBinaryImageKernel](/documentation/metalperformanceshaders/mpsbinaryimagekernel)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsbinaryimagekernel/2866333-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsbinaryimagekernel/2866331-init)

#### Methods

- [func encode(commandBuffer: any MTLCommandBuffer, primaryTexture: any MTLTexture, inPlaceSecondaryTexture: UnsafeMutablePointer<any MTLTexture>, fallbackCopyAllocator: MPSCopyAllocator?) -> Bool](/documentation/metalperformanceshaders/mpsbinaryimagekernel/1618890-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, inPlacePrimaryTexture: UnsafeMutablePointer<any MTLTexture>, secondaryTexture: any MTLTexture, fallbackCopyAllocator: MPSCopyAllocator?) -> Bool](/documentation/metalperformanceshaders/mpsbinaryimagekernel/1618771-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, primaryTexture: any MTLTexture, secondaryTexture: any MTLTexture, destinationTexture: any MTLTexture)](/documentation/metalperformanceshaders/mpsbinaryimagekernel/1618871-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, primaryImage: MPSImage, secondaryImage: MPSImage, destinationImage: MPSImage)](/documentation/metalperformanceshaders/mpsbinaryimagekernel/2866330-encode)
- [func primarySourceRegion(forDestinationSize: MTLSize) -> MPSRegion](/documentation/metalperformanceshaders/mpsbinaryimagekernel/1618900-primarysourceregion)
- [func secondarySourceRegion(forDestinationSize: MTLSize) -> MPSRegion](/documentation/metalperformanceshaders/mpsbinaryimagekernel/1618838-secondarysourceregion)

#### Properties

- [var primaryOffset: MPSOffset](/documentation/metalperformanceshaders/mpsbinaryimagekernel/1618880-primaryoffset)
- [var secondaryOffset: MPSOffset](/documentation/metalperformanceshaders/mpsbinaryimagekernel/1618755-secondaryoffset)
- [var primaryEdgeMode: MPSImageEdgeMode](/documentation/metalperformanceshaders/mpsbinaryimagekernel/1618782-primaryedgemode)
- [var secondaryEdgeMode: MPSImageEdgeMode](/documentation/metalperformanceshaders/mpsbinaryimagekernel/1618848-secondaryedgemode)
- [var clipRect: MTLRegion](/documentation/metalperformanceshaders/mpsbinaryimagekernel/1618879-cliprect)

### Constants

- [MPSRectNoClip](/documentation/metalperformanceshaders/image_filters/mpsrectnoclip)

#### Constants

- [let MPSRectNoClip: MTLRegion](/documentation/metalperformanceshaders/mpsrectnoclip)

## Neural Networks

- [Training a Neural Network with Metal Performance Shaders](/documentation/metalperformanceshaders/training_a_neural_network_with_metal_performance_shaders)
- [MPSImage](/documentation/metalperformanceshaders/mpsimage)

### Initializers

- [init(device: any MTLDevice, imageDescriptor: MPSImageDescriptor)](/documentation/metalperformanceshaders/mpsimage/1648920-init)
- [MPSImageDescriptor](/documentation/metalperformanceshaders/mpsimagedescriptor)

#### Methods

- [init(channelFormat: MPSImageFeatureChannelFormat, width: Int, height: Int, featureChannels: Int)](/documentation/metalperformanceshaders/mpsimagedescriptor/1648819-init)
- [init(channelFormat: MPSImageFeatureChannelFormat, width: Int, height: Int, featureChannels: Int, numberOfImages: Int, usage: MTLTextureUsage)](/documentation/metalperformanceshaders/mpsimagedescriptor/1648893-init)

#### Properties

- [var width: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648830-width)
- [var height: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648947-height)
- [var featureChannels: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648918-featurechannels)
- [var numberOfImages: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648846-numberofimages)
- [var pixelFormat: MTLPixelFormat](/documentation/metalperformanceshaders/mpsimagedescriptor/1648913-pixelformat)
- [var channelFormat: MPSImageFeatureChannelFormat](/documentation/metalperformanceshaders/mpsimagedescriptor/1648818-channelformat)
- [var cpuCacheMode: MTLCPUCacheMode](/documentation/metalperformanceshaders/mpsimagedescriptor/1648930-cpucachemode)
- [var storageMode: MTLStorageMode](/documentation/metalperformanceshaders/mpsimagedescriptor/1648955-storagemode)
- [var usage: MTLTextureUsage](/documentation/metalperformanceshaders/mpsimagedescriptor/1648937-usage)

#### Instance Methods

- [func copy(with: NSZone?) -> Self](/documentation/metalperformanceshaders/mpsimagedescriptor/3020686-copy)
- [init(texture: any MTLTexture, featureChannels: Int)](/documentation/metalperformanceshaders/mpsimage/2097547-init)
- [init(parentImage: MPSImage, sliceRange: NSRange, featureChannels: Int)](/documentation/metalperformanceshaders/mpsimage/2942493-init)

### Methods

- [func setPurgeableState(MPSPurgeableState) -> MPSPurgeableState](/documentation/metalperformanceshaders/mpsimage/1648820-setpurgeablestate)
- [MPSPurgeableState](/documentation/metalperformanceshaders/mpspurgeablestate)

#### Constants

- [case allocationDeferred](/documentation/metalperformanceshaders/mpspurgeablestate/allocationdeferred)
- [case keepCurrent](/documentation/metalperformanceshaders/mpspurgeablestate/keepcurrent)
- [case nonVolatile](/documentation/metalperformanceshaders/mpspurgeablestate/nonvolatile)
- [case volatile](/documentation/metalperformanceshaders/mpspurgeablestate/volatile)
- [case empty](/documentation/metalperformanceshaders/mpspurgeablestate/empty)

### Methods to Read and Write Raw Data

- [func readBytes(UnsafeMutableRawPointer, dataLayout: MPSDataLayout, bytesPerRow: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2867105-readbytes)
- [func readBytes(UnsafeMutableRawPointer, dataLayout: MPSDataLayout, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2867188-readbytes)
- [func writeBytes(UnsafeRawPointer, dataLayout: MPSDataLayout, bytesPerRow: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2867055-writebytes)
- [func writeBytes(UnsafeRawPointer, dataLayout: MPSDataLayout, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2867189-writebytes)
- [MPSImageReadWriteParams](/documentation/metalperformanceshaders/mpsimagereadwriteparams)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsimagereadwriteparams/2867022-init)
- [init(featureChannelOffset: Int, numberOfFeatureChannelsToReadWrite: Int)](/documentation/metalperformanceshaders/mpsimagereadwriteparams/2867128-init)

#### Instance Properties

- [var featureChannelOffset: Int](/documentation/metalperformanceshaders/mpsimagereadwriteparams/2867064-featurechanneloffset)
- [var numberOfFeatureChannelsToReadWrite: Int](/documentation/metalperformanceshaders/mpsimagereadwriteparams/2867173-numberoffeaturechannelstoreadwri)
- [MPSDataLayout](/documentation/metalperformanceshaders/mpsdatalayout)

#### Enumeration Cases

- [case featureChannelsxHeightxWidth](/documentation/metalperformanceshaders/mpsdatalayout/featurechannelsxheightxwidth)
- [case HeightxWidthxFeatureChannels](/documentation/metalperformanceshaders/mpsdatalayout/heightxwidthxfeaturechannels)

### Methods to Get an Image Allocator

- [class func defaultAllocator() -> any MPSImageAllocator](/documentation/metalperformanceshaders/mpsimage/2867148-defaultallocator)
- [MPSImageAllocator](/documentation/metalperformanceshaders/mpsimageallocator)

#### Instance Methods

- [func image(for: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor, kernel: MPSKernel) -> MPSImage](/documentation/metalperformanceshaders/mpsimageallocator/2866966-image)
- [func imageBatch(for: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor, kernel: MPSKernel, count: Int) -> [MPSImage]](/documentation/metalperformanceshaders/mpsimageallocator/3020685-imagebatch)

### Properties

- [var device: any MTLDevice](/documentation/metalperformanceshaders/mpsimage/1648857-device)
- [var width: Int](/documentation/metalperformanceshaders/mpsimage/1648884-width)
- [var height: Int](/documentation/metalperformanceshaders/mpsimage/1648952-height)
- [var featureChannels: Int](/documentation/metalperformanceshaders/mpsimage/1648901-featurechannels)
- [var numberOfImages: Int](/documentation/metalperformanceshaders/mpsimage/1648900-numberofimages)
- [var textureType: MTLTextureType](/documentation/metalperformanceshaders/mpsimage/1648948-texturetype)
- [MTLTextureType](/documentation/metal/mtltexturetype)
- [var pixelFormat: MTLPixelFormat](/documentation/metalperformanceshaders/mpsimage/1648844-pixelformat)
- [MTLPixelFormat](/documentation/metal/mtlpixelformat)
- [var precision: Int](/documentation/metalperformanceshaders/mpsimage/1648880-precision)
- [var usage: MTLTextureUsage](/documentation/metalperformanceshaders/mpsimage/1648828-usage)
- [MTLTextureUsage](/documentation/metal/mtltextureusage)
- [var pixelSize: Int](/documentation/metalperformanceshaders/mpsimage/1648854-pixelsize)
- [var texture: any MTLTexture](/documentation/metalperformanceshaders/mpsimage/1648903-texture)
- [MTLTexture](/documentation/metal/mtltexture)
- [var label: String?](/documentation/metalperformanceshaders/mpsimage/1648899-label)

### Instance Properties

- [var featureChannelFormat: MPSImageFeatureChannelFormat](/documentation/metalperformanceshaders/mpsimage/3131715-featurechannelformat)
- [var parent: MPSImage?](/documentation/metalperformanceshaders/mpsimage/2942490-parent)

### Instance Methods

- [func batchRepresentation() -> [MPSImage]](/documentation/metalperformanceshaders/mpsimage/2942495-batchrepresentation)
- [func batchRepresentation(withSubRange: NSRange) -> [MPSImage]](/documentation/metalperformanceshaders/mpsimage/2942492-batchrepresentation)
- [func readBytes(UnsafeMutableRawPointer, dataLayout: MPSDataLayout, bytesPerRow: Int, bytesPerImage: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2951914-readbytes)
- [func resourceSize() -> Int](/documentation/metalperformanceshaders/mpsimage/2942494-resourcesize)
- [func subImage(withFeatureChannelRange: NSRange) -> MPSImage](/documentation/metalperformanceshaders/mpsimage/2942488-subimage)
- [func synchronize(on: any MTLCommandBuffer)](/documentation/metalperformanceshaders/mpsimage/2942491-synchronize)
- [func writeBytes(UnsafeRawPointer, dataLayout: MPSDataLayout, bytesPerColumn: Int, bytesPerRow: Int, bytesPerImage: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/3143488-writebytes)
- [func writeBytes(UnsafeRawPointer, dataLayout: MPSDataLayout, bytesPerRow: Int, bytesPerImage: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2951915-writebytes)
- [MPSTemporaryImage](/documentation/metalperformanceshaders/mpstemporaryimage)

### Initializers

- [init(commandBuffer: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor)](/documentation/metalperformanceshaders/mpstemporaryimage/2097545-init)
- [MPSImageDescriptor](/documentation/metalperformanceshaders/mpsimagedescriptor)

#### Methods

- [init(channelFormat: MPSImageFeatureChannelFormat, width: Int, height: Int, featureChannels: Int)](/documentation/metalperformanceshaders/mpsimagedescriptor/1648819-init)
- [init(channelFormat: MPSImageFeatureChannelFormat, width: Int, height: Int, featureChannels: Int, numberOfImages: Int, usage: MTLTextureUsage)](/documentation/metalperformanceshaders/mpsimagedescriptor/1648893-init)

#### Properties

- [var width: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648830-width)
- [var height: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648947-height)
- [var featureChannels: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648918-featurechannels)
- [var numberOfImages: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648846-numberofimages)
- [var pixelFormat: MTLPixelFormat](/documentation/metalperformanceshaders/mpsimagedescriptor/1648913-pixelformat)
- [var channelFormat: MPSImageFeatureChannelFormat](/documentation/metalperformanceshaders/mpsimagedescriptor/1648818-channelformat)
- [var cpuCacheMode: MTLCPUCacheMode](/documentation/metalperformanceshaders/mpsimagedescriptor/1648930-cpucachemode)
- [var storageMode: MTLStorageMode](/documentation/metalperformanceshaders/mpsimagedescriptor/1648955-storagemode)
- [var usage: MTLTextureUsage](/documentation/metalperformanceshaders/mpsimagedescriptor/1648937-usage)

#### Instance Methods

- [func copy(with: NSZone?) -> Self](/documentation/metalperformanceshaders/mpsimagedescriptor/3020686-copy)
- [init(commandBuffer: any MTLCommandBuffer, textureDescriptor: MTLTextureDescriptor)](/documentation/metalperformanceshaders/mpstemporaryimage/2097543-init)
- [MTLTextureDescriptor](/documentation/metal/mtltexturedescriptor)
- [init(commandBuffer: any MTLCommandBuffer, textureDescriptor: MTLTextureDescriptor, featureChannels: Int)](/documentation/metalperformanceshaders/mpstemporaryimage/2942489-init)

### Methods

- [class func prefetchStorage(with: any MTLCommandBuffer, imageDescriptorList: [MPSImageDescriptor])](/documentation/metalperformanceshaders/mpstemporaryimage/2097544-prefetchstorage)

### Methods to Get an Image Allocator

- [class func defaultAllocator() -> any MPSImageAllocator](/documentation/metalperformanceshaders/mpstemporaryimage/2867130-defaultallocator)
- [MPSImageAllocator](/documentation/metalperformanceshaders/mpsimageallocator)

#### Instance Methods

- [func image(for: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor, kernel: MPSKernel) -> MPSImage](/documentation/metalperformanceshaders/mpsimageallocator/2866966-image)
- [func imageBatch(for: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor, kernel: MPSKernel, count: Int) -> [MPSImage]](/documentation/metalperformanceshaders/mpsimageallocator/3020685-imagebatch)

### Properties

- [var readCount: Int](/documentation/metalperformanceshaders/mpstemporaryimage/2097546-readcount)
- [Objects that Simplify the Creation of Neural Networks](/documentation/metalperformanceshaders/objects_that_simplify_the_creation_of_neural_networks)

### Neural Network Graphs

- [MPSNNGraph](/documentation/metalperformanceshaders/mpsnngraph)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnngraph/2867043-init)
- [init?(device: any MTLDevice, resultImage: MPSNNImageNode)](/documentation/metalperformanceshaders/mpsnngraph/2867077-init)
- [init?(device: any MTLDevice, resultImage: MPSNNImageNode, resultImageIsNeeded: Bool)](/documentation/metalperformanceshaders/mpsnngraph/2953955-init)
- [init?(device: any MTLDevice, resultImages: [MPSNNImageNode], resultsAreNeeded: UnsafeMutablePointer<ObjCBool>?)](/documentation/metalperformanceshaders/mpsnngraph/3037385-init)

#### Instance Properties

- [var destinationImageAllocator: any MPSImageAllocator](/documentation/metalperformanceshaders/mpsnngraph/2866998-destinationimageallocator)
- [MPSImageAllocator](/documentation/metalperformanceshaders/mpsimageallocator)

##### Instance Methods

- [func image(for: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor, kernel: MPSKernel) -> MPSImage](/documentation/metalperformanceshaders/mpsimageallocator/2866966-image)
- [func imageBatch(for: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor, kernel: MPSKernel, count: Int) -> [MPSImage]](/documentation/metalperformanceshaders/mpsimageallocator/3020685-imagebatch)
- [var intermediateImageHandles: [any MPSHandle]?](/documentation/metalperformanceshaders/mpsnngraph/2867000-intermediateimagehandles)
- [var outputStateIsTemporary: Bool](/documentation/metalperformanceshaders/mpsnngraph/2867094-outputstateistemporary)
- [var resultHandle: (any MPSHandle)?](/documentation/metalperformanceshaders/mpsnngraph/2867123-resulthandle)
- [var resultStateHandles: [any MPSHandle]?](/documentation/metalperformanceshaders/mpsnngraph/2867149-resultstatehandles)
- [var sourceImageHandles: [any MPSHandle]](/documentation/metalperformanceshaders/mpsnngraph/2867012-sourceimagehandles)
- [var sourceStateHandles: [any MPSHandle]?](/documentation/metalperformanceshaders/mpsnngraph/2867056-sourcestatehandles)
- [var format: MPSImageFeatureChannelFormat](/documentation/metalperformanceshaders/mpsnngraph/2953133-format)
- [var resultImageIsNeeded: Bool](/documentation/metalperformanceshaders/mpsnngraph/2953954-resultimageisneeded)

#### Instance Methods

- [func encode(to: any MTLCommandBuffer, sourceImages: [MPSImage]) -> MPSImage?](/documentation/metalperformanceshaders/mpsnngraph/2867036-encode)
- [func encode(to: any MTLCommandBuffer, sourceImages: [MPSImage], sourceStates: [MPSState]?, intermediateImages: NSMutableArray?, destinationStates: NSMutableArray?) -> MPSImage?](/documentation/metalperformanceshaders/mpsnngraph/2867011-encode)
- [MPSState](/documentation/metalperformanceshaders/mpsstate)

##### Instance Properties

- [var isTemporary: Bool](/documentation/metalperformanceshaders/mpsstate/2867114-istemporary)
- [var label: String?](/documentation/metalperformanceshaders/mpsstate/2867179-label)
- [var readCount: Int](/documentation/metalperformanceshaders/mpsstate/2867042-readcount)
- [var resource: (any MTLResource)?](/documentation/metalperformanceshaders/mpsstate/2942398-resource)
- [var resourceCount: Int](/documentation/metalperformanceshaders/mpsstate/2947900-resourcecount)

##### Initializers

- [init(device: any MTLDevice, bufferSize: Int)](/documentation/metalperformanceshaders/mpsstate/2942392-init)
- [init(device: any MTLDevice, resourceList: MPSStateResourceList)](/documentation/metalperformanceshaders/mpsstate/2947908-init)
- [init(device: any MTLDevice, textureDescriptor: MTLTextureDescriptor)](/documentation/metalperformanceshaders/mpsstate/2942400-init)
- [init(resource: (any MTLResource)?)](/documentation/metalperformanceshaders/mpsstate/2942390-init)
- [init(resources: [any MTLResource]?)](/documentation/metalperformanceshaders/mpsstate/2947895-init)

##### Instance Methods

- [func bufferSize(at: Int) -> Int](/documentation/metalperformanceshaders/mpsstate/2947913-buffersize)
- [func destinationImageDescriptor(forSourceImages: [MPSImage], sourceStates: [MPSState]?, for: MPSKernel, suggestedDescriptor: MPSImageDescriptor) -> MPSImageDescriptor](/documentation/metalperformanceshaders/mpsstate/2942394-destinationimagedescriptor)
- [func resource(at: Int, allocateMemory: Bool) -> (any MTLResource)?](/documentation/metalperformanceshaders/mpsstate/2947916-resource)
- [func resourceSize() -> Int](/documentation/metalperformanceshaders/mpsstate/2942397-resourcesize)
- [func resourceType(at: Int) -> MPSStateResourceType](/documentation/metalperformanceshaders/mpsstate/2947902-resourcetype)
- [func synchronize(on: any MTLCommandBuffer)](/documentation/metalperformanceshaders/mpsstate/2942396-synchronize)
- [func textureInfo(at: Int) -> MPSStateTextureInfo](/documentation/metalperformanceshaders/mpsstate/2947899-textureinfo)

##### Type Methods

- [class func temporaryState(with: any MTLCommandBuffer) -> Self](/documentation/metalperformanceshaders/mpsstate/2942393-temporarystate)
- [class func temporaryState(with: any MTLCommandBuffer, bufferSize: Int) -> Self](/documentation/metalperformanceshaders/mpsstate/2942391-temporarystate)
- [class func temporaryState(with: any MTLCommandBuffer, resourceList: MPSStateResourceList) -> Self](/documentation/metalperformanceshaders/mpsstate/2947915-temporarystate)
- [class func temporaryState(with: any MTLCommandBuffer, textureDescriptor: MTLTextureDescriptor) -> Self](/documentation/metalperformanceshaders/mpsstate/2942395-temporarystate)
- [MPSNNBinaryGradientState](/documentation/metalperformanceshaders/mpsnnbinarygradientstate)
- [MPSNNGradientState](/documentation/metalperformanceshaders/mpsnngradientstate)
- [func executeAsync(withSourceImages: [MPSImage], completionHandler: MPSNNGraphCompletionHandler) -> MPSImage](/documentation/metalperformanceshaders/mpsnngraph/2890826-executeasync)
- [MPSNNGraphCompletionHandler](/documentation/metalperformanceshaders/mpsnngraphcompletionhandler)
- [func encodeBatch(to: any MTLCommandBuffer, sourceImages: [[MPSImage]], sourceStates: [[MPSState]]?) -> [MPSImage]?](/documentation/metalperformanceshaders/mpsnngraph/2953952-encodebatch)
- [func encodeBatch(to: any MTLCommandBuffer, sourceImages: [[MPSImage]], sourceStates: [[MPSState]]?, intermediateImages: NSMutableArray?, destinationStates: NSMutableArray?) -> [MPSImage]?](/documentation/metalperformanceshaders/mpsnngraph/2942459-encodebatch)
- [func readCountForSourceImage(at: Int) -> Int](/documentation/metalperformanceshaders/mpsnngraph/3037386-readcountforsourceimage)
- [func readCountForSourceState(at: Int) -> Int](/documentation/metalperformanceshaders/mpsnngraph/3037387-readcountforsourcestate)
- [func reloadFromDataSources()](/documentation/metalperformanceshaders/mpsnngraph/2976512-reloadfromdatasources)
- [MPSNNImageNode](/documentation/metalperformanceshaders/mpsnnimagenode)

#### Initializers

- [init(handle: (any MPSHandle)?)](/documentation/metalperformanceshaders/mpsnnimagenode/2866483-init)

#### Instance Properties

- [var exportFromGraph: Bool](/documentation/metalperformanceshaders/mpsnnimagenode/2866478-exportfromgraph)
- [var format: MPSImageFeatureChannelFormat](/documentation/metalperformanceshaders/mpsnnimagenode/2866498-format)
- [MPSImageFeatureChannelFormat](/documentation/metalperformanceshaders/mpsimagefeaturechannelformat)

##### Constants

- [case none](/documentation/metalperformanceshaders/mpsimagefeaturechannelformat/none)
- [case unorm8](/documentation/metalperformanceshaders/mpsimagefeaturechannelformat/unorm8)
- [case unorm16](/documentation/metalperformanceshaders/mpsimagefeaturechannelformat/unorm16)
- [case float16](/documentation/metalperformanceshaders/mpsimagefeaturechannelformat/float16)
- [case float32](/documentation/metalperformanceshaders/mpsimagefeaturechannelformat/float32)

##### Enumeration Cases

- [case count](/documentation/metalperformanceshaders/mpsimagefeaturechannelformat/count)
- [var handle: (any MPSHandle)?](/documentation/metalperformanceshaders/mpsnnimagenode/2866406-handle)
- [var imageAllocator: any MPSImageAllocator](/documentation/metalperformanceshaders/mpsnnimagenode/2866490-imageallocator)
- [var stopGradient: Bool](/documentation/metalperformanceshaders/mpsnnimagenode/3020689-stopgradient)
- [var synchronizeResource: Bool](/documentation/metalperformanceshaders/mpsnnimagenode/2942638-synchronizeresource)

#### Type Methods

- [class func exportedNode(with: (any MPSHandle)?) -> Self](/documentation/metalperformanceshaders/mpsnnimagenode/2866440-exportednode)

#### Supporting Types

- [MPSHandle](/documentation/metalperformanceshaders/mpshandle)

##### Instance Methods

- [func label() -> String?](/documentation/metalperformanceshaders/mpshandle/2866414-label)
- [MPSImageFeatureChannelFormat](/documentation/metalperformanceshaders/mpsimagefeaturechannelformat)

##### Constants

- [case none](/documentation/metalperformanceshaders/mpsimagefeaturechannelformat/none)
- [case unorm8](/documentation/metalperformanceshaders/mpsimagefeaturechannelformat/unorm8)
- [case unorm16](/documentation/metalperformanceshaders/mpsimagefeaturechannelformat/unorm16)
- [case float16](/documentation/metalperformanceshaders/mpsimagefeaturechannelformat/float16)
- [case float32](/documentation/metalperformanceshaders/mpsimagefeaturechannelformat/float32)

##### Enumeration Cases

- [case count](/documentation/metalperformanceshaders/mpsimagefeaturechannelformat/count)
- [MPSImageAllocator](/documentation/metalperformanceshaders/mpsimageallocator)

##### Instance Methods

- [func image(for: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor, kernel: MPSKernel) -> MPSImage](/documentation/metalperformanceshaders/mpsimageallocator/2866966-image)
- [func imageBatch(for: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor, kernel: MPSKernel, count: Int) -> [MPSImage]](/documentation/metalperformanceshaders/mpsimageallocator/3020685-imagebatch)
- [MPSHandle](/documentation/metalperformanceshaders/mpshandle)

#### Instance Methods

- [func label() -> String?](/documentation/metalperformanceshaders/mpshandle/2866414-label)

### Arithmetic Layer Nodes

- [MPSNNAdditionNode](/documentation/metalperformanceshaders/mpsnnadditionnode)
- [MPSNNAdditionGradientNode](/documentation/metalperformanceshaders/mpsnnadditiongradientnode)
- [MPSNNSubtractionNode](/documentation/metalperformanceshaders/mpsnnsubtractionnode)
- [MPSNNSubtractionGradientNode](/documentation/metalperformanceshaders/mpsnnsubtractiongradientnode)
- [MPSNNMultiplicationNode](/documentation/metalperformanceshaders/mpsnnmultiplicationnode)
- [MPSNNMultiplicationGradientNode](/documentation/metalperformanceshaders/mpsnnmultiplicationgradientnode)
- [MPSNNDivisionNode](/documentation/metalperformanceshaders/mpsnndivisionnode)
- [MPSNNBinaryArithmeticNode](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode)

#### Initializers

- [init(leftSource: MPSNNImageNode, rightSource: MPSNNImageNode)](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2890825-init)
- [init(sources: [MPSNNImageNode])](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2890820-init)

#### Instance Properties

- [var bias: Float](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2952964-bias)
- [var maximumValue: Float](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2952979-maximumvalue)
- [var minimumValue: Float](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2952970-minimumvalue)
- [var primaryScale: Float](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2952966-primaryscale)
- [var primaryStrideInFeatureChannels: Int](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2952983-primarystrideinfeaturechannels)
- [var primaryStrideInPixelsX: Int](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2952973-primarystrideinpixelsx)
- [var primaryStrideInPixelsY: Int](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2952996-primarystrideinpixelsy)
- [var secondaryScale: Float](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2952976-secondaryscale)
- [var secondaryStrideInFeatureChannels: Int](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2952974-secondarystrideinfeaturechannels)
- [var secondaryStrideInPixelsX: Int](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2952972-secondarystrideinpixelsx)
- [var secondaryStrideInPixelsY: Int](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2952985-secondarystrideinpixelsy)

#### Instance Methods

- [func gradientClass() -> AnyClass](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2952978-gradientclass)
- [func gradientFilters(withSources: [MPSNNImageNode]) -> [MPSNNGradientFilterNode]](/documentation/metalperformanceshaders/mpsnnbinaryarithmeticnode/2952967-gradientfilters)
- [MPSNNArithmeticGradientNode](/documentation/metalperformanceshaders/mpsnnarithmeticgradientnode)

#### Initializers

- [init(gradientImages: [MPSNNImageNode], forwardFilter: MPSNNFilterNode, isSecondarySourceFilter: Bool)](/documentation/metalperformanceshaders/mpsnnarithmeticgradientnode/2952980-init)
- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNBinaryGradientStateNode, isSecondarySourceFilter: Bool)](/documentation/metalperformanceshaders/mpsnnarithmeticgradientnode/2956166-init)

#### Instance Properties

- [var bias: Float](/documentation/metalperformanceshaders/mpsnnarithmeticgradientnode/2952988-bias)
- [var isSecondarySourceFilter: Bool](/documentation/metalperformanceshaders/mpsnnarithmeticgradientnode/2952987-issecondarysourcefilter)
- [var maximumValue: Float](/documentation/metalperformanceshaders/mpsnnarithmeticgradientnode/2952986-maximumvalue)
- [var minimumValue: Float](/documentation/metalperformanceshaders/mpsnnarithmeticgradientnode/2952989-minimumvalue)
- [var primaryScale: Float](/documentation/metalperformanceshaders/mpsnnarithmeticgradientnode/2952993-primaryscale)
- [var secondaryScale: Float](/documentation/metalperformanceshaders/mpsnnarithmeticgradientnode/2952981-secondaryscale)
- [var secondaryStrideInFeatureChannels: Int](/documentation/metalperformanceshaders/mpsnnarithmeticgradientnode/2952984-secondarystrideinfeaturechannels)
- [var secondaryStrideInPixelsX: Int](/documentation/metalperformanceshaders/mpsnnarithmeticgradientnode/2952968-secondarystrideinpixelsx)
- [var secondaryStrideInPixelsY: Int](/documentation/metalperformanceshaders/mpsnnarithmeticgradientnode/2952994-secondarystrideinpixelsy)
- [MPSNNArithmeticGradientStateNode](/documentation/metalperformanceshaders/mpsnnarithmeticgradientstatenode)

### Convolution Layer Nodes

- [MPSCNNBinaryConvolutionNode](/documentation/metalperformanceshaders/mpscnnbinaryconvolutionnode)

#### Initializers

- [init(source: MPSNNImageNode, weights: any MPSCNNConvolutionDataSource, scaleValue: Float, type: MPSCNNBinaryConvolutionType, flags: MPSCNNBinaryConvolutionFlags)](/documentation/metalperformanceshaders/mpscnnbinaryconvolutionnode/2866509-init)
- [MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource)

##### Instance Methods

- [func biasTerms() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867023-biasterms)
- [func dataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867139-datatype)
- [func descriptor() -> MPSCNNConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867050-descriptor)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2881197-label)
- [func load() -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867049-load)
- [func lookupTableForUInt8Kernel() -> UnsafeMutablePointer<Float>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867186-lookuptableforuint8kernel)
- [func purge()](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867134-purge)
- [func rangesForUInt8Kernel() -> UnsafeMutablePointer<vector_float2>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867145-rangesforuint8kernel)
- [func weights() -> UnsafeMutableRawPointer](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867187-weights)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3013778-copy)
- [func kernelWeightsDataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3564466-kernelweightsdatatype)
- [func update(with: any MTLCommandBuffer, gradientState: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> MPSCNNConvolutionWeightsAndBiasesState?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953007-update)
- [func update(with: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953009-update)
- [func weightsLayout() -> MPSCNNConvolutionWeightsLayout](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3325840-weightslayout)
- [func weightsQuantizationType() -> MPSCNNWeightsQuantizationType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2976466-weightsquantizationtype)
- [MPSCNNBinaryConvolutionType](/documentation/metalperformanceshaders/mpscnnbinaryconvolutiontype)

##### Enumeration Cases

- [case AND](/documentation/metalperformanceshaders/mpscnnbinaryconvolutiontype/and)
- [case XNOR](/documentation/metalperformanceshaders/mpscnnbinaryconvolutiontype/xnor)
- [case binaryWeights](/documentation/metalperformanceshaders/mpscnnbinaryconvolutiontype/binaryweights)
- [MPSCNNBinaryConvolutionFlags](/documentation/metalperformanceshaders/mpscnnbinaryconvolutionflags)

##### Enumeration Cases

- [case none](/documentation/metalperformanceshaders/mpscnnbinaryconvolutionflags/none)
- [case useBetaScaling](/documentation/metalperformanceshaders/mpscnnbinaryconvolutionflags/usebetascaling)
- [init(source: MPSNNImageNode, weights: any MPSCNNConvolutionDataSource, outputBiasTerms: UnsafePointer<Float>?, outputScaleTerms: UnsafePointer<Float>?, inputBiasTerms: UnsafePointer<Float>?, inputScaleTerms: UnsafePointer<Float>?, type: MPSCNNBinaryConvolutionType, flags: MPSCNNBinaryConvolutionFlags)](/documentation/metalperformanceshaders/mpscnnbinaryconvolutionnode/2942631-init)
- [MPSCNNConvolutionNode](/documentation/metalperformanceshaders/mpscnnconvolutionnode)

#### Initializers

- [init(source: MPSNNImageNode, weights: any MPSCNNConvolutionDataSource)](/documentation/metalperformanceshaders/mpscnnconvolutionnode/2866470-init)
- [MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource)

##### Instance Methods

- [func biasTerms() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867023-biasterms)
- [func dataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867139-datatype)
- [func descriptor() -> MPSCNNConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867050-descriptor)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2881197-label)
- [func load() -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867049-load)
- [func lookupTableForUInt8Kernel() -> UnsafeMutablePointer<Float>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867186-lookuptableforuint8kernel)
- [func purge()](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867134-purge)
- [func rangesForUInt8Kernel() -> UnsafeMutablePointer<vector_float2>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867145-rangesforuint8kernel)
- [func weights() -> UnsafeMutableRawPointer](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867187-weights)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3013778-copy)
- [func kernelWeightsDataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3564466-kernelweightsdatatype)
- [func update(with: any MTLCommandBuffer, gradientState: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> MPSCNNConvolutionWeightsAndBiasesState?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953007-update)
- [func update(with: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953009-update)
- [func weightsLayout() -> MPSCNNConvolutionWeightsLayout](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3325840-weightslayout)
- [func weightsQuantizationType() -> MPSCNNWeightsQuantizationType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2976466-weightsquantizationtype)

#### Instance Properties

- [var accumulatorPrecision: MPSNNConvolutionAccumulatorPrecisionOption](/documentation/metalperformanceshaders/mpscnnconvolutionnode/2980757-accumulatorprecision)
- [var convolutionGradientState: MPSCNNConvolutionGradientStateNode?](/documentation/metalperformanceshaders/mpscnnconvolutionnode/2942634-convolutiongradientstate)
- [var trainingStyle: MPSNNTrainingStyle](/documentation/metalperformanceshaders/mpscnnconvolutionnode/3197822-trainingstyle)
- [MPSCNNConvolutionTransposeNode](/documentation/metalperformanceshaders/mpscnnconvolutiontransposenode)

#### Initializers

- [MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource)

##### Instance Methods

- [func biasTerms() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867023-biasterms)
- [func dataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867139-datatype)
- [func descriptor() -> MPSCNNConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867050-descriptor)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2881197-label)
- [func load() -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867049-load)
- [func lookupTableForUInt8Kernel() -> UnsafeMutablePointer<Float>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867186-lookuptableforuint8kernel)
- [func purge()](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867134-purge)
- [func rangesForUInt8Kernel() -> UnsafeMutablePointer<vector_float2>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867145-rangesforuint8kernel)
- [func weights() -> UnsafeMutableRawPointer](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867187-weights)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3013778-copy)
- [func kernelWeightsDataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3564466-kernelweightsdatatype)
- [func update(with: any MTLCommandBuffer, gradientState: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> MPSCNNConvolutionWeightsAndBiasesState?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953007-update)
- [func update(with: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953009-update)
- [func weightsLayout() -> MPSCNNConvolutionWeightsLayout](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3325840-weightslayout)
- [func weightsQuantizationType() -> MPSCNNWeightsQuantizationType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2976466-weightsquantizationtype)
- [init(source: MPSNNImageNode, convolutionGradientState: MPSCNNConvolutionGradientStateNode?, weights: any MPSCNNConvolutionDataSource)](/documentation/metalperformanceshaders/mpscnnconvolutiontransposenode/2942641-init)
- [MPSCNNConvolutionGradientNode](/documentation/metalperformanceshaders/mpscnnconvolutiongradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, convolutionGradientState: MPSCNNConvolutionGradientStateNode, weights: (any MPSCNNConvolutionDataSource)?)](/documentation/metalperformanceshaders/mpscnnconvolutiongradientnode/2947999-init)
- [MPSCNNConvolutionGradientStateNode](/documentation/metalperformanceshaders/mpscnnconvolutiongradientstatenode)
- [MPSCNNCrossChannelNormalizationGradientNode](/documentation/metalperformanceshaders/mpscnncrosschannelnormalizationgradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode, kernelSize: Int)](/documentation/metalperformanceshaders/mpscnncrosschannelnormalizationgradientnode/2948043-init)

#### Instance Properties

- [var kernelSize: Int](/documentation/metalperformanceshaders/mpscnncrosschannelnormalizationgradientnode/2948049-kernelsize)

### Pooling Layer Nodes

- [MPSCNNPoolingAverageNode](/documentation/metalperformanceshaders/mpscnnpoolingaveragenode)
- [MPSCNNDilatedPoolingMaxNode](/documentation/metalperformanceshaders/mpscnndilatedpoolingmaxnode)

#### Initializers

- [init(source: MPSNNImageNode, filterSize: Int)](/documentation/metalperformanceshaders/mpscnndilatedpoolingmaxnode/2873240-init)
- [init(source: MPSNNImageNode, filterSize: Int, stride: Int, dilationRate: Int)](/documentation/metalperformanceshaders/mpscnndilatedpoolingmaxnode/2887340-init)
- [init(source: MPSNNImageNode, kernelWidth: Int, kernelHeight: Int, strideInPixelsX: Int, strideInPixelsY: Int, dilationRateX: Int, dilationRateY: Int)](/documentation/metalperformanceshaders/mpscnndilatedpoolingmaxnode/2887339-init)

#### Instance Properties

- [var dilationRateX: Int](/documentation/metalperformanceshaders/mpscnndilatedpoolingmaxnode/2887341-dilationratex)
- [var dilationRateY: Int](/documentation/metalperformanceshaders/mpscnndilatedpoolingmaxnode/2887342-dilationratey)
- [MPSCNNPoolingL2NormNode](/documentation/metalperformanceshaders/mpscnnpoolingl2normnode)
- [MPSCNNPoolingMaxNode](/documentation/metalperformanceshaders/mpscnnpoolingmaxnode)
- [MPSCNNPoolingNode](/documentation/metalperformanceshaders/mpscnnpoolingnode)

#### Initializers

- [init(source: MPSNNImageNode, filterSize: Int)](/documentation/metalperformanceshaders/mpscnnpoolingnode/2866488-init)
- [init(source: MPSNNImageNode, filterSize: Int, stride: Int)](/documentation/metalperformanceshaders/mpscnnpoolingnode/2866444-init)
- [init(source: MPSNNImageNode, kernelWidth: Int, kernelHeight: Int, strideInPixelsX: Int, strideInPixelsY: Int)](/documentation/metalperformanceshaders/mpscnnpoolingnode/2866471-init)

#### Instance Properties

- [var kernelHeight: Int](/documentation/metalperformanceshaders/mpscnnpoolingnode/2993001-kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshaders/mpscnnpoolingnode/2993002-kernelwidth)
- [var strideInPixelsX: Int](/documentation/metalperformanceshaders/mpscnnpoolingnode/2993003-strideinpixelsx)
- [var strideInPixelsY: Int](/documentation/metalperformanceshaders/mpscnnpoolingnode/2993004-strideinpixelsy)
- [MPSCNNDilatedPoolingMaxGradientNode](/documentation/metalperformanceshaders/mpscnndilatedpoolingmaxgradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode, kernelWidth: Int, kernelHeight: Int, strideInPixelsX: Int, strideInPixelsY: Int, dilationRateX: Int, dilationRateY: Int)](/documentation/metalperformanceshaders/mpscnndilatedpoolingmaxgradientnode/2948026-init)

#### Instance Properties

- [var dilationRateX: Int](/documentation/metalperformanceshaders/mpscnndilatedpoolingmaxgradientnode/2947996-dilationratex)
- [var dilationRateY: Int](/documentation/metalperformanceshaders/mpscnndilatedpoolingmaxgradientnode/2948037-dilationratey)
- [MPSCNNPoolingAverageGradientNode](/documentation/metalperformanceshaders/mpscnnpoolingaveragegradientnode)
- [MPSCNNPoolingGradientNode](/documentation/metalperformanceshaders/mpscnnpoolinggradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode, kernelWidth: Int, kernelHeight: Int, strideInPixelsX: Int, strideInPixelsY: Int, paddingPolicy: (any MPSNNPadding)?)](/documentation/metalperformanceshaders/mpscnnpoolinggradientnode/2948011-init)

#### Instance Properties

- [var kernelHeight: Int](/documentation/metalperformanceshaders/mpscnnpoolinggradientnode/2947992-kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshaders/mpscnnpoolinggradientnode/2948034-kernelwidth)
- [var strideInPixelsX: Int](/documentation/metalperformanceshaders/mpscnnpoolinggradientnode/2948018-strideinpixelsx)
- [var strideInPixelsY: Int](/documentation/metalperformanceshaders/mpscnnpoolinggradientnode/2948048-strideinpixelsy)
- [MPSCNNPoolingL2NormGradientNode](/documentation/metalperformanceshaders/mpscnnpoolingl2normgradientnode)
- [MPSCNNPoolingMaxGradientNode](/documentation/metalperformanceshaders/mpscnnpoolingmaxgradientnode)

### Fully Connected Layer Nodes

- [MPSCNNBinaryFullyConnectedNode](/documentation/metalperformanceshaders/mpscnnbinaryfullyconnectednode)

#### Initializers

- [init(source: MPSNNImageNode, weights: any MPSCNNConvolutionDataSource, scaleValue: Float, type: MPSCNNBinaryConvolutionType, flags: MPSCNNBinaryConvolutionFlags)](/documentation/metalperformanceshaders/mpscnnbinaryfullyconnectednode/2866443-init)
- [MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource)

##### Instance Methods

- [func biasTerms() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867023-biasterms)
- [func dataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867139-datatype)
- [func descriptor() -> MPSCNNConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867050-descriptor)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2881197-label)
- [func load() -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867049-load)
- [func lookupTableForUInt8Kernel() -> UnsafeMutablePointer<Float>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867186-lookuptableforuint8kernel)
- [func purge()](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867134-purge)
- [func rangesForUInt8Kernel() -> UnsafeMutablePointer<vector_float2>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867145-rangesforuint8kernel)
- [func weights() -> UnsafeMutableRawPointer](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867187-weights)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3013778-copy)
- [func kernelWeightsDataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3564466-kernelweightsdatatype)
- [func update(with: any MTLCommandBuffer, gradientState: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> MPSCNNConvolutionWeightsAndBiasesState?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953007-update)
- [func update(with: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953009-update)
- [func weightsLayout() -> MPSCNNConvolutionWeightsLayout](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3325840-weightslayout)
- [func weightsQuantizationType() -> MPSCNNWeightsQuantizationType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2976466-weightsquantizationtype)
- [init(source: MPSNNImageNode, weights: any MPSCNNConvolutionDataSource, outputBiasTerms: UnsafePointer<Float>?, outputScaleTerms: UnsafePointer<Float>?, inputBiasTerms: UnsafePointer<Float>?, inputScaleTerms: UnsafePointer<Float>?, type: MPSCNNBinaryConvolutionType, flags: MPSCNNBinaryConvolutionFlags)](/documentation/metalperformanceshaders/mpscnnbinaryfullyconnectednode/2942637-init)
- [MPSCNNFullyConnectedNode](/documentation/metalperformanceshaders/mpscnnfullyconnectednode)

#### Initializers

- [init(source: MPSNNImageNode, weights: any MPSCNNConvolutionDataSource)](/documentation/metalperformanceshaders/mpscnnfullyconnectednode/2866412-init)

### Neuron Layer Nodes

- [MPSCNNNeuronAbsoluteNode](/documentation/metalperformanceshaders/mpscnnneuronabsolutenode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnneuronabsolutenode/2921448-init)
- [MPSCNNNeuronELUNode](/documentation/metalperformanceshaders/mpscnnneuronelunode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnneuronelunode/2921447-init)
- [init(source: MPSNNImageNode, a: Float)](/documentation/metalperformanceshaders/mpscnnneuronelunode/2921454-init)
- [MPSCNNNeuronHardSigmoidNode](/documentation/metalperformanceshaders/mpscnnneuronhardsigmoidnode)

#### Initializers

- [init(source: MPSNNImageNode, a: Float, b: Float)](/documentation/metalperformanceshaders/mpscnnneuronhardsigmoidnode/2875181-init)
- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnneuronhardsigmoidnode/2921455-init)
- [MPSCNNNeuronLinearNode](/documentation/metalperformanceshaders/mpscnnneuronlinearnode)

#### Initializers

- [init(source: MPSNNImageNode, a: Float, b: Float)](/documentation/metalperformanceshaders/mpscnnneuronlinearnode/2866495-init)
- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnneuronlinearnode/2921456-init)
- [MPSCNNNeuronPReLUNode](/documentation/metalperformanceshaders/mpscnnneuronprelunode)

#### Initializers

- [init(source: MPSNNImageNode, aData: Data)](/documentation/metalperformanceshaders/mpscnnneuronprelunode/2921595-init)
- [MPSCNNNeuronReLUNNode](/documentation/metalperformanceshaders/mpscnnneuronrelunnode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnneuronrelunnode/2921593-init)
- [init(source: MPSNNImageNode, a: Float, b: Float)](/documentation/metalperformanceshaders/mpscnnneuronrelunnode/2921596-init)
- [MPSCNNNeuronReLUNode](/documentation/metalperformanceshaders/mpscnnneuronrelunode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnneuronrelunode/2921464-init)
- [init(source: MPSNNImageNode, a: Float)](/documentation/metalperformanceshaders/mpscnnneuronrelunode/2921462-init)
- [MPSCNNNeuronSigmoidNode](/documentation/metalperformanceshaders/mpscnnneuronsigmoidnode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnneuronsigmoidnode/2921458-init)
- [MPSCNNNeuronSoftPlusNode](/documentation/metalperformanceshaders/mpscnnneuronsoftplusnode)

#### Initializers

- [init(source: MPSNNImageNode, a: Float, b: Float)](/documentation/metalperformanceshaders/mpscnnneuronsoftplusnode/2866413-init)
- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnneuronsoftplusnode/2921457-init)
- [MPSCNNNeuronSoftSignNode](/documentation/metalperformanceshaders/mpscnnneuronsoftsignnode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnneuronsoftsignnode/2921463-init)
- [MPSCNNNeuronTanHNode](/documentation/metalperformanceshaders/mpscnnneurontanhnode)

#### Initializers

- [init(source: MPSNNImageNode, a: Float, b: Float)](/documentation/metalperformanceshaders/mpscnnneurontanhnode/2866481-init)
- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnneurontanhnode/2921465-init)
- [MPSCNNNeuronExponentialNode](/documentation/metalperformanceshaders/mpscnnneuronexponentialnode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnneuronexponentialnode/2951936-init)
- [init(source: MPSNNImageNode, a: Float, b: Float, c: Float)](/documentation/metalperformanceshaders/mpscnnneuronexponentialnode/2951933-init)
- [MPSCNNNeuronGradientNode](/documentation/metalperformanceshaders/mpscnnneurongradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode, descriptor: MPSNNNeuronDescriptor)](/documentation/metalperformanceshaders/mpscnnneurongradientnode/2948031-init)

#### Instance Properties

- [var descriptor: MPSNNNeuronDescriptor](/documentation/metalperformanceshaders/mpscnnneurongradientnode/2948040-descriptor)
- [MPSCNNNeuronLogarithmNode](/documentation/metalperformanceshaders/mpscnnneuronlogarithmnode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnneuronlogarithmnode/2951949-init)
- [init(source: MPSNNImageNode, a: Float, b: Float, c: Float)](/documentation/metalperformanceshaders/mpscnnneuronlogarithmnode/2951939-init)
- [MPSCNNNeuronPowerNode](/documentation/metalperformanceshaders/mpscnnneuronpowernode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnneuronpowernode/2951937-init)
- [init(source: MPSNNImageNode, a: Float, b: Float, c: Float)](/documentation/metalperformanceshaders/mpscnnneuronpowernode/2951946-init)
- [MPSCNNNeuronNode](/documentation/metalperformanceshaders/mpscnnneuronnode)

#### Supporting Types

- [MPSCNNNeuronType](/documentation/metalperformanceshaders/mpscnnneurontype)

##### Enumeration Cases

- [case none](/documentation/metalperformanceshaders/mpscnnneurontype/none)
- [case reLU](/documentation/metalperformanceshaders/mpscnnneurontype/relu)
- [case linear](/documentation/metalperformanceshaders/mpscnnneurontype/linear)
- [case sigmoid](/documentation/metalperformanceshaders/mpscnnneurontype/sigmoid)
- [case hardSigmoid](/documentation/metalperformanceshaders/mpscnnneurontype/hardsigmoid)
- [case tanH](/documentation/metalperformanceshaders/mpscnnneurontype/tanh)
- [case absolute](/documentation/metalperformanceshaders/mpscnnneurontype/absolute)
- [case softPlus](/documentation/metalperformanceshaders/mpscnnneurontype/softplus)
- [case softSign](/documentation/metalperformanceshaders/mpscnnneurontype/softsign)
- [case ELU](/documentation/metalperformanceshaders/mpscnnneurontype/elu)
- [case count](/documentation/metalperformanceshaders/mpscnnneurontype/count)
- [case exponential](/documentation/metalperformanceshaders/mpscnnneurontype/exponential)
- [case geLU](/documentation/metalperformanceshaders/mpscnnneurontype/gelu)
- [case logarithm](/documentation/metalperformanceshaders/mpscnnneurontype/logarithm)
- [case pReLU](/documentation/metalperformanceshaders/mpscnnneurontype/prelu)
- [case power](/documentation/metalperformanceshaders/mpscnnneurontype/power)
- [case reLUN](/documentation/metalperformanceshaders/mpscnnneurontype/relun)

#### Initializers

- [init(source: MPSNNImageNode, descriptor: MPSNNNeuronDescriptor)](/documentation/metalperformanceshaders/mpscnnneuronnode/3019333-init)

#### Instance Properties

- [var a: Float](/documentation/metalperformanceshaders/mpscnnneuronnode/2921459-a)
- [var b: Float](/documentation/metalperformanceshaders/mpscnnneuronnode/2921461-b)
- [var c: Float](/documentation/metalperformanceshaders/mpscnnneuronnode/2935553-c)

### Softmax Layer Nodes

- [MPSCNNSoftMaxNode](/documentation/metalperformanceshaders/mpscnnsoftmaxnode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnsoftmaxnode/2866408-init)
- [MPSCNNLogSoftMaxNode](/documentation/metalperformanceshaders/mpscnnlogsoftmaxnode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnlogsoftmaxnode/2866457-init)
- [MPSCNNLogSoftMaxGradientNode](/documentation/metalperformanceshaders/mpscnnlogsoftmaxgradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode)](/documentation/metalperformanceshaders/mpscnnlogsoftmaxgradientnode/2947971-init)
- [MPSCNNSoftMaxGradientNode](/documentation/metalperformanceshaders/mpscnnsoftmaxgradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode)](/documentation/metalperformanceshaders/mpscnnsoftmaxgradientnode/2948039-init)

### Normalization Layer Nodes

- [MPSCNNCrossChannelNormalizationNode](/documentation/metalperformanceshaders/mpscnncrosschannelnormalizationnode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnncrosschannelnormalizationnode/2866459-init)
- [init(source: MPSNNImageNode, kernelSize: Int)](/documentation/metalperformanceshaders/mpscnncrosschannelnormalizationnode/2866456-init)

#### Instance Properties

- [var kernelSizeInFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnncrosschannelnormalizationnode/2866419-kernelsizeinfeaturechannels)
- [MPSCNNLocalContrastNormalizationNode](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationnode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationnode/2866454-init)
- [init(source: MPSNNImageNode, kernelSize: Int)](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationnode/2866473-init)

#### Instance Properties

- [var kernelHeight: Int](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationnode/2866485-kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationnode/2866441-kernelwidth)
- [var p0: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationnode/2866510-p0)
- [var pm: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationnode/2866404-pm)
- [var ps: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationnode/2866500-ps)
- [MPSCNNSpatialNormalizationNode](/documentation/metalperformanceshaders/mpscnnspatialnormalizationnode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnspatialnormalizationnode/2866502-init)
- [init(source: MPSNNImageNode, kernelSize: Int)](/documentation/metalperformanceshaders/mpscnnspatialnormalizationnode/2866438-init)

#### Instance Properties

- [var kernelHeight: Int](/documentation/metalperformanceshaders/mpscnnspatialnormalizationnode/2866424-kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshaders/mpscnnspatialnormalizationnode/2866402-kernelwidth)
- [MPSCNNBatchNormalizationGradientNode](/documentation/metalperformanceshaders/mpscnnbatchnormalizationgradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode)](/documentation/metalperformanceshaders/mpscnnbatchnormalizationgradientnode/2953939-init)
- [MPSCNNBatchNormalizationNode](/documentation/metalperformanceshaders/mpscnnbatchnormalizationnode)

#### Initializers

- [init(source: MPSNNImageNode, dataSource: any MPSCNNBatchNormalizationDataSource)](/documentation/metalperformanceshaders/mpscnnbatchnormalizationnode/2948004-init)

#### Instance Properties

- [var flags: MPSCNNBatchNormalizationFlags](/documentation/metalperformanceshaders/mpscnnbatchnormalizationnode/2953940-flags)
- [var trainingStyle: MPSNNTrainingStyle](/documentation/metalperformanceshaders/mpscnnbatchnormalizationnode/3197821-trainingstyle)
- [MPSCNNBatchNormalizationDataSource](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource)

#### Initializers

- [init?(coder: NSCoder)](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/2951886-init)

#### Type Properties

- [static var supportsSecureCoding: Bool](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/2951887-supportssecurecoding)

#### Instance Methods

- [func beta() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/2942586-beta)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/3013773-copy)
- [func encode(with: NSCoder)](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/2951882-encode)
- [func epsilon() -> Float](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/2947917-epsilon)
- [func gamma() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/2942605-gamma)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/2953128-label)
- [func load() -> Bool](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/2942579-load)
- [func mean() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/2942589-mean)
- [func numberOfFeatureChannels() -> Int](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/2942596-numberoffeaturechannels)
- [func purge()](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/2942607-purge)
- [func updateGammaAndBeta(with: MPSCNNBatchNormalizationState) -> Bool](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/2953129-updategammaandbeta)
- [func updateGammaAndBeta(with: any MTLCommandBuffer, batchNormalizationState: MPSCNNBatchNormalizationState) -> MPSCNNNormalizationGammaAndBetaState?](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/2951891-updategammaandbeta)
- [func updateMeanAndVariance(with: MPSCNNBatchNormalizationState) -> Bool](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/3002360-updatemeanandvariance)
- [func updateMeanAndVariance(with: any MTLCommandBuffer, batchNormalizationState: MPSCNNBatchNormalizationState) -> MPSCNNNormalizationMeanAndVarianceState?](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/3002361-updatemeanandvariance)
- [func variance() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnbatchnormalizationdatasource/2942592-variance)
- [MPSCNNInstanceNormalizationGradientNode](/documentation/metalperformanceshaders/mpscnninstancenormalizationgradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode)](/documentation/metalperformanceshaders/mpscnninstancenormalizationgradientnode/2951954-init)
- [MPSCNNInstanceNormalizationDataSource](/documentation/metalperformanceshaders/mpscnninstancenormalizationdatasource)

#### Initializers

- [init?(coder: NSCoder)](/documentation/metalperformanceshaders/mpscnninstancenormalizationdatasource/2947957-init)

#### Instance Properties

- [var numberOfFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnninstancenormalizationdatasource/2947961-numberoffeaturechannels)

#### Type Properties

- [static var supportsSecureCoding: Bool](/documentation/metalperformanceshaders/mpscnninstancenormalizationdatasource/2947952-supportssecurecoding)

#### Instance Methods

- [func beta() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnninstancenormalizationdatasource/2953922-beta)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnninstancenormalizationdatasource/3013780-copy)
- [func encode(with: NSCoder)](/documentation/metalperformanceshaders/mpscnninstancenormalizationdatasource/2947953-encode)
- [func epsilon() -> Float](/documentation/metalperformanceshaders/mpscnninstancenormalizationdatasource/2953925-epsilon)
- [func gamma() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnninstancenormalizationdatasource/2953923-gamma)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnninstancenormalizationdatasource/2952998-label)
- [func load() -> Bool](/documentation/metalperformanceshaders/mpscnninstancenormalizationdatasource/3088878-load)
- [func purge()](/documentation/metalperformanceshaders/mpscnninstancenormalizationdatasource/3088879-purge)
- [func updateGammaAndBeta(with: any MTLCommandBuffer, instanceNormalizationStateBatch: [MPSCNNInstanceNormalizationGradientState]) -> MPSCNNNormalizationGammaAndBetaState?](/documentation/metalperformanceshaders/mpscnninstancenormalizationdatasource/2953926-updategammaandbeta)
- [func updateGammaAndBeta(withInstanceNormalizationStateBatch: [MPSCNNInstanceNormalizationGradientState]) -> Bool](/documentation/metalperformanceshaders/mpscnninstancenormalizationdatasource/2953931-updategammaandbeta)
- [MPSCNNInstanceNormalizationNode](/documentation/metalperformanceshaders/mpscnninstancenormalizationnode)

#### Initializers

- [init(source: MPSNNImageNode, dataSource: any MPSCNNInstanceNormalizationDataSource)](/documentation/metalperformanceshaders/mpscnninstancenormalizationnode/2951940-init)

#### Instance Properties

- [var trainingStyle: MPSNNTrainingStyle](/documentation/metalperformanceshaders/mpscnninstancenormalizationnode/3197824-trainingstyle)
- [MPSCNNLocalContrastNormalizationGradientNode](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode, kernelWidth: Int, kernelHeight: Int)](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradientnode/2948016-init)

#### Instance Properties

- [var alpha: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradientnode/2947973-alpha)
- [var beta: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradientnode/2947977-beta)
- [var delta: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradientnode/2948014-delta)
- [var kernelHeight: Int](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradientnode/2948019-kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradientnode/2947965-kernelwidth)
- [var p0: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradientnode/2948017-p0)
- [var pm: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradientnode/2948053-pm)
- [var ps: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradientnode/2948008-ps)
- [MPSCNNSpatialNormalizationGradientNode](/documentation/metalperformanceshaders/mpscnnspatialnormalizationgradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode, kernelSize: Int)](/documentation/metalperformanceshaders/mpscnnspatialnormalizationgradientnode/2948009-init)

#### Instance Properties

- [var alpha: Float](/documentation/metalperformanceshaders/mpscnnspatialnormalizationgradientnode/2948027-alpha)
- [var beta: Float](/documentation/metalperformanceshaders/mpscnnspatialnormalizationgradientnode/2948006-beta)
- [var delta: Float](/documentation/metalperformanceshaders/mpscnnspatialnormalizationgradientnode/2947968-delta)
- [var kernelHeight: Int](/documentation/metalperformanceshaders/mpscnnspatialnormalizationgradientnode/2948020-kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshaders/mpscnnspatialnormalizationgradientnode/2948013-kernelwidth)
- [MPSCNNNormalizationNode](/documentation/metalperformanceshaders/mpscnnnormalizationnode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnnormalizationnode/2866425-init)

#### Instance Properties

- [var alpha: Float](/documentation/metalperformanceshaders/mpscnnnormalizationnode/2866474-alpha)
- [var beta: Float](/documentation/metalperformanceshaders/mpscnnnormalizationnode/2866497-beta)
- [var delta: Float](/documentation/metalperformanceshaders/mpscnnnormalizationnode/2866482-delta)

### Upsampling Layer Nodes

- [MPSCNNUpsamplingBilinearNode](/documentation/metalperformanceshaders/mpscnnupsamplingbilinearnode)

#### Initializers

- [init(source: MPSNNImageNode, integerScaleFactorX: Int, integerScaleFactorY: Int)](/documentation/metalperformanceshaders/mpscnnupsamplingbilinearnode/2875152-init)
- [init(source: MPSNNImageNode, integerScaleFactorX: Int, integerScaleFactorY: Int, alignCorners: Bool)](/documentation/metalperformanceshaders/mpscnnupsamplingbilinearnode/2966688-init)

#### Instance Properties

- [var scaleFactorX: Double](/documentation/metalperformanceshaders/mpscnnupsamplingbilinearnode/2875153-scalefactorx)
- [var scaleFactorY: Double](/documentation/metalperformanceshaders/mpscnnupsamplingbilinearnode/2875150-scalefactory)
- [var alignCorners: Bool](/documentation/metalperformanceshaders/mpscnnupsamplingbilinearnode/2966687-aligncorners)
- [MPSCNNUpsamplingNearestNode](/documentation/metalperformanceshaders/mpscnnupsamplingnearestnode)

#### Initializers

- [init(source: MPSNNImageNode, integerScaleFactorX: Int, integerScaleFactorY: Int)](/documentation/metalperformanceshaders/mpscnnupsamplingnearestnode/2875222-init)

#### Instance Properties

- [var scaleFactorX: Double](/documentation/metalperformanceshaders/mpscnnupsamplingnearestnode/2875209-scalefactorx)
- [var scaleFactorY: Double](/documentation/metalperformanceshaders/mpscnnupsamplingnearestnode/2875155-scalefactory)
- [MPSCNNUpsamplingBilinearGradientNode](/documentation/metalperformanceshaders/mpscnnupsamplingbilineargradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode, scaleFactorX: Double, scaleFactorY: Double)](/documentation/metalperformanceshaders/mpscnnupsamplingbilineargradientnode/2947991-init)

#### Instance Properties

- [var scaleFactorX: Double](/documentation/metalperformanceshaders/mpscnnupsamplingbilineargradientnode/2948051-scalefactorx)
- [var scaleFactorY: Double](/documentation/metalperformanceshaders/mpscnnupsamplingbilineargradientnode/2948054-scalefactory)
- [MPSCNNUpsamplingNearestGradientNode](/documentation/metalperformanceshaders/mpscnnupsamplingnearestgradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode, scaleFactorX: Double, scaleFactorY: Double)](/documentation/metalperformanceshaders/mpscnnupsamplingnearestgradientnode/2947983-init)

#### Instance Properties

- [var scaleFactorX: Double](/documentation/metalperformanceshaders/mpscnnupsamplingnearestgradientnode/2948024-scalefactorx)
- [var scaleFactorY: Double](/documentation/metalperformanceshaders/mpscnnupsamplingnearestgradientnode/2948035-scalefactory)

### Resampling Nodes

- [MPSNNBilinearScaleNode](/documentation/metalperformanceshaders/mpsnnbilinearscalenode)
- [MPSNNLanczosScaleNode](/documentation/metalperformanceshaders/mpsnnlanczosscalenode)
- [MPSNNScaleNode](/documentation/metalperformanceshaders/mpsnnscalenode)

#### Initializers

- [init(source: MPSNNImageNode, outputSize: MTLSize)](/documentation/metalperformanceshaders/mpsnnscalenode/2915285-init)
- [init(source: MPSNNImageNode, transformProvider: (any MPSImageTransformProvider)?, outputSize: MTLSize)](/documentation/metalperformanceshaders/mpsnnscalenode/2915278-init)
- [MPSImageTransformProvider](/documentation/metalperformanceshaders/mpsimagetransformprovider)

#### Instance Methods

- [func transform(forSourceImage: MPSImage, handle: (any MPSHandle)?) -> MPSScaleTransform](/documentation/metalperformanceshaders/mpsimagetransformprovider/2915282-transform)

### Dropout Layer Nodes

- [MPSCNNDropoutNode](/documentation/metalperformanceshaders/mpscnndropoutnode)

#### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnndropoutnode/2947969-init)
- [init(source: MPSNNImageNode, keepProbability: Float)](/documentation/metalperformanceshaders/mpscnndropoutnode/2948000-init)
- [init(source: MPSNNImageNode, keepProbability: Float, seed: Int, maskStrideInPixels: MTLSize)](/documentation/metalperformanceshaders/mpscnndropoutnode/2947990-init)

#### Instance Properties

- [var keepProbability: Float](/documentation/metalperformanceshaders/mpscnndropoutnode/2947982-keepprobability)
- [var maskStrideInPixels: MTLSize](/documentation/metalperformanceshaders/mpscnndropoutnode/2947998-maskstrideinpixels)
- [var seed: Int](/documentation/metalperformanceshaders/mpscnndropoutnode/2948030-seed)
- [MPSCNNDropoutGradientNode](/documentation/metalperformanceshaders/mpscnndropoutgradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode, keepProbability: Float, seed: Int, maskStrideInPixels: MTLSize)](/documentation/metalperformanceshaders/mpscnndropoutgradientnode/2948001-init)

#### Instance Properties

- [var keepProbability: Float](/documentation/metalperformanceshaders/mpscnndropoutgradientnode/2947988-keepprobability)
- [var maskStrideInPixels: MTLSize](/documentation/metalperformanceshaders/mpscnndropoutgradientnode/2947972-maskstrideinpixels)
- [var seed: Int](/documentation/metalperformanceshaders/mpscnndropoutgradientnode/2948003-seed)

### Kernel Concatenation Nodes

- [MPSNNConcatenationNode](/documentation/metalperformanceshaders/mpsnnconcatenationnode)

#### Initializers

- [init(sources: [MPSNNImageNode])](/documentation/metalperformanceshaders/mpsnnconcatenationnode/2866423-init)
- [MPSNNConcatenationGradientNode](/documentation/metalperformanceshaders/mpsnnconcatenationgradientnode)

#### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode)](/documentation/metalperformanceshaders/mpsnnconcatenationgradientnode/2951934-init)

### Loss Layer Nodes

- [MPSCNNLossNode](/documentation/metalperformanceshaders/mpscnnlossnode)

#### Initializers

- [init(source: MPSNNImageNode, lossDescriptor: MPSCNNLossDescriptor)](/documentation/metalperformanceshaders/mpscnnlossnode/2951947-init)

#### Instance Properties

- [var inputLabels: MPSNNLabelsNode](/documentation/metalperformanceshaders/mpscnnlossnode/2951942-inputlabels)
- [MPSCNNYOLOLossNode](/documentation/metalperformanceshaders/mpscnnyololossnode)

#### Initializers

- [init(source: MPSNNImageNode, lossDescriptor: MPSCNNYOLOLossDescriptor)](/documentation/metalperformanceshaders/mpscnnyololossnode/2976514-init)

#### Instance Properties

- [var inputLabels: MPSNNLabelsNode](/documentation/metalperformanceshaders/mpscnnyololossnode/2976515-inputlabels)
- [MPSNNLabelsNode](/documentation/metalperformanceshaders/mpsnnlabelsnode)

### Filter Node Base Classes

- [MPSNNFilterNode](/documentation/metalperformanceshaders/mpsnnfilternode)

#### Instance Properties

- [var label: String?](/documentation/metalperformanceshaders/mpsnnfilternode/2866465-label)
- [var paddingPolicy: any MPSNNPadding](/documentation/metalperformanceshaders/mpsnnfilternode/2866496-paddingpolicy)
- [MPSNNPadding](/documentation/metalperformanceshaders/mpsnnpadding)

##### Instance Methods

- [func destinationImageDescriptor(forSourceImages: [MPSImage], sourceStates: [MPSState]?, for: MPSKernel, suggestedDescriptor: MPSImageDescriptor) -> MPSImageDescriptor](/documentation/metalperformanceshaders/mpsnnpadding/2867167-destinationimagedescriptor)
- [MPSImage](/documentation/metalperformanceshaders/mpsimage)

###### Initializers

- [init(device: any MTLDevice, imageDescriptor: MPSImageDescriptor)](/documentation/metalperformanceshaders/mpsimage/1648920-init)
- [MPSImageDescriptor](/documentation/metalperformanceshaders/mpsimagedescriptor)

###### Methods

- [init(channelFormat: MPSImageFeatureChannelFormat, width: Int, height: Int, featureChannels: Int)](/documentation/metalperformanceshaders/mpsimagedescriptor/1648819-init)
- [init(channelFormat: MPSImageFeatureChannelFormat, width: Int, height: Int, featureChannels: Int, numberOfImages: Int, usage: MTLTextureUsage)](/documentation/metalperformanceshaders/mpsimagedescriptor/1648893-init)

###### Properties

- [var width: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648830-width)
- [var height: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648947-height)
- [var featureChannels: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648918-featurechannels)
- [var numberOfImages: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648846-numberofimages)
- [var pixelFormat: MTLPixelFormat](/documentation/metalperformanceshaders/mpsimagedescriptor/1648913-pixelformat)
- [var channelFormat: MPSImageFeatureChannelFormat](/documentation/metalperformanceshaders/mpsimagedescriptor/1648818-channelformat)
- [var cpuCacheMode: MTLCPUCacheMode](/documentation/metalperformanceshaders/mpsimagedescriptor/1648930-cpucachemode)
- [var storageMode: MTLStorageMode](/documentation/metalperformanceshaders/mpsimagedescriptor/1648955-storagemode)
- [var usage: MTLTextureUsage](/documentation/metalperformanceshaders/mpsimagedescriptor/1648937-usage)

###### Instance Methods

- [func copy(with: NSZone?) -> Self](/documentation/metalperformanceshaders/mpsimagedescriptor/3020686-copy)
- [init(texture: any MTLTexture, featureChannels: Int)](/documentation/metalperformanceshaders/mpsimage/2097547-init)
- [init(parentImage: MPSImage, sliceRange: NSRange, featureChannels: Int)](/documentation/metalperformanceshaders/mpsimage/2942493-init)

###### Methods

- [func setPurgeableState(MPSPurgeableState) -> MPSPurgeableState](/documentation/metalperformanceshaders/mpsimage/1648820-setpurgeablestate)
- [MPSPurgeableState](/documentation/metalperformanceshaders/mpspurgeablestate)

###### Constants

- [case allocationDeferred](/documentation/metalperformanceshaders/mpspurgeablestate/allocationdeferred)
- [case keepCurrent](/documentation/metalperformanceshaders/mpspurgeablestate/keepcurrent)
- [case nonVolatile](/documentation/metalperformanceshaders/mpspurgeablestate/nonvolatile)
- [case volatile](/documentation/metalperformanceshaders/mpspurgeablestate/volatile)
- [case empty](/documentation/metalperformanceshaders/mpspurgeablestate/empty)

###### Methods to Read and Write Raw Data

- [func readBytes(UnsafeMutableRawPointer, dataLayout: MPSDataLayout, bytesPerRow: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2867105-readbytes)
- [func readBytes(UnsafeMutableRawPointer, dataLayout: MPSDataLayout, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2867188-readbytes)
- [func writeBytes(UnsafeRawPointer, dataLayout: MPSDataLayout, bytesPerRow: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2867055-writebytes)
- [func writeBytes(UnsafeRawPointer, dataLayout: MPSDataLayout, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2867189-writebytes)
- [MPSImageReadWriteParams](/documentation/metalperformanceshaders/mpsimagereadwriteparams)

###### Initializers

- [init()](/documentation/metalperformanceshaders/mpsimagereadwriteparams/2867022-init)
- [init(featureChannelOffset: Int, numberOfFeatureChannelsToReadWrite: Int)](/documentation/metalperformanceshaders/mpsimagereadwriteparams/2867128-init)

###### Instance Properties

- [var featureChannelOffset: Int](/documentation/metalperformanceshaders/mpsimagereadwriteparams/2867064-featurechanneloffset)
- [var numberOfFeatureChannelsToReadWrite: Int](/documentation/metalperformanceshaders/mpsimagereadwriteparams/2867173-numberoffeaturechannelstoreadwri)
- [MPSDataLayout](/documentation/metalperformanceshaders/mpsdatalayout)

###### Enumeration Cases

- [case featureChannelsxHeightxWidth](/documentation/metalperformanceshaders/mpsdatalayout/featurechannelsxheightxwidth)
- [case HeightxWidthxFeatureChannels](/documentation/metalperformanceshaders/mpsdatalayout/heightxwidthxfeaturechannels)

###### Methods to Get an Image Allocator

- [class func defaultAllocator() -> any MPSImageAllocator](/documentation/metalperformanceshaders/mpsimage/2867148-defaultallocator)
- [MPSImageAllocator](/documentation/metalperformanceshaders/mpsimageallocator)

###### Instance Methods

- [func image(for: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor, kernel: MPSKernel) -> MPSImage](/documentation/metalperformanceshaders/mpsimageallocator/2866966-image)
- [func imageBatch(for: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor, kernel: MPSKernel, count: Int) -> [MPSImage]](/documentation/metalperformanceshaders/mpsimageallocator/3020685-imagebatch)

###### Properties

- [var device: any MTLDevice](/documentation/metalperformanceshaders/mpsimage/1648857-device)
- [var width: Int](/documentation/metalperformanceshaders/mpsimage/1648884-width)
- [var height: Int](/documentation/metalperformanceshaders/mpsimage/1648952-height)
- [var featureChannels: Int](/documentation/metalperformanceshaders/mpsimage/1648901-featurechannels)
- [var numberOfImages: Int](/documentation/metalperformanceshaders/mpsimage/1648900-numberofimages)
- [var textureType: MTLTextureType](/documentation/metalperformanceshaders/mpsimage/1648948-texturetype)
- [MTLTextureType](/documentation/metal/mtltexturetype)
- [var pixelFormat: MTLPixelFormat](/documentation/metalperformanceshaders/mpsimage/1648844-pixelformat)
- [MTLPixelFormat](/documentation/metal/mtlpixelformat)
- [var precision: Int](/documentation/metalperformanceshaders/mpsimage/1648880-precision)
- [var usage: MTLTextureUsage](/documentation/metalperformanceshaders/mpsimage/1648828-usage)
- [MTLTextureUsage](/documentation/metal/mtltextureusage)
- [var pixelSize: Int](/documentation/metalperformanceshaders/mpsimage/1648854-pixelsize)
- [var texture: any MTLTexture](/documentation/metalperformanceshaders/mpsimage/1648903-texture)
- [MTLTexture](/documentation/metal/mtltexture)
- [var label: String?](/documentation/metalperformanceshaders/mpsimage/1648899-label)

###### Instance Properties

- [var featureChannelFormat: MPSImageFeatureChannelFormat](/documentation/metalperformanceshaders/mpsimage/3131715-featurechannelformat)
- [var parent: MPSImage?](/documentation/metalperformanceshaders/mpsimage/2942490-parent)

###### Instance Methods

- [func batchRepresentation() -> [MPSImage]](/documentation/metalperformanceshaders/mpsimage/2942495-batchrepresentation)
- [func batchRepresentation(withSubRange: NSRange) -> [MPSImage]](/documentation/metalperformanceshaders/mpsimage/2942492-batchrepresentation)
- [func readBytes(UnsafeMutableRawPointer, dataLayout: MPSDataLayout, bytesPerRow: Int, bytesPerImage: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2951914-readbytes)
- [func resourceSize() -> Int](/documentation/metalperformanceshaders/mpsimage/2942494-resourcesize)
- [func subImage(withFeatureChannelRange: NSRange) -> MPSImage](/documentation/metalperformanceshaders/mpsimage/2942488-subimage)
- [func synchronize(on: any MTLCommandBuffer)](/documentation/metalperformanceshaders/mpsimage/2942491-synchronize)
- [func writeBytes(UnsafeRawPointer, dataLayout: MPSDataLayout, bytesPerColumn: Int, bytesPerRow: Int, bytesPerImage: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/3143488-writebytes)
- [func writeBytes(UnsafeRawPointer, dataLayout: MPSDataLayout, bytesPerRow: Int, bytesPerImage: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2951915-writebytes)
- [MPSState](/documentation/metalperformanceshaders/mpsstate)

###### Instance Properties

- [var isTemporary: Bool](/documentation/metalperformanceshaders/mpsstate/2867114-istemporary)
- [var label: String?](/documentation/metalperformanceshaders/mpsstate/2867179-label)
- [var readCount: Int](/documentation/metalperformanceshaders/mpsstate/2867042-readcount)
- [var resource: (any MTLResource)?](/documentation/metalperformanceshaders/mpsstate/2942398-resource)
- [var resourceCount: Int](/documentation/metalperformanceshaders/mpsstate/2947900-resourcecount)

###### Initializers

- [init(device: any MTLDevice, bufferSize: Int)](/documentation/metalperformanceshaders/mpsstate/2942392-init)
- [init(device: any MTLDevice, resourceList: MPSStateResourceList)](/documentation/metalperformanceshaders/mpsstate/2947908-init)
- [init(device: any MTLDevice, textureDescriptor: MTLTextureDescriptor)](/documentation/metalperformanceshaders/mpsstate/2942400-init)
- [init(resource: (any MTLResource)?)](/documentation/metalperformanceshaders/mpsstate/2942390-init)
- [init(resources: [any MTLResource]?)](/documentation/metalperformanceshaders/mpsstate/2947895-init)

###### Instance Methods

- [func bufferSize(at: Int) -> Int](/documentation/metalperformanceshaders/mpsstate/2947913-buffersize)
- [func destinationImageDescriptor(forSourceImages: [MPSImage], sourceStates: [MPSState]?, for: MPSKernel, suggestedDescriptor: MPSImageDescriptor) -> MPSImageDescriptor](/documentation/metalperformanceshaders/mpsstate/2942394-destinationimagedescriptor)
- [func resource(at: Int, allocateMemory: Bool) -> (any MTLResource)?](/documentation/metalperformanceshaders/mpsstate/2947916-resource)
- [func resourceSize() -> Int](/documentation/metalperformanceshaders/mpsstate/2942397-resourcesize)
- [func resourceType(at: Int) -> MPSStateResourceType](/documentation/metalperformanceshaders/mpsstate/2947902-resourcetype)
- [func synchronize(on: any MTLCommandBuffer)](/documentation/metalperformanceshaders/mpsstate/2942396-synchronize)
- [func textureInfo(at: Int) -> MPSStateTextureInfo](/documentation/metalperformanceshaders/mpsstate/2947899-textureinfo)

###### Type Methods

- [class func temporaryState(with: any MTLCommandBuffer) -> Self](/documentation/metalperformanceshaders/mpsstate/2942393-temporarystate)
- [class func temporaryState(with: any MTLCommandBuffer, bufferSize: Int) -> Self](/documentation/metalperformanceshaders/mpsstate/2942391-temporarystate)
- [class func temporaryState(with: any MTLCommandBuffer, resourceList: MPSStateResourceList) -> Self](/documentation/metalperformanceshaders/mpsstate/2947915-temporarystate)
- [class func temporaryState(with: any MTLCommandBuffer, textureDescriptor: MTLTextureDescriptor) -> Self](/documentation/metalperformanceshaders/mpsstate/2942395-temporarystate)
- [MPSKernel](/documentation/metalperformanceshaders/mpskernel)

###### Initializers

- [init?(coder: NSCoder)](/documentation/metalperformanceshaders/mpskernel/2875161-init)
- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpskernel/2867190-init)

###### Methods

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpskernel/1618763-init)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpskernel/1618912-copy)

###### Properties

- [var options: MPSKernelOptions](/documentation/metalperformanceshaders/mpskernel/1618889-options)
- [MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions)

###### Constants

- [static var none: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1618816-none)
- [static var skipAPIValidation: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1618826-skipapivalidation)
- [static var allowReducedPrecision: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1618748-allowreducedprecision)
- [static var disableInternalTiling: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1648950-disableinternaltiling)
- [static var insertDebugGroups: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1648897-insertdebuggroups)

###### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpskerneloptions/1618747-init)

###### Type Properties

- [static var verbose: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/2889867-verbose)
- [var device: any MTLDevice](/documentation/metalperformanceshaders/mpskernel/1618824-device)
- [var label: String?](/documentation/metalperformanceshaders/mpskernel/1618803-label)
- [MPSImageDescriptor](/documentation/metalperformanceshaders/mpsimagedescriptor)

###### Methods

- [init(channelFormat: MPSImageFeatureChannelFormat, width: Int, height: Int, featureChannels: Int)](/documentation/metalperformanceshaders/mpsimagedescriptor/1648819-init)
- [init(channelFormat: MPSImageFeatureChannelFormat, width: Int, height: Int, featureChannels: Int, numberOfImages: Int, usage: MTLTextureUsage)](/documentation/metalperformanceshaders/mpsimagedescriptor/1648893-init)

###### Properties

- [var width: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648830-width)
- [var height: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648947-height)
- [var featureChannels: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648918-featurechannels)
- [var numberOfImages: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648846-numberofimages)
- [var pixelFormat: MTLPixelFormat](/documentation/metalperformanceshaders/mpsimagedescriptor/1648913-pixelformat)
- [var channelFormat: MPSImageFeatureChannelFormat](/documentation/metalperformanceshaders/mpsimagedescriptor/1648818-channelformat)
- [var cpuCacheMode: MTLCPUCacheMode](/documentation/metalperformanceshaders/mpsimagedescriptor/1648930-cpucachemode)
- [var storageMode: MTLStorageMode](/documentation/metalperformanceshaders/mpsimagedescriptor/1648955-storagemode)
- [var usage: MTLTextureUsage](/documentation/metalperformanceshaders/mpsimagedescriptor/1648937-usage)

###### Instance Methods

- [func copy(with: NSZone?) -> Self](/documentation/metalperformanceshaders/mpsimagedescriptor/3020686-copy)
- [func paddingMethod() -> MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpadding/2866950-paddingmethod)
- [func label() -> String](/documentation/metalperformanceshaders/mpsnnpadding/2889870-label)
- [func inverse() -> Self?](/documentation/metalperformanceshaders/mpsnnpadding/2942456-inverse)
- [var resultImage: MPSNNImageNode](/documentation/metalperformanceshaders/mpsnnfilternode/2866492-resultimage)
- [var resultState: MPSNNStateNode?](/documentation/metalperformanceshaders/mpsnnfilternode/2866503-resultstate)
- [var resultStates: [MPSNNStateNode]?](/documentation/metalperformanceshaders/mpsnnfilternode/2866486-resultstates)
- [MPSNNStateNode](/documentation/metalperformanceshaders/mpsnnstatenode)

##### Instance Properties

- [var handle: (any MPSHandle)?](/documentation/metalperformanceshaders/mpsnnstatenode/2866426-handle)
- [var exportFromGraph: Bool](/documentation/metalperformanceshaders/mpsnnstatenode/2942640-exportfromgraph)
- [var synchronizeResource: Bool](/documentation/metalperformanceshaders/mpsnnstatenode/2942639-synchronizeresource)
- [MPSNNBinaryGradientStateNode](/documentation/metalperformanceshaders/mpsnnbinarygradientstatenode)
- [MPSNNGradientStateNode](/documentation/metalperformanceshaders/mpsnngradientstatenode)

#### Instance Methods

- [func gradientFilter(withSource: MPSNNImageNode) -> MPSNNGradientFilterNode](/documentation/metalperformanceshaders/mpsnnfilternode/2953941-gradientfilter)
- [func gradientFilter(withSources: [MPSNNImageNode]) -> MPSNNGradientFilterNode](/documentation/metalperformanceshaders/mpsnnfilternode/2948052-gradientfilter)
- [func gradientFilters(withSource: MPSNNImageNode) -> [MPSNNGradientFilterNode]](/documentation/metalperformanceshaders/mpsnnfilternode/2953944-gradientfilters)
- [func gradientFilters(withSources: [MPSNNImageNode]) -> [MPSNNGradientFilterNode]](/documentation/metalperformanceshaders/mpsnnfilternode/2951955-gradientfilters)
- [func trainingGraph(withSourceGradient: MPSNNImageNode?, nodeHandler: MPSGradientNodeBlock?) -> [MPSNNFilterNode]?](/documentation/metalperformanceshaders/mpsnnfilternode/3020688-traininggraph)
- [MPSNNGradientFilterNode](/documentation/metalperformanceshaders/mpsnngradientfilternode)

### Protocols

- [MPSNNTrainableNode](/documentation/metalperformanceshaders/mpsnntrainablenode)

#### Instance Properties

- [var trainingStyle: MPSNNTrainingStyle](/documentation/metalperformanceshaders/mpsnntrainablenode/2952971-trainingstyle)
- [Convolutional Neural Network Kernels](/documentation/metalperformanceshaders/convolutional_neural_network_kernels)

### Arithmetic Layers

- [MPSCNNAdd](/documentation/metalperformanceshaders/mpscnnadd)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnadd/2942501-init)
- [MPSCNNAddGradient](/documentation/metalperformanceshaders/mpscnnaddgradient)

#### Initializers

- [init(device: any MTLDevice, isSecondarySourceFilter: Bool)](/documentation/metalperformanceshaders/mpscnnaddgradient/2956163-init)
- [MPSCNNSubtract](/documentation/metalperformanceshaders/mpscnnsubtract)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnsubtract/2942503-init)
- [MPSCNNSubtractGradient](/documentation/metalperformanceshaders/mpscnnsubtractgradient)

#### Initializers

- [init(device: any MTLDevice, isSecondarySourceFilter: Bool)](/documentation/metalperformanceshaders/mpscnnsubtractgradient/2956165-init)
- [MPSCNNMultiply](/documentation/metalperformanceshaders/mpscnnmultiply)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnmultiply/2942507-init)
- [MPSCNNMultiplyGradient](/documentation/metalperformanceshaders/mpscnnmultiplygradient)

#### Initializers

- [init(device: any MTLDevice, isSecondarySourceFilter: Bool)](/documentation/metalperformanceshaders/mpscnnmultiplygradient/2956164-init)
- [MPSCNNDivide](/documentation/metalperformanceshaders/mpscnndivide)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnndivide/2942508-init)
- [MPSCNNArithmetic](/documentation/metalperformanceshaders/mpscnnarithmetic)

#### Instance Properties

- [var bias: Float](/documentation/metalperformanceshaders/mpscnnarithmetic/2942499-bias)
- [var maximumValue: Float](/documentation/metalperformanceshaders/mpscnnarithmetic/2942498-maximumvalue)
- [var minimumValue: Float](/documentation/metalperformanceshaders/mpscnnarithmetic/2942502-minimumvalue)
- [var primaryScale: Float](/documentation/metalperformanceshaders/mpscnnarithmetic/2942509-primaryscale)
- [var primaryStrideInFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnarithmetic/2947963-primarystrideinfeaturechannels)
- [var secondaryScale: Float](/documentation/metalperformanceshaders/mpscnnarithmetic/2942497-secondaryscale)
- [var secondaryStrideInFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnarithmetic/2947964-secondarystrideinfeaturechannels)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, primaryImage: MPSImage, secondaryImage: MPSImage, destinationState: MPSCNNArithmeticGradientState, destinationImage: MPSImage)](/documentation/metalperformanceshaders/mpscnnarithmetic/2954876-encode)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, primaryImages: [MPSImage], secondaryImages: [MPSImage], destinationStates: [MPSCNNArithmeticGradientState], destinationImages: [MPSImage])](/documentation/metalperformanceshaders/mpscnnarithmetic/2954877-encodebatch)
- [MPSCNNArithmeticGradient](/documentation/metalperformanceshaders/mpscnnarithmeticgradient)

#### Instance Properties

- [var bias: Float](/documentation/metalperformanceshaders/mpscnnarithmeticgradient/2951855-bias)
- [var isSecondarySourceFilter: Bool](/documentation/metalperformanceshaders/mpscnnarithmeticgradient/2951852-issecondarysourcefilter)
- [var maximumValue: Float](/documentation/metalperformanceshaders/mpscnnarithmeticgradient/2951854-maximumvalue)
- [var minimumValue: Float](/documentation/metalperformanceshaders/mpscnnarithmeticgradient/2951858-minimumvalue)
- [var primaryScale: Float](/documentation/metalperformanceshaders/mpscnnarithmeticgradient/2951861-primaryscale)
- [var secondaryScale: Float](/documentation/metalperformanceshaders/mpscnnarithmeticgradient/2951856-secondaryscale)
- [var secondaryStrideInFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnarithmeticgradient/2951853-secondarystrideinfeaturechannels)
- [MPSCNNArithmeticGradientState](/documentation/metalperformanceshaders/mpscnnarithmeticgradientstate)

### Convolution Layers

- [MPSCNNBinaryConvolution](/documentation/metalperformanceshaders/mpscnnbinaryconvolution)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnbinaryconvolution/2867194-init)
- [init(device: any MTLDevice, convolutionData: any MPSCNNConvolutionDataSource, outputBiasTerms: UnsafePointer<Float>?, outputScaleTerms: UnsafePointer<Float>?, inputBiasTerms: UnsafePointer<Float>?, inputScaleTerms: UnsafePointer<Float>?, type: MPSCNNBinaryConvolutionType, flags: MPSCNNBinaryConvolutionFlags)](/documentation/metalperformanceshaders/mpscnnbinaryconvolution/2866978-init)
- [init(device: any MTLDevice, convolutionData: any MPSCNNConvolutionDataSource, scaleValue: Float, type: MPSCNNBinaryConvolutionType, flags: MPSCNNBinaryConvolutionFlags)](/documentation/metalperformanceshaders/mpscnnbinaryconvolution/2866981-init)
- [MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource)

##### Instance Methods

- [func biasTerms() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867023-biasterms)
- [func dataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867139-datatype)
- [func descriptor() -> MPSCNNConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867050-descriptor)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2881197-label)
- [func load() -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867049-load)
- [func lookupTableForUInt8Kernel() -> UnsafeMutablePointer<Float>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867186-lookuptableforuint8kernel)
- [func purge()](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867134-purge)
- [func rangesForUInt8Kernel() -> UnsafeMutablePointer<vector_float2>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867145-rangesforuint8kernel)
- [func weights() -> UnsafeMutableRawPointer](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867187-weights)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3013778-copy)
- [func kernelWeightsDataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3564466-kernelweightsdatatype)
- [func update(with: any MTLCommandBuffer, gradientState: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> MPSCNNConvolutionWeightsAndBiasesState?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953007-update)
- [func update(with: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953009-update)
- [func weightsLayout() -> MPSCNNConvolutionWeightsLayout](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3325840-weightslayout)
- [func weightsQuantizationType() -> MPSCNNWeightsQuantizationType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2976466-weightsquantizationtype)
- [MPSCNNBinaryConvolutionType](/documentation/metalperformanceshaders/mpscnnbinaryconvolutiontype)

##### Enumeration Cases

- [case AND](/documentation/metalperformanceshaders/mpscnnbinaryconvolutiontype/and)
- [case XNOR](/documentation/metalperformanceshaders/mpscnnbinaryconvolutiontype/xnor)
- [case binaryWeights](/documentation/metalperformanceshaders/mpscnnbinaryconvolutiontype/binaryweights)
- [MPSCNNBinaryConvolutionFlags](/documentation/metalperformanceshaders/mpscnnbinaryconvolutionflags)

##### Enumeration Cases

- [case none](/documentation/metalperformanceshaders/mpscnnbinaryconvolutionflags/none)
- [case useBetaScaling](/documentation/metalperformanceshaders/mpscnnbinaryconvolutionflags/usebetascaling)

#### Instance Properties

- [var inputFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnbinaryconvolution/2867126-inputfeaturechannels)
- [var outputFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnbinaryconvolution/2866959-outputfeaturechannels)
- [MPSCNNConvolution](/documentation/metalperformanceshaders/mpscnnconvolution)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnconvolution/2867142-init)
- [init(device: any MTLDevice, convolutionDescriptor: MPSCNNConvolutionDescriptor, kernelWeights: UnsafePointer<Float>, biasTerms: UnsafePointer<Float>?, flags: MPSCNNConvolutionFlags)](/documentation/metalperformanceshaders/mpscnnconvolution/1648861-init)
- [MPSCNNConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor)

##### Initializers

- [init?(coder: NSCoder)](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2867024-init)
- [init(kernelWidth: Int, kernelHeight: Int, inputFeatureChannels: Int, outputFeatureChannels: Int)](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648813-init)
- [init(kernelWidth: Int, kernelHeight: Int, inputFeatureChannels: Int, outputFeatureChannels: Int, neuronFilter: MPSCNNNeuron?)](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648876-init)

##### Instance Properties

- [var groups: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648849-groups)
- [var inputFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648934-inputfeaturechannels)
- [var kernelHeight: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648904-kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648959-kernelwidth)
- [var outputFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648852-outputfeaturechannels)
- [var strideInPixelsX: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648908-strideinpixelsx)
- [var strideInPixelsY: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648847-strideinpixelsy)
- [var neuron: MPSCNNNeuron?](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1829442-neuron)
- [var dilationRateX: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2881195-dilationratex)
- [var dilationRateY: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2881196-dilationratey)
- [func neuronParameterA() -> Float](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2875215-neuronparametera)
- [func neuronParameterB() -> Float](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2875213-neuronparameterb)
- [func neuronType() -> MPSCNNNeuronType](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2875219-neurontype)
- [var fusedNeuronDescriptor: MPSNNNeuronDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2953957-fusedneurondescriptor)

##### Instance Methods

- [func encode(with: NSCoder)](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2866972-encode)
- [func setBatchNormalizationParametersForInferenceWithMean(UnsafePointer<Float>?, variance: UnsafePointer<Float>?, gamma: UnsafePointer<Float>?, beta: UnsafePointer<Float>?, epsilon: Float)](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2867057-setbatchnormalizationparametersf)
- [func setNeuronToPReLUWithParametersA(Data)](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2921663-setneurontopreluwithparametersa)
- [func setNeuronType(MPSCNNNeuronType, parameterA: Float, parameterB: Float)](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2921657-setneurontype)

##### Type Properties

- [class var supportsSecureCoding: Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2867154-supportssecurecoding)
- [MPSCNNConvolutionFlags](/documentation/metalperformanceshaders/mpscnnconvolutionflags)

##### Enumeration Cases

- [case none](/documentation/metalperformanceshaders/mpscnnconvolutionflags/none)
- [init(device: any MTLDevice, weights: any MPSCNNConvolutionDataSource)](/documentation/metalperformanceshaders/mpscnnconvolution/2867092-init)
- [MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource)

##### Instance Methods

- [func biasTerms() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867023-biasterms)
- [func dataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867139-datatype)
- [func descriptor() -> MPSCNNConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867050-descriptor)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2881197-label)
- [func load() -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867049-load)
- [func lookupTableForUInt8Kernel() -> UnsafeMutablePointer<Float>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867186-lookuptableforuint8kernel)
- [func purge()](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867134-purge)
- [func rangesForUInt8Kernel() -> UnsafeMutablePointer<vector_float2>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867145-rangesforuint8kernel)
- [func weights() -> UnsafeMutableRawPointer](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867187-weights)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3013778-copy)
- [func kernelWeightsDataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3564466-kernelweightsdatatype)
- [func update(with: any MTLCommandBuffer, gradientState: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> MPSCNNConvolutionWeightsAndBiasesState?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953007-update)
- [func update(with: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953009-update)
- [func weightsLayout() -> MPSCNNConvolutionWeightsLayout](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3325840-weightslayout)
- [func weightsQuantizationType() -> MPSCNNWeightsQuantizationType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2976466-weightsquantizationtype)

#### Instance Properties

- [var inputFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnconvolution/1845268-inputfeaturechannels)
- [var outputFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnconvolution/1845271-outputfeaturechannels)
- [var groups: Int](/documentation/metalperformanceshaders/mpscnnconvolution/1845269-groups)
- [var subPixelScaleFactor: Int](/documentation/metalperformanceshaders/mpscnnconvolution/2873341-subpixelscalefactor)
- [var neuron: MPSCNNNeuron?](/documentation/metalperformanceshaders/mpscnnconvolution/1845274-neuron)
- [MPSCNNNeuron](/documentation/metalperformanceshaders/mpscnnneuron)

##### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnneuron/2867058-init)
- [init(device: any MTLDevice, neuronDescriptor: MPSNNNeuronDescriptor)](/documentation/metalperformanceshaders/mpscnnneuron/2942315-init)

##### Instance Properties

- [var a: Float](/documentation/metalperformanceshaders/mpscnnneuron/2942297-a)
- [var b: Float](/documentation/metalperformanceshaders/mpscnnneuron/2942306-b)
- [var c: Float](/documentation/metalperformanceshaders/mpscnnneuron/2942303-c)
- [var data: Data?](/documentation/metalperformanceshaders/mpscnnneuron/2942308-data)
- [var neuronType: MPSCNNNeuronType](/documentation/metalperformanceshaders/mpscnnneuron/2942309-neurontype)
- [var neuronType: MPSCNNNeuronType](/documentation/metalperformanceshaders/mpscnnconvolution/2875190-neurontype)
- [MPSCNNNeuronType](/documentation/metalperformanceshaders/mpscnnneurontype)

##### Enumeration Cases

- [case none](/documentation/metalperformanceshaders/mpscnnneurontype/none)
- [case reLU](/documentation/metalperformanceshaders/mpscnnneurontype/relu)
- [case linear](/documentation/metalperformanceshaders/mpscnnneurontype/linear)
- [case sigmoid](/documentation/metalperformanceshaders/mpscnnneurontype/sigmoid)
- [case hardSigmoid](/documentation/metalperformanceshaders/mpscnnneurontype/hardsigmoid)
- [case tanH](/documentation/metalperformanceshaders/mpscnnneurontype/tanh)
- [case absolute](/documentation/metalperformanceshaders/mpscnnneurontype/absolute)
- [case softPlus](/documentation/metalperformanceshaders/mpscnnneurontype/softplus)
- [case softSign](/documentation/metalperformanceshaders/mpscnnneurontype/softsign)
- [case ELU](/documentation/metalperformanceshaders/mpscnnneurontype/elu)
- [case count](/documentation/metalperformanceshaders/mpscnnneurontype/count)
- [case exponential](/documentation/metalperformanceshaders/mpscnnneurontype/exponential)
- [case geLU](/documentation/metalperformanceshaders/mpscnnneurontype/gelu)
- [case logarithm](/documentation/metalperformanceshaders/mpscnnneurontype/logarithm)
- [case pReLU](/documentation/metalperformanceshaders/mpscnnneurontype/prelu)
- [case power](/documentation/metalperformanceshaders/mpscnnneurontype/power)
- [case reLUN](/documentation/metalperformanceshaders/mpscnnneurontype/relun)
- [var neuronParameterA: Float](/documentation/metalperformanceshaders/mpscnnconvolution/2875214-neuronparametera)
- [var neuronParameterB: Float](/documentation/metalperformanceshaders/mpscnnconvolution/2875218-neuronparameterb)
- [var accumulatorPrecisionOption: MPSNNConvolutionAccumulatorPrecisionOption](/documentation/metalperformanceshaders/mpscnnconvolution/2942410-accumulatorprecisionoption)
- [var channelMultiplier: Int](/documentation/metalperformanceshaders/mpscnnconvolution/2919729-channelmultiplier)
- [var dataSource: any MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolution/2953961-datasource)
- [var fusedNeuronDescriptor: MPSNNNeuronDescriptor?](/documentation/metalperformanceshaders/mpscnnconvolution/3013776-fusedneurondescriptor)
- [var neuronParameterC: Float](/documentation/metalperformanceshaders/mpscnnconvolution/2935626-neuronparameterc)

#### Instance Methods

- [func exportWeightsAndBiases(with: any MTLCommandBuffer, resultStateCanBeTemporary: Bool) -> MPSCNNConvolutionWeightsAndBiasesState](/documentation/metalperformanceshaders/mpscnnconvolution/2953001-exportweightsandbiases)
- [func reloadWeightsAndBiases(with: any MPSCNNConvolutionDataSource)](/documentation/metalperformanceshaders/mpscnnconvolution/2942428-reloadweightsandbiases)
- [func reloadWeightsAndBiases(with: any MTLCommandBuffer, state: MPSCNNConvolutionWeightsAndBiasesState)](/documentation/metalperformanceshaders/mpscnnconvolution/2953962-reloadweightsandbiases)
- [func reloadWeightsAndBiasesFromDataSource()](/documentation/metalperformanceshaders/mpscnnconvolution/2966657-reloadweightsandbiasesfromdataso)
- [func resultState(sourceImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSCNNConvolutionGradientState?](/documentation/metalperformanceshaders/mpscnnconvolution/2947883-resultstate)
- [func resultStateBatch(sourceImage: [MPSImage], sourceStates: [[MPSState]]?, destinationImage: [MPSImage]) -> [MPSCNNConvolutionGradientState]?](/documentation/metalperformanceshaders/mpscnnconvolution/2947881-resultstatebatch)
- [func temporaryResultState(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSCNNConvolutionGradientState?](/documentation/metalperformanceshaders/mpscnnconvolution/2947885-temporaryresultstate)
- [func temporaryResultStateBatch(commandBuffer: any MTLCommandBuffer, sourceImage: [MPSImage], sourceStates: [[MPSState]]?, destinationImage: [MPSImage]) -> [MPSCNNConvolutionGradientState]?](/documentation/metalperformanceshaders/mpscnnconvolution/2947886-temporaryresultstatebatch)
- [MPSCNNDepthWiseConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnndepthwiseconvolutiondescriptor)

#### Instance Properties

- [var channelMultiplier: Int](/documentation/metalperformanceshaders/mpscnndepthwiseconvolutiondescriptor/2919731-channelmultiplier)
- [MPSCNNSubPixelConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnsubpixelconvolutiondescriptor)

#### Instance Properties

- [var subPixelScaleFactor: Int](/documentation/metalperformanceshaders/mpscnnsubpixelconvolutiondescriptor/2875156-subpixelscalefactor)
- [MPSCNNConvolutionTranspose](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/2866995-init)
- [init(device: any MTLDevice, weights: any MPSCNNConvolutionDataSource)](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/2867157-init)
- [MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource)

##### Instance Methods

- [func biasTerms() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867023-biasterms)
- [func dataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867139-datatype)
- [func descriptor() -> MPSCNNConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867050-descriptor)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2881197-label)
- [func load() -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867049-load)
- [func lookupTableForUInt8Kernel() -> UnsafeMutablePointer<Float>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867186-lookuptableforuint8kernel)
- [func purge()](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867134-purge)
- [func rangesForUInt8Kernel() -> UnsafeMutablePointer<vector_float2>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867145-rangesforuint8kernel)
- [func weights() -> UnsafeMutableRawPointer](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867187-weights)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3013778-copy)
- [func kernelWeightsDataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3564466-kernelweightsdatatype)
- [func update(with: any MTLCommandBuffer, gradientState: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> MPSCNNConvolutionWeightsAndBiasesState?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953007-update)
- [func update(with: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953009-update)
- [func weightsLayout() -> MPSCNNConvolutionWeightsLayout](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3325840-weightslayout)
- [func weightsQuantizationType() -> MPSCNNWeightsQuantizationType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2976466-weightsquantizationtype)

#### Instance Properties

- [var groups: Int](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/2867099-groups)
- [var inputFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/2867174-inputfeaturechannels)
- [var kernelOffsetX: Int](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/2867176-kerneloffsetx)
- [var kernelOffsetY: Int](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/2867086-kerneloffsety)
- [var outputFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/2867016-outputfeaturechannels)
- [var accumulatorPrecisionOption: MPSNNConvolutionAccumulatorPrecisionOption](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/2951924-accumulatorprecisionoption)
- [var dataSource: any MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/3131769-datasource)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, convolutionGradientState: MPSCNNConvolutionGradientState?) -> MPSImage](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/2942409-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, convolutionGradientState: MPSCNNConvolutionGradientState?, destinationImage: MPSImage)](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/2942429-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, convolutionGradientState: MPSCNNConvolutionGradientState?, destinationState: AutoreleasingUnsafeMutablePointer<MPSCNNConvolutionTransposeGradientState?>, destinationStateIsTemporary: Bool) -> MPSImage](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/3131771-encode)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], convolutionGradientStates: [MPSCNNConvolutionGradientState]?) -> [MPSImage]](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/2942406-encodebatch)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], convolutionGradientStates: [MPSCNNConvolutionGradientState]?, destinationImages: [MPSImage])](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/2942411-encodebatch)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], convolutionGradientStates: [MPSCNNConvolutionGradientState]?, destinationStates: AutoreleasingUnsafeMutablePointer<NSArray?>, destinationStateIsTemporary: Bool) -> [MPSImage]](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/3131770-encodebatch)
- [func exportWeightsAndBiases(with: any MTLCommandBuffer, resultStateCanBeTemporary: Bool) -> MPSCNNConvolutionWeightsAndBiasesState](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/3131772-exportweightsandbiases)
- [func reloadWeightsAndBiases(with: any MTLCommandBuffer, state: MPSCNNConvolutionWeightsAndBiasesState)](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/3131774-reloadweightsandbiases)
- [func reloadWeightsAndBiasesFromDataSource()](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/3131773-reloadweightsandbiasesfromdataso)
- [func resultState(sourceImage: MPSImage, sourceStates: [MPSCNNConvolutionGradientState]?, destinationImage: MPSImage) -> MPSCNNConvolutionTransposeGradientState?](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/3131776-resultstate)
- [func resultStateBatch(sourceImage: [MPSImage], sourceStates: [[MPSCNNConvolutionGradientState]]?, destinationImage: [MPSImage]) -> [MPSCNNConvolutionTransposeGradientState]?](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/3131775-resultstatebatch)
- [func temporaryResultState(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, sourceStates: [MPSCNNConvolutionGradientState]?, destinationImage: MPSImage) -> MPSCNNConvolutionTransposeGradientState?](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/3131778-temporaryresultstate)
- [func temporaryResultStateBatch(commandBuffer: any MTLCommandBuffer, sourceImage: [MPSImage], sourceStates: [[MPSCNNConvolutionGradientState]]?, destinationImage: [MPSImage]) -> [MPSCNNConvolutionTransposeGradientState]?](/documentation/metalperformanceshaders/mpscnnconvolutiontranspose/3131777-temporaryresultstatebatch)
- [MPSCNNConvolutionGradient](/documentation/metalperformanceshaders/mpscnnconvolutiongradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnconvolutiongradient/2942425-init)
- [init(device: any MTLDevice, weights: any MPSCNNConvolutionDataSource)](/documentation/metalperformanceshaders/mpscnnconvolutiongradient/2942414-init)

#### Instance Properties

- [var channelMultiplier: Int](/documentation/metalperformanceshaders/mpscnnconvolutiongradient/2966658-channelmultiplier)
- [var dataSource: any MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiongradient/2953959-datasource)
- [var gradientOption: MPSCNNConvolutionGradientOption](/documentation/metalperformanceshaders/mpscnnconvolutiongradient/2942432-gradientoption)
- [var groups: Int](/documentation/metalperformanceshaders/mpscnnconvolutiongradient/2942430-groups)
- [var serializeWeightsAndBiases: Bool](/documentation/metalperformanceshaders/mpscnnconvolutiongradient/2951926-serializeweightsandbiases)
- [var sourceGradientFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnconvolutiongradient/2947880-sourcegradientfeaturechannels)
- [var sourceImageFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnconvolutiongradient/2947882-sourceimagefeaturechannels)

#### Instance Methods

- [func reloadWeightsAndBiases(with: any MTLCommandBuffer, state: MPSCNNConvolutionWeightsAndBiasesState)](/documentation/metalperformanceshaders/mpscnnconvolutiongradient/2953960-reloadweightsandbiases)
- [func reloadWeightsAndBiasesFromDataSource()](/documentation/metalperformanceshaders/mpscnnconvolutiongradient/2966659-reloadweightsandbiasesfromdataso)
- [MPSCNNConvolutionGradientState](/documentation/metalperformanceshaders/mpscnnconvolutiongradientstate)

#### Instance Properties

- [var convolution: MPSCNNConvolution](/documentation/metalperformanceshaders/mpscnnconvolutiongradientstate/2953958-convolution)
- [var gradientForBiases: any MTLBuffer](/documentation/metalperformanceshaders/mpscnnconvolutiongradientstate/2947887-gradientforbiases)
- [var gradientForWeights: any MTLBuffer](/documentation/metalperformanceshaders/mpscnnconvolutiongradientstate/2947889-gradientforweights)
- [var gradientForWeightsLayout: MPSCNNConvolutionWeightsLayout](/documentation/metalperformanceshaders/mpscnnconvolutiongradientstate/3325841-gradientforweightslayout)
- [MPSImageSizeEncodingState](/documentation/metalperformanceshaders/mpsimagesizeencodingstate)

#### Instance Properties

- [var sourceHeight: Int](/documentation/metalperformanceshaders/mpsimagesizeencodingstate/2873329-sourceheight)
- [var sourceWidth: Int](/documentation/metalperformanceshaders/mpsimagesizeencodingstate/2873364-sourcewidth)
- [MPSCNNConvolutionWeightsAndBiasesState](/documentation/metalperformanceshaders/mpscnnconvolutionweightsandbiasesstate)

#### Initializers

- [init(device: any MTLDevice, cnnConvolutionDescriptor: MPSCNNConvolutionDescriptor)](/documentation/metalperformanceshaders/mpscnnconvolutionweightsandbiasesstate/2953004-init)
- [init(weights: any MTLBuffer, biases: (any MTLBuffer)?)](/documentation/metalperformanceshaders/mpscnnconvolutionweightsandbiasesstate/2953008-init)
- [init(weights: any MTLBuffer, weightsOffset: Int, biases: (any MTLBuffer)?, biasesOffset: Int, cnnConvolutionDescriptor: MPSCNNConvolutionDescriptor)](/documentation/metalperformanceshaders/mpscnnconvolutionweightsandbiasesstate/3325843-init)

#### Instance Properties

- [var biases: (any MTLBuffer)?](/documentation/metalperformanceshaders/mpscnnconvolutionweightsandbiasesstate/2953002-biases)
- [var biasesOffset: Int](/documentation/metalperformanceshaders/mpscnnconvolutionweightsandbiasesstate/3325842-biasesoffset)
- [var weights: any MTLBuffer](/documentation/metalperformanceshaders/mpscnnconvolutionweightsandbiasesstate/2953006-weights)
- [var weightsOffset: Int](/documentation/metalperformanceshaders/mpscnnconvolutionweightsandbiasesstate/3325844-weightsoffset)

#### Type Methods

- [class func temporaryCNNConvolutionWeightsAndBiasesState(with: any MTLCommandBuffer, cnnConvolutionDescriptor: MPSCNNConvolutionDescriptor) -> Self](/documentation/metalperformanceshaders/mpscnnconvolutionweightsandbiasesstate/2953005-temporarycnnconvolutionweightsan)

### Pooling Layers

- [MPSCNNPoolingAverage](/documentation/metalperformanceshaders/mpscnnpoolingaverage)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnpoolingaverage/2866999-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int, strideInPixelsX: Int, strideInPixelsY: Int)](/documentation/metalperformanceshaders/mpscnnpoolingaverage/2875216-init)

#### Instance Properties

- [var zeroPadSizeX: Int](/documentation/metalperformanceshaders/mpscnnpoolingaverage/2875207-zeropadsizex)
- [var zeroPadSizeY: Int](/documentation/metalperformanceshaders/mpscnnpoolingaverage/2875221-zeropadsizey)
- [MPSCNNPoolingAverageGradient](/documentation/metalperformanceshaders/mpscnnpoolingaveragegradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnpoolingaveragegradient/2942345-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int, strideInPixelsX: Int, strideInPixelsY: Int)](/documentation/metalperformanceshaders/mpscnnpoolingaveragegradient/2942339-init)

#### Instance Properties

- [var zeroPadSizeX: Int](/documentation/metalperformanceshaders/mpscnnpoolingaveragegradient/2942341-zeropadsizex)
- [var zeroPadSizeY: Int](/documentation/metalperformanceshaders/mpscnnpoolingaveragegradient/2942354-zeropadsizey)
- [MPSCNNPoolingL2Norm](/documentation/metalperformanceshaders/mpscnnpoolingl2norm)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnpoolingl2norm/2867141-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int, strideInPixelsX: Int, strideInPixelsY: Int)](/documentation/metalperformanceshaders/mpscnnpoolingl2norm/2875162-init)
- [MPSCNNPoolingMax](/documentation/metalperformanceshaders/mpscnnpoolingmax)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnpoolingmax/2867097-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int, strideInPixelsX: Int, strideInPixelsY: Int)](/documentation/metalperformanceshaders/mpscnnpoolingmax/2875151-init)
- [MPSCNNDilatedPoolingMax](/documentation/metalperformanceshaders/mpscnndilatedpoolingmax)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnndilatedpoolingmax/2873025-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int, dilationRateX: Int, dilationRateY: Int, strideInPixelsX: Int, strideInPixelsY: Int)](/documentation/metalperformanceshaders/mpscnndilatedpoolingmax/2881192-init)

#### Instance Properties

- [var dilationRateX: Int](/documentation/metalperformanceshaders/mpscnndilatedpoolingmax/2881194-dilationratex)
- [var dilationRateY: Int](/documentation/metalperformanceshaders/mpscnndilatedpoolingmax/2881193-dilationratey)
- [MPSCNNPooling](/documentation/metalperformanceshaders/mpscnnpooling)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnpooling/2866975-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int)](/documentation/metalperformanceshaders/mpscnnpooling/1648887-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int, strideInPixelsX: Int, strideInPixelsY: Int)](/documentation/metalperformanceshaders/mpscnnpooling/1648902-init)
- [MPSCNNPoolingGradient](/documentation/metalperformanceshaders/mpscnnpoolinggradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnpoolinggradient/2942350-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int)](/documentation/metalperformanceshaders/mpscnnpoolinggradient/2942337-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int, strideInPixelsX: Int, strideInPixelsY: Int)](/documentation/metalperformanceshaders/mpscnnpoolinggradient/2942347-init)

#### Instance Properties

- [var sourceSize: MTLSize](/documentation/metalperformanceshaders/mpscnnpoolinggradient/2942343-sourcesize)
- [MPSCNNDilatedPoolingMaxGradient](/documentation/metalperformanceshaders/mpscnndilatedpoolingmaxgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnndilatedpoolingmaxgradient/2942346-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int, dilationRateX: Int, dilationRateY: Int, strideInPixelsX: Int, strideInPixelsY: Int)](/documentation/metalperformanceshaders/mpscnndilatedpoolingmaxgradient/2942349-init)
- [MPSCNNPoolingL2NormGradient](/documentation/metalperformanceshaders/mpscnnpoolingl2normgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnpoolingl2normgradient/2942352-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int, strideInPixelsX: Int, strideInPixelsY: Int)](/documentation/metalperformanceshaders/mpscnnpoolingl2normgradient/2942355-init)
- [MPSCNNPoolingMaxGradient](/documentation/metalperformanceshaders/mpscnnpoolingmaxgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnpoolingmaxgradient/2942342-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int, strideInPixelsX: Int, strideInPixelsY: Int)](/documentation/metalperformanceshaders/mpscnnpoolingmaxgradient/2942348-init)

### Fully Connected Layers

- [MPSCNNBinaryFullyConnected](/documentation/metalperformanceshaders/mpscnnbinaryfullyconnected)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnbinaryfullyconnected/2867052-init)
- [init(device: any MTLDevice, convolutionData: any MPSCNNConvolutionDataSource, outputBiasTerms: UnsafePointer<Float>?, outputScaleTerms: UnsafePointer<Float>?, inputBiasTerms: UnsafePointer<Float>?, inputScaleTerms: UnsafePointer<Float>?, type: MPSCNNBinaryConvolutionType, flags: MPSCNNBinaryConvolutionFlags)](/documentation/metalperformanceshaders/mpscnnbinaryfullyconnected/2867059-init)
- [init(device: any MTLDevice, convolutionData: any MPSCNNConvolutionDataSource, scaleValue: Float, type: MPSCNNBinaryConvolutionType, flags: MPSCNNBinaryConvolutionFlags)](/documentation/metalperformanceshaders/mpscnnbinaryfullyconnected/2867196-init)
- [MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource)

##### Instance Methods

- [func biasTerms() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867023-biasterms)
- [func dataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867139-datatype)
- [func descriptor() -> MPSCNNConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867050-descriptor)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2881197-label)
- [func load() -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867049-load)
- [func lookupTableForUInt8Kernel() -> UnsafeMutablePointer<Float>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867186-lookuptableforuint8kernel)
- [func purge()](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867134-purge)
- [func rangesForUInt8Kernel() -> UnsafeMutablePointer<vector_float2>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867145-rangesforuint8kernel)
- [func weights() -> UnsafeMutableRawPointer](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867187-weights)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3013778-copy)
- [func kernelWeightsDataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3564466-kernelweightsdatatype)
- [func update(with: any MTLCommandBuffer, gradientState: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> MPSCNNConvolutionWeightsAndBiasesState?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953007-update)
- [func update(with: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953009-update)
- [func weightsLayout() -> MPSCNNConvolutionWeightsLayout](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3325840-weightslayout)
- [func weightsQuantizationType() -> MPSCNNWeightsQuantizationType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2976466-weightsquantizationtype)
- [MPSCNNBinaryConvolutionType](/documentation/metalperformanceshaders/mpscnnbinaryconvolutiontype)

##### Enumeration Cases

- [case AND](/documentation/metalperformanceshaders/mpscnnbinaryconvolutiontype/and)
- [case XNOR](/documentation/metalperformanceshaders/mpscnnbinaryconvolutiontype/xnor)
- [case binaryWeights](/documentation/metalperformanceshaders/mpscnnbinaryconvolutiontype/binaryweights)
- [MPSCNNBinaryConvolutionFlags](/documentation/metalperformanceshaders/mpscnnbinaryconvolutionflags)

##### Enumeration Cases

- [case none](/documentation/metalperformanceshaders/mpscnnbinaryconvolutionflags/none)
- [case useBetaScaling](/documentation/metalperformanceshaders/mpscnnbinaryconvolutionflags/usebetascaling)
- [MPSCNNFullyConnected](/documentation/metalperformanceshaders/mpscnnfullyconnected)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnfullyconnected/2867158-init)
- [init(device: any MTLDevice, weights: any MPSCNNConvolutionDataSource)](/documentation/metalperformanceshaders/mpscnnfullyconnected/2867198-init)
- [MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource)

##### Instance Methods

- [func biasTerms() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867023-biasterms)
- [func dataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867139-datatype)
- [func descriptor() -> MPSCNNConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867050-descriptor)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2881197-label)
- [func load() -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867049-load)
- [func lookupTableForUInt8Kernel() -> UnsafeMutablePointer<Float>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867186-lookuptableforuint8kernel)
- [func purge()](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867134-purge)
- [func rangesForUInt8Kernel() -> UnsafeMutablePointer<vector_float2>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867145-rangesforuint8kernel)
- [func weights() -> UnsafeMutableRawPointer](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867187-weights)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3013778-copy)
- [func kernelWeightsDataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3564466-kernelweightsdatatype)
- [func update(with: any MTLCommandBuffer, gradientState: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> MPSCNNConvolutionWeightsAndBiasesState?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953007-update)
- [func update(with: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953009-update)
- [func weightsLayout() -> MPSCNNConvolutionWeightsLayout](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3325840-weightslayout)
- [func weightsQuantizationType() -> MPSCNNWeightsQuantizationType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2976466-weightsquantizationtype)
- [init(device: any MTLDevice, convolutionDescriptor: MPSCNNConvolutionDescriptor, kernelWeights: UnsafePointer<Float>, biasTerms: UnsafePointer<Float>?, flags: MPSCNNConvolutionFlags)](/documentation/metalperformanceshaders/mpscnnfullyconnected/1829441-init)
- [MPSCNNConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor)

##### Initializers

- [init?(coder: NSCoder)](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2867024-init)
- [init(kernelWidth: Int, kernelHeight: Int, inputFeatureChannels: Int, outputFeatureChannels: Int)](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648813-init)
- [init(kernelWidth: Int, kernelHeight: Int, inputFeatureChannels: Int, outputFeatureChannels: Int, neuronFilter: MPSCNNNeuron?)](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648876-init)

##### Instance Properties

- [var groups: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648849-groups)
- [var inputFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648934-inputfeaturechannels)
- [var kernelHeight: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648904-kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648959-kernelwidth)
- [var outputFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648852-outputfeaturechannels)
- [var strideInPixelsX: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648908-strideinpixelsx)
- [var strideInPixelsY: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1648847-strideinpixelsy)
- [var neuron: MPSCNNNeuron?](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/1829442-neuron)
- [var dilationRateX: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2881195-dilationratex)
- [var dilationRateY: Int](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2881196-dilationratey)
- [func neuronParameterA() -> Float](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2875215-neuronparametera)
- [func neuronParameterB() -> Float](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2875213-neuronparameterb)
- [func neuronType() -> MPSCNNNeuronType](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2875219-neurontype)
- [var fusedNeuronDescriptor: MPSNNNeuronDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2953957-fusedneurondescriptor)

##### Instance Methods

- [func encode(with: NSCoder)](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2866972-encode)
- [func setBatchNormalizationParametersForInferenceWithMean(UnsafePointer<Float>?, variance: UnsafePointer<Float>?, gamma: UnsafePointer<Float>?, beta: UnsafePointer<Float>?, epsilon: Float)](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2867057-setbatchnormalizationparametersf)
- [func setNeuronToPReLUWithParametersA(Data)](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2921663-setneurontopreluwithparametersa)
- [func setNeuronType(MPSCNNNeuronType, parameterA: Float, parameterB: Float)](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2921657-setneurontype)

##### Type Properties

- [class var supportsSecureCoding: Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondescriptor/2867154-supportssecurecoding)
- [MPSCNNConvolutionFlags](/documentation/metalperformanceshaders/mpscnnconvolutionflags)

##### Enumeration Cases

- [case none](/documentation/metalperformanceshaders/mpscnnconvolutionflags/none)
- [MPSCNNFullyConnectedGradient](/documentation/metalperformanceshaders/mpscnnfullyconnectedgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnfullyconnectedgradient/2951923-init)
- [init(device: any MTLDevice, weights: any MPSCNNConvolutionDataSource)](/documentation/metalperformanceshaders/mpscnnfullyconnectedgradient/2951921-init)

### Neuron Layers

- [MPSCNNNeuronAbsolute](/documentation/metalperformanceshaders/mpscnnneuronabsolute)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnneuronabsolute/1648809-init)
- [MPSCNNNeuronELU](/documentation/metalperformanceshaders/mpscnnneuronelu)

#### Initializers

- [init(device: any MTLDevice, a: Float)](/documentation/metalperformanceshaders/mpscnnneuronelu/2867048-init)
- [MPSCNNNeuronHardSigmoid](/documentation/metalperformanceshaders/mpscnnneuronhardsigmoid)

#### Initializers

- [init(device: any MTLDevice, a: Float, b: Float)](/documentation/metalperformanceshaders/mpscnnneuronhardsigmoid/2875217-init)
- [MPSCNNNeuronLinear](/documentation/metalperformanceshaders/mpscnnneuronlinear)

#### Initializers

- [init(device: any MTLDevice, a: Float, b: Float)](/documentation/metalperformanceshaders/mpscnnneuronlinear/1648888-init)
- [MPSCNNNeuronPReLU](/documentation/metalperformanceshaders/mpscnnneuronprelu)

#### Initializers

- [init(device: any MTLDevice, a: UnsafePointer<Float>, count: Int)](/documentation/metalperformanceshaders/mpscnnneuronprelu/2921661-init)
- [MPSCNNNeuronReLUN](/documentation/metalperformanceshaders/mpscnnneuronrelun)

#### Initializers

- [init(device: any MTLDevice, a: Float, b: Float)](/documentation/metalperformanceshaders/mpscnnneuronrelun/2921658-init)
- [MPSCNNNeuronReLU](/documentation/metalperformanceshaders/mpscnnneuronrelu)

#### Initializers

- [init(device: any MTLDevice, a: Float)](/documentation/metalperformanceshaders/mpscnnneuronrelu/1648926-init)
- [MPSCNNNeuronSigmoid](/documentation/metalperformanceshaders/mpscnnneuronsigmoid)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnneuronsigmoid/1648890-init)
- [MPSCNNNeuronSoftPlus](/documentation/metalperformanceshaders/mpscnnneuronsoftplus)

#### Initializers

- [init(device: any MTLDevice, a: Float, b: Float)](/documentation/metalperformanceshaders/mpscnnneuronsoftplus/2866983-init)
- [MPSCNNNeuronSoftSign](/documentation/metalperformanceshaders/mpscnnneuronsoftsign)

#### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnneuronsoftsign/2866994-init)
- [MPSCNNNeuronTanH](/documentation/metalperformanceshaders/mpscnnneurontanh)

#### Initializers

- [init(device: any MTLDevice, a: Float, b: Float)](/documentation/metalperformanceshaders/mpscnnneurontanh/1648815-init)
- [MPSCNNNeuron](/documentation/metalperformanceshaders/mpscnnneuron)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnneuron/2867058-init)
- [init(device: any MTLDevice, neuronDescriptor: MPSNNNeuronDescriptor)](/documentation/metalperformanceshaders/mpscnnneuron/2942315-init)

#### Instance Properties

- [var a: Float](/documentation/metalperformanceshaders/mpscnnneuron/2942297-a)
- [var b: Float](/documentation/metalperformanceshaders/mpscnnneuron/2942306-b)
- [var c: Float](/documentation/metalperformanceshaders/mpscnnneuron/2942303-c)
- [var data: Data?](/documentation/metalperformanceshaders/mpscnnneuron/2942308-data)
- [var neuronType: MPSCNNNeuronType](/documentation/metalperformanceshaders/mpscnnneuron/2942309-neurontype)
- [MPSCNNNeuronExponential](/documentation/metalperformanceshaders/mpscnnneuronexponential)

#### Initializers

- [init(device: any MTLDevice, a: Float, b: Float, c: Float)](/documentation/metalperformanceshaders/mpscnnneuronexponential/2951870-init)
- [MPSCNNNeuronGradient](/documentation/metalperformanceshaders/mpscnnneurongradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnneurongradient/2942304-init)
- [init(device: any MTLDevice, neuronDescriptor: MPSNNNeuronDescriptor)](/documentation/metalperformanceshaders/mpscnnneurongradient/2942293-init)

#### Instance Properties

- [var a: Float](/documentation/metalperformanceshaders/mpscnnneurongradient/2942312-a)
- [var b: Float](/documentation/metalperformanceshaders/mpscnnneurongradient/2942313-b)
- [var c: Float](/documentation/metalperformanceshaders/mpscnnneurongradient/2942310-c)
- [var data: Data?](/documentation/metalperformanceshaders/mpscnnneurongradient/2942314-data)
- [var neuronType: MPSCNNNeuronType](/documentation/metalperformanceshaders/mpscnnneurongradient/2942300-neurontype)
- [MPSCNNNeuronLogarithm](/documentation/metalperformanceshaders/mpscnnneuronlogarithm)

#### Initializers

- [init(device: any MTLDevice, a: Float, b: Float, c: Float)](/documentation/metalperformanceshaders/mpscnnneuronlogarithm/2951871-init)
- [MPSCNNNeuronPower](/documentation/metalperformanceshaders/mpscnnneuronpower)

#### Initializers

- [init(device: any MTLDevice, a: Float, b: Float, c: Float)](/documentation/metalperformanceshaders/mpscnnneuronpower/2951868-init)
- [MPSNNNeuronDescriptor](/documentation/metalperformanceshaders/mpsnnneurondescriptor)

#### Instance Properties

- [var a: Float](/documentation/metalperformanceshaders/mpsnnneurondescriptor/2942316-a)
- [var b: Float](/documentation/metalperformanceshaders/mpsnnneurondescriptor/2942302-b)
- [var c: Float](/documentation/metalperformanceshaders/mpsnnneurondescriptor/2942305-c)
- [var data: Data?](/documentation/metalperformanceshaders/mpsnnneurondescriptor/2942299-data)
- [var neuronType: MPSCNNNeuronType](/documentation/metalperformanceshaders/mpsnnneurondescriptor/2942292-neurontype)

#### Type Methods

- [class func cnnNeuronDescriptor(with: MPSCNNNeuronType) -> MPSNNNeuronDescriptor](/documentation/metalperformanceshaders/mpsnnneurondescriptor/2942307-cnnneurondescriptor)
- [class func cnnNeuronDescriptor(with: MPSCNNNeuronType, a: Float) -> MPSNNNeuronDescriptor](/documentation/metalperformanceshaders/mpsnnneurondescriptor/2942301-cnnneurondescriptor)
- [class func cnnNeuronDescriptor(with: MPSCNNNeuronType, a: Float, b: Float) -> MPSNNNeuronDescriptor](/documentation/metalperformanceshaders/mpsnnneurondescriptor/2942295-cnnneurondescriptor)
- [class func cnnNeuronDescriptor(with: MPSCNNNeuronType, a: Float, b: Float, c: Float) -> MPSNNNeuronDescriptor](/documentation/metalperformanceshaders/mpsnnneurondescriptor/2942296-cnnneurondescriptor)
- [class func cnnNeuronPReLUDescriptor(with: Data, noCopy: Bool) -> MPSNNNeuronDescriptor](/documentation/metalperformanceshaders/mpsnnneurondescriptor/2942317-cnnneuronpreludescriptor)

### Softmax Layers

- [MPSCNNSoftMax](/documentation/metalperformanceshaders/mpscnnsoftmax)
- [MPSCNNLogSoftMax](/documentation/metalperformanceshaders/mpscnnlogsoftmax)
- [MPSCNNLogSoftMaxGradient](/documentation/metalperformanceshaders/mpscnnlogsoftmaxgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnlogsoftmaxgradient/2942619-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnlogsoftmaxgradient/2942622-init)
- [MPSCNNSoftMaxGradient](/documentation/metalperformanceshaders/mpscnnsoftmaxgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnsoftmaxgradient/2942618-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnsoftmaxgradient/2942620-init)

### Normalization Layers

- [MPSCNNCrossChannelNormalization](/documentation/metalperformanceshaders/mpscnncrosschannelnormalization)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnncrosschannelnormalization/2866991-init)
- [init(device: any MTLDevice, kernelSize: Int)](/documentation/metalperformanceshaders/mpscnncrosschannelnormalization/1648834-init)

#### Instance Properties

- [var alpha: Float](/documentation/metalperformanceshaders/mpscnncrosschannelnormalization/1648896-alpha)
- [var beta: Float](/documentation/metalperformanceshaders/mpscnncrosschannelnormalization/1648879-beta)
- [var delta: Float](/documentation/metalperformanceshaders/mpscnncrosschannelnormalization/1648881-delta)
- [var kernelSize: Int](/documentation/metalperformanceshaders/mpscnncrosschannelnormalization/1648811-kernelsize)
- [MPSCNNCrossChannelNormalizationGradient](/documentation/metalperformanceshaders/mpscnncrosschannelnormalizationgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnncrosschannelnormalizationgradient/2942476-init)
- [init(device: any MTLDevice, kernelSize: Int)](/documentation/metalperformanceshaders/mpscnncrosschannelnormalizationgradient/2942463-init)

#### Instance Properties

- [var alpha: Float](/documentation/metalperformanceshaders/mpscnncrosschannelnormalizationgradient/2942464-alpha)
- [var beta: Float](/documentation/metalperformanceshaders/mpscnncrosschannelnormalizationgradient/2942477-beta)
- [var delta: Float](/documentation/metalperformanceshaders/mpscnncrosschannelnormalizationgradient/2942465-delta)
- [var kernelSize: Int](/documentation/metalperformanceshaders/mpscnncrosschannelnormalizationgradient/2942468-kernelsize)
- [MPSCNNLocalContrastNormalization](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalization)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalization/2867185-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int)](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalization/1648924-init)

#### Instance Properties

- [var alpha: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalization/1648923-alpha)
- [var beta: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalization/1648905-beta)
- [var delta: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalization/1648812-delta)
- [var p0: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalization/1648953-p0)
- [var pm: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalization/1648907-pm)
- [var ps: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalization/1648942-ps)
- [MPSCNNLocalContrastNormalizationGradient](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradient/2942467-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int)](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradient/2942462-init)

#### Instance Properties

- [var alpha: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradient/2942471-alpha)
- [var beta: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradient/2942484-beta)
- [var delta: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradient/2942482-delta)
- [var p0: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradient/2942472-p0)
- [var pm: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradient/2942485-pm)
- [var ps: Float](/documentation/metalperformanceshaders/mpscnnlocalcontrastnormalizationgradient/2942466-ps)
- [MPSCNNSpatialNormalization](/documentation/metalperformanceshaders/mpscnnspatialnormalization)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnspatialnormalization/2867021-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int)](/documentation/metalperformanceshaders/mpscnnspatialnormalization/1648831-init)

#### Instance Properties

- [var alpha: Float](/documentation/metalperformanceshaders/mpscnnspatialnormalization/1648825-alpha)
- [var beta: Float](/documentation/metalperformanceshaders/mpscnnspatialnormalization/1648936-beta)
- [var delta: Float](/documentation/metalperformanceshaders/mpscnnspatialnormalization/1648933-delta)
- [MPSCNNSpatialNormalizationGradient](/documentation/metalperformanceshaders/mpscnnspatialnormalizationgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnspatialnormalizationgradient/2942473-init)
- [init(device: any MTLDevice, kernelWidth: Int, kernelHeight: Int)](/documentation/metalperformanceshaders/mpscnnspatialnormalizationgradient/2942461-init)

#### Instance Properties

- [var alpha: Float](/documentation/metalperformanceshaders/mpscnnspatialnormalizationgradient/2942478-alpha)
- [var beta: Float](/documentation/metalperformanceshaders/mpscnnspatialnormalizationgradient/2942470-beta)
- [var delta: Float](/documentation/metalperformanceshaders/mpscnnspatialnormalizationgradient/2942486-delta)
- [MPSCNNBatchNormalization](/documentation/metalperformanceshaders/mpscnnbatchnormalization)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnbatchnormalization/2942602-init)
- [init(device: any MTLDevice, dataSource: any MPSCNNBatchNormalizationDataSource)](/documentation/metalperformanceshaders/mpscnnbatchnormalization/2942600-init)
- [init(device: any MTLDevice, dataSource: any MPSCNNBatchNormalizationDataSource, fusedNeuronDescriptor: MPSNNNeuronDescriptor?)](/documentation/metalperformanceshaders/mpscnnbatchnormalization/3013771-init)

#### Instance Properties

- [var dataSource: any MPSCNNBatchNormalizationDataSource](/documentation/metalperformanceshaders/mpscnnbatchnormalization/2953967-datasource)
- [var epsilon: Float](/documentation/metalperformanceshaders/mpscnnbatchnormalization/2942599-epsilon)
- [var numberOfFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnbatchnormalization/2942604-numberoffeaturechannels)

#### Instance Methods

- [func encode(to: any MTLCommandBuffer, sourceImage: MPSImage, batchNormalizationState: MPSCNNBatchNormalizationState, destinationImage: MPSImage)](/documentation/metalperformanceshaders/mpscnnbatchnormalization/2942591-encode)
- [func encodeBatch(to: any MTLCommandBuffer, sourceImages: [MPSImage], batchNormalizationState: MPSCNNBatchNormalizationState, destinationImages: [MPSImage])](/documentation/metalperformanceshaders/mpscnnbatchnormalization/2942610-encodebatch)
- [func reloadDataSource(any MPSCNNBatchNormalizationDataSource)](/documentation/metalperformanceshaders/mpscnnbatchnormalization/2942609-reloaddatasource)
- [func reloadGammaAndBeta(with: any MTLCommandBuffer, gammaAndBetaState: MPSCNNNormalizationGammaAndBetaState)](/documentation/metalperformanceshaders/mpscnnbatchnormalization/2953965-reloadgammaandbeta)
- [func reloadGammaAndBetaFromDataSource()](/documentation/metalperformanceshaders/mpscnnbatchnormalization/2976464-reloadgammaandbetafromdatasource)
- [func reloadMeanAndVariance(with: any MTLCommandBuffer, meanAndVarianceState: MPSCNNNormalizationMeanAndVarianceState)](/documentation/metalperformanceshaders/mpscnnbatchnormalization/3002359-reloadmeanandvariance)
- [func reloadMeanAndVarianceFromDataSource()](/documentation/metalperformanceshaders/mpscnnbatchnormalization/3002358-reloadmeanandvariancefromdatasou)
- [func resultState(sourceImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSCNNBatchNormalizationState?](/documentation/metalperformanceshaders/mpscnnbatchnormalization/2954874-resultstate)
- [func temporaryResultState(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSCNNBatchNormalizationState?](/documentation/metalperformanceshaders/mpscnnbatchnormalization/2954875-temporaryresultstate)
- [MPSCNNBatchNormalizationGradient](/documentation/metalperformanceshaders/mpscnnbatchnormalizationgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnbatchnormalizationgradient/3019331-init)
- [init(device: any MTLDevice, fusedNeuronDescriptor: MPSNNNeuronDescriptor?)](/documentation/metalperformanceshaders/mpscnnbatchnormalizationgradient/3019332-init)

#### Instance Methods

- [func encode(to: any MTLCommandBuffer, sourceGradient: MPSImage, sourceImage: MPSImage, batchNormalizationState: MPSCNNBatchNormalizationState) -> MPSImage](/documentation/metalperformanceshaders/mpscnnbatchnormalizationgradient/2951885-encode)
- [func encode(to: any MTLCommandBuffer, sourceGradient: MPSImage, sourceImage: MPSImage, batchNormalizationState: MPSCNNBatchNormalizationState, destinationGradient: MPSImage)](/documentation/metalperformanceshaders/mpscnnbatchnormalizationgradient/2951895-encode)
- [func encodeBatch(to: any MTLCommandBuffer, sourceGradients: [MPSImage], sourceImages: [MPSImage], batchNormalizationState: MPSCNNBatchNormalizationState) -> [MPSImage]](/documentation/metalperformanceshaders/mpscnnbatchnormalizationgradient/2942590-encodebatch)
- [func encodeBatch(to: any MTLCommandBuffer, sourceGradients: [MPSImage], sourceImages: [MPSImage], batchNormalizationState: MPSCNNBatchNormalizationState, destinationGradients: [MPSImage])](/documentation/metalperformanceshaders/mpscnnbatchnormalizationgradient/2942608-encodebatch)
- [MPSCNNBatchNormalizationState](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstate)

#### Instance Properties

- [var batchNormalization: MPSCNNBatchNormalization](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstate/2953969-batchnormalization)

#### Instance Methods

- [func beta() -> (any MTLBuffer)?](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstate/2951888-beta)
- [func gamma() -> (any MTLBuffer)?](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstate/2951892-gamma)
- [func gradientForBeta() -> (any MTLBuffer)?](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstate/2951890-gradientforbeta)
- [func gradientForGamma() -> (any MTLBuffer)?](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstate/2951893-gradientforgamma)
- [func mean() -> (any MTLBuffer)?](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstate/2942612-mean)
- [func reset()](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstate/2942587-reset)
- [func variance() -> (any MTLBuffer)?](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstate/2942603-variance)
- [MPSCNNNormalizationMeanAndVarianceState](/documentation/metalperformanceshaders/mpscnnnormalizationmeanandvariancestate)

#### Initializers

- [init(mean: any MTLBuffer, variance: any MTLBuffer)](/documentation/metalperformanceshaders/mpscnnnormalizationmeanandvariancestate/3002363-init)

#### Instance Properties

- [var mean: any MTLBuffer](/documentation/metalperformanceshaders/mpscnnnormalizationmeanandvariancestate/3002364-mean)
- [var variance: any MTLBuffer](/documentation/metalperformanceshaders/mpscnnnormalizationmeanandvariancestate/3002366-variance)

#### Type Methods

- [class func temporaryState(with: any MTLCommandBuffer, numberOfFeatureChannels: Int) -> Self](/documentation/metalperformanceshaders/mpscnnnormalizationmeanandvariancestate/3002365-temporarystate)
- [MPSCNNBatchNormalizationStatistics](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstatistics)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstatistics/2942578-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstatistics/2953968-init)

#### Instance Methods

- [func encodeBatch(to: any MTLCommandBuffer, sourceImages: [MPSImage], batchNormalizationState: MPSCNNBatchNormalizationState)](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstatistics/2942584-encodebatch)
- [MPSCNNBatchNormalizationStatisticsGradient](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstatisticsgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstatisticsgradient/3013774-init)
- [init(device: any MTLDevice, fusedNeuronDescriptor: MPSNNNeuronDescriptor?)](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstatisticsgradient/3013775-init)

#### Instance Methods

- [func encodeBatch(to: any MTLCommandBuffer, sourceGradients: [MPSImage], sourceImages: [MPSImage], batchNormalizationState: MPSCNNBatchNormalizationState)](/documentation/metalperformanceshaders/mpscnnbatchnormalizationstatisticsgradient/2953964-encodebatch)
- [MPSCNNInstanceNormalization](/documentation/metalperformanceshaders/mpscnninstancenormalization)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnninstancenormalization/2947948-init)
- [init(device: any MTLDevice, dataSource: any MPSCNNInstanceNormalizationDataSource)](/documentation/metalperformanceshaders/mpscnninstancenormalization/2947947-init)

#### Instance Properties

- [var dataSource: any MPSCNNInstanceNormalizationDataSource](/documentation/metalperformanceshaders/mpscnninstancenormalization/2953927-datasource)
- [var epsilon: Float](/documentation/metalperformanceshaders/mpscnninstancenormalization/2947943-epsilon)

#### Instance Methods

- [func reloadDataSource(any MPSCNNInstanceNormalizationDataSource)](/documentation/metalperformanceshaders/mpscnninstancenormalization/2947958-reloaddatasource)
- [func reloadGammaAndBeta(with: any MTLCommandBuffer, gammaAndBetaState: MPSCNNNormalizationGammaAndBetaState)](/documentation/metalperformanceshaders/mpscnninstancenormalization/2953921-reloadgammaandbeta)
- [func reloadGammaAndBetaFromDataSource()](/documentation/metalperformanceshaders/mpscnninstancenormalization/2976471-reloadgammaandbetafromdatasource)
- [func resultState(sourceImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSCNNInstanceNormalizationGradientState?](/documentation/metalperformanceshaders/mpscnninstancenormalization/2947959-resultstate)
- [func temporaryResultState(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSCNNInstanceNormalizationGradientState?](/documentation/metalperformanceshaders/mpscnninstancenormalization/2956160-temporaryresultstate)
- [MPSCNNInstanceNormalizationGradient](/documentation/metalperformanceshaders/mpscnninstancenormalizationgradient)
- [MPSCNNInstanceNormalizationGradientState](/documentation/metalperformanceshaders/mpscnninstancenormalizationgradientstate)

#### Instance Properties

- [var beta: (any MTLBuffer)?](/documentation/metalperformanceshaders/mpscnninstancenormalizationgradientstate/2956162-beta)
- [var gamma: (any MTLBuffer)?](/documentation/metalperformanceshaders/mpscnninstancenormalizationgradientstate/2956161-gamma)
- [var gradientForBeta: any MTLBuffer](/documentation/metalperformanceshaders/mpscnninstancenormalizationgradientstate/2953930-gradientforbeta)
- [var gradientForGamma: any MTLBuffer](/documentation/metalperformanceshaders/mpscnninstancenormalizationgradientstate/2953928-gradientforgamma)
- [var instanceNormalization: MPSCNNInstanceNormalization](/documentation/metalperformanceshaders/mpscnninstancenormalizationgradientstate/2953924-instancenormalization)
- [MPSCNNNormalizationGammaAndBetaState](/documentation/metalperformanceshaders/mpscnnnormalizationgammaandbetastate)

#### Initializers

- [init(gamma: any MTLBuffer, beta: any MTLBuffer)](/documentation/metalperformanceshaders/mpscnnnormalizationgammaandbetastate/2953936-init)

#### Instance Properties

- [var beta: any MTLBuffer](/documentation/metalperformanceshaders/mpscnnnormalizationgammaandbetastate/2953938-beta)
- [var gamma: any MTLBuffer](/documentation/metalperformanceshaders/mpscnnnormalizationgammaandbetastate/2953934-gamma)

#### Type Methods

- [class func temporaryState(with: any MTLCommandBuffer, numberOfFeatureChannels: Int) -> Self](/documentation/metalperformanceshaders/mpscnnnormalizationgammaandbetastate/2953937-temporarystate)

### Upsampling Layers

- [MPSCNNUpsampling](/documentation/metalperformanceshaders/mpscnnupsampling)

#### Instance Properties

- [var scaleFactorX: Double](/documentation/metalperformanceshaders/mpscnnupsampling/2875206-scalefactorx)
- [var scaleFactorY: Double](/documentation/metalperformanceshaders/mpscnnupsampling/2875154-scalefactory)
- [var alignCorners: Bool](/documentation/metalperformanceshaders/mpscnnupsampling/2966660-aligncorners)
- [MPSCNNUpsamplingBilinear](/documentation/metalperformanceshaders/mpscnnupsamplingbilinear)

#### Initializers

- [init(device: any MTLDevice, integerScaleFactorX: Int, integerScaleFactorY: Int)](/documentation/metalperformanceshaders/mpscnnupsamplingbilinear/2875160-init)
- [init(device: any MTLDevice, integerScaleFactorX: Int, integerScaleFactorY: Int, alignCorners: Bool)](/documentation/metalperformanceshaders/mpscnnupsamplingbilinear/2966661-init)
- [MPSCNNUpsamplingNearest](/documentation/metalperformanceshaders/mpscnnupsamplingnearest)

#### Initializers

- [init(device: any MTLDevice, integerScaleFactorX: Int, integerScaleFactorY: Int)](/documentation/metalperformanceshaders/mpscnnupsamplingnearest/2875223-init)
- [MPSCNNUpsamplingBilinearGradient](/documentation/metalperformanceshaders/mpscnnupsamplingbilineargradient)

#### Initializers

- [init(device: any MTLDevice, integerScaleFactorX: Int, integerScaleFactorY: Int)](/documentation/metalperformanceshaders/mpscnnupsamplingbilineargradient/2947918-init)
- [MPSCNNUpsamplingGradient](/documentation/metalperformanceshaders/mpscnnupsamplinggradient)

#### Instance Properties

- [var scaleFactorX: Double](/documentation/metalperformanceshaders/mpscnnupsamplinggradient/2942630-scalefactorx)
- [var scaleFactorY: Double](/documentation/metalperformanceshaders/mpscnnupsamplinggradient/2942628-scalefactory)
- [MPSCNNUpsamplingNearestGradient](/documentation/metalperformanceshaders/mpscnnupsamplingnearestgradient)

#### Initializers

- [init(device: any MTLDevice, integerScaleFactorX: Int, integerScaleFactorY: Int)](/documentation/metalperformanceshaders/mpscnnupsamplingnearestgradient/2947920-init)

### Dropout Layers

- [MPSCNNDropout](/documentation/metalperformanceshaders/mpscnndropout)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnndropout/2942514-init)
- [init(device: any MTLDevice, keepProbability: Float, seed: Int, maskStrideInPixels: MTLSize)](/documentation/metalperformanceshaders/mpscnndropout/2942522-init)

#### Instance Properties

- [var keepProbability: Float](/documentation/metalperformanceshaders/mpscnndropout/2942524-keepprobability)
- [var maskStrideInPixels: MTLSize](/documentation/metalperformanceshaders/mpscnndropout/2942519-maskstrideinpixels)
- [var seed: Int](/documentation/metalperformanceshaders/mpscnndropout/2942517-seed)

#### Instance Methods

- [func resultState(sourceImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSCNNDropoutGradientState?](/documentation/metalperformanceshaders/mpscnndropout/3131793-resultstate)
- [func resultStateBatch(sourceImage: [MPSImage], sourceStates: [[MPSState]]?, destinationImage: [MPSImage]) -> MPSCNNDropoutGradientState?](/documentation/metalperformanceshaders/mpscnndropout/3131792-resultstatebatch)
- [func temporaryResultState(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSCNNDropoutGradientState?](/documentation/metalperformanceshaders/mpscnndropout/3131795-temporaryresultstate)
- [func temporaryResultStateBatch(commandBuffer: any MTLCommandBuffer, sourceImage: [MPSImage], sourceStates: [[MPSState]]?, destinationImage: [MPSImage]) -> [MPSCNNDropoutGradientState]?](/documentation/metalperformanceshaders/mpscnndropout/3131794-temporaryresultstatebatch)
- [MPSCNNDropoutGradient](/documentation/metalperformanceshaders/mpscnndropoutgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnndropoutgradient/2942521-init)
- [init(device: any MTLDevice, keepProbability: Float, seed: Int, maskStrideInPixels: MTLSize)](/documentation/metalperformanceshaders/mpscnndropoutgradient/2942518-init)

#### Instance Properties

- [var keepProbability: Float](/documentation/metalperformanceshaders/mpscnndropoutgradient/2942520-keepprobability)
- [var maskStrideInPixels: MTLSize](/documentation/metalperformanceshaders/mpscnndropoutgradient/2942515-maskstrideinpixels)
- [var seed: Int](/documentation/metalperformanceshaders/mpscnndropoutgradient/2942528-seed)
- [MPSCNNDropoutGradientState](/documentation/metalperformanceshaders/mpscnndropoutgradientstate)

#### Instance Methods

- [func maskData() -> Data](/documentation/metalperformanceshaders/mpscnndropoutgradientstate/2942527-maskdata)

### Loss Layers

- [MPSCNNLoss](/documentation/metalperformanceshaders/mpscnnloss)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnloss/2942379-init)
- [init(device: any MTLDevice, lossDescriptor: MPSCNNLossDescriptor)](/documentation/metalperformanceshaders/mpscnnloss/2942377-init)

#### Instance Properties

- [var delta: Float](/documentation/metalperformanceshaders/mpscnnloss/2942360-delta)
- [var epsilon: Float](/documentation/metalperformanceshaders/mpscnnloss/2942371-epsilon)
- [var labelSmoothing: Float](/documentation/metalperformanceshaders/mpscnnloss/2942358-labelsmoothing)
- [var lossType: MPSCNNLossType](/documentation/metalperformanceshaders/mpscnnloss/2942359-losstype)
- [var numberOfClasses: Int](/documentation/metalperformanceshaders/mpscnnloss/2942389-numberofclasses)
- [var reduceAcrossBatch: Bool](/documentation/metalperformanceshaders/mpscnnloss/3547981-reduceacrossbatch)
- [var reductionType: MPSCNNReductionType](/documentation/metalperformanceshaders/mpscnnloss/2942365-reductiontype)
- [var weight: Float](/documentation/metalperformanceshaders/mpscnnloss/2942387-weight)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, labels: MPSCNNLossLabels) -> MPSImage](/documentation/metalperformanceshaders/mpscnnloss/2951838-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, labels: MPSCNNLossLabels, destinationImage: MPSImage)](/documentation/metalperformanceshaders/mpscnnloss/2951843-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], labels: [MPSCNNLossLabels]) -> [MPSImage]](/documentation/metalperformanceshaders/mpscnnloss/2951839-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], labels: [MPSCNNLossLabels], destinationImages: [MPSImage])](/documentation/metalperformanceshaders/mpscnnloss/2951846-encode)
- [MPSCNNLossDataDescriptor](/documentation/metalperformanceshaders/mpscnnlossdatadescriptor)

#### Initializers

- [init?(data: Data, layout: MPSDataLayout, size: MTLSize)](/documentation/metalperformanceshaders/mpscnnlossdatadescriptor/2951840-init)

#### Instance Properties

- [var bytesPerImage: Int](/documentation/metalperformanceshaders/mpscnnlossdatadescriptor/2951847-bytesperimage)
- [var bytesPerRow: Int](/documentation/metalperformanceshaders/mpscnnlossdatadescriptor/2951849-bytesperrow)
- [var layout: MPSDataLayout](/documentation/metalperformanceshaders/mpscnnlossdatadescriptor/2951842-layout)
- [var size: MTLSize](/documentation/metalperformanceshaders/mpscnnlossdatadescriptor/2951848-size)
- [MPSCNNLossDescriptor](/documentation/metalperformanceshaders/mpscnnlossdescriptor)

#### Initializers

- [init(type: MPSCNNLossType, reductionType: MPSCNNReductionType)](/documentation/metalperformanceshaders/mpscnnlossdescriptor/2942373-init)

#### Instance Properties

- [var delta: Float](/documentation/metalperformanceshaders/mpscnnlossdescriptor/2942378-delta)
- [var epsilon: Float](/documentation/metalperformanceshaders/mpscnnlossdescriptor/2942362-epsilon)
- [var labelSmoothing: Float](/documentation/metalperformanceshaders/mpscnnlossdescriptor/2942369-labelsmoothing)
- [var lossType: MPSCNNLossType](/documentation/metalperformanceshaders/mpscnnlossdescriptor/2942381-losstype)
- [var numberOfClasses: Int](/documentation/metalperformanceshaders/mpscnnlossdescriptor/2942382-numberofclasses)
- [var reduceAcrossBatch: Bool](/documentation/metalperformanceshaders/mpscnnlossdescriptor/3547982-reduceacrossbatch)
- [var reductionType: MPSCNNReductionType](/documentation/metalperformanceshaders/mpscnnlossdescriptor/2942388-reductiontype)
- [var weight: Float](/documentation/metalperformanceshaders/mpscnnlossdescriptor/2942367-weight)
- [MPSCNNLossLabels](/documentation/metalperformanceshaders/mpscnnlosslabels)

#### Initializers

- [init(device: any MTLDevice, labelsDescriptor: MPSCNNLossDataDescriptor)](/documentation/metalperformanceshaders/mpscnnlosslabels/2951850-init)
- [init(device: any MTLDevice, lossImageSize: MTLSize, labelsDescriptor: MPSCNNLossDataDescriptor, weightsDescriptor: MPSCNNLossDataDescriptor?)](/documentation/metalperformanceshaders/mpscnnlosslabels/2951841-init)
- [init(device: any MTLDevice, lossImageSize: MTLSize, labelsImage: MPSImage, weightsImage: MPSImage?)](/documentation/metalperformanceshaders/mpscnnlosslabels/3114086-init)

#### Instance Methods

- [func labelsImage() -> MPSImage](/documentation/metalperformanceshaders/mpscnnlosslabels/2976472-labelsimage)
- [func lossImage() -> MPSImage](/documentation/metalperformanceshaders/mpscnnlosslabels/2951845-lossimage)
- [func weightsImage() -> MPSImage](/documentation/metalperformanceshaders/mpscnnlosslabels/2976473-weightsimage)
- [MPSCNNYOLOLoss](/documentation/metalperformanceshaders/mpscnnyololoss)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnyololoss/2976480-init)
- [init(device: any MTLDevice, lossDescriptor: MPSCNNYOLOLossDescriptor)](/documentation/metalperformanceshaders/mpscnnyololoss/2976481-init)

#### Instance Properties

- [var anchorBoxes: Data](/documentation/metalperformanceshaders/mpscnnyololoss/2976475-anchorboxes)
- [var lossClasses: MPSCNNLoss](/documentation/metalperformanceshaders/mpscnnyololoss/2976482-lossclasses)
- [var lossConfidence: MPSCNNLoss](/documentation/metalperformanceshaders/mpscnnyololoss/2976483-lossconfidence)
- [var lossWH: MPSCNNLoss](/documentation/metalperformanceshaders/mpscnnyololoss/2976484-losswh)
- [var lossXY: MPSCNNLoss](/documentation/metalperformanceshaders/mpscnnyololoss/2976485-lossxy)
- [var maxIOUForObjectAbsence: Float](/documentation/metalperformanceshaders/mpscnnyololoss/2976486-maxiouforobjectabsence)
- [var minIOUForObjectPresence: Float](/documentation/metalperformanceshaders/mpscnnyololoss/2976487-miniouforobjectpresence)
- [var numberOfAnchorBoxes: Int](/documentation/metalperformanceshaders/mpscnnyololoss/2976488-numberofanchorboxes)
- [var reduceAcrossBatch: Bool](/documentation/metalperformanceshaders/mpscnnyololoss/3547983-reduceacrossbatch)
- [var reductionType: MPSCNNReductionType](/documentation/metalperformanceshaders/mpscnnyololoss/2976489-reductiontype)
- [var scaleClass: Float](/documentation/metalperformanceshaders/mpscnnyololoss/2976490-scaleclass)
- [var scaleNoObject: Float](/documentation/metalperformanceshaders/mpscnnyololoss/2976491-scalenoobject)
- [var scaleObject: Float](/documentation/metalperformanceshaders/mpscnnyololoss/2976492-scaleobject)
- [var scaleWH: Float](/documentation/metalperformanceshaders/mpscnnyololoss/2976493-scalewh)
- [var scaleXY: Float](/documentation/metalperformanceshaders/mpscnnyololoss/2976494-scalexy)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, labels: MPSCNNLossLabels) -> MPSImage](/documentation/metalperformanceshaders/mpscnnyololoss/2976478-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, labels: MPSCNNLossLabels, destinationImage: MPSImage)](/documentation/metalperformanceshaders/mpscnnyololoss/2976479-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], labels: [MPSCNNLossLabels]) -> [MPSImage]](/documentation/metalperformanceshaders/mpscnnyololoss/2976476-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], labels: [MPSCNNLossLabels], destinationImages: [MPSImage])](/documentation/metalperformanceshaders/mpscnnyololoss/2976477-encode)
- [MPSCNNYOLOLossDescriptor](/documentation/metalperformanceshaders/mpscnnyololossdescriptor)

#### Instance Properties

- [var anchorBoxes: Data](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976498-anchorboxes)
- [var classesLossDescriptor: MPSCNNLossDescriptor](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976499-classeslossdescriptor)
- [var confidenceLossDescriptor: MPSCNNLossDescriptor](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976501-confidencelossdescriptor)
- [var maxIOUForObjectAbsence: Float](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976502-maxiouforobjectabsence)
- [var minIOUForObjectPresence: Float](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976503-miniouforobjectpresence)
- [var numberOfAnchorBoxes: Int](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976504-numberofanchorboxes)
- [var reduceAcrossBatch: Bool](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/3547984-reduceacrossbatch)
- [var reductionType: MPSCNNReductionType](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976505-reductiontype)
- [var rescore: Bool](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976506-rescore)
- [var scaleClass: Float](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976507-scaleclass)
- [var scaleNoObject: Float](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976508-scalenoobject)
- [var scaleObject: Float](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976509-scaleobject)
- [var scaleWH: Float](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976510-scalewh)
- [var scaleXY: Float](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976511-scalexy)
- [var whLossDescriptor: MPSCNNLossDescriptor](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976496-whlossdescriptor)
- [var xyLossDescriptor: MPSCNNLossDescriptor](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976497-xylossdescriptor)

#### Type Methods

- [class func cnnLossDescriptor(withXYLossType: MPSCNNLossType, whLossType: MPSCNNLossType, confidenceLossType: MPSCNNLossType, classesLossType: MPSCNNLossType, reductionType: MPSCNNReductionType, anchorBoxes: Data, numberOfAnchorBoxes: Int) -> MPSCNNYOLOLossDescriptor](/documentation/metalperformanceshaders/mpscnnyololossdescriptor/2976500-cnnlossdescriptor)

### Reduction Layers

- [MPSNNReduceRowMax](/documentation/metalperformanceshaders/mpsnnreducerowmax)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducerowmax/3197842-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducerowmax/2942559-init)
- [MPSNNReduceRowMin](/documentation/metalperformanceshaders/mpsnnreducerowmin)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducerowmin/3197844-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducerowmin/2942555-init)
- [MPSNNReduceRowSum](/documentation/metalperformanceshaders/mpsnnreducerowsum)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducerowsum/3197845-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducerowsum/2942536-init)
- [MPSNNReduceRowMean](/documentation/metalperformanceshaders/mpsnnreducerowmean)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducerowmean/3197843-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducerowmean/2942548-init)
- [MPSNNReduceColumnMax](/documentation/metalperformanceshaders/mpsnnreducecolumnmax)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducecolumnmax/3197830-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducecolumnmax/2942541-init)
- [MPSNNReduceColumnMin](/documentation/metalperformanceshaders/mpsnnreducecolumnmin)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducecolumnmin/3197832-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducecolumnmin/2942542-init)
- [MPSNNReduceColumnSum](/documentation/metalperformanceshaders/mpsnnreducecolumnsum)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducecolumnsum/3197833-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducecolumnsum/2942540-init)
- [MPSNNReduceColumnMean](/documentation/metalperformanceshaders/mpsnnreducecolumnmean)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducecolumnmean/3197831-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducecolumnmean/2942546-init)
- [MPSNNReduceFeatureChannelsMax](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsmax)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsmax/3197838-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsmax/2942532-init)
- [MPSNNReduceFeatureChannelsMin](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsmin)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsmin/3197840-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsmin/2942565-init)
- [MPSNNReduceFeatureChannelsSum](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelssum)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelssum/3197841-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelssum/2942538-init)

#### Instance Properties

- [var weight: Float](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelssum/2942545-weight)
- [MPSNNReduceFeatureChannelsMean](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsmean)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsmean/3197839-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsmean/2942557-init)
- [MPSNNReduceFeatureChannelsArgumentMax](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsargumentmax)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsargumentmax/3197836-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsargumentmax/2976518-init)
- [MPSNNReduceFeatureChannelsArgumentMin](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsargumentmin)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsargumentmin/3197837-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsargumentmin/2976520-init)
- [MPSNNReduceFeatureChannelsAndWeightsSum](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsandweightssum)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsandweightssum/3197835-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsandweightssum/2942562-init)
- [init(device: any MTLDevice, doWeightedSumByNonZeroWeights: Bool)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsandweightssum/2942551-init)

#### Instance Properties

- [var doWeightedSumByNonZeroWeights: Bool](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsandweightssum/2942543-doweightedsumbynonzeroweights)
- [MPSNNReduceFeatureChannelsAndWeightsMean](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsandweightsmean)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsandweightsmean/3197834-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreducefeaturechannelsandweightsmean/2942537-init)
- [MPSNNReduceUnary](/documentation/metalperformanceshaders/mpsnnreduceunary)

#### Instance Properties

- [var clipRectSource: MTLRegion](/documentation/metalperformanceshaders/mpsnnreduceunary/2942547-cliprectsource)
- [var offset: MPSOffset](/documentation/metalperformanceshaders/mpsnnreduceunary/3750642-offset)
- [MPSNNReduceBinary](/documentation/metalperformanceshaders/mpsnnreducebinary)

#### Instance Properties

- [var primaryOffset: MPSOffset](/documentation/metalperformanceshaders/mpsnnreducebinary/3750640-primaryoffset)
- [var primarySourceClipRect: MTLRegion](/documentation/metalperformanceshaders/mpsnnreducebinary/2942561-primarysourcecliprect)
- [var secondaryOffset: MPSOffset](/documentation/metalperformanceshaders/mpsnnreducebinary/3750641-secondaryoffset)
- [var secondarySourceClipRect: MTLRegion](/documentation/metalperformanceshaders/mpsnnreducebinary/2942556-secondarysourcecliprect)

### Reshape Layer

- [MPSNNReshape](/documentation/metalperformanceshaders/mpsnnreshape)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreshape/2951930-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreshape/2951929-init)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, destinationState: AutoreleasingUnsafeMutablePointer<MPSState?>, destinationStateIsTemporary: Bool, reshapedWidth: Int, reshapedHeight: Int, reshapedFeatureChannels: Int) -> MPSImage](/documentation/metalperformanceshaders/mpsnnreshape/3547991-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, reshapedWidth: Int, reshapedHeight: Int, reshapedFeatureChannels: Int) -> MPSImage](/documentation/metalperformanceshaders/mpsnnreshape/3547992-encode)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], destinationStates: AutoreleasingUnsafeMutablePointer<NSArray?>, destinationStateIsTemporary: Bool, reshapedWidth: Int, reshapedHeight: Int, reshapedFeatureChannels: Int) -> [MPSImage]](/documentation/metalperformanceshaders/mpsnnreshape/3547989-encodebatch)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], reshapedWidth: Int, reshapedHeight: Int, reshapedFeatureChannels: Int) -> [MPSImage]](/documentation/metalperformanceshaders/mpsnnreshape/3547990-encodebatch)

### Slice Layer

- [MPSNNSlice](/documentation/metalperformanceshaders/mpsnnslice)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnslice/2942403-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnslice/2942401-init)

### Optimization Layers

- [MPSNNOptimizerAdam](/documentation/metalperformanceshaders/mpsnnoptimizeradam)

#### Initializers

- [init(device: any MTLDevice, beta1: Double, beta2: Double, epsilon: Float, timeStep: Int, optimizerDescriptor: MPSNNOptimizerDescriptor)](/documentation/metalperformanceshaders/mpsnnoptimizeradam/2966718-init)
- [init(device: any MTLDevice, learningRate: Float)](/documentation/metalperformanceshaders/mpsnnoptimizeradam/2966719-init)

#### Instance Properties

- [var beta1: Double](/documentation/metalperformanceshaders/mpsnnoptimizeradam/2966714-beta1)
- [var beta2: Double](/documentation/metalperformanceshaders/mpsnnoptimizeradam/2966715-beta2)
- [var epsilon: Float](/documentation/metalperformanceshaders/mpsnnoptimizeradam/2966717-epsilon)
- [var timeStep: Int](/documentation/metalperformanceshaders/mpsnnoptimizeradam/2966720-timestep)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, batchNormalizationGradientState: MPSCNNBatchNormalizationState, batchNormalizationSourceState: MPSCNNBatchNormalizationState, inputMomentumVectors: [MPSVector], inputVelocityVectors: [MPSVector], maximumVelocityVectors: [MPSVector]?, resultState: MPSCNNNormalizationGammaAndBetaState)](/documentation/metalperformanceshaders/mpsnnoptimizeradam/3175013-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, batchNormalizationGradientState: MPSCNNBatchNormalizationState, batchNormalizationSourceState: MPSCNNBatchNormalizationState, inputMomentumVectors: [MPSVector]?, inputVelocityVectors: [MPSVector]?, resultState: MPSCNNNormalizationGammaAndBetaState)](/documentation/metalperformanceshaders/mpsnnoptimizeradam/3013781-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, batchNormalizationState: MPSCNNBatchNormalizationState, inputMomentumVectors: [MPSVector], inputVelocityVectors: [MPSVector], maximumVelocityVectors: [MPSVector]?, resultState: MPSCNNNormalizationGammaAndBetaState)](/documentation/metalperformanceshaders/mpsnnoptimizeradam/3175014-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, batchNormalizationState: MPSCNNBatchNormalizationState, inputMomentumVectors: [MPSVector]?, inputVelocityVectors: [MPSVector]?, resultState: MPSCNNNormalizationGammaAndBetaState)](/documentation/metalperformanceshaders/mpsnnoptimizeradam/3019334-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, convolutionGradientState: MPSCNNConvolutionGradientState, convolutionSourceState: MPSCNNConvolutionWeightsAndBiasesState, inputMomentumVectors: [MPSVector], inputVelocityVectors: [MPSVector], maximumVelocityVectors: [MPSVector]?, resultState: MPSCNNConvolutionWeightsAndBiasesState)](/documentation/metalperformanceshaders/mpsnnoptimizeradam/3175015-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, convolutionGradientState: MPSCNNConvolutionGradientState, convolutionSourceState: MPSCNNConvolutionWeightsAndBiasesState, inputMomentumVectors: [MPSVector]?, inputVelocityVectors: [MPSVector]?, resultState: MPSCNNConvolutionWeightsAndBiasesState)](/documentation/metalperformanceshaders/mpsnnoptimizeradam/3013782-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, inputGradientMatrix: MPSMatrix, inputValuesMatrix: MPSMatrix, inputMomentumMatrix: MPSMatrix, inputVelocityMatrix: MPSMatrix, maximumVelocityMatrix: MPSMatrix?, resultValuesMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsnnoptimizeradam/3197825-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, inputGradientMatrix: MPSMatrix, inputValuesMatrix: MPSMatrix, inputMomentumMatrix: MPSMatrix, inputVelocityMatrix: MPSMatrix, resultValuesMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsnnoptimizeradam/3197826-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, inputGradientVector: MPSVector, inputValuesVector: MPSVector, inputMomentumVector: MPSVector, inputVelocityVector: MPSVector, maximumVelocityVector: MPSVector?, resultValuesVector: MPSVector)](/documentation/metalperformanceshaders/mpsnnoptimizeradam/3175016-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, inputGradientVector: MPSVector, inputValuesVector: MPSVector, inputMomentumVector: MPSVector, inputVelocityVector: MPSVector, resultValuesVector: MPSVector)](/documentation/metalperformanceshaders/mpsnnoptimizeradam/2966716-encode)
- [MPSNNOptimizerRMSProp](/documentation/metalperformanceshaders/mpsnnoptimizerrmsprop)

#### Initializers

- [init(device: any MTLDevice, decay: Double, epsilon: Float, optimizerDescriptor: MPSNNOptimizerDescriptor)](/documentation/metalperformanceshaders/mpsnnoptimizerrmsprop/2966737-init)
- [init(device: any MTLDevice, learningRate: Float)](/documentation/metalperformanceshaders/mpsnnoptimizerrmsprop/2966738-init)

#### Instance Properties

- [var decay: Double](/documentation/metalperformanceshaders/mpsnnoptimizerrmsprop/2966734-decay)
- [var epsilon: Float](/documentation/metalperformanceshaders/mpsnnoptimizerrmsprop/2966736-epsilon)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, batchNormalizationGradientState: MPSCNNBatchNormalizationState, batchNormalizationSourceState: MPSCNNBatchNormalizationState, inputSumOfSquaresVectors: [MPSVector]?, resultState: MPSCNNNormalizationGammaAndBetaState)](/documentation/metalperformanceshaders/mpsnnoptimizerrmsprop/3013783-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, batchNormalizationState: MPSCNNBatchNormalizationState, inputSumOfSquaresVectors: [MPSVector]?, resultState: MPSCNNNormalizationGammaAndBetaState)](/documentation/metalperformanceshaders/mpsnnoptimizerrmsprop/3019335-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, convolutionGradientState: MPSCNNConvolutionGradientState, convolutionSourceState: MPSCNNConvolutionWeightsAndBiasesState, inputSumOfSquaresVectors: [MPSVector]?, resultState: MPSCNNConvolutionWeightsAndBiasesState)](/documentation/metalperformanceshaders/mpsnnoptimizerrmsprop/3013784-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, inputGradientMatrix: MPSMatrix, inputValuesMatrix: MPSMatrix, inputSumOfSquaresMatrix: MPSMatrix, resultValuesMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsnnoptimizerrmsprop/3197827-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, inputGradientVector: MPSVector, inputValuesVector: MPSVector, inputSumOfSquaresVector: MPSVector, resultValuesVector: MPSVector)](/documentation/metalperformanceshaders/mpsnnoptimizerrmsprop/2966735-encode)
- [MPSNNOptimizerStochasticGradientDescent](/documentation/metalperformanceshaders/mpsnnoptimizerstochasticgradientdescent)

#### Initializers

- [init(device: any MTLDevice, learningRate: Float)](/documentation/metalperformanceshaders/mpsnnoptimizerstochasticgradientdescent/2966741-init)
- [init(device: any MTLDevice, momentumScale: Float, useNesterovMomentum: Bool, optimizerDescriptor: MPSNNOptimizerDescriptor)](/documentation/metalperformanceshaders/mpsnnoptimizerstochasticgradientdescent/3675591-init)
- [init(device: any MTLDevice, momentumScale: Float, useNestrovMomentum: Bool, optimizerDescriptor: MPSNNOptimizerDescriptor)](/documentation/metalperformanceshaders/mpsnnoptimizerstochasticgradientdescent/2966742-init)

#### Instance Properties

- [var momentumScale: Float](/documentation/metalperformanceshaders/mpsnnoptimizerstochasticgradientdescent/2966743-momentumscale)
- [var useNesterovMomentum: Bool](/documentation/metalperformanceshaders/mpsnnoptimizerstochasticgradientdescent/3675592-usenesterovmomentum)
- [var useNestrovMomentum: Bool](/documentation/metalperformanceshaders/mpsnnoptimizerstochasticgradientdescent/2966744-usenestrovmomentum)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, batchNormalizationGradientState: MPSCNNBatchNormalizationState, batchNormalizationSourceState: MPSCNNBatchNormalizationState, inputMomentumVectors: [MPSVector]?, resultState: MPSCNNNormalizationGammaAndBetaState)](/documentation/metalperformanceshaders/mpsnnoptimizerstochasticgradientdescent/3013785-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, batchNormalizationState: MPSCNNBatchNormalizationState, inputMomentumVectors: [MPSVector]?, resultState: MPSCNNNormalizationGammaAndBetaState)](/documentation/metalperformanceshaders/mpsnnoptimizerstochasticgradientdescent/3019336-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, convolutionGradientState: MPSCNNConvolutionGradientState, convolutionSourceState: MPSCNNConvolutionWeightsAndBiasesState, inputMomentumVectors: [MPSVector]?, resultState: MPSCNNConvolutionWeightsAndBiasesState)](/documentation/metalperformanceshaders/mpsnnoptimizerstochasticgradientdescent/3013786-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, inputGradientMatrix: MPSMatrix, inputValuesMatrix: MPSMatrix, inputMomentumMatrix: MPSMatrix?, resultValuesMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsnnoptimizerstochasticgradientdescent/3197828-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, inputGradientVector: MPSVector, inputValuesVector: MPSVector, inputMomentumVector: MPSVector?, resultValuesVector: MPSVector)](/documentation/metalperformanceshaders/mpsnnoptimizerstochasticgradientdescent/2966740-encode)
- [MPSNNOptimizer](/documentation/metalperformanceshaders/mpsnnoptimizer)

#### Instance Properties

- [var applyGradientClipping: Bool](/documentation/metalperformanceshaders/mpsnnoptimizer/2966705-applygradientclipping)
- [var gradientClipMax: Float](/documentation/metalperformanceshaders/mpsnnoptimizer/2966706-gradientclipmax)
- [var gradientClipMin: Float](/documentation/metalperformanceshaders/mpsnnoptimizer/2966707-gradientclipmin)
- [var gradientRescale: Float](/documentation/metalperformanceshaders/mpsnnoptimizer/2966708-gradientrescale)
- [var learningRate: Float](/documentation/metalperformanceshaders/mpsnnoptimizer/2966709-learningrate)
- [var regularizationScale: Float](/documentation/metalperformanceshaders/mpsnnoptimizer/2966710-regularizationscale)
- [var regularizationType: MPSNNRegularizationType](/documentation/metalperformanceshaders/mpsnnoptimizer/2966711-regularizationtype)

#### Instance Methods

- [func setLearningRate(Float)](/documentation/metalperformanceshaders/mpsnnoptimizer/2966712-setlearningrate)
- [MPSNNOptimizerDescriptor](/documentation/metalperformanceshaders/mpsnnoptimizerdescriptor)

#### Initializers

- [init(learningRate: Float, gradientRescale: Float, applyGradientClipping: Bool, gradientClipMax: Float, gradientClipMin: Float, regularizationType: MPSNNRegularizationType, regularizationScale: Float)](/documentation/metalperformanceshaders/mpsnnoptimizerdescriptor/2966726-init)
- [init(learningRate: Float, gradientRescale: Float, regularizationType: MPSNNRegularizationType, regularizationScale: Float)](/documentation/metalperformanceshaders/mpsnnoptimizerdescriptor/2966727-init)

#### Instance Properties

- [var applyGradientClipping: Bool](/documentation/metalperformanceshaders/mpsnnoptimizerdescriptor/2966722-applygradientclipping)
- [var gradientClipMax: Float](/documentation/metalperformanceshaders/mpsnnoptimizerdescriptor/2966723-gradientclipmax)
- [var gradientClipMin: Float](/documentation/metalperformanceshaders/mpsnnoptimizerdescriptor/2966724-gradientclipmin)
- [var gradientRescale: Float](/documentation/metalperformanceshaders/mpsnnoptimizerdescriptor/2966725-gradientrescale)
- [var learningRate: Float](/documentation/metalperformanceshaders/mpsnnoptimizerdescriptor/2966728-learningrate)
- [var regularizationScale: Float](/documentation/metalperformanceshaders/mpsnnoptimizerdescriptor/2966731-regularizationscale)
- [var regularizationType: MPSNNRegularizationType](/documentation/metalperformanceshaders/mpsnnoptimizerdescriptor/2966732-regularizationtype)

### Layer Base Classes

- [MPSCNNKernel](/documentation/metalperformanceshaders/mpscnnkernel)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnkernel/2865655-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnkernel/2865653-init)

#### Instance Properties

- [var offset: MPSOffset](/documentation/metalperformanceshaders/mpscnnkernel/1648835-offset)
- [MPSOffset](/documentation/metalperformanceshaders/mpsoffset)

##### Initializers

- [init()](/documentation/metalperformanceshaders/mpsoffset/1618896-init)
- [init(x: Int, y: Int, z: Int)](/documentation/metalperformanceshaders/mpsoffset/1618740-init)

##### Instance Properties

- [var x: Int](/documentation/metalperformanceshaders/mpsoffset/1618861-x)
- [var y: Int](/documentation/metalperformanceshaders/mpsoffset/1618846-y)
- [var z: Int](/documentation/metalperformanceshaders/mpsoffset/1618881-z)
- [var clipRect: MTLRegion](/documentation/metalperformanceshaders/mpscnnkernel/1648911-cliprect)
- [MTLRegion](/documentation/metal/mtlregion)
- [var destinationFeatureChannelOffset: Int](/documentation/metalperformanceshaders/mpscnnkernel/2097550-destinationfeaturechanneloffset)
- [var edgeMode: MPSImageEdgeMode](/documentation/metalperformanceshaders/mpscnnkernel/1648826-edgemode)
- [MPSImageEdgeMode](/documentation/metalperformanceshaders/mpsimageedgemode)

##### Constants

- [case zero](/documentation/metalperformanceshaders/mpsimageedgemode/zero)
- [case clamp](/documentation/metalperformanceshaders/mpsimageedgemode/clamp)

##### Enumeration Cases

- [case constant](/documentation/metalperformanceshaders/mpsimageedgemode/constant)
- [case mirror](/documentation/metalperformanceshaders/mpsimageedgemode/mirror)
- [case mirrorWithEdge](/documentation/metalperformanceshaders/mpsimageedgemode/mirrorwithedge)
- [var kernelHeight: Int](/documentation/metalperformanceshaders/mpscnnkernel/2865648-kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshaders/mpscnnkernel/2865637-kernelwidth)
- [var strideInPixelsX: Int](/documentation/metalperformanceshaders/mpscnnkernel/2865654-strideinpixelsx)
- [var strideInPixelsY: Int](/documentation/metalperformanceshaders/mpscnnkernel/2865644-strideinpixelsy)
- [var isBackwards: Bool](/documentation/metalperformanceshaders/mpscnnkernel/2865634-isbackwards)
- [var padding: any MPSNNPadding](/documentation/metalperformanceshaders/mpscnnkernel/2865657-padding)
- [MPSNNPadding](/documentation/metalperformanceshaders/mpsnnpadding)

##### Instance Methods

- [func destinationImageDescriptor(forSourceImages: [MPSImage], sourceStates: [MPSState]?, for: MPSKernel, suggestedDescriptor: MPSImageDescriptor) -> MPSImageDescriptor](/documentation/metalperformanceshaders/mpsnnpadding/2867167-destinationimagedescriptor)
- [MPSImage](/documentation/metalperformanceshaders/mpsimage)

###### Initializers

- [init(device: any MTLDevice, imageDescriptor: MPSImageDescriptor)](/documentation/metalperformanceshaders/mpsimage/1648920-init)
- [MPSImageDescriptor](/documentation/metalperformanceshaders/mpsimagedescriptor)

###### Methods

- [init(channelFormat: MPSImageFeatureChannelFormat, width: Int, height: Int, featureChannels: Int)](/documentation/metalperformanceshaders/mpsimagedescriptor/1648819-init)
- [init(channelFormat: MPSImageFeatureChannelFormat, width: Int, height: Int, featureChannels: Int, numberOfImages: Int, usage: MTLTextureUsage)](/documentation/metalperformanceshaders/mpsimagedescriptor/1648893-init)

###### Properties

- [var width: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648830-width)
- [var height: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648947-height)
- [var featureChannels: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648918-featurechannels)
- [var numberOfImages: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648846-numberofimages)
- [var pixelFormat: MTLPixelFormat](/documentation/metalperformanceshaders/mpsimagedescriptor/1648913-pixelformat)
- [var channelFormat: MPSImageFeatureChannelFormat](/documentation/metalperformanceshaders/mpsimagedescriptor/1648818-channelformat)
- [var cpuCacheMode: MTLCPUCacheMode](/documentation/metalperformanceshaders/mpsimagedescriptor/1648930-cpucachemode)
- [var storageMode: MTLStorageMode](/documentation/metalperformanceshaders/mpsimagedescriptor/1648955-storagemode)
- [var usage: MTLTextureUsage](/documentation/metalperformanceshaders/mpsimagedescriptor/1648937-usage)

###### Instance Methods

- [func copy(with: NSZone?) -> Self](/documentation/metalperformanceshaders/mpsimagedescriptor/3020686-copy)
- [init(texture: any MTLTexture, featureChannels: Int)](/documentation/metalperformanceshaders/mpsimage/2097547-init)
- [init(parentImage: MPSImage, sliceRange: NSRange, featureChannels: Int)](/documentation/metalperformanceshaders/mpsimage/2942493-init)

###### Methods

- [func setPurgeableState(MPSPurgeableState) -> MPSPurgeableState](/documentation/metalperformanceshaders/mpsimage/1648820-setpurgeablestate)
- [MPSPurgeableState](/documentation/metalperformanceshaders/mpspurgeablestate)

###### Constants

- [case allocationDeferred](/documentation/metalperformanceshaders/mpspurgeablestate/allocationdeferred)
- [case keepCurrent](/documentation/metalperformanceshaders/mpspurgeablestate/keepcurrent)
- [case nonVolatile](/documentation/metalperformanceshaders/mpspurgeablestate/nonvolatile)
- [case volatile](/documentation/metalperformanceshaders/mpspurgeablestate/volatile)
- [case empty](/documentation/metalperformanceshaders/mpspurgeablestate/empty)

###### Methods to Read and Write Raw Data

- [func readBytes(UnsafeMutableRawPointer, dataLayout: MPSDataLayout, bytesPerRow: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2867105-readbytes)
- [func readBytes(UnsafeMutableRawPointer, dataLayout: MPSDataLayout, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2867188-readbytes)
- [func writeBytes(UnsafeRawPointer, dataLayout: MPSDataLayout, bytesPerRow: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2867055-writebytes)
- [func writeBytes(UnsafeRawPointer, dataLayout: MPSDataLayout, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2867189-writebytes)
- [MPSImageReadWriteParams](/documentation/metalperformanceshaders/mpsimagereadwriteparams)

###### Initializers

- [init()](/documentation/metalperformanceshaders/mpsimagereadwriteparams/2867022-init)
- [init(featureChannelOffset: Int, numberOfFeatureChannelsToReadWrite: Int)](/documentation/metalperformanceshaders/mpsimagereadwriteparams/2867128-init)

###### Instance Properties

- [var featureChannelOffset: Int](/documentation/metalperformanceshaders/mpsimagereadwriteparams/2867064-featurechanneloffset)
- [var numberOfFeatureChannelsToReadWrite: Int](/documentation/metalperformanceshaders/mpsimagereadwriteparams/2867173-numberoffeaturechannelstoreadwri)
- [MPSDataLayout](/documentation/metalperformanceshaders/mpsdatalayout)

###### Enumeration Cases

- [case featureChannelsxHeightxWidth](/documentation/metalperformanceshaders/mpsdatalayout/featurechannelsxheightxwidth)
- [case HeightxWidthxFeatureChannels](/documentation/metalperformanceshaders/mpsdatalayout/heightxwidthxfeaturechannels)

###### Methods to Get an Image Allocator

- [class func defaultAllocator() -> any MPSImageAllocator](/documentation/metalperformanceshaders/mpsimage/2867148-defaultallocator)
- [MPSImageAllocator](/documentation/metalperformanceshaders/mpsimageallocator)

###### Instance Methods

- [func image(for: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor, kernel: MPSKernel) -> MPSImage](/documentation/metalperformanceshaders/mpsimageallocator/2866966-image)
- [func imageBatch(for: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor, kernel: MPSKernel, count: Int) -> [MPSImage]](/documentation/metalperformanceshaders/mpsimageallocator/3020685-imagebatch)

###### Properties

- [var device: any MTLDevice](/documentation/metalperformanceshaders/mpsimage/1648857-device)
- [var width: Int](/documentation/metalperformanceshaders/mpsimage/1648884-width)
- [var height: Int](/documentation/metalperformanceshaders/mpsimage/1648952-height)
- [var featureChannels: Int](/documentation/metalperformanceshaders/mpsimage/1648901-featurechannels)
- [var numberOfImages: Int](/documentation/metalperformanceshaders/mpsimage/1648900-numberofimages)
- [var textureType: MTLTextureType](/documentation/metalperformanceshaders/mpsimage/1648948-texturetype)
- [MTLTextureType](/documentation/metal/mtltexturetype)
- [var pixelFormat: MTLPixelFormat](/documentation/metalperformanceshaders/mpsimage/1648844-pixelformat)
- [MTLPixelFormat](/documentation/metal/mtlpixelformat)
- [var precision: Int](/documentation/metalperformanceshaders/mpsimage/1648880-precision)
- [var usage: MTLTextureUsage](/documentation/metalperformanceshaders/mpsimage/1648828-usage)
- [MTLTextureUsage](/documentation/metal/mtltextureusage)
- [var pixelSize: Int](/documentation/metalperformanceshaders/mpsimage/1648854-pixelsize)
- [var texture: any MTLTexture](/documentation/metalperformanceshaders/mpsimage/1648903-texture)
- [MTLTexture](/documentation/metal/mtltexture)
- [var label: String?](/documentation/metalperformanceshaders/mpsimage/1648899-label)

###### Instance Properties

- [var featureChannelFormat: MPSImageFeatureChannelFormat](/documentation/metalperformanceshaders/mpsimage/3131715-featurechannelformat)
- [var parent: MPSImage?](/documentation/metalperformanceshaders/mpsimage/2942490-parent)

###### Instance Methods

- [func batchRepresentation() -> [MPSImage]](/documentation/metalperformanceshaders/mpsimage/2942495-batchrepresentation)
- [func batchRepresentation(withSubRange: NSRange) -> [MPSImage]](/documentation/metalperformanceshaders/mpsimage/2942492-batchrepresentation)
- [func readBytes(UnsafeMutableRawPointer, dataLayout: MPSDataLayout, bytesPerRow: Int, bytesPerImage: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2951914-readbytes)
- [func resourceSize() -> Int](/documentation/metalperformanceshaders/mpsimage/2942494-resourcesize)
- [func subImage(withFeatureChannelRange: NSRange) -> MPSImage](/documentation/metalperformanceshaders/mpsimage/2942488-subimage)
- [func synchronize(on: any MTLCommandBuffer)](/documentation/metalperformanceshaders/mpsimage/2942491-synchronize)
- [func writeBytes(UnsafeRawPointer, dataLayout: MPSDataLayout, bytesPerColumn: Int, bytesPerRow: Int, bytesPerImage: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/3143488-writebytes)
- [func writeBytes(UnsafeRawPointer, dataLayout: MPSDataLayout, bytesPerRow: Int, bytesPerImage: Int, region: MTLRegion, featureChannelInfo: MPSImageReadWriteParams, imageIndex: Int)](/documentation/metalperformanceshaders/mpsimage/2951915-writebytes)
- [MPSState](/documentation/metalperformanceshaders/mpsstate)

###### Instance Properties

- [var isTemporary: Bool](/documentation/metalperformanceshaders/mpsstate/2867114-istemporary)
- [var label: String?](/documentation/metalperformanceshaders/mpsstate/2867179-label)
- [var readCount: Int](/documentation/metalperformanceshaders/mpsstate/2867042-readcount)
- [var resource: (any MTLResource)?](/documentation/metalperformanceshaders/mpsstate/2942398-resource)
- [var resourceCount: Int](/documentation/metalperformanceshaders/mpsstate/2947900-resourcecount)

###### Initializers

- [init(device: any MTLDevice, bufferSize: Int)](/documentation/metalperformanceshaders/mpsstate/2942392-init)
- [init(device: any MTLDevice, resourceList: MPSStateResourceList)](/documentation/metalperformanceshaders/mpsstate/2947908-init)
- [init(device: any MTLDevice, textureDescriptor: MTLTextureDescriptor)](/documentation/metalperformanceshaders/mpsstate/2942400-init)
- [init(resource: (any MTLResource)?)](/documentation/metalperformanceshaders/mpsstate/2942390-init)
- [init(resources: [any MTLResource]?)](/documentation/metalperformanceshaders/mpsstate/2947895-init)

###### Instance Methods

- [func bufferSize(at: Int) -> Int](/documentation/metalperformanceshaders/mpsstate/2947913-buffersize)
- [func destinationImageDescriptor(forSourceImages: [MPSImage], sourceStates: [MPSState]?, for: MPSKernel, suggestedDescriptor: MPSImageDescriptor) -> MPSImageDescriptor](/documentation/metalperformanceshaders/mpsstate/2942394-destinationimagedescriptor)
- [func resource(at: Int, allocateMemory: Bool) -> (any MTLResource)?](/documentation/metalperformanceshaders/mpsstate/2947916-resource)
- [func resourceSize() -> Int](/documentation/metalperformanceshaders/mpsstate/2942397-resourcesize)
- [func resourceType(at: Int) -> MPSStateResourceType](/documentation/metalperformanceshaders/mpsstate/2947902-resourcetype)
- [func synchronize(on: any MTLCommandBuffer)](/documentation/metalperformanceshaders/mpsstate/2942396-synchronize)
- [func textureInfo(at: Int) -> MPSStateTextureInfo](/documentation/metalperformanceshaders/mpsstate/2947899-textureinfo)

###### Type Methods

- [class func temporaryState(with: any MTLCommandBuffer) -> Self](/documentation/metalperformanceshaders/mpsstate/2942393-temporarystate)
- [class func temporaryState(with: any MTLCommandBuffer, bufferSize: Int) -> Self](/documentation/metalperformanceshaders/mpsstate/2942391-temporarystate)
- [class func temporaryState(with: any MTLCommandBuffer, resourceList: MPSStateResourceList) -> Self](/documentation/metalperformanceshaders/mpsstate/2947915-temporarystate)
- [class func temporaryState(with: any MTLCommandBuffer, textureDescriptor: MTLTextureDescriptor) -> Self](/documentation/metalperformanceshaders/mpsstate/2942395-temporarystate)
- [MPSKernel](/documentation/metalperformanceshaders/mpskernel)

###### Initializers

- [init?(coder: NSCoder)](/documentation/metalperformanceshaders/mpskernel/2875161-init)
- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpskernel/2867190-init)

###### Methods

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpskernel/1618763-init)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpskernel/1618912-copy)

###### Properties

- [var options: MPSKernelOptions](/documentation/metalperformanceshaders/mpskernel/1618889-options)
- [MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions)

###### Constants

- [static var none: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1618816-none)
- [static var skipAPIValidation: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1618826-skipapivalidation)
- [static var allowReducedPrecision: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1618748-allowreducedprecision)
- [static var disableInternalTiling: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1648950-disableinternaltiling)
- [static var insertDebugGroups: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1648897-insertdebuggroups)

###### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpskerneloptions/1618747-init)

###### Type Properties

- [static var verbose: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/2889867-verbose)
- [var device: any MTLDevice](/documentation/metalperformanceshaders/mpskernel/1618824-device)
- [var label: String?](/documentation/metalperformanceshaders/mpskernel/1618803-label)
- [MPSImageDescriptor](/documentation/metalperformanceshaders/mpsimagedescriptor)

###### Methods

- [init(channelFormat: MPSImageFeatureChannelFormat, width: Int, height: Int, featureChannels: Int)](/documentation/metalperformanceshaders/mpsimagedescriptor/1648819-init)
- [init(channelFormat: MPSImageFeatureChannelFormat, width: Int, height: Int, featureChannels: Int, numberOfImages: Int, usage: MTLTextureUsage)](/documentation/metalperformanceshaders/mpsimagedescriptor/1648893-init)

###### Properties

- [var width: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648830-width)
- [var height: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648947-height)
- [var featureChannels: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648918-featurechannels)
- [var numberOfImages: Int](/documentation/metalperformanceshaders/mpsimagedescriptor/1648846-numberofimages)
- [var pixelFormat: MTLPixelFormat](/documentation/metalperformanceshaders/mpsimagedescriptor/1648913-pixelformat)
- [var channelFormat: MPSImageFeatureChannelFormat](/documentation/metalperformanceshaders/mpsimagedescriptor/1648818-channelformat)
- [var cpuCacheMode: MTLCPUCacheMode](/documentation/metalperformanceshaders/mpsimagedescriptor/1648930-cpucachemode)
- [var storageMode: MTLStorageMode](/documentation/metalperformanceshaders/mpsimagedescriptor/1648955-storagemode)
- [var usage: MTLTextureUsage](/documentation/metalperformanceshaders/mpsimagedescriptor/1648937-usage)

###### Instance Methods

- [func copy(with: NSZone?) -> Self](/documentation/metalperformanceshaders/mpsimagedescriptor/3020686-copy)
- [func paddingMethod() -> MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpadding/2866950-paddingmethod)
- [func label() -> String](/documentation/metalperformanceshaders/mpsnnpadding/2889870-label)
- [func inverse() -> Self?](/documentation/metalperformanceshaders/mpsnnpadding/2942456-inverse)
- [var destinationImageAllocator: any MPSImageAllocator](/documentation/metalperformanceshaders/mpscnnkernel/2865650-destinationimageallocator)
- [MPSImageAllocator](/documentation/metalperformanceshaders/mpsimageallocator)

##### Instance Methods

- [func image(for: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor, kernel: MPSKernel) -> MPSImage](/documentation/metalperformanceshaders/mpsimageallocator/2866966-image)
- [func imageBatch(for: any MTLCommandBuffer, imageDescriptor: MPSImageDescriptor, kernel: MPSKernel, count: Int) -> [MPSImage]](/documentation/metalperformanceshaders/mpsimageallocator/3020685-imagebatch)
- [var dilationRateX: Int](/documentation/metalperformanceshaders/mpscnnkernel/2942669-dilationratex)
- [var dilationRateY: Int](/documentation/metalperformanceshaders/mpscnnkernel/2942679-dilationratey)
- [var isStateModified: Bool](/documentation/metalperformanceshaders/mpscnnkernel/2942673-isstatemodified)
- [var sourceFeatureChannelMaxCount: Int](/documentation/metalperformanceshaders/mpscnnkernel/2951917-sourcefeaturechannelmaxcount)
- [var sourceFeatureChannelOffset: Int](/documentation/metalperformanceshaders/mpscnnkernel/2942682-sourcefeaturechanneloffset)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage) -> MPSImage](/documentation/metalperformanceshaders/mpscnnkernel/2865642-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, destinationImage: MPSImage)](/documentation/metalperformanceshaders/mpscnnkernel/1648919-encode)
- [func appendBatchBarrier() -> Bool](/documentation/metalperformanceshaders/mpscnnkernel/2942671-appendbatchbarrier)
- [func batchEncodingStorageSize(sourceImage: [MPSImage], sourceStates: [[MPSState]]?, destinationImage: [MPSImage]?) -> Int](/documentation/metalperformanceshaders/mpscnnkernel/3237263-batchencodingstoragesize)
- [func destinationImageDescriptor(sourceImages: [MPSImage], sourceStates: [MPSState]?) -> MPSImageDescriptor](/documentation/metalperformanceshaders/mpscnnkernel/2942661-destinationimagedescriptor)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, destinationState: MPSState, destinationImage: MPSImage)](/documentation/metalperformanceshaders/mpscnnkernel/2942672-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, destinationState: AutoreleasingUnsafeMutablePointer<MPSState?>, destinationStateIsTemporary: Bool) -> MPSImage](/documentation/metalperformanceshaders/mpscnnkernel/2942680-encode)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage]) -> [MPSImage]](/documentation/metalperformanceshaders/mpscnnkernel/2942651-encodebatch)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], destinationImages: [MPSImage])](/documentation/metalperformanceshaders/mpscnnkernel/2942681-encodebatch)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], destinationStates: [MPSState]?, destinationImages: [MPSImage])](/documentation/metalperformanceshaders/mpscnnkernel/2942649-encodebatch)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], destinationStates: AutoreleasingUnsafeMutablePointer<NSArray?>, destinationStateIsTemporary: Bool) -> [MPSImage]](/documentation/metalperformanceshaders/mpscnnkernel/2942646-encodebatch)
- [func encodingStorageSize(sourceImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage?) -> Int](/documentation/metalperformanceshaders/mpscnnkernel/3237264-encodingstoragesize)
- [func isResultStateReusedAcrossBatch() -> Bool](/documentation/metalperformanceshaders/mpscnnkernel/2942665-isresultstatereusedacrossbatch)
- [func resultState(sourceImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSState?](/documentation/metalperformanceshaders/mpscnnkernel/2947932-resultstate)
- [func resultStateBatch(sourceImage: [MPSImage], sourceStates: [[MPSState]]?, destinationImage: [MPSImage]) -> [MPSState]?](/documentation/metalperformanceshaders/mpscnnkernel/2947931-resultstatebatch)
- [func temporaryResultState(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSState?](/documentation/metalperformanceshaders/mpscnnkernel/2947937-temporaryresultstate)
- [func temporaryResultStateBatch(commandBuffer: any MTLCommandBuffer, sourceImage: [MPSImage], sourceStates: [[MPSState]]?, destinationImage: [MPSImage]) -> [MPSState]?](/documentation/metalperformanceshaders/mpscnnkernel/2947939-temporaryresultstatebatch)
- [MPSCNNBinaryKernel](/documentation/metalperformanceshaders/mpscnnbinarykernel)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865640-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865629-init)

#### Instance Properties

- [var clipRect: MTLRegion](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865641-cliprect)
- [var destinationFeatureChannelOffset: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865643-destinationfeaturechanneloffset)
- [var destinationImageAllocator: any MPSImageAllocator](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865651-destinationimageallocator)
- [var isBackwards: Bool](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865652-isbackwards)
- [var padding: any MPSNNPadding](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865630-padding)
- [var primaryEdgeMode: MPSImageEdgeMode](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865646-primaryedgemode)
- [var primaryOffset: MPSOffset](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865645-primaryoffset)
- [var primaryStrideInPixelsX: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865658-primarystrideinpixelsx)
- [var primaryStrideInPixelsY: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865656-primarystrideinpixelsy)
- [var secondaryEdgeMode: MPSImageEdgeMode](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865631-secondaryedgemode)
- [var secondaryOffset: MPSOffset](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865628-secondaryoffset)
- [var secondaryStrideInPixelsX: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865649-secondarystrideinpixelsx)
- [var secondaryStrideInPixelsY: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865639-secondarystrideinpixelsy)
- [var isStateModified: Bool](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942660-isstatemodified)
- [var primaryDilationRateX: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942677-primarydilationratex)
- [var primaryDilationRateY: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942662-primarydilationratey)
- [var primaryKernelHeight: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942648-primarykernelheight)
- [var primaryKernelWidth: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942666-primarykernelwidth)
- [var primarySourceFeatureChannelMaxCount: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2951919-primarysourcefeaturechannelmaxco)
- [var primarySourceFeatureChannelOffset: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942656-primarysourcefeaturechanneloffse)
- [var secondaryDilationRateX: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942645-secondarydilationratex)
- [var secondaryDilationRateY: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942667-secondarydilationratey)
- [var secondaryKernelHeight: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942664-secondarykernelheight)
- [var secondaryKernelWidth: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942658-secondarykernelwidth)
- [var secondarySourceFeatureChannelMaxCount: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2951918-secondarysourcefeaturechannelmax)
- [var secondarySourceFeatureChannelOffset: Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942654-secondarysourcefeaturechanneloff)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, primaryImage: MPSImage, secondaryImage: MPSImage) -> MPSImage](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865632-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, primaryImage: MPSImage, secondaryImage: MPSImage, destinationImage: MPSImage)](/documentation/metalperformanceshaders/mpscnnbinarykernel/2865636-encode)
- [func appendBatchBarrier() -> Bool](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942642-appendbatchbarrier)
- [func batchEncodingStorageSize(primaryImage: [MPSImage], secondaryImage: [MPSImage], sourceStates: [[MPSState]]?, destinationImage: [MPSImage]?) -> Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/3237261-batchencodingstoragesize)
- [func destinationImageDescriptor(forSourceImages: [MPSImage], sourceStates: [MPSState]?) -> MPSImageDescriptor](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942686-destinationimagedescriptor)
- [func encode(commandBuffer: any MTLCommandBuffer, primaryImage: MPSImage, secondaryImage: MPSImage, destinationState: AutoreleasingUnsafeMutablePointer<MPSState?>, destinationStateIsTemporary: Bool) -> MPSImage](/documentation/metalperformanceshaders/mpscnnbinarykernel/2947936-encode)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, primaryImages: [MPSImage], secondaryImages: [MPSImage]) -> [MPSImage]](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942650-encodebatch)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, primaryImages: [MPSImage], secondaryImages: [MPSImage], destinationImages: [MPSImage])](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942670-encodebatch)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, primaryImages: [MPSImage], secondaryImages: [MPSImage], destinationStates: AutoreleasingUnsafeMutablePointer<NSArray?>, destinationStateIsTemporary: Bool) -> [MPSImage]](/documentation/metalperformanceshaders/mpscnnbinarykernel/2947934-encodebatch)
- [func encodingStorageSize(primaryImage: MPSImage, secondaryImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage?) -> Int](/documentation/metalperformanceshaders/mpscnnbinarykernel/3237262-encodingstoragesize)
- [func isResultStateReusedAcrossBatch() -> Bool](/documentation/metalperformanceshaders/mpscnnbinarykernel/2942659-isresultstatereusedacrossbatch)
- [func resultState(primaryImage: MPSImage, secondaryImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSState?](/documentation/metalperformanceshaders/mpscnnbinarykernel/2947935-resultstate)
- [func resultStateBatch(primaryImage: [MPSImage], secondaryImage: [MPSImage], sourceStates: [[MPSState]]?, destinationImage: [MPSImage]) -> [MPSState]?](/documentation/metalperformanceshaders/mpscnnbinarykernel/2947930-resultstatebatch)
- [func temporaryResultState(commandBuffer: any MTLCommandBuffer, primaryImage: MPSImage, secondaryImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSState?](/documentation/metalperformanceshaders/mpscnnbinarykernel/2947938-temporaryresultstate)
- [func temporaryResultStateBatch(commandBuffer: any MTLCommandBuffer, primaryImage: [MPSImage], secondaryImage: [MPSImage], sourceStates: [[MPSState]]?, destinationImage: [MPSImage]) -> [MPSState]?](/documentation/metalperformanceshaders/mpscnnbinarykernel/2947933-temporaryresultstatebatch)
- [MPSCNNGradientKernel](/documentation/metalperformanceshaders/mpscnngradientkernel)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnngradientkernel/2942647-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnngradientkernel/2942657-init)

#### Instance Properties

- [var kernelOffsetX: Int](/documentation/metalperformanceshaders/mpscnngradientkernel/2942676-kerneloffsetx)
- [var kernelOffsetY: Int](/documentation/metalperformanceshaders/mpscnngradientkernel/2942644-kerneloffsety)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, sourceGradient: MPSImage, sourceImage: MPSImage, gradientState: MPSState) -> MPSImage](/documentation/metalperformanceshaders/mpscnngradientkernel/2942663-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceGradient: MPSImage, sourceImage: MPSImage, gradientState: MPSState, destinationGradient: MPSImage)](/documentation/metalperformanceshaders/mpscnngradientkernel/2942675-encode)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceGradients: [MPSImage], sourceImages: [MPSImage], gradientStates: [MPSState]) -> [MPSImage]](/documentation/metalperformanceshaders/mpscnngradientkernel/2942668-encodebatch)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceGradients: [MPSImage], sourceImages: [MPSImage], gradientStates: [MPSState], destinationGradients: [MPSImage])](/documentation/metalperformanceshaders/mpscnngradientkernel/2942653-encodebatch)

### Predefined Padding Policies

- [MPSNNDefaultPadding](/documentation/metalperformanceshaders/mpsnndefaultpadding)

#### Initializers

- [init(method: MPSNNPaddingMethod)](/documentation/metalperformanceshaders/mpsnndefaultpadding/2867160-init)
- [MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod)

##### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867040-init)

##### Type Properties

- [static var addRemainderToBottomLeft: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867061-addremaindertobottomleft)
- [static var addRemainderToBottomRight: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2866951-addremaindertobottomright)
- [static var addRemainderToMask: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867108-addremaindertomask)
- [static var addRemainderToTopRight: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867161-addremaindertotopright)
- [static var alignBottomRight: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867062-alignbottomright)
- [static var alignMask: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867015-alignmask)
- [static var alignTopLeft: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867109-aligntopleft)
- [static var align_reserved: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867116-align_reserved)
- [static var custom: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2866952-custom)
- [static var sizeFull: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867100-sizefull)
- [static var sizeMask: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867095-sizemask)
- [static var sizeSame: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867069-sizesame)
- [static var size_reserved: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867003-size_reserved)
- [static var excludeEdges: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2890785-excludeedges)
- [static var centered: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867573-centered)
- [static var customAllowForNodeFusion: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/3763056-customallowfornodefusion)
- [static var customWhitelistForNodeFusion: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/3020690-customwhitelistfornodefusion)
- [static var topLeft: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867575-topleft)
- [static var validOnly: MPSNNPaddingMethod](/documentation/metalperformanceshaders/mpsnnpaddingmethod/2867574-validonly)

#### Instance Methods

- [func label() -> String](/documentation/metalperformanceshaders/mpsnndefaultpadding/2889871-label)

#### Type Methods

- [class func forTensorflowAveragePooling() -> Self](/documentation/metalperformanceshaders/mpsnndefaultpadding/2867164-fortensorflowaveragepooling)
- [class func forTensorflowAveragePoolingValidOnly() -> Self](/documentation/metalperformanceshaders/mpsnndefaultpadding/2947962-fortensorflowaveragepoolingvalid)
- [Recurrent Neural Networks](/documentation/metalperformanceshaders/recurrent_neural_networks)

### Recurrent Neural Networks

- [MPSRNNImageInferenceLayer](/documentation/metalperformanceshaders/mpsrnnimageinferencelayer)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsrnnimageinferencelayer/2865743-init)
- [init(device: any MTLDevice, rnnDescriptor: MPSRNNDescriptor)](/documentation/metalperformanceshaders/mpsrnnimageinferencelayer/2865691-init)
- [init(device: any MTLDevice, rnnDescriptors: [MPSRNNDescriptor])](/documentation/metalperformanceshaders/mpsrnnimageinferencelayer/2865682-init)
- [MPSRNNDescriptor](/documentation/metalperformanceshaders/mpsrnndescriptor)

##### Instance Properties

- [var inputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsrnndescriptor/2865707-inputfeaturechannels)
- [var layerSequenceDirection: MPSRNNSequenceDirection](/documentation/metalperformanceshaders/mpsrnndescriptor/2865730-layersequencedirection)
- [var outputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsrnndescriptor/2865702-outputfeaturechannels)
- [var useFloat32Weights: Bool](/documentation/metalperformanceshaders/mpsrnndescriptor/2881202-usefloat32weights)
- [var useLayerInputUnitTransformMode: Bool](/documentation/metalperformanceshaders/mpsrnndescriptor/2865687-uselayerinputunittransformmode)

#### Instance Properties

- [var bidirectionalCombineMode: MPSRNNBidirectionalCombineMode](/documentation/metalperformanceshaders/mpsrnnimageinferencelayer/2865737-bidirectionalcombinemode)
- [MPSRNNBidirectionalCombineMode](/documentation/metalperformanceshaders/mpsrnnbidirectionalcombinemode)

##### Enumeration Cases

- [case add](/documentation/metalperformanceshaders/mpsrnnbidirectionalcombinemode/add)
- [case concatenate](/documentation/metalperformanceshaders/mpsrnnbidirectionalcombinemode/concatenate)
- [case none](/documentation/metalperformanceshaders/mpsrnnbidirectionalcombinemode/none)
- [var numberOfLayers: Int](/documentation/metalperformanceshaders/mpsrnnimageinferencelayer/2865697-numberoflayers)
- [var recurrentOutputIsTemporary: Bool](/documentation/metalperformanceshaders/mpsrnnimageinferencelayer/2865749-recurrentoutputistemporary)
- [var storeAllIntermediateStates: Bool](/documentation/metalperformanceshaders/mpsrnnimageinferencelayer/2865706-storeallintermediatestates)
- [var inputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsrnnimageinferencelayer/2890141-inputfeaturechannels)
- [var outputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsrnnimageinferencelayer/2890140-outputfeaturechannels)

#### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsrnnimageinferencelayer/2865728-copy)
- [func encodeBidirectionalSequence(commandBuffer: any MTLCommandBuffer, sourceSequence: [MPSImage], destinationForwardImages: [MPSImage], destinationBackwardImages: [MPSImage]?)](/documentation/metalperformanceshaders/mpsrnnimageinferencelayer/2865693-encodebidirectionalsequence)
- [func encodeSequence(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], destinationImages: [MPSImage], recurrentInputState: MPSRNNRecurrentImageState?, recurrentOutputStates: NSMutableArray?)](/documentation/metalperformanceshaders/mpsrnnimageinferencelayer/2865717-encodesequence)
- [MPSRNNRecurrentImageState](/documentation/metalperformanceshaders/mpsrnnrecurrentimagestate)

##### Instance Methods

- [func getMemoryCellImage(forLayerIndex: Int) -> MPSImage?](/documentation/metalperformanceshaders/mpsrnnrecurrentimagestate/2865740-getmemorycellimage)
- [func getRecurrentOutputImage(forLayerIndex: Int) -> MPSImage?](/documentation/metalperformanceshaders/mpsrnnrecurrentimagestate/2865742-getrecurrentoutputimage)
- [MPSRNNMatrixInferenceLayer](/documentation/metalperformanceshaders/mpsrnnmatrixinferencelayer)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsrnnmatrixinferencelayer/2865745-init)
- [init(device: any MTLDevice, rnnDescriptor: MPSRNNDescriptor)](/documentation/metalperformanceshaders/mpsrnnmatrixinferencelayer/2865704-init)
- [init(device: any MTLDevice, rnnDescriptors: [MPSRNNDescriptor])](/documentation/metalperformanceshaders/mpsrnnmatrixinferencelayer/2865751-init)
- [MPSRNNDescriptor](/documentation/metalperformanceshaders/mpsrnndescriptor)

##### Instance Properties

- [var inputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsrnndescriptor/2865707-inputfeaturechannels)
- [var layerSequenceDirection: MPSRNNSequenceDirection](/documentation/metalperformanceshaders/mpsrnndescriptor/2865730-layersequencedirection)
- [var outputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsrnndescriptor/2865702-outputfeaturechannels)
- [var useFloat32Weights: Bool](/documentation/metalperformanceshaders/mpsrnndescriptor/2881202-usefloat32weights)
- [var useLayerInputUnitTransformMode: Bool](/documentation/metalperformanceshaders/mpsrnndescriptor/2865687-uselayerinputunittransformmode)

#### Instance Properties

- [var bidirectionalCombineMode: MPSRNNBidirectionalCombineMode](/documentation/metalperformanceshaders/mpsrnnmatrixinferencelayer/2865739-bidirectionalcombinemode)
- [MPSRNNBidirectionalCombineMode](/documentation/metalperformanceshaders/mpsrnnbidirectionalcombinemode)

##### Enumeration Cases

- [case add](/documentation/metalperformanceshaders/mpsrnnbidirectionalcombinemode/add)
- [case concatenate](/documentation/metalperformanceshaders/mpsrnnbidirectionalcombinemode/concatenate)
- [case none](/documentation/metalperformanceshaders/mpsrnnbidirectionalcombinemode/none)
- [var inputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsrnnmatrixinferencelayer/2890143-inputfeaturechannels)
- [var numberOfLayers: Int](/documentation/metalperformanceshaders/mpsrnnmatrixinferencelayer/2873347-numberoflayers)
- [var outputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsrnnmatrixinferencelayer/2890142-outputfeaturechannels)
- [var recurrentOutputIsTemporary: Bool](/documentation/metalperformanceshaders/mpsrnnmatrixinferencelayer/2865714-recurrentoutputistemporary)
- [var storeAllIntermediateStates: Bool](/documentation/metalperformanceshaders/mpsrnnmatrixinferencelayer/2865729-storeallintermediatestates)

#### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsrnnmatrixinferencelayer/2865746-copy)
- [func encodeBidirectionalSequence(commandBuffer: any MTLCommandBuffer, sourceSequence: [MPSMatrix], destinationForwardMatrices: [MPSMatrix], destinationBackwardMatrices: [MPSMatrix]?)](/documentation/metalperformanceshaders/mpsrnnmatrixinferencelayer/2865698-encodebidirectionalsequence)
- [func encodeSequence(commandBuffer: any MTLCommandBuffer, sourceMatrices: [MPSMatrix], destinationMatrices: [MPSMatrix], recurrentInputState: MPSRNNRecurrentMatrixState?, recurrentOutputStates: NSMutableArray?)](/documentation/metalperformanceshaders/mpsrnnmatrixinferencelayer/2865705-encodesequence)
- [MPSRNNRecurrentMatrixState](/documentation/metalperformanceshaders/mpsrnnrecurrentmatrixstate)

##### Instance Methods

- [func getMemoryCellMatrix(forLayerIndex: Int) -> MPSMatrix?](/documentation/metalperformanceshaders/mpsrnnrecurrentmatrixstate/2873390-getmemorycellmatrix)
- [func getRecurrentOutputMatrix(forLayerIndex: Int) -> MPSMatrix?](/documentation/metalperformanceshaders/mpsrnnrecurrentmatrixstate/2873339-getrecurrentoutputmatrix)
- [func encodeSequence(commandBuffer: any MTLCommandBuffer, sourceMatrices: [MPSMatrix], sourceOffsets: UnsafeMutablePointer<Int>?, destinationMatrices: [MPSMatrix], destinationOffsets: UnsafeMutablePointer<Int>?, recurrentInputState: MPSRNNRecurrentMatrixState?, recurrentOutputStates: NSMutableArray?)](/documentation/metalperformanceshaders/mpsrnnmatrixinferencelayer/2966781-encodesequence)
- [MPSRNNSingleGateDescriptor](/documentation/metalperformanceshaders/mpsrnnsinglegatedescriptor)

#### Instance Properties

- [var inputWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpsrnnsinglegatedescriptor/2865723-inputweights)
- [var recurrentWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpsrnnsinglegatedescriptor/2865686-recurrentweights)
- [MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource)

##### Instance Methods

- [func biasTerms() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867023-biasterms)
- [func dataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867139-datatype)
- [func descriptor() -> MPSCNNConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867050-descriptor)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2881197-label)
- [func load() -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867049-load)
- [func lookupTableForUInt8Kernel() -> UnsafeMutablePointer<Float>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867186-lookuptableforuint8kernel)
- [func purge()](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867134-purge)
- [func rangesForUInt8Kernel() -> UnsafeMutablePointer<vector_float2>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867145-rangesforuint8kernel)
- [func weights() -> UnsafeMutableRawPointer](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867187-weights)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3013778-copy)
- [func kernelWeightsDataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3564466-kernelweightsdatatype)
- [func update(with: any MTLCommandBuffer, gradientState: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> MPSCNNConvolutionWeightsAndBiasesState?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953007-update)
- [func update(with: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953009-update)
- [func weightsLayout() -> MPSCNNConvolutionWeightsLayout](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3325840-weightslayout)
- [func weightsQuantizationType() -> MPSCNNWeightsQuantizationType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2976466-weightsquantizationtype)

#### Type Methods

- [class func createRNNSingleGateDescriptor(withInputFeatureChannels: Int, outputFeatureChannels: Int) -> Self](/documentation/metalperformanceshaders/mpsrnnsinglegatedescriptor/2865703-creaternnsinglegatedescriptor)
- [MPSGRUDescriptor](/documentation/metalperformanceshaders/mpsgrudescriptor)

#### Instance Properties

- [var flipOutputGates: Bool](/documentation/metalperformanceshaders/mpsgrudescriptor/2878271-flipoutputgates)
- [var gatePnormValue: Float](/documentation/metalperformanceshaders/mpsgrudescriptor/2873332-gatepnormvalue)
- [var inputGateInputWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpsgrudescriptor/2865690-inputgateinputweights)
- [var inputGateRecurrentWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpsgrudescriptor/2865724-inputgaterecurrentweights)
- [var outputGateInputGateWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpsgrudescriptor/2878270-outputgateinputgateweights)
- [var outputGateInputWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpsgrudescriptor/2865722-outputgateinputweights)
- [var outputGateRecurrentWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpsgrudescriptor/2865699-outputgaterecurrentweights)
- [var recurrentGateInputWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpsgrudescriptor/2865719-recurrentgateinputweights)
- [var recurrentGateRecurrentWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpsgrudescriptor/2865695-recurrentgaterecurrentweights)
- [MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource)

##### Instance Methods

- [func biasTerms() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867023-biasterms)
- [func dataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867139-datatype)
- [func descriptor() -> MPSCNNConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867050-descriptor)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2881197-label)
- [func load() -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867049-load)
- [func lookupTableForUInt8Kernel() -> UnsafeMutablePointer<Float>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867186-lookuptableforuint8kernel)
- [func purge()](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867134-purge)
- [func rangesForUInt8Kernel() -> UnsafeMutablePointer<vector_float2>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867145-rangesforuint8kernel)
- [func weights() -> UnsafeMutableRawPointer](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867187-weights)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3013778-copy)
- [func kernelWeightsDataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3564466-kernelweightsdatatype)
- [func update(with: any MTLCommandBuffer, gradientState: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> MPSCNNConvolutionWeightsAndBiasesState?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953007-update)
- [func update(with: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953009-update)
- [func weightsLayout() -> MPSCNNConvolutionWeightsLayout](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3325840-weightslayout)
- [func weightsQuantizationType() -> MPSCNNWeightsQuantizationType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2976466-weightsquantizationtype)

#### Type Methods

- [class func createGRUDescriptor(withInputFeatureChannels: Int, outputFeatureChannels: Int) -> Self](/documentation/metalperformanceshaders/mpsgrudescriptor/2865715-creategrudescriptor)
- [MPSLSTMDescriptor](/documentation/metalperformanceshaders/mpslstmdescriptor)

#### Instance Properties

- [var cellGateInputWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpslstmdescriptor/2865741-cellgateinputweights)
- [var cellGateMemoryWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpslstmdescriptor/2865683-cellgatememoryweights)
- [var cellGateRecurrentWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpslstmdescriptor/2865679-cellgaterecurrentweights)
- [var cellToOutputNeuronParamA: Float](/documentation/metalperformanceshaders/mpslstmdescriptor/2865744-celltooutputneuronparama)
- [var cellToOutputNeuronParamB: Float](/documentation/metalperformanceshaders/mpslstmdescriptor/2865694-celltooutputneuronparamb)
- [var cellToOutputNeuronType: MPSCNNNeuronType](/documentation/metalperformanceshaders/mpslstmdescriptor/2865736-celltooutputneurontype)
- [MPSCNNNeuronType](/documentation/metalperformanceshaders/mpscnnneurontype)

##### Enumeration Cases

- [case none](/documentation/metalperformanceshaders/mpscnnneurontype/none)
- [case reLU](/documentation/metalperformanceshaders/mpscnnneurontype/relu)
- [case linear](/documentation/metalperformanceshaders/mpscnnneurontype/linear)
- [case sigmoid](/documentation/metalperformanceshaders/mpscnnneurontype/sigmoid)
- [case hardSigmoid](/documentation/metalperformanceshaders/mpscnnneurontype/hardsigmoid)
- [case tanH](/documentation/metalperformanceshaders/mpscnnneurontype/tanh)
- [case absolute](/documentation/metalperformanceshaders/mpscnnneurontype/absolute)
- [case softPlus](/documentation/metalperformanceshaders/mpscnnneurontype/softplus)
- [case softSign](/documentation/metalperformanceshaders/mpscnnneurontype/softsign)
- [case ELU](/documentation/metalperformanceshaders/mpscnnneurontype/elu)
- [case count](/documentation/metalperformanceshaders/mpscnnneurontype/count)
- [case exponential](/documentation/metalperformanceshaders/mpscnnneurontype/exponential)
- [case geLU](/documentation/metalperformanceshaders/mpscnnneurontype/gelu)
- [case logarithm](/documentation/metalperformanceshaders/mpscnnneurontype/logarithm)
- [case pReLU](/documentation/metalperformanceshaders/mpscnnneurontype/prelu)
- [case power](/documentation/metalperformanceshaders/mpscnnneurontype/power)
- [case reLUN](/documentation/metalperformanceshaders/mpscnnneurontype/relun)
- [var forgetGateInputWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpslstmdescriptor/2865734-forgetgateinputweights)
- [var forgetGateMemoryWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpslstmdescriptor/2865689-forgetgatememoryweights)
- [var forgetGateRecurrentWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpslstmdescriptor/2865735-forgetgaterecurrentweights)
- [var inputGateInputWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpslstmdescriptor/2865684-inputgateinputweights)
- [var inputGateMemoryWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpslstmdescriptor/2865731-inputgatememoryweights)
- [var inputGateRecurrentWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpslstmdescriptor/2865747-inputgaterecurrentweights)
- [var memoryWeightsAreDiagonal: Bool](/documentation/metalperformanceshaders/mpslstmdescriptor/2865712-memoryweightsarediagonal)
- [var outputGateInputWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpslstmdescriptor/2865701-outputgateinputweights)
- [var outputGateMemoryWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpslstmdescriptor/2865688-outputgatememoryweights)
- [var outputGateRecurrentWeights: (any MPSCNNConvolutionDataSource)?](/documentation/metalperformanceshaders/mpslstmdescriptor/2865750-outputgaterecurrentweights)
- [MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource)

##### Instance Methods

- [func biasTerms() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867023-biasterms)
- [func dataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867139-datatype)
- [func descriptor() -> MPSCNNConvolutionDescriptor](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867050-descriptor)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2881197-label)
- [func load() -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867049-load)
- [func lookupTableForUInt8Kernel() -> UnsafeMutablePointer<Float>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867186-lookuptableforuint8kernel)
- [func purge()](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867134-purge)
- [func rangesForUInt8Kernel() -> UnsafeMutablePointer<vector_float2>](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867145-rangesforuint8kernel)
- [func weights() -> UnsafeMutableRawPointer](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2867187-weights)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3013778-copy)
- [func kernelWeightsDataType() -> MPSDataType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3564466-kernelweightsdatatype)
- [func update(with: any MTLCommandBuffer, gradientState: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> MPSCNNConvolutionWeightsAndBiasesState?](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953007-update)
- [func update(with: MPSCNNConvolutionGradientState, sourceState: MPSCNNConvolutionWeightsAndBiasesState) -> Bool](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2953009-update)
- [func weightsLayout() -> MPSCNNConvolutionWeightsLayout](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/3325840-weightslayout)
- [func weightsQuantizationType() -> MPSCNNWeightsQuantizationType](/documentation/metalperformanceshaders/mpscnnconvolutiondatasource/2976466-weightsquantizationtype)
- [var cellToOutputNeuronParamC: Float](/documentation/metalperformanceshaders/mpslstmdescriptor/2935551-celltooutputneuronparamc)

#### Type Methods

- [class func createLSTMDescriptor(withInputFeatureChannels: Int, outputFeatureChannels: Int) -> Self](/documentation/metalperformanceshaders/mpslstmdescriptor/2865681-createlstmdescriptor)
- [MPSRNNSequenceDirection](/documentation/metalperformanceshaders/mpsrnnsequencedirection)

#### Enumeration Cases

- [case backward](/documentation/metalperformanceshaders/mpsrnnsequencedirection/backward)
- [case forward](/documentation/metalperformanceshaders/mpsrnnsequencedirection/forward)
- [MPSRNNMatrixTrainingLayer](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966793-init)
- [init(device: any MTLDevice, rnnDescriptor: MPSRNNDescriptor, trainableWeights: NSMutableArray)](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966794-init)

#### Instance Properties

- [var accumulateWeightGradients: Bool](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966783-accumulateweightgradients)
- [var inputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966795-inputfeaturechannels)
- [var outputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966796-outputfeaturechannels)
- [var recurrentOutputIsTemporary: Bool](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966797-recurrentoutputistemporary)
- [var storeAllIntermediateStates: Bool](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966798-storeallintermediatestates)
- [var trainingStateIsTemporary: Bool](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966799-trainingstateistemporary)

#### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966784-copy)
- [func createTemporaryWeightGradientMatrices(NSMutableArray, dataType: MPSDataType, commandBuffer: any MTLCommandBuffer)](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966785-createtemporaryweightgradientmat)
- [func createWeightGradientMatrices(NSMutableArray, dataType: MPSDataType)](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966786-createweightgradientmatrices)
- [func createWeightMatrices(NSMutableArray)](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966787-createweightmatrices)
- [func encodeCopyWeights(commandBuffer: any MTLCommandBuffer, weights: [MPSMatrix], matrixId: MPSRNNMatrixId, matrix: MPSMatrix, copyFromWeightsToMatrix: Bool, matrixOffset: MTLOrigin)](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966788-encodecopyweights)
- [func encodeForwardSequence(commandBuffer: any MTLCommandBuffer, sourceMatrices: [MPSMatrix], destinationMatrices: [MPSMatrix], trainingStates: NSMutableArray, weights: [MPSMatrix])](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966789-encodeforwardsequence)
- [func encodeForwardSequence(commandBuffer: any MTLCommandBuffer, sourceMatrices: [MPSMatrix], sourceOffsets: UnsafeMutablePointer<Int>?, destinationMatrices: [MPSMatrix], destinationOffsets: UnsafeMutablePointer<Int>?, trainingStates: NSMutableArray, recurrentInputState: MPSRNNRecurrentMatrixState?, recurrentOutputStates: NSMutableArray?, weights: [MPSMatrix])](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966790-encodeforwardsequence)
- [func encodeGradientSequence(commandBuffer: any MTLCommandBuffer, forwardSources: [MPSMatrix], forwardSourceOffsets: UnsafeMutablePointer<Int>?, sourceGradients: [MPSMatrix], sourceOffsets: UnsafeMutablePointer<Int>?, destinationGradients: [MPSMatrix]?, destinationOffsets: UnsafeMutablePointer<Int>?, weightGradients: [MPSMatrix]?, trainingStates: [MPSRNNMatrixTrainingState], recurrentInputState: MPSRNNRecurrentMatrixState?, recurrentOutputStates: NSMutableArray?, weights: [MPSMatrix])](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966791-encodegradientsequence)
- [func encodeGradientSequence(commandBuffer: any MTLCommandBuffer, forwardSources: [MPSMatrix], sourceGradients: [MPSMatrix], destinationGradients: [MPSMatrix]?, weightGradients: [MPSMatrix]?, trainingStates: [MPSRNNMatrixTrainingState], weights: [MPSMatrix])](/documentation/metalperformanceshaders/mpsrnnmatrixtraininglayer/2966792-encodegradientsequence)
- [MPSRNNMatrixTrainingState](/documentation/metalperformanceshaders/mpsrnnmatrixtrainingstate)

## Matrices and Vectors

- [Matrices and Vectors](/documentation/metalperformanceshaders/matrices_and_vectors)

### Matrices

- [MPSMatrix](/documentation/metalperformanceshaders/mpsmatrix)

#### Methods

- [init(buffer: any MTLBuffer, descriptor: MPSMatrixDescriptor)](/documentation/metalperformanceshaders/mpsmatrix/2143201-init)

#### Properties

- [var device: any MTLDevice](/documentation/metalperformanceshaders/mpsmatrix/2143209-device)
- [var rows: Int](/documentation/metalperformanceshaders/mpsmatrix/2143210-rows)
- [var columns: Int](/documentation/metalperformanceshaders/mpsmatrix/2143207-columns)
- [var dataType: MPSDataType](/documentation/metalperformanceshaders/mpsmatrix/2143197-datatype)
- [var rowBytes: Int](/documentation/metalperformanceshaders/mpsmatrix/2143208-rowbytes)
- [var data: any MTLBuffer](/documentation/metalperformanceshaders/mpsmatrix/2143205-data)
- [var matrices: Int](/documentation/metalperformanceshaders/mpsmatrix/2873334-matrices)
- [var matrixBytes: Int](/documentation/metalperformanceshaders/mpsmatrix/2873344-matrixbytes)

#### Initializers

- [init(buffer: any MTLBuffer, offset: Int, descriptor: MPSMatrixDescriptor)](/documentation/metalperformanceshaders/mpsmatrix/3229863-init)
- [init(device: any MTLDevice, descriptor: MPSMatrixDescriptor)](/documentation/metalperformanceshaders/mpsmatrix/2942567-init)

#### Instance Properties

- [var offset: Int](/documentation/metalperformanceshaders/mpsmatrix/3375740-offset)

#### Instance Methods

- [func resourceSize() -> Int](/documentation/metalperformanceshaders/mpsmatrix/2942569-resourcesize)
- [func synchronize(on: any MTLCommandBuffer)](/documentation/metalperformanceshaders/mpsmatrix/2942571-synchronize)
- [MPSMatrixDescriptor](/documentation/metalperformanceshaders/mpsmatrixdescriptor)

#### Initializers

- [init(rows: Int, columns: Int, matrices: Int, rowBytes: Int, matrixBytes: Int, dataType: MPSDataType)](/documentation/metalperformanceshaders/mpsmatrixdescriptor/2873350-init)
- [init(rows: Int, columns: Int, rowBytes: Int, dataType: MPSDataType)](/documentation/metalperformanceshaders/mpsmatrixdescriptor/2873331-init)

#### Methods

- [init(dimensions: Int, columns: Int, rowBytes: Int, dataType: MPSDataType)](/documentation/metalperformanceshaders/mpsmatrixdescriptor/2143206-init)
- [class func rowBytes(fromColumns: Int, dataType: MPSDataType) -> Int](/documentation/metalperformanceshaders/mpsmatrixdescriptor/2143204-rowbytes)
- [class func rowBytes(forColumns: Int, dataType: MPSDataType) -> Int](/documentation/metalperformanceshaders/mpsmatrixdescriptor/2873394-rowbytes)

#### Properties

- [var rows: Int](/documentation/metalperformanceshaders/mpsmatrixdescriptor/2143203-rows)
- [var columns: Int](/documentation/metalperformanceshaders/mpsmatrixdescriptor/2143196-columns)
- [var dataType: MPSDataType](/documentation/metalperformanceshaders/mpsmatrixdescriptor/2143202-datatype)
- [MPSDataType](/documentation/metalperformanceshaders/mpsdatatype)

##### Constants

- [case floatBit](/documentation/metalperformanceshaders/mpsdatatype/floatbit)
- [case float32](/documentation/metalperformanceshaders/mpsdatatype/float32)

##### Enumeration Cases

- [case invalid](/documentation/metalperformanceshaders/mpsdatatype/invalid)
- [case float16](/documentation/metalperformanceshaders/mpsdatatype/float16)
- [case int16](/documentation/metalperformanceshaders/mpsdatatype/int16)
- [case int8](/documentation/metalperformanceshaders/mpsdatatype/int8)
- [case normalizedBit](/documentation/metalperformanceshaders/mpsdatatype/normalizedbit)
- [case signedBit](/documentation/metalperformanceshaders/mpsdatatype/signedbit)
- [case uInt16](/documentation/metalperformanceshaders/mpsdatatype/uint16)
- [case uInt32](/documentation/metalperformanceshaders/mpsdatatype/uint32)
- [case uInt8](/documentation/metalperformanceshaders/mpsdatatype/uint8)
- [case unorm1](/documentation/metalperformanceshaders/mpsdatatype/unorm1)
- [case unorm8](/documentation/metalperformanceshaders/mpsdatatype/unorm8)
- [case alternateEncodingBit](/documentation/metalperformanceshaders/mpsdatatype/alternateencodingbit)
- [case bFloat16](/documentation/metalperformanceshaders/mpsdatatype/bfloat16)
- [case bool](/documentation/metalperformanceshaders/mpsdatatype/bool)
- [case complexBit](/documentation/metalperformanceshaders/mpsdatatype/complexbit)
- [case complexFloat16](/documentation/metalperformanceshaders/mpsdatatype/complexfloat16)
- [case complexFloat32](/documentation/metalperformanceshaders/mpsdatatype/complexfloat32)
- [case int2](/documentation/metalperformanceshaders/mpsdatatype/int2)
- [case int32](/documentation/metalperformanceshaders/mpsdatatype/int32)
- [case int4](/documentation/metalperformanceshaders/mpsdatatype/int4)
- [case int64](/documentation/metalperformanceshaders/mpsdatatype/int64)
- [case uInt2](/documentation/metalperformanceshaders/mpsdatatype/uint2)
- [case uInt4](/documentation/metalperformanceshaders/mpsdatatype/uint4)
- [case uInt64](/documentation/metalperformanceshaders/mpsdatatype/uint64)

##### Type Properties

- [static var intBit: MPSDataType](/documentation/metalperformanceshaders/mpsdatatype/2866103-intbit)
- [var rowBytes: Int](/documentation/metalperformanceshaders/mpsmatrixdescriptor/2143199-rowbytes)
- [var matrices: Int](/documentation/metalperformanceshaders/mpsmatrixdescriptor/2873351-matrices)
- [var matrixBytes: Int](/documentation/metalperformanceshaders/mpsmatrixdescriptor/2873387-matrixbytes)
- [MPSTemporaryMatrix](/documentation/metalperformanceshaders/mpstemporarymatrix)

#### Initializers

- [init(commandBuffer: any MTLCommandBuffer, matrixDescriptor: MPSMatrixDescriptor)](/documentation/metalperformanceshaders/mpstemporarymatrix/2867180-init)

#### Instance Properties

- [var readCount: Int](/documentation/metalperformanceshaders/mpstemporarymatrix/2867151-readcount)

#### Type Methods

- [class func prefetchStorage(with: any MTLCommandBuffer, matrixDescriptorList: [MPSMatrixDescriptor])](/documentation/metalperformanceshaders/mpstemporarymatrix/2867073-prefetchstorage)

### Vectors

- [MPSVector](/documentation/metalperformanceshaders/mpsvector)

#### Initializers

- [init(buffer: any MTLBuffer, descriptor: MPSVectorDescriptor)](/documentation/metalperformanceshaders/mpsvector/2873346-init)
- [init(buffer: any MTLBuffer, offset: Int, descriptor: MPSVectorDescriptor)](/documentation/metalperformanceshaders/mpsvector/3229864-init)
- [init(device: any MTLDevice, descriptor: MPSVectorDescriptor)](/documentation/metalperformanceshaders/mpsvector/2942566-init)

#### Instance Properties

- [var data: any MTLBuffer](/documentation/metalperformanceshaders/mpsvector/2873393-data)
- [var dataType: MPSDataType](/documentation/metalperformanceshaders/mpsvector/2873336-datatype)
- [var device: any MTLDevice](/documentation/metalperformanceshaders/mpsvector/2873338-device)
- [var length: Int](/documentation/metalperformanceshaders/mpsvector/2873392-length)
- [var vectorBytes: Int](/documentation/metalperformanceshaders/mpsvector/2873340-vectorbytes)
- [var vectors: Int](/documentation/metalperformanceshaders/mpsvector/2873388-vectors)
- [var offset: Int](/documentation/metalperformanceshaders/mpsvector/3375741-offset)

#### Instance Methods

- [func resourceSize() -> Int](/documentation/metalperformanceshaders/mpsvector/2942570-resourcesize)
- [func synchronize(on: any MTLCommandBuffer)](/documentation/metalperformanceshaders/mpsvector/2942568-synchronize)
- [MPSVectorDescriptor](/documentation/metalperformanceshaders/mpsvectordescriptor)

#### Initializers

- [init(length: Int, dataType: MPSDataType)](/documentation/metalperformanceshaders/mpsvectordescriptor/2873328-init)
- [init(length: Int, vectors: Int, vectorBytes: Int, dataType: MPSDataType)](/documentation/metalperformanceshaders/mpsvectordescriptor/2873348-init)

#### Instance Properties

- [var dataType: MPSDataType](/documentation/metalperformanceshaders/mpsvectordescriptor/2873362-datatype)
- [var length: Int](/documentation/metalperformanceshaders/mpsvectordescriptor/2873345-length)
- [var vectorBytes: Int](/documentation/metalperformanceshaders/mpsvectordescriptor/2873335-vectorbytes)
- [var vectors: Int](/documentation/metalperformanceshaders/mpsvectordescriptor/2873333-vectors)

#### Type Methods

- [class func vectorBytes(forLength: Int, dataType: MPSDataType) -> Int](/documentation/metalperformanceshaders/mpsvectordescriptor/2873337-vectorbytes)
- [MPSTemporaryVector](/documentation/metalperformanceshaders/mpstemporaryvector)

#### Initializers

- [init(commandBuffer: any MTLCommandBuffer, descriptor: MPSVectorDescriptor)](/documentation/metalperformanceshaders/mpstemporaryvector/2935550-init)

#### Instance Properties

- [var readCount: Int](/documentation/metalperformanceshaders/mpstemporaryvector/2935547-readcount)

#### Type Methods

- [class func prefetchStorage(with: any MTLCommandBuffer, descriptorList: [MPSVectorDescriptor])](/documentation/metalperformanceshaders/mpstemporaryvector/2935544-prefetchstorage)

### Classes for Decomposition and Solving

- [MPSMatrixDecompositionCholesky](/documentation/metalperformanceshaders/mpsmatrixdecompositioncholesky)

#### Initializers

- [init(device: any MTLDevice, lower: Bool, order: Int)](/documentation/metalperformanceshaders/mpsmatrixdecompositioncholesky/2867119-init)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, sourceMatrix: MPSMatrix, resultMatrix: MPSMatrix, status: (any MTLBuffer)?)](/documentation/metalperformanceshaders/mpsmatrixdecompositioncholesky/2867004-encode)
- [MPSMatrixSolveCholesky](/documentation/metalperformanceshaders/mpsmatrixsolvecholesky)

#### Initializers

- [init(device: any MTLDevice, upper: Bool, order: Int, numberOfRightHandSides: Int)](/documentation/metalperformanceshaders/mpsmatrixsolvecholesky/2873006-init)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, sourceMatrix: MPSMatrix, rightHandSideMatrix: MPSMatrix, solutionMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsmatrixsolvecholesky/2866957-encode)
- [MPSMatrixDecompositionLU](/documentation/metalperformanceshaders/mpsmatrixdecompositionlu)

#### Initializers

- [init(device: any MTLDevice, rows: Int, columns: Int)](/documentation/metalperformanceshaders/mpsmatrixdecompositionlu/2866960-init)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, sourceMatrix: MPSMatrix, resultMatrix: MPSMatrix, pivotIndices: MPSMatrix, info: (any MTLBuffer)?)](/documentation/metalperformanceshaders/mpsmatrixdecompositionlu/2867184-encode)
- [MPSMatrixSolveLU](/documentation/metalperformanceshaders/mpsmatrixsolvelu)

#### Initializers

- [init(device: any MTLDevice, transpose: Bool, order: Int, numberOfRightHandSides: Int)](/documentation/metalperformanceshaders/mpsmatrixsolvelu/2873005-init)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, sourceMatrix: MPSMatrix, rightHandSideMatrix: MPSMatrix, pivotIndices: MPSMatrix, solutionMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsmatrixsolvelu/2867074-encode)
- [MPSMatrixSolveTriangular](/documentation/metalperformanceshaders/mpsmatrixsolvetriangular)

#### Initializers

- [init(device: any MTLDevice, right: Bool, upper: Bool, transpose: Bool, unit: Bool, order: Int, numberOfRightHandSides: Int, alpha: Double)](/documentation/metalperformanceshaders/mpsmatrixsolvetriangular/2873007-init)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, sourceMatrix: MPSMatrix, rightHandSideMatrix: MPSMatrix, solutionMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsmatrixsolvetriangular/2867027-encode)
- [MPSMatrixUnaryKernel](/documentation/metalperformanceshaders/mpsmatrixunarykernel)

#### Instance Properties

- [var batchSize: Int](/documentation/metalperformanceshaders/mpsmatrixunarykernel/2867118-batchsize)
- [var batchStart: Int](/documentation/metalperformanceshaders/mpsmatrixunarykernel/2866990-batchstart)
- [var resultMatrixOrigin: MTLOrigin](/documentation/metalperformanceshaders/mpsmatrixunarykernel/2867150-resultmatrixorigin)
- [var sourceMatrixOrigin: MTLOrigin](/documentation/metalperformanceshaders/mpsmatrixunarykernel/2867053-sourcematrixorigin)
- [MPSMatrixBinaryKernel](/documentation/metalperformanceshaders/mpsmatrixbinarykernel)

#### Instance Properties

- [var batchSize: Int](/documentation/metalperformanceshaders/mpsmatrixbinarykernel/2867089-batchsize)
- [var batchStart: Int](/documentation/metalperformanceshaders/mpsmatrixbinarykernel/2867152-batchstart)
- [var primarySourceMatrixOrigin: MTLOrigin](/documentation/metalperformanceshaders/mpsmatrixbinarykernel/2867182-primarysourcematrixorigin)
- [var resultMatrixOrigin: MTLOrigin](/documentation/metalperformanceshaders/mpsmatrixbinarykernel/2867193-resultmatrixorigin)
- [var secondarySourceMatrixOrigin: MTLOrigin](/documentation/metalperformanceshaders/mpsmatrixbinarykernel/2867096-secondarysourcematrixorigin)
- [MPSMatrixDecompositionStatus](/documentation/metalperformanceshaders/mpsmatrixdecompositionstatus)

#### Enumeration Cases

- [case failure](/documentation/metalperformanceshaders/mpsmatrixdecompositionstatus/failure)
- [case nonPositiveDefinite](/documentation/metalperformanceshaders/mpsmatrixdecompositionstatus/nonpositivedefinite)
- [case singular](/documentation/metalperformanceshaders/mpsmatrixdecompositionstatus/singular)
- [case success](/documentation/metalperformanceshaders/mpsmatrixdecompositionstatus/success)

### Matrix Arithmetic Operations

- [MPSMatrixSum](/documentation/metalperformanceshaders/mpsmatrixsum)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixsum/2935614-init)
- [init(device: any MTLDevice, count: Int, rows: Int, columns: Int, transpose: Bool)](/documentation/metalperformanceshaders/mpsmatrixsum/2935623-init)

#### Instance Properties

- [var columns: Int](/documentation/metalperformanceshaders/mpsmatrixsum/2935615-columns)
- [var count: Int](/documentation/metalperformanceshaders/mpsmatrixsum/2935620-count)
- [var neuronParameterA: Float](/documentation/metalperformanceshaders/mpsmatrixsum/2935624-neuronparametera)
- [var neuronParameterB: Float](/documentation/metalperformanceshaders/mpsmatrixsum/2935616-neuronparameterb)
- [var neuronParameterC: Float](/documentation/metalperformanceshaders/mpsmatrixsum/2935618-neuronparameterc)
- [var resultMatrixOrigin: MTLOrigin](/documentation/metalperformanceshaders/mpsmatrixsum/3152564-resultmatrixorigin)
- [var rows: Int](/documentation/metalperformanceshaders/mpsmatrixsum/2935622-rows)
- [var transpose: Bool](/documentation/metalperformanceshaders/mpsmatrixsum/2935621-transpose)

#### Instance Methods

- [func encode(to: any MTLCommandBuffer, sourceMatrices: [MPSMatrix], resultMatrix: MPSMatrix, scale: MPSVector?, offsetVector: MPSVector?, biasVector: MPSVector?, start: Int)](/documentation/metalperformanceshaders/mpsmatrixsum/2935613-encode)
- [func neuronType() -> MPSCNNNeuronType](/documentation/metalperformanceshaders/mpsmatrixsum/2935625-neurontype)
- [func setNeuronType(MPSCNNNeuronType, parameterA: Float, parameterB: Float, parameterC: Float)](/documentation/metalperformanceshaders/mpsmatrixsum/2935617-setneurontype)
- [MPSMatrixMultiplication](/documentation/metalperformanceshaders/mpsmatrixmultiplication)

#### Methods

- [init(device: any MTLDevice, transposeLeft: Bool, transposeRight: Bool, resultRows: Int, resultColumns: Int, interiorColumns: Int, alpha: Double, beta: Double)](/documentation/metalperformanceshaders/mpsmatrixmultiplication/2147845-init)
- [func encode(commandBuffer: any MTLCommandBuffer, leftMatrix: MPSMatrix, rightMatrix: MPSMatrix, resultMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsmatrixmultiplication/2147848-encode)

#### Properties

- [var leftMatrixOrigin: MTLOrigin](/documentation/metalperformanceshaders/mpsmatrixmultiplication/2147846-leftmatrixorigin)
- [var rightMatrixOrigin: MTLOrigin](/documentation/metalperformanceshaders/mpsmatrixmultiplication/2147851-rightmatrixorigin)
- [var resultMatrixOrigin: MTLOrigin](/documentation/metalperformanceshaders/mpsmatrixmultiplication/2147847-resultmatrixorigin)
- [var batchSize: Int](/documentation/metalperformanceshaders/mpsmatrixmultiplication/2873082-batchsize)
- [var batchStart: Int](/documentation/metalperformanceshaders/mpsmatrixmultiplication/2873081-batchstart)

#### Initializers

- [init(device: any MTLDevice, resultRows: Int, resultColumns: Int, interiorColumns: Int)](/documentation/metalperformanceshaders/mpsmatrixmultiplication/2909034-init)
- [MPSMatrixVectorMultiplication](/documentation/metalperformanceshaders/mpsmatrixvectormultiplication)

#### Initializers

- [init(device: any MTLDevice, transpose: Bool, rows: Int, columns: Int, alpha: Double, beta: Double)](/documentation/metalperformanceshaders/mpsmatrixvectormultiplication/2873083-init)
- [init(device: any MTLDevice, rows: Int, columns: Int)](/documentation/metalperformanceshaders/mpsmatrixvectormultiplication/2909035-init)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, inputMatrix: MPSMatrix, inputVector: MPSVector, resultVector: MPSVector)](/documentation/metalperformanceshaders/mpsmatrixvectormultiplication/2873084-encode)
- [MPSMatrixFindTopK](/documentation/metalperformanceshaders/mpsmatrixfindtopk)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixfindtopk/2935582-init)
- [init(device: any MTLDevice, numberOfTopKValues: Int)](/documentation/metalperformanceshaders/mpsmatrixfindtopk/2935575-init)

#### Instance Properties

- [var indexOffset: Int](/documentation/metalperformanceshaders/mpsmatrixfindtopk/2935574-indexoffset)
- [var numberOfTopKValues: Int](/documentation/metalperformanceshaders/mpsmatrixfindtopk/2935577-numberoftopkvalues)
- [var sourceColumns: Int](/documentation/metalperformanceshaders/mpsmatrixfindtopk/2935573-sourcecolumns)
- [var sourceRows: Int](/documentation/metalperformanceshaders/mpsmatrixfindtopk/2935580-sourcerows)

#### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsmatrixfindtopk/2935581-copy)
- [func encode(commandBuffer: any MTLCommandBuffer, inputMatrix: MPSMatrix, resultIndexMatrix: MPSMatrix, resultValueMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsmatrixfindtopk/2935579-encode)

### Matrix Copying Operations

- [MPSMatrixCopy](/documentation/metalperformanceshaders/mpsmatrixcopy)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixcopy/2915334-init)
- [init(device: any MTLDevice, copyRows: Int, copyColumns: Int, sourcesAreTransposed: Bool, destinationsAreTransposed: Bool)](/documentation/metalperformanceshaders/mpsmatrixcopy/2915345-init)

#### Instance Properties

- [var copyColumns: Int](/documentation/metalperformanceshaders/mpsmatrixcopy/2915325-copycolumns)
- [var copyRows: Int](/documentation/metalperformanceshaders/mpsmatrixcopy/2915342-copyrows)
- [var destinationsAreTransposed: Bool](/documentation/metalperformanceshaders/mpsmatrixcopy/2915326-destinationsaretransposed)
- [var sourcesAreTransposed: Bool](/documentation/metalperformanceshaders/mpsmatrixcopy/2915340-sourcesaretransposed)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, copyDescriptor: MPSMatrixCopyDescriptor)](/documentation/metalperformanceshaders/mpsmatrixcopy/2915341-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, copyDescriptor: MPSMatrixCopyDescriptor, rowPermuteIndices: MPSVector?, rowPermuteOffset: Int, columnPermuteIndices: MPSVector?, columnPermuteOffset: Int)](/documentation/metalperformanceshaders/mpsmatrixcopy/2935558-encode)
- [MPSMatrixCopyToImage](/documentation/metalperformanceshaders/mpsmatrixcopytoimage)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixcopytoimage/2976459-init)
- [init(device: any MTLDevice, dataLayout: MPSDataLayout)](/documentation/metalperformanceshaders/mpsmatrixcopytoimage/2976460-init)

#### Instance Properties

- [var dataLayout: MPSDataLayout](/documentation/metalperformanceshaders/mpsmatrixcopytoimage/2976457-datalayout)
- [var sourceMatrixBatchIndex: Int](/documentation/metalperformanceshaders/mpsmatrixcopytoimage/2976461-sourcematrixbatchindex)
- [var sourceMatrixOrigin: MTLOrigin](/documentation/metalperformanceshaders/mpsmatrixcopytoimage/2976462-sourcematrixorigin)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, sourceMatrix: MPSMatrix, destinationImage: MPSImage)](/documentation/metalperformanceshaders/mpsmatrixcopytoimage/2976458-encode)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceMatrix: MPSMatrix, destinationImages: [MPSImage])](/documentation/metalperformanceshaders/mpsmatrixcopytoimage/3013770-encodebatch)
- [MPSMatrixCopyDescriptor](/documentation/metalperformanceshaders/mpsmatrixcopydescriptor)

#### Initializers

- [init(device: any MTLDevice, count: Int)](/documentation/metalperformanceshaders/mpsmatrixcopydescriptor/2915324-init)
- [init(sourceMatrices: [MPSMatrix], destinationMatrices: [MPSMatrix], offsetVector: MPSVector?, offset: Int)](/documentation/metalperformanceshaders/mpsmatrixcopydescriptor/2915344-init)
- [init(sourceMatrix: MPSMatrix, destinationMatrix: MPSMatrix, offsets: MPSMatrixCopyOffsets)](/documentation/metalperformanceshaders/mpsmatrixcopydescriptor/2915333-init)

#### Instance Methods

- [func setCopyOperationAt(Int, sourceMatrix: MPSMatrix, destinationMatrix: MPSMatrix, offsets: MPSMatrixCopyOffsets)](/documentation/metalperformanceshaders/mpsmatrixcopydescriptor/2915331-setcopyoperationat)
- [MPSImageCopyToMatrix](/documentation/metalperformanceshaders/mpsimagecopytomatrix)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagecopytomatrix/2873213-init)
- [init(device: any MTLDevice, dataLayout: MPSDataLayout)](/documentation/metalperformanceshaders/mpsimagecopytomatrix/2873210-init)

#### Instance Properties

- [var dataLayout: MPSDataLayout](/documentation/metalperformanceshaders/mpsimagecopytomatrix/2873216-datalayout)
- [var destinationMatrixBatchIndex: Int](/documentation/metalperformanceshaders/mpsimagecopytomatrix/2873211-destinationmatrixbatchindex)
- [var destinationMatrixOrigin: MTLOrigin](/documentation/metalperformanceshaders/mpsimagecopytomatrix/2873215-destinationmatrixorigin)

#### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, destinationMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsimagecopytomatrix/2873212-encode)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], destinationMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsimagecopytomatrix/3013769-encodebatch)

### Matrix Neural Network Operations

- [MPSMatrixFullyConnected](/documentation/metalperformanceshaders/mpsmatrixfullyconnected)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixfullyconnected/2935611-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixfullyconnected/2935584-init)

#### Instance Properties

- [var alpha: Double](/documentation/metalperformanceshaders/mpsmatrixfullyconnected/2935608-alpha)
- [var sourceInputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsmatrixfullyconnected/2935597-sourceinputfeaturechannels)
- [var sourceNumberOfFeatureVectors: Int](/documentation/metalperformanceshaders/mpsmatrixfullyconnected/2935609-sourcenumberoffeaturevectors)
- [var sourceOutputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsmatrixfullyconnected/2935592-sourceoutputfeaturechannels)

#### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsmatrixfullyconnected/2935595-copy)
- [func encode(commandBuffer: any MTLCommandBuffer, inputMatrix: MPSMatrix, weightMatrix: MPSMatrix, biasVector: MPSVector?, resultMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsmatrixfullyconnected/2935596-encode)
- [func neuronParameterA() -> Float](/documentation/metalperformanceshaders/mpsmatrixfullyconnected/2935602-neuronparametera)
- [func neuronParameterB() -> Float](/documentation/metalperformanceshaders/mpsmatrixfullyconnected/2935591-neuronparameterb)
- [func neuronParameterC() -> Float](/documentation/metalperformanceshaders/mpsmatrixfullyconnected/2935594-neuronparameterc)
- [func neuronType() -> MPSCNNNeuronType](/documentation/metalperformanceshaders/mpsmatrixfullyconnected/2935588-neurontype)
- [func setNeuronType(MPSCNNNeuronType, parameterA: Float, parameterB: Float, parameterC: Float)](/documentation/metalperformanceshaders/mpsmatrixfullyconnected/2935593-setneurontype)
- [MPSMatrixFullyConnectedGradient](/documentation/metalperformanceshaders/mpsmatrixfullyconnectedgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixfullyconnectedgradient/2966667-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixfullyconnectedgradient/2966668-init)

#### Instance Properties

- [var alpha: Double](/documentation/metalperformanceshaders/mpsmatrixfullyconnectedgradient/2966663-alpha)
- [var sourceInputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsmatrixfullyconnectedgradient/2966669-sourceinputfeaturechannels)
- [var sourceNumberOfFeatureVectors: Int](/documentation/metalperformanceshaders/mpsmatrixfullyconnectedgradient/2966670-sourcenumberoffeaturevectors)
- [var sourceOutputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsmatrixfullyconnectedgradient/2966671-sourceoutputfeaturechannels)

#### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsmatrixfullyconnectedgradient/2966664-copy)
- [func encodeForData(to: any MTLCommandBuffer, gradientMatrix: MPSMatrix, weightMatrix: MPSMatrix, resultGradientForDataMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsmatrixfullyconnectedgradient/2966665-encodefordata)
- [func encodeForWeightsAndBias(to: any MTLCommandBuffer, gradientMatrix: MPSMatrix, inputMatrix: MPSMatrix, resultGradientForWeightMatrix: MPSMatrix, resultGradientForBiasVector: MPSVector?)](/documentation/metalperformanceshaders/mpsmatrixfullyconnectedgradient/2966666-encodeforweightsandbias)
- [MPSMatrixNeuron](/documentation/metalperformanceshaders/mpsmatrixneuron)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixneuron/2935600-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixneuron/2935603-init)

#### Instance Properties

- [var alpha: Double](/documentation/metalperformanceshaders/mpsmatrixneuron/2935605-alpha)
- [var sourceInputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsmatrixneuron/2935599-sourceinputfeaturechannels)
- [var sourceNumberOfFeatureVectors: Int](/documentation/metalperformanceshaders/mpsmatrixneuron/2935607-sourcenumberoffeaturevectors)

#### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsmatrixneuron/2935604-copy)
- [func encode(commandBuffer: any MTLCommandBuffer, inputMatrix: MPSMatrix, biasVector: MPSVector?, resultMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsmatrixneuron/2935606-encode)
- [func neuronParameterA() -> Float](/documentation/metalperformanceshaders/mpsmatrixneuron/2935583-neuronparametera)
- [func neuronParameterB() -> Float](/documentation/metalperformanceshaders/mpsmatrixneuron/2935585-neuronparameterb)
- [func neuronParameterC() -> Float](/documentation/metalperformanceshaders/mpsmatrixneuron/2935598-neuronparameterc)
- [func neuronType() -> MPSCNNNeuronType](/documentation/metalperformanceshaders/mpsmatrixneuron/2935587-neurontype)
- [func setNeuronToPReLUWithParametersA(Data)](/documentation/metalperformanceshaders/mpsmatrixneuron/2935610-setneurontopreluwithparametersa)
- [func setNeuronType(MPSCNNNeuronType, parameterA: Float, parameterB: Float, parameterC: Float)](/documentation/metalperformanceshaders/mpsmatrixneuron/2935590-setneurontype)
- [MPSMatrixNeuronGradient](/documentation/metalperformanceshaders/mpsmatrixneurongradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixneurongradient/2966676-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixneurongradient/2966677-init)

#### Instance Properties

- [var alpha: Double](/documentation/metalperformanceshaders/mpsmatrixneurongradient/2966673-alpha)
- [var sourceInputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsmatrixneurongradient/2966684-sourceinputfeaturechannels)
- [var sourceNumberOfFeatureVectors: Int](/documentation/metalperformanceshaders/mpsmatrixneurongradient/2966685-sourcenumberoffeaturevectors)

#### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsmatrixneurongradient/2966674-copy)
- [func encode(to: any MTLCommandBuffer, gradientMatrix: MPSMatrix, inputMatrix: MPSMatrix, biasVector: MPSVector?, resultGradientForDataMatrix: MPSMatrix, resultGradientForBiasVector: MPSVector?)](/documentation/metalperformanceshaders/mpsmatrixneurongradient/2966675-encode)
- [func neuronParameterA() -> Float](/documentation/metalperformanceshaders/mpsmatrixneurongradient/2966678-neuronparametera)
- [func neuronParameterB() -> Float](/documentation/metalperformanceshaders/mpsmatrixneurongradient/2966679-neuronparameterb)
- [func neuronParameterC() -> Float](/documentation/metalperformanceshaders/mpsmatrixneurongradient/2966680-neuronparameterc)
- [func neuronType() -> MPSCNNNeuronType](/documentation/metalperformanceshaders/mpsmatrixneurongradient/2966681-neurontype)
- [func setNeuronToPReLUWithParametersA(Data)](/documentation/metalperformanceshaders/mpsmatrixneurongradient/2966682-setneurontopreluwithparametersa)
- [func setNeuronType(MPSCNNNeuronType, parameterA: Float, parameterB: Float, parameterC: Float)](/documentation/metalperformanceshaders/mpsmatrixneurongradient/2966683-setneurontype)

### Matrix Softmax Operations

- [MPSMatrixLogSoftMax](/documentation/metalperformanceshaders/mpsmatrixlogsoftmax)
- [MPSMatrixLogSoftMaxGradient](/documentation/metalperformanceshaders/mpsmatrixlogsoftmaxgradient)
- [MPSMatrixSoftMax](/documentation/metalperformanceshaders/mpsmatrixsoftmax)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixsoftmax/2935565-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixsoftmax/2935562-init)

#### Instance Properties

- [var sourceColumns: Int](/documentation/metalperformanceshaders/mpsmatrixsoftmax/2935560-sourcecolumns)
- [var sourceRows: Int](/documentation/metalperformanceshaders/mpsmatrixsoftmax/2935561-sourcerows)

#### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsmatrixsoftmax/2935566-copy)
- [func encode(commandBuffer: any MTLCommandBuffer, inputMatrix: MPSMatrix, resultMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsmatrixsoftmax/2935563-encode)
- [MPSMatrixSoftMaxGradient](/documentation/metalperformanceshaders/mpsmatrixsoftmaxgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixsoftmaxgradient/2966653-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixsoftmaxgradient/2966654-init)

#### Instance Properties

- [var sourceColumns: Int](/documentation/metalperformanceshaders/mpsmatrixsoftmaxgradient/2966655-sourcecolumns)
- [var sourceRows: Int](/documentation/metalperformanceshaders/mpsmatrixsoftmaxgradient/2966656-sourcerows)

#### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsmatrixsoftmaxgradient/2966651-copy)
- [func encode(to: any MTLCommandBuffer, gradientMatrix: MPSMatrix, forwardOutputMatrix: MPSMatrix, resultMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsmatrixsoftmaxgradient/2966652-encode)

### Matrix Normalization Operations

- [MPSMatrixBatchNormalization](/documentation/metalperformanceshaders/mpsmatrixbatchnormalization)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixbatchnormalization/2980734-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixbatchnormalization/2980735-init)

#### Instance Properties

- [var computeStatistics: Bool](/documentation/metalperformanceshaders/mpsmatrixbatchnormalization/2980730-computestatistics)
- [var epsilon: Float](/documentation/metalperformanceshaders/mpsmatrixbatchnormalization/2980733-epsilon)
- [var sourceInputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsmatrixbatchnormalization/2980741-sourceinputfeaturechannels)
- [var sourceNumberOfFeatureVectors: Int](/documentation/metalperformanceshaders/mpsmatrixbatchnormalization/2980742-sourcenumberoffeaturevectors)

#### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsmatrixbatchnormalization/2980731-copy)
- [func encode(commandBuffer: any MTLCommandBuffer, inputMatrix: MPSMatrix, meanVector: MPSVector, varianceVector: MPSVector, gammaVector: MPSVector?, betaVector: MPSVector?, resultMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsmatrixbatchnormalization/2980732-encode)
- [func neuronParameterA() -> Float](/documentation/metalperformanceshaders/mpsmatrixbatchnormalization/2980736-neuronparametera)
- [func neuronParameterB() -> Float](/documentation/metalperformanceshaders/mpsmatrixbatchnormalization/2980737-neuronparameterb)
- [func neuronParameterC() -> Float](/documentation/metalperformanceshaders/mpsmatrixbatchnormalization/2980738-neuronparameterc)
- [func neuronType() -> MPSCNNNeuronType](/documentation/metalperformanceshaders/mpsmatrixbatchnormalization/2980739-neurontype)
- [func setNeuronType(MPSCNNNeuronType, parameterA: Float, parameterB: Float, parameterC: Float)](/documentation/metalperformanceshaders/mpsmatrixbatchnormalization/2980740-setneurontype)
- [MPSMatrixBatchNormalizationGradient](/documentation/metalperformanceshaders/mpsmatrixbatchnormalizationgradient)

#### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixbatchnormalizationgradient/2980747-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixbatchnormalizationgradient/2980748-init)

#### Instance Properties

- [var epsilon: Float](/documentation/metalperformanceshaders/mpsmatrixbatchnormalizationgradient/2980746-epsilon)
- [var sourceInputFeatureChannels: Int](/documentation/metalperformanceshaders/mpsmatrixbatchnormalizationgradient/2980754-sourceinputfeaturechannels)
- [var sourceNumberOfFeatureVectors: Int](/documentation/metalperformanceshaders/mpsmatrixbatchnormalizationgradient/2980755-sourcenumberoffeaturevectors)

#### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsmatrixbatchnormalizationgradient/2980744-copy)
- [func encode(to: any MTLCommandBuffer, gradientMatrix: MPSMatrix, inputMatrix: MPSMatrix, mean: MPSVector, varianceVector: MPSVector, gammaVector: MPSVector?, betaVector: MPSVector?, resultGradientForDataMatrix: MPSMatrix, resultGradientForGammaVector: MPSVector?, resultGradientForBetaVector: MPSVector?)](/documentation/metalperformanceshaders/mpsmatrixbatchnormalizationgradient/2980745-encode)
- [func neuronParameterA() -> Float](/documentation/metalperformanceshaders/mpsmatrixbatchnormalizationgradient/2980749-neuronparametera)
- [func neuronParameterB() -> Float](/documentation/metalperformanceshaders/mpsmatrixbatchnormalizationgradient/2980750-neuronparameterb)
- [func neuronParameterC() -> Float](/documentation/metalperformanceshaders/mpsmatrixbatchnormalizationgradient/2980751-neuronparameterc)
- [func neuronType() -> MPSCNNNeuronType](/documentation/metalperformanceshaders/mpsmatrixbatchnormalizationgradient/2980752-neurontype)
- [func setNeuronType(MPSCNNNeuronType, parameterA: Float, parameterB: Float, parameterC: Float)](/documentation/metalperformanceshaders/mpsmatrixbatchnormalizationgradient/2980753-setneurontype)

## Kernel Base Classes

- [MPSKernel](/documentation/metalperformanceshaders/mpskernel)

### Initializers

- [init?(coder: NSCoder)](/documentation/metalperformanceshaders/mpskernel/2875161-init)
- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpskernel/2867190-init)

### Methods

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpskernel/1618763-init)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpskernel/1618912-copy)

### Properties

- [var options: MPSKernelOptions](/documentation/metalperformanceshaders/mpskernel/1618889-options)
- [MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions)

#### Constants

- [static var none: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1618816-none)
- [static var skipAPIValidation: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1618826-skipapivalidation)
- [static var allowReducedPrecision: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1618748-allowreducedprecision)
- [static var disableInternalTiling: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1648950-disableinternaltiling)
- [static var insertDebugGroups: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/1648897-insertdebuggroups)

#### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpskerneloptions/1618747-init)

#### Type Properties

- [static var verbose: MPSKernelOptions](/documentation/metalperformanceshaders/mpskerneloptions/2889867-verbose)
- [var device: any MTLDevice](/documentation/metalperformanceshaders/mpskernel/1618824-device)
- [var label: String?](/documentation/metalperformanceshaders/mpskernel/1618803-label)

## Keyed Archivers

- [NSKeyedArchiver](/documentation/foundation/nskeyedarchiver)
- [MPSKeyedUnarchiver](/documentation/metalperformanceshaders/mpskeyedunarchiver)

### Initializers

- [init?(device: any MTLDevice)](/documentation/metalperformanceshaders/mpskeyedunarchiver/2951874-init)
- [init(forReadingFrom: Data, device: any MTLDevice, error: NSErrorPointer)](/documentation/metalperformanceshaders/mpskeyedunarchiver/2966644-init)
- [init(forReadingWith: Data, device: any MTLDevice)](/documentation/metalperformanceshaders/mpskeyedunarchiver/2951877-init)

### Instance Methods

- [func mpsMTLDevice() -> any MTLDevice](/documentation/metalperformanceshaders/mpskeyedunarchiver/2951880-mpsmtldevice)

### Type Methods

- [class func unarchiveObject(with: Data, device: any MTLDevice) -> Any?](/documentation/metalperformanceshaders/mpskeyedunarchiver/2951881-unarchiveobject)
- [class func unarchiveObject(withFile: String, device: any MTLDevice) -> Any?](/documentation/metalperformanceshaders/mpskeyedunarchiver/2951875-unarchiveobject)
- [class func unarchiveTopLevelObject(with: Data, device: any MTLDevice) -> Any](/documentation/metalperformanceshaders/mpskeyedunarchiver/2951876-unarchivetoplevelobject)
- [class func unarchivedObject(of: AnyClass, from: Data, device: any MTLDevice) -> Any](/documentation/metalperformanceshaders/mpskeyedunarchiver/2976453-unarchivedobject)
- [class func unarchivedObject(ofClasses: Set<AnyHashable>, from: Data, device: any MTLDevice) -> Any](/documentation/metalperformanceshaders/mpskeyedunarchiver/2976454-unarchivedobject)
- [MPSDeviceProvider](/documentation/metalperformanceshaders/mpsdeviceprovider)

### Instance Methods

- [func mpsMTLDevice() -> (any MTLDevice)!](/documentation/metalperformanceshaders/mpsdeviceprovider/2875211-mpsmtldevice)

## Ray Tracing

- [Animating and Denoising a Raytraced Scene](/documentation/metalperformanceshaders/animating_and_denoising_a_raytraced_scene)
- [MPSRayIntersector](/documentation/metalperformanceshaders/mpsrayintersector)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsrayintersector/2998438-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsrayintersector/2998439-init)

### Instance Properties

- [var boundingBoxIntersectionTestType: MPSBoundingBoxIntersectionTestType](/documentation/metalperformanceshaders/mpsrayintersector/3013799-boundingboxintersectiontesttype)
- [var cullMode: MTLCullMode](/documentation/metalperformanceshaders/mpsrayintersector/2998433-cullmode)
- [var frontFacingWinding: MTLWinding](/documentation/metalperformanceshaders/mpsrayintersector/2998437-frontfacingwinding)
- [var intersectionDataType: MPSIntersectionDataType](/documentation/metalperformanceshaders/mpsrayintersector/2998440-intersectiondatatype)
- [var intersectionStride: Int](/documentation/metalperformanceshaders/mpsrayintersector/2998441-intersectionstride)
- [var rayDataType: MPSRayDataType](/documentation/metalperformanceshaders/mpsrayintersector/2998443-raydatatype)
- [var rayIndexDataType: MPSDataType](/documentation/metalperformanceshaders/mpsrayintersector/3131884-rayindexdatatype)
- [var rayMask: UInt32](/documentation/metalperformanceshaders/mpsrayintersector/3152591-raymask)
- [var rayMaskOperator: MPSRayMaskOperator](/documentation/metalperformanceshaders/mpsrayintersector/3242876-raymaskoperator)
- [var rayMaskOptions: MPSRayMaskOptions](/documentation/metalperformanceshaders/mpsrayintersector/2998444-raymaskoptions)
- [var rayStride: Int](/documentation/metalperformanceshaders/mpsrayintersector/2998445-raystride)
- [var triangleIntersectionTestType: MPSTriangleIntersectionTestType](/documentation/metalperformanceshaders/mpsrayintersector/3013800-triangleintersectiontesttype)

### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsrayintersector/2998432-copy)
- [func encode(with: NSCoder)](/documentation/metalperformanceshaders/mpsrayintersector/2998436-encode)
- [func encodeIntersection(commandBuffer: any MTLCommandBuffer, intersectionType: MPSIntersectionType, rayBuffer: any MTLBuffer, rayBufferOffset: Int, intersectionBuffer: any MTLBuffer, intersectionBufferOffset: Int, rayCount: Int, accelerationStructure: MPSAccelerationStructure)](/documentation/metalperformanceshaders/mpsrayintersector/2998434-encodeintersection)
- [func encodeIntersection(commandBuffer: any MTLCommandBuffer, intersectionType: MPSIntersectionType, rayBuffer: any MTLBuffer, rayBufferOffset: Int, intersectionBuffer: any MTLBuffer, intersectionBufferOffset: Int, rayCountBuffer: any MTLBuffer, rayCountBufferOffset: Int, accelerationStructure: MPSAccelerationStructure)](/documentation/metalperformanceshaders/mpsrayintersector/2998435-encodeintersection)
- [func encodeIntersection(commandBuffer: any MTLCommandBuffer, intersectionType: MPSIntersectionType, rayBuffer: any MTLBuffer, rayBufferOffset: Int, rayIndexBuffer: any MTLBuffer, rayIndexBufferOffset: Int, intersectionBuffer: any MTLBuffer, intersectionBufferOffset: Int, rayIndexCount: Int, accelerationStructure: MPSAccelerationStructure)](/documentation/metalperformanceshaders/mpsrayintersector/3131882-encodeintersection)
- [func encodeIntersection(commandBuffer: any MTLCommandBuffer, intersectionType: MPSIntersectionType, rayBuffer: any MTLBuffer, rayBufferOffset: Int, rayIndexBuffer: any MTLBuffer, rayIndexBufferOffset: Int, intersectionBuffer: any MTLBuffer, intersectionBufferOffset: Int, rayIndexCountBuffer: any MTLBuffer, rayIndexCountBufferOffset: Int, accelerationStructure: MPSAccelerationStructure)](/documentation/metalperformanceshaders/mpsrayintersector/3131883-encodeintersection)
- [func encodeIntersection(commandBuffer: any MTLCommandBuffer, intersectionType: MPSIntersectionType, rayTexture: any MTLTexture, intersectionTexture: any MTLTexture, accelerationStructure: MPSAccelerationStructure)](/documentation/metalperformanceshaders/mpsrayintersector/3143553-encodeintersection)
- [func recommendedMinimumRayBatchSize(rayCount: Int) -> Int](/documentation/metalperformanceshaders/mpsrayintersector/2998446-recommendedminimumraybatchsize)
- [MPSAccelerationStructureGroup](/documentation/metalperformanceshaders/mpsaccelerationstructuregroup)

### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsaccelerationstructuregroup/2980784-init)

### Instance Properties

- [var device: any MTLDevice](/documentation/metalperformanceshaders/mpsaccelerationstructuregroup/2980783-device)
- [MPSInstanceAccelerationStructure](/documentation/metalperformanceshaders/mpsinstanceaccelerationstructure)

### Instance Properties

- [var accelerationStructures: [MPSPolygonAccelerationStructure]?](/documentation/metalperformanceshaders/mpsinstanceaccelerationstructure/2980787-accelerationstructures)
- [var instanceBuffer: (any MTLBuffer)?](/documentation/metalperformanceshaders/mpsinstanceaccelerationstructure/2980788-instancebuffer)
- [var instanceBufferOffset: Int](/documentation/metalperformanceshaders/mpsinstanceaccelerationstructure/2980789-instancebufferoffset)
- [var instanceCount: Int](/documentation/metalperformanceshaders/mpsinstanceaccelerationstructure/2980790-instancecount)
- [var maskBuffer: (any MTLBuffer)?](/documentation/metalperformanceshaders/mpsinstanceaccelerationstructure/2980791-maskbuffer)
- [var maskBufferOffset: Int](/documentation/metalperformanceshaders/mpsinstanceaccelerationstructure/2980792-maskbufferoffset)
- [var transformBuffer: (any MTLBuffer)?](/documentation/metalperformanceshaders/mpsinstanceaccelerationstructure/2980793-transformbuffer)
- [var transformBufferOffset: Int](/documentation/metalperformanceshaders/mpsinstanceaccelerationstructure/2980794-transformbufferoffset)
- [var transformType: MPSTransformType](/documentation/metalperformanceshaders/mpsinstanceaccelerationstructure/2980795-transformtype)
- [MPSTriangleAccelerationStructure](/documentation/metalperformanceshaders/mpstriangleaccelerationstructure)

### Instance Properties

- [var triangleCount: Int](/documentation/metalperformanceshaders/mpstriangleaccelerationstructure/2980881-trianglecount)
- [MPSAccelerationStructure](/documentation/metalperformanceshaders/mpsaccelerationstructure)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsaccelerationstructure/2980765-init)
- [init?(coder: NSCoder, group: MPSAccelerationStructureGroup)](/documentation/metalperformanceshaders/mpsaccelerationstructure/2980766-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsaccelerationstructure/2980767-init)
- [init(group: MPSAccelerationStructureGroup)](/documentation/metalperformanceshaders/mpsaccelerationstructure/2980768-init)

### Instance Properties

- [var boundingBox: MPSAxisAlignedBoundingBox](/documentation/metalperformanceshaders/mpsaccelerationstructure/2980759-boundingbox)
- [var group: MPSAccelerationStructureGroup](/documentation/metalperformanceshaders/mpsaccelerationstructure/2980764-group)
- [var status: MPSAccelerationStructureStatus](/documentation/metalperformanceshaders/mpsaccelerationstructure/2980771-status)
- [var usage: MPSAccelerationStructureUsage](/documentation/metalperformanceshaders/mpsaccelerationstructure/2980772-usage)

### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsaccelerationstructure/2980760-copy)
- [func copy(with: NSZone?, group: MPSAccelerationStructureGroup) -> Self](/documentation/metalperformanceshaders/mpsaccelerationstructure/2980761-copy)
- [func encode(with: NSCoder)](/documentation/metalperformanceshaders/mpsaccelerationstructure/2980763-encode)
- [func encodeRefit(commandBuffer: any MTLCommandBuffer)](/documentation/metalperformanceshaders/mpsaccelerationstructure/2980762-encoderefit)
- [func rebuild()](/documentation/metalperformanceshaders/mpsaccelerationstructure/2980769-rebuild)
- [func rebuild(completionHandler: MPSAccelerationStructureCompletionHandler)](/documentation/metalperformanceshaders/mpsaccelerationstructure/2980770-rebuild)

## Classes

- [MPSCNNConvolutionTransposeGradient](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradient)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradient/3131783-init)
- [init(device: any MTLDevice, weights: any MPSCNNConvolutionDataSource)](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradient/3131784-init)

### Instance Properties

- [var dataSource: any MPSCNNConvolutionDataSource](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradient/3131780-datasource)
- [var gradientOption: MPSCNNConvolutionGradientOption](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradient/3131781-gradientoption)
- [var groups: Int](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradient/3131782-groups)
- [var sourceGradientFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradient/3131787-sourcegradientfeaturechannels)
- [var sourceImageFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradient/3131788-sourceimagefeaturechannels)

### Instance Methods

- [func reloadWeightsAndBiases(with: any MTLCommandBuffer, state: MPSCNNConvolutionWeightsAndBiasesState)](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradient/3131786-reloadweightsandbiases)
- [func reloadWeightsAndBiasesFromDataSource()](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradient/3131785-reloadweightsandbiasesfromdataso)
- [MPSCNNConvolutionTransposeGradientNode](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradientnode)

### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, convolutionTransposeGradientState: MPSCNNConvolutionTransposeGradientStateNode, weights: (any MPSCNNConvolutionDataSource)?)](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradientnode/3143550-init)
- [MPSCNNConvolutionTransposeGradientState](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradientstate)

### Instance Properties

- [var convolutionTranspose: MPSCNNConvolutionTranspose](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradientstate/3131790-convolutiontranspose)
- [MPSCNNConvolutionTransposeGradientStateNode](/documentation/metalperformanceshaders/mpscnnconvolutiontransposegradientstatenode)
- [MPSCNNFullyConnectedGradientNode](/documentation/metalperformanceshaders/mpscnnfullyconnectedgradientnode)

### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, convolutionGradientState: MPSCNNConvolutionGradientStateNode, weights: (any MPSCNNConvolutionDataSource)?)](/documentation/metalperformanceshaders/mpscnnfullyconnectedgradientnode/3152566-init)
- [MPSCNNGroupNormalization](/documentation/metalperformanceshaders/mpscnngroupnormalization)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnngroupnormalization/3152536-init)
- [init(device: any MTLDevice, dataSource: any MPSCNNGroupNormalizationDataSource)](/documentation/metalperformanceshaders/mpscnngroupnormalization/3152537-init)

### Instance Properties

- [var dataSource: any MPSCNNGroupNormalizationDataSource](/documentation/metalperformanceshaders/mpscnngroupnormalization/3152534-datasource)
- [var epsilon: Float](/documentation/metalperformanceshaders/mpscnngroupnormalization/3152535-epsilon)

### Instance Methods

- [func reloadGammaAndBeta(with: any MTLCommandBuffer, gammaAndBetaState: MPSCNNNormalizationGammaAndBetaState)](/documentation/metalperformanceshaders/mpscnngroupnormalization/3152539-reloadgammaandbeta)
- [func reloadGammaAndBetaFromDataSource()](/documentation/metalperformanceshaders/mpscnngroupnormalization/3152538-reloadgammaandbetafromdatasource)
- [func resultState(sourceImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSCNNGroupNormalizationGradientState?](/documentation/metalperformanceshaders/mpscnngroupnormalization/3152540-resultstate)
- [func temporaryResultState(commandBuffer: any MTLCommandBuffer, sourceImage: MPSImage, sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSCNNGroupNormalizationGradientState?](/documentation/metalperformanceshaders/mpscnngroupnormalization/3152541-temporaryresultstate)
- [MPSCNNGroupNormalizationGradient](/documentation/metalperformanceshaders/mpscnngroupnormalizationgradient)
- [MPSCNNGroupNormalizationGradientNode](/documentation/metalperformanceshaders/mpscnngroupnormalizationgradientnode)

### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode)](/documentation/metalperformanceshaders/mpscnngroupnormalizationgradientnode/3152569-init)
- [MPSCNNGroupNormalizationGradientState](/documentation/metalperformanceshaders/mpscnngroupnormalizationgradientstate)

### Instance Properties

- [var beta: (any MTLBuffer)?](/documentation/metalperformanceshaders/mpscnngroupnormalizationgradientstate/3152557-beta)
- [var gamma: (any MTLBuffer)?](/documentation/metalperformanceshaders/mpscnngroupnormalizationgradientstate/3152558-gamma)
- [var gradientForBeta: any MTLBuffer](/documentation/metalperformanceshaders/mpscnngroupnormalizationgradientstate/3152559-gradientforbeta)
- [var gradientForGamma: any MTLBuffer](/documentation/metalperformanceshaders/mpscnngroupnormalizationgradientstate/3152560-gradientforgamma)
- [var groupNormalization: MPSCNNGroupNormalization](/documentation/metalperformanceshaders/mpscnngroupnormalizationgradientstate/3152561-groupnormalization)
- [MPSCNNGroupNormalizationNode](/documentation/metalperformanceshaders/mpscnngroupnormalizationnode)

### Initializers

- [init(source: MPSNNImageNode, dataSource: any MPSCNNGroupNormalizationDataSource)](/documentation/metalperformanceshaders/mpscnngroupnormalizationnode/3152572-init)

### Instance Properties

- [var trainingStyle: MPSNNTrainingStyle](/documentation/metalperformanceshaders/mpscnngroupnormalizationnode/3197823-trainingstyle)
- [MPSCNNMultiaryKernel](/documentation/metalperformanceshaders/mpscnnmultiarykernel)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043425-init)
- [init(device: any MTLDevice, sourceCount: Int)](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043426-init)

### Instance Properties

- [var clipRect: MTLRegion](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043412-cliprect)
- [var destinationFeatureChannelOffset: Int](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043413-destinationfeaturechanneloffset)
- [var destinationImageAllocator: any MPSImageAllocator](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043414-destinationimageallocator)
- [var isBackwards: Bool](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043427-isbackwards)
- [var isStateModified: Bool](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043429-isstatemodified)
- [var padding: any MPSNNPadding](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043433-padding)
- [var sourceCount: Int](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043446-sourcecount)

### Instance Methods

- [func appendBatchBarrier() -> Bool](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043411-appendbatchbarrier)
- [func destinationImageDescriptor(sourceImages: [MPSImage], sourceStates: [MPSState]?) -> MPSImageDescriptor](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043415-destinationimagedescriptor)
- [func dilationRateXatIndex(Int) -> Int](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043416-dilationratexatindex)
- [func dilationRateYatIndex(Int) -> Int](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043417-dilationrateyatindex)
- [func edgeMode(at: Int) -> MPSImageEdgeMode](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043418-edgemode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage]) -> MPSImage](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043422-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], destinationImage: MPSImage)](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043423-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], destinationState: AutoreleasingUnsafeMutablePointer<MPSState?>, destinationStateIsTemporary: Bool) -> MPSImage](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043424-encode)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [[MPSImage]]) -> [MPSImage]](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043419-encodebatch)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [[MPSImage]], destinationImages: [MPSImage])](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043420-encodebatch)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [[MPSImage]], destinationStates: AutoreleasingUnsafeMutablePointer<NSArray?>, destinationStateIsTemporary: Bool) -> [MPSImage]](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043421-encodebatch)
- [func isResultStateReusedAcrossBatch() -> Bool](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043428-isresultstatereusedacrossbatch)
- [func kernelHeight(at: Int) -> Int](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043430-kernelheight)
- [func kernelWidth(at: Int) -> Int](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043431-kernelwidth)
- [func offset(at: Int) -> MPSOffset](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043432-offset)
- [func resultState(sourceImages: [MPSImage], sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSState?](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043435-resultstate)
- [func resultStateBatch(sourceImages: [[MPSImage]], sourceStates: [[MPSState]]?, destinationImage: [MPSImage]) -> [MPSState]?](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043434-resultstatebatch)
- [func setDilationRateX(Int, at: Int)](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043436-setdilationratex)
- [func setDilationRateY(Int, at: Int)](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043437-setdilationratey)
- [func setEdgeMode(MPSImageEdgeMode, at: Int)](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043438-setedgemode)
- [func setKernelHeight(Int, at: Int)](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043439-setkernelheight)
- [func setKernelWidth(Int, at: Int)](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043440-setkernelwidth)
- [func setOffset(MPSOffset, at: Int)](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043441-setoffset)
- [func setSourceFeatureChannelMaxCount(Int, at: Int)](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043442-setsourcefeaturechannelmaxcount)
- [func setSourceFeatureChannelOffset(Int, at: Int)](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043443-setsourcefeaturechanneloffset)
- [func setStrideInPixelsX(Int, at: Int)](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043444-setstrideinpixelsx)
- [func setStrideInPixelsY(Int, at: Int)](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043445-setstrideinpixelsy)
- [func sourceFeatureChannelMaxCount(at: Int) -> Int](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043447-sourcefeaturechannelmaxcount)
- [func sourceFeatureChannelOffset(at: Int) -> Int](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043448-sourcefeaturechanneloffset)
- [func stride(inPixelsXatIndex: Int) -> Int](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043449-stride)
- [func stride(inPixelsYatIndex: Int) -> Int](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043450-stride)
- [func temporaryResultState(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], sourceStates: [MPSState]?, destinationImage: MPSImage) -> MPSState?](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043452-temporaryresultstate)
- [func temporaryResultStateBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [[MPSImage]], sourceStates: [[MPSState]]?, destinationImage: [MPSImage]) -> [MPSState]?](/documentation/metalperformanceshaders/mpscnnmultiarykernel/3043451-temporaryresultstatebatch)
- [MPSCNNNeuronGeLUNode](/documentation/metalperformanceshaders/mpscnnneurongelunode)

### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpscnnneurongelunode/3237266-init)
- [MPSCommandBuffer](/documentation/metalperformanceshaders/mpscommandbuffer)

### Initializers

- [init(commandBuffer: any MTLCommandBuffer)](/documentation/metalperformanceshaders/mpscommandbuffer/3114031-init)
- [init(from: any MTLCommandQueue)](/documentation/metalperformanceshaders/mpscommandbuffer/3114029-init)

### Instance Properties

- [var commandBuffer: any MTLCommandBuffer](/documentation/metalperformanceshaders/mpscommandbuffer/3114028-commandbuffer)
- [var heapProvider: (any MPSHeapProvider)?](/documentation/metalperformanceshaders/mpscommandbuffer/3229857-heapprovider)
- [var predicate: MPSPredicate?](/documentation/metalperformanceshaders/mpscommandbuffer/3114032-predicate)
- [var rootCommandBuffer: any MTLCommandBuffer](/documentation/metalperformanceshaders/mpscommandbuffer/3166772-rootcommandbuffer)

### Instance Methods

- [func commitAndContinue()](/documentation/metalperformanceshaders/mpscommandbuffer/3152524-commitandcontinue)
- [func prefetchHeap(forWorkloadSize: Int)](/documentation/metalperformanceshaders/mpscommandbuffer/3229858-prefetchheap)
- [MPSImageCanny](/documentation/metalperformanceshaders/mpsimagecanny)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagecanny/3547971-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagecanny/3547972-init)
- [init(device: any MTLDevice, linearToGrayScaleTransform: UnsafePointer<Float>, sigma: Float)](/documentation/metalperformanceshaders/mpsimagecanny/3547973-init)

### Instance Properties

- [var colorTransform: UnsafePointer<Float>](/documentation/metalperformanceshaders/mpsimagecanny/3547969-colortransform)
- [var highThreshold: Float](/documentation/metalperformanceshaders/mpsimagecanny/3547970-highthreshold)
- [var lowThreshold: Float](/documentation/metalperformanceshaders/mpsimagecanny/3547974-lowthreshold)
- [var sigma: Float](/documentation/metalperformanceshaders/mpsimagecanny/3547975-sigma)
- [var useFastMode: Bool](/documentation/metalperformanceshaders/mpsimagecanny/3547976-usefastmode)
- [MPSImageEDLines](/documentation/metalperformanceshaders/mpsimageedlines)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimageedlines/3618920-init)
- [init(device: any MTLDevice, gaussianSigma: Float, minLineLength: UInt16, maxLines: Int, detailRatio: UInt16, gradientThreshold: Float, lineErrorThreshold: Float, mergeLocalityThreshold: Float)](/documentation/metalperformanceshaders/mpsimageedlines/3618921-init)

### Instance Properties

- [var clipRectSource: MTLRegion](/documentation/metalperformanceshaders/mpsimageedlines/3618915-cliprectsource)
- [var detailRatio: UInt16](/documentation/metalperformanceshaders/mpsimageedlines/3618916-detailratio)
- [var gaussianSigma: Float](/documentation/metalperformanceshaders/mpsimageedlines/3618918-gaussiansigma)
- [var gradientThreshold: Float](/documentation/metalperformanceshaders/mpsimageedlines/3618919-gradientthreshold)
- [var lineErrorThreshold: Float](/documentation/metalperformanceshaders/mpsimageedlines/3618922-lineerrorthreshold)
- [var maxLines: Int](/documentation/metalperformanceshaders/mpsimageedlines/3618923-maxlines)
- [var mergeLocalityThreshold: Float](/documentation/metalperformanceshaders/mpsimageedlines/3618924-mergelocalitythreshold)
- [var minLineLength: UInt16](/documentation/metalperformanceshaders/mpsimageedlines/3618925-minlinelength)

### Instance Methods

- [func encode(to: any MTLCommandBuffer, sourceTexture: any MTLTexture, destinationTexture: (any MTLTexture)?, endpointBuffer: any MTLBuffer, endpointOffset: Int)](/documentation/metalperformanceshaders/mpsimageedlines/3618917-encode)
- [MPSImageNormalizedHistogram](/documentation/metalperformanceshaders/mpsimagenormalizedhistogram)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsimagenormalizedhistogram/3019325-init)
- [init(device: any MTLDevice, histogramInfo: UnsafePointer<MPSImageHistogramInfo>)](/documentation/metalperformanceshaders/mpsimagenormalizedhistogram/3019326-init)

### Instance Properties

- [var clipRectSource: MTLRegion](/documentation/metalperformanceshaders/mpsimagenormalizedhistogram/3019321-cliprectsource)
- [var histogramInfo: MPSImageHistogramInfo](/documentation/metalperformanceshaders/mpsimagenormalizedhistogram/3019323-histograminfo)
- [var zeroHistogram: Bool](/documentation/metalperformanceshaders/mpsimagenormalizedhistogram/3019327-zerohistogram)

### Instance Methods

- [func encode(to: any MTLCommandBuffer, sourceTexture: any MTLTexture, minmaxTexture: any MTLTexture, histogram: any MTLBuffer, histogramOffset: Int)](/documentation/metalperformanceshaders/mpsimagenormalizedhistogram/3019322-encode)
- [func histogramSize(forSourceFormat: MTLPixelFormat) -> Int](/documentation/metalperformanceshaders/mpsimagenormalizedhistogram/3019324-histogramsize)
- [MPSMatrixRandom](/documentation/metalperformanceshaders/mpsmatrixrandom)

### Instance Properties

- [var batchSize: Int](/documentation/metalperformanceshaders/mpsmatrixrandom/3242847-batchsize)
- [var batchStart: Int](/documentation/metalperformanceshaders/mpsmatrixrandom/3242848-batchstart)
- [var destinationDataType: MPSDataType](/documentation/metalperformanceshaders/mpsmatrixrandom/3242849-destinationdatatype)
- [var distributionType: MPSMatrixRandomDistribution](/documentation/metalperformanceshaders/mpsmatrixrandom/3242850-distributiontype)

### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer, destinationMatrix: MPSMatrix)](/documentation/metalperformanceshaders/mpsmatrixrandom/3325839-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, destinationVector: MPSVector)](/documentation/metalperformanceshaders/mpsmatrixrandom/3242851-encode)
- [MPSMatrixRandomDistributionDescriptor](/documentation/metalperformanceshaders/mpsmatrixrandomdistributiondescriptor)

### Instance Properties

- [var distributionType: MPSMatrixRandomDistribution](/documentation/metalperformanceshaders/mpsmatrixrandomdistributiondescriptor/3242857-distributiontype)
- [var maximum: Float](/documentation/metalperformanceshaders/mpsmatrixrandomdistributiondescriptor/3242858-maximum)
- [var mean: Float](/documentation/metalperformanceshaders/mpsmatrixrandomdistributiondescriptor/3242859-mean)
- [var minimum: Float](/documentation/metalperformanceshaders/mpsmatrixrandomdistributiondescriptor/3242860-minimum)
- [var standardDeviation: Float](/documentation/metalperformanceshaders/mpsmatrixrandomdistributiondescriptor/3242861-standarddeviation)

### Type Methods

- [class func `default`() -> MPSMatrixRandomDistributionDescriptor](/documentation/metalperformanceshaders/mpsmatrixrandomdistributiondescriptor/3242856-default)
- [class func normalDistributionDescriptor(withMean: Float, standardDeviation: Float) -> MPSMatrixRandomDistributionDescriptor](/documentation/metalperformanceshaders/mpsmatrixrandomdistributiondescriptor/3547979-normaldistributiondescriptor)
- [class func normalDistributionDescriptor(withMean: Float, standardDeviation: Float, minimum: Float, maximum: Float) -> MPSMatrixRandomDistributionDescriptor](/documentation/metalperformanceshaders/mpsmatrixrandomdistributiondescriptor/3547980-normaldistributiondescriptor)
- [class func uniformDistributionDescriptor(withMinimum: Float, maximum: Float) -> MPSMatrixRandomDistributionDescriptor](/documentation/metalperformanceshaders/mpsmatrixrandomdistributiondescriptor/3242862-uniformdistributiondescriptor)
- [MPSMatrixRandomMTGP32](/documentation/metalperformanceshaders/mpsmatrixrandommtgp32)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixrandommtgp32/3242864-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixrandommtgp32/3242865-init)
- [init(device: any MTLDevice, destinationDataType: MPSDataType, seed: Int)](/documentation/metalperformanceshaders/mpsmatrixrandommtgp32/3242866-init)
- [init(device: any MTLDevice, destinationDataType: MPSDataType, seed: Int, distributionDescriptor: MPSMatrixRandomDistributionDescriptor)](/documentation/metalperformanceshaders/mpsmatrixrandommtgp32/3242867-init)

### Instance Methods

- [func synchronizeState(on: any MTLCommandBuffer)](/documentation/metalperformanceshaders/mpsmatrixrandommtgp32/3242868-synchronizestate)
- [MPSMatrixRandomPhilox](/documentation/metalperformanceshaders/mpsmatrixrandomphilox)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixrandomphilox/3242870-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsmatrixrandomphilox/3242871-init)
- [init(device: any MTLDevice, destinationDataType: MPSDataType, seed: Int)](/documentation/metalperformanceshaders/mpsmatrixrandomphilox/3242872-init)
- [init(device: any MTLDevice, destinationDataType: MPSDataType, seed: Int, distributionDescriptor: MPSMatrixRandomDistributionDescriptor)](/documentation/metalperformanceshaders/mpsmatrixrandomphilox/3242873-init)
- [MPSNDArray](/documentation/metalperformanceshaders/mpsndarray)

### Initializers

- [init(buffer: any MTLBuffer, offset: Int, descriptor: MPSNDArrayDescriptor)](/documentation/metalperformanceshaders/mpsndarray/4391636-init)
- [init(device: any MTLDevice, descriptor: MPSNDArrayDescriptor)](/documentation/metalperformanceshaders/mpsndarray/3114049-init)
- [init(device: any MTLDevice, scalar: Double)](/documentation/metalperformanceshaders/mpsndarray/3114051-init)

### Instance Properties

- [var dataType: MPSDataType](/documentation/metalperformanceshaders/mpsndarray/3114041-datatype)
- [var dataTypeSize: Int](/documentation/metalperformanceshaders/mpsndarray/3114042-datatypesize)
- [var device: any MTLDevice](/documentation/metalperformanceshaders/mpsndarray/3114045-device)
- [var label: String?](/documentation/metalperformanceshaders/mpsndarray/3114052-label)
- [var numberOfDimensions: Int](/documentation/metalperformanceshaders/mpsndarray/3114055-numberofdimensions)
- [var parent: MPSNDArray?](/documentation/metalperformanceshaders/mpsndarray/3114056-parent)

### Instance Methods

- [func arrayView(with: MPSNDArrayDescriptor) -> MPSNDArray?](/documentation/metalperformanceshaders/mpsndarray/4438553-arrayview)
- [func arrayView(with: any MTLCommandBuffer, descriptor: MPSNDArrayDescriptor, aliasing: MPSAliasingStrategy) -> MPSNDArray?](/documentation/metalperformanceshaders/mpsndarray/3114040-arrayview)
- [func arrayView(withDimensionCount: Int, dimensionSizes: UnsafePointer<Int>, strides: UnsafePointer<Int>) -> MPSNDArray?](/documentation/metalperformanceshaders/mpsndarray/4408693-arrayview)
- [func arrayView(withShape: [NSNumber]?, strides: [NSNumber]) -> MPSNDArray?](/documentation/metalperformanceshaders/mpsndarray/4408694-arrayview)
- [func descriptor() -> MPSNDArrayDescriptor](/documentation/metalperformanceshaders/mpsndarray/3114044-descriptor)
- [func exportData(with: any MTLCommandBuffer, to: any MTLBuffer, destinationDataType: MPSDataType, offset: Int, rowStrides: UnsafeMutablePointer<Int>?)](/documentation/metalperformanceshaders/mpsndarray/3131729-exportdata)
- [func exportData(with: any MTLCommandBuffer, to: [MPSImage], offset: MPSImageCoordinate)](/documentation/metalperformanceshaders/mpsndarray/3152526-exportdata)
- [func importData(with: any MTLCommandBuffer, from: [MPSImage], offset: MPSImageCoordinate)](/documentation/metalperformanceshaders/mpsndarray/3152527-importdata)
- [func importData(with: any MTLCommandBuffer, from: any MTLBuffer, sourceDataType: MPSDataType, offset: Int, rowStrides: UnsafeMutablePointer<Int>?)](/documentation/metalperformanceshaders/mpsndarray/3131730-importdata)
- [func length(ofDimension: Int) -> Int](/documentation/metalperformanceshaders/mpsndarray/3114053-length)
- [func readBytes(UnsafeMutableRawPointer, strideBytes: UnsafeMutablePointer<Int>?)](/documentation/metalperformanceshaders/mpsndarray/3114057-readbytes)
- [func resourceSize() -> Int](/documentation/metalperformanceshaders/mpsndarray/3114058-resourcesize)
- [func synchronize(on: any MTLCommandBuffer)](/documentation/metalperformanceshaders/mpsndarray/3114059-synchronize)
- [func userBuffer() -> (any MTLBuffer)?](/documentation/metalperformanceshaders/mpsndarray/4408695-userbuffer)
- [func writeBytes(UnsafeMutableRawPointer, strideBytes: UnsafeMutablePointer<Int>?)](/documentation/metalperformanceshaders/mpsndarray/3114060-writebytes)

### Type Methods

- [class func defaultAllocator() -> any MPSNDArrayAllocator](/documentation/metalperformanceshaders/mpsndarray/3131728-defaultallocator)
- [MPSNDArrayAffineInt4Dequantize](/documentation/metalperformanceshaders/mpsndarrayaffineint4dequantize)

### Initializers

- [init(device: any MTLDevice, quantizationDescriptor: MPSNDArrayAffineQuantizationDescriptor)](/documentation/metalperformanceshaders/mpsndarrayaffineint4dequantize/4446149-init)
- [MPSNDArrayAffineQuantizationDescriptor](/documentation/metalperformanceshaders/mpsndarrayaffinequantizationdescriptor)

### Initializers

- [init()](/documentation/metalperformanceshaders/mpsndarrayaffinequantizationdescriptor/4446136-init)
- [init(dataType: MPSDataType, hasZeroPoint: Bool, hasMinValue: Bool)](/documentation/metalperformanceshaders/mpsndarrayaffinequantizationdescriptor/4446137-init)

### Instance Properties

- [var hasMinValue: Bool](/documentation/metalperformanceshaders/mpsndarrayaffinequantizationdescriptor/4446134-hasminvalue)
- [var hasZeroPoint: Bool](/documentation/metalperformanceshaders/mpsndarrayaffinequantizationdescriptor/4446135-haszeropoint)
- [var implicitZeroPoint: Bool](/documentation/metalperformanceshaders/mpsndarrayaffinequantizationdescriptor/4462739-implicitzeropoint)
- [MPSNDArrayBinaryKernel](/documentation/metalperformanceshaders/mpsndarraybinarykernel)

### Initializers

- [init(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3175005-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143501-init)

### Instance Properties

- [var primaryDilationRates: MPSNDArraySizes](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143502-primarydilationrates)
- [var primaryEdgeMode: MPSImageEdgeMode](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143503-primaryedgemode)
- [var primaryKernelSizes: MPSNDArraySizes](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143504-primarykernelsizes)
- [var primaryOffsets: MPSNDArrayOffsets](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143505-primaryoffsets)
- [var primaryStrides: MPSNDArrayOffsets](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143506-primarystrides)
- [var secondaryDilationRates: MPSNDArraySizes](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143507-secondarydilationrates)
- [var secondaryEdgeMode: MPSImageEdgeMode](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143508-secondaryedgemode)
- [var secondaryKernelSizes: MPSNDArraySizes](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143509-secondarykernelsizes)
- [var secondaryOffsets: MPSNDArrayOffsets](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143510-secondaryoffsets)
- [var secondaryStrides: MPSNDArrayOffsets](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143511-secondarystrides)

### Instance Methods

- [func encode(to: any MTLCommandBuffer, primarySourceArray: MPSNDArray, secondarySourceArray: MPSNDArray) -> MPSNDArray](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143497-encode)
- [func encode(to: any MTLCommandBuffer, primarySourceArray: MPSNDArray, secondarySourceArray: MPSNDArray, destinationArray: MPSNDArray)](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143498-encode)
- [func encode(to: any MTLCommandBuffer, primarySourceArray: MPSNDArray, secondarySourceArray: MPSNDArray, resultState: MPSState?, destinationArray: MPSNDArray)](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143499-encode)
- [func encode(to: any MTLCommandBuffer, primarySourceArray: MPSNDArray, secondarySourceArray: MPSNDArray, resultState: AutoreleasingUnsafeMutablePointer<MPSState?>?, outputStateIsTemporary: Bool) -> MPSNDArray](/documentation/metalperformanceshaders/mpsndarraybinarykernel/3143500-encode)
- [MPSNDArrayBinaryPrimaryGradientKernel](/documentation/metalperformanceshaders/mpsndarraybinaryprimarygradientkernel)

### Initializers

- [init(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarraybinaryprimarygradientkernel/3175006-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarraybinaryprimarygradientkernel/3143515-init)

### Instance Methods

- [func encode(to: any MTLCommandBuffer, primarySourceArray: MPSNDArray, secondarySourceArray: MPSNDArray, sourceGradient: MPSNDArray, gradientState: MPSState) -> MPSNDArray](/documentation/metalperformanceshaders/mpsndarraybinaryprimarygradientkernel/3143513-encode)
- [func encode(to: any MTLCommandBuffer, primarySourceArray: MPSNDArray, secondarySourceArray: MPSNDArray, sourceGradient: MPSNDArray, gradientState: MPSState, destinationArray: MPSNDArray)](/documentation/metalperformanceshaders/mpsndarraybinaryprimarygradientkernel/3143514-encode)
- [MPSNDArrayBinarySecondaryGradientKernel](/documentation/metalperformanceshaders/mpsndarraybinarysecondarygradientkernel)

### Initializers

- [init(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarraybinarysecondarygradientkernel/3175007-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarraybinarysecondarygradientkernel/3143519-init)

### Instance Methods

- [func encode(to: any MTLCommandBuffer, primarySourceArray: MPSNDArray, secondarySourceArray: MPSNDArray, sourceGradient: MPSNDArray, gradientState: MPSState) -> MPSNDArray](/documentation/metalperformanceshaders/mpsndarraybinarysecondarygradientkernel/3143517-encode)
- [func encode(to: any MTLCommandBuffer, primarySourceArray: MPSNDArray, secondarySourceArray: MPSNDArray, sourceGradient: MPSNDArray, gradientState: MPSState, destinationArray: MPSNDArray)](/documentation/metalperformanceshaders/mpsndarraybinarysecondarygradientkernel/3143518-encode)
- [MPSNDArrayDescriptor](/documentation/metalperformanceshaders/mpsndarraydescriptor)

### Initializers

- [init(dataType: MPSDataType, dimensionCount: Int, dimensionSizes: UnsafeMutablePointer<Int>)](/documentation/metalperformanceshaders/mpsndarraydescriptor/3114063-init)
- [init(dataType: MPSDataType, shape: [NSNumber])](/documentation/metalperformanceshaders/mpsndarraydescriptor/3143491-init)

### Instance Properties

- [var dataType: MPSDataType](/documentation/metalperformanceshaders/mpsndarraydescriptor/3114062-datatype)
- [var numberOfDimensions: Int](/documentation/metalperformanceshaders/mpsndarraydescriptor/3114067-numberofdimensions)
- [var preferPackedRows: Bool](/documentation/metalperformanceshaders/mpsndarraydescriptor/4423114-preferpackedrows)

### Instance Methods

- [func dimensionOrder() -> vector_uchar16](/documentation/metalperformanceshaders/mpsndarraydescriptor/3114065-dimensionorder)
- [func getShape() -> [NSNumber]](/documentation/metalperformanceshaders/mpsndarraydescriptor/4423112-getshape)
- [func length(ofDimension: Int) -> Int](/documentation/metalperformanceshaders/mpsndarraydescriptor/3114066-length)
- [func permute(withDimensionOrder: UnsafeMutablePointer<Int>)](/documentation/metalperformanceshaders/mpsndarraydescriptor/4423113-permute)
- [func reshape(withDimensionCount: Int, dimensionSizes: UnsafeMutablePointer<Int>)](/documentation/metalperformanceshaders/mpsndarraydescriptor/3143492-reshape)
- [func reshape(withShape: [NSNumber])](/documentation/metalperformanceshaders/mpsndarraydescriptor/3143493-reshape)
- [func sliceDimension(Int, withSubrange: MPSDimensionSlice)](/documentation/metalperformanceshaders/mpsndarraydescriptor/3114069-slicedimension)
- [func sliceRange(forDimension: Int) -> MPSDimensionSlice](/documentation/metalperformanceshaders/mpsndarraydescriptor/3114070-slicerange)
- [func transposeDimension(Int, withDimension: Int)](/documentation/metalperformanceshaders/mpsndarraydescriptor/3114071-transposedimension)
- [MPSNDArrayGather](/documentation/metalperformanceshaders/mpsndarraygather)

### Instance Properties

- [var axis: Int](/documentation/metalperformanceshaders/mpsndarraygather/3152529-axis)
- [MPSNDArrayGatherGradient](/documentation/metalperformanceshaders/mpsndarraygathergradient)
- [MPSNDArrayGatherGradientState](/documentation/metalperformanceshaders/mpsndarraygathergradientstate)
- [MPSNDArrayGradientState](/documentation/metalperformanceshaders/mpsndarraygradientstate)
- [MPSNDArrayIdentity](/documentation/metalperformanceshaders/mpsndarrayidentity)

### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarrayidentity/4438555-init)

### Instance Methods

- [func reshape(with: (any MTLComputeCommandEncoder)?, commandBuffer: (any MTLCommandBuffer)?, sourceArray: MPSNDArray, dimensionCount: Int, dimensionSizes: UnsafeMutablePointer<Int>, destinationArray: MPSNDArray?) -> MPSNDArray?](/documentation/metalperformanceshaders/mpsndarrayidentity/4438558-reshape)
- [func reshape(with: (any MTLComputeCommandEncoder)?, commandBuffer: (any MTLCommandBuffer)?, sourceArray: MPSNDArray, shape: [NSNumber], destinationArray: MPSNDArray?) -> MPSNDArray?](/documentation/metalperformanceshaders/mpsndarrayidentity/4438559-reshape)
- [func reshape(with: (any MTLCommandBuffer)?, sourceArray: MPSNDArray, dimensionCount: Int, dimensionSizes: UnsafeMutablePointer<Int>, destinationArray: MPSNDArray?) -> MPSNDArray?](/documentation/metalperformanceshaders/mpsndarrayidentity/4438556-reshape)
- [func reshape(with: (any MTLCommandBuffer)?, sourceArray: MPSNDArray, shape: [NSNumber], destinationArray: MPSNDArray?) -> MPSNDArray?](/documentation/metalperformanceshaders/mpsndarrayidentity/4438557-reshape)
- [MPSNDArrayLUTDequantize](/documentation/metalperformanceshaders/mpsndarraylutdequantize)

### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarraylutdequantize/4446151-init)
- [MPSNDArrayLUTQuantizationDescriptor](/documentation/metalperformanceshaders/mpsndarraylutquantizationdescriptor)

### Initializers

- [init(dataType: MPSDataType)](/documentation/metalperformanceshaders/mpsndarraylutquantizationdescriptor/4446139-init)
- [init(dataType: MPSDataType, vectorAxis: Int)](/documentation/metalperformanceshaders/mpsndarraylutquantizationdescriptor/4446140-init)
- [MPSNDArrayMatrixMultiplication](/documentation/metalperformanceshaders/mpsndarraymatrixmultiplication)

### Instance Properties

- [var alpha: Double](/documentation/metalperformanceshaders/mpsndarraymatrixmultiplication/3131760-alpha)
- [var beta: Double](/documentation/metalperformanceshaders/mpsndarraymatrixmultiplication/3131761-beta)
- [MPSNDArrayMultiaryBase](/documentation/metalperformanceshaders/mpsndarraymultiarybase)

### Initializers

- [init(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarraymultiarybase/3131740-init)
- [init(device: any MTLDevice, sourceCount: Int)](/documentation/metalperformanceshaders/mpsndarraymultiarybase/3131741-init)

### Instance Properties

- [var destinationArrayAllocator: any MPSNDArrayAllocator](/documentation/metalperformanceshaders/mpsndarraymultiarybase/3131735-destinationarrayallocator)

### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpsndarraymultiarybase/3131734-copy)
- [func destinationArrayDescriptor(forSourceArrays: [MPSNDArray], sourceState: MPSState?) -> MPSNDArrayDescriptor](/documentation/metalperformanceshaders/mpsndarraymultiarybase/3131736-destinationarraydescriptor)
- [func dilationRates(forSourceIndex: Int) -> MPSNDArraySizes](/documentation/metalperformanceshaders/mpsndarraymultiarybase/3131737-dilationrates)
- [func edgeMode(atSourceIndex: Int) -> MPSImageEdgeMode](/documentation/metalperformanceshaders/mpsndarraymultiarybase/3131738-edgemode)
- [func encode(with: NSCoder)](/documentation/metalperformanceshaders/mpsndarraymultiarybase/3131739-encode)
- [func kernelSizes(forSourceIndex: Int) -> MPSNDArraySizes](/documentation/metalperformanceshaders/mpsndarraymultiarybase/3131742-kernelsizes)
- [func offsets(atSourceIndex: Int) -> MPSNDArrayOffsets](/documentation/metalperformanceshaders/mpsndarraymultiarybase/3131743-offsets)
- [func resultState(forSourceArrays: [MPSNDArray], sourceStates: [MPSState]?, destinationArray: MPSNDArray) -> MPSState?](/documentation/metalperformanceshaders/mpsndarraymultiarybase/3143521-resultstate)
- [func strides(forSourceIndex: Int) -> MPSNDArrayOffsets](/documentation/metalperformanceshaders/mpsndarraymultiarybase/3131749-strides)
- [MPSNDArrayMultiaryGradientKernel](/documentation/metalperformanceshaders/mpsndarraymultiarygradientkernel)

### Initializers

- [init(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarraymultiarygradientkernel/3175008-init)
- [init(device: any MTLDevice, sourceCount: Int, sourceGradientIndex: Int)](/documentation/metalperformanceshaders/mpsndarraymultiarygradientkernel/3143524-init)

### Instance Methods

- [func encode(to: any MTLCommandBuffer, sourceArrays: [MPSNDArray], sourceGradient: MPSNDArray, gradientState: MPSState) -> MPSNDArray](/documentation/metalperformanceshaders/mpsndarraymultiarygradientkernel/3143522-encode)
- [func encode(to: any MTLCommandBuffer, sourceArrays: [MPSNDArray], sourceGradient: MPSNDArray, gradientState: MPSState, destinationArray: MPSNDArray)](/documentation/metalperformanceshaders/mpsndarraymultiarygradientkernel/3143523-encode)
- [MPSNDArrayMultiaryKernel](/documentation/metalperformanceshaders/mpsndarraymultiarykernel)

### Initializers

- [init(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarraymultiarykernel/3175009-init)
- [init(device: any MTLDevice, sourceCount: Int)](/documentation/metalperformanceshaders/mpsndarraymultiarykernel/3175010-init)

### Instance Methods

- [func encode(to: (any MTLComputeCommandEncoder)?, commandBuffer: any MTLCommandBuffer, sourceArrays: [MPSNDArray], destinationArray: MPSNDArray)](/documentation/metalperformanceshaders/mpsndarraymultiarykernel/4462738-encode)
- [func encode(to: any MTLCommandBuffer, sourceArrays: [MPSNDArray]) -> MPSNDArray](/documentation/metalperformanceshaders/mpsndarraymultiarykernel/3143525-encode)
- [func encode(to: any MTLCommandBuffer, sourceArrays: [MPSNDArray], destinationArray: MPSNDArray)](/documentation/metalperformanceshaders/mpsndarraymultiarykernel/3143526-encode)
- [func encode(to: any MTLCommandBuffer, sourceArrays: [MPSNDArray], resultState: MPSState?, destinationArray: MPSNDArray)](/documentation/metalperformanceshaders/mpsndarraymultiarykernel/3143527-encode)
- [func encode(to: any MTLCommandBuffer, sourceArrays: [MPSNDArray], resultState: AutoreleasingUnsafeMutablePointer<MPSState?>?, outputStateIsTemporary: Bool) -> MPSNDArray](/documentation/metalperformanceshaders/mpsndarraymultiarykernel/3143528-encode)
- [MPSNDArrayQuantizationDescriptor](/documentation/metalperformanceshaders/mpsndarrayquantizationdescriptor)

### Instance Properties

- [var quantizationDataType: MPSDataType](/documentation/metalperformanceshaders/mpsndarrayquantizationdescriptor/4446142-quantizationdatatype)
- [var quantizationScheme: MPSNDArrayQuantizationScheme](/documentation/metalperformanceshaders/mpsndarrayquantizationdescriptor/4446143-quantizationscheme)
- [MPSNDArrayQuantizedMatrixMultiplication](/documentation/metalperformanceshaders/mpsndarrayquantizedmatrixmultiplication)

### Initializers

- [init(device: any MTLDevice, leftQuantizationDescriptor: MPSNDArrayQuantizationDescriptor?, rightQuantizationDescriptor: MPSNDArrayQuantizationDescriptor?)](/documentation/metalperformanceshaders/mpsndarrayquantizedmatrixmultiplication/4446153-init)
- [MPSNDArrayStridedSlice](/documentation/metalperformanceshaders/mpsndarraystridedslice)

### Instance Properties

- [var strides: MPSNDArrayOffsets](/documentation/metalperformanceshaders/mpsndarraystridedslice/3143546-strides)
- [MPSNDArrayStridedSliceGradient](/documentation/metalperformanceshaders/mpsndarraystridedslicegradient)
- [MPSNDArrayUnaryGradientKernel](/documentation/metalperformanceshaders/mpsndarrayunarygradientkernel)

### Initializers

- [init(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarrayunarygradientkernel/3175011-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarrayunarygradientkernel/3143532-init)

### Instance Methods

- [func encode(to: any MTLCommandBuffer, sourceArray: MPSNDArray, sourceGradient: MPSNDArray, gradientState: MPSState) -> MPSNDArray](/documentation/metalperformanceshaders/mpsndarrayunarygradientkernel/3143530-encode)
- [func encode(to: any MTLCommandBuffer, sourceArray: MPSNDArray, sourceGradient: MPSNDArray, gradientState: MPSState, destinationArray: MPSNDArray)](/documentation/metalperformanceshaders/mpsndarrayunarygradientkernel/3143531-encode)
- [MPSNDArrayUnaryKernel](/documentation/metalperformanceshaders/mpsndarrayunarykernel)

### Initializers

- [init(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarrayunarykernel/3175012-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsndarrayunarykernel/3143540-init)

### Instance Properties

- [var dilationRates: MPSNDArraySizes](/documentation/metalperformanceshaders/mpsndarrayunarykernel/3143534-dilationrates)
- [var edgeMode: MPSImageEdgeMode](/documentation/metalperformanceshaders/mpsndarrayunarykernel/3143535-edgemode)
- [var kernelSizes: MPSNDArraySizes](/documentation/metalperformanceshaders/mpsndarrayunarykernel/3143541-kernelsizes)
- [var offsets: MPSNDArrayOffsets](/documentation/metalperformanceshaders/mpsndarrayunarykernel/3143542-offsets)
- [var strides: MPSNDArrayOffsets](/documentation/metalperformanceshaders/mpsndarrayunarykernel/3143543-strides)

### Instance Methods

- [func encode(to: any MTLCommandBuffer, sourceArray: MPSNDArray) -> MPSNDArray](/documentation/metalperformanceshaders/mpsndarrayunarykernel/3143536-encode)
- [func encode(to: any MTLCommandBuffer, sourceArray: MPSNDArray, destinationArray: MPSNDArray)](/documentation/metalperformanceshaders/mpsndarrayunarykernel/3143537-encode)
- [func encode(to: any MTLCommandBuffer, sourceArray: MPSNDArray, resultState: MPSState?, destinationArray: MPSNDArray)](/documentation/metalperformanceshaders/mpsndarrayunarykernel/3143538-encode)
- [func encode(to: any MTLCommandBuffer, sourceArray: MPSNDArray, resultState: AutoreleasingUnsafeMutablePointer<MPSState?>?, outputStateIsTemporary: Bool) -> MPSNDArray](/documentation/metalperformanceshaders/mpsndarrayunarykernel/3143539-encode)
- [MPSNDArrayVectorLUTDequantize](/documentation/metalperformanceshaders/mpsndarrayvectorlutdequantize)

### Initializers

- [init(device: any MTLDevice, axis: Int)](/documentation/metalperformanceshaders/mpsndarrayvectorlutdequantize/4446155-init)

### Instance Properties

- [var vectorAxis: Int](/documentation/metalperformanceshaders/mpsndarrayvectorlutdequantize/4446156-vectoraxis)
- [MPSNNCompare](/documentation/metalperformanceshaders/mpsnncompare)

### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnncompare/3037375-init)

### Instance Properties

- [var comparisonType: MPSNNComparisonType](/documentation/metalperformanceshaders/mpsnncompare/3037374-comparisontype)
- [var threshold: Float](/documentation/metalperformanceshaders/mpsnncompare/3037376-threshold)
- [MPSNNComparisonNode](/documentation/metalperformanceshaders/mpsnncomparisonnode)

### Instance Properties

- [var comparisonType: MPSNNComparisonType](/documentation/metalperformanceshaders/mpsnncomparisonnode/3037389-comparisontype)
- [MPSNNCropAndResizeBilinear](/documentation/metalperformanceshaders/mpsnncropandresizebilinear)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnncropandresizebilinear/3013788-init)
- [init(device: any MTLDevice, resizeWidth: Int, resizeHeight: Int, numberOfRegions: Int, regions: UnsafePointer<MPSRegion>)](/documentation/metalperformanceshaders/mpsnncropandresizebilinear/3013789-init)

### Instance Properties

- [var numberOfRegions: Int](/documentation/metalperformanceshaders/mpsnncropandresizebilinear/3013790-numberofregions)
- [var regions: UnsafePointer<MPSRegion>](/documentation/metalperformanceshaders/mpsnncropandresizebilinear/3013791-regions)
- [var resizeHeight: Int](/documentation/metalperformanceshaders/mpsnncropandresizebilinear/3013792-resizeheight)
- [var resizeWidth: Int](/documentation/metalperformanceshaders/mpsnncropandresizebilinear/3013793-resizewidth)
- [MPSNNForwardLoss](/documentation/metalperformanceshaders/mpsnnforwardloss)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnforwardloss/3131801-init)
- [init(device: any MTLDevice, lossDescriptor: MPSCNNLossDescriptor)](/documentation/metalperformanceshaders/mpsnnforwardloss/3131802-init)

### Instance Properties

- [var delta: Float](/documentation/metalperformanceshaders/mpsnnforwardloss/3131797-delta)
- [var epsilon: Float](/documentation/metalperformanceshaders/mpsnnforwardloss/3131800-epsilon)
- [var labelSmoothing: Float](/documentation/metalperformanceshaders/mpsnnforwardloss/3131803-labelsmoothing)
- [var lossType: MPSCNNLossType](/documentation/metalperformanceshaders/mpsnnforwardloss/3131804-losstype)
- [var numberOfClasses: Int](/documentation/metalperformanceshaders/mpsnnforwardloss/3131805-numberofclasses)
- [var reduceAcrossBatch: Bool](/documentation/metalperformanceshaders/mpsnnforwardloss/3547985-reduceacrossbatch)
- [var reductionType: MPSCNNReductionType](/documentation/metalperformanceshaders/mpsnnforwardloss/3131806-reductiontype)
- [var weight: Float](/documentation/metalperformanceshaders/mpsnnforwardloss/3131807-weight)

### Instance Methods

- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], labels: [MPSImage], weights: [MPSImage]?, destinationStates: [MPSState]?, destinationImages: [MPSImage])](/documentation/metalperformanceshaders/mpsnnforwardloss/3131798-encodebatch)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceImages: [MPSImage], labels: [MPSImage], weights: [MPSImage]?, outStates: AutoreleasingUnsafeMutablePointer<NSArray?>?, isTemporary: Bool) -> [MPSImage]](/documentation/metalperformanceshaders/mpsnnforwardloss/3131799-encodebatch)
- [MPSNNForwardLossNode](/documentation/metalperformanceshaders/mpsnnforwardlossnode)

### Initializers

- [init(source: MPSNNImageNode, labels: MPSNNImageNode, lossDescriptor: MPSCNNLossDescriptor)](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131832-init)
- [init(source: MPSNNImageNode, labels: MPSNNImageNode, weights: MPSNNImageNode?, lossDescriptor: MPSCNNLossDescriptor)](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131833-init)
- [init(source: MPSNNImageNode, labels: MPSNNImageNode, weights: MPSNNImageNode, lossDescriptor: MPSCNNLossDescriptor)](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131838-init)
- [init(sources: [MPSNNImageNode], lossDescriptor: MPSCNNLossDescriptor)](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131834-init)

### Instance Properties

- [var delta: Float](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131826-delta)
- [var epsilon: Float](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131827-epsilon)
- [var labelSmoothing: Float](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131835-labelsmoothing)
- [var lossType: MPSCNNLossType](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131836-losstype)
- [var numberOfClasses: Int](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131840-numberofclasses)
- [var propertyCallBack: (any MPSNNLossCallback)?](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131841-propertycallback)
- [var reduceAcrossBatch: Bool](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3547987-reduceacrossbatch)
- [var reductionType: MPSCNNReductionType](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131842-reductiontype)
- [var weight: Float](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131843-weight)

### Instance Methods

- [func gradientFilter(withSource: MPSNNImageNode) -> MPSNNLossGradientNode](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131828-gradientfilter)
- [func gradientFilter(withSources: [MPSNNImageNode]) -> MPSNNLossGradientNode](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131829-gradientfilter)
- [func gradientFilters(withSource: MPSNNImageNode) -> [MPSNNLossGradientNode]](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131830-gradientfilters)
- [func gradientFilters(withSources: [MPSNNImageNode]) -> [MPSNNLossGradientNode]](/documentation/metalperformanceshaders/mpsnnforwardlossnode/3131831-gradientfilters)
- [MPSNNGramMatrixCalculation](/documentation/metalperformanceshaders/mpsnngrammatrixcalculation)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnngrammatrixcalculation/3114078-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnngrammatrixcalculation/3114079-init)
- [init(device: any MTLDevice, alpha: Float)](/documentation/metalperformanceshaders/mpsnngrammatrixcalculation/3114080-init)

### Instance Properties

- [var alpha: Float](/documentation/metalperformanceshaders/mpsnngrammatrixcalculation/3114077-alpha)
- [MPSNNGramMatrixCalculationGradient](/documentation/metalperformanceshaders/mpsnngrammatrixcalculationgradient)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnngrammatrixcalculationgradient/3114083-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnngrammatrixcalculationgradient/3114084-init)
- [init(device: any MTLDevice, alpha: Float)](/documentation/metalperformanceshaders/mpsnngrammatrixcalculationgradient/3114085-init)

### Instance Properties

- [var alpha: Float](/documentation/metalperformanceshaders/mpsnngrammatrixcalculationgradient/3114082-alpha)
- [MPSNNGramMatrixCalculationGradientNode](/documentation/metalperformanceshaders/mpsnngrammatrixcalculationgradientnode)

### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode)](/documentation/metalperformanceshaders/mpsnngrammatrixcalculationgradientnode/3114089-init)
- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode, alpha: Float)](/documentation/metalperformanceshaders/mpsnngrammatrixcalculationgradientnode/3114090-init)

### Instance Properties

- [var alpha: Float](/documentation/metalperformanceshaders/mpsnngrammatrixcalculationgradientnode/3114088-alpha)
- [MPSNNGramMatrixCalculationNode](/documentation/metalperformanceshaders/mpsnngrammatrixcalculationnode)

### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpsnngrammatrixcalculationnode/3114095-init)
- [init(source: MPSNNImageNode, alpha: Float)](/documentation/metalperformanceshaders/mpsnngrammatrixcalculationnode/3114096-init)

### Instance Properties

- [var alpha: Float](/documentation/metalperformanceshaders/mpsnngrammatrixcalculationnode/3114094-alpha)
- [var propertyCallBack: (any MPSNNGramMatrixCallback)?](/documentation/metalperformanceshaders/mpsnngrammatrixcalculationnode/3131844-propertycallback)
- [MPSNNGridSample](/documentation/metalperformanceshaders/mpsnngridsample)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnngridsample/3131870-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnngridsample/3131871-init)

### Instance Properties

- [var useGridValueAsInputCoordinate: Bool](/documentation/metalperformanceshaders/mpsnngridsample/3131872-usegridvalueasinputcoordinate)
- [MPSNNInitialGradient](/documentation/metalperformanceshaders/mpsnninitialgradient)

### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnninitialgradient/3131809-init)
- [MPSNNInitialGradientNode](/documentation/metalperformanceshaders/mpsnninitialgradientnode)

### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpsnninitialgradientnode/3131848-init)
- [MPSNNLocalCorrelation](/documentation/metalperformanceshaders/mpsnnlocalcorrelation)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnlocalcorrelation/3197829-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnlocalcorrelation/3131875-init)
- [init(device: any MTLDevice, windowInX: Int, windowInY: Int, strideInX: Int, strideInY: Int)](/documentation/metalperformanceshaders/mpsnnlocalcorrelation/3131876-init)

### Instance Properties

- [var strideInX: Int](/documentation/metalperformanceshaders/mpsnnlocalcorrelation/3131877-strideinx)
- [var strideInY: Int](/documentation/metalperformanceshaders/mpsnnlocalcorrelation/3131878-strideiny)
- [var windowInX: Int](/documentation/metalperformanceshaders/mpsnnlocalcorrelation/3131879-windowinx)
- [var windowInY: Int](/documentation/metalperformanceshaders/mpsnnlocalcorrelation/3131880-windowiny)
- [MPSNNLossGradient](/documentation/metalperformanceshaders/mpsnnlossgradient)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnlossgradient/3131816-init)
- [init(device: any MTLDevice, lossDescriptor: MPSCNNLossDescriptor)](/documentation/metalperformanceshaders/mpsnnlossgradient/3131817-init)

### Instance Properties

- [var computeLabelGradients: Bool](/documentation/metalperformanceshaders/mpsnnlossgradient/3131811-computelabelgradients)
- [var delta: Float](/documentation/metalperformanceshaders/mpsnnlossgradient/3131812-delta)
- [var epsilon: Float](/documentation/metalperformanceshaders/mpsnnlossgradient/3131815-epsilon)
- [var labelSmoothing: Float](/documentation/metalperformanceshaders/mpsnnlossgradient/3131818-labelsmoothing)
- [var lossType: MPSCNNLossType](/documentation/metalperformanceshaders/mpsnnlossgradient/3131819-losstype)
- [var numberOfClasses: Int](/documentation/metalperformanceshaders/mpsnnlossgradient/3131820-numberofclasses)
- [var reduceAcrossBatch: Bool](/documentation/metalperformanceshaders/mpsnnlossgradient/3547986-reduceacrossbatch)
- [var reductionType: MPSCNNReductionType](/documentation/metalperformanceshaders/mpsnnlossgradient/3131821-reductiontype)
- [var weight: Float](/documentation/metalperformanceshaders/mpsnnlossgradient/3131822-weight)

### Instance Methods

- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceGradients: [MPSImage], sourceImages: [MPSImage], labels: [MPSImage], weights: [MPSImage]?, sourceStates: [MPSState]?) -> [MPSImage]](/documentation/metalperformanceshaders/mpsnnlossgradient/3131813-encodebatch)
- [func encodeBatch(commandBuffer: any MTLCommandBuffer, sourceGradients: [MPSImage], sourceImages: [MPSImage], labels: [MPSImage], weights: [MPSImage]?, sourceStates: [MPSState]?, destinationGradients: [MPSImage])](/documentation/metalperformanceshaders/mpsnnlossgradient/3131814-encodebatch)
- [MPSNNLossGradientNode](/documentation/metalperformanceshaders/mpsnnlossgradientnode)

### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, labels: MPSNNImageNode, gradientState: MPSNNGradientStateNode?, lossDescriptor: MPSCNNLossDescriptor, isLabelsGradientFilter: Bool)](/documentation/metalperformanceshaders/mpsnnlossgradientnode/3131855-init)
- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, labels: MPSNNImageNode, weights: MPSNNImageNode?, gradientState: MPSNNGradientStateNode?, lossDescriptor: MPSCNNLossDescriptor, isLabelsGradientFilter: Bool)](/documentation/metalperformanceshaders/mpsnnlossgradientnode/3131856-init)
- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, labels: MPSNNImageNode, weights: MPSNNImageNode, gradientState: MPSNNGradientStateNode?, lossDescriptor: MPSCNNLossDescriptor, isLabelsGradientFilter: Bool)](/documentation/metalperformanceshaders/mpsnnlossgradientnode/3131862-init)
- [init(sources: [MPSNNImageNode], gradientState: MPSNNGradientStateNode?, lossDescriptor: MPSCNNLossDescriptor, isLabelsGradientFilter: Bool)](/documentation/metalperformanceshaders/mpsnnlossgradientnode/3131857-init)

### Instance Properties

- [var delta: Float](/documentation/metalperformanceshaders/mpsnnlossgradientnode/3131853-delta)
- [var epsilon: Float](/documentation/metalperformanceshaders/mpsnnlossgradientnode/3131854-epsilon)
- [var isLabelsGradientFilter: Bool](/documentation/metalperformanceshaders/mpsnnlossgradientnode/3131858-islabelsgradientfilter)
- [var labelSmoothing: Float](/documentation/metalperformanceshaders/mpsnnlossgradientnode/3131859-labelsmoothing)
- [var lossType: MPSCNNLossType](/documentation/metalperformanceshaders/mpsnnlossgradientnode/3131860-losstype)
- [var numberOfClasses: Int](/documentation/metalperformanceshaders/mpsnnlossgradientnode/3131864-numberofclasses)
- [var propertyCallBack: (any MPSNNLossCallback)?](/documentation/metalperformanceshaders/mpsnnlossgradientnode/3131865-propertycallback)
- [var reduceAcrossBatch: Bool](/documentation/metalperformanceshaders/mpsnnlossgradientnode/3547988-reduceacrossbatch)
- [var reductionType: MPSCNNReductionType](/documentation/metalperformanceshaders/mpsnnlossgradientnode/3131866-reductiontype)
- [var weight: Float](/documentation/metalperformanceshaders/mpsnnlossgradientnode/3131867-weight)
- [MPSNNMultiaryGradientState](/documentation/metalperformanceshaders/mpsnnmultiarygradientstate)
- [MPSNNMultiaryGradientStateNode](/documentation/metalperformanceshaders/mpsnnmultiarygradientstatenode)
- [MPSNNPad](/documentation/metalperformanceshaders/mpsnnpad)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnpad/3037428-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnpad/3037429-init)
- [init(device: any MTLDevice, paddingSizeBefore: MPSImageCoordinate, paddingSizeAfter: MPSImageCoordinate)](/documentation/metalperformanceshaders/mpsnnpad/3037430-init)
- [init(device: any MTLDevice, paddingSizeBefore: MPSImageCoordinate, paddingSizeAfter: MPSImageCoordinate, fillValueArray: Data?)](/documentation/metalperformanceshaders/mpsnnpad/3037431-init)

### Instance Properties

- [var fillValue: Float](/documentation/metalperformanceshaders/mpsnnpad/3037427-fillvalue)
- [var paddingSizeAfter: MPSImageCoordinate](/documentation/metalperformanceshaders/mpsnnpad/3037432-paddingsizeafter)
- [var paddingSizeBefore: MPSImageCoordinate](/documentation/metalperformanceshaders/mpsnnpad/3037433-paddingsizebefore)
- [MPSNNPadGradient](/documentation/metalperformanceshaders/mpsnnpadgradient)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnpadgradient/3037435-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnpadgradient/3037436-init)
- [MPSNNPadGradientNode](/documentation/metalperformanceshaders/mpsnnpadgradientnode)

### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode)](/documentation/metalperformanceshaders/mpsnnpadgradientnode/3037391-init)
- [MPSNNPadNode](/documentation/metalperformanceshaders/mpsnnpadnode)

### Initializers

- [init(source: MPSNNImageNode, paddingSizeBefore: MPSImageCoordinate, paddingSizeAfter: MPSImageCoordinate, edgeMode: MPSImageEdgeMode)](/documentation/metalperformanceshaders/mpsnnpadnode/3037395-init)

### Instance Properties

- [var fillValue: Float](/documentation/metalperformanceshaders/mpsnnpadnode/3037394-fillvalue)
- [MPSNNReductionColumnMaxNode](/documentation/metalperformanceshaders/mpsnnreductioncolumnmaxnode)
- [MPSNNReductionColumnMeanNode](/documentation/metalperformanceshaders/mpsnnreductioncolumnmeannode)
- [MPSNNReductionColumnMinNode](/documentation/metalperformanceshaders/mpsnnreductioncolumnminnode)
- [MPSNNReductionColumnSumNode](/documentation/metalperformanceshaders/mpsnnreductioncolumnsumnode)
- [MPSNNReductionFeatureChannelsArgumentMaxNode](/documentation/metalperformanceshaders/mpsnnreductionfeaturechannelsargumentmaxnode)
- [MPSNNReductionFeatureChannelsArgumentMinNode](/documentation/metalperformanceshaders/mpsnnreductionfeaturechannelsargumentminnode)
- [MPSNNReductionFeatureChannelsMaxNode](/documentation/metalperformanceshaders/mpsnnreductionfeaturechannelsmaxnode)
- [MPSNNReductionFeatureChannelsMeanNode](/documentation/metalperformanceshaders/mpsnnreductionfeaturechannelsmeannode)
- [MPSNNReductionFeatureChannelsMinNode](/documentation/metalperformanceshaders/mpsnnreductionfeaturechannelsminnode)
- [MPSNNReductionFeatureChannelsSumNode](/documentation/metalperformanceshaders/mpsnnreductionfeaturechannelssumnode)

### Instance Properties

- [var weight: Float](/documentation/metalperformanceshaders/mpsnnreductionfeaturechannelssumnode/3037407-weight)
- [MPSNNReductionRowMaxNode](/documentation/metalperformanceshaders/mpsnnreductionrowmaxnode)
- [MPSNNReductionRowMeanNode](/documentation/metalperformanceshaders/mpsnnreductionrowmeannode)
- [MPSNNReductionRowMinNode](/documentation/metalperformanceshaders/mpsnnreductionrowminnode)
- [MPSNNReductionRowSumNode](/documentation/metalperformanceshaders/mpsnnreductionrowsumnode)
- [MPSNNReductionSpatialMeanGradientNode](/documentation/metalperformanceshaders/mpsnnreductionspatialmeangradientnode)

### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode)](/documentation/metalperformanceshaders/mpsnnreductionspatialmeangradientnode/3037413-init)
- [MPSNNReductionSpatialMeanNode](/documentation/metalperformanceshaders/mpsnnreductionspatialmeannode)
- [MPSNNReshapeGradient](/documentation/metalperformanceshaders/mpsnnreshapegradient)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreshapegradient/3037438-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnreshapegradient/3037439-init)
- [MPSNNReshapeGradientNode](/documentation/metalperformanceshaders/mpsnnreshapegradientnode)

### Initializers

- [init(sourceGradient: MPSNNImageNode, sourceImage: MPSNNImageNode, gradientState: MPSNNGradientStateNode)](/documentation/metalperformanceshaders/mpsnnreshapegradientnode/3037417-init)
- [MPSNNReshapeNode](/documentation/metalperformanceshaders/mpsnnreshapenode)

### Initializers

- [init(source: MPSNNImageNode, resultWidth: Int, resultHeight: Int, resultFeatureChannels: Int)](/documentation/metalperformanceshaders/mpsnnreshapenode/3037420-init)
- [MPSNNResizeBilinear](/documentation/metalperformanceshaders/mpsnnresizebilinear)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpsnnresizebilinear/3013794-init)
- [init(device: any MTLDevice, resizeWidth: Int, resizeHeight: Int, alignCorners: Bool)](/documentation/metalperformanceshaders/mpsnnresizebilinear/3012966-init)

### Instance Properties

- [var alignCorners: Bool](/documentation/metalperformanceshaders/mpsnnresizebilinear/3012965-aligncorners)
- [var resizeHeight: Int](/documentation/metalperformanceshaders/mpsnnresizebilinear/3012968-resizeheight)
- [var resizeWidth: Int](/documentation/metalperformanceshaders/mpsnnresizebilinear/3012969-resizewidth)
- [MPSNNUnaryReductionNode](/documentation/metalperformanceshaders/mpsnnunaryreductionnode)

### Initializers

- [init(source: MPSNNImageNode)](/documentation/metalperformanceshaders/mpsnnunaryreductionnode/3037424-init)

### Instance Properties

- [var clipRectSource: MTLRegion](/documentation/metalperformanceshaders/mpsnnunaryreductionnode/3037423-cliprectsource)
- [MPSPolygonAccelerationStructure](/documentation/metalperformanceshaders/mpspolygonaccelerationstructure)

### Instance Properties

- [var indexBuffer: (any MTLBuffer)?](/documentation/metalperformanceshaders/mpspolygonaccelerationstructure/3088894-indexbuffer)
- [var indexBufferOffset: Int](/documentation/metalperformanceshaders/mpspolygonaccelerationstructure/3088895-indexbufferoffset)
- [var indexType: MPSDataType](/documentation/metalperformanceshaders/mpspolygonaccelerationstructure/3088896-indextype)
- [var maskBuffer: (any MTLBuffer)?](/documentation/metalperformanceshaders/mpspolygonaccelerationstructure/3088897-maskbuffer)
- [var maskBufferOffset: Int](/documentation/metalperformanceshaders/mpspolygonaccelerationstructure/3088898-maskbufferoffset)
- [var polygonBuffers: [MPSPolygonBuffer]?](/documentation/metalperformanceshaders/mpspolygonaccelerationstructure/3152577-polygonbuffers)
- [var polygonCount: Int](/documentation/metalperformanceshaders/mpspolygonaccelerationstructure/3088899-polygoncount)
- [var polygonType: MPSPolygonType](/documentation/metalperformanceshaders/mpspolygonaccelerationstructure/3088900-polygontype)
- [var vertexBuffer: (any MTLBuffer)?](/documentation/metalperformanceshaders/mpspolygonaccelerationstructure/3088901-vertexbuffer)
- [var vertexBufferOffset: Int](/documentation/metalperformanceshaders/mpspolygonaccelerationstructure/3088902-vertexbufferoffset)
- [var vertexStride: Int](/documentation/metalperformanceshaders/mpspolygonaccelerationstructure/3088903-vertexstride)
- [MPSPolygonBuffer](/documentation/metalperformanceshaders/mpspolygonbuffer)

### Initializers

- [init()](/documentation/metalperformanceshaders/mpspolygonbuffer/3152582-init)
- [init?(coder: NSCoder)](/documentation/metalperformanceshaders/mpspolygonbuffer/3152583-init)

### Instance Properties

- [var indexBuffer: (any MTLBuffer)?](/documentation/metalperformanceshaders/mpspolygonbuffer/3152580-indexbuffer)
- [var indexBufferOffset: Int](/documentation/metalperformanceshaders/mpspolygonbuffer/3152581-indexbufferoffset)
- [var maskBuffer: (any MTLBuffer)?](/documentation/metalperformanceshaders/mpspolygonbuffer/3152584-maskbuffer)
- [var maskBufferOffset: Int](/documentation/metalperformanceshaders/mpspolygonbuffer/3152585-maskbufferoffset)
- [var polygonCount: Int](/documentation/metalperformanceshaders/mpspolygonbuffer/3152587-polygoncount)
- [var vertexBuffer: (any MTLBuffer)?](/documentation/metalperformanceshaders/mpspolygonbuffer/3152588-vertexbuffer)
- [var vertexBufferOffset: Int](/documentation/metalperformanceshaders/mpspolygonbuffer/3152589-vertexbufferoffset)

### Instance Methods

- [func copy(with: NSZone?) -> Self](/documentation/metalperformanceshaders/mpspolygonbuffer/3152579-copy)
- [MPSPredicate](/documentation/metalperformanceshaders/mpspredicate)

### Initializers

- [init(buffer: any MTLBuffer, offset: Int)](/documentation/metalperformanceshaders/mpspredicate/3114034-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpspredicate/3114035-init)

### Instance Properties

- [var predicateBuffer: any MTLBuffer](/documentation/metalperformanceshaders/mpspredicate/3114036-predicatebuffer)
- [var predicateOffset: Int](/documentation/metalperformanceshaders/mpspredicate/3114037-predicateoffset)
- [MPSQuadrilateralAccelerationStructure](/documentation/metalperformanceshaders/mpsquadrilateralaccelerationstructure)

### Instance Properties

- [var quadrilateralCount: Int](/documentation/metalperformanceshaders/mpsquadrilateralaccelerationstructure/3088909-quadrilateralcount)
- [MPSSVGF](/documentation/metalperformanceshaders/mpssvgf)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpssvgf/3143565-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpssvgf/3143566-init)

### Instance Properties

- [var bilateralFilterRadius: Int](/documentation/metalperformanceshaders/mpssvgf/3143555-bilateralfilterradius)
- [var bilateralFilterSigma: Float](/documentation/metalperformanceshaders/mpssvgf/3143556-bilateralfiltersigma)
- [var channelCount: Int](/documentation/metalperformanceshaders/mpssvgf/3143557-channelcount)
- [var channelCount2: Int](/documentation/metalperformanceshaders/mpssvgf/3143558-channelcount2)
- [var depthWeight: Float](/documentation/metalperformanceshaders/mpssvgf/3143560-depthweight)
- [var luminanceWeight: Float](/documentation/metalperformanceshaders/mpssvgf/3143567-luminanceweight)
- [var minimumFramesForVarianceEstimation: Int](/documentation/metalperformanceshaders/mpssvgf/3143568-minimumframesforvarianceestimati)
- [var normalWeight: Float](/documentation/metalperformanceshaders/mpssvgf/3143569-normalweight)
- [var reprojectionThreshold: Float](/documentation/metalperformanceshaders/mpssvgf/3143570-reprojectionthreshold)
- [var temporalReprojectionBlendFactor: Float](/documentation/metalperformanceshaders/mpssvgf/3143571-temporalreprojectionblendfactor)
- [var temporalWeighting: MPSTemporalWeighting](/documentation/metalperformanceshaders/mpssvgf/3143572-temporalweighting)
- [var varianceEstimationRadius: Int](/documentation/metalperformanceshaders/mpssvgf/3143573-varianceestimationradius)
- [var varianceEstimationSigma: Float](/documentation/metalperformanceshaders/mpssvgf/3143574-varianceestimationsigma)
- [var variancePrefilterRadius: Int](/documentation/metalperformanceshaders/mpssvgf/3143575-varianceprefilterradius)
- [var variancePrefilterSigma: Float](/documentation/metalperformanceshaders/mpssvgf/3143576-varianceprefiltersigma)

### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpssvgf/3143559-copy)
- [func encode(with: NSCoder)](/documentation/metalperformanceshaders/mpssvgf/3143564-encode)
- [func encodeBilateralFilter(to: any MTLCommandBuffer, stepDistance: Int, sourceTexture: any MTLTexture, destinationTexture: any MTLTexture, depthNormalTexture: any MTLTexture)](/documentation/metalperformanceshaders/mpssvgf/3242891-encodebilateralfilter)
- [func encodeBilateralFilter(to: any MTLCommandBuffer, stepDistance: Int, sourceTexture: any MTLTexture, destinationTexture: any MTLTexture, sourceTexture2: (any MTLTexture)?, destinationTexture2: (any MTLTexture)?, depthNormalTexture: any MTLTexture)](/documentation/metalperformanceshaders/mpssvgf/3143561-encodebilateralfilter)
- [func encodeReprojection(to: any MTLCommandBuffer, sourceTexture: any MTLTexture, previousTexture: any MTLTexture, destinationTexture: any MTLTexture, previousLuminanceMomentsTexture: any MTLTexture, destinationLuminanceMomentsTexture: any MTLTexture, previousFrameCount: any MTLTexture, destinationFrameCount: any MTLTexture, motionVectorTexture: (any MTLTexture)?, depthNormalTexture: (any MTLTexture)?, previousDepthNormalTexture: (any MTLTexture)?)](/documentation/metalperformanceshaders/mpssvgf/3242892-encodereprojection)
- [func encodeReprojection(to: any MTLCommandBuffer, sourceTexture: any MTLTexture, previousTexture: any MTLTexture, destinationTexture: any MTLTexture, previousLuminanceMomentsTexture: any MTLTexture, destinationLuminanceMomentsTexture: any MTLTexture, sourceTexture2: (any MTLTexture)?, previousTexture2: (any MTLTexture)?, destinationTexture2: (any MTLTexture)?, previousLuminanceMomentsTexture2: (any MTLTexture)?, destinationLuminanceMomentsTexture2: (any MTLTexture)?, previousFrameCount: any MTLTexture, destinationFrameCount: any MTLTexture, motionVectorTexture: (any MTLTexture)?, depthNormalTexture: (any MTLTexture)?, previousDepthNormalTexture: (any MTLTexture)?)](/documentation/metalperformanceshaders/mpssvgf/3143562-encodereprojection)
- [func encodeVarianceEstimation(to: any MTLCommandBuffer, sourceTexture: any MTLTexture, luminanceMomentsTexture: any MTLTexture, destinationTexture: any MTLTexture, frameCount: any MTLTexture, depthNormalTexture: (any MTLTexture)?)](/documentation/metalperformanceshaders/mpssvgf/3242893-encodevarianceestimation)
- [func encodeVarianceEstimation(to: any MTLCommandBuffer, sourceTexture: any MTLTexture, luminanceMomentsTexture: any MTLTexture, destinationTexture: any MTLTexture, sourceTexture2: (any MTLTexture)?, luminanceMomentsTexture2: (any MTLTexture)?, destinationTexture2: (any MTLTexture)?, frameCount: any MTLTexture, depthNormalTexture: (any MTLTexture)?)](/documentation/metalperformanceshaders/mpssvgf/3143563-encodevarianceestimation)
- [MPSSVGFDefaultTextureAllocator](/documentation/metalperformanceshaders/mpssvgfdefaulttextureallocator)

### Initializers

- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpssvgfdefaulttextureallocator/3242897-init)

### Instance Properties

- [var allocatedTextureCount: Int](/documentation/metalperformanceshaders/mpssvgfdefaulttextureallocator/3242895-allocatedtexturecount)
- [var device: any MTLDevice](/documentation/metalperformanceshaders/mpssvgfdefaulttextureallocator/3242896-device)

### Instance Methods

- [func reset()](/documentation/metalperformanceshaders/mpssvgfdefaulttextureallocator/3242898-reset)
- [func `return`(any MTLTexture)](/documentation/metalperformanceshaders/mpssvgfdefaulttextureallocator/3242899-return)
- [func texture(with: MTLPixelFormat, width: Int, height: Int) -> (any MTLTexture)?](/documentation/metalperformanceshaders/mpssvgfdefaulttextureallocator/3242900-texture)
- [MPSSVGFDenoiser](/documentation/metalperformanceshaders/mpssvgfdenoiser)

### Initializers

- [init(SVGF: MPSSVGF, textureAllocator: any MPSSVGFTextureAllocator)](/documentation/metalperformanceshaders/mpssvgfdenoiser/3242908-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpssvgfdenoiser/3353094-init)

### Instance Properties

- [var bilateralFilterIterations: Int](/documentation/metalperformanceshaders/mpssvgfdenoiser/3242902-bilateralfilteriterations)
- [var svgf: MPSSVGF](/documentation/metalperformanceshaders/mpssvgfdenoiser/3242914-svgf)
- [var textureAllocator: any MPSSVGFTextureAllocator](/documentation/metalperformanceshaders/mpssvgfdenoiser/3242915-textureallocator)

### Instance Methods

- [func clearTemporalHistory()](/documentation/metalperformanceshaders/mpssvgfdenoiser/3242903-cleartemporalhistory)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceTexture: any MTLTexture, destinationTexture: AutoreleasingUnsafeMutablePointer<any MTLTexture>, sourceTexture2: (any MTLTexture)?, destinationTexture2: AutoreleasingUnsafeMutablePointer<any MTLTexture>?, motionVectorTexture: (any MTLTexture)?, depthNormalTexture: any MTLTexture, previousDepthNormalTexture: (any MTLTexture)?)](/documentation/metalperformanceshaders/mpssvgfdenoiser/3353092-encode)
- [func encode(commandBuffer: any MTLCommandBuffer, sourceTexture: any MTLTexture, motionVectorTexture: (any MTLTexture)?, depthNormalTexture: any MTLTexture, previousDepthNormalTexture: (any MTLTexture)?) -> any MTLTexture](/documentation/metalperformanceshaders/mpssvgfdenoiser/3353093-encode)
- [func releaseTemporaryTextures()](/documentation/metalperformanceshaders/mpssvgfdenoiser/3242911-releasetemporarytextures)
- [MPSStateResourceList](/documentation/metalperformanceshaders/mpsstateresourcelist)

### Initializers

- [init()](/documentation/metalperformanceshaders/mpsstateresourcelist/2947897-init)

### Instance Methods

- [func appendBuffer(Int)](/documentation/metalperformanceshaders/mpsstateresourcelist/2947905-appendbuffer)
- [func appendTexture(MTLTextureDescriptor)](/documentation/metalperformanceshaders/mpsstateresourcelist/2947894-appendtexture)
- [MPSTemporalAA](/documentation/metalperformanceshaders/mpstemporalaa)

### Initializers

- [init?(coder: NSCoder, device: any MTLDevice)](/documentation/metalperformanceshaders/mpstemporalaa/3143586-init)
- [init(device: any MTLDevice)](/documentation/metalperformanceshaders/mpstemporalaa/3143587-init)

### Instance Properties

- [var blendFactor: Float](/documentation/metalperformanceshaders/mpstemporalaa/3143582-blendfactor)

### Instance Methods

- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpstemporalaa/3143583-copy)
- [func encode(to: any MTLCommandBuffer, sourceTexture: any MTLTexture, previousTexture: any MTLTexture, destinationTexture: any MTLTexture, motionVectorTexture: (any MTLTexture)?, depthTexture: (any MTLTexture)?)](/documentation/metalperformanceshaders/mpstemporalaa/3143584-encode)
- [func encode(with: NSCoder)](/documentation/metalperformanceshaders/mpstemporalaa/3143585-encode)
- [MPSTemporaryNDArray](/documentation/metalperformanceshaders/mpstemporaryndarray)

### Initializers

- [init(commandBuffer: any MTLCommandBuffer, descriptor: MPSNDArrayDescriptor)](/documentation/metalperformanceshaders/mpstemporaryndarray/3114075-init)

### Instance Properties

- [var readCount: Int](/documentation/metalperformanceshaders/mpstemporaryndarray/3114074-readcount)

### Type Methods

- [class func defaultAllocator() -> any MPSNDArrayAllocator](/documentation/metalperformanceshaders/mpstemporaryndarray/3131732-defaultallocator)

## Protocols

- [MPSCNNGroupNormalizationDataSource](/documentation/metalperformanceshaders/mpscnngroupnormalizationdatasource)

### Initializers

- [init?(coder: NSCoder)](/documentation/metalperformanceshaders/mpscnngroupnormalizationdatasource/3152548-init)

### Instance Properties

- [var numberOfFeatureChannels: Int](/documentation/metalperformanceshaders/mpscnngroupnormalizationdatasource/3152550-numberoffeaturechannels)
- [var numberOfGroups: Int](/documentation/metalperformanceshaders/mpscnngroupnormalizationdatasource/3152551-numberofgroups)

### Type Properties

- [static var supportsSecureCoding: Bool](/documentation/metalperformanceshaders/mpscnngroupnormalizationdatasource/3152552-supportssecurecoding)

### Instance Methods

- [func beta() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnngroupnormalizationdatasource/3152543-beta)
- [func copy(with: NSZone?, device: (any MTLDevice)?) -> Self](/documentation/metalperformanceshaders/mpscnngroupnormalizationdatasource/3152544-copy)
- [func encode(with: NSCoder)](/documentation/metalperformanceshaders/mpscnngroupnormalizationdatasource/3152545-encode)
- [func epsilon() -> Float](/documentation/metalperformanceshaders/mpscnngroupnormalizationdatasource/3152546-epsilon)
- [func gamma() -> UnsafeMutablePointer<Float>?](/documentation/metalperformanceshaders/mpscnngroupnormalizationdatasource/3152547-gamma)
- [func label() -> String?](/documentation/metalperformanceshaders/mpscnngroupnormalizationdatasource/3152549-label)
- [func updateGammaAndBeta(with: any MTLCommandBuffer, groupNormalizationStateBatch: [MPSCNNGroupNormalizationGradientState]) -> MPSCNNNormalizationGammaAndBetaState?](/documentation/metalperformanceshaders/mpscnngroupnormalizationdatasource/3152553-updategammaandbeta)
- [func updateGammaAndBeta(withGroupNormalizationStateBatch: [MPSCNNGroupNormalizationGradientState]) -> Bool](/documentation/metalperformanceshaders/mpscnngroupnormalizationdatasource/3152554-updategammaandbeta)
- [MPSHeapProvider](/documentation/metalperformanceshaders/mpsheapprovider)

### Instance Methods

- [func newHeap(with: MTLHeapDescriptor) -> (any MTLHeap)?](/documentation/metalperformanceshaders/mpsheapprovider/3229861-newheap)
- [func retire(any MTLHeap, cacheDelay: Double)](/documentation/metalperformanceshaders/mpsheapprovider/3229862-retire)
- [MPSNDArrayAllocator](/documentation/metalperformanceshaders/mpsndarrayallocator)

### Instance Methods

- [func array(for: any MTLCommandBuffer, arrayDescriptor: MPSNDArrayDescriptor, kernel: MPSKernel) -> MPSNDArray](/documentation/metalperformanceshaders/mpsndarrayallocator/3143490-array)
- [MPSNNGramMatrixCallback](/documentation/metalperformanceshaders/mpsnngrammatrixcallback)

### Instance Methods

- [func alpha(forSourceImage: MPSImage, destinationImage: MPSImage) -> Float](/documentation/metalperformanceshaders/mpsnngrammatrixcallback/3131846-alpha)
- [MPSNNLossCallback](/documentation/metalperformanceshaders/mpsnnlosscallback)

### Instance Methods

- [func scalarWeight(forSourceImage: MPSImage, destinationImage: MPSImage) -> Float](/documentation/metalperformanceshaders/mpsnnlosscallback/3131851-scalarweight)
- [MPSSVGFTextureAllocator](/documentation/metalperformanceshaders/mpssvgftextureallocator)

### Instance Methods

- [func `return`(any MTLTexture)](/documentation/metalperformanceshaders/mpssvgftextureallocator/3242917-return)
- [func texture(with: MTLPixelFormat, width: Int, height: Int) -> (any MTLTexture)?](/documentation/metalperformanceshaders/mpssvgftextureallocator/3242918-texture)

## Reference

- [MetalPerformanceShaders Structures](/documentation/metalperformanceshaders/metalperformanceshaders_structures)

### Structures

- [MPSAccelerationStructureUsage](/documentation/metalperformanceshaders/mpsaccelerationstructureusage)

#### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpsaccelerationstructureusage/2998476-init)

#### Type Properties

- [static var frequentRebuild: MPSAccelerationStructureUsage](/documentation/metalperformanceshaders/mpsaccelerationstructureusage/2980778-frequentrebuild)
- [static var preferCPUBuild: MPSAccelerationStructureUsage](/documentation/metalperformanceshaders/mpsaccelerationstructureusage/3152575-prefercpubuild)
- [static var preferGPUBuild: MPSAccelerationStructureUsage](/documentation/metalperformanceshaders/mpsaccelerationstructureusage/3152576-prefergpubuild)
- [static var refit: MPSAccelerationStructureUsage](/documentation/metalperformanceshaders/mpsaccelerationstructureusage/2980780-refit)
- [MPSAliasingStrategy](/documentation/metalperformanceshaders/mpsaliasingstrategy)

#### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpsaliasingstrategy/3114269-init)

#### Type Properties

- [static var aliasingReserved: MPSAliasingStrategy](/documentation/metalperformanceshaders/mpsaliasingstrategy/3114017-aliasingreserved)
- [static var `default`: MPSAliasingStrategy](/documentation/metalperformanceshaders/mpsaliasingstrategy/3114018-default)
- [static var preferNonTemporaryMemory: MPSAliasingStrategy](/documentation/metalperformanceshaders/mpsaliasingstrategy/3114020-prefernontemporarymemory)
- [static var preferTemporaryMemory: MPSAliasingStrategy](/documentation/metalperformanceshaders/mpsaliasingstrategy/3114021-prefertemporarymemory)
- [static var shallAlias: MPSAliasingStrategy](/documentation/metalperformanceshaders/mpsaliasingstrategy/3114022-shallalias)
- [static var shallNotAlias: MPSAliasingStrategy](/documentation/metalperformanceshaders/mpsaliasingstrategy/3114023-shallnotalias)
- [MPSCNNBatchNormalizationFlags](/documentation/metalperformanceshaders/mpscnnbatchnormalizationflags)

#### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpscnnbatchnormalizationflags/2953974-init)

#### Type Properties

- [static var CalculateStatisticsAutomatic: MPSCNNBatchNormalizationFlags](/documentation/metalperformanceshaders/mpscnnbatchnormalizationflags/2953947-calculatestatisticsautomatic)
- [static var Default: MPSCNNBatchNormalizationFlags](/documentation/metalperformanceshaders/mpscnnbatchnormalizationflags/2953950-default)
- [static var calculateStatisticsAlways: MPSCNNBatchNormalizationFlags](/documentation/metalperformanceshaders/mpscnnbatchnormalizationflags/2953945-calculatestatisticsalways)
- [static var calculateStatisticsMask: MPSCNNBatchNormalizationFlags](/documentation/metalperformanceshaders/mpscnnbatchnormalizationflags/2953948-calculatestatisticsmask)
- [static var calculateStatisticsNever: MPSCNNBatchNormalizationFlags](/documentation/metalperformanceshaders/mpscnnbatchnormalizationflags/2953949-calculatestatisticsnever)
- [MPSCNNConvolutionGradientOption](/documentation/metalperformanceshaders/mpscnnconvolutiongradientoption)

#### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpscnnconvolutiongradientoption/2942694-init)

#### Type Properties

- [static var all: MPSCNNConvolutionGradientOption](/documentation/metalperformanceshaders/mpscnnconvolutiongradientoption/2942431-all)
- [static var gradientWithData: MPSCNNConvolutionGradientOption](/documentation/metalperformanceshaders/mpscnnconvolutiongradientoption/2942426-gradientwithdata)
- [static var gradientWithWeightsAndBias: MPSCNNConvolutionGradientOption](/documentation/metalperformanceshaders/mpscnnconvolutiongradientoption/2942422-gradientwithweightsandbias)
- [MPSCustomKernelArgumentCount](/documentation/metalperformanceshaders/mpscustomkernelargumentcount)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpscustomkernelargumentcount/2990510-init)
- [init(destinationTextureCount: UInt, sourceTextureCount: UInt, broadcastTextureCount: UInt)](/documentation/metalperformanceshaders/mpscustomkernelargumentcount/2990511-init)

#### Instance Properties

- [var broadcastTextureCount: UInt](/documentation/metalperformanceshaders/mpscustomkernelargumentcount/2990473-broadcasttexturecount)
- [var destinationTextureCount: UInt](/documentation/metalperformanceshaders/mpscustomkernelargumentcount/2990474-destinationtexturecount)
- [var sourceTextureCount: UInt](/documentation/metalperformanceshaders/mpscustomkernelargumentcount/2990475-sourcetexturecount)
- [MPSCustomKernelIndex](/documentation/metalperformanceshaders/mpscustomkernelindex)

#### Initializers

- [init(UInt32)](/documentation/metalperformanceshaders/mpscustomkernelindex/2967123-init)
- [init(rawValue: UInt32)](/documentation/metalperformanceshaders/mpscustomkernelindex/2967124-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/metalperformanceshaders/mpscustomkernelindex/2967125-rawvalue)
- [MPSCustomKernelInfo](/documentation/metalperformanceshaders/mpscustomkernelinfo)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpscustomkernelinfo/2967126-init)
- [init(clipOrigin: vector_ushort4, clipSize: vector_ushort4, destinationFeatureChannels: UInt16, destImageArraySize: UInt16, sourceImageCount: UInt16, threadgroupSize: UInt16, subbatchIndex: UInt16, subbatchStride: UInt16, idiv: MPSIntegerDivisionParams)](/documentation/metalperformanceshaders/mpscustomkernelinfo/3204127-init)

#### Instance Properties

- [var clipOrigin: vector_ushort4](/documentation/metalperformanceshaders/mpscustomkernelinfo/2954841-cliporigin)
- [var clipSize: vector_ushort4](/documentation/metalperformanceshaders/mpscustomkernelinfo/2954845-clipsize)
- [var destImageArraySize: UInt16](/documentation/metalperformanceshaders/mpscustomkernelinfo/2954849-destimagearraysize)
- [var destinationFeatureChannels: UInt16](/documentation/metalperformanceshaders/mpscustomkernelinfo/2954851-destinationfeaturechannels)
- [var idiv: MPSIntegerDivisionParams](/documentation/metalperformanceshaders/mpscustomkernelinfo/2954831-idiv)
- [var sourceImageCount: UInt16](/documentation/metalperformanceshaders/mpscustomkernelinfo/2954838-sourceimagecount)
- [var subbatchIndex: UInt16](/documentation/metalperformanceshaders/mpscustomkernelinfo/2954862-subbatchindex)
- [var subbatchStride: UInt16](/documentation/metalperformanceshaders/mpscustomkernelinfo/2954817-subbatchstride)
- [var threadgroupSize: UInt16](/documentation/metalperformanceshaders/mpscustomkernelinfo/2954832-threadgroupsize)
- [MPSCustomKernelSourceInfo](/documentation/metalperformanceshaders/mpscustomkernelsourceinfo)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpscustomkernelsourceinfo/2967127-init)
- [init(kernelOrigin: vector_short2, kernelPhase: vector_ushort2, kernelSize: vector_ushort2, offset: vector_short2, stride: vector_ushort2, dilationRate: vector_ushort2, featureChannelOffset: UInt16, featureChannels: UInt16, imageArrayOffset: UInt16, imageArraySize: UInt16)](/documentation/metalperformanceshaders/mpscustomkernelsourceinfo/3204128-init)

#### Instance Properties

- [var dilationRate: vector_ushort2](/documentation/metalperformanceshaders/mpscustomkernelsourceinfo/2954855-dilationrate)
- [var featureChannelOffset: UInt16](/documentation/metalperformanceshaders/mpscustomkernelsourceinfo/2954871-featurechanneloffset)
- [var featureChannels: UInt16](/documentation/metalperformanceshaders/mpscustomkernelsourceinfo/2954870-featurechannels)
- [var imageArrayOffset: UInt16](/documentation/metalperformanceshaders/mpscustomkernelsourceinfo/2954852-imagearrayoffset)
- [var imageArraySize: UInt16](/documentation/metalperformanceshaders/mpscustomkernelsourceinfo/2954840-imagearraysize)
- [var kernelOrigin: vector_short2](/documentation/metalperformanceshaders/mpscustomkernelsourceinfo/2954859-kernelorigin)
- [var kernelPhase: vector_ushort2](/documentation/metalperformanceshaders/mpscustomkernelsourceinfo/2954856-kernelphase)
- [var kernelSize: vector_ushort2](/documentation/metalperformanceshaders/mpscustomkernelsourceinfo/2954823-kernelsize)
- [var offset: vector_short2](/documentation/metalperformanceshaders/mpscustomkernelsourceinfo/2954837-offset)
- [var stride: vector_ushort2](/documentation/metalperformanceshaders/mpscustomkernelsourceinfo/2954820-stride)
- [MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicecapsvalues)

#### Initializers

- [init(UInt32)](/documentation/metalperformanceshaders/mpsdevicecapsvalues/3548827-init)
- [init(rawValue: UInt32)](/documentation/metalperformanceshaders/mpsdevicecapsvalues/3548828-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/metalperformanceshaders/mpsdevicecapsvalues/3548829-rawvalue)
- [MPSDeviceOptions](/documentation/metalperformanceshaders/mpsdeviceoptions)

#### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpsdeviceoptions/3088935-init)

#### Type Properties

- [static var Default: MPSDeviceOptions](/documentation/metalperformanceshaders/mpsdeviceoptions/3088915-default)
- [static var lowPower: MPSDeviceOptions](/documentation/metalperformanceshaders/mpsdeviceoptions/3088916-lowpower)
- [static var skipRemovable: MPSDeviceOptions](/documentation/metalperformanceshaders/mpsdeviceoptions/3088917-skipremovable)
- [MPSDimensionSlice](/documentation/metalperformanceshaders/mpsdimensionslice)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsdimensionslice/3114270-init)
- [init(start: Int, length: Int)](/documentation/metalperformanceshaders/mpsdimensionslice/3114271-init)

#### Instance Properties

- [var length: Int](/documentation/metalperformanceshaders/mpsdimensionslice/3114025-length)
- [var start: Int](/documentation/metalperformanceshaders/mpsdimensionslice/3114026-start)
- [MPSImageCoordinate](/documentation/metalperformanceshaders/mpsimagecoordinate)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsimagecoordinate/3037440-init)
- [init(x: Int, y: Int, channel: Int)](/documentation/metalperformanceshaders/mpsimagecoordinate/3037441-init)

#### Instance Properties

- [var channel: Int](/documentation/metalperformanceshaders/mpsimagecoordinate/3037364-channel)
- [var x: Int](/documentation/metalperformanceshaders/mpsimagecoordinate/3037365-x)
- [var y: Int](/documentation/metalperformanceshaders/mpsimagecoordinate/3037366-y)
- [MPSImageRegion](/documentation/metalperformanceshaders/mpsimageregion)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsimageregion/3037442-init)
- [init(offset: MPSImageCoordinate, size: MPSImageCoordinate)](/documentation/metalperformanceshaders/mpsimageregion/3037443-init)

#### Instance Properties

- [var offset: MPSImageCoordinate](/documentation/metalperformanceshaders/mpsimageregion/3037371-offset)
- [var size: MPSImageCoordinate](/documentation/metalperformanceshaders/mpsimageregion/3037372-size)
- [MPSImageType](/documentation/metalperformanceshaders/mpsimagetype)

#### Initializers

- [init(UInt32)](/documentation/metalperformanceshaders/mpsimagetype/2967128-init)
- [init(rawValue: UInt32)](/documentation/metalperformanceshaders/mpsimagetype/2967129-init)

#### Instance Properties

- [var rawValue: UInt32](/documentation/metalperformanceshaders/mpsimagetype/2967130-rawvalue)
- [MPSIntegerDivisionParams](/documentation/metalperformanceshaders/mpsintegerdivisionparams)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsintegerdivisionparams/2967131-init)
- [init(divisor: UInt16, recip: UInt16, addend: UInt16, shift: UInt16)](/documentation/metalperformanceshaders/mpsintegerdivisionparams/2967132-init)

#### Instance Properties

- [var addend: UInt16](/documentation/metalperformanceshaders/mpsintegerdivisionparams/2954861-addend)
- [var divisor: UInt16](/documentation/metalperformanceshaders/mpsintegerdivisionparams/2954836-divisor)
- [var recip: UInt16](/documentation/metalperformanceshaders/mpsintegerdivisionparams/2954850-recip)
- [var shift: UInt16](/documentation/metalperformanceshaders/mpsintegerdivisionparams/2954821-shift)
- [MPSIntersectionDistance](/documentation/metalperformanceshaders/mpsintersectiondistance)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsintersectiondistance/2980943-init)
- [init(distance: Float)](/documentation/metalperformanceshaders/mpsintersectiondistance/2980944-init)

#### Instance Properties

- [var distance: Float](/documentation/metalperformanceshaders/mpsintersectiondistance/2980841-distance)
- [MPSIntersectionDistancePrimitiveIndex](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindex)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindex/2980945-init)
- [init(distance: Float, primitiveIndex: UInt32)](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindex/3019344-init)

#### Instance Properties

- [var distance: Float](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindex/2980843-distance)
- [var primitiveIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindex/2980844-primitiveindex)
- [MPSIntersectionDistancePrimitiveIndexBufferIndex](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindex)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindex/3751699-init)
- [init(distance: Float, primitiveIndex: UInt32, bufferIndex: UInt32)](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindex/3751700-init)

#### Instance Properties

- [var bufferIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindex/3750648-bufferindex)
- [var distance: Float](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindex/3750649-distance)
- [var primitiveIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindex/3750650-primitiveindex)
- [MPSIntersectionDistancePrimitiveIndexBufferIndexCoordinates](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexcoordinates)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexcoordinates/3751701-init)
- [init(distance: Float, primitiveIndex: UInt32, bufferIndex: UInt32, coordinates: vector_float2)](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexcoordinates/3751702-init)

#### Instance Properties

- [var bufferIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexcoordinates/3750652-bufferindex)
- [var coordinates: vector_float2](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexcoordinates/3750653-coordinates)
- [var distance: Float](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexcoordinates/3750654-distance)
- [var primitiveIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexcoordinates/3750655-primitiveindex)
- [MPSIntersectionDistancePrimitiveIndexBufferIndexInstanceIndex](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindex)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindex/3751703-init)
- [init(distance: Float, primitiveIndex: UInt32, bufferIndex: UInt32, instanceIndex: UInt32)](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindex/3751704-init)

#### Instance Properties

- [var bufferIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindex/3750657-bufferindex)
- [var distance: Float](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindex/3750658-distance)
- [var instanceIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindex/3750659-instanceindex)
- [var primitiveIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindex/3750660-primitiveindex)
- [MPSIntersectionDistancePrimitiveIndexBufferIndexInstanceIndexCoordinates](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindexcoordinates)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindexcoordinates/3751705-init)
- [init(distance: Float, primitiveIndex: UInt32, bufferIndex: UInt32, instanceIndex: UInt32, coordinates: vector_float2)](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindexcoordinates/3751706-init)

#### Instance Properties

- [var bufferIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindexcoordinates/3750662-bufferindex)
- [var coordinates: vector_float2](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindexcoordinates/3750663-coordinates)
- [var distance: Float](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindexcoordinates/3750664-distance)
- [var instanceIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindexcoordinates/3750665-instanceindex)
- [var primitiveIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexbufferindexinstanceindexcoordinates/3750666-primitiveindex)
- [MPSIntersectionDistancePrimitiveIndexCoordinates](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexcoordinates)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexcoordinates/2980947-init)
- [init(distance: Float, primitiveIndex: UInt32, coordinates: vector_float2)](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexcoordinates/3019345-init)

#### Instance Properties

- [var coordinates: vector_float2](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexcoordinates/2980846-coordinates)
- [var distance: Float](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexcoordinates/2980847-distance)
- [var primitiveIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexcoordinates/2980848-primitiveindex)
- [MPSIntersectionDistancePrimitiveIndexInstanceIndex](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexinstanceindex)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexinstanceindex/2980949-init)
- [init(distance: Float, primitiveIndex: UInt32, instanceIndex: UInt32)](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexinstanceindex/3019346-init)

#### Instance Properties

- [var distance: Float](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexinstanceindex/2980850-distance)
- [var instanceIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexinstanceindex/2980851-instanceindex)
- [var primitiveIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexinstanceindex/2980852-primitiveindex)
- [MPSIntersectionDistancePrimitiveIndexInstanceIndexCoordinates](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexinstanceindexcoordinates)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexinstanceindexcoordinates/2980951-init)
- [init(distance: Float, primitiveIndex: UInt32, instanceIndex: UInt32, coordinates: vector_float2)](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexinstanceindexcoordinates/3019347-init)

#### Instance Properties

- [var coordinates: vector_float2](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexinstanceindexcoordinates/2980854-coordinates)
- [var distance: Float](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexinstanceindexcoordinates/2980855-distance)
- [var instanceIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexinstanceindexcoordinates/2980856-instanceindex)
- [var primitiveIndex: UInt32](/documentation/metalperformanceshaders/mpsintersectiondistanceprimitiveindexinstanceindexcoordinates/2980857-primitiveindex)
- [MPSMatrixCopyOffsets](/documentation/metalperformanceshaders/mpsmatrixcopyoffsets)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsmatrixcopyoffsets/2915323-init)
- [init(sourceRowOffset: UInt32, sourceColumnOffset: UInt32, destinationRowOffset: UInt32, destinationColumnOffset: UInt32)](/documentation/metalperformanceshaders/mpsmatrixcopyoffsets/2915339-init)

#### Instance Properties

- [var destinationColumnOffset: UInt32](/documentation/metalperformanceshaders/mpsmatrixcopyoffsets/2915328-destinationcolumnoffset)
- [var destinationRowOffset: UInt32](/documentation/metalperformanceshaders/mpsmatrixcopyoffsets/2915338-destinationrowoffset)
- [var sourceColumnOffset: UInt32](/documentation/metalperformanceshaders/mpsmatrixcopyoffsets/2915327-sourcecolumnoffset)
- [var sourceRowOffset: UInt32](/documentation/metalperformanceshaders/mpsmatrixcopyoffsets/2915337-sourcerowoffset)
- [MPSMatrixOffset](/documentation/metalperformanceshaders/mpsmatrixoffset)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsmatrixoffset/2935632-init)
- [init(rowOffset: UInt32, columnOffset: UInt32)](/documentation/metalperformanceshaders/mpsmatrixoffset/2935633-init)

#### Instance Properties

- [var columnOffset: UInt32](/documentation/metalperformanceshaders/mpsmatrixoffset/2935545-columnoffset)
- [var rowOffset: UInt32](/documentation/metalperformanceshaders/mpsmatrixoffset/2935546-rowoffset)
- [MPSMatrixRandomDistribution](/documentation/metalperformanceshaders/mpsmatrixrandomdistribution)

#### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpsmatrixrandomdistribution/3243123-init)

#### Type Properties

- [static var `default`: MPSMatrixRandomDistribution](/documentation/metalperformanceshaders/mpsmatrixrandomdistribution/3242853-default)
- [static var normal: MPSMatrixRandomDistribution](/documentation/metalperformanceshaders/mpsmatrixrandomdistribution/3547978-normal)
- [static var uniform: MPSMatrixRandomDistribution](/documentation/metalperformanceshaders/mpsmatrixrandomdistribution/3242854-uniform)
- [MPSNDArrayOffsets](/documentation/metalperformanceshaders/mpsndarrayoffsets)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsndarrayoffsets/3131950-init)
- [init(dimensions: (Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int))](/documentation/metalperformanceshaders/mpsndarrayoffsets/3131951-init)

#### Instance Properties

- [var dimensions: (Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int)](/documentation/metalperformanceshaders/mpsndarrayoffsets/3131765-dimensions)
- [MPSNDArrayQuantizationScheme](/documentation/metalperformanceshaders/mpsndarrayquantizationscheme)

#### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpsndarrayquantizationscheme/4446285-init)

#### Type Properties

- [static var none: MPSNDArrayQuantizationScheme](/documentation/metalperformanceshaders/mpsndarrayquantizationscheme/4446147-none)
- [static var typeAffine: MPSNDArrayQuantizationScheme](/documentation/metalperformanceshaders/mpsndarrayquantizationscheme/4446145-typeaffine)
- [static var typeLUT: MPSNDArrayQuantizationScheme](/documentation/metalperformanceshaders/mpsndarrayquantizationscheme/4446146-typelut)
- [MPSNDArraySizes](/documentation/metalperformanceshaders/mpsndarraysizes)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsndarraysizes/3131952-init)
- [init(dimensions: (Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int))](/documentation/metalperformanceshaders/mpsndarraysizes/3131953-init)

#### Instance Properties

- [var dimensions: (Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int, Int)](/documentation/metalperformanceshaders/mpsndarraysizes/3131767-dimensions)
- [MPSNNComparisonType](/documentation/metalperformanceshaders/mpsnncomparisontype)

#### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpsnncomparisontype/3037444-init)

#### Type Properties

- [static var equal: MPSNNComparisonType](/documentation/metalperformanceshaders/mpsnncomparisontype/3037378-equal)
- [static var greater: MPSNNComparisonType](/documentation/metalperformanceshaders/mpsnncomparisontype/3037379-greater)
- [static var greaterOrEqual: MPSNNComparisonType](/documentation/metalperformanceshaders/mpsnncomparisontype/3037380-greaterorequal)
- [static var less: MPSNNComparisonType](/documentation/metalperformanceshaders/mpsnncomparisontype/3037381-less)
- [static var lessOrEqual: MPSNNComparisonType](/documentation/metalperformanceshaders/mpsnncomparisontype/3037382-lessorequal)
- [static var notEqual: MPSNNComparisonType](/documentation/metalperformanceshaders/mpsnncomparisontype/3037383-notequal)
- [MPSNNConvolutionAccumulatorPrecisionOption](/documentation/metalperformanceshaders/mpsnnconvolutionaccumulatorprecisionoption)

#### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpsnnconvolutionaccumulatorprecisionoption/2942695-init)

#### Type Properties

- [static var float: MPSNNConvolutionAccumulatorPrecisionOption](/documentation/metalperformanceshaders/mpsnnconvolutionaccumulatorprecisionoption/2942457-float)
- [static var half: MPSNNConvolutionAccumulatorPrecisionOption](/documentation/metalperformanceshaders/mpsnnconvolutionaccumulatorprecisionoption/2942458-half)
- [MPSNNTrainingStyle](/documentation/metalperformanceshaders/mpsnntrainingstyle)

#### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpsnntrainingstyle/2953136-init)

#### Type Properties

- [static var UpdateDeviceNone: MPSNNTrainingStyle](/documentation/metalperformanceshaders/mpsnntrainingstyle/2952962-updatedevicenone)
- [static var updateDeviceCPU: MPSNNTrainingStyle](/documentation/metalperformanceshaders/mpsnntrainingstyle/2952961-updatedevicecpu)
- [static var updateDeviceGPU: MPSNNTrainingStyle](/documentation/metalperformanceshaders/mpsnntrainingstyle/2952963-updatedevicegpu)
- [MPSRayMaskOptions](/documentation/metalperformanceshaders/mpsraymaskoptions)

#### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshaders/mpsraymaskoptions/2998477-init)

#### Type Properties

- [static var instance: MPSRayMaskOptions](/documentation/metalperformanceshaders/mpsraymaskoptions/2980817-instance)
- [static var primitive: MPSRayMaskOptions](/documentation/metalperformanceshaders/mpsraymaskoptions/2980819-primitive)
- [MPSRayOriginDirection](/documentation/metalperformanceshaders/mpsrayorigindirection)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsrayorigindirection/2980953-init)
- [init(origin: vector_float3, direction: vector_float3)](/documentation/metalperformanceshaders/mpsrayorigindirection/2990512-init)

#### Instance Properties

- [var direction: vector_float3](/documentation/metalperformanceshaders/mpsrayorigindirection/2980860-direction)
- [var origin: vector_float3](/documentation/metalperformanceshaders/mpsrayorigindirection/2980861-origin)
- [MPSRayOriginMaskDirectionMaxDistance](/documentation/metalperformanceshaders/mpsrayoriginmaskdirectionmaxdistance)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsrayoriginmaskdirectionmaxdistance/2980955-init)
- [init(origin: MPSPackedFloat3, mask: UInt32, direction: MPSPackedFloat3, maxDistance: Float)](/documentation/metalperformanceshaders/mpsrayoriginmaskdirectionmaxdistance/2980956-init)

#### Instance Properties

- [var direction: MPSPackedFloat3](/documentation/metalperformanceshaders/mpsrayoriginmaskdirectionmaxdistance/2980863-direction)
- [var mask: UInt32](/documentation/metalperformanceshaders/mpsrayoriginmaskdirectionmaxdistance/2980864-mask)
- [var maxDistance: Float](/documentation/metalperformanceshaders/mpsrayoriginmaskdirectionmaxdistance/2980865-maxdistance)
- [var origin: MPSPackedFloat3](/documentation/metalperformanceshaders/mpsrayoriginmaskdirectionmaxdistance/2980866-origin)
- [MPSRayOriginMinDistanceDirectionMaxDistance](/documentation/metalperformanceshaders/mpsrayoriginmindistancedirectionmaxdistance)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsrayoriginmindistancedirectionmaxdistance/2980957-init)
- [init(origin: MPSPackedFloat3, minDistance: Float, direction: MPSPackedFloat3, maxDistance: Float)](/documentation/metalperformanceshaders/mpsrayoriginmindistancedirectionmaxdistance/2980958-init)

#### Instance Properties

- [var direction: MPSPackedFloat3](/documentation/metalperformanceshaders/mpsrayoriginmindistancedirectionmaxdistance/2980868-direction)
- [var maxDistance: Float](/documentation/metalperformanceshaders/mpsrayoriginmindistancedirectionmaxdistance/2980869-maxdistance)
- [var minDistance: Float](/documentation/metalperformanceshaders/mpsrayoriginmindistancedirectionmaxdistance/2980870-mindistance)
- [var origin: MPSPackedFloat3](/documentation/metalperformanceshaders/mpsrayoriginmindistancedirectionmaxdistance/2980871-origin)
- [MPSRayPackedOriginDirection](/documentation/metalperformanceshaders/mpsraypackedorigindirection)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsraypackedorigindirection/3243124-init)
- [init(origin: MPSPackedFloat3, direction: MPSPackedFloat3)](/documentation/metalperformanceshaders/mpsraypackedorigindirection/3243125-init)

#### Instance Properties

- [var direction: MPSPackedFloat3](/documentation/metalperformanceshaders/mpsraypackedorigindirection/3242889-direction)
- [var origin: MPSPackedFloat3](/documentation/metalperformanceshaders/mpsraypackedorigindirection/3242890-origin)
- [MPSStateTextureInfo](/documentation/metalperformanceshaders/mpsstatetextureinfo)

#### Initializers

- [init()](/documentation/metalperformanceshaders/mpsstatetextureinfo/2948059-init)
- [init(width: Int, height: Int, depth: Int, arrayLength: Int, pixelFormat: MTLPixelFormat, textureType: MTLTextureType, usage: MTLTextureUsage, _reserved: (Int, Int, Int, Int))](/documentation/metalperformanceshaders/mpsstatetextureinfo/2948058-init)

#### Instance Properties

- [var arrayLength: Int](/documentation/metalperformanceshaders/mpsstatetextureinfo/2947910-arraylength)
- [var depth: Int](/documentation/metalperformanceshaders/mpsstatetextureinfo/2947891-depth)
- [var height: Int](/documentation/metalperformanceshaders/mpsstatetextureinfo/2947898-height)
- [var pixelFormat: MTLPixelFormat](/documentation/metalperformanceshaders/mpsstatetextureinfo/2947893-pixelformat)
- [var textureType: MTLTextureType](/documentation/metalperformanceshaders/mpsstatetextureinfo/2947911-texturetype)
- [var usage: MTLTextureUsage](/documentation/metalperformanceshaders/mpsstatetextureinfo/2947896-usage)
- [var width: Int](/documentation/metalperformanceshaders/mpsstatetextureinfo/2947909-width)
- [MetalPerformanceShaders Enumerations](/documentation/metalperformanceshaders/metalperformanceshaders_enumerations)

### Enumerations

- [MPSAccelerationStructureStatus](/documentation/metalperformanceshaders/mpsaccelerationstructurestatus)

#### Enumeration Cases

- [case built](/documentation/metalperformanceshaders/mpsaccelerationstructurestatus/built)
- [case unbuilt](/documentation/metalperformanceshaders/mpsaccelerationstructurestatus/unbuilt)
- [MPSBoundingBoxIntersectionTestType](/documentation/metalperformanceshaders/mpsboundingboxintersectiontesttype)

#### Enumeration Cases

- [case axisAligned](/documentation/metalperformanceshaders/mpsboundingboxintersectiontesttype/axisaligned)
- [case `default`](/documentation/metalperformanceshaders/mpsboundingboxintersectiontesttype/default)
- [case fast](/documentation/metalperformanceshaders/mpsboundingboxintersectiontesttype/fast)
- [MPSCNNConvolutionWeightsLayout](/documentation/metalperformanceshaders/mpscnnconvolutionweightslayout)

#### Enumeration Cases

- [case OHWI](/documentation/metalperformanceshaders/mpscnnconvolutionweightslayout/ohwi)
- [MPSCNNLossType](/documentation/metalperformanceshaders/mpscnnlosstype)

#### Enumeration Cases

- [case categoricalCrossEntropy](/documentation/metalperformanceshaders/mpscnnlosstype/categoricalcrossentropy)
- [case cosineDistance](/documentation/metalperformanceshaders/mpscnnlosstype/cosinedistance)
- [case count](/documentation/metalperformanceshaders/mpscnnlosstype/count)
- [case hinge](/documentation/metalperformanceshaders/mpscnnlosstype/hinge)
- [case huber](/documentation/metalperformanceshaders/mpscnnlosstype/huber)
- [case kullbackLeiblerDivergence](/documentation/metalperformanceshaders/mpscnnlosstype/kullbackleiblerdivergence)
- [case log](/documentation/metalperformanceshaders/mpscnnlosstype/log)
- [case meanAbsoluteError](/documentation/metalperformanceshaders/mpscnnlosstype/meanabsoluteerror)
- [case meanSquaredError](/documentation/metalperformanceshaders/mpscnnlosstype/meansquarederror)
- [case sigmoidCrossEntropy](/documentation/metalperformanceshaders/mpscnnlosstype/sigmoidcrossentropy)
- [case softMaxCrossEntropy](/documentation/metalperformanceshaders/mpscnnlosstype/softmaxcrossentropy)
- [MPSCNNReductionType](/documentation/metalperformanceshaders/mpscnnreductiontype)

#### Enumeration Cases

- [case count](/documentation/metalperformanceshaders/mpscnnreductiontype/count)
- [case mean](/documentation/metalperformanceshaders/mpscnnreductiontype/mean)
- [case none](/documentation/metalperformanceshaders/mpscnnreductiontype/none)
- [case sum](/documentation/metalperformanceshaders/mpscnnreductiontype/sum)
- [case sumByNonZeroWeights](/documentation/metalperformanceshaders/mpscnnreductiontype/sumbynonzeroweights)
- [MPSCNNWeightsQuantizationType](/documentation/metalperformanceshaders/mpscnnweightsquantizationtype)

#### Enumeration Cases

- [case none](/documentation/metalperformanceshaders/mpscnnweightsquantizationtype/none)
- [MPSFloatDataTypeBit](/documentation/metalperformanceshaders/mpsfloatdatatypebit)

#### Enumeration Cases

- [case exponentBit](/documentation/metalperformanceshaders/mpsfloatdatatypebit/exponentbit)
- [case mantissaBit](/documentation/metalperformanceshaders/mpsfloatdatatypebit/mantissabit)
- [case signBit](/documentation/metalperformanceshaders/mpsfloatdatatypebit/signbit)
- [MPSFloatDataTypeShift](/documentation/metalperformanceshaders/mpsfloatdatatypeshift)

#### Enumeration Cases

- [case exponentShift](/documentation/metalperformanceshaders/mpsfloatdatatypeshift/exponentshift)
- [case mantissaShift](/documentation/metalperformanceshaders/mpsfloatdatatypeshift/mantissashift)
- [case signShift](/documentation/metalperformanceshaders/mpsfloatdatatypeshift/signshift)
- [MPSIntersectionDataType](/documentation/metalperformanceshaders/mpsintersectiondatatype)

#### Enumeration Cases

- [case distance](/documentation/metalperformanceshaders/mpsintersectiondatatype/distance)
- [case distancePrimitiveIndex](/documentation/metalperformanceshaders/mpsintersectiondatatype/distanceprimitiveindex)
- [case distancePrimitiveIndexBufferIndex](/documentation/metalperformanceshaders/mpsintersectiondatatype/distanceprimitiveindexbufferindex)
- [case distancePrimitiveIndexBufferIndexCoordinates](/documentation/metalperformanceshaders/mpsintersectiondatatype/distanceprimitiveindexbufferindexcoordinates)
- [case distancePrimitiveIndexBufferIndexInstanceIndex](/documentation/metalperformanceshaders/mpsintersectiondatatype/distanceprimitiveindexbufferindexinstanceindex)
- [case distancePrimitiveIndexBufferIndexInstanceIndexCoordinates](/documentation/metalperformanceshaders/mpsintersectiondatatype/distanceprimitiveindexbufferindexinstanceindexcoordinates)
- [case distancePrimitiveIndexCoordinates](/documentation/metalperformanceshaders/mpsintersectiondatatype/distanceprimitiveindexcoordinates)
- [case distancePrimitiveIndexInstanceIndex](/documentation/metalperformanceshaders/mpsintersectiondatatype/distanceprimitiveindexinstanceindex)
- [case distancePrimitiveIndexInstanceIndexCoordinates](/documentation/metalperformanceshaders/mpsintersectiondatatype/distanceprimitiveindexinstanceindexcoordinates)
- [MPSIntersectionType](/documentation/metalperformanceshaders/mpsintersectiontype)

#### Enumeration Cases

- [case any](/documentation/metalperformanceshaders/mpsintersectiontype/any)
- [case nearest](/documentation/metalperformanceshaders/mpsintersectiontype/nearest)
- [MPSNNRegularizationType](/documentation/metalperformanceshaders/mpsnnregularizationtype)

#### Enumeration Cases

- [case L1](/documentation/metalperformanceshaders/mpsnnregularizationtype/l1)
- [case L2](/documentation/metalperformanceshaders/mpsnnregularizationtype/l2)
- [case None](/documentation/metalperformanceshaders/mpsnnregularizationtype/none)
- [MPSPolygonType](/documentation/metalperformanceshaders/mpspolygontype)

#### Enumeration Cases

- [case quadrilateral](/documentation/metalperformanceshaders/mpspolygontype/quadrilateral)
- [case triangle](/documentation/metalperformanceshaders/mpspolygontype/triangle)
- [MPSRNNMatrixId](/documentation/metalperformanceshaders/mpsrnnmatrixid)

#### Enumeration Cases

- [case SingleGateInputWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/singlegateinputweights)
- [case gruInputGateBiasTerms](/documentation/metalperformanceshaders/mpsrnnmatrixid/gruinputgatebiasterms)
- [case gruInputGateInputWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/gruinputgateinputweights)
- [case gruInputGateRecurrentWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/gruinputgaterecurrentweights)
- [case gruOutputGateBiasTerms](/documentation/metalperformanceshaders/mpsrnnmatrixid/gruoutputgatebiasterms)
- [case gruOutputGateInputGateWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/gruoutputgateinputgateweights)
- [case gruOutputGateInputWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/gruoutputgateinputweights)
- [case gruOutputGateRecurrentWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/gruoutputgaterecurrentweights)
- [case gruRecurrentGateBiasTerms](/documentation/metalperformanceshaders/mpsrnnmatrixid/grurecurrentgatebiasterms)
- [case gruRecurrentGateInputWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/grurecurrentgateinputweights)
- [case gruRecurrentGateRecurrentWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/grurecurrentgaterecurrentweights)
- [case lstmForgetGateBiasTerms](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstmforgetgatebiasterms)
- [case lstmForgetGateInputWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstmforgetgateinputweights)
- [case lstmForgetGateMemoryWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstmforgetgatememoryweights)
- [case lstmForgetGateRecurrentWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstmforgetgaterecurrentweights)
- [case lstmInputGateBiasTerms](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstminputgatebiasterms)
- [case lstmInputGateInputWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstminputgateinputweights)
- [case lstmInputGateMemoryWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstminputgatememoryweights)
- [case lstmInputGateRecurrentWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstminputgaterecurrentweights)
- [case lstmMemoryGateBiasTerms](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstmmemorygatebiasterms)
- [case lstmMemoryGateInputWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstmmemorygateinputweights)
- [case lstmMemoryGateMemoryWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstmmemorygatememoryweights)
- [case lstmMemoryGateRecurrentWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstmmemorygaterecurrentweights)
- [case lstmOutputGateBiasTerms](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstmoutputgatebiasterms)
- [case lstmOutputGateInputWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstmoutputgateinputweights)
- [case lstmOutputGateMemoryWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstmoutputgatememoryweights)
- [case lstmOutputGateRecurrentWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/lstmoutputgaterecurrentweights)
- [case singleGateBiasTerms](/documentation/metalperformanceshaders/mpsrnnmatrixid/singlegatebiasterms)
- [case singleGateRecurrentWeights](/documentation/metalperformanceshaders/mpsrnnmatrixid/singlegaterecurrentweights)
- [MPSRayDataType](/documentation/metalperformanceshaders/mpsraydatatype)

#### Enumeration Cases

- [case originDirection](/documentation/metalperformanceshaders/mpsraydatatype/origindirection)
- [case originMaskDirectionMaxDistance](/documentation/metalperformanceshaders/mpsraydatatype/originmaskdirectionmaxdistance)
- [case originMinDistanceDirectionMaxDistance](/documentation/metalperformanceshaders/mpsraydatatype/originmindistancedirectionmaxdistance)
- [case packedOriginDirection](/documentation/metalperformanceshaders/mpsraydatatype/packedorigindirection)
- [MPSRayMaskOperator](/documentation/metalperformanceshaders/mpsraymaskoperator)

#### Enumeration Cases

- [case and](/documentation/metalperformanceshaders/mpsraymaskoperator/and)
- [case equal](/documentation/metalperformanceshaders/mpsraymaskoperator/equal)
- [case greaterThan](/documentation/metalperformanceshaders/mpsraymaskoperator/greaterthan)
- [case greaterThanOrEqualTo](/documentation/metalperformanceshaders/mpsraymaskoperator/greaterthanorequalto)
- [case lessThan](/documentation/metalperformanceshaders/mpsraymaskoperator/lessthan)
- [case lessThanOrEqualTo](/documentation/metalperformanceshaders/mpsraymaskoperator/lessthanorequalto)
- [case notAnd](/documentation/metalperformanceshaders/mpsraymaskoperator/notand)
- [case notEqual](/documentation/metalperformanceshaders/mpsraymaskoperator/notequal)
- [case notOr](/documentation/metalperformanceshaders/mpsraymaskoperator/notor)
- [case notXor](/documentation/metalperformanceshaders/mpsraymaskoperator/notxor)
- [case or](/documentation/metalperformanceshaders/mpsraymaskoperator/or)
- [case xor](/documentation/metalperformanceshaders/mpsraymaskoperator/xor)
- [MPSStateResourceType](/documentation/metalperformanceshaders/mpsstateresourcetype)

#### Enumeration Cases

- [case buffer](/documentation/metalperformanceshaders/mpsstateresourcetype/buffer)
- [case none](/documentation/metalperformanceshaders/mpsstateresourcetype/none)
- [case texture](/documentation/metalperformanceshaders/mpsstateresourcetype/texture)
- [MPSTemporalWeighting](/documentation/metalperformanceshaders/mpstemporalweighting)

#### Enumeration Cases

- [case average](/documentation/metalperformanceshaders/mpstemporalweighting/average)
- [case exponentialMovingAverage](/documentation/metalperformanceshaders/mpstemporalweighting/exponentialmovingaverage)
- [MPSTransformType](/documentation/metalperformanceshaders/mpstransformtype)

#### Enumeration Cases

- [case float4x4](/documentation/metalperformanceshaders/mpstransformtype/float4x4)
- [case identity](/documentation/metalperformanceshaders/mpstransformtype/identity)
- [MPSTriangleIntersectionTestType](/documentation/metalperformanceshaders/mpstriangleintersectiontesttype)

#### Enumeration Cases

- [case `default`](/documentation/metalperformanceshaders/mpstriangleintersectiontesttype/default)
- [case watertight](/documentation/metalperformanceshaders/mpstriangleintersectiontesttype/watertight)
- [MetalPerformanceShaders Constants](/documentation/metalperformanceshaders/metalperformanceshaders_constants)

### Constants

- [var MPSBatchSizeIndex: Int32](/documentation/metalperformanceshaders/mpsbatchsizeindex)
- [var MPSCustomKernelIndexDestIndex: MPSCustomKernelIndex](/documentation/metalperformanceshaders/mpscustomkernelindexdestindex)
- [var MPSCustomKernelIndexSrc0Index: MPSCustomKernelIndex](/documentation/metalperformanceshaders/mpscustomkernelindexsrc0index)
- [var MPSCustomKernelIndexSrc1Index: MPSCustomKernelIndex](/documentation/metalperformanceshaders/mpscustomkernelindexsrc1index)
- [var MPSCustomKernelIndexSrc2Index: MPSCustomKernelIndex](/documentation/metalperformanceshaders/mpscustomkernelindexsrc2index)
- [var MPSCustomKernelIndexSrc3Index: MPSCustomKernelIndex](/documentation/metalperformanceshaders/mpscustomkernelindexsrc3index)
- [var MPSCustomKernelIndexSrc4Index: MPSCustomKernelIndex](/documentation/metalperformanceshaders/mpscustomkernelindexsrc4index)
- [var MPSCustomKernelIndexUserDataIndex: MPSCustomKernelIndex](/documentation/metalperformanceshaders/mpscustomkernelindexuserdataindex)
- [var MPSDeviceCapsIndex: Int32](/documentation/metalperformanceshaders/mpsdevicecapsindex)
- [var MPSDeviceCapsLast: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicecapslast)
- [var MPSDeviceCapsNull: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicecapsnull)
- [var MPSDeviceIsAppleDevice: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdeviceisappledevice)
- [var MPSDeviceSupportsBFloat16Arithmetic: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicesupportsbfloat16arithmetic)
- [var MPSDeviceSupportsFloat16BicubicFiltering: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicesupportsfloat16bicubicfiltering)
- [var MPSDeviceSupportsFloat32Filtering: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicesupportsfloat32filtering)
- [var MPSDeviceSupportsNorm16BicubicFiltering: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicesupportsnorm16bicubicfiltering)
- [var MPSDeviceSupportsQuadShuffle: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicesupportsquadshuffle)
- [var MPSDeviceSupportsReadWriteTextures: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicesupportsreadwritetextures)
- [var MPSDeviceSupportsReadableArrayOfTextures: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicesupportsreadablearrayoftextures)
- [var MPSDeviceSupportsSimdReduction: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicesupportssimdreduction)
- [var MPSDeviceSupportsSimdShuffle: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicesupportssimdshuffle)
- [var MPSDeviceSupportsSimdShuffleAndFill: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicesupportssimdshuffleandfill)
- [var MPSDeviceSupportsSimdgroupBarrier: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicesupportssimdgroupbarrier)
- [var MPSDeviceSupportsWritableArrayOfTextures: MPSDeviceCapsValues](/documentation/metalperformanceshaders/mpsdevicesupportswritablearrayoftextures)
- [var MPSFunctionConstantIndex: Int32](/documentation/metalperformanceshaders/mpsfunctionconstantindex)
- [var MPSFunctionConstantIndexReserved: Int32](/documentation/metalperformanceshaders/mpsfunctionconstantindexreserved)
- [let MPSFunctionConstantNone: MPSFunctionConstant](/documentation/metalperformanceshaders/mpsfunctionconstantnone)
- [let MPSFunctionConstantNoneArray: (MPSFunctionConstant, MPSFunctionConstant)](/documentation/metalperformanceshaders/mpsfunctionconstantnonearray)
- [var MPSImageType2d: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype2d)
- [var MPSImageType2d_array: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype2d_array)
- [var MPSImageType2d_array_noAlpha: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype2d_array_noalpha)
- [var MPSImageType2d_noAlpha: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype2d_noalpha)
- [var MPSImageTypeArray2d: MPSImageType](/documentation/metalperformanceshaders/mpsimagetypearray2d)
- [var MPSImageTypeArray2d_array: MPSImageType](/documentation/metalperformanceshaders/mpsimagetypearray2d_array)
- [var MPSImageTypeArray2d_array_noAlpha: MPSImageType](/documentation/metalperformanceshaders/mpsimagetypearray2d_array_noalpha)
- [var MPSImageTypeArray2d_noAlpha: MPSImageType](/documentation/metalperformanceshaders/mpsimagetypearray2d_noalpha)
- [var MPSImageType_ArrayMask: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype_arraymask)
- [var MPSImageType_BatchMask: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype_batchmask)
- [var MPSImageType_bitCount: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype_bitcount)
- [var MPSImageType_mask: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype_mask)
- [var MPSImageType_noAlpha: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype_noalpha)
- [var MPSImageType_texelFormatBFloat16: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype_texelformatbfloat16)
- [var MPSImageType_texelFormatFloat16: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype_texelformatfloat16)
- [var MPSImageType_texelFormatMask: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype_texelformatmask)
- [var MPSImageType_texelFormatShift: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype_texelformatshift)
- [var MPSImageType_texelFormatStandard: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype_texelformatstandard)
- [var MPSImageType_texelFormatUnorm8: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype_texelformatunorm8)
- [var MPSImageType_typeMask: MPSImageType](/documentation/metalperformanceshaders/mpsimagetype_typemask)
- [var MPSNDArrayConstantIndex: Int32](/documentation/metalperformanceshaders/mpsndarrayconstantindex)
- [var MPSNDArrayConstantMultiDestDstAddressingIndex: Int32](/documentation/metalperformanceshaders/mpsndarrayconstantmultidestdstaddressingindex)
- [var MPSNDArrayConstantMultiDestIndex: Int32](/documentation/metalperformanceshaders/mpsndarrayconstantmultidestindex)
- [var MPSNDArrayConstantMultiDestIndex0: Int32](/documentation/metalperformanceshaders/mpsndarrayconstantmultidestindex0)
- [var MPSNDArrayConstantMultiDestIndex1: Int32](/documentation/metalperformanceshaders/mpsndarrayconstantmultidestindex1)
- [var MPSNDArrayConstantMultiDestSrcAddressingIndex: Int32](/documentation/metalperformanceshaders/mpsndarrayconstantmultidestsrcaddressingindex)
- [var MPSTextureLinkingConstantIndex: Int32](/documentation/metalperformanceshaders/mpstexturelinkingconstantindex)
- [var MPSUserAvailableFunctionConstantStartIndex: Int32](/documentation/metalperformanceshaders/mpsuseravailablefunctionconstantstartindex)
- [var MPSUserConstantIndex: Int32](/documentation/metalperformanceshaders/mpsuserconstantindex)
- [MetalPerformanceShaders Functions](/documentation/metalperformanceshaders/metalperformanceshaders_functions)

### Functions

- [func MPSDataTypeBitsCount(MPSDataType) -> Int](/documentation/metalperformanceshaders/4316495-mpsdatatypebitscount)
- [func MPSFindIntegerDivisionParams(UInt16) -> MPSIntegerDivisionParams](/documentation/metalperformanceshaders/2954868-mpsfindintegerdivisionparams)
- [func MPSGetCustomKernelBatchedDestinationIndex(MPSCustomKernelArgumentCount) -> UInt](/documentation/metalperformanceshaders/2990481-mpsgetcustomkernelbatcheddestina)
- [func MPSGetCustomKernelBatchedSourceIndex(MPSCustomKernelArgumentCount, UInt, UInt) -> UInt](/documentation/metalperformanceshaders/2990482-mpsgetcustomkernelbatchedsourcei)
- [func MPSGetCustomKernelBroadcastSourceIndex(MPSCustomKernelArgumentCount, UInt, UInt) -> UInt](/documentation/metalperformanceshaders/2990483-mpsgetcustomkernelbroadcastsourc)
- [func MPSGetCustomKernelMaxBatchSize(MPSCustomKernelArgumentCount, UInt) -> UInt](/documentation/metalperformanceshaders/2990484-mpsgetcustomkernelmaxbatchsize)
- [func MPSGetImageType(MPSImage) -> MPSImageType](/documentation/metalperformanceshaders/3131717-mpsgetimagetype)
- [func MPSGetPreferredDevice(MPSDeviceOptions) -> (any MTLDevice)?](/documentation/metalperformanceshaders/3088918-mpsgetpreferreddevice)
- [func MPSHintTemporaryMemoryHighWaterMark(any MTLCommandBuffer, Int)](/documentation/metalperformanceshaders/2990485-mpshinttemporarymemoryhighwaterm)
- [func MPSImageBatchIncrementReadCount([MPSImage], Int) -> Int](/documentation/metalperformanceshaders/2951916-mpsimagebatchincrementreadcount)
- [func MPSImageBatchIterate([MPSImage], (MPSImage, Int) -> Int) -> Int](/documentation/metalperformanceshaders/3019319-mpsimagebatchiterate)
- [func MPSImageBatchResourceSize([MPSImage]) -> Int](/documentation/metalperformanceshaders/2980727-mpsimagebatchresourcesize)
- [func MPSImageBatchSynchronize([MPSImage], any MTLCommandBuffer)](/documentation/metalperformanceshaders/2953951-mpsimagebatchsynchronize)
- [func MPSSetHeapCacheDuration(any MTLCommandBuffer, Double)](/documentation/metalperformanceshaders/2990486-mpssetheapcacheduration)
- [func MPSSizeofMPSDataType(MPSDataType) -> Int](/documentation/metalperformanceshaders/4092019-mpssizeofmpsdatatype)
- [func MPSStateBatchIncrementReadCount([MPSState]?, Int) -> Int](/documentation/metalperformanceshaders/2951920-mpsstatebatchincrementreadcount)
- [func MPSStateBatchResourceSize([MPSState]?) -> Int](/documentation/metalperformanceshaders/2980728-mpsstatebatchresourcesize)
- [func MPSStateBatchSynchronize([MPSState], any MTLCommandBuffer)](/documentation/metalperformanceshaders/2953920-mpsstatebatchsynchronize)
- [MetalPerformanceShaders Data Types](/documentation/metalperformanceshaders/metalperformanceshaders_data_types)

### Data Types

- [MPSAccelerationStructureCompletionHandler](/documentation/metalperformanceshaders/mpsaccelerationstructurecompletionhandler)
- [MPSAxisAlignedBoundingBox](/documentation/metalperformanceshaders/mpsaxisalignedboundingbox)
- [MPSDeviceCaps](/documentation/metalperformanceshaders/mpsdevicecaps)
- [MPSFunctionConstant](/documentation/metalperformanceshaders/mpsfunctionconstant)
- [MPSFunctionConstantInMetal](/documentation/metalperformanceshaders/mpsfunctionconstantinmetal)
- [MPSGradientNodeBlock](/documentation/metalperformanceshaders/mpsgradientnodeblock)
- [MPSPackedFloat3](/documentation/metalperformanceshaders/mpspackedfloat3)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
