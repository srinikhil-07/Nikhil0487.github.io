---
title: NSURLCredentialStorage For Authentication
layout: post
categories: apple framework
---

My experiments with NSURLCredentialStorage for handling authentication in Apple platforms.

Forming a NSURLCredentialStorage object:

1. Form a SecIdentity (for client certificate authentication),
2. Form a NSURLCredential object with your identity,
3. Form a NSURLProtectionSpace object, which is basically assigning the credential you created to a host,
4. Create a NSURLCredentialStorage object where you can set a shared credential object with your identity and NSURLProtectionSpace.

You can refer [this] StackOverflow link for example code of the above steps. One of the answers mentioned client certificate authentication won't work with NSURLCredentialStorage. But I wanted to check this myself. So I turned on CFNetwork debug logging, setup the NSURLCredentialStorage for my request and started looking into the console logs.

CFNetwork logging can be turned on for your app by calling below funtion

{% highlight swift %}
setenv("CFNETWORK_DIAGNOSTICS", "3", 1)
{% endhighlight %}

but do read about the security implications mentioned by [Apple].

Turns out, my network request was getting an authentication challenge in TLS layer, but the CFNetwork log printed NULL in response to the authentication challenge. I made sure my NSURLCredentialStorage had SecIdentity for my host but despite that the authentication challenge was always replied with NULL. 

So, NSURLCredentialStorage should be working only for Basic authentication as the above linked SO thread says. And this leaves us with only delegates as the means for handling complex authentication mechanism. 

You can find me on [Twitter].

[this]: https://stackoverflow.com/questions/4164846/nsurlcredentialstorage-and-client-certificate-authentication
[Apple]: https://developer.apple.com/documentation/network/debugging_https_problems_with_cfnetwork_diagnostic_logging
[Twitter]: https://twitter.com/nikhil38036647