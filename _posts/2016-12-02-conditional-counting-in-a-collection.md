---
layout: post
date: 2016-12-02
title: Conditional counting in a collection
published: true
permalink: /conditional-counting-in-a-collection/
---

# Conditional counting in a collection

If you ever find yourself needing to count the items in a collection based on a certain condition, this extension will be useful.

```swift
extension Collection {
    func count(where condition: (Iterator.Element) -> Bool) -> Int {
        var result = 0
        for element in self where condition(element) {
            result += 1
        }
        return result
    }
}
```

With the trailing closure syntax, this can be used really concisely.

```swift
let a = [0, 1, 1, 2, 3, 5, 8]
let c = a.count { $0 > 2 }
print(c) /// 3

```