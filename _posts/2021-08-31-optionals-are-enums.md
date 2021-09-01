---
title: "TIL: Optionals Are Enums!"
layout: post
---

![Very funny meme, Tobi](https://bitesizedswift.com/assets/uploads/optionals.png)

I did find this out the other day: Optionals are just enums in Swift. It makes total sense in hindsight, but I never gave it a second thought when _actually_ writing Swift:

```swift
public enum Optional<Wrapped> : ExpressibleByNilLiteral {
    case none
    case some(Wrapped)
}
```

Aren't [associated values](https://docs.swift.org/swift-book/LanguageGuide/Enumerations.html#Associated%20Values) the best?