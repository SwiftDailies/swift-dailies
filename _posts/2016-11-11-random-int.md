---
layout: post
date: 2016-11-11
title: Random Int
published: true
number: 1
---

# Random Int

Initialize a random Int via `Int(2...10)` or `Int(2..<10)`.

```
extension Int \{
'' init(_ range: ClosedRange<Int>) {
''     self = Int(arc4random_uniform(UInt32(range.upperBound + 1)) + UInt32(range.lowerBound))
'' }
'' init(_ range: Range<Int>) {
''     self = Int(arc4random_uniform(UInt32(range.upperBound) + UInt32(range.lowerBound)))
'' }
}
```