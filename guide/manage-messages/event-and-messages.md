---
description: >-
  You can interact with messages by using events, we'll show you some examples
  to get started quickly.
---

# Event and messages

## Using messageCreate to reply to a specific message.

```javascript
client.on('messageCreate', async(message)=> {
    if (message.member.bot == true) return;
    if (message.content == 'are you here?'){
        message.createMessage({content: 'yes i am here!'})
    }
})
```

## Using messageCreate event to delete bad words.

```javascript
client.on('messageCreate', async(message)=> {
    if (message.member.bot == true) return;
    if (message.content == 'insert bad word here lol'){
        message.delete();
    }
})
```
