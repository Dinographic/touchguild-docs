---
description: >-
  The Guilded Bot's client, where everything's happen and where the Guilded bot
  interacts with guilds/servers.
---

# Client

### Properties

| Property    | Description                                                                   | Type      |
| ----------- | ----------------------------------------------------------------------------- | --------- |
| params      | The bot's options you set when you're creating a new client. (includes token) | Object    |
| identifiers | Names of all standard Guilded events and their equivalent in simple stypes.   | Object    |
| ws          | The WebSocket manager used to connect to the API.                             | WSManager |
| cache       | The client's cache, used for storing things such as message contents          | Map       |
| token       | The bot's inserted token.                                                     | String    |

### Constructor

```javascript
new Client(params)
```

| Properties   | Description                  | Type   |
| ------------ | ---------------------------- | ------ |
| params       | Client's parameters/options. | Object |
| params.token | Bot's token                  | String |
