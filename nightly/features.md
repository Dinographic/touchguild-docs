---
description: New features included on Nightly builds.
---

# 🎯 Features

## Client methods

### lockTopic(channelID, topicID)

You're now able to use the lockTopic method to lock topics, haha ofc.

| Properties | Description           | Type   |
| ---------- | --------------------- | ------ |
| channelID  | id of the channel     | String |
| topicID    | id of the forum topic | Number |

### unlockTopic(channelID, topicID)

You can also unlock a specific topic with the unlockTopic method.

| Properties | Description           | Type   |
| ---------- | --------------------- | ------ |
| channelID  | id of the channel     | String |
| topicID    | id of the forum topic | Number |

## ForumTopic methods

### Use the lock() and unlock() methods.

You can lock & unlock the topic with its component.

```javascript
ForumTopic.lock();
ForumTopic.unlock();
// Note that 'ForumTopic' is an example of a 
// forum topic component variable
```
