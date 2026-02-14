# Core Audio Types Documentation

Source: https://sosumi.ai/documentation/coreaudiotypes

---
title: Core Audio Types
source: https://developer.apple.com/documentation/coreaudiotypes
timestamp: 2026-02-13T18:55:12.294Z
---

## Buffers

- [AudioBuffer](/documentation/coreaudiotypes/audiobuffer)

### Creating a Buffer

- [init()](/documentation/coreaudiotypes/audiobuffer/init())
- [init(mNumberChannels: UInt32, mDataByteSize: UInt32, mData: UnsafeMutableRawPointer?)](/documentation/coreaudiotypes/audiobuffer/init(mnumberchannels:mdatabytesize:mdata:))

### Accessing the Audio

- [var mNumberChannels: UInt32](/documentation/coreaudiotypes/audiobuffer/mnumberchannels)
- [var mDataByteSize: UInt32](/documentation/coreaudiotypes/audiobuffer/mdatabytesize)
- [var mData: UnsafeMutableRawPointer?](/documentation/coreaudiotypes/audiobuffer/mdata)

### Initializers

- [init<Element>(UnsafeMutableBufferPointer<Element>, numberOfChannels: Int)](/documentation/coreaudiotypes/audiobuffer/init(_:numberofchannels:))
- [AudioBufferList](/documentation/coreaudiotypes/audiobufferlist)

### Creating a Buffer List

- [init()](/documentation/coreaudiotypes/audiobufferlist/init())
- [init(mNumberBuffers: UInt32, mBuffers: AudioBuffer)](/documentation/coreaudiotypes/audiobufferlist/init(mnumberbuffers:mbuffers:))

### Accessing the Data

- [var mNumberBuffers: UInt32](/documentation/coreaudiotypes/audiobufferlist/mnumberbuffers)
- [var mBuffers: AudioBuffer](/documentation/coreaudiotypes/audiobufferlist/mbuffers)

### Type Methods

- [static func allocate(maximumBuffers: Int) -> UnsafeMutableAudioBufferListPointer](/documentation/coreaudiotypes/audiobufferlist/allocate(maximumbuffers:))
- [static func sizeInBytes(maximumBuffers: Int) -> Int](/documentation/coreaudiotypes/audiobufferlist/sizeinbytes(maximumbuffers:))

## Channels

- [AudioChannelDescription](/documentation/coreaudiotypes/audiochanneldescription)

### Creating a Channel Description

- [init()](/documentation/coreaudiotypes/audiochanneldescription/init())
- [init(mChannelLabel: AudioChannelLabel, mChannelFlags: AudioChannelFlags, mCoordinates: (Float32, Float32, Float32))](/documentation/coreaudiotypes/audiochanneldescription/init(mchannellabel:mchannelflags:mcoordinates:))

### Accessing the Data

- [var mChannelFlags: AudioChannelFlags](/documentation/coreaudiotypes/audiochanneldescription/mchannelflags)
- [var mChannelLabel: AudioChannelLabel](/documentation/coreaudiotypes/audiochanneldescription/mchannellabel)
- [var mCoordinates: (Float32, Float32, Float32)](/documentation/coreaudiotypes/audiochanneldescription/mcoordinates)
- [AudioChannelLabel](/documentation/coreaudiotypes/audiochannellabel)
- [Audio Channel Coordinates](/documentation/coreaudiotypes/audio-channel-coordinates)

#### Coordinates

- [AudioChannelCoordinateIndex](/documentation/coreaudiotypes/audiochannelcoordinateindex)

##### Coordinates

- [case coordinates_BackFront](/documentation/coreaudiotypes/audiochannelcoordinateindex/coordinates_backfront)
- [case coordinates_DownUp](/documentation/coreaudiotypes/audiochannelcoordinateindex/coordinates_downup)
- [case coordinates_LeftRight](/documentation/coreaudiotypes/audiochannelcoordinateindex/coordinates_leftright)
- [static var coordinates_Azimuth: AudioChannelCoordinateIndex](/documentation/coreaudiotypes/audiochannelcoordinateindex/coordinates_azimuth)
- [static var coordinates_Distance: AudioChannelCoordinateIndex](/documentation/coreaudiotypes/audiochannelcoordinateindex/coordinates_distance)
- [static var coordinates_Elevation: AudioChannelCoordinateIndex](/documentation/coreaudiotypes/audiochannelcoordinateindex/coordinates_elevation)

##### Initializers

- [init?(rawValue: UInt32)](/documentation/coreaudiotypes/audiochannelcoordinateindex/init(rawvalue:))
- [static var coordinates_Azimuth: AudioChannelCoordinateIndex](/documentation/coreaudiotypes/audiochannelcoordinateindex/coordinates_azimuth)
- [static var coordinates_Distance: AudioChannelCoordinateIndex](/documentation/coreaudiotypes/audiochannelcoordinateindex/coordinates_distance)
- [static var coordinates_Elevation: AudioChannelCoordinateIndex](/documentation/coreaudiotypes/audiochannelcoordinateindex/coordinates_elevation)

#### Flags

- [static var rectangularCoordinates: AudioChannelFlags](/documentation/coreaudiotypes/audiochannelflags/rectangularcoordinates)
- [static var sphericalCoordinates: AudioChannelFlags](/documentation/coreaudiotypes/audiochannelflags/sphericalcoordinates)
- [static var meters: AudioChannelFlags](/documentation/coreaudiotypes/audiochannelflags/meters)
- [AudioChannelFlags](/documentation/coreaudiotypes/audiochannelflags)

#### Flags

- [static var meters: AudioChannelFlags](/documentation/coreaudiotypes/audiochannelflags/meters)
- [static var rectangularCoordinates: AudioChannelFlags](/documentation/coreaudiotypes/audiochannelflags/rectangularcoordinates)
- [static var sphericalCoordinates: AudioChannelFlags](/documentation/coreaudiotypes/audiochannelflags/sphericalcoordinates)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coreaudiotypes/audiochannelflags/init(rawvalue:))
- [Audio Channel Labels](/documentation/coreaudiotypes/audio-channel-labels)

#### Labels

- [var kAudioChannelLabel_Ambisonic_W: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_ambisonic_w)
- [var kAudioChannelLabel_Ambisonic_X: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_ambisonic_x)
- [var kAudioChannelLabel_Ambisonic_Y: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_ambisonic_y)
- [var kAudioChannelLabel_Ambisonic_Z: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_ambisonic_z)
- [var kAudioChannelLabel_BeginReserved: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_beginreserved)
- [var kAudioChannelLabel_BinauralLeft: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_binauralleft)
- [var kAudioChannelLabel_BinauralRight: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_binauralright)
- [var kAudioChannelLabel_Center: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_center)
- [var kAudioChannelLabel_CenterBottom: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_centerbottom)
- [var kAudioChannelLabel_CenterSurround: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_centersurround)
- [var kAudioChannelLabel_CenterSurroundDirect: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_centersurrounddirect)
- [var kAudioChannelLabel_CenterTopFront: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_centertopfront)
- [var kAudioChannelLabel_CenterTopMiddle: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_centertopmiddle)
- [var kAudioChannelLabel_CenterTopRear: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_centertoprear)
- [var kAudioChannelLabel_ClickTrack: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_clicktrack)
- [var kAudioChannelLabel_DialogCentricMix: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_dialogcentricmix)
- [var kAudioChannelLabel_Discrete: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete)
- [var kAudioChannelLabel_Discrete_0: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_0)
- [var kAudioChannelLabel_Discrete_1: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_1)
- [var kAudioChannelLabel_Discrete_10: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_10)
- [var kAudioChannelLabel_Discrete_11: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_11)
- [var kAudioChannelLabel_Discrete_12: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_12)
- [var kAudioChannelLabel_Discrete_13: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_13)
- [var kAudioChannelLabel_Discrete_14: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_14)
- [var kAudioChannelLabel_Discrete_15: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_15)
- [var kAudioChannelLabel_Discrete_2: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_2)
- [var kAudioChannelLabel_Discrete_3: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_3)
- [var kAudioChannelLabel_Discrete_4: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_4)
- [var kAudioChannelLabel_Discrete_5: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_5)
- [var kAudioChannelLabel_Discrete_6: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_6)
- [var kAudioChannelLabel_Discrete_65535: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_65535)
- [var kAudioChannelLabel_Discrete_7: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_7)
- [var kAudioChannelLabel_Discrete_8: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_8)
- [var kAudioChannelLabel_Discrete_9: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_discrete_9)
- [var kAudioChannelLabel_EndReserved: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_endreserved)
- [var kAudioChannelLabel_ForeignLanguage: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_foreignlanguage)
- [var kAudioChannelLabel_HOA_ACN: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn)
- [var kAudioChannelLabel_HOA_ACN_0: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_0)
- [var kAudioChannelLabel_HOA_ACN_1: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_1)
- [var kAudioChannelLabel_HOA_ACN_10: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_10)
- [var kAudioChannelLabel_HOA_ACN_11: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_11)
- [var kAudioChannelLabel_HOA_ACN_12: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_12)
- [var kAudioChannelLabel_HOA_ACN_13: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_13)
- [var kAudioChannelLabel_HOA_ACN_14: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_14)
- [var kAudioChannelLabel_HOA_ACN_15: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_15)
- [var kAudioChannelLabel_HOA_ACN_2: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_2)
- [var kAudioChannelLabel_HOA_ACN_3: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_3)
- [var kAudioChannelLabel_HOA_ACN_4: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_4)
- [var kAudioChannelLabel_HOA_ACN_5: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_5)
- [var kAudioChannelLabel_HOA_ACN_6: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_6)
- [var kAudioChannelLabel_HOA_ACN_65024: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_65024)
- [var kAudioChannelLabel_HOA_ACN_7: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_7)
- [var kAudioChannelLabel_HOA_ACN_8: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_8)
- [var kAudioChannelLabel_HOA_ACN_9: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_acn_9)
- [var kAudioChannelLabel_HOA_N3D: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_n3d)
- [var kAudioChannelLabel_HOA_SN3D: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hoa_sn3d)
- [var kAudioChannelLabel_Haptic: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_haptic)
- [var kAudioChannelLabel_HeadphonesLeft: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_headphonesleft)
- [var kAudioChannelLabel_HeadphonesRight: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_headphonesright)
- [var kAudioChannelLabel_HearingImpaired: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_hearingimpaired)
- [var kAudioChannelLabel_LFE2: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_lfe2)
- [var kAudioChannelLabel_LFE3: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_lfe3)
- [var kAudioChannelLabel_LFEScreen: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_lfescreen)
- [var kAudioChannelLabel_Left: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_left)
- [var kAudioChannelLabel_LeftBackSurround: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_leftbacksurround)
- [var kAudioChannelLabel_LeftBottom: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_leftbottom)
- [var kAudioChannelLabel_LeftCenter: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_leftcenter)
- [var kAudioChannelLabel_LeftEdgeOfScreen: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_leftedgeofscreen)
- [var kAudioChannelLabel_LeftSideSurround: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_leftsidesurround)
- [var kAudioChannelLabel_LeftSurround: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_leftsurround)
- [var kAudioChannelLabel_LeftSurroundDirect: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_leftsurrounddirect)
- [var kAudioChannelLabel_LeftTopFront: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_lefttopfront)
- [var kAudioChannelLabel_LeftTopMiddle: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_lefttopmiddle)
- [var kAudioChannelLabel_LeftTopRear: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_lefttoprear)
- [var kAudioChannelLabel_LeftTopSurround: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_lefttopsurround)
- [var kAudioChannelLabel_LeftTotal: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_lefttotal)
- [var kAudioChannelLabel_LeftWide: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_leftwide)
- [var kAudioChannelLabel_MS_Mid: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_ms_mid)
- [var kAudioChannelLabel_MS_Side: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_ms_side)
- [var kAudioChannelLabel_Mono: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_mono)
- [var kAudioChannelLabel_Narration: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_narration)
- [var kAudioChannelLabel_Object: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_object)
- [var kAudioChannelLabel_RearSurroundLeft: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_rearsurroundleft)
- [var kAudioChannelLabel_RearSurroundRight: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_rearsurroundright)
- [var kAudioChannelLabel_Right: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_right)
- [var kAudioChannelLabel_RightBackSurround: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_rightbacksurround)
- [var kAudioChannelLabel_RightBottom: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_rightbottom)
- [var kAudioChannelLabel_RightCenter: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_rightcenter)
- [var kAudioChannelLabel_RightEdgeOfScreen: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_rightedgeofscreen)
- [var kAudioChannelLabel_RightSideSurround: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_rightsidesurround)
- [var kAudioChannelLabel_RightSurround: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_rightsurround)
- [var kAudioChannelLabel_RightSurroundDirect: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_rightsurrounddirect)
- [var kAudioChannelLabel_RightTopFront: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_righttopfront)
- [var kAudioChannelLabel_RightTopMiddle: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_righttopmiddle)
- [var kAudioChannelLabel_RightTopRear: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_righttoprear)
- [var kAudioChannelLabel_RightTopSurround: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_righttopsurround)
- [var kAudioChannelLabel_RightTotal: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_righttotal)
- [var kAudioChannelLabel_RightWide: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_rightwide)
- [var kAudioChannelLabel_TopBackCenter: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_topbackcenter)
- [var kAudioChannelLabel_TopBackLeft: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_topbackleft)
- [var kAudioChannelLabel_TopBackRight: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_topbackright)
- [var kAudioChannelLabel_TopCenterSurround: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_topcentersurround)
- [var kAudioChannelLabel_Unknown: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_unknown)
- [var kAudioChannelLabel_Unused: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_unused)
- [var kAudioChannelLabel_UseCoordinates: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_usecoordinates)
- [var kAudioChannelLabel_VerticalHeightCenter: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_verticalheightcenter)
- [var kAudioChannelLabel_VerticalHeightLeft: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_verticalheightleft)
- [var kAudioChannelLabel_VerticalHeightRight: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_verticalheightright)
- [var kAudioChannelLabel_XY_X: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_xy_x)
- [var kAudioChannelLabel_XY_Y: AudioChannelLabel](/documentation/coreaudiotypes/kaudiochannellabel_xy_y)

### Operators

- [static func == (AudioChannelDescription, AudioChannelDescription) -> Bool](/documentation/coreaudiotypes/audiochanneldescription/==(_:_:))
- [AudioChannelLayout](/documentation/coreaudiotypes/audiochannellayout)

### Accessing the Data

- [var mChannelBitmap: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannellayout/mchannelbitmap)
- [AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap)

#### Left

- [static var bit_Left: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_left)
- [static var bit_LeftCenter: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_leftcenter)
- [static var bit_LeftSurround: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_leftsurround)
- [static var bit_LeftSurroundDirect: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_leftsurrounddirect)
- [static var bit_LeftTopFront: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_lefttopfront)
- [static var bit_LeftTopMiddle: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_lefttopmiddle)
- [static var bit_LeftTopRear: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_lefttoprear)
- [static var bit_TopBackLeft: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_topbackleft)
- [static var bit_VerticalHeightLeft: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_verticalheightleft)

#### Center

- [static var bit_Center: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_center)
- [static var bit_CenterSurround: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_centersurround)
- [static var bit_CenterTopFront: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_centertopfront)
- [static var bit_CenterTopMiddle: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_centertopmiddle)
- [static var bit_CenterTopRear: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_centertoprear)
- [static var bit_TopBackCenter: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_topbackcenter)
- [static var bit_TopCenterSurround: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_topcentersurround)
- [static var bit_VerticalHeightCenter: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_verticalheightcenter)

#### Right

- [static var bit_Right: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_right)
- [static var bit_RightCenter: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_rightcenter)
- [static var bit_RightSurround: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_rightsurround)
- [static var bit_RightSurroundDirect: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_rightsurrounddirect)
- [static var bit_RightTopFront: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_righttopfront)
- [static var bit_RightTopMiddle: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_righttopmiddle)
- [static var bit_RightTopRear: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_righttoprear)
- [static var bit_TopBackRight: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_topbackright)
- [static var bit_VerticalHeightRight: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_verticalheightright)

#### Low-Frequency Effects

- [static var bit_LFEScreen: AudioChannelBitmap](/documentation/coreaudiotypes/audiochannelbitmap/bit_lfescreen)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coreaudiotypes/audiochannelbitmap/init(rawvalue:))
- [var mChannelDescriptions: AudioChannelDescription](/documentation/coreaudiotypes/audiochannellayout/mchanneldescriptions)
- [var mChannelLayoutTag: AudioChannelLayoutTag](/documentation/coreaudiotypes/audiochannellayout/mchannellayouttag)
- [AudioChannelLayoutTag](/documentation/coreaudiotypes/audiochannellayouttag)
- [Audio Channel Layout Tags](/documentation/coreaudiotypes/audio-channel-layout-tags)

#### General Layouts

- [var kAudioChannelLayoutTag_UseChannelDescriptions: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_usechanneldescriptions)
- [var kAudioChannelLayoutTag_UseChannelBitmap: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_usechannelbitmap)
- [var kAudioChannelLayoutTag_Mono: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mono)
- [var kAudioChannelLayoutTag_Stereo: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_stereo)
- [var kAudioChannelLayoutTag_StereoHeadphones: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_stereoheadphones)
- [var kAudioChannelLayoutTag_MatrixStereo: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_matrixstereo)
- [var kAudioChannelLayoutTag_MidSide: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_midside)
- [var kAudioChannelLayoutTag_XY: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_xy)
- [var kAudioChannelLayoutTag_Binaural: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_binaural)
- [var kAudioChannelLayoutTag_Ambisonic_B_Format: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_ambisonic_b_format)
- [var kAudioChannelLayoutTag_Quadraphonic: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_quadraphonic)
- [var kAudioChannelLayoutTag_Pentagonal: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_pentagonal)
- [var kAudioChannelLayoutTag_Hexagonal: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_hexagonal)
- [var kAudioChannelLayoutTag_Octagonal: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_octagonal)
- [var kAudioChannelLayoutTag_Cube: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cube)

#### Atmos Layouts

- [var kAudioChannelLayoutTag_Atmos_5_1_2: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_atmos_5_1_2)
- [var kAudioChannelLayoutTag_Atmos_5_1_4: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_atmos_5_1_4)
- [var kAudioChannelLayoutTag_Atmos_7_1_2: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_atmos_7_1_2)
- [var kAudioChannelLayoutTag_Atmos_7_1_4: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_atmos_7_1_4)
- [var kAudioChannelLayoutTag_Atmos_9_1_6: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_atmos_9_1_6)

#### MPEG Defined Layouts

- [var kAudioChannelLayoutTag_MPEG_1_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_1_0)
- [var kAudioChannelLayoutTag_MPEG_2_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_2_0)
- [var kAudioChannelLayoutTag_MPEG_3_0_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_3_0_a)
- [var kAudioChannelLayoutTag_MPEG_3_0_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_3_0_b)
- [var kAudioChannelLayoutTag_MPEG_4_0_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_4_0_a)
- [var kAudioChannelLayoutTag_MPEG_4_0_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_4_0_b)
- [var kAudioChannelLayoutTag_MPEG_5_0_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_5_0_a)
- [var kAudioChannelLayoutTag_MPEG_5_0_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_5_0_b)
- [var kAudioChannelLayoutTag_MPEG_5_0_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_5_0_c)
- [var kAudioChannelLayoutTag_MPEG_5_0_D: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_5_0_d)
- [var kAudioChannelLayoutTag_MPEG_5_0_E: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_5_0_e)
- [var kAudioChannelLayoutTag_MPEG_5_1_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_5_1_a)
- [var kAudioChannelLayoutTag_MPEG_5_1_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_5_1_b)
- [var kAudioChannelLayoutTag_MPEG_5_1_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_5_1_c)
- [var kAudioChannelLayoutTag_MPEG_5_1_D: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_5_1_d)
- [var kAudioChannelLayoutTag_MPEG_5_1_E: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_5_1_e)
- [var kAudioChannelLayoutTag_MPEG_6_1_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_6_1_a)
- [var kAudioChannelLayoutTag_MPEG_6_1_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_6_1_b)
- [var kAudioChannelLayoutTag_MPEG_7_1_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_7_1_a)
- [var kAudioChannelLayoutTag_MPEG_7_1_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_7_1_b)
- [var kAudioChannelLayoutTag_MPEG_7_1_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_7_1_c)
- [var kAudioChannelLayoutTag_MPEG_7_1_D: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_mpeg_7_1_d)
- [var kAudioChannelLayoutTag_Emagic_Default_7_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_emagic_default_7_1)
- [var kAudioChannelLayoutTag_SMPTE_DTV: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_smpte_dtv)

#### CICP

- [var kAudioChannelLayoutTag_CICP_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_1)
- [var kAudioChannelLayoutTag_CICP_2: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_2)
- [var kAudioChannelLayoutTag_CICP_3: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_3)
- [var kAudioChannelLayoutTag_CICP_4: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_4)
- [var kAudioChannelLayoutTag_CICP_5: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_5)
- [var kAudioChannelLayoutTag_CICP_6: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_6)
- [var kAudioChannelLayoutTag_CICP_7: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_7)
- [var kAudioChannelLayoutTag_CICP_9: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_9)
- [var kAudioChannelLayoutTag_CICP_10: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_10)
- [var kAudioChannelLayoutTag_CICP_11: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_11)
- [var kAudioChannelLayoutTag_CICP_12: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_12)
- [var kAudioChannelLayoutTag_CICP_13: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_13)
- [var kAudioChannelLayoutTag_CICP_14: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_14)
- [var kAudioChannelLayoutTag_CICP_15: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_15)
- [var kAudioChannelLayoutTag_CICP_16: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_16)
- [var kAudioChannelLayoutTag_CICP_17: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_17)
- [var kAudioChannelLayoutTag_CICP_18: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_18)
- [var kAudioChannelLayoutTag_CICP_19: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_19)
- [var kAudioChannelLayoutTag_CICP_20: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_cicp_20)

#### ITU Defined Layouts

- [var kAudioChannelLayoutTag_ITU_1_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_itu_1_0)
- [var kAudioChannelLayoutTag_ITU_2_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_itu_2_0)
- [var kAudioChannelLayoutTag_ITU_2_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_itu_2_1)
- [var kAudioChannelLayoutTag_ITU_2_2: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_itu_2_2)
- [var kAudioChannelLayoutTag_ITU_3_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_itu_3_0)
- [var kAudioChannelLayoutTag_ITU_3_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_itu_3_1)
- [var kAudioChannelLayoutTag_ITU_3_2: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_itu_3_2)
- [var kAudioChannelLayoutTag_ITU_3_2_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_itu_3_2_1)
- [var kAudioChannelLayoutTag_ITU_3_4_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_itu_3_4_1)

#### DVD Defined Layouts

- [var kAudioChannelLayoutTag_DVD_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_0)
- [var kAudioChannelLayoutTag_DVD_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_1)
- [var kAudioChannelLayoutTag_DVD_2: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_2)
- [var kAudioChannelLayoutTag_DVD_3: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_3)
- [var kAudioChannelLayoutTag_DVD_4: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_4)
- [var kAudioChannelLayoutTag_DVD_5: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_5)
- [var kAudioChannelLayoutTag_DVD_6: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_6)
- [var kAudioChannelLayoutTag_DVD_7: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_7)
- [var kAudioChannelLayoutTag_DVD_8: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_8)
- [var kAudioChannelLayoutTag_DVD_9: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_9)
- [var kAudioChannelLayoutTag_DVD_10: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_10)
- [var kAudioChannelLayoutTag_DVD_11: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_11)
- [var kAudioChannelLayoutTag_DVD_12: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_12)
- [var kAudioChannelLayoutTag_DVD_13: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_13)
- [var kAudioChannelLayoutTag_DVD_14: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_14)
- [var kAudioChannelLayoutTag_DVD_15: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_15)
- [var kAudioChannelLayoutTag_DVD_16: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_16)
- [var kAudioChannelLayoutTag_DVD_17: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_17)
- [var kAudioChannelLayoutTag_DVD_18: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_18)
- [var kAudioChannelLayoutTag_DVD_19: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_19)
- [var kAudioChannelLayoutTag_DVD_20: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dvd_20)

#### Symmetrical Layouts

- [var kAudioChannelLayoutTag_AudioUnit_4: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_audiounit_4)
- [var kAudioChannelLayoutTag_AudioUnit_5: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_audiounit_5)
- [var kAudioChannelLayoutTag_AudioUnit_6: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_audiounit_6)
- [var kAudioChannelLayoutTag_AudioUnit_8: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_audiounit_8)

#### Surround Based Layouts

- [var kAudioChannelLayoutTag_AudioUnit_5_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_audiounit_5_0)
- [var kAudioChannelLayoutTag_AudioUnit_6_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_audiounit_6_0)
- [var kAudioChannelLayoutTag_AudioUnit_7_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_audiounit_7_0)
- [var kAudioChannelLayoutTag_AudioUnit_7_0_Front: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_audiounit_7_0_front)
- [var kAudioChannelLayoutTag_AudioUnit_5_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_audiounit_5_1)
- [var kAudioChannelLayoutTag_AudioUnit_6_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_audiounit_6_1)
- [var kAudioChannelLayoutTag_AudioUnit_7_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_audiounit_7_1)
- [var kAudioChannelLayoutTag_AudioUnit_7_1_Front: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_audiounit_7_1_front)
- [var kAudioChannelLayoutTag_TMH_10_2_std: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_tmh_10_2_std)
- [var kAudioChannelLayoutTag_TMH_10_2_full: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_tmh_10_2_full)

#### AAC Defined Layouts

- [var kAudioChannelLayoutTag_AAC_3_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_aac_3_0)
- [var kAudioChannelLayoutTag_AAC_Quadraphonic: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_aac_quadraphonic)
- [var kAudioChannelLayoutTag_AAC_4_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_aac_4_0)
- [var kAudioChannelLayoutTag_AAC_5_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_aac_5_0)
- [var kAudioChannelLayoutTag_AAC_5_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_aac_5_1)
- [var kAudioChannelLayoutTag_AAC_6_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_aac_6_0)
- [var kAudioChannelLayoutTag_AAC_6_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_aac_6_1)
- [var kAudioChannelLayoutTag_AAC_7_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_aac_7_0)
- [var kAudioChannelLayoutTag_AAC_7_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_aac_7_1)
- [var kAudioChannelLayoutTag_AAC_7_1_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_aac_7_1_b)
- [var kAudioChannelLayoutTag_AAC_7_1_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_aac_7_1_c)
- [var kAudioChannelLayoutTag_AAC_Octagonal: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_aac_octagonal)

#### AC3 Defined Layouts

- [var kAudioChannelLayoutTag_AC3_1_0_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_ac3_1_0_1)
- [var kAudioChannelLayoutTag_AC3_3_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_ac3_3_0)
- [var kAudioChannelLayoutTag_AC3_3_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_ac3_3_1)
- [var kAudioChannelLayoutTag_AC3_3_0_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_ac3_3_0_1)
- [var kAudioChannelLayoutTag_AC3_2_1_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_ac3_2_1_1)
- [var kAudioChannelLayoutTag_AC3_3_1_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_ac3_3_1_1)

#### EAC3 Defined Layouts

- [var kAudioChannelLayoutTag_EAC_6_0_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_eac_6_0_a)
- [var kAudioChannelLayoutTag_EAC_7_0_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_eac_7_0_a)
- [var kAudioChannelLayoutTag_EAC3_6_1_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_eac3_6_1_a)
- [var kAudioChannelLayoutTag_EAC3_6_1_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_eac3_6_1_b)
- [var kAudioChannelLayoutTag_EAC3_6_1_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_eac3_6_1_c)
- [var kAudioChannelLayoutTag_EAC3_7_1_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_eac3_7_1_a)
- [var kAudioChannelLayoutTag_EAC3_7_1_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_eac3_7_1_b)
- [var kAudioChannelLayoutTag_EAC3_7_1_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_eac3_7_1_c)
- [var kAudioChannelLayoutTag_EAC3_7_1_D: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_eac3_7_1_d)
- [var kAudioChannelLayoutTag_EAC3_7_1_E: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_eac3_7_1_e)
- [var kAudioChannelLayoutTag_EAC3_7_1_F: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_eac3_7_1_f)
- [var kAudioChannelLayoutTag_EAC3_7_1_G: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_eac3_7_1_g)
- [var kAudioChannelLayoutTag_EAC3_7_1_H: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_eac3_7_1_h)

#### DTS Defined Layouts

- [var kAudioChannelLayoutTag_DTS_3_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_3_1)
- [var kAudioChannelLayoutTag_DTS_4_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_4_1)
- [var kAudioChannelLayoutTag_DTS_6_0_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_6_0_a)
- [var kAudioChannelLayoutTag_DTS_6_0_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_6_0_b)
- [var kAudioChannelLayoutTag_DTS_6_0_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_6_0_c)
- [var kAudioChannelLayoutTag_DTS_6_1_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_6_1_a)
- [var kAudioChannelLayoutTag_DTS_6_1_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_6_1_b)
- [var kAudioChannelLayoutTag_DTS_6_1_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_6_1_c)
- [var kAudioChannelLayoutTag_DTS_6_1_D: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_6_1_d)
- [var kAudioChannelLayoutTag_DTS_7_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_7_0)
- [var kAudioChannelLayoutTag_DTS_7_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_7_1)
- [var kAudioChannelLayoutTag_DTS_8_0_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_8_0_a)
- [var kAudioChannelLayoutTag_DTS_8_0_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_8_0_b)
- [var kAudioChannelLayoutTag_DTS_8_1_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_8_1_a)
- [var kAudioChannelLayoutTag_DTS_8_1_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_dts_8_1_b)

#### HOA Defined Layouts

- [var kAudioChannelLayoutTag_HOA_ACN_N3D: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_hoa_acn_n3d)
- [var kAudioChannelLayoutTag_HOA_ACN_SN3D: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_hoa_acn_sn3d)

#### General Information Tags

- [var kAudioChannelLayoutTag_DiscreteInOrder: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_discreteinorder)
- [var kAudioChannelLayoutTag_Unknown: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_unknown)

#### Reserved Tag Range

- [var kAudioChannelLayoutTag_BeginReserved: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_beginreserved)
- [var kAudioChannelLayoutTag_EndReserved: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_endreserved)

#### Wave Layouts

- [var kAudioChannelLayoutTag_WAVE_2_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_wave_2_1)
- [var kAudioChannelLayoutTag_WAVE_3_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_wave_3_0)
- [var kAudioChannelLayoutTag_WAVE_4_0_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_wave_4_0_a)
- [var kAudioChannelLayoutTag_WAVE_4_0_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_wave_4_0_b)
- [var kAudioChannelLayoutTag_WAVE_5_0_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_wave_5_0_a)
- [var kAudioChannelLayoutTag_WAVE_5_0_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_wave_5_0_b)
- [var kAudioChannelLayoutTag_WAVE_5_1_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_wave_5_1_a)
- [var kAudioChannelLayoutTag_WAVE_5_1_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_wave_5_1_b)
- [var kAudioChannelLayoutTag_WAVE_6_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_wave_6_1)
- [var kAudioChannelLayoutTag_WAVE_7_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_wave_7_1)

#### Logic Pro Layouts

- [var kAudioChannelLayoutTag_Logic_4_0_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_4_0_a)
- [var kAudioChannelLayoutTag_Logic_4_0_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_4_0_b)
- [var kAudioChannelLayoutTag_Logic_4_0_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_4_0_c)
- [var kAudioChannelLayoutTag_Logic_5_0_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_5_0_a)
- [var kAudioChannelLayoutTag_Logic_5_0_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_5_0_b)
- [var kAudioChannelLayoutTag_Logic_5_0_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_5_0_c)
- [var kAudioChannelLayoutTag_Logic_5_0_D: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_5_0_d)
- [var kAudioChannelLayoutTag_Logic_5_1_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_5_1_a)
- [var kAudioChannelLayoutTag_Logic_5_1_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_5_1_b)
- [var kAudioChannelLayoutTag_Logic_5_1_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_5_1_c)
- [var kAudioChannelLayoutTag_Logic_5_1_D: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_5_1_d)
- [var kAudioChannelLayoutTag_Logic_6_0_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_6_0_a)
- [var kAudioChannelLayoutTag_Logic_6_0_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_6_0_b)
- [var kAudioChannelLayoutTag_Logic_6_0_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_6_0_c)
- [var kAudioChannelLayoutTag_Logic_6_1_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_6_1_a)
- [var kAudioChannelLayoutTag_Logic_6_1_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_6_1_b)
- [var kAudioChannelLayoutTag_Logic_6_1_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_6_1_c)
- [var kAudioChannelLayoutTag_Logic_6_1_D: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_6_1_d)
- [var kAudioChannelLayoutTag_Logic_7_1_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_7_1_a)
- [var kAudioChannelLayoutTag_Logic_7_1_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_7_1_b)
- [var kAudioChannelLayoutTag_Logic_7_1_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_7_1_c)
- [var kAudioChannelLayoutTag_Logic_7_1_SDDS_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_7_1_sdds_a)
- [var kAudioChannelLayoutTag_Logic_7_1_SDDS_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_7_1_sdds_b)
- [var kAudioChannelLayoutTag_Logic_7_1_SDDS_C: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_7_1_sdds_c)
- [var kAudioChannelLayoutTag_Logic_Atmos_5_1_2: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_atmos_5_1_2)
- [var kAudioChannelLayoutTag_Logic_Atmos_5_1_4: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_atmos_5_1_4)
- [var kAudioChannelLayoutTag_Logic_Atmos_7_1_2: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_atmos_7_1_2)
- [var kAudioChannelLayoutTag_Logic_Atmos_7_1_4_A: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_atmos_7_1_4_a)
- [var kAudioChannelLayoutTag_Logic_Atmos_7_1_4_B: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_atmos_7_1_4_b)
- [var kAudioChannelLayoutTag_Logic_Atmos_7_1_6: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_atmos_7_1_6)
- [var kAudioChannelLayoutTag_Logic_Mono: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_mono)
- [var kAudioChannelLayoutTag_Logic_Quadraphonic: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_quadraphonic)
- [var kAudioChannelLayoutTag_Logic_Stereo: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_logic_stereo)
- [var mNumberChannelDescriptions: UInt32](/documentation/coreaudiotypes/audiochannellayout/mnumberchanneldescriptions)
- [func AudioChannelLayoutTag_GetNumberOfChannels(AudioChannelLayoutTag) -> UInt32](/documentation/coreaudiotypes/audiochannellayouttag_getnumberofchannels(_:))

### Initializers

- [init()](/documentation/coreaudiotypes/audiochannellayout/init())
- [init(mChannelLayoutTag: AudioChannelLayoutTag, mChannelBitmap: AudioChannelBitmap, mNumberChannelDescriptions: UInt32, mChannelDescriptions: AudioChannelDescription)](/documentation/coreaudiotypes/audiochannellayout/init(mchannellayouttag:mchannelbitmap:mnumberchanneldescriptions:mchanneldescriptions:))

### Structures

- [AudioChannelLayout.UnsafeMutablePointer](/documentation/coreaudiotypes/audiochannellayout/unsafemutablepointer)

#### Initializers

- [init?(UnsafeMutablePointer<AudioChannelLayout>?)](/documentation/coreaudiotypes/audiochannellayout/unsafemutablepointer/init(_:)-6v77t)
- [init(UnsafeMutablePointer<AudioChannelLayout>)](/documentation/coreaudiotypes/audiochannellayout/unsafemutablepointer/init(_:)-xfym)

#### Instance Properties

- [var count: Int](/documentation/coreaudiotypes/audiochannellayout/unsafemutablepointer/count)
- [var unsafeMutablePointer: UnsafeMutablePointer<AudioChannelLayout>](/documentation/coreaudiotypes/audiochannellayout/unsafemutablepointer/unsafemutablepointer)
- [var unsafePointer: UnsafePointer<AudioChannelLayout>](/documentation/coreaudiotypes/audiochannellayout/unsafemutablepointer/unsafepointer)
- [AudioChannelLayout.UnsafePointer](/documentation/coreaudiotypes/audiochannellayout/unsafepointer)

#### Initializers

- [init(UnsafePointer<AudioChannelLayout>)](/documentation/coreaudiotypes/audiochannellayout/unsafepointer/init(_:)-21nid)
- [init?(UnsafePointer<AudioChannelLayout>?)](/documentation/coreaudiotypes/audiochannellayout/unsafepointer/init(_:)-2vicp)

#### Instance Properties

- [var count: Int](/documentation/coreaudiotypes/audiochannellayout/unsafepointer/count)
- [var unsafePointer: UnsafePointer<AudioChannelLayout>](/documentation/coreaudiotypes/audiochannellayout/unsafepointer/unsafepointer)

### Type Methods

- [static func allocate(maximumDescriptions: Int) -> AudioChannelLayout.UnsafeMutablePointer](/documentation/coreaudiotypes/audiochannellayout/allocate(maximumdescriptions:))
- [static func sizeInBytes(maximumDescriptions: Int) -> Int](/documentation/coreaudiotypes/audiochannellayout/sizeinbytes(maximumdescriptions:))

## Codecs

- [AudioClassDescription](/documentation/coreaudiotypes/audioclassdescription)

### Accessing the Data

- [var mType: OSType](/documentation/coreaudiotypes/audioclassdescription/mtype)
- [var mSubType: OSType](/documentation/coreaudiotypes/audioclassdescription/msubtype)
- [var mManufacturer: OSType](/documentation/coreaudiotypes/audioclassdescription/mmanufacturer)

### Initializers

- [init()](/documentation/coreaudiotypes/audioclassdescription/init())
- [init(mType: OSType, mSubType: OSType, mManufacturer: OSType)](/documentation/coreaudiotypes/audioclassdescription/init(mtype:msubtype:mmanufacturer:))

## Audio Time

- [AudioTimeStamp](/documentation/coreaudiotypes/audiotimestamp)

### Accessing the Data

- [var mFlags: AudioTimeStampFlags](/documentation/coreaudiotypes/audiotimestamp/mflags)
- [var mHostTime: UInt64](/documentation/coreaudiotypes/audiotimestamp/mhosttime)
- [var mRateScalar: Float64](/documentation/coreaudiotypes/audiotimestamp/mratescalar)
- [var mReserved: UInt32](/documentation/coreaudiotypes/audiotimestamp/mreserved)
- [var mSMPTETime: SMPTETime](/documentation/coreaudiotypes/audiotimestamp/msmptetime)
- [var mSampleTime: Float64](/documentation/coreaudiotypes/audiotimestamp/msampletime)
- [var mWordClockTime: UInt64](/documentation/coreaudiotypes/audiotimestamp/mwordclocktime)

### Initializers

- [init()](/documentation/coreaudiotypes/audiotimestamp/init())
- [init(mSampleTime: Float64, mHostTime: UInt64, mRateScalar: Float64, mWordClockTime: UInt64, mSMPTETime: SMPTETime, mFlags: AudioTimeStampFlags, mReserved: UInt32)](/documentation/coreaudiotypes/audiotimestamp/init(msampletime:mhosttime:mratescalar:mwordclocktime:msmptetime:mflags:mreserved:))
- [AudioTimeStampFlags](/documentation/coreaudiotypes/audiotimestampflags)

### Initializers

- [init(rawValue: UInt32)](/documentation/coreaudiotypes/audiotimestampflags/init(rawvalue:))

### Type Properties

- [static var hostTimeValid: AudioTimeStampFlags](/documentation/coreaudiotypes/audiotimestampflags/hosttimevalid)
- [static var rateScalarValid: AudioTimeStampFlags](/documentation/coreaudiotypes/audiotimestampflags/ratescalarvalid)
- [static var sampleHostTimeValid: AudioTimeStampFlags](/documentation/coreaudiotypes/audiotimestampflags/samplehosttimevalid)
- [static var sampleTimeValid: AudioTimeStampFlags](/documentation/coreaudiotypes/audiotimestampflags/sampletimevalid)
- [static var smpteTimeValid: AudioTimeStampFlags](/documentation/coreaudiotypes/audiotimestampflags/smptetimevalid)
- [static var wordClockTimeValid: AudioTimeStampFlags](/documentation/coreaudiotypes/audiotimestampflags/wordclocktimevalid)

## SMPTE Time

- [SMPTETime](/documentation/coreaudiotypes/smptetime)

### Initializers

- [init()](/documentation/coreaudiotypes/smptetime/init())
- [init(mSubframes: Int16, mSubframeDivisor: Int16, mCounter: UInt32, mType: SMPTETimeType, mFlags: SMPTETimeFlags, mHours: Int16, mMinutes: Int16, mSeconds: Int16, mFrames: Int16)](/documentation/coreaudiotypes/smptetime/init(msubframes:msubframedivisor:mcounter:mtype:mflags:mhours:mminutes:mseconds:mframes:))

### Instance Properties

- [var mCounter: UInt32](/documentation/coreaudiotypes/smptetime/mcounter)
- [var mFlags: SMPTETimeFlags](/documentation/coreaudiotypes/smptetime/mflags)
- [var mFrames: Int16](/documentation/coreaudiotypes/smptetime/mframes)
- [var mHours: Int16](/documentation/coreaudiotypes/smptetime/mhours)
- [var mMinutes: Int16](/documentation/coreaudiotypes/smptetime/mminutes)
- [var mSeconds: Int16](/documentation/coreaudiotypes/smptetime/mseconds)
- [var mSubframeDivisor: Int16](/documentation/coreaudiotypes/smptetime/msubframedivisor)
- [var mSubframes: Int16](/documentation/coreaudiotypes/smptetime/msubframes)
- [var mType: SMPTETimeType](/documentation/coreaudiotypes/smptetime/mtype)
- [SMPTETimeFlags](/documentation/coreaudiotypes/smptetimeflags)

### Initializers

- [init(rawValue: UInt32)](/documentation/coreaudiotypes/smptetimeflags/init(rawvalue:))

### Type Properties

- [static var running: SMPTETimeFlags](/documentation/coreaudiotypes/smptetimeflags/running)
- [static var valid: SMPTETimeFlags](/documentation/coreaudiotypes/smptetimeflags/valid)
- [SMPTETimeType](/documentation/coreaudiotypes/smptetimetype)

### Constants

- [case type2398](/documentation/coreaudiotypes/smptetimetype/type2398)
- [case type24](/documentation/coreaudiotypes/smptetimetype/type24)
- [case type25](/documentation/coreaudiotypes/smptetimetype/type25)
- [case type2997](/documentation/coreaudiotypes/smptetimetype/type2997)
- [case type2997Drop](/documentation/coreaudiotypes/smptetimetype/type2997drop)
- [case type30](/documentation/coreaudiotypes/smptetimetype/type30)
- [case type30Drop](/documentation/coreaudiotypes/smptetimetype/type30drop)
- [case type50](/documentation/coreaudiotypes/smptetimetype/type50)
- [case type5994](/documentation/coreaudiotypes/smptetimetype/type5994)
- [case type5994Drop](/documentation/coreaudiotypes/smptetimetype/type5994drop)
- [case type60](/documentation/coreaudiotypes/smptetimetype/type60)
- [case type60Drop](/documentation/coreaudiotypes/smptetimetype/type60drop)

### Initializers

- [init?(rawValue: UInt32)](/documentation/coreaudiotypes/smptetimetype/init(rawvalue:))

## Values

- [AudioValueRange](/documentation/coreaudiotypes/audiovaluerange)

### Inspecting a range

- [var mMaximum: Float64](/documentation/coreaudiotypes/audiovaluerange/mmaximum)
- [var mMinimum: Float64](/documentation/coreaudiotypes/audiovaluerange/mminimum)

### Initializers

- [init()](/documentation/coreaudiotypes/audiovaluerange/init())
- [init(mMinimum: Float64, mMaximum: Float64)](/documentation/coreaudiotypes/audiovaluerange/init(mminimum:mmaximum:))
- [AudioValueTranslation](/documentation/coreaudiotypes/audiovaluetranslation)

### Initializers

- [init(mInputData: UnsafeMutableRawPointer, mInputDataSize: UInt32, mOutputData: UnsafeMutableRawPointer, mOutputDataSize: UInt32)](/documentation/coreaudiotypes/audiovaluetranslation/init(minputdata:minputdatasize:moutputdata:moutputdatasize:))

### Instance Properties

- [var mInputData: UnsafeMutableRawPointer](/documentation/coreaudiotypes/audiovaluetranslation/minputdata)
- [var mInputDataSize: UInt32](/documentation/coreaudiotypes/audiovaluetranslation/minputdatasize)
- [var mOutputData: UnsafeMutableRawPointer](/documentation/coreaudiotypes/audiovaluetranslation/moutputdata)
- [var mOutputDataSize: UInt32](/documentation/coreaudiotypes/audiovaluetranslation/moutputdatasize)

## Streams

- [AudioStreamBasicDescription](/documentation/coreaudiotypes/audiostreambasicdescription)

### Inspecting a description

- [var mFormatID: AudioFormatID](/documentation/coreaudiotypes/audiostreambasicdescription/mformatid)
- [var mFormatFlags: AudioFormatFlags](/documentation/coreaudiotypes/audiostreambasicdescription/mformatflags)
- [var mSampleRate: Float64](/documentation/coreaudiotypes/audiostreambasicdescription/msamplerate)
- [var mBitsPerChannel: UInt32](/documentation/coreaudiotypes/audiostreambasicdescription/mbitsperchannel)
- [var mBytesPerFrame: UInt32](/documentation/coreaudiotypes/audiostreambasicdescription/mbytesperframe)
- [var mChannelsPerFrame: UInt32](/documentation/coreaudiotypes/audiostreambasicdescription/mchannelsperframe)
- [var mBytesPerPacket: UInt32](/documentation/coreaudiotypes/audiostreambasicdescription/mbytesperpacket)
- [var mFramesPerPacket: UInt32](/documentation/coreaudiotypes/audiostreambasicdescription/mframesperpacket)
- [var mReserved: UInt32](/documentation/coreaudiotypes/audiostreambasicdescription/mreserved)

### Initializers

- [init()](/documentation/coreaudiotypes/audiostreambasicdescription/init())
- [init(mSampleRate: Float64, mFormatID: AudioFormatID, mFormatFlags: AudioFormatFlags, mBytesPerPacket: UInt32, mFramesPerPacket: UInt32, mBytesPerFrame: UInt32, mChannelsPerFrame: UInt32, mBitsPerChannel: UInt32, mReserved: UInt32)](/documentation/coreaudiotypes/audiostreambasicdescription/init(msamplerate:mformatid:mformatflags:mbytesperpacket:mframesperpacket:mbytesperframe:mchannelsperframe:mbitsperchannel:mreserved:))
- [AudioStreamPacketDescription](/documentation/coreaudiotypes/audiostreampacketdescription)

### Inspecting an audio stream packet description

- [var mDataByteSize: UInt32](/documentation/coreaudiotypes/audiostreampacketdescription/mdatabytesize)
- [var mStartOffset: Int64](/documentation/coreaudiotypes/audiostreampacketdescription/mstartoffset)
- [var mVariableFramesInPacket: UInt32](/documentation/coreaudiotypes/audiostreampacketdescription/mvariableframesinpacket)

### Creating an audio stream packet descripiton

- [init()](/documentation/coreaudiotypes/audiostreampacketdescription/init())
- [init(mStartOffset: Int64, mVariableFramesInPacket: UInt32, mDataByteSize: UInt32)](/documentation/coreaudiotypes/audiostreampacketdescription/init(mstartoffset:mvariableframesinpacket:mdatabytesize:))
- [AudioFormatFlags](/documentation/coreaudiotypes/audioformatflags)
- [Audio Format Flags](/documentation/coreaudiotypes/audio-format-flags)

### Format flags

- [var kAppleLosslessFormatFlag_16BitSourceData: AudioFormatFlags](/documentation/coreaudiotypes/kapplelosslessformatflag_16bitsourcedata)
- [var kAppleLosslessFormatFlag_20BitSourceData: AudioFormatFlags](/documentation/coreaudiotypes/kapplelosslessformatflag_20bitsourcedata)
- [var kAppleLosslessFormatFlag_24BitSourceData: AudioFormatFlags](/documentation/coreaudiotypes/kapplelosslessformatflag_24bitsourcedata)
- [var kAppleLosslessFormatFlag_32BitSourceData: AudioFormatFlags](/documentation/coreaudiotypes/kapplelosslessformatflag_32bitsourcedata)
- [var kAudioFormatFlagIsAlignedHigh: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagisalignedhigh)
- [var kAudioFormatFlagIsBigEndian: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagisbigendian)
- [var kAudioFormatFlagIsFloat: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagisfloat)
- [var kAudioFormatFlagIsNonInterleaved: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagisnoninterleaved)
- [var kAudioFormatFlagIsNonMixable: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagisnonmixable)
- [var kAudioFormatFlagIsPacked: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagispacked)
- [var kAudioFormatFlagIsSignedInteger: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagissignedinteger)
- [var kAudioFormatFlagsAreAllClear: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagsareallclear)
- [var kAudioFormatFlagsNativeEndian: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagsnativeendian)
- [var kAudioFormatFlagsNativeFloatPacked: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagsnativefloatpacked)
- [var kLinearPCMFormatFlagIsAlignedHigh: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagisalignedhigh)
- [var kLinearPCMFormatFlagIsBigEndian: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagisbigendian)
- [var kLinearPCMFormatFlagIsFloat: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagisfloat)
- [var kLinearPCMFormatFlagIsNonInterleaved: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagisnoninterleaved)
- [var kLinearPCMFormatFlagIsNonMixable: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagisnonmixable)
- [var kLinearPCMFormatFlagIsPacked: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagispacked)
- [var kLinearPCMFormatFlagIsSignedInteger: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagissignedinteger)
- [var kLinearPCMFormatFlagsAreAllClear: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagsareallclear)
- [var kLinearPCMFormatFlagsSampleFractionMask: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagssamplefractionmask)
- [var kLinearPCMFormatFlagsSampleFractionShift: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagssamplefractionshift)
- [var kAudioFormatFlagsAudioUnitCanonical: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagsaudiounitcanonical)
- [var kAudioFormatFlagsCanonical: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagscanonical)
- [AudioFormatID](/documentation/coreaudiotypes/audioformatid)
- [Audio Format Identifiers](/documentation/coreaudiotypes/audio-format-identifiers)

### Format identifiers

- [var kAudioFormat60958AC3: AudioFormatID](/documentation/coreaudiotypes/kaudioformat60958ac3)
- [var kAudioFormatAC3: AudioFormatID](/documentation/coreaudiotypes/kaudioformatac3)
- [var kAudioFormatAES3: AudioFormatID](/documentation/coreaudiotypes/kaudioformataes3)
- [var kAudioFormatALaw: AudioFormatID](/documentation/coreaudiotypes/kaudioformatalaw)
- [var kAudioFormatAMR: AudioFormatID](/documentation/coreaudiotypes/kaudioformatamr)
- [var kAudioFormatAMR_WB: AudioFormatID](/documentation/coreaudiotypes/kaudioformatamr_wb)
- [var kAudioFormatAppleIMA4: AudioFormatID](/documentation/coreaudiotypes/kaudioformatappleima4)
- [var kAudioFormatAppleLossless: AudioFormatID](/documentation/coreaudiotypes/kaudioformatapplelossless)
- [var kAudioFormatAudible: AudioFormatID](/documentation/coreaudiotypes/kaudioformataudible)
- [var kAudioFormatDVIIntelIMA: AudioFormatID](/documentation/coreaudiotypes/kaudioformatdviintelima)
- [var kAudioFormatEnhancedAC3: AudioFormatID](/documentation/coreaudiotypes/kaudioformatenhancedac3)
- [var kAudioFormatFLAC: AudioFormatID](/documentation/coreaudiotypes/kaudioformatflac)
- [var kAudioFormatLinearPCM: AudioFormatID](/documentation/coreaudiotypes/kaudioformatlinearpcm)
- [var kAudioFormatMACE3: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmace3)
- [var kAudioFormatMACE6: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmace6)
- [var kAudioFormatMIDIStream: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmidistream)
- [var kAudioFormatMPEG4AAC: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpeg4aac)
- [var kAudioFormatMPEG4AAC_ELD: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpeg4aac_eld)
- [var kAudioFormatMPEG4AAC_ELD_SBR: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpeg4aac_eld_sbr)
- [var kAudioFormatMPEG4AAC_ELD_V2: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpeg4aac_eld_v2)
- [var kAudioFormatMPEG4AAC_HE: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpeg4aac_he)
- [var kAudioFormatMPEG4AAC_HE_V2: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpeg4aac_he_v2)
- [var kAudioFormatMPEG4AAC_LD: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpeg4aac_ld)
- [var kAudioFormatMPEG4AAC_Spatial: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpeg4aac_spatial)
- [var kAudioFormatMPEG4CELP: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpeg4celp)
- [var kAudioFormatMPEG4HVXC: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpeg4hvxc)
- [var kAudioFormatMPEG4TwinVQ: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpeg4twinvq)
- [var kAudioFormatMPEGD_USAC: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpegd_usac)
- [var kAudioFormatMPEGLayer1: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpeglayer1)
- [var kAudioFormatMPEGLayer2: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpeglayer2)
- [var kAudioFormatMPEGLayer3: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmpeglayer3)
- [var kAudioFormatMicrosoftGSM: AudioFormatID](/documentation/coreaudiotypes/kaudioformatmicrosoftgsm)
- [var kAudioFormatOpus: AudioFormatID](/documentation/coreaudiotypes/kaudioformatopus)
- [var kAudioFormatParameterValueStream: AudioFormatID](/documentation/coreaudiotypes/kaudioformatparametervaluestream)
- [var kAudioFormatQDesign: AudioFormatID](/documentation/coreaudiotypes/kaudioformatqdesign)
- [var kAudioFormatQDesign2: AudioFormatID](/documentation/coreaudiotypes/kaudioformatqdesign2)
- [var kAudioFormatQUALCOMM: AudioFormatID](/documentation/coreaudiotypes/kaudioformatqualcomm)
- [var kAudioFormatTimeCode: AudioFormatID](/documentation/coreaudiotypes/kaudioformattimecode)
- [var kAudioFormatULaw: AudioFormatID](/documentation/coreaudiotypes/kaudioformatulaw)
- [var kAudioFormatiLBC: AudioFormatID](/documentation/coreaudiotypes/kaudioformatilbc)
- [let kAudioStreamAnyRate: Float64](/documentation/coreaudiotypes/kaudiostreamanyrate)
- [MPEG4ObjectID](/documentation/coreaudiotypes/mpeg4objectid)

### Constants

- [case AAC_LC](/documentation/coreaudiotypes/mpeg4objectid/aac_lc)
- [case AAC_LTP](/documentation/coreaudiotypes/mpeg4objectid/aac_ltp)
- [case aac_Main](/documentation/coreaudiotypes/mpeg4objectid/aac_main)
- [case AAC_SBR](/documentation/coreaudiotypes/mpeg4objectid/aac_sbr)
- [case AAC_SSR](/documentation/coreaudiotypes/mpeg4objectid/aac_ssr)
- [case aac_Scalable](/documentation/coreaudiotypes/mpeg4objectid/aac_scalable)
- [case CELP](/documentation/coreaudiotypes/mpeg4objectid/celp)
- [case HVXC](/documentation/coreaudiotypes/mpeg4objectid/hvxc)
- [case twinVQ](/documentation/coreaudiotypes/mpeg4objectid/twinvq)

### Initializers

- [init?(rawValue: Int)](/documentation/coreaudiotypes/mpeg4objectid/init(rawvalue:))

## Common Types

- [AVAudioInteger](/documentation/coreaudiotypes/avaudiointeger)
- [AVAudioUInteger](/documentation/coreaudiotypes/avaudiouinteger)
- [AudioSessionID](/documentation/coreaudiotypes/audiosessionid)
- [var kAudioUnitSampleFractionBits: Int32](/documentation/coreaudiotypes/kaudiounitsamplefractionbits)
- [var COREAUDIOTYPES_VERSION: Int32](/documentation/coreaudiotypes/coreaudiotypes_version)
- [AudioSampleType](/documentation/coreaudiotypes/audiosampletype)
- [AudioUnitSampleType](/documentation/coreaudiotypes/audiounitsampletype)
- [AudioFormatListItem](/documentation/coreaudiotypes/audioformatlistitem)

### Initializers

- [init()](/documentation/coreaudiotypes/audioformatlistitem/init())
- [init(mASBD: AudioStreamBasicDescription, mChannelLayoutTag: AudioChannelLayoutTag)](/documentation/coreaudiotypes/audioformatlistitem/init(masbd:mchannellayouttag:))

### Instance Properties

- [var mASBD: AudioStreamBasicDescription](/documentation/coreaudiotypes/audioformatlistitem/masbd)
- [var mChannelLayoutTag: AudioChannelLayoutTag](/documentation/coreaudiotypes/audioformatlistitem/mchannellayouttag)

## Errors

- [var kAudio_ParamError: OSStatus](/documentation/coreaudiotypes/kaudio_paramerror)
- [var kAudio_MemFullError: OSStatus](/documentation/coreaudiotypes/kaudio_memfullerror)
- [var kAudio_FileNotFoundError: OSStatus](/documentation/coreaudiotypes/kaudio_filenotfounderror)
- [var kAudio_UnimplementedError: OSStatus](/documentation/coreaudiotypes/kaudio_unimplementederror)

## Reference

- [CoreAudioTypes Enumerations](/documentation/coreaudiotypes/coreaudiotypes-enumerations)

### Enumerations

- [Audio Stream Basic Description Flags](/documentation/coreaudiotypes/audio-stream-basic-description-flags)

#### Constants

- [var kAppleLosslessFormatFlag_16BitSourceData: AudioFormatFlags](/documentation/coreaudiotypes/kapplelosslessformatflag_16bitsourcedata)
- [var kAppleLosslessFormatFlag_20BitSourceData: AudioFormatFlags](/documentation/coreaudiotypes/kapplelosslessformatflag_20bitsourcedata)
- [var kAppleLosslessFormatFlag_24BitSourceData: AudioFormatFlags](/documentation/coreaudiotypes/kapplelosslessformatflag_24bitsourcedata)
- [var kAppleLosslessFormatFlag_32BitSourceData: AudioFormatFlags](/documentation/coreaudiotypes/kapplelosslessformatflag_32bitsourcedata)
- [var kAudioFormatFlagIsAlignedHigh: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagisalignedhigh)
- [var kAudioFormatFlagIsBigEndian: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagisbigendian)
- [var kAudioFormatFlagIsFloat: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagisfloat)
- [var kAudioFormatFlagIsNonInterleaved: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagisnoninterleaved)
- [var kAudioFormatFlagIsNonMixable: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagisnonmixable)
- [var kAudioFormatFlagIsPacked: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagispacked)
- [var kAudioFormatFlagIsSignedInteger: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagissignedinteger)
- [var kAudioFormatFlagsAreAllClear: AudioFormatFlags](/documentation/coreaudiotypes/kaudioformatflagsareallclear)
- [var kLinearPCMFormatFlagIsAlignedHigh: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagisalignedhigh)
- [var kLinearPCMFormatFlagIsBigEndian: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagisbigendian)
- [var kLinearPCMFormatFlagIsFloat: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagisfloat)
- [var kLinearPCMFormatFlagIsNonInterleaved: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagisnoninterleaved)
- [var kLinearPCMFormatFlagIsNonMixable: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagisnonmixable)
- [var kLinearPCMFormatFlagIsPacked: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagispacked)
- [var kLinearPCMFormatFlagIsSignedInteger: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagissignedinteger)
- [var kLinearPCMFormatFlagsAreAllClear: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagsareallclear)
- [var kLinearPCMFormatFlagsSampleFractionMask: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagssamplefractionmask)
- [var kLinearPCMFormatFlagsSampleFractionShift: AudioFormatFlags](/documentation/coreaudiotypes/klinearpcmformatflagssamplefractionshift)
- [Anonymous](/documentation/coreaudiotypes/2962796-anonymous)
- [Anonymous](/documentation/coreaudiotypes/4278542-anonymous)

### Global variables

- [var CA_PREFER_FIXED_POINT: Int32](/documentation/coreaudiotypes/ca_prefer_fixed_point)

## Structures

- [AudioStreamPacketDependencyDescription](/documentation/coreaudiotypes/audiostreampacketdependencydescription)

### Initializers

- [init()](/documentation/coreaudiotypes/audiostreampacketdependencydescription/init())
- [init(mIsIndependentlyDecodable: UInt32, mPreRollCount: UInt32, mFlags: UInt32, mReserved: UInt32)](/documentation/coreaudiotypes/audiostreampacketdependencydescription/init(misindependentlydecodable:mprerollcount:mflags:mreserved:))

### Instance Properties

- [var mFlags: UInt32](/documentation/coreaudiotypes/audiostreampacketdependencydescription/mflags)
- [var mIsIndependentlyDecodable: UInt32](/documentation/coreaudiotypes/audiostreampacketdependencydescription/misindependentlydecodable)
- [var mPreRollCount: UInt32](/documentation/coreaudiotypes/audiostreampacketdependencydescription/mprerollcount)
- [var mReserved: UInt32](/documentation/coreaudiotypes/audiostreampacketdependencydescription/mreserved)

## Variables

- [var kAudioChannelLayoutTag_Ogg_3_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_ogg_3_0)
- [var kAudioChannelLayoutTag_Ogg_4_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_ogg_4_0)
- [var kAudioChannelLayoutTag_Ogg_5_0: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_ogg_5_0)
- [var kAudioChannelLayoutTag_Ogg_5_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_ogg_5_1)
- [var kAudioChannelLayoutTag_Ogg_6_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_ogg_6_1)
- [var kAudioChannelLayoutTag_Ogg_7_1: AudioChannelLayoutTag](/documentation/coreaudiotypes/kaudiochannellayouttag_ogg_7_1)
- [var kAudioFormatAPAC: AudioFormatID](/documentation/coreaudiotypes/kaudioformatapac)
- [var kAudio_BadFilePathError: OSStatus](/documentation/coreaudiotypes/kaudio_badfilepatherror)
- [var kAudio_FilePermissionError: OSStatus](/documentation/coreaudiotypes/kaudio_filepermissionerror)
- [var kAudio_NoError: OSStatus](/documentation/coreaudiotypes/kaudio_noerror)
- [var kAudio_TooManyFilesOpenError: OSStatus](/documentation/coreaudiotypes/kaudio_toomanyfilesopenerror)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
