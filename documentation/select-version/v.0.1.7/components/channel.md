---
description: >-
  The 'Channel' component is a 'GuildChannel' component as for now. This can
  change in the future by moving some data into an extension of 'Channel'.
---

# ☕ Channel

## Properties

| Property     | Description                                                                              | Type                                                   |
| ------------ | ---------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| data         | Original channel data.                                                                   | Object                                                 |
| client       | the client that receives the channel data                                                | <mark style="color:purple;"></mark>[Client](client.md) |
| id           | id of the channel                                                                        | String                                                 |
| type         | type of the channel                                                                      | String                                                 |
| name         | the name of the channel                                                                  | String                                                 |
| topic        | the topic/description of the channel                                                     | String                                                 |
| \_createdAt  | timestamp that the channel was created at                                                | Number                                                 |
| memberID     | id of the user that created the channel                                                  | String                                                 |
| \_updatedAt  | timestamp that the channel was updated at                                                | Number\|null                                           |
| guildID      | the id of the server                                                                     | String                                                 |
| parentID     | ID of the parent channel or parent thread, if present. Only relevant for server channels | String                                                 |
| categoryID   | id of the category the channel is in                                                     | String                                                 |
| groupID      | id of the group the channel is in                                                        | String                                                 |
| isPublic     | is the channel public?                                                                   | Boolean                                                |
| archivedBy   | id of the user that archived the channel                                                 | String                                                 |
| \_archivedAt | timestamp that the channel was archived at                                               | Number                                                 |
| createdAt    | string representation of the \_createdAt timestamp.                                      | Date                                                   |
| updatedAt    | string representation of the \_updatedAt timestamp.                                      | Date\|null                                             |
| archivedAt   | string representation of the \_archivedAt timestamp.                                     | Date\|null                                             |

## Constructor

```javascript
new Channel(rawData, client)
```

| Properties | Description                                     | Type                                         | Required? |
| ---------- | ----------------------------------------------- | -------------------------------------------- | --------- |
| rawData    | raw data received from ws and converted to JSON | Object                                       | true      |
| client     | Client                                          | [Client](client.md) | true      |

{% hint style="danger" %}
Do not use this constructor unless you know what you're doing. This constructor is used to return you rawdata into component.
{% endhint %}

## Methods

### createMessage(options)

Create a message in the channel.

| Properties              | Description                                                | Type           | Required? |
| ----------------------- | ---------------------------------------------------------- | -------------- | --------- |
| options                 | message's options                                          | Object         | true      |
| options.content         | message content                                            | String         | false     |
| options.embeds          | message's embeds                                           | Array\<Object> | false     |
| options.replyMessageIds | list of message id to reply                                | Array\<String> | false     |
| options.isSilent        | notify user(s)?                                            | Boolean        | false     |
| options.isPrivate       | message will only be seen by those mentioned or replied to | Boolean        | false     |

> Returns: <mark style="color:blue;">Promise</mark><[<mark style="color:purple;">Message</mark>](message.md)>

### edit(options)

Update the channel.

| Properties       | Description                    | Type    | Required? |
| ---------------- | ------------------------------ | ------- | --------- |
| options          | edit options                   | Object  | false     |
| options.name     | new channel name               | String  | false     |
| options.topic    | new channel topic/description. | String  | false     |
| options.isPublic | is the channel public?         | Boolean | false     |

> Returns: <mark style="color:purple;"><mark style="color:blue;">Promise<mark style="color:blue;"></mark><mark style="color:purple;"><</mark>[<mark style="color:purple;">Channel</mark>](channel.md)<mark style="color:purple;">></mark>

### delete()

Delete the channel.

> Returns: <mark style="color:purple;">Promise\<void></mark>
