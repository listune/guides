---
order: 650
icon: gear
---

# Settings Commands

Listune provides 16 server administration, configuration, and premium management commands.

## Summary Table

| Command | Type | Aliases | Access | Description |
| --- | --- | --- | --- | --- |
| `/247` | Slash & Prefix | None | Manager / Premium | Keeps Listune connected to your voice channel 24/7. |
| `/aichat` | Slash & Prefix | `ai` | Voter / Manager | Configures or removes the dedicated AI Music Assistant channel. |
| `/customize` | Slash & Prefix | `customization` | Manager / Premium | Customizes the bot server-specific nickname, bio, avatar, and banner. |
| `/djrole` | Slash & Prefix | None | Manager | Enables, sets, or disables the DJ role requirement for music controls. |
| `/language` | Slash & Prefix | `lang` | Owner / Manager | Changes the language used for bot messages and embeds. |
| `/lastfm` | Slash & Prefix | None | Member | Connects or disconnects your Last.fm profile for automatic track scrobbling. |
| `/player control` | Slash & Prefix | None | Manager | Configures player embed controls, button visibility, and filter menus. |
| `!prefix` | Prefix Only | `!setprefix` | Manager | Updates the text command prefix for this server. |
| `/premium claim` | Slash & Prefix | `pclaim`, `claim` | Member | Activates a Premium server slot using your linked Patreon or Ko-fi account. |
| `/premium unclaim` | Slash & Prefix | `punclaim`, `unclaim` | Member | Releases a Premium server slot so it can be used on another server. |
| `/set channel` | Slash & Prefix | None | Manager | Restricts bot commands to specific designated text channels. |
| `/setup` | Slash & Prefix | None | Manager | Creates a dedicated song-request channel with live player controls. |
| `/stage control` | Slash & Prefix | None | Manager | Configures permissions for stage voice channels and speaker requests. |
| `/status voicechannel`| Slash & Prefix | `svc` | Manager | Toggles updating the voice channel name with the currently playing track. |
| `/tempvoice` | Slash & Prefix | `tvn` | Manager | Sets up auto-generating temporary voice channels for community members. |
| `/themes` | Slash & Prefix | None | Manager | Sets the default canvas music card theme for the server. |

## Detailed Configuration Reference

### `/247`
- **Syntax**: `/247 mode:<enable|disable>` or `!247 <enable|disable>`
- **Requirements**: User must be connected to a voice channel. Requires the **Manage Server** permission and an active Premium plan.
- **Notes**: Prevents the bot from ever leaving the voice channel due to inactivity or empty channels.

### `/djrole`
- **Syntax**: `/djrole action:<enable|disable|set|reset> [role:<role>]` or `!djrole <enable|disable|set|reset> [@role]`
- **Requirements**: Manage Server permission.
- **Notes**: When enabled, general members without this role cannot skip, pause, adjust volume, or alter filters unless they are the original track requester. Server administrators always bypass DJ role restrictions.

### `!prefix`
- **Syntax**: `!prefix <new_prefix>` or `!setprefix <new_prefix>`
- **Requirements**: Manage Server permission.
- **Type**: Prefix Only (Max length: 10 characters).
- **Notes**: Changes the command prefix for the current guild. You can also change the prefix anytime through the Web Dashboard.

### `/premium claim` and `/premium unclaim`
- **Syntax**: `/premium claim platform:<patreon|kofi> [transaction_id:<id>]`
- **Syntax**: `/premium unclaim platform:<patreon|kofi>`
- **Requirements**: Member.
- **Notes**: Links your Patreon or Ko-fi supporter quota to the current server. If you leave the server or want to transfer perks to a different community, use `/premium unclaim` to restore your available quota immediately.

### `/setup`
- **Syntax**: `/setup action:<create|delete>` or `!setup <create|delete>`
- **Requirements**: Manage Channels and Manage Server permissions.
- **Notes**: Automatically creates a dedicated text channel pinned with a persistent music player card and interactive buttons. Users can type song titles directly into this channel without any prefix to queue them immediately.
