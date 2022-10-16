# 🤖 New Client methods

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

### disconnect(crashOnDisconnect?)

Disconnect the client from the Guilded API.

| Properties         | Description                                                                                                         | Type    |
| ------------------ | ------------------------------------------------------------------------------------------------------------------- | ------- |
| crashOnDisconnect? | <p>If true, it'll crash when executing the method. If false, it'll only log the action. </p><p>(default: false)</p> | Boolean |

### awardMember(guildID, memberID, xpAmount)

Awards a member using the built-in EXP system.

| Properties | Description                                               | Type   |
| ---------- | --------------------------------------------------------- | ------ |
| guildID    | the guild/server id                                       | String |
| memberID   | the guild member id                                       | String |
| xpAmount   | the amount of xp you'd like to give the specified member. | Number |

### setMemberXP(guildID, memberID, xpAmount)

Sets a member's xp using the built-in EXP system.

| Properties | Description                                | Type   |
| ---------- | ------------------------------------------ | ------ |
| guildID    | the guild/server id                        | String |
| memberID   | the guild member id                        | String |
| xpAmount   | the new amount of xp the member will have. | Number |

### awardRole(guildID, roleID, xpAmount)

Awards all members having a role using the built-in EXP system.

| Properties | Description                                                                 | Type   |
| ---------- | --------------------------------------------------------------------------- | ------ |
| guildID    | the guild/server id                                                         | String |
| roleID     | the role id                                                                 | Number |
| xpAmount   | the amount of xp you'd like to give to everybody having the specified role. | Number |
