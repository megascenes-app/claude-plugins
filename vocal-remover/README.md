# Vocal Remover

Vocal remover: split a song from your MegaScenes library into the instrumental and the vocals, two files for karaoke, covers, practice and remixes, or into six stems.

## What it does
Pick a song from your MegaScenes library. Claude tells you the price, which follows the length of the song, and returns the instrumental and the vocals as two files, or six stems (vocals, drums, bass, guitar, piano and the rest) if you ask.

**How the files are made:** each split is made by a source separation model that MegaScenes runs through its model providers: it separates the parts of your track and composes nothing new. Nothing is made until you say yes, and the price in credits comes first.

For your own songs and tracks you have the right to use.

## Install
In Claude Code:
```
/plugin marketplace add megascenes-app/claude-plugins
/plugin install vocal-remover@megascenes
```

## Connecting
- Vocal Remover talks to the MegaScenes server at `https://megascenes.com/api/claude/vocal-remover/mcp` (Streamable HTTP).
- Connecting opens MegaScenes: sign in, create an account, or continue without one and add your email when you pay (OAuth with PKCE). Then you come straight back to the chat.
- Each vocal split uses credits from your MegaScenes account and is priced before it runs; new accounts can start with a low-cost trial week.
- The files play in a viewer in the chat where Claude supports interactive apps; in Claude Code you get the links.

## Tools
| Tool | What it does |
|---|---|
| `list_vocal_split_models` | Models for vocal splits with settings and starting prices. Read-only. |
| `estimate_vocal_split_cost` | Exact price of one vocal split before it runs. Read-only. |
| `create_vocal_split` | Starts one vocal split in your account. Uses credits; needs sign-in. |
| `get_vocal_split` | Status and file links. Read-only. |
| `list_my_media` | Your recordings and tracks, uploads and files made here, with their length, to pick the one to start from. Read-only. |
| `get_account` | Your plan and credit balance. Read-only. |

## Example prompts
- "Remove the vocals from my latest MegaScenes song"
- "Make a karaoke version of my last track"
- "Split my latest song into drums, bass and vocals"

## Data and privacy
What you give for the vocal split (the song you pick from your library) goes to MegaScenes, stays in your MegaScenes account with the finished file, and is passed to the model provider that makes it. The plugin has no hooks or local scripts and sends nothing else.
- Privacy policy: https://megascenes.com/legal/privacy
- Terms of service: https://megascenes.com/legal/terms
- Documentation: https://megascenes.com/connectors#claude
- Support: https://megascenes.com/support
