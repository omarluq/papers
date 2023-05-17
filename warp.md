![Alt Text](https://assets-global.website-files.com/6427349e1bf2f0f378f73094/6427349e1bf2f05182f73359_Little_big_update%25403x-p-1600.png)
# Warp: The terminal for the 21st century, is it worth the hype?
If you keep up with the latest tools for software development, you have probably heard of or seen Warp. But in case you haven't, let's start by explaining what [Warp](https://www.warp.dev/) is.

The team behind Warp describes it as a blazingly fast, fully native rust-based terminal reimagined from the ground up to work like a modern app.

![Alt Text](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExYTkzMTNmM2Q2MzlkZDJlMmQ4NzY5OGNhNTA2N2JmMDdjMDM0YmE0NiZlcD12MV9pbnRlcm5hbF9naWZzX2dpZklkJmN0PWc/YbS3KkZSFGUkB4XO1X/giphy.gif)


While we can't fully explore the architecture behind Warp since it uses a proprietary rust-based native UI framework (the development team will eventually open-source the project based on their roadmap), here is what's made open for the public to know:
* The app uses [warp](https://github.com/seanmonstar/warp), a [hyper](https://hyper.rs/) based web server framework. Talking about hyper and the warp server framework deserves a paper of its own, but here are my 2 cents: hyper has been battle-tested for almost 10 years now, and it has some of the most impressive benchmark results for an HTTP client. It handles requests faster than some really popular tools such as tiny-http. The development team behind it is getting ready to release the stable version after 10 years of testing and development.
* The development team describes the UI framework used to build the Warp app as a fully native rust-based framework that doesn't depend on web technology to render the application. This means that you should expect the Warp terminal to be light on the CPU and RAM. This is important because in today's age, developers usually run multiple web-based desktop apps at the same time, such as VSCode, Docker Desktop, Slack, Discord, just to name a few. And these apps heavily utilize both the CPU and RAM, so the last thing you want is to introduce another Electron-based app to the fold.

#### Now let's dive into some of Warp's unique features that separate it from other terminals:
* ***Input Editor***: Warp offers inline text editor-like features. Unlike other command-line tools that offer minimal editing capabilities, you can use all types of modern editing shortcuts and commands within Warp. Think things like multi-line selecting, quick copy-paste, custom keybinds, etc.
* ***Command Search***: Warp ships with a powerful GPT-3 powered AI search, a language model that converts natural language into shell commands.
* ***Blocks***: Warp provides a modular and modern UI that groups an input and an output together. This allows you to navigate your terminal command by command without scrolling and easily perform actions like copy and share via a powerful context menu.
* ***Workflows***: Warp comes with a powerful workflow engine to optimize your day-to-day productivity. I like to think of Warp's workflows as aliases on steroids. You can package all types of command sequences into a single executable, document it, and access it via a GUI. For those with a team license, you can share your workflows with everyone in your organization.
* ***Custom themes***: Software engineers love to take full ownership of their work environment! From workflows to aliases to custom scripts, we always try to add our own unique flavor to our environment. Warp allows you to choose a fitting theme for your environment from a collection of pre-installed themes. But it doesn't stop there; you can also create your own theme in a simple YAML format or visit https://warp-themes.com/, a community-powered project to create and download custom themes.
#### I might sound like I'm just feeding the Warp hype train here, but the fact is I've been using Warp for both my personal and work Mac for the past 2 years, and I don't think I can go back to a normal terminal. However, there are a few issues with Warp that can hold you from jumping on the Warp hype train! We will look into those next.
* If you haven't guessed yet, Warp is currently available on macOS only. This is due to the fact that until recently, macOS was the only operating system that allowed Rust to be used for low-level kernel programming. However, last year, Linux added support for Rust with their 6.1 release. Just recently, in March of this year, David Weston, the Director of OS Security for Windows, announced the arrival of Rust in the Windows kernel. In recent news, some teams at Microsoft have already started rewriting some core Windows C/C++ libraries in Rust. This means that the arrival of Warp into Windows and Linux, in Thanos' words, is inevitable.

   ![Alt Text](https://media.giphy.com/media/ie76dJeem4xBDcf83e/giphy.gif)

* Warp won't work as your embedded IDE terminal. Nowadays, most engineers find themselves utilizing the embedded terminal with their editor of choice. While you can improve those terminals by using advanced shells such as oh-my-zsh or oh-my-fish, Warp is a native desktop app that won't integrate as your embedded terminal. Although that feature has been on the dev team roadmap for the past 2 years or more, it is probably not coming anytime soon due to the engineering difficulties that such a task holds. However, it's fair to mention that not all hope is lost yet. In theory, it is possible to integrate Warp into modern lightweight editors such as VSCode as an extension by using TypeScript and WebAssembly.

* Warp doesn't play nice with interactive shells*. It shouldn't come as a surprise, but Warp doesn't support all types of shells yet. While it supports your standard bash, zsh, or fish shell out of the box, you will lose most of the features we talked about if you decide to load an interactive shell* inside of Warp, even after you exit the interactive shell.
 
## Conclusion
![Alt Text](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNWUxMzhhNmViZWMzZmU0ZThmZDNhZTUwZWQ4MjM1NjZjNTU5Y2E2OSZlcD12MV9pbnRlcm5hbF9naWZzX2dpZklkJmN0PWc/U4nN1cilNUuosbdVya/giphy.gif)

While it is true that Warp comes light-years ahead of any other terminal out there, I still find myself drifting back to using the embedded terminal every now and then because it's right there in front of me while I'm coding, especially when I want to work with interactive shells. However, Warp is my daily driver for any other terminal need I have. The team behind the project is very impressive and ambitious, and they keep shipping awesome features year after year.

There are many more features in Warp that I use daily, and I would recommend visiting Warp's website at www.warp.dev to read about all the awesome features or even check them out on GitHub @warpdotdev if you want to learn more about the roadmap ahead and even contribute if you have the time.

In the end I would recommand giving Warp a try! you don't know it might change they way you work for years to come. 
 
 
![Alt Text](https://media.giphy.com/media/dsKnRuALlWsZG/giphy.gif)
 
__________________________________________________________________
<sub><sup> &copy; All Rights Reserved. This paper and its contents, excluding the images used, are the property of the author(s) and are protected by copyright laws. No part of this paper may be reproduced, distributed, or transmitted in any form or by any means, including photocopying, recording, or other electronic or mechanical methods, without the prior written permission of the author(s), except in the case of brief quotations embodied in critical reviews and certain other noncommercial uses permitted by copyright law. For permission requests regarding the images used, please refer to the appropriate copyright holder or source as indicated.</sup></sub>