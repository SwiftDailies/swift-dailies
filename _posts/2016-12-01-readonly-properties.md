---
layout: post
date: 2016-12-01
title: Readonly properties
published: true
permalink: /readonly-properties/
---

# Readonly properties

You can define a variable property as *external* read-only with `private(set)`. This way, a property is visible on the outside but only editable from within the struct (or class / enum).

```swift
struct Phone {
    private(set) var battery: Float = 1.0
    
    mutating func decreaseBattery() {
        battery -= 0.01
    }
}

var phone = Phone()
phone.decreaseBattery()
print(phone.battery)
phone.battery = 1.0 /// Compiler error
```