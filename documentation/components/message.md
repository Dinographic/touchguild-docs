---
description: >-
  The 'Message' component is a 'GuildMessage' component as for now. This can
  change in the future by moving some data into an extension of 'Message'.
---

# ⌨ Message

## Properties

| Property              | Description                                                                                                         | Type                                                   |
| --------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| \_data                | Original message data.                                                                                              | Object                                                 |
| \_client              | the client that receives the channel data                                                                           | <mark style="color:purple;"></mark>[Client](client.md) |
| id                    | id of the message                                                                                                   | String                                                 |
| type                  | type of message ('user' or 'system')                                                                                | String                                                 |
| channel               | channel where the message has been sent                                                                             | [Channel](channel.md)                                  |
| member                | message author                                                                                                      | Member  ----- to LINK                                  |
| guildID               | id of the message's server                                                                                          | String                                                 |
| channelID             | id of the message's channel                                                                                         | String                                                 |
| content               | message content                                                                                                     | String                                                 |
| embeds                | message's embed(s)                                                                                                  | Array\<Object>                                         |
| isPrivate             | is message private? true/false                                                                                      | Boolean                                                |
| isSilent              | if the message doesn't notify a user                                                                                | Boolean                                                |
| mentions              | Message mentions object                                                                                             | Object                                                 |
| \_createdAt           | timestamp that the message was created at                                                                           | Number                                                 |
| memberID              | id of the message author                                                                                            | String                                                 |
| \_updatedAt           | timestamp that the message was updated at                                                                           | Number\|null                                           |
| \_deletedAt           | Timestamp (unix epoch time) of the message's deletion.                                                              | Number\|null                                           |
| webhookID             | The ID of the webhook who created this message, if it was created by a webhook                                      | String                                                 |
| replyMessageIds       | List of ids mentioned in the message                                                                                | Array                                                  |
| \_lastMessageID       | last message sent with the message itself (cache)                                                                   | String                                                 |
| \_originalMessageID   | Original message, used to reply this one (cache)                                                                    | String                                                 |
| \_originalMessageBool | Used by the system to detect if the original message id has been transfered                                         | Boolean                                                |
|                       |                                                                                                                     |                                                        |
| oldContent            | old message content if edited                                                                                       | String                                                 |
| createdAt             | string representation of the \_createdAt timestamp.                                                                 | Date                                                   |
| updatedAt             | string representation of the \_updatedAt timestamp.                                                                 | Date\|void                                             |
| deletedAt             | string representation of the \_deletedAt timestamp.                                                                 | Date\|void                                             |
| member                | Get the member component, which returns Member when message guildID and memberID is defined or if Member is cached. | Member\|undefined                                      |
| guild                 | Guild component where the message has been sent                                                                     | Guild                                                  |
| channel               | Channel component where the message has been sent on                                                                | [Channel](channel.md)                                  |

## Constructor

```javascript
new Message(rawData, client, params)
```

| Properties                | Description                                         | Type                  | Required? |
| ------------------------- | --------------------------------------------------- | --------------------- | --------- |
| rawData                   | raw data received from ws and converted to JSON     | Object                | true      |
| client                    | Client                                              | [Client](client.md)   | true      |
| params?                   | Object of params                                    | Object                | false     |
| params.oldMessage?        | old message component, if cached.                   | [Message](message.md) | false     |
| params.originalMessageID? | ID of the transfered original message. If existant. | String                | false     |

{% hint style="danger" %}
Do not use this constructor unless you know what you're doing. This constructor is used to return you rawdata into component.
{% endhint %}

## Methods

### createMessage(options)

Create a message in the message's channel.

| Properties              | Description                                                | Type           | Required? |
| ----------------------- | ---------------------------------------------------------- | -------------- | --------- |
| options                 | message's options                                          | Object         | true      |
| options.content         | message content                                            | String         | false     |
| options.embeds          | message's embeds                                           | Array\<Object> | false     |
| options.replyMessageIds | list of message id to reply                                | Array\<String> | false     |
| options.isSilent        | notify user(s)?                                            | Boolean        | false     |
| options.isPrivate       | message will only be seen by those mentioned or replied to | Boolean        | false     |

> Returns: <mark style="color:blue;">Promise</mark><[<mark style="color:purple;">Message</mark>](message.md)>

### edit(newMessage)

Update/edit the message.

| Properties         | Description      | Type   | Required? |
| ------------------ | ---------------- | ------ | --------- |
| newMessage         | edit options     | Object | true      |
| newMessage.content | message content  | String | false     |
| newMessage.embeds  | message's embeds | Object | false     |

> Returns: <mark style="color:purple;">Promise<</mark>[<mark style="color:purple;">Message</mark>](message.md)<mark style="color:purple;">></mark>

### delete()

Delete the message.

> Returns: <mark style="color:purple;">Promise\<void></mark>

### editLastMessage(newMessage)

Edit the last message sent with the message itself.

| Properties         | Description      | Type   | Required? |
| ------------------ | ---------------- | ------ | --------- |
| newMessage         | edit options     | Object | true      |
| newMessage.content | message content  | String | false     |
| newMessage.embeds  | message's embeds | Object | false     |

> Returns: <mark style="color:purple;">Promise<</mark>[<mark style="color:purple;">Message</mark>](message.md)<mark style="color:purple;">></mark>

### deleteLastMessage()

Delete the last message sent with he message itself.

> Returns: <mark style="color:purple;">Promise\<boolean></mark>

### editOriginalMessage(newMessage)

Edit the message's original message, if existant.

| Properties         | Description      | Type   | Required? |
| ------------------ | ---------------- | ------ | --------- |
| newMessage         | edit options     | Object | true      |
| newMessage.content | message content  | String | false     |
| newMessage.embeds  | message's embeds | Object | false     |

> Returns: <mark style="color:purple;">Promise<</mark>[<mark style="color:purple;">Message</mark>](message.md)<mark style="color:purple;">></mark>

### deleteOriginalMessage()

Delete the message's original message, if existant.

> Returns: <mark style="color:purple;">Promise\<boolean></mark>

### addReaction(reaction)

Add a reaction to the message.

| Properties | Description | Type   | Required? |
| ---------- | ----------- | ------ | --------- |
| reaction   | reaction id | Number | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### removeReaction(reaction)

Remove a specific reaction from the message.

| Properties | Description | Type   | Required? |
| ---------- | ----------- | ------ | --------- |
| reaction   | reaction id | Number | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>
