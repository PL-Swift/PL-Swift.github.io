---
layout: default
title: PL/Swift - PostgreSQL Functions in Swift
tags: postgresql swift server side
---

<p>
  <img src="https://img.shields.io/badge/postgresql-10-yellow.svg" />
  <img src="https://img.shields.io/badge/swift-3-blue.svg" />
  <img src="https://img.shields.io/badge/swift-4-blue.svg" />
  <img src="https://img.shields.io/badge/swift-5-blue.svg" />
  <img src="https://img.shields.io/badge/os-macOS-green.svg?style=flat" />
  <img src="https://img.shields.io/badge/os-tuxOS-green.svg?style=flat" />
</p>

**PL/Swift**
allows you to write custom SQL functions and types for the 
[PostgreSQL](https://www.postgresql.org/)
database server in the 
[Swift](http://swift.org/) programming language.

*It does what?*
Assume you have a Swift function which turns an integer into a
[base36](https://en.wikipedia.org/wiki/Base36)
encoded String,
to replicate the trick used by URL shorteners
("`goo.gl/QvohfE`"):

```swift
func base36_encode(_ v: Int) -> String {
  return String(v, radix: 36)
}
```

and now you would like to use that in a SQL query, like so:

```sql
helge=# SELECT base36_encode(31337);
 base36_encode 
---------------
 o6h
(1 row)
```

This is what PL/Swift does. It helps you expose your Swift functions to
PostgreSQL.

*Does this make sense?*
Very likely not, it depends, as usual. But no. It doesn't.
Consider this a neat demo, not something you should do in the real world.

Another useful example?

```swift
import cows

func plcows_vaca() -> String {
  return cows.vaca() // returns a random ASCII cow
}
```

```sql
helge=# SELECT plcows_vaca();
        plcows_vaca         
----------------------------
              ((----))     +
              ((oooo))     +
       ///-----\\\///      +
     ///|||    |||         +
   *** ||||||---|||        +
       ^^^^^^    ^^^       +
 where milkshakes come from
(1 row)
```

### Documentation

PL/Swift documentation can be found here:
[pl-swift.github.io/docs/](https://pl-swift.github.io/docs/).

A small tutorial can be found over here:
[PL/Swift - PostgreSQL Functions in Swift](http://www.alwaysrightinstitute.com/plswift/).
