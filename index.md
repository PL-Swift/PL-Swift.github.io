---
layout: default
title: PL/Swift - PostgreSQL Functions in Swift
tags: postgresql swift server side
---

<p>
  <img src="https://img.shields.io/badge/postgresql-10-yellow.svg" />
  <img src="https://img.shields.io/badge/swift-3-blue.svg" />
  <img src="https://img.shields.io/badge/swift-4-blue.svg" />
  <img src="https://img.shields.io/badge/os-macOS-green.svg?style=flat" />
  <img src="https://img.shields.io/badge/os-tuxOS-green.svg?style=flat" />
</p>

PL/Swift
allows you to write custom SQL functions and types for the 
[PostgreSQL](https://www.postgresql.org/)
database server in the 
[Swift](http://swift.org/) programming language.

It does what?
Assume you have a Swift function which turns an integer into a
[base36](https://en.wikipedia.org/wiki/Base36)
encoded String:

```swift
func base36_encode(_ v: Int) -> String {
  return String(v, radix: 36)
}
```

PL/Swift documentation can be found here:
[pl-swift.github.io/docs/](https://pl-swift.github.io/docs/).
