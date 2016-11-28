---
layout: post
date: 2016-11-28
title: Order of functions in unit testing
published: true
permalink: /order-of-functions-in-unit-testing/
---

# Order of functions in unit testing

In a `XCTestCase`, every method starting with `test` gets called in an alphabetical order. So if you want to have them called in a specific order, you need to prefix them with a letter, which looks awkward, or a number.

```swift
func test1_FunctionName() {
	/// Gets called first.
}

func test2_AnotherFunctionName() {
	/// Gets called after the above function.
}
```