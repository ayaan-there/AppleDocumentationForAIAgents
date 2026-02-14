# ML Compute Documentation

Source: https://sosumi.ai/documentation/mlcompute

---
title: ML Compute
source: https://developer.apple.com/documentation/mlcompute
timestamp: 2026-02-13T18:59:49.334Z
---

## Components

- [MLCTensor](/documentation/mlcompute/mlctensor)

### Creating Tensors with Descriptors

- [convenience init(descriptor: MLCTensorDescriptor)](/documentation/mlcompute/mlctensor/init(descriptor:))
- [convenience init(descriptor: MLCTensorDescriptor, data: MLCTensorData)](/documentation/mlcompute/mlctensor/init(descriptor:data:))
- [convenience init(descriptor: MLCTensorDescriptor, fillWithData: NSNumber)](/documentation/mlcompute/mlctensor/init(descriptor:fillwithdata:))
- [convenience init(descriptor: MLCTensorDescriptor, randomInitializerType: MLCRandomInitializerType)](/documentation/mlcompute/mlctensor/init(descriptor:randominitializertype:))
- [MLCTensorDescriptor](/documentation/mlcompute/mlctensordescriptor)

#### Creating Tensor Descriptors

- [convenience init?(shape: [Int], dataType: MLCDataType)](/documentation/mlcompute/mlctensordescriptor/init(shape:datatype:))
- [convenience init?(shape: [Int], sequenceLengths: [Int], sortedSequences: Bool, dataType: MLCDataType)](/documentation/mlcompute/mlctensordescriptor/init(shape:sequencelengths:sortedsequences:datatype:))
- [convenience init?(width: Int, height: Int, featureChannelCount: Int, batchSize: Int)](/documentation/mlcompute/mlctensordescriptor/init(width:height:featurechannelcount:batchsize:))
- [convenience init?(width: Int, height: Int, featureChannelCount: Int, batchSize: Int, dataType: MLCDataType)](/documentation/mlcompute/mlctensordescriptor/init(width:height:featurechannelcount:batchsize:datatype:))
- [convenience init?(convolutionWeightsWithInputFeatureChannelCount: Int, outputFeatureChannelCount: Int, dataType: MLCDataType)](/documentation/mlcompute/mlctensordescriptor/init(convolutionweightswithinputfeaturechannelcount:outputfeaturechannelcount:datatype:))
- [convenience init?(convolutionWeightsWithWidth: Int, height: Int, inputFeatureChannelCount: Int, outputFeatureChannelCount: Int, dataType: MLCDataType)](/documentation/mlcompute/mlctensordescriptor/init(convolutionweightswithwidth:height:inputfeaturechannelcount:outputfeaturechannelcount:datatype:))
- [convenience init?(convolutionBiasesWithFeatureChannelCount: Int, dataType: MLCDataType)](/documentation/mlcompute/mlctensordescriptor/init(convolutionbiaseswithfeaturechannelcount:datatype:))
- [class var maxTensorDimensions: Int](/documentation/mlcompute/mlctensordescriptor/maxtensordimensions)

#### Inspecting Tensor Descriptors

- [var dataType: MLCDataType](/documentation/mlcompute/mlctensordescriptor/datatype)
- [var dimensionCount: Int](/documentation/mlcompute/mlctensordescriptor/dimensioncount)
- [var shape: [Int]](/documentation/mlcompute/mlctensordescriptor/shape-7i1rw)
- [var stride: [Int]](/documentation/mlcompute/mlctensordescriptor/stride-5mzlt)
- [var tensorAllocationSizeInBytes: Int](/documentation/mlcompute/mlctensordescriptor/tensorallocationsizeinbytes)
- [var sequenceLengths: [Int]?](/documentation/mlcompute/mlctensordescriptor/sequencelengths-3jdab)
- [var sortedSequences: Bool](/documentation/mlcompute/mlctensordescriptor/sortedsequences)
- [var batchSizePerSequenceStep: [Int]?](/documentation/mlcompute/mlctensordescriptor/batchsizepersequencestep-6iz59)
- [MLCDataType](/documentation/mlcompute/mlcdatatype)

#### Enumeration Cases

- [case float16](/documentation/mlcompute/mlcdatatype/float16)
- [case float32](/documentation/mlcompute/mlcdatatype/float32)
- [case boolean](/documentation/mlcompute/mlcdatatype/boolean)
- [case int8](/documentation/mlcompute/mlcdatatype/int8)
- [case int32](/documentation/mlcompute/mlcdatatype/int32)
- [case int64](/documentation/mlcompute/mlcdatatype/int64)
- [case uint8](/documentation/mlcompute/mlcdatatype/uint8)

#### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlcdatatype/init(rawvalue:))
- [MLCTensorData](/documentation/mlcompute/mlctensordata)

#### Creating Tensor Data

- [convenience init(bytesNoCopy: UnsafeMutableRawPointer, length: Int)](/documentation/mlcompute/mlctensordata/init(bytesnocopy:length:))
- [convenience init(bytesNoCopy: UnsafeMutableRawPointer, length: Int, deallocator: (UnsafeMutableRawPointer, Int) -> Void)](/documentation/mlcompute/mlctensordata/init(bytesnocopy:length:deallocator:))
- [convenience init(immutableBytesNoCopy: UnsafeRawPointer, length: Int)](/documentation/mlcompute/mlctensordata/init(immutablebytesnocopy:length:))

#### Inspecting Tensor Data

- [var bytes: UnsafeMutableRawPointer](/documentation/mlcompute/mlctensordata/bytes)
- [var length: Int](/documentation/mlcompute/mlctensordata/length)
- [MLCRandomInitializerType](/documentation/mlcompute/mlcrandominitializertype)

#### Enumeration Cases

- [case uniform](/documentation/mlcompute/mlcrandominitializertype/uniform)
- [case glorotUniform](/documentation/mlcompute/mlcrandominitializertype/glorotuniform)
- [case xavier](/documentation/mlcompute/mlcrandominitializertype/xavier)

#### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlcrandominitializertype/init(rawvalue:))

### Creating Tensors by Specifying Shape

- [convenience init(shape: [Int])](/documentation/mlcompute/mlctensor/init(shape:))
- [convenience init(shape: [Int], dataType: MLCDataType)](/documentation/mlcompute/mlctensor/init(shape:datatype:))
- [convenience init(shape: [Int], data: MLCTensorData, dataType: MLCDataType)](/documentation/mlcompute/mlctensor/init(shape:data:datatype:))
- [convenience init(shape: [Int], fillWithData: NSNumber, dataType: MLCDataType)](/documentation/mlcompute/mlctensor/init(shape:fillwithdata:datatype:))
- [convenience init(shape: [Int], randomInitializerType: MLCRandomInitializerType)](/documentation/mlcompute/mlctensor/init(shape:randominitializertype:))
- [convenience init(width: Int, height: Int, featureChannelCount: Int, batchSize: Int)](/documentation/mlcompute/mlctensor/init(width:height:featurechannelcount:batchsize:))
- [convenience init(width: Int, height: Int, featureChannelCount: Int, batchSize: Int, data: MLCTensorData)](/documentation/mlcompute/mlctensor/init(width:height:featurechannelcount:batchsize:data:))
- [convenience init(width: Int, height: Int, featureChannelCount: Int, batchSize: Int, data: MLCTensorData, dataType: MLCDataType)](/documentation/mlcompute/mlctensor/init(width:height:featurechannelcount:batchsize:data:datatype:))
- [convenience init(width: Int, height: Int, featureChannelCount: Int, batchSize: Int, fillWithData: Float, dataType: MLCDataType)](/documentation/mlcompute/mlctensor/init(width:height:featurechannelcount:batchsize:fillwithdata:datatype:))
- [convenience init(width: Int, height: Int, featureChannelCount: Int, batchSize: Int, randomInitializerType: MLCRandomInitializerType)](/documentation/mlcompute/mlctensor/init(width:height:featurechannelcount:batchsize:randominitializertype:))

### Creating Tensors by Specifying Sequence Lengths

- [convenience init(sequenceLength: Int, featureChannelCount: Int, batchSize: Int)](/documentation/mlcompute/mlctensor/init(sequencelength:featurechannelcount:batchsize:))
- [convenience init(sequenceLength: Int, featureChannelCount: Int, batchSize: Int, data: MLCTensorData?)](/documentation/mlcompute/mlctensor/init(sequencelength:featurechannelcount:batchsize:data:))
- [convenience init?(sequenceLengths: [Int], sortedSequences: Bool, featureChannelCount: Int, batchSize: Int, data: MLCTensorData?)](/documentation/mlcompute/mlctensor/init(sequencelengths:sortedsequences:featurechannelcount:batchsize:data:))
- [convenience init(sequenceLength: Int, featureChannelCount: Int, batchSize: Int, randomInitializerType: MLCRandomInitializerType)](/documentation/mlcompute/mlctensor/init(sequencelength:featurechannelcount:batchsize:randominitializertype:))
- [convenience init?(sequenceLengths: [Int], sortedSequences: Bool, featureChannelCount: Int, batchSize: Int, randomInitializerType: MLCRandomInitializerType)](/documentation/mlcompute/mlctensor/init(sequencelengths:sortedsequences:featurechannelcount:batchsize:randominitializertype:))

### Inspecting Tensors

- [var tensorID: Int](/documentation/mlcompute/mlctensor/tensorid)
- [var descriptor: MLCTensorDescriptor](/documentation/mlcompute/mlctensor/descriptor)
- [var data: Data?](/documentation/mlcompute/mlctensor/data)
- [var label: String](/documentation/mlcompute/mlctensor/label)
- [var device: MLCDevice?](/documentation/mlcompute/mlctensor/device)
- [var optimizerData: [MLCTensorData]](/documentation/mlcompute/mlctensor/optimizerdata)
- [var optimizerDeviceData: [MLCTensorOptimizerDeviceData]](/documentation/mlcompute/mlctensor/optimizerdevicedata)
- [var hasValidNumerics: Bool](/documentation/mlcompute/mlctensor/hasvalidnumerics)
- [MLCTensorOptimizerDeviceData](/documentation/mlcompute/mlctensoroptimizerdevicedata)

### Converting Tensors

- [func quantized(to: MLCDataType, scale: Float, bias: Int) -> MLCTensor?](/documentation/mlcompute/mlctensor/quantized(to:scale:bias:))
- [func quantized(to: MLCDataType, scale: MLCTensor, bias: MLCTensor, axis: Int) -> MLCTensor?](/documentation/mlcompute/mlctensor/quantized(to:scale:bias:axis:))
- [func dequantized(to: MLCDataType, scale: MLCTensor, zeroPoint: MLCTensor) -> MLCTensor?](/documentation/mlcompute/mlctensor/dequantized(to:scale:zeropoint:))
- [func dequantized(to: MLCDataType, scale: MLCTensor, bias: MLCTensor, axis: Int) -> MLCTensor?](/documentation/mlcompute/mlctensor/dequantized(to:scale:bias:axis:))

### Managing Tensor Data

- [func synchronizeData() -> Bool](/documentation/mlcompute/mlctensor/synchronizedata())
- [func synchronizeOptimizerData() -> Bool](/documentation/mlcompute/mlctensor/synchronizeoptimizerdata())
- [func copyDataFromDeviceMemory(toBytes: UnsafeMutableRawPointer, length: Int, synchronizeWithDevice: Bool) -> Bool](/documentation/mlcompute/mlctensor/copydatafromdevicememory(tobytes:length:synchronizewithdevice:))
- [func bindAndWriteData(MLCTensorData, to: MLCDevice) -> Bool](/documentation/mlcompute/mlctensor/bindandwritedata(_:to:))
- [func bindOptimizerData([MLCTensorData], deviceData: [MLCTensorOptimizerDeviceData]?) -> Bool](/documentation/mlcompute/mlctensor/bindoptimizerdata(_:devicedata:))
- [MLCPlatform](/documentation/mlcompute/mlcplatform)

### Getting the RNG Seed

- [class func getRNGseed() -> NSNumber?](/documentation/mlcompute/mlcplatform/getrngseed())

### Setting the RNG Seed

- [class func setRNGSeedTo(NSNumber)](/documentation/mlcompute/mlcplatform/setrngseedto(_:))
- [Layers](/documentation/mlcompute/layers)

### Activation Layers

- [MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer)

#### Creating Activation Layers

- [convenience init(descriptor: MLCActivationDescriptor)](/documentation/mlcompute/mlcactivationlayer/init(descriptor:))
- [Preconfigured Activation Layers](/documentation/mlcompute/preconfigured-activation-layers)

##### Factory Methods

- [class func celu(a: Float) -> Self](/documentation/mlcompute/mlcactivationlayer/celu(a:))
- [class func clamp(min: Float, max: Float) -> Self](/documentation/mlcompute/mlcactivationlayer/clamp(min:max:))
- [class func elu(a: Float) -> Self](/documentation/mlcompute/mlcactivationlayer/elu(a:))
- [class func hardShrink(a: Float) -> Self](/documentation/mlcompute/mlcactivationlayer/hardshrink(a:))
- [class func leakyReLU(negativeSlope: Float) -> Self](/documentation/mlcompute/mlcactivationlayer/leakyrelu(negativeslope:))
- [class func linear(scale: Float, bias: Float) -> Self](/documentation/mlcompute/mlcactivationlayer/linear(scale:bias:))
- [class func relun(a: Float, b: Float) -> Self](/documentation/mlcompute/mlcactivationlayer/relun(a:b:))
- [class func softPlus(beta: Float) -> Self](/documentation/mlcompute/mlcactivationlayer/softplus(beta:))
- [class func softShrink(a: Float) -> Self](/documentation/mlcompute/mlcactivationlayer/softshrink(a:))
- [class func threshold(Float, replacement: Float) -> Self](/documentation/mlcompute/mlcactivationlayer/threshold(_:replacement:))

##### Factory Properties

- [class var absolute: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/absolute)
- [class var celu: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/celu)
- [class var elu: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/elu)
- [class var gelu: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/gelu)
- [class var hardShrink: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/hardshrink)
- [class var hardSigmoid: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/hardsigmoid)
- [class var hardSwish: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/hardswish)
- [class var leakyReLU: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/leakyrelu)
- [class var logSigmoid: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/logsigmoid)
- [class var relu: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/relu)
- [class var relu6: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/relu6)
- [class var selu: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/selu)
- [class var sigmoid: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/sigmoid)
- [class var softPlus: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/softplus)
- [class var softShrink: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/softshrink)
- [class var softSign: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/softsign)
- [class var tanh: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/tanh)
- [class var tanhShrink: MLCActivationLayer](/documentation/mlcompute/mlcactivationlayer/tanhshrink)
- [MLCActivationDescriptor](/documentation/mlcompute/mlcactivationdescriptor)

##### Creating Activation Descriptors

- [convenience init?(type: MLCActivationType)](/documentation/mlcompute/mlcactivationdescriptor/init(type:))
- [convenience init?(type: MLCActivationType, a: Float)](/documentation/mlcompute/mlcactivationdescriptor/init(type:a:))
- [convenience init?(type: MLCActivationType, a: Float, b: Float)](/documentation/mlcompute/mlcactivationdescriptor/init(type:a:b:))
- [convenience init?(type: MLCActivationType, a: Float, b: Float, c: Float)](/documentation/mlcompute/mlcactivationdescriptor/init(type:a:b:c:))
- [MLCActivationType](/documentation/mlcompute/mlcactivationtype)

###### Enumeration Cases

- [case absolute](/documentation/mlcompute/mlcactivationtype/absolute)
- [case celu](/documentation/mlcompute/mlcactivationtype/celu)
- [case clamp](/documentation/mlcompute/mlcactivationtype/clamp)
- [case elu](/documentation/mlcompute/mlcactivationtype/elu)
- [case gelu](/documentation/mlcompute/mlcactivationtype/gelu)
- [case hardShrink](/documentation/mlcompute/mlcactivationtype/hardshrink)
- [case hardSigmoid](/documentation/mlcompute/mlcactivationtype/hardsigmoid)
- [case hardSwish](/documentation/mlcompute/mlcactivationtype/hardswish)
- [case linear](/documentation/mlcompute/mlcactivationtype/linear)
- [case logSigmoid](/documentation/mlcompute/mlcactivationtype/logsigmoid)
- [case none](/documentation/mlcompute/mlcactivationtype/none)
- [case relu](/documentation/mlcompute/mlcactivationtype/relu)
- [case relun](/documentation/mlcompute/mlcactivationtype/relun)
- [case selu](/documentation/mlcompute/mlcactivationtype/selu)
- [case sigmoid](/documentation/mlcompute/mlcactivationtype/sigmoid)
- [case softPlus](/documentation/mlcompute/mlcactivationtype/softplus)
- [case softShrink](/documentation/mlcompute/mlcactivationtype/softshrink)
- [case softSign](/documentation/mlcompute/mlcactivationtype/softsign)
- [case tanh](/documentation/mlcompute/mlcactivationtype/tanh)
- [case tanhShrink](/documentation/mlcompute/mlcactivationtype/tanhshrink)
- [case threshold](/documentation/mlcompute/mlcactivationtype/threshold)
- [var debugDescription: String](/documentation/mlcompute/mlcactivationtype/debugdescription)

###### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlcactivationtype/init(rawvalue:))

##### Inspecting Activation Descriptors

- [var activationType: MLCActivationType](/documentation/mlcompute/mlcactivationdescriptor/activationtype)
- [var a: Float](/documentation/mlcompute/mlcactivationdescriptor/a)
- [var b: Float](/documentation/mlcompute/mlcactivationdescriptor/b)
- [var c: Float](/documentation/mlcompute/mlcactivationdescriptor/c)

#### Inspecting Activation Layers

- [var descriptor: MLCActivationDescriptor](/documentation/mlcompute/mlcactivationlayer/descriptor)
- [MLCMultiheadAttentionLayer](/documentation/mlcompute/mlcmultiheadattentionlayer)

#### Creating Multi-Head Attention Layers

- [convenience init?(descriptor: MLCMultiheadAttentionDescriptor, weights: [MLCTensor], biases: [MLCTensor]?, attentionBiases: [MLCTensor]?)](/documentation/mlcompute/mlcmultiheadattentionlayer/init(descriptor:weights:biases:attentionbiases:))
- [MLCMultiheadAttentionDescriptor](/documentation/mlcompute/mlcmultiheadattentiondescriptor)

##### Creating Multi-Head Attention Descriptors

- [convenience init(modelDimension: Int, headCount: Int)](/documentation/mlcompute/mlcmultiheadattentiondescriptor/init(modeldimension:headcount:))
- [convenience init?(modelDimension: Int, keyDimension: Int, valueDimension: Int, headCount: Int, dropout: Float, hasBiases: Bool, hasAttentionBiases: Bool, addsZeroAttention: Bool)](/documentation/mlcompute/mlcmultiheadattentiondescriptor/init(modeldimension:keydimension:valuedimension:headcount:dropout:hasbiases:hasattentionbiases:addszeroattention:))

##### Inspecting Multi-Head Attention Descriptors

- [var modelDimension: Int](/documentation/mlcompute/mlcmultiheadattentiondescriptor/modeldimension)
- [var keyDimension: Int](/documentation/mlcompute/mlcmultiheadattentiondescriptor/keydimension)
- [var valueDimension: Int](/documentation/mlcompute/mlcmultiheadattentiondescriptor/valuedimension)
- [var headCount: Int](/documentation/mlcompute/mlcmultiheadattentiondescriptor/headcount)
- [var dropout: Float](/documentation/mlcompute/mlcmultiheadattentiondescriptor/dropout)
- [var hasBiases: Bool](/documentation/mlcompute/mlcmultiheadattentiondescriptor/hasbiases)
- [var hasAttentionBiases: Bool](/documentation/mlcompute/mlcmultiheadattentiondescriptor/hasattentionbiases)
- [var addsZeroAttention: Bool](/documentation/mlcompute/mlcmultiheadattentiondescriptor/addszeroattention)

#### Inspecting Multi-Head Attention Layers

- [var descriptor: MLCMultiheadAttentionDescriptor](/documentation/mlcompute/mlcmultiheadattentionlayer/descriptor)
- [var weights: [MLCTensor]](/documentation/mlcompute/mlcmultiheadattentionlayer/weights)
- [var biases: [MLCTensor]?](/documentation/mlcompute/mlcmultiheadattentionlayer/biases)
- [var attentionBiases: [MLCTensor]?](/documentation/mlcompute/mlcmultiheadattentionlayer/attentionbiases)
- [var weightsParameters: [MLCTensorParameter]](/documentation/mlcompute/mlcmultiheadattentionlayer/weightsparameters)
- [var biasesParameters: [MLCTensorParameter]?](/documentation/mlcompute/mlcmultiheadattentionlayer/biasesparameters)
- [MLCSoftmaxLayer](/documentation/mlcompute/mlcsoftmaxlayer)

#### Creating Softmax Layers

- [convenience init(operation: MLCSoftmaxOperation)](/documentation/mlcompute/mlcsoftmaxlayer/init(operation:))
- [convenience init(operation: MLCSoftmaxOperation, dimension: Int)](/documentation/mlcompute/mlcsoftmaxlayer/init(operation:dimension:))
- [MLCSoftmaxOperation](/documentation/mlcompute/mlcsoftmaxoperation)

##### Enumeration Cases

- [case softmax](/documentation/mlcompute/mlcsoftmaxoperation/softmax)
- [case logSoftmax](/documentation/mlcompute/mlcsoftmaxoperation/logsoftmax)
- [var debugDescription: String](/documentation/mlcompute/mlcsoftmaxoperation/debugdescription)

##### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlcsoftmaxoperation/init(rawvalue:))

#### Inspecting Softmax Layers

- [var operation: MLCSoftmaxOperation](/documentation/mlcompute/mlcsoftmaxlayer/operation)
- [var dimension: Int](/documentation/mlcompute/mlcsoftmaxlayer/dimension)

### Math Layers

- [MLCArithmeticLayer](/documentation/mlcompute/mlcarithmeticlayer)

#### Creating Arithmetic Layers

- [convenience init(operation: MLCArithmeticOperation)](/documentation/mlcompute/mlcarithmeticlayer/init(operation:))
- [MLCArithmeticOperation](/documentation/mlcompute/mlcarithmeticoperation)

##### Basic Operations

- [case add](/documentation/mlcompute/mlcarithmeticoperation/add)
- [case subtract](/documentation/mlcompute/mlcarithmeticoperation/subtract)
- [case multiply](/documentation/mlcompute/mlcarithmeticoperation/multiply)
- [case multiplyNoNaN](/documentation/mlcompute/mlcarithmeticoperation/multiplynonan)
- [case divide](/documentation/mlcompute/mlcarithmeticoperation/divide)
- [case divideNoNaN](/documentation/mlcompute/mlcarithmeticoperation/dividenonan)
- [case min](/documentation/mlcompute/mlcarithmeticoperation/min)
- [case max](/documentation/mlcompute/mlcarithmeticoperation/max)

##### Rounding Operations

- [case floor](/documentation/mlcompute/mlcarithmeticoperation/floor)
- [case round](/documentation/mlcompute/mlcarithmeticoperation/round)
- [case ceil](/documentation/mlcompute/mlcarithmeticoperation/ceil)

##### Trigonometric Operations

- [case sin](/documentation/mlcompute/mlcarithmeticoperation/sin)
- [case cos](/documentation/mlcompute/mlcarithmeticoperation/cos)
- [case tan](/documentation/mlcompute/mlcarithmeticoperation/tan)
- [case asin](/documentation/mlcompute/mlcarithmeticoperation/asin)
- [case acos](/documentation/mlcompute/mlcarithmeticoperation/acos)
- [case atan](/documentation/mlcompute/mlcarithmeticoperation/atan)
- [case sinh](/documentation/mlcompute/mlcarithmeticoperation/sinh)
- [case cosh](/documentation/mlcompute/mlcarithmeticoperation/cosh)
- [case tanh](/documentation/mlcompute/mlcarithmeticoperation/tanh)
- [case asinh](/documentation/mlcompute/mlcarithmeticoperation/asinh)
- [case acosh](/documentation/mlcompute/mlcarithmeticoperation/acosh)
- [case atanh](/documentation/mlcompute/mlcarithmeticoperation/atanh)

##### Advanced Operations

- [case sqrt](/documentation/mlcompute/mlcarithmeticoperation/sqrt)
- [case rsqrt](/documentation/mlcompute/mlcarithmeticoperation/rsqrt)
- [case pow](/documentation/mlcompute/mlcarithmeticoperation/pow)
- [case exp](/documentation/mlcompute/mlcarithmeticoperation/exp)
- [case exp2](/documentation/mlcompute/mlcarithmeticoperation/exp2)
- [case log](/documentation/mlcompute/mlcarithmeticoperation/log)
- [case log2](/documentation/mlcompute/mlcarithmeticoperation/log2)

##### Debugging

- [var debugDescription: String](/documentation/mlcompute/mlcarithmeticoperation/debugdescription)

##### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlcarithmeticoperation/init(rawvalue:))

#### Inspecting Arithmetic Layers

- [var operation: MLCArithmeticOperation](/documentation/mlcompute/mlcarithmeticlayer/operation)
- [MLCReductionLayer](/documentation/mlcompute/mlcreductionlayer)

#### Creating Reduction Layers

- [convenience init?(reductionType: MLCReductionType, dimension: Int)](/documentation/mlcompute/mlcreductionlayer/init(reductiontype:dimension:))
- [convenience init?(reductionType: MLCReductionType, dimensions: [Int])](/documentation/mlcompute/mlcreductionlayer/init(reductiontype:dimensions:))
- [MLCReductionType](/documentation/mlcompute/mlcreductiontype)

##### Enumeration Cases

- [case all](/documentation/mlcompute/mlcreductiontype/all)
- [case any](/documentation/mlcompute/mlcreductiontype/any)
- [case argMax](/documentation/mlcompute/mlcreductiontype/argmax)
- [case argMin](/documentation/mlcompute/mlcreductiontype/argmin)
- [case max](/documentation/mlcompute/mlcreductiontype/max)
- [case mean](/documentation/mlcompute/mlcreductiontype/mean)
- [case min](/documentation/mlcompute/mlcreductiontype/min)
- [case none](/documentation/mlcompute/mlcreductiontype/none)
- [case sum](/documentation/mlcompute/mlcreductiontype/sum)
- [case l1Norm](/documentation/mlcompute/mlcreductiontype/l1norm)
- [var debugDescription: String](/documentation/mlcompute/mlcreductiontype/debugdescription)

##### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlcreductiontype/init(rawvalue:))

#### Inspecting Reduction Layers

- [var reductionType: MLCReductionType](/documentation/mlcompute/mlcreductionlayer/reductiontype)
- [var dimension: Int](/documentation/mlcompute/mlcreductionlayer/dimension)
- [var dimensions: [Int]](/documentation/mlcompute/mlcreductionlayer/dimensions-9oph6)
- [MLCMatMulLayer](/documentation/mlcompute/mlcmatmullayer)

#### Creating Matrix Multiplication Layers

- [convenience init?(descriptor: MLCMatMulDescriptor)](/documentation/mlcompute/mlcmatmullayer/init(descriptor:))
- [MLCMatMulDescriptor](/documentation/mlcompute/mlcmatmuldescriptor)

##### Creating Matrix Multiplication Descriptors

- [convenience init()](/documentation/mlcompute/mlcmatmuldescriptor/init())
- [convenience init?(alpha: Float, transposesX: Bool, transposesY: Bool)](/documentation/mlcompute/mlcmatmuldescriptor/init(alpha:transposesx:transposesy:))

##### Inspecting Matrix Multiplication Descriptors

- [var alpha: Float](/documentation/mlcompute/mlcmatmuldescriptor/alpha)
- [var transposesX: Bool](/documentation/mlcompute/mlcmatmuldescriptor/transposesx)
- [var transposesY: Bool](/documentation/mlcompute/mlcmatmuldescriptor/transposesy)

#### Inspecting Matrix Multiplication Layers

- [var descriptor: MLCMatMulDescriptor](/documentation/mlcompute/mlcmatmullayer/descriptor)
- [MLCFullyConnectedLayer](/documentation/mlcompute/mlcfullyconnectedlayer)

#### Creating Fully Connected Layers

- [convenience init?(weights: MLCTensor, biases: MLCTensor?, descriptor: MLCConvolutionDescriptor)](/documentation/mlcompute/mlcfullyconnectedlayer/init(weights:biases:descriptor:))
- [MLCConvolutionDescriptor](/documentation/mlcompute/mlcconvolutiondescriptor)

##### Creating Convolution Descriptors

- [convenience init(type: MLCConvolutionType, kernelSizes: (height: Int, width: Int), inputFeatureChannelCount: Int, outputFeatureChannelCount: Int, groupCount: Int, strides: (y: Int, x: Int), dilationRates: (y: Int, x: Int), paddingPolicy: MLCPaddingPolicy)](/documentation/mlcompute/mlcconvolutiondescriptor/init(type:kernelsizes:inputfeaturechannelcount:outputfeaturechannelcount:groupcount:strides:dilationrates:paddingpolicy:))
- [convenience init(transposeWithKernelWidth: Int, kernelHeight: Int, inputFeatureChannelCount: Int, outputFeatureChannelCount: Int)](/documentation/mlcompute/mlcconvolutiondescriptor/init(transposewithkernelwidth:kernelheight:inputfeaturechannelcount:outputfeaturechannelcount:))
- [convenience init(depthwiseWithKernelWidth: Int, kernelHeight: Int, inputFeatureChannelCount: Int, channelMultiplier: Int)](/documentation/mlcompute/mlcconvolutiondescriptor/init(depthwisewithkernelwidth:kernelheight:inputfeaturechannelcount:channelmultiplier:))
- [MLCConvolutionType](/documentation/mlcompute/mlcconvolutiontype)

###### Enumeration Cases

- [case standard](/documentation/mlcompute/mlcconvolutiontype/standard)
- [case depthwise](/documentation/mlcompute/mlcconvolutiontype/depthwise)
- [case transposed](/documentation/mlcompute/mlcconvolutiontype/transposed)
- [var debugDescription: String](/documentation/mlcompute/mlcconvolutiontype/debugdescription)

###### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlcconvolutiontype/init(rawvalue:))

##### Inspecting Convolution Descriptors

- [var convolutionType: MLCConvolutionType](/documentation/mlcompute/mlcconvolutiondescriptor/convolutiontype)
- [var kernelSizes: (height: Int, width: Int)](/documentation/mlcompute/mlcconvolutiondescriptor/kernelsizes)
- [var inputFeatureChannelCount: Int](/documentation/mlcompute/mlcconvolutiondescriptor/inputfeaturechannelcount)
- [var outputFeatureChannelCount: Int](/documentation/mlcompute/mlcconvolutiondescriptor/outputfeaturechannelcount)
- [var strides: (y: Int, x: Int)](/documentation/mlcompute/mlcconvolutiondescriptor/strides)
- [var dilationRates: (y: Int, x: Int)](/documentation/mlcompute/mlcconvolutiondescriptor/dilationrates)
- [var groupCount: Int](/documentation/mlcompute/mlcconvolutiondescriptor/groupcount)
- [var paddingPolicy: MLCPaddingPolicy](/documentation/mlcompute/mlcconvolutiondescriptor/paddingpolicy-61tq3)
- [var isConvolutionTranspose: Bool](/documentation/mlcompute/mlcconvolutiondescriptor/isconvolutiontranspose)
- [var usesDepthwiseConvolution: Bool](/documentation/mlcompute/mlcconvolutiondescriptor/usesdepthwiseconvolution)

#### Inspecting Fully Connected Layers

- [var descriptor: MLCConvolutionDescriptor](/documentation/mlcompute/mlcfullyconnectedlayer/descriptor)
- [var weights: MLCTensor](/documentation/mlcompute/mlcfullyconnectedlayer/weights)
- [var biases: MLCTensor?](/documentation/mlcompute/mlcfullyconnectedlayer/biases)
- [var biasesParameter: MLCTensorParameter?](/documentation/mlcompute/mlcfullyconnectedlayer/biasesparameter)
- [var weightsParameter: MLCTensorParameter](/documentation/mlcompute/mlcfullyconnectedlayer/weightsparameter)
- [MLCGramMatrixLayer](/documentation/mlcompute/mlcgrammatrixlayer)

#### Creating Gram Matrix Layers

- [convenience init(scale: Float)](/documentation/mlcompute/mlcgrammatrixlayer/init(scale:))

#### Inspecting Gram Matrix Layers

- [var scale: Float](/documentation/mlcompute/mlcgrammatrixlayer/scale)
- [MLCComparisonLayer](/documentation/mlcompute/mlccomparisonlayer)

#### Creating Comparison Layers

- [convenience init(operation: MLCComparisonOperation)](/documentation/mlcompute/mlccomparisonlayer/init(operation:))
- [MLCComparisonOperation](/documentation/mlcompute/mlccomparisonoperation)

##### Enumeration Cases

- [case equal](/documentation/mlcompute/mlccomparisonoperation/equal)
- [case greater](/documentation/mlcompute/mlccomparisonoperation/greater)
- [case greaterOrEqual](/documentation/mlcompute/mlccomparisonoperation/greaterorequal)
- [case less](/documentation/mlcompute/mlccomparisonoperation/less)
- [case lessOrEqual](/documentation/mlcompute/mlccomparisonoperation/lessorequal)
- [case logicalAND](/documentation/mlcompute/mlccomparisonoperation/logicaland)
- [case logicalNAND](/documentation/mlcompute/mlccomparisonoperation/logicalnand)
- [case logicalNOR](/documentation/mlcompute/mlccomparisonoperation/logicalnor)
- [case logicalNOT](/documentation/mlcompute/mlccomparisonoperation/logicalnot)
- [case logicalOR](/documentation/mlcompute/mlccomparisonoperation/logicalor)
- [case logicalXOR](/documentation/mlcompute/mlccomparisonoperation/logicalxor)
- [case notEqual](/documentation/mlcompute/mlccomparisonoperation/notequal)
- [var debugDescription: String](/documentation/mlcompute/mlccomparisonoperation/debugdescription)

##### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlccomparisonoperation/init(rawvalue:))

#### Inspecting Comparison Layers

- [var operation: MLCComparisonOperation](/documentation/mlcompute/mlccomparisonlayer/operation)

### Transformation Layers

- [MLCTransposeLayer](/documentation/mlcompute/mlctransposelayer)

#### Creating Transpose Layers

- [convenience init?(dimensions: [Int])](/documentation/mlcompute/mlctransposelayer/init(dimensions:))

#### Inspecting Transpose Layers

- [var dimensions: [Int]](/documentation/mlcompute/mlctransposelayer/dimensions-71ed6)
- [MLCConcatenationLayer](/documentation/mlcompute/mlcconcatenationlayer)

#### Creating Concatenation Layers

- [convenience init()](/documentation/mlcompute/mlcconcatenationlayer/init())
- [convenience init(dimension: Int)](/documentation/mlcompute/mlcconcatenationlayer/init(dimension:))

#### Inspecting Concatenation Layers

- [var dimension: Int](/documentation/mlcompute/mlcconcatenationlayer/dimension)
- [MLCReshapeLayer](/documentation/mlcompute/mlcreshapelayer)

#### Creating Reshape Layers

- [convenience init?(shape: [Int])](/documentation/mlcompute/mlcreshapelayer/init(shape:))

#### Inspecting Reshape Layers

- [var shape: [Int]](/documentation/mlcompute/mlcreshapelayer/shape-8k50y)
- [MLCSliceLayer](/documentation/mlcompute/mlcslicelayer)

#### Creating Slice Layers

- [convenience init?(start: [Int], end: [Int], stride: [Int]?)](/documentation/mlcompute/mlcslicelayer/init(start:end:stride:))

#### Inspecting Slice Layers

- [var start: [Int]](/documentation/mlcompute/mlcslicelayer/start-6wsh6)
- [var end: [Int]](/documentation/mlcompute/mlcslicelayer/end-9xw91)
- [var stride: [Int]?](/documentation/mlcompute/mlcslicelayer/stride-84fhb)
- [MLCSplitLayer](/documentation/mlcompute/mlcsplitlayer)

#### Creating Split Layers

- [convenience init(splitCount: Int, dimension: Int)](/documentation/mlcompute/mlcsplitlayer/init(splitcount:dimension:))
- [convenience init(splitSectionLengths: [Int], dimension: Int)](/documentation/mlcompute/mlcsplitlayer/init(splitsectionlengths:dimension:))

#### Inspecting Split Layers

- [var dimension: Int](/documentation/mlcompute/mlcsplitlayer/dimension)
- [var splitCount: Int](/documentation/mlcompute/mlcsplitlayer/splitcount)
- [var splitSectionLengths: [Int]?](/documentation/mlcompute/mlcsplitlayer/splitsectionlengths-5abch)
- [MLCPaddingLayer](/documentation/mlcompute/mlcpaddinglayer)

#### Creating Padding Layers

- [convenience init(reflectionPadding: [Int])](/documentation/mlcompute/mlcpaddinglayer/init(reflectionpadding:))
- [convenience init(symmetricPadding: [Int])](/documentation/mlcompute/mlcpaddinglayer/init(symmetricpadding:))
- [convenience init(zeroPadding: [Int])](/documentation/mlcompute/mlcpaddinglayer/init(zeropadding:))
- [convenience init(constantPadding: [Int], constantValue: Float)](/documentation/mlcompute/mlcpaddinglayer/init(constantpadding:constantvalue:))

#### Inspecting Padding Layers

- [var paddingType: MLCPaddingType](/documentation/mlcompute/mlcpaddinglayer/paddingtype)
- [var paddingLeft: Int](/documentation/mlcompute/mlcpaddinglayer/paddingleft)
- [var paddingRight: Int](/documentation/mlcompute/mlcpaddinglayer/paddingright)
- [var paddingTop: Int](/documentation/mlcompute/mlcpaddinglayer/paddingtop)
- [var paddingBottom: Int](/documentation/mlcompute/mlcpaddinglayer/paddingbottom)
- [var constantValue: Float](/documentation/mlcompute/mlcpaddinglayer/constantvalue)
- [MLCScatterLayer](/documentation/mlcompute/mlcscatterlayer)

#### Creating Scatter Layers

- [convenience init?(dimension: Int, reductionType: MLCReductionType)](/documentation/mlcompute/mlcscatterlayer/init(dimension:reductiontype:))

#### Inspecting Scatter Layers

- [var dimension: Int](/documentation/mlcompute/mlcscatterlayer/dimension)
- [var reductionType: MLCReductionType](/documentation/mlcompute/mlcscatterlayer/reductiontype)
- [MLCSelectionLayer](/documentation/mlcompute/mlcselectionlayer)

#### Creating Selection Layers

- [convenience init()](/documentation/mlcompute/mlcselectionlayer/init())
- [MLCGatherLayer](/documentation/mlcompute/mlcgatherlayer)

#### Creating Gather Layers

- [convenience init(dimension: Int)](/documentation/mlcompute/mlcgatherlayer/init(dimension:))

#### Inspecting Gather Layers

- [var dimension: Int](/documentation/mlcompute/mlcgatherlayer/dimension)

### Normalization Layers

- [MLCLayerNormalizationLayer](/documentation/mlcompute/mlclayernormalizationlayer)

#### Creating Layer Normalization Layers

- [convenience init?(normalizedShape: [Int], beta: MLCTensor, gamma: MLCTensor, varianceEpsilon: Float)](/documentation/mlcompute/mlclayernormalizationlayer/init(normalizedshape:beta:gamma:varianceepsilon:)-5i2aa)
- [convenience init?(normalizedShape: [Int], beta: MLCTensor?, gamma: MLCTensor?, varianceEpsilon: Float)](/documentation/mlcompute/mlclayernormalizationlayer/init(normalizedshape:beta:gamma:varianceepsilon:)-28e6g)

#### Inspecting Layer Normalization Layers

- [var normalizedShape: [Int]](/documentation/mlcompute/mlclayernormalizationlayer/normalizedshape-8ujvv)
- [var beta: MLCTensor?](/documentation/mlcompute/mlclayernormalizationlayer/beta)
- [var gamma: MLCTensor?](/documentation/mlcompute/mlclayernormalizationlayer/gamma)
- [var varianceEpsilon: Float](/documentation/mlcompute/mlclayernormalizationlayer/varianceepsilon)
- [var betaParameter: MLCTensorParameter?](/documentation/mlcompute/mlclayernormalizationlayer/betaparameter)
- [var gammaParameter: MLCTensorParameter?](/documentation/mlcompute/mlclayernormalizationlayer/gammaparameter)
- [MLCBatchNormalizationLayer](/documentation/mlcompute/mlcbatchnormalizationlayer)

#### Creating Batch Normalization Layers

- [convenience init?(featureChannelCount: Int, mean: MLCTensor, variance: MLCTensor, beta: MLCTensor?, gamma: MLCTensor?, varianceEpsilon: Float)](/documentation/mlcompute/mlcbatchnormalizationlayer/init(featurechannelcount:mean:variance:beta:gamma:varianceepsilon:))
- [convenience init?(featureChannelCount: Int, mean: MLCTensor, variance: MLCTensor, beta: MLCTensor?, gamma: MLCTensor?, varianceEpsilon: Float, momentum: Float)](/documentation/mlcompute/mlcbatchnormalizationlayer/init(featurechannelcount:mean:variance:beta:gamma:varianceepsilon:momentum:))

#### Inspecting Batch Normalization Layers

- [var featureChannelCount: Int](/documentation/mlcompute/mlcbatchnormalizationlayer/featurechannelcount)
- [var mean: MLCTensor](/documentation/mlcompute/mlcbatchnormalizationlayer/mean)
- [var variance: MLCTensor](/documentation/mlcompute/mlcbatchnormalizationlayer/variance)
- [var beta: MLCTensor?](/documentation/mlcompute/mlcbatchnormalizationlayer/beta)
- [var gamma: MLCTensor?](/documentation/mlcompute/mlcbatchnormalizationlayer/gamma)
- [var varianceEpsilon: Float](/documentation/mlcompute/mlcbatchnormalizationlayer/varianceepsilon)
- [var momentum: Float](/documentation/mlcompute/mlcbatchnormalizationlayer/momentum)
- [var betaParameter: MLCTensorParameter?](/documentation/mlcompute/mlcbatchnormalizationlayer/betaparameter)
- [var gammaParameter: MLCTensorParameter?](/documentation/mlcompute/mlcbatchnormalizationlayer/gammaparameter)
- [MLCGroupNormalizationLayer](/documentation/mlcompute/mlcgroupnormalizationlayer)

#### Creating Group Normalization Layers

- [convenience init?(featureChannelCount: Int, groupCount: Int, beta: MLCTensor?, gamma: MLCTensor?, varianceEpsilon: Float)](/documentation/mlcompute/mlcgroupnormalizationlayer/init(featurechannelcount:groupcount:beta:gamma:varianceepsilon:))

#### Inspecting Group Normalization Layers

- [var featureChannelCount: Int](/documentation/mlcompute/mlcgroupnormalizationlayer/featurechannelcount)
- [var groupCount: Int](/documentation/mlcompute/mlcgroupnormalizationlayer/groupcount)
- [var beta: MLCTensor?](/documentation/mlcompute/mlcgroupnormalizationlayer/beta)
- [var gamma: MLCTensor?](/documentation/mlcompute/mlcgroupnormalizationlayer/gamma)
- [var varianceEpsilon: Float](/documentation/mlcompute/mlcgroupnormalizationlayer/varianceepsilon)
- [var betaParameter: MLCTensorParameter?](/documentation/mlcompute/mlcgroupnormalizationlayer/betaparameter)
- [var gammaParameter: MLCTensorParameter?](/documentation/mlcompute/mlcgroupnormalizationlayer/gammaparameter)
- [MLCInstanceNormalizationLayer](/documentation/mlcompute/mlcinstancenormalizationlayer)

#### Creating Instance Normalization Layers

- [convenience init?(featureChannelCount: Int, beta: MLCTensor?, gamma: MLCTensor?, varianceEpsilon: Float)](/documentation/mlcompute/mlcinstancenormalizationlayer/init(featurechannelcount:beta:gamma:varianceepsilon:))
- [convenience init?(featureChannelCount: Int, beta: MLCTensor?, gamma: MLCTensor?, varianceEpsilon: Float, momentum: Float)](/documentation/mlcompute/mlcinstancenormalizationlayer/init(featurechannelcount:beta:gamma:varianceepsilon:momentum:))
- [convenience init?(featureChannelCount: Int, mean: MLCTensor, variance: MLCTensor, beta: MLCTensor?, gamma: MLCTensor?, varianceEpsilon: Float, momentum: Float)](/documentation/mlcompute/mlcinstancenormalizationlayer/init(featurechannelcount:mean:variance:beta:gamma:varianceepsilon:momentum:))

#### Inspecting Instance Normalization Layers

- [var beta: MLCTensor?](/documentation/mlcompute/mlcinstancenormalizationlayer/beta)
- [var betaParameter: MLCTensorParameter?](/documentation/mlcompute/mlcinstancenormalizationlayer/betaparameter)
- [var featureChannelCount: Int](/documentation/mlcompute/mlcinstancenormalizationlayer/featurechannelcount)
- [var gamma: MLCTensor?](/documentation/mlcompute/mlcinstancenormalizationlayer/gamma)
- [var gammaParameter: MLCTensorParameter?](/documentation/mlcompute/mlcinstancenormalizationlayer/gammaparameter)
- [var mean: MLCTensor?](/documentation/mlcompute/mlcinstancenormalizationlayer/mean)
- [var momentum: Float](/documentation/mlcompute/mlcinstancenormalizationlayer/momentum)
- [var variance: MLCTensor?](/documentation/mlcompute/mlcinstancenormalizationlayer/variance)
- [var varianceEpsilon: Float](/documentation/mlcompute/mlcinstancenormalizationlayer/varianceepsilon)
- [MLCDropoutLayer](/documentation/mlcompute/mlcdropoutlayer)

#### Creating Dropout Layers

- [convenience init(rate: Float, seed: Int)](/documentation/mlcompute/mlcdropoutlayer/init(rate:seed:))

#### Inspecting a Dropout Layer

- [var rate: Float](/documentation/mlcompute/mlcdropoutlayer/rate)
- [var seed: Int](/documentation/mlcompute/mlcdropoutlayer/seed)

### Convolution and Recurrent Layers

- [MLCConvolutionLayer](/documentation/mlcompute/mlcconvolutionlayer)

#### Creating Convolution Layers

- [convenience init?(weights: MLCTensor, biases: MLCTensor?, descriptor: MLCConvolutionDescriptor)](/documentation/mlcompute/mlcconvolutionlayer/init(weights:biases:descriptor:))
- [MLCConvolutionDescriptor](/documentation/mlcompute/mlcconvolutiondescriptor)

##### Creating Convolution Descriptors

- [convenience init(type: MLCConvolutionType, kernelSizes: (height: Int, width: Int), inputFeatureChannelCount: Int, outputFeatureChannelCount: Int, groupCount: Int, strides: (y: Int, x: Int), dilationRates: (y: Int, x: Int), paddingPolicy: MLCPaddingPolicy)](/documentation/mlcompute/mlcconvolutiondescriptor/init(type:kernelsizes:inputfeaturechannelcount:outputfeaturechannelcount:groupcount:strides:dilationrates:paddingpolicy:))
- [convenience init(transposeWithKernelWidth: Int, kernelHeight: Int, inputFeatureChannelCount: Int, outputFeatureChannelCount: Int)](/documentation/mlcompute/mlcconvolutiondescriptor/init(transposewithkernelwidth:kernelheight:inputfeaturechannelcount:outputfeaturechannelcount:))
- [convenience init(depthwiseWithKernelWidth: Int, kernelHeight: Int, inputFeatureChannelCount: Int, channelMultiplier: Int)](/documentation/mlcompute/mlcconvolutiondescriptor/init(depthwisewithkernelwidth:kernelheight:inputfeaturechannelcount:channelmultiplier:))
- [MLCConvolutionType](/documentation/mlcompute/mlcconvolutiontype)

###### Enumeration Cases

- [case standard](/documentation/mlcompute/mlcconvolutiontype/standard)
- [case depthwise](/documentation/mlcompute/mlcconvolutiontype/depthwise)
- [case transposed](/documentation/mlcompute/mlcconvolutiontype/transposed)
- [var debugDescription: String](/documentation/mlcompute/mlcconvolutiontype/debugdescription)

###### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlcconvolutiontype/init(rawvalue:))

##### Inspecting Convolution Descriptors

- [var convolutionType: MLCConvolutionType](/documentation/mlcompute/mlcconvolutiondescriptor/convolutiontype)
- [var kernelSizes: (height: Int, width: Int)](/documentation/mlcompute/mlcconvolutiondescriptor/kernelsizes)
- [var inputFeatureChannelCount: Int](/documentation/mlcompute/mlcconvolutiondescriptor/inputfeaturechannelcount)
- [var outputFeatureChannelCount: Int](/documentation/mlcompute/mlcconvolutiondescriptor/outputfeaturechannelcount)
- [var strides: (y: Int, x: Int)](/documentation/mlcompute/mlcconvolutiondescriptor/strides)
- [var dilationRates: (y: Int, x: Int)](/documentation/mlcompute/mlcconvolutiondescriptor/dilationrates)
- [var groupCount: Int](/documentation/mlcompute/mlcconvolutiondescriptor/groupcount)
- [var paddingPolicy: MLCPaddingPolicy](/documentation/mlcompute/mlcconvolutiondescriptor/paddingpolicy-61tq3)
- [var isConvolutionTranspose: Bool](/documentation/mlcompute/mlcconvolutiondescriptor/isconvolutiontranspose)
- [var usesDepthwiseConvolution: Bool](/documentation/mlcompute/mlcconvolutiondescriptor/usesdepthwiseconvolution)

#### Inspecting Convolution Layers

- [var descriptor: MLCConvolutionDescriptor](/documentation/mlcompute/mlcconvolutionlayer/descriptor)
- [var weights: MLCTensor](/documentation/mlcompute/mlcconvolutionlayer/weights)
- [var biases: MLCTensor?](/documentation/mlcompute/mlcconvolutionlayer/biases)
- [var weightsParameter: MLCTensorParameter](/documentation/mlcompute/mlcconvolutionlayer/weightsparameter)
- [var biasesParameter: MLCTensorParameter?](/documentation/mlcompute/mlcconvolutionlayer/biasesparameter)
- [MLCLSTMLayer](/documentation/mlcompute/mlclstmlayer)

#### Creating LSTM Layers

- [convenience init?(descriptor: MLCLSTMDescriptor, inputWeights: [MLCTensor], hiddenWeights: [MLCTensor], biases: [MLCTensor]?)](/documentation/mlcompute/mlclstmlayer/init(descriptor:inputweights:hiddenweights:biases:))
- [convenience init?(descriptor: MLCLSTMDescriptor, inputWeights: [MLCTensor], hiddenWeights: [MLCTensor], peepholeWeights: [MLCTensor]?, biases: [MLCTensor]?)](/documentation/mlcompute/mlclstmlayer/init(descriptor:inputweights:hiddenweights:peepholeweights:biases:))
- [convenience init?(descriptor: MLCLSTMDescriptor, inputWeights: [MLCTensor], hiddenWeights: [MLCTensor], peepholeWeights: [MLCTensor]?, biases: [MLCTensor]?, gateActivations: [MLCActivationDescriptor], outputResultActivation: MLCActivationDescriptor)](/documentation/mlcompute/mlclstmlayer/init(descriptor:inputweights:hiddenweights:peepholeweights:biases:gateactivations:outputresultactivation:))
- [MLCLSTMDescriptor](/documentation/mlcompute/mlclstmdescriptor)

##### Creating LSTM Descriptors

- [convenience init(inputSize: Int, hiddenSize: Int, layerCount: Int)](/documentation/mlcompute/mlclstmdescriptor/init(inputsize:hiddensize:layercount:))
- [convenience init(inputSize: Int, hiddenSize: Int, layerCount: Int, usesBiases: Bool, isBidirectional: Bool, dropout: Float)](/documentation/mlcompute/mlclstmdescriptor/init(inputsize:hiddensize:layercount:usesbiases:isbidirectional:dropout:))
- [convenience init(inputSize: Int, hiddenSize: Int, layerCount: Int, usesBiases: Bool, batchFirst: Bool, isBidirectional: Bool, dropout: Float)](/documentation/mlcompute/mlclstmdescriptor/init(inputsize:hiddensize:layercount:usesbiases:batchfirst:isbidirectional:dropout:))
- [convenience init(inputSize: Int, hiddenSize: Int, layerCount: Int, usesBiases: Bool, batchFirst: Bool, isBidirectional: Bool, returnsSequences: Bool, dropout: Float)](/documentation/mlcompute/mlclstmdescriptor/init(inputsize:hiddensize:layercount:usesbiases:batchfirst:isbidirectional:returnssequences:dropout:))
- [convenience init(inputSize: Int, hiddenSize: Int, layerCount: Int, usesBiases: Bool, batchFirst: Bool, isBidirectional: Bool, returnsSequences: Bool, dropout: Float, resultMode: MLCLSTMResultMode)](/documentation/mlcompute/mlclstmdescriptor/init(inputsize:hiddensize:layercount:usesbiases:batchfirst:isbidirectional:returnssequences:dropout:resultmode:))

##### Inspecting LSTM Descriptors

- [var batchFirst: Bool](/documentation/mlcompute/mlclstmdescriptor/batchfirst)
- [var dropout: Float](/documentation/mlcompute/mlclstmdescriptor/dropout)
- [var hiddenSize: Int](/documentation/mlcompute/mlclstmdescriptor/hiddensize)
- [var inputSize: Int](/documentation/mlcompute/mlclstmdescriptor/inputsize)
- [var isBidirectional: Bool](/documentation/mlcompute/mlclstmdescriptor/isbidirectional)
- [var layerCount: Int](/documentation/mlcompute/mlclstmdescriptor/layercount)
- [var resultMode: MLCLSTMResultMode](/documentation/mlcompute/mlclstmdescriptor/resultmode)
- [var returnsSequences: Bool](/documentation/mlcompute/mlclstmdescriptor/returnssequences)
- [var usesBiases: Bool](/documentation/mlcompute/mlclstmdescriptor/usesbiases)
- [MLCLSTMResultMode](/documentation/mlcompute/mlclstmresultmode)

##### Enumeration Cases

- [case output](/documentation/mlcompute/mlclstmresultmode/output)
- [case outputAndStates](/documentation/mlcompute/mlclstmresultmode/outputandstates)
- [var debugDescription: String](/documentation/mlcompute/mlclstmresultmode/debugdescription)

##### Initializers

- [init?(rawValue: UInt64)](/documentation/mlcompute/mlclstmresultmode/init(rawvalue:))

#### Inspecting LSTM Layers

- [var descriptor: MLCLSTMDescriptor](/documentation/mlcompute/mlclstmlayer/descriptor)
- [var gateActivations: [MLCActivationDescriptor]](/documentation/mlcompute/mlclstmlayer/gateactivations)
- [var outputResultActivation: MLCActivationDescriptor](/documentation/mlcompute/mlclstmlayer/outputresultactivation)
- [var inputWeights: [MLCTensor]](/documentation/mlcompute/mlclstmlayer/inputweights)
- [var hiddenWeights: [MLCTensor]](/documentation/mlcompute/mlclstmlayer/hiddenweights)
- [var peepholeWeights: [MLCTensor]?](/documentation/mlcompute/mlclstmlayer/peepholeweights)
- [var biases: [MLCTensor]?](/documentation/mlcompute/mlclstmlayer/biases)
- [var inputWeightsParameters: [MLCTensorParameter]](/documentation/mlcompute/mlclstmlayer/inputweightsparameters)
- [var hiddenWeightsParameters: [MLCTensorParameter]](/documentation/mlcompute/mlclstmlayer/hiddenweightsparameters)
- [var peepholeWeightsParameters: [MLCTensorParameter]?](/documentation/mlcompute/mlclstmlayer/peepholeweightsparameters)
- [var biasesParameters: [MLCTensorParameter]?](/documentation/mlcompute/mlclstmlayer/biasesparameters)
- [MLCPoolingLayer](/documentation/mlcompute/mlcpoolinglayer)

#### Creating Pooling Layers

- [convenience init(descriptor: MLCPoolingDescriptor)](/documentation/mlcompute/mlcpoolinglayer/init(descriptor:))
- [MLCPoolingDescriptor](/documentation/mlcompute/mlcpoolingdescriptor)

##### Creating Pooling Descriptors

- [convenience init(type: MLCPoolingType, kernelSizes: (height: Int, width: Int), strides: (y: Int, x: Int), dilationRates: (y: Int, x: Int), paddingPolicy: MLCPaddingPolicy)](/documentation/mlcompute/mlcpoolingdescriptor/init(type:kernelsizes:strides:dilationrates:paddingpolicy:))

##### Inspecting Pooling Descriptors

- [var poolingType: MLCPoolingType](/documentation/mlcompute/mlcpoolingdescriptor/poolingtype-4ni07)
- [var kernelSizes: (height: Int, width: Int)](/documentation/mlcompute/mlcpoolingdescriptor/kernelsizes)
- [var strides: (y: Int, x: Int)](/documentation/mlcompute/mlcpoolingdescriptor/strides)
- [var dilationRates: (y: Int, x: Int)](/documentation/mlcompute/mlcpoolingdescriptor/dilationrates)
- [var paddingPolicy: MLCPaddingPolicy](/documentation/mlcompute/mlcpoolingdescriptor/paddingpolicy-7p8a2)
- [MLCPoolingType](/documentation/mlcompute/mlcpoolingtype-wb8j)

##### Enumeration Cases

- [case max](/documentation/mlcompute/mlcpoolingtype-wb8j/max)
- [case average(countIncludesPadding: Bool)](/documentation/mlcompute/mlcpoolingtype-wb8j/average(countincludespadding:))
- [case l2Norm](/documentation/mlcompute/mlcpoolingtype-wb8j/l2norm)
- [var debugDescription: String](/documentation/mlcompute/mlcpoolingtype-wb8j/debugdescription)

#### Inspecting Pooling Layers

- [var descriptor: MLCPoolingDescriptor](/documentation/mlcompute/mlcpoolinglayer/descriptor)
- [MLCUpsampleLayer](/documentation/mlcompute/mlcupsamplelayer)

#### Creating Upsample Layers

- [convenience init?(shape: [Int])](/documentation/mlcompute/mlcupsamplelayer/init(shape:))
- [convenience init?(shape: [Int], sampleMode: MLCSampleMode, alignsCorners: Bool)](/documentation/mlcompute/mlcupsamplelayer/init(shape:samplemode:alignscorners:))
- [MLCSampleMode](/documentation/mlcompute/mlcsamplemode)

##### Enumeration Cases

- [case nearest](/documentation/mlcompute/mlcsamplemode/nearest)
- [case linear](/documentation/mlcompute/mlcsamplemode/linear)
- [var debugDescription: String](/documentation/mlcompute/mlcsamplemode/debugdescription)

##### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlcsamplemode/init(rawvalue:))

#### Inspecting Upsample Layers

- [var shape: [Int]](/documentation/mlcompute/mlcupsamplelayer/shape-61n1u)
- [var sampleMode: MLCSampleMode](/documentation/mlcompute/mlcupsamplelayer/samplemode)
- [var alignsCorners: Bool](/documentation/mlcompute/mlcupsamplelayer/alignscorners)
- [MLCEmbeddingLayer](/documentation/mlcompute/mlcembeddinglayer)

#### Creating Embedding Layers

- [convenience init(descriptor: MLCEmbeddingDescriptor, weights: MLCTensor)](/documentation/mlcompute/mlcembeddinglayer/init(descriptor:weights:))
- [MLCEmbeddingDescriptor](/documentation/mlcompute/mlcembeddingdescriptor)

##### Creating Embedding Descriptors

- [convenience init?(embeddingCount: Int, embeddingDimension: Int)](/documentation/mlcompute/mlcembeddingdescriptor/init(embeddingcount:embeddingdimension:))
- [convenience init?(embeddingCount: Int, embeddingDimension: Int, paddingIndex: Int?, maximumNorm: Float?, pNorm: Float?, scalesGradientByFrequency: Bool)](/documentation/mlcompute/mlcembeddingdescriptor/init(embeddingcount:embeddingdimension:paddingindex:maximumnorm:pnorm:scalesgradientbyfrequency:))

##### Inspecting Embedding Descriptors

- [var embeddingCount: Int](/documentation/mlcompute/mlcembeddingdescriptor/embeddingcount-77gxz)
- [var embeddingDimension: Int](/documentation/mlcompute/mlcembeddingdescriptor/embeddingdimension-1u9g)
- [var paddingIndex: Int?](/documentation/mlcompute/mlcembeddingdescriptor/paddingindex-pb1e)
- [var maximumNorm: Float?](/documentation/mlcompute/mlcembeddingdescriptor/maximumnorm-17u0k)
- [var pNorm: Float?](/documentation/mlcompute/mlcembeddingdescriptor/pnorm-8vhw1)
- [var scalesGradientByFrequency: Bool](/documentation/mlcompute/mlcembeddingdescriptor/scalesgradientbyfrequency)

#### Inspecting Embedding Layers

- [var descriptor: MLCEmbeddingDescriptor](/documentation/mlcompute/mlcembeddinglayer/descriptor)
- [var weights: MLCTensor](/documentation/mlcompute/mlcembeddinglayer/weights)
- [var weightsParameter: MLCTensorParameter](/documentation/mlcompute/mlcembeddinglayer/weightsparameter)

### Loss Layers

- [MLCLossLayer](/documentation/mlcompute/mlclosslayer)

#### Creating Loss Layers with Descriptors

- [convenience init(descriptor: MLCLossDescriptor)](/documentation/mlcompute/mlclosslayer/init(descriptor:))
- [convenience init(descriptor: MLCLossDescriptor, weights: MLCTensor)](/documentation/mlcompute/mlclosslayer/init(descriptor:weights:))
- [MLCLossDescriptor](/documentation/mlcompute/mlclossdescriptor)

##### Creating Loss Descriptors

- [convenience init(type: MLCLossType, reductionType: MLCReductionType)](/documentation/mlcompute/mlclossdescriptor/init(type:reductiontype:))
- [convenience init(type: MLCLossType, reductionType: MLCReductionType, weight: Float)](/documentation/mlcompute/mlclossdescriptor/init(type:reductiontype:weight:))
- [convenience init(type: MLCLossType, reductionType: MLCReductionType, weight: Float, labelSmoothing: Float, classCount: Int)](/documentation/mlcompute/mlclossdescriptor/init(type:reductiontype:weight:labelsmoothing:classcount:))
- [convenience init(type: MLCLossType, reductionType: MLCReductionType, weight: Float, labelSmoothing: Float, classCount: Int, epsilon: Float, delta: Float)](/documentation/mlcompute/mlclossdescriptor/init(type:reductiontype:weight:labelsmoothing:classcount:epsilon:delta:))

##### Inspecting Loss Descriptors

- [var lossType: MLCLossType](/documentation/mlcompute/mlclossdescriptor/losstype)
- [var reductionType: MLCReductionType](/documentation/mlcompute/mlclossdescriptor/reductiontype)
- [var weight: Float](/documentation/mlcompute/mlclossdescriptor/weight)
- [var labelSmoothing: Float](/documentation/mlcompute/mlclossdescriptor/labelsmoothing)
- [var classCount: Int](/documentation/mlcompute/mlclossdescriptor/classcount)
- [var epsilon: Float](/documentation/mlcompute/mlclossdescriptor/epsilon)
- [var delta: Float](/documentation/mlcompute/mlclossdescriptor/delta)
- [MLCLossType](/documentation/mlcompute/mlclosstype)

##### Enumeration Cases

- [case categoricalCrossEntropy](/documentation/mlcompute/mlclosstype/categoricalcrossentropy)
- [case cosineDistance](/documentation/mlcompute/mlclosstype/cosinedistance)
- [case hinge](/documentation/mlcompute/mlclosstype/hinge)
- [case huber](/documentation/mlcompute/mlclosstype/huber)
- [case log](/documentation/mlcompute/mlclosstype/log)
- [case meanAbsoluteError](/documentation/mlcompute/mlclosstype/meanabsoluteerror)
- [case meanSquaredError](/documentation/mlcompute/mlclosstype/meansquarederror)
- [case sigmoidCrossEntropy](/documentation/mlcompute/mlclosstype/sigmoidcrossentropy)
- [case softmaxCrossEntropy](/documentation/mlcompute/mlclosstype/softmaxcrossentropy)
- [var debugDescription: String](/documentation/mlcompute/mlclosstype/debugdescription)

##### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlclosstype/init(rawvalue:))

#### Creating Loss Layers with Scalar Weights

- [class func softmaxCrossEntropy(reductionType: MLCReductionType, labelSmoothing: Float, classCount: Int, weight: Float) -> Self](/documentation/mlcompute/mlclosslayer/softmaxcrossentropy(reductiontype:labelsmoothing:classcount:weight:))
- [class func categoricalCrossEntropy(reductionType: MLCReductionType, labelSmoothing: Float, classCount: Int, weight: Float) -> Self](/documentation/mlcompute/mlclosslayer/categoricalcrossentropy(reductiontype:labelsmoothing:classcount:weight:))
- [class func sigmoidCrossEntropy(reductionType: MLCReductionType, labelSmoothing: Float, weight: Float) -> Self](/documentation/mlcompute/mlclosslayer/sigmoidcrossentropy(reductiontype:labelsmoothing:weight:))
- [class func log(reductionType: MLCReductionType, epsilon: Float, weight: Float) -> Self](/documentation/mlcompute/mlclosslayer/log(reductiontype:epsilon:weight:))
- [class func huberLoss(reductionType: MLCReductionType, delta: Float, weight: Float) -> Self](/documentation/mlcompute/mlclosslayer/huberloss(reductiontype:delta:weight:))
- [class func meanAbsoluteError(reductionType: MLCReductionType, weight: Float) -> Self](/documentation/mlcompute/mlclosslayer/meanabsoluteerror(reductiontype:weight:))
- [class func meanSquaredError(reductionType: MLCReductionType, weight: Float) -> Self](/documentation/mlcompute/mlclosslayer/meansquarederror(reductiontype:weight:))
- [class func hingeLoss(reductionType: MLCReductionType, weight: Float) -> Self](/documentation/mlcompute/mlclosslayer/hingeloss(reductiontype:weight:))
- [class func cosineDistance(reductionType: MLCReductionType, weight: Float) -> Self](/documentation/mlcompute/mlclosslayer/cosinedistance(reductiontype:weight:))

#### Creating Loss Layers with Tensor Weights

- [class func softmaxCrossEntropy(reductionType: MLCReductionType, labelSmoothing: Float, classCount: Int, weights: MLCTensor?) -> Self](/documentation/mlcompute/mlclosslayer/softmaxcrossentropy(reductiontype:labelsmoothing:classcount:weights:))
- [class func categoricalCrossEntropy(reductionType: MLCReductionType, labelSmoothing: Float, classCount: Int, weights: MLCTensor?) -> Self](/documentation/mlcompute/mlclosslayer/categoricalcrossentropy(reductiontype:labelsmoothing:classcount:weights:))
- [class func sigmoidCrossEntropy(reductionType: MLCReductionType, labelSmoothing: Float, weights: MLCTensor?) -> Self](/documentation/mlcompute/mlclosslayer/sigmoidcrossentropy(reductiontype:labelsmoothing:weights:))
- [class func log(reductionType: MLCReductionType, epsilon: Float, weights: MLCTensor?) -> Self](/documentation/mlcompute/mlclosslayer/log(reductiontype:epsilon:weights:))
- [class func huberLoss(reductionType: MLCReductionType, delta: Float, weights: MLCTensor?) -> Self](/documentation/mlcompute/mlclosslayer/huberloss(reductiontype:delta:weights:))
- [class func meanAbsoluteError(reductionType: MLCReductionType, weights: MLCTensor?) -> Self](/documentation/mlcompute/mlclosslayer/meanabsoluteerror(reductiontype:weights:))
- [class func meanSquaredError(reductionType: MLCReductionType, weights: MLCTensor?) -> Self](/documentation/mlcompute/mlclosslayer/meansquarederror(reductiontype:weights:))
- [class func hingeLoss(reductionType: MLCReductionType, weights: MLCTensor?) -> Self](/documentation/mlcompute/mlclosslayer/hingeloss(reductiontype:weights:))
- [class func cosineDistance(reductionType: MLCReductionType, weights: MLCTensor?) -> Self](/documentation/mlcompute/mlclosslayer/cosinedistance(reductiontype:weights:))

#### Inspecting Loss Layers

- [var descriptor: MLCLossDescriptor](/documentation/mlcompute/mlclosslayer/descriptor)
- [var weights: MLCTensor?](/documentation/mlcompute/mlclosslayer/weights)
- [MLCYOLOLossLayer](/documentation/mlcompute/mlcyololosslayer)

#### Creating YOLO Loss Layers

- [convenience init(descriptor: MLCYOLOLossDescriptor)](/documentation/mlcompute/mlcyololosslayer/init(descriptor:))
- [MLCYOLOLossDescriptor](/documentation/mlcompute/mlcyololossdescriptor)

##### Creating YOLO Loss Descriptors

- [convenience init(anchorBoxes: Data, anchorBoxCount: Int)](/documentation/mlcompute/mlcyololossdescriptor/init(anchorboxes:anchorboxcount:))

##### Inspecting YOLO Loss Descriptors

- [var anchorBoxCount: Int](/documentation/mlcompute/mlcyololossdescriptor/anchorboxcount)
- [var anchorBoxes: Data](/documentation/mlcompute/mlcyololossdescriptor/anchorboxes)
- [var maximumIOUForObjectAbsence: Float](/documentation/mlcompute/mlcyololossdescriptor/maximumiouforobjectabsence)
- [var minimumIOUForObjectPresence: Float](/documentation/mlcompute/mlcyololossdescriptor/minimumiouforobjectpresence)
- [var scaleClassLoss: Float](/documentation/mlcompute/mlcyololossdescriptor/scaleclassloss)
- [var scaleObjectConfidenceLoss: Float](/documentation/mlcompute/mlcyololossdescriptor/scaleobjectconfidenceloss)
- [var scaleNoObjectConfidenceLoss: Float](/documentation/mlcompute/mlcyololossdescriptor/scalenoobjectconfidenceloss)
- [var scaleSpatialPositionLoss: Float](/documentation/mlcompute/mlcyololossdescriptor/scalespatialpositionloss)
- [var scaleSpatialSizeLoss: Float](/documentation/mlcompute/mlcyololossdescriptor/scalespatialsizeloss)
- [var shouldRescore: Bool](/documentation/mlcompute/mlcyololossdescriptor/shouldrescore)

#### Inspecting YOLO Loss Layers

- [var yoloLossDescriptor: MLCYOLOLossDescriptor](/documentation/mlcompute/mlcyololosslayer/yololossdescriptor)

### Base Layer

- [MLCLayer](/documentation/mlcompute/mlclayer)

#### Inspecting a Layer

- [var layerID: Int](/documentation/mlcompute/mlclayer/layerid)
- [var label: String](/documentation/mlcompute/mlclayer/label)
- [var isDebuggingEnabled: Bool](/documentation/mlcompute/mlclayer/isdebuggingenabled)
- [var deviceType: MLCDeviceType](/documentation/mlcompute/mlclayer/devicetype)
- [class func supportsDataType(MLCDataType, on: MLCDevice) -> Bool](/documentation/mlcompute/mlclayer/supportsdatatype(_:on:))

### Supporting Types

- [MLCPaddingPolicy](/documentation/mlcompute/mlcpaddingpolicy-3hic8)

#### Enumeration Cases

- [case same](/documentation/mlcompute/mlcpaddingpolicy-3hic8/same)
- [case valid](/documentation/mlcompute/mlcpaddingpolicy-3hic8/valid)
- [case sized(y: Int, x: Int)](/documentation/mlcompute/mlcpaddingpolicy-3hic8/sized(y:x:))
- [var debugDescription: String](/documentation/mlcompute/mlcpaddingpolicy-3hic8/debugdescription)
- [MLCPaddingType](/documentation/mlcompute/mlcpaddingtype)

#### Enumeration Cases

- [case zero](/documentation/mlcompute/mlcpaddingtype/zero)
- [case reflect](/documentation/mlcompute/mlcpaddingtype/reflect)
- [case symmetric](/documentation/mlcompute/mlcpaddingtype/symmetric)
- [case constant](/documentation/mlcompute/mlcpaddingtype/constant)
- [var debugDescription: String](/documentation/mlcompute/mlcpaddingtype/debugdescription)

#### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlcpaddingtype/init(rawvalue:))
- [Training and Validation](/documentation/mlcompute/training-and-validation)

### Devices

- [MLCDevice](/documentation/mlcompute/mlcdevice)

#### Creating Devices

- [convenience init?(type: MLCDeviceType)](/documentation/mlcompute/mlcdevice/init(type:))
- [convenience init?(type: MLCDeviceType, selectsMultipleComputeDevices: Bool)](/documentation/mlcompute/mlcdevice/init(type:selectsmultiplecomputedevices:))
- [MLCDeviceType](/documentation/mlcompute/mlcdevicetype)

##### Device Types

- [case any](/documentation/mlcompute/mlcdevicetype/any)
- [case cpu](/documentation/mlcompute/mlcdevicetype/cpu)
- [case gpu](/documentation/mlcompute/mlcdevicetype/gpu)
- [case ane](/documentation/mlcompute/mlcdevicetype/ane)

##### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlcdevicetype/init(rawvalue:))
- [convenience init?(gpuDevices: [any MTLDevice])](/documentation/mlcompute/mlcdevice/init(gpudevices:))
- [class func cpu() -> Self](/documentation/mlcompute/mlcdevice/cpu())
- [class func gpu() -> Self?](/documentation/mlcompute/mlcdevice/gpu())
- [class func ane() -> Self?](/documentation/mlcompute/mlcdevice/ane())

#### Inspecting Devices

- [var type: MLCDeviceType](/documentation/mlcompute/mlcdevice/type)
- [var actualDeviceType: MLCDeviceType](/documentation/mlcompute/mlcdevice/actualdevicetype)
- [var gpuDevices: [any MTLDevice]](/documentation/mlcompute/mlcdevice/gpudevices)

### Graphs

- [MLCGraph](/documentation/mlcompute/mlcgraph)

#### Adding Layers to Graphs

- [func node(with: MLCLayer, source: MLCTensor) -> MLCTensor?](/documentation/mlcompute/mlcgraph/node(with:source:))
- [func node(with: MLCLayer, sources: [MLCTensor]) -> MLCTensor?](/documentation/mlcompute/mlcgraph/node(with:sources:))
- [func node(with: MLCLayer, sources: [MLCTensor], disableUpdate: Bool) -> MLCTensor?](/documentation/mlcompute/mlcgraph/node(with:sources:disableupdate:))
- [func node(with: MLCLayer, sources: [MLCTensor], lossLabels: [MLCTensor]) -> MLCTensor?](/documentation/mlcompute/mlcgraph/node(with:sources:losslabels:))

#### Adding New Layers to Graphs

- [func split(source: MLCTensor, splitCount: Int, dimension: Int) -> [MLCTensor]?](/documentation/mlcompute/mlcgraph/split(source:splitcount:dimension:))
- [func split(source: MLCTensor, splitSectionLengths: [Int], dimension: Int) -> [MLCTensor]?](/documentation/mlcompute/mlcgraph/split(source:splitsectionlengths:dimension:))
- [func concatenate(sources: [MLCTensor], dimension: Int) -> MLCTensor?](/documentation/mlcompute/mlcgraph/concatenate(sources:dimension:))
- [func reshape(shape: [Int], source: MLCTensor) -> MLCTensor?](/documentation/mlcompute/mlcgraph/reshape(shape:source:))
- [func gather(withDimension: Int, source: MLCTensor, indices: MLCTensor) -> MLCTensor?](/documentation/mlcompute/mlcgraph/gather(withdimension:source:indices:))
- [func scatter(withDimension: Int, source: MLCTensor, indices: MLCTensor, copyFrom: MLCTensor, reductionType: MLCReductionType) -> MLCTensor?](/documentation/mlcompute/mlcgraph/scatter(withdimension:source:indices:copyfrom:reductiontype:))
- [func transpose(dimensions: [Int], source: MLCTensor) -> MLCTensor?](/documentation/mlcompute/mlcgraph/transpose(dimensions:source:))

#### Associating Data with Input Tensors

- [func bindAndWriteData([String : MLCTensorData], forInputs: [String : MLCTensor], to: MLCDevice, batchSize: Int, synchronous: Bool) -> Bool](/documentation/mlcompute/mlcgraph/bindandwritedata(_:forinputs:to:batchsize:synchronous:))
- [func bindAndWriteData([String : MLCTensorData], forInputs: [String : MLCTensor], to: MLCDevice, synchronous: Bool) -> Bool](/documentation/mlcompute/mlcgraph/bindandwritedata(_:forinputs:to:synchronous:))

#### Inspecting Graphs

- [func sourceTensors(for: MLCLayer) -> [MLCTensor]](/documentation/mlcompute/mlcgraph/sourcetensors(for:))
- [func resultTensors(for: MLCLayer) -> [MLCTensor]](/documentation/mlcompute/mlcgraph/resulttensors(for:))
- [var device: MLCDevice?](/documentation/mlcompute/mlcgraph/device)
- [var layers: [MLCLayer]](/documentation/mlcompute/mlcgraph/layers)
- [var summarizedDOTDescription: String](/documentation/mlcompute/mlcgraph/summarizeddotdescription)
- [MLCTrainingGraph](/documentation/mlcompute/mlctraininggraph)

#### Creating Training Graphs

- [convenience init(graphObjects: [MLCGraph], lossLayer: MLCLayer?, optimizer: MLCOptimizer?)](/documentation/mlcompute/mlctraininggraph/init(graphobjects:losslayer:optimizer:))
- [Optimizers](/documentation/mlcompute/optimizers)

##### Optimizer Types

- [MLCSGDOptimizer](/documentation/mlcompute/mlcsgdoptimizer)

###### Creating an SGD Optimizer

- [convenience init(descriptor: MLCOptimizerDescriptor)](/documentation/mlcompute/mlcsgdoptimizer/init(descriptor:))
- [convenience init(descriptor: MLCOptimizerDescriptor, momentumScale: Float, usesNesterovMomentum: Bool)](/documentation/mlcompute/mlcsgdoptimizer/init(descriptor:momentumscale:usesnesterovmomentum:))

###### Inspecting an SGD Optimizer

- [var momentumScale: Float](/documentation/mlcompute/mlcsgdoptimizer/momentumscale)
- [var usesNesterovMomentum: Bool](/documentation/mlcompute/mlcsgdoptimizer/usesnesterovmomentum)
- [MLCRMSPropOptimizer](/documentation/mlcompute/mlcrmspropoptimizer)

###### Creating an RMSProp Optimizer

- [convenience init(descriptor: MLCOptimizerDescriptor)](/documentation/mlcompute/mlcrmspropoptimizer/init(descriptor:))
- [convenience init(descriptor: MLCOptimizerDescriptor, momentumScale: Float, alpha: Float, epsilon: Float, isCentered: Bool)](/documentation/mlcompute/mlcrmspropoptimizer/init(descriptor:momentumscale:alpha:epsilon:iscentered:))

###### Inspecting an RMSProp Optimizer

- [var momentumScale: Float](/documentation/mlcompute/mlcrmspropoptimizer/momentumscale)
- [var alpha: Float](/documentation/mlcompute/mlcrmspropoptimizer/alpha)
- [var epsilon: Float](/documentation/mlcompute/mlcrmspropoptimizer/epsilon)
- [var isCentered: Bool](/documentation/mlcompute/mlcrmspropoptimizer/iscentered)
- [MLCAdamOptimizer](/documentation/mlcompute/mlcadamoptimizer)

###### Creating an Adam Optimizer

- [convenience init(descriptor: MLCOptimizerDescriptor)](/documentation/mlcompute/mlcadamoptimizer/init(descriptor:))
- [convenience init(descriptor: MLCOptimizerDescriptor, beta1: Float, beta2: Float, epsilon: Float, timeStep: Int)](/documentation/mlcompute/mlcadamoptimizer/init(descriptor:beta1:beta2:epsilon:timestep:))
- [convenience init(descriptor: MLCOptimizerDescriptor, beta1: Float, beta2: Float, epsilon: Float, usesAMSGrad: Bool, timeStep: Int)](/documentation/mlcompute/mlcadamoptimizer/init(descriptor:beta1:beta2:epsilon:usesamsgrad:timestep:))

###### Inspecting an Adam Optimizer

- [var beta1: Float](/documentation/mlcompute/mlcadamoptimizer/beta1)
- [var beta2: Float](/documentation/mlcompute/mlcadamoptimizer/beta2)
- [var epsilon: Float](/documentation/mlcompute/mlcadamoptimizer/epsilon)
- [var timeStep: Int](/documentation/mlcompute/mlcadamoptimizer/timestep)
- [var usesAMSGrad: Bool](/documentation/mlcompute/mlcadamoptimizer/usesamsgrad)
- [MLCAdamWOptimizer](/documentation/mlcompute/mlcadamwoptimizer)

###### Creating an AdamW Optimizer

- [convenience init(descriptor: MLCOptimizerDescriptor)](/documentation/mlcompute/mlcadamwoptimizer/init(descriptor:))
- [convenience init(descriptor: MLCOptimizerDescriptor, beta1: Float, beta2: Float, epsilon: Float, usesAMSGrad: Bool, timeStep: Int)](/documentation/mlcompute/mlcadamwoptimizer/init(descriptor:beta1:beta2:epsilon:usesamsgrad:timestep:))

###### Inspecting an AdamW Optimizer

- [var beta1: Float](/documentation/mlcompute/mlcadamwoptimizer/beta1)
- [var beta2: Float](/documentation/mlcompute/mlcadamwoptimizer/beta2)
- [var epsilon: Float](/documentation/mlcompute/mlcadamwoptimizer/epsilon)
- [var timeStep: Int](/documentation/mlcompute/mlcadamwoptimizer/timestep)
- [var usesAMSGrad: Bool](/documentation/mlcompute/mlcadamwoptimizer/usesamsgrad)
- [MLCOptimizer](/documentation/mlcompute/mlcoptimizer)

###### Inspecting an Optimizer

- [var learningRate: Float](/documentation/mlcompute/mlcoptimizer/learningrate)
- [var gradientRescale: Float](/documentation/mlcompute/mlcoptimizer/gradientrescale)
- [var appliesGradientClipping: Bool](/documentation/mlcompute/mlcoptimizer/appliesgradientclipping)
- [var gradientClipMax: Float](/documentation/mlcompute/mlcoptimizer/gradientclipmax)
- [var gradientClipMin: Float](/documentation/mlcompute/mlcoptimizer/gradientclipmin)
- [var regularizationScale: Float](/documentation/mlcompute/mlcoptimizer/regularizationscale)
- [var regularizationType: MLCRegularizationType](/documentation/mlcompute/mlcoptimizer/regularizationtype)
- [var gradientClippingType: MLCGradientClippingType](/documentation/mlcompute/mlcoptimizer/gradientclippingtype)
- [MLCGradientClippingType](/documentation/mlcompute/mlcgradientclippingtype)

###### Gradient Clipping Types

- [case byValue](/documentation/mlcompute/mlcgradientclippingtype/byvalue)
- [case byNorm](/documentation/mlcompute/mlcgradientclippingtype/bynorm)
- [case byGlobalNorm](/documentation/mlcompute/mlcgradientclippingtype/byglobalnorm)
- [var debugDescription: String](/documentation/mlcompute/mlcgradientclippingtype/debugdescription)

###### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlcgradientclippingtype/init(rawvalue:))
- [var maximumClippingNorm: Float](/documentation/mlcompute/mlcoptimizer/maximumclippingnorm)
- [var customGlobalNorm: Float](/documentation/mlcompute/mlcoptimizer/customglobalnorm)

##### Supporting Types

- [MLCOptimizerDescriptor](/documentation/mlcompute/mlcoptimizerdescriptor)

###### Creating an Optimizer Descriptor

- [convenience init(learningRate: Float, gradientRescale: Float, regularizationType: MLCRegularizationType, regularizationScale: Float)](/documentation/mlcompute/mlcoptimizerdescriptor/init(learningrate:gradientrescale:regularizationtype:regularizationscale:))
- [convenience init(learningRate: Float, gradientRescale: Float, appliesGradientClipping: Bool, gradientClipMax: Float, gradientClipMin: Float, regularizationType: MLCRegularizationType, regularizationScale: Float)](/documentation/mlcompute/mlcoptimizerdescriptor/init(learningrate:gradientrescale:appliesgradientclipping:gradientclipmax:gradientclipmin:regularizationtype:regularizationscale:))
- [convenience init(learningRate: Float, gradientRescale: Float, appliesGradientClipping: Bool, gradientClippingType: MLCGradientClippingType, gradientClipMax: Float, gradientClipMin: Float, maximumClippingNorm: Float, customGlobalNorm: Float, regularizationType: MLCRegularizationType, regularizationScale: Float)](/documentation/mlcompute/mlcoptimizerdescriptor/init(learningrate:gradientrescale:appliesgradientclipping:gradientclippingtype:gradientclipmax:gradientclipmin:maximumclippingnorm:customglobalnorm:regularizationtype:regularizationscale:))

###### Inspecting an Optimizer Descriptor

- [var learningRate: Float](/documentation/mlcompute/mlcoptimizerdescriptor/learningrate)
- [var gradientRescale: Float](/documentation/mlcompute/mlcoptimizerdescriptor/gradientrescale)
- [var appliesGradientClipping: Bool](/documentation/mlcompute/mlcoptimizerdescriptor/appliesgradientclipping)
- [var gradientClipMax: Float](/documentation/mlcompute/mlcoptimizerdescriptor/gradientclipmax)
- [var gradientClipMin: Float](/documentation/mlcompute/mlcoptimizerdescriptor/gradientclipmin)
- [var regularizationScale: Float](/documentation/mlcompute/mlcoptimizerdescriptor/regularizationscale)
- [var regularizationType: MLCRegularizationType](/documentation/mlcompute/mlcoptimizerdescriptor/regularizationtype)
- [var gradientClippingType: MLCGradientClippingType](/documentation/mlcompute/mlcoptimizerdescriptor/gradientclippingtype)
- [MLCGradientClippingType](/documentation/mlcompute/mlcgradientclippingtype)

###### Gradient Clipping Types

- [case byValue](/documentation/mlcompute/mlcgradientclippingtype/byvalue)
- [case byNorm](/documentation/mlcompute/mlcgradientclippingtype/bynorm)
- [case byGlobalNorm](/documentation/mlcompute/mlcgradientclippingtype/byglobalnorm)
- [var debugDescription: String](/documentation/mlcompute/mlcgradientclippingtype/debugdescription)

###### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlcgradientclippingtype/init(rawvalue:))
- [var maximumClippingNorm: Float](/documentation/mlcompute/mlcoptimizerdescriptor/maximumclippingnorm)
- [var customGlobalNorm: Float](/documentation/mlcompute/mlcoptimizerdescriptor/customglobalnorm)
- [MLCRegularizationType](/documentation/mlcompute/mlcregularizationtype)

###### Enumeration Cases

- [case none](/documentation/mlcompute/mlcregularizationtype/none)
- [case l1](/documentation/mlcompute/mlcregularizationtype/l1)
- [case l2](/documentation/mlcompute/mlcregularizationtype/l2)

###### Initializers

- [init?(rawValue: Int32)](/documentation/mlcompute/mlcregularizationtype/init(rawvalue:))
- [MLCTensorParameter](/documentation/mlcompute/mlctensorparameter)

##### Creating Tensor Parameters

- [convenience init(tensor: MLCTensor)](/documentation/mlcompute/mlctensorparameter/init(tensor:))
- [convenience init(tensor: MLCTensor, optimizerData: [MLCTensorData]?)](/documentation/mlcompute/mlctensorparameter/init(tensor:optimizerdata:))

##### Inspecting Tensor Parameters

- [var tensor: MLCTensor](/documentation/mlcompute/mlctensorparameter/tensor)
- [var isUpdatable: Bool](/documentation/mlcompute/mlctensorparameter/isupdatable)

#### Preparing Training Graphs

- [func addInputs([String : MLCTensor], lossLabels: [String : MLCTensor]?) -> Bool](/documentation/mlcompute/mlctraininggraph/addinputs(_:losslabels:))
- [func addInputs([String : MLCTensor], lossLabels: [String : MLCTensor]?, lossLabelWeights: [String : MLCTensor]?) -> Bool](/documentation/mlcompute/mlctraininggraph/addinputs(_:losslabels:losslabelweights:))
- [func addOutputs([String : MLCTensor]) -> Bool](/documentation/mlcompute/mlctraininggraph/addoutputs(_:))
- [func stopGradient(for: [MLCTensor]) -> Bool](/documentation/mlcompute/mlctraininggraph/stopgradient(for:))
- [func compileOptimizer(MLCOptimizer) -> Bool](/documentation/mlcompute/mlctraininggraph/compileoptimizer(_:))
- [func compile(options: MLCGraphCompilationOptions, device: MLCDevice) -> Bool](/documentation/mlcompute/mlctraininggraph/compile(options:device:))
- [func compile(options: MLCGraphCompilationOptions, device: MLCDevice, inputTensors: [String : MLCTensor]?, inputTensorsData: [String : MLCTensorData]?) -> Bool](/documentation/mlcompute/mlctraininggraph/compile(options:device:inputtensors:inputtensorsdata:))
- [func link(with: [MLCTrainingGraph]) -> Bool](/documentation/mlcompute/mlctraininggraph/link(with:))
- [func allocateUserGradient(for: MLCTensor) -> MLCTensor?](/documentation/mlcompute/mlctraininggraph/allocateusergradient(for:))
- [MLCGraphCompilationOptions](/documentation/mlcompute/mlcgraphcompilationoptions)

##### Creating Graph Compilation Options

- [init(rawValue: UInt64)](/documentation/mlcompute/mlcgraphcompilationoptions/init(rawvalue:))
- [static var debugLayers: MLCGraphCompilationOptions](/documentation/mlcompute/mlcgraphcompilationoptions/debuglayers)
- [static var disableLayerFusion: MLCGraphCompilationOptions](/documentation/mlcompute/mlcgraphcompilationoptions/disablelayerfusion)
- [static var linkGraphs: MLCGraphCompilationOptions](/documentation/mlcompute/mlcgraphcompilationoptions/linkgraphs)
- [static var computeAllGradients: MLCGraphCompilationOptions](/documentation/mlcompute/mlcgraphcompilationoptions/computeallgradients)

#### Executing Training Iterations

- [func execute(inputsData: [String : MLCTensorData], lossLabelsData: [String : MLCTensorData]?, lossLabelWeightsData: [String : MLCTensorData]?, batchSize: Int, options: MLCExecutionOptions, completionHandler: MLCGraphCompletionHandler?) -> Bool](/documentation/mlcompute/mlctraininggraph/execute(inputsdata:losslabelsdata:losslabelweightsdata:batchsize:options:completionhandler:))
- [func execute(inputsData: [String : MLCTensorData], lossLabelsData: [String : MLCTensorData]?, lossLabelWeightsData: [String : MLCTensorData]?, outputsData: [String : MLCTensorData]?, batchSize: Int, options: MLCExecutionOptions, completionHandler: MLCGraphCompletionHandler?) -> Bool](/documentation/mlcompute/mlctraininggraph/execute(inputsdata:losslabelsdata:losslabelweightsdata:outputsdata:batchsize:options:completionhandler:))
- [func synchronizeUpdates()](/documentation/mlcompute/mlctraininggraph/synchronizeupdates())
- [func setTrainingTensorParameters([MLCTensorParameter]) -> Bool](/documentation/mlcompute/mlctraininggraph/settrainingtensorparameters(_:))
- [MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions)

##### Execution Options

- [init(rawValue: UInt64)](/documentation/mlcompute/mlcexecutionoptions/init(rawvalue:))
- [static var skipWritingInputDataToDevice: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/skipwritinginputdatatodevice)
- [static var synchronous: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/synchronous)
- [static var profiling: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/profiling)
- [static var perLayerProfiling: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/perlayerprofiling)
- [static var forwardForInference: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/forwardforinference)
- [MLCGraphCompletionHandler](/documentation/mlcompute/mlcgraphcompletionhandler)

#### Executing Forward, Gradient, and Optimizer Updates

- [func executeForward(batchSize: Int, options: MLCExecutionOptions, completionHandler: MLCGraphCompletionHandler?) -> Bool](/documentation/mlcompute/mlctraininggraph/executeforward(batchsize:options:completionhandler:))
- [func executeForward(batchSize: Int, options: MLCExecutionOptions, outputsData: [String : MLCTensorData]?, completionHandler: MLCGraphCompletionHandler?) -> Bool](/documentation/mlcompute/mlctraininggraph/executeforward(batchsize:options:outputsdata:completionhandler:))
- [func executeForward(batchSize: Int, options: MLCExecutionOptions, outputsData: [String : MLCTensorData]?) async throws -> (result: MLCTensor?, executionTime: TimeInterval)](/documentation/mlcompute/mlctraininggraph/executeforward(batchsize:options:outputsdata:))
- [func executeGradient(batchSize: Int, options: MLCExecutionOptions, completionHandler: MLCGraphCompletionHandler?) -> Bool](/documentation/mlcompute/mlctraininggraph/executegradient(batchsize:options:completionhandler:))
- [func executeGradient(batchSize: Int, options: MLCExecutionOptions, outputsData: [String : MLCTensorData]?, completionHandler: MLCGraphCompletionHandler?) -> Bool](/documentation/mlcompute/mlctraininggraph/executegradient(batchsize:options:outputsdata:completionhandler:))
- [func executeGradient(batchSize: Int, options: MLCExecutionOptions, outputsData: [String : MLCTensorData]?) async throws -> TimeInterval](/documentation/mlcompute/mlctraininggraph/executegradient(batchsize:options:outputsdata:))
- [func executeOptimizerUpdate(options: MLCExecutionOptions, completionHandler: MLCGraphCompletionHandler?) -> Bool](/documentation/mlcompute/mlctraininggraph/executeoptimizerupdate(options:completionhandler:))
- [func executeOptimizerUpdate(options: MLCExecutionOptions) async throws -> TimeInterval](/documentation/mlcompute/mlctraininggraph/executeoptimizerupdate(options:))
- [func synchronizeUpdates()](/documentation/mlcompute/mlctraininggraph/synchronizeupdates())
- [func setTrainingTensorParameters([MLCTensorParameter]) -> Bool](/documentation/mlcompute/mlctraininggraph/settrainingtensorparameters(_:))
- [MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions)

##### Execution Options

- [init(rawValue: UInt64)](/documentation/mlcompute/mlcexecutionoptions/init(rawvalue:))
- [static var skipWritingInputDataToDevice: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/skipwritinginputdatatodevice)
- [static var synchronous: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/synchronous)
- [static var profiling: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/profiling)
- [static var perLayerProfiling: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/perlayerprofiling)
- [static var forwardForInference: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/forwardforinference)
- [MLCGraphCompletionHandler](/documentation/mlcompute/mlcgraphcompletionhandler)

#### Inspecting Training Graphs

- [func bindOptimizerData([MLCTensorData], deviceData: [MLCTensorOptimizerDeviceData]?, with: MLCTensor) -> Bool](/documentation/mlcompute/mlctraininggraph/bindoptimizerdata(_:devicedata:with:))
- [var optimizer: MLCOptimizer?](/documentation/mlcompute/mlctraininggraph/optimizer)
- [var deviceMemorySize: Int](/documentation/mlcompute/mlctraininggraph/devicememorysize)
- [func gradientTensor(forInput: MLCTensor) -> MLCTensor?](/documentation/mlcompute/mlctraininggraph/gradienttensor(forinput:))
- [func sourceGradientTensors(for: MLCLayer) -> [MLCTensor]](/documentation/mlcompute/mlctraininggraph/sourcegradienttensors(for:))
- [func resultGradientTensors(for: MLCLayer) -> [MLCTensor]](/documentation/mlcompute/mlctraininggraph/resultgradienttensors(for:))
- [func gradientData(forParameter: MLCTensor, layer: MLCLayer) -> Data?](/documentation/mlcompute/mlctraininggraph/gradientdata(forparameter:layer:))
- [MLCInferenceGraph](/documentation/mlcompute/mlcinferencegraph)

#### Creating Inference Graphs

- [convenience init(graphObjects: [MLCGraph])](/documentation/mlcompute/mlcinferencegraph/init(graphobjects:))

#### Preparing Inference Graphs

- [func addInputs([String : MLCTensor]) -> Bool](/documentation/mlcompute/mlcinferencegraph/addinputs(_:))
- [func addInputs([String : MLCTensor], lossLabels: [String : MLCTensor]?, lossLabelWeights: [String : MLCTensor]?) -> Bool](/documentation/mlcompute/mlcinferencegraph/addinputs(_:losslabels:losslabelweights:))
- [func addOutputs([String : MLCTensor]) -> Bool](/documentation/mlcompute/mlcinferencegraph/addoutputs(_:))
- [func compile(options: MLCGraphCompilationOptions, device: MLCDevice) -> Bool](/documentation/mlcompute/mlcinferencegraph/compile(options:device:))
- [func compile(options: MLCGraphCompilationOptions, device: MLCDevice, inputTensors: [String : MLCTensor]?, inputTensorsData: [String : MLCTensorData]?) -> Bool](/documentation/mlcompute/mlcinferencegraph/compile(options:device:inputtensors:inputtensorsdata:))
- [func link(with: [MLCInferenceGraph]) -> Bool](/documentation/mlcompute/mlcinferencegraph/link(with:))
- [MLCGraphCompilationOptions](/documentation/mlcompute/mlcgraphcompilationoptions)

##### Creating Graph Compilation Options

- [init(rawValue: UInt64)](/documentation/mlcompute/mlcgraphcompilationoptions/init(rawvalue:))
- [static var debugLayers: MLCGraphCompilationOptions](/documentation/mlcompute/mlcgraphcompilationoptions/debuglayers)
- [static var disableLayerFusion: MLCGraphCompilationOptions](/documentation/mlcompute/mlcgraphcompilationoptions/disablelayerfusion)
- [static var linkGraphs: MLCGraphCompilationOptions](/documentation/mlcompute/mlcgraphcompilationoptions/linkgraphs)
- [static var computeAllGradients: MLCGraphCompilationOptions](/documentation/mlcompute/mlcgraphcompilationoptions/computeallgradients)

#### Executing Inference Graphs

- [func execute(inputsData: [String : MLCTensorData], batchSize: Int, options: MLCExecutionOptions, completionHandler: MLCGraphCompletionHandler?) -> Bool](/documentation/mlcompute/mlcinferencegraph/execute(inputsdata:batchsize:options:completionhandler:))
- [func execute(inputsData: [String : MLCTensorData], outputsData: [String : MLCTensorData]?, batchSize: Int, options: MLCExecutionOptions, completionHandler: MLCGraphCompletionHandler?) -> Bool](/documentation/mlcompute/mlcinferencegraph/execute(inputsdata:outputsdata:batchsize:options:completionhandler:))
- [func execute(inputsData: [String : MLCTensorData], lossLabelsData: [String : MLCTensorData]?, lossLabelWeightsData: [String : MLCTensorData]?, batchSize: Int, options: MLCExecutionOptions, completionHandler: MLCGraphCompletionHandler?) -> Bool](/documentation/mlcompute/mlcinferencegraph/execute(inputsdata:losslabelsdata:losslabelweightsdata:batchsize:options:completionhandler:))
- [func execute(inputsData: [String : MLCTensorData], lossLabelsData: [String : MLCTensorData]?, lossLabelWeightsData: [String : MLCTensorData]?, outputsData: [String : MLCTensorData]?, batchSize: Int, options: MLCExecutionOptions, completionHandler: MLCGraphCompletionHandler?) -> Bool](/documentation/mlcompute/mlcinferencegraph/execute(inputsdata:losslabelsdata:losslabelweightsdata:outputsdata:batchsize:options:completionhandler:))
- [func execute(inputsData: [String : MLCTensorData], lossLabelsData: [String : MLCTensorData]?, lossLabelWeightsData: [String : MLCTensorData]?, outputsData: [String : MLCTensorData]?, batchSize: Int, options: MLCExecutionOptions) async throws -> (result: MLCTensor?, executionTime: TimeInterval)](/documentation/mlcompute/mlcinferencegraph/execute(inputsdata:losslabelsdata:losslabelweightsdata:outputsdata:batchsize:options:))
- [MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions)

##### Execution Options

- [init(rawValue: UInt64)](/documentation/mlcompute/mlcexecutionoptions/init(rawvalue:))
- [static var skipWritingInputDataToDevice: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/skipwritinginputdatatodevice)
- [static var synchronous: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/synchronous)
- [static var profiling: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/profiling)
- [static var perLayerProfiling: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/perlayerprofiling)
- [static var forwardForInference: MLCExecutionOptions](/documentation/mlcompute/mlcexecutionoptions/forwardforinference)
- [MLCGraphCompletionHandler](/documentation/mlcompute/mlcgraphcompletionhandler)

#### Inspecting Inference Graphs

- [var deviceMemorySize: Int](/documentation/mlcompute/mlcinferencegraph/devicememorysize)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
