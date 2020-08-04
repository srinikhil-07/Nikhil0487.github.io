---
title: My First Swift Pitch
layout: post
categories: swift-5
---

There has been some gap now.

I have been doing some interesting things lately and one of them is pitching 
for a feature in Swift language. 

I was soving an algorithmic [challenge] in Swift and I wrote the following code piece.

{% highlight swift %}
var itr = 0
visited = Array.init(repeating: false, count: n+1)
for nodes in graph { //graph is an 2D array
    adjList.updateValue(nodes, forKey: itr)
    itr = itr+1
}
{% endhighlight %}

Each `nodes` in above example is an 1D array and to append them to a dictionary
with index as key, I had to use a seperate index variable `itr`.

In Swift we have 2 `types` of for-in loop: one iterating over sequences and 
the other over ranges. So, I had this idea of why not combine both in the 
same for-in loop statement and make for-in loop more `powerful` as one user put it in the
[forum] post.

So, this is the [forum]. Have a look. The great thing about this pitch (and Swift pitches in general) 
is that different users actually looked into the pitch and come out with alternatives, suggestions, discussions, pros, cons.

Although my pitch was termed additive and difficult to be accepted. It was a good experience. I would 
definitely do more pitches if I strongly feel the need in future.

The following are some of the new things I learnt about Swift from my pitch

1. Beware of the wordings and the code snippet style while pitching your idea,
2. [enumerated] - this is interesting but it can't fully solve the need for the pitch,
3. [zip] - this is actually very close to what the pitch tries, but one limiting factor is
that range and sequence iteration should have same count,
4. And others suggestions are more known like map etc.,

I also have this strong feeling that Swift will eventually add `power` to for-in loop
with a more elegant pitch, but I may be wrong.

[forum]: https://forums.swift.org/t/for-in-loop-combining-sequence-and-range/38745/15
[challenge]: https://github.com/Nikhil0487/Algorithmic-Problems-Swift/blob/master/July-2020/all_paths.swift
[enumerated]: https://developer.apple.com/documentation/swift/array/1687832-enumerated
[zip]: https://developer.apple.com/documentation/swift/1541125-zip