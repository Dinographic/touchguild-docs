---
description: >-
  The 'Message' component is a 'GuildMessage' component as for now. This can
  change in the future by moving some data into an extension of 'Message'.
---

# ⌨ Message

### Properties

| Property           | Description                                                                    | Type                                                   |
| ------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------ |
| data               | Original message data.                                                         | Object                                                 |
| fulldata           | Full original data including message data                                      | Object                                                 |
| client             | the client that receives the channel data                                      | <mark style="color:purple;"></mark>[Client](client.md) |
| id                 | id of the message                                                              | String                                                 |
| type               | type of message ('user' or 'system')                                           | String                                                 |
| channel            | channel where the message has been sent                                        | [Channel](channel.md)                                  |
| member             | message author                                                                 | Member  ----- to LINK                                  |
| guildID            | id of the message's server                                                     | String                                                 |
| channelID          | id of the message's channel                                                    | String                                                 |
| content            | message content                                                                | String                                                 |
| embeds             | message's embed(s)                                                             | Array\<Object>                                         |
| isPrivate          | is message private? true/false                                                 | Boolean                                                |
| isSilent           | if the message doesn't notify a user                                           | Boolean                                                |
| mentions           | Message mentions object                                                        | Object                                                 |
| createdAt          | timestamp that the message was created at                                      | String                                                 |
| createdBy          | id of the message author                                                       | String                                                 |
| updatedAt          | timestamp that the message was updated at                                      | String                                                 |
| createdByWebhookID | The ID of the webhook who created this message, if it was created by a webhook | String                                                 |
| oldContent         | old message content if edited                                                  | String                                                 |

## Constructor

```javascript
new Message(rawData, client, params)
```

| Properties        | Description                                     | Type                | Required? |
| ----------------- | ----------------------------------------------- | ------------------- | --------- |
| rawData           | raw data received from ws and converted to JSON | Object              | true      |
| client            | Client                                          | [Client](client.md) | true      |
| params            | Object of params                                | Object              | true      |
| params.oldContent | old message content, can be undefined           | String              | true      |

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

> Returns: <mark style="color:blue;">Promise</mark><<mark style="color:purple;">Message</mark>>

### edit(options)

Update/edit the message.

| Properties      | Description      | Type   | Required? |
| --------------- | ---------------- | ------ | --------- |
| options         | edit options     | Object | true      |
| options.content | message content  | String | false     |
| options.embeds  | message's embeds | Object | false     |

### delete()

Delete the message.
