---
description: Our vision, perspective about the TouchGuild library.
---

# 👀 Our vision

## This page is an archive and features legacy versions of TouchGuild. Any information coming from it is outdated.

##

## A library built by you, for you.

### Pull requests

We wanted to make a library where every bot developers collaborate to the project. By choosing the community, you, we're making what you like the most.

[Get started by making pull requests.](https://github.com/DinographicPixels/TouchGuild/pulls)

### Feature requests & bug report

If you know you won't collaborate to your library, you can still request features, they're helpful and they're representative of what the community would like to get.

You can also report bugs, they can be very important. By reporting you're enabling everyone to get back features that doesn't work anymore, or just issues with properties.

[You can create issues here. (issues includes feature requests & bugs, and even more).](https://github.com/DinographicPixels/TouchGuild/issues)

## TouchGuild Library Branding

### We introduce you the TouchGuild icons

<figure><img src="../.gitbook/assets/touchguild-icon.png" alt="TouchGuild Icon (mini)"><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/touchguild-fullicon.png" alt="TouchGuild full icon, made to be pleasant to look at."><figcaption></figcaption></figure>

## Innovation works when secrets are revealed.

### How the library works, how it treats Guilded API calls?

The library is receiving Guilded API calls through a WebSocket (WSManager.ts), this WebSocket is invoked when you use the 'connect()' method from [Client](../documentation/select-version/v.0.1.6/components/client.md). The Guilded API messages which are 'packets' and are converted to JSON then sent and received in the [Client](../documentation/select-version/v.0.1.6/components/client.md), the message is filtered and redirected to a message handler that treats and emit the component.

Every components are constructors, they delivers you the necessary methods, properties, and even cached properties, that helps you to be more productive.

We note that the library is licensed under[ Apache-2.0 license](https://github.com/DinographicPixels/TouchGuild/blob/main/LICENSE) .
