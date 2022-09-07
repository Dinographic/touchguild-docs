# 📆 CalendarEventRSVP

### Properties

| Property    | Description                                                                     | Type                |
| ----------- | ------------------------------------------------------------------------------- | ------------------- |
| data        | raw data                                                                        | Object              |
| client      | Client                                                                          | [Client](client.md) |
| id          | Calendar Event RSVP ID                                                          | Number              |
| guildID     | Guild/server ID                                                                 | String              |
| channelID   | Calendar channel id                                                             | String              |
| memberID    | RSVP member id                                                                  | String              |
| status      | Status of the RSVP (going, maybe, declined, invited, waitlisted, not responded) | String              |
| \_createdAt | Timestamp (unix epoch time) of the rsvp's creation.                             | Number\|null        |
| createdBy   | ID of the member that created the rsvp.                                         | String              |
| updatedBy   | ID of the member that updated the rsvp (if updated)                             | String              |
| member      | Member that created the rsvp.                                                   | [Member](member.md) |
| createdAt   | string representation of the \_createdAt timestamp                              | Date\|null          |

## Constructor

```javascript
new CalendarRSVP(rawData, client)
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

Edit the calendar rsvp.

| Properties     | Description                                                              | Type   | Required? |
| -------------- | ------------------------------------------------------------------------ | ------ | --------- |
| options        | Edit options                                                             | Object | true      |
| options.status | RSVP status (going, maybe, declined, invited, waitlisted, not responded) | String | true      |

> Returns: <mark style="color:purple;">Promise<</mark>[<mark style="color:purple;">CalendarEventRSVP</mark>](calendareventrsvp.md)<mark style="color:purple;">></mark>

### delete()

Delete the calendar rsvp.

> Returns: <mark style="color:purple;">Promise<</mark>void<mark style="color:purple;">></mark>
