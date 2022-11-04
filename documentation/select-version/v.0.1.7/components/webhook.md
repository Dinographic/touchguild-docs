# 💭 Webhook

## Properties

| Property    | Description                                            | Type                                         |
| ----------- | ------------------------------------------------------ | -------------------------------------------- |
| \_client    | Client                                                 | [Client](client.md) |
| id          | ID of the webhook                                      | String                                       |
| guildID     | ID of the guild the webhook got sent on.               | String                                       |
| channelID   | ID of the channel the webhook got sent on.             | String                                       |
| username    | Webhook username.                                      | String                                       |
| \_createdAt | Timestamp (unix epoch time) of the webhook's creation. | Number                                       |
| \_deletedAt | Timestamp (unix epoch time) of the webhook's deletion. | Number\|null                                 |
| createdBy   | ID of the webhook's owner.                             | String                                       |
| token       | Webhook token                                          | String\|null                                 |
| createdAt   | String representation of the \_createdAt timestamp.    | Date                                         |
| deletedAt   | String representation of the \_deletedAt timestamp.    | Date\|null                                   |

## Constructor

```javascript
new Webhook(rawData, client)
```

| Properties | Description                                     | Type                                         | Required? |
| ---------- | ----------------------------------------------- | -------------------------------------------- | --------- |
| rawData    | raw data received from ws and converted to JSON | Object                                       | true      |
| client     | Client                                          | [Client](client.md) | true      |

{% hint style="danger" %}
Do not use this constructor unless you know what you're doing. This constructor is used to return you rawdata into component.
{% endhint %}

## Methods

### edit()

Edit the webhook.

| Properties         | Description                      | Type   | Required? |
| ------------------ | -------------------------------- | ------ | --------- |
| options            | Edit options.                    | Object | true      |
| options.name       | New webhook's name.              | String | true      |
| options.channelID? | Move webhook to another channel. | String | false     |

> Returns: <mark style="color:purple;">Promise<</mark>[<mark style="color:purple;">Webhook</mark>](webhook.md)<mark style="color:purple;">></mark>

### delete()

Delete the webhook.

> Returns: <mark style="color:purple;">Promise\<void></mark>
