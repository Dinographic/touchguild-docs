---
description: >-
  The Member component extends the User component. (Member is a Guild Member or
  Server Member)
---

# 🫂 Member

## Properties

| Property   | Description                                        | Type                                       |
| ---------- | -------------------------------------------------- | ------------------------------------------ |
| roles      | Member's roles                                     | Array\|null                                |
| nickname   | Member's guild nickname                            | String\|null                               |
| \_joinedAt | Timestamp of when the user joined the guild.       | Number\|null                               |
| isOwner    | If the member is the guild's owner or not.         | Boolean                                    |
| guildID    | The ID of the guild.                               | String                                     |
| guild      | Guild component                                    | [Guild](../../v.0.1.7/components/guild.md) |
| joinedAt   | string representation of the \_joinedAt timestamp. | Date                                       |
| user       | User component with less information.              | [User](user.md)                            |

## Constructor

```javascript
new Member(rawData, client, guildID)
```

| Properties | Description                                     | Type                                         | Required? |
| ---------- | ----------------------------------------------- | -------------------------------------------- | --------- |
| rawData    | raw data received from ws and converted to JSON | Object                                       | true      |
| client     | Client                                          | [Client](../../v.0.1.7/components/client.md) | true      |
| guildID    | Guild id                                        | String                                       | true      |

{% hint style="danger" %}
Do not use this constructor unless you know what you're doing. This constructor is used to return you rawdata into component.
{% endhint %}

## Methods

### getSocialLink(socialMediaName)

Get a specific social link from member.

| Properties      | Description                                              | Type   | Required? |
| --------------- | -------------------------------------------------------- | ------ | --------- |
| socialMediaName | The name of the social you'd like to get from the member | String | true      |

> Returns: <mark style="color:purple;">Promise\<Object></mark>

### addToGroup(groupID)

Add member to a guild group.

| Properties | Description               | Type   | Required? |
| ---------- | ------------------------- | ------ | --------- |
| groupID    | the id of the guild group | String | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### removeFromGroup(groupID)

Remove member from a guild group.

| Properties | Description               | Type   | Required? |
| ---------- | ------------------------- | ------ | --------- |
| groupID    | the id of the guild group | String | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### addRole(roleID)

Add a role to member.

| Properties | Description        | Type   | Required? |
| ---------- | ------------------ | ------ | --------- |
| roleID     | the id of the role | Number | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### removeRole(roleID)

Remove a role from member.

| Properties | Description        | Type   | Required? |
| ---------- | ------------------ | ------ | --------- |
| roleID     | the id of the role | Number | true      |

> Returns: <mark style="color:purple;">Promise\<void></mark>

### award(xpAmount)

Awards member using the built-in EXP system. (Returns the 'total' of experience)

| Properties | Description  | Type   | Required? |
| ---------- | ------------ | ------ | --------- |
| xpAmount   | amount of xp | Number | true      |

> Returns: <mark style="color:purple;">Promise\<Number></mark>

### setXP(xpAmount)

Sets member's xp using the built-in EXP system. (Returns the 'total' of experience)

| Properties | Description  | Type   | Required? |
| ---------- | ------------ | ------ | --------- |
| xpAmount   | amount of xp | Number | true      |

> Returns: <mark style="color:purple;">Promise\<Number></mark>
