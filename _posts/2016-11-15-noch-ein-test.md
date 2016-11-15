---
layout: post
date: 2016-11-14
title: Test
published: true
number: 4
---

# Test

Initialize a random Int via `Int(2...10)` or `Int(2..<10)`.

```swift
`extension Int 
init(_ range: ClosedRange\<Int\>) 
self = Int(arc4random_uniform(UInt32(range.upperBound + 1)