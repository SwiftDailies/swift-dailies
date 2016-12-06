---
layout: post
date: 2016-12-05
title: Switch on tuples
published: true
permalink: /switch-on-tuples/
---

# Switch on tuples
You can perform a `switch` operation on a tuple and match different patterns to your needs. You can even assign the tuple values to new variables.

```swift
switch (indexPath.section, indexPath.row) {
	case (1...3, 1):
		/// Do something special
	case let (section, row):
		/// Do something special with section and row	
	case let (1, row):
		/// Do something special with row in section 1
	default: break
}
```