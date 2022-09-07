---
description: >-
  The Guild is also known as 'server', it's where everything happen, and where
  the bot interacts with people/the environment.
---

# 🏛 Guild

### Properties

| Property         | Description                                         | Type   |
| ---------------- | --------------------------------------------------- | ------ |
| client           | Client                                              | Client |
| id               | ID of the Guild/server.                             | String |
| ownerID          | The owner of the guild                              | String |
| type             | The guild's type                                    | String |
| name             | Guild name                                          | String |
| url              | URL of the guild                                    | String |
| about            | 'About' of the guild (description)                  | String |
| description      | The guild's description                             | String |
| about            | Same as 'description'.                              | String |
| iconURL          | the url of the guild's icon                         | String |
| bannerURL        | the url of the guild's banner                       | String |
| timezone         | the timezone of the guild                           | String |
| defaultChannelID | the id of the default channel of the guild          | String |
| \_createdAt      | Timestamp (unix epoch time) of the guild's creation | Number |
| createdAt        | string representation of the \_createdAt timestamp. | Date   |

## Constructor

```javascript
new Message(rawData, client)
```

| Properties | Description                                     | Type                | Required? |
| ---------- | ----------------------------------------------- | ------------------- | --------- |
| rawData    | raw data received from ws and converted to JSON | Object              | true      |
| client     | Client                                          | [Client](client.md) | true      |

{% hint style="danger" %}
Do not use this constructor unless you know what you're doing. This constructor is used to return you rawdata into component.
{% endhint %}
