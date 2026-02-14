# Synchronization Documentation

Source: https://sosumi.ai/documentation/synchronization

---
title: Synchronization
source: https://developer.apple.com/documentation/synchronization
timestamp: 2026-02-13T19:02:48.158Z
---

## Atomic Values

- [Atomic](/documentation/synchronization/atomic)

### Initializers

- [init(consuming Value)](/documentation/synchronization/atomic/init(_:))

### Instance Methods

- [func add(UInt128, ordering: AtomicUpdateOrdering) -> (oldValue: UInt128, newValue: UInt128)](/documentation/synchronization/atomic/add(_:ordering:)-1k1sq)
- [func add(Int16, ordering: AtomicUpdateOrdering) -> (oldValue: Int16, newValue: Int16)](/documentation/synchronization/atomic/add(_:ordering:)-34u14)
- [func add(UInt32, ordering: AtomicUpdateOrdering) -> (oldValue: UInt32, newValue: UInt32)](/documentation/synchronization/atomic/add(_:ordering:)-39vk1)
- [func add(UInt64, ordering: AtomicUpdateOrdering) -> (oldValue: UInt64, newValue: UInt64)](/documentation/synchronization/atomic/add(_:ordering:)-4dpjd)
- [func add(UInt16, ordering: AtomicUpdateOrdering) -> (oldValue: UInt16, newValue: UInt16)](/documentation/synchronization/atomic/add(_:ordering:)-4ocr0)
- [func add(Int8, ordering: AtomicUpdateOrdering) -> (oldValue: Int8, newValue: Int8)](/documentation/synchronization/atomic/add(_:ordering:)-6rhji)
- [func add(Int64, ordering: AtomicUpdateOrdering) -> (oldValue: Int64, newValue: Int64)](/documentation/synchronization/atomic/add(_:ordering:)-7ws8q)
- [func add(UInt8, ordering: AtomicUpdateOrdering) -> (oldValue: UInt8, newValue: UInt8)](/documentation/synchronization/atomic/add(_:ordering:)-8cc78)
- [func add(UInt, ordering: AtomicUpdateOrdering) -> (oldValue: UInt, newValue: UInt)](/documentation/synchronization/atomic/add(_:ordering:)-8xoe3)
- [func add(Int128, ordering: AtomicUpdateOrdering) -> (oldValue: Int128, newValue: Int128)](/documentation/synchronization/atomic/add(_:ordering:)-90njk)
- [func add(Int, ordering: AtomicUpdateOrdering) -> (oldValue: Int, newValue: Int)](/documentation/synchronization/atomic/add(_:ordering:)-97ilu)
- [func add(Int32, ordering: AtomicUpdateOrdering) -> (oldValue: Int32, newValue: Int32)](/documentation/synchronization/atomic/add(_:ordering:)-vm4c)
- [func bitwiseAnd(UInt128, ordering: AtomicUpdateOrdering) -> (oldValue: UInt128, newValue: UInt128)](/documentation/synchronization/atomic/bitwiseand(_:ordering:)-1baj3)
- [func bitwiseAnd(UInt16, ordering: AtomicUpdateOrdering) -> (oldValue: UInt16, newValue: UInt16)](/documentation/synchronization/atomic/bitwiseand(_:ordering:)-1gzwl)
- [func bitwiseAnd(Int8, ordering: AtomicUpdateOrdering) -> (oldValue: Int8, newValue: Int8)](/documentation/synchronization/atomic/bitwiseand(_:ordering:)-1yz1m)
- [func bitwiseAnd(Int16, ordering: AtomicUpdateOrdering) -> (oldValue: Int16, newValue: Int16)](/documentation/synchronization/atomic/bitwiseand(_:ordering:)-3zt46)
- [func bitwiseAnd(Int64, ordering: AtomicUpdateOrdering) -> (oldValue: Int64, newValue: Int64)](/documentation/synchronization/atomic/bitwiseand(_:ordering:)-4db7m)
- [func bitwiseAnd(Int128, ordering: AtomicUpdateOrdering) -> (oldValue: Int128, newValue: Int128)](/documentation/synchronization/atomic/bitwiseand(_:ordering:)-56lhq)
- [func bitwiseAnd(UInt32, ordering: AtomicUpdateOrdering) -> (oldValue: UInt32, newValue: UInt32)](/documentation/synchronization/atomic/bitwiseand(_:ordering:)-5iaoz)
- [func bitwiseAnd(Int, ordering: AtomicUpdateOrdering) -> (oldValue: Int, newValue: Int)](/documentation/synchronization/atomic/bitwiseand(_:ordering:)-5m0jk)
- [func bitwiseAnd(UInt, ordering: AtomicUpdateOrdering) -> (oldValue: UInt, newValue: UInt)](/documentation/synchronization/atomic/bitwiseand(_:ordering:)-5mhgj)
- [func bitwiseAnd(UInt64, ordering: AtomicUpdateOrdering) -> (oldValue: UInt64, newValue: UInt64)](/documentation/synchronization/atomic/bitwiseand(_:ordering:)-6mxdg)
- [func bitwiseAnd(Int32, ordering: AtomicUpdateOrdering) -> (oldValue: Int32, newValue: Int32)](/documentation/synchronization/atomic/bitwiseand(_:ordering:)-8ilt7)
- [func bitwiseAnd(UInt8, ordering: AtomicUpdateOrdering) -> (oldValue: UInt8, newValue: UInt8)](/documentation/synchronization/atomic/bitwiseand(_:ordering:)-l1a3)
- [func bitwiseOr(Int32, ordering: AtomicUpdateOrdering) -> (oldValue: Int32, newValue: Int32)](/documentation/synchronization/atomic/bitwiseor(_:ordering:)-206dk)
- [func bitwiseOr(Int64, ordering: AtomicUpdateOrdering) -> (oldValue: Int64, newValue: Int64)](/documentation/synchronization/atomic/bitwiseor(_:ordering:)-39r9q)
- [func bitwiseOr(UInt64, ordering: AtomicUpdateOrdering) -> (oldValue: UInt64, newValue: UInt64)](/documentation/synchronization/atomic/bitwiseor(_:ordering:)-4ozz5)
- [func bitwiseOr(UInt8, ordering: AtomicUpdateOrdering) -> (oldValue: UInt8, newValue: UInt8)](/documentation/synchronization/atomic/bitwiseor(_:ordering:)-4q8ef)
- [func bitwiseOr(Int128, ordering: AtomicUpdateOrdering) -> (oldValue: Int128, newValue: Int128)](/documentation/synchronization/atomic/bitwiseor(_:ordering:)-4y864)
- [func bitwiseOr(UInt128, ordering: AtomicUpdateOrdering) -> (oldValue: UInt128, newValue: UInt128)](/documentation/synchronization/atomic/bitwiseor(_:ordering:)-5574x)
- [func bitwiseOr(UInt16, ordering: AtomicUpdateOrdering) -> (oldValue: UInt16, newValue: UInt16)](/documentation/synchronization/atomic/bitwiseor(_:ordering:)-6fz7a)
- [func bitwiseOr(UInt, ordering: AtomicUpdateOrdering) -> (oldValue: UInt, newValue: UInt)](/documentation/synchronization/atomic/bitwiseor(_:ordering:)-6zz2p)
- [func bitwiseOr(Int, ordering: AtomicUpdateOrdering) -> (oldValue: Int, newValue: Int)](/documentation/synchronization/atomic/bitwiseor(_:ordering:)-72403)
- [func bitwiseOr(UInt32, ordering: AtomicUpdateOrdering) -> (oldValue: UInt32, newValue: UInt32)](/documentation/synchronization/atomic/bitwiseor(_:ordering:)-84e8q)
- [func bitwiseOr(Int16, ordering: AtomicUpdateOrdering) -> (oldValue: Int16, newValue: Int16)](/documentation/synchronization/atomic/bitwiseor(_:ordering:)-9191v)
- [func bitwiseOr(Int8, ordering: AtomicUpdateOrdering) -> (oldValue: Int8, newValue: Int8)](/documentation/synchronization/atomic/bitwiseor(_:ordering:)-aa7f)
- [func bitwiseXor(UInt128, ordering: AtomicUpdateOrdering) -> (oldValue: UInt128, newValue: UInt128)](/documentation/synchronization/atomic/bitwisexor(_:ordering:)-271x9)
- [func bitwiseXor(Int16, ordering: AtomicUpdateOrdering) -> (oldValue: Int16, newValue: Int16)](/documentation/synchronization/atomic/bitwisexor(_:ordering:)-2vrf)
- [func bitwiseXor(UInt32, ordering: AtomicUpdateOrdering) -> (oldValue: UInt32, newValue: UInt32)](/documentation/synchronization/atomic/bitwisexor(_:ordering:)-33l7y)
- [func bitwiseXor(Int, ordering: AtomicUpdateOrdering) -> (oldValue: Int, newValue: Int)](/documentation/synchronization/atomic/bitwisexor(_:ordering:)-4umey)
- [func bitwiseXor(UInt, ordering: AtomicUpdateOrdering) -> (oldValue: UInt, newValue: UInt)](/documentation/synchronization/atomic/bitwisexor(_:ordering:)-5df6p)
- [func bitwiseXor(Int8, ordering: AtomicUpdateOrdering) -> (oldValue: Int8, newValue: Int8)](/documentation/synchronization/atomic/bitwisexor(_:ordering:)-5vpxh)
- [func bitwiseXor(UInt16, ordering: AtomicUpdateOrdering) -> (oldValue: UInt16, newValue: UInt16)](/documentation/synchronization/atomic/bitwisexor(_:ordering:)-5zfc)
- [func bitwiseXor(Int128, ordering: AtomicUpdateOrdering) -> (oldValue: Int128, newValue: Int128)](/documentation/synchronization/atomic/bitwisexor(_:ordering:)-8t1qf)
- [func bitwiseXor(UInt64, ordering: AtomicUpdateOrdering) -> (oldValue: UInt64, newValue: UInt64)](/documentation/synchronization/atomic/bitwisexor(_:ordering:)-9l5qb)
- [func bitwiseXor(Int32, ordering: AtomicUpdateOrdering) -> (oldValue: Int32, newValue: Int32)](/documentation/synchronization/atomic/bitwisexor(_:ordering:)-9xi4f)
- [func bitwiseXor(UInt8, ordering: AtomicUpdateOrdering) -> (oldValue: UInt8, newValue: UInt8)](/documentation/synchronization/atomic/bitwisexor(_:ordering:)-m4nt)
- [func bitwiseXor(Int64, ordering: AtomicUpdateOrdering) -> (oldValue: Int64, newValue: Int64)](/documentation/synchronization/atomic/bitwisexor(_:ordering:)-sf4i)
- [func compareExchange(expected: consuming Value, desired: consuming Value, ordering: AtomicUpdateOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/compareexchange(expected:desired:ordering:)-33pf3)
- [func compareExchange(expected: consuming Value, desired: consuming Value, ordering: AtomicUpdateOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/compareexchange(expected:desired:ordering:)-6rsfl)
- [func compareExchange(expected: consuming Value, desired: consuming Value, ordering: AtomicUpdateOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/compareexchange(expected:desired:ordering:)-8uimm)
- [func compareExchange(expected: consuming Value, desired: consuming Value, ordering: AtomicUpdateOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/compareexchange(expected:desired:ordering:)-9bh60)
- [func compareExchange(expected: consuming Value, desired: consuming Value, ordering: AtomicUpdateOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/compareexchange(expected:desired:ordering:)-s52j)
- [func compareExchange(expected: consuming Value, desired: consuming Value, successOrdering: AtomicUpdateOrdering, failureOrdering: AtomicLoadOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/compareexchange(expected:desired:successordering:failureordering:)-5obt4)
- [func compareExchange(expected: consuming Value, desired: consuming Value, successOrdering: AtomicUpdateOrdering, failureOrdering: AtomicLoadOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/compareexchange(expected:desired:successordering:failureordering:)-7msfy)
- [func compareExchange(expected: consuming Value, desired: consuming Value, successOrdering: AtomicUpdateOrdering, failureOrdering: AtomicLoadOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/compareexchange(expected:desired:successordering:failureordering:)-82j0l)
- [func compareExchange(expected: consuming Value, desired: consuming Value, successOrdering: AtomicUpdateOrdering, failureOrdering: AtomicLoadOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/compareexchange(expected:desired:successordering:failureordering:)-8d36a)
- [func compareExchange(expected: consuming Value, desired: consuming Value, successOrdering: AtomicUpdateOrdering, failureOrdering: AtomicLoadOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/compareexchange(expected:desired:successordering:failureordering:)-cve0)
- [func exchange(consuming Value, ordering: AtomicUpdateOrdering) -> Value](/documentation/synchronization/atomic/exchange(_:ordering:)-5n6sy)
- [func exchange(consuming Value, ordering: AtomicUpdateOrdering) -> Value](/documentation/synchronization/atomic/exchange(_:ordering:)-8ip0d)
- [func exchange(consuming Value, ordering: AtomicUpdateOrdering) -> Value](/documentation/synchronization/atomic/exchange(_:ordering:)-9kb4s)
- [func exchange(consuming Value, ordering: AtomicUpdateOrdering) -> Value](/documentation/synchronization/atomic/exchange(_:ordering:)-9y5j8)
- [func exchange(consuming Value, ordering: AtomicUpdateOrdering) -> Value](/documentation/synchronization/atomic/exchange(_:ordering:)-ycta)
- [func load(ordering: AtomicLoadOrdering) -> Value](/documentation/synchronization/atomic/load(ordering:)-2u27y)
- [func load(ordering: AtomicLoadOrdering) -> Value](/documentation/synchronization/atomic/load(ordering:)-2v8gp)
- [func load(ordering: AtomicLoadOrdering) -> Value](/documentation/synchronization/atomic/load(ordering:)-3u18o)
- [func load(ordering: AtomicLoadOrdering) -> Value](/documentation/synchronization/atomic/load(ordering:)-4mv5b)
- [func load(ordering: AtomicLoadOrdering) -> Value](/documentation/synchronization/atomic/load(ordering:)-8ufx2)
- [func logicalAnd(Bool, ordering: AtomicUpdateOrdering) -> (oldValue: Bool, newValue: Bool)](/documentation/synchronization/atomic/logicaland(_:ordering:))
- [func logicalOr(Bool, ordering: AtomicUpdateOrdering) -> (oldValue: Bool, newValue: Bool)](/documentation/synchronization/atomic/logicalor(_:ordering:))
- [func logicalXor(Bool, ordering: AtomicUpdateOrdering) -> (oldValue: Bool, newValue: Bool)](/documentation/synchronization/atomic/logicalxor(_:ordering:))
- [func max(Int16, ordering: AtomicUpdateOrdering) -> (oldValue: Int16, newValue: Int16)](/documentation/synchronization/atomic/max(_:ordering:)-1l8lv)
- [func max(UInt, ordering: AtomicUpdateOrdering) -> (oldValue: UInt, newValue: UInt)](/documentation/synchronization/atomic/max(_:ordering:)-32cin)
- [func max(Int128, ordering: AtomicUpdateOrdering) -> (oldValue: Int128, newValue: Int128)](/documentation/synchronization/atomic/max(_:ordering:)-4e4mn)
- [func max(Int64, ordering: AtomicUpdateOrdering) -> (oldValue: Int64, newValue: Int64)](/documentation/synchronization/atomic/max(_:ordering:)-4rq6h)
- [func max(UInt128, ordering: AtomicUpdateOrdering) -> (oldValue: UInt128, newValue: UInt128)](/documentation/synchronization/atomic/max(_:ordering:)-5qqv7)
- [func max(UInt64, ordering: AtomicUpdateOrdering) -> (oldValue: UInt64, newValue: UInt64)](/documentation/synchronization/atomic/max(_:ordering:)-681q1)
- [func max(Int32, ordering: AtomicUpdateOrdering) -> (oldValue: Int32, newValue: Int32)](/documentation/synchronization/atomic/max(_:ordering:)-7kusb)
- [func max(UInt32, ordering: AtomicUpdateOrdering) -> (oldValue: UInt32, newValue: UInt32)](/documentation/synchronization/atomic/max(_:ordering:)-7qnkd)
- [func max(UInt8, ordering: AtomicUpdateOrdering) -> (oldValue: UInt8, newValue: UInt8)](/documentation/synchronization/atomic/max(_:ordering:)-7z7ub)
- [func max(Int, ordering: AtomicUpdateOrdering) -> (oldValue: Int, newValue: Int)](/documentation/synchronization/atomic/max(_:ordering:)-81jab)
- [func max(UInt16, ordering: AtomicUpdateOrdering) -> (oldValue: UInt16, newValue: UInt16)](/documentation/synchronization/atomic/max(_:ordering:)-957na)
- [func max(Int8, ordering: AtomicUpdateOrdering) -> (oldValue: Int8, newValue: Int8)](/documentation/synchronization/atomic/max(_:ordering:)-xy7u)
- [func min(Int, ordering: AtomicUpdateOrdering) -> (oldValue: Int, newValue: Int)](/documentation/synchronization/atomic/min(_:ordering:)-1uwzs)
- [func min(UInt64, ordering: AtomicUpdateOrdering) -> (oldValue: UInt64, newValue: UInt64)](/documentation/synchronization/atomic/min(_:ordering:)-2l64c)
- [func min(Int32, ordering: AtomicUpdateOrdering) -> (oldValue: Int32, newValue: Int32)](/documentation/synchronization/atomic/min(_:ordering:)-39r27)
- [func min(UInt8, ordering: AtomicUpdateOrdering) -> (oldValue: UInt8, newValue: UInt8)](/documentation/synchronization/atomic/min(_:ordering:)-3tiyt)
- [func min(UInt128, ordering: AtomicUpdateOrdering) -> (oldValue: UInt128, newValue: UInt128)](/documentation/synchronization/atomic/min(_:ordering:)-3tk2x)
- [func min(UInt32, ordering: AtomicUpdateOrdering) -> (oldValue: UInt32, newValue: UInt32)](/documentation/synchronization/atomic/min(_:ordering:)-4b62m)
- [func min(Int64, ordering: AtomicUpdateOrdering) -> (oldValue: Int64, newValue: Int64)](/documentation/synchronization/atomic/min(_:ordering:)-4wv9d)
- [func min(Int128, ordering: AtomicUpdateOrdering) -> (oldValue: Int128, newValue: Int128)](/documentation/synchronization/atomic/min(_:ordering:)-6bbf1)
- [func min(Int16, ordering: AtomicUpdateOrdering) -> (oldValue: Int16, newValue: Int16)](/documentation/synchronization/atomic/min(_:ordering:)-6ivky)
- [func min(Int8, ordering: AtomicUpdateOrdering) -> (oldValue: Int8, newValue: Int8)](/documentation/synchronization/atomic/min(_:ordering:)-73283)
- [func min(UInt16, ordering: AtomicUpdateOrdering) -> (oldValue: UInt16, newValue: UInt16)](/documentation/synchronization/atomic/min(_:ordering:)-8k42m)
- [func min(UInt, ordering: AtomicUpdateOrdering) -> (oldValue: UInt, newValue: UInt)](/documentation/synchronization/atomic/min(_:ordering:)-yogw)
- [func store(consuming Value, ordering: AtomicStoreOrdering)](/documentation/synchronization/atomic/store(_:ordering:)-195np)
- [func store(consuming Value, ordering: AtomicStoreOrdering)](/documentation/synchronization/atomic/store(_:ordering:)-22zxw)
- [func store(consuming Value, ordering: AtomicStoreOrdering)](/documentation/synchronization/atomic/store(_:ordering:)-532ut)
- [func store(consuming Value, ordering: AtomicStoreOrdering)](/documentation/synchronization/atomic/store(_:ordering:)-5q2fi)
- [func store(consuming Value, ordering: AtomicStoreOrdering)](/documentation/synchronization/atomic/store(_:ordering:)-97ua7)
- [func subtract(UInt128, ordering: AtomicUpdateOrdering) -> (oldValue: UInt128, newValue: UInt128)](/documentation/synchronization/atomic/subtract(_:ordering:)-1atf4)
- [func subtract(Int, ordering: AtomicUpdateOrdering) -> (oldValue: Int, newValue: Int)](/documentation/synchronization/atomic/subtract(_:ordering:)-1iop7)
- [func subtract(Int128, ordering: AtomicUpdateOrdering) -> (oldValue: Int128, newValue: Int128)](/documentation/synchronization/atomic/subtract(_:ordering:)-2ddui)
- [func subtract(UInt64, ordering: AtomicUpdateOrdering) -> (oldValue: UInt64, newValue: UInt64)](/documentation/synchronization/atomic/subtract(_:ordering:)-2ds2s)
- [func subtract(UInt32, ordering: AtomicUpdateOrdering) -> (oldValue: UInt32, newValue: UInt32)](/documentation/synchronization/atomic/subtract(_:ordering:)-3c2nm)
- [func subtract(Int8, ordering: AtomicUpdateOrdering) -> (oldValue: Int8, newValue: Int8)](/documentation/synchronization/atomic/subtract(_:ordering:)-47p0x)
- [func subtract(UInt8, ordering: AtomicUpdateOrdering) -> (oldValue: UInt8, newValue: UInt8)](/documentation/synchronization/atomic/subtract(_:ordering:)-5rq0s)
- [func subtract(UInt16, ordering: AtomicUpdateOrdering) -> (oldValue: UInt16, newValue: UInt16)](/documentation/synchronization/atomic/subtract(_:ordering:)-65sge)
- [func subtract(Int64, ordering: AtomicUpdateOrdering) -> (oldValue: Int64, newValue: Int64)](/documentation/synchronization/atomic/subtract(_:ordering:)-6eidf)
- [func subtract(Int32, ordering: AtomicUpdateOrdering) -> (oldValue: Int32, newValue: Int32)](/documentation/synchronization/atomic/subtract(_:ordering:)-7ebxd)
- [func subtract(Int16, ordering: AtomicUpdateOrdering) -> (oldValue: Int16, newValue: Int16)](/documentation/synchronization/atomic/subtract(_:ordering:)-9w06o)
- [func subtract(UInt, ordering: AtomicUpdateOrdering) -> (oldValue: UInt, newValue: UInt)](/documentation/synchronization/atomic/subtract(_:ordering:)-pqxe)
- [func weakCompareExchange(expected: consuming Value, desired: consuming Value, ordering: AtomicUpdateOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/weakcompareexchange(expected:desired:ordering:)-24bnb)
- [func weakCompareExchange(expected: consuming Value, desired: consuming Value, ordering: AtomicUpdateOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/weakcompareexchange(expected:desired:ordering:)-728eh)
- [func weakCompareExchange(expected: consuming Value, desired: consuming Value, ordering: AtomicUpdateOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/weakcompareexchange(expected:desired:ordering:)-72wpg)
- [func weakCompareExchange(expected: consuming Value, desired: consuming Value, ordering: AtomicUpdateOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/weakcompareexchange(expected:desired:ordering:)-9w8ty)
- [func weakCompareExchange(expected: consuming Value, desired: consuming Value, ordering: AtomicUpdateOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/weakcompareexchange(expected:desired:ordering:)-9xqnl)
- [func weakCompareExchange(expected: consuming Value, desired: consuming Value, successOrdering: AtomicUpdateOrdering, failureOrdering: AtomicLoadOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/weakcompareexchange(expected:desired:successordering:failureordering:)-2ywaz)
- [func weakCompareExchange(expected: consuming Value, desired: consuming Value, successOrdering: AtomicUpdateOrdering, failureOrdering: AtomicLoadOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/weakcompareexchange(expected:desired:successordering:failureordering:)-3p8t6)
- [func weakCompareExchange(expected: consuming Value, desired: consuming Value, successOrdering: AtomicUpdateOrdering, failureOrdering: AtomicLoadOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/weakcompareexchange(expected:desired:successordering:failureordering:)-7vtyo)
- [func weakCompareExchange(expected: consuming Value, desired: consuming Value, successOrdering: AtomicUpdateOrdering, failureOrdering: AtomicLoadOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/weakcompareexchange(expected:desired:successordering:failureordering:)-9kx2t)
- [func weakCompareExchange(expected: consuming Value, desired: consuming Value, successOrdering: AtomicUpdateOrdering, failureOrdering: AtomicLoadOrdering) -> (exchanged: Bool, original: Value)](/documentation/synchronization/atomic/weakcompareexchange(expected:desired:successordering:failureordering:)-kfa8)
- [func wrappingAdd(UInt16, ordering: AtomicUpdateOrdering) -> (oldValue: UInt16, newValue: UInt16)](/documentation/synchronization/atomic/wrappingadd(_:ordering:)-1cynr)
- [func wrappingAdd(UInt64, ordering: AtomicUpdateOrdering) -> (oldValue: UInt64, newValue: UInt64)](/documentation/synchronization/atomic/wrappingadd(_:ordering:)-35sou)
- [func wrappingAdd(Int, ordering: AtomicUpdateOrdering) -> (oldValue: Int, newValue: Int)](/documentation/synchronization/atomic/wrappingadd(_:ordering:)-3ihte)
- [func wrappingAdd(Int128, ordering: AtomicUpdateOrdering) -> (oldValue: Int128, newValue: Int128)](/documentation/synchronization/atomic/wrappingadd(_:ordering:)-3ltc9)
- [func wrappingAdd(Int32, ordering: AtomicUpdateOrdering) -> (oldValue: Int32, newValue: Int32)](/documentation/synchronization/atomic/wrappingadd(_:ordering:)-4da1i)
- [func wrappingAdd(Int8, ordering: AtomicUpdateOrdering) -> (oldValue: Int8, newValue: Int8)](/documentation/synchronization/atomic/wrappingadd(_:ordering:)-7flp6)
- [func wrappingAdd(UInt128, ordering: AtomicUpdateOrdering) -> (oldValue: UInt128, newValue: UInt128)](/documentation/synchronization/atomic/wrappingadd(_:ordering:)-8rrye)
- [func wrappingAdd(Int16, ordering: AtomicUpdateOrdering) -> (oldValue: Int16, newValue: Int16)](/documentation/synchronization/atomic/wrappingadd(_:ordering:)-8wun9)
- [func wrappingAdd(UInt32, ordering: AtomicUpdateOrdering) -> (oldValue: UInt32, newValue: UInt32)](/documentation/synchronization/atomic/wrappingadd(_:ordering:)-9ce27)
- [func wrappingAdd(UInt, ordering: AtomicUpdateOrdering) -> (oldValue: UInt, newValue: UInt)](/documentation/synchronization/atomic/wrappingadd(_:ordering:)-bmso)
- [func wrappingAdd(Int64, ordering: AtomicUpdateOrdering) -> (oldValue: Int64, newValue: Int64)](/documentation/synchronization/atomic/wrappingadd(_:ordering:)-u8d5)
- [func wrappingAdd(UInt8, ordering: AtomicUpdateOrdering) -> (oldValue: UInt8, newValue: UInt8)](/documentation/synchronization/atomic/wrappingadd(_:ordering:)-ussb)
- [func wrappingSubtract(Int16, ordering: AtomicUpdateOrdering) -> (oldValue: Int16, newValue: Int16)](/documentation/synchronization/atomic/wrappingsubtract(_:ordering:)-1bgvk)
- [func wrappingSubtract(Int64, ordering: AtomicUpdateOrdering) -> (oldValue: Int64, newValue: Int64)](/documentation/synchronization/atomic/wrappingsubtract(_:ordering:)-3795w)
- [func wrappingSubtract(UInt128, ordering: AtomicUpdateOrdering) -> (oldValue: UInt128, newValue: UInt128)](/documentation/synchronization/atomic/wrappingsubtract(_:ordering:)-43111)
- [func wrappingSubtract(Int, ordering: AtomicUpdateOrdering) -> (oldValue: Int, newValue: Int)](/documentation/synchronization/atomic/wrappingsubtract(_:ordering:)-6g9gv)
- [func wrappingSubtract(Int8, ordering: AtomicUpdateOrdering) -> (oldValue: Int8, newValue: Int8)](/documentation/synchronization/atomic/wrappingsubtract(_:ordering:)-6xyiw)
- [func wrappingSubtract(UInt32, ordering: AtomicUpdateOrdering) -> (oldValue: UInt32, newValue: UInt32)](/documentation/synchronization/atomic/wrappingsubtract(_:ordering:)-6y8r7)
- [func wrappingSubtract(UInt, ordering: AtomicUpdateOrdering) -> (oldValue: UInt, newValue: UInt)](/documentation/synchronization/atomic/wrappingsubtract(_:ordering:)-7136k)
- [func wrappingSubtract(UInt64, ordering: AtomicUpdateOrdering) -> (oldValue: UInt64, newValue: UInt64)](/documentation/synchronization/atomic/wrappingsubtract(_:ordering:)-7203n)
- [func wrappingSubtract(Int128, ordering: AtomicUpdateOrdering) -> (oldValue: Int128, newValue: Int128)](/documentation/synchronization/atomic/wrappingsubtract(_:ordering:)-7k1nk)
- [func wrappingSubtract(UInt8, ordering: AtomicUpdateOrdering) -> (oldValue: UInt8, newValue: UInt8)](/documentation/synchronization/atomic/wrappingsubtract(_:ordering:)-83zzr)
- [func wrappingSubtract(UInt16, ordering: AtomicUpdateOrdering) -> (oldValue: UInt16, newValue: UInt16)](/documentation/synchronization/atomic/wrappingsubtract(_:ordering:)-8o6j2)
- [func wrappingSubtract(Int32, ordering: AtomicUpdateOrdering) -> (oldValue: Int32, newValue: Int32)](/documentation/synchronization/atomic/wrappingsubtract(_:ordering:)-8xrpg)
- [AtomicLazyReference](/documentation/synchronization/atomiclazyreference)

### Initializers

- [init()](/documentation/synchronization/atomiclazyreference/init())

### Instance Methods

- [func load() -> Instance?](/documentation/synchronization/atomiclazyreference/load())
- [func storeIfNil(consuming Instance) -> Instance](/documentation/synchronization/atomiclazyreference/storeifnil(_:))
- [WordPair](/documentation/synchronization/wordpair)

### Initializers

- [init(first: UInt, second: UInt)](/documentation/synchronization/wordpair/init(first:second:))

### Instance Properties

- [var first: UInt](/documentation/synchronization/wordpair/first)
- [var second: UInt](/documentation/synchronization/wordpair/second)

### Default Implementations

- [AtomicRepresentable Implementations](/documentation/synchronization/wordpair/atomicrepresentable-implementations)

#### Type Aliases

- [WordPair.AtomicRepresentation](/documentation/synchronization/wordpair/atomicrepresentation)

#### Type Methods

- [static func decodeAtomicRepresentation(consuming WordPair.AtomicRepresentation) -> WordPair](/documentation/synchronization/wordpair/decodeatomicrepresentation(_:))
- [static func encodeAtomicRepresentation(consuming WordPair) -> WordPair.AtomicRepresentation](/documentation/synchronization/wordpair/encodeatomicrepresentation(_:))
- [CustomDebugStringConvertible Implementations](/documentation/synchronization/wordpair/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/synchronization/wordpair/debugdescription)
- [CustomStringConvertible Implementations](/documentation/synchronization/wordpair/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/synchronization/wordpair/description)
- [Equatable Implementations](/documentation/synchronization/wordpair/equatable-implementations)

#### Operators

- [static func == (WordPair, WordPair) -> Bool](/documentation/synchronization/wordpair/==(_:_:))
- [Hashable Implementations](/documentation/synchronization/wordpair/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/synchronization/wordpair/hash(into:))
- [AtomicRepresentable](/documentation/synchronization/atomicrepresentable)

### Associated Types

- [AtomicRepresentation](/documentation/synchronization/atomicrepresentable/atomicrepresentation)

### Type Methods

- [static func decodeAtomicRepresentation(consuming Self.AtomicRepresentation) -> Self](/documentation/synchronization/atomicrepresentable/decodeatomicrepresentation(_:))
- [static func encodeAtomicRepresentation(consuming Self) -> Self.AtomicRepresentation](/documentation/synchronization/atomicrepresentable/encodeatomicrepresentation(_:))
- [AtomicOptionalRepresentable](/documentation/synchronization/atomicoptionalrepresentable)

### Associated Types

- [AtomicOptionalRepresentation](/documentation/synchronization/atomicoptionalrepresentable/atomicoptionalrepresentation)

### Type Methods

- [static func decodeAtomicOptionalRepresentation(consuming Self.AtomicOptionalRepresentation) -> Self?](/documentation/synchronization/atomicoptionalrepresentable/decodeatomicoptionalrepresentation(_:))
- [static func encodeAtomicOptionalRepresentation(consuming Self?) -> Self.AtomicOptionalRepresentation](/documentation/synchronization/atomicoptionalrepresentable/encodeatomicoptionalrepresentation(_:))

## Memory Ordering Semantics

- [AtomicLoadOrdering](/documentation/synchronization/atomicloadordering)

### Type Properties

- [static var acquiring: AtomicLoadOrdering](/documentation/synchronization/atomicloadordering/acquiring)
- [static var relaxed: AtomicLoadOrdering](/documentation/synchronization/atomicloadordering/relaxed)
- [static var sequentiallyConsistent: AtomicLoadOrdering](/documentation/synchronization/atomicloadordering/sequentiallyconsistent)
- [AtomicStoreOrdering](/documentation/synchronization/atomicstoreordering)

### Type Properties

- [static var relaxed: AtomicStoreOrdering](/documentation/synchronization/atomicstoreordering/relaxed)
- [static var releasing: AtomicStoreOrdering](/documentation/synchronization/atomicstoreordering/releasing)
- [static var sequentiallyConsistent: AtomicStoreOrdering](/documentation/synchronization/atomicstoreordering/sequentiallyconsistent)
- [AtomicUpdateOrdering](/documentation/synchronization/atomicupdateordering)

### Type Properties

- [static var acquiring: AtomicUpdateOrdering](/documentation/synchronization/atomicupdateordering/acquiring)
- [static var acquiringAndReleasing: AtomicUpdateOrdering](/documentation/synchronization/atomicupdateordering/acquiringandreleasing)
- [static var relaxed: AtomicUpdateOrdering](/documentation/synchronization/atomicupdateordering/relaxed)
- [static var releasing: AtomicUpdateOrdering](/documentation/synchronization/atomicupdateordering/releasing)
- [static var sequentiallyConsistent: AtomicUpdateOrdering](/documentation/synchronization/atomicupdateordering/sequentiallyconsistent)
- [func atomicMemoryFence(ordering: AtomicUpdateOrdering)](/documentation/synchronization/atomicmemoryfence(ordering:))

## Structures

- [Mutex](/documentation/synchronization/mutex)

### Initializers

- [init(consuming sending Value)](/documentation/synchronization/mutex/init(_:))

### Instance Methods

- [func withLock<Result, E>((inout sending Value) throws(E) -> sending Result) throws(E) -> sending Result](/documentation/synchronization/mutex/withlock(_:))
- [func withLockIfAvailable<Result, E>((inout sending Value) throws(E) -> sending Result) throws(E) -> sending Result?](/documentation/synchronization/mutex/withlockifavailable(_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
