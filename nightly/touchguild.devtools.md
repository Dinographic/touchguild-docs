---
description: TouchGuild's Developer Tools, made accessible to everyone.
---

# ⚙ TouchGuild.DevTools

## call

Make requests to the Guilded API, communicate like TouchGuild does.

### Constructor

```typescript
new TouchGuild.DevTools.call();
```

### Asynchronous methods

#### get(endpoint: string, token: string, queryParams?: string|object, crashOnRejection?: boolean)

Make a GET request.

Returns: <mark style="color:purple;">Promise\<object|void></mark>



#### post(endpoint: string, token: string, data: string|object, crashOnRejection?: boolean)

Make a POST request.

Returns: <mark style="color:purple;">Promise\<object|void></mark>



#### put(endpoint: string, token: string, data: string|object, crashOnRejection?: boolean)

Make a PUT request.

Returns: <mark style="color:purple;">Promise\<object|void></mark>



#### patch(endpoint: string, token: string, data: string|object, crashOnRejection?: boolean)

Make a PATCH request.

Returns: <mark style="color:purple;">Promise\<object|void></mark>



#### delete(endpoint: string, token:string, crashOnRejection?: boolean)

Make a DELETE request.

Returns: <mark style="color:purple;">Promise\<object|void></mark>



### Synchronous methods

#### syncGetChannel(channelID:string, client: Client)

Get a synchronously a channel.

Returns: [<mark style="color:purple;">Channel</mark>](../documentation/components/channel.md)<mark style="color:purple;"></mark>

<mark style="color:purple;"></mark>

#### syncGetMember(guildID: string, memberID: string, client:Client)

Get a synchronously a member.

Returns: [<mark style="color:purple;">Member</mark>](../documentation/components/member.md)<mark style="color:purple;"></mark>



#### syncGetGuild(guildID: string, client: Client)

Get a synchronously a guild.

Returns: [<mark style="color:purple;">Guild</mark>](../documentation/components/guild.md)<mark style="color:purple;"></mark>



### Deprecated methods.

{% hint style="danger" %}
We do not recommend to use deprecated methods, they're may be very buggy & we do not plan to fix them.
{% endhint %}

#### FETCH(method: string, endpoint: string, TOKEN: any, BODY:string|any)

Make an HTTP request. (asynchronous)

Returns: <mark style="color:purple;">Promise\<object|void></mark>



#### SYNCFETCH(method: string, endpoint: string, TOKEN: any, BODY:string|any)

Make an HTPP request. (synchronous)

Returns: <mark style="color:purple;">object|void</mark>
