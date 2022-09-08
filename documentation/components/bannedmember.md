---
description: BannedMember is a component that extends the User component.
---

# ☠ BannedMember

## Properties

| Property      | Description                                 | Type              |
| ------------- | ------------------------------------------- | ----------------- |
| guildID       | ID of the Guild                             | String            |
| ban           | ban information                             | Object            |
| ban.reason    | reason of the ban                           | String            |
| ban.createdAt | timestamp of when the user has been banned. | Number\|null      |
| ban.createdBy | Banned Member ID.                           | String            |
| user          | Banned member information.                  | Object            |
| user.id       | Banned member id                            | String            |
| user.type     | Banned member type                          | String            |
| user.username | Banned member username                      | String            |
| guild         | Guild/server component                      | [Guild](guild.md) |

## Constructor

```javascript
new BannedMember(rawData, client)
```

| Properties | Description                                     | Type                | Required? |
| ---------- | ----------------------------------------------- | ------------------- | --------- |
| rawData    | raw data received from ws and converted to JSON | Object              | true      |
| client     | Client                                          | [Client](client.md) | true      |

{% hint style="danger" %}
Do not use this constructor unless you know what you're doing. This constructor is used to return you rawdata into component.
{% endhint %}

