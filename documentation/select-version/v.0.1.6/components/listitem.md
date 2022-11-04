---
description: ListItem is a 'list channel' component. It has his own properties and methods.
---

# ↗ ListItem

## Properties

| Property         | Description                                                                                             | Type                                                                                 |
| ---------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| \_data           | raw data                                                                                                | Object                                                                               |
| \_client         | client                                                                                                  | [Client](client.md)                                                                  |
| id               | item id                                                                                                 | String                                                                               |
| guildID          | id of the guild                                                                                         | String                                                                               |
| channelID        | id of the list channel                                                                                  | String                                                                               |
| content          | content of the item                                                                                     | String                                                                               |
| mentions         | mentions contained in the item                                                                          | Object ([<mark style="color:purple;">MentionsType</mark>](../types/mentionstype.md)) |
| \_createdAt      | timestamp of item's creation                                                                            | Number                                                                               |
| memberID         | id of the member who created the item                                                                   | String                                                                               |
| webhookID        | id of the webhook who created/updated the item.                                                         | String                                                                               |
| \_updatedAt      | timestamp of when the item got updated                                                                  | Number                                                                               |
| updatedBy        | id of the member that updated the item, if updated.                                                     | String                                                                               |
| parentListItemID | The ID of the parent list item if this list item is nested                                              | String                                                                               |
| \_completedAt    | timestamp of the item's completion                                                                      | Number                                                                               |
| completedBy      | set to completed by'?'                                                                                  | String                                                                               |
| note             | note object provided by guilded, with all the note information.                                         | Object                                                                               |
| member           | Member component of the the owner of the item or the user who updated the item (depends on the action). | [Member](member.md)\|void                                                            |
| createdAt        | string representation of the \_createdAt timestamp.                                                     | Date                                                                                 |
| updatedAt        | string representation of the \_updatedAt timestamp.                                                     | Date                                                                                 |
| completedAt      | string representation of the \_completedAt timestamp.                                                   | Date                                                                                 |

## Constructor

```javascript
new ListItem(rawData, client)
```

| Properties | Description                                     | Type                | Required? |
| ---------- | ----------------------------------------------- | ------------------- | --------- |
| rawData    | raw data received from ws and converted to JSON | Object              | true      |
| client     | Client                                          | [Client](client.md) | true      |

{% hint style="danger" %}
Do not use this constructor unless you know what you're doing. This constructor is used to return you rawdata into component.
{% endhint %}

## Methods

### edit(content, note?)

Edit the list item.

| Properties    | Description              | Type   | Required? |
| ------------- | ------------------------ | ------ | --------- |
| content       | New content of the item. | String | true      |
| note?         | Item's additional note   | Object | false     |
| note?.content | note's content           | String | true      |

> Returns: <mark style="color:purple;">Promise<</mark>[<mark style="color:purple;">ListItem</mark>](listitem.md)<mark style="color:purple;">></mark>

### delete()

Delete the list item.

> Returns: <mark style="color:purple;">Promise\<void></mark>

### complete()

Set the item to 'complete'.

> Returns: <mark style="color:purple;">Promise\<void></mark>

### uncomplete()

Set the item to 'uncomplete'.

> Returns: <mark style="color:purple;">Promise\<void></mark>
