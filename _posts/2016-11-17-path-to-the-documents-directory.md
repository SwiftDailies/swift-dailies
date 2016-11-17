# Path to the documents directory

This extension to `UIApplication` will give you the path to the *documents directory* as an `String` or `URL`.

```
extension UIApplication {
	var documentsDirectory: String {
		return NSSearchPathForDirectoriesInDomains(.DocumentDirectory, .UserDomainMask, true).first ?? ""
	}
	var documentsDirectoty: NSURL {
		return NSURL(string: self.documentsDirectory) ?? NSURL()
	}
}
```