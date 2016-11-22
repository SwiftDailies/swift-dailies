---
layout: post
date: 2016-11-22
title: Using hex values with Ints
published: true
permalink: /using-hex-values-with-ints/
---

# Using hex values with Ints

An `Int` can be initialized with a hexadecimal value, which is useful for storing color information.

```swift
static let White: Int = 0xFFFFFF
static let Black = 0x000000
static let fancyBlue = 0x00A4F8
```

This can be used with an extension on UIColor as described in [Initialize `UIColor` with a hex value](https://swiftdailies.github.io/initialize-uicolor-with-a-hex-value/).