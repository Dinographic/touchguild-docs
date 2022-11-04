---
description: >-
  It is the 'user' of the logged bot, it has every information about the
  connected bot.
---

# 👾 UserClient

## Properties

| Property    | Description                                         | Type                                         |
| ----------- | --------------------------------------------------- | -------------------------------------------- |
| \_client    | Client                                              | [Client](../../v.0.1.7/components/client.md) |
| id          | Bot user id                                         | String                                       |
| botID       | Bot ID                                              | String                                       |
| type        | Type of user, `bot` or `user`                       | String                                       |
| username    | User's username                                     | String                                       |
| \_createdAt | Timestamp of the user's creation.                   | Number                                       |
| createdAt   | string representation of the \_createdAt timestamp. | Date                                         |
| createdBy   | ID of the bot's owner.                              | String                                       |
| bot         | Boolean that shows if the user is a bot or not.     | Boolean                                      |

## Constructor

```javascript
new UserClient(rawData, client)
```

| Properties | Description                                     | Type                                         | Required? |
| ---------- | ----------------------------------------------- | -------------------------------------------- | --------- |
| rawData    | raw data received from ws and converted to JSON | Object                                       | true      |
| client     | Client                                          | [Client](../../v.0.1.7/components/client.md) | true      |

{% hint style="danger" %}
Do not use this constructor unless you know what you're doing. This constructor is used to return you rawdata into component.
{% endhint %}
