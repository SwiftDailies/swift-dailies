---
layout: post
date: 2016-12-07
title: Random Bool
published: true
permalink: /random-bool/
---

# Random Bool
This extension produces `true` or `false` on a random basis. Perfect for throwing a coin.

```swift
import Foundation

extension Bool {
	static var random: Bool {
		return arc4random_uniform(10000) < arc4random_uniform(10000)
	}
}
```