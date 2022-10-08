---
description: Frequently asked questions.
---

# 😅 FAQ

<details>

<summary>Why is TouchGuild in early access?</summary>

TouchGuild is deploying slowly, we tested every methods, events.. but we're sure there is hidden bugs. It's up to you to tell us the bugs, as you use the library!

[If you find a bug, make sure to report it by clicking here.](https://github.com/DinographicPixels/TouchGuild/issues)

When we'll see that the library is stable, we'll switch to a 'B.E.T.A' branch since the Guilded API is still in early access.

</details>

<details>

<summary>How to collaborate to the library's development?</summary>

You can make [pull requests](https://github.com/DinographicPixels/TouchGuild/pulls) through our [GitHub repository](https://github.com/DinographicPixels/TouchGuild/pulls). We're enabling everyone to collaborate to your library, because it is yours.

[You don't know how pull requests works? Click here.](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository)

</details>

<details>

<summary>"I don't get why I should use TouchGuild over guilded.js"</summary>

#### TouchGuild has a different approach about how you use a library.

While creating TouchGuild, we thought about how it should be used & how to make the library durable & even if deprecation happen.

We built TouchGuild to be durable, if deprecation happens you can still use it by importing 'calls' and send requests to the Guilded API, we also made proper methods to use less ram & get data that directly comes from the API itself. (those methods are called Non-REST methods)

We also built our cache to be simple but useful. The TouchGuild's cache stores message components when sent, so you can get information about them when you'd like, and even more. You can also get the whole cache by using 'Client.cache'.

We're making interfacing with the API accessible, and easier. Everything's related to this is gonna be managed by us. You have to build everything on your own, except the communcation layer between you & Guilded.

</details>

More frequently asked questions coming soon, as they're asked, haha!
