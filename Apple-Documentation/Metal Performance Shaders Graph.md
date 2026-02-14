# Metal Performance Shaders Graph Documentation

Source: https://sosumi.ai/documentation/metalperformanceshadersgraph

---
title: Metal Performance Shaders Graph
source: https://developer.apple.com/documentation/metalperformanceshadersgraph
timestamp: 2026-02-13T18:59:38.884Z
---

## Essentials

- [Adding custom functions to a shader graph](/documentation/metalperformanceshadersgraph/adding-custom-functions-to-a-shader-graph)
- [Training a neural network using MPSGraph](/documentation/metalperformanceshadersgraph/training-a-neural-network-using-mps-graph)
- [Filtering images with MPSGraph FFT operations](/documentation/metalperformanceshadersgraph/filtering-images-with-mpsgraph-fft-operations)

## Classes

- [MPSGraph](/documentation/metalperformanceshadersgraph/mpsgraph)

### Initializers

- [init()](/documentation/metalperformanceshadersgraph/mpsgraph/init())

### Instance Properties

- [var options: MPSGraphOptions](/documentation/metalperformanceshadersgraph/mpsgraph/options)
- [var placeholderTensors: [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/placeholdertensors)

### Instance Methods

- [func GRU(MPSGraphTensor, recurrentWeight: MPSGraphTensor, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, descriptor: MPSGraphGRUDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/gru(_:recurrentweight:inputweight:bias:descriptor:name:))
- [func GRU(MPSGraphTensor, recurrentWeight: MPSGraphTensor, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, initState: MPSGraphTensor?, descriptor: MPSGraphGRUDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/gru(_:recurrentweight:inputweight:bias:initstate:descriptor:name:))
- [func GRU(MPSGraphTensor, recurrentWeight: MPSGraphTensor, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, initState: MPSGraphTensor?, mask: MPSGraphTensor?, secondaryBias: MPSGraphTensor?, descriptor: MPSGraphGRUDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/gru(_:recurrentweight:inputweight:bias:initstate:mask:secondarybias:descriptor:name:))
- [func GRUGradients(MPSGraphTensor, recurrentWeight: MPSGraphTensor, sourceGradient: MPSGraphTensor, zState: MPSGraphTensor, outputFwd: MPSGraphTensor, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, descriptor: MPSGraphGRUDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/grugradients(_:recurrentweight:sourcegradient:zstate:outputfwd:inputweight:bias:descriptor:name:))
- [func GRUGradients(MPSGraphTensor, recurrentWeight: MPSGraphTensor, sourceGradient: MPSGraphTensor, zState: MPSGraphTensor, outputFwd: MPSGraphTensor, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, initState: MPSGraphTensor?, descriptor: MPSGraphGRUDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/grugradients(_:recurrentweight:sourcegradient:zstate:outputfwd:inputweight:bias:initstate:descriptor:name:))
- [func GRUGradients(MPSGraphTensor, recurrentWeight: MPSGraphTensor, sourceGradient: MPSGraphTensor, zState: MPSGraphTensor, outputFwd: MPSGraphTensor, stateGradient: MPSGraphTensor?, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, initState: MPSGraphTensor?, mask: MPSGraphTensor?, secondaryBias: MPSGraphTensor?, descriptor: MPSGraphGRUDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/grugradients(_:recurrentweight:sourcegradient:zstate:outputfwd:stategradient:inputweight:bias:initstate:mask:secondarybias:descriptor:name:))
- [func HammingDistance(primary: MPSGraphTensor, secondary: MPSGraphTensor, resultDataType: MPSDataType, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/hammingdistance(primary:secondary:resultdatatype:name:))
- [func HermiteanToRealFFT(MPSGraphTensor, axes: [NSNumber], descriptor: MPSGraphFFTDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/hermiteantorealfft(_:axes:descriptor:name:))
- [func HermiteanToRealFFT(MPSGraphTensor, axesTensor: MPSGraphTensor, descriptor: MPSGraphFFTDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/hermiteantorealfft(_:axestensor:descriptor:name:))
- [func L2NormPooling4D(MPSGraphTensor, descriptor: MPSGraphPooling4DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/l2normpooling4d(_:descriptor:name:))
- [func L2NormPooling4DGradient(MPSGraphTensor, source: MPSGraphTensor, descriptor: MPSGraphPooling4DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/l2normpooling4dgradient(_:source:descriptor:name:))
- [func LSTM(MPSGraphTensor, recurrentWeight: MPSGraphTensor, initState: MPSGraphTensor?, initCell: MPSGraphTensor?, descriptor: MPSGraphLSTMDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/lstm(_:recurrentweight:initstate:initcell:descriptor:name:))
- [func LSTM(MPSGraphTensor, recurrentWeight: MPSGraphTensor, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, initState: MPSGraphTensor?, initCell: MPSGraphTensor?, descriptor: MPSGraphLSTMDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/lstm(_:recurrentweight:inputweight:bias:initstate:initcell:descriptor:name:))
- [func LSTM(MPSGraphTensor, recurrentWeight: MPSGraphTensor, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, initState: MPSGraphTensor?, initCell: MPSGraphTensor?, mask: MPSGraphTensor?, peephole: MPSGraphTensor?, descriptor: MPSGraphLSTMDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/lstm(_:recurrentweight:inputweight:bias:initstate:initcell:mask:peephole:descriptor:name:))
- [func LSTMGradients(MPSGraphTensor, recurrentWeight: MPSGraphTensor, sourceGradient: MPSGraphTensor, zState: MPSGraphTensor, cellOutputFwd: MPSGraphTensor, descriptor: MPSGraphLSTMDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/lstmgradients(_:recurrentweight:sourcegradient:zstate:celloutputfwd:descriptor:name:))
- [func LSTMGradients(MPSGraphTensor, recurrentWeight: MPSGraphTensor, sourceGradient: MPSGraphTensor, zState: MPSGraphTensor, cellOutputFwd: MPSGraphTensor, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, initState: MPSGraphTensor?, initCell: MPSGraphTensor?, descriptor: MPSGraphLSTMDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/lstmgradients(_:recurrentweight:sourcegradient:zstate:celloutputfwd:inputweight:bias:initstate:initcell:descriptor:name:))
- [func LSTMGradients(MPSGraphTensor, recurrentWeight: MPSGraphTensor, sourceGradient: MPSGraphTensor, zState: MPSGraphTensor, cellOutputFwd: MPSGraphTensor, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, initState: MPSGraphTensor?, initCell: MPSGraphTensor?, mask: MPSGraphTensor?, descriptor: MPSGraphLSTMDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/lstmgradients(_:recurrentweight:sourcegradient:zstate:celloutputfwd:inputweight:bias:initstate:initcell:mask:descriptor:name:))
- [func LSTMGradients(MPSGraphTensor, recurrentWeight: MPSGraphTensor, sourceGradient: MPSGraphTensor, zState: MPSGraphTensor, cellOutputFwd: MPSGraphTensor, stateGradient: MPSGraphTensor?, cellGradient: MPSGraphTensor?, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, initState: MPSGraphTensor?, initCell: MPSGraphTensor?, mask: MPSGraphTensor?, peephole: MPSGraphTensor?, descriptor: MPSGraphLSTMDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/lstmgradients(_:recurrentweight:sourcegradient:zstate:celloutputfwd:stategradient:cellgradient:inputweight:bias:initstate:initcell:mask:peephole:descriptor:name:))
- [func absolute(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/absolute(with:name:))
- [func absoluteSquare(tensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/absolutesquare(tensor:name:))
- [func acos(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/acos(with:name:))
- [func acosh(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/acosh(with:name:))
- [func adam(currentLearningRate: MPSGraphTensor, beta1: MPSGraphTensor, beta2: MPSGraphTensor, epsilon: MPSGraphTensor, values: MPSGraphTensor, momentum: MPSGraphTensor, velocity: MPSGraphTensor, maximumVelocity: MPSGraphTensor?, gradient: MPSGraphTensor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/adam(currentlearningrate:beta1:beta2:epsilon:values:momentum:velocity:maximumvelocity:gradient:name:))
- [func adam(learningRate: MPSGraphTensor, beta1: MPSGraphTensor, beta2: MPSGraphTensor, epsilon: MPSGraphTensor, beta1Power: MPSGraphTensor, beta2Power: MPSGraphTensor, values: MPSGraphTensor, momentum: MPSGraphTensor, velocity: MPSGraphTensor, maximumVelocity: MPSGraphTensor?, gradient: MPSGraphTensor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/adam(learningrate:beta1:beta2:epsilon:beta1power:beta2power:values:momentum:velocity:maximumvelocity:gradient:name:))
- [func addition(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/addition(_:_:name:))
- [func applyStochasticGradientDescent(learningRate: MPSGraphTensor, variable: MPSGraphVariableOp, gradient: MPSGraphTensor, name: String?) -> MPSGraphOperation](/documentation/metalperformanceshadersgraph/mpsgraph/applystochasticgradientdescent(learningrate:variable:gradient:name:))
- [func argSort(MPSGraphTensor, axis: Int, descending: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/argsort(_:axis:descending:name:))
- [func argSort(MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/argsort(_:axis:name:))
- [func argSort(MPSGraphTensor, axisTensor: MPSGraphTensor, descending: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/argsort(_:axistensor:descending:name:))
- [func argSort(MPSGraphTensor, axisTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/argsort(_:axistensor:name:))
- [func asin(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/asin(with:name:))
- [func asinh(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/asinh(with:name:))
- [func assign(MPSGraphTensor, tensor: MPSGraphTensor, name: String?) -> MPSGraphOperation](/documentation/metalperformanceshadersgraph/mpsgraph/assign(_:tensor:name:))
- [func atan(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/atan(with:name:))
- [func atan2(withPrimaryTensor: MPSGraphTensor, secondaryTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/atan2(withprimarytensor:secondarytensor:name:))
- [func atanh(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/atanh(with:name:))
- [func avgPooling2D(withSourceTensor: MPSGraphTensor, descriptor: MPSGraphPooling2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/avgpooling2d(withsourcetensor:descriptor:name:))
- [func avgPooling2DGradient(withGradientTensor: MPSGraphTensor, sourceTensor: MPSGraphTensor, descriptor: MPSGraphPooling2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/avgpooling2dgradient(withgradienttensor:sourcetensor:descriptor:name:))
- [func avgPooling4D(MPSGraphTensor, descriptor: MPSGraphPooling4DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/avgpooling4d(_:descriptor:name:))
- [func avgPooling4DGradient(MPSGraphTensor, source: MPSGraphTensor, descriptor: MPSGraphPooling4DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/avgpooling4dgradient(_:source:descriptor:name:))
- [func bandPart(MPSGraphTensor, numLower: Int, numUpper: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/bandpart(_:numlower:numupper:name:))
- [func bandPart(MPSGraphTensor, numLowerTensor: MPSGraphTensor, numUpperTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/bandpart(_:numlowertensor:numuppertensor:name:))
- [func batchToSpace(MPSGraphTensor, spatialAxes: [NSNumber], batchAxis: Int, blockDimensions: [NSNumber], usePixelShuffleOrder: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/batchtospace(_:spatialaxes:batchaxis:blockdimensions:usepixelshuffleorder:name:))
- [func batchToSpace(MPSGraphTensor, spatialAxesTensor: MPSGraphTensor, batchAxisTensor: MPSGraphTensor, blockDimensionsTensor: MPSGraphTensor, usePixelShuffleOrder: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/batchtospace(_:spatialaxestensor:batchaxistensor:blockdimensionstensor:usepixelshuffleorder:name:))
- [func bitwiseAND(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/bitwiseand(_:_:name:))
- [func bitwiseLeftShift(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/bitwiseleftshift(_:_:name:))
- [func bitwiseNOT(MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/bitwisenot(_:name:))
- [func bitwiseOR(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/bitwiseor(_:_:name:))
- [func bitwisePopulationCount(MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/bitwisepopulationcount(_:name:))
- [func bitwiseRightShift(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/bitwiserightshift(_:_:name:))
- [func bitwiseXOR(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/bitwisexor(_:_:name:))
- [func bottomK(MPSGraphTensor, axis: Int, k: Int, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/bottomk(_:axis:k:name:))
- [func bottomK(MPSGraphTensor, axisTensor: MPSGraphTensor, kTensor: MPSGraphTensor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/bottomk(_:axistensor:ktensor:name:))
- [func bottomKGradient(MPSGraphTensor, source: MPSGraphTensor, axis: Int, k: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/bottomkgradient(_:source:axis:k:name:))
- [func bottomKGradient(MPSGraphTensor, source: MPSGraphTensor, axisTensor: MPSGraphTensor, kTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/bottomkgradient(_:source:axistensor:ktensor:name:))
- [func broadcast(MPSGraphTensor, shape: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/broadcast(_:shape:name:))
- [func broadcast(MPSGraphTensor, shapeTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/broadcast(_:shapetensor:name:))
- [func call(symbolName: String, inputTensors: [MPSGraphTensor], outputTypes: [MPSGraphType], name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/call(symbolname:inputtensors:outputtypes:name:))
- [func cast(MPSGraphTensor, to: MPSDataType, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cast(_:to:name:))
- [func ceil(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/ceil(with:name:))
- [func clamp(MPSGraphTensor, min: MPSGraphTensor, max: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/clamp(_:min:max:name:))
- [func colToIm(MPSGraphTensor, outputShape: [NSNumber], descriptor: MPSGraphImToColOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/coltoim(_:outputshape:descriptor:name:))
- [func compile(with: MPSGraphDevice?, feeds: [MPSGraphTensor : MPSGraphShapedType], targetTensors: [MPSGraphTensor], targetOperations: [MPSGraphOperation]?, compilationDescriptor: MPSGraphCompilationDescriptor?) -> MPSGraphExecutable](/documentation/metalperformanceshadersgraph/mpsgraph/compile(with:feeds:targettensors:targetoperations:compilationdescriptor:))
- [func complexConstant(realPart: Double, imaginaryPart: Double) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/complexconstant(realpart:imaginarypart:))
- [func complexConstant(realPart: Double, imaginaryPart: Double, dataType: MPSDataType) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/complexconstant(realpart:imaginarypart:datatype:))
- [func complexConstant(realPart: Double, imaginaryPart: Double, shape: [NSNumber], dataType: MPSDataType) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/complexconstant(realpart:imaginarypart:shape:datatype:))
- [func complexTensor(realTensor: MPSGraphTensor, imaginaryTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/complextensor(realtensor:imaginarytensor:name:))
- [func concatTensor(MPSGraphTensor, with: MPSGraphTensor, dimension: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/concattensor(_:with:dimension:name:))
- [func concatTensors([MPSGraphTensor], dimension: Int, interleave: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/concattensors(_:dimension:interleave:name:))
- [func concatTensors([MPSGraphTensor], dimension: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/concattensors(_:dimension:name:))
- [func conjugate(tensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/conjugate(tensor:name:))
- [func constant(Double, dataType: MPSDataType) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/constant(_:datatype:))
- [func constant(Double, shape: [NSNumber], dataType: MPSDataType) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/constant(_:shape:datatype:)-3wa0e)
- [func constant(Data, shape: [NSNumber], dataType: MPSDataType) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/constant(_:shape:datatype:)-ylr4)
- [func controlDependency(with: [MPSGraphOperation], dependentBlock: MPSGraphControlFlowDependencyBlock, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/controldependency(with:dependentblock:name:))
- [func convolution2D(MPSGraphTensor, weights: MPSGraphTensor, descriptor: MPSGraphConvolution2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolution2d(_:weights:descriptor:name:))
- [func convolution2DDataGradient(MPSGraphTensor, weights: MPSGraphTensor, outputShape: [NSNumber], forwardConvolutionDescriptor: MPSGraphConvolution2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolution2ddatagradient(_:weights:outputshape:forwardconvolutiondescriptor:name:))
- [func convolution2DDataGradient(MPSGraphTensor, weights: MPSGraphTensor, outputShapeTensor: MPSGraphTensor, forwardConvolutionDescriptor: MPSGraphConvolution2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolution2ddatagradient(_:weights:outputshapetensor:forwardconvolutiondescriptor:name:))
- [func convolution2DWeightsGradient(MPSGraphTensor, source: MPSGraphTensor, outputShape: [NSNumber], forwardConvolutionDescriptor: MPSGraphConvolution2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolution2dweightsgradient(_:source:outputshape:forwardconvolutiondescriptor:name:))
- [func convolution2DWeightsGradient(MPSGraphTensor, source: MPSGraphTensor, outputShapeTensor: MPSGraphTensor, forwardConvolutionDescriptor: MPSGraphConvolution2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolution2dweightsgradient(_:source:outputshapetensor:forwardconvolutiondescriptor:name:))
- [func convolution3D(MPSGraphTensor, weights: MPSGraphTensor, descriptor: MPSGraphConvolution3DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolution3d(_:weights:descriptor:name:))
- [func convolution3DDataGradient(MPSGraphTensor, weights: MPSGraphTensor, outputShape: [NSNumber], forwardConvolutionDescriptor: MPSGraphConvolution3DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolution3ddatagradient(_:weights:outputshape:forwardconvolutiondescriptor:name:))
- [func convolution3DDataGradient(MPSGraphTensor, weights: MPSGraphTensor, outputShapeTensor: MPSGraphTensor, forwardConvolutionDescriptor: MPSGraphConvolution3DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolution3ddatagradient(_:weights:outputshapetensor:forwardconvolutiondescriptor:name:))
- [func convolution3DWeightsGradient(MPSGraphTensor, source: MPSGraphTensor, outputShape: [NSNumber], forwardConvolutionDescriptor: MPSGraphConvolution3DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolution3dweightsgradient(_:source:outputshape:forwardconvolutiondescriptor:name:))
- [func convolution3DWeightsGradient(MPSGraphTensor, source: MPSGraphTensor, outputShapeTensor: MPSGraphTensor, forwardConvolutionDescriptor: MPSGraphConvolution3DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolution3dweightsgradient(_:source:outputshapetensor:forwardconvolutiondescriptor:name:))
- [func convolutionTranspose2D(MPSGraphTensor, weights: MPSGraphTensor, outputShape: [NSNumber], descriptor: MPSGraphConvolution2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolutiontranspose2d(_:weights:outputshape:descriptor:name:))
- [func convolutionTranspose2D(MPSGraphTensor, weights: MPSGraphTensor, outputShapeTensor: MPSGraphTensor, descriptor: MPSGraphConvolution2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolutiontranspose2d(_:weights:outputshapetensor:descriptor:name:))
- [func convolutionTranspose2DDataGradient(MPSGraphTensor, weights: MPSGraphTensor, outputShape: [NSNumber], forwardConvolutionDescriptor: MPSGraphConvolution2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolutiontranspose2ddatagradient(_:weights:outputshape:forwardconvolutiondescriptor:name:))
- [func convolutionTranspose2DDataGradient(MPSGraphTensor, weights: MPSGraphTensor, outputShapeTensor: MPSGraphTensor, forwardConvolutionDescriptor: MPSGraphConvolution2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolutiontranspose2ddatagradient(_:weights:outputshapetensor:forwardconvolutiondescriptor:name:))
- [func convolutionTranspose2DWeightsGradient(MPSGraphTensor, weights: MPSGraphTensor, outputShape: [NSNumber], forwardConvolutionDescriptor: MPSGraphConvolution2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolutiontranspose2dweightsgradient(_:weights:outputshape:forwardconvolutiondescriptor:name:))
- [func convolutionTranspose2DWeightsGradient(MPSGraphTensor, weights: MPSGraphTensor, outputShapeTensor: MPSGraphTensor, forwardConvolutionDescriptor: MPSGraphConvolution2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/convolutiontranspose2dweightsgradient(_:weights:outputshapetensor:forwardconvolutiondescriptor:name:))
- [func coordinate(alongAxis: Int, withShape: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/coordinate(alongaxis:withshape:name:))
- [func coordinate(alongAxis: Int, withShapeTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/coordinate(alongaxis:withshapetensor:name:))
- [func coordinate(alongAxisTensor: MPSGraphTensor, withShape: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/coordinate(alongaxistensor:withshape:name:))
- [func coordinate(alongAxisTensor: MPSGraphTensor, withShapeTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/coordinate(alongaxistensor:withshapetensor:name:))
- [func cos(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cos(with:name:))
- [func cosh(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cosh(with:name:))
- [func cumulativeMaximum(MPSGraphTensor, axis: Int, exclusive: Bool, reverse: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativemaximum(_:axis:exclusive:reverse:name:))
- [func cumulativeMaximum(MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativemaximum(_:axis:name:))
- [func cumulativeMaximum(MPSGraphTensor, axisTensor: MPSGraphTensor, exclusive: Bool, reverse: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativemaximum(_:axistensor:exclusive:reverse:name:))
- [func cumulativeMaximum(MPSGraphTensor, axisTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativemaximum(_:axistensor:name:))
- [func cumulativeMinimum(MPSGraphTensor, axis: Int, exclusive: Bool, reverse: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativeminimum(_:axis:exclusive:reverse:name:))
- [func cumulativeMinimum(MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativeminimum(_:axis:name:))
- [func cumulativeMinimum(MPSGraphTensor, axisTensor: MPSGraphTensor, exclusive: Bool, reverse: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativeminimum(_:axistensor:exclusive:reverse:name:))
- [func cumulativeMinimum(MPSGraphTensor, axisTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativeminimum(_:axistensor:name:))
- [func cumulativeProduct(MPSGraphTensor, axis: Int, exclusive: Bool, reverse: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativeproduct(_:axis:exclusive:reverse:name:))
- [func cumulativeProduct(MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativeproduct(_:axis:name:))
- [func cumulativeProduct(MPSGraphTensor, axisTensor: MPSGraphTensor, exclusive: Bool, reverse: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativeproduct(_:axistensor:exclusive:reverse:name:))
- [func cumulativeProduct(MPSGraphTensor, axisTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativeproduct(_:axistensor:name:))
- [func cumulativeSum(MPSGraphTensor, axis: Int, exclusive: Bool, reverse: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativesum(_:axis:exclusive:reverse:name:))
- [func cumulativeSum(MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativesum(_:axis:name:))
- [func cumulativeSum(MPSGraphTensor, axisTensor: MPSGraphTensor, exclusive: Bool, reverse: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativesum(_:axistensor:exclusive:reverse:name:))
- [func cumulativeSum(MPSGraphTensor, axisTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/cumulativesum(_:axistensor:name:))
- [func depth(toSpace2DTensor: MPSGraphTensor, widthAxis: Int, heightAxis: Int, depthAxis: Int, blockSize: Int, usePixelShuffleOrder: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/depth(tospace2dtensor:widthaxis:heightaxis:depthaxis:blocksize:usepixelshuffleorder:name:))
- [func depth(toSpace2DTensor: MPSGraphTensor, widthAxisTensor: MPSGraphTensor, heightAxisTensor: MPSGraphTensor, depthAxisTensor: MPSGraphTensor, blockSize: Int, usePixelShuffleOrder: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/depth(tospace2dtensor:widthaxistensor:heightaxistensor:depthaxistensor:blocksize:usepixelshuffleorder:name:))
- [func depthwiseConvolution2D(MPSGraphTensor, weights: MPSGraphTensor, descriptor: MPSGraphDepthwiseConvolution2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/depthwiseconvolution2d(_:weights:descriptor:name:))
- [func depthwiseConvolution2DDataGradient(MPSGraphTensor, weights: MPSGraphTensor, outputShape: [NSNumber], descriptor: MPSGraphDepthwiseConvolution2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/depthwiseconvolution2ddatagradient(_:weights:outputshape:descriptor:name:))
- [func depthwiseConvolution2DWeightsGradient(MPSGraphTensor, source: MPSGraphTensor, outputShape: [NSNumber], descriptor: MPSGraphDepthwiseConvolution2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/depthwiseconvolution2dweightsgradient(_:source:outputshape:descriptor:name:))
- [func depthwiseConvolution3D(MPSGraphTensor, weights: MPSGraphTensor, descriptor: MPSGraphDepthwiseConvolution3DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/depthwiseconvolution3d(_:weights:descriptor:name:))
- [func depthwiseConvolution3DDataGradient(MPSGraphTensor, weights: MPSGraphTensor, outputShape: [NSNumber]?, descriptor: MPSGraphDepthwiseConvolution3DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/depthwiseconvolution3ddatagradient(_:weights:outputshape:descriptor:name:))
- [func depthwiseConvolution3DWeightsGradient(MPSGraphTensor, source: MPSGraphTensor, outputShape: [NSNumber], descriptor: MPSGraphDepthwiseConvolution3DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/depthwiseconvolution3dweightsgradient(_:source:outputshape:descriptor:name:))
- [func dequantize(MPSGraphTensor, LUTTensor: MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/dequantize(_:luttensor:axis:name:))
- [func dequantize(MPSGraphTensor, LUTTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/dequantize(_:luttensor:name:))
- [func dequantize(MPSGraphTensor, scale: Double, zeroPoint: Double, dataType: MPSDataType, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/dequantize(_:scale:zeropoint:datatype:name:))
- [func dequantize(MPSGraphTensor, scaleTensor: MPSGraphTensor, dataType: MPSDataType, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/dequantize(_:scaletensor:datatype:name:))
- [func dequantize(MPSGraphTensor, scaleTensor: MPSGraphTensor, zeroPoint: Double, dataType: MPSDataType, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/dequantize(_:scaletensor:zeropoint:datatype:axis:name:))
- [func dequantize(MPSGraphTensor, scaleTensor: MPSGraphTensor, zeroPointTensor: MPSGraphTensor, dataType: MPSDataType, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/dequantize(_:scaletensor:zeropointtensor:datatype:axis:name:))
- [func dequantize(MPSGraphTensor, scaleTensor: MPSGraphTensor, zeroPointTensor: MPSGraphTensor, dataType: MPSDataType, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/dequantize(_:scaletensor:zeropointtensor:datatype:name:))
- [func division(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/division(_:_:name:))
- [func divisionNoNaN(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/divisionnonan(_:_:name:))
- [func dropout(MPSGraphTensor, rate: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/dropout(_:rate:name:)-16cq4)
- [func dropout(MPSGraphTensor, rate: Double, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/dropout(_:rate:name:)-6hvf3)
- [func encode(to: MPSCommandBuffer, feeds: [MPSGraphTensor : MPSGraphTensorData], targetOperations: [MPSGraphOperation]?, resultsDictionary: [MPSGraphTensor : MPSGraphTensorData], executionDescriptor: MPSGraphExecutionDescriptor?)](/documentation/metalperformanceshadersgraph/mpsgraph/encode(to:feeds:targetoperations:resultsdictionary:executiondescriptor:))
- [func encode(to: MPSCommandBuffer, feeds: [MPSGraphTensor : MPSGraphTensorData], targetTensors: [MPSGraphTensor], targetOperations: [MPSGraphOperation]?, executionDescriptor: MPSGraphExecutionDescriptor?) -> [MPSGraphTensor : MPSGraphTensorData]](/documentation/metalperformanceshadersgraph/mpsgraph/encode(to:feeds:targettensors:targetoperations:executiondescriptor:))
- [func equal(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/equal(_:_:name:))
- [func erf(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/erf(with:name:))
- [func expandDims(MPSGraphTensor, axes: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/expanddims(_:axes:name:))
- [func expandDims(MPSGraphTensor, axesTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/expanddims(_:axestensor:name:))
- [func expandDims(MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/expanddims(_:axis:name:))
- [func exponent(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/exponent(with:name:))
- [func exponentBase10(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/exponentbase10(with:name:))
- [func exponentBase2(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/exponentbase2(with:name:))
- [func fastFourierTransform(MPSGraphTensor, axes: [NSNumber], descriptor: MPSGraphFFTDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/fastfouriertransform(_:axes:descriptor:name:))
- [func fastFourierTransform(MPSGraphTensor, axesTensor: MPSGraphTensor, descriptor: MPSGraphFFTDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/fastfouriertransform(_:axestensor:descriptor:name:))
- [func flatten2D(MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/flatten2d(_:axis:name:))
- [func flatten2D(MPSGraphTensor, axisTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/flatten2d(_:axistensor:name:))
- [func floor(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/floor(with:name:))
- [func floorModulo(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/floormodulo(_:_:name:))
- [func `for`(lowerBound: MPSGraphTensor, upperBound: MPSGraphTensor, step: MPSGraphTensor, initialBodyArguments: [MPSGraphTensor], body: MPSGraphForLoopBodyBlock, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/for(lowerbound:upperbound:step:initialbodyarguments:body:name:))
- [func `for`(numberOfIterations: MPSGraphTensor, initialBodyArguments: [MPSGraphTensor], body: MPSGraphForLoopBodyBlock, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/for(numberofiterations:initialbodyarguments:body:name:))
- [func gather(withUpdatesTensor: MPSGraphTensor, indicesTensor: MPSGraphTensor, axis: Int, batchDimensions: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/gather(withupdatestensor:indicestensor:axis:batchdimensions:name:))
- [func gatherAlongAxis(Int, updates: MPSGraphTensor, indices: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/gatheralongaxis(_:updates:indices:name:))
- [func gatherAlongAxisTensor(MPSGraphTensor, updates: MPSGraphTensor, indices: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/gatheralongaxistensor(_:updates:indices:name:))
- [func gatherND(withUpdatesTensor: MPSGraphTensor, indicesTensor: MPSGraphTensor, batchDimensions: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/gathernd(withupdatestensor:indicestensor:batchdimensions:name:))
- [func gradients(of: MPSGraphTensor, with: [MPSGraphTensor], name: String?) -> [MPSGraphTensor : MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/gradients(of:with:name:))
- [func greaterThan(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/greaterthan(_:_:name:))
- [func greaterThanOrEqualTo(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/greaterthanorequalto(_:_:name:))
- [func identity(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/identity(with:name:))
- [func `if`(MPSGraphTensor, then: MPSGraphIfThenElseBlock, else: MPSGraphIfThenElseBlock?, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/if(_:then:else:name:))
- [func imToCol(MPSGraphTensor, descriptor: MPSGraphImToColOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/imtocol(_:descriptor:name:))
- [func imaginaryPartOfTensor(tensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/imaginarypartoftensor(tensor:name:))
- [func inverse(input: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/inverse(input:name:))
- [func isFinite(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/isfinite(with:name:))
- [func isInfinite(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/isinfinite(with:name:))
- [func isNaN(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/isnan(with:name:))
- [func leakyReLU(with: MPSGraphTensor, alpha: Double, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/leakyrelu(with:alpha:name:))
- [func leakyReLU(with: MPSGraphTensor, alphaTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/leakyrelu(with:alphatensor:name:))
- [func leakyReLUGradient(withIncomingGradient: MPSGraphTensor, sourceTensor: MPSGraphTensor, alphaTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/leakyrelugradient(withincominggradient:sourcetensor:alphatensor:name:))
- [func lessThan(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/lessthan(_:_:name:))
- [func lessThanOrEqualTo(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/lessthanorequalto(_:_:name:))
- [func logarithm(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/logarithm(with:name:))
- [func logarithmBase10(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/logarithmbase10(with:name:))
- [func logarithmBase2(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/logarithmbase2(with:name:))
- [func logicalAND(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/logicaland(_:_:name:))
- [func logicalNAND(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/logicalnand(_:_:name:))
- [func logicalNOR(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/logicalnor(_:_:name:))
- [func logicalOR(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/logicalor(_:_:name:))
- [func logicalXNOR(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/logicalxnor(_:_:name:))
- [func logicalXOR(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/logicalxor(_:_:name:))
- [func matrixMultiplication(primary: MPSGraphTensor, secondary: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/matrixmultiplication(primary:secondary:name:))
- [func maxPooling2D(withSourceTensor: MPSGraphTensor, descriptor: MPSGraphPooling2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/maxpooling2d(withsourcetensor:descriptor:name:))
- [func maxPooling2DGradient(withGradientTensor: MPSGraphTensor, indicesTensor: MPSGraphTensor, outputShape: [NSNumber], descriptor: MPSGraphPooling2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/maxpooling2dgradient(withgradienttensor:indicestensor:outputshape:descriptor:name:))
- [func maxPooling2DGradient(withGradientTensor: MPSGraphTensor, indicesTensor: MPSGraphTensor, outputShapeTensor: MPSGraphTensor, descriptor: MPSGraphPooling2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/maxpooling2dgradient(withgradienttensor:indicestensor:outputshapetensor:descriptor:name:))
- [func maxPooling2DGradient(withGradientTensor: MPSGraphTensor, sourceTensor: MPSGraphTensor, descriptor: MPSGraphPooling2DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/maxpooling2dgradient(withgradienttensor:sourcetensor:descriptor:name:))
- [func maxPooling2DReturnIndices(MPSGraphTensor, descriptor: MPSGraphPooling2DOpDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/maxpooling2dreturnindices(_:descriptor:name:))
- [func maxPooling4D(MPSGraphTensor, descriptor: MPSGraphPooling4DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/maxpooling4d(_:descriptor:name:))
- [func maxPooling4DGradient(MPSGraphTensor, source: MPSGraphTensor, descriptor: MPSGraphPooling4DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/maxpooling4dgradient(_:source:descriptor:name:))
- [func maxPooling4DGradient(withGradientTensor: MPSGraphTensor, indicesTensor: MPSGraphTensor, outputShape: [NSNumber], descriptor: MPSGraphPooling4DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/maxpooling4dgradient(withgradienttensor:indicestensor:outputshape:descriptor:name:))
- [func maxPooling4DGradient(withGradientTensor: MPSGraphTensor, indicesTensor: MPSGraphTensor, outputShapeTensor: MPSGraphTensor, descriptor: MPSGraphPooling4DOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/maxpooling4dgradient(withgradienttensor:indicestensor:outputshapetensor:descriptor:name:))
- [func maxPooling4DReturnIndices(MPSGraphTensor, descriptor: MPSGraphPooling4DOpDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/maxpooling4dreturnindices(_:descriptor:name:))
- [func maximum(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/maximum(_:_:name:))
- [func maximumWithNaNPropagation(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/maximumwithnanpropagation(_:_:name:))
- [func mean(of: MPSGraphTensor, axes: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/mean(of:axes:name:))
- [func minimum(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/minimum(_:_:name:))
- [func minimumWithNaNPropagation(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/minimumwithnanpropagation(_:_:name:))
- [func modulo(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/modulo(_:_:name:))
- [func multiplication(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/multiplication(_:_:name:))
- [func negative(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/negative(with:name:))
- [func nonMaximumSuppression(withBoxesTensor: MPSGraphTensor, scoresTensor: MPSGraphTensor, classIndicesTensor: MPSGraphTensor, iouThreshold: Float, scoreThreshold: Float, perClassSuppression: Bool, coordinateMode: MPSGraphNonMaximumSuppressionCoordinateMode, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/nonmaximumsuppression(withboxestensor:scorestensor:classindicestensor:iouthreshold:scorethreshold:perclasssuppression:coordinatemode:name:))
- [func nonMaximumSuppression(withBoxesTensor: MPSGraphTensor, scoresTensor: MPSGraphTensor, iouThreshold: Float, scoreThreshold: Float, perClassSuppression: Bool, coordinateMode: MPSGraphNonMaximumSuppressionCoordinateMode, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/nonmaximumsuppression(withboxestensor:scorestensor:iouthreshold:scorethreshold:perclasssuppression:coordinatemode:name:))
- [func nonZeroIndices(MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/nonzeroindices(_:name:))
- [func normalizationBetaGradient(withIncomingGradientTensor: MPSGraphTensor, sourceTensor: MPSGraphTensor, reductionAxes: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/normalizationbetagradient(withincominggradienttensor:sourcetensor:reductionaxes:name:))
- [func normalizationGammaGradient(withIncomingGradientTensor: MPSGraphTensor, sourceTensor: MPSGraphTensor, mean: MPSGraphTensor, varianceTensor: MPSGraphTensor, reductionAxes: [NSNumber], epsilon: Float, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/normalizationgammagradient(withincominggradienttensor:sourcetensor:mean:variancetensor:reductionaxes:epsilon:name:))
- [func normalizationGradient(withIncomingGradientTensor: MPSGraphTensor, sourceTensor: MPSGraphTensor, mean: MPSGraphTensor, varianceTensor: MPSGraphTensor, gammaTensor: MPSGraphTensor?, gammaGradientTensor: MPSGraphTensor?, betaGradientTensor: MPSGraphTensor?, reductionAxes: [NSNumber], epsilon: Float, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/normalizationgradient(withincominggradienttensor:sourcetensor:mean:variancetensor:gammatensor:gammagradienttensor:betagradienttensor:reductionaxes:epsilon:name:))
- [func normalize(MPSGraphTensor, mean: MPSGraphTensor, variance: MPSGraphTensor, gamma: MPSGraphTensor?, beta: MPSGraphTensor?, epsilon: Float, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/normalize(_:mean:variance:gamma:beta:epsilon:name:))
- [func not(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/not(with:name:))
- [func notEqual(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/notequal(_:_:name:))
- [func oneHot(withIndicesTensor: MPSGraphTensor, depth: Int, axis: Int, dataType: MPSDataType, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/onehot(withindicestensor:depth:axis:datatype:name:))
- [func oneHot(withIndicesTensor: MPSGraphTensor, depth: Int, axis: Int, dataType: MPSDataType, onValue: Double, offValue: Double, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/onehot(withindicestensor:depth:axis:datatype:onvalue:offvalue:name:))
- [func oneHot(withIndicesTensor: MPSGraphTensor, depth: Int, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/onehot(withindicestensor:depth:axis:name:))
- [func oneHot(withIndicesTensor: MPSGraphTensor, depth: Int, dataType: MPSDataType, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/onehot(withindicestensor:depth:datatype:name:))
- [func oneHot(withIndicesTensor: MPSGraphTensor, depth: Int, dataType: MPSDataType, onValue: Double, offValue: Double, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/onehot(withindicestensor:depth:datatype:onvalue:offvalue:name:))
- [func oneHot(withIndicesTensor: MPSGraphTensor, depth: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/onehot(withindicestensor:depth:name:))
- [func padGradient(withIncomingGradientTensor: MPSGraphTensor, sourceTensor: MPSGraphTensor, paddingMode: MPSGraphPaddingMode, leftPadding: [NSNumber], rightPadding: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/padgradient(withincominggradienttensor:sourcetensor:paddingmode:leftpadding:rightpadding:name:))
- [func padTensor(MPSGraphTensor, with: MPSGraphPaddingMode, leftPadding: [NSNumber], rightPadding: [NSNumber], constantValue: Double, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/padtensor(_:with:leftpadding:rightpadding:constantvalue:name:))
- [func placeholder(shape: [NSNumber]?, dataType: MPSDataType, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/placeholder(shape:datatype:name:))
- [func placeholder(shape: [NSNumber]?, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/placeholder(shape:name:))
- [func power(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/power(_:_:name:))
- [func quantize(MPSGraphTensor, scale: Double, zeroPoint: Double, dataType: MPSDataType, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/quantize(_:scale:zeropoint:datatype:name:))
- [func quantize(MPSGraphTensor, scaleTensor: MPSGraphTensor, zeroPoint: Double, dataType: MPSDataType, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/quantize(_:scaletensor:zeropoint:datatype:axis:name:))
- [func quantize(MPSGraphTensor, scaleTensor: MPSGraphTensor, zeroPointTensor: MPSGraphTensor, dataType: MPSDataType, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/quantize(_:scaletensor:zeropointtensor:datatype:axis:name:))
- [func randomPhiloxStateTensor(withCounterLow: Int, counterHigh: Int, key: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/randomphiloxstatetensor(withcounterlow:counterhigh:key:name:))
- [func randomPhiloxStateTensor(withSeed: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/randomphiloxstatetensor(withseed:name:))
- [func randomTensor(withShape: [NSNumber], descriptor: MPSGraphRandomOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/randomtensor(withshape:descriptor:name:))
- [func randomTensor(withShape: [NSNumber], descriptor: MPSGraphRandomOpDescriptor, seed: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/randomtensor(withshape:descriptor:seed:name:))
- [func randomTensor(withShape: [NSNumber], descriptor: MPSGraphRandomOpDescriptor, stateTensor: MPSGraphTensor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/randomtensor(withshape:descriptor:statetensor:name:))
- [func randomTensor(withShapeTensor: MPSGraphTensor, descriptor: MPSGraphRandomOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/randomtensor(withshapetensor:descriptor:name:))
- [func randomTensor(withShapeTensor: MPSGraphTensor, descriptor: MPSGraphRandomOpDescriptor, seed: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/randomtensor(withshapetensor:descriptor:seed:name:))
- [func randomTensor(withShapeTensor: MPSGraphTensor, descriptor: MPSGraphRandomOpDescriptor, stateTensor: MPSGraphTensor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/randomtensor(withshapetensor:descriptor:statetensor:name:))
- [func randomUniformTensor(withShape: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/randomuniformtensor(withshape:name:))
- [func randomUniformTensor(withShape: [NSNumber], seed: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/randomuniformtensor(withshape:seed:name:))
- [func randomUniformTensor(withShape: [NSNumber], stateTensor: MPSGraphTensor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/randomuniformtensor(withshape:statetensor:name:))
- [func randomUniformTensor(withShapeTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/randomuniformtensor(withshapetensor:name:))
- [func randomUniformTensor(withShapeTensor: MPSGraphTensor, seed: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/randomuniformtensor(withshapetensor:seed:name:))
- [func randomUniformTensor(withShapeTensor: MPSGraphTensor, stateTensor: MPSGraphTensor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/randomuniformtensor(withshapetensor:statetensor:name:))
- [func reLU(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/relu(with:name:))
- [func reLUGradient(withIncomingGradient: MPSGraphTensor, sourceTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/relugradient(withincominggradient:sourcetensor:name:))
- [func read(MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/read(_:name:))
- [func realPartOfTensor(tensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/realpartoftensor(tensor:name:))
- [func realToHermiteanFFT(MPSGraphTensor, axes: [NSNumber], descriptor: MPSGraphFFTDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/realtohermiteanfft(_:axes:descriptor:name:))
- [func realToHermiteanFFT(MPSGraphTensor, axesTensor: MPSGraphTensor, descriptor: MPSGraphFFTDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/realtohermiteanfft(_:axestensor:descriptor:name:))
- [func reciprocal(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reciprocal(with:name:))
- [func reciprocalSquareRoot(MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reciprocalsquareroot(_:name:))
- [func reductionAnd(with: MPSGraphTensor, axes: [NSNumber]?, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionand(with:axes:name:))
- [func reductionAnd(with: MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionand(with:axis:name:))
- [func reductionArgMaximum(with: MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionargmaximum(with:axis:name:))
- [func reductionArgMinimum(with: MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionargminimum(with:axis:name:))
- [func reductionMaximum(with: MPSGraphTensor, axes: [NSNumber]?, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionmaximum(with:axes:name:))
- [func reductionMaximum(with: MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionmaximum(with:axis:name:))
- [func reductionMaximumPropagateNaN(with: MPSGraphTensor, axes: [NSNumber]?, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionmaximumpropagatenan(with:axes:name:))
- [func reductionMaximumPropagateNaN(with: MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionmaximumpropagatenan(with:axis:name:))
- [func reductionMinimum(with: MPSGraphTensor, axes: [NSNumber]?, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionminimum(with:axes:name:))
- [func reductionMinimum(with: MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionminimum(with:axis:name:))
- [func reductionMinimumPropagateNaN(with: MPSGraphTensor, axes: [NSNumber]?, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionminimumpropagatenan(with:axes:name:))
- [func reductionMinimumPropagateNaN(with: MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionminimumpropagatenan(with:axis:name:))
- [func reductionOr(with: MPSGraphTensor, axes: [NSNumber]?, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionor(with:axes:name:))
- [func reductionOr(with: MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionor(with:axis:name:))
- [func reductionProduct(with: MPSGraphTensor, axes: [NSNumber]?, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionproduct(with:axes:name:))
- [func reductionProduct(with: MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionproduct(with:axis:name:))
- [func reductionSum(with: MPSGraphTensor, axes: [NSNumber]?, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionsum(with:axes:name:))
- [func reductionSum(with: MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reductionsum(with:axis:name:))
- [func reinterpretCast(MPSGraphTensor, to: MPSDataType, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reinterpretcast(_:to:name:))
- [func reshape(MPSGraphTensor, shape: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reshape(_:shape:name:))
- [func reshape(MPSGraphTensor, shapeTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reshape(_:shapetensor:name:))
- [func resize(MPSGraphTensor, size: [NSNumber], mode: MPSGraphResizeMode, centerResult: Bool, alignCorners: Bool, layout: MPSGraphTensorNamedDataLayout, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resize(_:size:mode:centerresult:aligncorners:layout:name:))
- [func resize(MPSGraphTensor, sizeTensor: MPSGraphTensor, mode: MPSGraphResizeMode, centerResult: Bool, alignCorners: Bool, layout: MPSGraphTensorNamedDataLayout, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resize(_:sizetensor:mode:centerresult:aligncorners:layout:name:))
- [func resize(MPSGraphTensor, sizeTensor: MPSGraphTensor, mode: MPSGraphResizeMode, centerResult: Bool, alignCorners: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resize(_:sizetensor:mode:centerresult:aligncorners:name:))
- [func resize(MPSGraphTensor, sizeTensor: MPSGraphTensor, scaleOffsetTensor: MPSGraphTensor, mode: MPSGraphResizeMode, layout: MPSGraphTensorNamedDataLayout, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resize(_:sizetensor:scaleoffsettensor:mode:layout:name:))
- [func resize(MPSGraphTensor, sizeTensor: MPSGraphTensor, scaleTensor: MPSGraphTensor, offsetTenor: MPSGraphTensor, mode: MPSGraphResizeMode, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resize(_:sizetensor:scaletensor:offsettenor:mode:name:))
- [func resize(withGradientTensor: MPSGraphTensor, input: MPSGraphTensor, mode: MPSGraphResizeMode, centerResult: Bool, alignCorners: Bool, layout: MPSGraphTensorNamedDataLayout, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resize(withgradienttensor:input:mode:centerresult:aligncorners:layout:name:))
- [func resize(withGradientTensor: MPSGraphTensor, input: MPSGraphTensor, scale: MPSGraphTensor, offsetTensor: MPSGraphTensor, mode: MPSGraphResizeMode, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resize(withgradienttensor:input:scale:offsettensor:mode:name:))
- [func resize(withGradientTensor: MPSGraphTensor, input: MPSGraphTensor, scaleOffsetTensor: MPSGraphTensor, mode: MPSGraphResizeMode, layout: MPSGraphTensorNamedDataLayout, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resize(withgradienttensor:input:scaleoffsettensor:mode:layout:name:))
- [func resizeBilinear(MPSGraphTensor, sizeTensor: MPSGraphTensor, centerResult: Bool, alignCorners: Bool, layout: MPSGraphTensorNamedDataLayout, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resizebilinear(_:sizetensor:centerresult:aligncorners:layout:name:))
- [func resizeBilinear(MPSGraphTensor, sizeTensor: MPSGraphTensor, centerResult: Bool, alignCorners: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resizebilinear(_:sizetensor:centerresult:aligncorners:name:))
- [func resizeBilinear(MPSGraphTensor, sizeTensor: MPSGraphTensor, scaleOffsetTensor: MPSGraphTensor, layout: MPSGraphTensorNamedDataLayout, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resizebilinear(_:sizetensor:scaleoffsettensor:layout:name:))
- [func resizeBilinear(MPSGraphTensor, sizeTensor: MPSGraphTensor, scaleTensor: MPSGraphTensor, offsetTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resizebilinear(_:sizetensor:scaletensor:offsettensor:name:))
- [func resizeBilinear(withGradientTensor: MPSGraphTensor, input: MPSGraphTensor, centerResult: Bool, alignCorners: Bool, layout: MPSGraphTensorNamedDataLayout, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resizebilinear(withgradienttensor:input:centerresult:aligncorners:layout:name:))
- [func resizeBilinear(withGradientTensor: MPSGraphTensor, input: MPSGraphTensor, scale: MPSGraphTensor, offsetTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resizebilinear(withgradienttensor:input:scale:offsettensor:name:))
- [func resizeBilinear(withGradientTensor: MPSGraphTensor, input: MPSGraphTensor, scaleOffsetTensor: MPSGraphTensor, layout: MPSGraphTensorNamedDataLayout, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resizebilinear(withgradienttensor:input:scaleoffsettensor:layout:name:))
- [func resizeNearest(MPSGraphTensor, sizeTensor: MPSGraphTensor, nearestRoundingMode: MPSGraphResizeNearestRoundingMode, centerResult: Bool, alignCorners: Bool, layout: MPSGraphTensorNamedDataLayout, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resizenearest(_:sizetensor:nearestroundingmode:centerresult:aligncorners:layout:name:))
- [func resizeNearest(MPSGraphTensor, sizeTensor: MPSGraphTensor, nearestRoundingMode: MPSGraphResizeNearestRoundingMode, centerResult: Bool, alignCorners: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resizenearest(_:sizetensor:nearestroundingmode:centerresult:aligncorners:name:))
- [func resizeNearest(MPSGraphTensor, sizeTensor: MPSGraphTensor, scaleOffsetTensor: MPSGraphTensor, nearestRoundingMode: MPSGraphResizeNearestRoundingMode, layout: MPSGraphTensorNamedDataLayout, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resizenearest(_:sizetensor:scaleoffsettensor:nearestroundingmode:layout:name:))
- [func resizeNearest(MPSGraphTensor, sizeTensor: MPSGraphTensor, scaleTensor: MPSGraphTensor, offsetTensor: MPSGraphTensor, nearestRoundingMode: MPSGraphResizeNearestRoundingMode, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resizenearest(_:sizetensor:scaletensor:offsettensor:nearestroundingmode:name:))
- [func resizeNearest(withGradientTensor: MPSGraphTensor, input: MPSGraphTensor, nearestRoundingMode: MPSGraphResizeNearestRoundingMode, centerResult: Bool, alignCorners: Bool, layout: MPSGraphTensorNamedDataLayout, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resizenearest(withgradienttensor:input:nearestroundingmode:centerresult:aligncorners:layout:name:))
- [func resizeNearest(withGradientTensor: MPSGraphTensor, input: MPSGraphTensor, scale: MPSGraphTensor, offsetTensor: MPSGraphTensor, nearestRoundingMode: MPSGraphResizeNearestRoundingMode, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resizenearest(withgradienttensor:input:scale:offsettensor:nearestroundingmode:name:))
- [func resizeNearest(withGradientTensor: MPSGraphTensor, input: MPSGraphTensor, scaleOffsetTensor: MPSGraphTensor, nearestRoundingMode: MPSGraphResizeNearestRoundingMode, layout: MPSGraphTensorNamedDataLayout, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/resizenearest(withgradienttensor:input:scaleoffsettensor:nearestroundingmode:layout:name:))
- [func reverse(MPSGraphTensor, axes: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reverse(_:axes:name:))
- [func reverse(MPSGraphTensor, axesTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reverse(_:axestensor:name:))
- [func reverse(MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reverse(_:name:))
- [func reverseSquareRoot(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/reversesquareroot(with:name:))
- [func rint(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/rint(with:name:))
- [func round(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/round(with:name:))
- [func run(feeds: [MPSGraphTensor : MPSGraphTensorData], targetTensors: [MPSGraphTensor], targetOperations: [MPSGraphOperation]?) -> [MPSGraphTensor : MPSGraphTensorData]](/documentation/metalperformanceshadersgraph/mpsgraph/run(feeds:targettensors:targetoperations:))
- [func run(with: any MTLCommandQueue, feeds: [MPSGraphTensor : MPSGraphTensorData], targetOperations: [MPSGraphOperation]?, resultsDictionary: [MPSGraphTensor : MPSGraphTensorData])](/documentation/metalperformanceshadersgraph/mpsgraph/run(with:feeds:targetoperations:resultsdictionary:))
- [func run(with: any MTLCommandQueue, feeds: [MPSGraphTensor : MPSGraphTensorData], targetTensors: [MPSGraphTensor], targetOperations: [MPSGraphOperation]?) -> [MPSGraphTensor : MPSGraphTensorData]](/documentation/metalperformanceshadersgraph/mpsgraph/run(with:feeds:targettensors:targetoperations:))
- [func runAsync(feeds: [MPSGraphTensor : MPSGraphTensorData], targetTensors: [MPSGraphTensor], targetOperations: [MPSGraphOperation]?, executionDescriptor: MPSGraphExecutionDescriptor?) -> [MPSGraphTensor : MPSGraphTensorData]](/documentation/metalperformanceshadersgraph/mpsgraph/runasync(feeds:targettensors:targetoperations:executiondescriptor:))
- [func runAsync(with: any MTLCommandQueue, feeds: [MPSGraphTensor : MPSGraphTensorData], targetOperations: [MPSGraphOperation]?, resultsDictionary: [MPSGraphTensor : MPSGraphTensorData], executionDescriptor: MPSGraphExecutionDescriptor?)](/documentation/metalperformanceshadersgraph/mpsgraph/runasync(with:feeds:targetoperations:resultsdictionary:executiondescriptor:))
- [func runAsync(with: any MTLCommandQueue, feeds: [MPSGraphTensor : MPSGraphTensorData], targetTensors: [MPSGraphTensor], targetOperations: [MPSGraphOperation]?, executionDescriptor: MPSGraphExecutionDescriptor?) -> [MPSGraphTensor : MPSGraphTensorData]](/documentation/metalperformanceshadersgraph/mpsgraph/runasync(with:feeds:targettensors:targetoperations:executiondescriptor:))
- [func sampleGrid(withSourceTensor: MPSGraphTensor, coordinateTensor: MPSGraphTensor, layout: MPSGraphTensorNamedDataLayout, normalizeCoordinates: Bool, relativeCoordinates: Bool, alignCorners: Bool, paddingMode: MPSGraphPaddingMode, nearestRoundingMode: MPSGraphResizeNearestRoundingMode, constantValue: Double, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/samplegrid(withsourcetensor:coordinatetensor:layout:normalizecoordinates:relativecoordinates:aligncorners:paddingmode:nearestroundingmode:constantvalue:name:))
- [func sampleGrid(withSourceTensor: MPSGraphTensor, coordinateTensor: MPSGraphTensor, layout: MPSGraphTensorNamedDataLayout, normalizeCoordinates: Bool, relativeCoordinates: Bool, alignCorners: Bool, paddingMode: MPSGraphPaddingMode, samplingMode: MPSGraphResizeMode, constantValue: Double, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/samplegrid(withsourcetensor:coordinatetensor:layout:normalizecoordinates:relativecoordinates:aligncorners:paddingmode:samplingmode:constantvalue:name:))
- [func scaledDotProductAttention(query: MPSGraphTensor, key: MPSGraphTensor, value: MPSGraphTensor, mask: MPSGraphTensor?, scale: Float, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/scaleddotproductattention(query:key:value:mask:scale:name:))
- [func scaledDotProductAttention(query: MPSGraphTensor, key: MPSGraphTensor, value: MPSGraphTensor, scale: Float, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/scaleddotproductattention(query:key:value:scale:name:))
- [func scatter(MPSGraphTensor, indices: MPSGraphTensor, shape: [NSNumber], axis: Int, mode: MPSGraphScatterMode, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/scatter(_:indices:shape:axis:mode:name:))
- [func scatterAlongAxis(Int, data: MPSGraphTensor, updates: MPSGraphTensor, indices: MPSGraphTensor, mode: MPSGraphScatterMode, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/scatteralongaxis(_:data:updates:indices:mode:name:))
- [func scatterAlongAxis(Int, updates: MPSGraphTensor, indices: MPSGraphTensor, shape: [NSNumber], mode: MPSGraphScatterMode, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/scatteralongaxis(_:updates:indices:shape:mode:name:))
- [func scatterAlongAxisTensor(MPSGraphTensor, data: MPSGraphTensor, updates: MPSGraphTensor, indices: MPSGraphTensor, mode: MPSGraphScatterMode, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/scatteralongaxistensor(_:data:updates:indices:mode:name:))
- [func scatterAlongAxisTensor(MPSGraphTensor, updates: MPSGraphTensor, indices: MPSGraphTensor, shape: [NSNumber], mode: MPSGraphScatterMode, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/scatteralongaxistensor(_:updates:indices:shape:mode:name:))
- [func scatterND(withUpdatesTensor: MPSGraphTensor, indicesTensor: MPSGraphTensor, shape: [NSNumber], batchDimensions: Int, mode: MPSGraphScatterMode, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/scatternd(withupdatestensor:indicestensor:shape:batchdimensions:mode:name:))
- [func scatterND(withUpdatesTensor: MPSGraphTensor, indicesTensor: MPSGraphTensor, shape: [NSNumber], batchDimensions: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/scatternd(withupdatestensor:indicestensor:shape:batchdimensions:name:))
- [func scatterNDWithData(MPSGraphTensor, updates: MPSGraphTensor, indices: MPSGraphTensor, batchDimensions: Int, mode: MPSGraphScatterMode, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/scatterndwithdata(_:updates:indices:batchdimensions:mode:name:))
- [func scatterWithData(MPSGraphTensor, updates: MPSGraphTensor, indices: MPSGraphTensor, axis: Int, mode: MPSGraphScatterMode, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/scatterwithdata(_:updates:indices:axis:mode:name:))
- [func select(predicate: MPSGraphTensor, trueTensor: MPSGraphTensor, falseTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/select(predicate:truetensor:falsetensor:name:))
- [func shapeOf(MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/shapeof(_:name:))
- [func sigmoid(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sigmoid(with:name:))
- [func sigmoidGradient(withIncomingGradient: MPSGraphTensor, sourceTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sigmoidgradient(withincominggradient:sourcetensor:name:))
- [func sign(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sign(with:name:))
- [func signbit(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/signbit(with:name:))
- [func sin(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sin(with:name:))
- [func singleGateRNN(MPSGraphTensor, recurrentWeight: MPSGraphTensor, initState: MPSGraphTensor?, descriptor: MPSGraphSingleGateRNNDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/singlegaternn(_:recurrentweight:initstate:descriptor:name:))
- [func singleGateRNN(MPSGraphTensor, recurrentWeight: MPSGraphTensor, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, initState: MPSGraphTensor?, descriptor: MPSGraphSingleGateRNNDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/singlegaternn(_:recurrentweight:inputweight:bias:initstate:descriptor:name:))
- [func singleGateRNN(MPSGraphTensor, recurrentWeight: MPSGraphTensor, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, initState: MPSGraphTensor?, mask: MPSGraphTensor?, descriptor: MPSGraphSingleGateRNNDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/singlegaternn(_:recurrentweight:inputweight:bias:initstate:mask:descriptor:name:))
- [func singleGateRNNGradients(MPSGraphTensor, recurrentWeight: MPSGraphTensor, sourceGradient: MPSGraphTensor, zState: MPSGraphTensor, initState: MPSGraphTensor?, descriptor: MPSGraphSingleGateRNNDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/singlegaternngradients(_:recurrentweight:sourcegradient:zstate:initstate:descriptor:name:))
- [func singleGateRNNGradients(MPSGraphTensor, recurrentWeight: MPSGraphTensor, sourceGradient: MPSGraphTensor, zState: MPSGraphTensor, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, initState: MPSGraphTensor?, descriptor: MPSGraphSingleGateRNNDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/singlegaternngradients(_:recurrentweight:sourcegradient:zstate:inputweight:bias:initstate:descriptor:name:))
- [func singleGateRNNGradients(MPSGraphTensor, recurrentWeight: MPSGraphTensor, sourceGradient: MPSGraphTensor, zState: MPSGraphTensor, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, initState: MPSGraphTensor?, mask: MPSGraphTensor?, descriptor: MPSGraphSingleGateRNNDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/singlegaternngradients(_:recurrentweight:sourcegradient:zstate:inputweight:bias:initstate:mask:descriptor:name:))
- [func singleGateRNNGradients(MPSGraphTensor, recurrentWeight: MPSGraphTensor, sourceGradient: MPSGraphTensor, zState: MPSGraphTensor, stateGradient: MPSGraphTensor?, inputWeight: MPSGraphTensor?, bias: MPSGraphTensor?, initState: MPSGraphTensor?, mask: MPSGraphTensor?, descriptor: MPSGraphSingleGateRNNDescriptor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/singlegaternngradients(_:recurrentweight:sourcegradient:zstate:stategradient:inputweight:bias:initstate:mask:descriptor:name:))
- [func sinh(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sinh(with:name:))
- [func sliceGradientTensor(MPSGraphTensor, fwdInShapeTensor: MPSGraphTensor, start: MPSGraphTensor, end: MPSGraphTensor, strideTensor: MPSGraphTensor, startMask: UInt32, endMask: UInt32, squeezeMask: UInt32, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/slicegradienttensor(_:fwdinshapetensor:start:end:stridetensor:startmask:endmask:squeezemask:name:))
- [func sliceGradientTensor(MPSGraphTensor, fwdInShapeTensor: MPSGraphTensor, start: MPSGraphTensor, sizeTensor: MPSGraphTensor, squeezeMask: UInt32, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/slicegradienttensor(_:fwdinshapetensor:start:sizetensor:squeezemask:name:))
- [func sliceGradientTensor(MPSGraphTensor, fwdInShapeTensor: MPSGraphTensor, starts: [NSNumber], ends: [NSNumber], strides: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/slicegradienttensor(_:fwdinshapetensor:starts:ends:strides:name:))
- [func sliceGradientTensor(MPSGraphTensor, fwdInShapeTensor: MPSGraphTensor, starts: [NSNumber], ends: [NSNumber], strides: [NSNumber], startMask: UInt32, endMask: UInt32, squeezeMask: UInt32, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/slicegradienttensor(_:fwdinshapetensor:starts:ends:strides:startmask:endmask:squeezemask:name:))
- [func sliceTensor(MPSGraphTensor, dimension: Int, start: Int, length: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/slicetensor(_:dimension:start:length:name:))
- [func sliceTensor(MPSGraphTensor, start: MPSGraphTensor, end: MPSGraphTensor, strideTensor: MPSGraphTensor, startMask: UInt32, endMask: UInt32, squeezeMask: UInt32, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/slicetensor(_:start:end:stridetensor:startmask:endmask:squeezemask:name:))
- [func sliceTensor(MPSGraphTensor, start: MPSGraphTensor, sizeTensor: MPSGraphTensor, squeezeMask: UInt32, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/slicetensor(_:start:sizetensor:squeezemask:name:))
- [func sliceTensor(MPSGraphTensor, starts: [NSNumber], ends: [NSNumber], strides: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/slicetensor(_:starts:ends:strides:name:))
- [func sliceTensor(MPSGraphTensor, starts: [NSNumber], ends: [NSNumber], strides: [NSNumber], startMask: UInt32, endMask: UInt32, squeezeMask: UInt32, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/slicetensor(_:starts:ends:strides:startmask:endmask:squeezemask:name:))
- [func sliceUpdateDataTensor(MPSGraphTensor, update: MPSGraphTensor, starts: [NSNumber], ends: [NSNumber], strides: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sliceupdatedatatensor(_:update:starts:ends:strides:name:))
- [func sliceUpdateDataTensor(MPSGraphTensor, update: MPSGraphTensor, starts: [NSNumber], ends: [NSNumber], strides: [NSNumber], startMask: UInt32, endMask: UInt32, squeezeMask: UInt32, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sliceupdatedatatensor(_:update:starts:ends:strides:startmask:endmask:squeezemask:name:))
- [func sliceUpdateDataTensor(MPSGraphTensor, update: MPSGraphTensor, startsTensor: MPSGraphTensor, endsTensor: MPSGraphTensor, stridesTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sliceupdatedatatensor(_:update:startstensor:endstensor:stridestensor:name:))
- [func sliceUpdateDataTensor(MPSGraphTensor, update: MPSGraphTensor, startsTensor: MPSGraphTensor, endsTensor: MPSGraphTensor, stridesTensor: MPSGraphTensor, startMask: UInt32, endMask: UInt32, squeezeMask: UInt32, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sliceupdatedatatensor(_:update:startstensor:endstensor:stridestensor:startmask:endmask:squeezemask:name:))
- [func softMax(with: MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/softmax(with:axis:name:))
- [func softMaxCrossEntropy(MPSGraphTensor, labels: MPSGraphTensor, axis: Int, reuctionType: MPSGraphLossReductionType, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/softmaxcrossentropy(_:labels:axis:reuctiontype:name:))
- [func softMaxCrossEntropyGradient(MPSGraphTensor, source: MPSGraphTensor, labels: MPSGraphTensor, axis: Int, reuctionType: MPSGraphLossReductionType, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/softmaxcrossentropygradient(_:source:labels:axis:reuctiontype:name:))
- [func softMaxGradient(withIncomingGradient: MPSGraphTensor, sourceTensor: MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/softmaxgradient(withincominggradient:sourcetensor:axis:name:))
- [func sort(MPSGraphTensor, axis: Int, descending: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sort(_:axis:descending:name:))
- [func sort(MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sort(_:axis:name:))
- [func sort(MPSGraphTensor, axisTensor: MPSGraphTensor, descending: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sort(_:axistensor:descending:name:))
- [func sort(MPSGraphTensor, axisTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sort(_:axistensor:name:))
- [func space(toDepth2DTensor: MPSGraphTensor, widthAxis: Int, heightAxis: Int, depthAxis: Int, blockSize: Int, usePixelShuffleOrder: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/space(todepth2dtensor:widthaxis:heightaxis:depthaxis:blocksize:usepixelshuffleorder:name:))
- [func space(toDepth2DTensor: MPSGraphTensor, widthAxisTensor: MPSGraphTensor, heightAxisTensor: MPSGraphTensor, depthAxisTensor: MPSGraphTensor, blockSize: Int, usePixelShuffleOrder: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/space(todepth2dtensor:widthaxistensor:heightaxistensor:depthaxistensor:blocksize:usepixelshuffleorder:name:))
- [func spaceToBatch(MPSGraphTensor, spatialAxes: [NSNumber], batchAxis: Int, blockDimensions: [NSNumber], usePixelShuffleOrder: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/spacetobatch(_:spatialaxes:batchaxis:blockdimensions:usepixelshuffleorder:name:))
- [func spaceToBatch(MPSGraphTensor, spatialAxesTensor: MPSGraphTensor, batchAxisTensor: MPSGraphTensor, blockDimensionsTensor: MPSGraphTensor, usePixelShuffleOrder: Bool, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/spacetobatch(_:spatialaxestensor:batchaxistensor:blockdimensionstensor:usepixelshuffleorder:name:))
- [func sparseTensor(sparseTensorWithDescriptor: MPSGraphCreateSparseOpDescriptor, tensors: [MPSGraphTensor], shape: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sparsetensor(sparsetensorwithdescriptor:tensors:shape:name:))
- [func sparseTensor(sparseTensorWithType: MPSGraphSparseStorageType, tensors: [MPSGraphTensor], shape: [NSNumber], dataType: MPSDataType, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/sparsetensor(sparsetensorwithtype:tensors:shape:datatype:name:))
- [func split(MPSGraphTensor, numSplits: Int, axis: Int, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/split(_:numsplits:axis:name:))
- [func split(MPSGraphTensor, splitSizes: [NSNumber], axis: Int, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/split(_:splitsizes:axis:name:))
- [func split(MPSGraphTensor, splitSizesTensor: MPSGraphTensor, axis: Int, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/split(_:splitsizestensor:axis:name:))
- [func square(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/square(with:name:))
- [func squareRoot(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/squareroot(with:name:))
- [func squeeze(MPSGraphTensor, axes: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/squeeze(_:axes:name:))
- [func squeeze(MPSGraphTensor, axesTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/squeeze(_:axestensor:name:))
- [func squeeze(MPSGraphTensor, axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/squeeze(_:axis:name:))
- [func squeeze(MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/squeeze(_:name:))
- [func stack([MPSGraphTensor], axis: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/stack(_:axis:name:))
- [func stencil(withSourceTensor: MPSGraphTensor, weightsTensor: MPSGraphTensor, descriptor: MPSGraphStencilOpDescriptor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/stencil(withsourcetensor:weightstensor:descriptor:name:))
- [func stochasticGradientDescent(learningRate: MPSGraphTensor, values: MPSGraphTensor, gradient: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/stochasticgradientdescent(learningrate:values:gradient:name:))
- [func subtraction(MPSGraphTensor, MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/subtraction(_:_:name:))
- [func tan(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/tan(with:name:))
- [func tanh(with: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/tanh(with:name:))
- [func tileGradient(withIncomingGradientTensor: MPSGraphTensor, sourceTensor: MPSGraphTensor, withMultiplier: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/tilegradient(withincominggradienttensor:sourcetensor:withmultiplier:name:))
- [func tileTensor(MPSGraphTensor, withMultiplier: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/tiletensor(_:withmultiplier:name:))
- [func topK(MPSGraphTensor, axis: Int, k: Int, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/topk(_:axis:k:name:))
- [func topK(MPSGraphTensor, axisTensor: MPSGraphTensor, kTensor: MPSGraphTensor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/topk(_:axistensor:ktensor:name:))
- [func topK(MPSGraphTensor, k: Int, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/topk(_:k:name:))
- [func topK(MPSGraphTensor, kTensor: MPSGraphTensor, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/topk(_:ktensor:name:))
- [func topKGradient(MPSGraphTensor, input: MPSGraphTensor, k: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/topkgradient(_:input:k:name:))
- [func topKGradient(MPSGraphTensor, input: MPSGraphTensor, kTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/topkgradient(_:input:ktensor:name:))
- [func topKGradient(MPSGraphTensor, source: MPSGraphTensor, axis: Int, k: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/topkgradient(_:source:axis:k:name:))
- [func topKGradient(MPSGraphTensor, source: MPSGraphTensor, axisTensor: MPSGraphTensor, kTensor: MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/topkgradient(_:source:axistensor:ktensor:name:))
- [func transpose(MPSGraphTensor, permutation: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/transpose(_:permutation:name:))
- [func transposeTensor(MPSGraphTensor, dimension: Int, withDimension: Int, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/transposetensor(_:dimension:withdimension:name:))
- [func truncate(MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/truncate(_:name:))
- [func variable(with: Data, shape: [NSNumber], dataType: MPSDataType, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/variable(with:shape:datatype:name:))
- [func variableFromTensor(MPSGraphTensor, name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/variablefromtensor(_:name:))
- [func variance(of: MPSGraphTensor, axes: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/variance(of:axes:name:))
- [func variance(of: MPSGraphTensor, mean: MPSGraphTensor, axes: [NSNumber], name: String?) -> MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraph/variance(of:mean:axes:name:))
- [func `while`(initialInputs: [MPSGraphTensor], before: MPSGraphWhileBeforeBlock, after: MPSGraphWhileAfterBlock, name: String?) -> [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraph/while(initialinputs:before:after:name:))

### Type Methods

- [class func new() -> Self](/documentation/metalperformanceshadersgraph/mpsgraph/new())
- [MPSGraphCompilationDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphcompilationdescriptor)

### Instance Properties

- [var callables: [String : MPSGraphExecutable]?](/documentation/metalperformanceshadersgraph/mpsgraphcompilationdescriptor/callables)
- [var compilationCompletionHandler: MPSGraphCompilationCompletionHandler](/documentation/metalperformanceshadersgraph/mpsgraphcompilationdescriptor/compilationcompletionhandler)
- [var dispatchQueue: dispatch_queue_t](/documentation/metalperformanceshadersgraph/mpsgraphcompilationdescriptor/dispatchqueue)
- [var optimizationLevel: MPSGraphOptimization](/documentation/metalperformanceshadersgraph/mpsgraphcompilationdescriptor/optimizationlevel)
- [var optimizationProfile: MPSGraphOptimizationProfile](/documentation/metalperformanceshadersgraph/mpsgraphcompilationdescriptor/optimizationprofile)
- [var reducedPrecisionFastMath: MPSGraphReducedPrecisionFastMath](/documentation/metalperformanceshadersgraph/mpsgraphcompilationdescriptor/reducedprecisionfastmath)
- [var waitForCompilationCompletion: Bool](/documentation/metalperformanceshadersgraph/mpsgraphcompilationdescriptor/waitforcompilationcompletion)

### Instance Methods

- [func disableTypeInference()](/documentation/metalperformanceshadersgraph/mpsgraphcompilationdescriptor/disabletypeinference())
- [MPSGraphConvolution2DOpDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor)

### Initializers

- [convenience init?(strideInX: Int, strideInY: Int, dilationRateInX: Int, dilationRateInY: Int, groups: Int, paddingLeft: Int, paddingRight: Int, paddingTop: Int, paddingBottom: Int, paddingStyle: MPSGraphPaddingStyle, dataLayout: MPSGraphTensorNamedDataLayout, weightsLayout: MPSGraphTensorNamedDataLayout)](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/init(strideinx:strideiny:dilationrateinx:dilationrateiny:groups:paddingleft:paddingright:paddingtop:paddingbottom:paddingstyle:datalayout:weightslayout:))
- [convenience init?(strideInX: Int, strideInY: Int, dilationRateInX: Int, dilationRateInY: Int, groups: Int, paddingStyle: MPSGraphPaddingStyle, dataLayout: MPSGraphTensorNamedDataLayout, weightsLayout: MPSGraphTensorNamedDataLayout)](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/init(strideinx:strideiny:dilationrateinx:dilationrateiny:groups:paddingstyle:datalayout:weightslayout:))

### Instance Properties

- [var dataLayout: MPSGraphTensorNamedDataLayout](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/datalayout)
- [var dilationRateInX: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/dilationrateinx)
- [var dilationRateInY: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/dilationrateiny)
- [var groups: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/groups)
- [var paddingBottom: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/paddingbottom)
- [var paddingLeft: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/paddingleft)
- [var paddingRight: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/paddingright)
- [var paddingStyle: MPSGraphPaddingStyle](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/paddingstyle)
- [var paddingTop: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/paddingtop)
- [var strideInX: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/strideinx)
- [var strideInY: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/strideiny)
- [var weightsLayout: MPSGraphTensorNamedDataLayout](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/weightslayout)

### Instance Methods

- [func setExplicitPaddingWithPaddingLeft(Int, paddingRight: Int, paddingTop: Int, paddingBottom: Int)](/documentation/metalperformanceshadersgraph/mpsgraphconvolution2dopdescriptor/setexplicitpaddingwithpaddingleft(_:paddingright:paddingtop:paddingbottom:))
- [MPSGraphConvolution3DOpDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor)

### Initializers

- [convenience init?(strideInX: Int, strideInY: Int, strideInZ: Int, dilationRateInX: Int, dilationRateInY: Int, dilationRateInZ: Int, groups: Int, paddingLeft: Int, paddingRight: Int, paddingTop: Int, paddingBottom: Int, paddingFront: Int, paddingBack: Int, paddingStyle: MPSGraphPaddingStyle, dataLayout: MPSGraphTensorNamedDataLayout, weightsLayout: MPSGraphTensorNamedDataLayout)](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/init(strideinx:strideiny:strideinz:dilationrateinx:dilationrateiny:dilationrateinz:groups:paddingleft:paddingright:paddingtop:paddingbottom:paddingfront:paddingback:paddingstyle:datalayout:weightslayout:))
- [convenience init?(strideInX: Int, strideInY: Int, strideInZ: Int, dilationRateInX: Int, dilationRateInY: Int, dilationRateInZ: Int, groups: Int, paddingStyle: MPSGraphPaddingStyle, dataLayout: MPSGraphTensorNamedDataLayout, weightsLayout: MPSGraphTensorNamedDataLayout)](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/init(strideinx:strideiny:strideinz:dilationrateinx:dilationrateiny:dilationrateinz:groups:paddingstyle:datalayout:weightslayout:))

### Instance Properties

- [var dataLayout: MPSGraphTensorNamedDataLayout](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/datalayout)
- [var dilationRateInX: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/dilationrateinx)
- [var dilationRateInY: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/dilationrateiny)
- [var dilationRateInZ: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/dilationrateinz)
- [var groups: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/groups)
- [var paddingBack: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/paddingback)
- [var paddingBottom: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/paddingbottom)
- [var paddingFront: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/paddingfront)
- [var paddingLeft: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/paddingleft)
- [var paddingRight: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/paddingright)
- [var paddingStyle: MPSGraphPaddingStyle](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/paddingstyle)
- [var paddingTop: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/paddingtop)
- [var strideInX: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/strideinx)
- [var strideInY: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/strideiny)
- [var strideInZ: Int](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/strideinz)
- [var weightsLayout: MPSGraphTensorNamedDataLayout](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/weightslayout)

### Instance Methods

- [func setExplicitPaddingWithPaddingLeft(Int, paddingRight: Int, paddingTop: Int, paddingBottom: Int, paddingFront: Int, paddingBack: Int)](/documentation/metalperformanceshadersgraph/mpsgraphconvolution3dopdescriptor/setexplicitpaddingwithpaddingleft(_:paddingright:paddingtop:paddingbottom:paddingfront:paddingback:))
- [MPSGraphCreateSparseOpDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphcreatesparseopdescriptor)

### Instance Properties

- [var dataType: MPSDataType](/documentation/metalperformanceshadersgraph/mpsgraphcreatesparseopdescriptor/datatype)
- [var sparseStorageType: MPSGraphSparseStorageType](/documentation/metalperformanceshadersgraph/mpsgraphcreatesparseopdescriptor/sparsestoragetype)

### Type Methods

- [class func sparseDescriptor(descriptorWithStorageType: MPSGraphSparseStorageType, dataType: MPSDataType) -> Self?](/documentation/metalperformanceshadersgraph/mpsgraphcreatesparseopdescriptor/sparsedescriptor(descriptorwithstoragetype:datatype:))
- [MPSGraphDepthwiseConvolution2DOpDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor)

### Initializers

- [convenience init?(dataLayout: MPSGraphTensorNamedDataLayout, weightsLayout: MPSGraphTensorNamedDataLayout)](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor/init(datalayout:weightslayout:))
- [convenience init?(strideInX: Int, strideInY: Int, dilationRateInX: Int, dilationRateInY: Int, paddingLeft: Int, paddingRight: Int, paddingTop: Int, paddingBottom: Int, paddingStyle: MPSGraphPaddingStyle, dataLayout: MPSGraphTensorNamedDataLayout, weightsLayout: MPSGraphTensorNamedDataLayout)](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor/init(strideinx:strideiny:dilationrateinx:dilationrateiny:paddingleft:paddingright:paddingtop:paddingbottom:paddingstyle:datalayout:weightslayout:))

### Instance Properties

- [var dataLayout: MPSGraphTensorNamedDataLayout](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor/datalayout)
- [var dilationRateInX: Int](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor/dilationrateinx)
- [var dilationRateInY: Int](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor/dilationrateiny)
- [var paddingBottom: Int](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor/paddingbottom)
- [var paddingLeft: Int](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor/paddingleft)
- [var paddingRight: Int](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor/paddingright)
- [var paddingStyle: MPSGraphPaddingStyle](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor/paddingstyle)
- [var paddingTop: Int](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor/paddingtop)
- [var strideInX: Int](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor/strideinx)
- [var strideInY: Int](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor/strideiny)
- [var weightsLayout: MPSGraphTensorNamedDataLayout](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor/weightslayout)

### Instance Methods

- [func setExplicitPaddingWithPaddingLeft(Int, paddingRight: Int, paddingTop: Int, paddingBottom: Int)](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution2dopdescriptor/setexplicitpaddingwithpaddingleft(_:paddingright:paddingtop:paddingbottom:))
- [MPSGraphDepthwiseConvolution3DOpDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution3dopdescriptor)

### Initializers

- [convenience init?(paddingStyle: MPSGraphPaddingStyle)](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution3dopdescriptor/init(paddingstyle:))
- [convenience init?(strides: [NSNumber], dilationRates: [NSNumber], paddingValues: [NSNumber], paddingStyle: MPSGraphPaddingStyle)](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution3dopdescriptor/init(strides:dilationrates:paddingvalues:paddingstyle:))

### Instance Properties

- [var channelDimensionIndex: Int](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution3dopdescriptor/channeldimensionindex)
- [var dilationRates: [NSNumber]](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution3dopdescriptor/dilationrates)
- [var paddingStyle: MPSGraphPaddingStyle](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution3dopdescriptor/paddingstyle)
- [var paddingValues: [NSNumber]](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution3dopdescriptor/paddingvalues)
- [var strides: [NSNumber]](/documentation/metalperformanceshadersgraph/mpsgraphdepthwiseconvolution3dopdescriptor/strides)
- [MPSGraphDevice](/documentation/metalperformanceshadersgraph/mpsgraphdevice)

### Initializers

- [convenience init(mtlDevice: any MTLDevice)](/documentation/metalperformanceshadersgraph/mpsgraphdevice/init(mtldevice:))

### Instance Properties

- [var metalDevice: (any MTLDevice)?](/documentation/metalperformanceshadersgraph/mpsgraphdevice/metaldevice)
- [var type: MPSGraphDeviceType](/documentation/metalperformanceshadersgraph/mpsgraphdevice/type)
- [MPSGraphExecutable](/documentation/metalperformanceshadersgraph/mpsgraphexecutable)

### Initializers

- [init(coreMLPackageAtURL: URL, descriptor: MPSGraphCompilationDescriptor?)](/documentation/metalperformanceshadersgraph/mpsgraphexecutable/init(coremlpackageaturl:descriptor:))
- [init(package: URL, descriptor: MPSGraphCompilationDescriptor?)](/documentation/metalperformanceshadersgraph/mpsgraphexecutable/init(package:descriptor:))

### Instance Properties

- [var feedTensors: [MPSGraphTensor]?](/documentation/metalperformanceshadersgraph/mpsgraphexecutable/feedtensors)
- [var options: MPSGraphOptions](/documentation/metalperformanceshadersgraph/mpsgraphexecutable/options)
- [var targetTensors: [MPSGraphTensor]?](/documentation/metalperformanceshadersgraph/mpsgraphexecutable/targettensors)

### Instance Methods

- [func encode(to: MPSCommandBuffer, inputs: [MPSGraphTensorData], results: [MPSGraphTensorData]?, executionDescriptor: MPSGraphExecutableExecutionDescriptor?) -> [MPSGraphTensorData]](/documentation/metalperformanceshadersgraph/mpsgraphexecutable/encode(to:inputs:results:executiondescriptor:))
- [func getOutputTypes(with: MPSGraphDevice?, inputTypes: [MPSGraphType], compilationDescriptor: MPSGraphCompilationDescriptor?) -> [MPSGraphShapedType]?](/documentation/metalperformanceshadersgraph/mpsgraphexecutable/getoutputtypes(with:inputtypes:compilationdescriptor:))
- [func run(with: any MTLCommandQueue, inputs: [MPSGraphTensorData], results: [MPSGraphTensorData]?, executionDescriptor: MPSGraphExecutableExecutionDescriptor?) -> [MPSGraphTensorData]](/documentation/metalperformanceshadersgraph/mpsgraphexecutable/run(with:inputs:results:executiondescriptor:))
- [func runAsync(with: any MTLCommandQueue, inputs: [MPSGraphTensorData], results: [MPSGraphTensorData]?, executionDescriptor: MPSGraphExecutableExecutionDescriptor?) -> [MPSGraphTensorData]](/documentation/metalperformanceshadersgraph/mpsgraphexecutable/runasync(with:inputs:results:executiondescriptor:))
- [func serialize(package: URL, descriptor: MPSGraphExecutableSerializationDescriptor?)](/documentation/metalperformanceshadersgraph/mpsgraphexecutable/serialize(package:descriptor:))
- [func specialize(with: MPSGraphDevice?, inputTypes: [MPSGraphType], compilationDescriptor: MPSGraphCompilationDescriptor?)](/documentation/metalperformanceshadersgraph/mpsgraphexecutable/specialize(with:inputtypes:compilationdescriptor:))
- [MPSGraphExecutableExecutionDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphexecutableexecutiondescriptor)

### Instance Properties

- [var completionHandler: MPSGraphExecutableCompletionHandler](/documentation/metalperformanceshadersgraph/mpsgraphexecutableexecutiondescriptor/completionhandler)
- [var scheduledHandler: MPSGraphExecutableScheduledHandler](/documentation/metalperformanceshadersgraph/mpsgraphexecutableexecutiondescriptor/scheduledhandler)
- [var waitUntilCompleted: Bool](/documentation/metalperformanceshadersgraph/mpsgraphexecutableexecutiondescriptor/waituntilcompleted)

### Instance Methods

- [func signal(any MTLSharedEvent, atExecutionEvent: MPSGraphExecutionStage, value: UInt64)](/documentation/metalperformanceshadersgraph/mpsgraphexecutableexecutiondescriptor/signal(_:atexecutionevent:value:))
- [func wait(for: any MTLSharedEvent, value: UInt64)](/documentation/metalperformanceshadersgraph/mpsgraphexecutableexecutiondescriptor/wait(for:value:))
- [MPSGraphExecutableSerializationDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphexecutableserializationdescriptor)

### Instance Properties

- [var append: Bool](/documentation/metalperformanceshadersgraph/mpsgraphexecutableserializationdescriptor/append)
- [var deploymentPlatform: MPSGraphDeploymentPlatform](/documentation/metalperformanceshadersgraph/mpsgraphexecutableserializationdescriptor/deploymentplatform)
- [var minimumDeploymentTarget: String](/documentation/metalperformanceshadersgraph/mpsgraphexecutableserializationdescriptor/minimumdeploymenttarget)
- [MPSGraphExecutionDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphexecutiondescriptor)

### Instance Properties

- [var compilationDescriptor: MPSGraphCompilationDescriptor?](/documentation/metalperformanceshadersgraph/mpsgraphexecutiondescriptor/compilationdescriptor)
- [var completionHandler: MPSGraphCompletionHandler](/documentation/metalperformanceshadersgraph/mpsgraphexecutiondescriptor/completionhandler)
- [var scheduledHandler: MPSGraphScheduledHandler](/documentation/metalperformanceshadersgraph/mpsgraphexecutiondescriptor/scheduledhandler)
- [var waitUntilCompleted: Bool](/documentation/metalperformanceshadersgraph/mpsgraphexecutiondescriptor/waituntilcompleted)

### Instance Methods

- [func signal(any MTLSharedEvent, atExecutionEvent: MPSGraphExecutionStage, value: UInt64)](/documentation/metalperformanceshadersgraph/mpsgraphexecutiondescriptor/signal(_:atexecutionevent:value:))
- [func wait(for: any MTLSharedEvent, value: UInt64)](/documentation/metalperformanceshadersgraph/mpsgraphexecutiondescriptor/wait(for:value:))
- [MPSGraphFFTDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphfftdescriptor)

### Instance Properties

- [var inverse: Bool](/documentation/metalperformanceshadersgraph/mpsgraphfftdescriptor/inverse)
- [var roundToOddHermitean: Bool](/documentation/metalperformanceshadersgraph/mpsgraphfftdescriptor/roundtooddhermitean)
- [var scalingMode: MPSGraphFFTScalingMode](/documentation/metalperformanceshadersgraph/mpsgraphfftdescriptor/scalingmode)
- [MPSGraphGRUDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphgrudescriptor)

### Instance Properties

- [var bidirectional: Bool](/documentation/metalperformanceshadersgraph/mpsgraphgrudescriptor/bidirectional)
- [var flipZ: Bool](/documentation/metalperformanceshadersgraph/mpsgraphgrudescriptor/flipz)
- [var outputGateActivation: MPSGraphRNNActivation](/documentation/metalperformanceshadersgraph/mpsgraphgrudescriptor/outputgateactivation)
- [var resetAfter: Bool](/documentation/metalperformanceshadersgraph/mpsgraphgrudescriptor/resetafter)
- [var resetGateActivation: MPSGraphRNNActivation](/documentation/metalperformanceshadersgraph/mpsgraphgrudescriptor/resetgateactivation)
- [var resetGateFirst: Bool](/documentation/metalperformanceshadersgraph/mpsgraphgrudescriptor/resetgatefirst)
- [var reverse: Bool](/documentation/metalperformanceshadersgraph/mpsgraphgrudescriptor/reverse)
- [var training: Bool](/documentation/metalperformanceshadersgraph/mpsgraphgrudescriptor/training)
- [var updateGateActivation: MPSGraphRNNActivation](/documentation/metalperformanceshadersgraph/mpsgraphgrudescriptor/updategateactivation)
- [MPSGraphImToColOpDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor)

### Initializers

- [convenience init?(kernelWidth: Int, kernelHeight: Int, strideInX: Int, strideInY: Int, dilationRateInX: Int, dilationRateInY: Int, dataLayout: MPSGraphTensorNamedDataLayout)](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor/init(kernelwidth:kernelheight:strideinx:strideiny:dilationrateinx:dilationrateiny:datalayout:))
- [convenience init?(kernelWidth: Int, kernelHeight: Int, strideInX: Int, strideInY: Int, dilationRateInX: Int, dilationRateInY: Int, paddingLeft: Int, paddingRight: Int, paddingTop: Int, paddingBottom: Int, dataLayout: MPSGraphTensorNamedDataLayout)](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor/init(kernelwidth:kernelheight:strideinx:strideiny:dilationrateinx:dilationrateiny:paddingleft:paddingright:paddingtop:paddingbottom:datalayout:))

### Instance Properties

- [var dataLayout: MPSGraphTensorNamedDataLayout](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor/datalayout)
- [var dilationRateInX: Int](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor/dilationrateinx)
- [var dilationRateInY: Int](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor/dilationrateiny)
- [var kernelHeight: Int](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor/kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor/kernelwidth)
- [var paddingBottom: Int](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor/paddingbottom)
- [var paddingLeft: Int](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor/paddingleft)
- [var paddingRight: Int](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor/paddingright)
- [var paddingTop: Int](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor/paddingtop)
- [var strideInX: Int](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor/strideinx)
- [var strideInY: Int](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor/strideiny)

### Instance Methods

- [func setExplicitPaddingWithPaddingLeft(Int, paddingRight: Int, paddingTop: Int, paddingBottom: Int)](/documentation/metalperformanceshadersgraph/mpsgraphimtocolopdescriptor/setexplicitpaddingwithpaddingleft(_:paddingright:paddingtop:paddingbottom:))
- [MPSGraphLSTMDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphlstmdescriptor)

### Instance Properties

- [var activation: MPSGraphRNNActivation](/documentation/metalperformanceshadersgraph/mpsgraphlstmdescriptor/activation)
- [var bidirectional: Bool](/documentation/metalperformanceshadersgraph/mpsgraphlstmdescriptor/bidirectional)
- [var cellGateActivation: MPSGraphRNNActivation](/documentation/metalperformanceshadersgraph/mpsgraphlstmdescriptor/cellgateactivation)
- [var forgetGateActivation: MPSGraphRNNActivation](/documentation/metalperformanceshadersgraph/mpsgraphlstmdescriptor/forgetgateactivation)
- [var forgetGateLast: Bool](/documentation/metalperformanceshadersgraph/mpsgraphlstmdescriptor/forgetgatelast)
- [var inputGateActivation: MPSGraphRNNActivation](/documentation/metalperformanceshadersgraph/mpsgraphlstmdescriptor/inputgateactivation)
- [var outputGateActivation: MPSGraphRNNActivation](/documentation/metalperformanceshadersgraph/mpsgraphlstmdescriptor/outputgateactivation)
- [var produceCell: Bool](/documentation/metalperformanceshadersgraph/mpsgraphlstmdescriptor/producecell)
- [var reverse: Bool](/documentation/metalperformanceshadersgraph/mpsgraphlstmdescriptor/reverse)
- [var training: Bool](/documentation/metalperformanceshadersgraph/mpsgraphlstmdescriptor/training)
- [MPSGraphObject](/documentation/metalperformanceshadersgraph/mpsgraphobject)
- [MPSGraphOperation](/documentation/metalperformanceshadersgraph/mpsgraphoperation)

### Instance Properties

- [var controlDependencies: [MPSGraphOperation]](/documentation/metalperformanceshadersgraph/mpsgraphoperation/controldependencies)
- [var graph: MPSGraph](/documentation/metalperformanceshadersgraph/mpsgraphoperation/graph)
- [var inputTensors: [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraphoperation/inputtensors)
- [var name: String](/documentation/metalperformanceshadersgraph/mpsgraphoperation/name)
- [var outputTensors: [MPSGraphTensor]](/documentation/metalperformanceshadersgraph/mpsgraphoperation/outputtensors)
- [MPSGraphPooling2DOpDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor)

### Initializers

- [convenience init?(kernelWidth: Int, kernelHeight: Int, strideInX: Int, strideInY: Int, dilationRateInX: Int, dilationRateInY: Int, paddingLeft: Int, paddingRight: Int, paddingTop: Int, paddingBottom: Int, paddingStyle: MPSGraphPaddingStyle, dataLayout: MPSGraphTensorNamedDataLayout)](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/init(kernelwidth:kernelheight:strideinx:strideiny:dilationrateinx:dilationrateiny:paddingleft:paddingright:paddingtop:paddingbottom:paddingstyle:datalayout:))
- [convenience init?(kernelWidth: Int, kernelHeight: Int, strideInX: Int, strideInY: Int, paddingStyle: MPSGraphPaddingStyle, dataLayout: MPSGraphTensorNamedDataLayout)](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/init(kernelwidth:kernelheight:strideinx:strideiny:paddingstyle:datalayout:))

### Instance Properties

- [var ceilMode: Bool](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/ceilmode)
- [var dataLayout: MPSGraphTensorNamedDataLayout](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/datalayout)
- [var dilationRateInX: Int](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/dilationrateinx)
- [var dilationRateInY: Int](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/dilationrateiny)
- [var includeZeroPadToAverage: Bool](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/includezeropadtoaverage)
- [var kernelHeight: Int](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/kernelheight)
- [var kernelWidth: Int](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/kernelwidth)
- [var paddingBottom: Int](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/paddingbottom)
- [var paddingLeft: Int](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/paddingleft)
- [var paddingRight: Int](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/paddingright)
- [var paddingStyle: MPSGraphPaddingStyle](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/paddingstyle)
- [var paddingTop: Int](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/paddingtop)
- [var returnIndicesDataType: MPSDataType](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/returnindicesdatatype)
- [var returnIndicesMode: MPSGraphPoolingReturnIndicesMode](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/returnindicesmode)
- [var strideInX: Int](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/strideinx)
- [var strideInY: Int](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/strideiny)

### Instance Methods

- [func setExplicitPaddingWithPaddingLeft(Int, paddingRight: Int, paddingTop: Int, paddingBottom: Int)](/documentation/metalperformanceshadersgraph/mpsgraphpooling2dopdescriptor/setexplicitpaddingwithpaddingleft(_:paddingright:paddingtop:paddingbottom:))
- [MPSGraphPooling4DOpDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphpooling4dopdescriptor)

### Initializers

- [convenience init?(kernelSizes: [NSNumber], paddingStyle: MPSGraphPaddingStyle)](/documentation/metalperformanceshadersgraph/mpsgraphpooling4dopdescriptor/init(kernelsizes:paddingstyle:))
- [convenience init?(kernelSizes: [NSNumber], strides: [NSNumber], dilationRates: [NSNumber], paddingValues: [NSNumber], paddingStyle: MPSGraphPaddingStyle)](/documentation/metalperformanceshadersgraph/mpsgraphpooling4dopdescriptor/init(kernelsizes:strides:dilationrates:paddingvalues:paddingstyle:))

### Instance Properties

- [var ceilMode: Bool](/documentation/metalperformanceshadersgraph/mpsgraphpooling4dopdescriptor/ceilmode)
- [var dilationRates: [NSNumber]](/documentation/metalperformanceshadersgraph/mpsgraphpooling4dopdescriptor/dilationrates)
- [var includeZeroPadToAverage: Bool](/documentation/metalperformanceshadersgraph/mpsgraphpooling4dopdescriptor/includezeropadtoaverage)
- [var kernelSizes: [NSNumber]](/documentation/metalperformanceshadersgraph/mpsgraphpooling4dopdescriptor/kernelsizes)
- [var paddingStyle: MPSGraphPaddingStyle](/documentation/metalperformanceshadersgraph/mpsgraphpooling4dopdescriptor/paddingstyle)
- [var paddingValues: [NSNumber]](/documentation/metalperformanceshadersgraph/mpsgraphpooling4dopdescriptor/paddingvalues)
- [var returnIndicesDataType: MPSDataType](/documentation/metalperformanceshadersgraph/mpsgraphpooling4dopdescriptor/returnindicesdatatype)
- [var returnIndicesMode: MPSGraphPoolingReturnIndicesMode](/documentation/metalperformanceshadersgraph/mpsgraphpooling4dopdescriptor/returnindicesmode)
- [var strides: [NSNumber]](/documentation/metalperformanceshadersgraph/mpsgraphpooling4dopdescriptor/strides)
- [MPSGraphRandomOpDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphrandomopdescriptor)

### Initializers

- [convenience init?(distribution: MPSGraphRandomDistribution, dataType: MPSDataType)](/documentation/metalperformanceshadersgraph/mpsgraphrandomopdescriptor/init(distribution:datatype:))

### Instance Properties

- [var dataType: MPSDataType](/documentation/metalperformanceshadersgraph/mpsgraphrandomopdescriptor/datatype)
- [var distribution: MPSGraphRandomDistribution](/documentation/metalperformanceshadersgraph/mpsgraphrandomopdescriptor/distribution)
- [var max: Float](/documentation/metalperformanceshadersgraph/mpsgraphrandomopdescriptor/max)
- [var maxInteger: Int](/documentation/metalperformanceshadersgraph/mpsgraphrandomopdescriptor/maxinteger)
- [var mean: Float](/documentation/metalperformanceshadersgraph/mpsgraphrandomopdescriptor/mean)
- [var min: Float](/documentation/metalperformanceshadersgraph/mpsgraphrandomopdescriptor/min)
- [var minInteger: Int](/documentation/metalperformanceshadersgraph/mpsgraphrandomopdescriptor/mininteger)
- [var samplingMethod: MPSGraphRandomNormalSamplingMethod](/documentation/metalperformanceshadersgraph/mpsgraphrandomopdescriptor/samplingmethod)
- [var standardDeviation: Float](/documentation/metalperformanceshadersgraph/mpsgraphrandomopdescriptor/standarddeviation)
- [MPSGraphShapedType](/documentation/metalperformanceshadersgraph/mpsgraphshapedtype)

### Initializers

- [init(shape: [NSNumber]?, dataType: MPSDataType)](/documentation/metalperformanceshadersgraph/mpsgraphshapedtype/init(shape:datatype:))

### Instance Properties

- [var dataType: MPSDataType](/documentation/metalperformanceshadersgraph/mpsgraphshapedtype/datatype)
- [var shape: [NSNumber]?](/documentation/metalperformanceshadersgraph/mpsgraphshapedtype/shape)

### Instance Methods

- [func isEqual(to: MPSGraphShapedType?) -> Bool](/documentation/metalperformanceshadersgraph/mpsgraphshapedtype/isequal(to:))
- [MPSGraphSingleGateRNNDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphsinglegaternndescriptor)

### Instance Properties

- [var activation: MPSGraphRNNActivation](/documentation/metalperformanceshadersgraph/mpsgraphsinglegaternndescriptor/activation)
- [var bidirectional: Bool](/documentation/metalperformanceshadersgraph/mpsgraphsinglegaternndescriptor/bidirectional)
- [var reverse: Bool](/documentation/metalperformanceshadersgraph/mpsgraphsinglegaternndescriptor/reverse)
- [var training: Bool](/documentation/metalperformanceshadersgraph/mpsgraphsinglegaternndescriptor/training)
- [MPSGraphStencilOpDescriptor](/documentation/metalperformanceshadersgraph/mpsgraphstencilopdescriptor)

### Initializers

- [convenience init?(explicitPadding: [NSNumber])](/documentation/metalperformanceshadersgraph/mpsgraphstencilopdescriptor/init(explicitpadding:))
- [convenience init?(offsets: [NSNumber], explicitPadding: [NSNumber])](/documentation/metalperformanceshadersgraph/mpsgraphstencilopdescriptor/init(offsets:explicitpadding:))
- [convenience init?(paddingStyle: MPSGraphPaddingStyle)](/documentation/metalperformanceshadersgraph/mpsgraphstencilopdescriptor/init(paddingstyle:))
- [convenience init?(reductionMode: MPSGraphReductionMode, offsets: [NSNumber], strides: [NSNumber], dilationRates: [NSNumber], explicitPadding: [NSNumber], boundaryMode: MPSGraphPaddingMode, paddingStyle: MPSGraphPaddingStyle, paddingConstant: Float)](/documentation/metalperformanceshadersgraph/mpsgraphstencilopdescriptor/init(reductionmode:offsets:strides:dilationrates:explicitpadding:boundarymode:paddingstyle:paddingconstant:))

### Instance Properties

- [var boundaryMode: MPSGraphPaddingMode](/documentation/metalperformanceshadersgraph/mpsgraphstencilopdescriptor/boundarymode)
- [var dilationRates: [NSNumber]](/documentation/metalperformanceshadersgraph/mpsgraphstencilopdescriptor/dilationrates)
- [var explicitPadding: [NSNumber]](/documentation/metalperformanceshadersgraph/mpsgraphstencilopdescriptor/explicitpadding)
- [var offsets: [NSNumber]](/documentation/metalperformanceshadersgraph/mpsgraphstencilopdescriptor/offsets)
- [var paddingConstant: Float](/documentation/metalperformanceshadersgraph/mpsgraphstencilopdescriptor/paddingconstant)
- [var paddingStyle: MPSGraphPaddingStyle](/documentation/metalperformanceshadersgraph/mpsgraphstencilopdescriptor/paddingstyle)
- [var reductionMode: MPSGraphReductionMode](/documentation/metalperformanceshadersgraph/mpsgraphstencilopdescriptor/reductionmode)
- [var strides: [NSNumber]](/documentation/metalperformanceshadersgraph/mpsgraphstencilopdescriptor/strides)
- [MPSGraphTensor](/documentation/metalperformanceshadersgraph/mpsgraphtensor)

### Instance Properties

- [var dataType: MPSDataType](/documentation/metalperformanceshadersgraph/mpsgraphtensor/datatype)
- [var operation: MPSGraphOperation](/documentation/metalperformanceshadersgraph/mpsgraphtensor/operation)
- [var shape: [NSNumber]?](/documentation/metalperformanceshadersgraph/mpsgraphtensor/shape)
- [MPSGraphTensorData](/documentation/metalperformanceshadersgraph/mpsgraphtensordata)

### Initializers

- [init(MPSMatrix)](/documentation/metalperformanceshadersgraph/mpsgraphtensordata/init(_:)-2go2)
- [init(MPSNDArray)](/documentation/metalperformanceshadersgraph/mpsgraphtensordata/init(_:)-4bnfb)
- [init([MPSImage])](/documentation/metalperformanceshadersgraph/mpsgraphtensordata/init(_:)-511a)
- [init(any MTLTensor)](/documentation/metalperformanceshadersgraph/mpsgraphtensordata/init(_:)-60j6x)
- [init(MPSVector)](/documentation/metalperformanceshadersgraph/mpsgraphtensordata/init(_:)-9kgoe)
- [init(MPSVector, rank: Int)](/documentation/metalperformanceshadersgraph/mpsgraphtensordata/init(_:rank:)-1e4ks)
- [init(MPSMatrix, rank: Int)](/documentation/metalperformanceshadersgraph/mpsgraphtensordata/init(_:rank:)-1lnxg)
- [init(any MTLBuffer, shape: [NSNumber], dataType: MPSDataType)](/documentation/metalperformanceshadersgraph/mpsgraphtensordata/init(_:shape:datatype:))
- [init(any MTLBuffer, shape: [NSNumber], dataType: MPSDataType, rowBytes: Int)](/documentation/metalperformanceshadersgraph/mpsgraphtensordata/init(_:shape:datatype:rowbytes:))
- [init(device: MPSGraphDevice, data: Data, shape: [NSNumber], dataType: MPSDataType)](/documentation/metalperformanceshadersgraph/mpsgraphtensordata/init(device:data:shape:datatype:))

### Instance Properties

- [var dataType: MPSDataType](/documentation/metalperformanceshadersgraph/mpsgraphtensordata/datatype)
- [var device: MPSGraphDevice](/documentation/metalperformanceshadersgraph/mpsgraphtensordata/device)
- [var shape: [NSNumber]](/documentation/metalperformanceshadersgraph/mpsgraphtensordata/shape)

### Instance Methods

- [func mpsndarray() -> MPSNDArray](/documentation/metalperformanceshadersgraph/mpsgraphtensordata/mpsndarray())
- [MPSGraphType](/documentation/metalperformanceshadersgraph/mpsgraphtype)
- [MPSGraphVariableOp](/documentation/metalperformanceshadersgraph/mpsgraphvariableop)

### Instance Properties

- [var dataType: MPSDataType](/documentation/metalperformanceshadersgraph/mpsgraphvariableop/datatype)
- [var shape: [NSNumber]](/documentation/metalperformanceshadersgraph/mpsgraphvariableop/shape)

## Structures

- [MPSGraphReducedPrecisionFastMath](/documentation/metalperformanceshadersgraph/mpsgraphreducedprecisionfastmath)

### Initializers

- [init(rawValue: UInt)](/documentation/metalperformanceshadersgraph/mpsgraphreducedprecisionfastmath/init(rawvalue:))

### Type Properties

- [static var allowFP16Conv2DWinogradTransformIntermediate: MPSGraphReducedPrecisionFastMath](/documentation/metalperformanceshadersgraph/mpsgraphreducedprecisionfastmath/allowfp16conv2dwinogradtransformintermediate)
- [static var allowFP16Intermediates: MPSGraphReducedPrecisionFastMath](/documentation/metalperformanceshadersgraph/mpsgraphreducedprecisionfastmath/allowfp16intermediates)
- [static var none: MPSGraphReducedPrecisionFastMath](/documentation/metalperformanceshadersgraph/mpsgraphreducedprecisionfastmath/none)

## Type Aliases

- [MPSGraphCompilationCompletionHandler](/documentation/metalperformanceshadersgraph/mpsgraphcompilationcompletionhandler)
- [MPSGraphCompletionHandler](/documentation/metalperformanceshadersgraph/mpsgraphcompletionhandler)
- [MPSGraphControlFlowDependencyBlock](/documentation/metalperformanceshadersgraph/mpsgraphcontrolflowdependencyblock)
- [MPSGraphExecutableCompletionHandler](/documentation/metalperformanceshadersgraph/mpsgraphexecutablecompletionhandler)
- [MPSGraphExecutableScheduledHandler](/documentation/metalperformanceshadersgraph/mpsgraphexecutablescheduledhandler)
- [MPSGraphForLoopBodyBlock](/documentation/metalperformanceshadersgraph/mpsgraphforloopbodyblock)
- [MPSGraphIfThenElseBlock](/documentation/metalperformanceshadersgraph/mpsgraphifthenelseblock)
- [MPSGraphScheduledHandler](/documentation/metalperformanceshadersgraph/mpsgraphscheduledhandler)
- [MPSGraphWhileAfterBlock](/documentation/metalperformanceshadersgraph/mpsgraphwhileafterblock)
- [MPSGraphWhileBeforeBlock](/documentation/metalperformanceshadersgraph/mpsgraphwhilebeforeblock)

## Enumerations

- [MPSGraphDeploymentPlatform](/documentation/metalperformanceshadersgraph/mpsgraphdeploymentplatform)

### Enumeration Cases

- [case iOS](/documentation/metalperformanceshadersgraph/mpsgraphdeploymentplatform/ios)
- [case macOS](/documentation/metalperformanceshadersgraph/mpsgraphdeploymentplatform/macos)
- [case tvOS](/documentation/metalperformanceshadersgraph/mpsgraphdeploymentplatform/tvos)
- [case visionOS](/documentation/metalperformanceshadersgraph/mpsgraphdeploymentplatform/visionos)

### Initializers

- [init?(rawValue: UInt64)](/documentation/metalperformanceshadersgraph/mpsgraphdeploymentplatform/init(rawvalue:))
- [MPSGraphDeviceType](/documentation/metalperformanceshadersgraph/mpsgraphdevicetype)

### Enumeration Cases

- [case metal](/documentation/metalperformanceshadersgraph/mpsgraphdevicetype/metal)

### Initializers

- [init?(rawValue: UInt32)](/documentation/metalperformanceshadersgraph/mpsgraphdevicetype/init(rawvalue:))
- [MPSGraphExecutionStage](/documentation/metalperformanceshadersgraph/mpsgraphexecutionstage)

### Enumeration Cases

- [case completed](/documentation/metalperformanceshadersgraph/mpsgraphexecutionstage/completed)

### Initializers

- [init?(rawValue: UInt64)](/documentation/metalperformanceshadersgraph/mpsgraphexecutionstage/init(rawvalue:))
- [MPSGraphFFTScalingMode](/documentation/metalperformanceshadersgraph/mpsgraphfftscalingmode)

### Enumeration Cases

- [case none](/documentation/metalperformanceshadersgraph/mpsgraphfftscalingmode/none)
- [case size](/documentation/metalperformanceshadersgraph/mpsgraphfftscalingmode/size)
- [case unitary](/documentation/metalperformanceshadersgraph/mpsgraphfftscalingmode/unitary)

### Initializers

- [init?(rawValue: UInt)](/documentation/metalperformanceshadersgraph/mpsgraphfftscalingmode/init(rawvalue:))
- [MPSGraphLossReductionType](/documentation/metalperformanceshadersgraph/mpsgraphlossreductiontype)

### Enumeration Cases

- [case mean](/documentation/metalperformanceshadersgraph/mpsgraphlossreductiontype/mean)
- [case none](/documentation/metalperformanceshadersgraph/mpsgraphlossreductiontype/none)
- [case sum](/documentation/metalperformanceshadersgraph/mpsgraphlossreductiontype/sum)

### Initializers

- [init?(rawValue: UInt64)](/documentation/metalperformanceshadersgraph/mpsgraphlossreductiontype/init(rawvalue:))

### Type Properties

- [static var axis: MPSGraphLossReductionType](/documentation/metalperformanceshadersgraph/mpsgraphlossreductiontype/axis)
- [MPSGraphNonMaximumSuppressionCoordinateMode](/documentation/metalperformanceshadersgraph/mpsgraphnonmaximumsuppressioncoordinatemode)

### Enumeration Cases

- [case centersHeightFirst](/documentation/metalperformanceshadersgraph/mpsgraphnonmaximumsuppressioncoordinatemode/centersheightfirst)
- [case centersWidthFirst](/documentation/metalperformanceshadersgraph/mpsgraphnonmaximumsuppressioncoordinatemode/centerswidthfirst)
- [case cornersWidthFirst](/documentation/metalperformanceshadersgraph/mpsgraphnonmaximumsuppressioncoordinatemode/cornerswidthfirst)
- [case explicit](/documentation/metalperformanceshadersgraph/mpsgraphnonmaximumsuppressioncoordinatemode/explicit)

### Initializers

- [init?(rawValue: UInt)](/documentation/metalperformanceshadersgraph/mpsgraphnonmaximumsuppressioncoordinatemode/init(rawvalue:))
- [MPSGraphOptimization](/documentation/metalperformanceshadersgraph/mpsgraphoptimization)

### Enumeration Cases

- [case level0](/documentation/metalperformanceshadersgraph/mpsgraphoptimization/level0)
- [case level1](/documentation/metalperformanceshadersgraph/mpsgraphoptimization/level1)

### Initializers

- [init?(rawValue: UInt64)](/documentation/metalperformanceshadersgraph/mpsgraphoptimization/init(rawvalue:))
- [MPSGraphOptimizationProfile](/documentation/metalperformanceshadersgraph/mpsgraphoptimizationprofile)

### Enumeration Cases

- [case performance](/documentation/metalperformanceshadersgraph/mpsgraphoptimizationprofile/performance)
- [case powerEfficiency](/documentation/metalperformanceshadersgraph/mpsgraphoptimizationprofile/powerefficiency)

### Initializers

- [init?(rawValue: UInt64)](/documentation/metalperformanceshadersgraph/mpsgraphoptimizationprofile/init(rawvalue:))
- [MPSGraphOptions](/documentation/metalperformanceshadersgraph/mpsgraphoptions)

### Enumeration Cases

- [case none](/documentation/metalperformanceshadersgraph/mpsgraphoptions/none)
- [case synchronizeResults](/documentation/metalperformanceshadersgraph/mpsgraphoptions/synchronizeresults)
- [case verbose](/documentation/metalperformanceshadersgraph/mpsgraphoptions/verbose)

### Initializers

- [init?(rawValue: UInt64)](/documentation/metalperformanceshadersgraph/mpsgraphoptions/init(rawvalue:))

### Type Properties

- [static var `default`: MPSGraphOptions](/documentation/metalperformanceshadersgraph/mpsgraphoptions/default)
- [MPSGraphPaddingMode](/documentation/metalperformanceshadersgraph/mpsgraphpaddingmode)

### Enumeration Cases

- [case antiPeriodic](/documentation/metalperformanceshadersgraph/mpsgraphpaddingmode/antiperiodic)
- [case clampToEdge](/documentation/metalperformanceshadersgraph/mpsgraphpaddingmode/clamptoedge)
- [case constant](/documentation/metalperformanceshadersgraph/mpsgraphpaddingmode/constant)
- [case periodic](/documentation/metalperformanceshadersgraph/mpsgraphpaddingmode/periodic)
- [case reflect](/documentation/metalperformanceshadersgraph/mpsgraphpaddingmode/reflect)
- [case symmetric](/documentation/metalperformanceshadersgraph/mpsgraphpaddingmode/symmetric)
- [case zero](/documentation/metalperformanceshadersgraph/mpsgraphpaddingmode/zero)

### Initializers

- [init?(rawValue: Int)](/documentation/metalperformanceshadersgraph/mpsgraphpaddingmode/init(rawvalue:))
- [MPSGraphPaddingStyle](/documentation/metalperformanceshadersgraph/mpsgraphpaddingstyle)

### Enumeration Cases

- [case ONNX_SAME_LOWER](/documentation/metalperformanceshadersgraph/mpsgraphpaddingstyle/onnx_same_lower)
- [case TF_SAME](/documentation/metalperformanceshadersgraph/mpsgraphpaddingstyle/tf_same)
- [case TF_VALID](/documentation/metalperformanceshadersgraph/mpsgraphpaddingstyle/tf_valid)
- [case explicit](/documentation/metalperformanceshadersgraph/mpsgraphpaddingstyle/explicit)
- [case explicitOffset](/documentation/metalperformanceshadersgraph/mpsgraphpaddingstyle/explicitoffset)

### Initializers

- [init?(rawValue: UInt)](/documentation/metalperformanceshadersgraph/mpsgraphpaddingstyle/init(rawvalue:))
- [MPSGraphPoolingReturnIndicesMode](/documentation/metalperformanceshadersgraph/mpsgraphpoolingreturnindicesmode)

### Enumeration Cases

- [case globalFlatten1D](/documentation/metalperformanceshadersgraph/mpsgraphpoolingreturnindicesmode/globalflatten1d)
- [case globalFlatten2D](/documentation/metalperformanceshadersgraph/mpsgraphpoolingreturnindicesmode/globalflatten2d)
- [case globalFlatten3D](/documentation/metalperformanceshadersgraph/mpsgraphpoolingreturnindicesmode/globalflatten3d)
- [case globalFlatten4D](/documentation/metalperformanceshadersgraph/mpsgraphpoolingreturnindicesmode/globalflatten4d)
- [case localFlatten1D](/documentation/metalperformanceshadersgraph/mpsgraphpoolingreturnindicesmode/localflatten1d)
- [case localFlatten2D](/documentation/metalperformanceshadersgraph/mpsgraphpoolingreturnindicesmode/localflatten2d)
- [case localFlatten3D](/documentation/metalperformanceshadersgraph/mpsgraphpoolingreturnindicesmode/localflatten3d)
- [case localFlatten4D](/documentation/metalperformanceshadersgraph/mpsgraphpoolingreturnindicesmode/localflatten4d)
- [case none](/documentation/metalperformanceshadersgraph/mpsgraphpoolingreturnindicesmode/none)

### Initializers

- [init?(rawValue: UInt)](/documentation/metalperformanceshadersgraph/mpsgraphpoolingreturnindicesmode/init(rawvalue:))
- [MPSGraphRNNActivation](/documentation/metalperformanceshadersgraph/mpsgraphrnnactivation)

### Enumeration Cases

- [case hardSigmoid](/documentation/metalperformanceshadersgraph/mpsgraphrnnactivation/hardsigmoid)
- [case none](/documentation/metalperformanceshadersgraph/mpsgraphrnnactivation/none)
- [case relu](/documentation/metalperformanceshadersgraph/mpsgraphrnnactivation/relu)
- [case sigmoid](/documentation/metalperformanceshadersgraph/mpsgraphrnnactivation/sigmoid)
- [case tanh](/documentation/metalperformanceshadersgraph/mpsgraphrnnactivation/tanh)

### Initializers

- [init?(rawValue: UInt)](/documentation/metalperformanceshadersgraph/mpsgraphrnnactivation/init(rawvalue:))
- [MPSGraphRandomDistribution](/documentation/metalperformanceshadersgraph/mpsgraphrandomdistribution)

### Enumeration Cases

- [case normal](/documentation/metalperformanceshadersgraph/mpsgraphrandomdistribution/normal)
- [case truncatedNormal](/documentation/metalperformanceshadersgraph/mpsgraphrandomdistribution/truncatednormal)
- [case uniform](/documentation/metalperformanceshadersgraph/mpsgraphrandomdistribution/uniform)

### Initializers

- [init?(rawValue: UInt64)](/documentation/metalperformanceshadersgraph/mpsgraphrandomdistribution/init(rawvalue:))
- [MPSGraphRandomNormalSamplingMethod](/documentation/metalperformanceshadersgraph/mpsgraphrandomnormalsamplingmethod)

### Enumeration Cases

- [case boxMuller](/documentation/metalperformanceshadersgraph/mpsgraphrandomnormalsamplingmethod/boxmuller)
- [case invCDF](/documentation/metalperformanceshadersgraph/mpsgraphrandomnormalsamplingmethod/invcdf)

### Initializers

- [init?(rawValue: UInt64)](/documentation/metalperformanceshadersgraph/mpsgraphrandomnormalsamplingmethod/init(rawvalue:))
- [MPSGraphReductionMode](/documentation/metalperformanceshadersgraph/mpsgraphreductionmode)

### Enumeration Cases

- [case argumentMax](/documentation/metalperformanceshadersgraph/mpsgraphreductionmode/argumentmax)
- [case argumentMin](/documentation/metalperformanceshadersgraph/mpsgraphreductionmode/argumentmin)
- [case max](/documentation/metalperformanceshadersgraph/mpsgraphreductionmode/max)
- [case min](/documentation/metalperformanceshadersgraph/mpsgraphreductionmode/min)
- [case product](/documentation/metalperformanceshadersgraph/mpsgraphreductionmode/product)
- [case sum](/documentation/metalperformanceshadersgraph/mpsgraphreductionmode/sum)

### Initializers

- [init?(rawValue: UInt)](/documentation/metalperformanceshadersgraph/mpsgraphreductionmode/init(rawvalue:))
- [MPSGraphResizeMode](/documentation/metalperformanceshadersgraph/mpsgraphresizemode)

### Enumeration Cases

- [case bilinear](/documentation/metalperformanceshadersgraph/mpsgraphresizemode/bilinear)
- [case nearest](/documentation/metalperformanceshadersgraph/mpsgraphresizemode/nearest)

### Initializers

- [init?(rawValue: UInt)](/documentation/metalperformanceshadersgraph/mpsgraphresizemode/init(rawvalue:))
- [MPSGraphResizeNearestRoundingMode](/documentation/metalperformanceshadersgraph/mpsgraphresizenearestroundingmode)

### Enumeration Cases

- [case ceil](/documentation/metalperformanceshadersgraph/mpsgraphresizenearestroundingmode/ceil)
- [case floor](/documentation/metalperformanceshadersgraph/mpsgraphresizenearestroundingmode/floor)
- [case roundPreferCeil](/documentation/metalperformanceshadersgraph/mpsgraphresizenearestroundingmode/roundpreferceil)
- [case roundPreferFloor](/documentation/metalperformanceshadersgraph/mpsgraphresizenearestroundingmode/roundpreferfloor)
- [case roundToEven](/documentation/metalperformanceshadersgraph/mpsgraphresizenearestroundingmode/roundtoeven)
- [case roundToOdd](/documentation/metalperformanceshadersgraph/mpsgraphresizenearestroundingmode/roundtoodd)

### Initializers

- [init?(rawValue: UInt)](/documentation/metalperformanceshadersgraph/mpsgraphresizenearestroundingmode/init(rawvalue:))
- [MPSGraphScatterMode](/documentation/metalperformanceshadersgraph/mpsgraphscattermode)

### Enumeration Cases

- [case add](/documentation/metalperformanceshadersgraph/mpsgraphscattermode/add)
- [case div](/documentation/metalperformanceshadersgraph/mpsgraphscattermode/div)
- [case max](/documentation/metalperformanceshadersgraph/mpsgraphscattermode/max)
- [case min](/documentation/metalperformanceshadersgraph/mpsgraphscattermode/min)
- [case mul](/documentation/metalperformanceshadersgraph/mpsgraphscattermode/mul)
- [case set](/documentation/metalperformanceshadersgraph/mpsgraphscattermode/set)
- [case sub](/documentation/metalperformanceshadersgraph/mpsgraphscattermode/sub)

### Initializers

- [init?(rawValue: Int)](/documentation/metalperformanceshadersgraph/mpsgraphscattermode/init(rawvalue:))
- [MPSGraphSparseStorageType](/documentation/metalperformanceshadersgraph/mpsgraphsparsestoragetype)

### Enumeration Cases

- [case COO](/documentation/metalperformanceshadersgraph/mpsgraphsparsestoragetype/coo)
- [case CSC](/documentation/metalperformanceshadersgraph/mpsgraphsparsestoragetype/csc)
- [case CSR](/documentation/metalperformanceshadersgraph/mpsgraphsparsestoragetype/csr)

### Initializers

- [init?(rawValue: UInt64)](/documentation/metalperformanceshadersgraph/mpsgraphsparsestoragetype/init(rawvalue:))
- [MPSGraphTensorNamedDataLayout](/documentation/metalperformanceshadersgraph/mpsgraphtensornameddatalayout)

### Enumeration Cases

- [case CHW](/documentation/metalperformanceshadersgraph/mpsgraphtensornameddatalayout/chw)
- [case DHWIO](/documentation/metalperformanceshadersgraph/mpsgraphtensornameddatalayout/dhwio)
- [case HW](/documentation/metalperformanceshadersgraph/mpsgraphtensornameddatalayout/hw)
- [case HWC](/documentation/metalperformanceshadersgraph/mpsgraphtensornameddatalayout/hwc)
- [case HWIO](/documentation/metalperformanceshadersgraph/mpsgraphtensornameddatalayout/hwio)
- [case NCDHW](/documentation/metalperformanceshadersgraph/mpsgraphtensornameddatalayout/ncdhw)
- [case NCHW](/documentation/metalperformanceshadersgraph/mpsgraphtensornameddatalayout/nchw)
- [case NDHWC](/documentation/metalperformanceshadersgraph/mpsgraphtensornameddatalayout/ndhwc)
- [case NHWC](/documentation/metalperformanceshadersgraph/mpsgraphtensornameddatalayout/nhwc)
- [case OIDHW](/documentation/metalperformanceshadersgraph/mpsgraphtensornameddatalayout/oidhw)
- [case OIHW](/documentation/metalperformanceshadersgraph/mpsgraphtensornameddatalayout/oihw)

### Initializers

- [init?(rawValue: UInt)](/documentation/metalperformanceshadersgraph/mpsgraphtensornameddatalayout/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
