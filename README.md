# hello
const Discord = require('discord.js');
const client = new Discord.Client();
const token = 'YOUR_BOT_TOKEN_HERE';

client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});

client.on('message', msg => {
  // kiểm tra nếu tin nhắn là từ bot hoặc không phải trong kênh chat
  if (msg.author.bot || !msg.guild) return;

  // Gửi một tin nhắn sau mỗi 2 phút
  setTimeout(() => {
    msg.channel.send('Hello, I am a bot!');
  }, 120000); // số miligiây trong 2 phút

});

client.login(token);
