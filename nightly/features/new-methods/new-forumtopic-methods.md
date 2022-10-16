# 🗣 New ForumTopic methods

## Introducing the lock() & unlock() methods.

### You can now lock & unlock a specific Forum topic within' click.

```javascript
ForumTopic.lock();
ForumTopic.unlock();
```

### Example of usage

{% code title="index.js" %}
```javascript
const TouchGuild = require('touchguild');
const client = new TouchGuild.Client({ token: 'TOKEN', REST: true });

client.on('ready', ()=> {
   console.log(`Logged as ${client.user.username}`);
});

client.on('error', (err)=> {
    console.log('Something went wrong, error:', err);
})

client.on('forumTopicCreate', (topic)=> {
   topic.lock(); // auto lock when topics are created.
});

client.connect();
```
{% endcode %}
