---
layout: post
date: 2016-11-25
title: Using the nil-coalescing operator
published: true
permalink: /using-the-nil-coalescing-operator/
---

# Using the nil-coalescing operator

The nil-coalescing operator `??` lets you provide a default value while trying to unwrap an optional. You use it like this:

```swift
let colors: [UIColor] = []
let red = colors.first ?? .red
print(red)
```

This often eliminates the need for `if let` or `guard` statement.