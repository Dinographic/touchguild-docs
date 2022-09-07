---
description: BannedMember is a component that extends the User component.
---

# ☠ BannedMember

### Properties

| Property                 | Description                 | Type                |
| ------------------------ | --------------------------- | ------------------- |
| data                     | raw data                    | Object              |
| client                   | client                      | [Client](client.md) |
| id                       |                             | String              |
| guildID                  |                             | String              |
| channelID                |                             | String              |
| name                     |                             | String              |
| description              |                             | String              |
| location                 |                             | String              |
| url                      |                             | String              |
| color                    |                             | Number              |
| rsvpLimit                |                             | Number              |
| \_startsAt               |                             | Number\|null        |
| duration                 | duration in ms of the event | Number              |
| isPrivate                |                             | Boolean             |
| mentions                 |                             | Object              |
| \_createdAt              |                             | Number\|null        |
| memberID                 |                             | String              |
| cancellation             |                             | Object              |
| cancellation.description |                             | String              |
| cancellation.createdBy   |                             | String              |

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

