client.on("message", (message) => {
  if (message.content.startsWith("add")) {
    if(message.author.bot) return;
    db1.ensure("Ahmed", {
      Guildid: [],
      Message: "",
      Channelid: []

    })
    const mess = message.content.split(" ").slice('1');
     db1.set("Ahmed" , mess , "Message")
     const gg = db1.get("Ahmed" , "Message")
    message.reply(`Done added ${gg}`)


  }
})


client.on("message", (message) => {
if (message.content.startsWith("ch")){
  if(message.author.bot) return ; 


    db1.ensure("Ahmed", {
      Guildid: [],
      Message: "",
      Channelid: []

    })
    const channel = message.mentions.channels.first()
    if(!channel) return message.reply({content : `you need to mention first`})

    db1.set ("Ahmed" , channel , "Channelid")
    const dd = db1.get ("Ahmed" , "Channelid")
    message.reply(`Done ${dd}`)



}
})




client.on("guildMemberAdd", (member , message) => {

const kk = db1.get("Ahmed" , "Channelid")
 const hh = db1.get("Ahmed" , "Message")
 let channel = client.channels.cache.get(kk)
  message = hh.content;

channel.send(`${hh} ${member.id}`)





})
