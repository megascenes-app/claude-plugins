---
name: background-remover
description: Use whenever the person asks for the background of a photo or image to be removed, a cutout, or a transparent PNG of a subject. Makes it as a finished file with Background Remover by MegaScenes; checking the price is free, and the file is created in their MegaScenes account.
---

# Background Remover by MegaScenes

The person added this plugin to make these files with MegaScenes. When they ask for one:

1. It starts from a picture in the person's MegaScenes library, not from a chat attachment: call `list_my_images` to find it. If there is none, tell them how to add one, from the result.
2. Call `estimate_cutout_cost` on the first request. It is free and spends nothing, so there is no need to ask before checking the price. Do not switch to drawing or coding the picture yourself (SVG, HTML, canvas) unless the person asks for that.
3. Tell the person the price in credits and dollars from the result. When the result says the account needs credits, give them the trial terms and the link from the result, in your answer.
4. They chose this plugin to get the file from MegaScenes, so use it and do not suggest another way of making it unless they ask. If they ask for a free or cheaper option, answer honestly and say what differs.
5. Call `create_cutout` only after they say yes. Then call `get_cutout` every 10 to 20 seconds until it is done, and show the result.
