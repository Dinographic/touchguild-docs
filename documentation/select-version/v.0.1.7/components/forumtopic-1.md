---
description: Component assigned to a ForumTopic, similar to Message.
---

# 📃 ForumTopicComment

## Properties

| Property   | Description                                                                                                                                                                                                                         | Type                                         |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------- |
| \_client   | Client                                                                                                                                                                                                                              | [Client](../../v.0.1.7/components/client.md) |
| id         | The ID of the forum topic comment                                                                                                                                                                                                   | Number                                       |
| content    | The content of the forum topic comment                                                                                                                                                                                              | String                                       |
| createdAt  | The ISO 8601 timestamp that the forum topic comment was created at                                                                                                                                                                  | String                                       |
| updatedAt? | The ISO 8601 timestamp that the forum topic comment was updated at, if relevant                                                                                                                                                     | String                                       |
| topicID    | The ID of the forum topic                                                                                                                                                                                                           | Number                                       |
| createdBy  | The ID of the user who created this forum topic comment (Note: If this event has createdByWebhookId present, this field will still be populated, but can be ignored. In this case, the value of this field will always be Ann6LewA) | String                                       |
| guildID    | ID of the forum topic's server, if somehow provided.                                                                                                                                                                                | String                                       |
| channelID  | ID of the forum channel, if somehow provided.                                                                                                                                                                                       | String                                       |

## Constructor

```javascript
new ForumTopicComment(rawData, client, options?)
```

| Properties          | Description                                               | Type                                         | Required? |
| ------------------- | --------------------------------------------------------- | -------------------------------------------- | --------- |
| rawData             | raw data received from ws and converted to JSON           | Object                                       | true      |
| client              | Client                                                    | [Client](../../v.0.1.7/components/client.md) | true      |
| options?            | additional information we can give to a ForumTopicComment | Object                                       | false     |
| options?.guildID?   | id of the comment's server, not provided by Guilded       | String \| null                               | false     |
| options?.channelID? | id of the comment's channel, not provided by Guilded      | String \| null                               | false     |

{% hint style="danger" %}
Do not use this constructor unless you know what you're doing. This constructor is used to return you rawdata into component.
{% endhint %}

## Methods

### createTopicComment(channelID, options)

Add a comment to the same forum topic as this comment.

| Properties      | Description                                                                         | Type   | Required? |
| --------------- | ----------------------------------------------------------------------------------- | ------ | --------- |
| channelID       | id of the forum channel (needed since Guilded does not provide us this information) | String | true      |
| options         | create options                                                                      | Object | true      |
| options.content | content of the comment                                                              | String | true      |

> Returns: <mark style="color:purple;">Promise<</mark>[<mark style="color:purple;">ForumTopicComment</mark>](forumtopic-1.md)<mark style="color:purple;">></mark>

### edit(channelID, options?)

Edit this forum topic's comment.

| Properties      | Description                                                                         | Type   | Required? |
| --------------- | ----------------------------------------------------------------------------------- | ------ | --------- |
| channelID       | id of the forum channel (needed since Guilded does not provide us this information) | String | true      |
| options?        | create options                                                                      | Object | false     |
| options.content | content of the comment                                                              | String | false     |

> Returns: <mark style="color:purple;">Promise<</mark>[<mark style="color:purple;">ForumTopicComment</mark>](forumtopic-1.md)<mark style="color:purple;">></mark>

### delete(channelID)

Delete this forum topic comment.

| Properties | Description                                                                         | Type   | Required? |
| ---------- | ----------------------------------------------------------------------------------- | ------ | --------- |
| channelID  | id of the forum channel (needed since Guilded does not provide us this information) | String | true      |

Returns: <mark style="color:purple;">Promise\<void></mark>
