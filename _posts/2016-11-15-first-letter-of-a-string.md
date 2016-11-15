---
layout: post
date: 2016-11-15
title: First letter of a string
published: true
permalink: /first-letter-of-a-string/
---

# Get the first letter of a string

This snippet will give you the first letter of a string.

~~ ```swift
extension String {
	var firstLetter: String {
		guard self != "" else {
			return ""
		}
		return String(self[self.startIndex])
	}	
}
~~ ```

This is empty for an empty string.

```swift
let stringOne = "string"
let stringTwo = ""
let stringThree = "🙂"
print(stringOne.firstLetter)
print(stringTwo.firstLetter)
print(stringThree.firstLetter)
```

```swift
>> s
>> 
>> 🙂
```