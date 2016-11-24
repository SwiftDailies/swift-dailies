---
layout: post
date: 2016-11-24
title: Localized String constants
published: true
permalink: /localized-string-constants/
---

# Localized String constants

Another possibility for providing `String` constants is via an extension on the `String` type itself. This way it is even possible to automatically use the correct localized version of the string. 

```swift
extension String {
	private static func localized(key: String) -> String {
		return NSLocalizedString(key, comment: "")
	}

	static var cancel = "Cancel"
	static var save = String.localized(key: "save")
}

let cancel: String = .cancel
let save: String = .save
```

Via [Swifting](https://swifting.io/blog/2016/11/20/27-localize-your-strings-swiftly/?utm_campaign=This%2BWeek%2Bin%2BSwift&utm_medium=email&utm_source=This_Week_in_Swift_111).