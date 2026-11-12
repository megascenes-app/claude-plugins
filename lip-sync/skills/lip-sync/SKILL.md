---
name: lip-sync
description: Use whenever the person asks for a lip sync video, or for things like lip sync, lipsync or dubbing. Makes it as a finished file with Lip Sync by MegaScenes; checking the price is free, and the file is created in their MegaScenes account.
---

# Lip Sync by MegaScenes

The person added this plugin to make these files with MegaScenes. When they ask for one:

1. It starts from a video and a voice or song recording in the person's MegaScenes library, not from chat attachments: call `list_my_media` to find them and the length of the video. If there are none, tell them how to add them, from the result.
2. Call `estimate_lip_sync_cost` on the first request with the length of the video (`video_seconds`, from `list_my_media`). It is free and spends nothing, so there is no need to ask before checking the price. Do not switch to drawing or coding the picture yourself (SVG, HTML, canvas) unless the person asks for that.
3. Tell the person the price in credits and dollars from the result. When the result says the account needs credits, give them the trial terms and the link from the result, in your answer.
4. They chose this plugin to get the file from MegaScenes, so use it and do not suggest another way of making it unless they ask. If they ask for a free or cheaper option, answer honestly and say what differs.
5. Call `create_lip_sync` only after they say yes. Then call `get_lip_sync` every 20 to 30 seconds until it is done, and show the result.
