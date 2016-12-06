---
layout: post
date: 2016-12-06
title: Case matching on optionals
published: true
permalink: /case-matching-on-optionals/
---

# Case matching on optionals
If you try to `switch` on an optional you will fail when matching against an already unwrapped value. This extension will match the value anyway and fail if it’s `nil`.

```swift
func ~=<T: Equatable>(pattern: T?, value: T?) -> Bool {
return pattern == value
}
```