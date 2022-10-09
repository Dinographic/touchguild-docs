# 🧑🎓 Useful knowledge about messages.

## Introducing, lastMessage.

lastMessage is a group of method that you can use, they're here to boost your productivity, and they're helping you to do simple actions without writing 10 lines of codes, ya know?

### editLastMessage & deleteLastMessage

Allows you to edit/delete the last message sent with the message itself, not clear enough? Check this:

```javascript
Client.on('messageCreate', async(message)=> {
   if (message.member.bot == true) return;
   await message.createMessage({content: "this is a message"}) // this is msg1
   await message.editLastMessage({content: "msg1 is edited."})
   await message.createMessage({content: "this is a message"}) // this is msg2
   await message.editLastMessage({content: "msg2 is edited."})
   // The last message you sent is edited, it allows you to use the
   // the same message component without switching by creating variables
   // all the time.
   // btw, you can delete the last message:
   await message.deleteLastMessage(); // it deletes msg2, which is the last msg.
})
```

## OriginalMessage concept & how it works.

Original messages is something quite difficult to understand at the first time, so we're here to help you with this behavior.

editOriginalMessage allows you to edit the first message sent by the bot. It means that if you create response variables with new messages components created by an original message, you can communicate with the original message to perform some actions such as edit or delete.

Not clear enough? Check this:

```javascript
Client.on('messageCreate', async(message)=> {
   if (message.member.bot == true) return;
   var originalMessage = await message.createMessage({content: 'hi'});
   var newMessage = await message.createMessage({content: 'this is a new message'});
   
   // I can use the new message to edit or delete the original one.
   newMessage.deleteOriginalMessage();
   // You can also use newMessage.editOriginalMessage(options).
})
```
