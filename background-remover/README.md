# Background Remover

Background remover: cut the subject out of a photo or image from your MegaScenes library and get it on a transparent PNG, for product shots, stickers, profile pictures and designs.

## What it does
Pick an image from your MegaScenes library. Claude tells you the price, then cuts out the main subject and returns it on a transparent background. Nothing is repainted or added.

**How the files are made:** each cutout is made by a background removal model that MegaScenes runs through its model providers: it keeps the pixels of your subject and draws nothing new. Nothing is made until you say yes, and the price in credits comes first.

Starts from an image in your MegaScenes library: files attached in the chat are not passed to the plugin.

## Install
In Claude Code:
```
/plugin marketplace add megascenes-app/claude-plugins
/plugin install background-remover@megascenes
```

## Connecting
- Background Remover talks to the MegaScenes server at `https://megascenes.com/api/claude/background-remover/mcp` (Streamable HTTP).
- Connecting opens MegaScenes: sign in, create an account, or continue without one and add your email when you pay (OAuth with PKCE). Then you come straight back to the chat.
- Each cutout uses credits from your MegaScenes account and is priced before it runs; new accounts can start with a low-cost trial week.
- The cutouts show in a viewer in the chat where Claude supports interactive apps; in Claude Code you get the links.

## Tools
| Tool | What it does |
|---|---|
| `list_cutout_models` | Models for cutouts with settings and starting prices. Read-only. |
| `estimate_cutout_cost` | Exact price of one cutout before it runs. Read-only. |
| `create_cutout` | Starts one cutout in your account. Uses credits; needs sign-in. |
| `get_cutout` | Status and file links. Read-only. |
| `list_my_images` | Your uploads and images made here, to pick the one to start from. Read-only. |
| `get_account` | Your plan and credit balance. Read-only. |

## Example prompts
- "Remove the background from my latest MegaScenes image"
- "Which of my images can I cut out?"
- "Make a transparent PNG of my most recent product photo"

## Data and privacy
What you give for the cutout (the image you pick from your library) goes to MegaScenes, stays in your MegaScenes account with the finished file, and is passed to the model provider that makes it. The plugin has no hooks or local scripts and sends nothing else.
- Privacy policy: https://megascenes.com/legal/privacy
- Terms of service: https://megascenes.com/legal/terms
- Documentation: https://megascenes.com/connectors#claude
- Support: https://megascenes.com/support
