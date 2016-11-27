---
layout: post
date: 2016-11-27
title: Combining colors
published: true
permalink: combining-colors
---

# Combining colors

This is from a blog post from [We heart Swift](https://www.weheartswift.com/combining-colors/?utm_campaign=This%2BWeek%2Bin%2BSwift&utm_medium=web&utm_source=This_Week_in_Swift_110). It's about combining two `UIColor`objects with a lerping function: `(1 - α) * A + α * B` and it can be put in an extension on `UIColor` itself

```swift
extension UIColor {
	var rgba: (red: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat) {
		guard let components = self.cgColor.components else {
			return (red: 0, green: 0, blue: 0, alpha: 0)
		}

		return (red: components[0], green: components[1], blue: components[2], alpha: components[3])
	}

	func combine(with color: UIColor, amount: CGFloat) -> UIColor {
		func lerp(from a: CGFloat, to b: CGFloat, alpha: CGFloat) -> CGFloat {
			return (1 - alpha) * a + alpha * b
		}

		let fromComponents = self.rgba
		let toComponents = color.rgba

		let redAmount = lerp(from: fromComponents.red, to: toComponents.red, alpha: amount)
		let greenAmount = lerp(from: fromComponents.green, to: toComponents.green, alpha: amount)
		let blueAmount = lerp(from: fromComponents.blue, to: toComponents.blue, alpha: amount)

		return UIColor(red: redAmount, green: greenAmount, blue: blueAmount, alpha: 1)
	}
}

let combined = UIColor.red.combine(with: .blue, amount: 0.5)
```

Via [We heart Swift](https://www.weheartswift.com/combining-colors/?utm_campaign=This%2BWeek%2Bin%2BSwift&utm_medium=web&utm_source=This_Week_in_Swift_110).