---
layout: post
date: 2016-11-21
title: Init DateFormatter with format
published: true
permalink: /init-dateformatter-with-format/
---

# Init DateFormatter with format

Initialize a DateFormatter directly with a format string.

```
extension DateFormatter {
	convenience init(with format: String) {
		self.init()
		self.dateFormat = format
	}
}
```

Use it like this.

```
let format = "YYYY-MM-dd"
let formatter = DateFormatter(with: format)
let dateString = formatter.string(from: Date()