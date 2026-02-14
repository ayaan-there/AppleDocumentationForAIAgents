# BrowserEngineCore Documentation

Source: https://sosumi.ai/documentation/browserenginecore

---
title: BrowserEngineCore
source: https://developer.apple.com/documentation/browserenginecore
timestamp: 2026-02-13T18:54:26.182Z
---

## Kernel events

- [func be_kevent(Int32, UnsafePointer<kevent>!, Int32, UnsafeMutablePointer<kevent>!, Int32, UInt32) -> Int32](/documentation/browserenginecore/be_kevent(_:_:_:_:_:_:))
- [func be_kevent64(Int32, UnsafePointer<kevent64_s>!, Int32, UnsafeMutablePointer<kevent64_s>!, Int32, UInt32) -> Int32](/documentation/browserenginecore/be_kevent64(_:_:_:_:_:_:))
- [var BE_KEVENT_NO_FLAGS: Int32](/documentation/browserenginecore/be_kevent_no_flags)
- [var BE_KEVENT_RETURN_IMMEDIATELY: Int32](/documentation/browserenginecore/be_kevent_return_immediately)

## JIT compilation

- [var BE_JIT_WRITE_PROTECT_TAG: Int](/documentation/browserenginecore/be_jit_write_protect_tag)

## Classes

- [BEAudioSession](/documentation/browserenginecore/beaudiosession-6b7ig)

### Initializers

- [init(audioSession: AVAudioSession)](/documentation/browserenginecore/beaudiosession-6b7ig/init(audiosession:))

### Instance Properties

- [var availableOutputs: [AVAudioSessionPortDescription]?](/documentation/browserenginecore/beaudiosession-6b7ig/availableoutputs)
- [var preferredOutput: AVAudioSessionPortDescription?](/documentation/browserenginecore/beaudiosession-6b7ig/preferredoutput)

### Instance Methods

- [func setPreferredOutput(AVAudioSessionPortDescription?) throws](/documentation/browserenginecore/beaudiosession-6b7ig/setpreferredoutput(_:))
- [BEAudioSession](/documentation/browserenginecore/beaudiosession-7bb2q)

### Initializers

- [init(audioSession: AVAudioSession)](/documentation/browserenginecore/beaudiosession-7bb2q/init(audiosession:))

### Instance Properties

- [var availableOutputs: Array<AVAudioSessionPortDescription>](/documentation/browserenginecore/beaudiosession-7bb2q/availableoutputs)
- [var preferredOutput: AVAudioSessionPortDescription?](/documentation/browserenginecore/beaudiosession-7bb2q/preferredoutput)

### Instance Methods

- [func setPreferredOutput(AVAudioSessionPortDescription?) throws](/documentation/browserenginecore/beaudiosession-7bb2q/setpreferredoutput(_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
