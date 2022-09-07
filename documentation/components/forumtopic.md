---
description: Component coming from a 'Forum' channel.
---

# 📆 ForumTopic

## Properties

| Property         | Description                                                                | Type         |
| ---------------- | -------------------------------------------------------------------------- | ------------ |
| \_client         | Client                                                                     | Client       |
| id               | Forum topic id                                                             | Number       |
| guildID          | Guild/server id                                                            | String       |
| channelID        | Forum channel id                                                           | String       |
| name             | Topic name/title                                                           | String       |
| title            | Topic name/title                                                           | String       |
| \_createdAt      | Timestamp (unix epoch time) of the topic's creation.                       | Number       |
| memberID         | ID of the member who created the topic                                     | String       |
| webhookID        | ID of the webhook that created the topic (if created by webhook)           | String       |
| \_updatedAt      | Timestamp (unix epoch time) of when the topic got updated. (if updated)    | Number\|null |
| bumpedAt         | Timestamp (unix epoch time) that the forum topic was bumped at.            | String       |
| content          | Content of the topic                                                       | String       |
| mentions         | Topic mentions                                                             | Object       |
| guild            | Guild/server the topic is in                                               | Guild        |
| member           | Member who created the topic                                               | Member       |
| channel          | The forum channel, where the topic is in                                   | Channel      |
| createdAt        | string representation of the \_createdAt timestamp                         | Date         |
| updatedAt        | string representation of the \_updatedAt timestamp                         | Date\|null   |
| createdByWebhook | Boolean that tells you if the forum topic was created by a webhook or not. | Boolean      |

## Constructor

```javascript
new ForumTopic(rawData, client)
```

| Properties | Description                                     | Type                | Required? |
| ---------- | ----------------------------------------------- | ------------------- | --------- |
| rawData    | raw data received from ws and converted to JSON | Object              | true      |
| client     | Client                                          | [Client](client.md) | true      |

{% hint style="danger" %}
Do not use this constructor unless you know what you're doing. This constructor is used to return you rawdata into component.
{% endhint %}

## Methods

### edit(options)

Edit the forum topic.

| Properties       | Description           | Type   | Required? |
| ---------------- | --------------------- | ------ | --------- |
| options          | Edit options          | Object | true      |
| options.title?   | New topic title/name. | String | false     |
| options.content? | New topic content.    | String | false     |

> Returns: <mark style="color:purple;">Promise<</mark>[<mark style="color:purple;">CalendarEventRSVP</mark>](calendareventrsvp.md)<mark style="color:purple;">></mark>

### delete()

Delete the forum topic.

> Returns: <mark style="color:purple;">Promise\<void></mark>

### pin()

Pin the forum topic.

> Returns: <mark style="color:purple;">Promise\<void></mark>

### unpin()

Unpin the forum topic.

> Returns: <mark style="color:purple;">Promise\<void></mark>
