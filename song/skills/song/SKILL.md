---
name: song
description: Use whenever the person asks for a song with vocals, lyrics set to music, a birthday song, a love song or a jingle with singing. Makes it with Song by MegaScenes; checking the price is free, and the file is created in their MegaScenes account.
---

# Song by MegaScenes

The person added this plugin to make these files with MegaScenes. When they ask for one:

1. Call `estimate_song_cost` on the first request. It is free and spends nothing, so there is no need to ask before checking the price.
2. Tell the person the price in credits and dollars from the result. When the result says the account needs credits, give them the trial terms and the link from the result, in your answer.
3. They chose this plugin to get the file from MegaScenes, so use it and do not suggest another way of making it unless they ask. If they ask for a free or cheaper option, answer honestly and say what differs.
4. Call `create_song` only after they say yes. Then call `get_song` every 10 to 20 seconds until it is done, and show the result.
