# Force Feedback Documentation

Source: https://sosumi.ai/documentation/forcefeedback

---
title: Force Feedback
source: https://developer.apple.com/documentation/forcefeedback
timestamp: 2026-02-13T18:57:08.936Z
---

## Reference

- [ForceFeedback.h](/documentation/forcefeedback/forcefeedback-h)

### Miscellaneous

- [func FFCreateDevice(io_service_t, UnsafeMutablePointer<FFDeviceObjectReference?>!) -> HRESULT](/documentation/forcefeedback/ffcreatedevice(_:_:))
- [func FFDeviceCreateEffect(FFDeviceObjectReference!, CFUUID!, UnsafeMutablePointer<FFEFFECT>!, UnsafeMutablePointer<FFEffectObjectReference?>!) -> HRESULT](/documentation/forcefeedback/ffdevicecreateeffect(_:_:_:_:))
- [func FFDeviceEscape(FFDeviceObjectReference!, UnsafeMutablePointer<FFEFFESCAPE>!) -> HRESULT](/documentation/forcefeedback/ffdeviceescape(_:_:))
- [func FFDeviceGetForceFeedbackCapabilities(FFDeviceObjectReference!, UnsafeMutablePointer<FFCAPABILITIES>!) -> HRESULT](/documentation/forcefeedback/ffdevicegetforcefeedbackcapabilities(_:_:))
- [func FFDeviceGetForceFeedbackProperty(FFDeviceObjectReference!, FFProperty, UnsafeMutableRawPointer!, IOByteCount) -> HRESULT](/documentation/forcefeedback/ffdevicegetforcefeedbackproperty(_:_:_:_:))
- [func FFDeviceGetForceFeedbackState(FFDeviceObjectReference!, UnsafeMutablePointer<FFState>!) -> HRESULT](/documentation/forcefeedback/ffdevicegetforcefeedbackstate(_:_:))
- [func FFDeviceReleaseEffect(FFDeviceObjectReference!, FFEffectObjectReference!) -> HRESULT](/documentation/forcefeedback/ffdevicereleaseeffect(_:_:))
- [func FFDeviceSendForceFeedbackCommand(FFDeviceObjectReference!, FFCommandFlag) -> HRESULT](/documentation/forcefeedback/ffdevicesendforcefeedbackcommand(_:_:))
- [func FFDeviceSetCooperativeLevel(FFDeviceObjectReference!, UnsafeMutableRawPointer!, FFCooperativeLevelFlag) -> HRESULT](/documentation/forcefeedback/ffdevicesetcooperativelevel(_:_:_:))
- [func FFDeviceSetForceFeedbackProperty(FFDeviceObjectReference!, FFProperty, UnsafeMutableRawPointer!) -> HRESULT](/documentation/forcefeedback/ffdevicesetforcefeedbackproperty(_:_:_:))
- [func FFEffectDownload(FFEffectObjectReference!) -> HRESULT](/documentation/forcefeedback/ffeffectdownload(_:))
- [func FFEffectEscape(FFEffectObjectReference!, UnsafeMutablePointer<FFEFFESCAPE>!) -> HRESULT](/documentation/forcefeedback/ffeffectescape(_:_:))
- [func FFEffectGetEffectStatus(FFEffectObjectReference!, UnsafeMutablePointer<FFEffectStatusFlag>!) -> HRESULT](/documentation/forcefeedback/ffeffectgeteffectstatus(_:_:))
- [func FFEffectGetParameters(FFEffectObjectReference!, UnsafeMutablePointer<FFEFFECT>!, FFEffectParameterFlag) -> HRESULT](/documentation/forcefeedback/ffeffectgetparameters(_:_:_:))
- [func FFEffectSetParameters(FFEffectObjectReference!, UnsafeMutablePointer<FFEFFECT>!, FFEffectParameterFlag) -> HRESULT](/documentation/forcefeedback/ffeffectsetparameters(_:_:_:))
- [func FFEffectStart(FFEffectObjectReference!, UInt32, FFEffectStartFlag) -> HRESULT](/documentation/forcefeedback/ffeffectstart(_:_:_:))
- [func FFEffectStop(FFEffectObjectReference!) -> HRESULT](/documentation/forcefeedback/ffeffectstop(_:))
- [func FFEffectUnload(FFEffectObjectReference!) -> HRESULT](/documentation/forcefeedback/ffeffectunload(_:))
- [func FFIsForceFeedback(io_service_t) -> HRESULT](/documentation/forcefeedback/ffisforcefeedback(_:))
- [func FFReleaseDevice(FFDeviceObjectReference!) -> HRESULT](/documentation/forcefeedback/ffreleasedevice(_:))

### Data Types

- [FFCAPABILITIES](/documentation/forcefeedback/ffcapabilities)

#### Initializers

- [init()](/documentation/forcefeedback/ffcapabilities/init())
- [init(ffSpecVer: NumVersion, supportedEffects: UInt32, emulatedEffects: UInt32, subType: UInt32, numFfAxes: UInt32, ffAxes: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8), storageCapacity: UInt32, playbackCapacity: UInt32, firmwareVer: NumVersion, hardwareVer: NumVersion, driverVer: NumVersion)](/documentation/forcefeedback/ffcapabilities/init(ffspecver:supportedeffects:emulatedeffects:subtype:numffaxes:ffaxes:storagecapacity:playbackcapacity:firmwarever:hardwarever:driverver:))

#### Instance Properties

- [var driverVer: NumVersion](/documentation/forcefeedback/ffcapabilities/driverver)
- [var emulatedEffects: UInt32](/documentation/forcefeedback/ffcapabilities/emulatedeffects)
- [var ffAxes: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/forcefeedback/ffcapabilities/ffaxes)
- [var ffSpecVer: NumVersion](/documentation/forcefeedback/ffcapabilities/ffspecver)
- [var firmwareVer: NumVersion](/documentation/forcefeedback/ffcapabilities/firmwarever)
- [var hardwareVer: NumVersion](/documentation/forcefeedback/ffcapabilities/hardwarever)
- [var numFfAxes: UInt32](/documentation/forcefeedback/ffcapabilities/numffaxes)
- [var playbackCapacity: UInt32](/documentation/forcefeedback/ffcapabilities/playbackcapacity)
- [var storageCapacity: UInt32](/documentation/forcefeedback/ffcapabilities/storagecapacity)
- [var subType: UInt32](/documentation/forcefeedback/ffcapabilities/subtype)
- [var supportedEffects: UInt32](/documentation/forcefeedback/ffcapabilities/supportedeffects)
- [FFCONDITION](/documentation/forcefeedback/ffcondition)

#### Initializers

- [init()](/documentation/forcefeedback/ffcondition/init())
- [init(lOffset: LONG, lPositiveCoefficient: LONG, lNegativeCoefficient: LONG, dwPositiveSaturation: DWORD, dwNegativeSaturation: DWORD, lDeadBand: LONG)](/documentation/forcefeedback/ffcondition/init(loffset:lpositivecoefficient:lnegativecoefficient:dwpositivesaturation:dwnegativesaturation:ldeadband:))

#### Instance Properties

- [var dwNegativeSaturation: DWORD](/documentation/forcefeedback/ffcondition/dwnegativesaturation)
- [var dwPositiveSaturation: DWORD](/documentation/forcefeedback/ffcondition/dwpositivesaturation)
- [var lDeadBand: LONG](/documentation/forcefeedback/ffcondition/ldeadband)
- [var lNegativeCoefficient: LONG](/documentation/forcefeedback/ffcondition/lnegativecoefficient)
- [var lOffset: LONG](/documentation/forcefeedback/ffcondition/loffset)
- [var lPositiveCoefficient: LONG](/documentation/forcefeedback/ffcondition/lpositivecoefficient)
- [FFCONSTANTFORCE](/documentation/forcefeedback/ffconstantforce)

#### Initializers

- [init()](/documentation/forcefeedback/ffconstantforce/init())
- [init(lMagnitude: LONG)](/documentation/forcefeedback/ffconstantforce/init(lmagnitude:))

#### Instance Properties

- [var lMagnitude: LONG](/documentation/forcefeedback/ffconstantforce/lmagnitude)
- [FFCUSTOMFORCE](/documentation/forcefeedback/ffcustomforce)

#### Initializers

- [init()](/documentation/forcefeedback/ffcustomforce/init())
- [init(cChannels: DWORD, dwSamplePeriod: DWORD, cSamples: DWORD, rglForceData: LPLONG!)](/documentation/forcefeedback/ffcustomforce/init(cchannels:dwsampleperiod:csamples:rglforcedata:))

#### Instance Properties

- [var cChannels: DWORD](/documentation/forcefeedback/ffcustomforce/cchannels)
- [var cSamples: DWORD](/documentation/forcefeedback/ffcustomforce/csamples)
- [var dwSamplePeriod: DWORD](/documentation/forcefeedback/ffcustomforce/dwsampleperiod)
- [var rglForceData: LPLONG!](/documentation/forcefeedback/ffcustomforce/rglforcedata)
- [FFEFFECT](/documentation/forcefeedback/ffeffect)

#### Initializers

- [init()](/documentation/forcefeedback/ffeffect/init())
- [init(dwSize: DWORD, dwFlags: DWORD, dwDuration: DWORD, dwSamplePeriod: DWORD, dwGain: DWORD, dwTriggerButton: DWORD, dwTriggerRepeatInterval: DWORD, cAxes: DWORD, rgdwAxes: LPDWORD!, rglDirection: LPLONG!, lpEnvelope: PFFENVELOPE!, cbTypeSpecificParams: DWORD, lpvTypeSpecificParams: UnsafeMutableRawPointer!, dwStartDelay: DWORD)](/documentation/forcefeedback/ffeffect/init(dwsize:dwflags:dwduration:dwsampleperiod:dwgain:dwtriggerbutton:dwtriggerrepeatinterval:caxes:rgdwaxes:rgldirection:lpenvelope:cbtypespecificparams:lpvtypespecificparams:dwstartdelay:))

#### Instance Properties

- [var cAxes: DWORD](/documentation/forcefeedback/ffeffect/caxes)
- [var cbTypeSpecificParams: DWORD](/documentation/forcefeedback/ffeffect/cbtypespecificparams)
- [var dwDuration: DWORD](/documentation/forcefeedback/ffeffect/dwduration)
- [var dwFlags: DWORD](/documentation/forcefeedback/ffeffect/dwflags)
- [var dwGain: DWORD](/documentation/forcefeedback/ffeffect/dwgain)
- [var dwSamplePeriod: DWORD](/documentation/forcefeedback/ffeffect/dwsampleperiod)
- [var dwSize: DWORD](/documentation/forcefeedback/ffeffect/dwsize)
- [var dwStartDelay: DWORD](/documentation/forcefeedback/ffeffect/dwstartdelay)
- [var dwTriggerButton: DWORD](/documentation/forcefeedback/ffeffect/dwtriggerbutton)
- [var dwTriggerRepeatInterval: DWORD](/documentation/forcefeedback/ffeffect/dwtriggerrepeatinterval)
- [var lpEnvelope: PFFENVELOPE!](/documentation/forcefeedback/ffeffect/lpenvelope)
- [var lpvTypeSpecificParams: UnsafeMutableRawPointer!](/documentation/forcefeedback/ffeffect/lpvtypespecificparams)
- [var rgdwAxes: LPDWORD!](/documentation/forcefeedback/ffeffect/rgdwaxes)
- [var rglDirection: LPLONG!](/documentation/forcefeedback/ffeffect/rgldirection)
- [FFEFFESCAPE](/documentation/forcefeedback/ffeffescape)

#### Initializers

- [init()](/documentation/forcefeedback/ffeffescape/init())
- [init(dwSize: DWORD, dwCommand: DWORD, lpvInBuffer: UnsafeMutableRawPointer!, cbInBuffer: DWORD, lpvOutBuffer: UnsafeMutableRawPointer!, cbOutBuffer: DWORD)](/documentation/forcefeedback/ffeffescape/init(dwsize:dwcommand:lpvinbuffer:cbinbuffer:lpvoutbuffer:cboutbuffer:))

#### Instance Properties

- [var cbInBuffer: DWORD](/documentation/forcefeedback/ffeffescape/cbinbuffer)
- [var cbOutBuffer: DWORD](/documentation/forcefeedback/ffeffescape/cboutbuffer)
- [var dwCommand: DWORD](/documentation/forcefeedback/ffeffescape/dwcommand)
- [var dwSize: DWORD](/documentation/forcefeedback/ffeffescape/dwsize)
- [var lpvInBuffer: UnsafeMutableRawPointer!](/documentation/forcefeedback/ffeffescape/lpvinbuffer)
- [var lpvOutBuffer: UnsafeMutableRawPointer!](/documentation/forcefeedback/ffeffescape/lpvoutbuffer)
- [FFENVELOPE](/documentation/forcefeedback/ffenvelope)

#### Initializers

- [init()](/documentation/forcefeedback/ffenvelope/init())
- [init(dwSize: DWORD, dwAttackLevel: DWORD, dwAttackTime: DWORD, dwFadeLevel: DWORD, dwFadeTime: DWORD)](/documentation/forcefeedback/ffenvelope/init(dwsize:dwattacklevel:dwattacktime:dwfadelevel:dwfadetime:))

#### Instance Properties

- [var dwAttackLevel: DWORD](/documentation/forcefeedback/ffenvelope/dwattacklevel)
- [var dwAttackTime: DWORD](/documentation/forcefeedback/ffenvelope/dwattacktime)
- [var dwFadeLevel: DWORD](/documentation/forcefeedback/ffenvelope/dwfadelevel)
- [var dwFadeTime: DWORD](/documentation/forcefeedback/ffenvelope/dwfadetime)
- [var dwSize: DWORD](/documentation/forcefeedback/ffenvelope/dwsize)
- [FFPERIODIC](/documentation/forcefeedback/ffperiodic)

#### Initializers

- [init()](/documentation/forcefeedback/ffperiodic/init())
- [init(dwMagnitude: DWORD, lOffset: LONG, dwPhase: DWORD, dwPeriod: DWORD)](/documentation/forcefeedback/ffperiodic/init(dwmagnitude:loffset:dwphase:dwperiod:))

#### Instance Properties

- [var dwMagnitude: DWORD](/documentation/forcefeedback/ffperiodic/dwmagnitude)
- [var dwPeriod: DWORD](/documentation/forcefeedback/ffperiodic/dwperiod)
- [var dwPhase: DWORD](/documentation/forcefeedback/ffperiodic/dwphase)
- [var lOffset: LONG](/documentation/forcefeedback/ffperiodic/loffset)
- [FFRAMPFORCE](/documentation/forcefeedback/fframpforce)

#### Initializers

- [init()](/documentation/forcefeedback/fframpforce/init())
- [init(lStart: LONG, lEnd: LONG)](/documentation/forcefeedback/fframpforce/init(lstart:lend:))

#### Instance Properties

- [var lEnd: LONG](/documentation/forcefeedback/fframpforce/lend)
- [var lStart: LONG](/documentation/forcefeedback/fframpforce/lstart)
- [ForceFeedbackConstants.h](/documentation/forcefeedback/forcefeedbackconstants-h)

### Constants

- [Miscellaneous Defines](/documentation/forcefeedback/miscellaneous-defines)

#### Constants

- [var E_PENDING: Int](/documentation/forcefeedback/e_pending)
- [var FF_DEGREES: Int32](/documentation/forcefeedback/ff_degrees)
- [var FF_DOWNLOADSKIPPED: HRESULT](/documentation/forcefeedback/ff_downloadskipped)
- [var FF_EFFECTRESTARTED: HRESULT](/documentation/forcefeedback/ff_effectrestarted)
- [var FF_FALSE: HRESULT](/documentation/forcefeedback/ff_false)
- [var FF_FFNOMINALMAX: Int32](/documentation/forcefeedback/ff_ffnominalmax)
- [var FF_INFINITE: UInt](/documentation/forcefeedback/ff_infinite)
- [var FF_OK: HRESULT](/documentation/forcefeedback/ff_ok)
- [var FF_SECONDS: Int32](/documentation/forcefeedback/ff_seconds)
- [var FF_TRUNCATED: HRESULT](/documentation/forcefeedback/ff_truncated)
- [var FF_TRUNCATEDANDRESTARTED: HRESULT](/documentation/forcefeedback/ff_truncatedandrestarted)
- [var FFEFF_OBJECTOFFSETS: UInt](/documentation/forcefeedback/ffeff_objectoffsets)
- [var FFERR_DEVICEFULL: Int](/documentation/forcefeedback/fferr_devicefull)
- [var FFERR_DEVICEPAUSED: Int](/documentation/forcefeedback/fferr_devicepaused)
- [var FFERR_DEVICERELEASED: Int](/documentation/forcefeedback/fferr_devicereleased)
- [var FFERR_EFFECTPLAYING: Int](/documentation/forcefeedback/fferr_effectplaying)
- [var FFERR_EFFECTTYPEMISMATCH: Int](/documentation/forcefeedback/fferr_effecttypemismatch)
- [var FFERR_EFFECTTYPENOTSUPPORTED: Int](/documentation/forcefeedback/fferr_effecttypenotsupported)
- [var FFERR_GENERIC: HRESULT](/documentation/forcefeedback/fferr_generic)
- [var FFERR_HASEFFECTS: Int](/documentation/forcefeedback/fferr_haseffects)
- [var FFERR_INCOMPLETEEFFECT: Int](/documentation/forcefeedback/fferr_incompleteeffect)
- [var FFERR_INTERNAL: Int](/documentation/forcefeedback/fferr_internal)
- [var FFERR_INVALIDDOWNLOADID: Int](/documentation/forcefeedback/fferr_invaliddownloadid)
- [var FFERR_INVALIDPARAM: HRESULT](/documentation/forcefeedback/fferr_invalidparam)
- [var FFERR_MOREDATA: Int](/documentation/forcefeedback/fferr_moredata)
- [var FFERR_NOINTERFACE: HRESULT](/documentation/forcefeedback/fferr_nointerface)
- [var FFERR_NOTDOWNLOADED: Int](/documentation/forcefeedback/fferr_notdownloaded)
- [var FFERR_NOTINITIALIZED: Int](/documentation/forcefeedback/fferr_notinitialized)
- [var FFERR_OUTOFMEMORY: HRESULT](/documentation/forcefeedback/fferr_outofmemory)
- [var FFERR_UNPLUGGED: Int](/documentation/forcefeedback/fferr_unplugged)
- [var FFERR_UNSUPPORTED: HRESULT](/documentation/forcefeedback/fferr_unsupported)
- [var FFERR_UNSUPPORTEDAXIS: Int](/documentation/forcefeedback/fferr_unsupportedaxis)
- [FFJOFS_<i>i</i>](/documentation/forcefeedback/ffjofs_i_i_i)
- [var FFJOFS_X: Int32](/documentation/forcefeedback/ffjofs_x)
- [FFCapabilitiesEffectSubType](/documentation/forcefeedback/ffcapabilitieseffectsubtype)
- [FFCapabilitiesEffectType](/documentation/forcefeedback/ffcapabilitieseffecttype)

#### Constants

- [var FFCAP_ET_CONSTANTFORCE: Int](/documentation/forcefeedback/ffcap_et_constantforce)
- [var FFCAP_ET_RAMPFORCE: Int](/documentation/forcefeedback/ffcap_et_rampforce)
- [var FFCAP_ET_SQUARE: Int](/documentation/forcefeedback/ffcap_et_square)
- [var FFCAP_ET_SINE: Int](/documentation/forcefeedback/ffcap_et_sine)
- [var FFCAP_ET_TRIANGLE: Int](/documentation/forcefeedback/ffcap_et_triangle)
- [var FFCAP_ET_SAWTOOTHUP: Int](/documentation/forcefeedback/ffcap_et_sawtoothup)
- [var FFCAP_ET_SAWTOOTHDOWN: Int](/documentation/forcefeedback/ffcap_et_sawtoothdown)
- [var FFCAP_ET_SPRING: Int](/documentation/forcefeedback/ffcap_et_spring)
- [var FFCAP_ET_DAMPER: Int](/documentation/forcefeedback/ffcap_et_damper)
- [var FFCAP_ET_INERTIA: Int](/documentation/forcefeedback/ffcap_et_inertia)
- [var FFCAP_ET_FRICTION: Int](/documentation/forcefeedback/ffcap_et_friction)
- [var FFCAP_ET_CUSTOMFORCE: Int](/documentation/forcefeedback/ffcap_et_customforce)
- [FFCommandFlag](/documentation/forcefeedback/ffcommandflag)
- [FFCooperativeLevelFlag](/documentation/forcefeedback/ffcooperativelevelflag)
- [FFCoordinateSystemFlag](/documentation/forcefeedback/ffcoordinatesystemflag)

#### Constants

- [var FFEFF_CARTESIAN: Int](/documentation/forcefeedback/ffeff_cartesian)
- [var FFEFF_POLAR: Int](/documentation/forcefeedback/ffeff_polar)
- [var FFEFF_SPHERICAL: Int](/documentation/forcefeedback/ffeff_spherical)
- [FFEffectParameterFlag](/documentation/forcefeedback/ffeffectparameterflag)
- [FFEffectStartFlag](/documentation/forcefeedback/ffeffectstartflag)
- [FFEffectStatusFlag](/documentation/forcefeedback/ffeffectstatusflag)
- [FFProperty](/documentation/forcefeedback/ffproperty)
- [FFState](/documentation/forcefeedback/ffstate)
- [ForceFeedback Enumerations](/documentation/forcefeedback/forcefeedback-enumerations)

### Enumerations

- [Anonymous](/documentation/forcefeedback/forcefeedback-enumerations-1524471-anonymous)

#### Constants

- [var FFGFFS_ACTUATORSOFF: UInt32](/documentation/forcefeedback/ffgffs_actuatorsoff)
- [var FFGFFS_ACTUATORSON: UInt32](/documentation/forcefeedback/ffgffs_actuatorson)
- [var FFGFFS_DEVICELOST: UInt32](/documentation/forcefeedback/ffgffs_devicelost)
- [var FFGFFS_EMPTY: UInt32](/documentation/forcefeedback/ffgffs_empty)
- [var FFGFFS_PAUSED: UInt32](/documentation/forcefeedback/ffgffs_paused)
- [var FFGFFS_POWEROFF: UInt32](/documentation/forcefeedback/ffgffs_poweroff)
- [var FFGFFS_POWERON: UInt32](/documentation/forcefeedback/ffgffs_poweron)
- [var FFGFFS_SAFETYSWITCHOFF: UInt32](/documentation/forcefeedback/ffgffs_safetyswitchoff)
- [var FFGFFS_SAFETYSWITCHON: UInt32](/documentation/forcefeedback/ffgffs_safetyswitchon)
- [var FFGFFS_STOPPED: UInt32](/documentation/forcefeedback/ffgffs_stopped)
- [var FFGFFS_USERFFSWITCHOFF: UInt32](/documentation/forcefeedback/ffgffs_userffswitchoff)
- [var FFGFFS_USERFFSWITCHON: UInt32](/documentation/forcefeedback/ffgffs_userffswitchon)
- [Anonymous](/documentation/forcefeedback/forcefeedback-enumerations-1524584-anonymous)

#### Constants

- [var FFEFF_CARTESIAN: Int](/documentation/forcefeedback/ffeff_cartesian)
- [var FFEFF_POLAR: Int](/documentation/forcefeedback/ffeff_polar)
- [var FFEFF_SPHERICAL: Int](/documentation/forcefeedback/ffeff_spherical)
- [Anonymous](/documentation/forcefeedback/forcefeedback-enumerations-1524526-anonymous)

#### Constants

- [var FFSCL_BACKGROUND: Int](/documentation/forcefeedback/ffscl_background)
- [var FFSCL_EXCLUSIVE: Int](/documentation/forcefeedback/ffscl_exclusive)
- [var FFSCL_FOREGROUND: Int](/documentation/forcefeedback/ffscl_foreground)
- [var FFSCL_NONEXCLUSIVE: Int](/documentation/forcefeedback/ffscl_nonexclusive)
- [Anonymous](/documentation/forcefeedback/forcefeedback-enumerations-1524546-anonymous)

#### Constants

- [var FFPROP_AUTOCENTER: Int](/documentation/forcefeedback/ffprop_autocenter)
- [var FFPROP_FFGAIN: Int](/documentation/forcefeedback/ffprop_ffgain)
- [Anonymous](/documentation/forcefeedback/forcefeedback-enumerations-1524506-anonymous)

#### Constants

- [var FFSFFC_CONTINUE: Int](/documentation/forcefeedback/ffsffc_continue)
- [var FFSFFC_PAUSE: Int](/documentation/forcefeedback/ffsffc_pause)
- [var FFSFFC_RESET: Int](/documentation/forcefeedback/ffsffc_reset)
- [var FFSFFC_SETACTUATORSOFF: Int](/documentation/forcefeedback/ffsffc_setactuatorsoff)
- [var FFSFFC_SETACTUATORSON: Int](/documentation/forcefeedback/ffsffc_setactuatorson)
- [var FFSFFC_STOPALL: Int](/documentation/forcefeedback/ffsffc_stopall)
- [Anonymous](/documentation/forcefeedback/forcefeedback-enumerations-1524537-anonymous)

#### Constants

- [var FFCAP_ET_CONSTANTFORCE: Int](/documentation/forcefeedback/ffcap_et_constantforce)
- [var FFCAP_ET_CUSTOMFORCE: Int](/documentation/forcefeedback/ffcap_et_customforce)
- [var FFCAP_ET_DAMPER: Int](/documentation/forcefeedback/ffcap_et_damper)
- [var FFCAP_ET_FRICTION: Int](/documentation/forcefeedback/ffcap_et_friction)
- [var FFCAP_ET_INERTIA: Int](/documentation/forcefeedback/ffcap_et_inertia)
- [var FFCAP_ET_RAMPFORCE: Int](/documentation/forcefeedback/ffcap_et_rampforce)
- [var FFCAP_ET_SAWTOOTHDOWN: Int](/documentation/forcefeedback/ffcap_et_sawtoothdown)
- [var FFCAP_ET_SAWTOOTHUP: Int](/documentation/forcefeedback/ffcap_et_sawtoothup)
- [var FFCAP_ET_SINE: Int](/documentation/forcefeedback/ffcap_et_sine)
- [var FFCAP_ET_SPRING: Int](/documentation/forcefeedback/ffcap_et_spring)
- [var FFCAP_ET_SQUARE: Int](/documentation/forcefeedback/ffcap_et_square)
- [var FFCAP_ET_TRIANGLE: Int](/documentation/forcefeedback/ffcap_et_triangle)
- [Anonymous](/documentation/forcefeedback/forcefeedback-enumerations-1524522-anonymous)

#### Constants

- [var FFES_NODOWNLOAD: UInt32](/documentation/forcefeedback/ffes_nodownload)
- [var FFES_SOLO: UInt32](/documentation/forcefeedback/ffes_solo)
- [Anonymous](/documentation/forcefeedback/forcefeedback-enumerations-1524566-anonymous)

#### Constants

- [var FFEGES_EMULATED: Int](/documentation/forcefeedback/ffeges_emulated)
- [var FFEGES_NOTPLAYING: Int](/documentation/forcefeedback/ffeges_notplaying)
- [var FFEGES_PLAYING: Int](/documentation/forcefeedback/ffeges_playing)
- [Anonymous](/documentation/forcefeedback/forcefeedback-enumerations-1524447-anonymous)

#### Constants

- [var FFCAP_ST_KINESTHETIC: Int](/documentation/forcefeedback/ffcap_st_kinesthetic)
- [var FFCAP_ST_VIBRATION: Int](/documentation/forcefeedback/ffcap_st_vibration)
- [Anonymous](/documentation/forcefeedback/forcefeedback-enumerations-1524560-anonymous)

#### Constants

- [var FFEB_NOTRIGGER: UInt32](/documentation/forcefeedback/ffeb_notrigger)
- [var FFEP_ALLPARAMS: UInt32](/documentation/forcefeedback/ffep_allparams)
- [var FFEP_AXES: UInt32](/documentation/forcefeedback/ffep_axes)
- [var FFEP_DIRECTION: UInt32](/documentation/forcefeedback/ffep_direction)
- [var FFEP_DURATION: UInt32](/documentation/forcefeedback/ffep_duration)
- [var FFEP_ENVELOPE: UInt32](/documentation/forcefeedback/ffep_envelope)
- [var FFEP_GAIN: UInt32](/documentation/forcefeedback/ffep_gain)
- [var FFEP_NODOWNLOAD: UInt32](/documentation/forcefeedback/ffep_nodownload)
- [var FFEP_NORESTART: UInt32](/documentation/forcefeedback/ffep_norestart)
- [var FFEP_SAMPLEPERIOD: UInt32](/documentation/forcefeedback/ffep_sampleperiod)
- [var FFEP_START: UInt32](/documentation/forcefeedback/ffep_start)
- [var FFEP_STARTDELAY: UInt32](/documentation/forcefeedback/ffep_startdelay)
- [var FFEP_TRIGGERBUTTON: UInt32](/documentation/forcefeedback/ffep_triggerbutton)
- [var FFEP_TRIGGERREPEATINTERVAL: UInt32](/documentation/forcefeedback/ffep_triggerrepeatinterval)
- [var FFEP_TYPESPECIFICPARAMS: UInt32](/documentation/forcefeedback/ffep_typespecificparams)
- [ForceFeedback Constants](/documentation/forcefeedback/forcefeedback-constants)

### Constants

- [var FFJOFS_RX: Int32](/documentation/forcefeedback/ffjofs_rx)
- [var FFJOFS_RY: Int32](/documentation/forcefeedback/ffjofs_ry)
- [var FFJOFS_RZ: Int32](/documentation/forcefeedback/ffjofs_rz)
- [var FFJOFS_Y: Int32](/documentation/forcefeedback/ffjofs_y)
- [var FFJOFS_Z: Int32](/documentation/forcefeedback/ffjofs_z)

### Macros

- [ForceFeedback Data Types](/documentation/forcefeedback/forcefeedback-data-types)

### Data Types

- [DWORD](/documentation/forcefeedback/dword)
- [FFDeviceObjectReference](/documentation/forcefeedback/ffdeviceobjectreference)
- [FFEffectObjectReference](/documentation/forcefeedback/ffeffectobjectreference)
- [LONG](/documentation/forcefeedback/long)
- [LPDWORD](/documentation/forcefeedback/lpdword)
- [LPLONG](/documentation/forcefeedback/lplong)
- [PFFCAPABILITIES](/documentation/forcefeedback/pffcapabilities)
- [PFFCONDITION](/documentation/forcefeedback/pffcondition)
- [PFFCONSTANTFORCE](/documentation/forcefeedback/pffconstantforce)
- [PFFCUSTOMFORCE](/documentation/forcefeedback/pffcustomforce)
- [PFFEFFECT](/documentation/forcefeedback/pffeffect)
- [PFFEFFESCAPE](/documentation/forcefeedback/pffeffescape)
- [PFFENVELOPE](/documentation/forcefeedback/pffenvelope)
- [PFFPERIODIC](/documentation/forcefeedback/pffperiodic)
- [PFFRAMPFORCE](/documentation/forcefeedback/pfframpforce)

## Variables

- [var kFFAPIMajorRev: Int](/documentation/forcefeedback/kffapimajorrev)
- [var kFFAPIMinorAndBugRev: Int](/documentation/forcefeedback/kffapiminorandbugrev)
- [var kFFAPINonRelRev: Int](/documentation/forcefeedback/kffapinonrelrev)
- [var kFFAPIStage: Int](/documentation/forcefeedback/kffapistage)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
