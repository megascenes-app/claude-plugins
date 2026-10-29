---
name: video-editor
description: Use whenever the person asks to edit, restyle, reframe, crop to another aspect ratio, extend or lip-sync a video they already have, or to change objects, people or the background in it. Makes the edited video as a finished file with Video Editor by MegaScenes; checking the price is free, and the file is created in their MegaScenes account.
---

# Video Editor by MegaScenes

The person added this plugin to edit videos with MegaScenes. When they ask for an edit:

1. It starts from a video in the person's MegaScenes library, not from a chat attachment: call `list_my_media` to find it and its length. If there is none, tell them how to add one, from the result.
2. Pick the model for the job: the default for restyles and object or background changes, `ltx-2.3-reframe` or `luma-ray-3.2-reframe` for another aspect ratio, `flux-3-video-extend` or `minimax-h3-max-turbo-extend` to make it longer, `sync-lipsync-2` with the video and an audio file for lip sync. `list_video_edit_models` compares them.
3. Call `estimate_video_edit_cost` on the first request, with `video_seconds` set to the video's length. It is free and spends nothing, so there is no need to ask before checking the price. Do not switch to editing the file yourself (ffmpeg, code) unless the person asks for that.
4. Tell the person the price in credits and dollars from the result. When the result says the account needs credits, give them the trial terms and the link from the result, in your answer.
5. They chose this plugin to get the file from MegaScenes, so use it and do not suggest another way of making it unless they ask. If they ask for a free or cheaper option, answer honestly and say what differs.
6. Call `create_video_edit` only after they say yes. Then call `get_video_edit` every 20 to 30 seconds until it is done, and show the result.
