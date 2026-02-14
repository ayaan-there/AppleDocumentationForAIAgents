# Latent Semantic Mapping Documentation

Source: https://sosumi.ai/documentation/latentsemanticmapping

---
title: Latent Semantic Mapping
source: https://developer.apple.com/documentation/latentsemanticmapping
timestamp: 2026-02-13T18:58:38.597Z
---

## Text Classification

- [LSMMap](/documentation/latentsemanticmapping/lsmmap)

### Creating a Map

- [func LSMMapCreate(CFAllocator?, CFOptionFlags) -> Unmanaged<LSMMap>](/documentation/latentsemanticmapping/lsmmapcreate(_:_:))
- [Map Flags](/documentation/latentsemanticmapping/map-flags)

#### Constants

- [var kLSMMapPairs: Int](/documentation/latentsemanticmapping/klsmmappairs)
- [var kLSMMapTriplets: Int](/documentation/latentsemanticmapping/klsmmaptriplets)
- [var kLSMMapHashText: Int](/documentation/latentsemanticmapping/klsmmaphashtext)

### Managing a Map’s Properties

- [func LSMMapSetProperties(LSMMap, CFDictionary)](/documentation/latentsemanticmapping/lsmmapsetproperties(_:_:))
- [func LSMMapGetProperties(LSMMap) -> Unmanaged<CFDictionary>](/documentation/latentsemanticmapping/lsmmapgetproperties(_:))
- [Map Properties](/documentation/latentsemanticmapping/map-properties)

#### Properties

- [var kLSMAlgorithmKey: String](/documentation/latentsemanticmapping/klsmalgorithmkey)
- [var kLSMAlgorithmDense: String](/documentation/latentsemanticmapping/klsmalgorithmdense)
- [var kLSMAlgorithmSparse: String](/documentation/latentsemanticmapping/klsmalgorithmsparse)
- [var kLSMPrecisionKey: String](/documentation/latentsemanticmapping/klsmprecisionkey)
- [var kLSMPrecisionFloat: String](/documentation/latentsemanticmapping/klsmprecisionfloat)
- [var kLSMPrecisionDouble: String](/documentation/latentsemanticmapping/klsmprecisiondouble)
- [var kLSMDimensionKey: String](/documentation/latentsemanticmapping/klsmdimensionkey)
- [var kLSMIterationsKey: String](/documentation/latentsemanticmapping/klsmiterationskey)
- [var kLSMSweepAgeKey: String](/documentation/latentsemanticmapping/klsmsweepagekey)
- [var kLSMSweepCutoffKey: String](/documentation/latentsemanticmapping/klsmsweepcutoffkey)

### Starting Training Mode

- [func LSMMapStartTraining(LSMMap) -> OSStatus](/documentation/latentsemanticmapping/lsmmapstarttraining(_:))
- [func LSMMapAddCategory(LSMMap) -> LSMCategory](/documentation/latentsemanticmapping/lsmmapaddcategory(_:))
- [func LSMMapGetCategoryCount(LSMMap) -> CFIndex](/documentation/latentsemanticmapping/lsmmapgetcategorycount(_:))
- [func LSMMapSetStopWords(LSMMap, LSMText) -> OSStatus](/documentation/latentsemanticmapping/lsmmapsetstopwords(_:_:))
- [func LSMMapAddText(LSMMap, LSMText, LSMCategory) -> OSStatus](/documentation/latentsemanticmapping/lsmmapaddtext(_:_:_:))
- [func LSMMapAddTextWithWeight(LSMMap, LSMText, LSMCategory, Float) -> OSStatus](/documentation/latentsemanticmapping/lsmmapaddtextwithweight(_:_:_:_:))
- [LSMCategory](/documentation/latentsemanticmapping/lsmcategory)

### Starting Classification Mode

- [func LSMMapCompile(LSMMap) -> OSStatus](/documentation/latentsemanticmapping/lsmmapcompile(_:))
- [func LSMMapCreateClusters(CFAllocator?, LSMMap, CFArray?, CFIndex, CFOptionFlags) -> Unmanaged<CFArray>?](/documentation/latentsemanticmapping/lsmmapcreateclusters(_:_:_:_:_:))
- [Clustering Flags](/documentation/latentsemanticmapping/clustering-flags)

#### Constants

- [var kLSMClusterCategories: Int](/documentation/latentsemanticmapping/klsmclustercategories)
- [var kLSMClusterWords: Int](/documentation/latentsemanticmapping/klsmclusterwords)
- [var kLSMClusterTokens: Int](/documentation/latentsemanticmapping/klsmclustertokens)
- [var kLSMClusterKMeans: Int](/documentation/latentsemanticmapping/klsmclusterkmeans)
- [var kLSMClusterAgglomerative: Int](/documentation/latentsemanticmapping/klsmclusteragglomerative)
- [func LSMMapApplyClusters(LSMMap, CFArray) -> OSStatus](/documentation/latentsemanticmapping/lsmmapapplyclusters(_:_:))

### Loading and Saving a Map

- [func LSMMapCreateFromURL(CFAllocator?, CFURL, CFOptionFlags) -> Unmanaged<LSMMap>?](/documentation/latentsemanticmapping/lsmmapcreatefromurl(_:_:_:))
- [func LSMMapWriteToURL(LSMMap, CFURL, CFOptionFlags) -> OSStatus](/documentation/latentsemanticmapping/lsmmapwritetourl(_:_:_:))
- [func LSMMapWriteToStream(LSMMap, LSMText?, CFWriteStream, CFOptionFlags) -> OSStatus](/documentation/latentsemanticmapping/lsmmapwritetostream(_:_:_:_:))
- [Storage Flags](/documentation/latentsemanticmapping/storage-flags)

#### Constants

- [var kLSMMapDiscardCounts: Int](/documentation/latentsemanticmapping/klsmmapdiscardcounts)
- [var kLSMMapLoadMutable: Int](/documentation/latentsemanticmapping/klsmmaploadmutable)
- [var kLSMMapHashText: Int](/documentation/latentsemanticmapping/klsmmaphashtext)

### Getting the Type Identifier

- [func LSMMapGetTypeID() -> CFTypeID](/documentation/latentsemanticmapping/lsmmapgettypeid())
- [LSMText](/documentation/latentsemanticmapping/lsmtext)

### Creating a Text Object

- [func LSMTextCreate(CFAllocator?, LSMMap) -> Unmanaged<LSMText>](/documentation/latentsemanticmapping/lsmtextcreate(_:_:))

### Adding to the Text

- [func LSMTextAddToken(LSMText, CFData) -> OSStatus](/documentation/latentsemanticmapping/lsmtextaddtoken(_:_:))
- [func LSMTextAddWord(LSMText, CFString) -> OSStatus](/documentation/latentsemanticmapping/lsmtextaddword(_:_:))
- [func LSMTextAddWords(LSMText, CFString, CFLocale?, CFOptionFlags) -> OSStatus](/documentation/latentsemanticmapping/lsmtextaddwords(_:_:_:_:))
- [Parsing Flags](/documentation/latentsemanticmapping/parsing-flags)

#### Constants

- [var kLSMTextApplySpamHeuristics: Int](/documentation/latentsemanticmapping/klsmtextapplyspamheuristics)
- [var kLSMTextPreserveAcronyms: Int](/documentation/latentsemanticmapping/klsmtextpreserveacronyms)
- [var kLSMTextPreserveCase: Int](/documentation/latentsemanticmapping/klsmtextpreservecase)

### Getting the Type Identifier

- [func LSMTextGetTypeID() -> CFTypeID](/documentation/latentsemanticmapping/lsmtextgettypeid())
- [LSMResult](/documentation/latentsemanticmapping/lsmresult)

### Creating a Result

- [func LSMResultCreate(CFAllocator?, LSMMap, LSMText, CFIndex, CFOptionFlags) -> Unmanaged<LSMResult>](/documentation/latentsemanticmapping/lsmresultcreate(_:_:_:_:_:))
- [Result Flags](/documentation/latentsemanticmapping/result-flags)

#### Constants

- [var kLSMResultBestWords: Int](/documentation/latentsemanticmapping/klsmresultbestwords)

### Querying Result Information

- [func LSMResultGetCount(LSMResult) -> CFIndex](/documentation/latentsemanticmapping/lsmresultgetcount(_:))
- [func LSMResultGetCategory(LSMResult, CFIndex) -> LSMCategory](/documentation/latentsemanticmapping/lsmresultgetcategory(_:_:))
- [func LSMResultGetScore(LSMResult, CFIndex) -> Float](/documentation/latentsemanticmapping/lsmresultgetscore(_:_:))

### Getting a Result

- [func LSMResultCopyToken(LSMResult, CFIndex) -> Unmanaged<CFData>?](/documentation/latentsemanticmapping/lsmresultcopytoken(_:_:))
- [func LSMResultCopyTokenCluster(LSMResult, CFIndex) -> Unmanaged<CFArray>?](/documentation/latentsemanticmapping/lsmresultcopytokencluster(_:_:))
- [func LSMResultCopyWord(LSMResult, CFIndex) -> Unmanaged<CFString>?](/documentation/latentsemanticmapping/lsmresultcopyword(_:_:))
- [func LSMResultCopyWordCluster(LSMResult, CFIndex) -> Unmanaged<CFArray>?](/documentation/latentsemanticmapping/lsmresultcopywordcluster(_:_:))

### Getting the Type Identifier

- [func LSMResultGetTypeID() -> CFTypeID](/documentation/latentsemanticmapping/lsmresultgettypeid())

## Error Handling

- [Error Codes](/documentation/latentsemanticmapping/error-codes)

### Errors

- [var kLSMMapOutOfState: Int](/documentation/latentsemanticmapping/klsmmapoutofstate)
- [var kLSMMapNoSuchCategory: Int](/documentation/latentsemanticmapping/klsmmapnosuchcategory)
- [var kLSMMapWriteError: Int](/documentation/latentsemanticmapping/klsmmapwriteerror)
- [var kLSMMapBadPath: Int](/documentation/latentsemanticmapping/klsmmapbadpath)
- [var kLSMMapBadCluster: Int](/documentation/latentsemanticmapping/klsmmapbadcluster)
- [var kLSMMapOverflow: Int](/documentation/latentsemanticmapping/klsmmapoverflow)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
