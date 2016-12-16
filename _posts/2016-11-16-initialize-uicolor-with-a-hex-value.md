---
layout: post
date: 2016-11-16
title: Initialize UIColor with a hex value
published: true
permalink: /initialize-uicolor-with-a-hex-value/
--- 

# Initialize UIColor with a hex value

Sometimes it's useful to initialize an `UIColor` object with a hexadecimal `Int` value.

```swift
extension UIColor {
	convenience init(hex: Int, alpha: CGFloat = 1.0) {
		let red = CGFloat((hex & 0xFF0000) >> 16) / 255.0
		let green = CGFloat((hex & 0xFF00) >> 8) / 255.0
		let blue = CGFloat((hex & 0xFF)) / 255.0

		self.init(red:red, green:green, blue:blue, alpha:alpha)
	}
}
```

Use it like this:

```swift
let fancyBlue = UIColor(hex: 0x00A4F8)
````