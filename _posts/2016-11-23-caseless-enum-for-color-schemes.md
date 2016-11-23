---
layout: post
date: 2016-11-23
title: Caseless enum for color schemes
published: false
permalink: /caseless-enum-for-color-schemes/
---

# Caseless enum for color schemes

In Swift, *Enums* don't need to have case values but can still have static properties. This makes a great use case for storing constant values, since the enum can't be instantiated. For example with a color scheme, and an extension on `UIColor`, as described [here](https://swiftdailies.github.io/initialize-uicolor-with-a-hex-value/).

```swift
enum ColorScheme {
	static let darkText = UIColor(hex: 0x1A1A1A)
	static let lightText = UIColor(hex: 0x545454)

	static let darkGray = UIColor(hex: 0xDAE0E6)
	static let lightGray = UIColor(hex: 0xEEEEEE)
}
```

You can even nest Enums to provide better namespacing.