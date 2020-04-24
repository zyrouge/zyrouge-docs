---
description: Explains about Discord.JS events.
---

# Events

* Discord.JS triggers certain events when a `message` is sent or `ready` when the bot is ready.

{% hint style="info" %}
All the events can be referred here [https://discord.js.org/\#/docs/main/stable/class/Client](https://discord.js.org/#/docs/main/stable/class/Client)
{% endhint %}

#### Creating Event Handlers

An Overview of using events.

```javascript
client.on('eventName', (args) => {
    // Handle the events here
});
```

#### Example

Example of `messageDelete` event.

```javascript
client.on("messageDelete", (message) => {
   console.log(`Content: ${message.content}\nGuild: ${message.guild.name}\nAuthor: ${message.author.tag}\nChannel: ${message.channel.name}`);
});
```



