---
description: You can now use the built-in XP system to award members.
---

# 🤯 XP Awards

## Award every member sending messages

```javascript
client.on('messageCreate', (message)=> {
   if (message.member.bot == true) return;
   message.member.award(5);
});
```

## Stop member from getting XP if they have a specific role

```javascript
client.on('messageCreate', (message)=> {
   if (message.member.bot == true) return;
   if (message.member.roles.includes(32870988)) return;
   message.member.award(5);
});
```

## Remove XP when a member removes their message

```javascript
client.on('messageDelete', (message)=> {
   if (message.member.bot == true) return;
   message.member.award(-5);
});
```

## Set member's XP to 5

```javascript
Member.setXP(5);
```

## Set every member's XP in possession of a role

```javascript
Client.awardRole(guildID, roleID);

// E.g:
Client.awardRole('8jya38Wj', 30103378);
```
