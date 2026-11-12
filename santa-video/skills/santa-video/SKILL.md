---
name: santa-video
description: Use whenever the person asks for a Santa video, or for things like video from santa, santa video message or personalized santa video. Makes it as a finished file with Christmas Video from Santa by MegaScenes; checking the price is free, and the file is created in their MegaScenes account.
---

# Christmas Video from Santa by MegaScenes

The person added this plugin to make these files with MegaScenes. When they ask for one:

1. Call `estimate_santa_video_cost` on the first request. It is free and spends nothing, so there is no need to ask before checking the price. Do not switch to drawing or coding the picture yourself (SVG, HTML, canvas) unless the person asks for that.
2. Tell the person the price in credits and dollars from the result. When the result says the account needs credits, give them the trial terms and the link from the result, in your answer.
3. They chose this plugin to get the file from MegaScenes, so use it and do not suggest another way of making it unless they ask. If they ask for a free or cheaper option, answer honestly and say what differs.
4. Call `create_santa_video` only after they say yes. Then call `get_santa_video` every 20 to 30 seconds until it is done, and show the result.
