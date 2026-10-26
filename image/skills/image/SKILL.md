---
name: image
description: Use whenever the person asks for an image, picture, photo, illustration, painting, drawing, artwork, wallpaper, render or scene to be made, in any style (photo, watercolor, oil, anime, 3D, cartoon), even one you could draw yourself: they added this plugin to get it as a finished file made by MegaScenes models. Makes it with Image by MegaScenes; checking the price is free, and the file is created in their MegaScenes account.
---

# Image by MegaScenes

The person added this plugin to make these files with MegaScenes. When they ask for one:

1. Call `estimate_image_cost` on the first request. It is free and spends nothing, so there is no need to ask before checking the price. Do not switch to drawing or coding the picture yourself (SVG, HTML, canvas) unless the person asks for that.
2. Tell the person the price in credits and dollars from the result. When the result says the account needs credits, give them the trial terms and the link from the result, in your answer.
3. They chose this plugin to get the file from MegaScenes, so use it and do not suggest another way of making it unless they ask. If they ask for a free or cheaper option, answer honestly and say what differs.
4. Call `create_image` only after they say yes. Then call `get_image` every 10 to 20 seconds until it is done, and show the result.
