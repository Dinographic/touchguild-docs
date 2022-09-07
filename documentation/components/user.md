---
description: >-
  It is the default component for a 'user', it contains every basic information
  about the user, those can be seen by anyone.
---

# 🙇♂ User

## Properties

| Property    | Description                                         | Type                |
| ----------- | --------------------------------------------------- | ------------------- |
| \_client    | Client                                              | [Client](client.md) |
| id          | User id                                             | String              |
| type        | Type of user, bot or user                           | String              |
| username    | User's username                                     | String              |
| \_createdAt | Timestamp of the user's creation.                   | Number              |
| avatarURL   | user's avatar url                                   | String              |
| bannerURL   | user's banner url                                   | String              |
| createdAt   | string representation of the \_createdAt timestamp. | Date                |

## Constructor

```javascript
new User(rawData, client)
```

| Properties | Description                                     | Type                | Required? |
| ---------- | ----------------------------------------------- | ------------------- | --------- |
| rawData    | raw data received from ws and converted to JSON | Object              | true      |
| client     | Client                                          | [Client](client.md) | true      |

{% hint style="danger" %}
Do not use this constructor unless you know what you're doing. This constructor is used to return you rawdata into component.
{% endhint %}
