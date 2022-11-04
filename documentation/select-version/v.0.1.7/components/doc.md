---
description: Doc is component coming from a 'docs' channel.
---

# 📄 Doc

## Properties

| Property    | Description                                                           | Type                                                                                            |
| ----------- | --------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| data        | Raw data                                                              | Object                                                                                          |
| client      | Client                                                                | [Client](../../v.0.1.7/components/client.md)                                                    |
| id          | ID of the doc                                                         | Number                                                                                          |
| guildID     | Guild/server id                                                       | String                                                                                          |
| channelID   | ID of the 'docs' channel.                                             | String                                                                                          |
| title       | Doc title/name                                                        | String                                                                                          |
| name        | Doc title/name                                                        | String                                                                                          |
| content     | Content of the doc                                                    | String                                                                                          |
| mentions    | Doc mentions                                                          | Object ([<mark style="color:purple;">MentionsType</mark>](../../v.0.1.7/types/mentionstype.md)) |
| \_createdAt | Timestamp (unix epoch time) of the doc's creation.                    | Number\|null                                                                                    |
| memberID    | ID of the member who created the doc.                                 | String                                                                                          |
| \_updatedAt | Timestamp (unix epoch time) of when the doc was updated. (if updated) | Number\|null                                                                                    |
| updatedBy   | ID of the member who updated the doc. (if updated)                    | String                                                                                          |
| member      | Member that made emit the event.                                      | [Member](../../v.0.1.7/components/member.md)                                                    |
| createdAt   | String representation of the \_createdAt timestamp.                   | Date\|null                                                                                      |
| updatedAt   | String representation of the \_updatedAt timestamp.                   | Date\|null                                                                                      |

## Constructor

```javascript
new Doc(rawData, client)
```

| Properties | Description                                     | Type                                         | Required? |
| ---------- | ----------------------------------------------- | -------------------------------------------- | --------- |
| rawData    | raw data received from ws and converted to JSON | Object                                       | true      |
| client     | Client                                          | [Client](../../v.0.1.7/components/client.md) | true      |

{% hint style="danger" %}
Do not use this constructor unless you know what you're doing. This constructor is used to return you rawdata into component.
{% endhint %}

## Methods

### edit(options)

Edit the doc.

| Properties       | Description     | Type   | Required? |
| ---------------- | --------------- | ------ | --------- |
| options          | Edit options    | Object | true      |
| options.title?   | New doc title   | String | false     |
| options.content? | New doc content | String | false     |

> Returns: <mark style="color:purple;">Promise<</mark>[<mark style="color:purple;">Doc</mark>](../../v.0.1.7/components/doc.md)<mark style="color:purple;">></mark>

### delete()

Delete the doc.

> Returns: <mark style="color:purple;">Promise\<void></mark>
