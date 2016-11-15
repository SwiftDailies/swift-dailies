---
layout: post
title: Safe array indexing
date: 2016-11-12
published: true
permalink: /safe-array-indexing/
number: 2
---

# Safe array indexing

Returns `nil` if the index exceeds  the array’s bounds.

```swift
extension Array {
	subscript (safe index: Int)  Element? {
		return index < count ? self[index] : nil
	}
}
```

Via [Erica Sadun](http://ericasadun.com/2015/06/01/swift-safe-array-indexing-my-favorite-thing-of-the-new-week/).