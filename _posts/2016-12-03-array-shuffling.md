---
layout: post
date: 2016-12-03
title: Array shuffling
published: true
permalink: /array-shuffling/
---

# Array shuffling
Another short extension on `Array` which shuffles the items via a simple random sort algorithm. By comparing two random integers a random sort order is applied to the array. The `shuffled()` function is the non-mutating counterpart, which gives you a new array and leaves the old one in its previous order.

```
extension Array {
    mutating func shuffle() {
		for _ in 0..<self.count {
			self.sort() { _ in
				return arc4random_uniform(10000) < arc4random_uniform(10000)
			}
		}
	}
    
    func shuffled() -> [Element] {
        var copy = self
        copy.shuffle()
        return copy
    }
}
```