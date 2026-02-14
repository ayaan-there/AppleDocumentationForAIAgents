# Core Video Documentation

Source: https://sosumi.ai/documentation/corevideo

---
title: Core Video
source: https://developer.apple.com/documentation/corevideo
timestamp: 2026-02-13T18:55:50.221Z
---

## Data Processing

- [CVBuffer](/documentation/corevideo/cvbuffer-nfm)

### Working with attachments

- [func CVBufferHasAttachment(CVBuffer, CFString) -> Bool](/documentation/corevideo/cvbufferhasattachment(_:_:))
- [func CVBufferCopyAttachment(CVBuffer, CFString, UnsafeMutablePointer<CVAttachmentMode>?) -> CFTypeRef?](/documentation/corevideo/cvbuffercopyattachment(_:_:_:))
- [func CVBufferCopyAttachments(CVBuffer, CVAttachmentMode) -> CFDictionary?](/documentation/corevideo/cvbuffercopyattachments(_:_:))
- [func CVBufferSetAttachment(CVBuffer, CFString, CFTypeRef, CVAttachmentMode)](/documentation/corevideo/cvbuffersetattachment(_:_:_:_:))
- [func CVBufferSetAttachments(CVBuffer, CFDictionary, CVAttachmentMode)](/documentation/corevideo/cvbuffersetattachments(_:_:_:))
- [func CVBufferPropagateAttachments(CVBuffer, CVBuffer)](/documentation/corevideo/cvbufferpropagateattachments(_:_:))
- [func CVBufferRemoveAttachment(CVBuffer, CFString)](/documentation/corevideo/cvbufferremoveattachment(_:_:))
- [func CVBufferRemoveAllAttachments(CVBuffer)](/documentation/corevideo/cvbufferremoveallattachments(_:))
- [func CVBufferGetAttachment(CVBuffer, CFString, UnsafeMutablePointer<CVAttachmentMode>?) -> Unmanaged<CFTypeRef>?](/documentation/corevideo/cvbuffergetattachment(_:_:_:))
- [func CVBufferGetAttachments(CVBuffer, CVAttachmentMode) -> CFDictionary?](/documentation/corevideo/cvbuffergetattachments(_:_:))

### Data types

- [CVBuffer](/documentation/corevideo/cvbuffer)

#### Structures

- [CVBuffer.Attributes](/documentation/corevideo/cvbuffer/attributes)

##### Initializers

- [init(CVBuffer.CreationAttributes)](/documentation/corevideo/cvbuffer/attributes/init(_:))
- [init?(merging: [CVBuffer.Attributes])](/documentation/corevideo/cvbuffer/attributes/init(merging:))
- [init(pixelFormatTypes: [CVPixelFormatType]?, size: CVImageSize?, compatibility: CVPixelFormatDescription.Compatibility, bytesPerRowAlignment: Int?, planeAlignment: Int?, extendedPixels: CVPixelBufferPadding?)](/documentation/corevideo/cvbuffer/attributes/init(pixelformattypes:size:compatibility:bytesperrowalignment:planealignment:extendedpixels:))
- [init(rawAttributes: [String : any Sendable])](/documentation/corevideo/cvbuffer/attributes/init(rawattributes:))

##### Instance Properties

- [var pixelFormatTypes: [CVPixelFormatType]?](/documentation/corevideo/cvbuffer/attributes/pixelformattypes)
- [var rawAttributes: [String : any Sendable]](/documentation/corevideo/cvbuffer/attributes/rawattributes)

##### Subscripts

- [subscript(dynamicMember _: WritableKeyPath<CVBuffer.CreationAttributes, CVBuffer.CreationAttributes.Backing>) -> CVBuffer.CreationAttributes.Backing](/documentation/corevideo/cvbuffer/attributes/subscript(dynamicmember:)-1c1om)
- [subscript(dynamicMember _: WritableKeyPath<CVBuffer.CreationAttributes, CVPixelFormatDescription?>) -> CVPixelFormatDescription?](/documentation/corevideo/cvbuffer/attributes/subscript(dynamicmember:)-1o2ji)
- [subscript(dynamicMember _: WritableKeyPath<CVBuffer.CreationAttributes, Bool>) -> Bool?](/documentation/corevideo/cvbuffer/attributes/subscript(dynamicmember:)-21rr)
- [subscript(dynamicMember _: WritableKeyPath<CVBuffer.CreationAttributes, Int?>) -> Int?](/documentation/corevideo/cvbuffer/attributes/subscript(dynamicmember:)-3c1w8)
- [subscript(dynamicMember _: WritableKeyPath<CVBuffer.CreationAttributes, CVPixelFormatDescription.Compatibility>) -> CVPixelFormatDescription.Compatibility](/documentation/corevideo/cvbuffer/attributes/subscript(dynamicmember:)-5m9xn)
- [subscript(dynamicMember _: WritableKeyPath<CVBuffer.CreationAttributes, CVPixelFormatType>) -> CVPixelFormatType?](/documentation/corevideo/cvbuffer/attributes/subscript(dynamicmember:)-6jvmi)
- [subscript(dynamicMember _: WritableKeyPath<CVBuffer.CreationAttributes, CVPixelBufferPadding?>) -> CVPixelBufferPadding?](/documentation/corevideo/cvbuffer/attributes/subscript(dynamicmember:)-7bidb)
- [subscript(dynamicMember _: WritableKeyPath<CVBuffer.CreationAttributes, CVImageSize>) -> CVImageSize?](/documentation/corevideo/cvbuffer/attributes/subscript(dynamicmember:)-9n8bh)
- [CVBuffer.CreationAttributes](/documentation/corevideo/cvbuffer/creationattributes)

##### Initializers

- [init?(CVBuffer.Attributes)](/documentation/corevideo/cvbuffer/creationattributes/init(_:))
- [init(pixelFormatType: CVPixelFormatType, size: CVImageSize, compatibility: CVPixelFormatDescription.Compatibility, bytesPerRowAlignment: Int?, planeAlignment: Int?, extendedPixels: CVPixelBufferPadding?)](/documentation/corevideo/cvbuffer/creationattributes/init(pixelformattype:size:compatibility:bytesperrowalignment:planealignment:extendedpixels:))

##### Instance Properties

- [var backing: CVBuffer.CreationAttributes.Backing](/documentation/corevideo/cvbuffer/creationattributes/backing-swift.property)
- [var bytesPerRowAlignment: Int?](/documentation/corevideo/cvbuffer/creationattributes/bytesperrowalignment)
- [var compatibility: CVPixelFormatDescription.Compatibility](/documentation/corevideo/cvbuffer/creationattributes/compatibility)
- [var extendedPixels: CVPixelBufferPadding?](/documentation/corevideo/cvbuffer/creationattributes/extendedpixels)
- [var pixelFormatType: CVPixelFormatType](/documentation/corevideo/cvbuffer/creationattributes/pixelformattype)
- [var planeAlignment: Int?](/documentation/corevideo/cvbuffer/creationattributes/planealignment)
- [var size: CVImageSize](/documentation/corevideo/cvbuffer/creationattributes/size)

##### Enumerations

- [CVBuffer.CreationAttributes.Backing](/documentation/corevideo/cvbuffer/creationattributes/backing-swift.enum)

###### Enumeration Cases

- [case ioSurface](/documentation/corevideo/cvbuffer/creationattributes/backing-swift.enum/iosurface)
- [case ioSurfaceWithProperties([String : any Sendable])](/documentation/corevideo/cvbuffer/creationattributes/backing-swift.enum/iosurfacewithproperties(_:))
- [case memory](/documentation/corevideo/cvbuffer/creationattributes/backing-swift.enum/memory)

#### Type Aliases

- [CVBuffer.OriginPosition](/documentation/corevideo/cvbuffer/originposition)
- [CVBuffer.Padding](/documentation/corevideo/cvbuffer/padding)
- [CVBuffer.PlaneProperties](/documentation/corevideo/cvbuffer/planeproperties)
- [CVBuffer.Size](/documentation/corevideo/cvbuffer/size)
- [CVAttachmentMode](/documentation/corevideo/cvattachmentmode)

#### Constants

- [case shouldNotPropagate](/documentation/corevideo/cvattachmentmode/shouldnotpropagate)
- [case shouldPropagate](/documentation/corevideo/cvattachmentmode/shouldpropagate)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/corevideo/cvattachmentmode/init(rawvalue:))

### Constants

- [CVBuffer Attribute Keys](/documentation/corevideo/cvbuffer-attribute-keys)

#### Constants

- [let kCVBufferPropagatedAttachmentsKey: CFString](/documentation/corevideo/kcvbufferpropagatedattachmentskey)
- [let kCVBufferNonPropagatedAttachmentsKey: CFString](/documentation/corevideo/kcvbuffernonpropagatedattachmentskey)
- [CVBuffer Attachment Keys](/documentation/corevideo/cvbuffer-attachment-keys)

#### Constants

- [let kCVBufferMovieTimeKey: CFString](/documentation/corevideo/kcvbuffermovietimekey)
- [let kCVBufferTimeValueKey: CFString](/documentation/corevideo/kcvbuffertimevaluekey)
- [let kCVBufferTimeScaleKey: CFString](/documentation/corevideo/kcvbuffertimescalekey)
- [CVImageBuffer](/documentation/corevideo/cvimagebuffer-q40)

### Inspecting image buffers

- [func CVImageBufferGetCleanRect(CVImageBuffer) -> CGRect](/documentation/corevideo/cvimagebuffergetcleanrect(_:))
- [func CVImageBufferGetColorSpace(CVImageBuffer) -> Unmanaged<CGColorSpace>?](/documentation/corevideo/cvimagebuffergetcolorspace(_:))
- [func CVImageBufferGetDisplaySize(CVImageBuffer) -> CGSize](/documentation/corevideo/cvimagebuffergetdisplaysize(_:))
- [func CVImageBufferGetEncodedSize(CVImageBuffer) -> CGSize](/documentation/corevideo/cvimagebuffergetencodedsize(_:))
- [func CVImageBufferIsFlipped(CVImageBuffer) -> Bool](/documentation/corevideo/cvimagebufferisflipped(_:))

### Creating color spaces

- [func CVImageBufferCreateColorSpaceFromAttachments(CFDictionary) -> Unmanaged<CGColorSpace>?](/documentation/corevideo/cvimagebuffercreatecolorspacefromattachments(_:))

### Data types

- [CVImageBuffer](/documentation/corevideo/cvimagebuffer)

### Converting between strings and integer code points

- [func CVColorPrimariesGetIntegerCodePointForString(CFString?) -> Int32](/documentation/corevideo/cvcolorprimariesgetintegercodepointforstring(_:))
- [func CVColorPrimariesGetStringForIntegerCodePoint(Int32) -> Unmanaged<CFString>?](/documentation/corevideo/cvcolorprimariesgetstringforintegercodepoint(_:))
- [func CVTransferFunctionGetIntegerCodePointForString(CFString?) -> Int32](/documentation/corevideo/cvtransferfunctiongetintegercodepointforstring(_:))
- [func CVTransferFunctionGetStringForIntegerCodePoint(Int32) -> Unmanaged<CFString>?](/documentation/corevideo/cvtransferfunctiongetstringforintegercodepoint(_:))
- [func CVYCbCrMatrixGetIntegerCodePointForString(CFString?) -> Int32](/documentation/corevideo/cvycbcrmatrixgetintegercodepointforstring(_:))
- [func CVYCbCrMatrixGetStringForIntegerCodePoint(Int32) -> Unmanaged<CFString>?](/documentation/corevideo/cvycbcrmatrixgetstringforintegercodepoint(_:))

### Constants

- [Image Buffer Attachment Keys](/documentation/corevideo/image-buffer-attachment-keys)

#### Constants

- [let kCVImageBufferCGColorSpaceKey: CFString](/documentation/corevideo/kcvimagebuffercgcolorspacekey)
- [let kCVImageBufferCleanApertureKey: CFString](/documentation/corevideo/kcvimagebuffercleanaperturekey)
- [let kCVImageBufferPreferredCleanApertureKey: CFString](/documentation/corevideo/kcvimagebufferpreferredcleanaperturekey)
- [let kCVImageBufferFieldCountKey: CFString](/documentation/corevideo/kcvimagebufferfieldcountkey)
- [let kCVImageBufferFieldDetailKey: CFString](/documentation/corevideo/kcvimagebufferfielddetailkey)
- [let kCVImageBufferPixelAspectRatioKey: CFString](/documentation/corevideo/kcvimagebufferpixelaspectratiokey)
- [let kCVImageBufferDisplayDimensionsKey: CFString](/documentation/corevideo/kcvimagebufferdisplaydimensionskey)
- [let kCVImageBufferGammaLevelKey: CFString](/documentation/corevideo/kcvimagebuffergammalevelkey)
- [let kCVImageBufferICCProfileKey: CFString](/documentation/corevideo/kcvimagebuffericcprofilekey)
- [let kCVImageBufferYCbCrMatrixKey: CFString](/documentation/corevideo/kcvimagebufferycbcrmatrixkey)
- [let kCVImageBufferColorPrimariesKey: CFString](/documentation/corevideo/kcvimagebuffercolorprimarieskey)
- [let kCVImageBufferTransferFunctionKey: CFString](/documentation/corevideo/kcvimagebuffertransferfunctionkey)
- [let kCVImageBufferChromaLocationTopFieldKey: CFString](/documentation/corevideo/kcvimagebufferchromalocationtopfieldkey)
- [let kCVImageBufferChromaLocationBottomFieldKey: CFString](/documentation/corevideo/kcvimagebufferchromalocationbottomfieldkey)
- [let kCVImageBufferChromaSubsamplingKey: CFString](/documentation/corevideo/kcvimagebufferchromasubsamplingkey)
- [let kCVImageBufferAlphaChannelIsOpaque: CFString](/documentation/corevideo/kcvimagebufferalphachannelisopaque)
- [let kCVImageBufferContentLightLevelInfoKey: CFString](/documentation/corevideo/kcvimagebuffercontentlightlevelinfokey)
- [let kCVImageBufferMasteringDisplayColorVolumeKey: CFString](/documentation/corevideo/kcvimagebuffermasteringdisplaycolorvolumekey)
- [Image Buffer Clean Aperture Keys](/documentation/corevideo/image-buffer-clean-aperture-keys)

#### Constants

- [let kCVImageBufferCleanApertureWidthKey: CFString](/documentation/corevideo/kcvimagebuffercleanaperturewidthkey)
- [let kCVImageBufferCleanApertureHeightKey: CFString](/documentation/corevideo/kcvimagebuffercleanapertureheightkey)
- [let kCVImageBufferCleanApertureHorizontalOffsetKey: CFString](/documentation/corevideo/kcvimagebuffercleanaperturehorizontaloffsetkey)
- [let kCVImageBufferCleanApertureVerticalOffsetKey: CFString](/documentation/corevideo/kcvimagebuffercleanapertureverticaloffsetkey)
- [Image Buffer Pixel Aspect Ratio Keys](/documentation/corevideo/image-buffer-pixel-aspect-ratio-keys)

#### Constants

- [let kCVImageBufferPixelAspectRatioHorizontalSpacingKey: CFString](/documentation/corevideo/kcvimagebufferpixelaspectratiohorizontalspacingkey)
- [let kCVImageBufferPixelAspectRatioVerticalSpacingKey: CFString](/documentation/corevideo/kcvimagebufferpixelaspectratioverticalspacingkey)
- [Image Buffer Display Dimensions Keys](/documentation/corevideo/image-buffer-display-dimensions-keys)

#### Constants

- [let kCVImageBufferDisplayWidthKey: CFString](/documentation/corevideo/kcvimagebufferdisplaywidthkey)
- [let kCVImageBufferDisplayHeightKey: CFString](/documentation/corevideo/kcvimagebufferdisplayheightkey)
- [Image Buffer Field Detail Constants](/documentation/corevideo/image-buffer-field-detail-constants)

#### Constants

- [let kCVImageBufferFieldDetailTemporalTopFirst: CFString](/documentation/corevideo/kcvimagebufferfielddetailtemporaltopfirst)
- [let kCVImageBufferFieldDetailTemporalBottomFirst: CFString](/documentation/corevideo/kcvimagebufferfielddetailtemporalbottomfirst)
- [let kCVImageBufferFieldDetailSpatialFirstLineEarly: CFString](/documentation/corevideo/kcvimagebufferfielddetailspatialfirstlineearly)
- [let kCVImageBufferFieldDetailSpatialFirstLineLate: CFString](/documentation/corevideo/kcvimagebufferfielddetailspatialfirstlinelate)
- [Image Buffer YCbCr Matrix Constants](/documentation/corevideo/image-buffer-ycbcr-matrix-constants)

#### Constants

- [let kCVImageBufferYCbCrMatrix_ITU_R_2020: CFString](/documentation/corevideo/kcvimagebufferycbcrmatrix_itu_r_2020)
- [let kCVImageBufferYCbCrMatrix_P3_D65: CFString](/documentation/corevideo/kcvimagebufferycbcrmatrix_p3_d65)
- [let kCVImageBufferYCbCrMatrix_ITU_R_709_2: CFString](/documentation/corevideo/kcvimagebufferycbcrmatrix_itu_r_709_2)
- [let kCVImageBufferYCbCrMatrix_ITU_R_601_4: CFString](/documentation/corevideo/kcvimagebufferycbcrmatrix_itu_r_601_4)
- [let kCVImageBufferYCbCrMatrix_SMPTE_240M_1995: CFString](/documentation/corevideo/kcvimagebufferycbcrmatrix_smpte_240m_1995)
- [let kCVImageBufferYCbCrMatrix_DCI_P3: CFString](/documentation/corevideo/kcvimagebufferycbcrmatrix_dci_p3)
- [Image Buffer Color Primaries Constants](/documentation/corevideo/image-buffer-color-primaries-constants)

#### Constants

- [let kCVImageBufferColorPrimaries_ITU_R_709_2: CFString](/documentation/corevideo/kcvimagebuffercolorprimaries_itu_r_709_2)
- [let kCVImageBufferColorPrimaries_EBU_3213: CFString](/documentation/corevideo/kcvimagebuffercolorprimaries_ebu_3213)
- [let kCVImageBufferColorPrimaries_SMPTE_C: CFString](/documentation/corevideo/kcvimagebuffercolorprimaries_smpte_c)
- [let kCVImageBufferColorPrimaries_DCI_P3: CFString](/documentation/corevideo/kcvimagebuffercolorprimaries_dci_p3)
- [let kCVImageBufferColorPrimaries_ITU_R_2020: CFString](/documentation/corevideo/kcvimagebuffercolorprimaries_itu_r_2020)
- [let kCVImageBufferColorPrimaries_P3_D65: CFString](/documentation/corevideo/kcvimagebuffercolorprimaries_p3_d65)
- [let kCVImageBufferColorPrimaries_P22: CFString](/documentation/corevideo/kcvimagebuffercolorprimaries_p22)
- [Image Buffer Transfer Function Constants](/documentation/corevideo/image-buffer-transfer-function-constants)

#### Constants

- [let kCVImageBufferTransferFunction_ITU_R_709_2: CFString](/documentation/corevideo/kcvimagebuffertransferfunction_itu_r_709_2)
- [let kCVImageBufferTransferFunction_SMPTE_240M_1995: CFString](/documentation/corevideo/kcvimagebuffertransferfunction_smpte_240m_1995)
- [let kCVImageBufferTransferFunction_UseGamma: CFString](/documentation/corevideo/kcvimagebuffertransferfunction_usegamma)
- [let kCVImageBufferTransferFunction_sRGB: CFString](/documentation/corevideo/kcvimagebuffertransferfunction_srgb)
- [let kCVImageBufferTransferFunction_ITU_R_2020: CFString](/documentation/corevideo/kcvimagebuffertransferfunction_itu_r_2020)
- [let kCVImageBufferTransferFunction_SMPTE_ST_428_1: CFString](/documentation/corevideo/kcvimagebuffertransferfunction_smpte_st_428_1)
- [let kCVImageBufferTransferFunction_ITU_R_2100_HLG: CFString](/documentation/corevideo/kcvimagebuffertransferfunction_itu_r_2100_hlg)
- [let kCVImageBufferTransferFunction_SMPTE_ST_2084_PQ: CFString](/documentation/corevideo/kcvimagebuffertransferfunction_smpte_st_2084_pq)
- [Image Buffer Chroma Location Constants](/documentation/corevideo/image-buffer-chroma-location-constants)

#### Constants

- [let kCVImageBufferChromaLocation_Left: CFString](/documentation/corevideo/kcvimagebufferchromalocation_left)
- [let kCVImageBufferChromaLocation_Center: CFString](/documentation/corevideo/kcvimagebufferchromalocation_center)
- [let kCVImageBufferChromaLocation_TopLeft: CFString](/documentation/corevideo/kcvimagebufferchromalocation_topleft)
- [let kCVImageBufferChromaLocation_Top: CFString](/documentation/corevideo/kcvimagebufferchromalocation_top)
- [let kCVImageBufferChromaLocation_BottomLeft: CFString](/documentation/corevideo/kcvimagebufferchromalocation_bottomleft)
- [let kCVImageBufferChromaLocation_Bottom: CFString](/documentation/corevideo/kcvimagebufferchromalocation_bottom)
- [let kCVImageBufferChromaLocation_DV420: CFString](/documentation/corevideo/kcvimagebufferchromalocation_dv420)
- [Image Buffer Chroma Subsampling Constants](/documentation/corevideo/image-buffer-chroma-subsampling-constants)

#### Constants

- [let kCVImageBufferChromaSubsampling_420: CFString](/documentation/corevideo/kcvimagebufferchromasubsampling_420)
- [let kCVImageBufferChromaSubsampling_422: CFString](/documentation/corevideo/kcvimagebufferchromasubsampling_422)
- [let kCVImageBufferChromaSubsampling_411: CFString](/documentation/corevideo/kcvimagebufferchromasubsampling_411)
- [Image Buffer Display Mask Rectangle Keys](/documentation/corevideo/image-buffer-display-mask-rectangle-keys)

#### Constants

- [let kCVImageBufferDisplayMaskRectangle_LeftEdgePointsKey: CFString](/documentation/corevideo/kcvimagebufferdisplaymaskrectangle_leftedgepointskey)
- [let kCVImageBufferDisplayMaskRectangle_RectangleHeightKey: CFString](/documentation/corevideo/kcvimagebufferdisplaymaskrectangle_rectangleheightkey)
- [let kCVImageBufferDisplayMaskRectangle_RectangleLeftKey: CFString](/documentation/corevideo/kcvimagebufferdisplaymaskrectangle_rectangleleftkey)
- [let kCVImageBufferDisplayMaskRectangle_RectangleTopKey: CFString](/documentation/corevideo/kcvimagebufferdisplaymaskrectangle_rectangletopkey)
- [let kCVImageBufferDisplayMaskRectangle_RectangleWidthKey: CFString](/documentation/corevideo/kcvimagebufferdisplaymaskrectangle_rectanglewidthkey)
- [let kCVImageBufferDisplayMaskRectangle_ReferenceRasterHeightKey: CFString](/documentation/corevideo/kcvimagebufferdisplaymaskrectangle_referencerasterheightkey)
- [let kCVImageBufferDisplayMaskRectangle_ReferenceRasterWidthKey: CFString](/documentation/corevideo/kcvimagebufferdisplaymaskrectangle_referencerasterwidthkey)
- [let kCVImageBufferDisplayMaskRectangle_RightEdgePointsKey: CFString](/documentation/corevideo/kcvimagebufferdisplaymaskrectangle_rightedgepointskey)
- [CVPixelBuffer](/documentation/corevideo/cvpixelbuffer-q2e)

### Creating pixel buffers

- [func CVPixelBufferCreate(CFAllocator?, Int, Int, OSType, CFDictionary?, UnsafeMutablePointer<CVPixelBuffer?>) -> CVReturn](/documentation/corevideo/cvpixelbuffercreate(_:_:_:_:_:_:))
- [func CVPixelBufferCreateWithBytes(CFAllocator?, Int, Int, OSType, UnsafeMutableRawPointer, Int, CVPixelBufferReleaseBytesCallback?, UnsafeMutableRawPointer?, CFDictionary?, UnsafeMutablePointer<CVPixelBuffer?>) -> CVReturn](/documentation/corevideo/cvpixelbuffercreatewithbytes(_:_:_:_:_:_:_:_:_:_:))
- [func CVPixelBufferCreateWithPlanarBytes(CFAllocator?, Int, Int, OSType, UnsafeMutableRawPointer?, Int, Int, UnsafeMutablePointer<UnsafeMutableRawPointer?>, UnsafeMutablePointer<Int>, UnsafeMutablePointer<Int>, UnsafeMutablePointer<Int>, CVPixelBufferReleasePlanarBytesCallback?, UnsafeMutableRawPointer?, CFDictionary?, UnsafeMutablePointer<CVPixelBuffer?>) -> CVReturn](/documentation/corevideo/cvpixelbuffercreatewithplanarbytes(_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [func CVPixelBufferCreateWithIOSurface(CFAllocator?, IOSurfaceRef, CFDictionary?, UnsafeMutablePointer<Unmanaged<CVPixelBuffer>?>) -> CVReturn](/documentation/corevideo/cvpixelbuffercreatewithiosurface(_:_:_:_:))

### Inspecting Pixel Buffers

- [func CVPixelBufferGetBaseAddress(CVPixelBuffer) -> UnsafeMutableRawPointer?](/documentation/corevideo/cvpixelbuffergetbaseaddress(_:))
- [func CVPixelBufferGetBaseAddressOfPlane(CVPixelBuffer, Int) -> UnsafeMutableRawPointer?](/documentation/corevideo/cvpixelbuffergetbaseaddressofplane(_:_:))
- [func CVPixelBufferGetBytesPerRow(CVPixelBuffer) -> Int](/documentation/corevideo/cvpixelbuffergetbytesperrow(_:))
- [func CVPixelBufferGetBytesPerRowOfPlane(CVPixelBuffer, Int) -> Int](/documentation/corevideo/cvpixelbuffergetbytesperrowofplane(_:_:))
- [func CVPixelBufferGetHeight(CVPixelBuffer) -> Int](/documentation/corevideo/cvpixelbuffergetheight(_:))
- [func CVPixelBufferGetHeightOfPlane(CVPixelBuffer, Int) -> Int](/documentation/corevideo/cvpixelbuffergetheightofplane(_:_:))
- [func CVPixelBufferGetWidth(CVPixelBuffer) -> Int](/documentation/corevideo/cvpixelbuffergetwidth(_:))
- [func CVPixelBufferGetWidthOfPlane(CVPixelBuffer, Int) -> Int](/documentation/corevideo/cvpixelbuffergetwidthofplane(_:_:))
- [func CVPixelBufferIsPlanar(CVPixelBuffer) -> Bool](/documentation/corevideo/cvpixelbufferisplanar(_:))
- [func CVPixelBufferGetPlaneCount(CVPixelBuffer) -> Int](/documentation/corevideo/cvpixelbuffergetplanecount(_:))
- [func CVPixelBufferGetDataSize(CVPixelBuffer) -> Int](/documentation/corevideo/cvpixelbuffergetdatasize(_:))
- [func CVPixelBufferGetPixelFormatType(CVPixelBuffer) -> OSType](/documentation/corevideo/cvpixelbuffergetpixelformattype(_:))
- [func CVPixelBufferGetExtendedPixels(CVPixelBuffer, UnsafeMutablePointer<Int>?, UnsafeMutablePointer<Int>?, UnsafeMutablePointer<Int>?, UnsafeMutablePointer<Int>?)](/documentation/corevideo/cvpixelbuffergetextendedpixels(_:_:_:_:_:))
- [func CVPixelBufferGetIOSurface(CVPixelBuffer?) -> Unmanaged<IOSurfaceRef>?](/documentation/corevideo/cvpixelbuffergetiosurface(_:))
- [func CVPixelBufferCreateResolvedAttributesDictionary(CFAllocator?, CFArray?, UnsafeMutablePointer<CFDictionary?>) -> CVReturn](/documentation/corevideo/cvpixelbuffercreateresolvedattributesdictionary(_:_:_:))
- [func CVPixelBufferGetTypeID() -> CFTypeID](/documentation/corevideo/cvpixelbuffergettypeid())

### Modifying Pixel Buffers

- [func CVPixelBufferFillExtendedPixels(CVPixelBuffer) -> CVReturn](/documentation/corevideo/cvpixelbufferfillextendedpixels(_:))
- [func CVPixelBufferLockBaseAddress(CVPixelBuffer, CVPixelBufferLockFlags) -> CVReturn](/documentation/corevideo/cvpixelbufferlockbaseaddress(_:_:))
- [func CVPixelBufferUnlockBaseAddress(CVPixelBuffer, CVPixelBufferLockFlags) -> CVReturn](/documentation/corevideo/cvpixelbufferunlockbaseaddress(_:_:))

### Data Types

- [CVPixelBuffer](/documentation/corevideo/cvpixelbuffer)
- [CVPixelBufferLockFlags](/documentation/corevideo/cvpixelbufferlockflags)

#### Constants

- [static var readOnly: CVPixelBufferLockFlags](/documentation/corevideo/cvpixelbufferlockflags/readonly)

#### Initializers

- [init(rawValue: CVOptionFlags)](/documentation/corevideo/cvpixelbufferlockflags/init(rawvalue:))
- [CVPlanarComponentInfo](/documentation/corevideo/cvplanarcomponentinfo)

#### Initializers

- [init()](/documentation/corevideo/cvplanarcomponentinfo/init())
- [init(offset: Int32, rowBytes: UInt32)](/documentation/corevideo/cvplanarcomponentinfo/init(offset:rowbytes:))

#### Properties

- [var offset: Int32](/documentation/corevideo/cvplanarcomponentinfo/offset)
- [var rowBytes: UInt32](/documentation/corevideo/cvplanarcomponentinfo/rowbytes)
- [CVPlanarPixelBufferInfo](/documentation/corevideo/cvplanarpixelbufferinfo)

#### Initializers

- [init()](/documentation/corevideo/cvplanarpixelbufferinfo/init())
- [init(componentInfo: CVPlanarComponentInfo)](/documentation/corevideo/cvplanarpixelbufferinfo/init(componentinfo:))

#### Properties

- [var componentInfo: CVPlanarComponentInfo](/documentation/corevideo/cvplanarpixelbufferinfo/componentinfo)
- [CVPlanarPixelBufferInfo_YCbCrPlanar](/documentation/corevideo/cvplanarpixelbufferinfo_ycbcrplanar)

#### Initializers

- [init()](/documentation/corevideo/cvplanarpixelbufferinfo_ycbcrplanar/init())
- [init(componentInfoY: CVPlanarComponentInfo, componentInfoCb: CVPlanarComponentInfo, componentInfoCr: CVPlanarComponentInfo)](/documentation/corevideo/cvplanarpixelbufferinfo_ycbcrplanar/init(componentinfoy:componentinfocb:componentinfocr:))

#### Properties

- [var componentInfoCb: CVPlanarComponentInfo](/documentation/corevideo/cvplanarpixelbufferinfo_ycbcrplanar/componentinfocb)
- [var componentInfoCr: CVPlanarComponentInfo](/documentation/corevideo/cvplanarpixelbufferinfo_ycbcrplanar/componentinfocr)
- [var componentInfoY: CVPlanarComponentInfo](/documentation/corevideo/cvplanarpixelbufferinfo_ycbcrplanar/componentinfoy)
- [CVPlanarPixelBufferInfo_YCbCrBiPlanar](/documentation/corevideo/cvplanarpixelbufferinfo_ycbcrbiplanar)

#### Initializers

- [init()](/documentation/corevideo/cvplanarpixelbufferinfo_ycbcrbiplanar/init())
- [init(componentInfoY: CVPlanarComponentInfo, componentInfoCbCr: CVPlanarComponentInfo)](/documentation/corevideo/cvplanarpixelbufferinfo_ycbcrbiplanar/init(componentinfoy:componentinfocbcr:))

#### Properties

- [var componentInfoCbCr: CVPlanarComponentInfo](/documentation/corevideo/cvplanarpixelbufferinfo_ycbcrbiplanar/componentinfocbcr)
- [var componentInfoY: CVPlanarComponentInfo](/documentation/corevideo/cvplanarpixelbufferinfo_ycbcrbiplanar/componentinfoy)

### Callbacks

- [CVPixelBufferReleaseBytesCallback](/documentation/corevideo/cvpixelbufferreleasebytescallback)
- [CVPixelBufferReleasePlanarBytesCallback](/documentation/corevideo/cvpixelbufferreleaseplanarbytescallback)

### Constants

- [Pixel Buffer Attribute Keys](/documentation/corevideo/pixel-buffer-attribute-keys)

#### Constants

- [let kCVPixelBufferMemoryAllocatorKey: CFString](/documentation/corevideo/kcvpixelbuffermemoryallocatorkey)
- [let kCVPixelBufferPixelFormatTypeKey: CFString](/documentation/corevideo/kcvpixelbufferpixelformattypekey)
- [let kCVPixelBufferWidthKey: CFString](/documentation/corevideo/kcvpixelbufferwidthkey)
- [let kCVPixelBufferHeightKey: CFString](/documentation/corevideo/kcvpixelbufferheightkey)
- [let kCVPixelBufferExtendedPixelsLeftKey: CFString](/documentation/corevideo/kcvpixelbufferextendedpixelsleftkey)
- [let kCVPixelBufferExtendedPixelsTopKey: CFString](/documentation/corevideo/kcvpixelbufferextendedpixelstopkey)
- [let kCVPixelBufferExtendedPixelsRightKey: CFString](/documentation/corevideo/kcvpixelbufferextendedpixelsrightkey)
- [let kCVPixelBufferExtendedPixelsBottomKey: CFString](/documentation/corevideo/kcvpixelbufferextendedpixelsbottomkey)
- [let kCVPixelBufferBytesPerRowAlignmentKey: CFString](/documentation/corevideo/kcvpixelbufferbytesperrowalignmentkey)
- [let kCVPixelBufferCGBitmapContextCompatibilityKey: CFString](/documentation/corevideo/kcvpixelbuffercgbitmapcontextcompatibilitykey)
- [let kCVPixelBufferCGImageCompatibilityKey: CFString](/documentation/corevideo/kcvpixelbuffercgimagecompatibilitykey)
- [let kCVPixelBufferOpenGLCompatibilityKey: CFString](/documentation/corevideo/kcvpixelbufferopenglcompatibilitykey)
- [let kCVPixelBufferPlaneAlignmentKey: CFString](/documentation/corevideo/kcvpixelbufferplanealignmentkey)
- [let kCVPixelBufferIOSurfacePropertiesKey: CFString](/documentation/corevideo/kcvpixelbufferiosurfacepropertieskey)
- [let kCVPixelBufferOpenGLESCompatibilityKey: CFString](/documentation/corevideo/kcvpixelbufferopenglescompatibilitykey)
- [let kCVPixelBufferMetalCompatibilityKey: CFString](/documentation/corevideo/kcvpixelbuffermetalcompatibilitykey)
- [let kCVPixelBufferIOSurfaceCoreAnimationCompatibilityKey: CFString](/documentation/corevideo/kcvpixelbufferiosurfacecoreanimationcompatibilitykey)
- [let kCVPixelBufferIOSurfaceOpenGLFBOCompatibilityKey: CFString](/documentation/corevideo/kcvpixelbufferiosurfaceopenglfbocompatibilitykey)
- [let kCVPixelBufferIOSurfaceOpenGLESFBOCompatibilityKey: CFString](/documentation/corevideo/kcvpixelbufferiosurfaceopenglesfbocompatibilitykey)
- [let kCVPixelBufferIOSurfaceOpenGLTextureCompatibilityKey: CFString](/documentation/corevideo/kcvpixelbufferiosurfaceopengltexturecompatibilitykey)
- [let kCVPixelBufferIOSurfaceOpenGLESTextureCompatibilityKey: CFString](/documentation/corevideo/kcvpixelbufferiosurfaceopenglestexturecompatibilitykey)
- [let kCVPixelBufferOpenGLTextureCacheCompatibilityKey: CFString](/documentation/corevideo/kcvpixelbufferopengltexturecachecompatibilitykey)
- [let kCVPixelBufferOpenGLESTextureCacheCompatibilityKey: CFString](/documentation/corevideo/kcvpixelbufferopenglestexturecachecompatibilitykey)
- [CVPixelBufferPool](/documentation/corevideo/cvpixelbufferpool-77o)

### Creating pools

- [func CVPixelBufferPoolCreate(CFAllocator?, CFDictionary?, CFDictionary?, UnsafeMutablePointer<CVPixelBufferPool?>) -> CVReturn](/documentation/corevideo/cvpixelbufferpoolcreate(_:_:_:_:))
- [func CVPixelBufferPoolCreatePixelBuffer(CFAllocator?, CVPixelBufferPool, UnsafeMutablePointer<CVPixelBuffer?>) -> CVReturn](/documentation/corevideo/cvpixelbufferpoolcreatepixelbuffer(_:_:_:))
- [func CVPixelBufferPoolCreatePixelBufferWithAuxAttributes(CFAllocator?, CVPixelBufferPool, CFDictionary?, UnsafeMutablePointer<CVPixelBuffer?>) -> CVReturn](/documentation/corevideo/cvpixelbufferpoolcreatepixelbufferwithauxattributes(_:_:_:_:))

### Flushing pools

- [func CVPixelBufferPoolFlush(CVPixelBufferPool, CVPixelBufferPoolFlushFlags)](/documentation/corevideo/cvpixelbufferpoolflush(_:_:))

### Inspecting pools

- [func CVPixelBufferPoolGetAttributes(CVPixelBufferPool) -> CFDictionary?](/documentation/corevideo/cvpixelbufferpoolgetattributes(_:))
- [func CVPixelBufferPoolGetPixelBufferAttributes(CVPixelBufferPool) -> CFDictionary?](/documentation/corevideo/cvpixelbufferpoolgetpixelbufferattributes(_:))
- [func CVPixelBufferPoolGetTypeID() -> CFTypeID](/documentation/corevideo/cvpixelbufferpoolgettypeid())

### Data types

- [CVPixelBufferPool](/documentation/corevideo/cvpixelbufferpool)
- [CVPixelBufferPoolFlushFlags](/documentation/corevideo/cvpixelbufferpoolflushflags)

#### Type Properties

- [static var excessBuffers: CVPixelBufferPoolFlushFlags](/documentation/corevideo/cvpixelbufferpoolflushflags/excessbuffers)

#### Initializers

- [init(rawValue: CVOptionFlags)](/documentation/corevideo/cvpixelbufferpoolflushflags/init(rawvalue:))

### Constants

- [let kCVPixelBufferPoolMinimumBufferCountKey: CFString](/documentation/corevideo/kcvpixelbufferpoolminimumbuffercountkey)
- [let kCVPixelBufferPoolMaximumBufferAgeKey: CFString](/documentation/corevideo/kcvpixelbufferpoolmaximumbufferagekey)
- [let kCVPixelBufferPoolAllocationThresholdKey: CFString](/documentation/corevideo/kcvpixelbufferpoolallocationthresholdkey)

### Notifications

- [let kCVPixelBufferPoolFreeBufferNotification: CFString](/documentation/corevideo/kcvpixelbufferpoolfreebuffernotification)
- [CVPixelFormatDescription](/documentation/corevideo/cvpixelformatdescription)

### Creating Format Descriptions

- [func CVPixelFormatDescriptionCreateWithPixelFormatType(CFAllocator?, OSType) -> CFDictionary?](/documentation/corevideo/cvpixelformatdescriptioncreatewithpixelformattype(_:_:))
- [func CVPixelFormatDescriptionRegisterDescriptionWithPixelFormatType(CFDictionary, OSType)](/documentation/corevideo/cvpixelformatdescriptionregisterdescriptionwithpixelformattype(_:_:))

### Retrieving Format Descriptions

- [func CVPixelFormatDescriptionArrayCreateWithAllPixelFormatTypes(CFAllocator?) -> CFArray?](/documentation/corevideo/cvpixelformatdescriptionarraycreatewithallpixelformattypes(_:))

### Data Types

- [CVFillExtendedPixelsCallBackData](/documentation/corevideo/cvfillextendedpixelscallbackdata)

#### Initializers

- [init()](/documentation/corevideo/cvfillextendedpixelscallbackdata/init())
- [init(version: CFIndex, fillCallBack: CVFillExtendedPixelsCallBack?, refCon: UnsafeMutableRawPointer?)](/documentation/corevideo/cvfillextendedpixelscallbackdata/init(version:fillcallback:refcon:))

#### Properties

- [var fillCallBack: CVFillExtendedPixelsCallBack?](/documentation/corevideo/cvfillextendedpixelscallbackdata/fillcallback)
- [var refCon: UnsafeMutableRawPointer?](/documentation/corevideo/cvfillextendedpixelscallbackdata/refcon)
- [var version: CFIndex](/documentation/corevideo/cvfillextendedpixelscallbackdata/version)

### Callbacks

- [CVFillExtendedPixelsCallBack](/documentation/corevideo/cvfillextendedpixelscallback)

### Constants

- [Pixel Format Description Keys](/documentation/corevideo/pixel-format-description-keys)

#### Constants

- [let kCVPixelFormatComponentRange: CFString](/documentation/corevideo/kcvpixelformatcomponentrange)
- [let kCVPixelFormatComponentRange_FullRange: CFString](/documentation/corevideo/kcvpixelformatcomponentrange_fullrange)
- [let kCVPixelFormatComponentRange_VideoRange: CFString](/documentation/corevideo/kcvpixelformatcomponentrange_videorange)
- [let kCVPixelFormatComponentRange_WideRange: CFString](/documentation/corevideo/kcvpixelformatcomponentrange_widerange)
- [let kCVPixelFormatContainsRGB: CFString](/documentation/corevideo/kcvpixelformatcontainsrgb)
- [let kCVPixelFormatContainsYCbCr: CFString](/documentation/corevideo/kcvpixelformatcontainsycbcr)
- [let kCVPixelFormatName: CFString](/documentation/corevideo/kcvpixelformatname)
- [let kCVPixelFormatConstant: CFString](/documentation/corevideo/kcvpixelformatconstant)
- [let kCVPixelFormatCodecType: CFString](/documentation/corevideo/kcvpixelformatcodectype)
- [let kCVPixelFormatFourCC: CFString](/documentation/corevideo/kcvpixelformatfourcc)
- [let kCVPixelFormatContainsAlpha: CFString](/documentation/corevideo/kcvpixelformatcontainsalpha)
- [let kCVPixelFormatPlanes: CFString](/documentation/corevideo/kcvpixelformatplanes)
- [let kCVPixelFormatBlockWidth: CFString](/documentation/corevideo/kcvpixelformatblockwidth)
- [let kCVPixelFormatBlockHeight: CFString](/documentation/corevideo/kcvpixelformatblockheight)
- [let kCVPixelFormatBitsPerBlock: CFString](/documentation/corevideo/kcvpixelformatbitsperblock)
- [let kCVPixelFormatBlockHorizontalAlignment: CFString](/documentation/corevideo/kcvpixelformatblockhorizontalalignment)
- [let kCVPixelFormatBlockVerticalAlignment: CFString](/documentation/corevideo/kcvpixelformatblockverticalalignment)
- [let kCVPixelFormatBlackBlock: CFString](/documentation/corevideo/kcvpixelformatblackblock)
- [let kCVPixelFormatHorizontalSubsampling: CFString](/documentation/corevideo/kcvpixelformathorizontalsubsampling)
- [let kCVPixelFormatVerticalSubsampling: CFString](/documentation/corevideo/kcvpixelformatverticalsubsampling)
- [let kCVPixelFormatOpenGLFormat: CFString](/documentation/corevideo/kcvpixelformatopenglformat)
- [let kCVPixelFormatOpenGLType: CFString](/documentation/corevideo/kcvpixelformatopengltype)
- [let kCVPixelFormatOpenGLInternalFormat: CFString](/documentation/corevideo/kcvpixelformatopenglinternalformat)
- [let kCVPixelFormatCGBitmapInfo: CFString](/documentation/corevideo/kcvpixelformatcgbitmapinfo)
- [let kCVPixelFormatQDCompatibility: CFString](/documentation/corevideo/kcvpixelformatqdcompatibility)
- [let kCVPixelFormatCGBitmapContextCompatibility: CFString](/documentation/corevideo/kcvpixelformatcgbitmapcontextcompatibility)
- [let kCVPixelFormatCGImageCompatibility: CFString](/documentation/corevideo/kcvpixelformatcgimagecompatibility)
- [let kCVPixelFormatOpenGLCompatibility: CFString](/documentation/corevideo/kcvpixelformatopenglcompatibility)
- [let kCVPixelFormatOpenGLESCompatibility: CFString](/documentation/corevideo/kcvpixelformatopenglescompatibility)
- [let kCVPixelFormatFillExtendedPixelsCallback: CFString](/documentation/corevideo/kcvpixelformatfillextendedpixelscallback)
- [Pixel Format Identifiers](/documentation/corevideo/pixel-format-identifiers)

#### Constants

- [var kCVPixelFormatType_1Monochrome: OSType](/documentation/corevideo/kcvpixelformattype_1monochrome)
- [var kCVPixelFormatType_2Indexed: OSType](/documentation/corevideo/kcvpixelformattype_2indexed)
- [var kCVPixelFormatType_4Indexed: OSType](/documentation/corevideo/kcvpixelformattype_4indexed)
- [var kCVPixelFormatType_8Indexed: OSType](/documentation/corevideo/kcvpixelformattype_8indexed)
- [var kCVPixelFormatType_1IndexedGray_WhiteIsZero: OSType](/documentation/corevideo/kcvpixelformattype_1indexedgray_whiteiszero)
- [var kCVPixelFormatType_2IndexedGray_WhiteIsZero: OSType](/documentation/corevideo/kcvpixelformattype_2indexedgray_whiteiszero)
- [var kCVPixelFormatType_4IndexedGray_WhiteIsZero: OSType](/documentation/corevideo/kcvpixelformattype_4indexedgray_whiteiszero)
- [var kCVPixelFormatType_8IndexedGray_WhiteIsZero: OSType](/documentation/corevideo/kcvpixelformattype_8indexedgray_whiteiszero)
- [var kCVPixelFormatType_16BE555: OSType](/documentation/corevideo/kcvpixelformattype_16be555)
- [var kCVPixelFormatType_16LE555: OSType](/documentation/corevideo/kcvpixelformattype_16le555)
- [var kCVPixelFormatType_16LE5551: OSType](/documentation/corevideo/kcvpixelformattype_16le5551)
- [var kCVPixelFormatType_16BE565: OSType](/documentation/corevideo/kcvpixelformattype_16be565)
- [var kCVPixelFormatType_16LE565: OSType](/documentation/corevideo/kcvpixelformattype_16le565)
- [var kCVPixelFormatType_24RGB: OSType](/documentation/corevideo/kcvpixelformattype_24rgb)
- [var kCVPixelFormatType_24BGR: OSType](/documentation/corevideo/kcvpixelformattype_24bgr)
- [var kCVPixelFormatType_32ARGB: OSType](/documentation/corevideo/kcvpixelformattype_32argb)
- [var kCVPixelFormatType_32BGRA: OSType](/documentation/corevideo/kcvpixelformattype_32bgra)
- [var kCVPixelFormatType_32ABGR: OSType](/documentation/corevideo/kcvpixelformattype_32abgr)
- [var kCVPixelFormatType_32RGBA: OSType](/documentation/corevideo/kcvpixelformattype_32rgba)
- [var kCVPixelFormatType_64ARGB: OSType](/documentation/corevideo/kcvpixelformattype_64argb)
- [var kCVPixelFormatType_48RGB: OSType](/documentation/corevideo/kcvpixelformattype_48rgb)
- [var kCVPixelFormatType_32AlphaGray: OSType](/documentation/corevideo/kcvpixelformattype_32alphagray)
- [var kCVPixelFormatType_16Gray: OSType](/documentation/corevideo/kcvpixelformattype_16gray)
- [var kCVPixelFormatType_30RGB: OSType](/documentation/corevideo/kcvpixelformattype_30rgb)
- [var kCVPixelFormatType_422YpCbCr8: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr8)
- [var kCVPixelFormatType_4444YpCbCrA8: OSType](/documentation/corevideo/kcvpixelformattype_4444ypcbcra8)
- [var kCVPixelFormatType_4444YpCbCrA8R: OSType](/documentation/corevideo/kcvpixelformattype_4444ypcbcra8r)
- [var kCVPixelFormatType_4444AYpCbCr8: OSType](/documentation/corevideo/kcvpixelformattype_4444aypcbcr8)
- [var kCVPixelFormatType_4444AYpCbCr16: OSType](/documentation/corevideo/kcvpixelformattype_4444aypcbcr16)
- [var kCVPixelFormatType_444YpCbCr8: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr8)
- [var kCVPixelFormatType_422YpCbCr16: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr16)
- [var kCVPixelFormatType_422YpCbCr10: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr10)
- [var kCVPixelFormatType_444YpCbCr10: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr10)
- [var kCVPixelFormatType_420YpCbCr8Planar: OSType](/documentation/corevideo/kcvpixelformattype_420ypcbcr8planar)
- [var kCVPixelFormatType_420YpCbCr8PlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_420ypcbcr8planarfullrange)
- [var kCVPixelFormatType_422YpCbCr_4A_8BiPlanar: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr_4a_8biplanar)
- [var kCVPixelFormatType_420YpCbCr8BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_420ypcbcr8biplanarvideorange)
- [var kCVPixelFormatType_420YpCbCr8BiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_420ypcbcr8biplanarfullrange)
- [var kCVPixelFormatType_422YpCbCr8_yuvs: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr8_yuvs)
- [var kCVPixelFormatType_422YpCbCr8FullRange: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr8fullrange)
- [var kCVPixelFormatType_OneComponent8: OSType](/documentation/corevideo/kcvpixelformattype_onecomponent8)
- [var kCVPixelFormatType_TwoComponent8: OSType](/documentation/corevideo/kcvpixelformattype_twocomponent8)
- [var kCVPixelFormatType_OneComponent16Half: OSType](/documentation/corevideo/kcvpixelformattype_onecomponent16half)
- [var kCVPixelFormatType_OneComponent32Float: OSType](/documentation/corevideo/kcvpixelformattype_onecomponent32float)
- [var kCVPixelFormatType_TwoComponent16Half: OSType](/documentation/corevideo/kcvpixelformattype_twocomponent16half)
- [var kCVPixelFormatType_TwoComponent32Float: OSType](/documentation/corevideo/kcvpixelformattype_twocomponent32float)
- [var kCVPixelFormatType_64RGBAHalf: OSType](/documentation/corevideo/kcvpixelformattype_64rgbahalf)
- [var kCVPixelFormatType_128RGBAFloat: OSType](/documentation/corevideo/kcvpixelformattype_128rgbafloat)
- [var kCVPixelFormatType_14Bayer_BGGR: OSType](/documentation/corevideo/kcvpixelformattype_14bayer_bggr)
- [var kCVPixelFormatType_14Bayer_GBRG: OSType](/documentation/corevideo/kcvpixelformattype_14bayer_gbrg)
- [var kCVPixelFormatType_14Bayer_GRBG: OSType](/documentation/corevideo/kcvpixelformattype_14bayer_grbg)
- [var kCVPixelFormatType_14Bayer_RGGB: OSType](/documentation/corevideo/kcvpixelformattype_14bayer_rggb)
- [var kCVPixelFormatType_30RGBLEPackedWideGamut: OSType](/documentation/corevideo/kcvpixelformattype_30rgblepackedwidegamut)
- [var kCVPixelFormatType_ARGB2101010LEPacked: OSType](/documentation/corevideo/kcvpixelformattype_argb2101010lepacked)
- [var kCVPixelFormatType_420YpCbCr10BiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_420ypcbcr10biplanarfullrange)
- [var kCVPixelFormatType_420YpCbCr10BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_420ypcbcr10biplanarvideorange)
- [var kCVPixelFormatType_422YpCbCr10BiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr10biplanarfullrange)
- [var kCVPixelFormatType_422YpCbCr10BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr10biplanarvideorange)
- [var kCVPixelFormatType_444YpCbCr10BiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr10biplanarfullrange)
- [var kCVPixelFormatType_444YpCbCr10BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr10biplanarvideorange)
- [var kCVPixelFormatType_DepthFloat16: OSType](/documentation/corevideo/kcvpixelformattype_depthfloat16)
- [var kCVPixelFormatType_DepthFloat32: OSType](/documentation/corevideo/kcvpixelformattype_depthfloat32)
- [var kCVPixelFormatType_DisparityFloat16: OSType](/documentation/corevideo/kcvpixelformattype_disparityfloat16)
- [var kCVPixelFormatType_DisparityFloat32: OSType](/documentation/corevideo/kcvpixelformattype_disparityfloat32)
- [var kCVPixelFormatType_16VersatileBayer: OSType](/documentation/corevideo/kcvpixelformattype_16versatilebayer)
- [var kCVPixelFormatType_40ARGBLEWideGamut: OSType](/documentation/corevideo/kcvpixelformattype_40argblewidegamut)
- [var kCVPixelFormatType_40ARGBLEWideGamutPremultiplied: OSType](/documentation/corevideo/kcvpixelformattype_40argblewidegamutpremultiplied)
- [var kCVPixelFormatType_420YpCbCr8VideoRange_8A_TriPlanar: OSType](/documentation/corevideo/kcvpixelformattype_420ypcbcr8videorange_8a_triplanar)
- [var kCVPixelFormatType_422YpCbCr16BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr16biplanarvideorange)
- [var kCVPixelFormatType_422YpCbCr8BiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr8biplanarfullrange)
- [var kCVPixelFormatType_422YpCbCr8BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr8biplanarvideorange)
- [var kCVPixelFormatType_4444AYpCbCrFloat: OSType](/documentation/corevideo/kcvpixelformattype_4444aypcbcrfloat)
- [var kCVPixelFormatType_444YpCbCr16BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr16biplanarvideorange)
- [var kCVPixelFormatType_444YpCbCr16VideoRange_16A_TriPlanar: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr16videorange_16a_triplanar)
- [var kCVPixelFormatType_444YpCbCr8BiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr8biplanarfullrange)
- [var kCVPixelFormatType_444YpCbCr8BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr8biplanarvideorange)
- [var kCVPixelFormatType_64RGBALE: OSType](/documentation/corevideo/kcvpixelformattype_64rgbale)
- [var kCVPixelFormatType_64RGBA_DownscaledProResRAW: OSType](/documentation/corevideo/kcvpixelformattype_64rgba_downscaledproresraw)
- [var kCVPixelFormatType_OneComponent10: OSType](/documentation/corevideo/kcvpixelformattype_onecomponent10)
- [var kCVPixelFormatType_OneComponent12: OSType](/documentation/corevideo/kcvpixelformattype_onecomponent12)
- [var kCVPixelFormatType_OneComponent16: OSType](/documentation/corevideo/kcvpixelformattype_onecomponent16)
- [var kCVPixelFormatType_TwoComponent16: OSType](/documentation/corevideo/kcvpixelformattype_twocomponent16)

## Time Management

- [CVTime](/documentation/corevideo/cvtime-q1e)

### Inspecting the Host Clock

- [func CVGetCurrentHostTime() -> UInt64](/documentation/corevideo/cvgetcurrenthosttime())
- [func CVGetHostClockFrequency() -> Double](/documentation/corevideo/cvgethostclockfrequency())
- [func CVGetHostClockMinimumTimeDelta() -> UInt32](/documentation/corevideo/cvgethostclockminimumtimedelta())

### Data Types

- [CVTime](/documentation/corevideo/cvtime)

#### Initializers

- [init()](/documentation/corevideo/cvtime/init())
- [init(timeValue: Int64, timeScale: Int32, flags: Int32)](/documentation/corevideo/cvtime/init(timevalue:timescale:flags:))
- [init(timeValue: Int64, timeScale: Int32)](/documentation/corevideo/cvtime/init(timevalue:timescale:))

#### Properties

- [var flags: Int32](/documentation/corevideo/cvtime/flags)
- [var timeScale: Int32](/documentation/corevideo/cvtime/timescale)
- [var timeValue: Int64](/documentation/corevideo/cvtime/timevalue)

#### Instance Properties

- [var flagOptions: CVTimeFlags](/documentation/corevideo/cvtime/flagoptions)

#### Type Properties

- [static var indefinite: CVTime](/documentation/corevideo/cvtime/indefinite)
- [static var zero: CVTime](/documentation/corevideo/cvtime/zero)
- [CVTimeStamp](/documentation/corevideo/cvtimestamp-api)

#### Data Types

- [CVTimeStamp](/documentation/corevideo/cvtimestamp)

##### Initializers

- [init()](/documentation/corevideo/cvtimestamp/init())
- [init(version: UInt32, videoTimeScale: Int32, videoTime: Int64, hostTime: UInt64, rateScalar: Double, videoRefreshPeriod: Int64, smpteTime: CVSMPTETime, flags: UInt64, reserved: UInt64)](/documentation/corevideo/cvtimestamp/init(version:videotimescale:videotime:hosttime:ratescalar:videorefreshperiod:smptetime:flags:reserved:))
- [init(videoTime: CVTime?, hostTime: UInt64?, rateScaler: Double?, videoRefreshPeriod: Int64?, smpteTime: CVSMPTETime?, topField: Bool, bottomField: Bool)](/documentation/corevideo/cvtimestamp/init(videotime:hosttime:ratescaler:videorefreshperiod:smptetime:topfield:bottomfield:))

##### Properties

- [var flags: UInt64](/documentation/corevideo/cvtimestamp/flags)
- [var hostTime: UInt64](/documentation/corevideo/cvtimestamp/hosttime)
- [var rateScalar: Double](/documentation/corevideo/cvtimestamp/ratescalar)
- [var reserved: UInt64](/documentation/corevideo/cvtimestamp/reserved)
- [var smpteTime: CVSMPTETime](/documentation/corevideo/cvtimestamp/smptetime)
- [var version: UInt32](/documentation/corevideo/cvtimestamp/version)
- [var videoRefreshPeriod: Int64](/documentation/corevideo/cvtimestamp/videorefreshperiod)
- [var videoTime: Int64](/documentation/corevideo/cvtimestamp/videotime)
- [var videoTimeScale: Int32](/documentation/corevideo/cvtimestamp/videotimescale)

##### Instance Properties

- [var flagOptions: CVTimeStampFlags](/documentation/corevideo/cvtimestamp/flagoptions)
- [CVSMPTETime](/documentation/corevideo/cvsmptetime)

#### Initializers

- [init()](/documentation/corevideo/cvsmptetime/init())
- [init(subframes: Int16, subframeDivisor: Int16, counter: UInt32, type: UInt32, flags: UInt32, hours: Int16, minutes: Int16, seconds: Int16, frames: Int16)](/documentation/corevideo/cvsmptetime/init(subframes:subframedivisor:counter:type:flags:hours:minutes:seconds:frames:)-4yakl)
- [init(subframes: Int16, subframeDivisor: Int16, counter: UInt32, type: CVSMPTETimeType, flags: CVSMPTETimeFlags, hours: Int16, minutes: Int16, seconds: Int16, frames: Int16)](/documentation/corevideo/cvsmptetime/init(subframes:subframedivisor:counter:type:flags:hours:minutes:seconds:frames:)-7s092)

#### Properties

- [var counter: UInt32](/documentation/corevideo/cvsmptetime/counter)
- [var flags: UInt32](/documentation/corevideo/cvsmptetime/flags)
- [var frames: Int16](/documentation/corevideo/cvsmptetime/frames)
- [var hours: Int16](/documentation/corevideo/cvsmptetime/hours)
- [var minutes: Int16](/documentation/corevideo/cvsmptetime/minutes)
- [var seconds: Int16](/documentation/corevideo/cvsmptetime/seconds)
- [var subframeDivisor: Int16](/documentation/corevideo/cvsmptetime/subframedivisor)
- [var subframes: Int16](/documentation/corevideo/cvsmptetime/subframes)
- [var type: UInt32](/documentation/corevideo/cvsmptetime/type)

#### Instance Properties

- [var flagOptions: CVSMPTETimeFlags](/documentation/corevideo/cvsmptetime/flagoptions)
- [var typeOptions: CVSMPTETimeType](/documentation/corevideo/cvsmptetime/typeoptions)

### Constants

- [CVTime Values](/documentation/corevideo/cvtime-values)

#### Constants

- [let kCVZeroTime: CVTime](/documentation/corevideo/kcvzerotime)
- [let kCVIndefiniteTime: CVTime](/documentation/corevideo/kcvindefinitetime)

### Enumerations

- [CVSMPTETimeType](/documentation/corevideo/cvsmptetimetype)

#### Constants

- [case type24](/documentation/corevideo/cvsmptetimetype/type24)
- [case type25](/documentation/corevideo/cvsmptetimetype/type25)
- [case type2997](/documentation/corevideo/cvsmptetimetype/type2997)
- [case type2997Drop](/documentation/corevideo/cvsmptetimetype/type2997drop)
- [case type30](/documentation/corevideo/cvsmptetimetype/type30)
- [case type30Drop](/documentation/corevideo/cvsmptetimetype/type30drop)
- [case type5994](/documentation/corevideo/cvsmptetimetype/type5994)
- [case type60](/documentation/corevideo/cvsmptetimetype/type60)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/corevideo/cvsmptetimetype/init(rawvalue:))
- [CVSMPTETimeFlags](/documentation/corevideo/cvsmptetimeflags)

#### Constants

- [static var running: CVSMPTETimeFlags](/documentation/corevideo/cvsmptetimeflags/running)
- [static var valid: CVSMPTETimeFlags](/documentation/corevideo/cvsmptetimeflags/valid)

#### Initializers

- [init(rawValue: UInt32)](/documentation/corevideo/cvsmptetimeflags/init(rawvalue:))
- [CVTimeFlags](/documentation/corevideo/cvtimeflags)

#### Constants

- [static var isIndefinite: CVTimeFlags](/documentation/corevideo/cvtimeflags/isindefinite)

#### Initializers

- [init(rawValue: Int32)](/documentation/corevideo/cvtimeflags/init(rawvalue:))
- [CVTimeStampFlags](/documentation/corevideo/cvtimestampflags)

#### Constants

- [static var bottomField: CVTimeStampFlags](/documentation/corevideo/cvtimestampflags/bottomfield)
- [static var hostTimeValid: CVTimeStampFlags](/documentation/corevideo/cvtimestampflags/hosttimevalid)
- [static var isInterlaced: CVTimeStampFlags](/documentation/corevideo/cvtimestampflags/isinterlaced)
- [static var rateScalarValid: CVTimeStampFlags](/documentation/corevideo/cvtimestampflags/ratescalarvalid)
- [static var smpteTimeValid: CVTimeStampFlags](/documentation/corevideo/cvtimestampflags/smptetimevalid)
- [static var topField: CVTimeStampFlags](/documentation/corevideo/cvtimestampflags/topfield)
- [static var videoHostTimeValid: CVTimeStampFlags](/documentation/corevideo/cvtimestampflags/videohosttimevalid)
- [static var videoRefreshPeriodValid: CVTimeStampFlags](/documentation/corevideo/cvtimestampflags/videorefreshperiodvalid)
- [static var videoTimeValid: CVTimeStampFlags](/documentation/corevideo/cvtimestampflags/videotimevalid)

#### Initializers

- [init(rawValue: UInt64)](/documentation/corevideo/cvtimestampflags/init(rawvalue:))
- [CVDisplayLink](/documentation/corevideo/cvdisplaylink-k0k)

### Creating Display Links

- [func CVDisplayLinkCreateWithCGDisplay(CGDirectDisplayID, UnsafeMutablePointer<CVDisplayLink?>) -> CVReturn](/documentation/corevideo/cvdisplaylinkcreatewithcgdisplay(_:_:))
- [func CVDisplayLinkCreateWithCGDisplays(UnsafeMutablePointer<CGDirectDisplayID>, CFIndex, UnsafeMutablePointer<CVDisplayLink?>) -> CVReturn](/documentation/corevideo/cvdisplaylinkcreatewithcgdisplays(_:_:_:))
- [func CVDisplayLinkCreateWithActiveCGDisplays(UnsafeMutablePointer<CVDisplayLink?>) -> CVReturn](/documentation/corevideo/cvdisplaylinkcreatewithactivecgdisplays(_:))
- [func CVDisplayLinkCreateWithOpenGLDisplayMask(CGOpenGLDisplayMask, UnsafeMutablePointer<CVDisplayLink?>) -> CVReturn](/documentation/corevideo/cvdisplaylinkcreatewithopengldisplaymask(_:_:))

### Configuring Display Links

- [func CVDisplayLinkSetCurrentCGDisplay(CVDisplayLink, CGDirectDisplayID) -> CVReturn](/documentation/corevideo/cvdisplaylinksetcurrentcgdisplay(_:_:))
- [func CVDisplayLinkSetCurrentCGDisplayFromOpenGLContext(CVDisplayLink, CGLContextObj, CGLPixelFormatObj) -> CVReturn](/documentation/corevideo/cvdisplaylinksetcurrentcgdisplayfromopenglcontext(_:_:_:))
- [func CVDisplayLinkSetOutputCallback(CVDisplayLink, CVDisplayLinkOutputCallback?, UnsafeMutableRawPointer?) -> CVReturn](/documentation/corevideo/cvdisplaylinksetoutputcallback(_:_:_:))
- [func CVDisplayLinkSetOutputHandler(CVDisplayLink, CVDisplayLinkOutputHandler) -> CVReturn](/documentation/corevideo/cvdisplaylinksetoutputhandler(_:_:))
- [CVDisplayLinkOutputHandler](/documentation/corevideo/cvdisplaylinkoutputhandler)

### Inspecting Display Links

- [func CVDisplayLinkGetCurrentCGDisplay(CVDisplayLink) -> CGDirectDisplayID](/documentation/corevideo/cvdisplaylinkgetcurrentcgdisplay(_:))
- [func CVDisplayLinkGetCurrentTime(CVDisplayLink, UnsafeMutablePointer<CVTimeStamp>) -> CVReturn](/documentation/corevideo/cvdisplaylinkgetcurrenttime(_:_:))
- [func CVDisplayLinkTranslateTime(CVDisplayLink, UnsafePointer<CVTimeStamp>, UnsafeMutablePointer<CVTimeStamp>) -> CVReturn](/documentation/corevideo/cvdisplaylinktranslatetime(_:_:_:))
- [func CVDisplayLinkGetActualOutputVideoRefreshPeriod(CVDisplayLink) -> Double](/documentation/corevideo/cvdisplaylinkgetactualoutputvideorefreshperiod(_:))
- [func CVDisplayLinkGetNominalOutputVideoRefreshPeriod(CVDisplayLink) -> CVTime](/documentation/corevideo/cvdisplaylinkgetnominaloutputvideorefreshperiod(_:))
- [func CVDisplayLinkGetOutputVideoLatency(CVDisplayLink) -> CVTime](/documentation/corevideo/cvdisplaylinkgetoutputvideolatency(_:))
- [func CVDisplayLinkIsRunning(CVDisplayLink) -> Bool](/documentation/corevideo/cvdisplaylinkisrunning(_:))
- [func CVDisplayLinkGetTypeID() -> CFTypeID](/documentation/corevideo/cvdisplaylinkgettypeid())

### Managing Display Links

- [func CVDisplayLinkStart(CVDisplayLink) -> CVReturn](/documentation/corevideo/cvdisplaylinkstart(_:))
- [func CVDisplayLinkStop(CVDisplayLink) -> CVReturn](/documentation/corevideo/cvdisplaylinkstop(_:))

### Data Types

- [CVDisplayLink](/documentation/corevideo/cvdisplaylink)
- [CVOptionFlags](/documentation/corevideo/cvoptionflags)

### Callbacks

- [CVDisplayLinkOutputCallback](/documentation/corevideo/cvdisplaylinkoutputcallback)
- [CVDisplayLinkOutputHandler](/documentation/corevideo/cvdisplaylinkoutputhandler)

## Metal

- [CVMetalTextureCache](/documentation/corevideo/cvmetaltexturecache-q3j)

### Functions

- [func CVMetalTextureCacheCreate(CFAllocator?, CFDictionary?, any MTLDevice, CFDictionary?, UnsafeMutablePointer<CVMetalTextureCache?>) -> CVReturn](/documentation/corevideo/cvmetaltexturecachecreate(_:_:_:_:_:))
- [func CVMetalTextureCacheCreateTextureFromImage(CFAllocator?, CVMetalTextureCache, CVImageBuffer, CFDictionary?, MTLPixelFormat, Int, Int, Int, UnsafeMutablePointer<CVMetalTexture?>) -> CVReturn](/documentation/corevideo/cvmetaltexturecachecreatetexturefromimage(_:_:_:_:_:_:_:_:_:))
- [func CVMetalTextureCacheFlush(CVMetalTextureCache, CVOptionFlags)](/documentation/corevideo/cvmetaltexturecacheflush(_:_:))
- [func CVMetalTextureCacheGetTypeID() -> CFTypeID](/documentation/corevideo/cvmetaltexturecachegettypeid())

### Data Types

- [CVMetalTextureCache](/documentation/corevideo/cvmetaltexturecache)

### Constants

- [Cache Attributes](/documentation/corevideo/cvmetaltexturecache-cache-attributes)

#### Constants

- [let kCVMetalTextureCacheMaximumTextureAgeKey: CFString](/documentation/corevideo/kcvmetaltexturecachemaximumtextureagekey)
- [let kCVMetalTextureUsage: CFString](/documentation/corevideo/kcvmetaltextureusage)

### Related Documentation

- [Setting up a command structure](/documentation/metal/setting-up-a-command-structure)
- [CVMetalTexture](/documentation/corevideo/cvmetaltexture-q3g)

### Inspecting Textures

- [func CVMetalTextureGetTexture(CVMetalTexture) -> (any MTLTexture)?](/documentation/corevideo/cvmetaltexturegettexture(_:))
- [func CVMetalTextureGetCleanTexCoords(CVMetalTexture, UnsafeMutablePointer<Float>, UnsafeMutablePointer<Float>, UnsafeMutablePointer<Float>, UnsafeMutablePointer<Float>)](/documentation/corevideo/cvmetaltexturegetcleantexcoords(_:_:_:_:_:))
- [func CVMetalTextureIsFlipped(CVMetalTexture) -> Bool](/documentation/corevideo/cvmetaltextureisflipped(_:))
- [func CVMetalTextureGetTypeID() -> CFTypeID](/documentation/corevideo/cvmetaltexturegettypeid())

### Data Types

- [CVMetalTexture](/documentation/corevideo/cvmetaltexture)

## OpenGL

- [CVOpenGLTextureCache](/documentation/corevideo/cvopengltexturecache-780)

### Functions

- [func CVOpenGLTextureCacheCreate(CFAllocator?, CFDictionary?, CGLContextObj, CGLPixelFormatObj, CFDictionary?, UnsafeMutablePointer<CVOpenGLTextureCache?>) -> CVReturn](/documentation/corevideo/cvopengltexturecachecreate(_:_:_:_:_:_:))
- [func CVOpenGLTextureCacheCreateTextureFromImage(CFAllocator?, CVOpenGLTextureCache, CVImageBuffer, CFDictionary?, UnsafeMutablePointer<CVOpenGLTexture?>) -> CVReturn](/documentation/corevideo/cvopengltexturecachecreatetexturefromimage(_:_:_:_:_:))
- [func CVOpenGLTextureCacheFlush(CVOpenGLTextureCache, CVOptionFlags)](/documentation/corevideo/cvopengltexturecacheflush(_:_:))
- [func CVOpenGLTextureCacheGetTypeID() -> CFTypeID](/documentation/corevideo/cvopengltexturecachegettypeid())

### Data Types

- [CVOpenGLTextureCache](/documentation/corevideo/cvopengltexturecache)

### Constants

- [Cache Attributes](/documentation/corevideo/cvopengltexturecache-cache-attributes)

#### Key

- [let kCVOpenGLTextureCacheChromaSamplingModeKey: CFString](/documentation/corevideo/kcvopengltexturecachechromasamplingmodekey)

#### Values

- [let kCVOpenGLTextureCacheChromaSamplingModeAutomatic: CFString](/documentation/corevideo/kcvopengltexturecachechromasamplingmodeautomatic)
- [let kCVOpenGLTextureCacheChromaSamplingModeHighestQuality: CFString](/documentation/corevideo/kcvopengltexturecachechromasamplingmodehighestquality)
- [let kCVOpenGLTextureCacheChromaSamplingModeBestPerformance: CFString](/documentation/corevideo/kcvopengltexturecachechromasamplingmodebestperformance)
- [CVOpenGLTexture](/documentation/corevideo/cvopengltexture-782)

### Inspecting Textures

- [func CVOpenGLTextureGetName(CVOpenGLTexture) -> GLuint](/documentation/corevideo/cvopengltexturegetname(_:))
- [func CVOpenGLTextureGetTarget(CVOpenGLTexture) -> GLenum](/documentation/corevideo/cvopengltexturegettarget(_:))
- [func CVOpenGLTextureGetCleanTexCoords(CVOpenGLTexture, UnsafeMutablePointer<GLfloat>, UnsafeMutablePointer<GLfloat>, UnsafeMutablePointer<GLfloat>, UnsafeMutablePointer<GLfloat>)](/documentation/corevideo/cvopengltexturegetcleantexcoords(_:_:_:_:_:))
- [func CVOpenGLTextureIsFlipped(CVOpenGLTexture) -> Bool](/documentation/corevideo/cvopengltextureisflipped(_:))
- [func CVOpenGLTextureGetTypeID() -> CFTypeID](/documentation/corevideo/cvopengltexturegettypeid())

### Data Types

- [CVOpenGLTexture](/documentation/corevideo/cvopengltexture)
- [CVOpenGLBuffer](/documentation/corevideo/cvopenglbuffer-77s)

### Functions

- [func CVOpenGLBufferCreate(CFAllocator?, Int, Int, CFDictionary?, UnsafeMutablePointer<CVOpenGLBuffer?>) -> CVReturn](/documentation/corevideo/cvopenglbuffercreate(_:_:_:_:_:))
- [func CVOpenGLBufferAttach(CVOpenGLBuffer, CGLContextObj, GLenum, GLint, GLint) -> CVReturn](/documentation/corevideo/cvopenglbufferattach(_:_:_:_:_:))
- [func CVOpenGLBufferGetAttributes(CVOpenGLBuffer) -> Unmanaged<CFDictionary>?](/documentation/corevideo/cvopenglbuffergetattributes(_:))
- [func CVOpenGLBufferGetTypeID() -> CFTypeID](/documentation/corevideo/cvopenglbuffergettypeid())

### Data Types

- [CVOpenGLBuffer](/documentation/corevideo/cvopenglbuffer)

### Constants

- [let kCVOpenGLBufferHeight: CFString](/documentation/corevideo/kcvopenglbufferheight)
- [let kCVOpenGLBufferInternalFormat: CFString](/documentation/corevideo/kcvopenglbufferinternalformat)
- [let kCVOpenGLBufferMaximumMipmapLevel: CFString](/documentation/corevideo/kcvopenglbuffermaximummipmaplevel)
- [let kCVOpenGLBufferTarget: CFString](/documentation/corevideo/kcvopenglbuffertarget)
- [let kCVOpenGLBufferWidth: CFString](/documentation/corevideo/kcvopenglbufferwidth)
- [CVOpenGLBufferPool](/documentation/corevideo/cvopenglbufferpool-77j)

### Functions

- [func CVOpenGLBufferPoolCreate(CFAllocator?, CFDictionary?, CFDictionary?, UnsafeMutablePointer<CVOpenGLBufferPool?>) -> CVReturn](/documentation/corevideo/cvopenglbufferpoolcreate(_:_:_:_:))
- [func CVOpenGLBufferPoolCreateOpenGLBuffer(CFAllocator?, CVOpenGLBufferPool, UnsafeMutablePointer<CVOpenGLBuffer?>) -> CVReturn](/documentation/corevideo/cvopenglbufferpoolcreateopenglbuffer(_:_:_:))
- [func CVOpenGLBufferPoolGetAttributes(CVOpenGLBufferPool) -> Unmanaged<CFDictionary>?](/documentation/corevideo/cvopenglbufferpoolgetattributes(_:))
- [func CVOpenGLBufferPoolGetOpenGLBufferAttributes(CVOpenGLBufferPool) -> Unmanaged<CFDictionary>?](/documentation/corevideo/cvopenglbufferpoolgetopenglbufferattributes(_:))
- [func CVOpenGLBufferPoolGetTypeID() -> CFTypeID](/documentation/corevideo/cvopenglbufferpoolgettypeid())

### Data Types

- [CVOpenGLBufferPool](/documentation/corevideo/cvopenglbufferpool)

### Constants

- [let kCVOpenGLBufferPoolMaximumBufferAgeKey: CFString](/documentation/corevideo/kcvopenglbufferpoolmaximumbufferagekey)
- [let kCVOpenGLBufferPoolMinimumBufferCountKey: CFString](/documentation/corevideo/kcvopenglbufferpoolminimumbuffercountkey)

## OpenGL ES

- [CVOpenGLESTextureCache](/documentation/corevideo/cvopenglestexturecache-q2r)

### Functions

- [func CVOpenGLESTextureCacheCreate(CFAllocator?, CFDictionary?, CVEAGLContext, CFDictionary?, UnsafeMutablePointer<CVOpenGLESTextureCache?>) -> CVReturn](/documentation/corevideo/cvopenglestexturecachecreate(_:_:_:_:_:))
- [func CVOpenGLESTextureCacheCreateTextureFromImage(CFAllocator?, CVOpenGLESTextureCache, CVImageBuffer, CFDictionary?, GLenum, GLint, GLsizei, GLsizei, GLenum, GLenum, Int, UnsafeMutablePointer<CVOpenGLESTexture?>) -> CVReturn](/documentation/corevideo/cvopenglestexturecachecreatetexturefromimage(_:_:_:_:_:_:_:_:_:_:_:_:))
- [func CVOpenGLESTextureCacheFlush(CVOpenGLESTextureCache, CVOptionFlags)](/documentation/corevideo/cvopenglestexturecacheflush(_:_:))
- [func CVOpenGLESTextureCacheGetTypeID() -> CFTypeID](/documentation/corevideo/cvopenglestexturecachegettypeid())

### Data Types

- [CVOpenGLESTextureCache](/documentation/corevideo/cvopenglestexturecache)
- [CVEAGLContext](/documentation/corevideo/cveaglcontext)

### Constants

- [Cache Attributes](/documentation/corevideo/cvopenglestexturecache-cache-attributes)

#### Constants

- [let kCVOpenGLESTextureCacheMaximumTextureAgeKey: CFString](/documentation/corevideo/kcvopenglestexturecachemaximumtextureagekey)
- [CVOpenGLESTexture](/documentation/corevideo/cvopenglestexture-q2s)

### Inspecting Textures

- [func CVOpenGLESTextureGetTarget(CVOpenGLESTexture) -> GLenum](/documentation/corevideo/cvopenglestexturegettarget(_:))
- [func CVOpenGLESTextureGetName(CVOpenGLESTexture) -> GLuint](/documentation/corevideo/cvopenglestexturegetname(_:))
- [func CVOpenGLESTextureGetCleanTexCoords(CVOpenGLESTexture, UnsafeMutablePointer<GLfloat>, UnsafeMutablePointer<GLfloat>, UnsafeMutablePointer<GLfloat>, UnsafeMutablePointer<GLfloat>)](/documentation/corevideo/cvopenglestexturegetcleantexcoords(_:_:_:_:_:))
- [func CVOpenGLESTextureIsFlipped(CVOpenGLESTexture) -> Bool](/documentation/corevideo/cvopenglestextureisflipped(_:))
- [func CVOpenGLESTextureGetTypeID() -> CFTypeID](/documentation/corevideo/cvopenglestexturegettypeid())

### Data Types

- [CVOpenGLESTexture](/documentation/corevideo/cvopenglestexture)

## Core Video Error Constants

- [Result Codes](/documentation/corevideo/result-codes)

### Common

- [var kCVReturnAllocationFailed: CVReturn](/documentation/corevideo/kcvreturnallocationfailed)
- [var kCVReturnError: CVReturn](/documentation/corevideo/kcvreturnerror)
- [var kCVReturnInvalidArgument: CVReturn](/documentation/corevideo/kcvreturninvalidargument)
- [var kCVReturnSuccess: CVReturn](/documentation/corevideo/kcvreturnsuccess)
- [var kCVReturnUnsupported: CVReturn](/documentation/corevideo/kcvreturnunsupported)
- [var kCVReturnLast: CVReturn](/documentation/corevideo/kcvreturnlast)
- [var kCVReturnFirst: CVReturn](/documentation/corevideo/kcvreturnfirst)

### Pixel Buffer

- [var kCVReturnInvalidPixelBufferAttributes: CVReturn](/documentation/corevideo/kcvreturninvalidpixelbufferattributes)
- [var kCVReturnInvalidPixelFormat: CVReturn](/documentation/corevideo/kcvreturninvalidpixelformat)
- [var kCVReturnInvalidSize: CVReturn](/documentation/corevideo/kcvreturninvalidsize)
- [var kCVReturnPixelBufferNotMetalCompatible: CVReturn](/documentation/corevideo/kcvreturnpixelbuffernotmetalcompatible)
- [var kCVReturnPixelBufferNotOpenGLCompatible: CVReturn](/documentation/corevideo/kcvreturnpixelbuffernotopenglcompatible)

### Buffer Pool

- [var kCVReturnRetry: CVReturn](/documentation/corevideo/kcvreturnretry)
- [var kCVReturnInvalidPoolAttributes: CVReturn](/documentation/corevideo/kcvreturninvalidpoolattributes)
- [var kCVReturnPoolAllocationFailed: CVReturn](/documentation/corevideo/kcvreturnpoolallocationfailed)
- [var kCVReturnWouldExceedAllocationThreshold: CVReturn](/documentation/corevideo/kcvreturnwouldexceedallocationthreshold)

### Display Link

- [var kCVReturnInvalidDisplay: CVReturn](/documentation/corevideo/kcvreturninvaliddisplay)
- [var kCVReturnDisplayLinkAlreadyRunning: CVReturn](/documentation/corevideo/kcvreturndisplaylinkalreadyrunning)
- [var kCVReturnDisplayLinkNotRunning: CVReturn](/documentation/corevideo/kcvreturndisplaylinknotrunning)
- [var kCVReturnDisplayLinkCallbacksNotSet: CVReturn](/documentation/corevideo/kcvreturndisplaylinkcallbacksnotset)
- [Data Types](/documentation/corevideo/data-types)

### Data Types

- [CVReturn](/documentation/corevideo/cvreturn)

## Reference

- [Core Video Enumerations](/documentation/corevideo/core-video-enumerations)

### Enumerations

- [Anonymous](/documentation/corevideo/anonymous-jbs3)

#### Constants

- [var kCVVersatileBayer_BayerPattern_BGGR: Int](/documentation/corevideo/kcvversatilebayer_bayerpattern_bggr)
- [var kCVVersatileBayer_BayerPattern_GBRG: Int](/documentation/corevideo/kcvversatilebayer_bayerpattern_gbrg)
- [var kCVVersatileBayer_BayerPattern_GRBG: Int](/documentation/corevideo/kcvversatilebayer_bayerpattern_grbg)
- [var kCVVersatileBayer_BayerPattern_RGGB: Int](/documentation/corevideo/kcvversatilebayer_bayerpattern_rggb)
- [Anonymous](/documentation/corevideo/anonymous-3k9gq)

#### Constants

- [var kCVPixelFormatType_Lossless_32BGRA: OSType](/documentation/corevideo/kcvpixelformattype_lossless_32bgra)
- [var kCVPixelFormatType_Lossless_420YpCbCr10PackedBiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_lossless_420ypcbcr10packedbiplanarvideorange)
- [var kCVPixelFormatType_Lossless_420YpCbCr8BiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_lossless_420ypcbcr8biplanarfullrange)
- [var kCVPixelFormatType_Lossless_420YpCbCr8BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_lossless_420ypcbcr8biplanarvideorange)
- [var kCVPixelFormatType_Lossless_422YpCbCr10PackedBiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_lossless_422ypcbcr10packedbiplanarvideorange)
- [Anonymous](/documentation/corevideo/anonymous-1csf0)

#### Constants

- [var kCVPixelFormatType_Lossy_32BGRA: OSType](/documentation/corevideo/kcvpixelformattype_lossy_32bgra)
- [var kCVPixelFormatType_Lossy_420YpCbCr10PackedBiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_lossy_420ypcbcr10packedbiplanarvideorange)
- [var kCVPixelFormatType_Lossy_420YpCbCr8BiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_lossy_420ypcbcr8biplanarfullrange)
- [var kCVPixelFormatType_Lossy_420YpCbCr8BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_lossy_420ypcbcr8biplanarvideorange)
- [var kCVPixelFormatType_Lossy_422YpCbCr10PackedBiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_lossy_422ypcbcr10packedbiplanarvideorange)
- [Core Video Constants](/documentation/corevideo/core-video-constants)

### Constants

- [var COREVIDEO_DECLARE_NULLABILITY: Bool](/documentation/corevideo/corevideo_declare_nullability)
- [var COREVIDEO_FALSE: Bool](/documentation/corevideo/corevideo_false)
- [var COREVIDEO_SUPPORTS_COLORSPACE: Bool](/documentation/corevideo/corevideo_supports_colorspace)
- [var COREVIDEO_SUPPORTS_DIRECT3D: Bool](/documentation/corevideo/corevideo_supports_direct3d)
- [var COREVIDEO_SUPPORTS_DISPLAYLINK: Bool](/documentation/corevideo/corevideo_supports_displaylink)
- [var COREVIDEO_SUPPORTS_GLES_TEX_IMAGE_IOSURFACE: Bool](/documentation/corevideo/corevideo_supports_gles_tex_image_iosurface)
- [var COREVIDEO_SUPPORTS_IOSURFACE: Bool](/documentation/corevideo/corevideo_supports_iosurface)
- [var COREVIDEO_INCLUDED_IOSURFACE_HEADER_FILE: Int32](/documentation/corevideo/corevideo_included_iosurface_header_file)
- [var COREVIDEO_SUPPORTS_IOSURFACE_PREFETCH: Bool](/documentation/corevideo/corevideo_supports_iosurface_prefetch)
- [var COREVIDEO_SUPPORTS_METAL: Bool](/documentation/corevideo/corevideo_supports_metal)
- [var COREVIDEO_SUPPORTS_OPENGL: Bool](/documentation/corevideo/corevideo_supports_opengl)
- [var COREVIDEO_SUPPORTS_OPENGLES: Bool](/documentation/corevideo/corevideo_supports_opengles)
- [var COREVIDEO_SUPPORTS_PERMANENT_ALLOCATOR: Bool](/documentation/corevideo/corevideo_supports_permanent_allocator)
- [var COREVIDEO_SUPPORTS_PREFETCH: Bool](/documentation/corevideo/corevideo_supports_prefetch)
- [var COREVIDEO_TRUE: Bool](/documentation/corevideo/corevideo_true)
- [var COREVIDEO_USE_DERIVED_ENUMS_FOR_CONSTANTS: Bool](/documentation/corevideo/corevideo_use_derived_enums_for_constants)
- [var COREVIDEO_USE_EAGLCONTEXT_CLASS_IN_API: Int32](/documentation/corevideo/corevideo_use_eaglcontext_class_in_api)
- [var COREVIDEO_USE_IOSURFACEREF: Bool](/documentation/corevideo/corevideo_use_iosurfaceref)
- [let kCVImageBufferAlphaChannelModeKey: CFString](/documentation/corevideo/kcvimagebufferalphachannelmodekey)
- [let kCVImageBufferAlphaChannelMode_PremultipliedAlpha: CFString](/documentation/corevideo/kcvimagebufferalphachannelmode_premultipliedalpha)
- [let kCVImageBufferAlphaChannelMode_StraightAlpha: CFString](/documentation/corevideo/kcvimagebufferalphachannelmode_straightalpha)
- [let kCVImageBufferAmbientViewingEnvironmentKey: CFString](/documentation/corevideo/kcvimagebufferambientviewingenvironmentkey)
- [let kCVImageBufferLogTransferFunctionKey: CFString](/documentation/corevideo/kcvimagebufferlogtransferfunctionkey)
- [let kCVImageBufferLogTransferFunction_AppleLog: CFString](/documentation/corevideo/kcvimagebufferlogtransferfunction_applelog)
- [let kCVImageBufferRegionOfInterestKey: CFString](/documentation/corevideo/kcvimagebufferregionofinterestkey)
- [let kCVImageBufferTransferFunction_Linear: CFString](/documentation/corevideo/kcvimagebuffertransferfunction_linear)
- [let kCVMetalTextureStorageMode: CFString](/documentation/corevideo/kcvmetaltexturestoragemode)
- [let kCVPixelBufferProResRAWKey_BlackLevel: CFString](/documentation/corevideo/kcvpixelbufferproresrawkey_blacklevel)
- [let kCVPixelBufferProResRAWKey_ColorMatrix: CFString](/documentation/corevideo/kcvpixelbufferproresrawkey_colormatrix)
- [let kCVPixelBufferProResRAWKey_GainFactor: CFString](/documentation/corevideo/kcvpixelbufferproresrawkey_gainfactor)
- [let kCVPixelBufferProResRAWKey_MetadataExtension: CFString](/documentation/corevideo/kcvpixelbufferproresrawkey_metadataextension)
- [let kCVPixelBufferProResRAWKey_RecommendedCrop: CFString](/documentation/corevideo/kcvpixelbufferproresrawkey_recommendedcrop)
- [let kCVPixelBufferProResRAWKey_SenselSitingOffsets: CFString](/documentation/corevideo/kcvpixelbufferproresrawkey_senselsitingoffsets)
- [let kCVPixelBufferProResRAWKey_WhiteBalanceBlueFactor: CFString](/documentation/corevideo/kcvpixelbufferproresrawkey_whitebalancebluefactor)
- [let kCVPixelBufferProResRAWKey_WhiteBalanceCCT: CFString](/documentation/corevideo/kcvpixelbufferproresrawkey_whitebalancecct)
- [let kCVPixelBufferProResRAWKey_WhiteBalanceRedFactor: CFString](/documentation/corevideo/kcvpixelbufferproresrawkey_whitebalanceredfactor)
- [let kCVPixelBufferProResRAWKey_WhiteLevel: CFString](/documentation/corevideo/kcvpixelbufferproresrawkey_whitelevel)
- [let kCVPixelBufferVersatileBayerKey_BayerPattern: CFString](/documentation/corevideo/kcvpixelbufferversatilebayerkey_bayerpattern)
- [let kCVPixelFormatContainsGrayscale: CFString](/documentation/corevideo/kcvpixelformatcontainsgrayscale)
- [let kCVPixelFormatContainsSenselArray: CFString](/documentation/corevideo/kcvpixelformatcontainssenselarray)
- [Core Video Functions](/documentation/corevideo/core-video-functions)

### Converting between strings and integer code points

- [func CVColorPrimariesGetIntegerCodePointForString(CFString?) -> Int32](/documentation/corevideo/cvcolorprimariesgetintegercodepointforstring(_:))
- [func CVColorPrimariesGetStringForIntegerCodePoint(Int32) -> Unmanaged<CFString>?](/documentation/corevideo/cvcolorprimariesgetstringforintegercodepoint(_:))
- [func CVTransferFunctionGetIntegerCodePointForString(CFString?) -> Int32](/documentation/corevideo/cvtransferfunctiongetintegercodepointforstring(_:))
- [func CVTransferFunctionGetStringForIntegerCodePoint(Int32) -> Unmanaged<CFString>?](/documentation/corevideo/cvtransferfunctiongetstringforintegercodepoint(_:))
- [func CVYCbCrMatrixGetIntegerCodePointForString(CFString?) -> Int32](/documentation/corevideo/cvycbcrmatrixgetintegercodepointforstring(_:))
- [func CVYCbCrMatrixGetStringForIntegerCodePoint(Int32) -> Unmanaged<CFString>?](/documentation/corevideo/cvycbcrmatrixgetstringforintegercodepoint(_:))

### Functions

- [func CVIsCompressedPixelFormatAvailable(OSType) -> Bool](/documentation/corevideo/cviscompressedpixelformatavailable(_:))
- [func CVPixelBufferCopyCreationAttributes(CVPixelBuffer) -> CFDictionary](/documentation/corevideo/cvpixelbuffercopycreationattributes(_:))

## Classes

- [CVMetalBufferCache](/documentation/corevideo/cvmetalbuffercache)
- [CVReadOnlyPixelBuffer](/documentation/corevideo/cvreadonlypixelbuffer)

### Initializers

- [init(consuming CVMutablePixelBuffer)](/documentation/corevideo/cvreadonlypixelbuffer/init(_:))
- [init(unsafeBuffer: sending CVPixelBuffer)](/documentation/corevideo/cvreadonlypixelbuffer/init(unsafebuffer:))

### Instance Methods

- [func withUnsafeBuffer<R>((CVPixelBuffer) throws -> sending R) rethrows -> sending R](/documentation/corevideo/cvreadonlypixelbuffer/withunsafebuffer(_:))

## Protocols

- [CVBufferRepresentable](/documentation/corevideo/cvbufferrepresentable)

### Associated Types

- [Buffer](/documentation/corevideo/cvbufferrepresentable/buffer)

### Instance Methods

- [func withUnsafeBuffer<R>((Self.Buffer) throws -> sending R) rethrows -> sending R](/documentation/corevideo/cvbufferrepresentable/withunsafebuffer(_:))
- [CVImageBufferRepresentable](/documentation/corevideo/cvimagebufferrepresentable)

### Instance Properties

- [var cleanRect: CGRect](/documentation/corevideo/cvimagebufferrepresentable/cleanrect)
- [var colorSpace: CGColorSpace?](/documentation/corevideo/cvimagebufferrepresentable/colorspace)
- [var displaySize: CGSize](/documentation/corevideo/cvimagebufferrepresentable/displaysize)
- [var encodedSize: CGSize](/documentation/corevideo/cvimagebufferrepresentable/encodedsize)
- [var originPosition: CVImageBufferOriginPosition](/documentation/corevideo/cvimagebufferrepresentable/originposition)
- [CVPixelBufferRepresentable](/documentation/corevideo/cvpixelbufferrepresentable)

### Instance Properties

- [var creationAttributes: CVPixelBufferCreationAttributes](/documentation/corevideo/cvpixelbufferrepresentable/creationattributes)
- [var extendedPixels: CVPixelBufferPadding](/documentation/corevideo/cvpixelbufferrepresentable/extendedpixels)
- [var isPlanar: Bool](/documentation/corevideo/cvpixelbufferrepresentable/isplanar)
- [var pixelFormatType: CVPixelFormatType](/documentation/corevideo/cvpixelbufferrepresentable/pixelformattype)
- [var planeCount: Int](/documentation/corevideo/cvpixelbufferrepresentable/planecount)
- [var planeProperties: [CVPixelBufferPlaneProperties]](/documentation/corevideo/cvpixelbufferrepresentable/planeproperties)
- [var size: CVImageSize](/documentation/corevideo/cvpixelbufferrepresentable/size)

### Instance Methods

- [func accessUnsafeRawPlaneBytes<R>(([(properties: CVPixelBufferPlaneProperties, bytes: UnsafeRawBufferPointer)]) throws -> sending R) rethrows -> sending R](/documentation/corevideo/cvpixelbufferrepresentable/accessunsaferawplanebytes(_:))
- [func isCompatibleWith(CVPixelBufferAttributes) -> Bool](/documentation/corevideo/cvpixelbufferrepresentable/iscompatiblewith(_:)-9fsoy)
- [func isCompatibleWith(CVPixelBufferCreationAttributes) -> Bool](/documentation/corevideo/cvpixelbufferrepresentable/iscompatiblewith(_:)-b775)
- [func withUnsafeBackingIOSurfaceIfPresent<R>((IOSurface) throws -> sending R) rethrows -> sending R?](/documentation/corevideo/cvpixelbufferrepresentable/withunsafebackingiosurfaceifpresent(_:))

## Structures

- [CVError](/documentation/corevideo/cverror)

### Initializers

- [init?(rawValue: CVReturn)](/documentation/corevideo/cverror/init(rawvalue:))

### Instance Properties

- [var errorDescription: String?](/documentation/corevideo/cverror/errordescription)

### Type Properties

- [static let allocationFailed: CVError](/documentation/corevideo/cverror/allocationfailed)
- [static let internalError: CVError](/documentation/corevideo/cverror/internalerror)
- [static let invalidArgument: CVError](/documentation/corevideo/cverror/invalidargument)
- [static let invalidPixelBufferAttributes: CVError](/documentation/corevideo/cverror/invalidpixelbufferattributes)
- [static let invalidPixelFormat: CVError](/documentation/corevideo/cverror/invalidpixelformat)
- [static let invalidPoolAttributes: CVError](/documentation/corevideo/cverror/invalidpoolattributes)
- [static let invalidSize: CVError](/documentation/corevideo/cverror/invalidsize)
- [static let pixelBufferNotMetalCompatible: CVError](/documentation/corevideo/cverror/pixelbuffernotmetalcompatible)
- [static let poolAllocationFailed: CVError](/documentation/corevideo/cverror/poolallocationfailed)
- [static let retry: CVError](/documentation/corevideo/cverror/retry)
- [static let unsupported: CVError](/documentation/corevideo/cverror/unsupported)
- [static let wouldExceedAllocationThreshold: CVError](/documentation/corevideo/cverror/wouldexceedallocationthreshold)

### Type Methods

- [static func check(CVReturn) throws(CVError)](/documentation/corevideo/cverror/check(_:))
- [CVImageSize](/documentation/corevideo/cvimagesize)

### Initializers

- [init(CGSize, rounded: FloatingPointRoundingRule)](/documentation/corevideo/cvimagesize/init(_:rounded:))
- [init(width: Int, height: Int)](/documentation/corevideo/cvimagesize/init(width:height:))

### Instance Properties

- [var height: Int](/documentation/corevideo/cvimagesize/height)
- [var width: Int](/documentation/corevideo/cvimagesize/width)

### Type Properties

- [static let zero: CVImageSize](/documentation/corevideo/cvimagesize/zero)
- [CVMutablePixelBuffer](/documentation/corevideo/cvmutablepixelbuffer)

### Classes

- [CVMutablePixelBuffer.Pool](/documentation/corevideo/cvmutablepixelbuffer/pool)

#### Structures

- [CVMutablePixelBuffer.Pool.AllocationAttributes](/documentation/corevideo/cvmutablepixelbuffer/pool/allocationattributes)

##### Initializers

- [init(allocationThreshold: Int?)](/documentation/corevideo/cvmutablepixelbuffer/pool/allocationattributes/init(allocationthreshold:))

##### Instance Properties

- [var allocationThreshold: Int?](/documentation/corevideo/cvmutablepixelbuffer/pool/allocationattributes/allocationthreshold)
- [CVMutablePixelBuffer.Pool.Configuration](/documentation/corevideo/cvmutablepixelbuffer/pool/configuration)

##### Initializers

- [init(ageOutDuration: TimeInterval, minimumBufferCount: Int)](/documentation/corevideo/cvmutablepixelbuffer/pool/configuration/init(ageoutduration:minimumbuffercount:))

##### Instance Properties

- [var ageOutDuration: TimeInterval](/documentation/corevideo/cvmutablepixelbuffer/pool/configuration/ageoutduration)
- [var minimumBufferCount: Int](/documentation/corevideo/cvmutablepixelbuffer/pool/configuration/minimumbuffercount)

#### Initializers

- [init(pixelBufferAttributes: CVPixelBufferCreationAttributes, configuration: CVMutablePixelBuffer.Pool.Configuration) throws](/documentation/corevideo/cvmutablepixelbuffer/pool/init(pixelbufferattributes:configuration:))
- [init(unsafePool: sending CVPixelBufferPool)](/documentation/corevideo/cvmutablepixelbuffer/pool/init(unsafepool:))

#### Instance Properties

- [var pixelBufferAttributes: CVPixelBufferCreationAttributes](/documentation/corevideo/cvmutablepixelbuffer/pool/pixelbufferattributes)

#### Instance Methods

- [func flush(agedOutOnly: Bool)](/documentation/corevideo/cvmutablepixelbuffer/pool/flush(agedoutonly:))
- [func makeMutablePixelBuffer(CVMutablePixelBuffer.Pool.AllocationAttributes) throws -> CVMutablePixelBuffer](/documentation/corevideo/cvmutablepixelbuffer/pool/makemutablepixelbuffer(_:))

### Initializers

- [init(CVPixelBufferCreationAttributes) throws](/documentation/corevideo/cvmutablepixelbuffer/init(_:))
- [init(unsafeBacking: IOSurface, matching: CVPixelBufferCreationAttributes) throws](/documentation/corevideo/cvmutablepixelbuffer/init(unsafebacking:matching:))
- [init(unsafeBuffer: sending CVPixelBuffer)](/documentation/corevideo/cvmutablepixelbuffer/init(unsafebuffer:))

### Instance Methods

- [func accessUnsafeMutableRawPlaneBytes<R>(([(properties: CVPixelBufferPlaneProperties, bytes: UnsafeMutableRawBufferPointer)]) throws -> sending R) rethrows -> sending R](/documentation/corevideo/cvmutablepixelbuffer/accessunsafemutablerawplanebytes(_:))
- [func fillExtendedPixels() -> Bool](/documentation/corevideo/cvmutablepixelbuffer/fillextendedpixels())
- [func withUnsafeBuffer<R>((CVPixelBuffer) throws -> sending R) rethrows -> sending R](/documentation/corevideo/cvmutablepixelbuffer/withunsafebuffer(_:))
- [CVPixelBufferAttributes](/documentation/corevideo/cvpixelbufferattributes)

### Initializers

- [init(CVPixelBufferCreationAttributes)](/documentation/corevideo/cvpixelbufferattributes/init(_:))
- [init?(merging: [CVPixelBufferAttributes])](/documentation/corevideo/cvpixelbufferattributes/init(merging:))
- [init(pixelFormatTypes: [CVPixelFormatType]?, size: CVImageSize?, compatibility: CVPixelFormatDescription.Compatibility, bytesPerRowAlignment: Int?, planeAlignment: Int?, extendedPixels: CVPixelBufferPadding?)](/documentation/corevideo/cvpixelbufferattributes/init(pixelformattypes:size:compatibility:bytesperrowalignment:planealignment:extendedpixels:))
- [init(rawAttributes: [String : any Sendable])](/documentation/corevideo/cvpixelbufferattributes/init(rawattributes:))

### Instance Properties

- [var pixelFormatTypes: [CVPixelFormatType]?](/documentation/corevideo/cvpixelbufferattributes/pixelformattypes)
- [var rawAttributes: [String : any Sendable]](/documentation/corevideo/cvpixelbufferattributes/rawattributes)

### Subscripts

- [subscript(dynamicMember _: WritableKeyPath<CVPixelBufferCreationAttributes, Int?>) -> Int?](/documentation/corevideo/cvpixelbufferattributes/subscript(dynamicmember:)-16n5o)
- [subscript(dynamicMember _: WritableKeyPath<CVPixelBufferCreationAttributes, CVPixelFormatDescription?>) -> CVPixelFormatDescription?](/documentation/corevideo/cvpixelbufferattributes/subscript(dynamicmember:)-2fcvp)
- [subscript(dynamicMember _: WritableKeyPath<CVPixelBufferCreationAttributes, CVPixelBufferPadding?>) -> CVPixelBufferPadding?](/documentation/corevideo/cvpixelbufferattributes/subscript(dynamicmember:)-2kg2b)
- [subscript(dynamicMember _: WritableKeyPath<CVPixelBufferCreationAttributes, CVPixelFormatDescription.Compatibility>) -> CVPixelFormatDescription.Compatibility](/documentation/corevideo/cvpixelbufferattributes/subscript(dynamicmember:)-4r0es)
- [subscript(dynamicMember _: WritableKeyPath<CVPixelBufferCreationAttributes, CVPixelFormatType>) -> CVPixelFormatType?](/documentation/corevideo/cvpixelbufferattributes/subscript(dynamicmember:)-63jp4)
- [subscript(dynamicMember _: WritableKeyPath<CVPixelBufferCreationAttributes, Bool>) -> Bool?](/documentation/corevideo/cvpixelbufferattributes/subscript(dynamicmember:)-7nhki)
- [subscript(dynamicMember _: WritableKeyPath<CVPixelBufferCreationAttributes, CVImageSize>) -> CVImageSize?](/documentation/corevideo/cvpixelbufferattributes/subscript(dynamicmember:)-95xgt)
- [subscript(dynamicMember _: WritableKeyPath<CVPixelBufferCreationAttributes, CVPixelBufferCreationAttributes.Backing>) -> CVPixelBufferCreationAttributes.Backing](/documentation/corevideo/cvpixelbufferattributes/subscript(dynamicmember:)-jo6l)
- [CVPixelBufferCreationAttributes](/documentation/corevideo/cvpixelbuffercreationattributes)

### Initializers

- [init?(CVPixelBufferAttributes)](/documentation/corevideo/cvpixelbuffercreationattributes/init(_:))
- [init(pixelFormatType: CVPixelFormatType, size: CVImageSize, compatibility: CVPixelFormatDescription.Compatibility, bytesPerRowAlignment: Int?, planeAlignment: Int?, extendedPixels: CVPixelBufferPadding?)](/documentation/corevideo/cvpixelbuffercreationattributes/init(pixelformattype:size:compatibility:bytesperrowalignment:planealignment:extendedpixels:))

### Instance Properties

- [var backing: CVPixelBufferCreationAttributes.Backing](/documentation/corevideo/cvpixelbuffercreationattributes/backing-swift.property)
- [var bytesPerRowAlignment: Int?](/documentation/corevideo/cvpixelbuffercreationattributes/bytesperrowalignment)
- [var compatibility: CVPixelFormatDescription.Compatibility](/documentation/corevideo/cvpixelbuffercreationattributes/compatibility)
- [var extendedPixels: CVPixelBufferPadding?](/documentation/corevideo/cvpixelbuffercreationattributes/extendedpixels)
- [var pixelFormatType: CVPixelFormatType](/documentation/corevideo/cvpixelbuffercreationattributes/pixelformattype)
- [var planeAlignment: Int?](/documentation/corevideo/cvpixelbuffercreationattributes/planealignment)
- [var size: CVImageSize](/documentation/corevideo/cvpixelbuffercreationattributes/size)

### Enumerations

- [CVPixelBufferCreationAttributes.Backing](/documentation/corevideo/cvpixelbuffercreationattributes/backing-swift.enum)

#### Enumeration Cases

- [case ioSurface](/documentation/corevideo/cvpixelbuffercreationattributes/backing-swift.enum/iosurface)
- [case ioSurfaceWithProperties([String : any Sendable])](/documentation/corevideo/cvpixelbuffercreationattributes/backing-swift.enum/iosurfacewithproperties(_:))
- [case memory](/documentation/corevideo/cvpixelbuffercreationattributes/backing-swift.enum/memory)
- [CVPixelBufferPadding](/documentation/corevideo/cvpixelbufferpadding)

### Initializers

- [init(left: Int, right: Int, top: Int, bottom: Int)](/documentation/corevideo/cvpixelbufferpadding/init(left:right:top:bottom:))

### Instance Properties

- [var bottom: Int](/documentation/corevideo/cvpixelbufferpadding/bottom)
- [var left: Int](/documentation/corevideo/cvpixelbufferpadding/left)
- [var right: Int](/documentation/corevideo/cvpixelbufferpadding/right)
- [var top: Int](/documentation/corevideo/cvpixelbufferpadding/top)

### Type Properties

- [static let zero: CVPixelBufferPadding](/documentation/corevideo/cvpixelbufferpadding/zero)
- [CVPixelBufferPlaneProperties](/documentation/corevideo/cvpixelbufferplaneproperties)

### Initializers

- [init(size: CVImageSize, bytesPerRow: Int)](/documentation/corevideo/cvpixelbufferplaneproperties/init(size:bytesperrow:))

### Instance Properties

- [var bytesPerRow: Int](/documentation/corevideo/cvpixelbufferplaneproperties/bytesperrow)
- [var size: CVImageSize](/documentation/corevideo/cvpixelbufferplaneproperties/size)
- [CVPixelFormatDescription](/documentation/corevideo/cvpixelformatdescription)

### Creating Format Descriptions

- [func CVPixelFormatDescriptionCreateWithPixelFormatType(CFAllocator?, OSType) -> CFDictionary?](/documentation/corevideo/cvpixelformatdescriptioncreatewithpixelformattype(_:_:))
- [func CVPixelFormatDescriptionRegisterDescriptionWithPixelFormatType(CFDictionary, OSType)](/documentation/corevideo/cvpixelformatdescriptionregisterdescriptionwithpixelformattype(_:_:))

### Retrieving Format Descriptions

- [func CVPixelFormatDescriptionArrayCreateWithAllPixelFormatTypes(CFAllocator?) -> CFArray?](/documentation/corevideo/cvpixelformatdescriptionarraycreatewithallpixelformattypes(_:))

### Data Types

- [CVFillExtendedPixelsCallBackData](/documentation/corevideo/cvfillextendedpixelscallbackdata)

#### Initializers

- [init()](/documentation/corevideo/cvfillextendedpixelscallbackdata/init())
- [init(version: CFIndex, fillCallBack: CVFillExtendedPixelsCallBack?, refCon: UnsafeMutableRawPointer?)](/documentation/corevideo/cvfillextendedpixelscallbackdata/init(version:fillcallback:refcon:))

#### Properties

- [var fillCallBack: CVFillExtendedPixelsCallBack?](/documentation/corevideo/cvfillextendedpixelscallbackdata/fillcallback)
- [var refCon: UnsafeMutableRawPointer?](/documentation/corevideo/cvfillextendedpixelscallbackdata/refcon)
- [var version: CFIndex](/documentation/corevideo/cvfillextendedpixelscallbackdata/version)

### Callbacks

- [CVFillExtendedPixelsCallBack](/documentation/corevideo/cvfillextendedpixelscallback)

### Constants

- [Pixel Format Description Keys](/documentation/corevideo/pixel-format-description-keys)

#### Constants

- [let kCVPixelFormatComponentRange: CFString](/documentation/corevideo/kcvpixelformatcomponentrange)
- [let kCVPixelFormatComponentRange_FullRange: CFString](/documentation/corevideo/kcvpixelformatcomponentrange_fullrange)
- [let kCVPixelFormatComponentRange_VideoRange: CFString](/documentation/corevideo/kcvpixelformatcomponentrange_videorange)
- [let kCVPixelFormatComponentRange_WideRange: CFString](/documentation/corevideo/kcvpixelformatcomponentrange_widerange)
- [let kCVPixelFormatContainsRGB: CFString](/documentation/corevideo/kcvpixelformatcontainsrgb)
- [let kCVPixelFormatContainsYCbCr: CFString](/documentation/corevideo/kcvpixelformatcontainsycbcr)
- [let kCVPixelFormatName: CFString](/documentation/corevideo/kcvpixelformatname)
- [let kCVPixelFormatConstant: CFString](/documentation/corevideo/kcvpixelformatconstant)
- [let kCVPixelFormatCodecType: CFString](/documentation/corevideo/kcvpixelformatcodectype)
- [let kCVPixelFormatFourCC: CFString](/documentation/corevideo/kcvpixelformatfourcc)
- [let kCVPixelFormatContainsAlpha: CFString](/documentation/corevideo/kcvpixelformatcontainsalpha)
- [let kCVPixelFormatPlanes: CFString](/documentation/corevideo/kcvpixelformatplanes)
- [let kCVPixelFormatBlockWidth: CFString](/documentation/corevideo/kcvpixelformatblockwidth)
- [let kCVPixelFormatBlockHeight: CFString](/documentation/corevideo/kcvpixelformatblockheight)
- [let kCVPixelFormatBitsPerBlock: CFString](/documentation/corevideo/kcvpixelformatbitsperblock)
- [let kCVPixelFormatBlockHorizontalAlignment: CFString](/documentation/corevideo/kcvpixelformatblockhorizontalalignment)
- [let kCVPixelFormatBlockVerticalAlignment: CFString](/documentation/corevideo/kcvpixelformatblockverticalalignment)
- [let kCVPixelFormatBlackBlock: CFString](/documentation/corevideo/kcvpixelformatblackblock)
- [let kCVPixelFormatHorizontalSubsampling: CFString](/documentation/corevideo/kcvpixelformathorizontalsubsampling)
- [let kCVPixelFormatVerticalSubsampling: CFString](/documentation/corevideo/kcvpixelformatverticalsubsampling)
- [let kCVPixelFormatOpenGLFormat: CFString](/documentation/corevideo/kcvpixelformatopenglformat)
- [let kCVPixelFormatOpenGLType: CFString](/documentation/corevideo/kcvpixelformatopengltype)
- [let kCVPixelFormatOpenGLInternalFormat: CFString](/documentation/corevideo/kcvpixelformatopenglinternalformat)
- [let kCVPixelFormatCGBitmapInfo: CFString](/documentation/corevideo/kcvpixelformatcgbitmapinfo)
- [let kCVPixelFormatQDCompatibility: CFString](/documentation/corevideo/kcvpixelformatqdcompatibility)
- [let kCVPixelFormatCGBitmapContextCompatibility: CFString](/documentation/corevideo/kcvpixelformatcgbitmapcontextcompatibility)
- [let kCVPixelFormatCGImageCompatibility: CFString](/documentation/corevideo/kcvpixelformatcgimagecompatibility)
- [let kCVPixelFormatOpenGLCompatibility: CFString](/documentation/corevideo/kcvpixelformatopenglcompatibility)
- [let kCVPixelFormatOpenGLESCompatibility: CFString](/documentation/corevideo/kcvpixelformatopenglescompatibility)
- [let kCVPixelFormatFillExtendedPixelsCallback: CFString](/documentation/corevideo/kcvpixelformatfillextendedpixelscallback)
- [Pixel Format Identifiers](/documentation/corevideo/pixel-format-identifiers)

#### Constants

- [var kCVPixelFormatType_1Monochrome: OSType](/documentation/corevideo/kcvpixelformattype_1monochrome)
- [var kCVPixelFormatType_2Indexed: OSType](/documentation/corevideo/kcvpixelformattype_2indexed)
- [var kCVPixelFormatType_4Indexed: OSType](/documentation/corevideo/kcvpixelformattype_4indexed)
- [var kCVPixelFormatType_8Indexed: OSType](/documentation/corevideo/kcvpixelformattype_8indexed)
- [var kCVPixelFormatType_1IndexedGray_WhiteIsZero: OSType](/documentation/corevideo/kcvpixelformattype_1indexedgray_whiteiszero)
- [var kCVPixelFormatType_2IndexedGray_WhiteIsZero: OSType](/documentation/corevideo/kcvpixelformattype_2indexedgray_whiteiszero)
- [var kCVPixelFormatType_4IndexedGray_WhiteIsZero: OSType](/documentation/corevideo/kcvpixelformattype_4indexedgray_whiteiszero)
- [var kCVPixelFormatType_8IndexedGray_WhiteIsZero: OSType](/documentation/corevideo/kcvpixelformattype_8indexedgray_whiteiszero)
- [var kCVPixelFormatType_16BE555: OSType](/documentation/corevideo/kcvpixelformattype_16be555)
- [var kCVPixelFormatType_16LE555: OSType](/documentation/corevideo/kcvpixelformattype_16le555)
- [var kCVPixelFormatType_16LE5551: OSType](/documentation/corevideo/kcvpixelformattype_16le5551)
- [var kCVPixelFormatType_16BE565: OSType](/documentation/corevideo/kcvpixelformattype_16be565)
- [var kCVPixelFormatType_16LE565: OSType](/documentation/corevideo/kcvpixelformattype_16le565)
- [var kCVPixelFormatType_24RGB: OSType](/documentation/corevideo/kcvpixelformattype_24rgb)
- [var kCVPixelFormatType_24BGR: OSType](/documentation/corevideo/kcvpixelformattype_24bgr)
- [var kCVPixelFormatType_32ARGB: OSType](/documentation/corevideo/kcvpixelformattype_32argb)
- [var kCVPixelFormatType_32BGRA: OSType](/documentation/corevideo/kcvpixelformattype_32bgra)
- [var kCVPixelFormatType_32ABGR: OSType](/documentation/corevideo/kcvpixelformattype_32abgr)
- [var kCVPixelFormatType_32RGBA: OSType](/documentation/corevideo/kcvpixelformattype_32rgba)
- [var kCVPixelFormatType_64ARGB: OSType](/documentation/corevideo/kcvpixelformattype_64argb)
- [var kCVPixelFormatType_48RGB: OSType](/documentation/corevideo/kcvpixelformattype_48rgb)
- [var kCVPixelFormatType_32AlphaGray: OSType](/documentation/corevideo/kcvpixelformattype_32alphagray)
- [var kCVPixelFormatType_16Gray: OSType](/documentation/corevideo/kcvpixelformattype_16gray)
- [var kCVPixelFormatType_30RGB: OSType](/documentation/corevideo/kcvpixelformattype_30rgb)
- [var kCVPixelFormatType_422YpCbCr8: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr8)
- [var kCVPixelFormatType_4444YpCbCrA8: OSType](/documentation/corevideo/kcvpixelformattype_4444ypcbcra8)
- [var kCVPixelFormatType_4444YpCbCrA8R: OSType](/documentation/corevideo/kcvpixelformattype_4444ypcbcra8r)
- [var kCVPixelFormatType_4444AYpCbCr8: OSType](/documentation/corevideo/kcvpixelformattype_4444aypcbcr8)
- [var kCVPixelFormatType_4444AYpCbCr16: OSType](/documentation/corevideo/kcvpixelformattype_4444aypcbcr16)
- [var kCVPixelFormatType_444YpCbCr8: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr8)
- [var kCVPixelFormatType_422YpCbCr16: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr16)
- [var kCVPixelFormatType_422YpCbCr10: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr10)
- [var kCVPixelFormatType_444YpCbCr10: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr10)
- [var kCVPixelFormatType_420YpCbCr8Planar: OSType](/documentation/corevideo/kcvpixelformattype_420ypcbcr8planar)
- [var kCVPixelFormatType_420YpCbCr8PlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_420ypcbcr8planarfullrange)
- [var kCVPixelFormatType_422YpCbCr_4A_8BiPlanar: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr_4a_8biplanar)
- [var kCVPixelFormatType_420YpCbCr8BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_420ypcbcr8biplanarvideorange)
- [var kCVPixelFormatType_420YpCbCr8BiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_420ypcbcr8biplanarfullrange)
- [var kCVPixelFormatType_422YpCbCr8_yuvs: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr8_yuvs)
- [var kCVPixelFormatType_422YpCbCr8FullRange: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr8fullrange)
- [var kCVPixelFormatType_OneComponent8: OSType](/documentation/corevideo/kcvpixelformattype_onecomponent8)
- [var kCVPixelFormatType_TwoComponent8: OSType](/documentation/corevideo/kcvpixelformattype_twocomponent8)
- [var kCVPixelFormatType_OneComponent16Half: OSType](/documentation/corevideo/kcvpixelformattype_onecomponent16half)
- [var kCVPixelFormatType_OneComponent32Float: OSType](/documentation/corevideo/kcvpixelformattype_onecomponent32float)
- [var kCVPixelFormatType_TwoComponent16Half: OSType](/documentation/corevideo/kcvpixelformattype_twocomponent16half)
- [var kCVPixelFormatType_TwoComponent32Float: OSType](/documentation/corevideo/kcvpixelformattype_twocomponent32float)
- [var kCVPixelFormatType_64RGBAHalf: OSType](/documentation/corevideo/kcvpixelformattype_64rgbahalf)
- [var kCVPixelFormatType_128RGBAFloat: OSType](/documentation/corevideo/kcvpixelformattype_128rgbafloat)
- [var kCVPixelFormatType_14Bayer_BGGR: OSType](/documentation/corevideo/kcvpixelformattype_14bayer_bggr)
- [var kCVPixelFormatType_14Bayer_GBRG: OSType](/documentation/corevideo/kcvpixelformattype_14bayer_gbrg)
- [var kCVPixelFormatType_14Bayer_GRBG: OSType](/documentation/corevideo/kcvpixelformattype_14bayer_grbg)
- [var kCVPixelFormatType_14Bayer_RGGB: OSType](/documentation/corevideo/kcvpixelformattype_14bayer_rggb)
- [var kCVPixelFormatType_30RGBLEPackedWideGamut: OSType](/documentation/corevideo/kcvpixelformattype_30rgblepackedwidegamut)
- [var kCVPixelFormatType_ARGB2101010LEPacked: OSType](/documentation/corevideo/kcvpixelformattype_argb2101010lepacked)
- [var kCVPixelFormatType_420YpCbCr10BiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_420ypcbcr10biplanarfullrange)
- [var kCVPixelFormatType_420YpCbCr10BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_420ypcbcr10biplanarvideorange)
- [var kCVPixelFormatType_422YpCbCr10BiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr10biplanarfullrange)
- [var kCVPixelFormatType_422YpCbCr10BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr10biplanarvideorange)
- [var kCVPixelFormatType_444YpCbCr10BiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr10biplanarfullrange)
- [var kCVPixelFormatType_444YpCbCr10BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr10biplanarvideorange)
- [var kCVPixelFormatType_DepthFloat16: OSType](/documentation/corevideo/kcvpixelformattype_depthfloat16)
- [var kCVPixelFormatType_DepthFloat32: OSType](/documentation/corevideo/kcvpixelformattype_depthfloat32)
- [var kCVPixelFormatType_DisparityFloat16: OSType](/documentation/corevideo/kcvpixelformattype_disparityfloat16)
- [var kCVPixelFormatType_DisparityFloat32: OSType](/documentation/corevideo/kcvpixelformattype_disparityfloat32)
- [var kCVPixelFormatType_16VersatileBayer: OSType](/documentation/corevideo/kcvpixelformattype_16versatilebayer)
- [var kCVPixelFormatType_40ARGBLEWideGamut: OSType](/documentation/corevideo/kcvpixelformattype_40argblewidegamut)
- [var kCVPixelFormatType_40ARGBLEWideGamutPremultiplied: OSType](/documentation/corevideo/kcvpixelformattype_40argblewidegamutpremultiplied)
- [var kCVPixelFormatType_420YpCbCr8VideoRange_8A_TriPlanar: OSType](/documentation/corevideo/kcvpixelformattype_420ypcbcr8videorange_8a_triplanar)
- [var kCVPixelFormatType_422YpCbCr16BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr16biplanarvideorange)
- [var kCVPixelFormatType_422YpCbCr8BiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr8biplanarfullrange)
- [var kCVPixelFormatType_422YpCbCr8BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_422ypcbcr8biplanarvideorange)
- [var kCVPixelFormatType_4444AYpCbCrFloat: OSType](/documentation/corevideo/kcvpixelformattype_4444aypcbcrfloat)
- [var kCVPixelFormatType_444YpCbCr16BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr16biplanarvideorange)
- [var kCVPixelFormatType_444YpCbCr16VideoRange_16A_TriPlanar: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr16videorange_16a_triplanar)
- [var kCVPixelFormatType_444YpCbCr8BiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr8biplanarfullrange)
- [var kCVPixelFormatType_444YpCbCr8BiPlanarVideoRange: OSType](/documentation/corevideo/kcvpixelformattype_444ypcbcr8biplanarvideorange)
- [var kCVPixelFormatType_64RGBALE: OSType](/documentation/corevideo/kcvpixelformattype_64rgbale)
- [var kCVPixelFormatType_64RGBA_DownscaledProResRAW: OSType](/documentation/corevideo/kcvpixelformattype_64rgba_downscaledproresraw)
- [var kCVPixelFormatType_OneComponent10: OSType](/documentation/corevideo/kcvpixelformattype_onecomponent10)
- [var kCVPixelFormatType_OneComponent12: OSType](/documentation/corevideo/kcvpixelformattype_onecomponent12)
- [var kCVPixelFormatType_OneComponent16: OSType](/documentation/corevideo/kcvpixelformattype_onecomponent16)
- [var kCVPixelFormatType_TwoComponent16: OSType](/documentation/corevideo/kcvpixelformattype_twocomponent16)
- [CVPixelFormatType](/documentation/corevideo/cvpixelformattype)

### Instance Properties

- [var isCompressionAvailable: Bool](/documentation/corevideo/cvpixelformattype/iscompressionavailable)

## Variables

- [let kCVImageBufferDisplayMaskRectangleKey: CFString](/documentation/corevideo/kcvimagebufferdisplaymaskrectanglekey)
- [let kCVImageBufferDisplayMaskRectangleStereoLeftKey: CFString](/documentation/corevideo/kcvimagebufferdisplaymaskrectanglestereoleftkey)
- [let kCVImageBufferDisplayMaskRectangleStereoRightKey: CFString](/documentation/corevideo/kcvimagebufferdisplaymaskrectanglestereorightkey)
- [let kCVImageBufferLogTransferFunction_AppleLog2: CFString](/documentation/corevideo/kcvimagebufferlogtransferfunction_applelog2)
- [let kCVImageBufferPostDecodeProcessingFrameMetadataKey: CFString](/documentation/corevideo/kcvimagebufferpostdecodeprocessingframemetadatakey)
- [let kCVImageBufferPostDecodeProcessingSequenceMetadataKey: CFString](/documentation/corevideo/kcvimagebufferpostdecodeprocessingsequencemetadatakey)
- [let kCVImageBufferSceneIlluminationKey: CFString](/documentation/corevideo/kcvimagebuffersceneilluminationkey)
- [let kCVMetalBufferCacheMaximumBufferAgeKey: CFString](/documentation/corevideo/kcvmetalbuffercachemaximumbufferagekey)
- [let kCVPixelBufferIOSurfacePurgeableKey: CFString](/documentation/corevideo/kcvpixelbufferiosurfacepurgeablekey)
- [let kCVPixelFormatBitsPerComponent: CFString](/documentation/corevideo/kcvpixelformatbitspercomponent)
- [var kCVPixelFormatType_30RGBLE_8A_BiPlanar: OSType](/documentation/corevideo/kcvpixelformattype_30rgble_8a_biplanar)
- [var kCVPixelFormatType_30RGB_r210: OSType](/documentation/corevideo/kcvpixelformattype_30rgb_r210)
- [var kCVPixelFormatType_96VersatileBayerPacked12: OSType](/documentation/corevideo/kcvpixelformattype_96versatilebayerpacked12)
- [var kCVPixelFormatType_Lossless_30RGBLEPackedWideGamut: OSType](/documentation/corevideo/kcvpixelformattype_lossless_30rgblepackedwidegamut)
- [var kCVPixelFormatType_Lossless_30RGBLE_8A_BiPlanar: OSType](/documentation/corevideo/kcvpixelformattype_lossless_30rgble_8a_biplanar)
- [var kCVPixelFormatType_Lossless_420YpCbCr10PackedBiPlanarFullRange: OSType](/documentation/corevideo/kcvpixelformattype_lossless_420ypcbcr10packedbiplanarfullrange)
- [var kCVPixelFormatType_Lossless_64RGBAHalf: OSType](/documentation/corevideo/kcvpixelformattype_lossless_64rgbahalf)

## Functions

- [func CVMetalBufferCacheCreate(CFAllocator?, CFDictionary?, any MTLDevice, UnsafeMutablePointer<CVMetalBufferCache?>) -> CVReturn](/documentation/corevideo/cvmetalbuffercachecreate(_:_:_:_:))
- [func CVMetalBufferCacheCreateBufferFromImage(CFAllocator?, CVMetalBufferCache, CVImageBuffer, UnsafeMutablePointer<CVMetalBuffer?>) -> CVReturn](/documentation/corevideo/cvmetalbuffercachecreatebufferfromimage(_:_:_:_:))
- [func CVMetalBufferCacheFlush(CVMetalBufferCache, CVOptionFlags)](/documentation/corevideo/cvmetalbuffercacheflush(_:_:))
- [func CVMetalBufferCacheGetTypeID() -> CFTypeID](/documentation/corevideo/cvmetalbuffercachegettypeid())
- [func CVMetalBufferGetBuffer(CVMetalBuffer) -> (any MTLBuffer)?](/documentation/corevideo/cvmetalbuffergetbuffer(_:))
- [func CVMetalBufferGetTypeID() -> CFTypeID](/documentation/corevideo/cvmetalbuffergettypeid())
- [func CVPixelBufferIsCompatibleWithAttributes(CVPixelBuffer, CFDictionary?) -> Bool](/documentation/corevideo/cvpixelbufferiscompatiblewithattributes(_:_:))
- [func CVPixelFormatTypeCopyFourCharCodeString(OSType) -> CFString](/documentation/corevideo/cvpixelformattypecopyfourcharcodestring(_:))

## Type Aliases

- [CVMetalBuffer](/documentation/corevideo/cvmetalbuffer)

## Enumerations

- [CVImageBufferOriginPosition](/documentation/corevideo/cvimagebufferoriginposition)

### Enumeration Cases

- [case bottomLeft](/documentation/corevideo/cvimagebufferoriginposition/bottomleft)
- [case topLeft](/documentation/corevideo/cvimagebufferoriginposition/topleft)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
