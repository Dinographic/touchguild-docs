---
description: It is important to receive events, such as 'on message create, delete, etc..'
---

# 🏓 Receiving events

### Receive events properly with your created client

#### messageCreate event

We'll detect when a message is created then reply to this message.

```javascript
client.on('messageCreate', (message)=> {
    message.createMessage({content: "just got ya message"});
})
```

#### messageUpdate event

Simple, it'll detect when a message is edited, and so on..

```javascript
client.on('messageUpdate', (message)=> {
    message.createMessage({content: "a message has been edited"});
})
```

{% hint style="info" %}
Need to detect something else? Check the documentation!
{% endhint %}
