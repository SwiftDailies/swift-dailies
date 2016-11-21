---
layout: post
date: 2016-11-20
title: Adding Floats to Ints without hassle
published: true
permalink: /adding-floats-to-ints-without-hassle/
--- 

# Adding Floats to Ints without hassle

This extension lets you add `Float`, `Double` and `CGFloat` to an `Int` without the need to cast them beforehand.

```swift
extension Int {
	static func +(lhs: Int, rhs: Float) -> Float {
		return Float(lhs) + rhs
	}
	static func +(lhs: Int, rhs: Double) -> Double {
		return Double(lhs) + rhs
	}
	static func +(lhs: Int, rhs: CGFloat) -> CGFloat {
		return CGFloat(lhs) + rhs
	}
}
```