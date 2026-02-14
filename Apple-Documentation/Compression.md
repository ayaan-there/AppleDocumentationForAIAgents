# Compression Documentation

Source: https://sosumi.ai/documentation/compression

---
title: Compression
source: https://developer.apple.com/documentation/compression
timestamp: 2026-02-13T18:55:04.034Z
---

## Objects that simplify multiple-step compression

- [Compressing and decompressing data with input and output filters](/documentation/accelerate/compressing-and-decompressing-data-with-input-and-output-filters)
- [Compressing and decompressing files with stream compression](/documentation/accelerate/compressing-and-decompressing-files-with-stream-compression)
- [InputFilter](/documentation/compression/inputfilter)

### Initializers

- [init(FilterOperation, using: Algorithm, bufferCapacity: Int, readingFrom: (Int) throws -> D?) throws](/documentation/compression/inputfilter/init(_:using:buffercapacity:readingfrom:))

### Instance Methods

- [func readData(ofLength: Int) throws -> Data?](/documentation/compression/inputfilter/readdata(oflength:))
- [OutputFilter](/documentation/compression/outputfilter)

### Initializers

- [init(FilterOperation, using: Algorithm, bufferCapacity: Int, writingTo: (Data?) throws -> Void) throws](/documentation/compression/outputfilter/init(_:using:buffercapacity:writingto:))

### Instance Methods

- [func write<D>(D?) throws](/documentation/compression/outputfilter/write(_:))
- [func finalize() throws](/documentation/compression/outputfilter/finalize())
- [Algorithm](/documentation/compression/algorithm)

### Enumeration Cases

- [case brotli](/documentation/compression/algorithm/brotli)
- [case lz4](/documentation/compression/algorithm/lz4)
- [case lzbitmap](/documentation/compression/algorithm/lzbitmap)
- [case lzfse](/documentation/compression/algorithm/lzfse)
- [case lzma](/documentation/compression/algorithm/lzma)
- [case zlib](/documentation/compression/algorithm/zlib)
- [FilterError](/documentation/compression/filtererror)

### Enumeration Cases

- [case invalidData](/documentation/compression/filtererror/invaliddata)
- [case invalidState](/documentation/compression/filtererror/invalidstate)
- [FilterOperation](/documentation/compression/filteroperation)

### Enumeration Cases

- [case compress](/documentation/compression/filteroperation/compress)
- [case decompress](/documentation/compression/filteroperation/decompress)

## Multiple-step compression

- [compression_stream](/documentation/compression/compression_stream)

### Initializers

- [init(dst_ptr: UnsafeMutablePointer<UInt8>, dst_size: Int, src_ptr: UnsafePointer<UInt8>, src_size: Int, state: UnsafeMutableRawPointer?)](/documentation/compression/compression_stream/init(dst_ptr:dst_size:src_ptr:src_size:state:))

### Compression Stream Properties

- [var dst_ptr: UnsafeMutablePointer<UInt8>](/documentation/compression/compression_stream/dst_ptr)
- [var dst_size: Int](/documentation/compression/compression_stream/dst_size)
- [var src_ptr: UnsafePointer<UInt8>](/documentation/compression/compression_stream/src_ptr)
- [var src_size: Int](/documentation/compression/compression_stream/src_size)
- [var state: UnsafeMutableRawPointer?](/documentation/compression/compression_stream/state)
- [func compression_stream_init(UnsafeMutablePointer<compression_stream>, compression_stream_operation, compression_algorithm) -> compression_status](/documentation/compression/compression_stream_init(_:_:_:))
- [func compression_stream_process(UnsafeMutablePointer<compression_stream>, Int32) -> compression_status](/documentation/compression/compression_stream_process(_:_:))
- [func compression_stream_destroy(UnsafeMutablePointer<compression_stream>) -> compression_status](/documentation/compression/compression_stream_destroy(_:))
- [compression_status](/documentation/compression/compression_status)

### Status Constants

- [var COMPRESSION_STATUS_OK: compression_status](/documentation/compression/compression_status_ok)
- [var COMPRESSION_STATUS_END: compression_status](/documentation/compression/compression_status_end)
- [var COMPRESSION_STATUS_ERROR: compression_status](/documentation/compression/compression_status_error)

### Initializers

- [init(Int32)](/documentation/compression/compression_status/init(_:))
- [init(rawValue: Int32)](/documentation/compression/compression_status/init(rawvalue:))

### Instance Properties

- [var rawValue: Int32](/documentation/compression/compression_status/rawvalue)
- [compression_stream_flags](/documentation/compression/compression_stream_flags)

### Flag Constants

- [var COMPRESSION_STREAM_FINALIZE: compression_stream_flags](/documentation/compression/compression_stream_finalize)

### Initializers

- [init(UInt32)](/documentation/compression/compression_stream_flags/init(_:))
- [init(rawValue: UInt32)](/documentation/compression/compression_stream_flags/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/compression/compression_stream_flags/rawvalue)
- [compression_stream_operation](/documentation/compression/compression_stream_operation)

### Operation Constants

- [var COMPRESSION_STREAM_ENCODE: compression_stream_operation](/documentation/compression/compression_stream_encode)
- [var COMPRESSION_STREAM_DECODE: compression_stream_operation](/documentation/compression/compression_stream_decode)

### Initializers

- [init(UInt32)](/documentation/compression/compression_stream_operation/init(_:))
- [init(rawValue: UInt32)](/documentation/compression/compression_stream_operation/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/compression/compression_stream_operation/rawvalue)
- [compression_algorithm](/documentation/compression/compression_algorithm)

### Algorithm Constants

- [var COMPRESSION_LZFSE: compression_algorithm](/documentation/compression/compression_lzfse)
- [var COMPRESSION_LZ4: compression_algorithm](/documentation/compression/compression_lz4)
- [var COMPRESSION_LZ4_RAW: compression_algorithm](/documentation/compression/compression_lz4_raw)
- [var COMPRESSION_LZMA: compression_algorithm](/documentation/compression/compression_lzma)
- [var COMPRESSION_ZLIB: compression_algorithm](/documentation/compression/compression_zlib)
- [var COMPRESSION_BROTLI: compression_algorithm](/documentation/compression/compression_brotli)
- [var COMPRESSION_LZBITMAP: compression_algorithm](/documentation/compression/compression_lzbitmap)

### Initializers

- [init(UInt32)](/documentation/compression/compression_algorithm/init(_:))
- [init(rawValue: UInt32)](/documentation/compression/compression_algorithm/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/compression/compression_algorithm/rawvalue)

## Single-step compression

- [Compressing and decompressing data with buffer compression](/documentation/accelerate/compressing-and-decompressing-data-with-buffer-compression)
- [func compression_encode_scratch_buffer_size(compression_algorithm) -> Int](/documentation/compression/compression_encode_scratch_buffer_size(_:))
- [func compression_encode_buffer(UnsafeMutablePointer<UInt8>, Int, UnsafePointer<UInt8>, Int, UnsafeMutableRawPointer?, compression_algorithm) -> Int](/documentation/compression/compression_encode_buffer(_:_:_:_:_:_:))
- [func compression_decode_scratch_buffer_size(compression_algorithm) -> Int](/documentation/compression/compression_decode_scratch_buffer_size(_:))
- [func compression_decode_buffer(UnsafeMutablePointer<UInt8>, Int, UnsafePointer<UInt8>, Int, UnsafeMutableRawPointer?, compression_algorithm) -> Int](/documentation/compression/compression_decode_buffer(_:_:_:_:_:_:))
- [compression_algorithm](/documentation/compression/compression_algorithm)

### Algorithm Constants

- [var COMPRESSION_LZFSE: compression_algorithm](/documentation/compression/compression_lzfse)
- [var COMPRESSION_LZ4: compression_algorithm](/documentation/compression/compression_lz4)
- [var COMPRESSION_LZ4_RAW: compression_algorithm](/documentation/compression/compression_lz4_raw)
- [var COMPRESSION_LZMA: compression_algorithm](/documentation/compression/compression_lzma)
- [var COMPRESSION_ZLIB: compression_algorithm](/documentation/compression/compression_zlib)
- [var COMPRESSION_BROTLI: compression_algorithm](/documentation/compression/compression_brotli)
- [var COMPRESSION_LZBITMAP: compression_algorithm](/documentation/compression/compression_lzbitmap)

### Initializers

- [init(UInt32)](/documentation/compression/compression_algorithm/init(_:))
- [init(rawValue: UInt32)](/documentation/compression/compression_algorithm/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/compression/compression_algorithm/rawvalue)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
