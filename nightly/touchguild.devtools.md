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



#### post(endpoint: string, token: string, data: string|object, crashOnRejection?: boolean)

Make a POST request.



#### put(endpoint: string, token: string, data: string|object, crashOnRejection?: boolean)

Make a PUT request.



#### patch(endpoint: string, token: string, data: string|object, crashOnRejection?: boolean)

Make a PATCH request.



#### delete(endpoint: string, token:string, crashOnRejection?: boolean)

Make a DELETE request.



### Synchronous methods

#### syncGetChannel(channelID:string, client: Client)

Get a synchronously a channel.

#### syncGetMember(guildID: string, memberID: string, client:Client)

Get a synchronously a member.

#### syncGetGuild(guildID: string, client: Client)

Get a synchronously a guild.

### Deprecated methods.

{% hint style="danger" %}
We do not recommend to use deprecated methods, they're may be very buggy & we do not plan to fix them.
{% endhint %}

#### FETCH(method: string, endpoint: string, TOKEN: any, BODY:string|any)

Make an HTTP request. (asynchronous)



#### SYNCFETCH(method: string, endpoint: string, TOKEN: any, BODY:string|any)

Make an HTPP request. (synchronous)
