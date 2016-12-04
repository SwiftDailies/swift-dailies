---
layout: post
date: 2016-12-04
title: first(where:)
published: true
permalink: /first(where:)/
---

# first(where:)

You can use the `first` function on arrays with a `where` parameter to specify a condition. The first item that matches the condition gets returned.

```swift
var a = [1, 2, 4, 8, 16, 32]

/// Conditional `where` closure
let b = a.first(where: { (int) -> Bool in
    return int > 4
})

/// Short trailing closure syntax
let c = a.first { $0 > 4 }
```