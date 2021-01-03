---
title: Learning SwiftUI
layout: post
categories: swiftui
---

So, I started learning SwiftUI from the official SwiftUI essential tutorial. SwiftUI is interesting and
the answering the following questions effectively summarises the tutorial.

1. What are stacks? What are the different types of Stacks?
2. Define the behavior of spacer, padding, formatters, offsets?
3. What are @State, @Observable, @EnvironmentalObject and @Publish properties? 
And how do they interact with each other?

And the tutorial teaches various UI elements in an interesting way and it's all very good until
you relaize that you are a passive learner and not an active one. So, this led me to an interesting idea to actually try apply the principles introduced in a simple way.

For my first ever iOS app using UIKit, I've used NewsAPI and why not use the same here?

So after some thinking, I came with the below simple idea mapping various tutorial parts to NewsAPI.
Translating Landmark app components to News headlines app components, we can form the below mapping


1. Landmark Lists: Display list of your country's top headlines returned by the API,
2. Landmark Categories: Display categories of NewsAPI top headline (there are about 6 of them),
3. Landmark Featured: Feature top headlines randomised (and after some usage in phone intelligense basde on apps usage) to pick most relevant News item,
4. Tab view to switch between points 1 and 2,
5. User profile: Editable view with relevant fields,
6. Animation: Start forming animations based on users news reading patterns.

Further steps:
1. Integrating with UIKit,
2. Creating a macOS app.

I wish to implement above and open source it on GitHub.


[official]: https://developer.apple.com/tutorials/swiftui
[first]: https://github.com/Nikhil0487/NewsApp
[NewsAPI]: https://newsapi.org