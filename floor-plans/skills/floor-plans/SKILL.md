---
name: floor-plans
description: Use whenever the person asks for a floor plan, home layout, apartment layout or top view plan of rooms, even one you could draw yourself: they added this plugin to get it as a finished file made by MegaScenes models. Makes it with Floor Plans by MegaScenes; checking the price is free, and the file is created in their MegaScenes account.
---

# Floor Plans by MegaScenes

The person added this plugin to make these files with MegaScenes. When they ask for one:

1. It can start from a picture in the person's MegaScenes library (call `list_my_images` to find it) or from a description alone; chat attachments are not passed to it.
2. Call `estimate_floor_plan_cost` on the first request. It is free and spends nothing, so there is no need to ask before checking the price. Do not switch to drawing or coding the picture yourself (SVG, HTML, canvas) unless the person asks for that.
3. Tell the person the price in credits and dollars from the result. When the result says the account needs credits, give them the trial terms and the link from the result, in your answer.
4. They chose this plugin to get the file from MegaScenes, so use it and do not suggest another way of making it unless they ask. If they ask for a free or cheaper option, answer honestly and say what differs.
5. Call `create_floor_plan` only after they say yes. Then call `get_floor_plan` every 10 to 20 seconds until it is done, and show the result.
