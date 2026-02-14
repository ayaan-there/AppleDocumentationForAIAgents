# Core Text Documentation

Source: https://sosumi.ai/documentation/coretext

---
title: Core Text
source: https://developer.apple.com/documentation/coretext
timestamp: 2026-02-13T18:55:46.039Z
---

## Opaque Types

- [CTFont](/documentation/coretext/ctfont)

### Creating Fonts

- [func CTFontCreateWithName(CFString, CGFloat, UnsafePointer<CGAffineTransform>?) -> CTFont](/documentation/coretext/ctfontcreatewithname(_:_:_:))
- [func CTFontCreateWithNameAndOptions(CFString, CGFloat, UnsafePointer<CGAffineTransform>?, CTFontOptions) -> CTFont](/documentation/coretext/ctfontcreatewithnameandoptions(_:_:_:_:))
- [func CTFontCreateWithFontDescriptor(CTFontDescriptor, CGFloat, UnsafePointer<CGAffineTransform>?) -> CTFont](/documentation/coretext/ctfontcreatewithfontdescriptor(_:_:_:))
- [func CTFontCreateWithFontDescriptorAndOptions(CTFontDescriptor, CGFloat, UnsafePointer<CGAffineTransform>?, CTFontOptions) -> CTFont](/documentation/coretext/ctfontcreatewithfontdescriptorandoptions(_:_:_:_:))
- [func CTFontCreateUIFontForLanguage(CTFontUIFontType, CGFloat, CFString?) -> CTFont?](/documentation/coretext/ctfontcreateuifontforlanguage(_:_:_:))
- [func CTFontCreateCopyWithAttributes(CTFont, CGFloat, UnsafePointer<CGAffineTransform>?, CTFontDescriptor?) -> CTFont](/documentation/coretext/ctfontcreatecopywithattributes(_:_:_:_:))
- [func CTFontCreateCopyWithSymbolicTraits(CTFont, CGFloat, UnsafePointer<CGAffineTransform>?, CTFontSymbolicTraits, CTFontSymbolicTraits) -> CTFont?](/documentation/coretext/ctfontcreatecopywithsymbolictraits(_:_:_:_:_:))
- [func CTFontCreateCopyWithFamily(CTFont, CGFloat, UnsafePointer<CGAffineTransform>?, CFString) -> CTFont?](/documentation/coretext/ctfontcreatecopywithfamily(_:_:_:_:))
- [func CTFontCreateForString(CTFont, CFString, CFRange) -> CTFont](/documentation/coretext/ctfontcreateforstring(_:_:_:))
- [func CTFontCreateForStringWithLanguage(CTFont, CFString, CFRange, CFString?) -> CTFont](/documentation/coretext/ctfontcreateforstringwithlanguage(_:_:_:_:))

### Getting Font Data

- [func CTFontCopyFontDescriptor(CTFont) -> CTFontDescriptor](/documentation/coretext/ctfontcopyfontdescriptor(_:))
- [func CTFontCopyAttribute(CTFont, CFString) -> CFTypeRef?](/documentation/coretext/ctfontcopyattribute(_:_:))
- [func CTFontGetSize(CTFont) -> CGFloat](/documentation/coretext/ctfontgetsize(_:))
- [func CTFontGetMatrix(CTFont) -> CGAffineTransform](/documentation/coretext/ctfontgetmatrix(_:))
- [func CTFontGetSymbolicTraits(CTFont) -> CTFontSymbolicTraits](/documentation/coretext/ctfontgetsymbolictraits(_:))
- [func CTFontCopyTraits(CTFont) -> CFDictionary](/documentation/coretext/ctfontcopytraits(_:))
- [func CTFontCopyDefaultCascadeListForLanguages(CTFont, CFArray?) -> CFArray?](/documentation/coretext/ctfontcopydefaultcascadelistforlanguages(_:_:))

### Getting Font Names

- [func CTFontCopyPostScriptName(CTFont) -> CFString](/documentation/coretext/ctfontcopypostscriptname(_:))
- [func CTFontCopyFamilyName(CTFont) -> CFString](/documentation/coretext/ctfontcopyfamilyname(_:))
- [func CTFontCopyFullName(CTFont) -> CFString](/documentation/coretext/ctfontcopyfullname(_:))
- [func CTFontCopyDisplayName(CTFont) -> CFString](/documentation/coretext/ctfontcopydisplayname(_:))
- [func CTFontCopyName(CTFont, CFString) -> CFString?](/documentation/coretext/ctfontcopyname(_:_:))
- [func CTFontCopyLocalizedName(CTFont, CFString, UnsafeMutablePointer<Unmanaged<CFString>?>?) -> CFString?](/documentation/coretext/ctfontcopylocalizedname(_:_:_:))

### Working With Encoding

- [func CTFontCopyCharacterSet(CTFont) -> CFCharacterSet](/documentation/coretext/ctfontcopycharacterset(_:))
- [func CTFontGetStringEncoding(CTFont) -> CFStringEncoding](/documentation/coretext/ctfontgetstringencoding(_:))
- [func CTFontCopySupportedLanguages(CTFont) -> CFArray](/documentation/coretext/ctfontcopysupportedlanguages(_:))

### Getting Font Metrics

- [func CTFontGetAscent(CTFont) -> CGFloat](/documentation/coretext/ctfontgetascent(_:))
- [func CTFontGetDescent(CTFont) -> CGFloat](/documentation/coretext/ctfontgetdescent(_:))
- [func CTFontGetLeading(CTFont) -> CGFloat](/documentation/coretext/ctfontgetleading(_:))
- [func CTFontGetUnitsPerEm(CTFont) -> UInt32](/documentation/coretext/ctfontgetunitsperem(_:))
- [func CTFontGetGlyphCount(CTFont) -> CFIndex](/documentation/coretext/ctfontgetglyphcount(_:))
- [func CTFontGetBoundingBox(CTFont) -> CGRect](/documentation/coretext/ctfontgetboundingbox(_:))
- [func CTFontGetUnderlinePosition(CTFont) -> CGFloat](/documentation/coretext/ctfontgetunderlineposition(_:))
- [func CTFontGetUnderlineThickness(CTFont) -> CGFloat](/documentation/coretext/ctfontgetunderlinethickness(_:))
- [func CTFontGetSlantAngle(CTFont) -> CGFloat](/documentation/coretext/ctfontgetslantangle(_:))
- [func CTFontGetCapHeight(CTFont) -> CGFloat](/documentation/coretext/ctfontgetcapheight(_:))
- [func CTFontGetXHeight(CTFont) -> CGFloat](/documentation/coretext/ctfontgetxheight(_:))

### Getting Glyph Data

- [func CTFontCreatePathForGlyph(CTFont, CGGlyph, UnsafePointer<CGAffineTransform>?) -> CGPath?](/documentation/coretext/ctfontcreatepathforglyph(_:_:_:))
- [func CTFontGetGlyphWithName(CTFont, CFString) -> CGGlyph](/documentation/coretext/ctfontgetglyphwithname(_:_:))
- [func CTFontGetBoundingRectsForGlyphs(CTFont, CTFontOrientation, UnsafePointer<CGGlyph>, UnsafeMutablePointer<CGRect>?, CFIndex) -> CGRect](/documentation/coretext/ctfontgetboundingrectsforglyphs(_:_:_:_:_:))
- [func CTFontGetAdvancesForGlyphs(CTFont, CTFontOrientation, UnsafePointer<CGGlyph>, UnsafeMutablePointer<CGSize>?, CFIndex) -> Double](/documentation/coretext/ctfontgetadvancesforglyphs(_:_:_:_:_:))
- [func CTFontGetOpticalBoundsForGlyphs(CTFont, UnsafePointer<CGGlyph>, UnsafeMutablePointer<CGRect>?, CFIndex, CFOptionFlags) -> CGRect](/documentation/coretext/ctfontgetopticalboundsforglyphs(_:_:_:_:_:))
- [func CTFontGetVerticalTranslationsForGlyphs(CTFont, UnsafePointer<CGGlyph>, UnsafeMutablePointer<CGSize>, CFIndex)](/documentation/coretext/ctfontgetverticaltranslationsforglyphs(_:_:_:_:))

### Working With Font Variations

- [func CTFontCopyVariationAxes(CTFont) -> CFArray?](/documentation/coretext/ctfontcopyvariationaxes(_:))
- [func CTFontCopyVariation(CTFont) -> CFDictionary?](/documentation/coretext/ctfontcopyvariation(_:))

### Getting Font Features

- [func CTFontCopyFeatures(CTFont) -> CFArray?](/documentation/coretext/ctfontcopyfeatures(_:))
- [func CTFontCopyFeatureSettings(CTFont) -> CFArray?](/documentation/coretext/ctfontcopyfeaturesettings(_:))

### Working with Glyphs

- [func CTFontGetGlyphsForCharacters(CTFont, UnsafePointer<UniChar>, UnsafeMutablePointer<CGGlyph>, CFIndex) -> Bool](/documentation/coretext/ctfontgetglyphsforcharacters(_:_:_:_:))
- [func CTFontDrawGlyphs(CTFont, UnsafePointer<CGGlyph>, UnsafePointer<CGPoint>, Int, CGContext)](/documentation/coretext/ctfontdrawglyphs(_:_:_:_:_:))
- [func CTFontGetLigatureCaretPositions(CTFont, CGGlyph, UnsafeMutablePointer<CGFloat>?, CFIndex) -> CFIndex](/documentation/coretext/ctfontgetligaturecaretpositions(_:_:_:_:))

### Converting Fonts

- [func CTFontCopyGraphicsFont(CTFont, UnsafeMutablePointer<Unmanaged<CTFontDescriptor>?>?) -> CGFont](/documentation/coretext/ctfontcopygraphicsfont(_:_:))
- [func CTFontCreateWithGraphicsFont(CGFont, CGFloat, UnsafePointer<CGAffineTransform>?, CTFontDescriptor?) -> CTFont](/documentation/coretext/ctfontcreatewithgraphicsfont(_:_:_:_:))
- [func CTFontGetPlatformFont(CTFont, UnsafeMutablePointer<Unmanaged<CTFontDescriptor>?>?) -> ATSFontRef](/documentation/coretext/ctfontgetplatformfont(_:_:))
- [func CTFontCreateWithPlatformFont(ATSFontRef, CGFloat, UnsafePointer<CGAffineTransform>?, CTFontDescriptor?) -> CTFont?](/documentation/coretext/ctfontcreatewithplatformfont(_:_:_:_:))
- [func CTFontCreateWithQuickdrawInstance(ConstStr255Param?, Int16, UInt8, CGFloat) -> CTFont](/documentation/coretext/ctfontcreatewithquickdrawinstance(_:_:_:_:))

### Getting Font Table Data

- [func CTFontCopyAvailableTables(CTFont, CTFontTableOptions) -> CFArray?](/documentation/coretext/ctfontcopyavailabletables(_:_:))
- [func CTFontCopyTable(CTFont, CTFontTableTag, CTFontTableOptions) -> CFData?](/documentation/coretext/ctfontcopytable(_:_:_:))

### Getting the Type Identifier

- [func CTFontGetTypeID() -> CFTypeID](/documentation/coretext/ctfontgettypeid())

### Global Variables

- [Name Specifier Constants](/documentation/coretext/name-specifier-constants)

#### Constants

- [let kCTFontCopyrightNameKey: CFString](/documentation/coretext/kctfontcopyrightnamekey)
- [let kCTFontFamilyNameKey: CFString](/documentation/coretext/kctfontfamilynamekey)
- [let kCTFontSubFamilyNameKey: CFString](/documentation/coretext/kctfontsubfamilynamekey)
- [let kCTFontStyleNameKey: CFString](/documentation/coretext/kctfontstylenamekey)
- [let kCTFontUniqueNameKey: CFString](/documentation/coretext/kctfontuniquenamekey)
- [let kCTFontFullNameKey: CFString](/documentation/coretext/kctfontfullnamekey)
- [let kCTFontVersionNameKey: CFString](/documentation/coretext/kctfontversionnamekey)
- [let kCTFontPostScriptNameKey: CFString](/documentation/coretext/kctfontpostscriptnamekey)
- [let kCTFontTrademarkNameKey: CFString](/documentation/coretext/kctfonttrademarknamekey)
- [let kCTFontManufacturerNameKey: CFString](/documentation/coretext/kctfontmanufacturernamekey)
- [let kCTFontDesignerNameKey: CFString](/documentation/coretext/kctfontdesignernamekey)
- [let kCTFontDescriptionNameKey: CFString](/documentation/coretext/kctfontdescriptionnamekey)
- [let kCTFontVendorURLNameKey: CFString](/documentation/coretext/kctfontvendorurlnamekey)
- [let kCTFontDesignerURLNameKey: CFString](/documentation/coretext/kctfontdesignerurlnamekey)
- [let kCTFontLicenseNameKey: CFString](/documentation/coretext/kctfontlicensenamekey)
- [let kCTFontLicenseURLNameKey: CFString](/documentation/coretext/kctfontlicenseurlnamekey)
- [let kCTFontSampleTextNameKey: CFString](/documentation/coretext/kctfontsampletextnamekey)
- [let kCTFontPostScriptCIDNameKey: CFString](/documentation/coretext/kctfontpostscriptcidnamekey)
- [Font Variation Axis Dictionary Keys](/documentation/coretext/font-variation-axis-dictionary-keys)

#### Constants

- [let kCTFontVariationAxisIdentifierKey: CFString](/documentation/coretext/kctfontvariationaxisidentifierkey)
- [let kCTFontVariationAxisMinimumValueKey: CFString](/documentation/coretext/kctfontvariationaxisminimumvaluekey)
- [let kCTFontVariationAxisMaximumValueKey: CFString](/documentation/coretext/kctfontvariationaxismaximumvaluekey)
- [let kCTFontVariationAxisDefaultValueKey: CFString](/documentation/coretext/kctfontvariationaxisdefaultvaluekey)
- [let kCTFontVariationAxisNameKey: CFString](/documentation/coretext/kctfontvariationaxisnamekey)
- [let kCTFontVariationAxisHiddenKey: CFString](/documentation/coretext/kctfontvariationaxishiddenkey)
- [Font Feature Constants](/documentation/coretext/font-feature-constants)

#### Constants

- [let kCTFontFeatureTypeIdentifierKey: CFString](/documentation/coretext/kctfontfeaturetypeidentifierkey)
- [let kCTFontFeatureTypeNameKey: CFString](/documentation/coretext/kctfontfeaturetypenamekey)
- [let kCTFontFeatureTypeExclusiveKey: CFString](/documentation/coretext/kctfontfeaturetypeexclusivekey)
- [let kCTFontFeatureTypeSelectorsKey: CFString](/documentation/coretext/kctfontfeaturetypeselectorskey)
- [let kCTFontFeatureSelectorIdentifierKey: CFString](/documentation/coretext/kctfontfeatureselectoridentifierkey)
- [let kCTFontFeatureSelectorNameKey: CFString](/documentation/coretext/kctfontfeatureselectornamekey)
- [let kCTFontFeatureSelectorDefaultKey: CFString](/documentation/coretext/kctfontfeatureselectordefaultkey)
- [let kCTFontFeatureSelectorSettingKey: CFString](/documentation/coretext/kctfontfeatureselectorsettingkey)
- [let kCTFontFeatureSampleTextKey: CFString](/documentation/coretext/kctfontfeaturesampletextkey)
- [let kCTFontFeatureTooltipTextKey: CFString](/documentation/coretext/kctfontfeaturetooltiptextkey)

### Enumerations

- [CTFontUIFontType](/documentation/coretext/ctfontuifonttype)

#### Constants

- [case none](/documentation/coretext/ctfontuifonttype/none)
- [case user](/documentation/coretext/ctfontuifonttype/user)
- [case userFixedPitch](/documentation/coretext/ctfontuifonttype/userfixedpitch)
- [case system](/documentation/coretext/ctfontuifonttype/system)
- [case emphasizedSystem](/documentation/coretext/ctfontuifonttype/emphasizedsystem)
- [case smallSystem](/documentation/coretext/ctfontuifonttype/smallsystem)
- [case smallEmphasizedSystem](/documentation/coretext/ctfontuifonttype/smallemphasizedsystem)
- [case miniSystem](/documentation/coretext/ctfontuifonttype/minisystem)
- [case miniEmphasizedSystem](/documentation/coretext/ctfontuifonttype/miniemphasizedsystem)
- [case views](/documentation/coretext/ctfontuifonttype/views)
- [case application](/documentation/coretext/ctfontuifonttype/application)
- [case label](/documentation/coretext/ctfontuifonttype/label)
- [case menuTitle](/documentation/coretext/ctfontuifonttype/menutitle)
- [case menuItem](/documentation/coretext/ctfontuifonttype/menuitem)
- [case menuItemMark](/documentation/coretext/ctfontuifonttype/menuitemmark)
- [case menuItemCmdKey](/documentation/coretext/ctfontuifonttype/menuitemcmdkey)
- [case windowTitle](/documentation/coretext/ctfontuifonttype/windowtitle)
- [case pushButton](/documentation/coretext/ctfontuifonttype/pushbutton)
- [case utilityWindowTitle](/documentation/coretext/ctfontuifonttype/utilitywindowtitle)
- [case alertHeader](/documentation/coretext/ctfontuifonttype/alertheader)
- [case systemDetail](/documentation/coretext/ctfontuifonttype/systemdetail)
- [case emphasizedSystemDetail](/documentation/coretext/ctfontuifonttype/emphasizedsystemdetail)
- [case toolbar](/documentation/coretext/ctfontuifonttype/toolbar)
- [case smallToolbar](/documentation/coretext/ctfontuifonttype/smalltoolbar)
- [case message](/documentation/coretext/ctfontuifonttype/message)
- [case palette](/documentation/coretext/ctfontuifonttype/palette)
- [case toolTip](/documentation/coretext/ctfontuifonttype/tooltip)
- [case controlContent](/documentation/coretext/ctfontuifonttype/controlcontent)

#### Deprecated

- [static var kCTFontNoFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontnofonttype)
- [static var kCTFontUserFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontuserfonttype)
- [static var kCTFontUserFixedPitchFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontuserfixedpitchfonttype)
- [static var kCTFontSystemFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontsystemfonttype)
- [static var kCTFontEmphasizedSystemFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontemphasizedsystemfonttype)
- [static var kCTFontSmallSystemFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontsmallsystemfonttype)
- [static var kCTFontSmallEmphasizedSystemFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontsmallemphasizedsystemfonttype)
- [static var kCTFontMiniSystemFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontminisystemfonttype)
- [static var kCTFontMiniEmphasizedSystemFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontminiemphasizedsystemfonttype)
- [static var kCTFontViewsFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontviewsfonttype)
- [static var kCTFontApplicationFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontapplicationfonttype)
- [static var kCTFontLabelFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontlabelfonttype)
- [static var kCTFontMenuTitleFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontmenutitlefonttype)
- [static var kCTFontMenuItemFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontmenuitemfonttype)
- [static var kCTFontMenuItemMarkFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontmenuitemmarkfonttype)
- [static var kCTFontMenuItemCmdKeyFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontmenuitemcmdkeyfonttype)
- [static var kCTFontWindowTitleFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontwindowtitlefonttype)
- [static var kCTFontPushButtonFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontpushbuttonfonttype)
- [static var kCTFontUtilityWindowTitleFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontutilitywindowtitlefonttype)
- [static var kCTFontAlertHeaderFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontalertheaderfonttype)
- [static var kCTFontSystemDetailFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontsystemdetailfonttype)
- [static var kCTFontEmphasizedSystemDetailFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontemphasizedsystemdetailfonttype)
- [static var kCTFontToolbarFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfonttoolbarfonttype)
- [static var kCTFontSmallToolbarFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontsmalltoolbarfonttype)
- [static var kCTFontMessageFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontmessagefonttype)
- [static var kCTFontPaletteFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontpalettefonttype)
- [static var kCTFontToolTipFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfonttooltipfonttype)
- [static var kCTFontControlContentFontType: CTFontUIFontType](/documentation/coretext/ctfontuifonttype/kctfontcontrolcontentfonttype)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coretext/ctfontuifonttype/init(rawvalue:))
- [CTFontTableTag](/documentation/coretext/ctfonttabletag)

#### Constants

- [var kCTFontTableBASE: Int](/documentation/coretext/kctfonttablebase)
- [var kCTFontTableCFF: Int](/documentation/coretext/kctfonttablecff)
- [var kCTFontTableDSIG: Int](/documentation/coretext/kctfonttabledsig)
- [var kCTFontTableEBDT: Int](/documentation/coretext/kctfonttableebdt)
- [var kCTFontTableEBLC: Int](/documentation/coretext/kctfonttableeblc)
- [var kCTFontTableEBSC: Int](/documentation/coretext/kctfonttableebsc)
- [var kCTFontTableGDEF: Int](/documentation/coretext/kctfonttablegdef)
- [var kCTFontTableGPOS: Int](/documentation/coretext/kctfonttablegpos)
- [var kCTFontTableGSUB: Int](/documentation/coretext/kctfonttablegsub)
- [var kCTFontTableJSTF: Int](/documentation/coretext/kctfonttablejstf)
- [var kCTFontTableLTSH: Int](/documentation/coretext/kctfonttableltsh)
- [var kCTFontTableOS2: Int](/documentation/coretext/kctfonttableos2)
- [var kCTFontTablePCLT: Int](/documentation/coretext/kctfonttablepclt)
- [var kCTFontTableVDMX: Int](/documentation/coretext/kctfonttablevdmx)
- [var kCTFontTableVORG: Int](/documentation/coretext/kctfonttablevorg)
- [var kCTFontTableZapf: Int](/documentation/coretext/kctfonttablezapf)
- [var kCTFontTableAcnt: Int](/documentation/coretext/kctfonttableacnt)
- [var kCTFontTableAvar: Int](/documentation/coretext/kctfonttableavar)
- [var kCTFontTableBdat: Int](/documentation/coretext/kctfonttablebdat)
- [var kCTFontTableBhed: Int](/documentation/coretext/kctfonttablebhed)
- [var kCTFontTableBloc: Int](/documentation/coretext/kctfonttablebloc)
- [var kCTFontTableBsln: Int](/documentation/coretext/kctfonttablebsln)
- [var kCTFontTableCmap: Int](/documentation/coretext/kctfonttablecmap)
- [var kCTFontTableCvar: Int](/documentation/coretext/kctfonttablecvar)
- [var kCTFontTableCvt: Int](/documentation/coretext/kctfonttablecvt)
- [var kCTFontTableFdsc: Int](/documentation/coretext/kctfonttablefdsc)
- [var kCTFontTableFeat: Int](/documentation/coretext/kctfonttablefeat)
- [var kCTFontTableFmtx: Int](/documentation/coretext/kctfonttablefmtx)
- [var kCTFontTableFpgm: Int](/documentation/coretext/kctfonttablefpgm)
- [var kCTFontTableFvar: Int](/documentation/coretext/kctfonttablefvar)
- [var kCTFontTableGasp: Int](/documentation/coretext/kctfonttablegasp)
- [var kCTFontTableGlyf: Int](/documentation/coretext/kctfonttableglyf)
- [var kCTFontTableGvar: Int](/documentation/coretext/kctfonttablegvar)
- [var kCTFontTableHdmx: Int](/documentation/coretext/kctfonttablehdmx)
- [var kCTFontTableHead: Int](/documentation/coretext/kctfonttablehead)
- [var kCTFontTableHhea: Int](/documentation/coretext/kctfonttablehhea)
- [var kCTFontTableHmtx: Int](/documentation/coretext/kctfonttablehmtx)
- [var kCTFontTableHsty: Int](/documentation/coretext/kctfonttablehsty)
- [var kCTFontTableJust: Int](/documentation/coretext/kctfonttablejust)
- [var kCTFontTableKern: Int](/documentation/coretext/kctfonttablekern)
- [var kCTFontTableKerx: Int](/documentation/coretext/kctfonttablekerx)
- [var kCTFontTableLcar: Int](/documentation/coretext/kctfonttablelcar)
- [var kCTFontTableLoca: Int](/documentation/coretext/kctfonttableloca)
- [var kCTFontTableMaxp: Int](/documentation/coretext/kctfonttablemaxp)
- [var kCTFontTableMort: Int](/documentation/coretext/kctfonttablemort)
- [var kCTFontTableMorx: Int](/documentation/coretext/kctfonttablemorx)
- [var kCTFontTableName: Int](/documentation/coretext/kctfonttablename)
- [var kCTFontTableOpbd: Int](/documentation/coretext/kctfonttableopbd)
- [var kCTFontTablePost: Int](/documentation/coretext/kctfonttablepost)
- [var kCTFontTablePrep: Int](/documentation/coretext/kctfonttableprep)
- [var kCTFontTableProp: Int](/documentation/coretext/kctfonttableprop)
- [var kCTFontTableSbit: Int](/documentation/coretext/kctfonttablesbit)
- [var kCTFontTableSbix: Int](/documentation/coretext/kctfonttablesbix)
- [var kCTFontTableTrak: Int](/documentation/coretext/kctfonttabletrak)
- [var kCTFontTableVhea: Int](/documentation/coretext/kctfonttablevhea)
- [var kCTFontTableVmtx: Int](/documentation/coretext/kctfonttablevmtx)
- [CTFontTableOptions](/documentation/coretext/ctfonttableoptions)

#### Constants

- [init(rawValue: UInt32)](/documentation/coretext/ctfonttableoptions/init(rawvalue:))
- [static var excludeSynthetic: CTFontTableOptions](/documentation/coretext/ctfonttableoptions/excludesynthetic)
- [CTFontOptions](/documentation/coretext/ctfontoptions)

#### Constants

- [static var preventAutoActivation: CTFontOptions](/documentation/coretext/ctfontoptions/preventautoactivation)
- [static var preferSystemFont: CTFontOptions](/documentation/coretext/ctfontoptions/prefersystemfont)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/coretext/ctfontoptions/init(rawvalue:))

#### Type Properties

- [static var preventAutoDownload: CTFontOptions](/documentation/coretext/ctfontoptions/preventautodownload)

### Initializers

- [init(CTFontUIFontType, size: CGFloat)](/documentation/coretext/ctfont/init(_:size:)-3do9m)
- [init(CTFontDescriptor, size: CGFloat)](/documentation/coretext/ctfont/init(_:size:)-6lcja)
- [init(CFString, size: CGFloat)](/documentation/coretext/ctfont/init(_:size:)-8bj7b)
- [init(CTFontUIFontType, size: CGFloat, language: CFString?)](/documentation/coretext/ctfont/init(_:size:language:))
- [init(CFString, transform: CGAffineTransform)](/documentation/coretext/ctfont/init(_:transform:)-3sscp)
- [init(CTFontDescriptor, transform: CGAffineTransform)](/documentation/coretext/ctfont/init(_:transform:)-a23v)
- [init(font: CTFont, string: CFString, range: CFRange)](/documentation/coretext/ctfont/init(font:string:range:))
- [init(font: CTFont, string: CFString, range: CFRange, language: CFString?)](/documentation/coretext/ctfont/init(font:string:range:language:))
- [CTFontCollection](/documentation/coretext/ctfontcollection)

### Creating Font Collections

- [func CTFontCollectionCreateFromAvailableFonts(CFDictionary?) -> CTFontCollection](/documentation/coretext/ctfontcollectioncreatefromavailablefonts(_:))
- [func CTFontCollectionCreateWithFontDescriptors(CFArray?, CFDictionary?) -> CTFontCollection](/documentation/coretext/ctfontcollectioncreatewithfontdescriptors(_:_:))
- [func CTFontCollectionCreateCopyWithFontDescriptors(CTFontCollection, CFArray?, CFDictionary?) -> CTFontCollection](/documentation/coretext/ctfontcollectioncreatecopywithfontdescriptors(_:_:_:))
- [func CTFontCollectionCreateMutableCopy(CTFontCollection) -> CTMutableFontCollection](/documentation/coretext/ctfontcollectioncreatemutablecopy(_:))

### Excluding and Including Font Descriptors

- [func CTFontCollectionCopyExclusionDescriptors(CTFontCollection) -> CFArray?](/documentation/coretext/ctfontcollectioncopyexclusiondescriptors(_:))
- [func CTFontCollectionCopyQueryDescriptors(CTFontCollection) -> CFArray?](/documentation/coretext/ctfontcollectioncopyquerydescriptors(_:))
- [func CTFontCollectionSetExclusionDescriptors(CTMutableFontCollection, CFArray?)](/documentation/coretext/ctfontcollectionsetexclusiondescriptors(_:_:))
- [func CTFontCollectionSetQueryDescriptors(CTMutableFontCollection, CFArray?)](/documentation/coretext/ctfontcollectionsetquerydescriptors(_:_:))

### Getting Font Descriptors

- [func CTFontCollectionCreateMatchingFontDescriptors(CTFontCollection) -> CFArray?](/documentation/coretext/ctfontcollectioncreatematchingfontdescriptors(_:))
- [func CTFontCollectionCreateMatchingFontDescriptorsWithOptions(CTFontCollection, CFDictionary?) -> CFArray?](/documentation/coretext/ctfontcollectioncreatematchingfontdescriptorswithoptions(_:_:))
- [func CTFontCollectionCreateMatchingFontDescriptorsSortedWithCallback(CTFontCollection, CTFontCollectionSortDescriptorsCallback?, UnsafeMutableRawPointer?) -> CFArray?](/documentation/coretext/ctfontcollectioncreatematchingfontdescriptorssortedwithcallback(_:_:_:))
- [func CTFontCollectionCreateMatchingFontDescriptorsForFamily(CTFontCollection, CFString, CFDictionary?) -> CFArray?](/documentation/coretext/ctfontcollectioncreatematchingfontdescriptorsforfamily(_:_:_:))
- [CTFontCollectionSortDescriptorsCallback](/documentation/coretext/ctfontcollectionsortdescriptorscallback)

### Get Font Descriptor Attributes

- [func CTFontCollectionCopyFontAttribute(CTFontCollection, CFString, CTFontCollectionCopyOptions) -> CFArray](/documentation/coretext/ctfontcollectioncopyfontattribute(_:_:_:))
- [func CTFontCollectionCopyFontAttributes(CTFontCollection, CFSet, CTFontCollectionCopyOptions) -> CFArray](/documentation/coretext/ctfontcollectioncopyfontattributes(_:_:_:))

### Getting the Type Identifier

- [func CTFontCollectionGetTypeID() -> CFTypeID](/documentation/coretext/ctfontcollectiongettypeid())

### Data Types

- [CTMutableFontCollection](/documentation/coretext/ctmutablefontcollection)

### Constants

- [let kCTFontCollectionRemoveDuplicatesOption: CFString](/documentation/coretext/kctfontcollectionremoveduplicatesoption)
- [CTFontCollectionCopyOptions](/documentation/coretext/ctfontcollectioncopyoptions)

#### Constants

- [static var standardSort: CTFontCollectionCopyOptions](/documentation/coretext/ctfontcollectioncopyoptions/standardsort)
- [static var unique: CTFontCollectionCopyOptions](/documentation/coretext/ctfontcollectioncopyoptions/unique)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coretext/ctfontcollectioncopyoptions/init(rawvalue:))
- [CTFontDescriptor](/documentation/coretext/ctfontdescriptor)

### Creating Font Descriptors

- [func CTFontDescriptorCreateWithNameAndSize(CFString, CGFloat) -> CTFontDescriptor](/documentation/coretext/ctfontdescriptorcreatewithnameandsize(_:_:))
- [func CTFontDescriptorCreateWithAttributes(CFDictionary) -> CTFontDescriptor](/documentation/coretext/ctfontdescriptorcreatewithattributes(_:))
- [func CTFontDescriptorCreateCopyWithAttributes(CTFontDescriptor, CFDictionary) -> CTFontDescriptor](/documentation/coretext/ctfontdescriptorcreatecopywithattributes(_:_:))
- [func CTFontDescriptorCreateCopyWithVariation(CTFontDescriptor, CFNumber, CGFloat) -> CTFontDescriptor](/documentation/coretext/ctfontdescriptorcreatecopywithvariation(_:_:_:))
- [func CTFontDescriptorCreateCopyWithFeature(CTFontDescriptor, CFNumber, CFNumber) -> CTFontDescriptor](/documentation/coretext/ctfontdescriptorcreatecopywithfeature(_:_:_:))
- [func CTFontDescriptorCreateCopyWithFamily(CTFontDescriptor, CFString) -> CTFontDescriptor?](/documentation/coretext/ctfontdescriptorcreatecopywithfamily(_:_:))
- [func CTFontDescriptorCreateCopyWithSymbolicTraits(CTFontDescriptor, CTFontSymbolicTraits, CTFontSymbolicTraits) -> CTFontDescriptor?](/documentation/coretext/ctfontdescriptorcreatecopywithsymbolictraits(_:_:_:))
- [func CTFontDescriptorCreateMatchingFontDescriptors(CTFontDescriptor, CFSet?) -> CFArray?](/documentation/coretext/ctfontdescriptorcreatematchingfontdescriptors(_:_:))
- [func CTFontDescriptorCreateMatchingFontDescriptor(CTFontDescriptor, CFSet?) -> CTFontDescriptor?](/documentation/coretext/ctfontdescriptorcreatematchingfontdescriptor(_:_:))

### Getting Attributes

- [func CTFontDescriptorCopyAttributes(CTFontDescriptor) -> CFDictionary](/documentation/coretext/ctfontdescriptorcopyattributes(_:))
- [func CTFontDescriptorCopyAttribute(CTFontDescriptor, CFString) -> CFTypeRef?](/documentation/coretext/ctfontdescriptorcopyattribute(_:_:))
- [func CTFontDescriptorCopyLocalizedAttribute(CTFontDescriptor, CFString, UnsafeMutablePointer<Unmanaged<CFString>?>?) -> CFTypeRef?](/documentation/coretext/ctfontdescriptorcopylocalizedattribute(_:_:_:))

### Getting the Font Descriptor Type

- [func CTFontDescriptorGetTypeID() -> CFTypeID](/documentation/coretext/ctfontdescriptorgettypeid())

### Accessing Font Attributes

- [Font Attributes](/documentation/coretext/font-attributes)

#### Font Attribute Keys

- [let kCTFontURLAttribute: CFString](/documentation/coretext/kctfonturlattribute)
- [let kCTFontNameAttribute: CFString](/documentation/coretext/kctfontnameattribute)
- [let kCTFontDisplayNameAttribute: CFString](/documentation/coretext/kctfontdisplaynameattribute)
- [let kCTFontFamilyNameAttribute: CFString](/documentation/coretext/kctfontfamilynameattribute)
- [let kCTFontStyleNameAttribute: CFString](/documentation/coretext/kctfontstylenameattribute)
- [let kCTFontTraitsAttribute: CFString](/documentation/coretext/kctfonttraitsattribute)
- [let kCTFontVariationAttribute: CFString](/documentation/coretext/kctfontvariationattribute)
- [let kCTFontSizeAttribute: CFString](/documentation/coretext/kctfontsizeattribute)
- [let kCTFontMatrixAttribute: CFString](/documentation/coretext/kctfontmatrixattribute)
- [let kCTFontCascadeListAttribute: CFString](/documentation/coretext/kctfontcascadelistattribute)
- [let kCTFontCharacterSetAttribute: CFString](/documentation/coretext/kctfontcharactersetattribute)
- [let kCTFontLanguagesAttribute: CFString](/documentation/coretext/kctfontlanguagesattribute)
- [let kCTFontBaselineAdjustAttribute: CFString](/documentation/coretext/kctfontbaselineadjustattribute)
- [let kCTFontMacintoshEncodingsAttribute: CFString](/documentation/coretext/kctfontmacintoshencodingsattribute)
- [let kCTFontFeaturesAttribute: CFString](/documentation/coretext/kctfontfeaturesattribute)
- [let kCTFontFeatureSettingsAttribute: CFString](/documentation/coretext/kctfontfeaturesettingsattribute)
- [let kCTFontFixedAdvanceAttribute: CFString](/documentation/coretext/kctfontfixedadvanceattribute)
- [let kCTFontOrientationAttribute: CFString](/documentation/coretext/kctfontorientationattribute)
- [let kCTFontFormatAttribute: CFString](/documentation/coretext/kctfontformatattribute)
- [let kCTFontRegistrationScopeAttribute: CFString](/documentation/coretext/kctfontregistrationscopeattribute)
- [let kCTFontPriorityAttribute: CFString](/documentation/coretext/kctfontpriorityattribute)
- [let kCTFontEnabledAttribute: CFString](/documentation/coretext/kctfontenabledattribute)
- [let kCTFontDownloadableAttribute: CFString](/documentation/coretext/kctfontdownloadableattribute)
- [let kCTFontDownloadedAttribute: CFString](/documentation/coretext/kctfontdownloadedattribute)
- [CTFontOrientation](/documentation/coretext/ctfontorientation)

#### Font Orientations

- [case `default`](/documentation/coretext/ctfontorientation/default)
- [case horizontal](/documentation/coretext/ctfontorientation/horizontal)
- [case vertical](/documentation/coretext/ctfontorientation/vertical)

#### Deprecated Constants

- [static var kCTFontDefaultOrientation: CTFontOrientation](/documentation/coretext/ctfontorientation/kctfontdefaultorientation)
- [static var kCTFontHorizontalOrientation: CTFontOrientation](/documentation/coretext/ctfontorientation/kctfonthorizontalorientation)
- [static var kCTFontVerticalOrientation: CTFontOrientation](/documentation/coretext/ctfontorientation/kctfontverticalorientation)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coretext/ctfontorientation/init(rawvalue:))
- [CTFontFormat](/documentation/coretext/ctfontformat)

#### Font Formats

- [case unrecognized](/documentation/coretext/ctfontformat/unrecognized)
- [case openTypePostScript](/documentation/coretext/ctfontformat/opentypepostscript)
- [case openTypeTrueType](/documentation/coretext/ctfontformat/opentypetruetype)
- [case trueType](/documentation/coretext/ctfontformat/truetype)
- [case postScript](/documentation/coretext/ctfontformat/postscript)
- [case bitmap](/documentation/coretext/ctfontformat/bitmap)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coretext/ctfontformat/init(rawvalue:))
- [CTFontPriority](/documentation/coretext/ctfontpriority)

#### Font Priority

- [var kCTFontPrioritySystem: Int](/documentation/coretext/kctfontprioritysystem)
- [var kCTFontPriorityNetwork: Int](/documentation/coretext/kctfontprioritynetwork)
- [var kCTFontPriorityComputer: Int](/documentation/coretext/kctfontprioritycomputer)
- [var kCTFontPriorityUser: Int](/documentation/coretext/kctfontpriorityuser)
- [var kCTFontPriorityDynamic: Int](/documentation/coretext/kctfontprioritydynamic)
- [var kCTFontPriorityProcess: Int](/documentation/coretext/kctfontpriorityprocess)

### Accessing Font Traits

- [Font Traits](/documentation/coretext/font-traits)

#### Font Trait Keys

- [let kCTFontSymbolicTrait: CFString](/documentation/coretext/kctfontsymbolictrait)
- [let kCTFontWeightTrait: CFString](/documentation/coretext/kctfontweighttrait)
- [let kCTFontWidthTrait: CFString](/documentation/coretext/kctfontwidthtrait)
- [let kCTFontSlantTrait: CFString](/documentation/coretext/kctfontslanttrait)
- [Font Class Mask Shift Constants](/documentation/coretext/font-class-mask-shift-constants)

#### Constants

- [var kCTFontClassMaskShift: Int](/documentation/coretext/kctfontclassmaskshift)
- [CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coretext/ctfontsymbolictraits/init(rawvalue:))

#### Symbolic Traits

- [static var traitItalic: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/traititalic)
- [static var traitBold: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/traitbold)
- [static var traitExpanded: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/traitexpanded)
- [static var traitCondensed: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/traitcondensed)
- [static var traitMonoSpace: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/traitmonospace)
- [static var traitVertical: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/traitvertical)
- [static var traitUIOptimized: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/traituioptimized)
- [static var traitColorGlyphs: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/traitcolorglyphs)
- [static var traitComposite: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/traitcomposite)
- [static var traitClassMask: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/traitclassmask)

#### Deprecated Constants

- [static var italicTrait: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/italictrait)
- [static var boldTrait: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/boldtrait)
- [static var expandedTrait: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/expandedtrait)
- [static var condensedTrait: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/condensedtrait)
- [static var monoSpaceTrait: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/monospacetrait)
- [static var verticalTrait: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/verticaltrait)
- [static var uiOptimizedTrait: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/uioptimizedtrait)
- [static var colorGlyphsTrait: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/colorglyphstrait)
- [static var compositeTrait: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/compositetrait)
- [static var classMaskTrait: CTFontSymbolicTraits](/documentation/coretext/ctfontsymbolictraits/classmasktrait)
- [CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coretext/ctfontstylisticclass/init(rawvalue:))

#### Stylistic Classes

- [static var classOldStyleSerifs: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/classoldstyleserifs)
- [static var classTransitionalSerifs: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/classtransitionalserifs)
- [static var classModernSerifs: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/classmodernserifs)
- [static var classClarendonSerifs: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/classclarendonserifs)
- [static var classSlabSerifs: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/classslabserifs)
- [static var classFreeformSerifs: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/classfreeformserifs)
- [static var classSansSerif: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/classsansserif)
- [static var classOrnamentals: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/classornamentals)
- [static var classScripts: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/classscripts)
- [static var classSymbolic: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/classsymbolic)

#### Deprecated Constants

- [static var oldStyleSerifsClass: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/oldstyleserifsclass)
- [static var transitionalSerifsClass: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/transitionalserifsclass)
- [static var modernSerifsClass: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/modernserifsclass)
- [static var clarendonSerifsClass: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/clarendonserifsclass)
- [static var slabSerifsClass: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/slabserifsclass)
- [static var freeformSerifsClass: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/freeformserifsclass)
- [static var sansSerifClass: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/sansserifclass)
- [static var ornamentalsClass: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/ornamentalsclass)
- [static var scriptsClass: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/scriptsclass)
- [static var symbolicClass: CTFontStylisticClass](/documentation/coretext/ctfontstylisticclass/symbolicclass)
- [CTFrame](/documentation/coretext/ctframe)

### Getting Frame Data

- [func CTFrameGetStringRange(CTFrame) -> CFRange](/documentation/coretext/ctframegetstringrange(_:))
- [func CTFrameGetVisibleStringRange(CTFrame) -> CFRange](/documentation/coretext/ctframegetvisiblestringrange(_:))
- [func CTFrameGetPath(CTFrame) -> CGPath](/documentation/coretext/ctframegetpath(_:))
- [func CTFrameGetFrameAttributes(CTFrame) -> CFDictionary?](/documentation/coretext/ctframegetframeattributes(_:))

### Getting Lines

- [func CTFrameGetLines(CTFrame) -> CFArray](/documentation/coretext/ctframegetlines(_:))
- [func CTFrameGetLineOrigins(CTFrame, CFRange, UnsafeMutablePointer<CGPoint>)](/documentation/coretext/ctframegetlineorigins(_:_:_:))

### Drawing the Frame

- [func CTFrameDraw(CTFrame, CGContext)](/documentation/coretext/ctframedraw(_:_:))

### Getting the Type Identifier

- [func CTFrameGetTypeID() -> CFTypeID](/documentation/coretext/ctframegettypeid())

### Data Types

- [CTFramePathFillRule](/documentation/coretext/ctframepathfillrule)

#### Enumeration Cases

- [case evenOdd](/documentation/coretext/ctframepathfillrule/evenodd)
- [case windingNumber](/documentation/coretext/ctframepathfillrule/windingnumber)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coretext/ctframepathfillrule/init(rawvalue:))

### Constants

- [CTFrameProgression](/documentation/coretext/ctframeprogression)

#### Constants

- [case topToBottom](/documentation/coretext/ctframeprogression/toptobottom)
- [case rightToLeft](/documentation/coretext/ctframeprogression/righttoleft)
- [case leftToRight](/documentation/coretext/ctframeprogression/lefttoright)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coretext/ctframeprogression/init(rawvalue:))
- [let kCTFrameProgressionAttributeName: CFString](/documentation/coretext/kctframeprogressionattributename)
- [let kCTFramePathFillRuleAttributeName: CFString](/documentation/coretext/kctframepathfillruleattributename)
- [let kCTFramePathWidthAttributeName: CFString](/documentation/coretext/kctframepathwidthattributename)
- [let kCTFrameClippingPathsAttributeName: CFString](/documentation/coretext/kctframeclippingpathsattributename)
- [let kCTFramePathClippingPathAttributeName: CFString](/documentation/coretext/kctframepathclippingpathattributename)
- [CTFramesetter](/documentation/coretext/ctframesetter)

### Creating a Framesetter

- [func CTFramesetterCreateWithAttributedString(CFAttributedString) -> CTFramesetter](/documentation/coretext/ctframesettercreatewithattributedstring(_:))
- [func CTFramesetterCreateWithTypesetter(CTTypesetter) -> CTFramesetter](/documentation/coretext/ctframesettercreatewithtypesetter(_:))

### Creating Frames

- [func CTFramesetterCreateFrame(CTFramesetter, CFRange, CGPath, CFDictionary?) -> CTFrame](/documentation/coretext/ctframesettercreateframe(_:_:_:_:))
- [func CTFramesetterGetTypesetter(CTFramesetter) -> CTTypesetter](/documentation/coretext/ctframesettergettypesetter(_:))

### Frame Sizing

- [func CTFramesetterSuggestFrameSizeWithConstraints(CTFramesetter, CFRange, CFDictionary?, CGSize, UnsafeMutablePointer<CFRange>?) -> CGSize](/documentation/coretext/ctframesettersuggestframesizewithconstraints(_:_:_:_:_:))

### Getting the Type Identifier

- [func CTFramesetterGetTypeID() -> CFTypeID](/documentation/coretext/ctframesettergettypeid())
- [CTGlyphInfo](/documentation/coretext/ctglyphinfo)

### Getting the GlyphInfo Type

- [func CTGlyphInfoGetTypeID() -> CFTypeID](/documentation/coretext/ctglyphinfogettypeid())

### Creating GlyphInfo Objects

- [func CTGlyphInfoCreateWithGlyphName(CFString, CTFont, CFString) -> CTGlyphInfo?](/documentation/coretext/ctglyphinfocreatewithglyphname(_:_:_:))
- [func CTGlyphInfoCreateWithGlyph(CGGlyph, CTFont, CFString) -> CTGlyphInfo?](/documentation/coretext/ctglyphinfocreatewithglyph(_:_:_:))
- [func CTGlyphInfoCreateWithCharacterIdentifier(CGFontIndex, CTCharacterCollection, CFString) -> CTGlyphInfo?](/documentation/coretext/ctglyphinfocreatewithcharacteridentifier(_:_:_:))

### Getting GlyphInfo Data

- [func CTGlyphInfoGetGlyphName(CTGlyphInfo) -> CFString?](/documentation/coretext/ctglyphinfogetglyphname(_:))
- [func CTGlyphInfoGetCharacterIdentifier(CTGlyphInfo) -> CGFontIndex](/documentation/coretext/ctglyphinfogetcharacteridentifier(_:))
- [func CTGlyphInfoGetCharacterCollection(CTGlyphInfo) -> CTCharacterCollection](/documentation/coretext/ctglyphinfogetcharactercollection(_:))
- [func CTGlyphInfoGetGlyph(CTGlyphInfo) -> CGGlyph](/documentation/coretext/ctglyphinfogetglyph(_:))

### Constants

- [CTCharacterCollection](/documentation/coretext/ctcharactercollection)

#### Constants

- [case identityMapping](/documentation/coretext/ctcharactercollection/identitymapping)
- [case adobeCNS1](/documentation/coretext/ctcharactercollection/adobecns1)
- [case adobeGB1](/documentation/coretext/ctcharactercollection/adobegb1)
- [case adobeJapan1](/documentation/coretext/ctcharactercollection/adobejapan1)
- [case adobeJapan2](/documentation/coretext/ctcharactercollection/adobejapan2)
- [case adobeKorea1](/documentation/coretext/ctcharactercollection/adobekorea1)

#### Deprecated

- [static var kCTIdentityMappingCharacterCollection: CTCharacterCollection](/documentation/coretext/ctcharactercollection/kctidentitymappingcharactercollection)
- [static var kCTAdobeCNS1CharacterCollection: CTCharacterCollection](/documentation/coretext/ctcharactercollection/kctadobecns1charactercollection)
- [static var kCTAdobeGB1CharacterCollection: CTCharacterCollection](/documentation/coretext/ctcharactercollection/kctadobegb1charactercollection)
- [static var kCTAdobeJapan1CharacterCollection: CTCharacterCollection](/documentation/coretext/ctcharactercollection/kctadobejapan1charactercollection)
- [static var kCTAdobeJapan2CharacterCollection: CTCharacterCollection](/documentation/coretext/ctcharactercollection/kctadobejapan2charactercollection)
- [static var kCTAdobeKorea1CharacterCollection: CTCharacterCollection](/documentation/coretext/ctcharactercollection/kctadobekorea1charactercollection)

#### Initializers

- [init?(rawValue: UInt16)](/documentation/coretext/ctcharactercollection/init(rawvalue:))
- [CTLine](/documentation/coretext/ctline)

### Creating Lines

- [func CTLineCreateWithAttributedString(CFAttributedString) -> CTLine](/documentation/coretext/ctlinecreatewithattributedstring(_:))
- [func CTLineCreateTruncatedLine(CTLine, Double, CTLineTruncationType, CTLine?) -> CTLine?](/documentation/coretext/ctlinecreatetruncatedline(_:_:_:_:))
- [func CTLineCreateJustifiedLine(CTLine, CGFloat, Double) -> CTLine?](/documentation/coretext/ctlinecreatejustifiedline(_:_:_:))

### Drawing the Line

- [func CTLineDraw(CTLine, CGContext)](/documentation/coretext/ctlinedraw(_:_:))

### Getting Line Data

- [func CTLineGetGlyphCount(CTLine) -> CFIndex](/documentation/coretext/ctlinegetglyphcount(_:))
- [func CTLineGetGlyphRuns(CTLine) -> CFArray](/documentation/coretext/ctlinegetglyphruns(_:))
- [func CTLineGetStringRange(CTLine) -> CFRange](/documentation/coretext/ctlinegetstringrange(_:))
- [func CTLineGetPenOffsetForFlush(CTLine, CGFloat, Double) -> Double](/documentation/coretext/ctlinegetpenoffsetforflush(_:_:_:))

### Measuring Lines

- [func CTLineGetImageBounds(CTLine, CGContext?) -> CGRect](/documentation/coretext/ctlinegetimagebounds(_:_:))
- [func CTLineGetTypographicBounds(CTLine, UnsafeMutablePointer<CGFloat>?, UnsafeMutablePointer<CGFloat>?, UnsafeMutablePointer<CGFloat>?) -> Double](/documentation/coretext/ctlinegettypographicbounds(_:_:_:_:))
- [func CTLineGetTrailingWhitespaceWidth(CTLine) -> Double](/documentation/coretext/ctlinegettrailingwhitespacewidth(_:))

### Getting Line Positioning

- [func CTLineGetStringIndexForPosition(CTLine, CGPoint) -> CFIndex](/documentation/coretext/ctlinegetstringindexforposition(_:_:))
- [func CTLineGetOffsetForStringIndex(CTLine, CFIndex, UnsafeMutablePointer<CGFloat>?) -> CGFloat](/documentation/coretext/ctlinegetoffsetforstringindex(_:_:_:))
- [func CTLineEnumerateCaretOffsets(CTLine, (Double, CFIndex, Bool, UnsafeMutablePointer<Bool>) -> Void)](/documentation/coretext/ctlineenumeratecaretoffsets(_:_:))

### Getting the Type Identifier

- [func CTLineGetTypeID() -> CFTypeID](/documentation/coretext/ctlinegettypeid())

### Constants

- [CTLineTruncationType](/documentation/coretext/ctlinetruncationtype)

#### Constants

- [case start](/documentation/coretext/ctlinetruncationtype/start)
- [case end](/documentation/coretext/ctlinetruncationtype/end)
- [case middle](/documentation/coretext/ctlinetruncationtype/middle)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coretext/ctlinetruncationtype/init(rawvalue:))
- [CTParagraphStyle](/documentation/coretext/ctparagraphstyle)

### Creating Paragraph Styles

- [func CTParagraphStyleCreate(UnsafePointer<CTParagraphStyleSetting>?, Int) -> CTParagraphStyle](/documentation/coretext/ctparagraphstylecreate(_:_:))
- [func CTParagraphStyleCreateCopy(CTParagraphStyle) -> CTParagraphStyle](/documentation/coretext/ctparagraphstylecreatecopy(_:))

### Getting the Value of a Style Specifier

- [func CTParagraphStyleGetValueForSpecifier(CTParagraphStyle, CTParagraphStyleSpecifier, Int, UnsafeMutableRawPointer) -> Bool](/documentation/coretext/ctparagraphstylegetvalueforspecifier(_:_:_:_:))

### Getting the Type Identifier

- [func CTParagraphStyleGetTypeID() -> CFTypeID](/documentation/coretext/ctparagraphstylegettypeid())

### Data Types

- [CTParagraphStyleSetting](/documentation/coretext/ctparagraphstylesetting)

#### Initializers

- [init(spec: CTParagraphStyleSpecifier, valueSize: Int, value: UnsafeRawPointer)](/documentation/coretext/ctparagraphstylesetting/init(spec:valuesize:value:))

#### Instance Properties

- [var spec: CTParagraphStyleSpecifier](/documentation/coretext/ctparagraphstylesetting/spec)
- [var value: UnsafeRawPointer](/documentation/coretext/ctparagraphstylesetting/value)
- [var valueSize: Int](/documentation/coretext/ctparagraphstylesetting/valuesize)

### Constants

- [CTTextAlignment](/documentation/coretext/cttextalignment)

#### Constants

- [case left](/documentation/coretext/cttextalignment/left)
- [case right](/documentation/coretext/cttextalignment/right)
- [case center](/documentation/coretext/cttextalignment/center)
- [case justified](/documentation/coretext/cttextalignment/justified)
- [case natural](/documentation/coretext/cttextalignment/natural)

#### Initializers

- [init(NSTextAlignment)](/documentation/coretext/cttextalignment/init(_:))
- [init?(rawValue: UInt8)](/documentation/coretext/cttextalignment/init(rawvalue:))

#### Deprecated

- [static var kCTLeftTextAlignment: CTTextAlignment](/documentation/coretext/cttextalignment/kctlefttextalignment)
- [static var kCTRightTextAlignment: CTTextAlignment](/documentation/coretext/cttextalignment/kctrighttextalignment)
- [static var kCTCenterTextAlignment: CTTextAlignment](/documentation/coretext/cttextalignment/kctcentertextalignment)
- [static var kCTJustifiedTextAlignment: CTTextAlignment](/documentation/coretext/cttextalignment/kctjustifiedtextalignment)
- [static var kCTNaturalTextAlignment: CTTextAlignment](/documentation/coretext/cttextalignment/kctnaturaltextalignment)
- [CTLineBreakMode](/documentation/coretext/ctlinebreakmode)

#### Constants

- [case byWordWrapping](/documentation/coretext/ctlinebreakmode/bywordwrapping)
- [case byCharWrapping](/documentation/coretext/ctlinebreakmode/bycharwrapping)
- [case byClipping](/documentation/coretext/ctlinebreakmode/byclipping)
- [case byTruncatingHead](/documentation/coretext/ctlinebreakmode/bytruncatinghead)
- [case byTruncatingTail](/documentation/coretext/ctlinebreakmode/bytruncatingtail)
- [case byTruncatingMiddle](/documentation/coretext/ctlinebreakmode/bytruncatingmiddle)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/coretext/ctlinebreakmode/init(rawvalue:))
- [CTWritingDirection](/documentation/coretext/ctwritingdirection)

#### Constants

- [case natural](/documentation/coretext/ctwritingdirection/natural)
- [case leftToRight](/documentation/coretext/ctwritingdirection/lefttoright)
- [case rightToLeft](/documentation/coretext/ctwritingdirection/righttoleft)

#### Initializers

- [init?(rawValue: Int8)](/documentation/coretext/ctwritingdirection/init(rawvalue:))
- [CTParagraphStyleSpecifier](/documentation/coretext/ctparagraphstylespecifier)

#### Constants

- [case alignment](/documentation/coretext/ctparagraphstylespecifier/alignment)
- [case firstLineHeadIndent](/documentation/coretext/ctparagraphstylespecifier/firstlineheadindent)
- [case headIndent](/documentation/coretext/ctparagraphstylespecifier/headindent)
- [case tailIndent](/documentation/coretext/ctparagraphstylespecifier/tailindent)
- [case tabStops](/documentation/coretext/ctparagraphstylespecifier/tabstops)
- [case defaultTabInterval](/documentation/coretext/ctparagraphstylespecifier/defaulttabinterval)
- [case lineBreakMode](/documentation/coretext/ctparagraphstylespecifier/linebreakmode)
- [case lineHeightMultiple](/documentation/coretext/ctparagraphstylespecifier/lineheightmultiple)
- [case maximumLineHeight](/documentation/coretext/ctparagraphstylespecifier/maximumlineheight)
- [case minimumLineHeight](/documentation/coretext/ctparagraphstylespecifier/minimumlineheight)
- [case lineSpacing](/documentation/coretext/ctparagraphstylespecifier/linespacing)
- [case paragraphSpacing](/documentation/coretext/ctparagraphstylespecifier/paragraphspacing)
- [case paragraphSpacingBefore](/documentation/coretext/ctparagraphstylespecifier/paragraphspacingbefore)
- [case baseWritingDirection](/documentation/coretext/ctparagraphstylespecifier/basewritingdirection)
- [case maximumLineSpacing](/documentation/coretext/ctparagraphstylespecifier/maximumlinespacing)
- [case minimumLineSpacing](/documentation/coretext/ctparagraphstylespecifier/minimumlinespacing)
- [case lineSpacingAdjustment](/documentation/coretext/ctparagraphstylespecifier/linespacingadjustment)
- [case count](/documentation/coretext/ctparagraphstylespecifier/count)

#### Enumeration Cases

- [case lineBoundsOptions](/documentation/coretext/ctparagraphstylespecifier/lineboundsoptions)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coretext/ctparagraphstylespecifier/init(rawvalue:))
- [CTRun](/documentation/coretext/ctrun)

### Getting Glyph Run Data

- [func CTRunGetGlyphCount(CTRun) -> CFIndex](/documentation/coretext/ctrungetglyphcount(_:))
- [func CTRunGetAttributes(CTRun) -> CFDictionary](/documentation/coretext/ctrungetattributes(_:))
- [func CTRunGetStatus(CTRun) -> CTRunStatus](/documentation/coretext/ctrungetstatus(_:))
- [func CTRunGetGlyphsPtr(CTRun) -> UnsafePointer<CGGlyph>?](/documentation/coretext/ctrungetglyphsptr(_:))
- [func CTRunGetGlyphs(CTRun, CFRange, UnsafeMutablePointer<CGGlyph>)](/documentation/coretext/ctrungetglyphs(_:_:_:))
- [func CTRunGetPositionsPtr(CTRun) -> UnsafePointer<CGPoint>?](/documentation/coretext/ctrungetpositionsptr(_:))
- [func CTRunGetPositions(CTRun, CFRange, UnsafeMutablePointer<CGPoint>)](/documentation/coretext/ctrungetpositions(_:_:_:))
- [func CTRunGetAdvancesPtr(CTRun) -> UnsafePointer<CGSize>?](/documentation/coretext/ctrungetadvancesptr(_:))
- [func CTRunGetAdvances(CTRun, CFRange, UnsafeMutablePointer<CGSize>)](/documentation/coretext/ctrungetadvances(_:_:_:))
- [func CTRunGetStringIndicesPtr(CTRun) -> UnsafePointer<CFIndex>?](/documentation/coretext/ctrungetstringindicesptr(_:))
- [func CTRunGetStringIndices(CTRun, CFRange, UnsafeMutablePointer<CFIndex>)](/documentation/coretext/ctrungetstringindices(_:_:_:))
- [func CTRunGetStringRange(CTRun) -> CFRange](/documentation/coretext/ctrungetstringrange(_:))

### Measuring the Glyph Run

- [func CTLineGetBoundsWithOptions(CTLine, CTLineBoundsOptions) -> CGRect](/documentation/coretext/ctlinegetboundswithoptions(_:_:))
- [func CTRunGetTypographicBounds(CTRun, CFRange, UnsafeMutablePointer<CGFloat>?, UnsafeMutablePointer<CGFloat>?, UnsafeMutablePointer<CGFloat>?) -> Double](/documentation/coretext/ctrungettypographicbounds(_:_:_:_:_:))
- [func CTRunGetImageBounds(CTRun, CGContext?, CFRange) -> CGRect](/documentation/coretext/ctrungetimagebounds(_:_:_:))
- [func CTRunGetBaseAdvancesAndOrigins(CTRun, CFRange, UnsafeMutablePointer<CGSize>?, UnsafeMutablePointer<CGPoint>?)](/documentation/coretext/ctrungetbaseadvancesandorigins(_:_:_:_:))

### Drawing the Glyph Run

- [func CTRunDraw(CTRun, CGContext, CFRange)](/documentation/coretext/ctrundraw(_:_:_:))
- [func CTRunGetTextMatrix(CTRun) -> CGAffineTransform](/documentation/coretext/ctrungettextmatrix(_:))

### Getting the Type Identifier

- [func CTRunGetTypeID() -> CFTypeID](/documentation/coretext/ctrungettypeid())

### Constants

- [CTRunStatus](/documentation/coretext/ctrunstatus)

#### Constants

- [static var rightToLeft: CTRunStatus](/documentation/coretext/ctrunstatus/righttoleft)
- [static var nonMonotonic: CTRunStatus](/documentation/coretext/ctrunstatus/nonmonotonic)
- [static var hasNonIdentityMatrix: CTRunStatus](/documentation/coretext/ctrunstatus/hasnonidentitymatrix)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coretext/ctrunstatus/init(rawvalue:))
- [CTRunDelegate](/documentation/coretext/ctrundelegate)

### Creating a Run Delegate

- [func CTRunDelegateCreate(UnsafePointer<CTRunDelegateCallbacks>, UnsafeMutableRawPointer?) -> CTRunDelegate?](/documentation/coretext/ctrundelegatecreate(_:_:))

### Getting Information About a Run Delegate

- [func CTRunDelegateGetRefCon(CTRunDelegate) -> UnsafeMutableRawPointer](/documentation/coretext/ctrundelegategetrefcon(_:))
- [func CTRunDelegateGetTypeID() -> CFTypeID](/documentation/coretext/ctrundelegategettypeid())

### Callbacks

- [CTRunDelegateGetAscentCallback](/documentation/coretext/ctrundelegategetascentcallback)
- [CTRunDelegateGetDescentCallback](/documentation/coretext/ctrundelegategetdescentcallback)
- [CTRunDelegateGetWidthCallback](/documentation/coretext/ctrundelegategetwidthcallback)
- [CTRunDelegateDeallocateCallback](/documentation/coretext/ctrundelegatedeallocatecallback)

### Data Types

- [CTRunDelegateCallbacks](/documentation/coretext/ctrundelegatecallbacks)

#### Initializers

- [init(version: CFIndex, dealloc: CTRunDelegateDeallocateCallback, getAscent: CTRunDelegateGetAscentCallback, getDescent: CTRunDelegateGetDescentCallback, getWidth: CTRunDelegateGetWidthCallback)](/documentation/coretext/ctrundelegatecallbacks/init(version:dealloc:getascent:getdescent:getwidth:))

#### Instance Properties

- [var dealloc: CTRunDelegateDeallocateCallback](/documentation/coretext/ctrundelegatecallbacks/dealloc)
- [var getAscent: CTRunDelegateGetAscentCallback](/documentation/coretext/ctrundelegatecallbacks/getascent)
- [var getDescent: CTRunDelegateGetDescentCallback](/documentation/coretext/ctrundelegatecallbacks/getdescent)
- [var getWidth: CTRunDelegateGetWidthCallback](/documentation/coretext/ctrundelegatecallbacks/getwidth)
- [var version: CFIndex](/documentation/coretext/ctrundelegatecallbacks/version)

### Constants

- [Run Delegate Versions](/documentation/coretext/1498177-run-delegate-versions)

#### Constants

- [var kCTRunDelegateVersion1: Int](/documentation/coretext/kctrundelegateversion1)
- [var kCTRunDelegateCurrentVersion: Int](/documentation/coretext/kctrundelegatecurrentversion)
- [CTTextTab](/documentation/coretext/cttexttab)

### Creating Text Tabs

- [func CTTextTabCreate(CTTextAlignment, Double, CFDictionary?) -> CTTextTab](/documentation/coretext/cttexttabcreate(_:_:_:))

### Getting Text Tab Data

- [func CTTextTabGetAlignment(CTTextTab) -> CTTextAlignment](/documentation/coretext/cttexttabgetalignment(_:))
- [func CTTextTabGetLocation(CTTextTab) -> Double](/documentation/coretext/cttexttabgetlocation(_:))
- [func CTTextTabGetOptions(CTTextTab) -> CFDictionary?](/documentation/coretext/cttexttabgetoptions(_:))

### Getting the Type Identifier

- [func CTTextTabGetTypeID() -> CFTypeID](/documentation/coretext/cttexttabgettypeid())

### Constants

- [let kCTTabColumnTerminatorsAttributeName: CFString](/documentation/coretext/kcttabcolumnterminatorsattributename)
- [CTTypesetter](/documentation/coretext/cttypesetter)

### Creating a Typesetter

- [func CTTypesetterCreateWithAttributedString(CFAttributedString) -> CTTypesetter](/documentation/coretext/cttypesettercreatewithattributedstring(_:))
- [func CTTypesetterCreateWithAttributedStringAndOptions(CFAttributedString, CFDictionary?) -> CTTypesetter?](/documentation/coretext/cttypesettercreatewithattributedstringandoptions(_:_:))

### Creating Lines

- [func CTTypesetterCreateLine(CTTypesetter, CFRange) -> CTLine](/documentation/coretext/cttypesettercreateline(_:_:))
- [func CTTypesetterCreateLineWithOffset(CTTypesetter, CFRange, Double) -> CTLine](/documentation/coretext/cttypesettercreatelinewithoffset(_:_:_:))

### Breaking Lines

- [func CTTypesetterSuggestLineBreak(CTTypesetter, CFIndex, Double) -> CFIndex](/documentation/coretext/cttypesettersuggestlinebreak(_:_:_:))
- [func CTTypesetterSuggestLineBreakWithOffset(CTTypesetter, CFIndex, Double, Double) -> CFIndex](/documentation/coretext/cttypesettersuggestlinebreakwithoffset(_:_:_:_:))
- [func CTTypesetterSuggestClusterBreak(CTTypesetter, CFIndex, Double) -> CFIndex](/documentation/coretext/cttypesettersuggestclusterbreak(_:_:_:))
- [func CTTypesetterSuggestClusterBreakWithOffset(CTTypesetter, CFIndex, Double, Double) -> CFIndex](/documentation/coretext/cttypesettersuggestclusterbreakwithoffset(_:_:_:_:))

### Getting the Type Identifier

- [func CTTypesetterGetTypeID() -> CFTypeID](/documentation/coretext/cttypesettergettypeid())

### Constants

- [Typesetter Options](/documentation/coretext/typesetter-options)

#### Constants

- [let kCTTypesetterOptionForcedEmbeddingLevel: CFString](/documentation/coretext/kcttypesetteroptionforcedembeddinglevel)
- [let kCTTypesetterOptionAllowUnboundedLayout: CFString](/documentation/coretext/kcttypesetteroptionallowunboundedlayout)
- [let kCTTypesetterOptionDisableBidiProcessing: CFString](/documentation/coretext/kcttypesetteroptiondisablebidiprocessing)

## Reference

- [Styling Attributed Strings](/documentation/coretext/styling-attributed-strings)

### Constants

- [String Attribute Name Constants](/documentation/coretext/string-attribute-name-constants)

#### Constants

- [let kCTCharacterShapeAttributeName: CFString](/documentation/coretext/kctcharactershapeattributename)
- [let kCTFontAttributeName: CFString](/documentation/coretext/kctfontattributename)
- [let kCTKernAttributeName: CFString](/documentation/coretext/kctkernattributename)
- [let kCTLigatureAttributeName: CFString](/documentation/coretext/kctligatureattributename)
- [let kCTForegroundColorAttributeName: CFString](/documentation/coretext/kctforegroundcolorattributename)
- [let kCTForegroundColorFromContextAttributeName: CFString](/documentation/coretext/kctforegroundcolorfromcontextattributename)
- [let kCTParagraphStyleAttributeName: CFString](/documentation/coretext/kctparagraphstyleattributename)
- [let kCTStrokeWidthAttributeName: CFString](/documentation/coretext/kctstrokewidthattributename)
- [let kCTStrokeColorAttributeName: CFString](/documentation/coretext/kctstrokecolorattributename)
- [let kCTSuperscriptAttributeName: CFString](/documentation/coretext/kctsuperscriptattributename)
- [let kCTUnderlineColorAttributeName: CFString](/documentation/coretext/kctunderlinecolorattributename)
- [let kCTUnderlineStyleAttributeName: CFString](/documentation/coretext/kctunderlinestyleattributename)
- [let kCTVerticalFormsAttributeName: CFString](/documentation/coretext/kctverticalformsattributename)
- [let kCTGlyphInfoAttributeName: CFString](/documentation/coretext/kctglyphinfoattributename)
- [let kCTRunDelegateAttributeName: CFString](/documentation/coretext/kctrundelegateattributename)
- [let kCTBaselineOffsetAttributeName: CFString](/documentation/coretext/kctbaselineoffsetattributename)
- [let kCTTrackingAttributeName: CFString](/documentation/coretext/kcttrackingattributename)
- [CTUnderlineStyle](/documentation/coretext/ctunderlinestyle)

#### Constants

- [static var single: CTUnderlineStyle](/documentation/coretext/ctunderlinestyle/single)
- [static var thick: CTUnderlineStyle](/documentation/coretext/ctunderlinestyle/thick)
- [static var double: CTUnderlineStyle](/documentation/coretext/ctunderlinestyle/double)

#### Initializers

- [init(rawValue: Int32)](/documentation/coretext/ctunderlinestyle/init(rawvalue:))
- [CTUnderlineStyleModifiers](/documentation/coretext/ctunderlinestylemodifiers)

#### Constants

- [static var patternSolid: CTUnderlineStyleModifiers](/documentation/coretext/ctunderlinestylemodifiers/patternsolid)
- [static var patternDot: CTUnderlineStyleModifiers](/documentation/coretext/ctunderlinestylemodifiers/patterndot)
- [static var patternDash: CTUnderlineStyleModifiers](/documentation/coretext/ctunderlinestylemodifiers/patterndash)
- [static var patternDashDot: CTUnderlineStyleModifiers](/documentation/coretext/ctunderlinestylemodifiers/patterndashdot)
- [static var patternDashDotDot: CTUnderlineStyleModifiers](/documentation/coretext/ctunderlinestylemodifiers/patterndashdotdot)

#### Initializers

- [init(rawValue: Int32)](/documentation/coretext/ctunderlinestylemodifiers/init(rawvalue:))
- [Core Text Structures](/documentation/coretext/core-text-structures)

### Structures

- [CTLineBoundsOptions](/documentation/coretext/ctlineboundsoptions)

#### Line Bounds Options

- [static var excludeTypographicLeading: CTLineBoundsOptions](/documentation/coretext/ctlineboundsoptions/excludetypographicleading)
- [static var excludeTypographicShifts: CTLineBoundsOptions](/documentation/coretext/ctlineboundsoptions/excludetypographicshifts)
- [static var includeLanguageExtents: CTLineBoundsOptions](/documentation/coretext/ctlineboundsoptions/includelanguageextents)
- [static var useGlyphPathBounds: CTLineBoundsOptions](/documentation/coretext/ctlineboundsoptions/useglyphpathbounds)
- [static var useHangingPunctuation: CTLineBoundsOptions](/documentation/coretext/ctlineboundsoptions/usehangingpunctuation)
- [static var useOpticalBounds: CTLineBoundsOptions](/documentation/coretext/ctlineboundsoptions/useopticalbounds)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/coretext/ctlineboundsoptions/init(rawvalue:))
- [LtagStringRange](/documentation/coretext/ltagstringrange)

#### Initializers

- [init()](/documentation/coretext/ltagstringrange/init())
- [init(offset: UInt16, length: UInt16)](/documentation/coretext/ltagstringrange/init(offset:length:))

#### Instance Properties

- [var length: UInt16](/documentation/coretext/ltagstringrange/length)
- [var offset: UInt16](/documentation/coretext/ltagstringrange/offset)
- [LtagTable](/documentation/coretext/ltagtable)

#### Initializers

- [init()](/documentation/coretext/ltagtable/init())
- [init(version: UInt32, flags: UInt32, numTags: UInt32, tagRange: LtagStringRange)](/documentation/coretext/ltagtable/init(version:flags:numtags:tagrange:))

#### Instance Properties

- [var flags: UInt32](/documentation/coretext/ltagtable/flags)
- [var numTags: UInt32](/documentation/coretext/ltagtable/numtags)
- [var tagRange: LtagStringRange](/documentation/coretext/ltagtable/tagrange)
- [var version: UInt32](/documentation/coretext/ltagtable/version)
- [SFNTLookupVectorHeader](/documentation/coretext/sfntlookupvectorheader)

#### Initializers

- [init()](/documentation/coretext/sfntlookupvectorheader/init())
- [init(valueSize: UInt16, firstGlyph: UInt16, count: UInt16, values: UInt8)](/documentation/coretext/sfntlookupvectorheader/init(valuesize:firstglyph:count:values:))

#### Instance Properties

- [var count: UInt16](/documentation/coretext/sfntlookupvectorheader/count)
- [var firstGlyph: UInt16](/documentation/coretext/sfntlookupvectorheader/firstglyph)
- [var valueSize: UInt16](/documentation/coretext/sfntlookupvectorheader/valuesize)
- [var values: UInt8](/documentation/coretext/sfntlookupvectorheader/values)
- [Core Text Enumerations](/documentation/coretext/core-text-enumerations)

### Enumerations

- [CTFontDescriptorMatchingState](/documentation/coretext/ctfontdescriptormatchingstate)

#### Constants

- [case didBegin](/documentation/coretext/ctfontdescriptormatchingstate/didbegin)
- [case didFinish](/documentation/coretext/ctfontdescriptormatchingstate/didfinish)
- [case willBeginQuerying](/documentation/coretext/ctfontdescriptormatchingstate/willbeginquerying)
- [case stalled](/documentation/coretext/ctfontdescriptormatchingstate/stalled)
- [case willBeginDownloading](/documentation/coretext/ctfontdescriptormatchingstate/willbegindownloading)
- [case downloading](/documentation/coretext/ctfontdescriptormatchingstate/downloading)
- [case didFinishDownloading](/documentation/coretext/ctfontdescriptormatchingstate/didfinishdownloading)
- [case didMatch](/documentation/coretext/ctfontdescriptormatchingstate/didmatch)
- [case didFailWithError](/documentation/coretext/ctfontdescriptormatchingstate/didfailwitherror)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coretext/ctfontdescriptormatchingstate/init(rawvalue:))
- [CTFontManagerAutoActivationSetting](/documentation/coretext/ctfontmanagerautoactivationsetting)

#### Constants

- [case `default`](/documentation/coretext/ctfontmanagerautoactivationsetting/default)
- [case disabled](/documentation/coretext/ctfontmanagerautoactivationsetting/disabled)
- [case enabled](/documentation/coretext/ctfontmanagerautoactivationsetting/enabled)
- [case promptUser](/documentation/coretext/ctfontmanagerautoactivationsetting/promptuser)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coretext/ctfontmanagerautoactivationsetting/init(rawvalue:))
- [CTFontManagerError](/documentation/coretext/ctfontmanagererror)

#### Constants

- [case fileNotFound](/documentation/coretext/ctfontmanagererror/filenotfound)
- [case insufficientPermissions](/documentation/coretext/ctfontmanagererror/insufficientpermissions)
- [case unrecognizedFormat](/documentation/coretext/ctfontmanagererror/unrecognizedformat)
- [case invalidFontData](/documentation/coretext/ctfontmanagererror/invalidfontdata)
- [case alreadyRegistered](/documentation/coretext/ctfontmanagererror/alreadyregistered)
- [case exceededResourceLimit](/documentation/coretext/ctfontmanagererror/exceededresourcelimit)
- [case assetNotFound](/documentation/coretext/ctfontmanagererror/assetnotfound)
- [case notRegistered](/documentation/coretext/ctfontmanagererror/notregistered)
- [case inUse](/documentation/coretext/ctfontmanagererror/inuse)
- [case systemRequired](/documentation/coretext/ctfontmanagererror/systemrequired)
- [case registrationFailed](/documentation/coretext/ctfontmanagererror/registrationfailed)
- [case missingEntitlement](/documentation/coretext/ctfontmanagererror/missingentitlement)
- [case insufficientInfo](/documentation/coretext/ctfontmanagererror/insufficientinfo)
- [case cancelledByUser](/documentation/coretext/ctfontmanagererror/cancelledbyuser)
- [case duplicatedName](/documentation/coretext/ctfontmanagererror/duplicatedname)
- [case invalidFilePath](/documentation/coretext/ctfontmanagererror/invalidfilepath)
- [case unsupportedScope](/documentation/coretext/ctfontmanagererror/unsupportedscope)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/coretext/ctfontmanagererror/init(rawvalue:))
- [CTFontManagerScope](/documentation/coretext/ctfontmanagerscope)

#### Constants

- [case none](/documentation/coretext/ctfontmanagerscope/none)
- [case process](/documentation/coretext/ctfontmanagerscope/process)
- [case persistent](/documentation/coretext/ctfontmanagerscope/persistent)
- [case session](/documentation/coretext/ctfontmanagerscope/session)
- [static var user: CTFontManagerScope](/documentation/coretext/ctfontmanagerscope/user)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coretext/ctfontmanagerscope/init(rawvalue:))
- [CTLineBoundsOptions](/documentation/coretext/ctlineboundsoptions)

#### Line Bounds Options

- [static var excludeTypographicLeading: CTLineBoundsOptions](/documentation/coretext/ctlineboundsoptions/excludetypographicleading)
- [static var excludeTypographicShifts: CTLineBoundsOptions](/documentation/coretext/ctlineboundsoptions/excludetypographicshifts)
- [static var includeLanguageExtents: CTLineBoundsOptions](/documentation/coretext/ctlineboundsoptions/includelanguageextents)
- [static var useGlyphPathBounds: CTLineBoundsOptions](/documentation/coretext/ctlineboundsoptions/useglyphpathbounds)
- [static var useHangingPunctuation: CTLineBoundsOptions](/documentation/coretext/ctlineboundsoptions/usehangingpunctuation)
- [static var useOpticalBounds: CTLineBoundsOptions](/documentation/coretext/ctlineboundsoptions/useopticalbounds)

#### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/coretext/ctlineboundsoptions/init(rawvalue:))
- [CTRubyAlignment](/documentation/coretext/ctrubyalignment)

#### Constants

- [case auto](/documentation/coretext/ctrubyalignment/auto)
- [case start](/documentation/coretext/ctrubyalignment/start)
- [case center](/documentation/coretext/ctrubyalignment/center)
- [case end](/documentation/coretext/ctrubyalignment/end)
- [case distributeLetter](/documentation/coretext/ctrubyalignment/distributeletter)
- [case distributeSpace](/documentation/coretext/ctrubyalignment/distributespace)
- [case lineEdge](/documentation/coretext/ctrubyalignment/lineedge)
- [case invalid](/documentation/coretext/ctrubyalignment/invalid)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/coretext/ctrubyalignment/init(rawvalue:))
- [CTRubyOverhang](/documentation/coretext/ctrubyoverhang)

#### Constants

- [case auto](/documentation/coretext/ctrubyoverhang/auto)
- [case start](/documentation/coretext/ctrubyoverhang/start)
- [case end](/documentation/coretext/ctrubyoverhang/end)
- [case none](/documentation/coretext/ctrubyoverhang/none)
- [case invalid](/documentation/coretext/ctrubyoverhang/invalid)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/coretext/ctrubyoverhang/init(rawvalue:))
- [CTRubyPosition](/documentation/coretext/ctrubyposition)

#### Constants

- [case before](/documentation/coretext/ctrubyposition/before)
- [case after](/documentation/coretext/ctrubyposition/after)
- [case interCharacter](/documentation/coretext/ctrubyposition/intercharacter)
- [case inline](/documentation/coretext/ctrubyposition/inline)
- [case count](/documentation/coretext/ctrubyposition/count)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/coretext/ctrubyposition/init(rawvalue:))
- [Core Text Constants](/documentation/coretext/core-text-constants)

### Constants

- [var ATSFONTREF_DEFINED: Int32](/documentation/coretext/atsfontref_defined)
- [var kBSLNIdeographicHighBaseline: Int](/documentation/coretext/kbslnideographichighbaseline)
- [let kCTAdaptiveImageProviderAttributeName: CFString](/documentation/coretext/kctadaptiveimageproviderattributename)
- [let kCTBackgroundColorAttributeName: CFString](/documentation/coretext/kctbackgroundcolorattributename)
- [let kCTBaselineClassAttributeName: CFString](/documentation/coretext/kctbaselineclassattributename)
- [let kCTBaselineClassHanging: CFString](/documentation/coretext/kctbaselineclasshanging)
- [let kCTBaselineClassIdeographicCentered: CFString](/documentation/coretext/kctbaselineclassideographiccentered)
- [let kCTBaselineClassIdeographicHigh: CFString](/documentation/coretext/kctbaselineclassideographichigh)
- [let kCTBaselineClassIdeographicLow: CFString](/documentation/coretext/kctbaselineclassideographiclow)
- [let kCTBaselineClassMath: CFString](/documentation/coretext/kctbaselineclassmath)
- [let kCTBaselineClassRoman: CFString](/documentation/coretext/kctbaselineclassroman)
- [let kCTBaselineInfoAttributeName: CFString](/documentation/coretext/kctbaselineinfoattributename)
- [let kCTBaselineOriginalFont: CFString](/documentation/coretext/kctbaselineoriginalfont)
- [let kCTBaselineReferenceFont: CFString](/documentation/coretext/kctbaselinereferencefont)
- [let kCTBaselineReferenceInfoAttributeName: CFString](/documentation/coretext/kctbaselinereferenceinfoattributename)
- [let kCTFontCollectionDisallowAutoActivationOption: CFString](/documentation/coretext/kctfontcollectiondisallowautoactivationoption)
- [let kCTFontCollectionIncludeDisabledFontsOption: CFString](/documentation/coretext/kctfontcollectionincludedisabledfontsoption)
- [let kCTFontDescriptorMatchingCurrentAssetSize: CFString](/documentation/coretext/kctfontdescriptormatchingcurrentassetsize)
- [let kCTFontDescriptorMatchingDescriptors: CFString](/documentation/coretext/kctfontdescriptormatchingdescriptors)
- [let kCTFontDescriptorMatchingError: CFString](/documentation/coretext/kctfontdescriptormatchingerror)
- [let kCTFontDescriptorMatchingPercentage: CFString](/documentation/coretext/kctfontdescriptormatchingpercentage)
- [let kCTFontDescriptorMatchingResult: CFString](/documentation/coretext/kctfontdescriptormatchingresult)
- [let kCTFontDescriptorMatchingSourceDescriptor: CFString](/documentation/coretext/kctfontdescriptormatchingsourcedescriptor)
- [let kCTFontDescriptorMatchingTotalAssetSize: CFString](/documentation/coretext/kctfontdescriptormatchingtotalassetsize)
- [let kCTFontDescriptorMatchingTotalDownloadedSize: CFString](/documentation/coretext/kctfontdescriptormatchingtotaldownloadedsize)
- [let kCTFontDownloadableAttribute: CFString](/documentation/coretext/kctfontdownloadableattribute)
- [let kCTFontDownloadedAttribute: CFString](/documentation/coretext/kctfontdownloadedattribute)
- [let kCTFontManagerBundleIdentifier: CFString](/documentation/coretext/kctfontmanagerbundleidentifier)
- [let kCTFontManagerErrorDomain: CFString](/documentation/coretext/kctfontmanagererrordomain)
- [let kCTFontManagerErrorFontAssetNameKey: CFString](/documentation/coretext/kctfontmanagererrorfontassetnamekey)
- [let kCTFontManagerErrorFontDescriptorsKey: CFString](/documentation/coretext/kctfontmanagererrorfontdescriptorskey)
- [let kCTFontManagerErrorFontURLsKey: CFString](/documentation/coretext/kctfontmanagererrorfonturlskey)
- [let kCTFontManagerRegisteredFontsChangedNotification: CFString](/documentation/coretext/kctfontmanagerregisteredfontschangednotification)
- [let kCTFontOpenTypeFeatureTag: CFString](/documentation/coretext/kctfontopentypefeaturetag)
- [let kCTFontOpenTypeFeatureValue: CFString](/documentation/coretext/kctfontopentypefeaturevalue)
- [let kCTFontOpticalSizeAttribute: CFString](/documentation/coretext/kctfontopticalsizeattribute)
- [let kCTFontRegistrationUserInfoAttribute: CFString](/documentation/coretext/kctfontregistrationuserinfoattribute)
- [var kCTFontTableAnkr: Int](/documentation/coretext/kctfonttableankr)
- [var kCTFontTableLtag: Int](/documentation/coretext/kctfonttableltag)
- [var kCTFontTableMATH: Int](/documentation/coretext/kctfonttablemath)
- [let kCTFontVariationAxesAttribute: CFString](/documentation/coretext/kctfontvariationaxesattribute)
- [let kCTHorizontalInVerticalFormsAttributeName: CFString](/documentation/coretext/kcthorizontalinverticalformsattributename)
- [let kCTLanguageAttributeName: CFString](/documentation/coretext/kctlanguageattributename)
- [let kCTRubyAnnotationAttributeName: CFString](/documentation/coretext/kctrubyannotationattributename)
- [let kCTRubyAnnotationScaleToFitAttributeName: CFString](/documentation/coretext/kctrubyannotationscaletofitattributename)
- [let kCTRubyAnnotationSizeFactorAttributeName: CFString](/documentation/coretext/kctrubyannotationsizefactorattributename)
- [var kCTVersionNumber10_10: Int32](/documentation/coretext/kctversionnumber10_10)
- [var kCTVersionNumber10_11: Int32](/documentation/coretext/kctversionnumber10_11)
- [var kCTVersionNumber10_12: Int32](/documentation/coretext/kctversionnumber10_12)
- [var kCTVersionNumber10_13: Int32](/documentation/coretext/kctversionnumber10_13)
- [var kCTVersionNumber10_14: Int32](/documentation/coretext/kctversionnumber10_14)
- [var kCTVersionNumber10_15: Int32](/documentation/coretext/kctversionnumber10_15)
- [var kCTVersionNumber10_5_2: Int32](/documentation/coretext/kctversionnumber10_5_2)
- [var kCTVersionNumber10_5_3: Int32](/documentation/coretext/kctversionnumber10_5_3)
- [var kCTVersionNumber10_5_5: Int32](/documentation/coretext/kctversionnumber10_5_5)
- [var kCTVersionNumber10_5: Int32](/documentation/coretext/kctversionnumber10_5)
- [var kCTVersionNumber10_6: Int32](/documentation/coretext/kctversionnumber10_6)
- [var kCTVersionNumber10_7: Int32](/documentation/coretext/kctversionnumber10_7)
- [var kCTVersionNumber10_8: Int32](/documentation/coretext/kctversionnumber10_8)
- [var kCTVersionNumber10_9: Int32](/documentation/coretext/kctversionnumber10_9)
- [var kCTVersionNumber11_0: Int32](/documentation/coretext/kctversionnumber11_0)
- [let kCTWritingDirectionAttributeName: CFString](/documentation/coretext/kctwritingdirectionattributename)
- [var kCTWritingDirectionEmbedding: Int](/documentation/coretext/kctwritingdirectionembedding)
- [var kCTWritingDirectionOverride: Int](/documentation/coretext/kctwritingdirectionoverride)
- [var kKERXDescending: Int](/documentation/coretext/kkerxdescending)
- [var kKERXValuesAreLong: Int](/documentation/coretext/kkerxvaluesarelong)
- [var kLanguageTagType: Int](/documentation/coretext/klanguagetagtype)
- [var kLTAGCurrentVersion: Int](/documentation/coretext/kltagcurrentversion)
- [var kMORXCoverLogicalOrder: Int](/documentation/coretext/kmorxcoverlogicalorder)
- [var kSTKCrossStreamReset: Int](/documentation/coretext/kstkcrossstreamreset)
- [Core Text Functions](/documentation/coretext/core-text-functions)

### Functions

- [func CTFontDescriptorMatchFontDescriptorsWithProgressHandler(CFArray, CFSet?, CTFontDescriptorProgressHandler) -> Bool](/documentation/coretext/ctfontdescriptormatchfontdescriptorswithprogresshandler(_:_:_:))
- [func CTFontManagerCompareFontFamilyNames(UnsafeRawPointer, UnsafeRawPointer, UnsafeMutableRawPointer?) -> CFComparisonResult](/documentation/coretext/ctfontmanagercomparefontfamilynames(_:_:_:))
- [func CTFontManagerCopyAvailableFontFamilyNames() -> CFArray](/documentation/coretext/ctfontmanagercopyavailablefontfamilynames())
- [func CTFontManagerCopyAvailableFontURLs() -> CFArray](/documentation/coretext/ctfontmanagercopyavailablefonturls())
- [func CTFontManagerCopyAvailablePostScriptNames() -> CFArray](/documentation/coretext/ctfontmanagercopyavailablepostscriptnames())
- [func CTFontManagerCreateFontDescriptorFromData(CFData) -> CTFontDescriptor?](/documentation/coretext/ctfontmanagercreatefontdescriptorfromdata(_:))
- [func CTFontManagerCreateFontDescriptorsFromURL(CFURL) -> CFArray?](/documentation/coretext/ctfontmanagercreatefontdescriptorsfromurl(_:))
- [func CTFontManagerCreateFontRequestRunLoopSource(CFIndex, (CFDictionary, pid_t) -> Unmanaged<CFArray>) -> CFRunLoopSource?](/documentation/coretext/ctfontmanagercreatefontrequestrunloopsource(_:_:))
- [func CTFontManagerEnableFontDescriptors(CFArray, Bool)](/documentation/coretext/ctfontmanagerenablefontdescriptors(_:_:))
- [func CTFontManagerGetAutoActivationSetting(CFString?) -> CTFontManagerAutoActivationSetting](/documentation/coretext/ctfontmanagergetautoactivationsetting(_:))
- [func CTFontManagerGetScopeForURL(CFURL) -> CTFontManagerScope](/documentation/coretext/ctfontmanagergetscopeforurl(_:))
- [func CTFontManagerIsSupportedFont(CFURL) -> Bool](/documentation/coretext/ctfontmanagerissupportedfont(_:))
- [func CTFontManagerRegisterFontsForURL(CFURL, CTFontManagerScope, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Bool](/documentation/coretext/ctfontmanagerregisterfontsforurl(_:_:_:))
- [func CTFontManagerRegisterFontsForURLs(CFArray, CTFontManagerScope, UnsafeMutablePointer<Unmanaged<CFArray>?>?) -> Bool](/documentation/coretext/ctfontmanagerregisterfontsforurls(_:_:_:))
- [func CTFontManagerRegisterGraphicsFont(CGFont, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Bool](/documentation/coretext/ctfontmanagerregistergraphicsfont(_:_:))
- [func CTFontManagerSetAutoActivationSetting(CFString?, CTFontManagerAutoActivationSetting)](/documentation/coretext/ctfontmanagersetautoactivationsetting(_:_:))
- [func CTFontManagerUnregisterFontsForURL(CFURL, CTFontManagerScope, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Bool](/documentation/coretext/ctfontmanagerunregisterfontsforurl(_:_:_:))
- [func CTFontManagerUnregisterFontsForURLs(CFArray, CTFontManagerScope, UnsafeMutablePointer<Unmanaged<CFArray>?>?) -> Bool](/documentation/coretext/ctfontmanagerunregisterfontsforurls(_:_:_:))
- [func CTFontManagerUnregisterGraphicsFont(CGFont, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Bool](/documentation/coretext/ctfontmanagerunregistergraphicsfont(_:_:))
- [func CTFontManagerCopyRegisteredFontDescriptors(CTFontManagerScope, Bool) -> CFArray](/documentation/coretext/ctfontmanagercopyregisteredfontdescriptors(_:_:))
- [func CTFontManagerCreateFontDescriptorsFromData(CFData) -> CFArray](/documentation/coretext/ctfontmanagercreatefontdescriptorsfromdata(_:))
- [func CTFontManagerRegisterFontDescriptors(CFArray, CTFontManagerScope, Bool, ((CFArray, Bool) -> Bool)?)](/documentation/coretext/ctfontmanagerregisterfontdescriptors(_:_:_:_:))
- [func CTFontManagerRegisterFontURLs(CFArray, CTFontManagerScope, Bool, ((CFArray, Bool) -> Bool)?)](/documentation/coretext/ctfontmanagerregisterfonturls(_:_:_:_:))
- [func CTFontManagerRegisterFontsWithAssetNames(CFArray, CFBundle?, CTFontManagerScope, Bool, ((CFArray, Bool) -> Bool)?)](/documentation/coretext/ctfontmanagerregisterfontswithassetnames(_:_:_:_:_:))
- [func CTFontManagerRequestFonts(CFArray, (CFArray) -> Void)](/documentation/coretext/ctfontmanagerrequestfonts(_:_:))
- [func CTFontManagerUnregisterFontDescriptors(CFArray, CTFontManagerScope, ((CFArray, Bool) -> Bool)?)](/documentation/coretext/ctfontmanagerunregisterfontdescriptors(_:_:_:))
- [func CTFontManagerUnregisterFontURLs(CFArray, CTFontManagerScope, ((CFArray, Bool) -> Bool)?)](/documentation/coretext/ctfontmanagerunregisterfonturls(_:_:_:))
- [func CTGetCoreTextVersion() -> UInt32](/documentation/coretext/ctgetcoretextversion())
- [func CTRubyAnnotationCreate(CTRubyAlignment, CTRubyOverhang, CGFloat, UnsafeMutablePointer<Unmanaged<CFString>?>) -> CTRubyAnnotation](/documentation/coretext/ctrubyannotationcreate(_:_:_:_:))
- [func CTRubyAnnotationCreateCopy(CTRubyAnnotation) -> CTRubyAnnotation](/documentation/coretext/ctrubyannotationcreatecopy(_:))
- [func CTRubyAnnotationCreateWithAttributes(CTRubyAlignment, CTRubyOverhang, CTRubyPosition, CFString, CFDictionary) -> CTRubyAnnotation](/documentation/coretext/ctrubyannotationcreatewithattributes(_:_:_:_:_:))
- [func CTRubyAnnotationGetAlignment(CTRubyAnnotation) -> CTRubyAlignment](/documentation/coretext/ctrubyannotationgetalignment(_:))
- [func CTRubyAnnotationGetOverhang(CTRubyAnnotation) -> CTRubyOverhang](/documentation/coretext/ctrubyannotationgetoverhang(_:))
- [func CTRubyAnnotationGetSizeFactor(CTRubyAnnotation) -> CGFloat](/documentation/coretext/ctrubyannotationgetsizefactor(_:))
- [func CTRubyAnnotationGetTextForPosition(CTRubyAnnotation, CTRubyPosition) -> CFString?](/documentation/coretext/ctrubyannotationgettextforposition(_:_:))
- [func CTRubyAnnotationGetTypeID() -> CFTypeID](/documentation/coretext/ctrubyannotationgettypeid())
- [func CTFontCopyNameForGlyph(CTFont, CGGlyph) -> CFString?](/documentation/coretext/ctfontcopynameforglyph(_:_:))
- [func CTFontDrawImageFromAdaptiveImageProviderAtPoint(CTFont, any CTAdaptiveImageProviding, CGPoint, CGContext)](/documentation/coretext/ctfontdrawimagefromadaptiveimageprovideratpoint(_:_:_:_:))
- [func CTFontGetTypographicBoundsForAdaptiveImageProvider(CTFont, (any CTAdaptiveImageProviding)?) -> CGRect](/documentation/coretext/ctfontgettypographicboundsforadaptiveimageprovider(_:_:))
- [func CTFontHasTable(CTFont, CTFontTableTag) -> Bool](/documentation/coretext/ctfonthastable(_:_:))
- [Core Text Data Types](/documentation/coretext/core-text-data-types)

### Data Types

- [ATSFontRef](/documentation/coretext/atsfontref)
- [CTFontCollectionSortDescriptorsCallback](/documentation/coretext/ctfontcollectionsortdescriptorscallback)
- [CTFontDescriptorProgressHandler](/documentation/coretext/ctfontdescriptorprogresshandler)
- [SFNT Support](/documentation/coretext/sfnt-support)

### Structures

- [AnchorPoint](/documentation/coretext/anchorpoint)

#### Initializers

- [init()](/documentation/coretext/anchorpoint/init())
- [init(x: Int16, y: Int16)](/documentation/coretext/anchorpoint/init(x:y:))

#### Instance Properties

- [var x: Int16](/documentation/coretext/anchorpoint/x)
- [var y: Int16](/documentation/coretext/anchorpoint/y)
- [AnchorPointTable](/documentation/coretext/anchorpointtable)

#### Initializers

- [init()](/documentation/coretext/anchorpointtable/init())
- [init(nPoints: UInt32, points: AnchorPoint)](/documentation/coretext/anchorpointtable/init(npoints:points:))

#### Instance Properties

- [var nPoints: UInt32](/documentation/coretext/anchorpointtable/npoints)
- [var points: AnchorPoint](/documentation/coretext/anchorpointtable/points)
- [AnkrTable](/documentation/coretext/ankrtable)

#### Initializers

- [init()](/documentation/coretext/ankrtable/init())
- [init(version: UInt16, flags: UInt16, lookupTableOffset: UInt32, anchorPointTableOffset: UInt32)](/documentation/coretext/ankrtable/init(version:flags:lookuptableoffset:anchorpointtableoffset:))

#### Instance Properties

- [var anchorPointTableOffset: UInt32](/documentation/coretext/ankrtable/anchorpointtableoffset)
- [var flags: UInt16](/documentation/coretext/ankrtable/flags)
- [var lookupTableOffset: UInt32](/documentation/coretext/ankrtable/lookuptableoffset)
- [var version: UInt16](/documentation/coretext/ankrtable/version)
- [BslnFormat0Part](/documentation/coretext/bslnformat0part)

#### Initializers

- [init()](/documentation/coretext/bslnformat0part/init())
- [init(deltas: (Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16))](/documentation/coretext/bslnformat0part/init(deltas:))

#### Instance Properties

- [var deltas: (Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16)](/documentation/coretext/bslnformat0part/deltas)
- [BslnFormat1Part](/documentation/coretext/bslnformat1part)

#### Initializers

- [init()](/documentation/coretext/bslnformat1part/init())
- [init(deltas: (Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16), mappingData: SFNTLookupTable)](/documentation/coretext/bslnformat1part/init(deltas:mappingdata:))

#### Instance Properties

- [var deltas: (Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16)](/documentation/coretext/bslnformat1part/deltas)
- [var mappingData: SFNTLookupTable](/documentation/coretext/bslnformat1part/mappingdata)
- [BslnFormat2Part](/documentation/coretext/bslnformat2part)

#### Initializers

- [init()](/documentation/coretext/bslnformat2part/init())
- [init(stdGlyph: UInt16, ctlPoints: (Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16))](/documentation/coretext/bslnformat2part/init(stdglyph:ctlpoints:))

#### Instance Properties

- [var ctlPoints: (Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16)](/documentation/coretext/bslnformat2part/ctlpoints)
- [var stdGlyph: UInt16](/documentation/coretext/bslnformat2part/stdglyph)
- [BslnFormat3Part](/documentation/coretext/bslnformat3part)

#### Initializers

- [init()](/documentation/coretext/bslnformat3part/init())
- [init(stdGlyph: UInt16, ctlPoints: (Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16), mappingData: SFNTLookupTable)](/documentation/coretext/bslnformat3part/init(stdglyph:ctlpoints:mappingdata:))

#### Instance Properties

- [var ctlPoints: (Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16, Int16)](/documentation/coretext/bslnformat3part/ctlpoints)
- [var mappingData: SFNTLookupTable](/documentation/coretext/bslnformat3part/mappingdata)
- [var stdGlyph: UInt16](/documentation/coretext/bslnformat3part/stdglyph)
- [BslnFormatUnion](/documentation/coretext/bslnformatunion)

#### Initializers

- [init()](/documentation/coretext/bslnformatunion/init())
- [init(fmt0Part: BslnFormat0Part)](/documentation/coretext/bslnformatunion/init(fmt0part:))
- [init(fmt1Part: BslnFormat1Part)](/documentation/coretext/bslnformatunion/init(fmt1part:))
- [init(fmt2Part: BslnFormat2Part)](/documentation/coretext/bslnformatunion/init(fmt2part:))
- [init(fmt3Part: BslnFormat3Part)](/documentation/coretext/bslnformatunion/init(fmt3part:))

#### Instance Properties

- [var fmt0Part: BslnFormat0Part](/documentation/coretext/bslnformatunion/fmt0part)
- [var fmt1Part: BslnFormat1Part](/documentation/coretext/bslnformatunion/fmt1part)
- [var fmt2Part: BslnFormat2Part](/documentation/coretext/bslnformatunion/fmt2part)
- [var fmt3Part: BslnFormat3Part](/documentation/coretext/bslnformatunion/fmt3part)
- [BslnTable](/documentation/coretext/bslntable)

#### Initializers

- [init()](/documentation/coretext/bslntable/init())
- [init(version: Fixed, format: BslnTableFormat, defaultBaseline: UInt16, parts: BslnFormatUnion)](/documentation/coretext/bslntable/init(version:format:defaultbaseline:parts:))

#### Instance Properties

- [var defaultBaseline: UInt16](/documentation/coretext/bslntable/defaultbaseline)
- [var format: BslnTableFormat](/documentation/coretext/bslntable/format)
- [var parts: BslnFormatUnion](/documentation/coretext/bslntable/parts)
- [var version: Fixed](/documentation/coretext/bslntable/version)
- [FontVariation](/documentation/coretext/fontvariation)

#### Initializers

- [init()](/documentation/coretext/fontvariation/init())
- [init(name: FourCharCode, value: Fixed)](/documentation/coretext/fontvariation/init(name:value:))

#### Instance Properties

- [var name: FourCharCode](/documentation/coretext/fontvariation/name)
- [var value: Fixed](/documentation/coretext/fontvariation/value)
- [JustDirectionTable](/documentation/coretext/justdirectiontable)

#### Initializers

- [init()](/documentation/coretext/justdirectiontable/init())
- [init(justClass: UInt16, widthDeltaClusters: UInt16, postcomp: UInt16, lookup: SFNTLookupTable)](/documentation/coretext/justdirectiontable/init(justclass:widthdeltaclusters:postcomp:lookup:))

#### Instance Properties

- [var justClass: UInt16](/documentation/coretext/justdirectiontable/justclass)
- [var lookup: SFNTLookupTable](/documentation/coretext/justdirectiontable/lookup)
- [var postcomp: UInt16](/documentation/coretext/justdirectiontable/postcomp)
- [var widthDeltaClusters: UInt16](/documentation/coretext/justdirectiontable/widthdeltaclusters)
- [JustPCAction](/documentation/coretext/justpcaction)

#### Initializers

- [init()](/documentation/coretext/justpcaction/init())
- [init(actionCount: UInt32, actions: JustPCActionSubrecord)](/documentation/coretext/justpcaction/init(actioncount:actions:))

#### Instance Properties

- [var actionCount: UInt32](/documentation/coretext/justpcaction/actioncount)
- [var actions: JustPCActionSubrecord](/documentation/coretext/justpcaction/actions)
- [JustPCActionSubrecord](/documentation/coretext/justpcactionsubrecord)

#### Initializers

- [init()](/documentation/coretext/justpcactionsubrecord/init())
- [init(theClass: UInt16, theType: JustPCActionType, length: UInt32, data: UInt32)](/documentation/coretext/justpcactionsubrecord/init(theclass:thetype:length:data:))

#### Instance Properties

- [var data: UInt32](/documentation/coretext/justpcactionsubrecord/data)
- [var length: UInt32](/documentation/coretext/justpcactionsubrecord/length)
- [var theClass: UInt16](/documentation/coretext/justpcactionsubrecord/theclass)
- [var theType: JustPCActionType](/documentation/coretext/justpcactionsubrecord/thetype)
- [JustPCConditionalAddAction](/documentation/coretext/justpcconditionaladdaction)

#### Initializers

- [init()](/documentation/coretext/justpcconditionaladdaction/init())
- [init(substThreshold: Fixed, addGlyph: UInt16, substGlyph: UInt16)](/documentation/coretext/justpcconditionaladdaction/init(substthreshold:addglyph:substglyph:))

#### Instance Properties

- [var addGlyph: UInt16](/documentation/coretext/justpcconditionaladdaction/addglyph)
- [var substGlyph: UInt16](/documentation/coretext/justpcconditionaladdaction/substglyph)
- [var substThreshold: Fixed](/documentation/coretext/justpcconditionaladdaction/substthreshold)
- [JustPCDecompositionAction](/documentation/coretext/justpcdecompositionaction)

#### Initializers

- [init()](/documentation/coretext/justpcdecompositionaction/init())
- [init(lowerLimit: Fixed, upperLimit: Fixed, order: UInt16, count: UInt16, glyphs: UInt16)](/documentation/coretext/justpcdecompositionaction/init(lowerlimit:upperlimit:order:count:glyphs:))

#### Instance Properties

- [var count: UInt16](/documentation/coretext/justpcdecompositionaction/count)
- [var glyphs: UInt16](/documentation/coretext/justpcdecompositionaction/glyphs)
- [var lowerLimit: Fixed](/documentation/coretext/justpcdecompositionaction/lowerlimit)
- [var order: UInt16](/documentation/coretext/justpcdecompositionaction/order)
- [var upperLimit: Fixed](/documentation/coretext/justpcdecompositionaction/upperlimit)
- [JustPCDuctilityAction](/documentation/coretext/justpcductilityaction)

#### Initializers

- [init()](/documentation/coretext/justpcductilityaction/init())
- [init(ductilityAxis: UInt32, minimumLimit: Fixed, noStretchValue: Fixed, maximumLimit: Fixed)](/documentation/coretext/justpcductilityaction/init(ductilityaxis:minimumlimit:nostretchvalue:maximumlimit:))

#### Instance Properties

- [var ductilityAxis: UInt32](/documentation/coretext/justpcductilityaction/ductilityaxis)
- [var maximumLimit: Fixed](/documentation/coretext/justpcductilityaction/maximumlimit)
- [var minimumLimit: Fixed](/documentation/coretext/justpcductilityaction/minimumlimit)
- [var noStretchValue: Fixed](/documentation/coretext/justpcductilityaction/nostretchvalue)
- [JustPCGlyphRepeatAddAction](/documentation/coretext/justpcglyphrepeataddaction)

#### Initializers

- [init()](/documentation/coretext/justpcglyphrepeataddaction/init())
- [init(flags: UInt16, glyph: UInt16)](/documentation/coretext/justpcglyphrepeataddaction/init(flags:glyph:))

#### Instance Properties

- [var flags: UInt16](/documentation/coretext/justpcglyphrepeataddaction/flags)
- [var glyph: UInt16](/documentation/coretext/justpcglyphrepeataddaction/glyph)
- [JustPostcompTable](/documentation/coretext/justpostcomptable)

#### Initializers

- [init()](/documentation/coretext/justpostcomptable/init())
- [init(lookupTable: SFNTLookupTable)](/documentation/coretext/justpostcomptable/init(lookuptable:))

#### Instance Properties

- [var lookupTable: SFNTLookupTable](/documentation/coretext/justpostcomptable/lookuptable)
- [JustTable](/documentation/coretext/justtable)

#### Initializers

- [init()](/documentation/coretext/justtable/init())
- [init(version: Fixed, format: UInt16, horizHeaderOffset: UInt16, vertHeaderOffset: UInt16)](/documentation/coretext/justtable/init(version:format:horizheaderoffset:vertheaderoffset:))

#### Instance Properties

- [var format: UInt16](/documentation/coretext/justtable/format)
- [var horizHeaderOffset: UInt16](/documentation/coretext/justtable/horizheaderoffset)
- [var version: Fixed](/documentation/coretext/justtable/version)
- [var vertHeaderOffset: UInt16](/documentation/coretext/justtable/vertheaderoffset)
- [JustWidthDeltaEntry](/documentation/coretext/justwidthdeltaentry)

#### Initializers

- [init()](/documentation/coretext/justwidthdeltaentry/init())
- [init(justClass: UInt32, beforeGrowLimit: Fixed, beforeShrinkLimit: Fixed, afterGrowLimit: Fixed, afterShrinkLimit: Fixed, growFlags: JustificationFlags, shrinkFlags: JustificationFlags)](/documentation/coretext/justwidthdeltaentry/init(justclass:beforegrowlimit:beforeshrinklimit:aftergrowlimit:aftershrinklimit:growflags:shrinkflags:))

#### Instance Properties

- [var afterGrowLimit: Fixed](/documentation/coretext/justwidthdeltaentry/aftergrowlimit)
- [var afterShrinkLimit: Fixed](/documentation/coretext/justwidthdeltaentry/aftershrinklimit)
- [var beforeGrowLimit: Fixed](/documentation/coretext/justwidthdeltaentry/beforegrowlimit)
- [var beforeShrinkLimit: Fixed](/documentation/coretext/justwidthdeltaentry/beforeshrinklimit)
- [var growFlags: JustificationFlags](/documentation/coretext/justwidthdeltaentry/growflags)
- [var justClass: UInt32](/documentation/coretext/justwidthdeltaentry/justclass)
- [var shrinkFlags: JustificationFlags](/documentation/coretext/justwidthdeltaentry/shrinkflags)
- [JustWidthDeltaGroup](/documentation/coretext/justwidthdeltagroup)

#### Initializers

- [init()](/documentation/coretext/justwidthdeltagroup/init())
- [init(count: UInt32, entries: JustWidthDeltaEntry)](/documentation/coretext/justwidthdeltagroup/init(count:entries:))

#### Instance Properties

- [var count: UInt32](/documentation/coretext/justwidthdeltagroup/count)
- [var entries: JustWidthDeltaEntry](/documentation/coretext/justwidthdeltagroup/entries)
- [KernFormatSpecificHeader](/documentation/coretext/kernformatspecificheader)

#### Initializers

- [init()](/documentation/coretext/kernformatspecificheader/init())
- [init(indexArray: KernIndexArrayHeader)](/documentation/coretext/kernformatspecificheader/init(indexarray:))
- [init(orderedList: KernOrderedListHeader)](/documentation/coretext/kernformatspecificheader/init(orderedlist:))
- [init(simpleArray: KernSimpleArrayHeader)](/documentation/coretext/kernformatspecificheader/init(simplearray:))
- [init(stateTable: KernStateHeader)](/documentation/coretext/kernformatspecificheader/init(statetable:))

#### Instance Properties

- [var indexArray: KernIndexArrayHeader](/documentation/coretext/kernformatspecificheader/indexarray)
- [var orderedList: KernOrderedListHeader](/documentation/coretext/kernformatspecificheader/orderedlist)
- [var simpleArray: KernSimpleArrayHeader](/documentation/coretext/kernformatspecificheader/simplearray)
- [var stateTable: KernStateHeader](/documentation/coretext/kernformatspecificheader/statetable)
- [KernIndexArrayHeader](/documentation/coretext/kernindexarrayheader)

#### Initializers

- [init()](/documentation/coretext/kernindexarrayheader/init())
- [init(glyphCount: UInt16, kernValueCount: UInt8, leftClassCount: UInt8, rightClassCount: UInt8, flags: UInt8, kernValue: Int16, leftClass: UInt8, rightClass: UInt8, kernIndex: UInt8)](/documentation/coretext/kernindexarrayheader/init(glyphcount:kernvaluecount:leftclasscount:rightclasscount:flags:kernvalue:leftclass:rightclass:kernindex:))

#### Instance Properties

- [var flags: UInt8](/documentation/coretext/kernindexarrayheader/flags)
- [var glyphCount: UInt16](/documentation/coretext/kernindexarrayheader/glyphcount)
- [var kernIndex: UInt8](/documentation/coretext/kernindexarrayheader/kernindex)
- [var kernValue: Int16](/documentation/coretext/kernindexarrayheader/kernvalue)
- [var kernValueCount: UInt8](/documentation/coretext/kernindexarrayheader/kernvaluecount)
- [var leftClass: UInt8](/documentation/coretext/kernindexarrayheader/leftclass)
- [var leftClassCount: UInt8](/documentation/coretext/kernindexarrayheader/leftclasscount)
- [var rightClass: UInt8](/documentation/coretext/kernindexarrayheader/rightclass)
- [var rightClassCount: UInt8](/documentation/coretext/kernindexarrayheader/rightclasscount)
- [KernKerningPair](/documentation/coretext/kernkerningpair)

#### Initializers

- [init()](/documentation/coretext/kernkerningpair/init())
- [init(left: UInt16, right: UInt16)](/documentation/coretext/kernkerningpair/init(left:right:))

#### Instance Properties

- [var left: UInt16](/documentation/coretext/kernkerningpair/left)
- [var right: UInt16](/documentation/coretext/kernkerningpair/right)
- [KernOffsetTable](/documentation/coretext/kernoffsettable)

#### Initializers

- [init()](/documentation/coretext/kernoffsettable/init())
- [init(firstGlyph: UInt16, nGlyphs: UInt16, offsetTable: KernArrayOffset)](/documentation/coretext/kernoffsettable/init(firstglyph:nglyphs:offsettable:))

#### Instance Properties

- [var firstGlyph: UInt16](/documentation/coretext/kernoffsettable/firstglyph)
- [var nGlyphs: UInt16](/documentation/coretext/kernoffsettable/nglyphs)
- [var offsetTable: KernArrayOffset](/documentation/coretext/kernoffsettable/offsettable)
- [KernOrderedListEntry](/documentation/coretext/kernorderedlistentry)

#### Initializers

- [init()](/documentation/coretext/kernorderedlistentry/init())
- [init(pair: KernKerningPair, value: KernKerningValue)](/documentation/coretext/kernorderedlistentry/init(pair:value:))

#### Instance Properties

- [var pair: KernKerningPair](/documentation/coretext/kernorderedlistentry/pair)
- [var value: KernKerningValue](/documentation/coretext/kernorderedlistentry/value)
- [KernOrderedListHeader](/documentation/coretext/kernorderedlistheader)

#### Initializers

- [init()](/documentation/coretext/kernorderedlistheader/init())
- [init(nPairs: UInt16, searchRange: UInt16, entrySelector: UInt16, rangeShift: UInt16, table: UInt16)](/documentation/coretext/kernorderedlistheader/init(npairs:searchrange:entryselector:rangeshift:table:))

#### Instance Properties

- [var entrySelector: UInt16](/documentation/coretext/kernorderedlistheader/entryselector)
- [var nPairs: UInt16](/documentation/coretext/kernorderedlistheader/npairs)
- [var rangeShift: UInt16](/documentation/coretext/kernorderedlistheader/rangeshift)
- [var searchRange: UInt16](/documentation/coretext/kernorderedlistheader/searchrange)
- [var table: UInt16](/documentation/coretext/kernorderedlistheader/table)
- [KernSimpleArrayHeader](/documentation/coretext/kernsimplearrayheader)

#### Initializers

- [init()](/documentation/coretext/kernsimplearrayheader/init())
- [init(rowWidth: UInt16, leftOffsetTable: UInt16, rightOffsetTable: UInt16, theArray: KernArrayOffset, firstTable: UInt16)](/documentation/coretext/kernsimplearrayheader/init(rowwidth:leftoffsettable:rightoffsettable:thearray:firsttable:))

#### Instance Properties

- [var firstTable: UInt16](/documentation/coretext/kernsimplearrayheader/firsttable)
- [var leftOffsetTable: UInt16](/documentation/coretext/kernsimplearrayheader/leftoffsettable)
- [var rightOffsetTable: UInt16](/documentation/coretext/kernsimplearrayheader/rightoffsettable)
- [var rowWidth: UInt16](/documentation/coretext/kernsimplearrayheader/rowwidth)
- [var theArray: KernArrayOffset](/documentation/coretext/kernsimplearrayheader/thearray)
- [KernStateEntry](/documentation/coretext/kernstateentry)

#### Initializers

- [init()](/documentation/coretext/kernstateentry/init())
- [init(newState: UInt16, flags: UInt16)](/documentation/coretext/kernstateentry/init(newstate:flags:))

#### Instance Properties

- [var flags: UInt16](/documentation/coretext/kernstateentry/flags)
- [var newState: UInt16](/documentation/coretext/kernstateentry/newstate)
- [KernStateHeader](/documentation/coretext/kernstateheader)

#### Initializers

- [init()](/documentation/coretext/kernstateheader/init())
- [init(header: STHeader, valueTable: UInt16, firstTable: UInt8)](/documentation/coretext/kernstateheader/init(header:valuetable:firsttable:))

#### Instance Properties

- [var firstTable: UInt8](/documentation/coretext/kernstateheader/firsttable)
- [var header: STHeader](/documentation/coretext/kernstateheader/header)
- [var valueTable: UInt16](/documentation/coretext/kernstateheader/valuetable)
- [KernSubtableHeader](/documentation/coretext/kernsubtableheader)

#### Initializers

- [init()](/documentation/coretext/kernsubtableheader/init())
- [init(length: Int32, stInfo: KernSubtableInfo, tupleIndex: Int16, fsHeader: KernFormatSpecificHeader)](/documentation/coretext/kernsubtableheader/init(length:stinfo:tupleindex:fsheader:))

#### Instance Properties

- [var fsHeader: KernFormatSpecificHeader](/documentation/coretext/kernsubtableheader/fsheader)
- [var length: Int32](/documentation/coretext/kernsubtableheader/length)
- [var stInfo: KernSubtableInfo](/documentation/coretext/kernsubtableheader/stinfo)
- [var tupleIndex: Int16](/documentation/coretext/kernsubtableheader/tupleindex)
- [KernTableHeader](/documentation/coretext/kerntableheader)

#### Initializers

- [init()](/documentation/coretext/kerntableheader/init())
- [init(version: Fixed, nTables: Int32, firstSubtable: UInt16)](/documentation/coretext/kerntableheader/init(version:ntables:firstsubtable:))

#### Instance Properties

- [var firstSubtable: UInt16](/documentation/coretext/kerntableheader/firstsubtable)
- [var nTables: Int32](/documentation/coretext/kerntableheader/ntables)
- [var version: Fixed](/documentation/coretext/kerntableheader/version)
- [KernVersion0Header](/documentation/coretext/kernversion0header)

#### Initializers

- [init()](/documentation/coretext/kernversion0header/init())
- [init(version: UInt16, nTables: UInt16, firstSubtable: UInt16)](/documentation/coretext/kernversion0header/init(version:ntables:firstsubtable:))

#### Instance Properties

- [var firstSubtable: UInt16](/documentation/coretext/kernversion0header/firstsubtable)
- [var nTables: UInt16](/documentation/coretext/kernversion0header/ntables)
- [var version: UInt16](/documentation/coretext/kernversion0header/version)
- [KernVersion0SubtableHeader](/documentation/coretext/kernversion0subtableheader)

#### Initializers

- [init()](/documentation/coretext/kernversion0subtableheader/init())
- [init(version: UInt16, length: UInt16, stInfo: KernSubtableInfo, fsHeader: KernFormatSpecificHeader)](/documentation/coretext/kernversion0subtableheader/init(version:length:stinfo:fsheader:))

#### Instance Properties

- [var fsHeader: KernFormatSpecificHeader](/documentation/coretext/kernversion0subtableheader/fsheader)
- [var length: UInt16](/documentation/coretext/kernversion0subtableheader/length)
- [var stInfo: KernSubtableInfo](/documentation/coretext/kernversion0subtableheader/stinfo)
- [var version: UInt16](/documentation/coretext/kernversion0subtableheader/version)
- [KerxAnchorPointAction](/documentation/coretext/kerxanchorpointaction)

#### Initializers

- [init()](/documentation/coretext/kerxanchorpointaction/init())
- [init(markAnchorPoint: UInt16, currAnchorPoint: UInt16)](/documentation/coretext/kerxanchorpointaction/init(markanchorpoint:curranchorpoint:))

#### Instance Properties

- [var currAnchorPoint: UInt16](/documentation/coretext/kerxanchorpointaction/curranchorpoint)
- [var markAnchorPoint: UInt16](/documentation/coretext/kerxanchorpointaction/markanchorpoint)
- [KerxControlPointAction](/documentation/coretext/kerxcontrolpointaction)

#### Initializers

- [init()](/documentation/coretext/kerxcontrolpointaction/init())
- [init(markControlPoint: UInt16, currControlPoint: UInt16)](/documentation/coretext/kerxcontrolpointaction/init(markcontrolpoint:currcontrolpoint:))

#### Instance Properties

- [var currControlPoint: UInt16](/documentation/coretext/kerxcontrolpointaction/currcontrolpoint)
- [var markControlPoint: UInt16](/documentation/coretext/kerxcontrolpointaction/markcontrolpoint)
- [KerxControlPointEntry](/documentation/coretext/kerxcontrolpointentry)

#### Initializers

- [init()](/documentation/coretext/kerxcontrolpointentry/init())
- [init(newState: UInt16, flags: UInt16, actionIndex: UInt16)](/documentation/coretext/kerxcontrolpointentry/init(newstate:flags:actionindex:))

#### Instance Properties

- [var actionIndex: UInt16](/documentation/coretext/kerxcontrolpointentry/actionindex)
- [var flags: UInt16](/documentation/coretext/kerxcontrolpointentry/flags)
- [var newState: UInt16](/documentation/coretext/kerxcontrolpointentry/newstate)
- [KerxControlPointHeader](/documentation/coretext/kerxcontrolpointheader)

#### Initializers

- [init()](/documentation/coretext/kerxcontrolpointheader/init())
- [init(header: STXHeader, flags: UInt32, firstTable: UInt8)](/documentation/coretext/kerxcontrolpointheader/init(header:flags:firsttable:))

#### Instance Properties

- [var firstTable: UInt8](/documentation/coretext/kerxcontrolpointheader/firsttable)
- [var flags: UInt32](/documentation/coretext/kerxcontrolpointheader/flags)
- [var header: STXHeader](/documentation/coretext/kerxcontrolpointheader/header)
- [KerxCoordinateAction](/documentation/coretext/kerxcoordinateaction)

#### Initializers

- [init()](/documentation/coretext/kerxcoordinateaction/init())
- [init(markX: UInt16, markY: UInt16, currX: UInt16, currY: UInt16)](/documentation/coretext/kerxcoordinateaction/init(markx:marky:currx:curry:))

#### Instance Properties

- [var currX: UInt16](/documentation/coretext/kerxcoordinateaction/currx)
- [var currY: UInt16](/documentation/coretext/kerxcoordinateaction/curry)
- [var markX: UInt16](/documentation/coretext/kerxcoordinateaction/markx)
- [var markY: UInt16](/documentation/coretext/kerxcoordinateaction/marky)
- [KerxFormatSpecificHeader](/documentation/coretext/kerxformatspecificheader)

#### Initializers

- [init()](/documentation/coretext/kerxformatspecificheader/init())
- [init(controlPoint: KerxControlPointHeader)](/documentation/coretext/kerxformatspecificheader/init(controlpoint:))
- [init(indexArray: KerxIndexArrayHeader)](/documentation/coretext/kerxformatspecificheader/init(indexarray:))
- [init(orderedList: KerxOrderedListHeader)](/documentation/coretext/kerxformatspecificheader/init(orderedlist:))
- [init(simpleArray: KerxSimpleArrayHeader)](/documentation/coretext/kerxformatspecificheader/init(simplearray:))
- [init(stateTable: KerxStateHeader)](/documentation/coretext/kerxformatspecificheader/init(statetable:))

#### Instance Properties

- [var controlPoint: KerxControlPointHeader](/documentation/coretext/kerxformatspecificheader/controlpoint)
- [var indexArray: KerxIndexArrayHeader](/documentation/coretext/kerxformatspecificheader/indexarray)
- [var orderedList: KerxOrderedListHeader](/documentation/coretext/kerxformatspecificheader/orderedlist)
- [var simpleArray: KerxSimpleArrayHeader](/documentation/coretext/kerxformatspecificheader/simplearray)
- [var stateTable: KerxStateHeader](/documentation/coretext/kerxformatspecificheader/statetable)
- [KerxIndexArrayHeader](/documentation/coretext/kerxindexarrayheader)

#### Initializers

- [init()](/documentation/coretext/kerxindexarrayheader/init())
- [init(flags: UInt32, rowCount: UInt16, columnCount: UInt16, rowIndexTableOffset: UInt32, columnIndexTableOffset: UInt32, kerningArrayOffset: UInt32, kerningVectorOffset: UInt32)](/documentation/coretext/kerxindexarrayheader/init(flags:rowcount:columncount:rowindextableoffset:columnindextableoffset:kerningarrayoffset:kerningvectoroffset:))

#### Instance Properties

- [var columnCount: UInt16](/documentation/coretext/kerxindexarrayheader/columncount)
- [var columnIndexTableOffset: UInt32](/documentation/coretext/kerxindexarrayheader/columnindextableoffset)
- [var flags: UInt32](/documentation/coretext/kerxindexarrayheader/flags)
- [var kerningArrayOffset: UInt32](/documentation/coretext/kerxindexarrayheader/kerningarrayoffset)
- [var kerningVectorOffset: UInt32](/documentation/coretext/kerxindexarrayheader/kerningvectoroffset)
- [var rowCount: UInt16](/documentation/coretext/kerxindexarrayheader/rowcount)
- [var rowIndexTableOffset: UInt32](/documentation/coretext/kerxindexarrayheader/rowindextableoffset)
- [KerxKerningPair](/documentation/coretext/kerxkerningpair)

#### Initializers

- [init()](/documentation/coretext/kerxkerningpair/init())
- [init(left: UInt16, right: UInt16)](/documentation/coretext/kerxkerningpair/init(left:right:))

#### Instance Properties

- [var left: UInt16](/documentation/coretext/kerxkerningpair/left)
- [var right: UInt16](/documentation/coretext/kerxkerningpair/right)
- [KerxOrderedListEntry](/documentation/coretext/kerxorderedlistentry)

#### Initializers

- [init()](/documentation/coretext/kerxorderedlistentry/init())
- [init(pair: KerxKerningPair, value: KernKerningValue)](/documentation/coretext/kerxorderedlistentry/init(pair:value:))

#### Instance Properties

- [var pair: KerxKerningPair](/documentation/coretext/kerxorderedlistentry/pair)
- [var value: KernKerningValue](/documentation/coretext/kerxorderedlistentry/value)
- [KerxOrderedListHeader](/documentation/coretext/kerxorderedlistheader)

#### Initializers

- [init()](/documentation/coretext/kerxorderedlistheader/init())
- [init(nPairs: UInt32, searchRange: UInt32, entrySelector: UInt32, rangeShift: UInt32, table: UInt32)](/documentation/coretext/kerxorderedlistheader/init(npairs:searchrange:entryselector:rangeshift:table:))

#### Instance Properties

- [var entrySelector: UInt32](/documentation/coretext/kerxorderedlistheader/entryselector)
- [var nPairs: UInt32](/documentation/coretext/kerxorderedlistheader/npairs)
- [var rangeShift: UInt32](/documentation/coretext/kerxorderedlistheader/rangeshift)
- [var searchRange: UInt32](/documentation/coretext/kerxorderedlistheader/searchrange)
- [var table: UInt32](/documentation/coretext/kerxorderedlistheader/table)
- [KerxSimpleArrayHeader](/documentation/coretext/kerxsimplearrayheader)

#### Initializers

- [init()](/documentation/coretext/kerxsimplearrayheader/init())
- [init(rowWidth: UInt32, leftOffsetTable: UInt32, rightOffsetTable: UInt32, theArray: KerxArrayOffset, firstTable: UInt32)](/documentation/coretext/kerxsimplearrayheader/init(rowwidth:leftoffsettable:rightoffsettable:thearray:firsttable:))

#### Instance Properties

- [var firstTable: UInt32](/documentation/coretext/kerxsimplearrayheader/firsttable)
- [var leftOffsetTable: UInt32](/documentation/coretext/kerxsimplearrayheader/leftoffsettable)
- [var rightOffsetTable: UInt32](/documentation/coretext/kerxsimplearrayheader/rightoffsettable)
- [var rowWidth: UInt32](/documentation/coretext/kerxsimplearrayheader/rowwidth)
- [var theArray: KerxArrayOffset](/documentation/coretext/kerxsimplearrayheader/thearray)
- [KerxStateEntry](/documentation/coretext/kerxstateentry)

#### Initializers

- [init()](/documentation/coretext/kerxstateentry/init())
- [init(newState: UInt16, flags: UInt16, valueIndex: UInt16)](/documentation/coretext/kerxstateentry/init(newstate:flags:valueindex:))

#### Instance Properties

- [var flags: UInt16](/documentation/coretext/kerxstateentry/flags)
- [var newState: UInt16](/documentation/coretext/kerxstateentry/newstate)
- [var valueIndex: UInt16](/documentation/coretext/kerxstateentry/valueindex)
- [KerxStateHeader](/documentation/coretext/kerxstateheader)

#### Initializers

- [init()](/documentation/coretext/kerxstateheader/init())
- [init(header: STXHeader, valueTable: UInt32, firstTable: UInt8)](/documentation/coretext/kerxstateheader/init(header:valuetable:firsttable:))

#### Instance Properties

- [var firstTable: UInt8](/documentation/coretext/kerxstateheader/firsttable)
- [var header: STXHeader](/documentation/coretext/kerxstateheader/header)
- [var valueTable: UInt32](/documentation/coretext/kerxstateheader/valuetable)
- [KerxSubtableHeader](/documentation/coretext/kerxsubtableheader)

#### Initializers

- [init()](/documentation/coretext/kerxsubtableheader/init())
- [init(length: UInt32, stInfo: KerxSubtableCoverage, tupleCount: UInt32, fsHeader: KerxFormatSpecificHeader)](/documentation/coretext/kerxsubtableheader/init(length:stinfo:tuplecount:fsheader:))

#### Instance Properties

- [var fsHeader: KerxFormatSpecificHeader](/documentation/coretext/kerxsubtableheader/fsheader)
- [var length: UInt32](/documentation/coretext/kerxsubtableheader/length)
- [var stInfo: KerxSubtableCoverage](/documentation/coretext/kerxsubtableheader/stinfo)
- [var tupleCount: UInt32](/documentation/coretext/kerxsubtableheader/tuplecount)
- [KerxTableHeader](/documentation/coretext/kerxtableheader)

#### Initializers

- [init()](/documentation/coretext/kerxtableheader/init())
- [init(version: Fixed, nTables: UInt32, firstSubtable: UInt32)](/documentation/coretext/kerxtableheader/init(version:ntables:firstsubtable:))

#### Instance Properties

- [var firstSubtable: UInt32](/documentation/coretext/kerxtableheader/firstsubtable)
- [var nTables: UInt32](/documentation/coretext/kerxtableheader/ntables)
- [var version: Fixed](/documentation/coretext/kerxtableheader/version)
- [LcarCaretClassEntry](/documentation/coretext/lcarcaretclassentry)

#### Initializers

- [init()](/documentation/coretext/lcarcaretclassentry/init())
- [init(count: UInt16, partials: UInt16)](/documentation/coretext/lcarcaretclassentry/init(count:partials:))

#### Instance Properties

- [var count: UInt16](/documentation/coretext/lcarcaretclassentry/count)
- [var partials: UInt16](/documentation/coretext/lcarcaretclassentry/partials)
- [LcarCaretTable](/documentation/coretext/lcarcarettable)

#### Initializers

- [init()](/documentation/coretext/lcarcarettable/init())
- [init(version: Fixed, format: UInt16, lookup: SFNTLookupTable)](/documentation/coretext/lcarcarettable/init(version:format:lookup:))

#### Instance Properties

- [var format: UInt16](/documentation/coretext/lcarcarettable/format)
- [var lookup: SFNTLookupTable](/documentation/coretext/lcarcarettable/lookup)
- [var version: Fixed](/documentation/coretext/lcarcarettable/version)
- [MortChain](/documentation/coretext/mortchain)

#### Initializers

- [init()](/documentation/coretext/mortchain/init())
- [init(defaultFlags: MortSubtableMaskFlags, length: UInt32, nFeatures: UInt16, nSubtables: UInt16, featureEntries: MortFeatureEntry)](/documentation/coretext/mortchain/init(defaultflags:length:nfeatures:nsubtables:featureentries:))

#### Instance Properties

- [var defaultFlags: MortSubtableMaskFlags](/documentation/coretext/mortchain/defaultflags)
- [var featureEntries: MortFeatureEntry](/documentation/coretext/mortchain/featureentries)
- [var length: UInt32](/documentation/coretext/mortchain/length)
- [var nFeatures: UInt16](/documentation/coretext/mortchain/nfeatures)
- [var nSubtables: UInt16](/documentation/coretext/mortchain/nsubtables)
- [MortContextualSubtable](/documentation/coretext/mortcontextualsubtable)

#### Initializers

- [init()](/documentation/coretext/mortcontextualsubtable/init())
- [init(header: STHeader, substitutionTableOffset: UInt16)](/documentation/coretext/mortcontextualsubtable/init(header:substitutiontableoffset:))

#### Instance Properties

- [var header: STHeader](/documentation/coretext/mortcontextualsubtable/header)
- [var substitutionTableOffset: UInt16](/documentation/coretext/mortcontextualsubtable/substitutiontableoffset)
- [MortFeatureEntry](/documentation/coretext/mortfeatureentry)

#### Initializers

- [init()](/documentation/coretext/mortfeatureentry/init())
- [init(featureType: UInt16, featureSelector: UInt16, enableFlags: MortSubtableMaskFlags, disableFlags: MortSubtableMaskFlags)](/documentation/coretext/mortfeatureentry/init(featuretype:featureselector:enableflags:disableflags:))

#### Instance Properties

- [var disableFlags: MortSubtableMaskFlags](/documentation/coretext/mortfeatureentry/disableflags)
- [var enableFlags: MortSubtableMaskFlags](/documentation/coretext/mortfeatureentry/enableflags)
- [var featureSelector: UInt16](/documentation/coretext/mortfeatureentry/featureselector)
- [var featureType: UInt16](/documentation/coretext/mortfeatureentry/featuretype)
- [MortInsertionSubtable](/documentation/coretext/mortinsertionsubtable)

#### Initializers

- [init()](/documentation/coretext/mortinsertionsubtable/init())
- [init(header: STHeader)](/documentation/coretext/mortinsertionsubtable/init(header:))

#### Instance Properties

- [var header: STHeader](/documentation/coretext/mortinsertionsubtable/header)
- [MortLigatureSubtable](/documentation/coretext/mortligaturesubtable)

#### Initializers

- [init()](/documentation/coretext/mortligaturesubtable/init())
- [init(header: STHeader, ligatureActionTableOffset: UInt16, componentTableOffset: UInt16, ligatureTableOffset: UInt16)](/documentation/coretext/mortligaturesubtable/init(header:ligatureactiontableoffset:componenttableoffset:ligaturetableoffset:))

#### Instance Properties

- [var componentTableOffset: UInt16](/documentation/coretext/mortligaturesubtable/componenttableoffset)
- [var header: STHeader](/documentation/coretext/mortligaturesubtable/header)
- [var ligatureActionTableOffset: UInt16](/documentation/coretext/mortligaturesubtable/ligatureactiontableoffset)
- [var ligatureTableOffset: UInt16](/documentation/coretext/mortligaturesubtable/ligaturetableoffset)
- [MortRearrangementSubtable](/documentation/coretext/mortrearrangementsubtable)

#### Initializers

- [init()](/documentation/coretext/mortrearrangementsubtable/init())
- [init(header: STHeader)](/documentation/coretext/mortrearrangementsubtable/init(header:))

#### Instance Properties

- [var header: STHeader](/documentation/coretext/mortrearrangementsubtable/header)
- [MortSpecificSubtable](/documentation/coretext/mortspecificsubtable)

#### Initializers

- [init()](/documentation/coretext/mortspecificsubtable/init())
- [init(contextual: MortContextualSubtable)](/documentation/coretext/mortspecificsubtable/init(contextual:))
- [init(insertion: MortInsertionSubtable)](/documentation/coretext/mortspecificsubtable/init(insertion:))
- [init(ligature: MortLigatureSubtable)](/documentation/coretext/mortspecificsubtable/init(ligature:))
- [init(rearrangement: MortRearrangementSubtable)](/documentation/coretext/mortspecificsubtable/init(rearrangement:))
- [init(swash: MortSwashSubtable)](/documentation/coretext/mortspecificsubtable/init(swash:))

#### Instance Properties

- [var contextual: MortContextualSubtable](/documentation/coretext/mortspecificsubtable/contextual)
- [var insertion: MortInsertionSubtable](/documentation/coretext/mortspecificsubtable/insertion)
- [var ligature: MortLigatureSubtable](/documentation/coretext/mortspecificsubtable/ligature)
- [var rearrangement: MortRearrangementSubtable](/documentation/coretext/mortspecificsubtable/rearrangement)
- [var swash: MortSwashSubtable](/documentation/coretext/mortspecificsubtable/swash)
- [MortSubtable](/documentation/coretext/mortsubtable)

#### Initializers

- [init()](/documentation/coretext/mortsubtable/init())
- [init(length: UInt16, coverage: UInt16, flags: MortSubtableMaskFlags, u: MortSpecificSubtable)](/documentation/coretext/mortsubtable/init(length:coverage:flags:u:))

#### Instance Properties

- [var coverage: UInt16](/documentation/coretext/mortsubtable/coverage)
- [var flags: MortSubtableMaskFlags](/documentation/coretext/mortsubtable/flags)
- [var length: UInt16](/documentation/coretext/mortsubtable/length)
- [var u: MortSpecificSubtable](/documentation/coretext/mortsubtable/u)
- [MortSwashSubtable](/documentation/coretext/mortswashsubtable)

#### Initializers

- [init()](/documentation/coretext/mortswashsubtable/init())
- [init(lookup: SFNTLookupTable)](/documentation/coretext/mortswashsubtable/init(lookup:))

#### Instance Properties

- [var lookup: SFNTLookupTable](/documentation/coretext/mortswashsubtable/lookup)
- [MortTable](/documentation/coretext/morttable)

#### Initializers

- [init()](/documentation/coretext/morttable/init())
- [init(version: Fixed, nChains: UInt32, chains: MortChain)](/documentation/coretext/morttable/init(version:nchains:chains:))

#### Instance Properties

- [var chains: MortChain](/documentation/coretext/morttable/chains)
- [var nChains: UInt32](/documentation/coretext/morttable/nchains)
- [var version: Fixed](/documentation/coretext/morttable/version)
- [MorxChain](/documentation/coretext/morxchain)

#### Initializers

- [init()](/documentation/coretext/morxchain/init())
- [init(defaultFlags: MortSubtableMaskFlags, length: UInt32, nFeatures: UInt32, nSubtables: UInt32, featureEntries: MortFeatureEntry)](/documentation/coretext/morxchain/init(defaultflags:length:nfeatures:nsubtables:featureentries:))

#### Instance Properties

- [var defaultFlags: MortSubtableMaskFlags](/documentation/coretext/morxchain/defaultflags)
- [var featureEntries: MortFeatureEntry](/documentation/coretext/morxchain/featureentries)
- [var length: UInt32](/documentation/coretext/morxchain/length)
- [var nFeatures: UInt32](/documentation/coretext/morxchain/nfeatures)
- [var nSubtables: UInt32](/documentation/coretext/morxchain/nsubtables)
- [MorxContextualSubtable](/documentation/coretext/morxcontextualsubtable)

#### Initializers

- [init()](/documentation/coretext/morxcontextualsubtable/init())
- [init(header: STXHeader, substitutionTableOffset: UInt32)](/documentation/coretext/morxcontextualsubtable/init(header:substitutiontableoffset:))

#### Instance Properties

- [var header: STXHeader](/documentation/coretext/morxcontextualsubtable/header)
- [var substitutionTableOffset: UInt32](/documentation/coretext/morxcontextualsubtable/substitutiontableoffset)
- [MorxInsertionSubtable](/documentation/coretext/morxinsertionsubtable)

#### Initializers

- [init()](/documentation/coretext/morxinsertionsubtable/init())
- [init(header: STXHeader, insertionGlyphTableOffset: UInt32)](/documentation/coretext/morxinsertionsubtable/init(header:insertionglyphtableoffset:))

#### Instance Properties

- [var header: STXHeader](/documentation/coretext/morxinsertionsubtable/header)
- [var insertionGlyphTableOffset: UInt32](/documentation/coretext/morxinsertionsubtable/insertionglyphtableoffset)
- [MorxLigatureSubtable](/documentation/coretext/morxligaturesubtable)

#### Initializers

- [init()](/documentation/coretext/morxligaturesubtable/init())
- [init(header: STXHeader, ligatureActionTableOffset: UInt32, componentTableOffset: UInt32, ligatureTableOffset: UInt32)](/documentation/coretext/morxligaturesubtable/init(header:ligatureactiontableoffset:componenttableoffset:ligaturetableoffset:))

#### Instance Properties

- [var componentTableOffset: UInt32](/documentation/coretext/morxligaturesubtable/componenttableoffset)
- [var header: STXHeader](/documentation/coretext/morxligaturesubtable/header)
- [var ligatureActionTableOffset: UInt32](/documentation/coretext/morxligaturesubtable/ligatureactiontableoffset)
- [var ligatureTableOffset: UInt32](/documentation/coretext/morxligaturesubtable/ligaturetableoffset)
- [MorxRearrangementSubtable](/documentation/coretext/morxrearrangementsubtable)

#### Initializers

- [init()](/documentation/coretext/morxrearrangementsubtable/init())
- [init(header: STXHeader)](/documentation/coretext/morxrearrangementsubtable/init(header:))

#### Instance Properties

- [var header: STXHeader](/documentation/coretext/morxrearrangementsubtable/header)
- [MorxSpecificSubtable](/documentation/coretext/morxspecificsubtable)

#### Initializers

- [init()](/documentation/coretext/morxspecificsubtable/init())
- [init(contextual: MorxContextualSubtable)](/documentation/coretext/morxspecificsubtable/init(contextual:))
- [init(insertion: MorxInsertionSubtable)](/documentation/coretext/morxspecificsubtable/init(insertion:))
- [init(ligature: MorxLigatureSubtable)](/documentation/coretext/morxspecificsubtable/init(ligature:))
- [init(rearrangement: MorxRearrangementSubtable)](/documentation/coretext/morxspecificsubtable/init(rearrangement:))
- [init(swash: MortSwashSubtable)](/documentation/coretext/morxspecificsubtable/init(swash:))

#### Instance Properties

- [var contextual: MorxContextualSubtable](/documentation/coretext/morxspecificsubtable/contextual)
- [var insertion: MorxInsertionSubtable](/documentation/coretext/morxspecificsubtable/insertion)
- [var ligature: MorxLigatureSubtable](/documentation/coretext/morxspecificsubtable/ligature)
- [var rearrangement: MorxRearrangementSubtable](/documentation/coretext/morxspecificsubtable/rearrangement)
- [var swash: MortSwashSubtable](/documentation/coretext/morxspecificsubtable/swash)
- [MorxSubtable](/documentation/coretext/morxsubtable)

#### Initializers

- [init()](/documentation/coretext/morxsubtable/init())
- [init(length: UInt32, coverage: UInt32, flags: MortSubtableMaskFlags, u: MorxSpecificSubtable)](/documentation/coretext/morxsubtable/init(length:coverage:flags:u:))

#### Instance Properties

- [var coverage: UInt32](/documentation/coretext/morxsubtable/coverage)
- [var flags: MortSubtableMaskFlags](/documentation/coretext/morxsubtable/flags)
- [var length: UInt32](/documentation/coretext/morxsubtable/length)
- [var u: MorxSpecificSubtable](/documentation/coretext/morxsubtable/u)
- [MorxTable](/documentation/coretext/morxtable)

#### Initializers

- [init()](/documentation/coretext/morxtable/init())
- [init(version: Fixed, nChains: UInt32, chains: MorxChain)](/documentation/coretext/morxtable/init(version:nchains:chains:))

#### Instance Properties

- [var chains: MorxChain](/documentation/coretext/morxtable/chains)
- [var nChains: UInt32](/documentation/coretext/morxtable/nchains)
- [var version: Fixed](/documentation/coretext/morxtable/version)
- [OpbdSideValues](/documentation/coretext/opbdsidevalues)

#### Initializers

- [init()](/documentation/coretext/opbdsidevalues/init())
- [init(leftSideShift: Int16, topSideShift: Int16, rightSideShift: Int16, bottomSideShift: Int16)](/documentation/coretext/opbdsidevalues/init(leftsideshift:topsideshift:rightsideshift:bottomsideshift:))

#### Instance Properties

- [var bottomSideShift: Int16](/documentation/coretext/opbdsidevalues/bottomsideshift)
- [var leftSideShift: Int16](/documentation/coretext/opbdsidevalues/leftsideshift)
- [var rightSideShift: Int16](/documentation/coretext/opbdsidevalues/rightsideshift)
- [var topSideShift: Int16](/documentation/coretext/opbdsidevalues/topsideshift)
- [OpbdTable](/documentation/coretext/opbdtable)

#### Initializers

- [init()](/documentation/coretext/opbdtable/init())
- [init(version: Fixed, format: OpbdTableFormat, lookupTable: SFNTLookupTable)](/documentation/coretext/opbdtable/init(version:format:lookuptable:))

#### Instance Properties

- [var format: OpbdTableFormat](/documentation/coretext/opbdtable/format)
- [var lookupTable: SFNTLookupTable](/documentation/coretext/opbdtable/lookuptable)
- [var version: Fixed](/documentation/coretext/opbdtable/version)
- [PropLookupSegment](/documentation/coretext/proplookupsegment)

#### Initializers

- [init()](/documentation/coretext/proplookupsegment/init())
- [init(lastGlyph: UInt16, firstGlyph: UInt16, value: UInt16)](/documentation/coretext/proplookupsegment/init(lastglyph:firstglyph:value:))

#### Instance Properties

- [var firstGlyph: UInt16](/documentation/coretext/proplookupsegment/firstglyph)
- [var lastGlyph: UInt16](/documentation/coretext/proplookupsegment/lastglyph)
- [var value: UInt16](/documentation/coretext/proplookupsegment/value)
- [PropLookupSingle](/documentation/coretext/proplookupsingle)

#### Initializers

- [init()](/documentation/coretext/proplookupsingle/init())
- [init(glyph: UInt16, props: PropCharProperties)](/documentation/coretext/proplookupsingle/init(glyph:props:))

#### Instance Properties

- [var glyph: UInt16](/documentation/coretext/proplookupsingle/glyph)
- [var props: PropCharProperties](/documentation/coretext/proplookupsingle/props)
- [PropTable](/documentation/coretext/proptable)

#### Initializers

- [init()](/documentation/coretext/proptable/init())
- [init(version: Fixed, format: UInt16, defaultProps: PropCharProperties, lookup: SFNTLookupTable)](/documentation/coretext/proptable/init(version:format:defaultprops:lookup:))

#### Instance Properties

- [var defaultProps: PropCharProperties](/documentation/coretext/proptable/defaultprops)
- [var format: UInt16](/documentation/coretext/proptable/format)
- [var lookup: SFNTLookupTable](/documentation/coretext/proptable/lookup)
- [var version: Fixed](/documentation/coretext/proptable/version)
- [ROTAGlyphEntry](/documentation/coretext/rotaglyphentry)

#### Initializers

- [init()](/documentation/coretext/rotaglyphentry/init())
- [init(GlyphIndexOffset: Int16, HBaselineOffset: Int16, VBaselineOffset: Int16)](/documentation/coretext/rotaglyphentry/init(glyphindexoffset:hbaselineoffset:vbaselineoffset:))

#### Instance Properties

- [var GlyphIndexOffset: Int16](/documentation/coretext/rotaglyphentry/glyphindexoffset)
- [var HBaselineOffset: Int16](/documentation/coretext/rotaglyphentry/hbaselineoffset)
- [var VBaselineOffset: Int16](/documentation/coretext/rotaglyphentry/vbaselineoffset)
- [ROTAHeader](/documentation/coretext/rotaheader)

#### Initializers

- [init()](/documentation/coretext/rotaheader/init())
- [init(Version: Fixed, Flags: UInt16, NMasters: UInt16, FirstGlyph: UInt16, LastGlyph: UInt16, lookup: SFNTLookupTable)](/documentation/coretext/rotaheader/init(version:flags:nmasters:firstglyph:lastglyph:lookup:))

#### Instance Properties

- [var FirstGlyph: UInt16](/documentation/coretext/rotaheader/firstglyph)
- [var Flags: UInt16](/documentation/coretext/rotaheader/flags)
- [var LastGlyph: UInt16](/documentation/coretext/rotaheader/lastglyph)
- [var NMasters: UInt16](/documentation/coretext/rotaheader/nmasters)
- [var Version: Fixed](/documentation/coretext/rotaheader/version)
- [var lookup: SFNTLookupTable](/documentation/coretext/rotaheader/lookup)
- [SFNTLookupArrayHeader](/documentation/coretext/sfntlookuparrayheader)

#### Initializers

- [init()](/documentation/coretext/sfntlookuparrayheader/init())
- [init(lookupValues: SFNTLookupValue)](/documentation/coretext/sfntlookuparrayheader/init(lookupvalues:))

#### Instance Properties

- [var lookupValues: SFNTLookupValue](/documentation/coretext/sfntlookuparrayheader/lookupvalues)
- [SFNTLookupBinarySearchHeader](/documentation/coretext/sfntlookupbinarysearchheader)

#### Initializers

- [init()](/documentation/coretext/sfntlookupbinarysearchheader/init())
- [init(unitSize: UInt16, nUnits: UInt16, searchRange: UInt16, entrySelector: UInt16, rangeShift: UInt16)](/documentation/coretext/sfntlookupbinarysearchheader/init(unitsize:nunits:searchrange:entryselector:rangeshift:))

#### Instance Properties

- [var entrySelector: UInt16](/documentation/coretext/sfntlookupbinarysearchheader/entryselector)
- [var nUnits: UInt16](/documentation/coretext/sfntlookupbinarysearchheader/nunits)
- [var rangeShift: UInt16](/documentation/coretext/sfntlookupbinarysearchheader/rangeshift)
- [var searchRange: UInt16](/documentation/coretext/sfntlookupbinarysearchheader/searchrange)
- [var unitSize: UInt16](/documentation/coretext/sfntlookupbinarysearchheader/unitsize)
- [SFNTLookupFormatSpecificHeader](/documentation/coretext/sfntlookupformatspecificheader)

#### Initializers

- [init()](/documentation/coretext/sfntlookupformatspecificheader/init())
- [init(segment: SFNTLookupSegmentHeader)](/documentation/coretext/sfntlookupformatspecificheader/init(segment:))
- [init(single: SFNTLookupSingleHeader)](/documentation/coretext/sfntlookupformatspecificheader/init(single:))
- [init(theArray: SFNTLookupArrayHeader)](/documentation/coretext/sfntlookupformatspecificheader/init(thearray:))
- [init(trimmedArray: SFNTLookupTrimmedArrayHeader)](/documentation/coretext/sfntlookupformatspecificheader/init(trimmedarray:))
- [init(vector: SFNTLookupVectorHeader)](/documentation/coretext/sfntlookupformatspecificheader/init(vector:))

#### Instance Properties

- [var segment: SFNTLookupSegmentHeader](/documentation/coretext/sfntlookupformatspecificheader/segment)
- [var single: SFNTLookupSingleHeader](/documentation/coretext/sfntlookupformatspecificheader/single)
- [var theArray: SFNTLookupArrayHeader](/documentation/coretext/sfntlookupformatspecificheader/thearray)
- [var trimmedArray: SFNTLookupTrimmedArrayHeader](/documentation/coretext/sfntlookupformatspecificheader/trimmedarray)
- [var vector: SFNTLookupVectorHeader](/documentation/coretext/sfntlookupformatspecificheader/vector)
- [SFNTLookupSegment](/documentation/coretext/sfntlookupsegment)

#### Initializers

- [init()](/documentation/coretext/sfntlookupsegment/init())
- [init(lastGlyph: UInt16, firstGlyph: UInt16, value: UInt16)](/documentation/coretext/sfntlookupsegment/init(lastglyph:firstglyph:value:))

#### Instance Properties

- [var firstGlyph: UInt16](/documentation/coretext/sfntlookupsegment/firstglyph)
- [var lastGlyph: UInt16](/documentation/coretext/sfntlookupsegment/lastglyph)
- [var value: UInt16](/documentation/coretext/sfntlookupsegment/value)
- [SFNTLookupSegmentHeader](/documentation/coretext/sfntlookupsegmentheader)

#### Initializers

- [init()](/documentation/coretext/sfntlookupsegmentheader/init())
- [init(binSearch: SFNTLookupBinarySearchHeader, segments: SFNTLookupSegment)](/documentation/coretext/sfntlookupsegmentheader/init(binsearch:segments:))

#### Instance Properties

- [var binSearch: SFNTLookupBinarySearchHeader](/documentation/coretext/sfntlookupsegmentheader/binsearch)
- [var segments: SFNTLookupSegment](/documentation/coretext/sfntlookupsegmentheader/segments)
- [SFNTLookupSingle](/documentation/coretext/sfntlookupsingle)

#### Initializers

- [init()](/documentation/coretext/sfntlookupsingle/init())
- [init(glyph: UInt16, value: UInt16)](/documentation/coretext/sfntlookupsingle/init(glyph:value:))

#### Instance Properties

- [var glyph: UInt16](/documentation/coretext/sfntlookupsingle/glyph)
- [var value: UInt16](/documentation/coretext/sfntlookupsingle/value)
- [SFNTLookupSingleHeader](/documentation/coretext/sfntlookupsingleheader)

#### Initializers

- [init()](/documentation/coretext/sfntlookupsingleheader/init())
- [init(binSearch: SFNTLookupBinarySearchHeader, entries: SFNTLookupSingle)](/documentation/coretext/sfntlookupsingleheader/init(binsearch:entries:))

#### Instance Properties

- [var binSearch: SFNTLookupBinarySearchHeader](/documentation/coretext/sfntlookupsingleheader/binsearch)
- [var entries: SFNTLookupSingle](/documentation/coretext/sfntlookupsingleheader/entries)
- [SFNTLookupTable](/documentation/coretext/sfntlookuptable)

#### Initializers

- [init()](/documentation/coretext/sfntlookuptable/init())
- [init(format: SFNTLookupTableFormat, fsHeader: SFNTLookupFormatSpecificHeader)](/documentation/coretext/sfntlookuptable/init(format:fsheader:))

#### Instance Properties

- [var format: SFNTLookupTableFormat](/documentation/coretext/sfntlookuptable/format)
- [var fsHeader: SFNTLookupFormatSpecificHeader](/documentation/coretext/sfntlookuptable/fsheader)
- [SFNTLookupTrimmedArrayHeader](/documentation/coretext/sfntlookuptrimmedarrayheader)

#### Initializers

- [init()](/documentation/coretext/sfntlookuptrimmedarrayheader/init())
- [init(firstGlyph: UInt16, count: UInt16, valueArray: SFNTLookupValue)](/documentation/coretext/sfntlookuptrimmedarrayheader/init(firstglyph:count:valuearray:))

#### Instance Properties

- [var count: UInt16](/documentation/coretext/sfntlookuptrimmedarrayheader/count)
- [var firstGlyph: UInt16](/documentation/coretext/sfntlookuptrimmedarrayheader/firstglyph)
- [var valueArray: SFNTLookupValue](/documentation/coretext/sfntlookuptrimmedarrayheader/valuearray)
- [STClassTable](/documentation/coretext/stclasstable)

#### Initializers

- [init()](/documentation/coretext/stclasstable/init())
- [init(firstGlyph: UInt16, nGlyphs: UInt16, classes: STClass)](/documentation/coretext/stclasstable/init(firstglyph:nglyphs:classes:))

#### Instance Properties

- [var classes: STClass](/documentation/coretext/stclasstable/classes)
- [var firstGlyph: UInt16](/documentation/coretext/stclasstable/firstglyph)
- [var nGlyphs: UInt16](/documentation/coretext/stclasstable/nglyphs)
- [STEntryOne](/documentation/coretext/stentryone)

#### Initializers

- [init()](/documentation/coretext/stentryone/init())
- [init(newState: UInt16, flags: UInt16, offset1: UInt16)](/documentation/coretext/stentryone/init(newstate:flags:offset1:))

#### Instance Properties

- [var flags: UInt16](/documentation/coretext/stentryone/flags)
- [var newState: UInt16](/documentation/coretext/stentryone/newstate)
- [var offset1: UInt16](/documentation/coretext/stentryone/offset1)
- [STEntryTwo](/documentation/coretext/stentrytwo)

#### Initializers

- [init()](/documentation/coretext/stentrytwo/init())
- [init(newState: UInt16, flags: UInt16, offset1: UInt16, offset2: UInt16)](/documentation/coretext/stentrytwo/init(newstate:flags:offset1:offset2:))

#### Instance Properties

- [var flags: UInt16](/documentation/coretext/stentrytwo/flags)
- [var newState: UInt16](/documentation/coretext/stentrytwo/newstate)
- [var offset1: UInt16](/documentation/coretext/stentrytwo/offset1)
- [var offset2: UInt16](/documentation/coretext/stentrytwo/offset2)
- [STEntryZero](/documentation/coretext/stentryzero)

#### Initializers

- [init()](/documentation/coretext/stentryzero/init())
- [init(newState: UInt16, flags: UInt16)](/documentation/coretext/stentryzero/init(newstate:flags:))

#### Instance Properties

- [var flags: UInt16](/documentation/coretext/stentryzero/flags)
- [var newState: UInt16](/documentation/coretext/stentryzero/newstate)
- [STHeader](/documentation/coretext/stheader)

#### Initializers

- [init()](/documentation/coretext/stheader/init())
- [init(filler: UInt8, nClasses: STClass, classTableOffset: UInt16, stateArrayOffset: UInt16, entryTableOffset: UInt16)](/documentation/coretext/stheader/init(filler:nclasses:classtableoffset:statearrayoffset:entrytableoffset:))

#### Instance Properties

- [var classTableOffset: UInt16](/documentation/coretext/stheader/classtableoffset)
- [var entryTableOffset: UInt16](/documentation/coretext/stheader/entrytableoffset)
- [var filler: UInt8](/documentation/coretext/stheader/filler)
- [var nClasses: STClass](/documentation/coretext/stheader/nclasses)
- [var stateArrayOffset: UInt16](/documentation/coretext/stheader/statearrayoffset)
- [STXEntryOne](/documentation/coretext/stxentryone)

#### Initializers

- [init()](/documentation/coretext/stxentryone/init())
- [init(newState: STXStateIndex, flags: UInt16, index1: UInt16)](/documentation/coretext/stxentryone/init(newstate:flags:index1:))

#### Instance Properties

- [var flags: UInt16](/documentation/coretext/stxentryone/flags)
- [var index1: UInt16](/documentation/coretext/stxentryone/index1)
- [var newState: STXStateIndex](/documentation/coretext/stxentryone/newstate)
- [STXEntryTwo](/documentation/coretext/stxentrytwo)

#### Initializers

- [init()](/documentation/coretext/stxentrytwo/init())
- [init(newState: STXStateIndex, flags: UInt16, index1: UInt16, index2: UInt16)](/documentation/coretext/stxentrytwo/init(newstate:flags:index1:index2:))

#### Instance Properties

- [var flags: UInt16](/documentation/coretext/stxentrytwo/flags)
- [var index1: UInt16](/documentation/coretext/stxentrytwo/index1)
- [var index2: UInt16](/documentation/coretext/stxentrytwo/index2)
- [var newState: STXStateIndex](/documentation/coretext/stxentrytwo/newstate)
- [STXEntryZero](/documentation/coretext/stxentryzero)

#### Initializers

- [init()](/documentation/coretext/stxentryzero/init())
- [init(newState: STXStateIndex, flags: UInt16)](/documentation/coretext/stxentryzero/init(newstate:flags:))

#### Instance Properties

- [var flags: UInt16](/documentation/coretext/stxentryzero/flags)
- [var newState: STXStateIndex](/documentation/coretext/stxentryzero/newstate)
- [STXHeader](/documentation/coretext/stxheader)

#### Initializers

- [init()](/documentation/coretext/stxheader/init())
- [init(nClasses: UInt32, classTableOffset: UInt32, stateArrayOffset: UInt32, entryTableOffset: UInt32)](/documentation/coretext/stxheader/init(nclasses:classtableoffset:statearrayoffset:entrytableoffset:))

#### Instance Properties

- [var classTableOffset: UInt32](/documentation/coretext/stxheader/classtableoffset)
- [var entryTableOffset: UInt32](/documentation/coretext/stxheader/entrytableoffset)
- [var nClasses: UInt32](/documentation/coretext/stxheader/nclasses)
- [var stateArrayOffset: UInt32](/documentation/coretext/stxheader/statearrayoffset)
- [TrakTable](/documentation/coretext/traktable)

#### Initializers

- [init()](/documentation/coretext/traktable/init())
- [init(version: Fixed, format: UInt16, horizOffset: UInt16, vertOffset: UInt16)](/documentation/coretext/traktable/init(version:format:horizoffset:vertoffset:))

#### Instance Properties

- [var format: UInt16](/documentation/coretext/traktable/format)
- [var horizOffset: UInt16](/documentation/coretext/traktable/horizoffset)
- [var version: Fixed](/documentation/coretext/traktable/version)
- [var vertOffset: UInt16](/documentation/coretext/traktable/vertoffset)
- [TrakTableData](/documentation/coretext/traktabledata)

#### Initializers

- [init()](/documentation/coretext/traktabledata/init())
- [init(nTracks: UInt16, nSizes: UInt16, sizeTableOffset: UInt32, trakTable: TrakTableEntry)](/documentation/coretext/traktabledata/init(ntracks:nsizes:sizetableoffset:traktable:))

#### Instance Properties

- [var nSizes: UInt16](/documentation/coretext/traktabledata/nsizes)
- [var nTracks: UInt16](/documentation/coretext/traktabledata/ntracks)
- [var sizeTableOffset: UInt32](/documentation/coretext/traktabledata/sizetableoffset)
- [var trakTable: TrakTableEntry](/documentation/coretext/traktabledata/traktable)
- [TrakTableEntry](/documentation/coretext/traktableentry)

#### Initializers

- [init()](/documentation/coretext/traktableentry/init())
- [init(track: Fixed, nameTableIndex: UInt16, sizesOffset: UInt16)](/documentation/coretext/traktableentry/init(track:nametableindex:sizesoffset:))

#### Instance Properties

- [var nameTableIndex: UInt16](/documentation/coretext/traktableentry/nametableindex)
- [var sizesOffset: UInt16](/documentation/coretext/traktableentry/sizesoffset)
- [var track: Fixed](/documentation/coretext/traktableentry/track)
- [sfntCMapEncoding](/documentation/coretext/sfntcmapencoding)

#### Initializers

- [init()](/documentation/coretext/sfntcmapencoding/init())
- [init(platformID: UInt16, scriptID: UInt16, offset: UInt32)](/documentation/coretext/sfntcmapencoding/init(platformid:scriptid:offset:))

#### Instance Properties

- [var offset: UInt32](/documentation/coretext/sfntcmapencoding/offset)
- [var platformID: UInt16](/documentation/coretext/sfntcmapencoding/platformid)
- [var scriptID: UInt16](/documentation/coretext/sfntcmapencoding/scriptid)
- [sfntCMapExtendedSubHeader](/documentation/coretext/sfntcmapextendedsubheader)

#### Initializers

- [init()](/documentation/coretext/sfntcmapextendedsubheader/init())
- [init(format: UInt16, reserved: UInt16, length: UInt32, language: UInt32)](/documentation/coretext/sfntcmapextendedsubheader/init(format:reserved:length:language:))

#### Instance Properties

- [var format: UInt16](/documentation/coretext/sfntcmapextendedsubheader/format)
- [var language: UInt32](/documentation/coretext/sfntcmapextendedsubheader/language)
- [var length: UInt32](/documentation/coretext/sfntcmapextendedsubheader/length)
- [var reserved: UInt16](/documentation/coretext/sfntcmapextendedsubheader/reserved)
- [sfntCMapHeader](/documentation/coretext/sfntcmapheader)

#### Initializers

- [init()](/documentation/coretext/sfntcmapheader/init())
- [init(version: UInt16, numTables: UInt16, encoding: sfntCMapEncoding)](/documentation/coretext/sfntcmapheader/init(version:numtables:encoding:))

#### Instance Properties

- [var encoding: sfntCMapEncoding](/documentation/coretext/sfntcmapheader/encoding)
- [var numTables: UInt16](/documentation/coretext/sfntcmapheader/numtables)
- [var version: UInt16](/documentation/coretext/sfntcmapheader/version)
- [sfntCMapSubHeader](/documentation/coretext/sfntcmapsubheader)

#### Initializers

- [init()](/documentation/coretext/sfntcmapsubheader/init())
- [init(format: UInt16, length: UInt16, languageID: UInt16)](/documentation/coretext/sfntcmapsubheader/init(format:length:languageid:))

#### Instance Properties

- [var format: UInt16](/documentation/coretext/sfntcmapsubheader/format)
- [var languageID: UInt16](/documentation/coretext/sfntcmapsubheader/languageid)
- [var length: UInt16](/documentation/coretext/sfntcmapsubheader/length)
- [sfntDescriptorHeader](/documentation/coretext/sfntdescriptorheader)

#### Initializers

- [init()](/documentation/coretext/sfntdescriptorheader/init())
- [init(version: Fixed, descriptorCount: Int32, descriptor: sfntFontDescriptor)](/documentation/coretext/sfntdescriptorheader/init(version:descriptorcount:descriptor:))

#### Instance Properties

- [var descriptor: sfntFontDescriptor](/documentation/coretext/sfntdescriptorheader/descriptor)
- [var descriptorCount: Int32](/documentation/coretext/sfntdescriptorheader/descriptorcount)
- [var version: Fixed](/documentation/coretext/sfntdescriptorheader/version)
- [sfntDirectory](/documentation/coretext/sfntdirectory)

#### Initializers

- [init()](/documentation/coretext/sfntdirectory/init())
- [init(format: FourCharCode, numOffsets: UInt16, searchRange: UInt16, entrySelector: UInt16, rangeShift: UInt16, table: sfntDirectoryEntry)](/documentation/coretext/sfntdirectory/init(format:numoffsets:searchrange:entryselector:rangeshift:table:))

#### Instance Properties

- [var entrySelector: UInt16](/documentation/coretext/sfntdirectory/entryselector)
- [var format: FourCharCode](/documentation/coretext/sfntdirectory/format)
- [var numOffsets: UInt16](/documentation/coretext/sfntdirectory/numoffsets)
- [var rangeShift: UInt16](/documentation/coretext/sfntdirectory/rangeshift)
- [var searchRange: UInt16](/documentation/coretext/sfntdirectory/searchrange)
- [var table: sfntDirectoryEntry](/documentation/coretext/sfntdirectory/table)
- [sfntDirectoryEntry](/documentation/coretext/sfntdirectoryentry)

#### Initializers

- [init()](/documentation/coretext/sfntdirectoryentry/init())
- [init(tableTag: FourCharCode, checkSum: UInt32, offset: UInt32, length: UInt32)](/documentation/coretext/sfntdirectoryentry/init(tabletag:checksum:offset:length:))

#### Instance Properties

- [var checkSum: UInt32](/documentation/coretext/sfntdirectoryentry/checksum)
- [var length: UInt32](/documentation/coretext/sfntdirectoryentry/length)
- [var offset: UInt32](/documentation/coretext/sfntdirectoryentry/offset)
- [var tableTag: FourCharCode](/documentation/coretext/sfntdirectoryentry/tabletag)
- [sfntFeatureHeader](/documentation/coretext/sfntfeatureheader)

#### Initializers

- [init()](/documentation/coretext/sfntfeatureheader/init())
- [init(version: Int32, featureNameCount: UInt16, featureSetCount: UInt16, reserved: Int32, names: sfntFeatureName, settings: sfntFontFeatureSetting, runs: sfntFontRunFeature)](/documentation/coretext/sfntfeatureheader/init(version:featurenamecount:featuresetcount:reserved:names:settings:runs:))

#### Instance Properties

- [var featureNameCount: UInt16](/documentation/coretext/sfntfeatureheader/featurenamecount)
- [var featureSetCount: UInt16](/documentation/coretext/sfntfeatureheader/featuresetcount)
- [var names: sfntFeatureName](/documentation/coretext/sfntfeatureheader/names)
- [var reserved: Int32](/documentation/coretext/sfntfeatureheader/reserved)
- [var runs: sfntFontRunFeature](/documentation/coretext/sfntfeatureheader/runs)
- [var settings: sfntFontFeatureSetting](/documentation/coretext/sfntfeatureheader/settings)
- [var version: Int32](/documentation/coretext/sfntfeatureheader/version)
- [sfntFeatureName](/documentation/coretext/sfntfeaturename)

#### Initializers

- [init()](/documentation/coretext/sfntfeaturename/init())
- [init(featureType: UInt16, settingCount: UInt16, offsetToSettings: Int32, featureFlags: UInt16, nameID: Int16)](/documentation/coretext/sfntfeaturename/init(featuretype:settingcount:offsettosettings:featureflags:nameid:))

#### Instance Properties

- [var featureFlags: UInt16](/documentation/coretext/sfntfeaturename/featureflags)
- [var featureType: UInt16](/documentation/coretext/sfntfeaturename/featuretype)
- [var nameID: Int16](/documentation/coretext/sfntfeaturename/nameid)
- [var offsetToSettings: Int32](/documentation/coretext/sfntfeaturename/offsettosettings)
- [var settingCount: UInt16](/documentation/coretext/sfntfeaturename/settingcount)
- [sfntFontDescriptor](/documentation/coretext/sfntfontdescriptor)

#### Initializers

- [init()](/documentation/coretext/sfntfontdescriptor/init())
- [init(name: FourCharCode, value: Fixed)](/documentation/coretext/sfntfontdescriptor/init(name:value:))

#### Instance Properties

- [var name: FourCharCode](/documentation/coretext/sfntfontdescriptor/name)
- [var value: Fixed](/documentation/coretext/sfntfontdescriptor/value)
- [sfntFontFeatureSetting](/documentation/coretext/sfntfontfeaturesetting)

#### Initializers

- [init()](/documentation/coretext/sfntfontfeaturesetting/init())
- [init(setting: UInt16, nameID: Int16)](/documentation/coretext/sfntfontfeaturesetting/init(setting:nameid:))

#### Instance Properties

- [var nameID: Int16](/documentation/coretext/sfntfontfeaturesetting/nameid)
- [var setting: UInt16](/documentation/coretext/sfntfontfeaturesetting/setting)
- [sfntFontRunFeature](/documentation/coretext/sfntfontrunfeature)

#### Initializers

- [init()](/documentation/coretext/sfntfontrunfeature/init())
- [init(featureType: UInt16, setting: UInt16)](/documentation/coretext/sfntfontrunfeature/init(featuretype:setting:))

#### Instance Properties

- [var featureType: UInt16](/documentation/coretext/sfntfontrunfeature/featuretype)
- [var setting: UInt16](/documentation/coretext/sfntfontrunfeature/setting)
- [sfntInstance](/documentation/coretext/sfntinstance)

#### Initializers

- [init()](/documentation/coretext/sfntinstance/init())
- [init(nameID: Int16, flags: Int16, coord: Fixed)](/documentation/coretext/sfntinstance/init(nameid:flags:coord:))

#### Instance Properties

- [var coord: Fixed](/documentation/coretext/sfntinstance/coord)
- [var flags: Int16](/documentation/coretext/sfntinstance/flags)
- [var nameID: Int16](/documentation/coretext/sfntinstance/nameid)
- [sfntNameHeader](/documentation/coretext/sfntnameheader)

#### Initializers

- [init()](/documentation/coretext/sfntnameheader/init())
- [init(format: UInt16, count: UInt16, stringOffset: UInt16, rec: sfntNameRecord)](/documentation/coretext/sfntnameheader/init(format:count:stringoffset:rec:))

#### Instance Properties

- [var count: UInt16](/documentation/coretext/sfntnameheader/count)
- [var format: UInt16](/documentation/coretext/sfntnameheader/format)
- [var rec: sfntNameRecord](/documentation/coretext/sfntnameheader/rec)
- [var stringOffset: UInt16](/documentation/coretext/sfntnameheader/stringoffset)
- [sfntNameRecord](/documentation/coretext/sfntnamerecord)

#### Initializers

- [init()](/documentation/coretext/sfntnamerecord/init())
- [init(platformID: UInt16, scriptID: UInt16, languageID: UInt16, nameID: UInt16, length: UInt16, offset: UInt16)](/documentation/coretext/sfntnamerecord/init(platformid:scriptid:languageid:nameid:length:offset:))

#### Instance Properties

- [var languageID: UInt16](/documentation/coretext/sfntnamerecord/languageid)
- [var length: UInt16](/documentation/coretext/sfntnamerecord/length)
- [var nameID: UInt16](/documentation/coretext/sfntnamerecord/nameid)
- [var offset: UInt16](/documentation/coretext/sfntnamerecord/offset)
- [var platformID: UInt16](/documentation/coretext/sfntnamerecord/platformid)
- [var scriptID: UInt16](/documentation/coretext/sfntnamerecord/scriptid)
- [sfntVariationAxis](/documentation/coretext/sfntvariationaxis)

#### Initializers

- [init()](/documentation/coretext/sfntvariationaxis/init())
- [init(axisTag: FourCharCode, minValue: Fixed, defaultValue: Fixed, maxValue: Fixed, flags: Int16, nameID: Int16)](/documentation/coretext/sfntvariationaxis/init(axistag:minvalue:defaultvalue:maxvalue:flags:nameid:))

#### Instance Properties

- [var axisTag: FourCharCode](/documentation/coretext/sfntvariationaxis/axistag)
- [var defaultValue: Fixed](/documentation/coretext/sfntvariationaxis/defaultvalue)
- [var flags: Int16](/documentation/coretext/sfntvariationaxis/flags)
- [var maxValue: Fixed](/documentation/coretext/sfntvariationaxis/maxvalue)
- [var minValue: Fixed](/documentation/coretext/sfntvariationaxis/minvalue)
- [var nameID: Int16](/documentation/coretext/sfntvariationaxis/nameid)
- [sfntVariationHeader](/documentation/coretext/sfntvariationheader)

#### Initializers

- [init()](/documentation/coretext/sfntvariationheader/init())
- [init(version: Fixed, offsetToData: UInt16, countSizePairs: UInt16, axisCount: UInt16, axisSize: UInt16, instanceCount: UInt16, instanceSize: UInt16, axis: sfntVariationAxis, instance: sfntInstance)](/documentation/coretext/sfntvariationheader/init(version:offsettodata:countsizepairs:axiscount:axissize:instancecount:instancesize:axis:instance:))

#### Instance Properties

- [var axis: sfntVariationAxis](/documentation/coretext/sfntvariationheader/axis)
- [var axisCount: UInt16](/documentation/coretext/sfntvariationheader/axiscount)
- [var axisSize: UInt16](/documentation/coretext/sfntvariationheader/axissize)
- [var countSizePairs: UInt16](/documentation/coretext/sfntvariationheader/countsizepairs)
- [var instance: sfntInstance](/documentation/coretext/sfntvariationheader/instance)
- [var instanceCount: UInt16](/documentation/coretext/sfntvariationheader/instancecount)
- [var instanceSize: UInt16](/documentation/coretext/sfntvariationheader/instancesize)
- [var offsetToData: UInt16](/documentation/coretext/sfntvariationheader/offsettodata)
- [var version: Fixed](/documentation/coretext/sfntvariationheader/version)
- [ALMXGlyphEntry](/documentation/coretext/almxglyphentry)

#### Initializers

- [init()](/documentation/coretext/almxglyphentry/init())
- [init(GlyphIndexOffset: Int16, HorizontalAdvance: Int16, XOffsetToHOrigin: Int16, VerticalAdvance: Int16, YOffsetToVOrigin: Int16)](/documentation/coretext/almxglyphentry/init(glyphindexoffset:horizontaladvance:xoffsettohorigin:verticaladvance:yoffsettovorigin:))

#### Instance Properties

- [var GlyphIndexOffset: Int16](/documentation/coretext/almxglyphentry/glyphindexoffset)
- [var HorizontalAdvance: Int16](/documentation/coretext/almxglyphentry/horizontaladvance)
- [var VerticalAdvance: Int16](/documentation/coretext/almxglyphentry/verticaladvance)
- [var XOffsetToHOrigin: Int16](/documentation/coretext/almxglyphentry/xoffsettohorigin)
- [var YOffsetToVOrigin: Int16](/documentation/coretext/almxglyphentry/yoffsettovorigin)
- [ALMXHeader](/documentation/coretext/almxheader)

#### Initializers

- [init()](/documentation/coretext/almxheader/init())
- [init(Version: Fixed, Flags: UInt16, NMasters: UInt16, FirstGlyph: UInt16, LastGlyph: UInt16, lookup: SFNTLookupTable)](/documentation/coretext/almxheader/init(version:flags:nmasters:firstglyph:lastglyph:lookup:))

#### Instance Properties

- [var FirstGlyph: UInt16](/documentation/coretext/almxheader/firstglyph)
- [var Flags: UInt16](/documentation/coretext/almxheader/flags)
- [var LastGlyph: UInt16](/documentation/coretext/almxheader/lastglyph)
- [var NMasters: UInt16](/documentation/coretext/almxheader/nmasters)
- [var Version: Fixed](/documentation/coretext/almxheader/version)
- [var lookup: SFNTLookupTable](/documentation/coretext/almxheader/lookup)

### Type Aliases

- [BslnBaselineClass](/documentation/coretext/bslnbaselineclass)
- [BslnBaselineRecord](/documentation/coretext/bslnbaselinerecord)
- [BslnTableFormat](/documentation/coretext/bslntableformat)
- [BslnTablePtr](/documentation/coretext/bslntableptr)
- [FontLanguageCode](/documentation/coretext/fontlanguagecode)
- [FontNameCode](/documentation/coretext/fontnamecode)
- [FontPlatformCode](/documentation/coretext/fontplatformcode)
- [FontScriptCode](/documentation/coretext/fontscriptcode)
- [JustPCActionType](/documentation/coretext/justpcactiontype)
- [JustPCUnconditionalAddAction](/documentation/coretext/justpcunconditionaladdaction)
- [JustificationFlags](/documentation/coretext/justificationflags)
- [KernArrayOffset](/documentation/coretext/kernarrayoffset)
- [KernKerningValue](/documentation/coretext/kernkerningvalue)
- [KernOffsetTablePtr](/documentation/coretext/kernoffsettableptr)
- [KernOrderedListEntryPtr](/documentation/coretext/kernorderedlistentryptr)
- [KernSubtableHeaderPtr](/documentation/coretext/kernsubtableheaderptr)
- [KernSubtableInfo](/documentation/coretext/kernsubtableinfo)
- [KernTableFormat](/documentation/coretext/kerntableformat)
- [KernTableHeaderHandle](/documentation/coretext/kerntableheaderhandle)
- [KernTableHeaderPtr](/documentation/coretext/kerntableheaderptr)
- [KerxArrayOffset](/documentation/coretext/kerxarrayoffset)
- [KerxOrderedListEntryPtr](/documentation/coretext/kerxorderedlistentryptr)
- [KerxSubtableCoverage](/documentation/coretext/kerxsubtablecoverage)
- [KerxSubtableHeaderPtr](/documentation/coretext/kerxsubtableheaderptr)
- [KerxTableHeaderHandle](/documentation/coretext/kerxtableheaderhandle)
- [KerxTableHeaderPtr](/documentation/coretext/kerxtableheaderptr)
- [LcarCaretTablePtr](/documentation/coretext/lcarcarettableptr)
- [MortLigatureActionEntry](/documentation/coretext/mortligatureactionentry)
- [MortSubtableMaskFlags](/documentation/coretext/mortsubtablemaskflags)
- [OpbdTableFormat](/documentation/coretext/opbdtableformat)
- [PropCharProperties](/documentation/coretext/propcharproperties)
- [SFNTLookupKind](/documentation/coretext/sfntlookupkind)
- [SFNTLookupOffset](/documentation/coretext/sfntlookupoffset)
- [SFNTLookupTableFormat](/documentation/coretext/sfntlookuptableformat)
- [SFNTLookupTableHandle](/documentation/coretext/sfntlookuptablehandle)
- [SFNTLookupTablePtr](/documentation/coretext/sfntlookuptableptr)
- [SFNTLookupValue](/documentation/coretext/sfntlookupvalue)
- [STClass](/documentation/coretext/stclass)
- [STEntryIndex](/documentation/coretext/stentryindex)
- [STXClass](/documentation/coretext/stxclass)
- [STXClassTable](/documentation/coretext/stxclasstable)
- [STXEntryIndex](/documentation/coretext/stxentryindex)
- [STXStateIndex](/documentation/coretext/stxstateindex)
- [TrakValue](/documentation/coretext/trakvalue)

### Constants

- [var cmapFontTableTag: Int](/documentation/coretext/cmapfonttabletag)
- [var descriptorFontTableTag: Int](/documentation/coretext/descriptorfonttabletag)
- [var featureFontTableTag: Int](/documentation/coretext/featurefonttabletag)
- [var kANKRCurrentVersion: Int](/documentation/coretext/kankrcurrentversion)
- [var kAbbrevSquaredLigaturesOffSelector: Int](/documentation/coretext/kabbrevsquaredligaturesoffselector)
- [var kAbbrevSquaredLigaturesOnSelector: Int](/documentation/coretext/kabbrevsquaredligaturesonselector)
- [var kAllCapsSelector: Int](/documentation/coretext/kallcapsselector)
- [var kAllLowerCaseSelector: Int](/documentation/coretext/kalllowercaseselector)
- [var kAllTypeFeaturesOffSelector: Int](/documentation/coretext/kalltypefeaturesoffselector)
- [var kAllTypeFeaturesOnSelector: Int](/documentation/coretext/kalltypefeaturesonselector)
- [var kAllTypographicFeaturesType: Int](/documentation/coretext/kalltypographicfeaturestype)
- [var kAltHalfWidthTextSelector: Int](/documentation/coretext/kalthalfwidthtextselector)
- [var kAltProportionalTextSelector: Int](/documentation/coretext/kaltproportionaltextselector)
- [var kAlternateHorizKanaOffSelector: Int](/documentation/coretext/kalternatehorizkanaoffselector)
- [var kAlternateHorizKanaOnSelector: Int](/documentation/coretext/kalternatehorizkanaonselector)
- [var kAlternateKanaType: Int](/documentation/coretext/kalternatekanatype)
- [var kAlternateVertKanaOffSelector: Int](/documentation/coretext/kalternatevertkanaoffselector)
- [var kAlternateVertKanaOnSelector: Int](/documentation/coretext/kalternatevertkanaonselector)
- [var kAnnotationType: Int](/documentation/coretext/kannotationtype)
- [var kAsteriskToMultiplyOffSelector: Int](/documentation/coretext/kasterisktomultiplyoffselector)
- [var kAsteriskToMultiplyOnSelector: Int](/documentation/coretext/kasterisktomultiplyonselector)
- [var kBSLNControlPointFormatNoMap: Int](/documentation/coretext/kbslncontrolpointformatnomap)
- [var kBSLNControlPointFormatWithMap: Int](/documentation/coretext/kbslncontrolpointformatwithmap)
- [var kBSLNCurrentVersion: Int](/documentation/coretext/kbslncurrentversion)
- [var kBSLNDistanceFormatNoMap: Int](/documentation/coretext/kbslndistanceformatnomap)
- [var kBSLNDistanceFormatWithMap: Int](/documentation/coretext/kbslndistanceformatwithmap)
- [var kBSLNHangingBaseline: Int](/documentation/coretext/kbslnhangingbaseline)
- [var kBSLNIdeographicCenterBaseline: Int](/documentation/coretext/kbslnideographiccenterbaseline)
- [var kBSLNIdeographicLowBaseline: Int](/documentation/coretext/kbslnideographiclowbaseline)
- [var kBSLNLastBaseline: Int](/documentation/coretext/kbslnlastbaseline)
- [var kBSLNMathBaseline: Int](/documentation/coretext/kbslnmathbaseline)
- [var kBSLNNoBaseline: Int](/documentation/coretext/kbslnnobaseline)
- [var kBSLNNoBaselineOverride: Int](/documentation/coretext/kbslnnobaselineoverride)
- [var kBSLNNumBaselineClasses: Int](/documentation/coretext/kbslnnumbaselineclasses)
- [var kBSLNRomanBaseline: Int](/documentation/coretext/kbslnromanbaseline)
- [var kBSLNTag: Int](/documentation/coretext/kbslntag)
- [var kBoxAnnotationSelector: Int](/documentation/coretext/kboxannotationselector)
- [var kCJKItalicRomanOffSelector: Int](/documentation/coretext/kcjkitalicromanoffselector)
- [var kCJKItalicRomanOnSelector: Int](/documentation/coretext/kcjkitalicromanonselector)
- [var kCJKItalicRomanSelector: Int](/documentation/coretext/kcjkitalicromanselector)
- [var kCJKRomanSpacingType: Int](/documentation/coretext/kcjkromanspacingtype)
- [var kCJKSymbolAltFiveSelector: Int](/documentation/coretext/kcjksymbolaltfiveselector)
- [var kCJKSymbolAltFourSelector: Int](/documentation/coretext/kcjksymbolaltfourselector)
- [var kCJKSymbolAltOneSelector: Int](/documentation/coretext/kcjksymbolaltoneselector)
- [var kCJKSymbolAltThreeSelector: Int](/documentation/coretext/kcjksymbolaltthreeselector)
- [var kCJKSymbolAltTwoSelector: Int](/documentation/coretext/kcjksymbolalttwoselector)
- [var kCJKSymbolAlternativesType: Int](/documentation/coretext/kcjksymbolalternativestype)
- [var kCJKVerticalRomanCenteredSelector: Int](/documentation/coretext/kcjkverticalromancenteredselector)
- [var kCJKVerticalRomanHBaselineSelector: Int](/documentation/coretext/kcjkverticalromanhbaselineselector)
- [var kCJKVerticalRomanPlacementType: Int](/documentation/coretext/kcjkverticalromanplacementtype)
- [var kCTFontTableCBDT: Int](/documentation/coretext/kctfonttablecbdt)
- [var kCTFontTableCBLC: Int](/documentation/coretext/kctfonttablecblc)
- [var kCTFontTableCFF2: Int](/documentation/coretext/kctfonttablecff2)
- [var kCTFontTableCOLR: Int](/documentation/coretext/kctfonttablecolr)
- [var kCTFontTableCPAL: Int](/documentation/coretext/kctfonttablecpal)
- [var kCTFontTableCidg: Int](/documentation/coretext/kctfonttablecidg)
- [var kCTFontTableFond: Int](/documentation/coretext/kctfonttablefond)
- [var kCTFontTableHVAR: Int](/documentation/coretext/kctfonttablehvar)
- [var kCTFontTableMERG: Int](/documentation/coretext/kctfonttablemerg)
- [var kCTFontTableMVAR: Int](/documentation/coretext/kctfonttablemvar)
- [var kCTFontTableMeta: Int](/documentation/coretext/kctfonttablemeta)
- [var kCTFontTableSTAT: Int](/documentation/coretext/kctfonttablestat)
- [var kCTFontTableSVG: Int](/documentation/coretext/kctfonttablesvg)
- [var kCTFontTableVVAR: Int](/documentation/coretext/kctfonttablevvar)
- [var kCTFontTableXref: Int](/documentation/coretext/kctfonttablexref)
- [var kCanonicalCompositionOffSelector: Int](/documentation/coretext/kcanonicalcompositionoffselector)
- [var kCanonicalCompositionOnSelector: Int](/documentation/coretext/kcanonicalcompositiononselector)
- [var kCaseSensitiveLayoutOffSelector: Int](/documentation/coretext/kcasesensitivelayoutoffselector)
- [var kCaseSensitiveLayoutOnSelector: Int](/documentation/coretext/kcasesensitivelayoutonselector)
- [var kCaseSensitiveLayoutType: Int](/documentation/coretext/kcasesensitivelayouttype)
- [var kCaseSensitiveSpacingOffSelector: Int](/documentation/coretext/kcasesensitivespacingoffselector)
- [var kCaseSensitiveSpacingOnSelector: Int](/documentation/coretext/kcasesensitivespacingonselector)
- [var kCharacterAlternativesType: Int](/documentation/coretext/kcharacteralternativestype)
- [var kCharacterShapeType: Int](/documentation/coretext/kcharactershapetype)
- [var kCircleAnnotationSelector: Int](/documentation/coretext/kcircleannotationselector)
- [var kCommonLigaturesOffSelector: Int](/documentation/coretext/kcommonligaturesoffselector)
- [var kCommonLigaturesOnSelector: Int](/documentation/coretext/kcommonligaturesonselector)
- [var kCompatibilityCompositionOffSelector: Int](/documentation/coretext/kcompatibilitycompositionoffselector)
- [var kCompatibilityCompositionOnSelector: Int](/documentation/coretext/kcompatibilitycompositiononselector)
- [var kContextualAlternatesOffSelector: Int](/documentation/coretext/kcontextualalternatesoffselector)
- [var kContextualAlternatesOnSelector: Int](/documentation/coretext/kcontextualalternatesonselector)
- [var kContextualAlternatesType: Int](/documentation/coretext/kcontextualalternatestype)
- [var kContextualLigaturesOffSelector: Int](/documentation/coretext/kcontextualligaturesoffselector)
- [var kContextualLigaturesOnSelector: Int](/documentation/coretext/kcontextualligaturesonselector)
- [var kContextualSwashAlternatesOffSelector: Int](/documentation/coretext/kcontextualswashalternatesoffselector)
- [var kContextualSwashAlternatesOnSelector: Int](/documentation/coretext/kcontextualswashalternatesonselector)
- [var kCursiveConnectionType: Int](/documentation/coretext/kcursiveconnectiontype)
- [var kCursiveSelector: Int](/documentation/coretext/kcursiveselector)
- [var kDecomposeDiacriticsSelector: Int](/documentation/coretext/kdecomposediacriticsselector)
- [var kDecorativeBordersSelector: Int](/documentation/coretext/kdecorativebordersselector)
- [var kDefaultCJKRomanSelector: Int](/documentation/coretext/kdefaultcjkromanselector)
- [var kDefaultLowerCaseSelector: Int](/documentation/coretext/kdefaultlowercaseselector)
- [var kDefaultUpperCaseSelector: Int](/documentation/coretext/kdefaultuppercaseselector)
- [var kDesignComplexityType: Int](/documentation/coretext/kdesigncomplexitytype)
- [var kDesignLevel1Selector: Int](/documentation/coretext/kdesignlevel1selector)
- [var kDesignLevel2Selector: Int](/documentation/coretext/kdesignlevel2selector)
- [var kDesignLevel3Selector: Int](/documentation/coretext/kdesignlevel3selector)
- [var kDesignLevel4Selector: Int](/documentation/coretext/kdesignlevel4selector)
- [var kDesignLevel5Selector: Int](/documentation/coretext/kdesignlevel5selector)
- [var kDiacriticsType: Int](/documentation/coretext/kdiacriticstype)
- [var kDiagonalFractionsSelector: Int](/documentation/coretext/kdiagonalfractionsselector)
- [var kDiamondAnnotationSelector: Int](/documentation/coretext/kdiamondannotationselector)
- [var kDingbatsSelector: Int](/documentation/coretext/kdingbatsselector)
- [var kDiphthongLigaturesOffSelector: Int](/documentation/coretext/kdiphthongligaturesoffselector)
- [var kDiphthongLigaturesOnSelector: Int](/documentation/coretext/kdiphthongligaturesonselector)
- [var kDisplayTextSelector: Int](/documentation/coretext/kdisplaytextselector)
- [var kEngravedTextSelector: Int](/documentation/coretext/kengravedtextselector)
- [var kExpertCharactersSelector: Int](/documentation/coretext/kexpertcharactersselector)
- [var kExponentsOffSelector: Int](/documentation/coretext/kexponentsoffselector)
- [var kExponentsOnSelector: Int](/documentation/coretext/kexponentsonselector)
- [var kFleuronsSelector: Int](/documentation/coretext/kfleuronsselector)
- [var kFontAlbanianLanguage: Int](/documentation/coretext/kfontalbanianlanguage)
- [var kFontAmharicLanguage: Int](/documentation/coretext/kfontamhariclanguage)
- [var kFontAmharicScript: Int](/documentation/coretext/kfontamharicscript)
- [var kFontArabicLanguage: Int](/documentation/coretext/kfontarabiclanguage)
- [var kFontArabicScript: Int](/documentation/coretext/kfontarabicscript)
- [var kFontArmenianLanguage: Int](/documentation/coretext/kfontarmenianlanguage)
- [var kFontArmenianScript: Int](/documentation/coretext/kfontarmenianscript)
- [var kFontAssameseLanguage: Int](/documentation/coretext/kfontassameselanguage)
- [var kFontAymaraLanguage: Int](/documentation/coretext/kfontaymaralanguage)
- [var kFontAzerbaijanArLanguage: Int](/documentation/coretext/kfontazerbaijanarlanguage)
- [var kFontAzerbaijaniLanguage: Int](/documentation/coretext/kfontazerbaijanilanguage)
- [var kFontBasqueLanguage: Int](/documentation/coretext/kfontbasquelanguage)
- [var kFontBengaliLanguage: Int](/documentation/coretext/kfontbengalilanguage)
- [var kFontBengaliScript: Int](/documentation/coretext/kfontbengaliscript)
- [var kFontBulgarianLanguage: Int](/documentation/coretext/kfontbulgarianlanguage)
- [var kFontBurmeseLanguage: Int](/documentation/coretext/kfontburmeselanguage)
- [var kFontBurmeseScript: Int](/documentation/coretext/kfontburmesescript)
- [var kFontByelorussianLanguage: Int](/documentation/coretext/kfontbyelorussianlanguage)
- [var kFontCatalanLanguage: Int](/documentation/coretext/kfontcatalanlanguage)
- [var kFontChewaLanguage: Int](/documentation/coretext/kfontchewalanguage)
- [var kFontChineseScript: Int](/documentation/coretext/kfontchinesescript)
- [var kFontCopyrightName: Int](/documentation/coretext/kfontcopyrightname)
- [var kFontCroatianLanguage: Int](/documentation/coretext/kfontcroatianlanguage)
- [var kFontCustom16BitScript: Int](/documentation/coretext/kfontcustom16bitscript)
- [var kFontCustom816BitScript: Int](/documentation/coretext/kfontcustom816bitscript)
- [var kFontCustom8BitScript: Int](/documentation/coretext/kfontcustom8bitscript)
- [var kFontCustomPlatform: Int](/documentation/coretext/kfontcustomplatform)
- [var kFontCyrillicScript: Int](/documentation/coretext/kfontcyrillicscript)
- [var kFontCzechLanguage: Int](/documentation/coretext/kfontczechlanguage)
- [var kFontDanishLanguage: Int](/documentation/coretext/kfontdanishlanguage)
- [var kFontDescriptionName: Int](/documentation/coretext/kfontdescriptionname)
- [var kFontDesignerName: Int](/documentation/coretext/kfontdesignername)
- [var kFontDesignerURLName: Int](/documentation/coretext/kfontdesignerurlname)
- [var kFontDevanagariScript: Int](/documentation/coretext/kfontdevanagariscript)
- [var kFontDutchLanguage: Int](/documentation/coretext/kfontdutchlanguage)
- [var kFontDzongkhaLanguage: Int](/documentation/coretext/kfontdzongkhalanguage)
- [var kFontEastEuropeanRomanScript: Int](/documentation/coretext/kfonteasteuropeanromanscript)
- [var kFontEnglishLanguage: Int](/documentation/coretext/kfontenglishlanguage)
- [var kFontEsperantoLanguage: Int](/documentation/coretext/kfontesperantolanguage)
- [var kFontEstonianLanguage: Int](/documentation/coretext/kfontestonianlanguage)
- [var kFontEthiopicScript: Int](/documentation/coretext/kfontethiopicscript)
- [var kFontExtendedArabicScript: Int](/documentation/coretext/kfontextendedarabicscript)
- [var kFontFaeroeseLanguage: Int](/documentation/coretext/kfontfaeroeselanguage)
- [var kFontFamilyName: Int](/documentation/coretext/kfontfamilyname)
- [var kFontFarsiLanguage: Int](/documentation/coretext/kfontfarsilanguage)
- [var kFontFinnishLanguage: Int](/documentation/coretext/kfontfinnishlanguage)
- [var kFontFlemishLanguage: Int](/documentation/coretext/kfontflemishlanguage)
- [var kFontFrenchLanguage: Int](/documentation/coretext/kfontfrenchlanguage)
- [var kFontFullName: Int](/documentation/coretext/kfontfullname)
- [var kFontGallaLanguage: Int](/documentation/coretext/kfontgallalanguage)
- [var kFontGeezScript: Int](/documentation/coretext/kfontgeezscript)
- [var kFontGeorgianLanguage: Int](/documentation/coretext/kfontgeorgianlanguage)
- [var kFontGeorgianScript: Int](/documentation/coretext/kfontgeorgianscript)
- [var kFontGermanLanguage: Int](/documentation/coretext/kfontgermanlanguage)
- [var kFontGreekLanguage: Int](/documentation/coretext/kfontgreeklanguage)
- [var kFontGreekScript: Int](/documentation/coretext/kfontgreekscript)
- [var kFontGuaraniLanguage: Int](/documentation/coretext/kfontguaranilanguage)
- [var kFontGujaratiLanguage: Int](/documentation/coretext/kfontgujaratilanguage)
- [var kFontGujaratiScript: Int](/documentation/coretext/kfontgujaratiscript)
- [var kFontGurmukhiScript: Int](/documentation/coretext/kfontgurmukhiscript)
- [var kFontHebrewLanguage: Int](/documentation/coretext/kfonthebrewlanguage)
- [var kFontHebrewScript: Int](/documentation/coretext/kfonthebrewscript)
- [var kFontHindiLanguage: Int](/documentation/coretext/kfonthindilanguage)
- [var kFontHungarianLanguage: Int](/documentation/coretext/kfonthungarianlanguage)
- [var kFontISO10646_1993Semantics: Int](/documentation/coretext/kfontiso10646_1993semantics)
- [var kFontIcelandicLanguage: Int](/documentation/coretext/kfonticelandiclanguage)
- [var kFontIndonesianLanguage: Int](/documentation/coretext/kfontindonesianlanguage)
- [var kFontIrishLanguage: Int](/documentation/coretext/kfontirishlanguage)
- [var kFontItalianLanguage: Int](/documentation/coretext/kfontitalianlanguage)
- [var kFontJapaneseLanguage: Int](/documentation/coretext/kfontjapaneselanguage)
- [var kFontJapaneseScript: Int](/documentation/coretext/kfontjapanesescript)
- [var kFontJavaneseRomLanguage: Int](/documentation/coretext/kfontjavaneseromlanguage)
- [var kFontKannadaLanguage: Int](/documentation/coretext/kfontkannadalanguage)
- [var kFontKannadaScript: Int](/documentation/coretext/kfontkannadascript)
- [var kFontKashmiriLanguage: Int](/documentation/coretext/kfontkashmirilanguage)
- [var kFontKazakhLanguage: Int](/documentation/coretext/kfontkazakhlanguage)
- [var kFontKhmerLanguage: Int](/documentation/coretext/kfontkhmerlanguage)
- [var kFontKhmerScript: Int](/documentation/coretext/kfontkhmerscript)
- [var kFontKirghizLanguage: Int](/documentation/coretext/kfontkirghizlanguage)
- [var kFontKoreanLanguage: Int](/documentation/coretext/kfontkoreanlanguage)
- [var kFontKoreanScript: Int](/documentation/coretext/kfontkoreanscript)
- [var kFontKurdishLanguage: Int](/documentation/coretext/kfontkurdishlanguage)
- [var kFontLaoLanguage: Int](/documentation/coretext/kfontlaolanguage)
- [var kFontLaotianScript: Int](/documentation/coretext/kfontlaotianscript)
- [var kFontLappishLanguage: Int](/documentation/coretext/kfontlappishlanguage)
- [var kFontLastReservedName: Int](/documentation/coretext/kfontlastreservedname)
- [var kFontLatinLanguage: Int](/documentation/coretext/kfontlatinlanguage)
- [var kFontLatvianLanguage: Int](/documentation/coretext/kfontlatvianlanguage)
- [var kFontLettishLanguage: Int](/documentation/coretext/kfontlettishlanguage)
- [var kFontLicenseDescriptionName: Int](/documentation/coretext/kfontlicensedescriptionname)
- [var kFontLicenseInfoURLName: Int](/documentation/coretext/kfontlicenseinfourlname)
- [var kFontLithuanianLanguage: Int](/documentation/coretext/kfontlithuanianlanguage)
- [var kFontMacCompatibleFullName: Int](/documentation/coretext/kfontmaccompatiblefullname)
- [var kFontMacedonianLanguage: Int](/documentation/coretext/kfontmacedonianlanguage)
- [var kFontMacintoshPlatform: Int](/documentation/coretext/kfontmacintoshplatform)
- [var kFontMalagasyLanguage: Int](/documentation/coretext/kfontmalagasylanguage)
- [var kFontMalayArabicLanguage: Int](/documentation/coretext/kfontmalayarabiclanguage)
- [var kFontMalayRomanLanguage: Int](/documentation/coretext/kfontmalayromanlanguage)
- [var kFontMalayalamLanguage: Int](/documentation/coretext/kfontmalayalamlanguage)
- [var kFontMalayalamScript: Int](/documentation/coretext/kfontmalayalamscript)
- [var kFontMalteseLanguage: Int](/documentation/coretext/kfontmalteselanguage)
- [var kFontManufacturerName: Int](/documentation/coretext/kfontmanufacturername)
- [var kFontMarathiLanguage: Int](/documentation/coretext/kfontmarathilanguage)
- [var kFontMicrosoftPlatform: Int](/documentation/coretext/kfontmicrosoftplatform)
- [var kFontMicrosoftStandardScript: Int](/documentation/coretext/kfontmicrosoftstandardscript)
- [var kFontMicrosoftSymbolScript: Int](/documentation/coretext/kfontmicrosoftsymbolscript)
- [var kFontMicrosoftUCS4Script: Int](/documentation/coretext/kfontmicrosoftucs4script)
- [var kFontMoldavianLanguage: Int](/documentation/coretext/kfontmoldavianlanguage)
- [var kFontMongolianCyrLanguage: Int](/documentation/coretext/kfontmongoliancyrlanguage)
- [var kFontMongolianLanguage: Int](/documentation/coretext/kfontmongolianlanguage)
- [var kFontMongolianScript: Int](/documentation/coretext/kfontmongolianscript)
- [var kFontNepaliLanguage: Int](/documentation/coretext/kfontnepalilanguage)
- [var kFontNoLanguageCode: UInt32](/documentation/coretext/kfontnolanguagecode)
- [var kFontNoNameCode: UInt32](/documentation/coretext/kfontnonamecode)
- [var kFontNoPlatformCode: UInt32](/documentation/coretext/kfontnoplatformcode)
- [var kFontNoScriptCode: UInt32](/documentation/coretext/kfontnoscriptcode)
- [var kFontNorwegianLanguage: Int](/documentation/coretext/kfontnorwegianlanguage)
- [var kFontOriyaLanguage: Int](/documentation/coretext/kfontoriyalanguage)
- [var kFontOriyaScript: Int](/documentation/coretext/kfontoriyascript)
- [var kFontOromoLanguage: Int](/documentation/coretext/kfontoromolanguage)
- [var kFontPashtoLanguage: Int](/documentation/coretext/kfontpashtolanguage)
- [var kFontPersianLanguage: Int](/documentation/coretext/kfontpersianlanguage)
- [var kFontPolishLanguage: Int](/documentation/coretext/kfontpolishlanguage)
- [var kFontPortugueseLanguage: Int](/documentation/coretext/kfontportugueselanguage)
- [var kFontPostScriptCIDName: Int](/documentation/coretext/kfontpostscriptcidname)
- [var kFontPostscriptName: Int](/documentation/coretext/kfontpostscriptname)
- [var kFontPreferredFamilyName: Int](/documentation/coretext/kfontpreferredfamilyname)
- [var kFontPreferredSubfamilyName: Int](/documentation/coretext/kfontpreferredsubfamilyname)
- [var kFontPunjabiLanguage: Int](/documentation/coretext/kfontpunjabilanguage)
- [var kFontQuechuaLanguage: Int](/documentation/coretext/kfontquechualanguage)
- [var kFontRSymbolScript: Int](/documentation/coretext/kfontrsymbolscript)
- [var kFontReservedPlatform: Int](/documentation/coretext/kfontreservedplatform)
- [var kFontRomanScript: Int](/documentation/coretext/kfontromanscript)
- [var kFontRomanianLanguage: Int](/documentation/coretext/kfontromanianlanguage)
- [var kFontRuandaLanguage: Int](/documentation/coretext/kfontruandalanguage)
- [var kFontRundiLanguage: Int](/documentation/coretext/kfontrundilanguage)
- [var kFontRussian: Int](/documentation/coretext/kfontrussian)
- [var kFontRussianLanguage: Int](/documentation/coretext/kfontrussianlanguage)
- [var kFontSaamiskLanguage: Int](/documentation/coretext/kfontsaamisklanguage)
- [var kFontSampleTextName: Int](/documentation/coretext/kfontsampletextname)
- [var kFontSanskritLanguage: Int](/documentation/coretext/kfontsanskritlanguage)
- [var kFontSerbianLanguage: Int](/documentation/coretext/kfontserbianlanguage)
- [var kFontSimpChineseLanguage: Int](/documentation/coretext/kfontsimpchineselanguage)
- [var kFontSimpleChineseScript: Int](/documentation/coretext/kfontsimplechinesescript)
- [var kFontSindhiLanguage: Int](/documentation/coretext/kfontsindhilanguage)
- [var kFontSindhiScript: Int](/documentation/coretext/kfontsindhiscript)
- [var kFontSinhaleseLanguage: Int](/documentation/coretext/kfontsinhaleselanguage)
- [var kFontSinhaleseScript: Int](/documentation/coretext/kfontsinhalesescript)
- [var kFontSlavicScript: Int](/documentation/coretext/kfontslavicscript)
- [var kFontSlovakLanguage: Int](/documentation/coretext/kfontslovaklanguage)
- [var kFontSlovenianLanguage: Int](/documentation/coretext/kfontslovenianlanguage)
- [var kFontSomaliLanguage: Int](/documentation/coretext/kfontsomalilanguage)
- [var kFontSpanishLanguage: Int](/documentation/coretext/kfontspanishlanguage)
- [var kFontStyleName: Int](/documentation/coretext/kfontstylename)
- [var kFontSundaneseRomLanguage: Int](/documentation/coretext/kfontsundaneseromlanguage)
- [var kFontSwahiliLanguage: Int](/documentation/coretext/kfontswahililanguage)
- [var kFontSwedishLanguage: Int](/documentation/coretext/kfontswedishlanguage)
- [var kFontTagalogLanguage: Int](/documentation/coretext/kfonttagaloglanguage)
- [var kFontTajikiLanguage: Int](/documentation/coretext/kfonttajikilanguage)
- [var kFontTamilLanguage: Int](/documentation/coretext/kfonttamillanguage)
- [var kFontTamilScript: Int](/documentation/coretext/kfonttamilscript)
- [var kFontTatarLanguage: Int](/documentation/coretext/kfonttatarlanguage)
- [var kFontTeluguLanguage: Int](/documentation/coretext/kfonttelugulanguage)
- [var kFontTeluguScript: Int](/documentation/coretext/kfontteluguscript)
- [var kFontThaiLanguage: Int](/documentation/coretext/kfontthailanguage)
- [var kFontThaiScript: Int](/documentation/coretext/kfontthaiscript)
- [var kFontTibetanLanguage: Int](/documentation/coretext/kfonttibetanlanguage)
- [var kFontTibetanScript: Int](/documentation/coretext/kfonttibetanscript)
- [var kFontTigrinyaLanguage: Int](/documentation/coretext/kfonttigrinyalanguage)
- [var kFontTradChineseLanguage: Int](/documentation/coretext/kfonttradchineselanguage)
- [var kFontTrademarkName: Int](/documentation/coretext/kfonttrademarkname)
- [var kFontTraditionalChineseScript: Int](/documentation/coretext/kfonttraditionalchinesescript)
- [var kFontTurkishLanguage: Int](/documentation/coretext/kfontturkishlanguage)
- [var kFontTurkmenLanguage: Int](/documentation/coretext/kfontturkmenlanguage)
- [var kFontUighurLanguage: Int](/documentation/coretext/kfontuighurlanguage)
- [var kFontUkrainianLanguage: Int](/documentation/coretext/kfontukrainianlanguage)
- [var kFontUnicodeDefaultSemantics: Int](/documentation/coretext/kfontunicodedefaultsemantics)
- [var kFontUnicodePlatform: Int](/documentation/coretext/kfontunicodeplatform)
- [var kFontUnicodeV1_1Semantics: Int](/documentation/coretext/kfontunicodev1_1semantics)
- [var kFontUnicodeV2_0BMPOnlySemantics: Int](/documentation/coretext/kfontunicodev2_0bmponlysemantics)
- [var kFontUnicodeV2_0FullCoverageSemantics: Int](/documentation/coretext/kfontunicodev2_0fullcoveragesemantics)
- [var kFontUnicodeV4_0VariationSequenceSemantics: Int](/documentation/coretext/kfontunicodev4_0variationsequencesemantics)
- [var kFontUnicode_FullRepertoire: Int](/documentation/coretext/kfontunicode_fullrepertoire)
- [var kFontUninterpretedScript: Int](/documentation/coretext/kfontuninterpretedscript)
- [var kFontUniqueName: Int](/documentation/coretext/kfontuniquename)
- [var kFontUrduLanguage: Int](/documentation/coretext/kfonturdulanguage)
- [var kFontUzbekLanguage: Int](/documentation/coretext/kfontuzbeklanguage)
- [var kFontVendorURLName: Int](/documentation/coretext/kfontvendorurlname)
- [var kFontVersionName: Int](/documentation/coretext/kfontversionname)
- [var kFontVietnameseLanguage: Int](/documentation/coretext/kfontvietnameselanguage)
- [var kFontVietnameseScript: Int](/documentation/coretext/kfontvietnamesescript)
- [var kFontWelshLanguage: Int](/documentation/coretext/kfontwelshlanguage)
- [var kFontYiddishLanguage: Int](/documentation/coretext/kfontyiddishlanguage)
- [var kFormInterrobangOffSelector: Int](/documentation/coretext/kforminterrobangoffselector)
- [var kFormInterrobangOnSelector: Int](/documentation/coretext/kforminterrobangonselector)
- [var kFractionsType: Int](/documentation/coretext/kfractionstype)
- [var kFullWidthCJKRomanSelector: Int](/documentation/coretext/kfullwidthcjkromanselector)
- [var kFullWidthIdeographsSelector: Int](/documentation/coretext/kfullwidthideographsselector)
- [var kFullWidthKanaSelector: Int](/documentation/coretext/kfullwidthkanaselector)
- [var kHalfWidthCJKRomanSelector: Int](/documentation/coretext/khalfwidthcjkromanselector)
- [var kHalfWidthIdeographsSelector: Int](/documentation/coretext/khalfwidthideographsselector)
- [var kHalfWidthTextSelector: Int](/documentation/coretext/khalfwidthtextselector)
- [var kHanjaToHangulAltOneSelector: Int](/documentation/coretext/khanjatohangulaltoneselector)
- [var kHanjaToHangulAltThreeSelector: Int](/documentation/coretext/khanjatohangulaltthreeselector)
- [var kHanjaToHangulAltTwoSelector: Int](/documentation/coretext/khanjatohangulalttwoselector)
- [var kHanjaToHangulSelector: Int](/documentation/coretext/khanjatohangulselector)
- [var kHideDiacriticsSelector: Int](/documentation/coretext/khidediacriticsselector)
- [var kHiraganaToKatakanaSelector: Int](/documentation/coretext/khiraganatokatakanaselector)
- [var kHistoricalLigaturesOffSelector: Int](/documentation/coretext/khistoricalligaturesoffselector)
- [var kHistoricalLigaturesOnSelector: Int](/documentation/coretext/khistoricalligaturesonselector)
- [var kHojoCharactersSelector: Int](/documentation/coretext/khojocharactersselector)
- [var kHyphenToEnDashOffSelector: Int](/documentation/coretext/khyphentoendashoffselector)
- [var kHyphenToEnDashOnSelector: Int](/documentation/coretext/khyphentoendashonselector)
- [var kHyphenToMinusOffSelector: Int](/documentation/coretext/khyphentominusoffselector)
- [var kHyphenToMinusOnSelector: Int](/documentation/coretext/khyphentominusonselector)
- [var kHyphensToEmDashOffSelector: Int](/documentation/coretext/khyphenstoemdashoffselector)
- [var kHyphensToEmDashOnSelector: Int](/documentation/coretext/khyphenstoemdashonselector)
- [var kIdeographicAltFiveSelector: Int](/documentation/coretext/kideographicaltfiveselector)
- [var kIdeographicAltFourSelector: Int](/documentation/coretext/kideographicaltfourselector)
- [var kIdeographicAltOneSelector: Int](/documentation/coretext/kideographicaltoneselector)
- [var kIdeographicAltThreeSelector: Int](/documentation/coretext/kideographicaltthreeselector)
- [var kIdeographicAltTwoSelector: Int](/documentation/coretext/kideographicalttwoselector)
- [var kIdeographicAlternativesType: Int](/documentation/coretext/kideographicalternativestype)
- [var kIdeographicSpacingType: Int](/documentation/coretext/kideographicspacingtype)
- [var kIlluminatedCapsSelector: Int](/documentation/coretext/killuminatedcapsselector)
- [var kInequalityLigaturesOffSelector: Int](/documentation/coretext/kinequalityligaturesoffselector)
- [var kInequalityLigaturesOnSelector: Int](/documentation/coretext/kinequalityligaturesonselector)
- [var kInferiorsSelector: Int](/documentation/coretext/kinferiorsselector)
- [var kInitialCapsAndSmallCapsSelector: Int](/documentation/coretext/kinitialcapsandsmallcapsselector)
- [var kInitialCapsSelector: Int](/documentation/coretext/kinitialcapsselector)
- [var kInternationalSymbolsSelector: Int](/documentation/coretext/kinternationalsymbolsselector)
- [var kInvertedBoxAnnotationSelector: Int](/documentation/coretext/kinvertedboxannotationselector)
- [var kInvertedCircleAnnotationSelector: Int](/documentation/coretext/kinvertedcircleannotationselector)
- [var kInvertedRoundedBoxAnnotationSelector: Int](/documentation/coretext/kinvertedroundedboxannotationselector)
- [var kItalicCJKRomanType: Int](/documentation/coretext/kitaliccjkromantype)
- [var kJIS1978CharactersSelector: Int](/documentation/coretext/kjis1978charactersselector)
- [var kJIS1983CharactersSelector: Int](/documentation/coretext/kjis1983charactersselector)
- [var kJIS1990CharactersSelector: Int](/documentation/coretext/kjis1990charactersselector)
- [var kJIS2004CharactersSelector: Int](/documentation/coretext/kjis2004charactersselector)
- [var kJUSTCurrentVersion: Int](/documentation/coretext/kjustcurrentversion)
- [var kJUSTKashidaPriority: Int](/documentation/coretext/kjustkashidapriority)
- [var kJUSTLetterPriority: Int](/documentation/coretext/kjustletterpriority)
- [var kJUSTNullPriority: Int](/documentation/coretext/kjustnullpriority)
- [var kJUSTOverrideLimits: Int](/documentation/coretext/kjustoverridelimits)
- [var kJUSTOverridePriority: Int](/documentation/coretext/kjustoverridepriority)
- [var kJUSTOverrideUnlimited: Int](/documentation/coretext/kjustoverrideunlimited)
- [var kJUSTPriorityCount: Int](/documentation/coretext/kjustprioritycount)
- [var kJUSTPriorityMask: Int](/documentation/coretext/kjustprioritymask)
- [var kJUSTSpacePriority: Int](/documentation/coretext/kjustspacepriority)
- [var kJUSTStandardFormat: Int](/documentation/coretext/kjuststandardformat)
- [var kJUSTTag: Int](/documentation/coretext/kjusttag)
- [var kJUSTUnlimited: Int](/documentation/coretext/kjustunlimited)
- [var kJUSTnoGlyphcode: Int](/documentation/coretext/kjustnoglyphcode)
- [var kJUSTpcConditionalAddAction: Int](/documentation/coretext/kjustpcconditionaladdaction)
- [var kJUSTpcDecompositionAction: Int](/documentation/coretext/kjustpcdecompositionaction)
- [var kJUSTpcDuctilityAction: Int](/documentation/coretext/kjustpcductilityaction)
- [var kJUSTpcGlyphRepeatAddAction: Int](/documentation/coretext/kjustpcglyphrepeataddaction)
- [var kJUSTpcGlyphStretchAction: Int](/documentation/coretext/kjustpcglyphstretchaction)
- [var kJUSTpcUnconditionalAddAction: Int](/documentation/coretext/kjustpcunconditionaladdaction)
- [var kKERNCrossStream: Int](/documentation/coretext/kkerncrossstream)
- [var kKERNCrossStreamResetNote: Int](/documentation/coretext/kkerncrossstreamresetnote)
- [var kKERNCurrentVersion: Int](/documentation/coretext/kkerncurrentversion)
- [var kKERNFormatMask: Int](/documentation/coretext/kkernformatmask)
- [var kKERNIndexArray: Int](/documentation/coretext/kkernindexarray)
- [var kKERNLineEndKerning: Int](/documentation/coretext/kkernlineendkerning)
- [var kKERNLineStart: Int](/documentation/coretext/kkernlinestart)
- [var kKERNNoCrossKerning: Int](/documentation/coretext/kkernnocrosskerning)
- [var kKERNNoStakeNote: Int](/documentation/coretext/kkernnostakenote)
- [var kKERNNotApplied: Int](/documentation/coretext/kkernnotapplied)
- [var kKERNNotesRequested: Int](/documentation/coretext/kkernnotesrequested)
- [var kKERNOrderedList: Int](/documentation/coretext/kkernorderedlist)
- [var kKERNResetCrossStream: Int](/documentation/coretext/kkernresetcrossstream)
- [var kKERNSimpleArray: Int](/documentation/coretext/kkernsimplearray)
- [var kKERNStateTable: Int](/documentation/coretext/kkernstatetable)
- [var kKERNTag: Int](/documentation/coretext/kkerntag)
- [var kKERNUnusedBits: Int](/documentation/coretext/kkernunusedbits)
- [var kKERNVariation: Int](/documentation/coretext/kkernvariation)
- [var kKERNVertical: Int](/documentation/coretext/kkernvertical)
- [var kKERXActionOffsetMask: UInt32](/documentation/coretext/kkerxactionoffsetmask)
- [var kKERXActionTypeAnchorPoints: UInt32](/documentation/coretext/kkerxactiontypeanchorpoints)
- [var kKERXActionTypeControlPoints: UInt32](/documentation/coretext/kkerxactiontypecontrolpoints)
- [var kKERXActionTypeCoordinates: UInt32](/documentation/coretext/kkerxactiontypecoordinates)
- [var kKERXActionTypeMask: UInt32](/documentation/coretext/kkerxactiontypemask)
- [var kKERXControlPoint: Int](/documentation/coretext/kkerxcontrolpoint)
- [var kKERXCrossStream: Int](/documentation/coretext/kkerxcrossstream)
- [var kKERXCrossStreamResetNote: Int](/documentation/coretext/kkerxcrossstreamresetnote)
- [var kKERXCurrentVersion: Int](/documentation/coretext/kkerxcurrentversion)
- [var kKERXFormatMask: Int](/documentation/coretext/kkerxformatmask)
- [var kKERXIndexArray: Int](/documentation/coretext/kkerxindexarray)
- [var kKERXLineEndKerning: Int](/documentation/coretext/kkerxlineendkerning)
- [var kKERXLineStart: Int](/documentation/coretext/kkerxlinestart)
- [var kKERXNoCrossKerning: Int](/documentation/coretext/kkerxnocrosskerning)
- [var kKERXNoStakeNote: Int](/documentation/coretext/kkerxnostakenote)
- [var kKERXNotApplied: Int](/documentation/coretext/kkerxnotapplied)
- [var kKERXNotesRequested: Int](/documentation/coretext/kkerxnotesrequested)
- [var kKERXOrderedList: Int](/documentation/coretext/kkerxorderedlist)
- [var kKERXResetCrossStream: Int](/documentation/coretext/kkerxresetcrossstream)
- [var kKERXSimpleArray: Int](/documentation/coretext/kkerxsimplearray)
- [var kKERXStateTable: Int](/documentation/coretext/kkerxstatetable)
- [var kKERXTag: Int](/documentation/coretext/kkerxtag)
- [var kKERXUnusedBits: Int](/documentation/coretext/kkerxunusedbits)
- [var kKERXUnusedFlags: UInt32](/documentation/coretext/kkerxunusedflags)
- [var kKERXVariation: Int](/documentation/coretext/kkerxvariation)
- [var kKERXVertical: Int](/documentation/coretext/kkerxvertical)
- [var kKanaSpacingType: Int](/documentation/coretext/kkanaspacingtype)
- [var kKanaToRomanizationSelector: Int](/documentation/coretext/kkanatoromanizationselector)
- [var kKatakanaToHiraganaSelector: Int](/documentation/coretext/kkatakanatohiraganaselector)
- [var kLCARCtlPointFormat: Int](/documentation/coretext/klcarctlpointformat)
- [var kLCARCurrentVersion: Int](/documentation/coretext/klcarcurrentversion)
- [var kLCARLinearFormat: Int](/documentation/coretext/klcarlinearformat)
- [var kLCARTag: Int](/documentation/coretext/klcartag)
- [var kLastFeatureType: Int](/documentation/coretext/klastfeaturetype)
- [var kLetterCaseType: Int](/documentation/coretext/klettercasetype)
- [var kLigaturesType: Int](/documentation/coretext/kligaturestype)
- [var kLineFinalSwashesOffSelector: Int](/documentation/coretext/klinefinalswashesoffselector)
- [var kLineFinalSwashesOnSelector: Int](/documentation/coretext/klinefinalswashesonselector)
- [var kLineInitialSwashesOffSelector: Int](/documentation/coretext/klineinitialswashesoffselector)
- [var kLineInitialSwashesOnSelector: Int](/documentation/coretext/klineinitialswashesonselector)
- [var kLinguisticRearrangementOffSelector: Int](/documentation/coretext/klinguisticrearrangementoffselector)
- [var kLinguisticRearrangementOnSelector: Int](/documentation/coretext/klinguisticrearrangementonselector)
- [var kLinguisticRearrangementType: Int](/documentation/coretext/klinguisticrearrangementtype)
- [var kLogosOffSelector: Int](/documentation/coretext/klogosoffselector)
- [var kLogosOnSelector: Int](/documentation/coretext/klogosonselector)
- [var kLowerCaseNumbersSelector: Int](/documentation/coretext/klowercasenumbersselector)
- [var kLowerCasePetiteCapsSelector: Int](/documentation/coretext/klowercasepetitecapsselector)
- [var kLowerCaseSmallCapsSelector: Int](/documentation/coretext/klowercasesmallcapsselector)
- [var kLowerCaseType: Int](/documentation/coretext/klowercasetype)
- [var kMORTContextualType: Int](/documentation/coretext/kmortcontextualtype)
- [var kMORTCoverDescending: Int](/documentation/coretext/kmortcoverdescending)
- [var kMORTCoverIgnoreVertical: Int](/documentation/coretext/kmortcoverignorevertical)
- [var kMORTCoverTypeMask: Int](/documentation/coretext/kmortcovertypemask)
- [var kMORTCoverVertical: Int](/documentation/coretext/kmortcoververtical)
- [var kMORTCurrInsertBefore: Int](/documentation/coretext/kmortcurrinsertbefore)
- [var kMORTCurrInsertCountMask: Int](/documentation/coretext/kmortcurrinsertcountmask)
- [var kMORTCurrInsertCountShift: Int](/documentation/coretext/kmortcurrinsertcountshift)
- [var kMORTCurrInsertKashidaLike: Int](/documentation/coretext/kmortcurrinsertkashidalike)
- [var kMORTCurrJustTableCountMask: Int](/documentation/coretext/kmortcurrjusttablecountmask)
- [var kMORTCurrJustTableCountShift: Int](/documentation/coretext/kmortcurrjusttablecountshift)
- [var kMORTCurrentVersion: Int](/documentation/coretext/kmortcurrentversion)
- [var kMORTDoInsertionsBefore: Int](/documentation/coretext/kmortdoinsertionsbefore)
- [var kMORTInsertionType: Int](/documentation/coretext/kmortinsertiontype)
- [var kMORTInsertionsCountMask: Int](/documentation/coretext/kmortinsertionscountmask)
- [var kMORTIsSplitVowelPiece: Int](/documentation/coretext/kmortissplitvowelpiece)
- [var kMORTLigFormOffsetMask: Int](/documentation/coretext/kmortligformoffsetmask)
- [var kMORTLigFormOffsetShift: Int](/documentation/coretext/kmortligformoffsetshift)
- [var kMORTLigLastAction: Int](/documentation/coretext/kmortliglastaction)
- [var kMORTLigStoreLigature: Int](/documentation/coretext/kmortligstoreligature)
- [var kMORTLigatureType: Int](/documentation/coretext/kmortligaturetype)
- [var kMORTMarkInsertBefore: Int](/documentation/coretext/kmortmarkinsertbefore)
- [var kMORTMarkInsertCountMask: Int](/documentation/coretext/kmortmarkinsertcountmask)
- [var kMORTMarkInsertCountShift: Int](/documentation/coretext/kmortmarkinsertcountshift)
- [var kMORTMarkInsertKashidaLike: Int](/documentation/coretext/kmortmarkinsertkashidalike)
- [var kMORTMarkJustTableCountMask: Int](/documentation/coretext/kmortmarkjusttablecountmask)
- [var kMORTMarkJustTableCountShift: Int](/documentation/coretext/kmortmarkjusttablecountshift)
- [var kMORTRearrangementType: Int](/documentation/coretext/kmortrearrangementtype)
- [var kMORTSwashType: Int](/documentation/coretext/kmortswashtype)
- [var kMORTTag: Int](/documentation/coretext/kmorttag)
- [var kMORTraCDx: Int](/documentation/coretext/kmortracdx)
- [var kMORTraCDxA: Int](/documentation/coretext/kmortracdxa)
- [var kMORTraCDxAB: Int](/documentation/coretext/kmortracdxab)
- [var kMORTraCDxBA: Int](/documentation/coretext/kmortracdxba)
- [var kMORTraDCx: Int](/documentation/coretext/kmortradcx)
- [var kMORTraDCxA: Int](/documentation/coretext/kmortradcxa)
- [var kMORTraDCxAB: Int](/documentation/coretext/kmortradcxab)
- [var kMORTraDCxBA: Int](/documentation/coretext/kmortradcxba)
- [var kMORTraDx: Int](/documentation/coretext/kmortradx)
- [var kMORTraDxA: Int](/documentation/coretext/kmortradxa)
- [var kMORTraDxAB: Int](/documentation/coretext/kmortradxab)
- [var kMORTraDxBA: Int](/documentation/coretext/kmortradxba)
- [var kMORTraNoAction: Int](/documentation/coretext/kmortranoaction)
- [var kMORTraxA: Int](/documentation/coretext/kmortraxa)
- [var kMORTraxAB: Int](/documentation/coretext/kmortraxab)
- [var kMORTraxBA: Int](/documentation/coretext/kmortraxba)
- [var kMORXCoverDescending: Int](/documentation/coretext/kmorxcoverdescending)
- [var kMORXCoverIgnoreVertical: Int](/documentation/coretext/kmorxcoverignorevertical)
- [var kMORXCoverTypeMask: Int](/documentation/coretext/kmorxcovertypemask)
- [var kMORXCoverVertical: Int](/documentation/coretext/kmorxcoververtical)
- [var kMORXCurrentVersion: Int](/documentation/coretext/kmorxcurrentversion)
- [var kMORXTag: Int](/documentation/coretext/kmorxtag)
- [var kMathSymbolsSelector: Int](/documentation/coretext/kmathsymbolsselector)
- [var kMathematicalExtrasType: Int](/documentation/coretext/kmathematicalextrastype)
- [var kMathematicalGreekOffSelector: Int](/documentation/coretext/kmathematicalgreekoffselector)
- [var kMathematicalGreekOnSelector: Int](/documentation/coretext/kmathematicalgreekonselector)
- [var kMonospacedNumbersSelector: Int](/documentation/coretext/kmonospacednumbersselector)
- [var kMonospacedTextSelector: Int](/documentation/coretext/kmonospacedtextselector)
- [var kNLCCharactersSelector: Int](/documentation/coretext/knlccharactersselector)
- [var kNoAlternatesSelector: Int](/documentation/coretext/knoalternatesselector)
- [var kNoAnnotationSelector: Int](/documentation/coretext/knoannotationselector)
- [var kNoCJKItalicRomanSelector: Int](/documentation/coretext/knocjkitalicromanselector)
- [var kNoCJKSymbolAlternativesSelector: Int](/documentation/coretext/knocjksymbolalternativesselector)
- [var kNoFractionsSelector: Int](/documentation/coretext/knofractionsselector)
- [var kNoIdeographicAlternativesSelector: Int](/documentation/coretext/knoideographicalternativesselector)
- [var kNoOrnamentsSelector: Int](/documentation/coretext/knoornamentsselector)
- [var kNoRubyKanaSelector: Int](/documentation/coretext/knorubykanaselector)
- [var kNoStyleOptionsSelector: Int](/documentation/coretext/knostyleoptionsselector)
- [var kNoStylisticAlternatesSelector: Int](/documentation/coretext/knostylisticalternatesselector)
- [var kNoTransliterationSelector: Int](/documentation/coretext/knotransliterationselector)
- [var kNonFinalSwashesOffSelector: Int](/documentation/coretext/knonfinalswashesoffselector)
- [var kNonFinalSwashesOnSelector: Int](/documentation/coretext/knonfinalswashesonselector)
- [var kNormalPositionSelector: Int](/documentation/coretext/knormalpositionselector)
- [var kNumberCaseType: Int](/documentation/coretext/knumbercasetype)
- [var kNumberSpacingType: Int](/documentation/coretext/knumberspacingtype)
- [var kOPBDControlPointFormat: Int](/documentation/coretext/kopbdcontrolpointformat)
- [var kOPBDCurrentVersion: Int](/documentation/coretext/kopbdcurrentversion)
- [var kOPBDDistanceFormat: Int](/documentation/coretext/kopbddistanceformat)
- [var kOPBDTag: Int](/documentation/coretext/kopbdtag)
- [var kOrdinalsSelector: Int](/documentation/coretext/kordinalsselector)
- [var kOrnamentSetsType: Int](/documentation/coretext/kornamentsetstype)
- [var kOverlappingCharactersType: Int](/documentation/coretext/koverlappingcharacterstype)
- [var kPROPALDirectionClass: Int](/documentation/coretext/kpropaldirectionclass)
- [var kPROPANDirectionClass: Int](/documentation/coretext/kpropandirectionclass)
- [var kPROPBNDirectionClass: Int](/documentation/coretext/kpropbndirectionclass)
- [var kPROPCSDirectionClass: Int](/documentation/coretext/kpropcsdirectionclass)
- [var kPROPCanHangLTMask: Int](/documentation/coretext/kpropcanhangltmask)
- [var kPROPCanHangRBMask: Int](/documentation/coretext/kpropcanhangrbmask)
- [var kPROPCurrentVersion: Int](/documentation/coretext/kpropcurrentversion)
- [var kPROPDirectionMask: Int](/documentation/coretext/kpropdirectionmask)
- [var kPROPENDirectionClass: Int](/documentation/coretext/kpropendirectionclass)
- [var kPROPESDirectionClass: Int](/documentation/coretext/kpropesdirectionclass)
- [var kPROPETDirectionClass: Int](/documentation/coretext/kpropetdirectionclass)
- [var kPROPIsFloaterMask: Int](/documentation/coretext/kpropisfloatermask)
- [var kPROPLDirectionClass: Int](/documentation/coretext/kpropldirectionclass)
- [var kPROPLREDirectionClass: Int](/documentation/coretext/kproplredirectionclass)
- [var kPROPLRODirectionClass: Int](/documentation/coretext/kproplrodirectionclass)
- [var kPROPNSMDirectionClass: Int](/documentation/coretext/kpropnsmdirectionclass)
- [var kPROPNumDirectionClasses: Int](/documentation/coretext/kpropnumdirectionclasses)
- [var kPROPONDirectionClass: Int](/documentation/coretext/kpropondirectionclass)
- [var kPROPPDFDirectionClass: Int](/documentation/coretext/kproppdfdirectionclass)
- [var kPROPPSDirectionClass: Int](/documentation/coretext/kproppsdirectionclass)
- [var kPROPPairOffsetMask: Int](/documentation/coretext/kproppairoffsetmask)
- [var kPROPPairOffsetShift: Int](/documentation/coretext/kproppairoffsetshift)
- [var kPROPPairOffsetSign: Int](/documentation/coretext/kproppairoffsetsign)
- [var kPROPRDirectionClass: Int](/documentation/coretext/kproprdirectionclass)
- [var kPROPRLEDirectionClass: Int](/documentation/coretext/kproprledirectionclass)
- [var kPROPRLODirectionClass: Int](/documentation/coretext/kproprlodirectionclass)
- [var kPROPRightConnectMask: Int](/documentation/coretext/kproprightconnectmask)
- [var kPROPSDirectionClass: Int](/documentation/coretext/kpropsdirectionclass)
- [var kPROPSENDirectionClass: Int](/documentation/coretext/kpropsendirectionclass)
- [var kPROPTag: Int](/documentation/coretext/kproptag)
- [var kPROPUseRLPairMask: Int](/documentation/coretext/kpropuserlpairmask)
- [var kPROPWSDirectionClass: Int](/documentation/coretext/kpropwsdirectionclass)
- [var kPROPZeroReserved: Int](/documentation/coretext/kpropzeroreserved)
- [var kParenthesisAnnotationSelector: Int](/documentation/coretext/kparenthesisannotationselector)
- [var kPartiallyConnectedSelector: Int](/documentation/coretext/kpartiallyconnectedselector)
- [var kPeriodAnnotationSelector: Int](/documentation/coretext/kperiodannotationselector)
- [var kPeriodsToEllipsisOffSelector: Int](/documentation/coretext/kperiodstoellipsisoffselector)
- [var kPeriodsToEllipsisOnSelector: Int](/documentation/coretext/kperiodstoellipsisonselector)
- [var kPiCharactersSelector: Int](/documentation/coretext/kpicharactersselector)
- [var kPreventOverlapOffSelector: Int](/documentation/coretext/kpreventoverlapoffselector)
- [var kPreventOverlapOnSelector: Int](/documentation/coretext/kpreventoverlaponselector)
- [var kProportionalCJKRomanSelector: Int](/documentation/coretext/kproportionalcjkromanselector)
- [var kProportionalIdeographsSelector: Int](/documentation/coretext/kproportionalideographsselector)
- [var kProportionalKanaSelector: Int](/documentation/coretext/kproportionalkanaselector)
- [var kProportionalNumbersSelector: Int](/documentation/coretext/kproportionalnumbersselector)
- [var kProportionalTextSelector: Int](/documentation/coretext/kproportionaltextselector)
- [var kQuarterWidthNumbersSelector: Int](/documentation/coretext/kquarterwidthnumbersselector)
- [var kQuarterWidthTextSelector: Int](/documentation/coretext/kquarterwidthtextselector)
- [var kRareLigaturesOffSelector: Int](/documentation/coretext/krareligaturesoffselector)
- [var kRareLigaturesOnSelector: Int](/documentation/coretext/krareligaturesonselector)
- [var kRebusPicturesOffSelector: Int](/documentation/coretext/krebuspicturesoffselector)
- [var kRebusPicturesOnSelector: Int](/documentation/coretext/krebuspicturesonselector)
- [var kRequiredLigaturesOffSelector: Int](/documentation/coretext/krequiredligaturesoffselector)
- [var kRequiredLigaturesOnSelector: Int](/documentation/coretext/krequiredligaturesonselector)
- [var kRomanNumeralAnnotationSelector: Int](/documentation/coretext/kromannumeralannotationselector)
- [var kRomanizationToHiraganaSelector: Int](/documentation/coretext/kromanizationtohiraganaselector)
- [var kRomanizationToKatakanaSelector: Int](/documentation/coretext/kromanizationtokatakanaselector)
- [var kRoundedBoxAnnotationSelector: Int](/documentation/coretext/kroundedboxannotationselector)
- [var kRubyKanaOffSelector: Int](/documentation/coretext/krubykanaoffselector)
- [var kRubyKanaOnSelector: Int](/documentation/coretext/krubykanaonselector)
- [var kRubyKanaSelector: Int](/documentation/coretext/krubykanaselector)
- [var kRubyKanaType: Int](/documentation/coretext/krubykanatype)
- [var kSFNTLookupSegmentArray: Int](/documentation/coretext/ksfntlookupsegmentarray)
- [var kSFNTLookupSegmentSingle: Int](/documentation/coretext/ksfntlookupsegmentsingle)
- [var kSFNTLookupSimpleArray: Int](/documentation/coretext/ksfntlookupsimplearray)
- [var kSFNTLookupSingleTable: Int](/documentation/coretext/ksfntlookupsingletable)
- [var kSFNTLookupTrimmedArray: Int](/documentation/coretext/ksfntlookuptrimmedarray)
- [var kSFNTLookupVector: Int](/documentation/coretext/ksfntlookupvector)
- [var kSTClassDeletedGlyph: Int](/documentation/coretext/kstclassdeletedglyph)
- [var kSTClassEndOfLine: Int](/documentation/coretext/kstclassendofline)
- [var kSTClassEndOfText: Int](/documentation/coretext/kstclassendoftext)
- [var kSTClassOutOfBounds: Int](/documentation/coretext/kstclassoutofbounds)
- [var kSTLigActionMask: Int](/documentation/coretext/kstligactionmask)
- [var kSTMarkEnd: Int](/documentation/coretext/kstmarkend)
- [var kSTNoAdvance: Int](/documentation/coretext/kstnoadvance)
- [var kSTRearrVerbMask: Int](/documentation/coretext/kstrearrverbmask)
- [var kSTSetMark: Int](/documentation/coretext/kstsetmark)
- [var kSTXHasLigAction: Int](/documentation/coretext/kstxhasligaction)
- [var kScientificInferiorsSelector: Int](/documentation/coretext/kscientificinferiorsselector)
- [var kShowDiacriticsSelector: Int](/documentation/coretext/kshowdiacriticsselector)
- [var kSimplifiedCharactersSelector: Int](/documentation/coretext/ksimplifiedcharactersselector)
- [var kSlashToDivideOffSelector: Int](/documentation/coretext/kslashtodivideoffselector)
- [var kSlashToDivideOnSelector: Int](/documentation/coretext/kslashtodivideonselector)
- [var kSlashedZeroOffSelector: Int](/documentation/coretext/kslashedzerooffselector)
- [var kSlashedZeroOnSelector: Int](/documentation/coretext/kslashedzeroonselector)
- [var kSmallCapsSelector: Int](/documentation/coretext/ksmallcapsselector)
- [var kSmartQuotesOffSelector: Int](/documentation/coretext/ksmartquotesoffselector)
- [var kSmartQuotesOnSelector: Int](/documentation/coretext/ksmartquotesonselector)
- [var kSmartSwashType: Int](/documentation/coretext/ksmartswashtype)
- [var kSquaredLigaturesOffSelector: Int](/documentation/coretext/ksquaredligaturesoffselector)
- [var kSquaredLigaturesOnSelector: Int](/documentation/coretext/ksquaredligaturesonselector)
- [var kStyleOptionsType: Int](/documentation/coretext/kstyleoptionstype)
- [var kStylisticAltEightOffSelector: Int](/documentation/coretext/kstylisticalteightoffselector)
- [var kStylisticAltEightOnSelector: Int](/documentation/coretext/kstylisticalteightonselector)
- [var kStylisticAltEighteenOffSelector: Int](/documentation/coretext/kstylisticalteighteenoffselector)
- [var kStylisticAltEighteenOnSelector: Int](/documentation/coretext/kstylisticalteighteenonselector)
- [var kStylisticAltElevenOffSelector: Int](/documentation/coretext/kstylisticaltelevenoffselector)
- [var kStylisticAltElevenOnSelector: Int](/documentation/coretext/kstylisticaltelevenonselector)
- [var kStylisticAltFifteenOffSelector: Int](/documentation/coretext/kstylisticaltfifteenoffselector)
- [var kStylisticAltFifteenOnSelector: Int](/documentation/coretext/kstylisticaltfifteenonselector)
- [var kStylisticAltFiveOffSelector: Int](/documentation/coretext/kstylisticaltfiveoffselector)
- [var kStylisticAltFiveOnSelector: Int](/documentation/coretext/kstylisticaltfiveonselector)
- [var kStylisticAltFourOffSelector: Int](/documentation/coretext/kstylisticaltfouroffselector)
- [var kStylisticAltFourOnSelector: Int](/documentation/coretext/kstylisticaltfouronselector)
- [var kStylisticAltFourteenOffSelector: Int](/documentation/coretext/kstylisticaltfourteenoffselector)
- [var kStylisticAltFourteenOnSelector: Int](/documentation/coretext/kstylisticaltfourteenonselector)
- [var kStylisticAltNineOffSelector: Int](/documentation/coretext/kstylisticaltnineoffselector)
- [var kStylisticAltNineOnSelector: Int](/documentation/coretext/kstylisticaltnineonselector)
- [var kStylisticAltNineteenOffSelector: Int](/documentation/coretext/kstylisticaltnineteenoffselector)
- [var kStylisticAltNineteenOnSelector: Int](/documentation/coretext/kstylisticaltnineteenonselector)
- [var kStylisticAltOneOffSelector: Int](/documentation/coretext/kstylisticaltoneoffselector)
- [var kStylisticAltOneOnSelector: Int](/documentation/coretext/kstylisticaltoneonselector)
- [var kStylisticAltSevenOffSelector: Int](/documentation/coretext/kstylisticaltsevenoffselector)
- [var kStylisticAltSevenOnSelector: Int](/documentation/coretext/kstylisticaltsevenonselector)
- [var kStylisticAltSeventeenOffSelector: Int](/documentation/coretext/kstylisticaltseventeenoffselector)
- [var kStylisticAltSeventeenOnSelector: Int](/documentation/coretext/kstylisticaltseventeenonselector)
- [var kStylisticAltSixOffSelector: Int](/documentation/coretext/kstylisticaltsixoffselector)
- [var kStylisticAltSixOnSelector: Int](/documentation/coretext/kstylisticaltsixonselector)
- [var kStylisticAltSixteenOffSelector: Int](/documentation/coretext/kstylisticaltsixteenoffselector)
- [var kStylisticAltSixteenOnSelector: Int](/documentation/coretext/kstylisticaltsixteenonselector)
- [var kStylisticAltTenOffSelector: Int](/documentation/coretext/kstylisticalttenoffselector)
- [var kStylisticAltTenOnSelector: Int](/documentation/coretext/kstylisticalttenonselector)
- [var kStylisticAltThirteenOffSelector: Int](/documentation/coretext/kstylisticaltthirteenoffselector)
- [var kStylisticAltThirteenOnSelector: Int](/documentation/coretext/kstylisticaltthirteenonselector)
- [var kStylisticAltThreeOffSelector: Int](/documentation/coretext/kstylisticaltthreeoffselector)
- [var kStylisticAltThreeOnSelector: Int](/documentation/coretext/kstylisticaltthreeonselector)
- [var kStylisticAltTwelveOffSelector: Int](/documentation/coretext/kstylisticalttwelveoffselector)
- [var kStylisticAltTwelveOnSelector: Int](/documentation/coretext/kstylisticalttwelveonselector)
- [var kStylisticAltTwentyOffSelector: Int](/documentation/coretext/kstylisticalttwentyoffselector)
- [var kStylisticAltTwentyOnSelector: Int](/documentation/coretext/kstylisticalttwentyonselector)
- [var kStylisticAltTwoOffSelector: Int](/documentation/coretext/kstylisticalttwooffselector)
- [var kStylisticAltTwoOnSelector: Int](/documentation/coretext/kstylisticalttwoonselector)
- [var kStylisticAlternativesType: Int](/documentation/coretext/kstylisticalternativestype)
- [var kSubstituteVerticalFormsOffSelector: Int](/documentation/coretext/ksubstituteverticalformsoffselector)
- [var kSubstituteVerticalFormsOnSelector: Int](/documentation/coretext/ksubstituteverticalformsonselector)
- [var kSuperiorsSelector: Int](/documentation/coretext/ksuperiorsselector)
- [var kSwashAlternatesOffSelector: Int](/documentation/coretext/kswashalternatesoffselector)
- [var kSwashAlternatesOnSelector: Int](/documentation/coretext/kswashalternatesonselector)
- [var kSymbolLigaturesOffSelector: Int](/documentation/coretext/ksymbolligaturesoffselector)
- [var kSymbolLigaturesOnSelector: Int](/documentation/coretext/ksymbolligaturesonselector)
- [var kTRAKCurrentVersion: Int](/documentation/coretext/ktrakcurrentversion)
- [var kTRAKTag: Int](/documentation/coretext/ktraktag)
- [var kTRAKUniformFormat: Int](/documentation/coretext/ktrakuniformformat)
- [var kTallCapsSelector: Int](/documentation/coretext/ktallcapsselector)
- [var kTextSpacingType: Int](/documentation/coretext/ktextspacingtype)
- [var kThirdWidthNumbersSelector: Int](/documentation/coretext/kthirdwidthnumbersselector)
- [var kThirdWidthTextSelector: Int](/documentation/coretext/kthirdwidthtextselector)
- [var kTitlingCapsSelector: Int](/documentation/coretext/ktitlingcapsselector)
- [var kTraditionalAltFiveSelector: Int](/documentation/coretext/ktraditionalaltfiveselector)
- [var kTraditionalAltFourSelector: Int](/documentation/coretext/ktraditionalaltfourselector)
- [var kTraditionalAltOneSelector: Int](/documentation/coretext/ktraditionalaltoneselector)
- [var kTraditionalAltThreeSelector: Int](/documentation/coretext/ktraditionalaltthreeselector)
- [var kTraditionalAltTwoSelector: Int](/documentation/coretext/ktraditionalalttwoselector)
- [var kTraditionalCharactersSelector: Int](/documentation/coretext/ktraditionalcharactersselector)
- [var kTraditionalNamesCharactersSelector: Int](/documentation/coretext/ktraditionalnamescharactersselector)
- [var kTranscodingCompositionOffSelector: Int](/documentation/coretext/ktranscodingcompositionoffselector)
- [var kTranscodingCompositionOnSelector: Int](/documentation/coretext/ktranscodingcompositiononselector)
- [var kTransliterationType: Int](/documentation/coretext/ktransliterationtype)
- [var kTypographicExtrasType: Int](/documentation/coretext/ktypographicextrastype)
- [var kUnconnectedSelector: Int](/documentation/coretext/kunconnectedselector)
- [var kUnicodeDecompositionType: Int](/documentation/coretext/kunicodedecompositiontype)
- [var kUpperAndLowerCaseSelector: Int](/documentation/coretext/kupperandlowercaseselector)
- [var kUpperCaseNumbersSelector: Int](/documentation/coretext/kuppercasenumbersselector)
- [var kUpperCasePetiteCapsSelector: Int](/documentation/coretext/kuppercasepetitecapsselector)
- [var kUpperCaseSmallCapsSelector: Int](/documentation/coretext/kuppercasesmallcapsselector)
- [var kUpperCaseType: Int](/documentation/coretext/kuppercasetype)
- [var kVerticalFractionsSelector: Int](/documentation/coretext/kverticalfractionsselector)
- [var kVerticalPositionType: Int](/documentation/coretext/kverticalpositiontype)
- [var kVerticalSubstitutionType: Int](/documentation/coretext/kverticalsubstitutiontype)
- [var kWordFinalSwashesOffSelector: Int](/documentation/coretext/kwordfinalswashesoffselector)
- [var kWordFinalSwashesOnSelector: Int](/documentation/coretext/kwordfinalswashesonselector)
- [var kWordInitialSwashesOffSelector: Int](/documentation/coretext/kwordinitialswashesoffselector)
- [var kWordInitialSwashesOnSelector: Int](/documentation/coretext/kwordinitialswashesonselector)
- [var nameFontTableTag: Int](/documentation/coretext/namefonttabletag)
- [var nonGlyphID: Int](/documentation/coretext/nonglyphid)
- [var os2FontTableTag: Int](/documentation/coretext/os2fonttabletag)
- [var sizeof_sfntCMapEncoding: Int](/documentation/coretext/sizeof_sfntcmapencoding)
- [var sizeof_sfntCMapExtendedSubHeader: Int](/documentation/coretext/sizeof_sfntcmapextendedsubheader)
- [var sizeof_sfntCMapHeader: Int](/documentation/coretext/sizeof_sfntcmapheader)
- [var sizeof_sfntCMapSubHeader: Int](/documentation/coretext/sizeof_sfntcmapsubheader)
- [var sizeof_sfntDescriptorHeader: Int](/documentation/coretext/sizeof_sfntdescriptorheader)
- [var sizeof_sfntDirectory: Int](/documentation/coretext/sizeof_sfntdirectory)
- [var sizeof_sfntInstance: Int](/documentation/coretext/sizeof_sfntinstance)
- [var sizeof_sfntNameHeader: Int](/documentation/coretext/sizeof_sfntnameheader)
- [var sizeof_sfntNameRecord: Int](/documentation/coretext/sizeof_sfntnamerecord)
- [var sizeof_sfntVariationAxis: Int](/documentation/coretext/sizeof_sfntvariationaxis)
- [var sizeof_sfntVariationHeader: Int](/documentation/coretext/sizeof_sfntvariationheader)
- [var variationFontTableTag: Int](/documentation/coretext/variationfonttabletag)

## Macros

- [Macros](/documentation/coretext/coretext-macros)

## Classes

- [CTRubyAnnotation](/documentation/coretext/ctrubyannotation)

## Protocols

- [CTAdaptiveImageProviding](/documentation/coretext/ctadaptiveimageproviding)

### Instance Methods

- [func image(forProposedSize: CGSize, scaleFactor: CGFloat, imageOffset: UnsafeMutablePointer<CGPoint>, imageSize: UnsafeMutablePointer<CGSize>) -> CGImage?](/documentation/coretext/ctadaptiveimageproviding/image(forproposedsize:scalefactor:imageoffset:imagesize:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
