---
layout: post
date: 2016-11-14
title: Print with file and function name
permalink: /print-with-file-and-function-name/
published: true
---

# Print with file and function name

You can print console messages with a custom global log function capturing the file and function name.

```swift
func log(message: String = "", file: String = #file, line: Int = #line, function: String = #function) {
    var logString = ""

    if let encoded = file.addingPercentEncoding(withAllowedCharacters: .urlHostAllowed), let url = NSURL(string: encoded), let lastPathComponent = url.lastPathComponent {
        logString += "\(lastPathComponent)"
    } else {
        logString += "\(file)"
    }

    logString += ":\(line) - \(function)"

    if message != "" {
        logString += "\n>>> \(message)"
    }

    print(logString)
}
```

When called with no parameters from the app delegate, this will print out:

```
`AppDelegate.swift:48 - application(_:didFinishLaunchingWithOptions:)
````