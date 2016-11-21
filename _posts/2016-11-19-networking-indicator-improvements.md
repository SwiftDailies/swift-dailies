---
layout: post
date: 2016-11-19
title: Networking indicator improvements
published: true
permalink: /networking-indicator-improvements/
--- 

# Networking indicator improvements

This class can be used to consistently update the networking indicator multiple times. It keeps track of how many times the networking indicator was shown, which is useful for dismissing it while making multiple network requests.

```
class NetworkIndicator: NSObject {
	private static var count = 0 {
		didSet {
			count = max(count, 0)
		}
	}

	static func setVisible() {
		NetworkIndicator.set(visible: true)
	}

	static func setHidden() {
		NetworkIndicator.set(visible: false)
	}

	private static func set(visible isVisible: Bool) {
		count += isVisible ? 1 : -1
		UIApplication.shared.isNetworkActivityIndicatorVisible = (count > 0)
	}
}
```