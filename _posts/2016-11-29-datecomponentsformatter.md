---
layout: post
date: 2016-11-29
title: DateComponentsFormatter
published: false
permalink: /datecomponentsformatter/
---

# DateComponentsFormatter
The `DateComponentsFormatter` class, which was introduced with iOS 8 and macOS 10.10, gives you string representations of `DateComponents`. It can even prefix the result string with a time-remaining-phrase so that you can easily show the time until a specific date.

```swift
let components = DateComponents(calendar: .current,
                                year: 2016, 
                                month: 12, 
                                day:24)
let xmas = components.date!
let interval = xmas - Date()
let formatter = DateComponentsFormatter()
formatter.unitsStyle = .full
formatter.includesTimeRemainingPhrase = true
formatter.allowedUnits = [.day, .weekOfMonth]
let string = formatter.string(from: interval)
```

The great advantage of this technique is, that the resulting string automatically gets formatted with the right locale.