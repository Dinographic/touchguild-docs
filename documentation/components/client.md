---
description: >-
  The Guilded Bot's client, where everything's happen and where the Guilded bot
  interacts with guilds/servers.
---

# Client

### Properties

| Property    | Description                                                                   | Type      |
| ----------- | ----------------------------------------------------------------------------- | --------- |
| params      | The bot's options you set when you're creating a new client. (includes token) | Object    |
| identifiers | Names of all standard Guilded events and their equivalent in simple stypes.   | Object    |
| ws          | The WebSocket manager used to connect to the API.                             | WSManager |
| cache       | The client's cache, used for storing things such as message contents          | Map       |
| token       | The bot's inserted token.                                                     | String    |

## Constructor

```javascript
new Client(params)
```

| Properties   | Description                  | Type   | Required? |
| ------------ | ---------------------------- | ------ | --------- |
| params       | Client's parameters/options. | Object | true      |
| params.token | Bot's token                  | String | true      |

## Methods

{% hint style="info" %}
Client have standard event emitter types, they're not listed there.
{% endhint %}

### connect()

Connects your bot to the Guilded API.

### getChannel(channelID)

Get a specific channel's information.

| Properties | Description                          | Type   |
| ---------- | ------------------------------------ | ------ |
| channelID  | id of the channel you'd like to get. | String |

> Returns: <mark style="color:purple;">Channel</mark>



### getMember(guildID, memberID)

Get a specific guild's/server's member.

| Properties | Description      | Type   |
| ---------- | ---------------- | ------ |
| guildID    | id of the server | String |
| memberID   | id of the user   | String |

> Returns: <mark style="color:purple;">Member</mark>

### getGuild(guildID)

Get a specific guild/server.

| Properties | Description      | Type   |
| ---------- | ---------------- | ------ |
| guildID    | id of the server | String |

> Returns: <mark style="color:purple;">Guild</mark>

### createChannel(location, name, type, options)

Create a channel within given location.

| Properties          | Description                          | Type    | Required? |
| ------------------- | ------------------------------------ | ------- | --------- |
| location            | new channel's location               | Object  | true      |
| location.guildID    | id of the server                     | String  | false     |
| location.groupID    | id of the group                      | String  | false     |
| location.categoryID | id of the category                   | String  | false     |
| name                | new channel's name                   | String  | true      |
| type                | new channel's type (example: 'chat') | String  | true      |
| options             | new channel's options                | Object  | false     |
| options.topic       | new channel's topic, description.    | String  | false     |
| options.isPublic    | --                                   | Boolean | false     |

> Returns: <mark style="color:purple;">Channel</mark>

### createMessage(channelID, options)

Create a message in a specific channel.

| Properties              | Description                                                | Type           | Required? |
| ----------------------- | ---------------------------------------------------------- | -------------- | --------- |
| channelID               | channel's id                                               | String         | true      |
| options                 | message's options                                          | Object         | true      |
| options.content         | message content                                            | String         | false     |
| options.embeds          | message's embeds                                           | Array\<Object> | false     |
| options.replyMessageIds | list of message id to reply                                | Array\<String> | false     |
| options.isSilent        | notify user(s)?                                            | Boolean        | false     |
| options.isPrivate       | message will only be seen by those mentioned or replied to | Boolean        | false     |

> Returns: <mark style="color:blue;">Promise</mark><<mark style="color:purple;">Message</mark>>

### editMessage(channelID, messageID, newMessage)

Update a specific message.

| Properties         | Description           | Type           | Required? |
| ------------------ | --------------------- | -------------- | --------- |
| channelID          | channel's id          | String         | true      |
| messageID          | target message id     | String         | true      |
| newMessage         | new message's options | Object         | true      |
| newMessage.content | new message content   | String         | false     |
| newMessage.embeds  | new message's embeds  | Array\<Object> | false     |

### deleteMessage(channelID, messageID)

Delete a specific message.

| Properties | Description       | Type   | Required? |
| ---------- | ----------------- | ------ | --------- |
| channelID  | channel's id      | String | true      |
| messageID  | target message id | String | true      |
