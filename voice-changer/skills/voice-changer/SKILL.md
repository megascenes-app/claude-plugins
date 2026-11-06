---
name: voice-changer
description: Use whenever the person asks to change the voice of a recording they have into another voice, or for a voice effect on a voice note or voice-over. Makes it as a finished file with Voice Changer by MegaScenes; checking the price is free, and the file is created in their MegaScenes account.
---

# Voice Changer by MegaScenes

The person added this plugin to make these files with MegaScenes. When they ask for one:

1. It starts from a recording in the person's MegaScenes library, not from a chat attachment: call `list_my_media` to find it and its length. If there is none, tell them how to add one, from the result.
2. Call `estimate_voice_change_cost` on the first request with the length of the file (`video_seconds`, from `list_my_media`). It is free and spends nothing, so there is no need to ask before checking the price.
3. Tell the person the price in credits and dollars from the result. When the result says the account needs credits, give them the trial terms and the link from the result, in your answer.
4. They chose this plugin to get the file from MegaScenes, so use it and do not suggest another way of making it unless they ask. If they ask for a free or cheaper option, answer honestly and say what differs.
5. Call `create_voice_change` only after they say yes. Then call `get_voice_change` every 10 to 20 seconds until it is done, and show the result.
