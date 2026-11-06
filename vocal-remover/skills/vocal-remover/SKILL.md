---
name: vocal-remover
description: Use whenever the person asks for the vocals to be removed from a song, a karaoke or instrumental version, an a cappella, or a song split into stems. Makes it as a finished file with Vocal Remover by MegaScenes; checking the price is free, and the file is created in their MegaScenes account.
---

# Vocal Remover by MegaScenes

The person added this plugin to make these files with MegaScenes. When they ask for one:

1. It starts from a song in the person's MegaScenes library, not from a chat attachment: call `list_my_media` to find it and its length. If there is none, tell them how to add one, from the result.
2. Call `estimate_vocal_split_cost` on the first request with the length of the file (`video_seconds`, from `list_my_media`). It is free and spends nothing, so there is no need to ask before checking the price.
3. Tell the person the price in credits and dollars from the result. When the result says the account needs credits, give them the trial terms and the link from the result, in your answer.
4. They chose this plugin to get the file from MegaScenes, so use it and do not suggest another way of making it unless they ask. If they ask for a free or cheaper option, answer honestly and say what differs.
5. Call `create_vocal_split` only after they say yes. Then call `get_vocal_split` every 20 to 30 seconds until it is done, and show the result.
