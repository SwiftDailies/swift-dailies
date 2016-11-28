---
layout: post
date: 2016-11-30
title: Subtracting dates
published: false
permalink: /subtracting-dates/
---

# Subtracting dates

A small extension on `Date` to overload the minus operator for easy time interval calculation.

```swift
extension Date {
    static func -(lhs: Date, rhs: Date) -> TimeInterval {
        return lhs.timeIntervalSince(rhs)
    }
}
```