# 🤖 New Client properties

## Client.user

### Client.user has every information of the logged bot.

It includes: id, botID, username, createdAt & createdBy properties.

[More information about types, here.](../../../documentation/types/userclienttypes.md)

```typescript
console.log(client.user.id) // Output: 123456789 (your logged bot's user id)
```

```typescript
console.log(client.user.botID) // Output: 123456789 (your logged bot id)
```

```typescript
client.on('ready', ()=> {
   console.log('Logged as', client.user.username);
})

// Now you can console.log the username of the bot when logged in.
```

```typescript
console.log(client.user.createdAt) // Will output a number in unix epoch time.
```

```typescript
console.log(client.user.createdBy) 
// Output: '4kR9QRVA' (will output the user id of the bot's owner)
```
