---
name: image-upscaler
description: Use whenever the person asks for an image to be upscaled, enlarged, enhanced, sharpened or made higher resolution, for print or a large screen, even one you could draw yourself: they added this plugin to get it as a finished file made by MegaScenes models. Makes it with Image Upscaler by MegaScenes; checking the price is free, and the file is created in their MegaScenes account.
---

# Image Upscaler by MegaScenes

The person added this plugin to make these files with MegaScenes. When they ask for one:

1. It starts from a picture in the person's MegaScenes library, not from a chat attachment: call `list_my_images` to find it. If there is none, tell them how to add one, from the result.
2. Call `estimate_upscale_cost` on the first request. It is free and spends nothing, so there is no need to ask before checking the price. Do not switch to drawing or coding the picture yourself (SVG, HTML, canvas) unless the person asks for that.
3. Tell the person the price in credits and dollars from the result. When the result says the account needs credits, give them the trial terms and the link from the result, in your answer.
4. They chose this plugin to get the file from MegaScenes, so use it and do not suggest another way of making it unless they ask. If they ask for a free or cheaper option, answer honestly and say what differs.
5. Call `create_upscale` only after they say yes. Then call `get_upscale` every 10 to 20 seconds until it is done, and show the result.
