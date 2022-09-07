---
description: >-
  The Guilded Bot's client, where everything's happen and where the Guilded bot
  interacts with guilds/servers.
---

# 🤖 Client

## Properties

| Property    | Description                                                                   | Type      |
| ----------- | ----------------------------------------------------------------------------- | --------- |
| params      | The bot's options you set when you're creating a new client. (includes token) | Object    |
| identifiers | Names of all standard Guilded events and their equivalent in simple types.    | Object    |
| ws          | The WebSocket manager used to connect to the API.                             | WSManager |
| cache       | The client's cache, used for storing things such as message contents          | Map       |
| token       | The bot's inserted token.                                                     | String    |

## Constructor

```javascript
new Client(params)
```

| Properties   | Description                                            | Type    | Required? |
| ------------ | ------------------------------------------------------ | ------- | --------- |
| params       | Client's parameters/options.                           | Object  | true      |
| params.token | Bot's token                                            | String  | true      |
| params.REST  | Enable/disable REST methods, it is enabled by default. | Boolean | false     |

## Methods

{% hint style="info" %}
Client have standard event emitter types, they're not listed there.
{% endhint %}

### connect()

Connects your bot to the Guilded API.

### getRESTChannel(channelID)

Get a specific channel's information.

| Properties | Description                          | Type   |
| ---------- | ------------------------------------ | ------ |
| channelID  | id of the channel you'd like to get. | String |

> Returns: <mark style="color:purple;">Promise\<Channel></mark>



### getRESTMember(guildID, memberID)

Get a specific guild's/server's member.

| Properties | Description      | Type   |
| ---------- | ---------------- | ------ |
| guildID    | id of the server | String |
| memberID   | id of the user   | String |

> Returns: <mark style="color:purple;">Promise\<Member></mark>

### getRESTGuild(guildID)

Get a specific guild/server.

| Properties | Description      | Type   |
| ---------- | ---------------- | ------ |
| guildID    | id of the server | String |

> Returns: <mark style="color:purple;">Promise\<Guild></mark>

### getRESTChannelMessages(channelID, filter?)

Get a list channel Message component.

| Properties             | Description                      | Type    |
| ---------------------- | -------------------------------- | ------- |
| channelID              | id of the channel                | String  |
| filter?                | filter channel messages          | Object  |
| filter.before?         | Date-time string                 | String  |
| filter.after?          | Date-time string                 | String  |
| filter.limit?          | Limit the channel message output | Number  |
| filter.includePrivate? | Include private messages or not  | Boolean |

> Returns: <mark style="color:purple;">Promise\<Array<</mark>[<mark style="color:purple;">Message</mark>](message.md)<mark style="color:purple;">>></mark>

### getRESTChannelDocs(channelID, filter?)

Get a list of channel Doc component.

| Properties     | Description                  | Type   |
| -------------- | ---------------------------- | ------ |
| channelID      | id of the channel            | String |
| filter?        | filter channel docs          | Object |
| filter.before? | Date-time string             | String |
| filter.limit?  | Limit the channel doc output | Number |

> Returns: <mark style="color:purple;">Promise\<Array\<Doc>></mark>

### getRESTChannelDoc(channelID, docID)

Get a specific channel doc.

| Properties | Description       | Type   |
| ---------- | ----------------- | ------ |
| channelID  | id of the channel | String |
| docID      | id of the doc     | Number |

> Returns: <mark style="color:purple;">Promise\<Doc></mark>

### getRESTForumTopics(channelID, filter?)

Get a list of ForumTopic component.

| Properties     | Description                  | Type   |
| -------------- | ---------------------------- | ------ |
| channelID      | id of the channel            | String |
| filter?        | filter forum topics          | Object |
| filter.before? | Date-time string             | String |
| filter.limit?  | Limit the forum topic output | Number |

> Returns: <mark style="color:purple;">Promise\<Array\<ForumTopic>></mark>

### getRESTForumTopic(channelID, topicID)

Get a specific ForumTopic component

| Properties | Description       | Type   |
| ---------- | ----------------- | ------ |
| channelID  | id of the channel | String |
| topicID    | id of the topic   | Number |

> Returns: <mark style="color:purple;">Promise\<ForumTopic></mark>

### getRESTCalendarEvents(channelID, filter?)

Get a list of CalendarEvent component

| Properties     | Description                     | Type   |
| -------------- | ------------------------------- | ------ |
| channelID      | id of the channel               | String |
| filter?        | filter calendar events          | Object |
| filter.before? | Date-time string                | String |
| filter.after?  | Date-time string                | String |
| filter.limit?  | Limit the calendar event output | Number |

> Returns: <mark style="color:purple;">Promise\<Array\<CalendarEvent>></mark>

### getRESTCalendarEvent(channelID, eventID)

Get a specific calendar event component

| Properties | Description                            | Type   |
| ---------- | -------------------------------------- | ------ |
| channelID  | id of the channel containing the event | String |
| eventID    | id of the event                        | Number |

> Returns: <mark style="color:purple;">Promise\<CalendarEvent></mark>

### getRESTCalendarRsvps(channelID, eventID)

Get a list of calendar event rsvp

| Properties | Description                            | Type   |
| ---------- | -------------------------------------- | ------ |
| channelID  | id of the channel containing the event | String |
| eventID    | id of the event                        | Number |

> Returns: <mark style="color:purple;">Promise\<Array\<CalendarRSVP>></mark>

### getRESTCalendarRsvp(channelID, eventID, memberID)

Get a specific calendar event rsvp

| Properties | Description                            | Type   |
| ---------- | -------------------------------------- | ------ |
| channelID  | id of the channel containing the event | String |
| eventID    | id of the event                        | Number |
| memberID   | id of the member                       | String |

> Returns: <mark style="color:purple;">Promise\<CalendarRSVP></mark>

### getRESTListItem(channelID, itemID)

Get a specific item from a list channel.

| Properties | Description                                | Type   |
| ---------- | ------------------------------------------ | ------ |
| channelID  | id of the channel containing the list item | String |
| itemID     | id of the item                             | String |

> Returns: <mark style="color:purple;">Promise\<ListItem></mark>

### getRESTListItems(channelID)

Get a list of ListItem from a list channel.

| Properties | Description                                 | Type   |
| ---------- | ------------------------------------------- | ------ |
| channelID  | id of the channel containing the list items | String |

> Returns: <mark style="color:purple;">Promise\<Array\<ListItem>></mark>

### getRESTGuildWebhook(guildID, webhookID)

Get a guild webhook.

| Properties | Description       | Type   |
| ---------- | ----------------- | ------ |
| guildID    | id of the guild   | String |
| webhookID  | id of the webhook | String |

> Returns: <mark style="color:purple;">Promise\<Webhook></mark>

### getRESTChannelWebhooks(guildID, channelID)

Get a list of webhook selected from a specific channel.

| Properties | Description       | Type   |
| ---------- | ----------------- | ------ |
| guildID    | id of the guild   | String |
| channelID  | id of the channel | String |

> Returns: <mark style="color:purple;">Promise\<Array\<Webhook>></mark>

### getChannelMessages(channelID, filter?)

Get a list of channel messages, only basic data included.

| Properties             | Description                      | Type    |
| ---------------------- | -------------------------------- | ------- |
| channelID              | id of the channel                | String  |
| filter?                | filter channel messages          | String  |
| filter.before?         | Date-time string                 | String  |
| filter.after?          | Date-time string                 | String  |
| filter.limit?          | Limit the channel mesage output  | Number  |
| filter.includePrivate? | Include private messages or not. | Boolean |

> Returns: <mark style="color:purple;">Promise\<Array\<Object>></mark>

{% hint style="warning" %}
Non-REST Methods only returns an object/array, methods and cached information aren't provided.

Be aware that the returned object/array is having Guilded API types and not ours.
{% endhint %}

{% hint style="info" %}
Non-REST Methods can provide better response time than the REST ones when it treats multiple object of information.
{% endhint %}

### getChannelDocs(channelID, filter?)

Get a list of channel docs, only basic data included.

| Properties     | Description                       | Type   |
| -------------- | --------------------------------- | ------ |
| channelID      | id of the channel containing docs | String |
| filter?        | filter channel docs               | String |
| filter.before? | Date-time string                  | String |
| filter.limit?  | Limit the channel doc output      | Number |

> Returns: <mark style="color:purple;">Promise\<Array\<Object>></mark>

{% hint style="warning" %}
Non-REST Methods only returns an object/array, methods and cached information aren't provided.

Be aware that the returned object/array is having Guilded API types and not ours.
{% endhint %}

{% hint style="info" %}
Non-REST Methods can provide better response time than the REST ones when it treats multiple object of information.
{% endhint %}

### getForumTopics(channelID, filter?)

Get a list of forum topic, only basic data included.

| Properties     | Description                               | Type   |
| -------------- | ----------------------------------------- | ------ |
| channelID      | id of the forum channel containing topics | String |
| filter?        | filter forum topics                       | String |
| filter.before? | Date-time string                          | String |
| filter.limit?  | Limit the forum topic output              | Number |

> Returns: <mark style="color:purple;">Promise\<Array\<Object>></mark>

{% hint style="warning" %}
Non-REST Methods only returns an object/array, methods and cached information aren't provided.

Be aware that the returned object/array is having Guilded API types and not ours.
{% endhint %}

{% hint style="info" %}
Non-REST Methods can provide better response time than the REST ones when it treats multiple object of information.
{% endhint %}

### getCalendarEvents(channelID, filter?)

Get a list of calendar event, only basic data included.

| Properties     | Description                                  | Type   |
| -------------- | -------------------------------------------- | ------ |
| channelID      | id of the calendar channel containing events | String |
| filter?        | filter calendar events                       | String |
| filter.before? | Date-time string                             | String |
| filter.after?  | Date-time string                             | String |
| filter.limit?  | Limit the calendar event output              | Number |

> Returns: <mark style="color:purple;">Promise\<Array\<Object>></mark>

{% hint style="warning" %}
Non-REST Methods only returns an object/array, methods and cached information aren't provided.

Be aware that the returned object/array is having Guilded API types and not ours.
{% endhint %}

{% hint style="info" %}
Non-REST Methods can provide better response time than the REST ones when it treats multiple object of information.
{% endhint %}

### getCalendarRsvps(channelID, eventID)

Get a list of calendar event rsvp, only basic data included.

| Properties | Description                                  | Type   |
| ---------- | -------------------------------------------- | ------ |
| channelID  | id of the calendar channel containing events | String |
| eventID    | id of the calendar event                     | Number |

> Returns: <mark style="color:purple;">Promise\<Array\<Object>></mark>

{% hint style="warning" %}
Non-REST Methods only returns an object/array, methods and cached information aren't provided.

Be aware that the returned object/array is having Guilded API types and not ours.
{% endhint %}

{% hint style="info" %}
Non-REST Methods can provide better response time than the REST ones when it treats multiple object of information.
{% endhint %}

### getListItems(channelID)

List of item of the selected list channel, only basic data included.

| Properties | Description                                      | Type   |
| ---------- | ------------------------------------------------ | ------ |
| channelID  | id of the list channel which contains the items. | String |

> Returns: <mark style="color:purple;">Promise\<Array\<Object>></mark>

{% hint style="warning" %}
Non-REST Methods only returns an object/array, methods and cached information aren't provided.

Be aware that the returned object/array is having Guilded API types and not ours.
{% endhint %}

{% hint style="info" %}
Non-REST Methods can provide better response time than the REST ones when it treats multiple object of information.
{% endhint %}

### getMemberRoles(guildID, memberID)

Gives you a list of every roles the member has.

| Properties | Description             | Type   |
| ---------- | ----------------------- | ------ |
| guildID    | id of the server/guild  | String |
| memberID   | id of the target member | String |

{% hint style="success" %}
getMemberRoles is the only proposed method to get member's roles, it is because there is nothing to treat, it's just an array of 'roles' which are numbers/int.
{% endhint %}

> Returns: <mark style="color:purple;">Promise\<Array\<Number>></mark>

### getChannelWebhooks(guildID, channelID)

Returns you a list of channel webhooks, only basic data included.

| Properties | Description            | Type   |
| ---------- | ---------------------- | ------ |
| guildID    | id of the server/guild | String |
| channelID  | id of the channel      | String |

> Returns: <mark style="color:purple;">Promise\<Array\<Object>></mark>

{% hint style="warning" %}
Non-REST Methods only returns an object/array, methods and cached information aren't provided.

Be aware that the returned object/array is having Guilded API types and not ours.
{% endhint %}

{% hint style="info" %}
Non-REST Methods can provide better response time than the REST ones when it treats multiple object of information.
{% endhint %}

### createChannel(location, name, type, options)

Create a channel in a guild, can also be placed in a group or category.

| Properties         | Description                                                                                                                  | Type    | Required? |
| ------------------ | ---------------------------------------------------------------------------------------------------------------------------- | ------- | --------- |
| guildID            | id of the guild/server                                                                                                       | Object  | true      |
| name               | new channel's name                                                                                                           | String  | true      |
| type               | new channel's type  ("announcement", "chat", "calendar", "forums", "media", "docs", "voice", "list", "scheduling", "stream") | String  | true      |
| options            | new channel's options                                                                                                        | Object  | false     |
| options.topic      | new channel's topic/description.                                                                                             | String  | false     |
| options.isPublic   | --                                                                                                                           | Boolean | false     |
| options.categoryID | locate the channel in a specific category                                                                                    | Number  | false     |
| options.groupID    | locate the channel in a specific group                                                                                       | String  | false     |

> Returns: <mark style="color:purple;">Promise<</mark>[<mark style="color:purple;">Channel</mark>](channel.md)<mark style="color:purple;">></mark>

### createMessage(channelID, options)

Create a message in a specific channel.

| Properties              | Description                                                | Type           | Required? |
| ----------------------- | ---------------------------------------------------------- | -------------- | --------- |
| channelID               | channel's id                                               | String         | true      |
| options                 | message's options                                          | Object         | true      |
| options.content         | message content                                            | String         | false     |
| options.embeds          | message's embeds                                           | Array\<Object> | false     |
| options.replyMessageIds | list of message id to reply                                | Array\<String> | false     |
| options.isSilent        | notify user(s)?                                            | Boolean        | false     |
| options.isPrivate       | message will only be seen by those mentioned or replied to | Boolean        | false     |

> Returns: <mark style="color:blue;">Promise</mark><[<mark style="color:purple;">Message</mark>](message.md)>

### editMessage(channelID, messageID, newMessage)

Update a specific message.

| Properties         | Description           | Type           | Required? |
| ------------------ | --------------------- | -------------- | --------- |
| channelID          | channel's id          | String         | true      |
| messageID          | target message id     | String         | true      |
| newMessage         | new message's options | Object         | true      |
| newMessage.content | new message content   | String         | false     |
| newMessage.embeds  | new message's embeds  | Array\<Object> | false     |

> Returns: <mark style="color:purple;">Promise<</mark>[<mark style="color:purple;">Message</mark>](message.md)<mark style="color:purple;">></mark>

### deleteMessage(channelID, messageID)

Delete a specific message.

| Properties | Description       | Type   | Required? |
| ---------- | ----------------- | ------ | --------- |
| channelID  | channel's id      | String | true      |
| messageID  | target message id | String | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### addMessageReaction(channelID, messageID, reaction)

Add a reaction to a channel message

| Properties | Description       | Type   | Required? |
| ---------- | ----------------- | ------ | --------- |
| channelID  | channel id        | String | true      |
| messageID  | target message id | String | true      |
| reaction   | emote id          | Number | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### removeMessageReaction(channelID, messageID, reaction)

Remove a specific reaction from a channel message.

| Properties | Description       | Type   | Required? |
| ---------- | ----------------- | ------ | --------- |
| channelID  | channel id        | String | true      |
| messageID  | target message id | String | true      |
| reaction   | emote id          | Number | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### createTopic(channelID, options)

Create a topic in a forum.

| Properties      | Description      | Type   | Required? |
| --------------- | ---------------- | ------ | --------- |
| channelID       | forum channel id | String | true      |
| options         | topic options    | Object | true      |
| options.title   | topic title      | String | true      |
| options.content | topic content    | String | true      |

> Returns: <mark style="color:purple;">Promise\<ForumTopic></mark>

### editTopic(channelID, topicID)

Edit a specific forum topic

| Properties       | Description      | Type   | Required? |
| ---------------- | ---------------- | ------ | --------- |
| channelID        | forum channel id | String | true      |
| topicID          | forum topic id   | Number | true      |
| options          | topic options    | Object | true      |
| options.title?   | topic title      | String | false     |
| options.content? | topic content    | String | false     |

> Returns: <mark style="color:purple;">Promise\<ForumTopic></mark>

### deleteTopic(channelID, topicID)

Delete a specific forum topic

| Properties | Description      | Type   | Required? |
| ---------- | ---------------- | ------ | --------- |
| channelID  | forum channel id | String | true      |
| topicID    | forum topic id   | Number | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### pinTopic(channelID, topicID)

Pin a specific forum topic.

| Properties | Description      | Type   | Required? |
| ---------- | ---------------- | ------ | --------- |
| channelID  | forum channel id | String | true      |
| topicID    | forum topic id   | Number | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### unpinTopic(channelID, topicID)

Unpin a specific forum topic.

| Properties | Description      | Type   | Required? |
| ---------- | ---------------- | ------ | --------- |
| channelID  | forum channel id | String | true      |
| topicID    | forum topic id   | Number | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### createDoc(channelID, options)

Create a doc in a docs channel.

| Properties      | Description    | Type   | Required? |
| --------------- | -------------- | ------ | --------- |
| channelID       | doc channel id | String | true      |
| options         | doc options    | Object | true      |
| options.title   | doc title      | String | true      |
| options.content | doc content    | String | true      |

> Returns: <mark style="color:purple;">Promise\<Doc></mark>

### editDoc(channelID, docID, options)

Edit a specific doc.

| Properties       | Description    | Type   | Required? |
| ---------------- | -------------- | ------ | --------- |
| channelID        | doc channel id | String | true      |
| docID            | channel doc id | Number | true      |
| options          | doc options    | Object | true      |
| options.title?   | doc title      | String | false     |
| options.content? | doc content    | String | false     |

> Returns: <mark style="color:purple;">Promise\<Doc></mark>

### deleteDoc(channelID)

Delete a specific channel doc.

| Properties | Description    | Type   | Required? |
| ---------- | -------------- | ------ | --------- |
| channelID  | doc channel id | String | true      |
| docID      | channel doc id | Number | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### createCalendarEvent(channelID, options)

Create a calendar event.

| Properties           | Description                     | Type    | Required? |
| -------------------- | ------------------------------- | ------- | --------- |
| channelID            | calendar channel id             | String  | true      |
| options              | calendar event options          | Object  | true      |
| options.name         | event name                      | String  | true      |
| options.description? | event description               | String  | false     |
| options.location?    | event location, can be anything | String  | false     |
| options.startsAt?    | Date-time string                | String  | false     |
| options.url?         | event url                       | String  | false     |
| options.color?       | event color                     | Number  | false     |
| options.rsvpLimit?   | event entry limit               | Number  | false     |
| options.duration?    | event duration in ms            | Number  | false     |
| options.isPrivate?   | --                              | Boolean | false     |



> Returns: <mark style="color:purple;">Promise\<CalendarEvent></mark>

### editCalendarEvent(channelID, eventID, options)

Edit a specific calendar event.

| Properties           | Description                     | Type    | Required? |
| -------------------- | ------------------------------- | ------- | --------- |
| channelID            | calendar channel id             | String  | true      |
| eventID              | calendar event id               | Number  | true      |
| options              | calendar event options          | Object  | true      |
| options.name?        | event name                      | String  | false     |
| options.description? | event description               | String  | false     |
| options.location?    | event location, can be anything | String  | false     |
| options.startsAt?    | Date-time string                | String  | false     |
| options.url?         | event url                       | String  | false     |
| options.color?       | event color                     | Number  | false     |
| options.rsvpLimit?   | event entry limit               | Number  | false     |
| options.duration?    | event duration in ms            | Number  | false     |
| options.isPrivate?   | --                              | Boolean | false     |

> Returns: <mark style="color:purple;">Promise\<CalendarEvent></mark>

### deleteCalendarEvent(channelID, eventID)

Delete a specific calendar event.

| Properties | Description         | Type   | Required? |
| ---------- | ------------------- | ------ | --------- |
| channelID  | calendar channel id | String | true      |
| eventID    | calendar event id   | Number | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### editCalendarRsvp(channelID, eventID, memberID)

Add/edit a specific calendar event RSVP.

| Properties     | Description                                                                            | Type   | Required? |
| -------------- | -------------------------------------------------------------------------------------- | ------ | --------- |
| channelID      | calendar channel id                                                                    | String | true      |
| eventID        | calendar event id                                                                      | Number | true      |
| memberID       | rsvp member id                                                                         | String | true      |
| options        | event rsvp options                                                                     | Object | true      |
| options.status | RSVP status ('going' ,'maybe'\|, 'declined', 'invited', 'waitlisted', 'not responded') | String | true      |



> Returns: <mark style="color:purple;">Promise\<CalendarRSVP></mark>

### deleteCalendarRsvp(channelID, eventID, memberID)

Delete a specific calendar event RSVP.

| Properties | Description           | Type   | Required? |
| ---------- | --------------------- | ------ | --------- |
| channelID  | calendar channel id   | String | true      |
| eventID    | calendar event id     | Number | true      |
| memberID   | rsvp target member id | String | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### createListItem(channelID, content, note?)

Create an item within a list channel.

| Properties   | Description                  | Type   | Required? |
| ------------ | ---------------------------- | ------ | --------- |
| channelID    | 'List' channel id.           | String | true      |
| content      | content/message of the list  | String | true      |
| note?        | Note object                  | Object | false     |
| note.content | add a note/edit note content | String | true      |

> Returns: <mark style="color:purple;">Promise\<ListItem></mark>

### editListItem(channelID, itemID, content, note?)

Edit a list item.

| Properties   | Description                  | Type   | Required? |
| ------------ | ---------------------------- | ------ | --------- |
| channelID    | 'List' channel id.           | String | true      |
| itemID       | ID of the target item.       | String | true      |
| content      | content/message of the list  | String | true      |
| note?        | Note object                  | Object | false     |
| note.content | add a note/edit note content | String | true      |

> Returns: <mark style="color:purple;">Promise\<ListItem></mark>

### completeListItem(channelID, itemID)

Complete (checkmark will show up) a specific item from a list channel.

| Properties | Description            | Type   | Required? |
| ---------- | ---------------------- | ------ | --------- |
| channelID  | 'List' channel id.     | String | true      |
| itemID     | ID of the target item. | String | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### uncompleteListItem(channelID, itemID)

Uncomplete (checkmark will disappear) a specific item from a list channel.

| Properties | Description            | Type   | Required? |
| ---------- | ---------------------- | ------ | --------- |
| channelID  | 'List' channel id.     | String | true      |
| itemID     | ID of the target item. | String | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### addGuildMemberGroup(groupID, memberID)

Add a Guild Member to a Guild group.

| Properties | Description              | Type   | Required? |
| ---------- | ------------------------ | ------ | --------- |
| groupID    | Guild group id           | String | true      |
| memberID   | ID of the target member. | String | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### removeGuildMemberGroup(groupID, memberID)

Remove a Guild Member from a Guild group.

| Properties | Description              | Type   | Required? |
| ---------- | ------------------------ | ------ | --------- |
| groupID    | Guild group id           | String | true      |
| memberID   | ID of the target member. | String | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### addGuildMemberRole(guildID, memberID, roleID)

Add a role to a guild member.

| Properties | Description              | Type   | Required? |
| ---------- | ------------------------ | ------ | --------- |
| groupID    | Guild group id           | String | true      |
| memberID   | ID of the target member. | String | true      |
| roleID     | Role to add              | Number | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### removeGuildMemberRole(guildID, memberID, roleID)

Remove a role from a guild member.

| Properties | Description              | Type   | Required? |
| ---------- | ------------------------ | ------ | --------- |
| groupID    | Guild group id           | String | true      |
| memberID   | ID of the target member. | String | true      |
| roleID     | Role to add              | Number | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>



### createGuildWebhook(guildID, channelID, name)

| Properties | Description             | Type   | Required? |
| ---------- | ----------------------- | ------ | --------- |
| guildID    | id of the guild/server  | String | true      |
| channelID  | id of the channel       | String | true      |
| name       | name of the new webhook | String | true      |

> Returns: <mark style="color:purple;">Promise\<Webhook></mark>

