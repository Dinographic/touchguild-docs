---
description: Learn more about your bot's user.
---

# 🎰 Get bot's information

## Log bot's username when ready.

```javascript
client.on('ready', ()=> {
   console.log('Logged as', client.user.username);
});
```

## Log every information about the logged bot.

```javascript
client.on('ready', ()=> {
   console.log(client.user);
});
```

Output (example):

<pre class="language-json"><code class="lang-json"><strong>UserClient {
</strong>  _client: Client,
  id: "AQbXpB84",
  botID: "c06b6d42-05db-4af7-8a28-faae65b53e7a",
  type: "bot",
  username: "touchguild testing bot",
  _createdAt: 1666429419806,
  createdBy: "4kR9QRVA"
}</code></pre>

You can use the information like the one above to do whatever you want with it.
