---
description: Calendar Event is a specific event from a calendar channel, so obvious.
---

# 🗓 CalendarEvent

## Properties

| Property                | Description                                         | Type                                                                                            |
| ----------------------- | --------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| data                    | raw data                                            | Object                                                                                          |
| client                  | client                                              | [Client](../../v.0.1.6/components/client.md)                                                    |
| id                      | event id                                            | String                                                                                          |
| guildID                 | guild id                                            | String                                                                                          |
| channelID               | id of the channel                                   | String                                                                                          |
| name                    | event name                                          | String                                                                                          |
| description             | event description                                   | String                                                                                          |
| location                | event location set by member                        | String                                                                                          |
| url                     | event url set by member                             | String                                                                                          |
| color                   | event color                                         | Number                                                                                          |
| rsvpLimit               | attendant/entry limit                               | Number                                                                                          |
| \_startsAt              | timestamp of when the event starts.                 | Number\|null                                                                                    |
| duration                | duration in ms of the event                         | Number                                                                                          |
| isPrivate               | //                                                  | Boolean                                                                                         |
| mentions                | event's mentions                                    | Object ([<mark style="color:purple;">MentionsType</mark>](../../v.0.1.6/types/mentionstype.md)) |
| \_createdAt             | timestamp of the event's creation.                  | Number\|null                                                                                    |
| memberID                | id of the member who created the event.             | String                                                                                          |
| cancelation             | cancelation info (if canceled)                      | Object\|null                                                                                    |
| cancelation.description | cancelation description                             | String                                                                                          |
| cancelation.createdBy   | id of the member who canceled the event.            | String                                                                                          |
| member                  | Member that created the event.                      | [Member](../../v.0.1.6/components/member.md)                                                    |
| createdAt               | string representation of the \_createdAt timestamp. | Date                                                                                            |

## Constructor

```javascript
new CalendarEvent(rawData, client)
```

| Properties | Description                                     | Type                                         | Required? |
| ---------- | ----------------------------------------------- | -------------------------------------------- | --------- |
| rawData    | raw data received from ws and converted to JSON | Object                                       | true      |
| client     | Client                                          | [Client](../../v.0.1.6/components/client.md) | true      |

{% hint style="danger" %}
Do not use this constructor unless you know what you're doing. This constructor is used to return you rawdata into component.
{% endhint %}

## Methods

### edit(options)

Edit the calendar event.

| Properties           | Description               | Type    | Required? |
| -------------------- | ------------------------- | ------- | --------- |
| options              | edit options              | Object  | true      |
| options.name?        | new event's name          | String  | false     |
| options.description? | new event's description   | String  | false     |
| options.location?    | new event's location      | String  | false     |
| options.startsAt?    | date-time string          | String  | false     |
| options.url?         | new event's url           | String  | false     |
| options.color?       | new event's color         | Number  | false     |
| options.rsvpLimit?   | new event's entry limit   | Number  | false     |
| options.duration?    | new event's duration      | Number  | false     |
| options.isPrivate?   | new event's private param | Boolean | false     |

> Returns: <mark style="color:purple;">Promise<</mark>[<mark style="color:purple;">CalendarEvent</mark>](../../v.0.1.6/components/calendarevent.md)<mark style="color:purple;">></mark>

### delete()

Delete the calendar event.

> Returns: <mark style="color:purple;">Promise\<void></mark>
