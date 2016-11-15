---
layout: post
date: 2016-11-16
title: Initialize UIColor with a hex value
published: false
permalink: /initialize-uicolor-with-a-hex-value/
--- 

# Initialize UIColor with a hex value

Sometimes it's useful to initialize an `UIColor` object with a hexadecimal `Int` value.

```swift
`extension UIColor 
convenience init(hex: Int, alpha: CGFloat = 1.0) 
let red = CGFloat((hex & 0xFF0000) \>\> 16