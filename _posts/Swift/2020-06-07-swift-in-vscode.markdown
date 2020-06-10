---
title: Using Swift with VS Code
layout: post
categories: swift-5
---

Recently I started experimenting a lot with Swift on macOS and Linux.

I have successfully configured Swift in VSCode on both macOS and Linux.
Below are the steps that I followed for macOS:

1. Install VSCode if you haven't and follow [Matt's] steps,
2. After step 1, try creating a new Swift file and start writing Swift code,
3. Most probably you would be getting Swift language server crashes,
4. For this to fix, first run the command 'xcrun --find sourcekit-lsp'. Note it seems 
sourcekit-lsp is packed in Xcode from 11.4 and upwards only,
5. Copy the output of step 4 to VSCode->Preferences->Settings->Extensions->Sourcekit-LSP->Server path
6. Reload VSCode and Swift auto-completion will now work flawlessly.

Will write another article on setting up Swift with VSCode on Linux. 

You can find me on [Twitter].

Notes:
1. Ray Wenderlich has an excellent [introduction] of how Language-Server-Protocol works in their
article on Swift in Linux,
2. Apple's sourcekit repository is [here]

[Matt's]:  https://nshipster.com/vscode/
[introduction]: https://www.raywenderlich.com/8325890-a-complete-guide-to-swift-development-on-linux
[here]: https://github.com/apple/sourcekit-lsp
[Twitter]: https://twitter.com/nikhil38036647