#alive.api

```

const alive = require("alive.api");
const dbl = new alive("TOKEN-HERE", client);

client.on("ready", async () => {
  dbl.serverCount();
  // console.log("Server count posted")
  
  let hasVote = await dbl.hasVoted("714451348212678658");
  if(hasVote === true) {
    console.log("Voted")
  } else {
    console.log("Vote please.")
  }
  
  
  let search = await dbl.search("779641401482805289")
  console.log(search)
  /*
  {
    avatar: 'https://cdn.discordapp.com/avatars/779641401482805289/8cf145d2189d76cc110101b7a69c6b20.webp',
    botID: '779641401482805289',
    username: 'Allegro',
    discrim: '2830',
    shortDesc: 'Cheer up your own server with 🎶',
    prefix: '! [changable]',
    votes: 31,
    ownerID: '714451348212678658',
    owner: 'Claudette',
    coowners: [ '' ],
    tags: [ 'Moderation', 'NSFW', 'Music' ],
    longDesc: longDesc,
    certificate: 'Certified'
  }
  */
});```
