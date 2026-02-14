# Metal Documentation

Source: https://sosumi.ai/documentation/metal

---
title: Metal
source: https://developer.apple.com/documentation/metal
timestamp: 2026-02-13T19:23:43.906Z
---

## Essentials

- [Understanding the Metal 4 core API](/documentation/metal/understanding-the-metal-4-core-api)
- [Drawing a triangle with Metal 4](/documentation/metal/drawing-a-triangle-with-metal-4)
- [Performing calculations on a GPU](/documentation/metal/performing-calculations-on-a-gpu)
- [Using Metal to draw a view’s contents](/documentation/metal/using-metal-to-draw-a-view's-contents)

## Samples

- [Metal sample code library](/documentation/metal/metal-sample-code-library)

### Compute workflows

- [Performing calculations on a GPU](/documentation/metal/performing-calculations-on-a-gpu)
- [Selecting device objects for compute processing](/documentation/metal/selecting-device-objects-for-compute-processing)
- [Customizing a TensorFlow operation](/documentation/metal/customizing-a-tensorflow-operation)
- [Customizing a PyTorch operation](/documentation/metal/customizing-a-pytorch-operation)

### Render workflows

- [Using Metal to draw a view’s contents](/documentation/metal/using-metal-to-draw-a-view's-contents)
- [Drawing a triangle with Metal 4](/documentation/metal/drawing-a-triangle-with-metal-4)
- [Selecting device objects for graphics rendering](/documentation/metal/selecting-device-objects-for-graphics-rendering)
- [Customizing render pass setup](/documentation/metal/customizing-render-pass-setup)
- [Creating a custom Metal view](/documentation/metal/creating-a-custom-metal-view)
- [Calculating primitive visibility using depth testing](/documentation/metal/calculating-primitive-visibility-using-depth-testing)
- [Encoding indirect command buffers on the CPU](/documentation/metal/encoding-indirect-command-buffers-on-the-cpu)
- [Implementing order-independent transparency with image blocks](/documentation/metal/implementing-order-independent-transparency-with-image-blocks)
- [Loading textures and models using Metal fast resource loading](/documentation/metal/loading-textures-and-models-using-metal-fast-resource-loading)
- [Adjusting the level of detail using Metal mesh shaders](/documentation/metal/adjusting-the-level-of-detail-using-metal-mesh-shaders)
- [Creating a 3D application with hydra rendering](/documentation/metal/creating-a-3d-application-with-hydra-rendering)
- [Culling occluded geometry using the visibility result buffer](/documentation/metal/culling-occluded-geometry-using-the-visibility-result-buffer)
- [Improving edge-rendering quality with multisample antialiasing (MSAA)](/documentation/metal/improving-edge-rendering-quality-with-multisample-antialiasing-msaa)
- [Achieving smooth frame rates with a Metal display link](/documentation/metal/achieving-smooth-frame-rates-with-a-metal-display-link)

### Textures

- [Processing a texture in a compute function](/documentation/metal/processing-a-texture-in-a-compute-function)
- [Reading pixel data from a drawable texture](/documentation/metal/reading-pixel-data-from-a-drawable-texture)
- [Creating and sampling textures](/documentation/metal/creating-and-sampling-textures)
- [Streaming large images with Metal sparse textures](/documentation/metal/streaming-large-images-with-metal-sparse-textures)

### Argument buffers

- [Managing groups of resources with argument buffers](/documentation/metal/managing-groups-of-resources-with-argument-buffers)
- [Using argument buffers with resource heaps](/documentation/metal/using-argument-buffers-with-resource-heaps)
- [Encoding argument buffers on the GPU](/documentation/metal/encoding-argument-buffers-on-the-gpu)
- [Rendering terrain dynamically with argument buffers](/documentation/metal/rendering-terrain-dynamically-with-argument-buffers)

### Shaders

- [Creating a Metal dynamic library](/documentation/metal/creating-a-metal-dynamic-library)
- [Using function specialization to build pipeline variants](/documentation/metal/using-function-specialization-to-build-pipeline-variants)

### Synchronization

- [Synchronizing CPU and GPU work](/documentation/metal/synchronizing-cpu-and-gpu-work)
- [Implementing a multistage image filter using heaps and events](/documentation/metal/implementing-a-multistage-image-filter-using-heaps-and-events)
- [Implementing a multistage image filter using heaps and fences](/documentation/metal/implementing-a-multistage-image-filter-using-heaps-and-fences)

### Lighting techniques

- [Rendering a scene with forward plus lighting using tile shaders](/documentation/metal/rendering-a-scene-with-forward-plus-lighting-using-tile-shaders)
- [Rendering a scene with deferred lighting in Objective-C](/documentation/metal/rendering-a-scene-with-deferred-lighting-in-objective-c)
- [Rendering a scene with deferred lighting in Swift](/documentation/metal/rendering-a-scene-with-deferred-lighting-in-swift)
- [Rendering a scene with deferred lighting in C++](/documentation/metal/rendering-a-scene-with-deferred-lighting-in-c++)
- [Rendering reflections with fewer render passes](/documentation/metal/rendering-reflections-with-fewer-render-passes)

### Multiple techniques

- [Modern rendering with Metal](/documentation/metal/modern-rendering-with-metal)
- [Encoding indirect command buffers on the GPU](/documentation/metal/encoding-indirect-command-buffers-on-the-gpu)

### Ray tracing

- [Rendering reflections in real time using ray tracing](/documentation/metal/rendering-reflections-in-real-time-using-ray-tracing)
- [Accelerating ray tracing using Metal](/documentation/metal/accelerating-ray-tracing-using-metal)
- [Control the ray tracing process using intersection queries](/documentation/metal/control-the-ray-tracing-process-using-intersection-queries)
- [Accelerating ray tracing and motion blur using Metal](/documentation/metal/accelerating-ray-tracing-and-motion-blur-using-metal)
- [Rendering a curve primitive in a ray tracing scene](/documentation/metal/rendering-a-curve-primitive-in-a-ray-tracing-scene)

### HDR

- [Processing HDR images with Metal](/documentation/metal/processing-hdr-images-with-metal)

### OpenGL

- [Migrating OpenGL code to Metal](/documentation/metal/migrating-opengl-code-to-metal)
- [Mixing Metal and OpenGL rendering in a view](/documentation/metal/mixing-metal-and-opengl-rendering-in-a-view)

## GPU devices

- [GPU devices and work submission](/documentation/metal/gpu-devices-and-work-submission)

### Locating and inspecting a GPU device

- [Getting the default GPU](/documentation/metal/getting-the-default-gpu)
- [Detecting GPU features and Metal software versions](/documentation/metal/detecting-gpu-features-and-metal-software-versions)
- [func MTLCreateSystemDefaultDevice() -> (any MTLDevice)?](/documentation/metal/mtlcreatesystemdefaultdevice())
- [MTLDevice](/documentation/metal/mtldevice)

#### Working with GPU devices

- [Device inspection](/documentation/metal/device-inspection)

##### Checking a GPU device’s feature support

- [func supportsFamily(MTLGPUFamily) -> Bool](/documentation/metal/mtldevice/supportsfamily(_:))
- [MTLGPUFamily](/documentation/metal/mtlgpufamily)

###### Checking for Metal family GPU support

- [case metal4](/documentation/metal/mtlgpufamily/metal4)
- [case metal3](/documentation/metal/mtlgpufamily/metal3)

###### Checking for Apple family GPU support

- [case apple9](/documentation/metal/mtlgpufamily/apple9)
- [case apple8](/documentation/metal/mtlgpufamily/apple8)
- [case apple7](/documentation/metal/mtlgpufamily/apple7)
- [case apple6](/documentation/metal/mtlgpufamily/apple6)
- [case apple5](/documentation/metal/mtlgpufamily/apple5)
- [case apple4](/documentation/metal/mtlgpufamily/apple4)
- [case apple3](/documentation/metal/mtlgpufamily/apple3)
- [case apple2](/documentation/metal/mtlgpufamily/apple2)
- [case apple1](/documentation/metal/mtlgpufamily/apple1)

###### Checking for common GPU support

- [case common3](/documentation/metal/mtlgpufamily/common3)
- [case common2](/documentation/metal/mtlgpufamily/common2)
- [case common1](/documentation/metal/mtlgpufamily/common1)

###### Checking for macOS family GPU support

- [case mac2](/documentation/metal/mtlgpufamily/mac2)
- [case mac1](/documentation/metal/mtlgpufamily/mac1)

###### Checking for Mac Catalyst family GPU support

- [case macCatalyst2](/documentation/metal/mtlgpufamily/maccatalyst2)
- [case macCatalyst1](/documentation/metal/mtlgpufamily/maccatalyst1)

###### Swift support

- [init?(rawValue: Int)](/documentation/metal/mtlgpufamily/init(rawvalue:))

###### Enumeration Cases

- [case apple10](/documentation/metal/mtlgpufamily/apple10)
- [func supportsFeatureSet(MTLFeatureSet) -> Bool](/documentation/metal/mtldevice/supportsfeatureset(_:))
- [MTLFeatureSet](/documentation/metal/mtlfeatureset)

###### iOS GPU family 5

- [case iOS_GPUFamily5_v1](/documentation/metal/mtlfeatureset/ios_gpufamily5_v1)

###### iOS GPU family 4

- [case iOS_GPUFamily4_v2](/documentation/metal/mtlfeatureset/ios_gpufamily4_v2)
- [case iOS_GPUFamily4_v1](/documentation/metal/mtlfeatureset/ios_gpufamily4_v1)

###### iOS GPU family 3

- [case iOS_GPUFamily3_v4](/documentation/metal/mtlfeatureset/ios_gpufamily3_v4)
- [case iOS_GPUFamily3_v3](/documentation/metal/mtlfeatureset/ios_gpufamily3_v3)
- [case iOS_GPUFamily3_v2](/documentation/metal/mtlfeatureset/ios_gpufamily3_v2)
- [case iOS_GPUFamily3_v1](/documentation/metal/mtlfeatureset/ios_gpufamily3_v1)

###### iOS GPU family 2

- [case iOS_GPUFamily2_v5](/documentation/metal/mtlfeatureset/ios_gpufamily2_v5)
- [case iOS_GPUFamily2_v4](/documentation/metal/mtlfeatureset/ios_gpufamily2_v4)
- [case iOS_GPUFamily2_v3](/documentation/metal/mtlfeatureset/ios_gpufamily2_v3)
- [case iOS_GPUFamily2_v2](/documentation/metal/mtlfeatureset/ios_gpufamily2_v2)
- [case iOS_GPUFamily2_v1](/documentation/metal/mtlfeatureset/ios_gpufamily2_v1)

###### iOS GPU family 1

- [case iOS_GPUFamily1_v5](/documentation/metal/mtlfeatureset/ios_gpufamily1_v5)
- [case iOS_GPUFamily1_v4](/documentation/metal/mtlfeatureset/ios_gpufamily1_v4)
- [case iOS_GPUFamily1_v3](/documentation/metal/mtlfeatureset/ios_gpufamily1_v3)
- [case iOS_GPUFamily1_v2](/documentation/metal/mtlfeatureset/ios_gpufamily1_v2)
- [case iOS_GPUFamily1_v1](/documentation/metal/mtlfeatureset/ios_gpufamily1_v1)

###### tvOS GPU family 2

- [case tvOS_GPUFamily2_v2](/documentation/metal/mtlfeatureset/tvos_gpufamily2_v2)
- [case tvOS_GPUFamily2_v1](/documentation/metal/mtlfeatureset/tvos_gpufamily2_v1)

###### tvOS GPU family 1

- [case tvOS_GPUFamily1_v4](/documentation/metal/mtlfeatureset/tvos_gpufamily1_v4)
- [case tvOS_GPUFamily1_v3](/documentation/metal/mtlfeatureset/tvos_gpufamily1_v3)
- [case tvOS_GPUFamily1_v2](/documentation/metal/mtlfeatureset/tvos_gpufamily1_v2)
- [case tvOS_GPUFamily1_v1](/documentation/metal/mtlfeatureset/tvos_gpufamily1_v1-swift.enum.case)

###### macOS GPU family 2

- [case macOS_GPUFamily2_v1](/documentation/metal/mtlfeatureset/macos_gpufamily2_v1)

###### macOS GPU family 1

- [case macOS_GPUFamily1_v4](/documentation/metal/mtlfeatureset/macos_gpufamily1_v4)
- [case macOS_GPUFamily1_v3](/documentation/metal/mtlfeatureset/macos_gpufamily1_v3)
- [case macOS_GPUFamily1_v2](/documentation/metal/mtlfeatureset/macos_gpufamily1_v2)
- [case macOS_GPUFamily1_v1](/documentation/metal/mtlfeatureset/macos_gpufamily1_v1)

###### macOS tier 2

- [case macOS_ReadWriteTextureTier2](/documentation/metal/mtlfeatureset/macos_readwritetexturetier2)

###### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlfeatureset/init(rawvalue:))

###### Type Properties

- [static var osx_GPUFamily1_v1: MTLFeatureSet](/documentation/metal/mtlfeatureset/osx_gpufamily1_v1)
- [static var osx_GPUFamily1_v2: MTLFeatureSet](/documentation/metal/mtlfeatureset/osx_gpufamily1_v2)
- [static var osx_ReadWriteTextureTier2: MTLFeatureSet](/documentation/metal/mtlfeatureset/osx_readwritetexturetier2)
- [static var tvos_GPUFamily1_v1: MTLFeatureSet](/documentation/metal/mtlfeatureset/tvos_gpufamily1_v1-swift.type.property)

##### Checking compute support

- [var maxThreadgroupMemoryLength: Int](/documentation/metal/mtldevice/maxthreadgroupmemorylength)
- [var maxThreadsPerThreadgroup: MTLSize](/documentation/metal/mtldevice/maxthreadsperthreadgroup)

##### Checking render support

- [var supportsRaytracing: Bool](/documentation/metal/mtldevice/supportsraytracing)
- [var supportsPrimitiveMotionBlur: Bool](/documentation/metal/mtldevice/supportsprimitivemotionblur)
- [var supportsRaytracingFromRender: Bool](/documentation/metal/mtldevice/supportsraytracingfromrender)
- [var supports32BitMSAA: Bool](/documentation/metal/mtldevice/supports32bitmsaa)
- [var supportsPullModelInterpolation: Bool](/documentation/metal/mtldevice/supportspullmodelinterpolation)
- [var supportsShaderBarycentricCoordinates: Bool](/documentation/metal/mtldevice/supportsshaderbarycentriccoordinates)
- [func supportsVertexAmplificationCount(Int) -> Bool](/documentation/metal/mtldevice/supportsvertexamplificationcount(_:))
- [var areProgrammableSamplePositionsSupported: Bool](/documentation/metal/mtldevice/areprogrammablesamplepositionssupported)
- [var areRasterOrderGroupsSupported: Bool](/documentation/metal/mtldevice/arerasterordergroupssupported)
- [var areBarycentricCoordsSupported: Bool](/documentation/metal/mtldevice/arebarycentriccoordssupported)

##### Checking texture and sampler support

- [var supports32BitFloatFiltering: Bool](/documentation/metal/mtldevice/supports32bitfloatfiltering)
- [var supportsBCTextureCompression: Bool](/documentation/metal/mtldevice/supportsbctexturecompression)
- [var isDepth24Stencil8PixelFormatSupported: Bool](/documentation/metal/mtldevice/isdepth24stencil8pixelformatsupported)
- [var supportsQueryTextureLOD: Bool](/documentation/metal/mtldevice/supportsquerytexturelod)
- [var readWriteTextureSupport: MTLReadWriteTextureTier](/documentation/metal/mtldevice/readwritetexturesupport)

###### Read-write texture tiers

- [MTLReadWriteTextureTier](/documentation/metal/mtlreadwritetexturetier)

###### Enumeration cases

- [case tier1](/documentation/metal/mtlreadwritetexturetier/tier1)
- [case tier2](/documentation/metal/mtlreadwritetexturetier/tier2)
- [case tierNone](/documentation/metal/mtlreadwritetexturetier/tiernone)

###### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlreadwritetexturetier/init(rawvalue:))

##### Checking function pointer support

- [var supportsFunctionPointers: Bool](/documentation/metal/mtldevice/supportsfunctionpointers)
- [var supportsFunctionPointersFromRender: Bool](/documentation/metal/mtldevice/supportsfunctionpointersfromrender)

##### Checking a GPU device’s memory

- [var currentAllocatedSize: Int](/documentation/metal/mtldevice/currentallocatedsize)
- [var recommendedMaxWorkingSetSize: UInt64](/documentation/metal/mtldevice/recommendedmaxworkingsetsize)
- [var hasUnifiedMemory: Bool](/documentation/metal/mtldevice/hasunifiedmemory)
- [var maxTransferRate: UInt64](/documentation/metal/mtldevice/maxtransferrate)

##### Sampling a GPU device’s counters

- [var counterSets: [any MTLCounterSet]?](/documentation/metal/mtldevice/countersets)
- [func supportsCounterSampling(MTLCounterSamplingPoint) -> Bool](/documentation/metal/mtldevice/supportscountersampling(_:))
- [MTLCounterSamplingPoint](/documentation/metal/mtlcountersamplingpoint)

###### Reading sampling boundary types

- [case atBlitBoundary](/documentation/metal/mtlcountersamplingpoint/atblitboundary)
- [case atDispatchBoundary](/documentation/metal/mtlcountersamplingpoint/atdispatchboundary)
- [case atDrawBoundary](/documentation/metal/mtlcountersamplingpoint/atdrawboundary)
- [case atStageBoundary](/documentation/metal/mtlcountersamplingpoint/atstageboundary)
- [case atTileDispatchBoundary](/documentation/metal/mtlcountersamplingpoint/attiledispatchboundary)

###### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlcountersamplingpoint/init(rawvalue:))
- [func makeCounterSampleBuffer(descriptor: MTLCounterSampleBufferDescriptor) throws -> any MTLCounterSampleBuffer](/documentation/metal/mtldevice/makecountersamplebuffer(descriptor:))

##### Sampling GPU and CPU timestamps simultaneously

- [- sampleTimestamps:gpuTimestamp:](/documentation/metal/mtldevice/sampletimestamps())

##### Identifying a GPU device

- [var name: String](/documentation/metal/mtldevice/name)
- [var architecture: MTLArchitecture](/documentation/metal/mtldevice/architecture)
- [MTLArchitecture](/documentation/metal/mtlarchitecture)

###### Inspecting a GPU device’s architecture details

- [var name: String](/documentation/metal/mtlarchitecture/name)
- [var registryID: UInt64](/documentation/metal/mtldevice/registryid)
- [var location: MTLDeviceLocation](/documentation/metal/mtldevice/location)
- [MTLDeviceLocation](/documentation/metal/mtldevicelocation)

###### Determining the GPU’s location

- [case builtIn](/documentation/metal/mtldevicelocation/builtin)
- [case slot](/documentation/metal/mtldevicelocation/slot)
- [case external](/documentation/metal/mtldevicelocation/external)
- [case unspecified](/documentation/metal/mtldevicelocation/unspecified)

###### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtldevicelocation/init(rawvalue:))
- [var locationNumber: Int](/documentation/metal/mtldevice/locationnumber)
- [var isLowPower: Bool](/documentation/metal/mtldevice/islowpower)
- [var isRemovable: Bool](/documentation/metal/mtldevice/isremovable)
- [var isHeadless: Bool](/documentation/metal/mtldevice/isheadless)
- [var peerGroupID: UInt64](/documentation/metal/mtldevice/peergroupid)
- [var peerCount: UInt32](/documentation/metal/mtldevice/peercount)
- [var peerIndex: UInt32](/documentation/metal/mtldevice/peerindex)
- [Work submission](/documentation/metal/work-submission)

##### Creating command queues

- [func makeCommandQueue() -> (any MTLCommandQueue)?](/documentation/metal/mtldevice/makecommandqueue())
- [func makeCommandQueue(maxCommandBufferCount: Int) -> (any MTLCommandQueue)?](/documentation/metal/mtldevice/makecommandqueue(maxcommandbuffercount:))

##### Creating residency sets

- [func makeResidencySet(descriptor: MTLResidencySetDescriptor) throws -> any MTLResidencySet](/documentation/metal/mtldevice/makeresidencyset(descriptor:))

##### Creating I/O command queues

- [func makeIOCommandQueue(descriptor: MTLIOCommandQueueDescriptor) throws -> any MTLIOCommandQueue](/documentation/metal/mtldevice/makeiocommandqueue(descriptor:))

##### Creating I/O file handles

- [func makeIOFileHandle(url: URL) throws -> any MTLIOFileHandle](/documentation/metal/mtldevice/makeiofilehandle(url:))
- [func makeIOFileHandle(url: URL, compressionMethod: MTLIOCompressionMethod) throws -> any MTLIOFileHandle](/documentation/metal/mtldevice/makeiofilehandle(url:compressionmethod:))
- [func makeIOHandle(url: URL) throws -> any MTLIOFileHandle](/documentation/metal/mtldevice/makeiohandle(url:))
- [func makeIOHandle(url: URL, compressionMethod: MTLIOCompressionMethod) throws -> any MTLIOFileHandle](/documentation/metal/mtldevice/makeiohandle(url:compressionmethod:))

##### Creating indirect command buffers

- [func makeIndirectCommandBuffer(descriptor: MTLIndirectCommandBufferDescriptor, maxCommandCount: Int, options: MTLResourceOptions) -> (any MTLIndirectCommandBuffer)?](/documentation/metal/mtldevice/makeindirectcommandbuffer(descriptor:maxcommandcount:options:))
- [Pipeline state creation](/documentation/metal/pipeline-state-creation)

##### Creating render pipeline states with vertex shaders

- [func makeRenderPipelineState(descriptor: MTLRenderPipelineDescriptor) throws -> any MTLRenderPipelineState](/documentation/metal/mtldevice/makerenderpipelinestate(descriptor:))
- [func makeRenderPipelineState(descriptor: MTLRenderPipelineDescriptor, completionHandler: ((any MTLRenderPipelineState)?, (any Error)?) -> Void)](/documentation/metal/mtldevice/makerenderpipelinestate(descriptor:completionhandler:))
- [func makeRenderPipelineState(descriptor: MTLRenderPipelineDescriptor, options: MTLPipelineOption) throws -> (any MTLRenderPipelineState, MTLRenderPipelineReflection?)](/documentation/metal/mtldevice/makerenderpipelinestate(descriptor:options:)-89vxc)
- [func makeRenderPipelineState(descriptor: MTLRenderPipelineDescriptor, options: MTLPipelineOption, reflection: AutoreleasingUnsafeMutablePointer<MTLAutoreleasedRenderPipelineReflection?>?) throws -> any MTLRenderPipelineState](/documentation/metal/mtldevice/makerenderpipelinestate(descriptor:options:reflection:))
- [func makeRenderPipelineState(descriptor: MTLRenderPipelineDescriptor, options: MTLPipelineOption, completionHandler: ((any MTLRenderPipelineState)?, MTLRenderPipelineReflection?, (any Error)?) -> Void)](/documentation/metal/mtldevice/makerenderpipelinestate(descriptor:options:completionhandler:)-5gdww)

##### Creating render pipeline states with mesh shaders

- [func makeRenderPipelineState(descriptor: MTLMeshRenderPipelineDescriptor, options: MTLPipelineOption) throws -> (any MTLRenderPipelineState, MTLRenderPipelineReflection?)](/documentation/metal/mtldevice/makerenderpipelinestate(descriptor:options:)-yrak)
- [func makeRenderPipelineState(descriptor: MTLMeshRenderPipelineDescriptor, options: MTLPipelineOption, completionHandler: ((any MTLRenderPipelineState)?, MTLRenderPipelineReflection?, (any Error)?) -> Void)](/documentation/metal/mtldevice/makerenderpipelinestate(descriptor:options:completionhandler:)-1wvya)

##### Creating tile render pipeline states

- [func makeRenderPipelineState(tileDescriptor: MTLTileRenderPipelineDescriptor, options: MTLPipelineOption) throws -> (any MTLRenderPipelineState, MTLRenderPipelineReflection?)](/documentation/metal/mtldevice/makerenderpipelinestate(tiledescriptor:options:))
- [func makeRenderPipelineState(tileDescriptor: MTLTileRenderPipelineDescriptor, options: MTLPipelineOption, reflection: AutoreleasingUnsafeMutablePointer<MTLAutoreleasedRenderPipelineReflection?>?) throws -> any MTLRenderPipelineState](/documentation/metal/mtldevice/makerenderpipelinestate(tiledescriptor:options:reflection:))
- [func makeRenderPipelineState(tileDescriptor: MTLTileRenderPipelineDescriptor, options: MTLPipelineOption, completionHandler: ((any MTLRenderPipelineState)?, MTLRenderPipelineReflection?, (any Error)?) -> Void)](/documentation/metal/mtldevice/makerenderpipelinestate(tiledescriptor:options:completionhandler:))

##### Creating compute pipeline states

- [func makeComputePipelineState(descriptor: MTLComputePipelineDescriptor, options: MTLPipelineOption, reflection: AutoreleasingUnsafeMutablePointer<MTLAutoreleasedComputePipelineReflection?>?) throws -> any MTLComputePipelineState](/documentation/metal/mtldevice/makecomputepipelinestate(descriptor:options:reflection:))
- [func makeComputePipelineState(descriptor: MTLComputePipelineDescriptor, options: MTLPipelineOption, completionHandler: ((any MTLComputePipelineState)?, MTLComputePipelineReflection?, (any Error)?) -> Void)](/documentation/metal/mtldevice/makecomputepipelinestate(descriptor:options:completionhandler:))
- [func makeComputePipelineState(function: any MTLFunction) throws -> any MTLComputePipelineState](/documentation/metal/mtldevice/makecomputepipelinestate(function:))
- [func makeComputePipelineState(function: any MTLFunction, completionHandler: ((any MTLComputePipelineState)?, (any Error)?) -> Void)](/documentation/metal/mtldevice/makecomputepipelinestate(function:completionhandler:))
- [func makeComputePipelineState(function: any MTLFunction, options: MTLPipelineOption, reflection: AutoreleasingUnsafeMutablePointer<MTLAutoreleasedComputePipelineReflection?>?) throws -> any MTLComputePipelineState](/documentation/metal/mtldevice/makecomputepipelinestate(function:options:reflection:))
- [func makeComputePipelineState(function: any MTLFunction, options: MTLPipelineOption, completionHandler: ((any MTLComputePipelineState)?, MTLComputePipelineReflection?, (any Error)?) -> Void)](/documentation/metal/mtldevice/makecomputepipelinestate(function:options:completionhandler:))

##### Creating depth and stencil states

- [func makeDepthStencilState(descriptor: MTLDepthStencilDescriptor) -> (any MTLDepthStencilState)?](/documentation/metal/mtldevice/makedepthstencilstate(descriptor:))

##### Supporting types

- [MTLNewRenderPipelineStateCompletionHandler](/documentation/metal/mtlnewrenderpipelinestatecompletionhandler)
- [MTLNewRenderPipelineStateWithReflectionCompletionHandler](/documentation/metal/mtlnewrenderpipelinestatewithreflectioncompletionhandler)
- [MTLNewComputePipelineStateCompletionHandler](/documentation/metal/mtlnewcomputepipelinestatecompletionhandler)
- [MTLNewComputePipelineStateWithReflectionCompletionHandler](/documentation/metal/mtlnewcomputepipelinestatewithreflectioncompletionhandler)
- [Resource creation](/documentation/metal/resource-creation)

##### Working with resource heaps

- [func makeHeap(descriptor: MTLHeapDescriptor) -> (any MTLHeap)?](/documentation/metal/mtldevice/makeheap(descriptor:))
- [func heapBufferSizeAndAlign(length: Int, options: MTLResourceOptions) -> MTLSizeAndAlign](/documentation/metal/mtldevice/heapbuffersizeandalign(length:options:))
- [func heapTextureSizeAndAlign(descriptor: MTLTextureDescriptor) -> MTLSizeAndAlign](/documentation/metal/mtldevice/heaptexturesizeandalign(descriptor:))
- [func heapAccelerationStructureSizeAndAlign(size: Int) -> MTLSizeAndAlign](/documentation/metal/mtldevice/heapaccelerationstructuresizeandalign(size:))
- [func heapAccelerationStructureSizeAndAlign(descriptor: MTLAccelerationStructureDescriptor) -> MTLSizeAndAlign](/documentation/metal/mtldevice/heapaccelerationstructuresizeandalign(descriptor:))
- [MTLSizeAndAlign](/documentation/metal/mtlsizeandalign)

###### Accessing the size and alignment

- [var size: Int](/documentation/metal/mtlsizeandalign/size)
- [var align: Int](/documentation/metal/mtlsizeandalign/align)

###### Creating instances

- [init()](/documentation/metal/mtlsizeandalign/init())
- [init(size: Int, align: Int)](/documentation/metal/mtlsizeandalign/init(size:align:))

##### Creating buffers

- [var maxBufferLength: Int](/documentation/metal/mtldevice/maxbufferlength)
- [func makeBuffer(length: Int, options: MTLResourceOptions) -> (any MTLBuffer)?](/documentation/metal/mtldevice/makebuffer(length:options:))
- [func makeBuffer(bytes: UnsafeRawPointer, length: Int, options: MTLResourceOptions) -> (any MTLBuffer)?](/documentation/metal/mtldevice/makebuffer(bytes:length:options:))
- [func makeBuffer(bytesNoCopy: UnsafeMutableRawPointer, length: Int, options: MTLResourceOptions, deallocator: ((UnsafeMutableRawPointer, Int) -> Void)?) -> (any MTLBuffer)?](/documentation/metal/mtldevice/makebuffer(bytesnocopy:length:options:deallocator:))

##### Creating textures

- [func makeTexture(descriptor: MTLTextureDescriptor) -> (any MTLTexture)?](/documentation/metal/mtldevice/maketexture(descriptor:))
- [func makeTexture(descriptor: MTLTextureDescriptor, iosurface: IOSurfaceRef, plane: Int) -> (any MTLTexture)?](/documentation/metal/mtldevice/maketexture(descriptor:iosurface:plane:))
- [func makeSharedTexture(descriptor: MTLTextureDescriptor) -> (any MTLTexture)?](/documentation/metal/mtldevice/makesharedtexture(descriptor:))
- [func makeSharedTexture(handle: MTLSharedTextureHandle) -> (any MTLTexture)?](/documentation/metal/mtldevice/makesharedtexture(handle:))
- [func minimumLinearTextureAlignment(for: MTLPixelFormat) -> Int](/documentation/metal/mtldevice/minimumlineartexturealignment(for:))
- [func minimumTextureBufferAlignment(for: MTLPixelFormat) -> Int](/documentation/metal/mtldevice/minimumtexturebufferalignment(for:))

##### Creating samplers

- [func supportsTextureSampleCount(Int) -> Bool](/documentation/metal/mtldevice/supportstexturesamplecount(_:))
- [func makeSamplerState(descriptor: MTLSamplerDescriptor) -> (any MTLSamplerState)?](/documentation/metal/mtldevice/makesamplerstate(descriptor:))
- [func getDefaultSamplePositions(sampleCount: Int) -> [MTLSamplePosition]](/documentation/metal/mtldevice/getdefaultsamplepositions(samplecount:))

##### Working with sparse textures

- [func sparseTileSize(textureType: MTLTextureType, pixelFormat: MTLPixelFormat, sampleCount: Int, sparsePageSize: MTLSparsePageSize) -> MTLSize](/documentation/metal/mtldevice/sparsetilesize(texturetype:pixelformat:samplecount:sparsepagesize:))
- [func sparseTileSize(with: MTLTextureType, pixelFormat: MTLPixelFormat, sampleCount: Int) -> MTLSize](/documentation/metal/mtldevice/sparsetilesize(with:pixelformat:samplecount:))
- [func sparseTileSizeInBytes(sparsePageSize: MTLSparsePageSize) -> Int](/documentation/metal/mtldevice/sparsetilesizeinbytes(sparsepagesize:))
- [var sparseTileSizeInBytes: Int](/documentation/metal/mtldevice/sparsetilesizeinbytes)
- [func convertSparsePixelRegions(UnsafePointer<MTLRegion>, toTileRegions: UnsafeMutablePointer<MTLRegion>, withTileSize: MTLSize, alignmentMode: MTLSparseTextureRegionAlignmentMode, numRegions: Int)](/documentation/metal/mtldevice/convertsparsepixelregions(_:totileregions:withtilesize:alignmentmode:numregions:))
- [func convertSparseTileRegions(UnsafePointer<MTLRegion>, toPixelRegions: UnsafeMutablePointer<MTLRegion>, withTileSize: MTLSize, numRegions: Int)](/documentation/metal/mtldevice/convertsparsetileregions(_:topixelregions:withtilesize:numregions:))
- [MTLSparsePageSize](/documentation/metal/mtlsparsepagesize)

###### Sparse texture page sizes

- [case size16](/documentation/metal/mtlsparsepagesize/size16)
- [case size64](/documentation/metal/mtlsparsepagesize/size64)
- [case size256](/documentation/metal/mtlsparsepagesize/size256)

###### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlsparsepagesize/init(rawvalue:))
- [MTLSparseTextureRegionAlignmentMode](/documentation/metal/mtlsparsetextureregionalignmentmode)

###### Specifying the alignment mode

- [case outward](/documentation/metal/mtlsparsetextureregionalignmentmode/outward)
- [case inward](/documentation/metal/mtlsparsetextureregionalignmentmode/inward)

###### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlsparsetextureregionalignmentmode/init(rawvalue:))

##### Creating acceleration structures for ray tracing

- [func makeAccelerationStructure(descriptor: MTLAccelerationStructureDescriptor) -> (any MTLAccelerationStructure)?](/documentation/metal/mtldevice/makeaccelerationstructure(descriptor:))
- [func makeAccelerationStructure(size: Int) -> (any MTLAccelerationStructure)?](/documentation/metal/mtldevice/makeaccelerationstructure(size:))
- [func accelerationStructureSizes(descriptor: MTLAccelerationStructureDescriptor) -> MTLAccelerationStructureSizes](/documentation/metal/mtldevice/accelerationstructuresizes(descriptor:))
- [MTLAccelerationStructureSizes](/documentation/metal/mtlaccelerationstructuresizes)

###### Retrieving the sizes

- [var accelerationStructureSize: Int](/documentation/metal/mtlaccelerationstructuresizes/accelerationstructuresize)
- [var buildScratchBufferSize: Int](/documentation/metal/mtlaccelerationstructuresizes/buildscratchbuffersize)
- [var refitScratchBufferSize: Int](/documentation/metal/mtlaccelerationstructuresizes/refitscratchbuffersize)

###### Creating an acceleration size structure

- [init()](/documentation/metal/mtlaccelerationstructuresizes/init())
- [init(accelerationStructureSize: Int, buildScratchBufferSize: Int, refitScratchBufferSize: Int)](/documentation/metal/mtlaccelerationstructuresizes/init(accelerationstructuresize:buildscratchbuffersize:refitscratchbuffersize:))

##### Creating argument buffer encoders

- [var argumentBuffersSupport: MTLArgumentBuffersTier](/documentation/metal/mtldevice/argumentbufferssupport)

###### Argument buffer tiers

- [MTLArgumentBuffersTier](/documentation/metal/mtlargumentbufferstier)

###### Enumeration cases

- [case tier1](/documentation/metal/mtlargumentbufferstier/tier1)
- [case tier2](/documentation/metal/mtlargumentbufferstier/tier2)

###### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlargumentbufferstier/init(rawvalue:))
- [var maxArgumentBufferSamplerCount: Int](/documentation/metal/mtldevice/maxargumentbuffersamplercount)
- [func makeArgumentEncoder(arguments: [MTLArgumentDescriptor]) -> (any MTLArgumentEncoder)?](/documentation/metal/mtldevice/makeargumentencoder(arguments:))
- [func makeArgumentEncoder(bufferBinding: any MTLBufferBinding) -> any MTLArgumentEncoder](/documentation/metal/mtldevice/makeargumentencoder(bufferbinding:))

##### Creating fences and events

- [func makeFence() -> (any MTLFence)?](/documentation/metal/mtldevice/makefence())
- [func makeEvent() -> (any MTLEvent)?](/documentation/metal/mtldevice/makeevent())
- [func makeSharedEvent() -> (any MTLSharedEvent)?](/documentation/metal/mtldevice/makesharedevent())
- [func makeSharedEvent(handle: MTLSharedEventHandle) -> (any MTLSharedEvent)?](/documentation/metal/mtldevice/makesharedevent(handle:))

##### Creating rasterization rate maps

- [func supportsRasterizationRateMap(layerCount: Int) -> Bool](/documentation/metal/mtldevice/supportsrasterizationratemap(layercount:))
- [func makeRasterizationRateMap(descriptor: MTLRasterizationRateMapDescriptor) -> (any MTLRasterizationRateMap)?](/documentation/metal/mtldevice/makerasterizationratemap(descriptor:))
- [Shader library and archive creation](/documentation/metal/shader-library-and-archive-creation)

##### Creating shader libraries

- [func makeDefaultLibrary() -> (any MTLLibrary)?](/documentation/metal/mtldevice/makedefaultlibrary())
- [func makeDefaultLibrary(bundle: Bundle) throws -> any MTLLibrary](/documentation/metal/mtldevice/makedefaultlibrary(bundle:))
- [func makeLibrary(URL: URL) throws -> any MTLLibrary](/documentation/metal/mtldevice/makelibrary(url:))
- [func makeLibrary(source: String, options: MTLCompileOptions?) throws -> any MTLLibrary](/documentation/metal/mtldevice/makelibrary(source:options:))
- [func makeLibrary(source: String, options: MTLCompileOptions?, completionHandler: ((any MTLLibrary)?, (any Error)?) -> Void)](/documentation/metal/mtldevice/makelibrary(source:options:completionhandler:))
- [func makeLibrary(stitchedDescriptor: MTLStitchedLibraryDescriptor) throws -> any MTLLibrary](/documentation/metal/mtldevice/makelibrary(stitcheddescriptor:))
- [func makeLibrary(stitchedDescriptor: MTLStitchedLibraryDescriptor, completionHandler: ((any MTLLibrary)?, (any Error)?) -> Void)](/documentation/metal/mtldevice/makelibrary(stitcheddescriptor:completionhandler:))
- [func makeLibrary(data: DispatchData) throws -> any MTLLibrary](/documentation/metal/mtldevice/makelibrary(data:)-7khmh)
- [func makeLibrary(data: dispatch_data_t) throws -> any MTLLibrary](/documentation/metal/mtldevice/makelibrary(data:))
- [MTLNewLibraryCompletionHandler](/documentation/metal/mtlnewlibrarycompletionhandler)
- [func makeLibrary(filepath: String) throws -> any MTLLibrary](/documentation/metal/mtldevice/makelibrary(filepath:))

##### Creating dynamic shader libraries

- [var supportsDynamicLibraries: Bool](/documentation/metal/mtldevice/supportsdynamiclibraries)
- [var supportsRenderDynamicLibraries: Bool](/documentation/metal/mtldevice/supportsrenderdynamiclibraries)
- [func makeDynamicLibrary(library: any MTLLibrary) throws -> any MTLDynamicLibrary](/documentation/metal/mtldevice/makedynamiclibrary(library:))
- [func makeDynamicLibrary(url: URL) throws -> any MTLDynamicLibrary](/documentation/metal/mtldevice/makedynamiclibrary(url:))
- [MTLDynamicLibraryError.Code](/documentation/metal/mtldynamiclibraryerror-swift.struct/code)

###### Error codes

- [case none](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/none)
- [case invalidFile](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/invalidfile)
- [case compilationFailure](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/compilationfailure)
- [case unresolvedInstallName](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/unresolvedinstallname)
- [case dependencyLoadFailure](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/dependencyloadfailure)
- [case unsupported](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/unsupported)
- [case none](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/none)
- [case invalidFile](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/invalidfile)
- [case compilationFailure](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/compilationfailure)
- [case unresolvedInstallName](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/unresolvedinstallname)
- [case dependencyLoadFailure](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/dependencyloadfailure)
- [case unsupported](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/unsupported)

###### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/init(rawvalue:))
- [let MTLDynamicLibraryDomain: String](/documentation/metal/mtldynamiclibrarydomain)

##### Creating binary shader archives

- [func makeBinaryArchive(descriptor: MTLBinaryArchiveDescriptor) throws -> any MTLBinaryArchive](/documentation/metal/mtldevice/makebinaryarchive(descriptor:))
- [MTLBinaryArchiveDescriptor](/documentation/metal/mtlbinaryarchivedescriptor)

###### Choosing an archive file

- [var url: URL?](/documentation/metal/mtlbinaryarchivedescriptor/url)
- [MTLBinaryArchiveError.Code](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code)

###### Error codes

- [case none](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/none)
- [case invalidFile](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/invalidfile)
- [case compilationFailure](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/compilationfailure)
- [case unexpectedElement](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/unexpectedelement)
- [case internalError](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/internalerror)
- [case none](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/none)
- [case invalidFile](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/invalidfile)
- [case compilationFailure](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/compilationfailure)
- [case unexpectedElement](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/unexpectedelement)
- [case internalError](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/internalerror)

###### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/init(rawvalue:))
- [let MTLBinaryArchiveDomain: String](/documentation/metal/mtlbinaryarchivedomain)

#### Instance Properties

- [var maximumConcurrentCompilationTaskCount: Int](/documentation/metal/mtldevice/maximumconcurrentcompilationtaskcount)
- [var shouldMaximizeConcurrentCompilation: Bool](/documentation/metal/mtldevice/shouldmaximizeconcurrentcompilation)

#### Instance Methods

- [func functionHandle(function: any MTLFunction) -> (any MTLFunctionHandle)?](/documentation/metal/mtldevice/functionhandle(function:)-4bw39)
- [func functionHandle(function: any MTL4BinaryFunction) -> (any MTLFunctionHandle)?](/documentation/metal/mtldevice/functionhandle(function:)-w9ia)
- [func makeArchive(url: URL) throws -> any MTL4Archive](/documentation/metal/mtldevice/makearchive(url:))
- [func makeArgumentTable(descriptor: MTL4ArgumentTableDescriptor) throws -> any MTL4ArgumentTable](/documentation/metal/mtldevice/makeargumenttable(descriptor:))
- [func makeBuffer(length: Int, options: MTLResourceOptions, placementSparsePageSize: MTLSparsePageSize) -> (any MTLBuffer)?](/documentation/metal/mtldevice/makebuffer(length:options:placementsparsepagesize:))
- [func makeCommandAllocator() -> (any MTL4CommandAllocator)?](/documentation/metal/mtldevice/makecommandallocator())
- [func makeCommandAllocator(descriptor: MTL4CommandAllocatorDescriptor) throws -> any MTL4CommandAllocator](/documentation/metal/mtldevice/makecommandallocator(descriptor:))
- [func makeCommandBuffer() -> (any MTL4CommandBuffer)?](/documentation/metal/mtldevice/makecommandbuffer())
- [func makeCommandQueue(descriptor: MTLCommandQueueDescriptor) -> (any MTLCommandQueue)?](/documentation/metal/mtldevice/makecommandqueue(descriptor:))
- [func makeCompiler(descriptor: MTL4CompilerDescriptor) throws -> any MTL4Compiler](/documentation/metal/mtldevice/makecompiler(descriptor:))
- [func makeCounterHeap(descriptor: MTL4CounterHeapDescriptor) throws -> any MTL4CounterHeap](/documentation/metal/mtldevice/makecounterheap(descriptor:))
- [func makeLogState(descriptor: MTLLogStateDescriptor) throws -> any MTLLogState](/documentation/metal/mtldevice/makelogstate(descriptor:))
- [func makeMTL4CommandQueue() -> (any MTL4CommandQueue)?](/documentation/metal/mtldevice/makemtl4commandqueue())
- [func makeMTL4CommandQueue(descriptor: MTL4CommandQueueDescriptor) throws -> any MTL4CommandQueue](/documentation/metal/mtldevice/makemtl4commandqueue(descriptor:))
- [func makePipelineDataSetSerializer(descriptor: MTL4PipelineDataSetSerializerDescriptor) -> any MTL4PipelineDataSetSerializer](/documentation/metal/mtldevice/makepipelinedatasetserializer(descriptor:))
- [func makeTensor(descriptor: MTLTensorDescriptor) throws -> any MTLTensor](/documentation/metal/mtldevice/maketensor(descriptor:))
- [func makeTextureViewPool(descriptor: MTLResourceViewPoolDescriptor) throws -> any MTLTextureViewPool](/documentation/metal/mtldevice/maketextureviewpool(descriptor:))
- [func queryTimestampFrequency() -> UInt64](/documentation/metal/mtldevice/querytimestampfrequency())
- [func size(ofCounterHeapEntry: MTL4CounterHeapType) -> Int](/documentation/metal/mtldevice/size(ofcounterheapentry:))
- [func tensorSizeAndAlign(descriptor: MTLTensorDescriptor) -> MTLSizeAndAlign](/documentation/metal/mtldevice/tensorsizeandalign(descriptor:))
- [Multi-GPU systems](/documentation/metal/multi-gpu-systems)

#### Locating GPUs

- [Finding multiple GPUs on an Intel-based Mac](/documentation/metal/finding-multiple-gpus-on-an-intel-based-mac)
- [Getting the GPU that drives a view’s display](/documentation/metal/getting-the-gpu-that-drives-a-views-display)
- [func MTLCopyAllDevices() -> [any MTLDevice]](/documentation/metal/mtlcopyalldevices())
- [func MTLCopyAllDevicesWithObserver(handler: (any MTLDevice, MTLDeviceNotificationName) -> Void) -> (devices: [any MTLDevice], observer: NSObject)](/documentation/metal/mtlcopyalldeviceswithobserver(handler:))
- [func MTLRemoveDeviceObserver(any NSObjectProtocol)](/documentation/metal/mtlremovedeviceobserver(_:))
- [func CGDirectDisplayCopyCurrentMetalDevice(CGDirectDisplayID) -> (any MTLDevice)?](/documentation/coregraphics/cgdirectdisplaycopycurrentmetaldevice(_:))
- [MTLDeviceNotificationHandler](/documentation/metal/mtldevicenotificationhandler)
- [MTLDeviceNotificationName](/documentation/metal/mtldevicenotificationname)

##### Creating a notification name

- [static let wasAdded: MTLDeviceNotificationName](/documentation/metal/mtldevicenotificationname/wasadded)
- [static let removalRequested: MTLDeviceNotificationName](/documentation/metal/mtldevicenotificationname/removalrequested)
- [static let wasRemoved: MTLDeviceNotificationName](/documentation/metal/mtldevicenotificationname/wasremoved)
- [init(rawValue: String)](/documentation/metal/mtldevicenotificationname/init(rawvalue:))

#### Selecting GPUs

- [Adjusting for GPU memory bandwidth tradeoffs](/documentation/metal/adjusting-for-gpu-memory-bandwidth-tradeoffs)
- [Assessing multi-GPU and multi-display setups on an Intel-based Mac](/documentation/metal/assessing-multi-gpu-and-multi-display-setups-on-an-intel-based-mac)
- [Selecting device objects for graphics rendering](/documentation/metal/selecting-device-objects-for-graphics-rendering)
- [Selecting device objects for compute processing](/documentation/metal/selecting-device-objects-for-compute-processing)

#### Working with external GPUs

- [Handling external GPU additions and removals](/documentation/metal/handling-external-gpu-additions-and-removals)
- [Transferring data between connected GPUs](/documentation/metal/transferring-data-between-connected-gpus)

### Submitting work to a GPU with Metal 4

- [MTL4CommandQueue](/documentation/metal/mtl4commandqueue)

#### Instance Properties

- [var device: any MTLDevice](/documentation/metal/mtl4commandqueue/device)
- [var label: String?](/documentation/metal/mtl4commandqueue/label)

#### Instance Methods

- [func addResidencySet(any MTLResidencySet)](/documentation/metal/mtl4commandqueue/addresidencyset(_:))
- [- addResidencySets:count:](/documentation/metal/mtl4commandqueue/addresidencysets(_:))
- [- commit:count:options:](/documentation/metal/mtl4commandqueue/commit(_:options:))
- [func copyMappings(sourceBuffer: any MTLBuffer, destinationBuffer: any MTLBuffer, operations: [MTL4CopySparseBufferMappingOperation])](/documentation/metal/mtl4commandqueue/copymappings(sourcebuffer:destinationbuffer:operations:))
- [func copyMappings(sourceTexture: any MTLTexture, destinationTexture: any MTLTexture, operations: [MTL4CopySparseTextureMappingOperation])](/documentation/metal/mtl4commandqueue/copymappings(sourcetexture:destinationtexture:operations:))
- [func removeResidencySet(any MTLResidencySet)](/documentation/metal/mtl4commandqueue/removeresidencyset(_:))
- [- removeResidencySets:count:](/documentation/metal/mtl4commandqueue/removeresidencysets(_:))
- [func signalDrawable(any MTLDrawable)](/documentation/metal/mtl4commandqueue/signaldrawable(_:))
- [func signalEvent(any MTLEvent, value: UInt64)](/documentation/metal/mtl4commandqueue/signalevent(_:value:))
- [func updateMappings(buffer: any MTLBuffer, heap: (any MTLHeap)?, operations: [MTL4UpdateSparseBufferMappingOperation])](/documentation/metal/mtl4commandqueue/updatemappings(buffer:heap:operations:))
- [func updateMappings(texture: any MTLTexture, heap: (any MTLHeap)?, operations: [MTL4UpdateSparseTextureMappingOperation])](/documentation/metal/mtl4commandqueue/updatemappings(texture:heap:operations:))
- [func waitForDrawable(any MTLDrawable)](/documentation/metal/mtl4commandqueue/waitfordrawable(_:))
- [func waitForEvent(any MTLEvent, value: UInt64)](/documentation/metal/mtl4commandqueue/waitforevent(_:value:))
- [MTL4CommandQueueDescriptor](/documentation/metal/mtl4commandqueuedescriptor)

#### Instance Properties

- [var feedbackQueue: dispatch_queue_t?](/documentation/metal/mtl4commandqueuedescriptor/feedbackqueue)
- [var label: String?](/documentation/metal/mtl4commandqueuedescriptor/label)
- [MTL4CommandQueueError](/documentation/metal/mtl4commandqueueerror-swift.struct)

#### Type Properties

- [static var accessRevoked: MTL4CommandQueueError.Code](/documentation/metal/mtl4commandqueueerror-swift.struct/accessrevoked)
- [static var deviceRemoved: MTL4CommandQueueError.Code](/documentation/metal/mtl4commandqueueerror-swift.struct/deviceremoved)
- [static var errorDomain: String](/documentation/metal/mtl4commandqueueerror-swift.struct/errordomain)
- [static var `internal`: MTL4CommandQueueError.Code](/documentation/metal/mtl4commandqueueerror-swift.struct/internal)
- [static var none: MTL4CommandQueueError.Code](/documentation/metal/mtl4commandqueueerror-swift.struct/none)
- [static var notPermitted: MTL4CommandQueueError.Code](/documentation/metal/mtl4commandqueueerror-swift.struct/notpermitted)
- [static var outOfMemory: MTL4CommandQueueError.Code](/documentation/metal/mtl4commandqueueerror-swift.struct/outofmemory)
- [static var timeout: MTL4CommandQueueError.Code](/documentation/metal/mtl4commandqueueerror-swift.struct/timeout)
- [MTL4CommandQueueError.Code](/documentation/metal/mtl4commandqueueerror-swift.struct/code)

#### Enumeration Cases

- [case accessRevoked](/documentation/metal/mtl4commandqueueerror-swift.struct/code/accessrevoked)
- [case deviceRemoved](/documentation/metal/mtl4commandqueueerror-swift.struct/code/deviceremoved)
- [case `internal`](/documentation/metal/mtl4commandqueueerror-swift.struct/code/internal)
- [case none](/documentation/metal/mtl4commandqueueerror-swift.struct/code/none)
- [case notPermitted](/documentation/metal/mtl4commandqueueerror-swift.struct/code/notpermitted)
- [case outOfMemory](/documentation/metal/mtl4commandqueueerror-swift.struct/code/outofmemory)
- [case timeout](/documentation/metal/mtl4commandqueueerror-swift.struct/code/timeout)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtl4commandqueueerror-swift.struct/code/init(rawvalue:))
- [let MTL4CommandQueueErrorDomain: String](/documentation/metal/mtl4commandqueueerrordomain)
- [MTL4CommandBuffer](/documentation/metal/mtl4commandbuffer)

#### Instance Properties

- [var device: any MTLDevice](/documentation/metal/mtl4commandbuffer/device)
- [var label: String?](/documentation/metal/mtl4commandbuffer/label)

#### Instance Methods

- [func beginCommandBuffer(allocator: any MTL4CommandAllocator)](/documentation/metal/mtl4commandbuffer/begincommandbuffer(allocator:))
- [func beginCommandBuffer(allocator: any MTL4CommandAllocator, options: MTL4CommandBufferOptions)](/documentation/metal/mtl4commandbuffer/begincommandbuffer(allocator:options:))
- [func endCommandBuffer()](/documentation/metal/mtl4commandbuffer/endcommandbuffer())
- [func makeComputeCommandEncoder() -> (any MTL4ComputeCommandEncoder)?](/documentation/metal/mtl4commandbuffer/makecomputecommandencoder())
- [func makeMachineLearningCommandEncoder() -> (any MTL4MachineLearningCommandEncoder)?](/documentation/metal/mtl4commandbuffer/makemachinelearningcommandencoder())
- [func makeRenderCommandEncoder(descriptor: MTL4RenderPassDescriptor, options: MTL4RenderEncoderOptions) -> (any MTL4RenderCommandEncoder)?](/documentation/metal/mtl4commandbuffer/makerendercommandencoder(descriptor:options:))
- [func popDebugGroup()](/documentation/metal/mtl4commandbuffer/popdebuggroup())
- [func pushDebugGroup(String)](/documentation/metal/mtl4commandbuffer/pushdebuggroup(_:))
- [func resolveCounterHeap(any MTL4CounterHeap, range: Range<Int>, buffer: MTL4BufferRange, fenceToWait: (any MTLFence)?, fenceToUpdate: (any MTLFence)?)](/documentation/metal/mtl4commandbuffer/resolvecounterheap(_:range:buffer:fencetowait:fencetoupdate:))
- [func useResidencySet(any MTLResidencySet)](/documentation/metal/mtl4commandbuffer/useresidencyset(_:))
- [- useResidencySets:count:](/documentation/metal/mtl4commandbuffer/useresidencysets(_:))
- [func writeTimestamp(counterHeap: any MTL4CounterHeap, index: Int)](/documentation/metal/mtl4commandbuffer/writetimestamp(counterheap:index:))
- [MTL4CommandBufferOptions](/documentation/metal/mtl4commandbufferoptions)

#### Instance Properties

- [var logState: (any MTLLogState)?](/documentation/metal/mtl4commandbufferoptions/logstate)
- [MTL4CommandEncoder](/documentation/metal/mtl4commandencoder)

#### Instance Properties

- [var commandBuffer: (any MTL4CommandBuffer)?](/documentation/metal/mtl4commandencoder/commandbuffer)
- [var label: String?](/documentation/metal/mtl4commandencoder/label)

#### Instance Methods

- [func barrier(afterEncoderStages: MTLStages, beforeEncoderStages: MTLStages, visibilityOptions: MTL4VisibilityOptions)](/documentation/metal/mtl4commandencoder/barrier(afterencoderstages:beforeencoderstages:visibilityoptions:))
- [func barrier(afterQueueStages: MTLStages, beforeStages: MTLStages, visibilityOptions: MTL4VisibilityOptions)](/documentation/metal/mtl4commandencoder/barrier(afterqueuestages:beforestages:visibilityoptions:))
- [func barrier(afterStages: MTLStages, beforeQueueStages: MTLStages, visibilityOptions: MTL4VisibilityOptions)](/documentation/metal/mtl4commandencoder/barrier(afterstages:beforequeuestages:visibilityoptions:))
- [func endEncoding()](/documentation/metal/mtl4commandencoder/endencoding())
- [func insertDebugSignpost(String)](/documentation/metal/mtl4commandencoder/insertdebugsignpost(_:))
- [func popDebugGroup()](/documentation/metal/mtl4commandencoder/popdebuggroup())
- [func pushDebugGroup(String)](/documentation/metal/mtl4commandencoder/pushdebuggroup(_:))
- [func updateFence(any MTLFence, afterEncoderStages: MTLStages)](/documentation/metal/mtl4commandencoder/updatefence(_:afterencoderstages:))
- [func waitForFence(any MTLFence, beforeEncoderStages: MTLStages)](/documentation/metal/mtl4commandencoder/waitforfence(_:beforeencoderstages:))
- [MTL4RenderEncoderOptions](/documentation/metal/mtl4renderencoderoptions)

#### Initializers

- [init(rawValue: UInt)](/documentation/metal/mtl4renderencoderoptions/init(rawvalue:))

#### Type Properties

- [static var resuming: MTL4RenderEncoderOptions](/documentation/metal/mtl4renderencoderoptions/resuming)
- [static var suspending: MTL4RenderEncoderOptions](/documentation/metal/mtl4renderencoderoptions/suspending)
- [MTL4ArgumentTable](/documentation/metal/mtl4argumenttable)

#### Instance Properties

- [var device: any MTLDevice](/documentation/metal/mtl4argumenttable/device)
- [var label: String?](/documentation/metal/mtl4argumenttable/label)

#### Instance Methods

- [func setAddress(MTLGPUAddress, attributeStride: Int, index: Int)](/documentation/metal/mtl4argumenttable/setaddress(_:attributestride:index:))
- [func setAddress(MTLGPUAddress, index: Int)](/documentation/metal/mtl4argumenttable/setaddress(_:index:))
- [func setResource(MTLResourceID, bufferIndex: Int)](/documentation/metal/mtl4argumenttable/setresource(_:bufferindex:))
- [func setSamplerState(MTLResourceID, index: Int)](/documentation/metal/mtl4argumenttable/setsamplerstate(_:index:))
- [func setTexture(MTLResourceID, index: Int)](/documentation/metal/mtl4argumenttable/settexture(_:index:))
- [MTL4ArgumentTableDescriptor](/documentation/metal/mtl4argumenttabledescriptor)

#### Instance Properties

- [var initializeBindings: Bool](/documentation/metal/mtl4argumenttabledescriptor/initializebindings)
- [var label: String?](/documentation/metal/mtl4argumenttabledescriptor/label)
- [var maxBufferBindCount: Int](/documentation/metal/mtl4argumenttabledescriptor/maxbufferbindcount)
- [var maxSamplerStateBindCount: Int](/documentation/metal/mtl4argumenttabledescriptor/maxsamplerstatebindcount)
- [var maxTextureBindCount: Int](/documentation/metal/mtl4argumenttabledescriptor/maxtexturebindcount)
- [var supportAttributeStrides: Bool](/documentation/metal/mtl4argumenttabledescriptor/supportattributestrides)
- [MTL4CommandAllocator](/documentation/metal/mtl4commandallocator)

#### Instance Properties

- [var device: any MTLDevice](/documentation/metal/mtl4commandallocator/device)
- [var label: String?](/documentation/metal/mtl4commandallocator/label)

#### Instance Methods

- [func allocatedSize() -> UInt64](/documentation/metal/mtl4commandallocator/allocatedsize())
- [func reset()](/documentation/metal/mtl4commandallocator/reset())
- [MTL4CommandAllocatorDescriptor](/documentation/metal/mtl4commandallocatordescriptor)

#### Instance Properties

- [var label: String?](/documentation/metal/mtl4commandallocatordescriptor/label)
- [MTL4CommitOptions](/documentation/metal/mtl4commitoptions)

#### Instance Methods

- [func addFeedbackHandler(MTL4CommitFeedbackHandler)](/documentation/metal/mtl4commitoptions/addfeedbackhandler(_:))
- [MTL4CommitFeedback](/documentation/metal/mtl4commitfeedback)

#### Instance Properties

- [var error: (any Error)?](/documentation/metal/mtl4commitfeedback/error)
- [var gpuEndTime: CFTimeInterval](/documentation/metal/mtl4commitfeedback/gpuendtime)
- [var gpuStartTime: CFTimeInterval](/documentation/metal/mtl4commitfeedback/gpustarttime)
- [MTL4CommitFeedbackHandler](/documentation/metal/mtl4commitfeedbackhandler)
- [MTL4CounterHeap](/documentation/metal/mtl4counterheap)

#### Instance Properties

- [var count: Int](/documentation/metal/mtl4counterheap/count)
- [var label: String?](/documentation/metal/mtl4counterheap/label)
- [var type: MTL4CounterHeapType](/documentation/metal/mtl4counterheap/type)

#### Instance Methods

- [func invalidateCounterRange(Range<Int>)](/documentation/metal/mtl4counterheap/invalidatecounterrange(_:))
- [func resolveCounterRange(Range<Int>) throws -> Data?](/documentation/metal/mtl4counterheap/resolvecounterrange(_:))
- [MTL4CounterHeapDescriptor](/documentation/metal/mtl4counterheapdescriptor)

#### Instance Properties

- [var count: Int](/documentation/metal/mtl4counterheapdescriptor/count)
- [var type: MTL4CounterHeapType](/documentation/metal/mtl4counterheapdescriptor/type)
- [MTL4CounterHeapType](/documentation/metal/mtl4counterheaptype)

#### Enumeration Cases

- [case invalid](/documentation/metal/mtl4counterheaptype/invalid)
- [case timestamp](/documentation/metal/mtl4counterheaptype/timestamp)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtl4counterheaptype/init(rawvalue:))
- [MTL4TimestampHeapEntry](/documentation/metal/mtl4timestampheapentry)

#### Initializers

- [init()](/documentation/metal/mtl4timestampheapentry/init())
- [init(timestamp: UInt64)](/documentation/metal/mtl4timestampheapentry/init(timestamp:))

#### Instance Properties

- [var timestamp: UInt64](/documentation/metal/mtl4timestampheapentry/timestamp)
- [MTL4TimestampGranularity](/documentation/metal/mtl4timestampgranularity)

#### Enumeration Cases

- [case precise](/documentation/metal/mtl4timestampgranularity/precise)
- [case relaxed](/documentation/metal/mtl4timestampgranularity/relaxed)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtl4timestampgranularity/init(rawvalue:))

### Submitting work to a GPU with Metal

- [Setting up a command structure](/documentation/metal/setting-up-a-command-structure)
- [MTLCommandQueue](/documentation/metal/mtlcommandqueue)

#### Creating command buffers

- [func makeCommandBuffer(descriptor: MTLCommandBufferDescriptor) -> (any MTLCommandBuffer)?](/documentation/metal/mtlcommandqueue/makecommandbuffer(descriptor:))
- [func makeCommandBuffer() -> (any MTLCommandBuffer)?](/documentation/metal/mtlcommandqueue/makecommandbuffer())
- [func makeCommandBufferWithUnretainedReferences() -> (any MTLCommandBuffer)?](/documentation/metal/mtlcommandqueue/makecommandbufferwithunretainedreferences())

#### Attaching residency sets

- [func addResidencySet(any MTLResidencySet)](/documentation/metal/mtlcommandqueue/addresidencyset(_:))
- [- addResidencySets:count:](/documentation/metal/mtlcommandqueue/addresidencysets(_:))

#### Detaching residency sets

- [func removeResidencySet(any MTLResidencySet)](/documentation/metal/mtlcommandqueue/removeresidencyset(_:))
- [func removeResidencySets([any MTLResidencySet])](/documentation/metal/mtlcommandqueue/removeresidencysets(_:))

#### Identifying the command queue

- [var device: any MTLDevice](/documentation/metal/mtlcommandqueue/device)
- [var label: String?](/documentation/metal/mtlcommandqueue/label)

#### Deprecated

- [func insertDebugCaptureBoundary()](/documentation/metal/mtlcommandqueue/insertdebugcaptureboundary())
- [MTLCommandQueueDescriptor](/documentation/metal/mtlcommandqueuedescriptor)

#### Instance Properties

- [var logState: (any MTLLogState)?](/documentation/metal/mtlcommandqueuedescriptor/logstate)
- [var maxCommandBufferCount: Int](/documentation/metal/mtlcommandqueuedescriptor/maxcommandbuffercount)
- [MTLCommandBuffer](/documentation/metal/mtlcommandbuffer)

#### Creating command encoders

- [Command encoder factory methods](/documentation/metal/command-encoder-factory-methods)

##### Creating render encoders

- [func makeRenderCommandEncoder(descriptor: MTLRenderPassDescriptor) -> (any MTLRenderCommandEncoder)?](/documentation/metal/mtlcommandbuffer/makerendercommandencoder(descriptor:))

##### Creating parallel render encoders

- [func makeParallelRenderCommandEncoder(descriptor: MTLRenderPassDescriptor) -> (any MTLParallelRenderCommandEncoder)?](/documentation/metal/mtlcommandbuffer/makeparallelrendercommandencoder(descriptor:))

##### Creating acceleration structure encoders

- [func makeAccelerationStructureCommandEncoder(descriptor: MTLAccelerationStructurePassDescriptor) -> any MTLAccelerationStructureCommandEncoder](/documentation/metal/mtlcommandbuffer/makeaccelerationstructurecommandencoder(descriptor:))
- [func makeAccelerationStructureCommandEncoder() -> (any MTLAccelerationStructureCommandEncoder)?](/documentation/metal/mtlcommandbuffer/makeaccelerationstructurecommandencoder())

##### Creating compute encoders

- [func makeComputeCommandEncoder(descriptor: MTLComputePassDescriptor) -> (any MTLComputeCommandEncoder)?](/documentation/metal/mtlcommandbuffer/makecomputecommandencoder(descriptor:))
- [func makeComputeCommandEncoder() -> (any MTLComputeCommandEncoder)?](/documentation/metal/mtlcommandbuffer/makecomputecommandencoder())
- [func makeComputeCommandEncoder(dispatchType: MTLDispatchType) -> (any MTLComputeCommandEncoder)?](/documentation/metal/mtlcommandbuffer/makecomputecommandencoder(dispatchtype:))
- [MTLDispatchType](/documentation/metal/mtldispatchtype)

###### Execution dispatch types

- [case concurrent](/documentation/metal/mtldispatchtype/concurrent)
- [case serial](/documentation/metal/mtldispatchtype/serial)

###### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtldispatchtype/init(rawvalue:))

##### Creating blit encoders

- [func makeBlitCommandEncoder() -> (any MTLBlitCommandEncoder)?](/documentation/metal/mtlcommandbuffer/makeblitcommandencoder())
- [func makeBlitCommandEncoder(descriptor: MTLBlitPassDescriptor) -> (any MTLBlitCommandEncoder)?](/documentation/metal/mtlcommandbuffer/makeblitcommandencoder(descriptor:))

##### Creating resource state encoders

- [func resourceStateCommandEncoder(with: MTLResourceStatePassDescriptor) -> (any MTLResourceStateCommandEncoder)?](/documentation/metal/mtlcommandbuffer/resourcestatecommandencoder(with:))
- [func makeResourceStateCommandEncoder() -> (any MTLResourceStateCommandEncoder)?](/documentation/metal/mtlcommandbuffer/makeresourcestatecommandencoder())

#### Attaching residency sets

- [func useResidencySet(any MTLResidencySet)](/documentation/metal/mtlcommandbuffer/useresidencyset(_:))
- [func useResidencySets([any MTLResidencySet])](/documentation/metal/mtlcommandbuffer/useresidencysets(_:))

#### Synchronizing passes with events

- [func encodeWaitForEvent(any MTLEvent, value: UInt64)](/documentation/metal/mtlcommandbuffer/encodewaitforevent(_:value:))
- [func encodeSignalEvent(any MTLEvent, value: UInt64)](/documentation/metal/mtlcommandbuffer/encodesignalevent(_:value:))

#### Presenting a drawable

- [func present(any MTLDrawable)](/documentation/metal/mtlcommandbuffer/present(_:))
- [func present(any MTLDrawable, atTime: CFTimeInterval)](/documentation/metal/mtlcommandbuffer/present(_:attime:))
- [func present(any MTLDrawable, afterMinimumDuration: CFTimeInterval)](/documentation/metal/mtlcommandbuffer/present(_:afterminimumduration:))

#### Registering state change handlers

- [func addScheduledHandler(MTLCommandBufferHandler)](/documentation/metal/mtlcommandbuffer/addscheduledhandler(_:))
- [func addCompletedHandler(MTLCommandBufferHandler)](/documentation/metal/mtlcommandbuffer/addcompletedhandler(_:))
- [MTLCommandBufferHandler](/documentation/metal/mtlcommandbufferhandler)

#### Submitting a command buffer

- [func enqueue()](/documentation/metal/mtlcommandbuffer/enqueue())
- [func commit()](/documentation/metal/mtlcommandbuffer/commit())

#### Waiting for state changes

- [func waitUntilScheduled()](/documentation/metal/mtlcommandbuffer/waituntilscheduled())
- [func waitUntilCompleted()](/documentation/metal/mtlcommandbuffer/waituntilcompleted())

#### Troubleshooting a command buffer

- [var status: MTLCommandBufferStatus](/documentation/metal/mtlcommandbuffer/status)
- [MTLCommandBufferStatus](/documentation/metal/mtlcommandbufferstatus)

##### Command buffer states

- [case notEnqueued](/documentation/metal/mtlcommandbufferstatus/notenqueued)
- [case enqueued](/documentation/metal/mtlcommandbufferstatus/enqueued)
- [case committed](/documentation/metal/mtlcommandbufferstatus/committed)
- [case scheduled](/documentation/metal/mtlcommandbufferstatus/scheduled)
- [case completed](/documentation/metal/mtlcommandbufferstatus/completed)
- [case error](/documentation/metal/mtlcommandbufferstatus/error)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlcommandbufferstatus/init(rawvalue:))
- [Command buffer debugging](/documentation/metal/command-buffer-debugging)

##### Identifying the command buffer

- [var label: String?](/documentation/metal/mtlcommandbuffer/label)
- [var commandQueue: any MTLCommandQueue](/documentation/metal/mtlcommandbuffer/commandqueue)
- [var device: any MTLDevice](/documentation/metal/mtlcommandbuffer/device)

##### Grouping commands within a GPU frame capture

- [func pushDebugGroup(String)](/documentation/metal/mtlcommandbuffer/pushdebuggroup(_:))
- [func popDebugGroup()](/documentation/metal/mtlcommandbuffer/popdebuggroup())

##### Getting error details

- [var error: (any Error)?](/documentation/metal/mtlcommandbuffer/error)
- [var errorOptions: MTLCommandBufferErrorOption](/documentation/metal/mtlcommandbuffer/erroroptions)
- [MTLCommandBufferEncoderInfo](/documentation/metal/mtlcommandbufferencoderinfo)

###### Inspecting execution information

- [var label: String](/documentation/metal/mtlcommandbufferencoderinfo/label)
- [var debugSignposts: [String]](/documentation/metal/mtlcommandbufferencoderinfo/debugsignposts)
- [var errorState: MTLCommandEncoderErrorState](/documentation/metal/mtlcommandbufferencoderinfo/errorstate)
- [MTLCommandEncoderErrorState](/documentation/metal/mtlcommandencodererrorstate)

###### Getting the error state

- [case completed](/documentation/metal/mtlcommandencodererrorstate/completed)
- [case pending](/documentation/metal/mtlcommandencodererrorstate/pending)
- [case affected](/documentation/metal/mtlcommandencodererrorstate/affected)
- [case faulted](/documentation/metal/mtlcommandencodererrorstate/faulted)
- [case unknown](/documentation/metal/mtlcommandencodererrorstate/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlcommandencodererrorstate/init(rawvalue:))
- [let MTLCommandBufferEncoderInfoErrorKey: String](/documentation/metal/mtlcommandbufferencoderinfoerrorkey)

##### Reading the runtime message logs

- [var logs: MTLLogContainer](/documentation/metal/mtlcommandbuffer/logs-518l2)

##### Checking scheduling times on the CPU

- [var kernelStartTime: CFTimeInterval](/documentation/metal/mtlcommandbuffer/kernelstarttime)
- [var kernelEndTime: CFTimeInterval](/documentation/metal/mtlcommandbuffer/kernelendtime)

##### Checking execution times on the GPU

- [var gpuStartTime: CFTimeInterval](/documentation/metal/mtlcommandbuffer/gpustarttime)
- [var gpuEndTime: CFTimeInterval](/documentation/metal/mtlcommandbuffer/gpuendtime)

##### Determining whether to maintain strong references

- [var retainedReferences: Bool](/documentation/metal/mtlcommandbuffer/retainedreferences)

#### Instance Methods

- [func completed() async](/documentation/metal/mtlcommandbuffer/completed())
- [func scheduled() async](/documentation/metal/mtlcommandbuffer/scheduled())
- [MTLCommandBufferDescriptor](/documentation/metal/mtlcommandbufferdescriptor)

#### Configuring the command buffer

- [var logState: (any MTLLogState)?](/documentation/metal/mtlcommandbufferdescriptor/logstate)
- [var retainedReferences: Bool](/documentation/metal/mtlcommandbufferdescriptor/retainedreferences)
- [var errorOptions: MTLCommandBufferErrorOption](/documentation/metal/mtlcommandbufferdescriptor/erroroptions)
- [MTLCommandBufferErrorOption](/documentation/metal/mtlcommandbuffererroroption)

##### Buffer error options

- [static var encoderExecutionStatus: MTLCommandBufferErrorOption](/documentation/metal/mtlcommandbuffererroroption/encoderexecutionstatus)

##### Protocol support

- [init(rawValue: UInt)](/documentation/metal/mtlcommandbuffererroroption/init(rawvalue:))
- [MTLCommandBufferError](/documentation/metal/mtlcommandbuffererror-swift.struct)

#### Errors codes

- [static var none: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/none)
- [static var timeout: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/timeout)
- [static var pageFault: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/pagefault)
- [static var notPermitted: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/notpermitted)
- [static var outOfMemory: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/outofmemory)
- [static var invalidResource: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/invalidresource)
- [static var memoryless: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/memoryless)
- [static var deviceRemoved: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/deviceremoved)
- [static var stackOverflow: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/stackoverflow)
- [static var accessRevoked: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/accessrevoked)
- [static var `internal`: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/internal)
- [MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/code)

##### Error codes

- [case none](/documentation/metal/mtlcommandbuffererror-swift.struct/code/none)
- [case timeout](/documentation/metal/mtlcommandbuffererror-swift.struct/code/timeout)
- [case pageFault](/documentation/metal/mtlcommandbuffererror-swift.struct/code/pagefault)
- [case notPermitted](/documentation/metal/mtlcommandbuffererror-swift.struct/code/notpermitted)
- [case outOfMemory](/documentation/metal/mtlcommandbuffererror-swift.struct/code/outofmemory)
- [case invalidResource](/documentation/metal/mtlcommandbuffererror-swift.struct/code/invalidresource)
- [case memoryless](/documentation/metal/mtlcommandbuffererror-swift.struct/code/memoryless)
- [case deviceRemoved](/documentation/metal/mtlcommandbuffererror-swift.struct/code/deviceremoved)
- [case stackOverflow](/documentation/metal/mtlcommandbuffererror-swift.struct/code/stackoverflow)
- [static var accessRevoked: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/code/accessrevoked)
- [case `internal`](/documentation/metal/mtlcommandbuffererror-swift.struct/code/internal)

##### Deprecated

- [case blacklisted](/documentation/metal/mtlcommandbuffererror-swift.struct/code/blacklisted)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlcommandbuffererror-swift.struct/code/init(rawvalue:))

#### Error domain

- [static var errorDomain: String](/documentation/metal/mtlcommandbuffererror-swift.struct/errordomain)
- [let MTLCommandBufferErrorDomain: String](/documentation/metal/mtlcommandbuffererrordomain)

#### Deprecated

- [static var blacklisted: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/blacklisted)
- [MTLCommandEncoder](/documentation/metal/mtlcommandencoder)

#### Ending command encoding

- [func endEncoding()](/documentation/metal/mtlcommandencoder/endencoding())

#### Annotating the command buffer with debug information

- [func insertDebugSignpost(String)](/documentation/metal/mtlcommandencoder/insertdebugsignpost(_:))
- [func pushDebugGroup(String)](/documentation/metal/mtlcommandencoder/pushdebuggroup(_:))
- [func popDebugGroup()](/documentation/metal/mtlcommandencoder/popdebuggroup())

#### Identifying the command encoder

- [var device: any MTLDevice](/documentation/metal/mtlcommandencoder/device)
- [var label: String?](/documentation/metal/mtlcommandencoder/label)

#### Instance Methods

- [func barrier(afterQueueStages: MTLStages, beforeStages: MTLStages)](/documentation/metal/mtlcommandencoder/barrier(afterqueuestages:beforestages:))

### Suspending work on a GPU

- [Preparing your Metal app to run in the background](/documentation/metal/preparing-your-metal-app-to-run-in-the-background)

## Command encoders

- [Render passes](/documentation/metal/render-passes)

### Encoding a render pass

- [MTL4RenderCommandEncoder](/documentation/metal/mtl4rendercommandencoder)

#### Configuring pipeline state

- [func setRenderPipelineState(any MTLRenderPipelineState)](/documentation/metal/mtl4rendercommandencoder/setrenderpipelinestate(_:))

#### Configuring the actions for attachments

- [func setColorStoreAction(MTLStoreAction, index: Int)](/documentation/metal/mtl4rendercommandencoder/setcolorstoreaction(_:index:))
- [func setDepthStoreAction(MTLStoreAction)](/documentation/metal/mtl4rendercommandencoder/setdepthstoreaction(_:))
- [func setStencilStoreAction(MTLStoreAction)](/documentation/metal/mtl4rendercommandencoder/setstencilstoreaction(_:))

#### Configuring blend behavior

- [func setBlendColor(red: Float, green: Float, blue: Float, alpha: Float)](/documentation/metal/mtl4rendercommandencoder/setblendcolor(red:green:blue:alpha:))
- [func setColorAttachmentMap(MTLLogicalToPhysicalColorAttachmentMap?)](/documentation/metal/mtl4rendercommandencoder/setcolorattachmentmap(_:))

#### Configuring rendering behavior

- [func setTriangleFillMode(MTLTriangleFillMode)](/documentation/metal/mtl4rendercommandencoder/settrianglefillmode(_:))
- [func setFrontFacing(MTLWinding)](/documentation/metal/mtl4rendercommandencoder/setfrontfacing(_:))
- [func setCullMode(MTLCullMode)](/documentation/metal/mtl4rendercommandencoder/setcullmode(_:))

#### Configuring depth and stencil behavior

- [func setDepthStencilState((any MTLDepthStencilState)?)](/documentation/metal/mtl4rendercommandencoder/setdepthstencilstate(_:))
- [func setDepthBias(Float, slopeScale: Float, clamp: Float)](/documentation/metal/mtl4rendercommandencoder/setdepthbias(_:slopescale:clamp:))
- [func setDepthClipMode(MTLDepthClipMode)](/documentation/metal/mtl4rendercommandencoder/setdepthclipmode(_:))
- [func setDepthTestBounds(ClosedRange<Float>)](/documentation/metal/mtl4rendercommandencoder/setdepthtestbounds(_:))
- [func setStencilReferenceValue(UInt32)](/documentation/metal/mtl4rendercommandencoder/setstencilreferencevalue(_:))
- [func setStencilReferenceValue(front: UInt32, back: UInt32)](/documentation/metal/mtl4rendercommandencoder/setstencilreferencevalue(front:back:))

#### Configuring viewport and scissor behavior

- [func setViewport(MTLViewport)](/documentation/metal/mtl4rendercommandencoder/setviewport(_:))
- [- setViewports:count:](/documentation/metal/mtl4rendercommandencoder/setviewports(_:))
- [func setScissorRect(MTLScissorRect)](/documentation/metal/mtl4rendercommandencoder/setscissorrect(_:))
- [- setScissorRects:count:](/documentation/metal/mtl4rendercommandencoder/setscissorrects(_:))

#### Configuring visibility testing

- [func setVisibilityResultMode(MTLVisibilityResultMode, offset: Int)](/documentation/metal/mtl4rendercommandencoder/setvisibilityresultmode(_:offset:))

#### Configuring vertex amplification

- [func setVertexAmplificationCount(Int)](/documentation/metal/mtl4rendercommandencoder/setvertexamplificationcount(_:)-85tu1)
- [func setVertexAmplificationCount([MTLVertexAmplificationViewMapping])](/documentation/metal/mtl4rendercommandencoder/setvertexamplificationcount(_:)-911ja)

#### Configuring persistent threadgroup memory

- [func setObjectThreadgroupMemoryLength(Int, index: Int)](/documentation/metal/mtl4rendercommandencoder/setobjectthreadgroupmemorylength(_:index:))
- [func setThreadgroupMemoryLength(Int, offset: Int, index: Int)](/documentation/metal/mtl4rendercommandencoder/setthreadgroupmemorylength(_:offset:index:))

#### Binding argument tables

- [func setArgumentTable(any MTL4ArgumentTable, stages: MTLRenderStages)](/documentation/metal/mtl4rendercommandencoder/setargumenttable(_:stages:))

#### Drawing with vertices

- [func drawPrimitives(primitiveType: MTLPrimitiveType, vertexStart: Int, vertexCount: Int)](/documentation/metal/mtl4rendercommandencoder/drawprimitives(primitivetype:vertexstart:vertexcount:))
- [func drawPrimitives(primitiveType: MTLPrimitiveType, vertexStart: Int, vertexCount: Int, instanceCount: Int)](/documentation/metal/mtl4rendercommandencoder/drawprimitives(primitivetype:vertexstart:vertexcount:instancecount:))
- [func drawPrimitives(primitiveType: MTLPrimitiveType, vertexStart: Int, vertexCount: Int, instanceCount: Int, baseInstance: Int)](/documentation/metal/mtl4rendercommandencoder/drawprimitives(primitivetype:vertexstart:vertexcount:instancecount:baseinstance:))
- [func drawPrimitives(primitiveType: MTLPrimitiveType, indirectBuffer: MTLGPUAddress)](/documentation/metal/mtl4rendercommandencoder/drawprimitives(primitivetype:indirectbuffer:))

#### Drawing with indexed vertices

- [func drawIndexedPrimitives(primitiveType: MTLPrimitiveType, indexCount: Int, indexType: MTLIndexType, indexBuffer: MTLGPUAddress, indexBufferLength: Int)](/documentation/metal/mtl4rendercommandencoder/drawindexedprimitives(primitivetype:indexcount:indextype:indexbuffer:indexbufferlength:))
- [func drawIndexedPrimitives(primitiveType: MTLPrimitiveType, indexCount: Int, indexType: MTLIndexType, indexBuffer: MTLGPUAddress, indexBufferLength: Int, instanceCount: Int)](/documentation/metal/mtl4rendercommandencoder/drawindexedprimitives(primitivetype:indexcount:indextype:indexbuffer:indexbufferlength:instancecount:))
- [func drawIndexedPrimitives(primitiveType: MTLPrimitiveType, indexCount: Int, indexType: MTLIndexType, indexBuffer: MTLGPUAddress, indexBufferLength: Int, instanceCount: Int, baseVertex: Int, baseInstance: Int)](/documentation/metal/mtl4rendercommandencoder/drawindexedprimitives(primitivetype:indexcount:indextype:indexbuffer:indexbufferlength:instancecount:basevertex:baseinstance:))
- [func drawIndexedPrimitives(primitiveType: MTLPrimitiveType, indexType: MTLIndexType, indexBuffer: MTLGPUAddress, indexBufferLength: Int, indirectBuffer: MTLGPUAddress)](/documentation/metal/mtl4rendercommandencoder/drawindexedprimitives(primitivetype:indextype:indexbuffer:indexbufferlength:indirectbuffer:))

#### Drawing with meshes

- [func drawMeshThreads(threadsPerGrid: MTLSize, threadsPerObjectThreadgroup: MTLSize, threadsPerMeshThreadgroup: MTLSize)](/documentation/metal/mtl4rendercommandencoder/drawmeshthreads(threadspergrid:threadsperobjectthreadgroup:threadspermeshthreadgroup:))
- [func drawMeshThreadgroups(threadgroupsPerGrid: MTLSize, threadsPerObjectThreadgroup: MTLSize, threadsPerMeshThreadgroup: MTLSize)](/documentation/metal/mtl4rendercommandencoder/drawmeshthreadgroups(threadgroupspergrid:threadsperobjectthreadgroup:threadspermeshthreadgroup:))
- [func drawMeshThreadgroups(indirectBuffer: MTLGPUAddress, threadsPerObjectThreadgroup: MTLSize, threadsPerMeshThreadgroup: MTLSize)](/documentation/metal/mtl4rendercommandencoder/drawmeshthreadgroups(indirectbuffer:threadsperobjectthreadgroup:threadspermeshthreadgroup:))

#### Drawing with tile shaders

- [func dispatchThreadsPerTile(MTLSize)](/documentation/metal/mtl4rendercommandencoder/dispatchthreadspertile(_:))
- [var tileWidth: Int](/documentation/metal/mtl4rendercommandencoder/tilewidth)
- [var tileHeight: Int](/documentation/metal/mtl4rendercommandencoder/tileheight)

#### Running commands from indirect command buffers

- [func executeCommands(buffer: any MTLIndirectCommandBuffer, range: Range<Int>)](/documentation/metal/mtl4rendercommandencoder/executecommands(buffer:range:))
- [func executeCommands(buffer: any MTLIndirectCommandBuffer, indirectBuffer: MTLGPUAddress)](/documentation/metal/mtl4rendercommandencoder/executecommands(buffer:indirectbuffer:))

#### Sampling counters

- [func writeTimestamp(granularity: MTL4TimestampGranularity, after: MTLRenderStages, counterHeap: any MTL4CounterHeap, index: Int)](/documentation/metal/mtl4rendercommandencoder/writetimestamp(granularity:after:counterheap:index:))
- [MTLRenderCommandEncoder](/documentation/metal/mtlrendercommandencoder)

#### Configuration commands

- [Render pass configuration](/documentation/metal/render-pass-configuration)

##### Configuring pipeline state

- [func setRenderPipelineState(any MTLRenderPipelineState)](/documentation/metal/mtlrendercommandencoder/setrenderpipelinestate(_:))

##### Configuring the actions for attachments

- [func setColorStoreAction(MTLStoreAction, index: Int)](/documentation/metal/mtlrendercommandencoder/setcolorstoreaction(_:index:))
- [func setColorStoreActionOptions(MTLStoreActionOptions, index: Int)](/documentation/metal/mtlrendercommandencoder/setcolorstoreactionoptions(_:index:))
- [func setDepthStoreAction(MTLStoreAction)](/documentation/metal/mtlrendercommandencoder/setdepthstoreaction(_:))
- [func setDepthStoreActionOptions(MTLStoreActionOptions)](/documentation/metal/mtlrendercommandencoder/setdepthstoreactionoptions(_:))
- [func setStencilStoreAction(MTLStoreAction)](/documentation/metal/mtlrendercommandencoder/setstencilstoreaction(_:))
- [func setStencilStoreActionOptions(MTLStoreActionOptions)](/documentation/metal/mtlrendercommandencoder/setstencilstoreactionoptions(_:))

##### Configuring blend behavior

- [func setBlendColor(red: Float, green: Float, blue: Float, alpha: Float)](/documentation/metal/mtlrendercommandencoder/setblendcolor(red:green:blue:alpha:))
- [func setColorAttachmentMap(MTLLogicalToPhysicalColorAttachmentMap?)](/documentation/metal/mtlrendercommandencoder/setcolorattachmentmap(_:))

##### Configuring rendering behavior

- [func setTriangleFillMode(MTLTriangleFillMode)](/documentation/metal/mtlrendercommandencoder/settrianglefillmode(_:))
- [func setFrontFacing(MTLWinding)](/documentation/metal/mtlrendercommandencoder/setfrontfacing(_:))
- [func setCullMode(MTLCullMode)](/documentation/metal/mtlrendercommandencoder/setcullmode(_:))

##### Configuring depth and stencil behavior

- [func setDepthStencilState((any MTLDepthStencilState)?)](/documentation/metal/mtlrendercommandencoder/setdepthstencilstate(_:))
- [func setDepthBias(Float, slopeScale: Float, clamp: Float)](/documentation/metal/mtlrendercommandencoder/setdepthbias(_:slopescale:clamp:))
- [func setDepthClipMode(MTLDepthClipMode)](/documentation/metal/mtlrendercommandencoder/setdepthclipmode(_:))
- [func setDepthTestBounds(ClosedRange<Float>)](/documentation/metal/mtlrendercommandencoder/setdepthtestbounds(_:))
- [func setStencilReferenceValue(UInt32)](/documentation/metal/mtlrendercommandencoder/setstencilreferencevalue(_:))
- [func setStencilReferenceValues(front: UInt32, back: UInt32)](/documentation/metal/mtlrendercommandencoder/setstencilreferencevalues(front:back:))

##### Configuring viewport and scissor behavior

- [func setViewport(MTLViewport)](/documentation/metal/mtlrendercommandencoder/setviewport(_:))
- [- setViewports:count:](/documentation/metal/mtlrendercommandencoder/setviewports(_:))
- [func setScissorRect(MTLScissorRect)](/documentation/metal/mtlrendercommandencoder/setscissorrect(_:))
- [- setScissorRects:count:](/documentation/metal/mtlrendercommandencoder/setscissorrects(_:))

##### Configuring visibility testing

- [func setVisibilityResultMode(MTLVisibilityResultMode, offset: Int)](/documentation/metal/mtlrendercommandencoder/setvisibilityresultmode(_:offset:))

##### Configuring vertex amplification

- [func setVertexAmplificationCount(Int, viewMappings: UnsafePointer<MTLVertexAmplificationViewMapping>?)](/documentation/metal/mtlrendercommandencoder/setvertexamplificationcount(_:viewmappings:))

##### Configuring tessellation factors

- [func setTessellationFactorScale(Float)](/documentation/metal/mtlrendercommandencoder/settessellationfactorscale(_:))
- [func setTessellationFactorBuffer((any MTLBuffer)?, offset: Int, instanceStride: Int)](/documentation/metal/mtlrendercommandencoder/settessellationfactorbuffer(_:offset:instancestride:))

##### Configuring persistent threadgroup memory

- [func setObjectThreadgroupMemoryLength(Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setobjectthreadgroupmemorylength(_:index:))
- [func setThreadgroupMemoryLength(Int, offset: Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setthreadgroupmemorylength(_:offset:index:))

#### Resource preparation commands

- [Mesh and object shader resource preparation commands](/documentation/metal/mesh-and-object-shader-resource-preparation-commands)

##### Assigning buffers for object shaders

- [func setObjectBuffer((any MTLBuffer)?, offset: Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setobjectbuffer(_:offset:index:))
- [- setObjectBuffers:offsets:withRange:](/documentation/metal/mtlrendercommandencoder/setobjectbuffers(_:offsets:range:))
- [func setObjectBytes(UnsafeRawPointer, length: Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setobjectbytes(_:length:index:))
- [func setObjectBufferOffset(Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setobjectbufferoffset(_:index:))

##### Assigning textures for object shaders

- [func setObjectTexture((any MTLTexture)?, index: Int)](/documentation/metal/mtlrendercommandencoder/setobjecttexture(_:index:))
- [- setObjectTextures:withRange:](/documentation/metal/mtlrendercommandencoder/setobjecttextures(_:range:))

##### Assigning sampler states for object shaders

- [func setObjectSamplerState((any MTLSamplerState)?, index: Int)](/documentation/metal/mtlrendercommandencoder/setobjectsamplerstate(_:index:))
- [func setObjectSamplerState((any MTLSamplerState)?, lodMinClamp: Float, lodMaxClamp: Float, index: Int)](/documentation/metal/mtlrendercommandencoder/setobjectsamplerstate(_:lodminclamp:lodmaxclamp:index:))
- [- setObjectSamplerStates:withRange:](/documentation/metal/mtlrendercommandencoder/setobjectsamplerstates(_:range:))
- [- setObjectSamplerStates:lodMinClamps:lodMaxClamps:withRange:](/documentation/metal/mtlrendercommandencoder/setobjectsamplerstates(_:lodminclamps:lodmaxclamps:range:))

##### Assigning buffers for mesh shaders

- [func setMeshBuffer((any MTLBuffer)?, offset: Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setmeshbuffer(_:offset:index:))
- [- setMeshBuffers:offsets:withRange:](/documentation/metal/mtlrendercommandencoder/setmeshbuffers(_:offsets:range:))
- [func setMeshBytes(UnsafeRawPointer, length: Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setmeshbytes(_:length:index:))
- [func setMeshBufferOffset(Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setmeshbufferoffset(_:index:))

##### Assigning textures for mesh shaders

- [func setMeshTexture((any MTLTexture)?, index: Int)](/documentation/metal/mtlrendercommandencoder/setmeshtexture(_:index:))
- [- setMeshTextures:withRange:](/documentation/metal/mtlrendercommandencoder/setmeshtextures(_:range:))

##### Assigning sampler states for mesh shaders

- [func setMeshSamplerState((any MTLSamplerState)?, index: Int)](/documentation/metal/mtlrendercommandencoder/setmeshsamplerstate(_:index:))
- [func setMeshSamplerState((any MTLSamplerState)?, lodMinClamp: Float, lodMaxClamp: Float, index: Int)](/documentation/metal/mtlrendercommandencoder/setmeshsamplerstate(_:lodminclamp:lodmaxclamp:index:))
- [- setMeshSamplerStates:withRange:](/documentation/metal/mtlrendercommandencoder/setmeshsamplerstates(_:range:))
- [- setMeshSamplerStates:lodMinClamps:lodMaxClamps:withRange:](/documentation/metal/mtlrendercommandencoder/setmeshsamplerstates(_:lodminclamps:lodmaxclamps:range:))
- [Vertex shader resource preparation commands](/documentation/metal/vertex-shader-resource-preparation-commands)

##### Assigning buffers

- [func setVertexBuffer((any MTLBuffer)?, offset: Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setvertexbuffer(_:offset:index:))
- [func setVertexBuffer((any MTLBuffer)?, offset: Int, attributeStride: Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setvertexbuffer(_:offset:attributestride:index:))
- [- setVertexBuffers:offsets:withRange:](/documentation/metal/mtlrendercommandencoder/setvertexbuffers(_:offsets:range:))
- [- setVertexBuffers:offsets:attributeStrides:withRange:](/documentation/metal/mtlrendercommandencoder/setvertexbuffers(_:offsets:attributestrides:range:))
- [func setVertexBytes(UnsafeRawPointer, length: Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setvertexbytes(_:length:index:))
- [func setVertexBytes(UnsafeRawPointer, length: Int, attributeStride: Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setvertexbytes(_:length:attributestride:index:))
- [func setVertexBufferOffset(Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setvertexbufferoffset(_:index:))
- [func setVertexBufferOffset(offset: Int, attributeStride: Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setvertexbufferoffset(offset:attributestride:index:))

##### Assigning textures

- [func setVertexTexture((any MTLTexture)?, index: Int)](/documentation/metal/mtlrendercommandencoder/setvertextexture(_:index:))
- [- setVertexTextures:withRange:](/documentation/metal/mtlrendercommandencoder/setvertextextures(_:range:))

##### Assigning sampler states

- [func setVertexSamplerState((any MTLSamplerState)?, index: Int)](/documentation/metal/mtlrendercommandencoder/setvertexsamplerstate(_:index:))
- [func setVertexSamplerState((any MTLSamplerState)?, lodMinClamp: Float, lodMaxClamp: Float, index: Int)](/documentation/metal/mtlrendercommandencoder/setvertexsamplerstate(_:lodminclamp:lodmaxclamp:index:))
- [- setVertexSamplerStates:withRange:](/documentation/metal/mtlrendercommandencoder/setvertexsamplerstates(_:range:))
- [- setVertexSamplerStates:lodMinClamps:lodMaxClamps:withRange:](/documentation/metal/mtlrendercommandencoder/setvertexsamplerstates(_:lodminclamps:lodmaxclamps:range:))

##### Assigning acceleration structures

- [func setVertexAccelerationStructure((any MTLAccelerationStructure)?, bufferIndex: Int)](/documentation/metal/mtlrendercommandencoder/setvertexaccelerationstructure(_:bufferindex:))

##### Assigning visible function tables

- [func setVertexVisibleFunctionTable((any MTLVisibleFunctionTable)?, bufferIndex: Int)](/documentation/metal/mtlrendercommandencoder/setvertexvisiblefunctiontable(_:bufferindex:))
- [- setVertexVisibleFunctionTables:withBufferRange:](/documentation/metal/mtlrendercommandencoder/setvertexvisiblefunctiontables(_:bufferrange:))

##### Assigning intersection function tables

- [func setVertexIntersectionFunctionTable((any MTLIntersectionFunctionTable)?, bufferIndex: Int)](/documentation/metal/mtlrendercommandencoder/setvertexintersectionfunctiontable(_:bufferindex:))
- [- setVertexIntersectionFunctionTables:withBufferRange:](/documentation/metal/mtlrendercommandencoder/setvertexintersectionfunctiontables(_:bufferrange:))
- [Fragment shader resource preparation commands](/documentation/metal/fragment-shader-resource-preparation-commands)

##### Assigning buffers

- [func setFragmentBuffer((any MTLBuffer)?, offset: Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setfragmentbuffer(_:offset:index:))
- [- setFragmentBuffers:offsets:withRange:](/documentation/metal/mtlrendercommandencoder/setfragmentbuffers(_:offsets:range:))
- [func setFragmentBytes(UnsafeRawPointer, length: Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setfragmentbytes(_:length:index:))
- [func setFragmentBufferOffset(Int, index: Int)](/documentation/metal/mtlrendercommandencoder/setfragmentbufferoffset(_:index:))

##### Assigning textures

- [func setFragmentTexture((any MTLTexture)?, index: Int)](/documentation/metal/mtlrendercommandencoder/setfragmenttexture(_:index:))
- [- setFragmentTextures:withRange:](/documentation/metal/mtlrendercommandencoder/setfragmenttextures(_:range:))

##### Assigning sampler states

- [func setFragmentSamplerState((any MTLSamplerState)?, index: Int)](/documentation/metal/mtlrendercommandencoder/setfragmentsamplerstate(_:index:))
- [func setFragmentSamplerState((any MTLSamplerState)?, lodMinClamp: Float, lodMaxClamp: Float, index: Int)](/documentation/metal/mtlrendercommandencoder/setfragmentsamplerstate(_:lodminclamp:lodmaxclamp:index:))
- [- setFragmentSamplerStates:withRange:](/documentation/metal/mtlrendercommandencoder/setfragmentsamplerstates(_:range:))
- [- setFragmentSamplerStates:lodMinClamps:lodMaxClamps:withRange:](/documentation/metal/mtlrendercommandencoder/setfragmentsamplerstates(_:lodminclamps:lodmaxclamps:range:))

##### Assigning acceleration structures

- [func setFragmentAccelerationStructure((any MTLAccelerationStructure)?, bufferIndex: Int)](/documentation/metal/mtlrendercommandencoder/setfragmentaccelerationstructure(_:bufferindex:))

##### Assigning visible function tables

- [func setFragmentVisibleFunctionTable((any MTLVisibleFunctionTable)?, bufferIndex: Int)](/documentation/metal/mtlrendercommandencoder/setfragmentvisiblefunctiontable(_:bufferindex:))
- [- setFragmentVisibleFunctionTables:withBufferRange:](/documentation/metal/mtlrendercommandencoder/setfragmentvisiblefunctiontables(_:bufferrange:))

##### Assigning intersection function tables

- [func setFragmentIntersectionFunctionTable((any MTLIntersectionFunctionTable)?, bufferIndex: Int)](/documentation/metal/mtlrendercommandencoder/setfragmentintersectionfunctiontable(_:bufferindex:))
- [- setFragmentIntersectionFunctionTables:withBufferRange:](/documentation/metal/mtlrendercommandencoder/setfragmentintersectionfunctiontables(_:bufferrange:))
- [Tile shaders resource preparation commands](/documentation/metal/tile-shaders-resource-preparation-commands)

##### Assigning buffers

- [func setTileBuffer((any MTLBuffer)?, offset: Int, index: Int)](/documentation/metal/mtlrendercommandencoder/settilebuffer(_:offset:index:))
- [- setTileBuffers:offsets:withRange:](/documentation/metal/mtlrendercommandencoder/settilebuffers(_:offsets:range:))
- [func setTileBytes(UnsafeRawPointer, length: Int, index: Int)](/documentation/metal/mtlrendercommandencoder/settilebytes(_:length:index:))
- [func setTileBufferOffset(Int, index: Int)](/documentation/metal/mtlrendercommandencoder/settilebufferoffset(_:index:))

##### Assigning textures

- [func setTileTexture((any MTLTexture)?, index: Int)](/documentation/metal/mtlrendercommandencoder/settiletexture(_:index:))
- [- setTileTextures:withRange:](/documentation/metal/mtlrendercommandencoder/settiletextures(_:range:))

##### Assigning sampler states

- [func setTileSamplerState((any MTLSamplerState)?, index: Int)](/documentation/metal/mtlrendercommandencoder/settilesamplerstate(_:index:))
- [func setTileSamplerState((any MTLSamplerState)?, lodMinClamp: Float, lodMaxClamp: Float, index: Int)](/documentation/metal/mtlrendercommandencoder/settilesamplerstate(_:lodminclamp:lodmaxclamp:index:))
- [- setTileSamplerStates:withRange:](/documentation/metal/mtlrendercommandencoder/settilesamplerstates(_:range:))
- [- setTileSamplerStates:lodMinClamps:lodMaxClamps:withRange:](/documentation/metal/mtlrendercommandencoder/settilesamplerstates(_:lodminclamps:lodmaxclamps:range:))

##### Assigning acceleration structures

- [func setTileAccelerationStructure((any MTLAccelerationStructure)?, bufferIndex: Int)](/documentation/metal/mtlrendercommandencoder/settileaccelerationstructure(_:bufferindex:))

##### Assigning visible function tables

- [func setTileVisibleFunctionTable((any MTLVisibleFunctionTable)?, bufferIndex: Int)](/documentation/metal/mtlrendercommandencoder/settilevisiblefunctiontable(_:bufferindex:))
- [- setTileVisibleFunctionTables:withBufferRange:](/documentation/metal/mtlrendercommandencoder/settilevisiblefunctiontables(_:bufferrange:))

##### Assigning intersection function tables

- [func setTileIntersectionFunctionTable((any MTLIntersectionFunctionTable)?, bufferIndex: Int)](/documentation/metal/mtlrendercommandencoder/settileintersectionfunctiontable(_:bufferindex:))
- [func setTileIntersectionFunctionTables([(any MTLIntersectionFunctionTable)?], bufferRange: Range<Int>)](/documentation/metal/mtlrendercommandencoder/settileintersectionfunctiontables(_:bufferrange:))
- [Argument buffer resource preparation commands](/documentation/metal/argument-buffer-resource-preparation-commands)

##### Loading individual resources for argument buffers

- [func useResource(any MTLResource, usage: MTLResourceUsage, stages: MTLRenderStages)](/documentation/metal/mtlrendercommandencoder/useresource(_:usage:stages:))
- [- useResources:count:usage:stages:](/documentation/metal/mtlrendercommandencoder/useresources(_:usage:stages:))

##### Loading heaps and the resources they contain for argument buffers

- [func useHeap(any MTLHeap, stages: MTLRenderStages)](/documentation/metal/mtlrendercommandencoder/useheap(_:stages:))
- [- useHeaps:count:stages:](/documentation/metal/mtlrendercommandencoder/useheaps(_:stages:))

#### Drawing with vertices

- [func drawPrimitives(type: MTLPrimitiveType, vertexStart: Int, vertexCount: Int)](/documentation/metal/mtlrendercommandencoder/drawprimitives(type:vertexstart:vertexcount:))
- [func drawPrimitives(type: MTLPrimitiveType, vertexStart: Int, vertexCount: Int, instanceCount: Int)](/documentation/metal/mtlrendercommandencoder/drawprimitives(type:vertexstart:vertexcount:instancecount:))
- [func drawPrimitives(type: MTLPrimitiveType, vertexStart: Int, vertexCount: Int, instanceCount: Int, baseInstance: Int)](/documentation/metal/mtlrendercommandencoder/drawprimitives(type:vertexstart:vertexcount:instancecount:baseinstance:))
- [func drawPrimitives(type: MTLPrimitiveType, indirectBuffer: any MTLBuffer, indirectBufferOffset: Int)](/documentation/metal/mtlrendercommandencoder/drawprimitives(type:indirectbuffer:indirectbufferoffset:))

#### Drawing with indexed vertices

- [func drawIndexedPrimitives(type: MTLPrimitiveType, indexCount: Int, indexType: MTLIndexType, indexBuffer: any MTLBuffer, indexBufferOffset: Int)](/documentation/metal/mtlrendercommandencoder/drawindexedprimitives(type:indexcount:indextype:indexbuffer:indexbufferoffset:))
- [func drawIndexedPrimitives(type: MTLPrimitiveType, indexCount: Int, indexType: MTLIndexType, indexBuffer: any MTLBuffer, indexBufferOffset: Int, instanceCount: Int)](/documentation/metal/mtlrendercommandencoder/drawindexedprimitives(type:indexcount:indextype:indexbuffer:indexbufferoffset:instancecount:))
- [func drawIndexedPrimitives(type: MTLPrimitiveType, indexCount: Int, indexType: MTLIndexType, indexBuffer: any MTLBuffer, indexBufferOffset: Int, instanceCount: Int, baseVertex: Int, baseInstance: Int)](/documentation/metal/mtlrendercommandencoder/drawindexedprimitives(type:indexcount:indextype:indexbuffer:indexbufferoffset:instancecount:basevertex:baseinstance:))
- [func drawIndexedPrimitives(type: MTLPrimitiveType, indexType: MTLIndexType, indexBuffer: any MTLBuffer, indexBufferOffset: Int, indirectBuffer: any MTLBuffer, indirectBufferOffset: Int)](/documentation/metal/mtlrendercommandencoder/drawindexedprimitives(type:indextype:indexbuffer:indexbufferoffset:indirectbuffer:indirectbufferoffset:))

#### Drawing with meshes

- [func drawMeshThreads(MTLSize, threadsPerObjectThreadgroup: MTLSize, threadsPerMeshThreadgroup: MTLSize)](/documentation/metal/mtlrendercommandencoder/drawmeshthreads(_:threadsperobjectthreadgroup:threadspermeshthreadgroup:))
- [func drawMeshThreadgroups(MTLSize, threadsPerObjectThreadgroup: MTLSize, threadsPerMeshThreadgroup: MTLSize)](/documentation/metal/mtlrendercommandencoder/drawmeshthreadgroups(_:threadsperobjectthreadgroup:threadspermeshthreadgroup:))
- [func drawMeshThreadgroups(indirectBuffer: any MTLBuffer, indirectBufferOffset: Int, threadsPerObjectThreadgroup: MTLSize, threadsPerMeshThreadgroup: MTLSize)](/documentation/metal/mtlrendercommandencoder/drawmeshthreadgroups(indirectbuffer:indirectbufferoffset:threadsperobjectthreadgroup:threadspermeshthreadgroup:))

#### Drawing with tessellation patches

- [func drawPatches(numberOfPatchControlPoints: Int, patchStart: Int, patchCount: Int, patchIndexBuffer: (any MTLBuffer)?, patchIndexBufferOffset: Int, instanceCount: Int, baseInstance: Int)](/documentation/metal/mtlrendercommandencoder/drawpatches(numberofpatchcontrolpoints:patchstart:patchcount:patchindexbuffer:patchindexbufferoffset:instancecount:baseinstance:))
- [func drawPatches(numberOfPatchControlPoints: Int, patchIndexBuffer: (any MTLBuffer)?, patchIndexBufferOffset: Int, indirectBuffer: any MTLBuffer, indirectBufferOffset: Int)](/documentation/metal/mtlrendercommandencoder/drawpatches(numberofpatchcontrolpoints:patchindexbuffer:patchindexbufferoffset:indirectbuffer:indirectbufferoffset:))

#### Drawing with indexed tessellation patches

- [func drawIndexedPatches(numberOfPatchControlPoints: Int, patchStart: Int, patchCount: Int, patchIndexBuffer: (any MTLBuffer)?, patchIndexBufferOffset: Int, controlPointIndexBuffer: any MTLBuffer, controlPointIndexBufferOffset: Int, instanceCount: Int, baseInstance: Int)](/documentation/metal/mtlrendercommandencoder/drawindexedpatches(numberofpatchcontrolpoints:patchstart:patchcount:patchindexbuffer:patchindexbufferoffset:controlpointindexbuffer:controlpointindexbufferoffset:instancecount:baseinstance:))
- [func drawIndexedPatches(numberOfPatchControlPoints: Int, patchIndexBuffer: (any MTLBuffer)?, patchIndexBufferOffset: Int, controlPointIndexBuffer: any MTLBuffer, controlPointIndexBufferOffset: Int, indirectBuffer: any MTLBuffer, indirectBufferOffset: Int)](/documentation/metal/mtlrendercommandencoder/drawindexedpatches(numberofpatchcontrolpoints:patchindexbuffer:patchindexbufferoffset:controlpointindexbuffer:controlpointindexbufferoffset:indirectbuffer:indirectbufferoffset:))

#### Drawing with tile shaders

- [func dispatchThreadsPerTile(MTLSize)](/documentation/metal/mtlrendercommandencoder/dispatchthreadspertile(_:))
- [var tileWidth: Int](/documentation/metal/mtlrendercommandencoder/tilewidth)
- [var tileHeight: Int](/documentation/metal/mtlrendercommandencoder/tileheight)

#### Preventing resource access conflicts

- [func waitForFence(any MTLFence, before: MTLRenderStages)](/documentation/metal/mtlrendercommandencoder/waitforfence(_:before:))
- [func updateFence(any MTLFence, after: MTLRenderStages)](/documentation/metal/mtlrendercommandencoder/updatefence(_:after:))
- [func memoryBarrier(resources: [any MTLResource], after: MTLRenderStages, before: MTLRenderStages)](/documentation/metal/mtlrendercommandencoder/memorybarrier(resources:after:before:))
- [func memoryBarrier(scope: MTLBarrierScope, after: MTLRenderStages, before: MTLRenderStages)](/documentation/metal/mtlrendercommandencoder/memorybarrier(scope:after:before:))

#### Running commands from indirect command buffers

- [- executeCommandsInBuffer:withRange:](/documentation/metal/mtlrendercommandencoder/executecommandsinbuffer(_:range:))
- [- executeCommandsInBuffer:indirectBuffer:indirectBufferOffset:](/documentation/metal/mtlrendercommandencoder/executecommandsinbuffer(_:indirectbuffer:offset:))

#### Sampling counters

- [func sampleCounters(sampleBuffer: any MTLCounterSampleBuffer, sampleIndex: Int, barrier: Bool)](/documentation/metal/mtlrendercommandencoder/samplecounters(samplebuffer:sampleindex:barrier:))

#### Deprecated

- [Deprecated symbols](/documentation/metal/deprecated-symbols)

##### Deprecated methods

- [func useResource(any MTLResource, usage: MTLResourceUsage)](/documentation/metal/mtlrendercommandencoder/useresource(_:usage:))
- [func use(any MTLResource, usage: MTLResourceUsage, stages: MTLRenderStages)](/documentation/metal/mtlrendercommandencoder/use(_:usage:stages:))
- [- useResources:count:usage:](/documentation/metal/mtlrendercommandencoder/useresources(_:usage:))
- [func use(UnsafePointer<any MTLResource>, count: Int, usage: MTLResourceUsage, stages: MTLRenderStages)](/documentation/metal/mtlrendercommandencoder/use(_:count:usage:stages:))
- [func useHeap(any MTLHeap)](/documentation/metal/mtlrendercommandencoder/useheap(_:))
- [func use(any MTLHeap, stages: MTLRenderStages)](/documentation/metal/mtlrendercommandencoder/use(_:stages:))
- [- useHeaps:count:](/documentation/metal/mtlrendercommandencoder/useheaps(_:))
- [func use(UnsafePointer<any MTLHeap>, count: Int, stages: MTLRenderStages)](/documentation/metal/mtlrendercommandencoder/use(_:count:stages:))
- [func textureBarrier()](/documentation/metal/mtlrendercommandencoder/texturebarrier())
- [MTL4RenderEncoderOptions](/documentation/metal/mtl4renderencoderoptions)

#### Initializers

- [init(rawValue: UInt)](/documentation/metal/mtl4renderencoderoptions/init(rawvalue:))

#### Type Properties

- [static var resuming: MTL4RenderEncoderOptions](/documentation/metal/mtl4renderencoderoptions/resuming)
- [static var suspending: MTL4RenderEncoderOptions](/documentation/metal/mtl4renderencoderoptions/suspending)
- [MTLTriangleFillMode](/documentation/metal/mtltrianglefillmode)

#### Fill modes

- [case fill](/documentation/metal/mtltrianglefillmode/fill)
- [case lines](/documentation/metal/mtltrianglefillmode/lines)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtltrianglefillmode/init(rawvalue:))
- [MTLWinding](/documentation/metal/mtlwinding)

#### Winding options

- [case clockwise](/documentation/metal/mtlwinding/clockwise)
- [case counterClockwise](/documentation/metal/mtlwinding/counterclockwise)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlwinding/init(rawvalue:))
- [MTLCullMode](/documentation/metal/mtlcullmode)

#### Cull modes

- [case none](/documentation/metal/mtlcullmode/none)
- [case front](/documentation/metal/mtlcullmode/front)
- [case back](/documentation/metal/mtlcullmode/back)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlcullmode/init(rawvalue:))
- [MTLPrimitiveType](/documentation/metal/mtlprimitivetype)

#### Geometric primitive types

- [case point](/documentation/metal/mtlprimitivetype/point)
- [case line](/documentation/metal/mtlprimitivetype/line)
- [case lineStrip](/documentation/metal/mtlprimitivetype/linestrip)
- [case triangle](/documentation/metal/mtlprimitivetype/triangle)
- [case triangleStrip](/documentation/metal/mtlprimitivetype/trianglestrip)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlprimitivetype/init(rawvalue:))
- [MTLIndexType](/documentation/metal/mtlindextype)

#### Index types

- [case uint16](/documentation/metal/mtlindextype/uint16)
- [case uint32](/documentation/metal/mtlindextype/uint32)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlindextype/init(rawvalue:))
- [MTLDepthClipMode](/documentation/metal/mtldepthclipmode)

#### Clip modes

- [case clip](/documentation/metal/mtldepthclipmode/clip)
- [case clamp](/documentation/metal/mtldepthclipmode/clamp)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtldepthclipmode/init(rawvalue:))
- [MTLVisibilityResultMode](/documentation/metal/mtlvisibilityresultmode)

#### Result modes

- [case disabled](/documentation/metal/mtlvisibilityresultmode/disabled)
- [case boolean](/documentation/metal/mtlvisibilityresultmode/boolean)
- [case counting](/documentation/metal/mtlvisibilityresultmode/counting)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlvisibilityresultmode/init(rawvalue:))
- [MTLVisibilityResultType](/documentation/metal/mtlvisibilityresulttype)

#### Enumeration Cases

- [case accumulate](/documentation/metal/mtlvisibilityresulttype/accumulate)
- [case reset](/documentation/metal/mtlvisibilityresulttype/reset)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlvisibilityresulttype/init(rawvalue:))

### Encoding a render pass in parallel

- [MTLParallelRenderCommandEncoder](/documentation/metal/mtlparallelrendercommandencoder)

#### Creating a render command encoder

- [func makeRenderCommandEncoder() -> (any MTLRenderCommandEncoder)?](/documentation/metal/mtlparallelrendercommandencoder/makerendercommandencoder())

#### Setting render pass state

- [func setColorStoreAction(MTLStoreAction, index: Int)](/documentation/metal/mtlparallelrendercommandencoder/setcolorstoreaction(_:index:))
- [func setColorStoreActionOptions(MTLStoreActionOptions, index: Int)](/documentation/metal/mtlparallelrendercommandencoder/setcolorstoreactionoptions(_:index:))
- [func setDepthStoreAction(MTLStoreAction)](/documentation/metal/mtlparallelrendercommandencoder/setdepthstoreaction(_:))
- [func setDepthStoreActionOptions(MTLStoreActionOptions)](/documentation/metal/mtlparallelrendercommandencoder/setdepthstoreactionoptions(_:))
- [func setStencilStoreAction(MTLStoreAction)](/documentation/metal/mtlparallelrendercommandencoder/setstencilstoreaction(_:))
- [func setStencilStoreActionOptions(MTLStoreActionOptions)](/documentation/metal/mtlparallelrendercommandencoder/setstencilstoreactionoptions(_:))
- [MTLLoadAction](/documentation/metal/mtlloadaction)

#### Load actions

- [case dontCare](/documentation/metal/mtlloadaction/dontcare)
- [case load](/documentation/metal/mtlloadaction/load)
- [case clear](/documentation/metal/mtlloadaction/clear)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlloadaction/init(rawvalue:))
- [MTLStoreAction](/documentation/metal/mtlstoreaction)

#### Store actions

- [case dontCare](/documentation/metal/mtlstoreaction/dontcare)
- [case store](/documentation/metal/mtlstoreaction/store)
- [case multisampleResolve](/documentation/metal/mtlstoreaction/multisampleresolve)
- [case storeAndMultisampleResolve](/documentation/metal/mtlstoreaction/storeandmultisampleresolve)
- [case unknown](/documentation/metal/mtlstoreaction/unknown)
- [case customSampleDepthStore](/documentation/metal/mtlstoreaction/customsampledepthstore)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlstoreaction/init(rawvalue:))
- [MTLStoreActionOptions](/documentation/metal/mtlstoreactionoptions)

#### Using programmable sample positions

- [static var customSamplePositions: MTLStoreActionOptions](/documentation/metal/mtlstoreactionoptions/customsamplepositions)

#### Initializers

- [init(rawValue: UInt)](/documentation/metal/mtlstoreactionoptions/init(rawvalue:))

### Configuring a render command encoder

- [MTL4RenderPassDescriptor](/documentation/metal/mtl4renderpassdescriptor)

#### Instance Properties

- [var colorAttachments: MTLRenderPassColorAttachmentDescriptorArray](/documentation/metal/mtl4renderpassdescriptor/colorattachments)
- [var defaultRasterSampleCount: Int](/documentation/metal/mtl4renderpassdescriptor/defaultrastersamplecount)
- [var depthAttachment: MTLRenderPassDepthAttachmentDescriptor!](/documentation/metal/mtl4renderpassdescriptor/depthattachment)
- [var imageblockSampleLength: Int](/documentation/metal/mtl4renderpassdescriptor/imageblocksamplelength)
- [var rasterizationRateMap: (any MTLRasterizationRateMap)?](/documentation/metal/mtl4renderpassdescriptor/rasterizationratemap)
- [var renderTargetArrayLength: Int](/documentation/metal/mtl4renderpassdescriptor/rendertargetarraylength)
- [var renderTargetHeight: Int](/documentation/metal/mtl4renderpassdescriptor/rendertargetheight)
- [var renderTargetWidth: Int](/documentation/metal/mtl4renderpassdescriptor/rendertargetwidth)
- [var samplePositions: [MTLSamplePosition]](/documentation/metal/mtl4renderpassdescriptor/samplepositions)
- [var stencilAttachment: MTLRenderPassStencilAttachmentDescriptor!](/documentation/metal/mtl4renderpassdescriptor/stencilattachment)
- [var supportColorAttachmentMapping: Bool](/documentation/metal/mtl4renderpassdescriptor/supportcolorattachmentmapping)
- [var threadgroupMemoryLength: Int](/documentation/metal/mtl4renderpassdescriptor/threadgroupmemorylength)
- [var tileHeight: Int](/documentation/metal/mtl4renderpassdescriptor/tileheight)
- [var tileWidth: Int](/documentation/metal/mtl4renderpassdescriptor/tilewidth)
- [var visibilityResultBuffer: (any MTLBuffer)?](/documentation/metal/mtl4renderpassdescriptor/visibilityresultbuffer)
- [var visibilityResultType: MTLVisibilityResultType](/documentation/metal/mtl4renderpassdescriptor/visibilityresulttype)
- [MTLRenderPassDescriptor](/documentation/metal/mtlrenderpassdescriptor)

#### Specifying the attachments for a rendering pass

- [var colorAttachments: MTLRenderPassColorAttachmentDescriptorArray](/documentation/metal/mtlrenderpassdescriptor/colorattachments)
- [var depthAttachment: MTLRenderPassDepthAttachmentDescriptor!](/documentation/metal/mtlrenderpassdescriptor/depthattachment)
- [var stencilAttachment: MTLRenderPassStencilAttachmentDescriptor!](/documentation/metal/mtlrenderpassdescriptor/stencilattachment)

#### Specifying the visibility result buffer

- [var visibilityResultBuffer: (any MTLBuffer)?](/documentation/metal/mtlrenderpassdescriptor/visibilityresultbuffer)

#### Layered rendering

- [var renderTargetArrayLength: Int](/documentation/metal/mtlrenderpassdescriptor/rendertargetarraylength)
- [var renderTargetWidth: Int](/documentation/metal/mtlrenderpassdescriptor/rendertargetwidth)
- [var renderTargetHeight: Int](/documentation/metal/mtlrenderpassdescriptor/rendertargetheight)

#### Using programmable sample positions

- [func MTLSamplePositionMake(Float, Float) -> MTLSamplePosition](/documentation/metal/mtlsamplepositionmake(_:_:))
- [- setSamplePositions:count:](/documentation/metal/mtlrenderpassdescriptor/setsamplepositions(_:))
- [func getSamplePositions() -> [MTLSamplePosition]](/documentation/metal/mtlrenderpassdescriptor/getsamplepositions())

#### Specifying tile shading parameters

- [var imageblockSampleLength: Int](/documentation/metal/mtlrenderpassdescriptor/imageblocksamplelength)
- [var threadgroupMemoryLength: Int](/documentation/metal/mtlrenderpassdescriptor/threadgroupmemorylength)
- [var tileWidth: Int](/documentation/metal/mtlrenderpassdescriptor/tilewidth)
- [var tileHeight: Int](/documentation/metal/mtlrenderpassdescriptor/tileheight)

#### Specifying sample counts

- [var defaultRasterSampleCount: Int](/documentation/metal/mtlrenderpassdescriptor/defaultrastersamplecount)

#### Specifying a rasterization rate map

- [var rasterizationRateMap: (any MTLRasterizationRateMap)?](/documentation/metal/mtlrenderpassdescriptor/rasterizationratemap)

#### Specifying sample buffers for GPU counters

- [var sampleBufferAttachments: MTLRenderPassSampleBufferAttachmentDescriptorArray](/documentation/metal/mtlrenderpassdescriptor/samplebufferattachments)

#### Instance Properties

- [var supportColorAttachmentMapping: Bool](/documentation/metal/mtlrenderpassdescriptor/supportcolorattachmentmapping)
- [var visibilityResultType: MTLVisibilityResultType](/documentation/metal/mtlrenderpassdescriptor/visibilityresulttype)
- [MTLRenderPassAttachmentDescriptor](/documentation/metal/mtlrenderpassattachmentdescriptor)

#### Specifying the texture for the attachment

- [var texture: (any MTLTexture)?](/documentation/metal/mtlrenderpassattachmentdescriptor/texture)
- [var level: Int](/documentation/metal/mtlrenderpassattachmentdescriptor/level)
- [var slice: Int](/documentation/metal/mtlrenderpassattachmentdescriptor/slice)
- [var depthPlane: Int](/documentation/metal/mtlrenderpassattachmentdescriptor/depthplane)

#### Specifying rendering pass actions

- [var loadAction: MTLLoadAction](/documentation/metal/mtlrenderpassattachmentdescriptor/loadaction)
- [var storeAction: MTLStoreAction](/documentation/metal/mtlrenderpassattachmentdescriptor/storeaction)
- [var storeActionOptions: MTLStoreActionOptions](/documentation/metal/mtlrenderpassattachmentdescriptor/storeactionoptions)

#### Specifying the texture to resolve multisample data

- [var resolveTexture: (any MTLTexture)?](/documentation/metal/mtlrenderpassattachmentdescriptor/resolvetexture)
- [var resolveLevel: Int](/documentation/metal/mtlrenderpassattachmentdescriptor/resolvelevel)
- [var resolveSlice: Int](/documentation/metal/mtlrenderpassattachmentdescriptor/resolveslice)
- [var resolveDepthPlane: Int](/documentation/metal/mtlrenderpassattachmentdescriptor/resolvedepthplane)
- [MTLRenderPassColorAttachmentDescriptorArray](/documentation/metal/mtlrenderpasscolorattachmentdescriptorarray)

#### Accessing the description of a color attachment

- [subscript(Int) -> MTLRenderPassColorAttachmentDescriptor!](/documentation/metal/mtlrenderpasscolorattachmentdescriptorarray/subscript(_:))
- [MTLRenderPassColorAttachmentDescriptor](/documentation/metal/mtlrenderpasscolorattachmentdescriptor)

#### Specifying clearing value

- [var clearColor: MTLClearColor](/documentation/metal/mtlrenderpasscolorattachmentdescriptor/clearcolor)
- [func MTLClearColorMake(Double, Double, Double, Double) -> MTLClearColor](/documentation/metal/mtlclearcolormake(_:_:_:_:))
- [MTLClearColor](/documentation/metal/mtlclearcolor)

#### Initializers

- [init()](/documentation/metal/mtlclearcolor/init())
- [init(red: Double, green: Double, blue: Double, alpha: Double)](/documentation/metal/mtlclearcolor/init(red:green:blue:alpha:))

#### Instance Properties

- [var alpha: Double](/documentation/metal/mtlclearcolor/alpha)
- [var blue: Double](/documentation/metal/mtlclearcolor/blue)
- [var green: Double](/documentation/metal/mtlclearcolor/green)
- [var red: Double](/documentation/metal/mtlclearcolor/red)
- [MTLRenderPassDepthAttachmentDescriptor](/documentation/metal/mtlrenderpassdepthattachmentdescriptor)

#### Specifying clearing value

- [var clearDepth: Double](/documentation/metal/mtlrenderpassdepthattachmentdescriptor/cleardepth)

#### MSAA depth resolve

- [var depthResolveFilter: MTLMultisampleDepthResolveFilter](/documentation/metal/mtlrenderpassdepthattachmentdescriptor/depthresolvefilter)
- [MTLMultisampleDepthResolveFilter](/documentation/metal/mtlmultisampledepthresolvefilter)

#### Depth resolve filters

- [case sample0](/documentation/metal/mtlmultisampledepthresolvefilter/sample0)
- [case min](/documentation/metal/mtlmultisampledepthresolvefilter/min)
- [case max](/documentation/metal/mtlmultisampledepthresolvefilter/max)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlmultisampledepthresolvefilter/init(rawvalue:))
- [MTL4RenderPipelineColorAttachmentDescriptorArray](/documentation/metal/mtl4renderpipelinecolorattachmentdescriptorarray)

#### Instance Methods

- [func reset()](/documentation/metal/mtl4renderpipelinecolorattachmentdescriptorarray/reset())

#### Subscripts

- [subscript(Int) -> MTL4RenderPipelineColorAttachmentDescriptor!](/documentation/metal/mtl4renderpipelinecolorattachmentdescriptorarray/subscript(_:))
- [MTLTileRenderPipelineColorAttachmentDescriptorArray](/documentation/metal/mtltilerenderpipelinecolorattachmentdescriptorarray)

#### Instance methods

- [subscript(Int) -> MTLTileRenderPipelineColorAttachmentDescriptor](/documentation/metal/mtltilerenderpipelinecolorattachmentdescriptorarray/subscript(_:))
- [MTLRenderPassStencilAttachmentDescriptor](/documentation/metal/mtlrenderpassstencilattachmentdescriptor)

#### Specifying the resolve filter

- [var stencilResolveFilter: MTLMultisampleStencilResolveFilter](/documentation/metal/mtlrenderpassstencilattachmentdescriptor/stencilresolvefilter)

#### Specifying the stencil clear value

- [var clearStencil: UInt32](/documentation/metal/mtlrenderpassstencilattachmentdescriptor/clearstencil)
- [MTLMultisampleStencilResolveFilter](/documentation/metal/mtlmultisamplestencilresolvefilter)

#### Stencil resolve filters

- [case depthResolvedSample](/documentation/metal/mtlmultisamplestencilresolvefilter/depthresolvedsample)
- [case sample0](/documentation/metal/mtlmultisamplestencilresolvefilter/sample0)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlmultisamplestencilresolvefilter/init(rawvalue:))
- [MTLRenderPassSampleBufferAttachmentDescriptorArray](/documentation/metal/mtlrenderpasssamplebufferattachmentdescriptorarray)

#### Accessing a sample buffer attachment

- [subscript(Int) -> MTLRenderPassSampleBufferAttachmentDescriptor!](/documentation/metal/mtlrenderpasssamplebufferattachmentdescriptorarray/subscript(_:))
- [MTLRenderPassSampleBufferAttachmentDescriptor](/documentation/metal/mtlrenderpasssamplebufferattachmentdescriptor)

#### Configuring the sample buffer attachment

- [var sampleBuffer: (any MTLCounterSampleBuffer)?](/documentation/metal/mtlrenderpasssamplebufferattachmentdescriptor/samplebuffer)
- [var startOfVertexSampleIndex: Int](/documentation/metal/mtlrenderpasssamplebufferattachmentdescriptor/startofvertexsampleindex)
- [var endOfVertexSampleIndex: Int](/documentation/metal/mtlrenderpasssamplebufferattachmentdescriptor/endofvertexsampleindex)
- [var startOfFragmentSampleIndex: Int](/documentation/metal/mtlrenderpasssamplebufferattachmentdescriptor/startoffragmentsampleindex)
- [var endOfFragmentSampleIndex: Int](/documentation/metal/mtlrenderpasssamplebufferattachmentdescriptor/endoffragmentsampleindex)
- [MTLLogicalToPhysicalColorAttachmentMap](/documentation/metal/mtllogicaltophysicalcolorattachmentmap)

#### Instance Methods

- [func reset()](/documentation/metal/mtllogicaltophysicalcolorattachmentmap/reset())

#### Subscripts

- [subscript(Int) -> Int](/documentation/metal/mtllogicaltophysicalcolorattachmentmap/subscript(_:))
- [MTLDispatchThreadsIndirectArguments](/documentation/metal/mtldispatchthreadsindirectarguments)

#### Initializers

- [init()](/documentation/metal/mtldispatchthreadsindirectarguments/init())
- [init(threadsPerGrid: (UInt32, UInt32, UInt32), threadsPerThreadgroup: (UInt32, UInt32, UInt32))](/documentation/metal/mtldispatchthreadsindirectarguments/init(threadspergrid:threadsperthreadgroup:))

#### Instance Properties

- [var threadsPerGrid: (UInt32, UInt32, UInt32)](/documentation/metal/mtldispatchthreadsindirectarguments/threadspergrid)
- [var threadsPerThreadgroup: (UInt32, UInt32, UInt32)](/documentation/metal/mtldispatchthreadsindirectarguments/threadsperthreadgroup)

### Render pipeline states

- [MTLRenderPipelineState](/documentation/metal/mtlrenderpipelinestate)

#### Identifying a pipeline state

- [var device: any MTLDevice](/documentation/metal/mtlrenderpipelinestate/device)
- [var label: String?](/documentation/metal/mtlrenderpipelinestate/label)
- [var gpuResourceID: MTLResourceID](/documentation/metal/mtlrenderpipelinestate/gpuresourceid)

#### Checking object shader memory requirements

- [var maxTotalThreadsPerObjectThreadgroup: Int](/documentation/metal/mtlrenderpipelinestate/maxtotalthreadsperobjectthreadgroup)
- [var objectThreadExecutionWidth: Int](/documentation/metal/mtlrenderpipelinestate/objectthreadexecutionwidth)

#### Checking mesh shader memory requirements

- [var maxTotalThreadsPerMeshThreadgroup: Int](/documentation/metal/mtlrenderpipelinestate/maxtotalthreadspermeshthreadgroup)
- [var maxTotalThreadgroupsPerMeshGrid: Int](/documentation/metal/mtlrenderpipelinestate/maxtotalthreadgroupspermeshgrid)
- [var meshThreadExecutionWidth: Int](/documentation/metal/mtlrenderpipelinestate/meshthreadexecutionwidth)

#### Checking tile shader memory requirements

- [var maxTotalThreadsPerThreadgroup: Int](/documentation/metal/mtlrenderpipelinestate/maxtotalthreadsperthreadgroup)
- [var threadgroupSizeMatchesTileSize: Bool](/documentation/metal/mtlrenderpipelinestate/threadgroupsizematchestilesize)
- [var imageblockSampleLength: Int](/documentation/metal/mtlrenderpipelinestate/imageblocksamplelength)
- [func imageblockMemoryLength(forDimensions: MTLSize) -> Int](/documentation/metal/mtlrenderpipelinestate/imageblockmemorylength(fordimensions:))

#### Checking feature support

- [var supportIndirectCommandBuffers: Bool](/documentation/metal/mtlrenderpipelinestate/supportindirectcommandbuffers)

#### Checking shader validation

- [var shaderValidation: MTLShaderValidation](/documentation/metal/mtlrenderpipelinestate/shadervalidation)

#### Creating function handles and tables

- [func functionHandle(function: any MTLFunction, stage: MTLRenderStages) -> (any MTLFunctionHandle)?](/documentation/metal/mtlrenderpipelinestate/functionhandle(function:stage:)-7uvul)
- [func makeVisibleFunctionTable(descriptor: MTLVisibleFunctionTableDescriptor, stage: MTLRenderStages) -> (any MTLVisibleFunctionTable)?](/documentation/metal/mtlrenderpipelinestate/makevisiblefunctiontable(descriptor:stage:))
- [func makeIntersectionFunctionTable(descriptor: MTLIntersectionFunctionTableDescriptor, stage: MTLRenderStages) -> (any MTLIntersectionFunctionTable)?](/documentation/metal/mtlrenderpipelinestate/makeintersectionfunctiontable(descriptor:stage:))

#### Creating modified clones of the render pipeline

- [func makeRenderPipelineState(additionalBinaryFunctions: MTLRenderPipelineFunctionsDescriptor) throws -> any MTLRenderPipelineState](/documentation/metal/mtlrenderpipelinestate/makerenderpipelinestate(additionalbinaryfunctions:)-84te1)

#### Instance Properties

- [var reflection: MTLRenderPipelineReflection?](/documentation/metal/mtlrenderpipelinestate/reflection)
- [var requiredThreadsPerMeshThreadgroup: MTLSize](/documentation/metal/mtlrenderpipelinestate/requiredthreadspermeshthreadgroup)
- [var requiredThreadsPerObjectThreadgroup: MTLSize](/documentation/metal/mtlrenderpipelinestate/requiredthreadsperobjectthreadgroup)
- [var requiredThreadsPerTileThreadgroup: MTLSize](/documentation/metal/mtlrenderpipelinestate/requiredthreadspertilethreadgroup)

#### Instance Methods

- [func functionHandle(function: any MTL4BinaryFunction, stage: MTLRenderStages) -> (any MTLFunctionHandle)?](/documentation/metal/mtlrenderpipelinestate/functionhandle(function:stage:)-1pgxo)
- [func functionHandle(withName: String, stage: MTLRenderStages) -> (any MTLFunctionHandle)?](/documentation/metal/mtlrenderpipelinestate/functionhandle(withname:stage:))
- [func makeRenderPipelineDescriptorForSpecialization() -> MTL4PipelineDescriptor](/documentation/metal/mtlrenderpipelinestate/makerenderpipelinedescriptorforspecialization())
- [func makeRenderPipelineState(additionalBinaryFunctions: MTL4RenderPipelineBinaryFunctionsDescriptor) throws -> any MTLRenderPipelineState](/documentation/metal/mtlrenderpipelinestate/makerenderpipelinestate(additionalbinaryfunctions:)-49r1w)
- [MTL4RenderPipelineDescriptor](/documentation/metal/mtl4renderpipelinedescriptor)

#### Instance Properties

- [var alphaToCoverageState: MTL4AlphaToCoverageState](/documentation/metal/mtl4renderpipelinedescriptor/alphatocoveragestate)
- [var alphaToOneState: MTL4AlphaToOneState](/documentation/metal/mtl4renderpipelinedescriptor/alphatoonestate)
- [var colorAttachmentMappingState: MTL4LogicalToPhysicalColorAttachmentMappingState](/documentation/metal/mtl4renderpipelinedescriptor/colorattachmentmappingstate)
- [var colorAttachments: MTL4RenderPipelineColorAttachmentDescriptorArray](/documentation/metal/mtl4renderpipelinedescriptor/colorattachments)
- [var fragmentFunctionDescriptor: MTL4FunctionDescriptor?](/documentation/metal/mtl4renderpipelinedescriptor/fragmentfunctiondescriptor)
- [var fragmentStaticLinkingDescriptor: MTL4StaticLinkingDescriptor!](/documentation/metal/mtl4renderpipelinedescriptor/fragmentstaticlinkingdescriptor)
- [var inputPrimitiveTopology: MTLPrimitiveTopologyClass](/documentation/metal/mtl4renderpipelinedescriptor/inputprimitivetopology)
- [var isRasterizationEnabled: Bool](/documentation/metal/mtl4renderpipelinedescriptor/israsterizationenabled)
- [var maxVertexAmplificationCount: Int](/documentation/metal/mtl4renderpipelinedescriptor/maxvertexamplificationcount)
- [var rasterSampleCount: Int](/documentation/metal/mtl4renderpipelinedescriptor/rastersamplecount)
- [var supportFragmentBinaryLinking: Bool](/documentation/metal/mtl4renderpipelinedescriptor/supportfragmentbinarylinking)
- [var supportIndirectCommandBuffers: MTL4IndirectCommandBufferSupportState](/documentation/metal/mtl4renderpipelinedescriptor/supportindirectcommandbuffers)
- [var supportVertexBinaryLinking: Bool](/documentation/metal/mtl4renderpipelinedescriptor/supportvertexbinarylinking)
- [var vertexDescriptor: MTLVertexDescriptor?](/documentation/metal/mtl4renderpipelinedescriptor/vertexdescriptor)
- [var vertexFunctionDescriptor: MTL4FunctionDescriptor?](/documentation/metal/mtl4renderpipelinedescriptor/vertexfunctiondescriptor)
- [var vertexStaticLinkingDescriptor: MTL4StaticLinkingDescriptor!](/documentation/metal/mtl4renderpipelinedescriptor/vertexstaticlinkingdescriptor)

#### Instance Methods

- [func reset()](/documentation/metal/mtl4renderpipelinedescriptor/reset())
- [MTLRenderPipelineDescriptor](/documentation/metal/mtlrenderpipelinedescriptor)

#### Identifying the render pipeline state object

- [var label: String?](/documentation/metal/mtlrenderpipelinedescriptor/label)

#### Specifying graphics functions and associated data

- [var vertexFunction: (any MTLFunction)?](/documentation/metal/mtlrenderpipelinedescriptor/vertexfunction)
- [var fragmentFunction: (any MTLFunction)?](/documentation/metal/mtlrenderpipelinedescriptor/fragmentfunction)
- [var maxVertexCallStackDepth: Int](/documentation/metal/mtlrenderpipelinedescriptor/maxvertexcallstackdepth)
- [var maxFragmentCallStackDepth: Int](/documentation/metal/mtlrenderpipelinedescriptor/maxfragmentcallstackdepth)

#### Specifying buffer layouts and fetch behavior

- [var vertexDescriptor: MTLVertexDescriptor?](/documentation/metal/mtlrenderpipelinedescriptor/vertexdescriptor)

#### Specifying buffer mutability

- [var vertexBuffers: MTLPipelineBufferDescriptorArray](/documentation/metal/mtlrenderpipelinedescriptor/vertexbuffers)
- [var fragmentBuffers: MTLPipelineBufferDescriptorArray](/documentation/metal/mtlrenderpipelinedescriptor/fragmentbuffers)

#### Specifying rendering pipeline state

- [func reset()](/documentation/metal/mtlrenderpipelinedescriptor/reset())
- [var colorAttachments: MTLRenderPipelineColorAttachmentDescriptorArray](/documentation/metal/mtlrenderpipelinedescriptor/colorattachments)
- [var depthAttachmentPixelFormat: MTLPixelFormat](/documentation/metal/mtlrenderpipelinedescriptor/depthattachmentpixelformat)
- [var stencilAttachmentPixelFormat: MTLPixelFormat](/documentation/metal/mtlrenderpipelinedescriptor/stencilattachmentpixelformat)

#### Specifying rasterization and visibility state

- [var isAlphaToCoverageEnabled: Bool](/documentation/metal/mtlrenderpipelinedescriptor/isalphatocoverageenabled)
- [var isAlphaToOneEnabled: Bool](/documentation/metal/mtlrenderpipelinedescriptor/isalphatooneenabled)
- [var isRasterizationEnabled: Bool](/documentation/metal/mtlrenderpipelinedescriptor/israsterizationenabled)
- [var inputPrimitiveTopology: MTLPrimitiveTopologyClass](/documentation/metal/mtlrenderpipelinedescriptor/inputprimitivetopology)
- [var rasterSampleCount: Int](/documentation/metal/mtlrenderpipelinedescriptor/rastersamplecount)
- [MTLPrimitiveTopologyClass](/documentation/metal/mtlprimitivetopologyclass)

##### Topology classes

- [case unspecified](/documentation/metal/mtlprimitivetopologyclass/unspecified)
- [case point](/documentation/metal/mtlprimitivetopologyclass/point)
- [case line](/documentation/metal/mtlprimitivetopologyclass/line)
- [case triangle](/documentation/metal/mtlprimitivetopologyclass/triangle)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlprimitivetopologyclass/init(rawvalue:))
- [var sampleCount: Int](/documentation/metal/mtlrenderpipelinedescriptor/samplecount)

#### Specifying tessellation state

- [var maxTessellationFactor: Int](/documentation/metal/mtlrenderpipelinedescriptor/maxtessellationfactor)
- [var isTessellationFactorScaleEnabled: Bool](/documentation/metal/mtlrenderpipelinedescriptor/istessellationfactorscaleenabled)
- [var tessellationFactorFormat: MTLTessellationFactorFormat](/documentation/metal/mtlrenderpipelinedescriptor/tessellationfactorformat)
- [var tessellationControlPointIndexType: MTLTessellationControlPointIndexType](/documentation/metal/mtlrenderpipelinedescriptor/tessellationcontrolpointindextype)
- [var tessellationFactorStepFunction: MTLTessellationFactorStepFunction](/documentation/metal/mtlrenderpipelinedescriptor/tessellationfactorstepfunction)
- [var tessellationOutputWindingOrder: MTLWinding](/documentation/metal/mtlrenderpipelinedescriptor/tessellationoutputwindingorder)
- [var tessellationPartitionMode: MTLTessellationPartitionMode](/documentation/metal/mtlrenderpipelinedescriptor/tessellationpartitionmode)
- [MTLTessellationFactorFormat](/documentation/metal/mtltessellationfactorformat)

##### Factor formats

- [case half](/documentation/metal/mtltessellationfactorformat/half)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtltessellationfactorformat/init(rawvalue:))
- [MTLTessellationControlPointIndexType](/documentation/metal/mtltessellationcontrolpointindextype)

##### Index types

- [case none](/documentation/metal/mtltessellationcontrolpointindextype/none)
- [case uint16](/documentation/metal/mtltessellationcontrolpointindextype/uint16)
- [case uint32](/documentation/metal/mtltessellationcontrolpointindextype/uint32)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtltessellationcontrolpointindextype/init(rawvalue:))
- [MTLTessellationFactorStepFunction](/documentation/metal/mtltessellationfactorstepfunction)

##### Factor step functions

- [case constant](/documentation/metal/mtltessellationfactorstepfunction/constant)
- [case perPatch](/documentation/metal/mtltessellationfactorstepfunction/perpatch)
- [case perInstance](/documentation/metal/mtltessellationfactorstepfunction/perinstance)
- [case perPatchAndPerInstance](/documentation/metal/mtltessellationfactorstepfunction/perpatchandperinstance)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtltessellationfactorstepfunction/init(rawvalue:))
- [MTLTessellationPartitionMode](/documentation/metal/mtltessellationpartitionmode)

##### Partition modes

- [case pow2](/documentation/metal/mtltessellationpartitionmode/pow2)
- [case integer](/documentation/metal/mtltessellationpartitionmode/integer)
- [case fractionalOdd](/documentation/metal/mtltessellationpartitionmode/fractionalodd)
- [case fractionalEven](/documentation/metal/mtltessellationpartitionmode/fractionaleven)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtltessellationpartitionmode/init(rawvalue:))

#### Specifying indirect command buffers usage

- [var supportIndirectCommandBuffers: Bool](/documentation/metal/mtlrenderpipelinedescriptor/supportindirectcommandbuffers)

#### Specifying the maximum vertex amplification count

- [var maxVertexAmplificationCount: Int](/documentation/metal/mtlrenderpipelinedescriptor/maxvertexamplificationcount)

#### Specifying precompiled shader binaries

- [var supportAddingVertexBinaryFunctions: Bool](/documentation/metal/mtlrenderpipelinedescriptor/supportaddingvertexbinaryfunctions)
- [var supportAddingFragmentBinaryFunctions: Bool](/documentation/metal/mtlrenderpipelinedescriptor/supportaddingfragmentbinaryfunctions)
- [var binaryArchives: [any MTLBinaryArchive]?](/documentation/metal/mtlrenderpipelinedescriptor/binaryarchives)

#### Specifying callable functions for the pipeline

- [var vertexLinkedFunctions: MTLLinkedFunctions!](/documentation/metal/mtlrenderpipelinedescriptor/vertexlinkedfunctions)
- [var fragmentLinkedFunctions: MTLLinkedFunctions!](/documentation/metal/mtlrenderpipelinedescriptor/fragmentlinkedfunctions)

#### Specifying shader validation

- [var shaderValidation: MTLShaderValidation](/documentation/metal/mtlrenderpipelinedescriptor/shadervalidation)

#### Instance Properties

- [var fragmentPreloadedLibraries: [any MTLDynamicLibrary]](/documentation/metal/mtlrenderpipelinedescriptor/fragmentpreloadedlibraries)
- [var vertexPreloadedLibraries: [any MTLDynamicLibrary]](/documentation/metal/mtlrenderpipelinedescriptor/vertexpreloadedlibraries)
- [MTLRenderPipelineFunctionsDescriptor](/documentation/metal/mtlrenderpipelinefunctionsdescriptor)

#### Configuring the descriptor’s functions

- [var vertexAdditionalBinaryFunctions: [any MTLFunction]?](/documentation/metal/mtlrenderpipelinefunctionsdescriptor/vertexadditionalbinaryfunctions)
- [var fragmentAdditionalBinaryFunctions: [any MTLFunction]?](/documentation/metal/mtlrenderpipelinefunctionsdescriptor/fragmentadditionalbinaryfunctions)
- [var tileAdditionalBinaryFunctions: [any MTLFunction]?](/documentation/metal/mtlrenderpipelinefunctionsdescriptor/tileadditionalbinaryfunctions)
- [MTL4MeshRenderPipelineDescriptor](/documentation/metal/mtl4meshrenderpipelinedescriptor)

#### Instance Properties

- [var alphaToCoverageState: MTL4AlphaToCoverageState](/documentation/metal/mtl4meshrenderpipelinedescriptor/alphatocoveragestate)
- [var alphaToOneState: MTL4AlphaToOneState](/documentation/metal/mtl4meshrenderpipelinedescriptor/alphatoonestate)
- [var colorAttachmentMappingState: MTL4LogicalToPhysicalColorAttachmentMappingState](/documentation/metal/mtl4meshrenderpipelinedescriptor/colorattachmentmappingstate)
- [var colorAttachments: MTL4RenderPipelineColorAttachmentDescriptorArray](/documentation/metal/mtl4meshrenderpipelinedescriptor/colorattachments)
- [var fragmentFunctionDescriptor: MTL4FunctionDescriptor?](/documentation/metal/mtl4meshrenderpipelinedescriptor/fragmentfunctiondescriptor)
- [var fragmentStaticLinkingDescriptor: MTL4StaticLinkingDescriptor!](/documentation/metal/mtl4meshrenderpipelinedescriptor/fragmentstaticlinkingdescriptor)
- [var isRasterizationEnabled: Bool](/documentation/metal/mtl4meshrenderpipelinedescriptor/israsterizationenabled)
- [var maxTotalThreadgroupsPerMeshGrid: Int](/documentation/metal/mtl4meshrenderpipelinedescriptor/maxtotalthreadgroupspermeshgrid)
- [var maxTotalThreadsPerMeshThreadgroup: Int](/documentation/metal/mtl4meshrenderpipelinedescriptor/maxtotalthreadspermeshthreadgroup)
- [var maxTotalThreadsPerObjectThreadgroup: Int](/documentation/metal/mtl4meshrenderpipelinedescriptor/maxtotalthreadsperobjectthreadgroup)
- [var maxVertexAmplificationCount: Int](/documentation/metal/mtl4meshrenderpipelinedescriptor/maxvertexamplificationcount)
- [var meshFunctionDescriptor: MTL4FunctionDescriptor?](/documentation/metal/mtl4meshrenderpipelinedescriptor/meshfunctiondescriptor)
- [var meshStaticLinkingDescriptor: MTL4StaticLinkingDescriptor!](/documentation/metal/mtl4meshrenderpipelinedescriptor/meshstaticlinkingdescriptor)
- [var meshThreadgroupSizeIsMultipleOfThreadExecutionWidth: Bool](/documentation/metal/mtl4meshrenderpipelinedescriptor/meshthreadgroupsizeismultipleofthreadexecutionwidth)
- [var objectFunctionDescriptor: MTL4FunctionDescriptor?](/documentation/metal/mtl4meshrenderpipelinedescriptor/objectfunctiondescriptor)
- [var objectStaticLinkingDescriptor: MTL4StaticLinkingDescriptor!](/documentation/metal/mtl4meshrenderpipelinedescriptor/objectstaticlinkingdescriptor)
- [var objectThreadgroupSizeIsMultipleOfThreadExecutionWidth: Bool](/documentation/metal/mtl4meshrenderpipelinedescriptor/objectthreadgroupsizeismultipleofthreadexecutionwidth)
- [var payloadMemoryLength: Int](/documentation/metal/mtl4meshrenderpipelinedescriptor/payloadmemorylength)
- [var rasterSampleCount: Int](/documentation/metal/mtl4meshrenderpipelinedescriptor/rastersamplecount)
- [var requiredThreadsPerMeshThreadgroup: MTLSize](/documentation/metal/mtl4meshrenderpipelinedescriptor/requiredthreadspermeshthreadgroup)
- [var requiredThreadsPerObjectThreadgroup: MTLSize](/documentation/metal/mtl4meshrenderpipelinedescriptor/requiredthreadsperobjectthreadgroup)
- [var supportFragmentBinaryLinking: Bool](/documentation/metal/mtl4meshrenderpipelinedescriptor/supportfragmentbinarylinking)
- [var supportIndirectCommandBuffers: MTL4IndirectCommandBufferSupportState](/documentation/metal/mtl4meshrenderpipelinedescriptor/supportindirectcommandbuffers)
- [var supportMeshBinaryLinking: Bool](/documentation/metal/mtl4meshrenderpipelinedescriptor/supportmeshbinarylinking)
- [var supportObjectBinaryLinking: Bool](/documentation/metal/mtl4meshrenderpipelinedescriptor/supportobjectbinarylinking)

#### Instance Methods

- [func reset()](/documentation/metal/mtl4meshrenderpipelinedescriptor/reset())
- [MTLMeshRenderPipelineDescriptor](/documentation/metal/mtlmeshrenderpipelinedescriptor)

#### Instance Properties

- [var binaryArchives: [any MTLBinaryArchive]?](/documentation/metal/mtlmeshrenderpipelinedescriptor/binaryarchives)
- [var colorAttachments: MTLRenderPipelineColorAttachmentDescriptorArray](/documentation/metal/mtlmeshrenderpipelinedescriptor/colorattachments)
- [var depthAttachmentPixelFormat: MTLPixelFormat](/documentation/metal/mtlmeshrenderpipelinedescriptor/depthattachmentpixelformat)
- [var fragmentBuffers: MTLPipelineBufferDescriptorArray](/documentation/metal/mtlmeshrenderpipelinedescriptor/fragmentbuffers)
- [var fragmentFunction: (any MTLFunction)?](/documentation/metal/mtlmeshrenderpipelinedescriptor/fragmentfunction)
- [var fragmentLinkedFunctions: MTLLinkedFunctions!](/documentation/metal/mtlmeshrenderpipelinedescriptor/fragmentlinkedfunctions)
- [var isAlphaToCoverageEnabled: Bool](/documentation/metal/mtlmeshrenderpipelinedescriptor/isalphatocoverageenabled)
- [var isAlphaToOneEnabled: Bool](/documentation/metal/mtlmeshrenderpipelinedescriptor/isalphatooneenabled)
- [var isRasterizationEnabled: Bool](/documentation/metal/mtlmeshrenderpipelinedescriptor/israsterizationenabled)
- [var label: String?](/documentation/metal/mtlmeshrenderpipelinedescriptor/label)
- [var maxTotalThreadgroupsPerMeshGrid: Int](/documentation/metal/mtlmeshrenderpipelinedescriptor/maxtotalthreadgroupspermeshgrid)
- [var maxTotalThreadsPerMeshThreadgroup: Int](/documentation/metal/mtlmeshrenderpipelinedescriptor/maxtotalthreadspermeshthreadgroup)
- [var maxTotalThreadsPerObjectThreadgroup: Int](/documentation/metal/mtlmeshrenderpipelinedescriptor/maxtotalthreadsperobjectthreadgroup)
- [var maxVertexAmplificationCount: Int](/documentation/metal/mtlmeshrenderpipelinedescriptor/maxvertexamplificationcount)
- [var meshBuffers: MTLPipelineBufferDescriptorArray](/documentation/metal/mtlmeshrenderpipelinedescriptor/meshbuffers)
- [var meshFunction: (any MTLFunction)?](/documentation/metal/mtlmeshrenderpipelinedescriptor/meshfunction)
- [var meshLinkedFunctions: MTLLinkedFunctions!](/documentation/metal/mtlmeshrenderpipelinedescriptor/meshlinkedfunctions)
- [var meshThreadgroupSizeIsMultipleOfThreadExecutionWidth: Bool](/documentation/metal/mtlmeshrenderpipelinedescriptor/meshthreadgroupsizeismultipleofthreadexecutionwidth)
- [var objectBuffers: MTLPipelineBufferDescriptorArray](/documentation/metal/mtlmeshrenderpipelinedescriptor/objectbuffers)
- [var objectFunction: (any MTLFunction)?](/documentation/metal/mtlmeshrenderpipelinedescriptor/objectfunction)
- [var objectLinkedFunctions: MTLLinkedFunctions!](/documentation/metal/mtlmeshrenderpipelinedescriptor/objectlinkedfunctions)
- [var objectThreadgroupSizeIsMultipleOfThreadExecutionWidth: Bool](/documentation/metal/mtlmeshrenderpipelinedescriptor/objectthreadgroupsizeismultipleofthreadexecutionwidth)
- [var payloadMemoryLength: Int](/documentation/metal/mtlmeshrenderpipelinedescriptor/payloadmemorylength)
- [var rasterSampleCount: Int](/documentation/metal/mtlmeshrenderpipelinedescriptor/rastersamplecount)
- [var requiredThreadsPerMeshThreadgroup: MTLSize](/documentation/metal/mtlmeshrenderpipelinedescriptor/requiredthreadspermeshthreadgroup)
- [var requiredThreadsPerObjectThreadgroup: MTLSize](/documentation/metal/mtlmeshrenderpipelinedescriptor/requiredthreadsperobjectthreadgroup)
- [var shaderValidation: MTLShaderValidation](/documentation/metal/mtlmeshrenderpipelinedescriptor/shadervalidation)
- [var stencilAttachmentPixelFormat: MTLPixelFormat](/documentation/metal/mtlmeshrenderpipelinedescriptor/stencilattachmentpixelformat)
- [var supportIndirectCommandBuffers: Bool](/documentation/metal/mtlmeshrenderpipelinedescriptor/supportindirectcommandbuffers)

#### Instance Methods

- [func reset()](/documentation/metal/mtlmeshrenderpipelinedescriptor/reset())
- [MTLPipelineBufferDescriptor](/documentation/metal/mtlpipelinebufferdescriptor)

#### Setting buffer mutability

- [var mutability: MTLMutability](/documentation/metal/mtlpipelinebufferdescriptor/mutability)
- [MTLMutability](/documentation/metal/mtlmutability)

##### Enumeration cases

- [case `default`](/documentation/metal/mtlmutability/default)
- [case mutable](/documentation/metal/mtlmutability/mutable)
- [case immutable](/documentation/metal/mtlmutability/immutable)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlmutability/init(rawvalue:))
- [MTLPipelineBufferDescriptorArray](/documentation/metal/mtlpipelinebufferdescriptorarray)

#### Accessing array elements

- [subscript(Int) -> MTLPipelineBufferDescriptor!](/documentation/metal/mtlpipelinebufferdescriptorarray/subscript(_:))
- [MTL4RenderPipelineColorAttachmentDescriptor](/documentation/metal/mtl4renderpipelinecolorattachmentdescriptor)

#### Instance Properties

- [var alphaBlendOperation: MTLBlendOperation](/documentation/metal/mtl4renderpipelinecolorattachmentdescriptor/alphablendoperation)
- [var blendingState: MTL4BlendState](/documentation/metal/mtl4renderpipelinecolorattachmentdescriptor/blendingstate)
- [var destinationAlphaBlendFactor: MTLBlendFactor](/documentation/metal/mtl4renderpipelinecolorattachmentdescriptor/destinationalphablendfactor)
- [var destinationRGBBlendFactor: MTLBlendFactor](/documentation/metal/mtl4renderpipelinecolorattachmentdescriptor/destinationrgbblendfactor)
- [var pixelFormat: MTLPixelFormat](/documentation/metal/mtl4renderpipelinecolorattachmentdescriptor/pixelformat)
- [var rgbBlendOperation: MTLBlendOperation](/documentation/metal/mtl4renderpipelinecolorattachmentdescriptor/rgbblendoperation)
- [var sourceAlphaBlendFactor: MTLBlendFactor](/documentation/metal/mtl4renderpipelinecolorattachmentdescriptor/sourcealphablendfactor)
- [var sourceRGBBlendFactor: MTLBlendFactor](/documentation/metal/mtl4renderpipelinecolorattachmentdescriptor/sourcergbblendfactor)
- [var writeMask: MTLColorWriteMask](/documentation/metal/mtl4renderpipelinecolorattachmentdescriptor/writemask)

#### Instance Methods

- [func reset()](/documentation/metal/mtl4renderpipelinecolorattachmentdescriptor/reset())
- [MTLRenderPipelineColorAttachmentDescriptor](/documentation/metal/mtlrenderpipelinecolorattachmentdescriptor)

#### Configuring render pipeline states

- [var pixelFormat: MTLPixelFormat](/documentation/metal/mtlrenderpipelinecolorattachmentdescriptor/pixelformat)
- [var writeMask: MTLColorWriteMask](/documentation/metal/mtlrenderpipelinecolorattachmentdescriptor/writemask)
- [MTLColorWriteMask](/documentation/metal/mtlcolorwritemask)

##### Initializers

- [init(rawValue: UInt)](/documentation/metal/mtlcolorwritemask/init(rawvalue:))

##### Type Properties

- [static var all: MTLColorWriteMask](/documentation/metal/mtlcolorwritemask/all)
- [static var alpha: MTLColorWriteMask](/documentation/metal/mtlcolorwritemask/alpha)
- [static var blue: MTLColorWriteMask](/documentation/metal/mtlcolorwritemask/blue)
- [static var green: MTLColorWriteMask](/documentation/metal/mtlcolorwritemask/green)
- [static var red: MTLColorWriteMask](/documentation/metal/mtlcolorwritemask/red)
- [static var unspecialized: MTLColorWriteMask](/documentation/metal/mtlcolorwritemask/unspecialized)

#### Controlling blend operations

- [var isBlendingEnabled: Bool](/documentation/metal/mtlrenderpipelinecolorattachmentdescriptor/isblendingenabled)
- [var alphaBlendOperation: MTLBlendOperation](/documentation/metal/mtlrenderpipelinecolorattachmentdescriptor/alphablendoperation)
- [var rgbBlendOperation: MTLBlendOperation](/documentation/metal/mtlrenderpipelinecolorattachmentdescriptor/rgbblendoperation)
- [MTLBlendOperation](/documentation/metal/mtlblendoperation)

##### Blend operations

- [case add](/documentation/metal/mtlblendoperation/add)
- [case subtract](/documentation/metal/mtlblendoperation/subtract)
- [case reverseSubtract](/documentation/metal/mtlblendoperation/reversesubtract)
- [case min](/documentation/metal/mtlblendoperation/min)
- [case max](/documentation/metal/mtlblendoperation/max)

##### Enumeration Cases

- [case unspecialized](/documentation/metal/mtlblendoperation/unspecialized)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlblendoperation/init(rawvalue:))

#### Configuring blend factors

- [var destinationAlphaBlendFactor: MTLBlendFactor](/documentation/metal/mtlrenderpipelinecolorattachmentdescriptor/destinationalphablendfactor)
- [var destinationRGBBlendFactor: MTLBlendFactor](/documentation/metal/mtlrenderpipelinecolorattachmentdescriptor/destinationrgbblendfactor)
- [var sourceAlphaBlendFactor: MTLBlendFactor](/documentation/metal/mtlrenderpipelinecolorattachmentdescriptor/sourcealphablendfactor)
- [var sourceRGBBlendFactor: MTLBlendFactor](/documentation/metal/mtlrenderpipelinecolorattachmentdescriptor/sourcergbblendfactor)
- [MTLBlendFactor](/documentation/metal/mtlblendfactor)

##### Blend factors

- [case zero](/documentation/metal/mtlblendfactor/zero)
- [case one](/documentation/metal/mtlblendfactor/one)
- [case sourceColor](/documentation/metal/mtlblendfactor/sourcecolor)
- [case oneMinusSourceColor](/documentation/metal/mtlblendfactor/oneminussourcecolor)
- [case sourceAlpha](/documentation/metal/mtlblendfactor/sourcealpha)
- [case oneMinusSourceAlpha](/documentation/metal/mtlblendfactor/oneminussourcealpha)
- [case destinationColor](/documentation/metal/mtlblendfactor/destinationcolor)
- [case oneMinusDestinationColor](/documentation/metal/mtlblendfactor/oneminusdestinationcolor)
- [case destinationAlpha](/documentation/metal/mtlblendfactor/destinationalpha)
- [case oneMinusDestinationAlpha](/documentation/metal/mtlblendfactor/oneminusdestinationalpha)
- [case sourceAlphaSaturated](/documentation/metal/mtlblendfactor/sourcealphasaturated)
- [case blendColor](/documentation/metal/mtlblendfactor/blendcolor)
- [case oneMinusBlendColor](/documentation/metal/mtlblendfactor/oneminusblendcolor)
- [case blendAlpha](/documentation/metal/mtlblendfactor/blendalpha)
- [case oneMinusBlendAlpha](/documentation/metal/mtlblendfactor/oneminusblendalpha)
- [case source1Color](/documentation/metal/mtlblendfactor/source1color)
- [case oneMinusSource1Color](/documentation/metal/mtlblendfactor/oneminussource1color)
- [case source1Alpha](/documentation/metal/mtlblendfactor/source1alpha)
- [case oneMinusSource1Alpha](/documentation/metal/mtlblendfactor/oneminussource1alpha)

##### Enumeration Cases

- [case unspecialized](/documentation/metal/mtlblendfactor/unspecialized)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlblendfactor/init(rawvalue:))
- [MTLRenderPipelineColorAttachmentDescriptorArray](/documentation/metal/mtlrenderpipelinecolorattachmentdescriptorarray)

#### Accessing render pipeline state for a color attachment

- [subscript(Int) -> MTLRenderPipelineColorAttachmentDescriptor!](/documentation/metal/mtlrenderpipelinecolorattachmentdescriptorarray/subscript(_:))
- [MTL4TileRenderPipelineDescriptor](/documentation/metal/mtl4tilerenderpipelinedescriptor)

#### Instance Properties

- [var colorAttachments: MTLTileRenderPipelineColorAttachmentDescriptorArray](/documentation/metal/mtl4tilerenderpipelinedescriptor/colorattachments)
- [var maxTotalThreadsPerThreadgroup: Int](/documentation/metal/mtl4tilerenderpipelinedescriptor/maxtotalthreadsperthreadgroup)
- [var rasterSampleCount: Int](/documentation/metal/mtl4tilerenderpipelinedescriptor/rastersamplecount)
- [var requiredThreadsPerThreadgroup: MTLSize](/documentation/metal/mtl4tilerenderpipelinedescriptor/requiredthreadsperthreadgroup)
- [var staticLinkingDescriptor: MTL4StaticLinkingDescriptor!](/documentation/metal/mtl4tilerenderpipelinedescriptor/staticlinkingdescriptor)
- [var supportBinaryLinking: Bool](/documentation/metal/mtl4tilerenderpipelinedescriptor/supportbinarylinking)
- [var threadgroupSizeMatchesTileSize: Bool](/documentation/metal/mtl4tilerenderpipelinedescriptor/threadgroupsizematchestilesize)
- [var tileFunctionDescriptor: MTL4FunctionDescriptor?](/documentation/metal/mtl4tilerenderpipelinedescriptor/tilefunctiondescriptor)

#### Instance Methods

- [func reset()](/documentation/metal/mtl4tilerenderpipelinedescriptor/reset())
- [MTLTileRenderPipelineDescriptor](/documentation/metal/mtltilerenderpipelinedescriptor)

#### Identifying the render pipeline

- [var label: String?](/documentation/metal/mtltilerenderpipelinedescriptor/label)

#### Specifying graphics functions and associated data

- [var tileFunction: any MTLFunction](/documentation/metal/mtltilerenderpipelinedescriptor/tilefunction)
- [var tileBuffers: MTLPipelineBufferDescriptorArray](/documentation/metal/mtltilerenderpipelinedescriptor/tilebuffers)
- [var maxCallStackDepth: Int](/documentation/metal/mtltilerenderpipelinedescriptor/maxcallstackdepth)

#### Specifying rasterization and visibility state

- [var threadgroupSizeMatchesTileSize: Bool](/documentation/metal/mtltilerenderpipelinedescriptor/threadgroupsizematchestilesize)
- [var rasterSampleCount: Int](/documentation/metal/mtltilerenderpipelinedescriptor/rastersamplecount)

#### Specifying rendering pipeline state

- [func reset()](/documentation/metal/mtltilerenderpipelinedescriptor/reset())
- [var colorAttachments: MTLTileRenderPipelineColorAttachmentDescriptorArray](/documentation/metal/mtltilerenderpipelinedescriptor/colorattachments)

#### Specifying threads per threadgroup

- [var maxTotalThreadsPerThreadgroup: Int](/documentation/metal/mtltilerenderpipelinedescriptor/maxtotalthreadsperthreadgroup)

#### Specifying precompiled shader binaries

- [var supportAddingBinaryFunctions: Bool](/documentation/metal/mtltilerenderpipelinedescriptor/supportaddingbinaryfunctions)
- [var binaryArchives: [any MTLBinaryArchive]?](/documentation/metal/mtltilerenderpipelinedescriptor/binaryarchives)

#### Specifying callable functions for the pipeline

- [var linkedFunctions: MTLLinkedFunctions!](/documentation/metal/mtltilerenderpipelinedescriptor/linkedfunctions)

#### Specifying shader validation

- [var shaderValidation: MTLShaderValidation](/documentation/metal/mtltilerenderpipelinedescriptor/shadervalidation)

#### Instance Properties

- [var preloadedLibraries: [any MTLDynamicLibrary]](/documentation/metal/mtltilerenderpipelinedescriptor/preloadedlibraries)
- [var requiredThreadsPerThreadgroup: MTLSize](/documentation/metal/mtltilerenderpipelinedescriptor/requiredthreadsperthreadgroup)
- [MTLTileRenderPipelineColorAttachmentDescriptor](/documentation/metal/mtltilerenderpipelinecolorattachmentdescriptor)

#### Specifying pixel format

- [var pixelFormat: MTLPixelFormat](/documentation/metal/mtltilerenderpipelinecolorattachmentdescriptor/pixelformat)
- [MTLPipelineOption](/documentation/metal/mtlpipelineoption)

#### Retrieving argument information

- [static var bufferTypeInfo: MTLPipelineOption](/documentation/metal/mtlpipelineoption/buffertypeinfo)
- [static var failOnBinaryArchiveMiss: MTLPipelineOption](/documentation/metal/mtlpipelineoption/failonbinaryarchivemiss)
- [static var argumentInfo: MTLPipelineOption](/documentation/metal/mtlpipelineoption/argumentinfo)

#### Creating compilation options

- [init(rawValue: UInt)](/documentation/metal/mtlpipelineoption/init(rawvalue:))

#### Type properties

- [static var bindingInfo: MTLPipelineOption](/documentation/metal/mtlpipelineoption/bindinginfo)
- [MTL4RenderPipelineBinaryFunctionsDescriptor](/documentation/metal/mtl4renderpipelinebinaryfunctionsdescriptor)

#### Instance Properties

- [var fragmentAdditionalBinaryFunctions: [any MTL4BinaryFunction]?](/documentation/metal/mtl4renderpipelinebinaryfunctionsdescriptor/fragmentadditionalbinaryfunctions)
- [var meshAdditionalBinaryFunctions: [any MTL4BinaryFunction]?](/documentation/metal/mtl4renderpipelinebinaryfunctionsdescriptor/meshadditionalbinaryfunctions)
- [var objectAdditionalBinaryFunctions: [any MTL4BinaryFunction]?](/documentation/metal/mtl4renderpipelinebinaryfunctionsdescriptor/objectadditionalbinaryfunctions)
- [var tileAdditionalBinaryFunctions: [any MTL4BinaryFunction]?](/documentation/metal/mtl4renderpipelinebinaryfunctionsdescriptor/tileadditionalbinaryfunctions)
- [var vertexAdditionalBinaryFunctions: [any MTL4BinaryFunction]?](/documentation/metal/mtl4renderpipelinebinaryfunctionsdescriptor/vertexadditionalbinaryfunctions)

#### Instance Methods

- [func reset()](/documentation/metal/mtl4renderpipelinebinaryfunctionsdescriptor/reset())
- [MTL4RenderPipelineDynamicLinkingDescriptor](/documentation/metal/mtl4renderpipelinedynamiclinkingdescriptor)

#### Instance Properties

- [var fragmentLinkingDescriptor: MTL4PipelineStageDynamicLinkingDescriptor](/documentation/metal/mtl4renderpipelinedynamiclinkingdescriptor/fragmentlinkingdescriptor)
- [var meshLinkingDescriptor: MTL4PipelineStageDynamicLinkingDescriptor](/documentation/metal/mtl4renderpipelinedynamiclinkingdescriptor/meshlinkingdescriptor)
- [var objectLinkingDescriptor: MTL4PipelineStageDynamicLinkingDescriptor](/documentation/metal/mtl4renderpipelinedynamiclinkingdescriptor/objectlinkingdescriptor)
- [var tileLinkingDescriptor: MTL4PipelineStageDynamicLinkingDescriptor](/documentation/metal/mtl4renderpipelinedynamiclinkingdescriptor/tilelinkingdescriptor)
- [var vertexLinkingDescriptor: MTL4PipelineStageDynamicLinkingDescriptor](/documentation/metal/mtl4renderpipelinedynamiclinkingdescriptor/vertexlinkingdescriptor)

### Dynamic render pipeline states

- [MTLViewport](/documentation/metal/mtlviewport)

#### Creating a viewport

- [init()](/documentation/metal/mtlviewport/init())
- [init(originX: Double, originY: Double, width: Double, height: Double, znear: Double, zfar: Double)](/documentation/metal/mtlviewport/init(originx:originy:width:height:znear:zfar:))

#### Specifying viewport boundaries

- [var originX: Double](/documentation/metal/mtlviewport/originx)
- [var originY: Double](/documentation/metal/mtlviewport/originy)
- [var width: Double](/documentation/metal/mtlviewport/width)
- [var height: Double](/documentation/metal/mtlviewport/height)
- [var znear: Double](/documentation/metal/mtlviewport/znear)
- [var zfar: Double](/documentation/metal/mtlviewport/zfar)
- [MTLScissorRect](/documentation/metal/mtlscissorrect)

#### Creating a scissor rectangle

- [init()](/documentation/metal/mtlscissorrect/init())
- [init(x: Int, y: Int, width: Int, height: Int)](/documentation/metal/mtlscissorrect/init(x:y:width:height:))

#### Specifying scissor boundaries

- [var height: Int](/documentation/metal/mtlscissorrect/height)
- [var width: Int](/documentation/metal/mtlscissorrect/width)
- [var x: Int](/documentation/metal/mtlscissorrect/x)
- [var y: Int](/documentation/metal/mtlscissorrect/y)
- [MTLVertexAmplificationViewMapping](/documentation/metal/mtlvertexamplificationviewmapping)

#### Creating a view mapping

- [init()](/documentation/metal/mtlvertexamplificationviewmapping/init())
- [init(viewportArrayIndexOffset: UInt32, renderTargetArrayIndexOffset: UInt32)](/documentation/metal/mtlvertexamplificationviewmapping/init(viewportarrayindexoffset:rendertargetarrayindexoffset:))

#### Specifying mapping offsets

- [var renderTargetArrayIndexOffset: UInt32](/documentation/metal/mtlvertexamplificationviewmapping/rendertargetarrayindexoffset)
- [var viewportArrayIndexOffset: UInt32](/documentation/metal/mtlvertexamplificationviewmapping/viewportarrayindexoffset)
- [MTLQuadTessellationFactorsHalf](/documentation/metal/mtlquadtessellationfactorshalf)

#### Initializers

- [init()](/documentation/metal/mtlquadtessellationfactorshalf/init())
- [init(edgeTessellationFactor: (UInt16, UInt16, UInt16, UInt16), insideTessellationFactor: (UInt16, UInt16))](/documentation/metal/mtlquadtessellationfactorshalf/init(edgetessellationfactor:insidetessellationfactor:))

#### Instance Properties

- [var edgeTessellationFactor: (UInt16, UInt16, UInt16, UInt16)](/documentation/metal/mtlquadtessellationfactorshalf/edgetessellationfactor)
- [var insideTessellationFactor: (UInt16, UInt16)](/documentation/metal/mtlquadtessellationfactorshalf/insidetessellationfactor)
- [MTLTriangleTessellationFactorsHalf](/documentation/metal/mtltriangletessellationfactorshalf)

#### Initializers

- [init()](/documentation/metal/mtltriangletessellationfactorshalf/init())
- [init(edgeTessellationFactor: (UInt16, UInt16, UInt16), insideTessellationFactor: UInt16)](/documentation/metal/mtltriangletessellationfactorshalf/init(edgetessellationfactor:insidetessellationfactor:))

#### Instance Properties

- [var edgeTessellationFactor: (UInt16, UInt16, UInt16)](/documentation/metal/mtltriangletessellationfactorshalf/edgetessellationfactor)
- [var insideTessellationFactor: UInt16](/documentation/metal/mtltriangletessellationfactorshalf/insidetessellationfactor)

### Render pass inputs

- [MTLVertexDescriptor](/documentation/metal/mtlvertexdescriptor)

#### Setting default values

- [func reset()](/documentation/metal/mtlvertexdescriptor/reset())

#### Accessing the vertex buffer layouts and vertex attributes

- [var attributes: MTLVertexAttributeDescriptorArray](/documentation/metal/mtlvertexdescriptor/attributes)
- [var layouts: MTLVertexBufferLayoutDescriptorArray](/documentation/metal/mtlvertexdescriptor/layouts)
- [MTLVertexAttributeDescriptor](/documentation/metal/mtlvertexattributedescriptor)

#### Organizing the vertex attribute

- [var format: MTLVertexFormat](/documentation/metal/mtlvertexattributedescriptor/format)
- [var offset: Int](/documentation/metal/mtlvertexattributedescriptor/offset)
- [var bufferIndex: Int](/documentation/metal/mtlvertexattributedescriptor/bufferindex)
- [MTLVertexFormat](/documentation/metal/mtlvertexformat)

##### Vertex formats

- [case invalid](/documentation/metal/mtlvertexformat/invalid)
- [case uchar](/documentation/metal/mtlvertexformat/uchar)
- [case uchar2](/documentation/metal/mtlvertexformat/uchar2)
- [case uchar3](/documentation/metal/mtlvertexformat/uchar3)
- [case uchar4](/documentation/metal/mtlvertexformat/uchar4)
- [case char](/documentation/metal/mtlvertexformat/char)
- [case char2](/documentation/metal/mtlvertexformat/char2)
- [case char3](/documentation/metal/mtlvertexformat/char3)
- [case char4](/documentation/metal/mtlvertexformat/char4)
- [case ucharNormalized](/documentation/metal/mtlvertexformat/ucharnormalized)
- [case uchar2Normalized](/documentation/metal/mtlvertexformat/uchar2normalized)
- [case uchar3Normalized](/documentation/metal/mtlvertexformat/uchar3normalized)
- [case uchar4Normalized](/documentation/metal/mtlvertexformat/uchar4normalized)
- [case charNormalized](/documentation/metal/mtlvertexformat/charnormalized)
- [case char2Normalized](/documentation/metal/mtlvertexformat/char2normalized)
- [case char3Normalized](/documentation/metal/mtlvertexformat/char3normalized)
- [case char4Normalized](/documentation/metal/mtlvertexformat/char4normalized)
- [case ushort](/documentation/metal/mtlvertexformat/ushort)
- [case ushort2](/documentation/metal/mtlvertexformat/ushort2)
- [case ushort3](/documentation/metal/mtlvertexformat/ushort3)
- [case ushort4](/documentation/metal/mtlvertexformat/ushort4)
- [case short](/documentation/metal/mtlvertexformat/short)
- [case short2](/documentation/metal/mtlvertexformat/short2)
- [case short3](/documentation/metal/mtlvertexformat/short3)
- [case short4](/documentation/metal/mtlvertexformat/short4)
- [case ushortNormalized](/documentation/metal/mtlvertexformat/ushortnormalized)
- [case ushort2Normalized](/documentation/metal/mtlvertexformat/ushort2normalized)
- [case ushort3Normalized](/documentation/metal/mtlvertexformat/ushort3normalized)
- [case ushort4Normalized](/documentation/metal/mtlvertexformat/ushort4normalized)
- [case shortNormalized](/documentation/metal/mtlvertexformat/shortnormalized)
- [case short2Normalized](/documentation/metal/mtlvertexformat/short2normalized)
- [case short3Normalized](/documentation/metal/mtlvertexformat/short3normalized)
- [case short4Normalized](/documentation/metal/mtlvertexformat/short4normalized)
- [case half](/documentation/metal/mtlvertexformat/half)
- [case half2](/documentation/metal/mtlvertexformat/half2)
- [case half3](/documentation/metal/mtlvertexformat/half3)
- [case half4](/documentation/metal/mtlvertexformat/half4)
- [case float](/documentation/metal/mtlvertexformat/float)
- [case float2](/documentation/metal/mtlvertexformat/float2)
- [case float3](/documentation/metal/mtlvertexformat/float3)
- [case float4](/documentation/metal/mtlvertexformat/float4)
- [case uint](/documentation/metal/mtlvertexformat/uint)
- [case uint2](/documentation/metal/mtlvertexformat/uint2)
- [case uint3](/documentation/metal/mtlvertexformat/uint3)
- [case uint4](/documentation/metal/mtlvertexformat/uint4)
- [case int](/documentation/metal/mtlvertexformat/int)
- [case int2](/documentation/metal/mtlvertexformat/int2)
- [case int3](/documentation/metal/mtlvertexformat/int3)
- [case int4](/documentation/metal/mtlvertexformat/int4)
- [case int1010102Normalized](/documentation/metal/mtlvertexformat/int1010102normalized)
- [case uint1010102Normalized](/documentation/metal/mtlvertexformat/uint1010102normalized)
- [case uchar4Normalized_bgra](/documentation/metal/mtlvertexformat/uchar4normalized_bgra)

##### Enumeration Cases

- [case floatRG11B10](/documentation/metal/mtlvertexformat/floatrg11b10)
- [case floatRGB9E5](/documentation/metal/mtlvertexformat/floatrgb9e5)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlvertexformat/init(rawvalue:))
- [MTLVertexAttributeDescriptorArray](/documentation/metal/mtlvertexattributedescriptorarray)

#### Accessing a specified vertex attribute

- [subscript(Int) -> MTLVertexAttributeDescriptor!](/documentation/metal/mtlvertexattributedescriptorarray/subscript(_:))
- [MTLVertexBufferLayoutDescriptor](/documentation/metal/mtlvertexbufferlayoutdescriptor)

#### Organizing the vertex buffer layout

- [var stepFunction: MTLVertexStepFunction](/documentation/metal/mtlvertexbufferlayoutdescriptor/stepfunction)
- [var stepRate: Int](/documentation/metal/mtlvertexbufferlayoutdescriptor/steprate)
- [var stride: Int](/documentation/metal/mtlvertexbufferlayoutdescriptor/stride)
- [MTLVertexStepFunction](/documentation/metal/mtlvertexstepfunction)

##### Step functions

- [case constant](/documentation/metal/mtlvertexstepfunction/constant)
- [case perVertex](/documentation/metal/mtlvertexstepfunction/pervertex)
- [case perInstance](/documentation/metal/mtlvertexstepfunction/perinstance)
- [case perPatch](/documentation/metal/mtlvertexstepfunction/perpatch)
- [case perPatchControlPoint](/documentation/metal/mtlvertexstepfunction/perpatchcontrolpoint)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlvertexstepfunction/init(rawvalue:))
- [MTLVertexBufferLayoutDescriptorArray](/documentation/metal/mtlvertexbufferlayoutdescriptorarray)

#### Accessing a specified vertex buffer layout

- [subscript(Int) -> MTLVertexBufferLayoutDescriptor!](/documentation/metal/mtlvertexbufferlayoutdescriptorarray/subscript(_:))
- [let MTLBufferLayoutStrideDynamic: Int](/documentation/metal/mtlbufferlayoutstridedynamic)

### Render pass outputs

- [MTLDrawable](/documentation/metal/mtldrawable)

#### Identifying the drawable

- [var drawableID: Int](/documentation/metal/mtldrawable/drawableid)

#### Presenting the drawable

- [func present()](/documentation/metal/mtldrawable/present())
- [func present(afterMinimumDuration: CFTimeInterval)](/documentation/metal/mtldrawable/present(afterminimumduration:))
- [func present(at: CFTimeInterval)](/documentation/metal/mtldrawable/present(at:))

#### Getting presentation information

- [func addPresentedHandler(MTLDrawablePresentedHandler)](/documentation/metal/mtldrawable/addpresentedhandler(_:))
- [var presentedTime: CFTimeInterval](/documentation/metal/mtldrawable/presentedtime)
- [MTLDrawablePresentedHandler](/documentation/metal/mtldrawablepresentedhandler)

### Depth testing

- [Calculating primitive visibility using depth testing](/documentation/metal/calculating-primitive-visibility-using-depth-testing)
- [MTLDepthStencilState](/documentation/metal/mtldepthstencilstate)

#### Identifying properties

- [var device: any MTLDevice](/documentation/metal/mtldepthstencilstate/device)
- [var label: String?](/documentation/metal/mtldepthstencilstate/label)

#### Instance Properties

- [var gpuResourceID: MTLResourceID](/documentation/metal/mtldepthstencilstate/gpuresourceid)
- [MTLDepthStencilDescriptor](/documentation/metal/mtldepthstencildescriptor)

#### Specifying depth operations

- [var depthCompareFunction: MTLCompareFunction](/documentation/metal/mtldepthstencildescriptor/depthcomparefunction)
- [var isDepthWriteEnabled: Bool](/documentation/metal/mtldepthstencildescriptor/isdepthwriteenabled)

#### Specifying stencil descriptors for primitives

- [var backFaceStencil: MTLStencilDescriptor!](/documentation/metal/mtldepthstencildescriptor/backfacestencil)
- [var frontFaceStencil: MTLStencilDescriptor!](/documentation/metal/mtldepthstencildescriptor/frontfacestencil)

#### Identifying properties

- [var label: String?](/documentation/metal/mtldepthstencildescriptor/label)
- [MTLStencilDescriptor](/documentation/metal/mtlstencildescriptor)

#### Configuring stencil functions and operations

- [var stencilFailureOperation: MTLStencilOperation](/documentation/metal/mtlstencildescriptor/stencilfailureoperation)
- [var depthFailureOperation: MTLStencilOperation](/documentation/metal/mtlstencildescriptor/depthfailureoperation)
- [var depthStencilPassOperation: MTLStencilOperation](/documentation/metal/mtlstencildescriptor/depthstencilpassoperation)
- [var stencilCompareFunction: MTLCompareFunction](/documentation/metal/mtlstencildescriptor/stencilcomparefunction)
- [MTLStencilOperation](/documentation/metal/mtlstenciloperation)

##### Stencil operations

- [case keep](/documentation/metal/mtlstenciloperation/keep)
- [case zero](/documentation/metal/mtlstenciloperation/zero)
- [case replace](/documentation/metal/mtlstenciloperation/replace)
- [case incrementClamp](/documentation/metal/mtlstenciloperation/incrementclamp)
- [case decrementClamp](/documentation/metal/mtlstenciloperation/decrementclamp)
- [case invert](/documentation/metal/mtlstenciloperation/invert)
- [case incrementWrap](/documentation/metal/mtlstenciloperation/incrementwrap)
- [case decrementWrap](/documentation/metal/mtlstenciloperation/decrementwrap)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlstenciloperation/init(rawvalue:))

#### Configuring stencil bit mask properties

- [var readMask: UInt32](/documentation/metal/mtlstencildescriptor/readmask)
- [var writeMask: UInt32](/documentation/metal/mtlstencildescriptor/writemask)

### Rasterization settings

- [Rendering at different rasterization rates](/documentation/metal/rendering-at-different-rasterization-rates)
- [Creating a rasterization rate map](/documentation/metal/creating-a-rasterization-rate-map)
- [Rendering with a rasterization rate map](/documentation/metal/rendering-with-a-rasterization-rate-map)
- [Scaling variable rasterization rate content](/documentation/metal/scaling-variable-rasterization-rate-content)
- [MTLRasterizationRateMapDescriptor](/documentation/metal/mtlrasterizationratemapdescriptor)

#### Creating rate map descriptors

- [convenience init(screenSize: MTLSize, label: String?)](/documentation/metal/mtlrasterizationratemapdescriptor/init(screensize:label:))
- [convenience init(screenSize: MTLSize, layer: MTLRasterizationRateLayerDescriptor, label: String?)](/documentation/metal/mtlrasterizationratemapdescriptor/init(screensize:layer:label:))
- [convenience init(screenSize: MTLSize, layers: [MTLRasterizationRateLayerDescriptor], label: String?)](/documentation/metal/mtlrasterizationratemapdescriptor/init(screensize:layers:label:))

#### Identifying the rate map

- [var label: String?](/documentation/metal/mtlrasterizationratemapdescriptor/label)

#### Configuring the viewport size

- [var screenSize: MTLSize](/documentation/metal/mtlrasterizationratemapdescriptor/screensize)

#### Configuring the rate map layers

- [var layerCount: Int](/documentation/metal/mtlrasterizationratemapdescriptor/layercount)
- [func layer(at: Int) -> MTLRasterizationRateLayerDescriptor?](/documentation/metal/mtlrasterizationratemapdescriptor/layer(at:))
- [func setLayer(MTLRasterizationRateLayerDescriptor?, at: Int)](/documentation/metal/mtlrasterizationratemapdescriptor/setlayer(_:at:))
- [var layers: MTLRasterizationRateLayerArray](/documentation/metal/mtlrasterizationratemapdescriptor/layers)
- [MTLRasterizationRateLayerArray](/documentation/metal/mtlrasterizationratelayerarray)

##### Accessing members of the array

- [subscript(Int) -> MTLRasterizationRateLayerDescriptor?](/documentation/metal/mtlrasterizationratelayerarray/subscript(_:))
- [MTLRasterizationRateLayerDescriptor](/documentation/metal/mtlrasterizationratelayerdescriptor)

###### Creating a layer rasterization rate descriptor

- [init(sampleCount: MTLSize)](/documentation/metal/mtlrasterizationratelayerdescriptor/init(samplecount:))
- [convenience init(horizontal: [Float], vertical: [Float])](/documentation/metal/mtlrasterizationratelayerdescriptor/init(horizontal:vertical:))

###### Inspecting the layer rate function parameters

- [var sampleCount: MTLSize](/documentation/metal/mtlrasterizationratelayerdescriptor/samplecount)
- [var maxSampleCount: MTLSize](/documentation/metal/mtlrasterizationratelayerdescriptor/maxsamplecount)
- [var horizontal: MTLRasterizationRateSampleArray](/documentation/metal/mtlrasterizationratelayerdescriptor/horizontal)
- [var vertical: MTLRasterizationRateSampleArray](/documentation/metal/mtlrasterizationratelayerdescriptor/vertical)
- [MTLRasterizationRateSampleArray](/documentation/metal/mtlrasterizationratesamplearray)

###### Accessing the array

- [subscript(Int) -> Float](/documentation/metal/mtlrasterizationratesamplearray/subscript(_:))
- [MTLRasterizationRateMap](/documentation/metal/mtlrasterizationratemap)

#### Identifying the rate map

- [var device: any MTLDevice](/documentation/metal/mtlrasterizationratemap/device)
- [var label: String?](/documentation/metal/mtlrasterizationratemap/label)

#### Inspecting geometric and rendering properties

- [var layerCount: Int](/documentation/metal/mtlrasterizationratemap/layercount)
- [var screenSize: MTLSize](/documentation/metal/mtlrasterizationratemap/screensize)
- [func physicalSize(layer: Int) -> MTLSize](/documentation/metal/mtlrasterizationratemap/physicalsize(layer:))
- [var physicalGranularity: MTLSize](/documentation/metal/mtlrasterizationratemap/physicalgranularity)

#### Converting between viewport and physical coordinates

- [func physicalCoordinates(screenCoordinates: MTLCoordinate2D, layer: Int) -> MTLCoordinate2D](/documentation/metal/mtlrasterizationratemap/physicalcoordinates(screencoordinates:layer:))
- [func screenCoordinates(physicalCoordinates: MTLCoordinate2D, layer: Int) -> MTLCoordinate2D](/documentation/metal/mtlrasterizationratemap/screencoordinates(physicalcoordinates:layer:))

#### Obtaining coordinate transformation data

- [var parameterDataSizeAndAlign: MTLSizeAndAlign](/documentation/metal/mtlrasterizationratemap/parameterdatasizeandalign)
- [func copyParameterData(buffer: any MTLBuffer, offset: Int)](/documentation/metal/mtlrasterizationratemap/copyparameterdata(buffer:offset:))
- [MTLCoordinate2D](/documentation/metal/mtlcoordinate2d)
- [func MTLCoordinate2DMake(Float, Float) -> MTLCoordinate2D](/documentation/metal/mtlcoordinate2dmake(_:_:))

### Optimizing techniques

- [Specifying drawing and dispatch arguments indirectly](/documentation/metal/specifying-drawing-and-dispatch-arguments-indirectly)
- [Rendering to multiple viewports in a draw command](/documentation/metal/rendering-to-multiple-viewports-in-a-draw-command)
- [Rendering to multiple texture slices in a draw command](/documentation/metal/rendering-to-multiple-texture-slices-in-a-draw-command)

### Advanced multisampling

- [Positioning samples programmatically](/documentation/metal/positioning-samples-programmatically)
- [Storing data a pass makes with custom sample positions for a subsequent pass](/documentation/metal/storing-data-a-pass-makes-with-custom-sample-positions-for-a-subsequent-pass)

### Applying rendering techniques

- [Drawing a triangle with Metal 4](/documentation/metal/drawing-a-triangle-with-metal-4)
- [Customizing render pass setup](/documentation/metal/customizing-render-pass-setup)
- [Setting load and store actions](/documentation/metal/setting-load-and-store-actions)
- [Improving rendering performance with vertex amplification](/documentation/metal/improving-rendering-performance-with-vertex-amplification)
- [Compute passes](/documentation/metal/compute-passes)

### Essentials

- [Performing calculations on a GPU](/documentation/metal/performing-calculations-on-a-gpu)
- [Processing a texture in a compute function](/documentation/metal/processing-a-texture-in-a-compute-function)

### Encoding a compute pass

- [Creating threads and threadgroups](/documentation/metal/creating-threads-and-threadgroups)
- [Calculating threadgroup and grid sizes](/documentation/metal/calculating-threadgroup-and-grid-sizes)
- [MTL4ComputeCommandEncoder](/documentation/metal/mtl4computecommandencoder)

#### Configuring the pass

- [func setComputePipelineState(any MTLComputePipelineState)](/documentation/metal/mtl4computecommandencoder/setcomputepipelinestate(_:))
- [func setArgumentTable((any MTL4ArgumentTable)?)](/documentation/metal/mtl4computecommandencoder/setargumenttable(_:))
- [func setThreadgroupMemoryLength(Int, index: Int)](/documentation/metal/mtl4computecommandencoder/setthreadgroupmemorylength(_:index:))
- [func setImageblockSize(width: Int, height: Int)](/documentation/metal/mtl4computecommandencoder/setimageblocksize(width:height:))

#### Inspecting the pass

- [func stages() -> MTLStages](/documentation/metal/mtl4computecommandencoder/stages())

#### Running dispatch commands

- [func dispatchThreads(threadsPerGrid: MTLSize, threadsPerThreadgroup: MTLSize)](/documentation/metal/mtl4computecommandencoder/dispatchthreads(threadspergrid:threadsperthreadgroup:))
- [func dispatchThreads(indirectBuffer: MTLGPUAddress)](/documentation/metal/mtl4computecommandencoder/dispatchthreads(indirectbuffer:))
- [func dispatchThreadgroups(threadgroupsPerGrid: MTLSize, threadsPerThreadgroup: MTLSize)](/documentation/metal/mtl4computecommandencoder/dispatchthreadgroups(threadgroupspergrid:threadsperthreadgroup:))
- [func dispatchThreadgroups(indirectBuffer: MTLGPUAddress, threadsPerThreadgroup: MTLSize)](/documentation/metal/mtl4computecommandencoder/dispatchthreadgroups(indirectbuffer:threadsperthreadgroup:))

#### Encoding buffer copy commands

- [func copy(sourceBuffer: any MTLBuffer, sourceOffset: Int, destinationBuffer: any MTLBuffer, destinationOffset: Int, size: Int)](/documentation/metal/mtl4computecommandencoder/copy(sourcebuffer:sourceoffset:destinationbuffer:destinationoffset:size:))

#### Encoding buffer-to-texture copy commands

- [func copy(sourceBuffer: any MTLBuffer, sourceOffset: Int, sourceBytesPerRow: Int, sourceBytesPerImage: Int, sourceSize: MTLSize, destinationTexture: any MTLTexture, destinationSlice: Int, destinationLevel: Int, destinationOrigin: MTLOrigin, options: MTLBlitOption)](/documentation/metal/mtl4computecommandencoder/copy(sourcebuffer:sourceoffset:sourcebytesperrow:sourcebytesperimage:sourcesize:destinationtexture:destinationslice:destinationlevel:destinationorigin:options:))

#### Encoding texture copy commands

- [func copy(sourceTensor: any MTLTensor, sourceOrigin: MTLTensorExtents, sourceDimensions: MTLTensorExtents, destinationTensor: any MTLTensor, destinationOrigin: MTLTensorExtents, destinationDimensions: MTLTensorExtents)](/documentation/metal/mtl4computecommandencoder/copy(sourcetensor:sourceorigin:sourcedimensions:destinationtensor:destinationorigin:destinationdimensions:))
- [func copy(sourceTexture: any MTLTexture, destinationTexture: any MTLTexture)](/documentation/metal/mtl4computecommandencoder/copy(sourcetexture:destinationtexture:))
- [func copy(sourceTexture: any MTLTexture, sourceSlice: Int, sourceLevel: Int, destinationTexture: any MTLTexture, destinationSlice: Int, destinationLevel: Int, sliceCount: Int, levelCount: Int)](/documentation/metal/mtl4computecommandencoder/copy(sourcetexture:sourceslice:sourcelevel:destinationtexture:destinationslice:destinationlevel:slicecount:levelcount:))
- [func copy(sourceTexture: any MTLTexture, sourceSlice: Int, sourceLevel: Int, sourceOrigin: MTLOrigin, sourceSize: MTLSize, destinationTexture: any MTLTexture, destinationSlice: Int, destinationLevel: Int, destinationOrigin: MTLOrigin)](/documentation/metal/mtl4computecommandencoder/copy(sourcetexture:sourceslice:sourcelevel:sourceorigin:sourcesize:destinationtexture:destinationslice:destinationlevel:destinationorigin:))

#### Encoding texture-to-buffer copy commands

- [func copy(sourceTexture: any MTLTexture, sourceSlice: Int, sourceLevel: Int, sourceOrigin: MTLOrigin, sourceSize: MTLSize, destinationBuffer: any MTLBuffer, destinationOffset: Int, destinationBytesPerRow: Int, destinationBytesPerImage: Int, options: MTLBlitOption)](/documentation/metal/mtl4computecommandencoder/copy(sourcetexture:sourceslice:sourcelevel:sourceorigin:sourcesize:destinationbuffer:destinationoffset:destinationbytesperrow:destinationbytesperimage:options:))

#### Encoding indirect command buffer copy commands

- [func copyCommands(sourceBuffer: any MTLIndirectCommandBuffer, sourceRange: Range<Int>, destinationBuffer: any MTLIndirectCommandBuffer, destinationIndex: Int)](/documentation/metal/mtl4computecommandencoder/copycommands(sourcebuffer:sourcerange:destinationbuffer:destinationindex:))

#### Encoding buffer fill commands

- [func fill(buffer: any MTLBuffer, range: Range<Int>, value: UInt8)](/documentation/metal/mtl4computecommandencoder/fill(buffer:range:value:))

#### Encoding mipmap generation commands

- [func generateMipmaps(texture: any MTLTexture)](/documentation/metal/mtl4computecommandencoder/generatemipmaps(texture:))

#### Encoding optimization commands

- [func optimizeCommands(buffer: any MTLIndirectCommandBuffer, range: Range<Int>)](/documentation/metal/mtl4computecommandencoder/optimizecommands(buffer:range:))
- [func optimizeContents(forCPUAccess: any MTLTexture)](/documentation/metal/mtl4computecommandencoder/optimizecontents(forcpuaccess:))
- [func optimizeContents(forCPUAccess: any MTLTexture, slice: Int, level: Int)](/documentation/metal/mtl4computecommandencoder/optimizecontents(forcpuaccess:slice:level:))
- [func optimizeContents(forGPUAccess: any MTLTexture)](/documentation/metal/mtl4computecommandencoder/optimizecontents(forgpuaccess:))
- [func optimizeContents(forGPUAccess: any MTLTexture, slice: Int, level: Int)](/documentation/metal/mtl4computecommandencoder/optimizecontents(forgpuaccess:slice:level:))

#### Encoding reset commands

- [func resetCommands(buffer: any MTLIndirectCommandBuffer, range: Range<Int>)](/documentation/metal/mtl4computecommandencoder/resetcommands(buffer:range:))

#### Encoding acceleration structure build commands

- [func build(destinationAccelerationStructure: any MTLAccelerationStructure, descriptor: MTL4AccelerationStructureDescriptor, scratchBuffer: MTL4BufferRange)](/documentation/metal/mtl4computecommandencoder/build(destinationaccelerationstructure:descriptor:scratchbuffer:))

#### Encoding acceleration structure copy commands

- [func copy(sourceAccelerationStructure: any MTLAccelerationStructure, destinationAccelerationStructure: any MTLAccelerationStructure)](/documentation/metal/mtl4computecommandencoder/copy(sourceaccelerationstructure:destinationaccelerationstructure:))
- [func copyAndCompact(sourceAccelerationStructure: any MTLAccelerationStructure, destinationAccelerationStructure: any MTLAccelerationStructure)](/documentation/metal/mtl4computecommandencoder/copyandcompact(sourceaccelerationstructure:destinationaccelerationstructure:))
- [func writeCompactedSize(sourceAccelerationStructure: any MTLAccelerationStructure, destinationBuffer: MTL4BufferRange)](/documentation/metal/mtl4computecommandencoder/writecompactedsize(sourceaccelerationstructure:destinationbuffer:))

#### Encoding acceleration structure refit commands

- [func refit(sourceAccelerationStructure: any MTLAccelerationStructure, descriptor: MTL4AccelerationStructureDescriptor, destinationAccelerationStructure: (any MTLAccelerationStructure)?, scratchBuffer: MTL4BufferRange, options: MTLAccelerationStructureRefitOptions)](/documentation/metal/mtl4computecommandencoder/refit(sourceaccelerationstructure:descriptor:destinationaccelerationstructure:scratchbuffer:options:))

#### Encoding indirect command buffers

- [func executeCommands(buffer: any MTLIndirectCommandBuffer, range: Range<Int>)](/documentation/metal/mtl4computecommandencoder/executecommands(buffer:range:))
- [func executeCommands(buffer: any MTLIndirectCommandBuffer, indirectBuffer: MTLGPUAddress)](/documentation/metal/mtl4computecommandencoder/executecommands(buffer:indirectbuffer:))

#### Encoding performance measurement commands

- [func writeTimestamp(granularity: MTL4TimestampGranularity, counterHeap: any MTL4CounterHeap, index: Int)](/documentation/metal/mtl4computecommandencoder/writetimestamp(granularity:counterheap:index:))
- [MTLComputeCommandEncoder](/documentation/metal/mtlcomputecommandencoder)

#### Configuring the pipeline state

- [func setComputePipelineState(any MTLComputePipelineState)](/documentation/metal/mtlcomputecommandencoder/setcomputepipelinestate(_:))
- [var dispatchType: MTLDispatchType](/documentation/metal/mtlcomputecommandencoder/dispatchtype)

#### Binding buffers

- [func setBuffer((any MTLBuffer)?, offset: Int, index: Int)](/documentation/metal/mtlcomputecommandencoder/setbuffer(_:offset:index:))
- [func setBuffer(any MTLBuffer, offset: Int, attributeStride: Int, index: Int)](/documentation/metal/mtlcomputecommandencoder/setbuffer(_:offset:attributestride:index:))
- [- setBuffers:offsets:withRange:](/documentation/metal/mtlcomputecommandencoder/setbuffers(_:offsets:range:))
- [- setBuffers:offsets:attributeStrides:withRange:](/documentation/metal/mtlcomputecommandencoder/setbuffers(_:offsets:attributestrides:range:))
- [func setBufferOffset(Int, index: Int)](/documentation/metal/mtlcomputecommandencoder/setbufferoffset(_:index:))
- [func setBufferOffset(offset: Int, attributeStride: Int, index: Int)](/documentation/metal/mtlcomputecommandencoder/setbufferoffset(offset:attributestride:index:))

#### Binding raw bytes

- [func setBytes(UnsafeRawPointer, length: Int, index: Int)](/documentation/metal/mtlcomputecommandencoder/setbytes(_:length:index:))
- [func setBytes(UnsafeRawPointer, length: Int, attributeStride: Int, index: Int)](/documentation/metal/mtlcomputecommandencoder/setbytes(_:length:attributestride:index:))

#### Binding textures

- [func setTexture((any MTLTexture)?, index: Int)](/documentation/metal/mtlcomputecommandencoder/settexture(_:index:))
- [- setTextures:withRange:](/documentation/metal/mtlcomputecommandencoder/settextures(_:range:))

#### Binding texture samplers

- [func setSamplerState((any MTLSamplerState)?, index: Int)](/documentation/metal/mtlcomputecommandencoder/setsamplerstate(_:index:))
- [func setSamplerState((any MTLSamplerState)?, lodMinClamp: Float, lodMaxClamp: Float, index: Int)](/documentation/metal/mtlcomputecommandencoder/setsamplerstate(_:lodminclamp:lodmaxclamp:index:))
- [- setSamplerStates:withRange:](/documentation/metal/mtlcomputecommandencoder/setsamplerstates(_:range:))
- [- setSamplerStates:lodMinClamps:lodMaxClamps:withRange:](/documentation/metal/mtlcomputecommandencoder/setsamplerstates(_:lodminclamps:lodmaxclamps:range:))

#### Binding function tables

- [func setVisibleFunctionTable((any MTLVisibleFunctionTable)?, bufferIndex: Int)](/documentation/metal/mtlcomputecommandencoder/setvisiblefunctiontable(_:bufferindex:))
- [- setVisibleFunctionTables:withBufferRange:](/documentation/metal/mtlcomputecommandencoder/setvisiblefunctiontables(_:bufferrange:))
- [- setIntersectionFunctionTables:withBufferRange:](/documentation/metal/mtlcomputecommandencoder/setintersectionfunctiontables(_:bufferrange:))

#### Binding arguments for acceleration structures

- [func setAccelerationStructure((any MTLAccelerationStructure)?, bufferIndex: Int)](/documentation/metal/mtlcomputecommandencoder/setaccelerationstructure(_:bufferindex:))
- [func setIntersectionFunctionTable((any MTLIntersectionFunctionTable)?, bufferIndex: Int)](/documentation/metal/mtlcomputecommandencoder/setintersectionfunctiontable(_:bufferindex:))

#### Making indirect resources resident

- [func useResource(any MTLResource, usage: MTLResourceUsage)](/documentation/metal/mtlcomputecommandencoder/useresource(_:usage:))
- [- useResources:count:usage:](/documentation/metal/mtlcomputecommandencoder/useresources(_:usage:))
- [func useHeap(any MTLHeap)](/documentation/metal/mtlcomputecommandencoder/useheap(_:))
- [- useHeaps:count:](/documentation/metal/mtlcomputecommandencoder/useheaps(_:))

#### Configuring tile memory

- [func setThreadgroupMemoryLength(Int, index: Int)](/documentation/metal/mtlcomputecommandencoder/setthreadgroupmemorylength(_:index:))
- [func setImageblockWidth(Int, height: Int)](/documentation/metal/mtlcomputecommandencoder/setimageblockwidth(_:height:))

#### Configuring stage-in data

- [func setStageInRegion(MTLRegion)](/documentation/metal/mtlcomputecommandencoder/setstageinregion(_:))
- [func setStageInRegionWithIndirectBuffer(any MTLBuffer, indirectBufferOffset: Int)](/documentation/metal/mtlcomputecommandencoder/setstageinregionwithindirectbuffer(_:indirectbufferoffset:))

#### Dispatching kernel calls directly

- [func dispatchThreads(MTLSize, threadsPerThreadgroup: MTLSize)](/documentation/metal/mtlcomputecommandencoder/dispatchthreads(_:threadsperthreadgroup:))
- [func dispatchThreadgroups(MTLSize, threadsPerThreadgroup: MTLSize)](/documentation/metal/mtlcomputecommandencoder/dispatchthreadgroups(_:threadsperthreadgroup:))

#### Dispatching from indirect command buffers

- [func dispatchThreadgroups(indirectBuffer: any MTLBuffer, indirectBufferOffset: Int, threadsPerThreadgroup: MTLSize)](/documentation/metal/mtlcomputecommandencoder/dispatchthreadgroups(indirectbuffer:indirectbufferoffset:threadsperthreadgroup:))
- [- executeCommandsInBuffer:withRange:](/documentation/metal/mtlcomputecommandencoder/executecommandsinbuffer(_:range:))
- [- executeCommandsInBuffer:indirectBuffer:indirectBufferOffset:](/documentation/metal/mtlcomputecommandencoder/executecommandsinbuffer(_:indirectbuffer:offset:))
- [func executeCommands(in: any MTLIndirectCommandBuffer, indirectBuffer: any MTLBuffer, indirectBufferOffset: Int)](/documentation/metal/mtlcomputecommandencoder/executecommands(in:indirectbuffer:indirectbufferoffset:))
- [func executeCommands(in: any MTLIndirectCommandBuffer, with: NSRange)](/documentation/metal/mtlcomputecommandencoder/executecommands(in:with:))

#### Preventing resource access conflicts

- [func waitForFence(any MTLFence)](/documentation/metal/mtlcomputecommandencoder/waitforfence(_:))
- [func updateFence(any MTLFence)](/documentation/metal/mtlcomputecommandencoder/updatefence(_:))
- [func memoryBarrier(scope: MTLBarrierScope)](/documentation/metal/mtlcomputecommandencoder/memorybarrier(scope:))
- [func memoryBarrier(resources: [any MTLResource])](/documentation/metal/mtlcomputecommandencoder/memorybarrier(resources:))

#### Sampling counters

- [func sampleCounters(sampleBuffer: any MTLCounterSampleBuffer, sampleIndex: Int, barrier: Bool)](/documentation/metal/mtlcomputecommandencoder/samplecounters(samplebuffer:sampleindex:barrier:))

### Configuring a compute pipeline state

- [MTL4ComputePipelineDescriptor](/documentation/metal/mtl4computepipelinedescriptor)

#### Instance Properties

- [var computeFunctionDescriptor: MTL4FunctionDescriptor?](/documentation/metal/mtl4computepipelinedescriptor/computefunctiondescriptor)
- [var maxTotalThreadsPerThreadgroup: Int](/documentation/metal/mtl4computepipelinedescriptor/maxtotalthreadsperthreadgroup)
- [var requiredThreadsPerThreadgroup: MTLSize](/documentation/metal/mtl4computepipelinedescriptor/requiredthreadsperthreadgroup)
- [var staticLinkingDescriptor: MTL4StaticLinkingDescriptor?](/documentation/metal/mtl4computepipelinedescriptor/staticlinkingdescriptor)
- [var supportBinaryLinking: Bool](/documentation/metal/mtl4computepipelinedescriptor/supportbinarylinking)
- [var supportIndirectCommandBuffers: MTL4IndirectCommandBufferSupportState](/documentation/metal/mtl4computepipelinedescriptor/supportindirectcommandbuffers)
- [var threadGroupSizeIsMultipleOfThreadExecutionWidth: Bool](/documentation/metal/mtl4computepipelinedescriptor/threadgroupsizeismultipleofthreadexecutionwidth)

#### Instance Methods

- [func reset()](/documentation/metal/mtl4computepipelinedescriptor/reset())
- [MTLComputePipelineDescriptor](/documentation/metal/mtlcomputepipelinedescriptor)

#### Configuring the compute execution environment

- [var computeFunction: (any MTLFunction)?](/documentation/metal/mtlcomputepipelinedescriptor/computefunction)
- [var threadGroupSizeIsMultipleOfThreadExecutionWidth: Bool](/documentation/metal/mtlcomputepipelinedescriptor/threadgroupsizeismultipleofthreadexecutionwidth)
- [var maxTotalThreadsPerThreadgroup: Int](/documentation/metal/mtlcomputepipelinedescriptor/maxtotalthreadsperthreadgroup)
- [var maxCallStackDepth: Int](/documentation/metal/mtlcomputepipelinedescriptor/maxcallstackdepth)

#### Configuring compute pass inputs

- [var stageInputDescriptor: MTLStageInputOutputDescriptor?](/documentation/metal/mtlcomputepipelinedescriptor/stageinputdescriptor)
- [MTLAttributeDescriptor](/documentation/metal/mtlattributedescriptor)

##### Defining attribute location

- [var bufferIndex: Int](/documentation/metal/mtlattributedescriptor/bufferindex)
- [var offset: Int](/documentation/metal/mtlattributedescriptor/offset)
- [var format: MTLAttributeFormat](/documentation/metal/mtlattributedescriptor/format)
- [MTLAttributeFormat](/documentation/metal/mtlattributeformat)

###### Invalid format

- [case invalid](/documentation/metal/mtlattributeformat/invalid)

###### Character data formats

- [case uchar](/documentation/metal/mtlattributeformat/uchar)
- [case uchar2](/documentation/metal/mtlattributeformat/uchar2)
- [case uchar3](/documentation/metal/mtlattributeformat/uchar3)
- [case uchar4](/documentation/metal/mtlattributeformat/uchar4)
- [case char](/documentation/metal/mtlattributeformat/char)
- [case char2](/documentation/metal/mtlattributeformat/char2)
- [case char3](/documentation/metal/mtlattributeformat/char3)
- [case char4](/documentation/metal/mtlattributeformat/char4)
- [case ucharNormalized](/documentation/metal/mtlattributeformat/ucharnormalized)
- [case uchar2Normalized](/documentation/metal/mtlattributeformat/uchar2normalized)
- [case uchar3Normalized](/documentation/metal/mtlattributeformat/uchar3normalized)
- [case uchar4Normalized](/documentation/metal/mtlattributeformat/uchar4normalized)
- [case charNormalized](/documentation/metal/mtlattributeformat/charnormalized)
- [case char2Normalized](/documentation/metal/mtlattributeformat/char2normalized)
- [case char3Normalized](/documentation/metal/mtlattributeformat/char3normalized)
- [case char4Normalized](/documentation/metal/mtlattributeformat/char4normalized)

###### 16-bit integer data formats

- [case ushort](/documentation/metal/mtlattributeformat/ushort)
- [case ushort2](/documentation/metal/mtlattributeformat/ushort2)
- [case ushort3](/documentation/metal/mtlattributeformat/ushort3)
- [case ushort4](/documentation/metal/mtlattributeformat/ushort4)
- [case short](/documentation/metal/mtlattributeformat/short)
- [case short2](/documentation/metal/mtlattributeformat/short2)
- [case short3](/documentation/metal/mtlattributeformat/short3)
- [case short4](/documentation/metal/mtlattributeformat/short4)
- [case ushortNormalized](/documentation/metal/mtlattributeformat/ushortnormalized)
- [case ushort2Normalized](/documentation/metal/mtlattributeformat/ushort2normalized)
- [case ushort3Normalized](/documentation/metal/mtlattributeformat/ushort3normalized)
- [case ushort4Normalized](/documentation/metal/mtlattributeformat/ushort4normalized)
- [case shortNormalized](/documentation/metal/mtlattributeformat/shortnormalized)
- [case short2Normalized](/documentation/metal/mtlattributeformat/short2normalized)
- [case short3Normalized](/documentation/metal/mtlattributeformat/short3normalized)
- [case short4Normalized](/documentation/metal/mtlattributeformat/short4normalized)

###### 32-bit integer data formats

- [case uint](/documentation/metal/mtlattributeformat/uint)
- [case uint2](/documentation/metal/mtlattributeformat/uint2)
- [case uint3](/documentation/metal/mtlattributeformat/uint3)
- [case uint4](/documentation/metal/mtlattributeformat/uint4)
- [case int](/documentation/metal/mtlattributeformat/int)
- [case int2](/documentation/metal/mtlattributeformat/int2)
- [case int3](/documentation/metal/mtlattributeformat/int3)
- [case int4](/documentation/metal/mtlattributeformat/int4)
- [case int1010102Normalized](/documentation/metal/mtlattributeformat/int1010102normalized)
- [case uint1010102Normalized](/documentation/metal/mtlattributeformat/uint1010102normalized)

###### 16-bit floating point formats

- [case half](/documentation/metal/mtlattributeformat/half)
- [case half2](/documentation/metal/mtlattributeformat/half2)
- [case half3](/documentation/metal/mtlattributeformat/half3)
- [case half4](/documentation/metal/mtlattributeformat/half4)

###### 32-bit floating point formats

- [case float](/documentation/metal/mtlattributeformat/float)
- [case float2](/documentation/metal/mtlattributeformat/float2)
- [case float3](/documentation/metal/mtlattributeformat/float3)
- [case float4](/documentation/metal/mtlattributeformat/float4)

###### Pixel data types

- [case uchar4Normalized_bgra](/documentation/metal/mtlattributeformat/uchar4normalized_bgra)
- [case floatRG11B10](/documentation/metal/mtlattributeformat/floatrg11b10)
- [case floatRGB9E5](/documentation/metal/mtlattributeformat/floatrgb9e5)

###### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlattributeformat/init(rawvalue:))
- [MTLAttributeDescriptorArray](/documentation/metal/mtlattributedescriptorarray)

##### Accessing attribute state objects

- [subscript(Int) -> MTLAttributeDescriptor!](/documentation/metal/mtlattributedescriptorarray/subscript(_:))
- [MTLBufferLayoutDescriptor](/documentation/metal/mtlbufferlayoutdescriptor)

##### Describing fetch behavior

- [var stride: Int](/documentation/metal/mtlbufferlayoutdescriptor/stride)
- [var stepFunction: MTLStepFunction](/documentation/metal/mtlbufferlayoutdescriptor/stepfunction)
- [var stepRate: Int](/documentation/metal/mtlbufferlayoutdescriptor/steprate)
- [MTLStepFunction](/documentation/metal/mtlstepfunction)

###### Step options

- [case constant](/documentation/metal/mtlstepfunction/constant)
- [case perInstance](/documentation/metal/mtlstepfunction/perinstance)
- [case perPatch](/documentation/metal/mtlstepfunction/perpatch)
- [case perPatchControlPoint](/documentation/metal/mtlstepfunction/perpatchcontrolpoint)
- [case perVertex](/documentation/metal/mtlstepfunction/pervertex)
- [case threadPositionInGridX](/documentation/metal/mtlstepfunction/threadpositioningridx)
- [case threadPositionInGridY](/documentation/metal/mtlstepfunction/threadpositioningridy)
- [case threadPositionInGridXIndexed](/documentation/metal/mtlstepfunction/threadpositioningridxindexed)
- [case threadPositionInGridYIndexed](/documentation/metal/mtlstepfunction/threadpositioningridyindexed)

###### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlstepfunction/init(rawvalue:))
- [MTLBufferLayoutDescriptorArray](/documentation/metal/mtlbufferlayoutdescriptorarray)

##### Array accessors

- [subscript(Int) -> MTLBufferLayoutDescriptor!](/documentation/metal/mtlbufferlayoutdescriptorarray/subscript(_:))

#### Configuring buffer mutability

- [var buffers: MTLPipelineBufferDescriptorArray](/documentation/metal/mtlcomputepipelinedescriptor/buffers)

#### Identifying the pipeline state object

- [var label: String?](/documentation/metal/mtlcomputepipelinedescriptor/label)

#### Configuring indirect command buffers

- [var supportIndirectCommandBuffers: Bool](/documentation/metal/mtlcomputepipelinedescriptor/supportindirectcommandbuffers)

#### Configuring shader validation

- [var shaderValidation: MTLShaderValidation](/documentation/metal/mtlcomputepipelinedescriptor/shadervalidation)

#### Reset to defaults

- [func reset()](/documentation/metal/mtlcomputepipelinedescriptor/reset())

#### Loading dynamic libraries to link at runtime

- [var preloadedLibraries: [any MTLDynamicLibrary]](/documentation/metal/mtlcomputepipelinedescriptor/preloadedlibraries)
- [var insertLibraries: [any MTLDynamicLibrary]?](/documentation/metal/mtlcomputepipelinedescriptor/insertlibraries)

#### Setting callable functions

- [var linkedFunctions: MTLLinkedFunctions?](/documentation/metal/mtlcomputepipelinedescriptor/linkedfunctions)

#### Loading binary archives

- [var supportAddingBinaryFunctions: Bool](/documentation/metal/mtlcomputepipelinedescriptor/supportaddingbinaryfunctions)
- [var binaryArchives: [any MTLBinaryArchive]?](/documentation/metal/mtlcomputepipelinedescriptor/binaryarchives)

#### Instance Properties

- [var requiredThreadsPerThreadgroup: MTLSize](/documentation/metal/mtlcomputepipelinedescriptor/requiredthreadsperthreadgroup)
- [MTLComputePipelineState](/documentation/metal/mtlcomputepipelinestate)

#### Identifying a pipeline state

- [var device: any MTLDevice](/documentation/metal/mtlcomputepipelinestate/device)
- [var gpuResourceID: MTLResourceID](/documentation/metal/mtlcomputepipelinestate/gpuresourceid)
- [var label: String?](/documentation/metal/mtlcomputepipelinestate/label)

#### Checking threadgroup attributes

- [var maxTotalThreadsPerThreadgroup: Int](/documentation/metal/mtlcomputepipelinestate/maxtotalthreadsperthreadgroup)
- [var threadExecutionWidth: Int](/documentation/metal/mtlcomputepipelinestate/threadexecutionwidth)
- [var staticThreadgroupMemoryLength: Int](/documentation/metal/mtlcomputepipelinestate/staticthreadgroupmemorylength)

#### Checking imageblock attributes

- [func imageblockMemoryLength(forDimensions: MTLSize) -> Int](/documentation/metal/mtlcomputepipelinestate/imageblockmemorylength(fordimensions:))

#### Checking indirect command buffer support

- [var supportIndirectCommandBuffers: Bool](/documentation/metal/mtlcomputepipelinestate/supportindirectcommandbuffers)

#### Checking shader validation

- [var shaderValidation: MTLShaderValidation](/documentation/metal/mtlcomputepipelinestate/shadervalidation)

#### Creating function handles

- [func functionHandle(function: any MTLFunction) -> (any MTLFunctionHandle)?](/documentation/metal/mtlcomputepipelinestate/functionhandle(function:)-7d523)

#### Adding visible functions

- [func makeComputePipelineStateWithAdditionalBinaryFunctions(functions: [any MTLFunction]) throws -> any MTLComputePipelineState](/documentation/metal/mtlcomputepipelinestate/makecomputepipelinestatewithadditionalbinaryfunctions(functions:))

#### Creating function tables

- [func makeVisibleFunctionTable(descriptor: MTLVisibleFunctionTableDescriptor) -> (any MTLVisibleFunctionTable)?](/documentation/metal/mtlcomputepipelinestate/makevisiblefunctiontable(descriptor:))
- [func makeIntersectionFunctionTable(descriptor: MTLIntersectionFunctionTableDescriptor) -> (any MTLIntersectionFunctionTable)?](/documentation/metal/mtlcomputepipelinestate/makeintersectionfunctiontable(descriptor:))

#### Instance Properties

- [var reflection: MTLComputePipelineReflection?](/documentation/metal/mtlcomputepipelinestate/reflection)
- [var requiredThreadsPerThreadgroup: MTLSize](/documentation/metal/mtlcomputepipelinestate/requiredthreadsperthreadgroup)

#### Instance Methods

- [func functionHandle(function: any MTL4BinaryFunction) -> (any MTLFunctionHandle)?](/documentation/metal/mtlcomputepipelinestate/functionhandle(function:)-8spaa)
- [func functionHandle(withName: String) -> (any MTLFunctionHandle)?](/documentation/metal/mtlcomputepipelinestate/functionhandle(withname:))
- [func makeComputePipelineState(additionalBinaryFunctions: [any MTL4BinaryFunction]) throws -> any MTLComputePipelineState](/documentation/metal/mtlcomputepipelinestate/makecomputepipelinestate(additionalbinaryfunctions:))
- [MTLStageInputOutputDescriptor](/documentation/metal/mtlstageinputoutputdescriptor)

#### Describing argument layouts

- [var attributes: MTLAttributeDescriptorArray](/documentation/metal/mtlstageinputoutputdescriptor/attributes)
- [var layouts: MTLBufferLayoutDescriptorArray](/documentation/metal/mtlstageinputoutputdescriptor/layouts)

#### Declaring index buffers for indirect compute commands

- [var indexBufferIndex: Int](/documentation/metal/mtlstageinputoutputdescriptor/indexbufferindex)
- [var indexType: MTLIndexType](/documentation/metal/mtlstageinputoutputdescriptor/indextype)

#### Resetting the descriptor

- [func reset()](/documentation/metal/mtlstageinputoutputdescriptor/reset())
- [MTLPipelineBufferDescriptor](/documentation/metal/mtlpipelinebufferdescriptor)

#### Setting buffer mutability

- [var mutability: MTLMutability](/documentation/metal/mtlpipelinebufferdescriptor/mutability)
- [MTLMutability](/documentation/metal/mtlmutability)

##### Enumeration cases

- [case `default`](/documentation/metal/mtlmutability/default)
- [case mutable](/documentation/metal/mtlmutability/mutable)
- [case immutable](/documentation/metal/mtlmutability/immutable)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlmutability/init(rawvalue:))
- [MTLPipelineBufferDescriptorArray](/documentation/metal/mtlpipelinebufferdescriptorarray)

#### Accessing array elements

- [subscript(Int) -> MTLPipelineBufferDescriptor!](/documentation/metal/mtlpipelinebufferdescriptorarray/subscript(_:))
- [MTLPipelineOption](/documentation/metal/mtlpipelineoption)

#### Retrieving argument information

- [static var bufferTypeInfo: MTLPipelineOption](/documentation/metal/mtlpipelineoption/buffertypeinfo)
- [static var failOnBinaryArchiveMiss: MTLPipelineOption](/documentation/metal/mtlpipelineoption/failonbinaryarchivemiss)
- [static var argumentInfo: MTLPipelineOption](/documentation/metal/mtlpipelineoption/argumentinfo)

#### Creating compilation options

- [init(rawValue: UInt)](/documentation/metal/mtlpipelineoption/init(rawvalue:))

#### Type properties

- [static var bindingInfo: MTLPipelineOption](/documentation/metal/mtlpipelineoption/bindinginfo)

### Configuring a compute pass

- [MTLComputePassDescriptor](/documentation/metal/mtlcomputepassdescriptor)

#### Configuring the dispatch mechanism

- [var dispatchType: MTLDispatchType](/documentation/metal/mtlcomputepassdescriptor/dispatchtype)

#### Specifying sample buffers for GPU counters

- [var sampleBufferAttachments: MTLComputePassSampleBufferAttachmentDescriptorArray](/documentation/metal/mtlcomputepassdescriptor/samplebufferattachments)
- [MTLDispatchType](/documentation/metal/mtldispatchtype)

#### Execution dispatch types

- [case concurrent](/documentation/metal/mtldispatchtype/concurrent)
- [case serial](/documentation/metal/mtldispatchtype/serial)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtldispatchtype/init(rawvalue:))
- [MTLDispatchThreadgroupsIndirectArguments](/documentation/metal/mtldispatchthreadgroupsindirectarguments)

#### Specifying the size of the threadgroup

- [init()](/documentation/metal/mtldispatchthreadgroupsindirectarguments/init())
- [init(threadgroupsPerGrid: (UInt32, UInt32, UInt32))](/documentation/metal/mtldispatchthreadgroupsindirectarguments/init(threadgroupspergrid:))
- [var threadgroupsPerGrid: (UInt32, UInt32, UInt32)](/documentation/metal/mtldispatchthreadgroupsindirectarguments/threadgroupspergrid)
- [MTLComputePassSampleBufferAttachmentDescriptor](/documentation/metal/mtlcomputepasssamplebufferattachmentdescriptor)

#### Configuring the sample buffer attachment

- [var sampleBuffer: (any MTLCounterSampleBuffer)?](/documentation/metal/mtlcomputepasssamplebufferattachmentdescriptor/samplebuffer)
- [var startOfEncoderSampleIndex: Int](/documentation/metal/mtlcomputepasssamplebufferattachmentdescriptor/startofencodersampleindex)
- [var endOfEncoderSampleIndex: Int](/documentation/metal/mtlcomputepasssamplebufferattachmentdescriptor/endofencodersampleindex)
- [MTLComputePassSampleBufferAttachmentDescriptorArray](/documentation/metal/mtlcomputepasssamplebufferattachmentdescriptorarray)

#### Accessing a sample buffer attachment

- [subscript(Int) -> MTLComputePassSampleBufferAttachmentDescriptor!](/documentation/metal/mtlcomputepasssamplebufferattachmentdescriptorarray/subscript(_:))
- [Machine-learning passes](/documentation/metal/machine-learning-passes)

### Encoding a machine-learning pass

- [MTL4MachineLearningCommandEncoder](/documentation/metal/mtl4machinelearningcommandencoder)

#### Configuring the pass

- [func setPipelineState(any MTL4MachineLearningPipelineState)](/documentation/metal/mtl4machinelearningcommandencoder/setpipelinestate(_:))
- [func setArgumentTable(any MTL4ArgumentTable)](/documentation/metal/mtl4machinelearningcommandencoder/setargumenttable(_:))

#### Running machine learning networks

- [func dispatchNetwork(intermediatesHeap: any MTLHeap)](/documentation/metal/mtl4machinelearningcommandencoder/dispatchnetwork(intermediatesheap:))
- [MTL4MachineLearningPipelineState](/documentation/metal/mtl4machinelearningpipelinestate)

#### Instance Properties

- [var device: any MTLDevice](/documentation/metal/mtl4machinelearningpipelinestate/device)
- [var intermediatesHeapSize: Int](/documentation/metal/mtl4machinelearningpipelinestate/intermediatesheapsize)
- [var label: String?](/documentation/metal/mtl4machinelearningpipelinestate/label)
- [var reflection: MTL4MachineLearningPipelineReflection?](/documentation/metal/mtl4machinelearningpipelinestate/reflection)

### Configuring a machine-learning pipeline

- [MTL4MachineLearningPipelineDescriptor](/documentation/metal/mtl4machinelearningpipelinedescriptor)

#### Instance Properties

- [var label: String?](/documentation/metal/mtl4machinelearningpipelinedescriptor/label)
- [var machineLearningFunctionDescriptor: MTL4FunctionDescriptor?](/documentation/metal/mtl4machinelearningpipelinedescriptor/machinelearningfunctiondescriptor)

#### Instance Methods

- [func inputDimensions(bufferIndex: Int) -> MTLTensorExtents?](/documentation/metal/mtl4machinelearningpipelinedescriptor/inputdimensions(bufferindex:))
- [func reset()](/documentation/metal/mtl4machinelearningpipelinedescriptor/reset())
- [func setInputDimensions(MTLTensorExtents?, bufferIndex: Int)](/documentation/metal/mtl4machinelearningpipelinedescriptor/setinputdimensions(_:bufferindex:)-34gir)
- [func setInputDimensions([MTLTensorExtents], bufferIndex: Int)](/documentation/metal/mtl4machinelearningpipelinedescriptor/setinputdimensions(_:bufferindex:)-8fnq7)
- [MTL4MachineLearningPipelineReflection](/documentation/metal/mtl4machinelearningpipelinereflection)

#### Instance Properties

- [var bindings: [any MTLBinding]](/documentation/metal/mtl4machinelearningpipelinereflection/bindings)
- [Blit passes](/documentation/metal/blit-passes)

### Encoding a blit pass

- [MTLBlitCommandEncoder](/documentation/metal/mtlblitcommandencoder)

#### Filling buffers

- [- fillBuffer:range:value:](/documentation/metal/mtlblitcommandencoder/fill(buffer:range:value:))

#### Generating texture mipmaps

- [func generateMipmaps(for: any MTLTexture)](/documentation/metal/mtlblitcommandencoder/generatemipmaps(for:))

#### Copying buffer data to another buffer

- [func copy(from: any MTLBuffer, sourceOffset: Int, to: any MTLBuffer, destinationOffset: Int, size: Int)](/documentation/metal/mtlblitcommandencoder/copy(from:sourceoffset:to:destinationoffset:size:))

#### Copying texture data to another texture

- [func copy(from: any MTLTexture, to: any MTLTexture)](/documentation/metal/mtlblitcommandencoder/copy(from:to:))
- [func copy(from: any MTLTexture, sourceSlice: Int, sourceLevel: Int, to: any MTLTexture, destinationSlice: Int, destinationLevel: Int, sliceCount: Int, levelCount: Int)](/documentation/metal/mtlblitcommandencoder/copy(from:sourceslice:sourcelevel:to:destinationslice:destinationlevel:slicecount:levelcount:))
- [func copy(from: any MTLTexture, sourceSlice: Int, sourceLevel: Int, sourceOrigin: MTLOrigin, sourceSize: MTLSize, to: any MTLTexture, destinationSlice: Int, destinationLevel: Int, destinationOrigin: MTLOrigin)](/documentation/metal/mtlblitcommandencoder/copy(from:sourceslice:sourcelevel:sourceorigin:sourcesize:to:destinationslice:destinationlevel:destinationorigin:))
- [func copy(from: any MTLTensor, sourceOrigin: MTLTensorExtents, sourceDimensions: MTLTensorExtents, to: any MTLTensor, destinationOrigin: MTLTensorExtents, destinationDimensions: MTLTensorExtents)](/documentation/metal/mtlblitcommandencoder/copy(from:sourceorigin:sourcedimensions:to:destinationorigin:destinationdimensions:))

#### Copying buffer data to a texture

- [func copy(from: any MTLBuffer, sourceOffset: Int, sourceBytesPerRow: Int, sourceBytesPerImage: Int, sourceSize: MTLSize, to: any MTLTexture, destinationSlice: Int, destinationLevel: Int, destinationOrigin: MTLOrigin)](/documentation/metal/mtlblitcommandencoder/copy(from:sourceoffset:sourcebytesperrow:sourcebytesperimage:sourcesize:to:destinationslice:destinationlevel:destinationorigin:))
- [func copy(from: any MTLBuffer, sourceOffset: Int, sourceBytesPerRow: Int, sourceBytesPerImage: Int, sourceSize: MTLSize, to: any MTLTexture, destinationSlice: Int, destinationLevel: Int, destinationOrigin: MTLOrigin, options: MTLBlitOption)](/documentation/metal/mtlblitcommandencoder/copy(from:sourceoffset:sourcebytesperrow:sourcebytesperimage:sourcesize:to:destinationslice:destinationlevel:destinationorigin:options:))

#### Copying texture data to a buffer

- [func copy(from: any MTLTexture, sourceSlice: Int, sourceLevel: Int, sourceOrigin: MTLOrigin, sourceSize: MTLSize, to: any MTLBuffer, destinationOffset: Int, destinationBytesPerRow: Int, destinationBytesPerImage: Int)](/documentation/metal/mtlblitcommandencoder/copy(from:sourceslice:sourcelevel:sourceorigin:sourcesize:to:destinationoffset:destinationbytesperrow:destinationbytesperimage:))
- [func copy(from: any MTLTexture, sourceSlice: Int, sourceLevel: Int, sourceOrigin: MTLOrigin, sourceSize: MTLSize, to: any MTLBuffer, destinationOffset: Int, destinationBytesPerRow: Int, destinationBytesPerImage: Int, options: MTLBlitOption)](/documentation/metal/mtlblitcommandencoder/copy(from:sourceslice:sourcelevel:sourceorigin:sourcesize:to:destinationoffset:destinationbytesperrow:destinationbytesperimage:options:))

#### Optimizing textures for GPU access

- [func optimizeContentsForGPUAccess(texture: any MTLTexture)](/documentation/metal/mtlblitcommandencoder/optimizecontentsforgpuaccess(texture:))
- [func optimizeContentsForGPUAccess(texture: any MTLTexture, slice: Int, level: Int)](/documentation/metal/mtlblitcommandencoder/optimizecontentsforgpuaccess(texture:slice:level:))

#### Optimizing textures for CPU access

- [func optimizeContentsForCPUAccess(texture: any MTLTexture)](/documentation/metal/mtlblitcommandencoder/optimizecontentsforcpuaccess(texture:))
- [func optimizeContentsForCPUAccess(texture: any MTLTexture, slice: Int, level: Int)](/documentation/metal/mtlblitcommandencoder/optimizecontentsforcpuaccess(texture:slice:level:))

#### Synchronizing managed resources

- [func synchronize(resource: any MTLResource)](/documentation/metal/mtlblitcommandencoder/synchronize(resource:))
- [func synchronize(texture: any MTLTexture, slice: Int, level: Int)](/documentation/metal/mtlblitcommandencoder/synchronize(texture:slice:level:))

#### Preventing resource access conflicts

- [func waitForFence(any MTLFence)](/documentation/metal/mtlblitcommandencoder/waitforfence(_:))
- [func updateFence(any MTLFence)](/documentation/metal/mtlblitcommandencoder/updatefence(_:))

#### Managing indirect command buffers

- [- copyIndirectCommandBuffer:sourceRange:destination:destinationIndex:](/documentation/metal/mtlblitcommandencoder/copyindirectcommandbuffer(_:sourcerange:destination:destinationindex:))
- [- resetCommandsInBuffer:withRange:](/documentation/metal/mtlblitcommandencoder/resetcommandsinbuffer(_:range:))
- [- optimizeIndirectCommandBuffer:withRange:](/documentation/metal/mtlblitcommandencoder/optimizeindirectcommandbuffer(_:range:))

#### Sampling counters

- [func sampleCounters(sampleBuffer: any MTLCounterSampleBuffer, sampleIndex: Int, barrier: Bool)](/documentation/metal/mtlblitcommandencoder/samplecounters(samplebuffer:sampleindex:barrier:))
- [- resolveCounters:inRange:destinationBuffer:destinationOffset:](/documentation/metal/mtlblitcommandencoder/resolvecounters(_:range:destinationbuffer:destinationoffset:))

#### Managing sparse texture access counters

- [func getTextureAccessCounters(any MTLTexture, region: MTLRegion, mipLevel: Int, slice: Int, resetCounters: Bool, countersBuffer: any MTLBuffer, countersBufferOffset: Int)](/documentation/metal/mtlblitcommandencoder/gettextureaccesscounters(_:region:miplevel:slice:resetcounters:countersbuffer:countersbufferoffset:))
- [func resetTextureAccessCounters(any MTLTexture, region: MTLRegion, mipLevel: Int, slice: Int)](/documentation/metal/mtlblitcommandencoder/resettextureaccesscounters(_:region:miplevel:slice:))
- [MTLBlitOption](/documentation/metal/mtlblitoption)

#### Depth and stencil buffer options

- [static var depthFromDepthStencil: MTLBlitOption](/documentation/metal/mtlblitoption/depthfromdepthstencil)
- [static var stencilFromDepthStencil: MTLBlitOption](/documentation/metal/mtlblitoption/stencilfromdepthstencil)

#### Texture compression options

- [static var rowLinearPVRTC: MTLBlitOption](/documentation/metal/mtlblitoption/rowlinearpvrtc)

#### Swift support

- [init(rawValue: UInt)](/documentation/metal/mtlblitoption/init(rawvalue:))

### Configuring a blit command encoder

- [MTLBlitPassDescriptor](/documentation/metal/mtlblitpassdescriptor)

#### Configuring sample buffer attachment descriptors for a blit pass

- [var sampleBufferAttachments: MTLBlitPassSampleBufferAttachmentDescriptorArray](/documentation/metal/mtlblitpassdescriptor/samplebufferattachments)
- [MTLBlitPassSampleBufferAttachmentDescriptor](/documentation/metal/mtlblitpasssamplebufferattachmentdescriptor)

#### Configuring the sample buffer attachment

- [var sampleBuffer: (any MTLCounterSampleBuffer)?](/documentation/metal/mtlblitpasssamplebufferattachmentdescriptor/samplebuffer)
- [var startOfEncoderSampleIndex: Int](/documentation/metal/mtlblitpasssamplebufferattachmentdescriptor/startofencodersampleindex)
- [var endOfEncoderSampleIndex: Int](/documentation/metal/mtlblitpasssamplebufferattachmentdescriptor/endofencodersampleindex)
- [MTLBlitPassSampleBufferAttachmentDescriptorArray](/documentation/metal/mtlblitpasssamplebufferattachmentdescriptorarray)

#### Accessing a sample buffer attachment descriptor

- [subscript(Int) -> MTLBlitPassSampleBufferAttachmentDescriptor!](/documentation/metal/mtlblitpasssamplebufferattachmentdescriptorarray/subscript(_:))
- [Indirect command encoding](/documentation/metal/indirect-command-encoding)

### Indirect command buffers

- [Creating an indirect command buffer](/documentation/metal/creating-an-indirect-command-buffer)
- [Specifying drawing and dispatch arguments indirectly](/documentation/metal/specifying-drawing-and-dispatch-arguments-indirectly)
- [Encoding indirect command buffers on the CPU](/documentation/metal/encoding-indirect-command-buffers-on-the-cpu)
- [Encoding indirect command buffers on the GPU](/documentation/metal/encoding-indirect-command-buffers-on-the-gpu)
- [MTLIndirectCommandBuffer](/documentation/metal/mtlindirectcommandbuffer)

#### Determining the maximum number of commands

- [var size: Int](/documentation/metal/mtlindirectcommandbuffer/size)

#### Retrieving commands

- [func indirectRenderCommandAt(Int) -> any MTLIndirectRenderCommand](/documentation/metal/mtlindirectcommandbuffer/indirectrendercommandat(_:))
- [func indirectComputeCommandAt(Int) -> any MTLIndirectComputeCommand](/documentation/metal/mtlindirectcommandbuffer/indirectcomputecommandat(_:))
- [func indirectComputeCommand(at: Int) -> any MTLIndirectComputeCommand](/documentation/metal/mtlindirectcommandbuffer/indirectcomputecommand(at:))

#### Resetting commands

- [- resetWithRange:](/documentation/metal/mtlindirectcommandbuffer/reset(_:))

#### Instance Properties

- [var gpuResourceID: MTLResourceID](/documentation/metal/mtlindirectcommandbuffer/gpuresourceid)
- [MTLIndirectCommandBufferDescriptor](/documentation/metal/mtlindirectcommandbufferdescriptor)

#### Declaring command types to encode

- [var commandTypes: MTLIndirectCommandType](/documentation/metal/mtlindirectcommandbufferdescriptor/commandtypes)

#### Declaring command inheritance

- [var inheritBuffers: Bool](/documentation/metal/mtlindirectcommandbufferdescriptor/inheritbuffers)
- [var inheritPipelineState: Bool](/documentation/metal/mtlindirectcommandbufferdescriptor/inheritpipelinestate)

#### Declaring the maximum number of argument buffers per command

- [var maxVertexBufferBindCount: Int](/documentation/metal/mtlindirectcommandbufferdescriptor/maxvertexbufferbindcount)
- [var maxFragmentBufferBindCount: Int](/documentation/metal/mtlindirectcommandbufferdescriptor/maxfragmentbufferbindcount)
- [var maxKernelBufferBindCount: Int](/documentation/metal/mtlindirectcommandbufferdescriptor/maxkernelbufferbindcount)

#### Instance Properties

- [var inheritCullMode: Bool](/documentation/metal/mtlindirectcommandbufferdescriptor/inheritcullmode)
- [var inheritDepthBias: Bool](/documentation/metal/mtlindirectcommandbufferdescriptor/inheritdepthbias)
- [var inheritDepthClipMode: Bool](/documentation/metal/mtlindirectcommandbufferdescriptor/inheritdepthclipmode)
- [var inheritDepthStencilState: Bool](/documentation/metal/mtlindirectcommandbufferdescriptor/inheritdepthstencilstate)
- [var inheritFrontFacingWinding: Bool](/documentation/metal/mtlindirectcommandbufferdescriptor/inheritfrontfacingwinding)
- [var inheritTriangleFillMode: Bool](/documentation/metal/mtlindirectcommandbufferdescriptor/inherittrianglefillmode)
- [var maxKernelThreadgroupMemoryBindCount: Int](/documentation/metal/mtlindirectcommandbufferdescriptor/maxkernelthreadgroupmemorybindcount)
- [var maxMeshBufferBindCount: Int](/documentation/metal/mtlindirectcommandbufferdescriptor/maxmeshbufferbindcount)
- [var maxObjectBufferBindCount: Int](/documentation/metal/mtlindirectcommandbufferdescriptor/maxobjectbufferbindcount)
- [var maxObjectThreadgroupMemoryBindCount: Int](/documentation/metal/mtlindirectcommandbufferdescriptor/maxobjectthreadgroupmemorybindcount)
- [var supportColorAttachmentMapping: Bool](/documentation/metal/mtlindirectcommandbufferdescriptor/supportcolorattachmentmapping)
- [var supportDynamicAttributeStride: Bool](/documentation/metal/mtlindirectcommandbufferdescriptor/supportdynamicattributestride)
- [var supportRayTracing: Bool](/documentation/metal/mtlindirectcommandbufferdescriptor/supportraytracing)
- [MTLIndirectCommandType](/documentation/metal/mtlindirectcommandtype)

#### Creating a set of command types

- [init(rawValue: UInt)](/documentation/metal/mtlindirectcommandtype/init(rawvalue:))

#### Specifying command types

- [static var draw: MTLIndirectCommandType](/documentation/metal/mtlindirectcommandtype/draw)
- [static var drawIndexed: MTLIndirectCommandType](/documentation/metal/mtlindirectcommandtype/drawindexed)
- [static var drawPatches: MTLIndirectCommandType](/documentation/metal/mtlindirectcommandtype/drawpatches)
- [static var drawIndexedPatches: MTLIndirectCommandType](/documentation/metal/mtlindirectcommandtype/drawindexedpatches)
- [static var concurrentDispatch: MTLIndirectCommandType](/documentation/metal/mtlindirectcommandtype/concurrentdispatch)
- [static var concurrentDispatchThreads: MTLIndirectCommandType](/documentation/metal/mtlindirectcommandtype/concurrentdispatchthreads)

#### Type Properties

- [static var drawMeshThreadgroups: MTLIndirectCommandType](/documentation/metal/mtlindirectcommandtype/drawmeshthreadgroups)
- [static var drawMeshThreads: MTLIndirectCommandType](/documentation/metal/mtlindirectcommandtype/drawmeshthreads)
- [MTLIndirectCommandBufferExecutionRange](/documentation/metal/mtlindirectcommandbufferexecutionrange)

#### Creating a command execution range

- [init()](/documentation/metal/mtlindirectcommandbufferexecutionrange/init())
- [init(location: UInt32, length: UInt32)](/documentation/metal/mtlindirectcommandbufferexecutionrange/init(location:length:))
- [func MTLIndirectCommandBufferExecutionRangeMake(UInt32, UInt32) -> MTLIndirectCommandBufferExecutionRange](/documentation/metal/mtlindirectcommandbufferexecutionrangemake(_:_:))

#### Examining the range

- [var location: UInt32](/documentation/metal/mtlindirectcommandbufferexecutionrange/location)
- [var length: UInt32](/documentation/metal/mtlindirectcommandbufferexecutionrange/length)
- [func MTLIndirectCommandBufferExecutionRangeMake(UInt32, UInt32) -> MTLIndirectCommandBufferExecutionRange](/documentation/metal/mtlindirectcommandbufferexecutionrangemake(_:_:))

### Indirect compute commands

- [MTLIndirectComputeCommand](/documentation/metal/mtlindirectcomputecommand)

#### Setting a command’s arguments

- [func setComputePipelineState(any MTLComputePipelineState)](/documentation/metal/mtlindirectcomputecommand/setcomputepipelinestate(_:))
- [func setImageblockWidth(Int, height: Int)](/documentation/metal/mtlindirectcomputecommand/setimageblockwidth(_:height:))
- [func setKernelBuffer(any MTLBuffer, offset: Int, at: Int)](/documentation/metal/mtlindirectcomputecommand/setkernelbuffer(_:offset:at:))
- [func setThreadgroupMemoryLength(Int, index: Int)](/documentation/metal/mtlindirectcomputecommand/setthreadgroupmemorylength(_:index:))
- [func setThreadgroupMemoryLength(Int, at: Int)](/documentation/metal/mtlindirectcomputecommand/setthreadgroupmemorylength(_:at:))
- [func setStageInRegion(MTLRegion)](/documentation/metal/mtlindirectcomputecommand/setstageinregion(_:))
- [func setStageIn(MTLRegion)](/documentation/metal/mtlindirectcomputecommand/setstagein(_:))

#### Synchronizing command execution

- [func setBarrier()](/documentation/metal/mtlindirectcomputecommand/setbarrier())
- [func clearBarrier()](/documentation/metal/mtlindirectcomputecommand/clearbarrier())

#### Encoding a compute command

- [func concurrentDispatchThreadgroups(MTLSize, threadsPerThreadgroup: MTLSize)](/documentation/metal/mtlindirectcomputecommand/concurrentdispatchthreadgroups(_:threadsperthreadgroup:))
- [func concurrentDispatchThreads(MTLSize, threadsPerThreadgroup: MTLSize)](/documentation/metal/mtlindirectcomputecommand/concurrentdispatchthreads(_:threadsperthreadgroup:))

#### Resetting a command

- [func reset()](/documentation/metal/mtlindirectcomputecommand/reset())

#### Instance Methods

- [func setKernelBuffer(any MTLBuffer, offset: Int, attributeStride: Int, at: Int)](/documentation/metal/mtlindirectcomputecommand/setkernelbuffer(_:offset:attributestride:at:))
- [MTLRegion](/documentation/metal/mtlregion)

#### Creating regions

- [init()](/documentation/metal/mtlregion/init())
- [init(origin: MTLOrigin, size: MTLSize)](/documentation/metal/mtlregion/init(origin:size:))
- [func MTLRegionMake1D(Int, Int) -> MTLRegion](/documentation/metal/mtlregionmake1d(_:_:))
- [func MTLRegionMake2D(Int, Int, Int, Int) -> MTLRegion](/documentation/metal/mtlregionmake2d(_:_:_:_:))
- [func MTLRegionMake3D(Int, Int, Int, Int, Int, Int) -> MTLRegion](/documentation/metal/mtlregionmake3d(_:_:_:_:_:_:))

#### Getting and setting region information

- [var origin: MTLOrigin](/documentation/metal/mtlregion/origin)
- [var size: MTLSize](/documentation/metal/mtlregion/size)
- [MTLSize](/documentation/metal/mtlsize)

#### Creating a size instance

- [init()](/documentation/metal/mtlsize/init())
- [init(width: Int, height: Int, depth: Int)](/documentation/metal/mtlsize/init(width:height:depth:))
- [func MTLSizeMake(Int, Int, Int) -> MTLSize](/documentation/metal/mtlsizemake(_:_:_:))

#### Accessing a size’s dimensions

- [var width: Int](/documentation/metal/mtlsize/width)
- [var height: Int](/documentation/metal/mtlsize/height)
- [var depth: Int](/documentation/metal/mtlsize/depth)
- [MTLOrigin](/documentation/metal/mtlorigin)

#### Creating origin points

- [init()](/documentation/metal/mtlorigin/init())
- [init(x: Int, y: Int, z: Int)](/documentation/metal/mtlorigin/init(x:y:z:))
- [func MTLOriginMake(Int, Int, Int) -> MTLOrigin](/documentation/metal/mtloriginmake(_:_:_:))

#### Getting and setting coordinate values

- [var x: Int](/documentation/metal/mtlorigin/x)
- [var y: Int](/documentation/metal/mtlorigin/y)
- [var z: Int](/documentation/metal/mtlorigin/z)
- [MTLStageInRegionIndirectArguments](/documentation/metal/mtlstageinregionindirectarguments)

#### Initializers

- [init()](/documentation/metal/mtlstageinregionindirectarguments/init())
- [init(stageInOrigin: (UInt32, UInt32, UInt32), stageInSize: (UInt32, UInt32, UInt32))](/documentation/metal/mtlstageinregionindirectarguments/init(stageinorigin:stageinsize:))

#### Instance Properties

- [var stageInOrigin: (UInt32, UInt32, UInt32)](/documentation/metal/mtlstageinregionindirectarguments/stageinorigin)
- [var stageInSize: (UInt32, UInt32, UInt32)](/documentation/metal/mtlstageinregionindirectarguments/stageinsize)
- [MTLDispatchThreadgroupsIndirectArguments](/documentation/metal/mtldispatchthreadgroupsindirectarguments)

#### Specifying the size of the threadgroup

- [init()](/documentation/metal/mtldispatchthreadgroupsindirectarguments/init())
- [init(threadgroupsPerGrid: (UInt32, UInt32, UInt32))](/documentation/metal/mtldispatchthreadgroupsindirectarguments/init(threadgroupspergrid:))
- [var threadgroupsPerGrid: (UInt32, UInt32, UInt32)](/documentation/metal/mtldispatchthreadgroupsindirectarguments/threadgroupspergrid)

### Render compute commands

- [MTLIndirectRenderCommand](/documentation/metal/mtlindirectrendercommand)

#### Setting command arguments

- [func setRenderPipelineState(any MTLRenderPipelineState)](/documentation/metal/mtlindirectrendercommand/setrenderpipelinestate(_:))
- [func setVertexBuffer(any MTLBuffer, offset: Int, at: Int)](/documentation/metal/mtlindirectrendercommand/setvertexbuffer(_:offset:at:))
- [func setFragmentBuffer(any MTLBuffer, offset: Int, at: Int)](/documentation/metal/mtlindirectrendercommand/setfragmentbuffer(_:offset:at:))

#### Encoding a drawing command

- [func drawPrimitives(MTLPrimitiveType, vertexStart: Int, vertexCount: Int, instanceCount: Int, baseInstance: Int)](/documentation/metal/mtlindirectrendercommand/drawprimitives(_:vertexstart:vertexcount:instancecount:baseinstance:))
- [func drawIndexedPrimitives(MTLPrimitiveType, indexCount: Int, indexType: MTLIndexType, indexBuffer: any MTLBuffer, indexBufferOffset: Int, instanceCount: Int, baseVertex: Int, baseInstance: Int)](/documentation/metal/mtlindirectrendercommand/drawindexedprimitives(_:indexcount:indextype:indexbuffer:indexbufferoffset:instancecount:basevertex:baseinstance:))
- [func drawPatches(Int, patchStart: Int, patchCount: Int, patchIndexBuffer: (any MTLBuffer)?, patchIndexBufferOffset: Int, instanceCount: Int, baseInstance: Int, tessellationFactorBuffer: any MTLBuffer, tessellationFactorBufferOffset: Int, tessellationFactorBufferInstanceStride: Int)](/documentation/metal/mtlindirectrendercommand/drawpatches(_:patchstart:patchcount:patchindexbuffer:patchindexbufferoffset:instancecount:baseinstance:tessellationfactorbuffer:tessellationfactorbufferoffset:tessellationfactorbufferinstancestride:))
- [func drawIndexedPatches(Int, patchStart: Int, patchCount: Int, patchIndexBuffer: (any MTLBuffer)?, patchIndexBufferOffset: Int, controlPointIndexBuffer: any MTLBuffer, controlPointIndexBufferOffset: Int, instanceCount: Int, baseInstance: Int, tessellationFactorBuffer: any MTLBuffer, tessellationFactorBufferOffset: Int, tessellationFactorBufferInstanceStride: Int)](/documentation/metal/mtlindirectrendercommand/drawindexedpatches(_:patchstart:patchcount:patchindexbuffer:patchindexbufferoffset:controlpointindexbuffer:controlpointindexbufferoffset:instancecount:baseinstance:tessellationfactorbuffer:tessellationfactorbufferoffset:tessellationfactorbu-4mdz8)

#### Resetting a command

- [func reset()](/documentation/metal/mtlindirectrendercommand/reset())

#### Instance Methods

- [func clearBarrier()](/documentation/metal/mtlindirectrendercommand/clearbarrier())
- [func drawMeshThreadgroups(MTLSize, threadsPerObjectThreadgroup: MTLSize, threadsPerMeshThreadgroup: MTLSize)](/documentation/metal/mtlindirectrendercommand/drawmeshthreadgroups(_:threadsperobjectthreadgroup:threadspermeshthreadgroup:))
- [func drawMeshThreads(MTLSize, threadsPerObjectThreadgroup: MTLSize, threadsPerMeshThreadgroup: MTLSize)](/documentation/metal/mtlindirectrendercommand/drawmeshthreads(_:threadsperobjectthreadgroup:threadspermeshthreadgroup:))
- [func setBarrier()](/documentation/metal/mtlindirectrendercommand/setbarrier())
- [func setCullMode(MTLCullMode)](/documentation/metal/mtlindirectrendercommand/setcullmode(_:))
- [func setDepthBias(Float, slopeScale: Float, clamp: Float)](/documentation/metal/mtlindirectrendercommand/setdepthbias(_:slopescale:clamp:))
- [func setDepthClipMode(MTLDepthClipMode)](/documentation/metal/mtlindirectrendercommand/setdepthclipmode(_:))
- [func setDepthStencilState((any MTLDepthStencilState)?)](/documentation/metal/mtlindirectrendercommand/setdepthstencilstate(_:))
- [func setFrontFacing(MTLWinding)](/documentation/metal/mtlindirectrendercommand/setfrontfacing(_:))
- [func setMeshBuffer(any MTLBuffer, offset: Int, at: Int)](/documentation/metal/mtlindirectrendercommand/setmeshbuffer(_:offset:at:))
- [func setObjectBuffer(any MTLBuffer, offset: Int, at: Int)](/documentation/metal/mtlindirectrendercommand/setobjectbuffer(_:offset:at:))
- [func setObjectThreadgroupMemoryLength(Int, index: Int)](/documentation/metal/mtlindirectrendercommand/setobjectthreadgroupmemorylength(_:index:))
- [func setTriangleFillMode(MTLTriangleFillMode)](/documentation/metal/mtlindirectrendercommand/settrianglefillmode(_:))
- [func setVertexBuffer(any MTLBuffer, offset: Int, attributeStride: Int, at: Int)](/documentation/metal/mtlindirectrendercommand/setvertexbuffer(_:offset:attributestride:at:))
- [MTLDrawPatchIndirectArguments](/documentation/metal/mtldrawpatchindirectarguments)

#### Initializers

- [init()](/documentation/metal/mtldrawpatchindirectarguments/init())
- [init(patchCount: UInt32, instanceCount: UInt32, patchStart: UInt32, baseInstance: UInt32)](/documentation/metal/mtldrawpatchindirectarguments/init(patchcount:instancecount:patchstart:baseinstance:))

#### Instance Properties

- [var baseInstance: UInt32](/documentation/metal/mtldrawpatchindirectarguments/baseinstance)
- [var instanceCount: UInt32](/documentation/metal/mtldrawpatchindirectarguments/instancecount)
- [var patchCount: UInt32](/documentation/metal/mtldrawpatchindirectarguments/patchcount)
- [var patchStart: UInt32](/documentation/metal/mtldrawpatchindirectarguments/patchstart)
- [MTLDrawPrimitivesIndirectArguments](/documentation/metal/mtldrawprimitivesindirectarguments)

#### Initializers

- [init()](/documentation/metal/mtldrawprimitivesindirectarguments/init())
- [init(vertexCount: UInt32, instanceCount: UInt32, vertexStart: UInt32, baseInstance: UInt32)](/documentation/metal/mtldrawprimitivesindirectarguments/init(vertexcount:instancecount:vertexstart:baseinstance:))

#### Instance Properties

- [var baseInstance: UInt32](/documentation/metal/mtldrawprimitivesindirectarguments/baseinstance)
- [var instanceCount: UInt32](/documentation/metal/mtldrawprimitivesindirectarguments/instancecount)
- [var vertexCount: UInt32](/documentation/metal/mtldrawprimitivesindirectarguments/vertexcount)
- [var vertexStart: UInt32](/documentation/metal/mtldrawprimitivesindirectarguments/vertexstart)
- [MTLDrawIndexedPrimitivesIndirectArguments](/documentation/metal/mtldrawindexedprimitivesindirectarguments)

#### Initializers

- [init()](/documentation/metal/mtldrawindexedprimitivesindirectarguments/init())
- [init(indexCount: UInt32, instanceCount: UInt32, indexStart: UInt32, baseVertex: Int32, baseInstance: UInt32)](/documentation/metal/mtldrawindexedprimitivesindirectarguments/init(indexcount:instancecount:indexstart:basevertex:baseinstance:))

#### Instance Properties

- [var baseInstance: UInt32](/documentation/metal/mtldrawindexedprimitivesindirectarguments/baseinstance)
- [var baseVertex: Int32](/documentation/metal/mtldrawindexedprimitivesindirectarguments/basevertex)
- [var indexCount: UInt32](/documentation/metal/mtldrawindexedprimitivesindirectarguments/indexcount)
- [var indexStart: UInt32](/documentation/metal/mtldrawindexedprimitivesindirectarguments/indexstart)
- [var instanceCount: UInt32](/documentation/metal/mtldrawindexedprimitivesindirectarguments/instancecount)
- [Ray tracing with acceleration structures](/documentation/metal/ray-tracing-with-acceleration-structures)

### Ray tracing samples

- [Accelerating ray tracing using Metal](/documentation/metal/accelerating-ray-tracing-using-metal)
- [Control the ray tracing process using intersection queries](/documentation/metal/control-the-ray-tracing-process-using-intersection-queries)
- [Rendering reflections in real time using ray tracing](/documentation/metal/rendering-reflections-in-real-time-using-ray-tracing)
- [Rendering a curve primitive in a ray tracing scene](/documentation/metal/rendering-a-curve-primitive-in-a-ray-tracing-scene)

### Acceleration structures

- [Improving ray-tracing data access using per-primitive data](/documentation/metal/improving-ray-tracing-data-access-using-per-primitive-data)
- [MTLAccelerationStructure](/documentation/metal/mtlaccelerationstructure)

#### Reading the structure’s size

- [var size: Int](/documentation/metal/mtlaccelerationstructure/size)

#### Instance Properties

- [var gpuResourceID: MTLResourceID](/documentation/metal/mtlaccelerationstructure/gpuresourceid)
- [MTL4AccelerationStructureDescriptor](/documentation/metal/mtl4accelerationstructuredescriptor)
- [MTLAccelerationStructureDescriptor](/documentation/metal/mtlaccelerationstructuredescriptor)

#### Specifying usage options

- [var usage: MTLAccelerationStructureUsage](/documentation/metal/mtlaccelerationstructuredescriptor/usage)
- [MTL4PrimitiveAccelerationStructureDescriptor](/documentation/metal/mtl4primitiveaccelerationstructuredescriptor)

#### Instance Properties

- [var geometryDescriptors: [MTL4AccelerationStructureGeometryDescriptor]?](/documentation/metal/mtl4primitiveaccelerationstructuredescriptor/geometrydescriptors)
- [var motionEndBorderMode: MTLMotionBorderMode](/documentation/metal/mtl4primitiveaccelerationstructuredescriptor/motionendbordermode)
- [var motionEndTime: Float](/documentation/metal/mtl4primitiveaccelerationstructuredescriptor/motionendtime)
- [var motionKeyframeCount: Int](/documentation/metal/mtl4primitiveaccelerationstructuredescriptor/motionkeyframecount)
- [var motionStartBorderMode: MTLMotionBorderMode](/documentation/metal/mtl4primitiveaccelerationstructuredescriptor/motionstartbordermode)
- [var motionStartTime: Float](/documentation/metal/mtl4primitiveaccelerationstructuredescriptor/motionstarttime)
- [MTLPrimitiveAccelerationStructureDescriptor](/documentation/metal/mtlprimitiveaccelerationstructuredescriptor)

#### Specifying geometry

- [var geometryDescriptors: [MTLAccelerationStructureGeometryDescriptor]?](/documentation/metal/mtlprimitiveaccelerationstructuredescriptor/geometrydescriptors)

#### Specifying motion behavior

- [var motionKeyframeCount: Int](/documentation/metal/mtlprimitiveaccelerationstructuredescriptor/motionkeyframecount)
- [var motionStartTime: Float](/documentation/metal/mtlprimitiveaccelerationstructuredescriptor/motionstarttime)
- [var motionEndTime: Float](/documentation/metal/mtlprimitiveaccelerationstructuredescriptor/motionendtime)
- [var motionStartBorderMode: MTLMotionBorderMode](/documentation/metal/mtlprimitiveaccelerationstructuredescriptor/motionstartbordermode)
- [var motionEndBorderMode: MTLMotionBorderMode](/documentation/metal/mtlprimitiveaccelerationstructuredescriptor/motionendbordermode)
- [MTLMotionBorderMode](/documentation/metal/mtlmotionbordermode)

##### Specifying motion modes

- [case clamp](/documentation/metal/mtlmotionbordermode/clamp)
- [case vanish](/documentation/metal/mtlmotionbordermode/vanish)

##### Initializers

- [init?(rawValue: UInt32)](/documentation/metal/mtlmotionbordermode/init(rawvalue:))
- [MTL4InstanceAccelerationStructureDescriptor](/documentation/metal/mtl4instanceaccelerationstructuredescriptor)

#### Instance Properties

- [var instanceCount: Int](/documentation/metal/mtl4instanceaccelerationstructuredescriptor/instancecount)
- [var instanceDescriptorBuffer: MTL4BufferRange](/documentation/metal/mtl4instanceaccelerationstructuredescriptor/instancedescriptorbuffer)
- [var instanceDescriptorStride: Int](/documentation/metal/mtl4instanceaccelerationstructuredescriptor/instancedescriptorstride)
- [var instanceDescriptorType: MTLAccelerationStructureInstanceDescriptorType](/documentation/metal/mtl4instanceaccelerationstructuredescriptor/instancedescriptortype)
- [var instanceTransformationMatrixLayout: MTLMatrixLayout](/documentation/metal/mtl4instanceaccelerationstructuredescriptor/instancetransformationmatrixlayout)
- [var motionTransformBuffer: MTL4BufferRange](/documentation/metal/mtl4instanceaccelerationstructuredescriptor/motiontransformbuffer)
- [var motionTransformCount: Int](/documentation/metal/mtl4instanceaccelerationstructuredescriptor/motiontransformcount)
- [var motionTransformStride: Int](/documentation/metal/mtl4instanceaccelerationstructuredescriptor/motiontransformstride)
- [var motionTransformType: MTLTransformType](/documentation/metal/mtl4instanceaccelerationstructuredescriptor/motiontransformtype)
- [MTLInstanceAccelerationStructureDescriptor](/documentation/metal/mtlinstanceaccelerationstructuredescriptor)

#### Specifying the instance structures

- [var instanceDescriptorType: MTLAccelerationStructureInstanceDescriptorType](/documentation/metal/mtlinstanceaccelerationstructuredescriptor/instancedescriptortype)
- [var instancedAccelerationStructures: [any MTLAccelerationStructure]?](/documentation/metal/mtlinstanceaccelerationstructuredescriptor/instancedaccelerationstructures)
- [MTLAccelerationStructureInstanceDescriptorType](/documentation/metal/mtlaccelerationstructureinstancedescriptortype)

##### Specifying the instance descriptor type

- [case `default`](/documentation/metal/mtlaccelerationstructureinstancedescriptortype/default)
- [case userID](/documentation/metal/mtlaccelerationstructureinstancedescriptortype/userid)
- [case motion](/documentation/metal/mtlaccelerationstructureinstancedescriptortype/motion)
- [case indirect](/documentation/metal/mtlaccelerationstructureinstancedescriptortype/indirect)
- [case indirectMotion](/documentation/metal/mtlaccelerationstructureinstancedescriptortype/indirectmotion)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlaccelerationstructureinstancedescriptortype/init(rawvalue:))

#### Specifying the list of instances

- [var instanceCount: Int](/documentation/metal/mtlinstanceaccelerationstructuredescriptor/instancecount)
- [var instanceDescriptorBuffer: (any MTLBuffer)?](/documentation/metal/mtlinstanceaccelerationstructuredescriptor/instancedescriptorbuffer)
- [var instanceDescriptorBufferOffset: Int](/documentation/metal/mtlinstanceaccelerationstructuredescriptor/instancedescriptorbufferoffset)
- [var instanceDescriptorStride: Int](/documentation/metal/mtlinstanceaccelerationstructuredescriptor/instancedescriptorstride)

#### Specifying motion data

- [var motionTransformCount: Int](/documentation/metal/mtlinstanceaccelerationstructuredescriptor/motiontransformcount)
- [var motionTransformBuffer: (any MTLBuffer)?](/documentation/metal/mtlinstanceaccelerationstructuredescriptor/motiontransformbuffer)
- [var motionTransformBufferOffset: Int](/documentation/metal/mtlinstanceaccelerationstructuredescriptor/motiontransformbufferoffset)

#### Instance Properties

- [var instanceTransformationMatrixLayout: MTLMatrixLayout](/documentation/metal/mtlinstanceaccelerationstructuredescriptor/instancetransformationmatrixlayout)
- [var motionTransformStride: Int](/documentation/metal/mtlinstanceaccelerationstructuredescriptor/motiontransformstride)
- [var motionTransformType: MTLTransformType](/documentation/metal/mtlinstanceaccelerationstructuredescriptor/motiontransformtype)
- [MTLAccelerationStructureCommandEncoder](/documentation/metal/mtlaccelerationstructurecommandencoder)

#### Building an acceleration structure

- [func build(accelerationStructure: any MTLAccelerationStructure, descriptor: MTLAccelerationStructureDescriptor, scratchBuffer: any MTLBuffer, scratchBufferOffset: Int)](/documentation/metal/mtlaccelerationstructurecommandencoder/build(accelerationstructure:descriptor:scratchbuffer:scratchbufferoffset:))

#### Copying an acceleration structure

- [func copy(sourceAccelerationStructure: any MTLAccelerationStructure, destinationAccelerationStructure: any MTLAccelerationStructure)](/documentation/metal/mtlaccelerationstructurecommandencoder/copy(sourceaccelerationstructure:destinationaccelerationstructure:))
- [func writeCompactedSize(accelerationStructure: any MTLAccelerationStructure, buffer: any MTLBuffer, offset: Int)](/documentation/metal/mtlaccelerationstructurecommandencoder/writecompactedsize(accelerationstructure:buffer:offset:))
- [func writeCompactedSize(accelerationStructure: any MTLAccelerationStructure, buffer: any MTLBuffer, offset: Int, sizeDataType: MTLDataType)](/documentation/metal/mtlaccelerationstructurecommandencoder/writecompactedsize(accelerationstructure:buffer:offset:sizedatatype:))
- [func copyAndCompact(sourceAccelerationStructure: any MTLAccelerationStructure, destinationAccelerationStructure: any MTLAccelerationStructure)](/documentation/metal/mtlaccelerationstructurecommandencoder/copyandcompact(sourceaccelerationstructure:destinationaccelerationstructure:))

#### Refitting an acceleration structure

- [func refit(sourceAccelerationStructure: any MTLAccelerationStructure, descriptor: MTLAccelerationStructureDescriptor, destinationAccelerationStructure: (any MTLAccelerationStructure)?, scratchBuffer: (any MTLBuffer)?, scratchBufferOffset: Int)](/documentation/metal/mtlaccelerationstructurecommandencoder/refit(sourceaccelerationstructure:descriptor:destinationaccelerationstructure:scratchbuffer:scratchbufferoffset:))
- [func refit(sourceAccelerationStructure: any MTLAccelerationStructure, descriptor: MTLAccelerationStructureDescriptor, destinationAccelerationStructure: (any MTLAccelerationStructure)?, scratchBuffer: (any MTLBuffer)?, scratchBufferOffset: Int, options: MTLAccelerationStructureRefitOptions)](/documentation/metal/mtlaccelerationstructurecommandencoder/refit(sourceaccelerationstructure:descriptor:destinationaccelerationstructure:scratchbuffer:scratchbufferoffset:options:))

#### Preventing resource access conflicts

- [func updateFence(any MTLFence)](/documentation/metal/mtlaccelerationstructurecommandencoder/updatefence(_:))
- [func waitForFence(any MTLFence)](/documentation/metal/mtlaccelerationstructurecommandencoder/waitforfence(_:))

#### Making indirect resources resident

- [func useHeap(any MTLHeap)](/documentation/metal/mtlaccelerationstructurecommandencoder/useheap(_:))
- [- useHeaps:count:](/documentation/metal/mtlaccelerationstructurecommandencoder/useheaps(_:))
- [func useResource(any MTLResource, usage: MTLResourceUsage)](/documentation/metal/mtlaccelerationstructurecommandencoder/useresource(_:usage:))
- [- useResources:count:usage:](/documentation/metal/mtlaccelerationstructurecommandencoder/useresources(_:usage:))
- [MTLResourceUsage](/documentation/metal/mtlresourceusage)

##### Initializers

- [init(rawValue: UInt)](/documentation/metal/mtlresourceusage/init(rawvalue:))

##### Type Properties

- [static var read: MTLResourceUsage](/documentation/metal/mtlresourceusage/read)
- [static var sample: MTLResourceUsage](/documentation/metal/mtlresourceusage/sample)
- [static var write: MTLResourceUsage](/documentation/metal/mtlresourceusage/write)

#### Sampling counters

- [func sampleCounters(sampleBuffer: any MTLCounterSampleBuffer, sampleIndex: Int, barrier: Bool)](/documentation/metal/mtlaccelerationstructurecommandencoder/samplecounters(samplebuffer:sampleindex:barrier:))
- [MTLAccelerationStructureUsage](/documentation/metal/mtlaccelerationstructureusage)

#### Applying options

- [static var refit: MTLAccelerationStructureUsage](/documentation/metal/mtlaccelerationstructureusage/refit)
- [static var preferFastBuild: MTLAccelerationStructureUsage](/documentation/metal/mtlaccelerationstructureusage/preferfastbuild)
- [static var preferFastIntersection: MTLAccelerationStructureUsage](/documentation/metal/mtlaccelerationstructureusage/preferfastintersection)
- [static var minimizeMemory: MTLAccelerationStructureUsage](/documentation/metal/mtlaccelerationstructureusage/minimizememory)
- [static var extendedLimits: MTLAccelerationStructureUsage](/documentation/metal/mtlaccelerationstructureusage/extendedlimits)

#### Swift support

- [init(rawValue: UInt)](/documentation/metal/mtlaccelerationstructureusage/init(rawvalue:))
- [MTLAccelerationStructureRefitOptions](/documentation/metal/mtlaccelerationstructurerefitoptions)

#### Initializers

- [init(rawValue: UInt)](/documentation/metal/mtlaccelerationstructurerefitoptions/init(rawvalue:))

#### Type Properties

- [static var perPrimitiveData: MTLAccelerationStructureRefitOptions](/documentation/metal/mtlaccelerationstructurerefitoptions/perprimitivedata)
- [static var vertexData: MTLAccelerationStructureRefitOptions](/documentation/metal/mtlaccelerationstructurerefitoptions/vertexdata)

### Acceleration structures passes

- [MTLAccelerationStructurePassDescriptor](/documentation/metal/mtlaccelerationstructurepassdescriptor)

#### Instance Properties

- [var sampleBufferAttachments: MTLAccelerationStructurePassSampleBufferAttachmentDescriptorArray](/documentation/metal/mtlaccelerationstructurepassdescriptor/samplebufferattachments)
- [MTLAccelerationStructurePassSampleBufferAttachmentDescriptor](/documentation/metal/mtlaccelerationstructurepasssamplebufferattachmentdescriptor)

#### Instance Properties

- [var endOfEncoderSampleIndex: Int](/documentation/metal/mtlaccelerationstructurepasssamplebufferattachmentdescriptor/endofencodersampleindex)
- [var sampleBuffer: (any MTLCounterSampleBuffer)?](/documentation/metal/mtlaccelerationstructurepasssamplebufferattachmentdescriptor/samplebuffer)
- [var startOfEncoderSampleIndex: Int](/documentation/metal/mtlaccelerationstructurepasssamplebufferattachmentdescriptor/startofencodersampleindex)
- [MTLAccelerationStructurePassSampleBufferAttachmentDescriptorArray](/documentation/metal/mtlaccelerationstructurepasssamplebufferattachmentdescriptorarray)

#### Subscripts

- [subscript(Int) -> MTLAccelerationStructurePassSampleBufferAttachmentDescriptor!](/documentation/metal/mtlaccelerationstructurepasssamplebufferattachmentdescriptorarray/subscript(_:))

### Geometry descriptors

- [MTL4AccelerationStructureGeometryDescriptor](/documentation/metal/mtl4accelerationstructuregeometrydescriptor)

#### Instance Properties

- [var allowDuplicateIntersectionFunctionInvocation: Bool](/documentation/metal/mtl4accelerationstructuregeometrydescriptor/allowduplicateintersectionfunctioninvocation)
- [var intersectionFunctionTableOffset: Int](/documentation/metal/mtl4accelerationstructuregeometrydescriptor/intersectionfunctiontableoffset)
- [var label: String?](/documentation/metal/mtl4accelerationstructuregeometrydescriptor/label)
- [var opaque: Bool](/documentation/metal/mtl4accelerationstructuregeometrydescriptor/opaque)
- [var primitiveDataBuffer: MTL4BufferRange](/documentation/metal/mtl4accelerationstructuregeometrydescriptor/primitivedatabuffer)
- [var primitiveDataElementSize: Int](/documentation/metal/mtl4accelerationstructuregeometrydescriptor/primitivedataelementsize)
- [var primitiveDataStride: Int](/documentation/metal/mtl4accelerationstructuregeometrydescriptor/primitivedatastride)
- [MTLAccelerationStructureGeometryDescriptor](/documentation/metal/mtlaccelerationstructuregeometrydescriptor)

#### Specifying base geometry properties

- [var label: String?](/documentation/metal/mtlaccelerationstructuregeometrydescriptor/label)
- [var intersectionFunctionTableOffset: Int](/documentation/metal/mtlaccelerationstructuregeometrydescriptor/intersectionfunctiontableoffset)
- [var opaque: Bool](/documentation/metal/mtlaccelerationstructuregeometrydescriptor/opaque)
- [var allowDuplicateIntersectionFunctionInvocation: Bool](/documentation/metal/mtlaccelerationstructuregeometrydescriptor/allowduplicateintersectionfunctioninvocation)

#### Instance Properties

- [var primitiveDataBuffer: (any MTLBuffer)?](/documentation/metal/mtlaccelerationstructuregeometrydescriptor/primitivedatabuffer)
- [var primitiveDataBufferOffset: Int](/documentation/metal/mtlaccelerationstructuregeometrydescriptor/primitivedatabufferoffset)
- [var primitiveDataElementSize: Int](/documentation/metal/mtlaccelerationstructuregeometrydescriptor/primitivedataelementsize)
- [var primitiveDataStride: Int](/documentation/metal/mtlaccelerationstructuregeometrydescriptor/primitivedatastride)
- [MTL4AccelerationStructureTriangleGeometryDescriptor](/documentation/metal/mtl4accelerationstructuretrianglegeometrydescriptor)

#### Instance Properties

- [var indexBuffer: MTL4BufferRange](/documentation/metal/mtl4accelerationstructuretrianglegeometrydescriptor/indexbuffer)
- [var indexType: MTLIndexType](/documentation/metal/mtl4accelerationstructuretrianglegeometrydescriptor/indextype)
- [var transformationMatrixBuffer: MTL4BufferRange](/documentation/metal/mtl4accelerationstructuretrianglegeometrydescriptor/transformationmatrixbuffer)
- [var transformationMatrixLayout: MTLMatrixLayout](/documentation/metal/mtl4accelerationstructuretrianglegeometrydescriptor/transformationmatrixlayout)
- [var triangleCount: Int](/documentation/metal/mtl4accelerationstructuretrianglegeometrydescriptor/trianglecount)
- [var vertexBuffer: MTL4BufferRange](/documentation/metal/mtl4accelerationstructuretrianglegeometrydescriptor/vertexbuffer)
- [var vertexFormat: MTLAttributeFormat](/documentation/metal/mtl4accelerationstructuretrianglegeometrydescriptor/vertexformat)
- [var vertexStride: Int](/documentation/metal/mtl4accelerationstructuretrianglegeometrydescriptor/vertexstride)
- [MTLAccelerationStructureTriangleGeometryDescriptor](/documentation/metal/mtlaccelerationstructuretrianglegeometrydescriptor)

#### Configuring the number of triangles

- [var triangleCount: Int](/documentation/metal/mtlaccelerationstructuretrianglegeometrydescriptor/trianglecount)

#### Configuring index data

- [var indexType: MTLIndexType](/documentation/metal/mtlaccelerationstructuretrianglegeometrydescriptor/indextype)
- [var indexBuffer: (any MTLBuffer)?](/documentation/metal/mtlaccelerationstructuretrianglegeometrydescriptor/indexbuffer)
- [var indexBufferOffset: Int](/documentation/metal/mtlaccelerationstructuretrianglegeometrydescriptor/indexbufferoffset)

#### Configuring vertex data

- [var vertexFormat: MTLAttributeFormat](/documentation/metal/mtlaccelerationstructuretrianglegeometrydescriptor/vertexformat)
- [var vertexBuffer: (any MTLBuffer)?](/documentation/metal/mtlaccelerationstructuretrianglegeometrydescriptor/vertexbuffer)
- [var vertexBufferOffset: Int](/documentation/metal/mtlaccelerationstructuretrianglegeometrydescriptor/vertexbufferoffset)
- [var vertexStride: Int](/documentation/metal/mtlaccelerationstructuretrianglegeometrydescriptor/vertexstride)

#### Configuring transformation data

- [var transformationMatrixLayout: MTLMatrixLayout](/documentation/metal/mtlaccelerationstructuretrianglegeometrydescriptor/transformationmatrixlayout)
- [var transformationMatrixBuffer: (any MTLBuffer)?](/documentation/metal/mtlaccelerationstructuretrianglegeometrydescriptor/transformationmatrixbuffer)
- [var transformationMatrixBufferOffset: Int](/documentation/metal/mtlaccelerationstructuretrianglegeometrydescriptor/transformationmatrixbufferoffset)
- [MTL4AccelerationStructureCurveGeometryDescriptor](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor)

#### Instance Properties

- [var controlPointBuffer: MTL4BufferRange](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor/controlpointbuffer)
- [var controlPointCount: Int](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor/controlpointcount)
- [var controlPointFormat: MTLAttributeFormat](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor/controlpointformat)
- [var controlPointStride: Int](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor/controlpointstride)
- [var curveBasis: MTLCurveBasis](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor/curvebasis)
- [var curveEndCaps: MTLCurveEndCaps](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor/curveendcaps)
- [var curveType: MTLCurveType](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor/curvetype)
- [var indexBuffer: MTL4BufferRange](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor/indexbuffer)
- [var indexType: MTLIndexType](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor/indextype)
- [var radiusBuffer: MTL4BufferRange](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor/radiusbuffer)
- [var radiusFormat: MTLAttributeFormat](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor/radiusformat)
- [var radiusStride: Int](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor/radiusstride)
- [var segmentControlPointCount: Int](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor/segmentcontrolpointcount)
- [var segmentCount: Int](/documentation/metal/mtl4accelerationstructurecurvegeometrydescriptor/segmentcount)
- [MTLAccelerationStructureCurveGeometryDescriptor](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor)

#### Instance Properties

- [var controlPointBuffer: (any MTLBuffer)?](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/controlpointbuffer)
- [var controlPointBufferOffset: Int](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/controlpointbufferoffset)
- [var controlPointCount: Int](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/controlpointcount)
- [var controlPointFormat: MTLAttributeFormat](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/controlpointformat)
- [var controlPointStride: Int](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/controlpointstride)
- [var curveBasis: MTLCurveBasis](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/curvebasis)
- [var curveEndCaps: MTLCurveEndCaps](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/curveendcaps)
- [var curveType: MTLCurveType](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/curvetype)
- [var indexBuffer: (any MTLBuffer)?](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/indexbuffer)
- [var indexBufferOffset: Int](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/indexbufferoffset)
- [var indexType: MTLIndexType](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/indextype)
- [var radiusBuffer: (any MTLBuffer)?](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/radiusbuffer)
- [var radiusBufferOffset: Int](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/radiusbufferoffset)
- [var radiusFormat: MTLAttributeFormat](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/radiusformat)
- [var radiusStride: Int](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/radiusstride)
- [var segmentControlPointCount: Int](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/segmentcontrolpointcount)
- [var segmentCount: Int](/documentation/metal/mtlaccelerationstructurecurvegeometrydescriptor/segmentcount)
- [MTLCurveType](/documentation/metal/mtlcurvetype)

#### Enumeration Cases

- [case flat](/documentation/metal/mtlcurvetype/flat)
- [case round](/documentation/metal/mtlcurvetype/round)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlcurvetype/init(rawvalue:))
- [MTLCurveBasis](/documentation/metal/mtlcurvebasis)

#### Enumeration Cases

- [case bSpline](/documentation/metal/mtlcurvebasis/bspline)
- [case bezier](/documentation/metal/mtlcurvebasis/bezier)
- [case catmullRom](/documentation/metal/mtlcurvebasis/catmullrom)
- [case linear](/documentation/metal/mtlcurvebasis/linear)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlcurvebasis/init(rawvalue:))
- [MTLCurveEndCaps](/documentation/metal/mtlcurveendcaps)

#### Enumeration Cases

- [case disk](/documentation/metal/mtlcurveendcaps/disk)
- [case none](/documentation/metal/mtlcurveendcaps/none)
- [case sphere](/documentation/metal/mtlcurveendcaps/sphere)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlcurveendcaps/init(rawvalue:))
- [MTL4AccelerationStructureBoundingBoxGeometryDescriptor](/documentation/metal/mtl4accelerationstructureboundingboxgeometrydescriptor)

#### Instance Properties

- [var boundingBoxBuffer: MTL4BufferRange](/documentation/metal/mtl4accelerationstructureboundingboxgeometrydescriptor/boundingboxbuffer)
- [var boundingBoxCount: Int](/documentation/metal/mtl4accelerationstructureboundingboxgeometrydescriptor/boundingboxcount)
- [var boundingBoxStride: Int](/documentation/metal/mtl4accelerationstructureboundingboxgeometrydescriptor/boundingboxstride)
- [MTLAccelerationStructureBoundingBoxGeometryDescriptor](/documentation/metal/mtlaccelerationstructureboundingboxgeometrydescriptor)

#### Specifying the number of bounding boxes

- [var boundingBoxCount: Int](/documentation/metal/mtlaccelerationstructureboundingboxgeometrydescriptor/boundingboxcount)

#### Specifying bounding boxes data

- [var boundingBoxBuffer: (any MTLBuffer)?](/documentation/metal/mtlaccelerationstructureboundingboxgeometrydescriptor/boundingboxbuffer)
- [var boundingBoxBufferOffset: Int](/documentation/metal/mtlaccelerationstructureboundingboxgeometrydescriptor/boundingboxbufferoffset)
- [var boundingBoxStride: Int](/documentation/metal/mtlaccelerationstructureboundingboxgeometrydescriptor/boundingboxstride)

### Motion geometry descriptors

- [MTL4AccelerationStructureMotionTriangleGeometryDescriptor](/documentation/metal/mtl4accelerationstructuremotiontrianglegeometrydescriptor)

#### Instance Properties

- [var indexBuffer: MTL4BufferRange](/documentation/metal/mtl4accelerationstructuremotiontrianglegeometrydescriptor/indexbuffer)
- [var indexType: MTLIndexType](/documentation/metal/mtl4accelerationstructuremotiontrianglegeometrydescriptor/indextype)
- [var transformationMatrixBuffer: MTL4BufferRange](/documentation/metal/mtl4accelerationstructuremotiontrianglegeometrydescriptor/transformationmatrixbuffer)
- [var transformationMatrixLayout: MTLMatrixLayout](/documentation/metal/mtl4accelerationstructuremotiontrianglegeometrydescriptor/transformationmatrixlayout)
- [var triangleCount: Int](/documentation/metal/mtl4accelerationstructuremotiontrianglegeometrydescriptor/trianglecount)
- [var vertexBuffers: MTL4BufferRange](/documentation/metal/mtl4accelerationstructuremotiontrianglegeometrydescriptor/vertexbuffers)
- [var vertexFormat: MTLAttributeFormat](/documentation/metal/mtl4accelerationstructuremotiontrianglegeometrydescriptor/vertexformat)
- [var vertexStride: Int](/documentation/metal/mtl4accelerationstructuremotiontrianglegeometrydescriptor/vertexstride)
- [MTLAccelerationStructureMotionTriangleGeometryDescriptor](/documentation/metal/mtlaccelerationstructuremotiontrianglegeometrydescriptor)

#### Specifying the number of triangles

- [var triangleCount: Int](/documentation/metal/mtlaccelerationstructuremotiontrianglegeometrydescriptor/trianglecount)

#### Specifying index data

- [var indexBuffer: (any MTLBuffer)?](/documentation/metal/mtlaccelerationstructuremotiontrianglegeometrydescriptor/indexbuffer)
- [var indexType: MTLIndexType](/documentation/metal/mtlaccelerationstructuremotiontrianglegeometrydescriptor/indextype)
- [var indexBufferOffset: Int](/documentation/metal/mtlaccelerationstructuremotiontrianglegeometrydescriptor/indexbufferoffset)

#### Specifying vertex data

- [var vertexBuffers: [MTLMotionKeyframeData]](/documentation/metal/mtlaccelerationstructuremotiontrianglegeometrydescriptor/vertexbuffers)
- [var vertexStride: Int](/documentation/metal/mtlaccelerationstructuremotiontrianglegeometrydescriptor/vertexstride)

#### Instance Properties

- [var transformationMatrixBuffer: (any MTLBuffer)?](/documentation/metal/mtlaccelerationstructuremotiontrianglegeometrydescriptor/transformationmatrixbuffer)
- [var transformationMatrixBufferOffset: Int](/documentation/metal/mtlaccelerationstructuremotiontrianglegeometrydescriptor/transformationmatrixbufferoffset)
- [var transformationMatrixLayout: MTLMatrixLayout](/documentation/metal/mtlaccelerationstructuremotiontrianglegeometrydescriptor/transformationmatrixlayout)
- [var vertexFormat: MTLAttributeFormat](/documentation/metal/mtlaccelerationstructuremotiontrianglegeometrydescriptor/vertexformat)
- [MTL4AccelerationStructureMotionCurveGeometryDescriptor](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor)

#### Instance Properties

- [var controlPointBuffers: MTL4BufferRange](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor/controlpointbuffers)
- [var controlPointCount: Int](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor/controlpointcount)
- [var controlPointFormat: MTLAttributeFormat](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor/controlpointformat)
- [var controlPointStride: Int](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor/controlpointstride)
- [var curveBasis: MTLCurveBasis](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor/curvebasis)
- [var curveEndCaps: MTLCurveEndCaps](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor/curveendcaps)
- [var curveType: MTLCurveType](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor/curvetype)
- [var indexBuffer: MTL4BufferRange](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor/indexbuffer)
- [var indexType: MTLIndexType](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor/indextype)
- [var radiusBuffers: MTL4BufferRange](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor/radiusbuffers)
- [var radiusFormat: MTLAttributeFormat](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor/radiusformat)
- [var radiusStride: Int](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor/radiusstride)
- [var segmentControlPointCount: Int](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor/segmentcontrolpointcount)
- [var segmentCount: Int](/documentation/metal/mtl4accelerationstructuremotioncurvegeometrydescriptor/segmentcount)
- [MTLAccelerationStructureMotionCurveGeometryDescriptor](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor)

#### Instance Properties

- [var controlPointBuffers: [MTLMotionKeyframeData]](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/controlpointbuffers)
- [var controlPointCount: Int](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/controlpointcount)
- [var controlPointFormat: MTLAttributeFormat](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/controlpointformat)
- [var controlPointStride: Int](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/controlpointstride)
- [var curveBasis: MTLCurveBasis](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/curvebasis)
- [var curveEndCaps: MTLCurveEndCaps](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/curveendcaps)
- [var curveType: MTLCurveType](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/curvetype)
- [var indexBuffer: (any MTLBuffer)?](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/indexbuffer)
- [var indexBufferOffset: Int](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/indexbufferoffset)
- [var indexType: MTLIndexType](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/indextype)
- [var radiusBuffers: [MTLMotionKeyframeData]](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/radiusbuffers)
- [var radiusFormat: MTLAttributeFormat](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/radiusformat)
- [var radiusStride: Int](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/radiusstride)
- [var segmentControlPointCount: Int](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/segmentcontrolpointcount)
- [var segmentCount: Int](/documentation/metal/mtlaccelerationstructuremotioncurvegeometrydescriptor/segmentcount)
- [MTL4AccelerationStructureMotionBoundingBoxGeometryDescriptor](/documentation/metal/mtl4accelerationstructuremotionboundingboxgeometrydescriptor)

#### Instance Properties

- [var boundingBoxBuffers: MTL4BufferRange](/documentation/metal/mtl4accelerationstructuremotionboundingboxgeometrydescriptor/boundingboxbuffers)
- [var boundingBoxCount: Int](/documentation/metal/mtl4accelerationstructuremotionboundingboxgeometrydescriptor/boundingboxcount)
- [var boundingBoxStride: Int](/documentation/metal/mtl4accelerationstructuremotionboundingboxgeometrydescriptor/boundingboxstride)
- [MTLAccelerationStructureMotionBoundingBoxGeometryDescriptor](/documentation/metal/mtlaccelerationstructuremotionboundingboxgeometrydescriptor)

#### Specifying the number of bounding boxes

- [var boundingBoxCount: Int](/documentation/metal/mtlaccelerationstructuremotionboundingboxgeometrydescriptor/boundingboxcount)

#### Specifying bounding boxes data

- [var boundingBoxBuffers: [MTLMotionKeyframeData]](/documentation/metal/mtlaccelerationstructuremotionboundingboxgeometrydescriptor/boundingboxbuffers)
- [var boundingBoxStride: Int](/documentation/metal/mtlaccelerationstructuremotionboundingboxgeometrydescriptor/boundingboxstride)
- [MTLMotionKeyframeData](/documentation/metal/mtlmotionkeyframedata)

#### Specifying the keyframe data

- [var buffer: (any MTLBuffer)?](/documentation/metal/mtlmotionkeyframedata/buffer)
- [var offset: Int](/documentation/metal/mtlmotionkeyframedata/offset)

### Instance descriptors

- [MTLAccelerationStructureInstanceDescriptor](/documentation/metal/mtlaccelerationstructureinstancedescriptor)

#### Creating an instance descriptor

- [init()](/documentation/metal/mtlaccelerationstructureinstancedescriptor/init())
- [init(transformationMatrix: MTLPackedFloat4x3, options: MTLAccelerationStructureInstanceOptions, mask: UInt32, intersectionFunctionTableOffset: UInt32, accelerationStructureIndex: UInt32)](/documentation/metal/mtlaccelerationstructureinstancedescriptor/init(transformationmatrix:options:mask:intersectionfunctiontableoffset:accelerationstructureindex:))

#### Specifying the instance

- [var accelerationStructureIndex: UInt32](/documentation/metal/mtlaccelerationstructureinstancedescriptor/accelerationstructureindex)

#### Specifying the instance transform

- [var transformationMatrix: MTLPackedFloat4x3](/documentation/metal/mtlaccelerationstructureinstancedescriptor/transformationmatrix)

#### Customizing intersection and hit tests for the instance

- [var intersectionFunctionTableOffset: UInt32](/documentation/metal/mtlaccelerationstructureinstancedescriptor/intersectionfunctiontableoffset)
- [var options: MTLAccelerationStructureInstanceOptions](/documentation/metal/mtlaccelerationstructureinstancedescriptor/options)
- [var mask: UInt32](/documentation/metal/mtlaccelerationstructureinstancedescriptor/mask)
- [MTLAccelerationStructureUserIDInstanceDescriptor](/documentation/metal/mtlaccelerationstructureuseridinstancedescriptor)

#### Creating an instance descriptor

- [init()](/documentation/metal/mtlaccelerationstructureuseridinstancedescriptor/init())
- [init(transformationMatrix: MTLPackedFloat4x3, options: MTLAccelerationStructureInstanceOptions, mask: UInt32, intersectionFunctionTableOffset: UInt32, accelerationStructureIndex: UInt32, userID: UInt32)](/documentation/metal/mtlaccelerationstructureuseridinstancedescriptor/init(transformationmatrix:options:mask:intersectionfunctiontableoffset:accelerationstructureindex:userid:))

#### Specifying the instance

- [var accelerationStructureIndex: UInt32](/documentation/metal/mtlaccelerationstructureuseridinstancedescriptor/accelerationstructureindex)

#### Specifying the instance transform

- [var transformationMatrix: MTLPackedFloat4x3](/documentation/metal/mtlaccelerationstructureuseridinstancedescriptor/transformationmatrix)

#### Customizing intersection and hit tests for the instance

- [var intersectionFunctionTableOffset: UInt32](/documentation/metal/mtlaccelerationstructureuseridinstancedescriptor/intersectionfunctiontableoffset)
- [var options: MTLAccelerationStructureInstanceOptions](/documentation/metal/mtlaccelerationstructureuseridinstancedescriptor/options)
- [var mask: UInt32](/documentation/metal/mtlaccelerationstructureuseridinstancedescriptor/mask)

#### Specifying the user identifier

- [var userID: UInt32](/documentation/metal/mtlaccelerationstructureuseridinstancedescriptor/userid)
- [MTLAccelerationStructureMotionInstanceDescriptor](/documentation/metal/mtlaccelerationstructuremotioninstancedescriptor)

#### Creating an instance descriptor

- [init()](/documentation/metal/mtlaccelerationstructuremotioninstancedescriptor/init())
- [init(options: MTLAccelerationStructureInstanceOptions, mask: UInt32, intersectionFunctionTableOffset: UInt32, accelerationStructureIndex: UInt32, userID: UInt32, motionTransformsStartIndex: UInt32, motionTransformsCount: UInt32, motionStartBorderMode: MTLMotionBorderMode, motionEndBorderMode: MTLMotionBorderMode, motionStartTime: Float, motionEndTime: Float)](/documentation/metal/mtlaccelerationstructuremotioninstancedescriptor/init(options:mask:intersectionfunctiontableoffset:accelerationstructureindex:userid:motiontransformsstartindex:motiontransformscount:motionstartbordermode:motionendbordermode:motionstarttime:motionendtime:))

#### Specifying the instance

- [var accelerationStructureIndex: UInt32](/documentation/metal/mtlaccelerationstructuremotioninstancedescriptor/accelerationstructureindex)

#### Specifying motion data

- [var motionStartTime: Float](/documentation/metal/mtlaccelerationstructuremotioninstancedescriptor/motionstarttime)
- [var motionEndTime: Float](/documentation/metal/mtlaccelerationstructuremotioninstancedescriptor/motionendtime)
- [var motionStartBorderMode: MTLMotionBorderMode](/documentation/metal/mtlaccelerationstructuremotioninstancedescriptor/motionstartbordermode)
- [var motionEndBorderMode: MTLMotionBorderMode](/documentation/metal/mtlaccelerationstructuremotioninstancedescriptor/motionendbordermode)
- [var motionTransformsStartIndex: UInt32](/documentation/metal/mtlaccelerationstructuremotioninstancedescriptor/motiontransformsstartindex)
- [var motionTransformsCount: UInt32](/documentation/metal/mtlaccelerationstructuremotioninstancedescriptor/motiontransformscount)

#### Customizing intersection and hit tests for the instance

- [var intersectionFunctionTableOffset: UInt32](/documentation/metal/mtlaccelerationstructuremotioninstancedescriptor/intersectionfunctiontableoffset)
- [var options: MTLAccelerationStructureInstanceOptions](/documentation/metal/mtlaccelerationstructuremotioninstancedescriptor/options)
- [var mask: UInt32](/documentation/metal/mtlaccelerationstructuremotioninstancedescriptor/mask)

#### Specifying the user identifier

- [var userID: UInt32](/documentation/metal/mtlaccelerationstructuremotioninstancedescriptor/userid)
- [MTLAccelerationStructureInstanceOptions](/documentation/metal/mtlaccelerationstructureinstanceoptions)

#### Creating instance flags

- [init(rawValue: UInt32)](/documentation/metal/mtlaccelerationstructureinstanceoptions/init(rawvalue:))

#### Usage options

- [static var disableTriangleCulling: MTLAccelerationStructureInstanceOptions](/documentation/metal/mtlaccelerationstructureinstanceoptions/disabletriangleculling)
- [static var triangleFrontFacingWindingCounterClockwise: MTLAccelerationStructureInstanceOptions](/documentation/metal/mtlaccelerationstructureinstanceoptions/trianglefrontfacingwindingcounterclockwise)
- [static var opaque: MTLAccelerationStructureInstanceOptions](/documentation/metal/mtlaccelerationstructureinstanceoptions/opaque)
- [static var nonOpaque: MTLAccelerationStructureInstanceOptions](/documentation/metal/mtlaccelerationstructureinstanceoptions/nonopaque)
- [MTL4IndirectInstanceAccelerationStructureDescriptor](/documentation/metal/mtl4indirectinstanceaccelerationstructuredescriptor)

#### Instance Properties

- [var instanceCountBuffer: MTL4BufferRange](/documentation/metal/mtl4indirectinstanceaccelerationstructuredescriptor/instancecountbuffer)
- [var instanceDescriptorBuffer: MTL4BufferRange](/documentation/metal/mtl4indirectinstanceaccelerationstructuredescriptor/instancedescriptorbuffer)
- [var instanceDescriptorStride: Int](/documentation/metal/mtl4indirectinstanceaccelerationstructuredescriptor/instancedescriptorstride)
- [var instanceDescriptorType: MTLAccelerationStructureInstanceDescriptorType](/documentation/metal/mtl4indirectinstanceaccelerationstructuredescriptor/instancedescriptortype)
- [var instanceTransformationMatrixLayout: MTLMatrixLayout](/documentation/metal/mtl4indirectinstanceaccelerationstructuredescriptor/instancetransformationmatrixlayout)
- [var maxInstanceCount: Int](/documentation/metal/mtl4indirectinstanceaccelerationstructuredescriptor/maxinstancecount)
- [var maxMotionTransformCount: Int](/documentation/metal/mtl4indirectinstanceaccelerationstructuredescriptor/maxmotiontransformcount)
- [var motionTransformBuffer: MTL4BufferRange](/documentation/metal/mtl4indirectinstanceaccelerationstructuredescriptor/motiontransformbuffer)
- [var motionTransformCountBuffer: MTL4BufferRange](/documentation/metal/mtl4indirectinstanceaccelerationstructuredescriptor/motiontransformcountbuffer)
- [var motionTransformStride: Int](/documentation/metal/mtl4indirectinstanceaccelerationstructuredescriptor/motiontransformstride)
- [var motionTransformType: MTLTransformType](/documentation/metal/mtl4indirectinstanceaccelerationstructuredescriptor/motiontransformtype)
- [MTLIndirectInstanceAccelerationStructureDescriptor](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor)

#### Instance Properties

- [var instanceCountBuffer: (any MTLBuffer)?](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/instancecountbuffer)
- [var instanceCountBufferOffset: Int](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/instancecountbufferoffset)
- [var instanceDescriptorBuffer: (any MTLBuffer)?](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/instancedescriptorbuffer)
- [var instanceDescriptorBufferOffset: Int](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/instancedescriptorbufferoffset)
- [var instanceDescriptorStride: Int](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/instancedescriptorstride)
- [var instanceDescriptorType: MTLAccelerationStructureInstanceDescriptorType](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/instancedescriptortype)
- [var instanceTransformationMatrixLayout: MTLMatrixLayout](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/instancetransformationmatrixlayout)
- [var maxInstanceCount: Int](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/maxinstancecount)
- [var maxMotionTransformCount: Int](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/maxmotiontransformcount)
- [var motionTransformBuffer: (any MTLBuffer)?](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/motiontransformbuffer)
- [var motionTransformBufferOffset: Int](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/motiontransformbufferoffset)
- [var motionTransformCountBuffer: (any MTLBuffer)?](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/motiontransformcountbuffer)
- [var motionTransformCountBufferOffset: Int](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/motiontransformcountbufferoffset)
- [var motionTransformStride: Int](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/motiontransformstride)
- [var motionTransformType: MTLTransformType](/documentation/metal/mtlindirectinstanceaccelerationstructuredescriptor/motiontransformtype)
- [MTLIndirectAccelerationStructureInstanceDescriptor](/documentation/metal/mtlindirectaccelerationstructureinstancedescriptor)

#### Initializers

- [init()](/documentation/metal/mtlindirectaccelerationstructureinstancedescriptor/init())
- [init(transformationMatrix: MTLPackedFloat4x3, options: MTLAccelerationStructureInstanceOptions, mask: UInt32, intersectionFunctionTableOffset: UInt32, userID: UInt32, accelerationStructureID: MTLResourceID)](/documentation/metal/mtlindirectaccelerationstructureinstancedescriptor/init(transformationmatrix:options:mask:intersectionfunctiontableoffset:userid:accelerationstructureid:))

#### Instance Properties

- [var accelerationStructureID: MTLResourceID](/documentation/metal/mtlindirectaccelerationstructureinstancedescriptor/accelerationstructureid)
- [var intersectionFunctionTableOffset: UInt32](/documentation/metal/mtlindirectaccelerationstructureinstancedescriptor/intersectionfunctiontableoffset)
- [var mask: UInt32](/documentation/metal/mtlindirectaccelerationstructureinstancedescriptor/mask)
- [var options: MTLAccelerationStructureInstanceOptions](/documentation/metal/mtlindirectaccelerationstructureinstancedescriptor/options)
- [var transformationMatrix: MTLPackedFloat4x3](/documentation/metal/mtlindirectaccelerationstructureinstancedescriptor/transformationmatrix)
- [var userID: UInt32](/documentation/metal/mtlindirectaccelerationstructureinstancedescriptor/userid)
- [MTLIndirectAccelerationStructureMotionInstanceDescriptor](/documentation/metal/mtlindirectaccelerationstructuremotioninstancedescriptor)

#### Specifying the instance

- [var accelerationStructureID: MTLResourceID](/documentation/metal/mtlindirectaccelerationstructuremotioninstancedescriptor/accelerationstructureid)

#### Specifying motion data

- [var motionStartTime: Float](/documentation/metal/mtlindirectaccelerationstructuremotioninstancedescriptor/motionstarttime)
- [var motionStartBorderMode: MTLMotionBorderMode](/documentation/metal/mtlindirectaccelerationstructuremotioninstancedescriptor/motionstartbordermode)
- [var motionEndTime: Float](/documentation/metal/mtlindirectaccelerationstructuremotioninstancedescriptor/motionendtime)
- [var motionEndBorderMode: MTLMotionBorderMode](/documentation/metal/mtlindirectaccelerationstructuremotioninstancedescriptor/motionendbordermode)
- [var motionTransformsCount: UInt32](/documentation/metal/mtlindirectaccelerationstructuremotioninstancedescriptor/motiontransformscount)
- [var motionTransformsStartIndex: UInt32](/documentation/metal/mtlindirectaccelerationstructuremotioninstancedescriptor/motiontransformsstartindex)

#### Specifying the user identifier

- [var userID: UInt32](/documentation/metal/mtlindirectaccelerationstructuremotioninstancedescriptor/userid)

#### Initializers

- [init()](/documentation/metal/mtlindirectaccelerationstructuremotioninstancedescriptor/init())
- [init(options: MTLAccelerationStructureInstanceOptions, mask: UInt32, intersectionFunctionTableOffset: UInt32, userID: UInt32, accelerationStructureID: MTLResourceID, motionTransformsStartIndex: UInt32, motionTransformsCount: UInt32, motionStartBorderMode: MTLMotionBorderMode, motionEndBorderMode: MTLMotionBorderMode, motionStartTime: Float, motionEndTime: Float)](/documentation/metal/mtlindirectaccelerationstructuremotioninstancedescriptor/init(options:mask:intersectionfunctiontableoffset:userid:accelerationstructureid:motiontransformsstartindex:motiontransformscount:motionstartbordermode:motionendbordermode:motionstarttime:motionendtime:))

#### Instance Properties

- [var intersectionFunctionTableOffset: UInt32](/documentation/metal/mtlindirectaccelerationstructuremotioninstancedescriptor/intersectionfunctiontableoffset)
- [var mask: UInt32](/documentation/metal/mtlindirectaccelerationstructuremotioninstancedescriptor/mask)
- [var options: MTLAccelerationStructureInstanceOptions](/documentation/metal/mtlindirectaccelerationstructuremotioninstancedescriptor/options)

### Intersection function tables

- [MTLIntersectionFunctionTable](/documentation/metal/mtlintersectionfunctiontable)

#### Setting a table entry

- [func setFunction((any MTLFunctionHandle)?, index: Int)](/documentation/metal/mtlintersectionfunctiontable/setfunction(_:index:))
- [func setFunctions([(any MTLFunctionHandle)?], range: Range<Int>)](/documentation/metal/mtlintersectionfunctiontable/setfunctions(_:range:))

#### Specifying arguments for intersection functions

- [func setBuffer((any MTLBuffer)?, offset: Int, index: Int)](/documentation/metal/mtlintersectionfunctiontable/setbuffer(_:offset:index:))
- [- setBuffers:offsets:withRange:](/documentation/metal/mtlintersectionfunctiontable/setbuffers(_:offsets:range:))
- [func setVisibleFunctionTable((any MTLVisibleFunctionTable)?, bufferIndex: Int)](/documentation/metal/mtlintersectionfunctiontable/setvisiblefunctiontable(_:bufferindex:))
- [- setVisibleFunctionTables:withBufferRange:](/documentation/metal/mtlintersectionfunctiontable/setvisiblefunctiontables(_:bufferrange:))

#### Specifying opaque triangle intersection testing

- [func setOpaqueTriangleIntersectionFunction(signature: MTLIntersectionFunctionSignature, index: Int)](/documentation/metal/mtlintersectionfunctiontable/setopaquetriangleintersectionfunction(signature:index:))
- [func setOpaqueTriangleIntersectionFunction(signature: MTLIntersectionFunctionSignature, range: NSRange)](/documentation/metal/mtlintersectionfunctiontable/setopaquetriangleintersectionfunction(signature:range:))

#### Instance Properties

- [var gpuResourceID: MTLResourceID](/documentation/metal/mtlintersectionfunctiontable/gpuresourceid)

#### Instance Methods

- [func setOpaqueCurveIntersectionFunction(signature: MTLIntersectionFunctionSignature, index: Int)](/documentation/metal/mtlintersectionfunctiontable/setopaquecurveintersectionfunction(signature:index:))
- [func setOpaqueCurveIntersectionFunction(signature: MTLIntersectionFunctionSignature, range: NSRange)](/documentation/metal/mtlintersectionfunctiontable/setopaquecurveintersectionfunction(signature:range:))
- [MTLIntersectionFunctionTableDescriptor](/documentation/metal/mtlintersectionfunctiontabledescriptor)

#### Configuring the table’s size

- [var functionCount: Int](/documentation/metal/mtlintersectionfunctiontabledescriptor/functioncount)
- [MTLIntersectionFunctionDescriptor](/documentation/metal/mtlintersectionfunctiondescriptor)
- [MTLIntersectionFunctionSignature](/documentation/metal/mtlintersectionfunctionsignature)

#### Initializing the intersection function signature

- [init(rawValue: UInt)](/documentation/metal/mtlintersectionfunctionsignature/init(rawvalue:))

#### Specifying the intersection function signature

- [static var instancing: MTLIntersectionFunctionSignature](/documentation/metal/mtlintersectionfunctionsignature/instancing)
- [static var triangleData: MTLIntersectionFunctionSignature](/documentation/metal/mtlintersectionfunctionsignature/triangledata)
- [static var worldSpaceData: MTLIntersectionFunctionSignature](/documentation/metal/mtlintersectionfunctionsignature/worldspacedata)

#### Type Properties

- [static var curveData: MTLIntersectionFunctionSignature](/documentation/metal/mtlintersectionfunctionsignature/curvedata)
- [static var extendedLimits: MTLIntersectionFunctionSignature](/documentation/metal/mtlintersectionfunctionsignature/extendedlimits)
- [static var instanceMotion: MTLIntersectionFunctionSignature](/documentation/metal/mtlintersectionfunctionsignature/instancemotion)
- [static var intersectionFunctionBuffer: MTLIntersectionFunctionSignature](/documentation/metal/mtlintersectionfunctionsignature/intersectionfunctionbuffer)
- [static var maxLevels: MTLIntersectionFunctionSignature](/documentation/metal/mtlintersectionfunctionsignature/maxlevels)
- [static var primitiveMotion: MTLIntersectionFunctionSignature](/documentation/metal/mtlintersectionfunctionsignature/primitivemotion)
- [static var userData: MTLIntersectionFunctionSignature](/documentation/metal/mtlintersectionfunctionsignature/userdata)
- [MTLIntersectionFunctionBufferArguments](/documentation/metal/mtlintersectionfunctionbufferarguments)

#### Initializers

- [init()](/documentation/metal/mtlintersectionfunctionbufferarguments/init())
- [init(intersectionFunctionBuffer: UInt64, intersectionFunctionBufferSize: UInt64, intersectionFunctionStride: UInt64)](/documentation/metal/mtlintersectionfunctionbufferarguments/init(intersectionfunctionbuffer:intersectionfunctionbuffersize:intersectionfunctionstride:))

#### Instance Properties

- [var intersectionFunctionBuffer: UInt64](/documentation/metal/mtlintersectionfunctionbufferarguments/intersectionfunctionbuffer)
- [var intersectionFunctionBufferSize: UInt64](/documentation/metal/mtlintersectionfunctionbufferarguments/intersectionfunctionbuffersize)
- [var intersectionFunctionStride: UInt64](/documentation/metal/mtlintersectionfunctionbufferarguments/intersectionfunctionstride)

### Supporting types

- [MTLAxisAlignedBoundingBox](/documentation/metal/mtlaxisalignedboundingbox-swift.typealias)
- [MTLPackedFloat3](/documentation/metal/mtlpackedfloat3-swift.typealias)
- [MTLPackedFloat4x3](/documentation/metal/mtlpackedfloat4x3-swift.typealias)
- [func MTLPackedFloat3Make(Float, Float, Float) -> MTLPackedFloat3](/documentation/metal/mtlpackedfloat3make(_:_:_:))
- [MTL4BufferRange](/documentation/metal/mtl4bufferrange)

#### Initializers

- [init()](/documentation/metal/mtl4bufferrange/init())
- [init(bufferAddress: MTLGPUAddress, length: UInt64)](/documentation/metal/mtl4bufferrange/init(bufferaddress:length:))

#### Instance Properties

- [var bufferAddress: MTLGPUAddress](/documentation/metal/mtl4bufferrange/bufferaddress)
- [var length: UInt64](/documentation/metal/mtl4bufferrange/length)
- [func MTL4BufferRangeMake(MTLGPUAddress, UInt64) -> MTL4BufferRange](/documentation/metal/mtl4bufferrangemake(_:_:))

## Resources

- [Resource fundamentals](/documentation/metal/resource-fundamentals)

### Resource management

- [Setting resource storage modes](/documentation/metal/setting-resource-storage-modes)
- [Choosing a resource storage mode for Apple GPUs](/documentation/metal/choosing-a-resource-storage-mode-for-apple-gpus)
- [Choosing a resource storage mode for Intel and AMD GPUs](/documentation/metal/choosing-a-resource-storage-mode-for-intel-and-amd-gpus)
- [Copying data to a private resource](/documentation/metal/copying-data-to-a-private-resource)
- [Synchronizing a managed resource in macOS](/documentation/metal/synchronizing-a-managed-resource-in-macos)
- [Transferring data between connected GPUs](/documentation/metal/transferring-data-between-connected-gpus)
- [Reducing the memory footprint of Metal apps](/documentation/metal/reducing-the-memory-footprint-of-metal-apps)

### Residency sets

- [Simplifying GPU resource management with residency sets](/documentation/metal/simplifying-gpu-resource-management-with-residency-sets)
- [MTLResidencySet](/documentation/metal/mtlresidencyset)

#### Adding allocations

- [func addAllocation(any MTLAllocation)](/documentation/metal/mtlresidencyset/addallocation(_:))
- [- addAllocations:count:](/documentation/metal/mtlresidencyset/addallocations(_:))

#### Removing allocations

- [func removeAllAllocations()](/documentation/metal/mtlresidencyset/removeallallocations())
- [func removeAllocation(any MTLAllocation)](/documentation/metal/mtlresidencyset/removeallocation(_:))
- [- removeAllocations:count:](/documentation/metal/mtlresidencyset/removeallocations(_:))

#### Finalizing pending allocation changes

- [func commit()](/documentation/metal/mtlresidencyset/commit())

#### Requesting residency for the allocations

- [func requestResidency()](/documentation/metal/mtlresidencyset/requestresidency())

#### Releasing the allocations from residency

- [func endResidency()](/documentation/metal/mtlresidencyset/endresidency())

#### Inspecting a residency set

- [var label: String?](/documentation/metal/mtlresidencyset/label)
- [var device: any MTLDevice](/documentation/metal/mtlresidencyset/device)
- [func containsAllocation(any MTLAllocation) -> Bool](/documentation/metal/mtlresidencyset/containsallocation(_:))
- [var allAllocations: [any MTLAllocation]](/documentation/metal/mtlresidencyset/allallocations)
- [var allocationCount: Int](/documentation/metal/mtlresidencyset/allocationcount)
- [var allocatedSize: UInt64](/documentation/metal/mtlresidencyset/allocatedsize)
- [MTLResidencySetDescriptor](/documentation/metal/mtlresidencysetdescriptor)

#### Configuring the residency set

- [var label: String?](/documentation/metal/mtlresidencysetdescriptor/label)
- [var initialCapacity: Int](/documentation/metal/mtlresidencysetdescriptor/initialcapacity)

### View pools

- [MTLResourceViewPool](/documentation/metal/mtlresourceviewpool)

#### Instance Properties

- [var baseResourceID: MTLResourceID](/documentation/metal/mtlresourceviewpool/baseresourceid)
- [var device: any MTLDevice](/documentation/metal/mtlresourceviewpool/device)
- [var label: String?](/documentation/metal/mtlresourceviewpool/label)
- [var resourceViewCount: Int](/documentation/metal/mtlresourceviewpool/resourceviewcount)

#### Instance Methods

- [func copyResourceViews(sourcePool: any MTLResourceViewPool, sourceRange: Range<Int>, destinationIndex: Int) -> MTLResourceID](/documentation/metal/mtlresourceviewpool/copyresourceviews(sourcepool:sourcerange:destinationindex:))
- [MTLResourceViewPoolDescriptor](/documentation/metal/mtlresourceviewpooldescriptor)

#### Instance Properties

- [var label: String?](/documentation/metal/mtlresourceviewpooldescriptor/label)
- [var resourceViewCount: Int](/documentation/metal/mtlresourceviewpooldescriptor/resourceviewcount)
- [MTLTextureViewPool](/documentation/metal/mtltextureviewpool)

#### Instance Methods

- [func setTextureView(buffer: any MTLBuffer, descriptor: MTLTextureDescriptor, offset: Int, bytesPerRow: Int, index: Int) -> MTLResourceID](/documentation/metal/mtltextureviewpool/settextureview(buffer:descriptor:offset:bytesperrow:index:))
- [func setTextureView(texture: any MTLTexture, descriptor: MTLTextureViewDescriptor, index: Int) -> MTLResourceID](/documentation/metal/mtltextureviewpool/settextureview(texture:descriptor:index:))
- [func setTextureView(texture: any MTLTexture, index: Int) -> MTLResourceID](/documentation/metal/mtltextureviewpool/settextureview(texture:index:))
- [MTLTextureViewDescriptor](/documentation/metal/mtltextureviewdescriptor)

#### Instance Properties

- [var levelRange: Range<Int>](/documentation/metal/mtltextureviewdescriptor/levelrange-55q8m)
- [var pixelFormat: MTLPixelFormat](/documentation/metal/mtltextureviewdescriptor/pixelformat)
- [var sliceRange: Range<Int>](/documentation/metal/mtltextureviewdescriptor/slicerange-6nq6v)
- [var swizzle: MTLTextureSwizzleChannels](/documentation/metal/mtltextureviewdescriptor/swizzle)
- [var textureType: MTLTextureType](/documentation/metal/mtltextureviewdescriptor/texturetype)

### Tensors

- [MTLTensor](/documentation/metal/mtltensor)

#### Instance Properties

- [var buffer: (any MTLBuffer)?](/documentation/metal/mtltensor/buffer)
- [var bufferOffset: Int](/documentation/metal/mtltensor/bufferoffset)
- [var dataType: MTLTensorDataType](/documentation/metal/mtltensor/datatype)
- [var dimensions: MTLTensorExtents](/documentation/metal/mtltensor/dimensions)
- [var gpuResourceID: MTLResourceID](/documentation/metal/mtltensor/gpuresourceid)
- [var strides: MTLTensorExtents?](/documentation/metal/mtltensor/strides)
- [var usage: MTLTensorUsage](/documentation/metal/mtltensor/usage)

#### Instance Methods

- [func getBytes(UnsafeMutableRawPointer, strides: MTLTensorExtents, sliceOrigin: MTLTensorExtents, sliceDimensions: MTLTensorExtents)](/documentation/metal/mtltensor/getbytes(_:strides:sliceorigin:slicedimensions:))
- [func replace(sliceOrigin: MTLTensorExtents, sliceDimensions: MTLTensorExtents, withBytes: UnsafeRawPointer, strides: MTLTensorExtents)](/documentation/metal/mtltensor/replace(sliceorigin:slicedimensions:withbytes:strides:))
- [MTLTensorDescriptor](/documentation/metal/mtltensordescriptor)

#### Instance Properties

- [var cpuCacheMode: MTLCPUCacheMode](/documentation/metal/mtltensordescriptor/cpucachemode)
- [var dataType: MTLTensorDataType](/documentation/metal/mtltensordescriptor/datatype)
- [var dimensions: MTLTensorExtents](/documentation/metal/mtltensordescriptor/dimensions)
- [var hazardTrackingMode: MTLHazardTrackingMode](/documentation/metal/mtltensordescriptor/hazardtrackingmode)
- [var resourceOptions: MTLResourceOptions](/documentation/metal/mtltensordescriptor/resourceoptions)
- [var storageMode: MTLStorageMode](/documentation/metal/mtltensordescriptor/storagemode)
- [var strides: MTLTensorExtents?](/documentation/metal/mtltensordescriptor/strides)
- [var usage: MTLTensorUsage](/documentation/metal/mtltensordescriptor/usage)
- [MTLTensorExtents](/documentation/metal/mtltensorextents)

#### Initializers

- [convenience init?([Int])](/documentation/metal/mtltensorextents/init(_:))

#### Instance Properties

- [var extents: [Int]](/documentation/metal/mtltensorextents/extents)
- [var rank: Int](/documentation/metal/mtltensorextents/rank)
- [MTLTensorReferenceType](/documentation/metal/mtltensorreferencetype)

#### Instance Properties

- [var access: MTLBindingAccess](/documentation/metal/mtltensorreferencetype/access)
- [var dimensions: MTLTensorExtents?](/documentation/metal/mtltensorreferencetype/dimensions)
- [var indexType: MTLDataType](/documentation/metal/mtltensorreferencetype/indextype)
- [var tensorDataType: MTLTensorDataType](/documentation/metal/mtltensorreferencetype/tensordatatype)
- [MTLTensorUsage](/documentation/metal/mtltensorusage)

#### Initializers

- [init(rawValue: UInt)](/documentation/metal/mtltensorusage/init(rawvalue:))

#### Type Properties

- [static var compute: MTLTensorUsage](/documentation/metal/mtltensorusage/compute)
- [static var machineLearning: MTLTensorUsage](/documentation/metal/mtltensorusage/machinelearning)
- [static var render: MTLTensorUsage](/documentation/metal/mtltensorusage/render)
- [let MTLTensorDomain: String](/documentation/metal/mtltensordomain)
- [MTLTensorBinding](/documentation/metal/mtltensorbinding)

#### Instance Properties

- [var dimensions: MTLTensorExtents?](/documentation/metal/mtltensorbinding/dimensions)
- [var indexType: MTLDataType](/documentation/metal/mtltensorbinding/indextype)
- [var tensorDataType: MTLTensorDataType](/documentation/metal/mtltensorbinding/tensordatatype)
- [MTLTensorError](/documentation/metal/mtltensorerror-swift.struct)

#### Type Properties

- [static var errorDomain: String](/documentation/metal/mtltensorerror-swift.struct/errordomain)
- [static var internalError: MTLTensorError.Code](/documentation/metal/mtltensorerror-swift.struct/internalerror)
- [static var invalidDescriptor: MTLTensorError.Code](/documentation/metal/mtltensorerror-swift.struct/invaliddescriptor)
- [static var none: MTLTensorError.Code](/documentation/metal/mtltensorerror-swift.struct/none)
- [MTLTensorError.Code](/documentation/metal/mtltensorerror-swift.struct/code)

#### Enumeration Cases

- [case internalError](/documentation/metal/mtltensorerror-swift.struct/code/internalerror)
- [case invalidDescriptor](/documentation/metal/mtltensorerror-swift.struct/code/invaliddescriptor)
- [case none](/documentation/metal/mtltensorerror-swift.struct/code/none)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtltensorerror-swift.struct/code/init(rawvalue:))
- [MTLTensorDataType](/documentation/metal/mtltensordatatype)

#### Enumeration Cases

- [case bfloat16](/documentation/metal/mtltensordatatype/bfloat16)
- [case float16](/documentation/metal/mtltensordatatype/float16)
- [case float32](/documentation/metal/mtltensordatatype/float32)
- [case int16](/documentation/metal/mtltensordatatype/int16)
- [case int32](/documentation/metal/mtltensordatatype/int32)
- [case int8](/documentation/metal/mtltensordatatype/int8)
- [case none](/documentation/metal/mtltensordatatype/none)
- [case uint16](/documentation/metal/mtltensordatatype/uint16)
- [case uint32](/documentation/metal/mtltensordatatype/uint32)
- [case uint8](/documentation/metal/mtltensordatatype/uint8)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtltensordatatype/init(rawvalue:))
- [let MTLTensorDomain: String](/documentation/metal/mtltensordomain)
- [var MTL_TENSOR_MAX_RANK: Int32](/documentation/metal/mtl_tensor_max_rank)

### Sparse resources

- [MTLBufferSparseTier](/documentation/metal/mtlbuffersparsetier)

#### Enumeration Cases

- [case tier1](/documentation/metal/mtlbuffersparsetier/tier1)
- [case tierNone](/documentation/metal/mtlbuffersparsetier/tiernone)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlbuffersparsetier/init(rawvalue:))
- [MTL4CopySparseBufferMappingOperation](/documentation/metal/mtl4copysparsebuffermappingoperation)

#### Initializers

- [init()](/documentation/metal/mtl4copysparsebuffermappingoperation/init())
- [init(sourceRange: NSRange, destinationOffset: Int)](/documentation/metal/mtl4copysparsebuffermappingoperation/init(sourcerange:destinationoffset:))

#### Instance Properties

- [var destinationOffset: Int](/documentation/metal/mtl4copysparsebuffermappingoperation/destinationoffset)
- [var sourceRange: NSRange](/documentation/metal/mtl4copysparsebuffermappingoperation/sourcerange)
- [MTL4UpdateSparseBufferMappingOperation](/documentation/metal/mtl4updatesparsebuffermappingoperation)

#### Initializers

- [init()](/documentation/metal/mtl4updatesparsebuffermappingoperation/init())
- [init(mode: MTLSparseTextureMappingMode, bufferRange: NSRange, heapOffset: Int)](/documentation/metal/mtl4updatesparsebuffermappingoperation/init(mode:bufferrange:heapoffset:))

#### Instance Properties

- [var bufferRange: NSRange](/documentation/metal/mtl4updatesparsebuffermappingoperation/bufferrange)
- [var heapOffset: Int](/documentation/metal/mtl4updatesparsebuffermappingoperation/heapoffset)
- [var mode: MTLSparseTextureMappingMode](/documentation/metal/mtl4updatesparsebuffermappingoperation/mode)
- [MTLTextureSparseTier](/documentation/metal/mtltexturesparsetier)

#### Enumeration Cases

- [case tier1](/documentation/metal/mtltexturesparsetier/tier1)
- [case tier2](/documentation/metal/mtltexturesparsetier/tier2)
- [case tierNone](/documentation/metal/mtltexturesparsetier/tiernone)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtltexturesparsetier/init(rawvalue:))
- [MTL4CopySparseTextureMappingOperation](/documentation/metal/mtl4copysparsetexturemappingoperation)

#### Initializers

- [init()](/documentation/metal/mtl4copysparsetexturemappingoperation/init())
- [init(sourceRegion: MTLRegion, sourceLevel: Int, sourceSlice: Int, destinationOrigin: MTLOrigin, destinationLevel: Int, destinationSlice: Int)](/documentation/metal/mtl4copysparsetexturemappingoperation/init(sourceregion:sourcelevel:sourceslice:destinationorigin:destinationlevel:destinationslice:))

#### Instance Properties

- [var destinationLevel: Int](/documentation/metal/mtl4copysparsetexturemappingoperation/destinationlevel)
- [var destinationOrigin: MTLOrigin](/documentation/metal/mtl4copysparsetexturemappingoperation/destinationorigin)
- [var destinationSlice: Int](/documentation/metal/mtl4copysparsetexturemappingoperation/destinationslice)
- [var sourceLevel: Int](/documentation/metal/mtl4copysparsetexturemappingoperation/sourcelevel)
- [var sourceRegion: MTLRegion](/documentation/metal/mtl4copysparsetexturemappingoperation/sourceregion)
- [var sourceSlice: Int](/documentation/metal/mtl4copysparsetexturemappingoperation/sourceslice)
- [MTL4UpdateSparseTextureMappingOperation](/documentation/metal/mtl4updatesparsetexturemappingoperation)

#### Initializers

- [init()](/documentation/metal/mtl4updatesparsetexturemappingoperation/init())
- [init(mode: MTLSparseTextureMappingMode, textureRegion: MTLRegion, textureLevel: Int, textureSlice: Int, heapOffset: Int)](/documentation/metal/mtl4updatesparsetexturemappingoperation/init(mode:textureregion:texturelevel:textureslice:heapoffset:))

#### Instance Properties

- [var heapOffset: Int](/documentation/metal/mtl4updatesparsetexturemappingoperation/heapoffset)
- [var mode: MTLSparseTextureMappingMode](/documentation/metal/mtl4updatesparsetexturemappingoperation/mode)
- [var textureLevel: Int](/documentation/metal/mtl4updatesparsetexturemappingoperation/texturelevel)
- [var textureRegion: MTLRegion](/documentation/metal/mtl4updatesparsetexturemappingoperation/textureregion)
- [var textureSlice: Int](/documentation/metal/mtl4updatesparsetexturemappingoperation/textureslice)

### Common resource functionality

- [MTLGPUAddress](/documentation/metal/mtlgpuaddress)
- [MTLAllocation](/documentation/metal/mtlallocation)

#### Inspecting an allocation

- [var allocatedSize: Int](/documentation/metal/mtlallocation/allocatedsize)
- [MTLResource](/documentation/metal/mtlresource)

#### Identifying the resource

- [var device: any MTLDevice](/documentation/metal/mtlresource/device)
- [var label: String?](/documentation/metal/mtlresource/label)

#### Reading memory and storage properties

- [var cpuCacheMode: MTLCPUCacheMode](/documentation/metal/mtlresource/cpucachemode)
- [var storageMode: MTLStorageMode](/documentation/metal/mtlresource/storagemode)
- [var hazardTrackingMode: MTLHazardTrackingMode](/documentation/metal/mtlresource/hazardtrackingmode)
- [var resourceOptions: MTLResourceOptions](/documentation/metal/mtlresource/resourceoptions)
- [MTLCPUCacheMode](/documentation/metal/mtlcpucachemode)

##### Specifying the cache mode

- [case defaultCache](/documentation/metal/mtlcpucachemode/defaultcache)
- [case writeCombined](/documentation/metal/mtlcpucachemode/writecombined)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlcpucachemode/init(rawvalue:))
- [MTLStorageMode](/documentation/metal/mtlstoragemode)

##### Storage mode options

- [case shared](/documentation/metal/mtlstoragemode/shared)
- [case managed](/documentation/metal/mtlstoragemode/managed)
- [case `private`](/documentation/metal/mtlstoragemode/private)
- [case memoryless](/documentation/metal/mtlstoragemode/memoryless)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlstoragemode/init(rawvalue:))
- [MTLHazardTrackingMode](/documentation/metal/mtlhazardtrackingmode)

##### Selecting the tracking mode

- [case `default`](/documentation/metal/mtlhazardtrackingmode/default)
- [case untracked](/documentation/metal/mtlhazardtrackingmode/untracked)
- [case tracked](/documentation/metal/mtlhazardtrackingmode/tracked)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlhazardtrackingmode/init(rawvalue:))

#### Setting the purgeable state of the resource

- [func setPurgeableState(MTLPurgeableState) -> MTLPurgeableState](/documentation/metal/mtlresource/setpurgeablestate(_:))
- [MTLPurgeableState](/documentation/metal/mtlpurgeablestate)

##### Specifying purgeable states

- [case keepCurrent](/documentation/metal/mtlpurgeablestate/keepcurrent)
- [case nonVolatile](/documentation/metal/mtlpurgeablestate/nonvolatile)
- [case volatile](/documentation/metal/mtlpurgeablestate/volatile)
- [case empty](/documentation/metal/mtlpurgeablestate/empty)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlpurgeablestate/init(rawvalue:))

#### Managing heap resources

- [var heapOffset: Int](/documentation/metal/mtlresource/heapoffset)
- [var heap: (any MTLHeap)?](/documentation/metal/mtlresource/heap)
- [func makeAliasable()](/documentation/metal/mtlresource/makealiasable())
- [func isAliasable() -> Bool](/documentation/metal/mtlresource/isaliasable())

#### Querying the allocated size

- [var allocatedSize: Int](/documentation/metal/mtlresource/allocatedsize)
- [MTLResourceOptions](/documentation/metal/mtlresourceoptions)

#### Initializing resource options

- [init(rawValue: UInt)](/documentation/metal/mtlresourceoptions/init(rawvalue:))

#### Specifying CPU cache modes

- [static var cpuCacheModeWriteCombined: MTLResourceOptions](/documentation/metal/mtlresourceoptions/cpucachemodewritecombined)

#### Specifying storage modes

- [static var storageModeShared: MTLResourceOptions](/documentation/metal/mtlresourceoptions/storagemodeshared)
- [static var storageModeManaged: MTLResourceOptions](/documentation/metal/mtlresourceoptions/storagemodemanaged)
- [static var storageModePrivate: MTLResourceOptions](/documentation/metal/mtlresourceoptions/storagemodeprivate)
- [static var storageModeMemoryless: MTLResourceOptions](/documentation/metal/mtlresourceoptions/storagemodememoryless)

#### Specifying hazard tracking

- [static var hazardTrackingModeTracked: MTLResourceOptions](/documentation/metal/mtlresourceoptions/hazardtrackingmodetracked)
- [static var hazardTrackingModeUntracked: MTLResourceOptions](/documentation/metal/mtlresourceoptions/hazardtrackingmodeuntracked)

#### Deprecated options

- [static var optionCPUCacheModeWriteCombined: MTLResourceOptions](/documentation/metal/mtlresourceoptions/optioncpucachemodewritecombined)
- [MTLResourceUsage](/documentation/metal/mtlresourceusage)

#### Initializers

- [init(rawValue: UInt)](/documentation/metal/mtlresourceusage/init(rawvalue:))

#### Type Properties

- [static var read: MTLResourceUsage](/documentation/metal/mtlresourceusage/read)
- [static var sample: MTLResourceUsage](/documentation/metal/mtlresourceusage/sample)
- [static var write: MTLResourceUsage](/documentation/metal/mtlresourceusage/write)
- [MTLResourceID](/documentation/metal/mtlresourceid)

#### Initializers

- [init()](/documentation/metal/mtlresourceid/init())
- [Buffers](/documentation/metal/buffers)

### General purpose buffers

- [MTLBuffer](/documentation/metal/mtlbuffer)

#### Creating a texture that shares buffer data

- [func makeTexture(descriptor: MTLTextureDescriptor, offset: Int, bytesPerRow: Int) -> (any MTLTexture)?](/documentation/metal/mtlbuffer/maketexture(descriptor:offset:bytesperrow:))

#### Reading the buffer’s data on the CPU

- [func contents() -> UnsafeMutableRawPointer](/documentation/metal/mtlbuffer/contents())

#### Synchronizing data to the GPU for managed buffers

- [func didModifyRange(Range<Int>)](/documentation/metal/mtlbuffer/didmodifyrange(_:))

#### Debugging buffers

- [func addDebugMarker(String, range: Range<Int>)](/documentation/metal/mtlbuffer/adddebugmarker(_:range:))
- [func removeAllDebugMarkers()](/documentation/metal/mtlbuffer/removealldebugmarkers())

#### Reading buffer length

- [var length: Int](/documentation/metal/mtlbuffer/length)

#### Creating views of buffers on other GPUs

- [func makeRemoteBufferView(any MTLDevice) -> (any MTLBuffer)?](/documentation/metal/mtlbuffer/makeremotebufferview(_:))
- [var remoteStorageBuffer: (any MTLBuffer)?](/documentation/metal/mtlbuffer/remotestoragebuffer)

#### Instance Properties

- [var gpuAddress: MTLGPUAddress](/documentation/metal/mtlbuffer/gpuaddress)
- [var sparseBufferTier: MTLBufferSparseTier](/documentation/metal/mtlbuffer/sparsebuffertier)

#### Instance Methods

- [func makeTensor(descriptor: MTLTensorDescriptor, offset: Int) throws -> any MTLTensor](/documentation/metal/mtlbuffer/maketensor(descriptor:offset:))

### Argument buffers

- [Improving CPU performance by using argument buffers](/documentation/metal/improving-cpu-performance-by-using-argument-buffers)
- [Managing groups of resources with argument buffers](/documentation/metal/managing-groups-of-resources-with-argument-buffers)
- [Tracking the resource residency of argument buffers](/documentation/metal/tracking-the-resource-residency-of-argument-buffers)
- [Indexing argument buffers](/documentation/metal/indexing-argument-buffers)
- [Rendering terrain dynamically with argument buffers](/documentation/metal/rendering-terrain-dynamically-with-argument-buffers)
- [Encoding argument buffers on the GPU](/documentation/metal/encoding-argument-buffers-on-the-gpu)
- [Using argument buffers with resource heaps](/documentation/metal/using-argument-buffers-with-resource-heaps)
- [MTLArgumentDescriptor](/documentation/metal/mtlargumentdescriptor)

#### Setting the descriptor’s properties

- [var dataType: MTLDataType](/documentation/metal/mtlargumentdescriptor/datatype)
- [var index: Int](/documentation/metal/mtlargumentdescriptor/index)
- [var access: MTLBindingAccess](/documentation/metal/mtlargumentdescriptor/access)
- [var arrayLength: Int](/documentation/metal/mtlargumentdescriptor/arraylength)
- [var constantBlockAlignment: Int](/documentation/metal/mtlargumentdescriptor/constantblockalignment)
- [var textureType: MTLTextureType](/documentation/metal/mtlargumentdescriptor/texturetype)
- [MTLArgumentEncoder](/documentation/metal/mtlargumentencoder)

#### Creating an argument buffer

- [func setArgumentBuffer((any MTLBuffer)?, offset: Int)](/documentation/metal/mtlargumentencoder/setargumentbuffer(_:offset:))
- [func setArgumentBuffer((any MTLBuffer)?, startOffset: Int, arrayElement: Int)](/documentation/metal/mtlargumentencoder/setargumentbuffer(_:startoffset:arrayelement:))
- [var encodedLength: Int](/documentation/metal/mtlargumentencoder/encodedlength)

#### Encoding buffers

- [func setBuffer((any MTLBuffer)?, offset: Int, index: Int)](/documentation/metal/mtlargumentencoder/setbuffer(_:offset:index:))
- [- setBuffers:offsets:withRange:](/documentation/metal/mtlargumentencoder/setbuffers(_:offsets:range:))

#### Encoding textures

- [func setTexture((any MTLTexture)?, index: Int)](/documentation/metal/mtlargumentencoder/settexture(_:index:))
- [func setTextures([(any MTLTexture)?], range: Range<Int>)](/documentation/metal/mtlargumentencoder/settextures(_:range:))

#### Encoding samplers

- [func setSamplerState((any MTLSamplerState)?, index: Int)](/documentation/metal/mtlargumentencoder/setsamplerstate(_:index:))
- [- setSamplerStates:withRange:](/documentation/metal/mtlargumentencoder/setsamplerstates(_:range:))

#### Encoding pipeline states

- [func setRenderPipelineState((any MTLRenderPipelineState)?, index: Int)](/documentation/metal/mtlargumentencoder/setrenderpipelinestate(_:index:))
- [- setRenderPipelineStates:withRange:](/documentation/metal/mtlargumentencoder/setrenderpipelinestates(_:range:))
- [func setComputePipelineState((any MTLComputePipelineState)?, index: Int)](/documentation/metal/mtlargumentencoder/setcomputepipelinestate(_:index:))
- [- setComputePipelineStates:withRange:](/documentation/metal/mtlargumentencoder/setcomputepipelinestates(_:with:))
- [func setComputePipelineState((any MTLComputePipelineState)?, at: Int)](/documentation/metal/mtlargumentencoder/setcomputepipelinestate(_:at:))
- [func setComputePipelineStates([(any MTLComputePipelineState)?], range: Range<Int>)](/documentation/metal/mtlargumentencoder/setcomputepipelinestates(_:range:))

#### Encoding inlined constant data

- [func constantData(at: Int) -> UnsafeMutableRawPointer](/documentation/metal/mtlargumentencoder/constantdata(at:))

#### Encoding indirect command buffers

- [func setIndirectCommandBuffer((any MTLIndirectCommandBuffer)?, index: Int)](/documentation/metal/mtlargumentencoder/setindirectcommandbuffer(_:index:))
- [- setIndirectCommandBuffers:withRange:](/documentation/metal/mtlargumentencoder/setindirectcommandbuffers(_:range:))

#### Encoding acceleration structures

- [func setAccelerationStructure((any MTLAccelerationStructure)?, index: Int)](/documentation/metal/mtlargumentencoder/setaccelerationstructure(_:index:))

#### Encoding function tables

- [func setVisibleFunctionTable((any MTLVisibleFunctionTable)?, index: Int)](/documentation/metal/mtlargumentencoder/setvisiblefunctiontable(_:index:))
- [func setIntersectionFunctionTable((any MTLIntersectionFunctionTable)?, index: Int)](/documentation/metal/mtlargumentencoder/setintersectionfunctiontable(_:index:))
- [func setIntersectionFunctionTables([(any MTLIntersectionFunctionTable)?], range: Range<Int>)](/documentation/metal/mtlargumentencoder/setintersectionfunctiontables(_:range:))
- [- setVisibleFunctionTables:withRange:](/documentation/metal/mtlargumentencoder/setvisiblefunctiontables(_:range:))

#### Creating a nested argument encoder

- [func makeArgumentEncoderForBuffer(atIndex: Int) -> (any MTLArgumentEncoder)?](/documentation/metal/mtlargumentencoder/makeargumentencoderforbuffer(atindex:))

#### Querying alignment

- [var alignment: Int](/documentation/metal/mtlargumentencoder/alignment)

#### Identifying the argument encoder

- [var label: String?](/documentation/metal/mtlargumentencoder/label)
- [var device: any MTLDevice](/documentation/metal/mtlargumentencoder/device)

#### Instance Methods

- [func setDepthStencilState((any MTLDepthStencilState)?, index: Int)](/documentation/metal/mtlargumentencoder/setdepthstencilstate(_:index:))
- [func setDepthStencilStates([(any MTLDepthStencilState)?], range: Range<Int>)](/documentation/metal/mtlargumentencoder/setdepthstencilstates(_:range:))
- [let MTLAttributeStrideStatic: Int](/documentation/metal/mtlattributestridestatic)

### Model I/O interoperability

- [MTKMesh](/documentation/metalkit/mtkmesh)
- [MTKMeshBuffer](/documentation/metalkit/mtkmeshbuffer)
- [MTKMeshBufferAllocator](/documentation/metalkit/mtkmeshbufferallocator)
- [MTKSubmesh](/documentation/metalkit/mtksubmesh)
- [MTKModelError](/documentation/metalkit/mtkmodelerror)
- [func MTKMetalVertexFormatFromModelIO(MDLVertexFormat) -> MTLVertexFormat](/documentation/metalkit/mtkmetalvertexformatfrommodelio(_:))
- [func MTKModelIOVertexFormatFromMetal(MTLVertexFormat) -> MDLVertexFormat](/documentation/metalkit/mtkmodeliovertexformatfrommetal(_:))
- [func MTKMetalVertexDescriptorFromModelIO(MDLVertexDescriptor) -> MTLVertexDescriptor?](/documentation/metalkit/mtkmetalvertexdescriptorfrommodelio(_:))
- [func MTKModelIOVertexDescriptorFromMetal(MTLVertexDescriptor) -> MDLVertexDescriptor](/documentation/metalkit/mtkmodeliovertexdescriptorfrommetal(_:))
- [Textures](/documentation/metal/textures)

### Texture basics

- [Understanding color-renderable pixel format sizes](/documentation/metal/understanding-color-renderable-pixel-format-sizes)
- [Optimizing texture data](/documentation/metal/optimizing-texture-data)
- [MTLTexture](/documentation/metal/mtltexture)

#### Copying data into a texture image

- [func replace(region: MTLRegion, mipmapLevel: Int, slice: Int, withBytes: UnsafeRawPointer, bytesPerRow: Int, bytesPerImage: Int)](/documentation/metal/mtltexture/replace(region:mipmaplevel:slice:withbytes:bytesperrow:bytesperimage:))
- [func replace(region: MTLRegion, mipmapLevel: Int, withBytes: UnsafeRawPointer, bytesPerRow: Int)](/documentation/metal/mtltexture/replace(region:mipmaplevel:withbytes:bytesperrow:))

#### Copying data from a texture image

- [func getBytes(UnsafeMutableRawPointer, bytesPerRow: Int, bytesPerImage: Int, from: MTLRegion, mipmapLevel: Int, slice: Int)](/documentation/metal/mtltexture/getbytes(_:bytesperrow:bytesperimage:from:mipmaplevel:slice:))
- [func getBytes(UnsafeMutableRawPointer, bytesPerRow: Int, from: MTLRegion, mipmapLevel: Int)](/documentation/metal/mtltexture/getbytes(_:bytesperrow:from:mipmaplevel:))

#### Creating textures by reinterpreting existing texture data

- [func makeTextureView(pixelFormat: MTLPixelFormat) -> (any MTLTexture)?](/documentation/metal/mtltexture/maketextureview(pixelformat:))
- [- newTextureViewWithPixelFormat:textureType:levels:slices:](/documentation/metal/mtltexture/maketextureview(pixelformat:texturetype:levels:slices:))
- [- newTextureViewWithPixelFormat:textureType:levels:slices:swizzle:](/documentation/metal/mtltexture/maketextureview(pixelformat:texturetype:levels:slices:swizzle:))

#### Querying texture attributes

- [var textureType: MTLTextureType](/documentation/metal/mtltexture/texturetype)
- [var pixelFormat: MTLPixelFormat](/documentation/metal/mtltexture/pixelformat)
- [var width: Int](/documentation/metal/mtltexture/width)
- [var height: Int](/documentation/metal/mtltexture/height)
- [var depth: Int](/documentation/metal/mtltexture/depth)
- [var mipmapLevelCount: Int](/documentation/metal/mtltexture/mipmaplevelcount)
- [var arrayLength: Int](/documentation/metal/mtltexture/arraylength)
- [var sampleCount: Int](/documentation/metal/mtltexture/samplecount)
- [var isFramebufferOnly: Bool](/documentation/metal/mtltexture/isframebufferonly)
- [var usage: MTLTextureUsage](/documentation/metal/mtltexture/usage)
- [var allowGPUOptimizedContents: Bool](/documentation/metal/mtltexture/allowgpuoptimizedcontents)
- [var isShareable: Bool](/documentation/metal/mtltexture/isshareable)
- [var swizzle: MTLTextureSwizzleChannels](/documentation/metal/mtltexture/swizzle)
- [MTLTextureType](/documentation/metal/mtltexturetype)

##### Specifying the texture type

- [case type1D](/documentation/metal/mtltexturetype/type1d)
- [case type1DArray](/documentation/metal/mtltexturetype/type1darray)
- [case type2D](/documentation/metal/mtltexturetype/type2d)
- [case type2DArray](/documentation/metal/mtltexturetype/type2darray)
- [case type2DMultisample](/documentation/metal/mtltexturetype/type2dmultisample)
- [case typeCube](/documentation/metal/mtltexturetype/typecube)
- [case typeCubeArray](/documentation/metal/mtltexturetype/typecubearray)
- [case type3D](/documentation/metal/mtltexturetype/type3d)
- [case type2DMultisampleArray](/documentation/metal/mtltexturetype/type2dmultisamplearray)
- [case typeTextureBuffer](/documentation/metal/mtltexturetype/typetexturebuffer)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtltexturetype/init(rawvalue:))
- [MTLTextureUsage](/documentation/metal/mtltextureusage)

##### Specifying texture usage options

- [static var unknown: MTLTextureUsage](/documentation/metal/mtltextureusage/unknown)
- [static var shaderRead: MTLTextureUsage](/documentation/metal/mtltextureusage/shaderread)
- [static var shaderWrite: MTLTextureUsage](/documentation/metal/mtltextureusage/shaderwrite)
- [static var shaderAtomic: MTLTextureUsage](/documentation/metal/mtltextureusage/shaderatomic)
- [static var renderTarget: MTLTextureUsage](/documentation/metal/mtltextureusage/rendertarget)
- [static var pixelFormatView: MTLTextureUsage](/documentation/metal/mtltextureusage/pixelformatview)

##### Creating texture usage options

- [init(rawValue: UInt)](/documentation/metal/mtltextureusage/init(rawvalue:))

#### Getting information about the IOSurface the texture was created from

- [var iosurface: IOSurfaceRef?](/documentation/metal/mtltexture/iosurface)
- [var iosurfacePlane: Int](/documentation/metal/mtltexture/iosurfaceplane)

#### Getting information about ancestor resources

- [var parent: (any MTLTexture)?](/documentation/metal/mtltexture/parent)
- [var parentRelativeLevel: Int](/documentation/metal/mtltexture/parentrelativelevel)
- [var parentRelativeSlice: Int](/documentation/metal/mtltexture/parentrelativeslice)
- [var buffer: (any MTLBuffer)?](/documentation/metal/mtltexture/buffer)
- [var bufferOffset: Int](/documentation/metal/mtltexture/bufferoffset)
- [var bufferBytesPerRow: Int](/documentation/metal/mtltexture/bufferbytesperrow)
- [var rootResource: (any MTLResource)?](/documentation/metal/mtltexture/rootresource)

#### Creating a shared texture handle

- [func makeSharedTextureHandle() -> MTLSharedTextureHandle?](/documentation/metal/mtltexture/makesharedtexturehandle())

#### Creating views of textures on other GPUs

- [func makeRemoteTextureView(any MTLDevice) -> (any MTLTexture)?](/documentation/metal/mtltexture/makeremotetextureview(_:))
- [var remoteStorageTexture: (any MTLTexture)?](/documentation/metal/mtltexture/remotestoragetexture)

#### Querying sparse properties

- [var isSparse: Bool](/documentation/metal/mtltexture/issparse)
- [var firstMipmapInTail: Int](/documentation/metal/mtltexture/firstmipmapintail)
- [var tailSizeInBytes: Int](/documentation/metal/mtltexture/tailsizeinbytes)

#### Instance Properties

- [var compressionType: MTLTextureCompressionType](/documentation/metal/mtltexture/compressiontype)
- [var gpuResourceID: MTLResourceID](/documentation/metal/mtltexture/gpuresourceid)
- [var sparseTextureTier: MTLTextureSparseTier](/documentation/metal/mtltexture/sparsetexturetier)

#### Instance Methods

- [func newTextureView(with: MTLTextureViewDescriptor) -> (any MTLTexture)?](/documentation/metal/mtltexture/newtextureview(with:))
- [MTLTextureCompressionType](/documentation/metal/mtltexturecompressiontype)

#### Enumeration Cases

- [case lossless](/documentation/metal/mtltexturecompressiontype/lossless)
- [case lossy](/documentation/metal/mtltexturecompressiontype/lossy)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtltexturecompressiontype/init(rawvalue:))
- [MTLTextureDescriptor](/documentation/metal/mtltexturedescriptor)

#### Creating texture descriptors

- [class func texture2DDescriptor(pixelFormat: MTLPixelFormat, width: Int, height: Int, mipmapped: Bool) -> MTLTextureDescriptor](/documentation/metal/mtltexturedescriptor/texture2ddescriptor(pixelformat:width:height:mipmapped:))
- [class func textureCubeDescriptor(pixelFormat: MTLPixelFormat, size: Int, mipmapped: Bool) -> MTLTextureDescriptor](/documentation/metal/mtltexturedescriptor/texturecubedescriptor(pixelformat:size:mipmapped:))
- [class func textureBufferDescriptor(with: MTLPixelFormat, width: Int, resourceOptions: MTLResourceOptions, usage: MTLTextureUsage) -> MTLTextureDescriptor](/documentation/metal/mtltexturedescriptor/texturebufferdescriptor(with:width:resourceoptions:usage:))

#### Specifying texture attributes

- [var textureType: MTLTextureType](/documentation/metal/mtltexturedescriptor/texturetype)
- [var pixelFormat: MTLPixelFormat](/documentation/metal/mtltexturedescriptor/pixelformat)
- [var width: Int](/documentation/metal/mtltexturedescriptor/width)
- [var height: Int](/documentation/metal/mtltexturedescriptor/height)
- [var depth: Int](/documentation/metal/mtltexturedescriptor/depth)
- [var mipmapLevelCount: Int](/documentation/metal/mtltexturedescriptor/mipmaplevelcount)
- [var sampleCount: Int](/documentation/metal/mtltexturedescriptor/samplecount)
- [var arrayLength: Int](/documentation/metal/mtltexturedescriptor/arraylength)
- [var resourceOptions: MTLResourceOptions](/documentation/metal/mtltexturedescriptor/resourceoptions)
- [var cpuCacheMode: MTLCPUCacheMode](/documentation/metal/mtltexturedescriptor/cpucachemode)
- [var storageMode: MTLStorageMode](/documentation/metal/mtltexturedescriptor/storagemode)
- [var hazardTrackingMode: MTLHazardTrackingMode](/documentation/metal/mtltexturedescriptor/hazardtrackingmode)
- [var allowGPUOptimizedContents: Bool](/documentation/metal/mtltexturedescriptor/allowgpuoptimizedcontents)
- [var usage: MTLTextureUsage](/documentation/metal/mtltexturedescriptor/usage)
- [var swizzle: MTLTextureSwizzleChannels](/documentation/metal/mtltexturedescriptor/swizzle)
- [MTLTextureSwizzleChannels](/documentation/metal/mtltextureswizzlechannels)

##### Creating a swizzle pattern

- [init()](/documentation/metal/mtltextureswizzlechannels/init())
- [MTLTextureSwizzleChannelsMake](/documentation/metal/mtltextureswizzlechannels/init(red:green:blue:alpha:))

##### Specifying swizzle values

- [var red: MTLTextureSwizzle](/documentation/metal/mtltextureswizzlechannels/red)
- [var green: MTLTextureSwizzle](/documentation/metal/mtltextureswizzlechannels/green)
- [var blue: MTLTextureSwizzle](/documentation/metal/mtltextureswizzlechannels/blue)
- [var alpha: MTLTextureSwizzle](/documentation/metal/mtltextureswizzlechannels/alpha)
- [MTLTextureSwizzle](/documentation/metal/mtltextureswizzle)

##### Specifying swizzle channels

- [case alpha](/documentation/metal/mtltextureswizzle/alpha)
- [case blue](/documentation/metal/mtltextureswizzle/blue)
- [case green](/documentation/metal/mtltextureswizzle/green)
- [case red](/documentation/metal/mtltextureswizzle/red)
- [case one](/documentation/metal/mtltextureswizzle/one)
- [case zero](/documentation/metal/mtltextureswizzle/zero)

##### Initializers

- [init?(rawValue: UInt8)](/documentation/metal/mtltextureswizzle/init(rawvalue:))
- [MTLTextureType](/documentation/metal/mtltexturetype)

##### Specifying the texture type

- [case type1D](/documentation/metal/mtltexturetype/type1d)
- [case type1DArray](/documentation/metal/mtltexturetype/type1darray)
- [case type2D](/documentation/metal/mtltexturetype/type2d)
- [case type2DArray](/documentation/metal/mtltexturetype/type2darray)
- [case type2DMultisample](/documentation/metal/mtltexturetype/type2dmultisample)
- [case typeCube](/documentation/metal/mtltexturetype/typecube)
- [case typeCubeArray](/documentation/metal/mtltexturetype/typecubearray)
- [case type3D](/documentation/metal/mtltexturetype/type3d)
- [case type2DMultisampleArray](/documentation/metal/mtltexturetype/type2dmultisamplearray)
- [case typeTextureBuffer](/documentation/metal/mtltexturetype/typetexturebuffer)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtltexturetype/init(rawvalue:))
- [MTLTextureUsage](/documentation/metal/mtltextureusage)

##### Specifying texture usage options

- [static var unknown: MTLTextureUsage](/documentation/metal/mtltextureusage/unknown)
- [static var shaderRead: MTLTextureUsage](/documentation/metal/mtltextureusage/shaderread)
- [static var shaderWrite: MTLTextureUsage](/documentation/metal/mtltextureusage/shaderwrite)
- [static var shaderAtomic: MTLTextureUsage](/documentation/metal/mtltextureusage/shaderatomic)
- [static var renderTarget: MTLTextureUsage](/documentation/metal/mtltextureusage/rendertarget)
- [static var pixelFormatView: MTLTextureUsage](/documentation/metal/mtltextureusage/pixelformatview)

##### Creating texture usage options

- [init(rawValue: UInt)](/documentation/metal/mtltextureusage/init(rawvalue:))

#### Instance Properties

- [var compressionType: MTLTextureCompressionType](/documentation/metal/mtltexturedescriptor/compressiontype)
- [var placementSparsePageSize: MTLSparsePageSize](/documentation/metal/mtltexturedescriptor/placementsparsepagesize)
- [MTKTextureLoader](/documentation/metalkit/mtktextureloader)
- [MTLSharedTextureHandle](/documentation/metal/mtlsharedtexturehandle)

#### Identifying the shared texture handle

- [var device: any MTLDevice](/documentation/metal/mtlsharedtexturehandle/device)
- [var label: String?](/documentation/metal/mtlsharedtexturehandle/label)
- [MTLPixelFormat](/documentation/metal/mtlpixelformat)

#### Ordinary 8-bit pixel formats

- [case a8Unorm](/documentation/metal/mtlpixelformat/a8unorm)
- [case r8Unorm](/documentation/metal/mtlpixelformat/r8unorm)
- [case r8Unorm_srgb](/documentation/metal/mtlpixelformat/r8unorm_srgb)
- [case r8Snorm](/documentation/metal/mtlpixelformat/r8snorm)
- [case r8Uint](/documentation/metal/mtlpixelformat/r8uint)
- [case r8Sint](/documentation/metal/mtlpixelformat/r8sint)

#### Ordinary 16-bit pixel formats

- [case r16Unorm](/documentation/metal/mtlpixelformat/r16unorm)
- [case r16Snorm](/documentation/metal/mtlpixelformat/r16snorm)
- [case r16Uint](/documentation/metal/mtlpixelformat/r16uint)
- [case r16Sint](/documentation/metal/mtlpixelformat/r16sint)
- [case r16Float](/documentation/metal/mtlpixelformat/r16float)
- [case rg8Unorm](/documentation/metal/mtlpixelformat/rg8unorm)
- [case rg8Unorm_srgb](/documentation/metal/mtlpixelformat/rg8unorm_srgb)
- [case rg8Snorm](/documentation/metal/mtlpixelformat/rg8snorm)
- [case rg8Uint](/documentation/metal/mtlpixelformat/rg8uint)
- [case rg8Sint](/documentation/metal/mtlpixelformat/rg8sint)

#### Packed 16-bit pixel formats

- [case b5g6r5Unorm](/documentation/metal/mtlpixelformat/b5g6r5unorm)
- [case a1bgr5Unorm](/documentation/metal/mtlpixelformat/a1bgr5unorm)
- [case abgr4Unorm](/documentation/metal/mtlpixelformat/abgr4unorm)
- [case bgr5A1Unorm](/documentation/metal/mtlpixelformat/bgr5a1unorm)

#### Ordinary 32-bit pixel formats

- [case r32Uint](/documentation/metal/mtlpixelformat/r32uint)
- [case r32Sint](/documentation/metal/mtlpixelformat/r32sint)
- [case r32Float](/documentation/metal/mtlpixelformat/r32float)
- [case rg16Unorm](/documentation/metal/mtlpixelformat/rg16unorm)
- [case rg16Snorm](/documentation/metal/mtlpixelformat/rg16snorm)
- [case rg16Uint](/documentation/metal/mtlpixelformat/rg16uint)
- [case rg16Sint](/documentation/metal/mtlpixelformat/rg16sint)
- [case rg16Float](/documentation/metal/mtlpixelformat/rg16float)
- [case rgba8Unorm](/documentation/metal/mtlpixelformat/rgba8unorm)
- [case rgba8Unorm_srgb](/documentation/metal/mtlpixelformat/rgba8unorm_srgb)
- [case rgba8Snorm](/documentation/metal/mtlpixelformat/rgba8snorm)
- [case rgba8Uint](/documentation/metal/mtlpixelformat/rgba8uint)
- [case rgba8Sint](/documentation/metal/mtlpixelformat/rgba8sint)
- [case bgra8Unorm](/documentation/metal/mtlpixelformat/bgra8unorm)
- [case bgra8Unorm_srgb](/documentation/metal/mtlpixelformat/bgra8unorm_srgb)

#### Packed 32-bit pixel formats

- [case bgr10a2Unorm](/documentation/metal/mtlpixelformat/bgr10a2unorm)
- [case rgb10a2Unorm](/documentation/metal/mtlpixelformat/rgb10a2unorm)
- [case rgb10a2Uint](/documentation/metal/mtlpixelformat/rgb10a2uint)
- [case rg11b10Float](/documentation/metal/mtlpixelformat/rg11b10float)
- [case rgb9e5Float](/documentation/metal/mtlpixelformat/rgb9e5float)

#### Ordinary 64-bit pixel formats

- [case rg32Uint](/documentation/metal/mtlpixelformat/rg32uint)
- [case rg32Sint](/documentation/metal/mtlpixelformat/rg32sint)
- [case rg32Float](/documentation/metal/mtlpixelformat/rg32float)
- [case rgba16Unorm](/documentation/metal/mtlpixelformat/rgba16unorm)
- [case rgba16Snorm](/documentation/metal/mtlpixelformat/rgba16snorm)
- [case rgba16Uint](/documentation/metal/mtlpixelformat/rgba16uint)
- [case rgba16Sint](/documentation/metal/mtlpixelformat/rgba16sint)
- [case rgba16Float](/documentation/metal/mtlpixelformat/rgba16float)

#### Ordinary 128-bit pixel formats

- [case rgba32Uint](/documentation/metal/mtlpixelformat/rgba32uint)
- [case rgba32Sint](/documentation/metal/mtlpixelformat/rgba32sint)
- [case rgba32Float](/documentation/metal/mtlpixelformat/rgba32float)

#### Compressed PVRTC pixel formats

- [case pvrtc_rgb_2bpp](/documentation/metal/mtlpixelformat/pvrtc_rgb_2bpp)
- [case pvrtc_rgb_2bpp_srgb](/documentation/metal/mtlpixelformat/pvrtc_rgb_2bpp_srgb)
- [case pvrtc_rgb_4bpp](/documentation/metal/mtlpixelformat/pvrtc_rgb_4bpp)
- [case pvrtc_rgb_4bpp_srgb](/documentation/metal/mtlpixelformat/pvrtc_rgb_4bpp_srgb)
- [case pvrtc_rgba_2bpp](/documentation/metal/mtlpixelformat/pvrtc_rgba_2bpp)
- [case pvrtc_rgba_2bpp_srgb](/documentation/metal/mtlpixelformat/pvrtc_rgba_2bpp_srgb)
- [case pvrtc_rgba_4bpp](/documentation/metal/mtlpixelformat/pvrtc_rgba_4bpp)
- [case pvrtc_rgba_4bpp_srgb](/documentation/metal/mtlpixelformat/pvrtc_rgba_4bpp_srgb)

#### Compressed EAC/ETC pixel formats

- [case eac_r11Unorm](/documentation/metal/mtlpixelformat/eac_r11unorm)
- [case eac_r11Snorm](/documentation/metal/mtlpixelformat/eac_r11snorm)
- [case eac_rg11Unorm](/documentation/metal/mtlpixelformat/eac_rg11unorm)
- [case eac_rg11Snorm](/documentation/metal/mtlpixelformat/eac_rg11snorm)
- [case eac_rgba8](/documentation/metal/mtlpixelformat/eac_rgba8)
- [case eac_rgba8_srgb](/documentation/metal/mtlpixelformat/eac_rgba8_srgb)
- [case etc2_rgb8](/documentation/metal/mtlpixelformat/etc2_rgb8)
- [case etc2_rgb8_srgb](/documentation/metal/mtlpixelformat/etc2_rgb8_srgb)
- [case etc2_rgb8a1](/documentation/metal/mtlpixelformat/etc2_rgb8a1)
- [case etc2_rgb8a1_srgb](/documentation/metal/mtlpixelformat/etc2_rgb8a1_srgb)

#### Compressed ASTC pixel formats

- [case astc_4x4_srgb](/documentation/metal/mtlpixelformat/astc_4x4_srgb)
- [case astc_5x4_srgb](/documentation/metal/mtlpixelformat/astc_5x4_srgb)
- [case astc_5x5_srgb](/documentation/metal/mtlpixelformat/astc_5x5_srgb)
- [case astc_6x5_srgb](/documentation/metal/mtlpixelformat/astc_6x5_srgb)
- [case astc_6x6_srgb](/documentation/metal/mtlpixelformat/astc_6x6_srgb)
- [case astc_8x5_srgb](/documentation/metal/mtlpixelformat/astc_8x5_srgb)
- [case astc_8x6_srgb](/documentation/metal/mtlpixelformat/astc_8x6_srgb)
- [case astc_8x8_srgb](/documentation/metal/mtlpixelformat/astc_8x8_srgb)
- [case astc_10x5_srgb](/documentation/metal/mtlpixelformat/astc_10x5_srgb)
- [case astc_10x6_srgb](/documentation/metal/mtlpixelformat/astc_10x6_srgb)
- [case astc_10x8_srgb](/documentation/metal/mtlpixelformat/astc_10x8_srgb)
- [case astc_10x10_srgb](/documentation/metal/mtlpixelformat/astc_10x10_srgb)
- [case astc_12x10_srgb](/documentation/metal/mtlpixelformat/astc_12x10_srgb)
- [case astc_12x12_srgb](/documentation/metal/mtlpixelformat/astc_12x12_srgb)
- [case astc_4x4_ldr](/documentation/metal/mtlpixelformat/astc_4x4_ldr)
- [case astc_5x4_ldr](/documentation/metal/mtlpixelformat/astc_5x4_ldr)
- [case astc_5x5_ldr](/documentation/metal/mtlpixelformat/astc_5x5_ldr)
- [case astc_6x5_ldr](/documentation/metal/mtlpixelformat/astc_6x5_ldr)
- [case astc_6x6_ldr](/documentation/metal/mtlpixelformat/astc_6x6_ldr)
- [case astc_8x5_ldr](/documentation/metal/mtlpixelformat/astc_8x5_ldr)
- [case astc_8x6_ldr](/documentation/metal/mtlpixelformat/astc_8x6_ldr)
- [case astc_8x8_ldr](/documentation/metal/mtlpixelformat/astc_8x8_ldr)
- [case astc_10x5_ldr](/documentation/metal/mtlpixelformat/astc_10x5_ldr)
- [case astc_10x6_ldr](/documentation/metal/mtlpixelformat/astc_10x6_ldr)
- [case astc_10x8_ldr](/documentation/metal/mtlpixelformat/astc_10x8_ldr)
- [case astc_10x10_ldr](/documentation/metal/mtlpixelformat/astc_10x10_ldr)
- [case astc_12x10_ldr](/documentation/metal/mtlpixelformat/astc_12x10_ldr)
- [case astc_12x12_ldr](/documentation/metal/mtlpixelformat/astc_12x12_ldr)
- [case astc_4x4_hdr](/documentation/metal/mtlpixelformat/astc_4x4_hdr)
- [case astc_5x4_hdr](/documentation/metal/mtlpixelformat/astc_5x4_hdr)
- [case astc_5x5_hdr](/documentation/metal/mtlpixelformat/astc_5x5_hdr)
- [case astc_6x5_hdr](/documentation/metal/mtlpixelformat/astc_6x5_hdr)
- [case astc_6x6_hdr](/documentation/metal/mtlpixelformat/astc_6x6_hdr)
- [case astc_8x5_hdr](/documentation/metal/mtlpixelformat/astc_8x5_hdr)
- [case astc_8x6_hdr](/documentation/metal/mtlpixelformat/astc_8x6_hdr)
- [case astc_8x8_hdr](/documentation/metal/mtlpixelformat/astc_8x8_hdr)
- [case astc_10x5_hdr](/documentation/metal/mtlpixelformat/astc_10x5_hdr)
- [case astc_10x6_hdr](/documentation/metal/mtlpixelformat/astc_10x6_hdr)
- [case astc_10x8_hdr](/documentation/metal/mtlpixelformat/astc_10x8_hdr)
- [case astc_10x10_hdr](/documentation/metal/mtlpixelformat/astc_10x10_hdr)
- [case astc_12x10_hdr](/documentation/metal/mtlpixelformat/astc_12x10_hdr)
- [case astc_12x12_hdr](/documentation/metal/mtlpixelformat/astc_12x12_hdr)

#### Compressed BC pixel formats

- [case bc1_rgba](/documentation/metal/mtlpixelformat/bc1_rgba)
- [case bc1_rgba_srgb](/documentation/metal/mtlpixelformat/bc1_rgba_srgb)
- [case bc2_rgba](/documentation/metal/mtlpixelformat/bc2_rgba)
- [case bc2_rgba_srgb](/documentation/metal/mtlpixelformat/bc2_rgba_srgb)
- [case bc3_rgba](/documentation/metal/mtlpixelformat/bc3_rgba)
- [case bc3_rgba_srgb](/documentation/metal/mtlpixelformat/bc3_rgba_srgb)
- [case bc4_rUnorm](/documentation/metal/mtlpixelformat/bc4_runorm)
- [case bc4_rSnorm](/documentation/metal/mtlpixelformat/bc4_rsnorm)
- [case bc5_rgUnorm](/documentation/metal/mtlpixelformat/bc5_rgunorm)
- [case bc5_rgSnorm](/documentation/metal/mtlpixelformat/bc5_rgsnorm)
- [case bc6H_rgbFloat](/documentation/metal/mtlpixelformat/bc6h_rgbfloat)
- [case bc6H_rgbuFloat](/documentation/metal/mtlpixelformat/bc6h_rgbufloat)
- [case bc7_rgbaUnorm](/documentation/metal/mtlpixelformat/bc7_rgbaunorm)
- [case bc7_rgbaUnorm_srgb](/documentation/metal/mtlpixelformat/bc7_rgbaunorm_srgb)

#### YUV pixel formats

- [case gbgr422](/documentation/metal/mtlpixelformat/gbgr422)
- [case bgrg422](/documentation/metal/mtlpixelformat/bgrg422)

#### Depth and stencil pixel formats

- [case depth16Unorm](/documentation/metal/mtlpixelformat/depth16unorm)
- [case depth32Float](/documentation/metal/mtlpixelformat/depth32float)
- [case stencil8](/documentation/metal/mtlpixelformat/stencil8)
- [case depth24Unorm_stencil8](/documentation/metal/mtlpixelformat/depth24unorm_stencil8)
- [case depth32Float_stencil8](/documentation/metal/mtlpixelformat/depth32float_stencil8)
- [case x32_stencil8](/documentation/metal/mtlpixelformat/x32_stencil8)
- [case x24_stencil8](/documentation/metal/mtlpixelformat/x24_stencil8)

#### Extended range and wide color pixel formats

- [case bgra10_xr](/documentation/metal/mtlpixelformat/bgra10_xr)
- [case bgra10_xr_srgb](/documentation/metal/mtlpixelformat/bgra10_xr_srgb)
- [case bgr10_xr](/documentation/metal/mtlpixelformat/bgr10_xr)
- [case bgr10_xr_srgb](/documentation/metal/mtlpixelformat/bgr10_xr_srgb)

#### Invalid pixel format

- [case invalid](/documentation/metal/mtlpixelformat/invalid)

#### Enumeration Cases

- [case unspecialized](/documentation/metal/mtlpixelformat/unspecialized)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlpixelformat/init(rawvalue:))

### Texture samplers

- [Creating and sampling textures](/documentation/metal/creating-and-sampling-textures)
- [MTLSamplerState](/documentation/metal/mtlsamplerstate)

#### Identifying the sampler

- [var device: any MTLDevice](/documentation/metal/mtlsamplerstate/device)
- [var label: String?](/documentation/metal/mtlsamplerstate/label)

#### Instance Properties

- [var gpuResourceID: MTLResourceID](/documentation/metal/mtlsamplerstate/gpuresourceid)
- [MTLSamplerDescriptor](/documentation/metal/mtlsamplerdescriptor)

#### Declaring the coordinate space

- [var normalizedCoordinates: Bool](/documentation/metal/mtlsamplerdescriptor/normalizedcoordinates)

#### Declaring addressing modes

- [var rAddressMode: MTLSamplerAddressMode](/documentation/metal/mtlsamplerdescriptor/raddressmode)
- [var sAddressMode: MTLSamplerAddressMode](/documentation/metal/mtlsamplerdescriptor/saddressmode)
- [var tAddressMode: MTLSamplerAddressMode](/documentation/metal/mtlsamplerdescriptor/taddressmode)
- [var borderColor: MTLSamplerBorderColor](/documentation/metal/mtlsamplerdescriptor/bordercolor)
- [MTLSamplerAddressMode](/documentation/metal/mtlsampleraddressmode)

##### Address mode options

- [case clampToEdge](/documentation/metal/mtlsampleraddressmode/clamptoedge)
- [case mirrorClampToEdge](/documentation/metal/mtlsampleraddressmode/mirrorclamptoedge)
- [case `repeat`](/documentation/metal/mtlsampleraddressmode/repeat)
- [case mirrorRepeat](/documentation/metal/mtlsampleraddressmode/mirrorrepeat)
- [case clampToZero](/documentation/metal/mtlsampleraddressmode/clamptozero)
- [case clampToBorderColor](/documentation/metal/mtlsampleraddressmode/clamptobordercolor)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlsampleraddressmode/init(rawvalue:))
- [MTLSamplerBorderColor](/documentation/metal/mtlsamplerbordercolor)

##### Specifying border color options

- [case transparentBlack](/documentation/metal/mtlsamplerbordercolor/transparentblack)
- [case opaqueBlack](/documentation/metal/mtlsamplerbordercolor/opaqueblack)
- [case opaqueWhite](/documentation/metal/mtlsamplerbordercolor/opaquewhite)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlsamplerbordercolor/init(rawvalue:))

#### Declaring filter modes

- [var minFilter: MTLSamplerMinMagFilter](/documentation/metal/mtlsamplerdescriptor/minfilter)
- [var magFilter: MTLSamplerMinMagFilter](/documentation/metal/mtlsamplerdescriptor/magfilter)
- [var mipFilter: MTLSamplerMipFilter](/documentation/metal/mtlsamplerdescriptor/mipfilter)
- [var lodMinClamp: Float](/documentation/metal/mtlsamplerdescriptor/lodminclamp)
- [var lodMaxClamp: Float](/documentation/metal/mtlsamplerdescriptor/lodmaxclamp)
- [var lodAverage: Bool](/documentation/metal/mtlsamplerdescriptor/lodaverage)
- [var maxAnisotropy: Int](/documentation/metal/mtlsamplerdescriptor/maxanisotropy)
- [MTLSamplerMinMagFilter](/documentation/metal/mtlsamplerminmagfilter)

##### Filter options

- [case nearest](/documentation/metal/mtlsamplerminmagfilter/nearest)
- [case linear](/documentation/metal/mtlsamplerminmagfilter/linear)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlsamplerminmagfilter/init(rawvalue:))
- [MTLSamplerMipFilter](/documentation/metal/mtlsamplermipfilter)

##### Specifying mip filter options

- [case notMipmapped](/documentation/metal/mtlsamplermipfilter/notmipmapped)
- [case nearest](/documentation/metal/mtlsamplermipfilter/nearest)
- [case linear](/documentation/metal/mtlsamplermipfilter/linear)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlsamplermipfilter/init(rawvalue:))

#### Declaring the depth comparison mode

- [var compareFunction: MTLCompareFunction](/documentation/metal/mtlsamplerdescriptor/comparefunction)
- [MTLCompareFunction](/documentation/metal/mtlcomparefunction)

##### Compare function options

- [case never](/documentation/metal/mtlcomparefunction/never)
- [case less](/documentation/metal/mtlcomparefunction/less)
- [case equal](/documentation/metal/mtlcomparefunction/equal)
- [case lessEqual](/documentation/metal/mtlcomparefunction/lessequal)
- [case greater](/documentation/metal/mtlcomparefunction/greater)
- [case notEqual](/documentation/metal/mtlcomparefunction/notequal)
- [case greaterEqual](/documentation/metal/mtlcomparefunction/greaterequal)
- [case always](/documentation/metal/mtlcomparefunction/always)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlcomparefunction/init(rawvalue:))

#### Declaring whether the sampler can be used in argument buffers

- [var supportArgumentBuffers: Bool](/documentation/metal/mtlsamplerdescriptor/supportargumentbuffers)

#### Identifying the sampler

- [var label: String?](/documentation/metal/mtlsamplerdescriptor/label)

#### Instance Properties

- [var lodBias: Float](/documentation/metal/mtlsamplerdescriptor/lodbias)
- [var reductionMode: MTLSamplerReductionMode](/documentation/metal/mtlsamplerdescriptor/reductionmode)
- [MTLSamplePosition](/documentation/metal/mtlsampleposition)

#### Initializers

- [init()](/documentation/metal/mtlsampleposition/init())
- [init(x: Float, y: Float)](/documentation/metal/mtlsampleposition/init(x:y:))

#### Instance Properties

- [var x: Float](/documentation/metal/mtlsampleposition/x)
- [var y: Float](/documentation/metal/mtlsampleposition/y)
- [MTLSamplerReductionMode](/documentation/metal/mtlsamplerreductionmode)

#### Enumeration Cases

- [case maximum](/documentation/metal/mtlsamplerreductionmode/maximum)
- [case minimum](/documentation/metal/mtlsamplerreductionmode/minimum)
- [case weightedAverage](/documentation/metal/mtlsamplerreductionmode/weightedaverage)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlsamplerreductionmode/init(rawvalue:))

### Texture mipmapping

- [Improving texture sampling quality and performance with mipmaps](/documentation/metal/improving-texture-sampling-quality-and-performance-with-mipmaps)
- [Creating a mipmapped texture](/documentation/metal/creating-a-mipmapped-texture)
- [Copying data into or out of mipmaps](/documentation/metal/copying-data-into-or-out-of-mipmaps)
- [Generating mipmap data](/documentation/metal/generating-mipmap-data)
- [Adding mipmap filtering to samplers](/documentation/metal/adding-mipmap-filtering-to-samplers)
- [Restricting access to specific mipmaps](/documentation/metal/restricting-access-to-specific-mipmaps)
- [Predicting which mips the GPU samples with level-of-detail queries](/documentation/metal/predicting-which-mips-the-gpu-samples-with-level-of-detail-queries)
- [Dynamically adjusting texture level of detail](/documentation/metal/dynamically-adjusting-texture-level-of-detail)

### Sparse textures

- [Managing sparse texture memory](/documentation/metal/managing-sparse-texture-memory)
- [Creating sparse heaps and sparse textures](/documentation/metal/creating-sparse-heaps-and-sparse-textures)
- [Converting between pixel regions and sparse tile regions](/documentation/metal/converting-between-pixel-regions-and-sparse-tile-regions)
- [Assigning memory to sparse textures](/documentation/metal/assigning-memory-to-sparse-textures)
- [Reading and writing to sparse textures](/documentation/metal/reading-and-writing-to-sparse-textures)
- [Estimating how often a texture region is accessed](/documentation/metal/estimating-how-often-a-texture-region-is-accessed)
- [MTLResourceStatePassDescriptor](/documentation/metal/mtlresourcestatepassdescriptor)

#### Specifying sample buffers for GPU counters

- [var sampleBufferAttachments: MTLResourceStatePassSampleBufferAttachmentDescriptorArray](/documentation/metal/mtlresourcestatepassdescriptor/samplebufferattachments)
- [MTLResourceStatePassSampleBufferAttachmentDescriptor](/documentation/metal/mtlresourcestatepasssamplebufferattachmentdescriptor)

#### Configuring the sample buffer attachment

- [var sampleBuffer: (any MTLCounterSampleBuffer)?](/documentation/metal/mtlresourcestatepasssamplebufferattachmentdescriptor/samplebuffer)
- [var startOfEncoderSampleIndex: Int](/documentation/metal/mtlresourcestatepasssamplebufferattachmentdescriptor/startofencodersampleindex)
- [var endOfEncoderSampleIndex: Int](/documentation/metal/mtlresourcestatepasssamplebufferattachmentdescriptor/endofencodersampleindex)
- [MTLResourceStatePassSampleBufferAttachmentDescriptorArray](/documentation/metal/mtlresourcestatepasssamplebufferattachmentdescriptorarray)

#### Accessing a sample buffer attachment

- [subscript(Int) -> MTLResourceStatePassSampleBufferAttachmentDescriptor!](/documentation/metal/mtlresourcestatepasssamplebufferattachmentdescriptorarray/subscript(_:))
- [MTLResourceStateCommandEncoder](/documentation/metal/mtlresourcestatecommandencoder)

#### Updating texture memory assignments

- [func updateTextureMapping(any MTLTexture, mode: MTLSparseTextureMappingMode, region: MTLRegion, mipLevel: Int, slice: Int)](/documentation/metal/mtlresourcestatecommandencoder/updatetexturemapping(_:mode:region:miplevel:slice:))
- [func updateTextureMappings(any MTLTexture, mode: MTLSparseTextureMappingMode, regions: UnsafePointer<MTLRegion>, mipLevels: UnsafePointer<Int>, slices: UnsafePointer<Int>, numRegions: Int)](/documentation/metal/mtlresourcestatecommandencoder/updatetexturemappings(_:mode:regions:miplevels:slices:numregions:))
- [MTLSparseTextureMappingMode](/documentation/metal/mtlsparsetexturemappingmode)

##### Specifying the mapping mode

- [case map](/documentation/metal/mtlsparsetexturemappingmode/map)
- [case unmap](/documentation/metal/mtlsparsetexturemappingmode/unmap)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlsparsetexturemappingmode/init(rawvalue:))

#### Updating texture memory assignments indirectly

- [func updateTextureMapping(any MTLTexture, mode: MTLSparseTextureMappingMode, indirectBuffer: any MTLBuffer, indirectBufferOffset: Int)](/documentation/metal/mtlresourcestatecommandencoder/updatetexturemapping(_:mode:indirectbuffer:indirectbufferoffset:))

#### Performing fence operations

- [func update(any MTLFence)](/documentation/metal/mtlresourcestatecommandencoder/update(_:))
- [func wait(for: any MTLFence)](/documentation/metal/mtlresourcestatecommandencoder/wait(for:))

#### Instance Methods

- [func moveTextureMappings(sourceTexture: any MTLTexture, sourceSlice: Int, sourceLevel: Int, sourceOrigin: MTLOrigin, sourceSize: MTLSize, destinationTexture: any MTLTexture, destinationSlice: Int, destinationLevel: Int, destinationOrigin: MTLOrigin)](/documentation/metal/mtlresourcestatecommandencoder/movetexturemappings(sourcetexture:sourceslice:sourcelevel:sourceorigin:sourcesize:destinationtexture:destinationslice:destinationlevel:destinationorigin:))
- [MTLMapIndirectArguments](/documentation/metal/mtlmapindirectarguments)

#### Creating indirect mapping arguments

- [init()](/documentation/metal/mtlmapindirectarguments/init())
- [init(regionOriginX: UInt32, regionOriginY: UInt32, regionOriginZ: UInt32, regionSizeWidth: UInt32, regionSizeHeight: UInt32, regionSizeDepth: UInt32, mipMapLevel: UInt32, sliceId: UInt32)](/documentation/metal/mtlmapindirectarguments/init(regionoriginx:regionoriginy:regionoriginz:regionsizewidth:regionsizeheight:regionsizedepth:mipmaplevel:sliceid:))

#### Specifying region origin

- [var regionOriginX: UInt32](/documentation/metal/mtlmapindirectarguments/regionoriginx)
- [var regionOriginY: UInt32](/documentation/metal/mtlmapindirectarguments/regionoriginy)
- [var regionOriginZ: UInt32](/documentation/metal/mtlmapindirectarguments/regionoriginz)

#### Specifying region dimensions

- [var regionSizeWidth: UInt32](/documentation/metal/mtlmapindirectarguments/regionsizewidth)
- [var regionSizeHeight: UInt32](/documentation/metal/mtlmapindirectarguments/regionsizeheight)
- [var regionSizeDepth: UInt32](/documentation/metal/mtlmapindirectarguments/regionsizedepth)

#### Specifying texture location

- [var mipMapLevel: UInt32](/documentation/metal/mtlmapindirectarguments/mipmaplevel)
- [var sliceId: UInt32](/documentation/metal/mtlmapindirectarguments/sliceid)

### Texture loading

- [MTKTextureLoader](/documentation/metalkit/mtktextureloader)
- [MTKTextureLoader.Error](/documentation/metalkit/mtktextureloader/error)
- [MTKTextureLoader.Option](/documentation/metalkit/mtktextureloader/option)
- [MTKTextureLoader.Callback](/documentation/metalkit/mtktextureloader/callback)
- [MTKTextureLoader.ArrayCallback](/documentation/metalkit/mtktextureloader/arraycallback)
- [Memory heaps](/documentation/metal/memory-heaps)

### Resource memory allocation and management

- [Using argument buffers with resource heaps](/documentation/metal/using-argument-buffers-with-resource-heaps)
- [Implementing a multistage image filter using heaps and events](/documentation/metal/implementing-a-multistage-image-filter-using-heaps-and-events)
- [Implementing a multistage image filter using heaps and fences](/documentation/metal/implementing-a-multistage-image-filter-using-heaps-and-fences)
- [MTLHeap](/documentation/metal/mtlheap)

#### Naming and identifying a heap

- [var label: String?](/documentation/metal/mtlheap/label)

#### Creating buffers from a heap

- [func makeBuffer(length: Int, options: MTLResourceOptions) -> (any MTLBuffer)?](/documentation/metal/mtlheap/makebuffer(length:options:))
- [func makeBuffer(length: Int, options: MTLResourceOptions, offset: Int) -> (any MTLBuffer)?](/documentation/metal/mtlheap/makebuffer(length:options:offset:))

#### Creating textures from a heap

- [func makeTexture(descriptor: MTLTextureDescriptor) -> (any MTLTexture)?](/documentation/metal/mtlheap/maketexture(descriptor:))
- [func makeTexture(descriptor: MTLTextureDescriptor, offset: Int) -> (any MTLTexture)?](/documentation/metal/mtlheap/maketexture(descriptor:offset:))

#### Creating acceleration structure from a heap

- [func makeAccelerationStructure(size: Int) -> (any MTLAccelerationStructure)?](/documentation/metal/mtlheap/makeaccelerationstructure(size:))
- [func makeAccelerationStructure(size: Int, offset: Int) -> (any MTLAccelerationStructure)?](/documentation/metal/mtlheap/makeaccelerationstructure(size:offset:))
- [func makeAccelerationStructure(descriptor: MTLAccelerationStructureDescriptor) -> (any MTLAccelerationStructure)?](/documentation/metal/mtlheap/makeaccelerationstructure(descriptor:))
- [func makeAccelerationStructure(descriptor: MTLAccelerationStructureDescriptor, offset: Int) -> (any MTLAccelerationStructure)?](/documentation/metal/mtlheap/makeaccelerationstructure(descriptor:offset:))

#### Configuring a heap’s purgeable state

- [func setPurgeableState(MTLPurgeableState) -> MTLPurgeableState](/documentation/metal/mtlheap/setpurgeablestate(_:))

#### Checking a heap’s size information

- [func maxAvailableSize(alignment: Int) -> Int](/documentation/metal/mtlheap/maxavailablesize(alignment:))
- [var size: Int](/documentation/metal/mtlheap/size)
- [var usedSize: Int](/documentation/metal/mtlheap/usedsize)
- [var currentAllocatedSize: Int](/documentation/metal/mtlheap/currentallocatedsize)

#### Checking a heap’s permanent configuration

- [var device: any MTLDevice](/documentation/metal/mtlheap/device)
- [var type: MTLHeapType](/documentation/metal/mtlheap/type)
- [var storageMode: MTLStorageMode](/documentation/metal/mtlheap/storagemode)
- [var cpuCacheMode: MTLCPUCacheMode](/documentation/metal/mtlheap/cpucachemode)
- [var hazardTrackingMode: MTLHazardTrackingMode](/documentation/metal/mtlheap/hazardtrackingmode)
- [var resourceOptions: MTLResourceOptions](/documentation/metal/mtlheap/resourceoptions)
- [MTLHeapDescriptor](/documentation/metal/mtlheapdescriptor)

#### Configuring a heap

- [var type: MTLHeapType](/documentation/metal/mtlheapdescriptor/type)
- [var storageMode: MTLStorageMode](/documentation/metal/mtlheapdescriptor/storagemode)
- [var cpuCacheMode: MTLCPUCacheMode](/documentation/metal/mtlheapdescriptor/cpucachemode)
- [var hazardTrackingMode: MTLHazardTrackingMode](/documentation/metal/mtlheapdescriptor/hazardtrackingmode)
- [var resourceOptions: MTLResourceOptions](/documentation/metal/mtlheapdescriptor/resourceoptions)
- [var size: Int](/documentation/metal/mtlheapdescriptor/size)
- [var sparsePageSize: MTLSparsePageSize](/documentation/metal/mtlheapdescriptor/sparsepagesize)

#### Instance Properties

- [var maxCompatiblePlacementSparsePageSize: MTLSparsePageSize](/documentation/metal/mtlheapdescriptor/maxcompatibleplacementsparsepagesize)
- [MTLHeapType](/documentation/metal/mtlheaptype)

#### Specifying the heap type

- [case automatic](/documentation/metal/mtlheaptype/automatic)
- [case placement](/documentation/metal/mtlheaptype/placement)
- [case sparse](/documentation/metal/mtlheaptype/sparse)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlheaptype/init(rawvalue:))
- [MTLSizeAndAlign](/documentation/metal/mtlsizeandalign)

#### Accessing the size and alignment

- [var size: Int](/documentation/metal/mtlsizeandalign/size)
- [var align: Int](/documentation/metal/mtlsizeandalign/align)

#### Creating instances

- [init()](/documentation/metal/mtlsizeandalign/init())
- [init(size: Int, align: Int)](/documentation/metal/mtlsizeandalign/init(size:align:))
- [Resource loading](/documentation/metal/resource-loading)

### I/O command queues

- [MTLIOCommandQueue](/documentation/metal/mtliocommandqueue)

#### Creating a input/output command buffer

- [func makeCommandBuffer() -> any MTLIOCommandBuffer](/documentation/metal/mtliocommandqueue/makecommandbuffer())
- [func makeCommandBufferWithUnretainedReferences() -> any MTLIOCommandBuffer](/documentation/metal/mtliocommandqueue/makecommandbufferwithunretainedreferences())

#### Adding a barrier to the queue

- [func enqueueBarrier()](/documentation/metal/mtliocommandqueue/enqueuebarrier())

#### Naming the queue

- [var label: String?](/documentation/metal/mtliocommandqueue/label)
- [MTLIOCommandQueueDescriptor](/documentation/metal/mtliocommandqueuedescriptor)

#### Configuring the input/output command queue

- [var priority: MTLIOPriority](/documentation/metal/mtliocommandqueuedescriptor/priority)
- [var type: MTLIOCommandQueueType](/documentation/metal/mtliocommandqueuedescriptor/type)
- [var maxCommandsInFlight: Int](/documentation/metal/mtliocommandqueuedescriptor/maxcommandsinflight)
- [var maxCommandBufferCount: Int](/documentation/metal/mtliocommandqueuedescriptor/maxcommandbuffercount)

#### Providing your own a scratch buffer

- [var scratchBufferAllocator: (any MTLIOScratchBufferAllocator)?](/documentation/metal/mtliocommandqueuedescriptor/scratchbufferallocator)
- [MTLIOPriority](/documentation/metal/mtliopriority)

#### I/O command queue priorities

- [case normal](/documentation/metal/mtliopriority/normal)
- [case low](/documentation/metal/mtliopriority/low)
- [case high](/documentation/metal/mtliopriority/high)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtliopriority/init(rawvalue:))
- [MTLIOCommandQueueType](/documentation/metal/mtliocommandqueuetype)

#### I/O command queue types

- [case concurrent](/documentation/metal/mtliocommandqueuetype/concurrent)
- [case serial](/documentation/metal/mtliocommandqueuetype/serial)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtliocommandqueuetype/init(rawvalue:))
- [MTLIOScratchBufferAllocator](/documentation/metal/mtlioscratchbufferallocator)

#### Providing scratch memory to a queue

- [func makeScratchBuffer(minimumSize: Int) -> (any MTLIOScratchBuffer)?](/documentation/metal/mtlioscratchbufferallocator/makescratchbuffer(minimumsize:))
- [MTLIOScratchBuffer](/documentation/metal/mtlioscratchbuffer)

#### Wrapping a buffer

- [var buffer: any MTLBuffer](/documentation/metal/mtlioscratchbuffer/buffer)

### I/O command buffers

- [MTLIOCommandBuffer](/documentation/metal/mtliocommandbuffer)

#### Loading assets

- [func load(any MTLBuffer, offset: Int, size: Int, sourceHandle: any MTLIOFileHandle, sourceHandleOffset: Int)](/documentation/metal/mtliocommandbuffer/load(_:offset:size:sourcehandle:sourcehandleoffset:))
- [func load(any MTLTexture, slice: Int, level: Int, size: MTLSize, sourceBytesPerRow: Int, sourceBytesPerImage: Int, destinationOrigin: MTLOrigin, sourceHandle: any MTLIOFileHandle, sourceHandleOffset: Int)](/documentation/metal/mtliocommandbuffer/load(_:slice:level:size:sourcebytesperrow:sourcebytesperimage:destinationorigin:sourcehandle:sourcehandleoffset:))
- [func loadBytes(UnsafeMutableRawPointer, size: Int, sourceHandle: any MTLIOFileHandle, sourceHandleOffset: Int)](/documentation/metal/mtliocommandbuffer/loadbytes(_:size:sourcehandle:sourcehandleoffset:))

#### Adding a barrier

- [func addBarrier()](/documentation/metal/mtliocommandbuffer/addbarrier())

#### Synchronizing a command buffer

- [func signalEvent(any MTLSharedEvent, value: UInt64)](/documentation/metal/mtliocommandbuffer/signalevent(_:value:))
- [func waitForEvent(any MTLSharedEvent, value: UInt64)](/documentation/metal/mtliocommandbuffer/waitforevent(_:value:))

#### Adding final commands

- [func copyStatus(buffer: any MTLBuffer, offset: Int)](/documentation/metal/mtliocommandbuffer/copystatus(buffer:offset:))
- [func addCompletedHandler(MTLIOCommandBufferHandler)](/documentation/metal/mtliocommandbuffer/addcompletedhandler(_:))

#### Submitting a command buffer

- [func commit()](/documentation/metal/mtliocommandbuffer/commit())
- [func enqueue()](/documentation/metal/mtliocommandbuffer/enqueue())

#### Canceling a command buffer

- [func tryCancel()](/documentation/metal/mtliocommandbuffer/trycancel())

#### Waiting for a command buffer

- [func waitUntilCompleted()](/documentation/metal/mtliocommandbuffer/waituntilcompleted())

#### Checking the state of a command buffer

- [var status: MTLIOStatus](/documentation/metal/mtliocommandbuffer/status)
- [var error: (any Error)?](/documentation/metal/mtliocommandbuffer/error)

#### Debugging a command buffer

- [var label: String?](/documentation/metal/mtliocommandbuffer/label)
- [func pushDebugGroup(String)](/documentation/metal/mtliocommandbuffer/pushdebuggroup(_:))
- [func popDebugGroup()](/documentation/metal/mtliocommandbuffer/popdebuggroup())
- [MTLIOFileHandle](/documentation/metal/mtliofilehandle)

#### Naming a file handle

- [var label: String?](/documentation/metal/mtliofilehandle/label)
- [MTLIOCommandBufferHandler](/documentation/metal/mtliocommandbufferhandler)
- [MTLIOStatus](/documentation/metal/mtliostatus)

#### I/O command queue states

- [case pending](/documentation/metal/mtliostatus/pending)
- [case complete](/documentation/metal/mtliostatus/complete)
- [case cancelled](/documentation/metal/mtliostatus/cancelled)
- [case error](/documentation/metal/mtliostatus/error)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtliostatus/init(rawvalue:))
- [MTLIOError.Code](/documentation/metal/mtlioerror-swift.struct/code)

#### Error codes

- [case urlInvalid](/documentation/metal/mtlioerror-swift.struct/code/urlinvalid)
- [case `internal`](/documentation/metal/mtlioerror-swift.struct/code/internal)
- [case urlInvalid](/documentation/metal/mtlioerror-swift.struct/code/urlinvalid)
- [case `internal`](/documentation/metal/mtlioerror-swift.struct/code/internal)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlioerror-swift.struct/code/init(rawvalue:))
- [let MTLIOErrorDomain: String](/documentation/metal/mtlioerrordomain)

### Asset compression

- [MTLIOCreateCompressionContext](/documentation/metal/mtliocreatecompressioncontext(_:_:_:))
- [MTLIOCompressionMethod](/documentation/metal/mtliocompressionmethod)

#### Compression codecs

- [case zlib](/documentation/metal/mtliocompressionmethod/zlib)
- [case lzfse](/documentation/metal/mtliocompressionmethod/lzfse)
- [case lz4](/documentation/metal/mtliocompressionmethod/lz4)
- [case lzma](/documentation/metal/mtliocompressionmethod/lzma)
- [case lzBitmap](/documentation/metal/mtliocompressionmethod/lzbitmap)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtliocompressionmethod/init(rawvalue:))
- [func MTLIOCompressionContextDefaultChunkSize() -> Int](/documentation/metal/mtliocompressioncontextdefaultchunksize())
- [MTLIOCompressionContext](/documentation/metal/mtliocompressioncontext)
- [func MTLIOCompressionContextAppendData(MTLIOCompressionContext, UnsafeRawPointer, Int)](/documentation/metal/mtliocompressioncontextappenddata(_:_:_:))
- [func MTLIOFlushAndDestroyCompressionContext(MTLIOCompressionContext) -> MTLIOCompressionStatus](/documentation/metal/mtlioflushanddestroycompressioncontext(_:))
- [MTLIOCompressionStatus](/documentation/metal/mtliocompressionstatus)

#### Compression result states

- [case complete](/documentation/metal/mtliocompressionstatus/complete)
- [case error](/documentation/metal/mtliocompressionstatus/error)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtliocompressionstatus/init(rawvalue:))
- [Resource synchronization](/documentation/metal/resource-synchronization)

### Synchronizing with barriers and fences

- [Synchronizing stages within a pass](/documentation/metal/synchronizing-stages-within-a-pass)
- [Synchronizing passes with a fence](/documentation/metal/synchronizing-passes-with-a-fence)
- [Synchronizing passes with consumer barriers](/documentation/metal/synchronizing-passes-with-consumer-barriers)
- [Synchronizing passes with producer barriers](/documentation/metal/synchronizing-passes-with-producer-barriers)
- [Synchronizing CPU and GPU work](/documentation/metal/synchronizing-cpu-and-gpu-work)
- [Implementing a multistage image filter using heaps and fences](/documentation/metal/implementing-a-multistage-image-filter-using-heaps-and-fences)
- [MTLStages](/documentation/metal/mtlstages)

#### Render pass stages

- [static var vertex: MTLStages](/documentation/metal/mtlstages/vertex)
- [static var fragment: MTLStages](/documentation/metal/mtlstages/fragment)
- [static var tile: MTLStages](/documentation/metal/mtlstages/tile)
- [static var object: MTLStages](/documentation/metal/mtlstages/object)
- [static var mesh: MTLStages](/documentation/metal/mtlstages/mesh)

#### Compute pass stages

- [static var dispatch: MTLStages](/documentation/metal/mtlstages/dispatch)
- [static var blit: MTLStages](/documentation/metal/mtlstages/blit)
- [static var accelerationStructure: MTLStages](/documentation/metal/mtlstages/accelerationstructure)
- [static var machineLearning: MTLStages](/documentation/metal/mtlstages/machinelearning)

#### Resource pass stages

- [static var resourceState: MTLStages](/documentation/metal/mtlstages/resourcestate)

#### Convenience values

- [static var all: MTLStages](/documentation/metal/mtlstages/all)

#### Swift support

- [init(rawValue: UInt)](/documentation/metal/mtlstages/init(rawvalue:))
- [MTLFence](/documentation/metal/mtlfence)

#### Identifying a fence

- [var device: any MTLDevice](/documentation/metal/mtlfence/device)
- [var label: String?](/documentation/metal/mtlfence/label)

#### Selecting render stages

- [MTLRenderStages](/documentation/metal/mtlrenderstages)

##### Render pass stages

- [static var object: MTLRenderStages](/documentation/metal/mtlrenderstages/object)
- [static var mesh: MTLRenderStages](/documentation/metal/mtlrenderstages/mesh)
- [static var vertex: MTLRenderStages](/documentation/metal/mtlrenderstages/vertex)
- [static var fragment: MTLRenderStages](/documentation/metal/mtlrenderstages/fragment)
- [static var tile: MTLRenderStages](/documentation/metal/mtlrenderstages/tile)

##### Swift support

- [init(rawValue: UInt)](/documentation/metal/mtlrenderstages/init(rawvalue:))
- [MTLRenderStages](/documentation/metal/mtlrenderstages)

#### Render pass stages

- [static var object: MTLRenderStages](/documentation/metal/mtlrenderstages/object)
- [static var mesh: MTLRenderStages](/documentation/metal/mtlrenderstages/mesh)
- [static var vertex: MTLRenderStages](/documentation/metal/mtlrenderstages/vertex)
- [static var fragment: MTLRenderStages](/documentation/metal/mtlrenderstages/fragment)
- [static var tile: MTLRenderStages](/documentation/metal/mtlrenderstages/tile)

#### Swift support

- [init(rawValue: UInt)](/documentation/metal/mtlrenderstages/init(rawvalue:))
- [MTLBarrierScope](/documentation/metal/mtlbarrierscope)

#### Initializers

- [init(rawValue: UInt)](/documentation/metal/mtlbarrierscope/init(rawvalue:))

#### Type Properties

- [static var buffers: MTLBarrierScope](/documentation/metal/mtlbarrierscope/buffers)
- [static var renderTargets: MTLBarrierScope](/documentation/metal/mtlbarrierscope/rendertargets)
- [static var textures: MTLBarrierScope](/documentation/metal/mtlbarrierscope/textures)
- [MTL4VisibilityOptions](/documentation/metal/mtl4visibilityoptions)

#### Initializers

- [init(rawValue: UInt)](/documentation/metal/mtl4visibilityoptions/init(rawvalue:))

#### Type Properties

- [static var device: MTL4VisibilityOptions](/documentation/metal/mtl4visibilityoptions/device)
- [static var resourceAlias: MTL4VisibilityOptions](/documentation/metal/mtl4visibilityoptions/resourcealias)

### Synchronizing with events

- [Implementing a multistage image filter using heaps and events](/documentation/metal/implementing-a-multistage-image-filter-using-heaps-and-events)
- [About synchronization events](/documentation/metal/about-synchronization-events)
- [Synchronizing events within a single device](/documentation/metal/synchronizing-events-within-a-single-device)
- [Synchronizing events across multiple devices or processes](/documentation/metal/synchronizing-events-across-multiple-devices-or-processes)
- [Synchronizing events between a GPU and the CPU](/documentation/metal/synchronizing-events-between-a-gpu-and-the-cpu)
- [MTLEvent](/documentation/metal/mtlevent)

#### Identifying the event

- [var device: (any MTLDevice)?](/documentation/metal/mtlevent/device)
- [var label: String?](/documentation/metal/mtlevent/label)
- [MTLSharedEvent](/documentation/metal/mtlsharedevent)

#### Synchronizing a shareable event

- [var signaledValue: UInt64](/documentation/metal/mtlsharedevent/signaledvalue)
- [func notify(MTLSharedEventListener, atValue: UInt64, block: MTLSharedEventNotificationBlock)](/documentation/metal/mtlsharedevent/notify(_:atvalue:block:))

#### Creating a shared event handle

- [func makeSharedEventHandle() -> MTLSharedEventHandle](/documentation/metal/mtlsharedevent/makesharedeventhandle())

#### Instance Methods

- [func valueSignaled(UInt64) async](/documentation/metal/mtlsharedevent/valuesignaled(_:))
- [func wait(untilSignaledValue: UInt64, timeoutMS: UInt64) -> Bool](/documentation/metal/mtlsharedevent/wait(untilsignaledvalue:timeoutms:))
- [MTLSharedEventHandle](/documentation/metal/mtlsharedeventhandle)

#### Identifying the shareable event handle

- [var label: String?](/documentation/metal/mtlsharedeventhandle/label)
- [MTLSharedEventListener](/documentation/metal/mtlsharedeventlistener)

#### Initializing a shareable event listener

- [init()](/documentation/metal/mtlsharedeventlistener/init())
- [init(dispatchQueue: dispatch_queue_t)](/documentation/metal/mtlsharedeventlistener/init(dispatchqueue:))

#### Getting the dispatch queue

- [var dispatchQueue: dispatch_queue_t](/documentation/metal/mtlsharedeventlistener/dispatchqueue)

#### Type Methods

- [class func shared() -> MTLSharedEventListener](/documentation/metal/mtlsharedeventlistener/shared())
- [MTLSharedEventNotificationBlock](/documentation/metal/mtlsharedeventnotificationblock)

## Shader compilation and libraries

- [Using the Metal 4 compilation API](/documentation/metal/using-the-metal-4-compilation-api)
- [Shader libraries](/documentation/metal/shader-libraries)

### Shader compilation

- [Metal libraries](/documentation/metal/metal-libraries)

#### Working with Metal intermediate representation libraries

- [Building a shader library by precompiling source files](/documentation/metal/building-a-shader-library-by-precompiling-source-files)
- [Minimizing the binary size of a shader library](/documentation/metal/minimizing-the-binary-size-of-a-shader-library)
- [Generating and loading a Metal library symbol file](/documentation/metal/generating-and-loading-a-metal-library-symbol-file)
- [Metal dynamic libraries](/documentation/metal/metal-dynamic-libraries)

#### Working with Metal dynamic libraries

- [Compiling and linking Metal dynamic libraries](/documentation/metal/compiling-and-linking-metal-dynamic-libraries)
- [Creating a Metal dynamic library](/documentation/metal/creating-a-metal-dynamic-library)
- [Metal binary archives](/documentation/metal/metal-binary-archives)

#### Working with Metal binary archives

- [Creating binary archives from device-built pipeline state objects](/documentation/metal/creating-binary-archives-from-device-built-pipeline-state-objects)
- [Manipulating Metal binary archives](/documentation/metal/manipulating-metal-binary-archives)
- [Compiling binary archives from a custom configuration script](/documentation/metal/compiling-binary-archives-from-a-custom-configuration-script)
- [MTL4Compiler](/documentation/metal/mtl4compiler)

#### Instance Properties

- [var device: any MTLDevice](/documentation/metal/mtl4compiler/device)
- [var label: String?](/documentation/metal/mtl4compiler/label)
- [var pipelineDataSetSerializer: (any MTL4PipelineDataSetSerializer)?](/documentation/metal/mtl4compiler/pipelinedatasetserializer)

#### Instance Methods

- [func makeBinaryFunction(descriptor: MTL4BinaryFunctionDescriptor, compilerTaskOptions: MTL4CompilerTaskOptions?) throws -> any MTL4BinaryFunction](/documentation/metal/mtl4compiler/makebinaryfunction(descriptor:compilertaskoptions:)-5o46e)
- [func makeBinaryFunction(descriptor: MTL4BinaryFunctionDescriptor, compilerTaskOptions: MTL4CompilerTaskOptions?) async throws -> any MTL4BinaryFunction](/documentation/metal/mtl4compiler/makebinaryfunction(descriptor:compilertaskoptions:)-hkc4)
- [func makeComputePipelineState(descriptor: MTL4ComputePipelineDescriptor, dynamicLinkingDescriptor: MTL4PipelineStageDynamicLinkingDescriptor?, compilerTaskOptions: MTL4CompilerTaskOptions?) async throws -> any MTLComputePipelineState](/documentation/metal/mtl4compiler/makecomputepipelinestate(descriptor:dynamiclinkingdescriptor:compilertaskoptions:)-19x)
- [func makeComputePipelineState(descriptor: MTL4ComputePipelineDescriptor, dynamicLinkingDescriptor: MTL4PipelineStageDynamicLinkingDescriptor?, compilerTaskOptions: MTL4CompilerTaskOptions?) throws -> any MTLComputePipelineState](/documentation/metal/mtl4compiler/makecomputepipelinestate(descriptor:dynamiclinkingdescriptor:compilertaskoptions:)-7dqdm)
- [func makeDynamicLibrary(library: any MTLLibrary) throws -> any MTLDynamicLibrary](/documentation/metal/mtl4compiler/makedynamiclibrary(library:))
- [func makeDynamicLibrary(url: URL) throws -> any MTLDynamicLibrary](/documentation/metal/mtl4compiler/makedynamiclibrary(url:))
- [func makeLibrary(descriptor: MTL4LibraryDescriptor) throws -> any MTLLibrary](/documentation/metal/mtl4compiler/makelibrary(descriptor:))
- [func makeMachineLearningPipelineState(descriptor: MTL4MachineLearningPipelineDescriptor) async throws -> any MTL4MachineLearningPipelineState](/documentation/metal/mtl4compiler/makemachinelearningpipelinestate(descriptor:)-36hxx)
- [func makeMachineLearningPipelineState(descriptor: MTL4MachineLearningPipelineDescriptor) throws -> any MTL4MachineLearningPipelineState](/documentation/metal/mtl4compiler/makemachinelearningpipelinestate(descriptor:)-909v1)
- [func makeRenderPipelineState(descriptor: MTL4PipelineDescriptor, dynamicLinkingDescriptor: MTL4RenderPipelineDynamicLinkingDescriptor?, compilerTaskOptions: MTL4CompilerTaskOptions?) async throws -> any MTLRenderPipelineState](/documentation/metal/mtl4compiler/makerenderpipelinestate(descriptor:dynamiclinkingdescriptor:compilertaskoptions:)-66wsk)
- [func makeRenderPipelineState(descriptor: MTL4PipelineDescriptor, dynamicLinkingDescriptor: MTL4RenderPipelineDynamicLinkingDescriptor?, compilerTaskOptions: MTL4CompilerTaskOptions?) throws -> any MTLRenderPipelineState](/documentation/metal/mtl4compiler/makerenderpipelinestate(descriptor:dynamiclinkingdescriptor:compilertaskoptions:)-84kox)
- [func makeRenderPipelineStateBySpecialization(descriptor: MTL4PipelineDescriptor, pipeline: any MTLRenderPipelineState) throws -> any MTLRenderPipelineState](/documentation/metal/mtl4compiler/makerenderpipelinestatebyspecialization(descriptor:pipeline:)-2636j)
- [func makeRenderPipelineStateBySpecialization(descriptor: MTL4PipelineDescriptor, pipeline: any MTLRenderPipelineState) async throws -> any MTLRenderPipelineState](/documentation/metal/mtl4compiler/makerenderpipelinestatebyspecialization(descriptor:pipeline:)-7s2wp)
- [MTL4CompilerDescriptor](/documentation/metal/mtl4compilerdescriptor)

#### Instance Properties

- [var label: String?](/documentation/metal/mtl4compilerdescriptor/label)
- [var pipelineDataSetSerializer: (any MTL4PipelineDataSetSerializer)?](/documentation/metal/mtl4compilerdescriptor/pipelinedatasetserializer)
- [MTL4CompilerTaskOptions](/documentation/metal/mtl4compilertaskoptions)

#### Instance Properties

- [var lookupArchives: [any MTL4Archive]?](/documentation/metal/mtl4compilertaskoptions/lookuparchives)
- [MTL4CompilerTaskStatus](/documentation/metal/mtl4compilertaskstatus)

#### Enumeration Cases

- [case compiling](/documentation/metal/mtl4compilertaskstatus/compiling)
- [case finished](/documentation/metal/mtl4compilertaskstatus/finished)
- [case none](/documentation/metal/mtl4compilertaskstatus/none)
- [case scheduled](/documentation/metal/mtl4compilertaskstatus/scheduled)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtl4compilertaskstatus/init(rawvalue:))
- [MTL4Archive](/documentation/metal/mtl4archive)

#### Identifying the archive

- [var label: String?](/documentation/metal/mtl4archive/label)

#### Instance Methods

- [func makeBinaryFunction(descriptor: MTL4BinaryFunctionDescriptor) throws -> any MTL4BinaryFunction](/documentation/metal/mtl4archive/makebinaryfunction(descriptor:))
- [func makeComputePipelineState(descriptor: MTL4ComputePipelineDescriptor, dynamicLinkingDescriptor: MTL4PipelineStageDynamicLinkingDescriptor?) throws -> any MTLComputePipelineState](/documentation/metal/mtl4archive/makecomputepipelinestate(descriptor:dynamiclinkingdescriptor:))
- [func makeRenderPipelineState(descriptor: MTL4PipelineDescriptor, dynamicLinkingDescriptor: MTL4RenderPipelineDynamicLinkingDescriptor?) throws -> any MTLRenderPipelineState](/documentation/metal/mtl4archive/makerenderpipelinestate(descriptor:dynamiclinkingdescriptor:))
- [MTL4BinaryFunction](/documentation/metal/mtl4binaryfunction)

#### Instance Properties

- [var functionType: MTLFunctionType](/documentation/metal/mtl4binaryfunction/functiontype)
- [var name: String?](/documentation/metal/mtl4binaryfunction/name)
- [MTL4BinaryFunctionDescriptor](/documentation/metal/mtl4binaryfunctiondescriptor)

#### Instance Properties

- [var functionDescriptor: MTL4FunctionDescriptor](/documentation/metal/mtl4binaryfunctiondescriptor/functiondescriptor)
- [var name: String](/documentation/metal/mtl4binaryfunctiondescriptor/name)
- [var options: MTL4BinaryFunctionOptions](/documentation/metal/mtl4binaryfunctiondescriptor/options)
- [MTL4BinaryFunctionOptions](/documentation/metal/mtl4binaryfunctionoptions)

#### Initializers

- [init(rawValue: UInt)](/documentation/metal/mtl4binaryfunctionoptions/init(rawvalue:))

#### Type Properties

- [static var pipelineIndependent: MTL4BinaryFunctionOptions](/documentation/metal/mtl4binaryfunctionoptions/pipelineindependent)
- [MTL4PipelineStageDynamicLinkingDescriptor](/documentation/metal/mtl4pipelinestagedynamiclinkingdescriptor)

#### Instance Properties

- [var binaryLinkedFunctions: [any MTL4BinaryFunction]?](/documentation/metal/mtl4pipelinestagedynamiclinkingdescriptor/binarylinkedfunctions)
- [var maxCallStackDepth: Int](/documentation/metal/mtl4pipelinestagedynamiclinkingdescriptor/maxcallstackdepth)
- [var preloadedLibraries: [any MTLDynamicLibrary]](/documentation/metal/mtl4pipelinestagedynamiclinkingdescriptor/preloadedlibraries)

### Pipeline compilation

- [MTL4BlendState](/documentation/metal/mtl4blendstate)

#### Enumeration Cases

- [case disabled](/documentation/metal/mtl4blendstate/disabled)
- [case enabled](/documentation/metal/mtl4blendstate/enabled)
- [case unspecialized](/documentation/metal/mtl4blendstate/unspecialized)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtl4blendstate/init(rawvalue:))
- [MTL4FunctionDescriptor](/documentation/metal/mtl4functiondescriptor)
- [MTL4IndirectCommandBufferSupportState](/documentation/metal/mtl4indirectcommandbuffersupportstate)

#### Enumeration Cases

- [case disabled](/documentation/metal/mtl4indirectcommandbuffersupportstate/disabled)
- [case enabled](/documentation/metal/mtl4indirectcommandbuffersupportstate/enabled)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtl4indirectcommandbuffersupportstate/init(rawvalue:))
- [MTL4LibraryDescriptor](/documentation/metal/mtl4librarydescriptor)

#### Instance Properties

- [var name: String?](/documentation/metal/mtl4librarydescriptor/name)
- [var options: MTLCompileOptions?](/documentation/metal/mtl4librarydescriptor/options)
- [var source: String?](/documentation/metal/mtl4librarydescriptor/source)
- [MTL4LibraryFunctionDescriptor](/documentation/metal/mtl4libraryfunctiondescriptor)

#### Instance Properties

- [var library: (any MTLLibrary)?](/documentation/metal/mtl4libraryfunctiondescriptor/library)
- [var name: String?](/documentation/metal/mtl4libraryfunctiondescriptor/name)
- [MTL4LogicalToPhysicalColorAttachmentMappingState](/documentation/metal/mtl4logicaltophysicalcolorattachmentmappingstate)

#### Enumeration Cases

- [case identity](/documentation/metal/mtl4logicaltophysicalcolorattachmentmappingstate/identity)
- [case inherited](/documentation/metal/mtl4logicaltophysicalcolorattachmentmappingstate/inherited)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtl4logicaltophysicalcolorattachmentmappingstate/init(rawvalue:))
- [MTL4NewBinaryFunctionCompletionHandler](/documentation/metal/mtl4newbinaryfunctioncompletionhandler)
- [MTL4NewMachineLearningPipelineStateCompletionHandler](/documentation/metal/mtl4newmachinelearningpipelinestatecompletionhandler)
- [MTL4ShaderReflection](/documentation/metal/mtl4shaderreflection)

#### Initializers

- [init(rawValue: UInt)](/documentation/metal/mtl4shaderreflection/init(rawvalue:))

#### Type Properties

- [static var bindingInfo: MTL4ShaderReflection](/documentation/metal/mtl4shaderreflection/bindinginfo)
- [static var bufferTypeInfo: MTL4ShaderReflection](/documentation/metal/mtl4shaderreflection/buffertypeinfo)
- [MTL4SpecializedFunctionDescriptor](/documentation/metal/mtl4specializedfunctiondescriptor)

#### Instance Properties

- [var constantValues: MTLFunctionConstantValues?](/documentation/metal/mtl4specializedfunctiondescriptor/constantvalues)
- [var functionDescriptor: MTL4FunctionDescriptor?](/documentation/metal/mtl4specializedfunctiondescriptor/functiondescriptor)
- [var specializedName: String?](/documentation/metal/mtl4specializedfunctiondescriptor/specializedname)
- [MTL4AlphaToCoverageState](/documentation/metal/mtl4alphatocoveragestate)

#### Enumeration Cases

- [case disabled](/documentation/metal/mtl4alphatocoveragestate/disabled)
- [case enabled](/documentation/metal/mtl4alphatocoveragestate/enabled)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtl4alphatocoveragestate/init(rawvalue:))
- [MTL4AlphaToOneState](/documentation/metal/mtl4alphatoonestate)

#### Enumeration Cases

- [case disabled](/documentation/metal/mtl4alphatoonestate/disabled)
- [case enabled](/documentation/metal/mtl4alphatoonestate/enabled)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtl4alphatoonestate/init(rawvalue:))
- [MTL4StaticLinkingDescriptor](/documentation/metal/mtl4staticlinkingdescriptor)

#### Instance Properties

- [var functionDescriptors: [MTL4FunctionDescriptor]?](/documentation/metal/mtl4staticlinkingdescriptor/functiondescriptors)
- [var groups: [String : [MTL4FunctionDescriptor]]?](/documentation/metal/mtl4staticlinkingdescriptor/groups)
- [var privateFunctionDescriptors: [MTL4FunctionDescriptor]?](/documentation/metal/mtl4staticlinkingdescriptor/privatefunctiondescriptors)
- [MTL4StitchedFunctionDescriptor](/documentation/metal/mtl4stitchedfunctiondescriptor)

#### Instance Properties

- [var functionDescriptors: [MTL4FunctionDescriptor]?](/documentation/metal/mtl4stitchedfunctiondescriptor/functiondescriptors)
- [var functionGraph: MTLFunctionStitchingGraph?](/documentation/metal/mtl4stitchedfunctiondescriptor/functiongraph)
- [MTLFunctionReflection](/documentation/metal/mtlfunctionreflection)

#### Instance Properties

- [var bindings: [any MTLBinding]](/documentation/metal/mtlfunctionreflection/bindings)
- [var userAnnotation: String?](/documentation/metal/mtlfunctionreflection/userannotation)
- [MTLNewDynamicLibraryCompletionHandler](/documentation/metal/mtlnewdynamiclibrarycompletionhandler)

### Pipeline harvesting

- [MTL4PipelineDataSetSerializer](/documentation/metal/mtl4pipelinedatasetserializer)

#### Instance Methods

- [func serializeAsArchiveAndFlush(url: URL) throws](/documentation/metal/mtl4pipelinedatasetserializer/serializeasarchiveandflush(url:))
- [func serializeAsPipelinesScript() throws -> Data](/documentation/metal/mtl4pipelinedatasetserializer/serializeaspipelinesscript())
- [MTL4PipelineDataSetSerializerConfiguration](/documentation/metal/mtl4pipelinedatasetserializerconfiguration)

#### Initializers

- [init(rawValue: UInt)](/documentation/metal/mtl4pipelinedatasetserializerconfiguration/init(rawvalue:))

#### Type Properties

- [static var captureBinaries: MTL4PipelineDataSetSerializerConfiguration](/documentation/metal/mtl4pipelinedatasetserializerconfiguration/capturebinaries)
- [static var captureDescriptors: MTL4PipelineDataSetSerializerConfiguration](/documentation/metal/mtl4pipelinedatasetserializerconfiguration/capturedescriptors)
- [MTL4PipelineDataSetSerializerDescriptor](/documentation/metal/mtl4pipelinedatasetserializerdescriptor)

#### Instance Properties

- [var configuration: MTL4PipelineDataSetSerializerConfiguration](/documentation/metal/mtl4pipelinedatasetserializerdescriptor/configuration)
- [MTL4PipelineDescriptor](/documentation/metal/mtl4pipelinedescriptor)

#### Instance Properties

- [var label: String?](/documentation/metal/mtl4pipelinedescriptor/label)
- [var options: MTL4PipelineOptions?](/documentation/metal/mtl4pipelinedescriptor/options)
- [MTL4PipelineOptions](/documentation/metal/mtl4pipelineoptions)

#### Instance Properties

- [var shaderReflection: MTL4ShaderReflection](/documentation/metal/mtl4pipelineoptions/shaderreflection)
- [var shaderValidation: MTLShaderValidation](/documentation/metal/mtl4pipelineoptions/shadervalidation)

### Shader library management

- [MTLLibrary](/documentation/metal/mtllibrary)

#### Querying basic library attributes

- [var installName: String?](/documentation/metal/mtllibrary/installname)
- [var type: MTLLibraryType](/documentation/metal/mtllibrary/type)

#### Querying library contents

- [var functionNames: [String]](/documentation/metal/mtllibrary/functionnames)

#### Creating shader function instances

- [func makeFunction(name: String) -> (any MTLFunction)?](/documentation/metal/mtllibrary/makefunction(name:))
- [func makeFunction(name: String, constantValues: MTLFunctionConstantValues, completionHandler: ((any MTLFunction)?, (any Error)?) -> Void)](/documentation/metal/mtllibrary/makefunction(name:constantvalues:completionhandler:))
- [func makeFunction(name: String, constantValues: MTLFunctionConstantValues) throws -> any MTLFunction](/documentation/metal/mtllibrary/makefunction(name:constantvalues:))
- [func makeFunction(descriptor: MTLFunctionDescriptor, completionHandler: ((any MTLFunction)?, (any Error)?) -> Void)](/documentation/metal/mtllibrary/makefunction(descriptor:completionhandler:))
- [func makeFunction(descriptor: MTLFunctionDescriptor) throws -> any MTLFunction](/documentation/metal/mtllibrary/makefunction(descriptor:))

#### Creating intersection function instances

- [func makeIntersectionFunction(descriptor: MTLIntersectionFunctionDescriptor, completionHandler: ((any MTLFunction)?, (any Error)?) -> Void)](/documentation/metal/mtllibrary/makeintersectionfunction(descriptor:completionhandler:))
- [func makeIntersectionFunction(descriptor: MTLIntersectionFunctionDescriptor) throws -> any MTLFunction](/documentation/metal/mtllibrary/makeintersectionfunction(descriptor:))

#### Identifying the library

- [var device: any MTLDevice](/documentation/metal/mtllibrary/device)
- [var label: String?](/documentation/metal/mtllibrary/label)

#### Instance Methods

- [func reflection(functionName: String) -> MTLFunctionReflection?](/documentation/metal/mtllibrary/reflection(functionname:))
- [MTLDynamicLibrary](/documentation/metal/mtldynamiclibrary)

#### Identifying the library

- [var device: any MTLDevice](/documentation/metal/mtldynamiclibrary/device)
- [var installName: String](/documentation/metal/mtldynamiclibrary/installname)
- [var label: String?](/documentation/metal/mtldynamiclibrary/label)

#### Saving a dynamic library to a file

- [func serialize(to: URL) throws](/documentation/metal/mtldynamiclibrary/serialize(to:))
- [MTLBinaryArchive](/documentation/metal/mtlbinaryarchive)

#### Identifying the archive

- [var device: any MTLDevice](/documentation/metal/mtlbinaryarchive/device)
- [var label: String?](/documentation/metal/mtlbinaryarchive/label)

#### Adding pipeline descriptors

- [func addComputePipelineFunctions(descriptor: MTLComputePipelineDescriptor) throws](/documentation/metal/mtlbinaryarchive/addcomputepipelinefunctions(descriptor:))
- [func addRenderPipelineFunctions(descriptor: MTLRenderPipelineDescriptor) throws](/documentation/metal/mtlbinaryarchive/addrenderpipelinefunctions(descriptor:))
- [func addTileRenderPipelineFunctions(descriptor: MTLTileRenderPipelineDescriptor) throws](/documentation/metal/mtlbinaryarchive/addtilerenderpipelinefunctions(descriptor:))
- [func addFunction(descriptor: MTLFunctionDescriptor, library: any MTLLibrary) throws](/documentation/metal/mtlbinaryarchive/addfunction(descriptor:library:))

#### Serializing archives

- [func serialize(to: URL) throws](/documentation/metal/mtlbinaryarchive/serialize(to:))

#### Instance Methods

- [func addLibrary(descriptor: MTLStitchedLibraryDescriptor) throws](/documentation/metal/mtlbinaryarchive/addlibrary(descriptor:))
- [func addMeshRenderPipelineFunctions(descriptor: MTLMeshRenderPipelineDescriptor) throws](/documentation/metal/mtlbinaryarchive/addmeshrenderpipelinefunctions(descriptor:))
- [MTLCompileOptions](/documentation/metal/mtlcompileoptions)

#### Configuring the compiler options

- [var enableLogging: Bool](/documentation/metal/mtlcompileoptions/enablelogging)
- [var mathMode: MTLMathMode](/documentation/metal/mtlcompileoptions/mathmode)

##### Supporting types

- [MTLMathMode](/documentation/metal/mtlmathmode)

###### Modes

- [case fast](/documentation/metal/mtlmathmode/fast)
- [case relaxed](/documentation/metal/mtlmathmode/relaxed)
- [case safe](/documentation/metal/mtlmathmode/safe)

###### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlmathmode/init(rawvalue:))
- [var mathFloatingPointFunctions: MTLMathFloatingPointFunctions](/documentation/metal/mtlcompileoptions/mathfloatingpointfunctions)

##### Supporting types

- [MTLMathFloatingPointFunctions](/documentation/metal/mtlmathfloatingpointfunctions)

###### Function sets

- [case fast](/documentation/metal/mtlmathfloatingpointfunctions/fast)
- [case precise](/documentation/metal/mtlmathfloatingpointfunctions/precise)

###### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlmathfloatingpointfunctions/init(rawvalue:))
- [var preserveInvariance: Bool](/documentation/metal/mtlcompileoptions/preserveinvariance)
- [var languageVersion: MTLLanguageVersion](/documentation/metal/mtlcompileoptions/languageversion)
- [var preprocessorMacros: [String : NSObject]?](/documentation/metal/mtlcompileoptions/preprocessormacros)
- [var optimizationLevel: MTLLibraryOptimizationLevel](/documentation/metal/mtlcompileoptions/optimizationlevel)
- [var libraries: [any MTLDynamicLibrary]?](/documentation/metal/mtlcompileoptions/libraries)
- [var fastMathEnabled: Bool](/documentation/metal/mtlcompileoptions/fastmathenabled)

#### Configuring the library output options

- [var libraryType: MTLLibraryType](/documentation/metal/mtlcompileoptions/librarytype)
- [var installName: String?](/documentation/metal/mtlcompileoptions/installname)

#### Instance Properties

- [var allowReferencingUndefinedSymbols: Bool](/documentation/metal/mtlcompileoptions/allowreferencingundefinedsymbols)
- [var compileSymbolVisibility: MTLCompileSymbolVisibility](/documentation/metal/mtlcompileoptions/compilesymbolvisibility)
- [var maxTotalThreadsPerThreadgroup: Int](/documentation/metal/mtlcompileoptions/maxtotalthreadsperthreadgroup)
- [var requiredThreadsPerThreadgroup: MTLSize](/documentation/metal/mtlcompileoptions/requiredthreadsperthreadgroup)
- [MTLLibraryType](/documentation/metal/mtllibrarytype)

#### Library options

- [case executable](/documentation/metal/mtllibrarytype/executable)
- [case dynamic](/documentation/metal/mtllibrarytype/dynamic)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtllibrarytype/init(rawvalue:))
- [MTLLanguageVersion](/documentation/metal/mtllanguageversion)

#### Version numbers

- [case version1_1](/documentation/metal/mtllanguageversion/version1_1)
- [case version1_2](/documentation/metal/mtllanguageversion/version1_2)
- [case version2_0](/documentation/metal/mtllanguageversion/version2_0)
- [case version2_1](/documentation/metal/mtllanguageversion/version2_1)
- [case version2_2](/documentation/metal/mtllanguageversion/version2_2)
- [case version2_3](/documentation/metal/mtllanguageversion/version2_3)
- [case version2_4](/documentation/metal/mtllanguageversion/version2_4)
- [case version3_0](/documentation/metal/mtllanguageversion/version3_0)
- [case version3_1](/documentation/metal/mtllanguageversion/version3_1)
- [case version3_2](/documentation/metal/mtllanguageversion/version3_2)
- [case version1_0](/documentation/metal/mtllanguageversion/version1_0)

#### Enumeration Cases

- [case version4_0](/documentation/metal/mtllanguageversion/version4_0)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtllanguageversion/init(rawvalue:))
- [MTLCompileSymbolVisibility](/documentation/metal/mtlcompilesymbolvisibility)

#### Enumeration Cases

- [case `default`](/documentation/metal/mtlcompilesymbolvisibility/default)
- [case hidden](/documentation/metal/mtlcompilesymbolvisibility/hidden)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlcompilesymbolvisibility/init(rawvalue:))
- [MTLLibraryOptimizationLevel](/documentation/metal/mtllibraryoptimizationlevel)

#### Optimization options

- [case `default`](/documentation/metal/mtllibraryoptimizationlevel/default)
- [case size](/documentation/metal/mtllibraryoptimizationlevel/size)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtllibraryoptimizationlevel/init(rawvalue:))

### Shader functions

- [MTLFunctionDescriptor](/documentation/metal/mtlfunctiondescriptor)

#### Specifying the function configuration

- [var name: String?](/documentation/metal/mtlfunctiondescriptor/name)
- [var specializedName: String?](/documentation/metal/mtlfunctiondescriptor/specializedname)
- [var constantValues: MTLFunctionConstantValues?](/documentation/metal/mtlfunctiondescriptor/constantvalues)
- [var options: MTLFunctionOptions](/documentation/metal/mtlfunctiondescriptor/options)
- [var binaryArchives: [any MTLBinaryArchive]?](/documentation/metal/mtlfunctiondescriptor/binaryarchives)
- [MTLFunctionOptions](/documentation/metal/mtlfunctionoptions)

##### Function compilation options

- [static var failOnBinaryArchiveMiss: MTLFunctionOptions](/documentation/metal/mtlfunctionoptions/failonbinaryarchivemiss)
- [static var compileToBinary: MTLFunctionOptions](/documentation/metal/mtlfunctionoptions/compiletobinary)
- [static var pipelineIndependent: MTLFunctionOptions](/documentation/metal/mtlfunctionoptions/pipelineindependent)
- [static var storeFunctionInMetalPipelinesScript: MTLFunctionOptions](/documentation/metal/mtlfunctionoptions/storefunctioninmetalpipelinesscript)
- [static var storeFunctionInMetalScript: MTLFunctionOptions](/documentation/metal/mtlfunctionoptions/storefunctioninmetalscript)

##### Swift support

- [init(rawValue: UInt)](/documentation/metal/mtlfunctionoptions/init(rawvalue:))
- [MTLLinkedFunctions](/documentation/metal/mtllinkedfunctions)

##### Specifying related functions

- [var functions: [any MTLFunction]?](/documentation/metal/mtllinkedfunctions/functions)
- [var binaryFunctions: [any MTLFunction]?](/documentation/metal/mtllinkedfunctions/binaryfunctions)
- [var groups: [String : [any MTLFunction]]?](/documentation/metal/mtllinkedfunctions/groups)
- [var privateFunctions: [any MTLFunction]?](/documentation/metal/mtllinkedfunctions/privatefunctions)
- [MTLFunction](/documentation/metal/mtlfunction)

#### Identifying shader functions

- [var device: any MTLDevice](/documentation/metal/mtlfunction/device)
- [var label: String?](/documentation/metal/mtlfunction/label)
- [var functionType: MTLFunctionType](/documentation/metal/mtlfunction/functiontype)
- [var name: String](/documentation/metal/mtlfunction/name)
- [MTLFunctionType](/documentation/metal/mtlfunctiontype)

##### Function types

- [case vertex](/documentation/metal/mtlfunctiontype/vertex)
- [case fragment](/documentation/metal/mtlfunctiontype/fragment)
- [case kernel](/documentation/metal/mtlfunctiontype/kernel)
- [case intersection](/documentation/metal/mtlfunctiontype/intersection)
- [case visible](/documentation/metal/mtlfunctiontype/visible)

##### Enumeration Cases

- [case mesh](/documentation/metal/mtlfunctiontype/mesh)
- [case object](/documentation/metal/mtlfunctiontype/object)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlfunctiontype/init(rawvalue:))
- [var options: MTLFunctionOptions](/documentation/metal/mtlfunction/options)
- [MTLFunctionOptions](/documentation/metal/mtlfunctionoptions)

##### Function compilation options

- [static var failOnBinaryArchiveMiss: MTLFunctionOptions](/documentation/metal/mtlfunctionoptions/failonbinaryarchivemiss)
- [static var compileToBinary: MTLFunctionOptions](/documentation/metal/mtlfunctionoptions/compiletobinary)
- [static var pipelineIndependent: MTLFunctionOptions](/documentation/metal/mtlfunctionoptions/pipelineindependent)
- [static var storeFunctionInMetalPipelinesScript: MTLFunctionOptions](/documentation/metal/mtlfunctionoptions/storefunctioninmetalpipelinesscript)
- [static var storeFunctionInMetalScript: MTLFunctionOptions](/documentation/metal/mtlfunctionoptions/storefunctioninmetalscript)

##### Swift support

- [init(rawValue: UInt)](/documentation/metal/mtlfunctionoptions/init(rawvalue:))

#### Identifying the tessellation patch

- [var patchType: MTLPatchType](/documentation/metal/mtlfunction/patchtype)
- [var patchControlPointCount: Int](/documentation/metal/mtlfunction/patchcontrolpointcount)
- [MTLPatchType](/documentation/metal/mtlpatchtype)

##### Patch types

- [case none](/documentation/metal/mtlpatchtype/none)
- [case triangle](/documentation/metal/mtlpatchtype/triangle)
- [case quad](/documentation/metal/mtlpatchtype/quad)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlpatchtype/init(rawvalue:))

#### Retrieving function attributes

- [var vertexAttributes: [MTLVertexAttribute]?](/documentation/metal/mtlfunction/vertexattributes)
- [var stageInputAttributes: [MTLAttribute]?](/documentation/metal/mtlfunction/stageinputattributes)

#### Retrieving function constants

- [var functionConstantsDictionary: [String : MTLFunctionConstant]](/documentation/metal/mtlfunction/functionconstantsdictionary)

#### Creating argument encoders

- [func makeArgumentEncoder(bufferIndex: Int) -> any MTLArgumentEncoder](/documentation/metal/mtlfunction/makeargumentencoder(bufferindex:))
- [func makeArgumentEncoder(bufferIndex: Int, reflection: AutoreleasingUnsafeMutablePointer<MTLAutoreleasedArgument?>?) -> any MTLArgumentEncoder](/documentation/metal/mtlfunction/makeargumentencoder(bufferindex:reflection:))
- [MTLFunctionHandle](/documentation/metal/mtlfunctionhandle)

#### Querying handle properties

- [var device: any MTLDevice](/documentation/metal/mtlfunctionhandle/device)
- [var functionType: MTLFunctionType](/documentation/metal/mtlfunctionhandle/functiontype)
- [var name: String](/documentation/metal/mtlfunctionhandle/name)

#### Instance Properties

- [var gpuResourceID: MTLResourceID](/documentation/metal/mtlfunctionhandle/gpuresourceid)
- [MTLVisibleFunctionTableDescriptor](/documentation/metal/mtlvisiblefunctiontabledescriptor)

#### Configuring the function table

- [var functionCount: Int](/documentation/metal/mtlvisiblefunctiontabledescriptor/functioncount)
- [MTLVisibleFunctionTable](/documentation/metal/mtlvisiblefunctiontable)

#### Setting a table entry

- [func setFunction((any MTLFunctionHandle)?, index: Int)](/documentation/metal/mtlvisiblefunctiontable/setfunction(_:index:))
- [- setFunctions:withRange:](/documentation/metal/mtlvisiblefunctiontable/setfunctions(_:range:))

#### Instance Properties

- [var gpuResourceID: MTLResourceID](/documentation/metal/mtlvisiblefunctiontable/gpuresourceid)
- [MTLIntersectionFunctionDescriptor](/documentation/metal/mtlintersectionfunctiondescriptor)
- [MTLIntersectionFunctionTableDescriptor](/documentation/metal/mtlintersectionfunctiontabledescriptor)

#### Configuring the table’s size

- [var functionCount: Int](/documentation/metal/mtlintersectionfunctiontabledescriptor/functioncount)
- [MTLIntersectionFunctionTable](/documentation/metal/mtlintersectionfunctiontable)

#### Setting a table entry

- [func setFunction((any MTLFunctionHandle)?, index: Int)](/documentation/metal/mtlintersectionfunctiontable/setfunction(_:index:))
- [func setFunctions([(any MTLFunctionHandle)?], range: Range<Int>)](/documentation/metal/mtlintersectionfunctiontable/setfunctions(_:range:))

#### Specifying arguments for intersection functions

- [func setBuffer((any MTLBuffer)?, offset: Int, index: Int)](/documentation/metal/mtlintersectionfunctiontable/setbuffer(_:offset:index:))
- [- setBuffers:offsets:withRange:](/documentation/metal/mtlintersectionfunctiontable/setbuffers(_:offsets:range:))
- [func setVisibleFunctionTable((any MTLVisibleFunctionTable)?, bufferIndex: Int)](/documentation/metal/mtlintersectionfunctiontable/setvisiblefunctiontable(_:bufferindex:))
- [- setVisibleFunctionTables:withBufferRange:](/documentation/metal/mtlintersectionfunctiontable/setvisiblefunctiontables(_:bufferrange:))

#### Specifying opaque triangle intersection testing

- [func setOpaqueTriangleIntersectionFunction(signature: MTLIntersectionFunctionSignature, index: Int)](/documentation/metal/mtlintersectionfunctiontable/setopaquetriangleintersectionfunction(signature:index:))
- [func setOpaqueTriangleIntersectionFunction(signature: MTLIntersectionFunctionSignature, range: NSRange)](/documentation/metal/mtlintersectionfunctiontable/setopaquetriangleintersectionfunction(signature:range:))

#### Instance Properties

- [var gpuResourceID: MTLResourceID](/documentation/metal/mtlintersectionfunctiontable/gpuresourceid)

#### Instance Methods

- [func setOpaqueCurveIntersectionFunction(signature: MTLIntersectionFunctionSignature, index: Int)](/documentation/metal/mtlintersectionfunctiontable/setopaquecurveintersectionfunction(signature:index:))
- [func setOpaqueCurveIntersectionFunction(signature: MTLIntersectionFunctionSignature, range: NSRange)](/documentation/metal/mtlintersectionfunctiontable/setopaquecurveintersectionfunction(signature:range:))

### Stitched function libraries

- [Customizing shaders using function pointers and stitching](/documentation/metal/customizing-shaders-using-function-pointers-and-stitching)
- [MTLStitchedLibraryDescriptor](/documentation/metal/mtlstitchedlibrarydescriptor)

#### Configuring a stitched library

- [var functions: [any MTLFunction]](/documentation/metal/mtlstitchedlibrarydescriptor/functions)
- [var functionGraphs: [MTLFunctionStitchingGraph]](/documentation/metal/mtlstitchedlibrarydescriptor/functiongraphs)

#### Instance Properties

- [var binaryArchives: [any MTLBinaryArchive]](/documentation/metal/mtlstitchedlibrarydescriptor/binaryarchives)
- [var options: MTLStitchedLibraryOptions](/documentation/metal/mtlstitchedlibrarydescriptor/options)
- [MTLFunctionStitchingGraph](/documentation/metal/mtlfunctionstitchinggraph)

#### Initializing a function graph

- [init(functionName: String, nodes: [MTLFunctionStitchingFunctionNode], outputNode: MTLFunctionStitchingFunctionNode?, attributes: [any MTLFunctionStitchingAttribute])](/documentation/metal/mtlfunctionstitchinggraph/init(functionname:nodes:outputnode:attributes:))

#### Configuring a function graph

- [var functionName: String](/documentation/metal/mtlfunctionstitchinggraph/functionname)
- [var nodes: [MTLFunctionStitchingFunctionNode]](/documentation/metal/mtlfunctionstitchinggraph/nodes)
- [var outputNode: MTLFunctionStitchingFunctionNode?](/documentation/metal/mtlfunctionstitchinggraph/outputnode)
- [var attributes: [any MTLFunctionStitchingAttribute]](/documentation/metal/mtlfunctionstitchinggraph/attributes)
- [MTLFunctionStitchingInputNode](/documentation/metal/mtlfunctionstitchinginputnode)

#### Initializing an input node

- [init(argumentIndex: Int)](/documentation/metal/mtlfunctionstitchinginputnode/init(argumentindex:))

#### Configuring an input node

- [var argumentIndex: Int](/documentation/metal/mtlfunctionstitchinginputnode/argumentindex)
- [MTLFunctionStitchingFunctionNode](/documentation/metal/mtlfunctionstitchingfunctionnode)

#### Initializing a function node

- [init(name: String, arguments: [any MTLFunctionStitchingNode], controlDependencies: [MTLFunctionStitchingFunctionNode])](/documentation/metal/mtlfunctionstitchingfunctionnode/init(name:arguments:controldependencies:))

#### Configuring a function node

- [var name: String](/documentation/metal/mtlfunctionstitchingfunctionnode/name)
- [var arguments: [any MTLFunctionStitchingNode]](/documentation/metal/mtlfunctionstitchingfunctionnode/arguments)
- [var controlDependencies: [MTLFunctionStitchingFunctionNode]](/documentation/metal/mtlfunctionstitchingfunctionnode/controldependencies)
- [MTLFunctionStitchingNode](/documentation/metal/mtlfunctionstitchingnode)
- [MTLFunctionStitchingAttributeAlwaysInline](/documentation/metal/mtlfunctionstitchingattributealwaysinline)
- [MTLFunctionStitchingAttribute](/documentation/metal/mtlfunctionstitchingattribute)

### Compile-time variant functions

- [MTLFunctionConstant](/documentation/metal/mtlfunctionconstant)

#### Reading the function constant’s properties

- [var name: String](/documentation/metal/mtlfunctionconstant/name)
- [var type: MTLDataType](/documentation/metal/mtlfunctionconstant/type)
- [var index: Int](/documentation/metal/mtlfunctionconstant/index)
- [var required: Bool](/documentation/metal/mtlfunctionconstant/required)
- [MTLFunctionConstantValues](/documentation/metal/mtlfunctionconstantvalues)

#### Setting constant values

- [func setConstantValue(UnsafeRawPointer, type: MTLDataType, index: Int)](/documentation/metal/mtlfunctionconstantvalues/setconstantvalue(_:type:index:))
- [func setConstantValue(UnsafeRawPointer, type: MTLDataType, withName: String)](/documentation/metal/mtlfunctionconstantvalues/setconstantvalue(_:type:withname:))
- [func setConstantValues(UnsafeRawPointer, type: MTLDataType, range: Range<Int>)](/documentation/metal/mtlfunctionconstantvalues/setconstantvalues(_:type:range:))

#### Resetting constant values

- [func reset()](/documentation/metal/mtlfunctionconstantvalues/reset())

### Introspection data

- [MTLComputePipelineReflection](/documentation/metal/mtlcomputepipelinereflection)

#### Obtaining the arguments of the compute function

- [var arguments: [MTLArgument]](/documentation/metal/mtlcomputepipelinereflection/arguments)

#### Instance Properties

- [var bindings: [any MTLBinding]](/documentation/metal/mtlcomputepipelinereflection/bindings)
- [MTLAutoreleasedComputePipelineReflection](/documentation/metal/mtlautoreleasedcomputepipelinereflection)
- [MTLRenderPipelineReflection](/documentation/metal/mtlrenderpipelinereflection)

#### Inspecting a shader’s parameter

- [var fragmentBindings: [any MTLBinding]](/documentation/metal/mtlrenderpipelinereflection/fragmentbindings)
- [var meshBindings: [any MTLBinding]](/documentation/metal/mtlrenderpipelinereflection/meshbindings)
- [var objectBindings: [any MTLBinding]](/documentation/metal/mtlrenderpipelinereflection/objectbindings)
- [var tileBindings: [any MTLBinding]](/documentation/metal/mtlrenderpipelinereflection/tilebindings)
- [var vertexBindings: [any MTLBinding]](/documentation/metal/mtlrenderpipelinereflection/vertexbindings)

#### Deprecated

- [var vertexArguments: [MTLArgument]?](/documentation/metal/mtlrenderpipelinereflection/vertexarguments)
- [var fragmentArguments: [MTLArgument]?](/documentation/metal/mtlrenderpipelinereflection/fragmentarguments)
- [var tileArguments: [MTLArgument]?](/documentation/metal/mtlrenderpipelinereflection/tilearguments)
- [MTLAutoreleasedRenderPipelineReflection](/documentation/metal/mtlautoreleasedrenderpipelinereflection)
- [MTLBindingType](/documentation/metal/mtlbindingtype)

#### Enumeration Cases

- [case buffer](/documentation/metal/mtlbindingtype/buffer)
- [case imageblock](/documentation/metal/mtlbindingtype/imageblock)
- [case imageblockData](/documentation/metal/mtlbindingtype/imageblockdata)
- [case instanceAccelerationStructure](/documentation/metal/mtlbindingtype/instanceaccelerationstructure)
- [case intersectionFunctionTable](/documentation/metal/mtlbindingtype/intersectionfunctiontable)
- [case objectPayload](/documentation/metal/mtlbindingtype/objectpayload)
- [case primitiveAccelerationStructure](/documentation/metal/mtlbindingtype/primitiveaccelerationstructure)
- [case sampler](/documentation/metal/mtlbindingtype/sampler)
- [case tensor](/documentation/metal/mtlbindingtype/tensor)
- [case texture](/documentation/metal/mtlbindingtype/texture)
- [case threadgroupMemory](/documentation/metal/mtlbindingtype/threadgroupmemory)
- [case visibleFunctionTable](/documentation/metal/mtlbindingtype/visiblefunctiontable)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlbindingtype/init(rawvalue:))
- [MTLBinding](/documentation/metal/mtlbinding)

#### Instance Properties

- [var access: MTLBindingAccess](/documentation/metal/mtlbinding/access)
- [var index: Int](/documentation/metal/mtlbinding/index)
- [var isArgument: Bool](/documentation/metal/mtlbinding/isargument)
- [var isUsed: Bool](/documentation/metal/mtlbinding/isused)
- [var name: String](/documentation/metal/mtlbinding/name)
- [var type: MTLBindingType](/documentation/metal/mtlbinding/type)
- [MTLBindingAccess](/documentation/metal/mtlbindingaccess)

#### Enumeration Cases

- [case readOnly](/documentation/metal/mtlbindingaccess/readonly)
- [case readWrite](/documentation/metal/mtlbindingaccess/readwrite)
- [case writeOnly](/documentation/metal/mtlbindingaccess/writeonly)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlbindingaccess/init(rawvalue:))
- [MTLBufferBinding](/documentation/metal/mtlbufferbinding)

#### Instance Properties

- [var bufferAlignment: Int](/documentation/metal/mtlbufferbinding/bufferalignment)
- [var bufferDataSize: Int](/documentation/metal/mtlbufferbinding/bufferdatasize)
- [var bufferDataType: MTLDataType](/documentation/metal/mtlbufferbinding/bufferdatatype)
- [var bufferPointerType: MTLPointerType?](/documentation/metal/mtlbufferbinding/bufferpointertype)
- [var bufferStructType: MTLStructType?](/documentation/metal/mtlbufferbinding/bufferstructtype)
- [MTLTextureBinding](/documentation/metal/mtltexturebinding)

#### Instance Properties

- [var arrayLength: Int](/documentation/metal/mtltexturebinding/arraylength)
- [var isDepthTexture: Bool](/documentation/metal/mtltexturebinding/isdepthtexture)
- [var textureDataType: MTLDataType](/documentation/metal/mtltexturebinding/texturedatatype)
- [var textureType: MTLTextureType](/documentation/metal/mtltexturebinding/texturetype)
- [MTLThreadgroupBinding](/documentation/metal/mtlthreadgroupbinding)

#### Instance Properties

- [var threadgroupMemoryAlignment: Int](/documentation/metal/mtlthreadgroupbinding/threadgroupmemoryalignment)
- [var threadgroupMemoryDataSize: Int](/documentation/metal/mtlthreadgroupbinding/threadgroupmemorydatasize)
- [MTLObjectPayloadBinding](/documentation/metal/mtlobjectpayloadbinding)

#### Instance Properties

- [var objectPayloadAlignment: Int](/documentation/metal/mtlobjectpayloadbinding/objectpayloadalignment)
- [var objectPayloadDataSize: Int](/documentation/metal/mtlobjectpayloadbinding/objectpayloaddatasize)

### Function arguments

- [MTLAttribute](/documentation/metal/mtlattribute)

#### Reading an attribute’s properties

- [var name: String](/documentation/metal/mtlattribute/name)
- [var attributeIndex: Int](/documentation/metal/mtlattribute/attributeindex)
- [var attributeType: MTLDataType](/documentation/metal/mtlattribute/attributetype)
- [var isActive: Bool](/documentation/metal/mtlattribute/isactive)
- [var isPatchControlPointData: Bool](/documentation/metal/mtlattribute/ispatchcontrolpointdata)
- [var isPatchData: Bool](/documentation/metal/mtlattribute/ispatchdata)
- [MTLVertexAttribute](/documentation/metal/mtlvertexattribute)

#### Describing the attribute

- [var name: String](/documentation/metal/mtlvertexattribute/name)
- [var attributeIndex: Int](/documentation/metal/mtlvertexattribute/attributeindex)
- [var attributeType: MTLDataType](/documentation/metal/mtlvertexattribute/attributetype)
- [var isActive: Bool](/documentation/metal/mtlvertexattribute/isactive)
- [var isPatchControlPointData: Bool](/documentation/metal/mtlvertexattribute/ispatchcontrolpointdata)
- [var isPatchData: Bool](/documentation/metal/mtlvertexattribute/ispatchdata)
- [MTLArgument](/documentation/metal/mtlargument)

#### Describing the argument

- [var name: String](/documentation/metal/mtlargument/name)
- [var isActive: Bool](/documentation/metal/mtlargument/isactive)
- [var index: Int](/documentation/metal/mtlargument/index)
- [var type: MTLArgumentType](/documentation/metal/mtlargument/type)
- [var access: MTLBindingAccess](/documentation/metal/mtlargument/access)

#### Describing a buffer argument

- [var bufferAlignment: Int](/documentation/metal/mtlargument/bufferalignment)
- [var bufferDataSize: Int](/documentation/metal/mtlargument/bufferdatasize)
- [var bufferDataType: MTLDataType](/documentation/metal/mtlargument/bufferdatatype)
- [var bufferStructType: MTLStructType?](/documentation/metal/mtlargument/bufferstructtype)
- [var bufferPointerType: MTLPointerType?](/documentation/metal/mtlargument/bufferpointertype)

#### Describing a texture argument

- [var textureDataType: MTLDataType](/documentation/metal/mtlargument/texturedatatype)
- [var textureType: MTLTextureType](/documentation/metal/mtlargument/texturetype)
- [var isDepthTexture: Bool](/documentation/metal/mtlargument/isdepthtexture)

#### Describing an array argument

- [var arrayLength: Int](/documentation/metal/mtlargument/arraylength)

#### Describing a threadgroup memory argument

- [var threadgroupMemoryAlignment: Int](/documentation/metal/mtlargument/threadgroupmemoryalignment)
- [var threadgroupMemoryDataSize: Int](/documentation/metal/mtlargument/threadgroupmemorydatasize)
- [MTLAutoreleasedArgument](/documentation/metal/mtlautoreleasedargument)
- [MTLArgumentType](/documentation/metal/mtlargumenttype)

#### Argument types

- [case buffer](/documentation/metal/mtlargumenttype/buffer)
- [case threadgroupMemory](/documentation/metal/mtlargumenttype/threadgroupmemory)
- [case texture](/documentation/metal/mtlargumenttype/texture)
- [case sampler](/documentation/metal/mtlargumenttype/sampler)
- [case imageblock](/documentation/metal/mtlargumenttype/imageblock)
- [case imageblockData](/documentation/metal/mtlargumenttype/imageblockdata)
- [case visibleFunctionTable](/documentation/metal/mtlargumenttype/visiblefunctiontable)
- [case intersectionFunctionTable](/documentation/metal/mtlargumenttype/intersectionfunctiontable)
- [case primitiveAccelerationStructure](/documentation/metal/mtlargumenttype/primitiveaccelerationstructure)
- [case instanceAccelerationStructure](/documentation/metal/mtlargumenttype/instanceaccelerationstructure)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlargumenttype/init(rawvalue:))
- [MTLArgumentAccess](/documentation/metal/mtlargumentaccess)

### Shader types

- [MTLType](/documentation/metal/mtltype)

#### Identifying the data type

- [var dataType: MTLDataType](/documentation/metal/mtltype/datatype)
- [MTLDataType](/documentation/metal/mtldatatype)

#### Boolean types

- [case bool](/documentation/metal/mtldatatype/bool)
- [case bool2](/documentation/metal/mtldatatype/bool2)
- [case bool3](/documentation/metal/mtldatatype/bool3)
- [case bool4](/documentation/metal/mtldatatype/bool4)

#### 8-bit integer types

- [case char](/documentation/metal/mtldatatype/char)
- [case char2](/documentation/metal/mtldatatype/char2)
- [case char3](/documentation/metal/mtldatatype/char3)
- [case char4](/documentation/metal/mtldatatype/char4)
- [case uchar](/documentation/metal/mtldatatype/uchar)
- [case uchar2](/documentation/metal/mtldatatype/uchar2)
- [case uchar3](/documentation/metal/mtldatatype/uchar3)
- [case uchar4](/documentation/metal/mtldatatype/uchar4)

#### 16-bit integer types

- [case short](/documentation/metal/mtldatatype/short)
- [case short2](/documentation/metal/mtldatatype/short2)
- [case short3](/documentation/metal/mtldatatype/short3)
- [case short4](/documentation/metal/mtldatatype/short4)
- [case ushort](/documentation/metal/mtldatatype/ushort)
- [case ushort2](/documentation/metal/mtldatatype/ushort2)
- [case ushort3](/documentation/metal/mtldatatype/ushort3)
- [case ushort4](/documentation/metal/mtldatatype/ushort4)

#### 16-bit floating-point types

- [case half](/documentation/metal/mtldatatype/half)
- [case half2](/documentation/metal/mtldatatype/half2)
- [case half3](/documentation/metal/mtldatatype/half3)
- [case half4](/documentation/metal/mtldatatype/half4)
- [case half2x2](/documentation/metal/mtldatatype/half2x2)
- [case half2x3](/documentation/metal/mtldatatype/half2x3)
- [case half2x4](/documentation/metal/mtldatatype/half2x4)
- [case half3x2](/documentation/metal/mtldatatype/half3x2)
- [case half3x3](/documentation/metal/mtldatatype/half3x3)
- [case half3x4](/documentation/metal/mtldatatype/half3x4)
- [case half4x2](/documentation/metal/mtldatatype/half4x2)
- [case half4x3](/documentation/metal/mtldatatype/half4x3)
- [case half4x4](/documentation/metal/mtldatatype/half4x4)
- [case bfloat](/documentation/metal/mtldatatype/bfloat)
- [case bfloat2](/documentation/metal/mtldatatype/bfloat2)
- [case bfloat3](/documentation/metal/mtldatatype/bfloat3)
- [case bfloat4](/documentation/metal/mtldatatype/bfloat4)

#### 32-bit floating-point types

- [case float](/documentation/metal/mtldatatype/float)
- [case float2](/documentation/metal/mtldatatype/float2)
- [case float3](/documentation/metal/mtldatatype/float3)
- [case float4](/documentation/metal/mtldatatype/float4)
- [case float2x2](/documentation/metal/mtldatatype/float2x2)
- [case float2x3](/documentation/metal/mtldatatype/float2x3)
- [case float2x4](/documentation/metal/mtldatatype/float2x4)
- [case float3x2](/documentation/metal/mtldatatype/float3x2)
- [case float3x3](/documentation/metal/mtldatatype/float3x3)
- [case float3x4](/documentation/metal/mtldatatype/float3x4)
- [case float4x2](/documentation/metal/mtldatatype/float4x2)
- [case float4x3](/documentation/metal/mtldatatype/float4x3)
- [case float4x4](/documentation/metal/mtldatatype/float4x4)

#### 32-bit integer types

- [case int](/documentation/metal/mtldatatype/int)
- [case int2](/documentation/metal/mtldatatype/int2)
- [case int3](/documentation/metal/mtldatatype/int3)
- [case int4](/documentation/metal/mtldatatype/int4)
- [case uint](/documentation/metal/mtldatatype/uint)
- [case uint2](/documentation/metal/mtldatatype/uint2)
- [case uint3](/documentation/metal/mtldatatype/uint3)
- [case uint4](/documentation/metal/mtldatatype/uint4)

#### 64-bit integer types

- [case long](/documentation/metal/mtldatatype/long)
- [case long2](/documentation/metal/mtldatatype/long2)
- [case long3](/documentation/metal/mtldatatype/long3)
- [case long4](/documentation/metal/mtldatatype/long4)
- [case ulong](/documentation/metal/mtldatatype/ulong)
- [case ulong2](/documentation/metal/mtldatatype/ulong2)
- [case ulong3](/documentation/metal/mtldatatype/ulong3)
- [case ulong4](/documentation/metal/mtldatatype/ulong4)

#### 8-bit pixel format types

- [case r8Snorm](/documentation/metal/mtldatatype/r8snorm)
- [case r8Unorm](/documentation/metal/mtldatatype/r8unorm)

#### 16-bit pixel format types

- [case rg8Snorm](/documentation/metal/mtldatatype/rg8snorm)
- [case rg8Unorm](/documentation/metal/mtldatatype/rg8unorm)
- [case r16Snorm](/documentation/metal/mtldatatype/r16snorm)
- [case r16Unorm](/documentation/metal/mtldatatype/r16unorm)

#### 32-bit pixel format types

- [case rgba8Snorm](/documentation/metal/mtldatatype/rgba8snorm)
- [case rgba8Unorm](/documentation/metal/mtldatatype/rgba8unorm)
- [case rgba8Unorm_srgb](/documentation/metal/mtldatatype/rgba8unorm_srgb)
- [case rg16Snorm](/documentation/metal/mtldatatype/rg16snorm)
- [case rg16Unorm](/documentation/metal/mtldatatype/rg16unorm)
- [case rgb10a2Unorm](/documentation/metal/mtldatatype/rgb10a2unorm)
- [case rgb9e5Float](/documentation/metal/mtldatatype/rgb9e5float)
- [case rg11b10Float](/documentation/metal/mtldatatype/rg11b10float)

#### 64-bit pixel format types

- [case rgba16Snorm](/documentation/metal/mtldatatype/rgba16snorm)
- [case rgba16Unorm](/documentation/metal/mtldatatype/rgba16unorm)

#### Metal resource types

- [case texture](/documentation/metal/mtldatatype/texture)
- [case indirectCommandBuffer](/documentation/metal/mtldatatype/indirectcommandbuffer)
- [case visibleFunctionTable](/documentation/metal/mtldatatype/visiblefunctiontable)
- [case intersectionFunctionTable](/documentation/metal/mtldatatype/intersectionfunctiontable)
- [case primitiveAccelerationStructure](/documentation/metal/mtldatatype/primitiveaccelerationstructure)
- [case instanceAccelerationStructure](/documentation/metal/mtldatatype/instanceaccelerationstructure)

#### Metal state types

- [case sampler](/documentation/metal/mtldatatype/sampler)
- [case renderPipeline](/documentation/metal/mtldatatype/renderpipeline)
- [case computePipeline](/documentation/metal/mtldatatype/computepipeline)

#### Collection types

- [case `struct`](/documentation/metal/mtldatatype/struct)
- [case array](/documentation/metal/mtldatatype/array)
- [case pointer](/documentation/metal/mtldatatype/pointer)

#### Invalid data types

- [case none](/documentation/metal/mtldatatype/none)

#### Enumeration Cases

- [case depthStencilState](/documentation/metal/mtldatatype/depthstencilstate)
- [case tensor](/documentation/metal/mtldatatype/tensor)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtldatatype/init(rawvalue:))
- [MTLArrayType](/documentation/metal/mtlarraytype)

#### Describing the array elements

- [var arrayLength: Int](/documentation/metal/mtlarraytype/arraylength)
- [var elementType: MTLDataType](/documentation/metal/mtlarraytype/elementtype)
- [var stride: Int](/documentation/metal/mtlarraytype/stride)
- [var argumentIndexStride: Int](/documentation/metal/mtlarraytype/argumentindexstride)

#### Obtaining details for complex array elements

- [func element() -> MTLArrayType?](/documentation/metal/mtlarraytype/element())
- [func elementStructType() -> MTLStructType?](/documentation/metal/mtlarraytype/elementstructtype())
- [func elementPointerType() -> MTLPointerType?](/documentation/metal/mtlarraytype/elementpointertype())
- [func elementTextureReferenceType() -> MTLTextureReferenceType?](/documentation/metal/mtlarraytype/elementtexturereferencetype())

#### Instance Methods

- [func elementTensorReferenceType() -> MTLTensorReferenceType?](/documentation/metal/mtlarraytype/elementtensorreferencetype())
- [MTLStructType](/documentation/metal/mtlstructtype)

#### Obtaining information about struct members

- [var members: [MTLStructMember]](/documentation/metal/mtlstructtype/members)
- [func memberByName(String) -> MTLStructMember?](/documentation/metal/mtlstructtype/memberbyname(_:))
- [MTLStructMember](/documentation/metal/mtlstructmember)

#### Describing the struct member

- [var name: String](/documentation/metal/mtlstructmember/name)
- [var dataType: MTLDataType](/documentation/metal/mtlstructmember/datatype)
- [var offset: Int](/documentation/metal/mtlstructmember/offset)
- [var argumentIndex: Int](/documentation/metal/mtlstructmember/argumentindex)

#### Obtaining struct member details

- [func arrayType() -> MTLArrayType?](/documentation/metal/mtlstructmember/arraytype())
- [func structType() -> MTLStructType?](/documentation/metal/mtlstructmember/structtype())
- [func pointerType() -> MTLPointerType?](/documentation/metal/mtlstructmember/pointertype())
- [func textureReferenceType() -> MTLTextureReferenceType?](/documentation/metal/mtlstructmember/texturereferencetype())

#### Instance Methods

- [func tensorReferenceType() -> MTLTensorReferenceType?](/documentation/metal/mtlstructmember/tensorreferencetype())
- [MTLPointerType](/documentation/metal/mtlpointertype)

#### Describing the pointer elements

- [var alignment: Int](/documentation/metal/mtlpointertype/alignment)
- [var dataSize: Int](/documentation/metal/mtlpointertype/datasize)
- [var elementType: MTLDataType](/documentation/metal/mtlpointertype/elementtype)
- [var access: MTLBindingAccess](/documentation/metal/mtlpointertype/access)
- [var elementIsArgumentBuffer: Bool](/documentation/metal/mtlpointertype/elementisargumentbuffer)

#### Obtaining details for complex pointer elements

- [func elementArrayType() -> MTLArrayType?](/documentation/metal/mtlpointertype/elementarraytype())
- [func elementStructType() -> MTLStructType?](/documentation/metal/mtlpointertype/elementstructtype())
- [MTLTextureReferenceType](/documentation/metal/mtltexturereferencetype)

#### Describing the texture

- [var textureType: MTLTextureType](/documentation/metal/mtltexturereferencetype/texturetype)
- [var textureDataType: MTLDataType](/documentation/metal/mtltexturereferencetype/texturedatatype)
- [var access: MTLBindingAccess](/documentation/metal/mtltexturereferencetype/access)
- [var isDepthTexture: Bool](/documentation/metal/mtltexturereferencetype/isdepthtexture)

### Shader logging

- [MTLLogStateDescriptor](/documentation/metal/mtllogstatedescriptor)

#### Instance properties

- [var bufferSize: Int](/documentation/metal/mtllogstatedescriptor/buffersize)
- [var level: MTLLogLevel](/documentation/metal/mtllogstatedescriptor/level)

#### Log levels

- [MTLLogLevel](/documentation/metal/mtlloglevel)

##### Enumeration cases

- [case debug](/documentation/metal/mtlloglevel/debug)
- [case info](/documentation/metal/mtlloglevel/info)
- [case notice](/documentation/metal/mtlloglevel/notice)
- [case error](/documentation/metal/mtlloglevel/error)
- [case fault](/documentation/metal/mtlloglevel/fault)
- [case undefined](/documentation/metal/mtlloglevel/undefined)

##### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlloglevel/init(rawvalue:))
- [MTLLogState](/documentation/metal/mtllogstate)

#### Instance Methods

- [func addLogHandler((String?, String?, MTLLogLevel, String) -> Void)](/documentation/metal/mtllogstate/addloghandler(_:))

### Errors

- [MTLLibraryError](/documentation/metal/mtllibraryerror-swift.struct)

#### Errors

- [static var unsupported: MTLLibraryError.Code](/documentation/metal/mtllibraryerror-swift.struct/unsupported)
- [static var `internal`: MTLLibraryError.Code](/documentation/metal/mtllibraryerror-swift.struct/internal)
- [static var compileFailure: MTLLibraryError.Code](/documentation/metal/mtllibraryerror-swift.struct/compilefailure)
- [static var compileWarning: MTLLibraryError.Code](/documentation/metal/mtllibraryerror-swift.struct/compilewarning)
- [static var fileNotFound: MTLLibraryError.Code](/documentation/metal/mtllibraryerror-swift.struct/filenotfound)
- [static var functionNotFound: MTLLibraryError.Code](/documentation/metal/mtllibraryerror-swift.struct/functionnotfound)

#### Error domain

- [static var errorDomain: String](/documentation/metal/mtllibraryerror-swift.struct/errordomain)
- [MTLLibraryError.Code](/documentation/metal/mtllibraryerror-swift.struct/code)

#### Errors

- [case unsupported](/documentation/metal/mtllibraryerror-swift.struct/code/unsupported)
- [case `internal`](/documentation/metal/mtllibraryerror-swift.struct/code/internal)
- [case compileFailure](/documentation/metal/mtllibraryerror-swift.struct/code/compilefailure)
- [case compileWarning](/documentation/metal/mtllibraryerror-swift.struct/code/compilewarning)
- [case fileNotFound](/documentation/metal/mtllibraryerror-swift.struct/code/filenotfound)
- [case functionNotFound](/documentation/metal/mtllibraryerror-swift.struct/code/functionnotfound)
- [case unsupported](/documentation/metal/mtllibraryerror-swift.struct/code/unsupported)
- [case `internal`](/documentation/metal/mtllibraryerror-swift.struct/code/internal)
- [case compileFailure](/documentation/metal/mtllibraryerror-swift.struct/code/compilefailure)
- [case compileWarning](/documentation/metal/mtllibraryerror-swift.struct/code/compilewarning)
- [case fileNotFound](/documentation/metal/mtllibraryerror-swift.struct/code/filenotfound)
- [case functionNotFound](/documentation/metal/mtllibraryerror-swift.struct/code/functionnotfound)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtllibraryerror-swift.struct/code/init(rawvalue:))
- [let MTLLibraryErrorDomain: String](/documentation/metal/mtllibraryerrordomain)
- [Using function specialization to build pipeline variants](/documentation/metal/using-function-specialization-to-build-pipeline-variants)

## Presentation

- [Managing your game window for Metal in macOS](/documentation/metal/managing-your-game-window-for-metal-in-macos)
- [Managing your Metal app window in iPadOS](/documentation/metal/managing-your-metal-app-window-in-ipados)
- [Adapting your game interface for smaller screens](/documentation/metal/adapting-your-game-interface-for-smaller-screens)
- [Onscreen presentation](/documentation/metal/onscreen-presentation)

### Presenting with core animation

- [Creating a custom Metal view](/documentation/metal/creating-a-custom-metal-view)
- [Reading pixel data from a drawable texture](/documentation/metal/reading-pixel-data-from-a-drawable-texture)
- [Achieving smooth frame rates with a Metal display link](/documentation/metal/achieving-smooth-frame-rates-with-a-metal-display-link)
- [CAMetalLayer](/documentation/quartzcore/cametallayer)
- [CAMetalDrawable](/documentation/quartzcore/cametaldrawable)

### Presenting with MetalKit

- [Using Metal to draw a view’s contents](/documentation/metal/using-metal-to-draw-a-view's-contents)
- [MTKView](/documentation/metalkit/mtkview)
- [MTKViewDelegate](/documentation/metalkit/mtkviewdelegate)
- [HDR content](/documentation/metal/hdr-content)

### High dynamic range content

- [Processing HDR images with Metal](/documentation/metal/processing-hdr-images-with-metal)
- [Displaying HDR content in a Metal layer](/documentation/metal/displaying-hdr-content-in-a-metal-layer)
- [Determining support for EDR values](/documentation/metal/determining-support-for-edr-values)
- [Using color spaces to display HDR content](/documentation/metal/using-color-spaces-to-display-hdr-content)
- [Using system tone mapping on video content](/documentation/metal/using-system-tone-mapping-on-video-content)
- [Performing your own tone mapping](/documentation/metal/performing-your-own-tone-mapping)
- [Implementing tone mapping on reference displays](/documentation/metal/implementing-tone-mapping-on-reference-displays)

## Developer tools

- [Supporting Simulator in a Metal app](/documentation/metal/supporting-simulator-in-a-metal-app)
- [Capturing Metal commands programmatically](/documentation/metal/capturing-metal-commands-programmatically)
- [Logging shader debug messages](/documentation/metal/logging-shader-debug-messages)
- [Developing Metal apps that run in Simulator](/documentation/metal/developing-metal-apps-that-run-in-simulator)
- [Improving your game’s graphics performance and settings](/documentation/metal/improving-your-games-graphics-performance-and-settings)
- [Metal debugger](/documentation/xcode/metal-debugger)
- [Metal developer workflows](/documentation/xcode/metal-developer-workflows)
- [GPU counters and counter sample buffers](/documentation/metal/gpu-counters-and-counter-sample-buffers)

### Counters and counter sets

- [Confirming which counters and counter sets a GPU supports](/documentation/metal/confirming-which-counters-and-counter-sets-a-gpu-supports)
- [MTLCounterSet](/documentation/metal/mtlcounterset)

#### Identifying a counter set

- [var name: String](/documentation/metal/mtlcounterset/name)

#### Checking which counters a GPU supports

- [var counters: [any MTLCounter]](/documentation/metal/mtlcounterset/counters)
- [MTLCommonCounterSet](/documentation/metal/mtlcommoncounterset)

#### Common counter set names

- [static let timestamp: MTLCommonCounterSet](/documentation/metal/mtlcommoncounterset/timestamp)
- [static let stageUtilization: MTLCommonCounterSet](/documentation/metal/mtlcommoncounterset/stageutilization)
- [static let statistic: MTLCommonCounterSet](/documentation/metal/mtlcommoncounterset/statistic)

#### Swift support

- [init(rawValue: String)](/documentation/metal/mtlcommoncounterset/init(rawvalue:))
- [MTLCounter](/documentation/metal/mtlcounter)

#### Identifying a counter

- [var name: String](/documentation/metal/mtlcounter/name)
- [MTLCommonCounter](/documentation/metal/mtlcommoncounter)

#### Common counter names

- [static let timestamp: MTLCommonCounter](/documentation/metal/mtlcommoncounter/timestamp)
- [static let tessellationInputPatches: MTLCommonCounter](/documentation/metal/mtlcommoncounter/tessellationinputpatches)
- [static let vertexInvocations: MTLCommonCounter](/documentation/metal/mtlcommoncounter/vertexinvocations)
- [static let postTessellationVertexInvocations: MTLCommonCounter](/documentation/metal/mtlcommoncounter/posttessellationvertexinvocations)
- [static let clipperInvocations: MTLCommonCounter](/documentation/metal/mtlcommoncounter/clipperinvocations)
- [static let clipperPrimitivesOut: MTLCommonCounter](/documentation/metal/mtlcommoncounter/clipperprimitivesout)
- [static let fragmentInvocations: MTLCommonCounter](/documentation/metal/mtlcommoncounter/fragmentinvocations)
- [static let fragmentsPassed: MTLCommonCounter](/documentation/metal/mtlcommoncounter/fragmentspassed)
- [static let computeKernelInvocations: MTLCommonCounter](/documentation/metal/mtlcommoncounter/computekernelinvocations)
- [static let totalCycles: MTLCommonCounter](/documentation/metal/mtlcommoncounter/totalcycles)
- [static let vertexCycles: MTLCommonCounter](/documentation/metal/mtlcommoncounter/vertexcycles)
- [static let postTessellationVertexCycles: MTLCommonCounter](/documentation/metal/mtlcommoncounter/posttessellationvertexcycles)
- [static let fragmentCycles: MTLCommonCounter](/documentation/metal/mtlcommoncounter/fragmentcycles)
- [static let tessellationCycles: MTLCommonCounter](/documentation/metal/mtlcommoncounter/tessellationcycles)
- [static let renderTargetWriteCycles: MTLCommonCounter](/documentation/metal/mtlcommoncounter/rendertargetwritecycles)

#### Swift support

- [init(rawValue: String)](/documentation/metal/mtlcommoncounter/init(rawvalue:))

### Counter sample buffers

- [Creating a counter sample buffer to store a GPU’s counter data during a pass](/documentation/metal/creating-a-counter-sample-buffer-to-store-a-gpus-counter-data-during-a-pass)
- [MTLCounterSampleBufferDescriptor](/documentation/metal/mtlcountersamplebufferdescriptor)

#### Configuring a descriptor for a counter sample buffer

- [var counterSet: (any MTLCounterSet)?](/documentation/metal/mtlcountersamplebufferdescriptor/counterset)
- [var label: String](/documentation/metal/mtlcountersamplebufferdescriptor/label)
- [var sampleCount: Int](/documentation/metal/mtlcountersamplebufferdescriptor/samplecount)
- [var storageMode: MTLStorageMode](/documentation/metal/mtlcountersamplebufferdescriptor/storagemode)
- [MTLCounterSampleBuffer](/documentation/metal/mtlcountersamplebuffer)

#### Resolving the counter sample buffer’s data

- [- resolveCounterRange:](/documentation/metal/mtlcountersamplebuffer/resolvecounterrange(_:))

#### Inspecting the counter sample buffer’s configuration

- [var label: String](/documentation/metal/mtlcountersamplebuffer/label)
- [var device: any MTLDevice](/documentation/metal/mtlcountersamplebuffer/device)
- [var sampleCount: Int](/documentation/metal/mtlcountersamplebuffer/samplecount)
- [Sampling GPU data into counter sample buffers](/documentation/metal/sampling-gpu-data-into-counter-sample-buffers)
- [var MTLCounterDontSample: Int](/documentation/metal/mtlcounterdontsample)

### Counter sample data output

- [Converting a GPU’s counter data into a readable format](/documentation/metal/converting-a-gpus-counter-data-into-a-readable-format)
- [MTLCounterResultTimestamp](/documentation/metal/mtlcounterresulttimestamp)

#### Timestamp values

- [var timestamp: UInt64](/documentation/metal/mtlcounterresulttimestamp/timestamp)

#### Swift support

- [init()](/documentation/metal/mtlcounterresulttimestamp/init())
- [init(timestamp: UInt64)](/documentation/metal/mtlcounterresulttimestamp/init(timestamp:))
- [MTLCounterResultStatistic](/documentation/metal/mtlcounterresultstatistic)

#### Statistics values

- [var tessellationInputPatches: UInt64](/documentation/metal/mtlcounterresultstatistic/tessellationinputpatches)
- [var vertexInvocations: UInt64](/documentation/metal/mtlcounterresultstatistic/vertexinvocations)
- [var postTessellationVertexInvocations: UInt64](/documentation/metal/mtlcounterresultstatistic/posttessellationvertexinvocations)
- [var clipperInvocations: UInt64](/documentation/metal/mtlcounterresultstatistic/clipperinvocations)
- [var clipperPrimitivesOut: UInt64](/documentation/metal/mtlcounterresultstatistic/clipperprimitivesout)
- [var fragmentInvocations: UInt64](/documentation/metal/mtlcounterresultstatistic/fragmentinvocations)
- [var fragmentsPassed: UInt64](/documentation/metal/mtlcounterresultstatistic/fragmentspassed)
- [var computeKernelInvocations: UInt64](/documentation/metal/mtlcounterresultstatistic/computekernelinvocations)

#### Swift support

- [init()](/documentation/metal/mtlcounterresultstatistic/init())
- [init(tessellationInputPatches: UInt64, vertexInvocations: UInt64, postTessellationVertexInvocations: UInt64, clipperInvocations: UInt64, clipperPrimitivesOut: UInt64, fragmentInvocations: UInt64, fragmentsPassed: UInt64, computeKernelInvocations: UInt64)](/documentation/metal/mtlcounterresultstatistic/init(tessellationinputpatches:vertexinvocations:posttessellationvertexinvocations:clipperinvocations:clipperprimitivesout:fragmentinvocations:fragmentspassed:computekernelinvocations:))
- [MTLCounterResultStageUtilization](/documentation/metal/mtlcounterresultstageutilization)

#### Stage utilization values

- [var totalCycles: UInt64](/documentation/metal/mtlcounterresultstageutilization/totalcycles)
- [var vertexCycles: UInt64](/documentation/metal/mtlcounterresultstageutilization/vertexcycles)
- [var tessellationCycles: UInt64](/documentation/metal/mtlcounterresultstageutilization/tessellationcycles)
- [var postTessellationVertexCycles: UInt64](/documentation/metal/mtlcounterresultstageutilization/posttessellationvertexcycles)
- [var fragmentCycles: UInt64](/documentation/metal/mtlcounterresultstageutilization/fragmentcycles)
- [var renderTargetCycles: UInt64](/documentation/metal/mtlcounterresultstageutilization/rendertargetcycles)

#### Swift support

- [init()](/documentation/metal/mtlcounterresultstageutilization/init())
- [init(totalCycles: UInt64, vertexCycles: UInt64, tessellationCycles: UInt64, postTessellationVertexCycles: UInt64, fragmentCycles: UInt64, renderTargetCycles: UInt64)](/documentation/metal/mtlcounterresultstageutilization/init(totalcycles:vertexcycles:tessellationcycles:posttessellationvertexcycles:fragmentcycles:rendertargetcycles:))
- [var MTLCounterErrorValue: UInt64](/documentation/metal/mtlcountererrorvalue)

### Timestamp data

- [Converting GPU timestamps into CPU time](/documentation/metal/converting-gpu-timestamps-into-cpu-time)
- [MTLTimestamp](/documentation/metal/mtltimestamp)

### Counter sample buffer errors

- [MTLCounterSampleBufferError](/documentation/metal/mtlcountersamplebuffererror-swift.struct)

#### Error code values

- [static var outOfMemory: MTLCounterSampleBufferError.Code](/documentation/metal/mtlcountersamplebuffererror-swift.struct/outofmemory)
- [static var invalid: MTLCounterSampleBufferError.Code](/documentation/metal/mtlcountersamplebuffererror-swift.struct/invalid)
- [static var `internal`: MTLCounterSampleBufferError.Code](/documentation/metal/mtlcountersamplebuffererror-swift.struct/internal)
- [MTLCounterSampleBufferError.Code](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code)

##### Error codes

- [case outOfMemory](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code/outofmemory)
- [case invalid](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code/invalid)
- [case `internal`](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code/internal)
- [case outOfMemory](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code/outofmemory)
- [case invalid](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code/invalid)
- [case `internal`](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code/internal)

##### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code/init(rawvalue:))

#### Error domain

- [static var errorDomain: String](/documentation/metal/mtlcountersamplebuffererror-swift.struct/errordomain)
- [let MTLCounterErrorDomain: String](/documentation/metal/mtlcountererrordomain)
- [Metal debugging types](/documentation/metal/metal-debugging-types)

### Frame capture

- [MTLCaptureDescriptor](/documentation/metal/mtlcapturedescriptor)

#### Setting capture parameters

- [var captureObject: Any?](/documentation/metal/mtlcapturedescriptor/captureobject)
- [var destination: MTLCaptureDestination](/documentation/metal/mtlcapturedescriptor/destination)
- [var outputURL: URL?](/documentation/metal/mtlcapturedescriptor/outputurl)
- [MTLCaptureManager](/documentation/metal/mtlcapturemanager)

#### Obtaining the shared capture manager

- [class func shared() -> MTLCaptureManager](/documentation/metal/mtlcapturemanager/shared())

#### Querying support for a capture destination

- [func supportsDestination(MTLCaptureDestination) -> Bool](/documentation/metal/mtlcapturemanager/supportsdestination(_:))

#### Creating a capture scope

- [func makeCaptureScope(device: any MTLDevice) -> any MTLCaptureScope](/documentation/metal/mtlcapturemanager/makecapturescope(device:))
- [func makeCaptureScope(commandQueue: any MTLCommandQueue) -> any MTLCaptureScope](/documentation/metal/mtlcapturemanager/makecapturescope(commandqueue:)-1rozd)
- [var defaultCaptureScope: (any MTLCaptureScope)?](/documentation/metal/mtlcapturemanager/defaultcapturescope)

#### Starting capture

- [func startCapture(with: MTLCaptureDescriptor) throws](/documentation/metal/mtlcapturemanager/startcapture(with:))
- [func startCapture(device: any MTLDevice)](/documentation/metal/mtlcapturemanager/startcapture(device:))
- [func startCapture(commandQueue: any MTLCommandQueue)](/documentation/metal/mtlcapturemanager/startcapture(commandqueue:))
- [func startCapture(scope: any MTLCaptureScope)](/documentation/metal/mtlcapturemanager/startcapture(scope:))

#### Stopping capture

- [func stopCapture()](/documentation/metal/mtlcapturemanager/stopcapture())

#### Monitoring capture

- [var isCapturing: Bool](/documentation/metal/mtlcapturemanager/iscapturing)

#### Instance Methods

- [func makeCaptureScope(commandQueue: any MTL4CommandQueue) -> any MTLCaptureScope](/documentation/metal/mtlcapturemanager/makecapturescope(commandqueue:)-9wie3)
- [MTLCaptureDestination](/documentation/metal/mtlcapturedestination)

#### Choosing a destination

- [case developerTools](/documentation/metal/mtlcapturedestination/developertools)
- [case gpuTraceDocument](/documentation/metal/mtlcapturedestination/gputracedocument)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlcapturedestination/init(rawvalue:))
- [MTLCaptureScope](/documentation/metal/mtlcapturescope)

#### Defining capture scope boundaries

- [func begin()](/documentation/metal/mtlcapturescope/begin())
- [func end()](/documentation/metal/mtlcapturescope/end())

#### Identifying the capture scope

- [var label: String?](/documentation/metal/mtlcapturescope/label)
- [var device: any MTLDevice](/documentation/metal/mtlcapturescope/device)
- [var commandQueue: (any MTLCommandQueue)?](/documentation/metal/mtlcapturescope/commandqueue)

#### Instance Properties

- [var mtl4CommandQueue: (any MTL4CommandQueue)?](/documentation/metal/mtlcapturescope/mtl4commandqueue)

### Capture errors

- [MTLCaptureError](/documentation/metal/mtlcaptureerror)

#### Errors

- [case alreadyCapturing](/documentation/metal/mtlcaptureerror/alreadycapturing)
- [case invalidDescriptor](/documentation/metal/mtlcaptureerror/invaliddescriptor)
- [case notSupported](/documentation/metal/mtlcaptureerror/notsupported)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlcaptureerror/init(rawvalue:))
- [let MTLCaptureErrorDomain: String](/documentation/metal/mtlcaptureerrordomain)

### Shader logs

- [MTLFunctionLog](/documentation/metal/mtlfunctionlog)

#### Getting the log messsage

- [var type: MTLFunctionLogType](/documentation/metal/mtlfunctionlog/type)
- [MTLFunctionLogType](/documentation/metal/mtlfunctionlogtype)

##### Enumeration cases

- [case validation](/documentation/metal/mtlfunctionlogtype/validation)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlfunctionlogtype/init(rawvalue:))

#### Getting execution details

- [var debugLocation: (any MTLFunctionLogDebugLocation)?](/documentation/metal/mtlfunctionlog/debuglocation)
- [var encoderLabel: String?](/documentation/metal/mtlfunctionlog/encoderlabel)
- [var function: (any MTLFunction)?](/documentation/metal/mtlfunctionlog/function)
- [MTLFunctionLogDebugLocation](/documentation/metal/mtlfunctionlogdebuglocation)

##### Inspecting the location details

- [var functionName: String?](/documentation/metal/mtlfunctionlogdebuglocation/functionname)
- [var url: URL?](/documentation/metal/mtlfunctionlogdebuglocation/url)
- [var line: Int](/documentation/metal/mtlfunctionlogdebuglocation/line)
- [var column: Int](/documentation/metal/mtlfunctionlogdebuglocation/column)
- [MTLLogContainer](/documentation/metal/mtllogcontainer-swift.struct)

## Apple silicon

- [Porting your Metal code to Apple silicon](/documentation/apple-silicon/porting-your-metal-code-to-apple-silicon)
- [Tailor your apps for Apple GPUs and tile-based deferred rendering](/documentation/metal/tailor-your-apps-for-apple-gpus-and-tile-based-deferred-rendering)

## Reference

- [Metal structures](/documentation/metal/metal-structures)

### Structures

- [MTLTensorError](/documentation/metal/mtltensorerror-swift.struct)

#### Type Properties

- [static var errorDomain: String](/documentation/metal/mtltensorerror-swift.struct/errordomain)
- [static var internalError: MTLTensorError.Code](/documentation/metal/mtltensorerror-swift.struct/internalerror)
- [static var invalidDescriptor: MTLTensorError.Code](/documentation/metal/mtltensorerror-swift.struct/invaliddescriptor)
- [static var none: MTLTensorError.Code](/documentation/metal/mtltensorerror-swift.struct/none)
- [MTLBinaryArchiveError](/documentation/metal/mtlbinaryarchiveerror-swift.struct)

#### Error codes

- [static var none: MTLBinaryArchiveError.Code](/documentation/metal/mtlbinaryarchiveerror-swift.struct/none)
- [static var invalidFile: MTLBinaryArchiveError.Code](/documentation/metal/mtlbinaryarchiveerror-swift.struct/invalidfile)
- [static var compilationFailure: MTLBinaryArchiveError.Code](/documentation/metal/mtlbinaryarchiveerror-swift.struct/compilationfailure)
- [static var unexpectedElement: MTLBinaryArchiveError.Code](/documentation/metal/mtlbinaryarchiveerror-swift.struct/unexpectedelement)
- [static var internalError: MTLBinaryArchiveError.Code](/documentation/metal/mtlbinaryarchiveerror-swift.struct/internalerror)
- [MTLBinaryArchiveError.Code](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code)

##### Error codes

- [case none](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/none)
- [case invalidFile](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/invalidfile)
- [case compilationFailure](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/compilationfailure)
- [case unexpectedElement](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/unexpectedelement)
- [case internalError](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/internalerror)
- [case none](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/none)
- [case invalidFile](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/invalidfile)
- [case compilationFailure](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/compilationfailure)
- [case unexpectedElement](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/unexpectedelement)
- [case internalError](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/internalerror)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlbinaryarchiveerror-swift.struct/code/init(rawvalue:))

#### Error domain

- [static var errorDomain: String](/documentation/metal/mtlbinaryarchiveerror-swift.struct/errordomain)
- [let MTLBinaryArchiveDomain: String](/documentation/metal/mtlbinaryarchivedomain)
- [MTLCommandBufferError](/documentation/metal/mtlcommandbuffererror-swift.struct)

#### Errors codes

- [static var none: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/none)
- [static var timeout: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/timeout)
- [static var pageFault: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/pagefault)
- [static var notPermitted: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/notpermitted)
- [static var outOfMemory: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/outofmemory)
- [static var invalidResource: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/invalidresource)
- [static var memoryless: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/memoryless)
- [static var deviceRemoved: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/deviceremoved)
- [static var stackOverflow: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/stackoverflow)
- [static var accessRevoked: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/accessrevoked)
- [static var `internal`: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/internal)
- [MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/code)

##### Error codes

- [case none](/documentation/metal/mtlcommandbuffererror-swift.struct/code/none)
- [case timeout](/documentation/metal/mtlcommandbuffererror-swift.struct/code/timeout)
- [case pageFault](/documentation/metal/mtlcommandbuffererror-swift.struct/code/pagefault)
- [case notPermitted](/documentation/metal/mtlcommandbuffererror-swift.struct/code/notpermitted)
- [case outOfMemory](/documentation/metal/mtlcommandbuffererror-swift.struct/code/outofmemory)
- [case invalidResource](/documentation/metal/mtlcommandbuffererror-swift.struct/code/invalidresource)
- [case memoryless](/documentation/metal/mtlcommandbuffererror-swift.struct/code/memoryless)
- [case deviceRemoved](/documentation/metal/mtlcommandbuffererror-swift.struct/code/deviceremoved)
- [case stackOverflow](/documentation/metal/mtlcommandbuffererror-swift.struct/code/stackoverflow)
- [static var accessRevoked: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/code/accessrevoked)
- [case `internal`](/documentation/metal/mtlcommandbuffererror-swift.struct/code/internal)

##### Deprecated

- [case blacklisted](/documentation/metal/mtlcommandbuffererror-swift.struct/code/blacklisted)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlcommandbuffererror-swift.struct/code/init(rawvalue:))

#### Error domain

- [static var errorDomain: String](/documentation/metal/mtlcommandbuffererror-swift.struct/errordomain)
- [let MTLCommandBufferErrorDomain: String](/documentation/metal/mtlcommandbuffererrordomain)

#### Deprecated

- [static var blacklisted: MTLCommandBufferError.Code](/documentation/metal/mtlcommandbuffererror-swift.struct/blacklisted)
- [MTLComponentTransform](/documentation/metal/mtlcomponenttransform)

#### Initializers

- [init()](/documentation/metal/mtlcomponenttransform/init())
- [init(scale: MTLPackedFloat3, shear: MTLPackedFloat3, pivot: MTLPackedFloat3, rotation: MTLPackedFloatQuaternion, translation: MTLPackedFloat3)](/documentation/metal/mtlcomponenttransform/init(scale:shear:pivot:rotation:translation:))

#### Instance Properties

- [var pivot: MTLPackedFloat3](/documentation/metal/mtlcomponenttransform/pivot)
- [var rotation: MTLPackedFloatQuaternion](/documentation/metal/mtlcomponenttransform/rotation)
- [var scale: MTLPackedFloat3](/documentation/metal/mtlcomponenttransform/scale)
- [var shear: MTLPackedFloat3](/documentation/metal/mtlcomponenttransform/shear)
- [var translation: MTLPackedFloat3](/documentation/metal/mtlcomponenttransform/translation)
- [MTLCounterSampleBufferError](/documentation/metal/mtlcountersamplebuffererror-swift.struct)

#### Error code values

- [static var outOfMemory: MTLCounterSampleBufferError.Code](/documentation/metal/mtlcountersamplebuffererror-swift.struct/outofmemory)
- [static var invalid: MTLCounterSampleBufferError.Code](/documentation/metal/mtlcountersamplebuffererror-swift.struct/invalid)
- [static var `internal`: MTLCounterSampleBufferError.Code](/documentation/metal/mtlcountersamplebuffererror-swift.struct/internal)
- [MTLCounterSampleBufferError.Code](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code)

##### Error codes

- [case outOfMemory](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code/outofmemory)
- [case invalid](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code/invalid)
- [case `internal`](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code/internal)
- [case outOfMemory](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code/outofmemory)
- [case invalid](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code/invalid)
- [case `internal`](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code/internal)

##### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlcountersamplebuffererror-swift.struct/code/init(rawvalue:))

#### Error domain

- [static var errorDomain: String](/documentation/metal/mtlcountersamplebuffererror-swift.struct/errordomain)
- [let MTLCounterErrorDomain: String](/documentation/metal/mtlcountererrordomain)
- [MTLDynamicLibraryError](/documentation/metal/mtldynamiclibraryerror-swift.struct)

#### Error codes

- [static var none: MTLDynamicLibraryError.Code](/documentation/metal/mtldynamiclibraryerror-swift.struct/none)
- [static var invalidFile: MTLDynamicLibraryError.Code](/documentation/metal/mtldynamiclibraryerror-swift.struct/invalidfile)
- [static var compilationFailure: MTLDynamicLibraryError.Code](/documentation/metal/mtldynamiclibraryerror-swift.struct/compilationfailure)
- [static var unresolvedInstallName: MTLDynamicLibraryError.Code](/documentation/metal/mtldynamiclibraryerror-swift.struct/unresolvedinstallname)
- [static var dependencyLoadFailure: MTLDynamicLibraryError.Code](/documentation/metal/mtldynamiclibraryerror-swift.struct/dependencyloadfailure)
- [static var unsupported: MTLDynamicLibraryError.Code](/documentation/metal/mtldynamiclibraryerror-swift.struct/unsupported)
- [MTLDynamicLibraryError.Code](/documentation/metal/mtldynamiclibraryerror-swift.struct/code)

##### Error codes

- [case none](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/none)
- [case invalidFile](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/invalidfile)
- [case compilationFailure](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/compilationfailure)
- [case unresolvedInstallName](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/unresolvedinstallname)
- [case dependencyLoadFailure](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/dependencyloadfailure)
- [case unsupported](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/unsupported)
- [case none](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/none)
- [case invalidFile](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/invalidfile)
- [case compilationFailure](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/compilationfailure)
- [case unresolvedInstallName](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/unresolvedinstallname)
- [case dependencyLoadFailure](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/dependencyloadfailure)
- [case unsupported](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/unsupported)

##### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtldynamiclibraryerror-swift.struct/code/init(rawvalue:))

#### Error domain

- [static var errorDomain: String](/documentation/metal/mtldynamiclibraryerror-swift.struct/errordomain)
- [let MTLDynamicLibraryDomain: String](/documentation/metal/mtldynamiclibrarydomain)
- [MTLIOError](/documentation/metal/mtlioerror-swift.struct)

#### Error codes

- [static var urlInvalid: MTLIOError.Code](/documentation/metal/mtlioerror-swift.struct/urlinvalid)
- [static var `internal`: MTLIOError.Code](/documentation/metal/mtlioerror-swift.struct/internal)
- [MTLIOError.Code](/documentation/metal/mtlioerror-swift.struct/code)

##### Error codes

- [case urlInvalid](/documentation/metal/mtlioerror-swift.struct/code/urlinvalid)
- [case `internal`](/documentation/metal/mtlioerror-swift.struct/code/internal)
- [case urlInvalid](/documentation/metal/mtlioerror-swift.struct/code/urlinvalid)
- [case `internal`](/documentation/metal/mtlioerror-swift.struct/code/internal)

##### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlioerror-swift.struct/code/init(rawvalue:))

#### Error domain

- [static var errorDomain: String](/documentation/metal/mtlioerror-swift.struct/errordomain)
- [let MTLIOErrorDomain: String](/documentation/metal/mtlioerrordomain)
- [MTLPackedFloatQuaternion](/documentation/metal/mtlpackedfloatquaternion)

#### Initializers

- [init()](/documentation/metal/mtlpackedfloatquaternion/init())
- [init(x: Float, y: Float, z: Float, w: Float)](/documentation/metal/mtlpackedfloatquaternion/init(x:y:z:w:))

#### Instance Properties

- [var w: Float](/documentation/metal/mtlpackedfloatquaternion/w)
- [var x: Float](/documentation/metal/mtlpackedfloatquaternion/x)
- [var y: Float](/documentation/metal/mtlpackedfloatquaternion/y)
- [var z: Float](/documentation/metal/mtlpackedfloatquaternion/z)
- [MTLStitchedLibraryOptions](/documentation/metal/mtlstitchedlibraryoptions)

#### Initializers

- [init(rawValue: UInt)](/documentation/metal/mtlstitchedlibraryoptions/init(rawvalue:))

#### Type Properties

- [static var failOnBinaryArchiveMiss: MTLStitchedLibraryOptions](/documentation/metal/mtlstitchedlibraryoptions/failonbinaryarchivemiss)
- [static var storeLibraryInMetalPipelinesScript: MTLStitchedLibraryOptions](/documentation/metal/mtlstitchedlibraryoptions/storelibraryinmetalpipelinesscript)
- [NSDeviceCertification](/documentation/metal/nsdevicecertification)

#### Initializers

- [init(rawValue: Int)](/documentation/metal/nsdevicecertification/init(rawvalue:))
- [NSProcessPerformanceProfile](/documentation/metal/nsprocessperformanceprofile)

#### Initializers

- [init(rawValue: Int)](/documentation/metal/nsprocessperformanceprofile/init(rawvalue:))
- [Metal enumerations](/documentation/metal/metal-enumerations)

### Enumerations

- [MTLTensorError.Code](/documentation/metal/mtltensorerror-swift.struct/code)

#### Enumeration Cases

- [case internalError](/documentation/metal/mtltensorerror-swift.struct/code/internalerror)
- [case invalidDescriptor](/documentation/metal/mtltensorerror-swift.struct/code/invaliddescriptor)
- [case none](/documentation/metal/mtltensorerror-swift.struct/code/none)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtltensorerror-swift.struct/code/init(rawvalue:))
- [MTLArgumentBuffersTier](/documentation/metal/mtlargumentbufferstier)

#### Enumeration cases

- [case tier1](/documentation/metal/mtlargumentbufferstier/tier1)
- [case tier2](/documentation/metal/mtlargumentbufferstier/tier2)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlargumentbufferstier/init(rawvalue:))
- [MTLLogStateError](/documentation/metal/mtllogstateerror)

#### Enumeration Cases

- [case invalid](/documentation/metal/mtllogstateerror/invalid)
- [case invalidSize](/documentation/metal/mtllogstateerror/invalidsize)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtllogstateerror/init(rawvalue:))
- [MTLMathFloatingPointFunctions](/documentation/metal/mtlmathfloatingpointfunctions)

#### Function sets

- [case fast](/documentation/metal/mtlmathfloatingpointfunctions/fast)
- [case precise](/documentation/metal/mtlmathfloatingpointfunctions/precise)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlmathfloatingpointfunctions/init(rawvalue:))
- [MTLMathMode](/documentation/metal/mtlmathmode)

#### Modes

- [case fast](/documentation/metal/mtlmathmode/fast)
- [case relaxed](/documentation/metal/mtlmathmode/relaxed)
- [case safe](/documentation/metal/mtlmathmode/safe)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlmathmode/init(rawvalue:))
- [MTLMatrixLayout](/documentation/metal/mtlmatrixlayout)

#### Enumeration Cases

- [case columnMajor](/documentation/metal/mtlmatrixlayout/columnmajor)
- [case rowMajor](/documentation/metal/mtlmatrixlayout/rowmajor)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlmatrixlayout/init(rawvalue:))
- [MTLReadWriteTextureTier](/documentation/metal/mtlreadwritetexturetier)

#### Enumeration cases

- [case tier1](/documentation/metal/mtlreadwritetexturetier/tier1)
- [case tier2](/documentation/metal/mtlreadwritetexturetier/tier2)
- [case tierNone](/documentation/metal/mtlreadwritetexturetier/tiernone)

#### Initializers

- [init?(rawValue: UInt)](/documentation/metal/mtlreadwritetexturetier/init(rawvalue:))
- [MTLShaderValidation](/documentation/metal/mtlshadervalidation)

#### Validation states

- [case `default`](/documentation/metal/mtlshadervalidation/default)
- [case disabled](/documentation/metal/mtlshadervalidation/disabled)
- [case enabled](/documentation/metal/mtlshadervalidation/enabled)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtlshadervalidation/init(rawvalue:))
- [MTLTransformType](/documentation/metal/mtltransformtype)

#### Enumeration Cases

- [case component](/documentation/metal/mtltransformtype/component)
- [case packedFloat4x3](/documentation/metal/mtltransformtype/packedfloat4x3)

#### Initializers

- [init?(rawValue: Int)](/documentation/metal/mtltransformtype/init(rawvalue:))
- [Metal constants](/documentation/metal/metal-constants)

### Error domains

- [let MTLLogStateErrorDomain: String](/documentation/metal/mtllogstateerrordomain)
- [Metal data types](/documentation/metal/metal-data-types)

### Data types

- [NSDeviceCertification](/documentation/metal/nsdevicecertification)

#### Initializers

- [init(rawValue: Int)](/documentation/metal/nsdevicecertification/init(rawvalue:))
- [NSProcessPerformanceProfile](/documentation/metal/nsprocessperformanceprofile)

#### Initializers

- [init(rawValue: Int)](/documentation/metal/nsprocessperformanceprofile/init(rawvalue:))
- [Metal variables](/documentation/metal/metal-variables)

### Global variables

- [var MTLResourceCPUCacheModeMask: UInt](/documentation/metal/mtlresourcecpucachemodemask)
- [var MTLResourceCPUCacheModeShift: Int32](/documentation/metal/mtlresourcecpucachemodeshift)
- [var MTLResourceHazardTrackingModeMask: UInt](/documentation/metal/mtlresourcehazardtrackingmodemask)
- [var MTLResourceHazardTrackingModeShift: Int32](/documentation/metal/mtlresourcehazardtrackingmodeshift)
- [var MTLResourceStorageModeMask: UInt](/documentation/metal/mtlresourcestoragemodemask)
- [var MTLResourceStorageModeShift: Int32](/documentation/metal/mtlresourcestoragemodeshift)
- [static let iPhonePerformanceGaming: NSDeviceCertification](/documentation/metal/nsdevicecertification/iphoneperformancegaming)
- [static let `default`: NSProcessPerformanceProfile](/documentation/metal/nsprocessperformanceprofile/default)
- [static let sustained: NSProcessPerformanceProfile](/documentation/metal/nsprocessperformanceprofile/sustained)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
