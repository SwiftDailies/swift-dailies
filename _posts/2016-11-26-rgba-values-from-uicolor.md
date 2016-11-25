---
layout: post
date: 2016-11-26
title: RGBA values from UIColor
published: true
permalink: /rgba-values-from-uicolor/
---

# RGBA values from UIColor

Another extension on `UIColor` to easily get the *red*, *green*, *blue* and *alpha* values.

```swift
extension UIColor {
	var rgba: (red: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat) {
		guard let components = self.cgColor.components else {
			return (red: 0, green: 0, blue: 0, alpha: 0)
		}

		return (red: components[0], green: components[1], blue: components[2], alpha: components[3])
	}
}

let red = UIColor(red: 0.2, green: 0.3, blue: 0.4, alpha: 0.7)
dump(red.rgba.blue)
```