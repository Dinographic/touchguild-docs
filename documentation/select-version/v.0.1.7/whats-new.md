---
description: Check out what's new.
---

# What's new?

## New

* **Added** [Lock & unlock forum topic features.](https://github.com/DinographicPixels/TouchGuild/pull/7)
* **All in one** type file, **reorganized types** (does not affect user experience)
* [Guild XP #14](https://github.com/DinographicPixels/TouchGuild/pull/14): Managing Guild Member's XP, including set/award.
* [Adding DevTools to the TouchGuild's index.](https://github.com/DinographicPixels/TouchGuild/pull/15)
* [Added Client.user & Updated WebSocket.](https://github.com/DinographicPixels/TouchGuild/pull/18)
* **Major change:** Integrated API Types into TouchGuild. (affects the whole library, makes the user-experience even better when using Non-REST methods)
* **Added** 'Invalid token' error.
* **Added** TouchGuild's http header
* **Made** scripts better with ESLint.
* **Added** `pkgconfig.ts`, this file provides every information about your current TouchGuild version.
* **Added** `ForumTopicComment` component, this component provides three methods: createTopicComment, edit & delete.
* **Added** a new Client method: `createTopicComment`
* **Added** a new Client method: `editTopicComment`
* **Added** a new Client method: `deleteTopicComment`
* **Added** a new Client method: `getRESTTopicComment`
* **Added** a new Client method: `getRESTTopicComments`
* **Added** a new Client method: `getTopicComments`
* **Added** a new Client method: `addTopicReaction`
* **Added** a new Client method: `removeTopicReaction`
* **Added** a new ForumTopic method: `addReaction`
* **Added** a new ForumTopic method: `removeReaction`
* **Added** a new gateway event: `guildCreate` (fired when bot joins a guild)
* **Added** a new gateway event: `forumTopicCommentCreate`
* **Added** a new gateway event: `forumTopicCommentUpdate`
* **Added** a new gateway event: `forumTopicCommentDelete`
* **Added** a new gateway event: `forumTopicReactionAdd`
* **Added** a new gateway event: `forumTopicReactionRemove`
* **Added** `GuildCreateInfo` types for the `guildCreate` event.
* Cache now **supports** ForumTopic & stores those components when needed.
* Now, every requests uses API Typings, it makes the library more accurate.
* **Added** the following exports: `ForumTopicComment` and `APITypes`

## Updated

* **Fixed**: [messageDelete event: cannot get message.content after deletion. #10](https://github.com/DinographicPixels/TouchGuild/issues/10)
* **Improved**: [Dev to Nightly: Improved web socket. #13](https://github.com/DinographicPixels/TouchGuild/pull/13)
* **Removed** unused imports (does not affect user experience)
* **Fixed**: [Issue while importing TouchGuild on repl.it or other services. (import error) #12](https://github.com/DinographicPixels/TouchGuild/issues/12)
* **Fixed** [ForumTopic.edit() does not work.](https://github.com/DinographicPixels/TouchGuild/issues/26)
* **Fixed** some component typings.
* **Fixed** `replayMissedEvents` not working.
* **Removed** `Types.ts`, replaced by `lib/tg-types/types.ts`
* **Updated** `target` from `ES6` to `ES2022`
* **Reduced** dependencies from 16 to 7!
* **Fixed** circular imports issues caused by Utils (calls).
* **Deleted** `UserClientInfo` (types), replaced by `UserClient` (component).
* **Updated** DevTools, supports retry when server response equals 429.
* **Fixed** `WSManagerParams` typings.
* **Deleted** reactionInfo, **replaced** by **messageReactionInfo** and **forumTopicReactionInfo**
* **Updated** endpoints & **fixed** typos.
* **Updated** identifiers by adding the new gateway events.
