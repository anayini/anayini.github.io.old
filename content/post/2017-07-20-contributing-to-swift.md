---
title: My First Contribution to Swift
date: 2017-07-20
tags: ["swift", "oss", "ios", "programming"]
---

My first contribution to the Swift programming language was [merged](https://github.com/apple/swift/pull/8354) earlier this year.
Despite the simplicity of the bug I fixed, the process took awhile and I learned a good deal in the process.  This post will briefly go over the fix I made and some give some advice for future contributors.

After deciding to contribute I browsed the [Swift Jira](https://bugs.swift.org) to find
a suitable beginner bug.  The first thing I did was filter for issues within the Standard Library
and the Swift Package Manager.  As someone completely new to a daunting codebase, it seemed
best to start somewhere  where I could mostly just write code in Swift.  My goal in looking
through the bugs was to find the easiest possible thing to fix.  I used two general filters my search:

+ The fix would require small, additive changes
+ The fix was tightly related to one specific type.

I ended up landing on [this](https://bugs.swift.org/browse/SR-4172).  The bug was fairly straightforward
make `() == ()` compile.  This fulfilled my filters: I needed to make a small, additive change (add an `==` method)
and the fix was tightly related to one specific type (`Tuple`).
