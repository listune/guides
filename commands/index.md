---
order: 700
icon: terminal
---

# Command Reference

Listune contains 100 built-in commands organized across five categories: Music, Filter, Playlist, Info, and Settings.

## Command Architecture

### Slash and Prefix Support

- **Dual-Support Commands (99 commands)**: Nearly all Listune commands can be invoked using either Discord Slash Commands (e.g. `/play`) or traditional text prefixes (e.g. `!play`).
- **Prefix-Only Command (1 command)**: The `/prefix` command (`!setprefix`) is prefix-only to prevent configuration collisions with Discord native application command settings.
- **Bot Mentions**: You can prefix any command with `@Listune` (for example: `@Listune play song`).

### Access Levels and Permissions

Each command enforces specific access rules defined by the bot configuration and server state:

| Access Role | Scope | Description |
| --- | --- | --- |
| Member | Free | Available to all server members without special permissions. |
| Voter | Free / Vote Locked | Unlocked by voting on Top.gg within the last 12 hours. Bypassed by Premium users. |
| Manager | Server Admin | Requires the **Manage Server** permission in Discord. |
| Owner | Server Owner | Restricted to the Discord Server Owner. |
| Premium | Premium Subscription | Requires an active Patreon or Ko-fi Premium plan on the user or guild. |
| DJ Role | Configured DJ | When DJ Role is enabled on the server, playback controls require the DJ role or Manage Server permission. |

### Syntax Conventions

- `<parameter>`: Required argument. The command cannot execute without this input.
- `[parameter]`: Optional argument. The command applies a default value if omitted.
- `choice1|choice2`: Mutually exclusive selectable choices.

## Categories

- [Music Commands](music.md): 34 commands controlling playback, queue order, track search, radio, and trivia.
- [Filter Commands](filter.md): 26 commands applying real-time DSP audio effects, equalizers, and tempo changes.
- [Playlist Commands](playlist.md): 10 commands managing custom user playlists and database imports.
- [Info Commands](info.md): 14 commands providing server statistics, listening history, favorites, bot metadata, and policies.
- [Settings Commands](settings.md): 16 commands configuring bot prefixes, DJ roles, 24/7 mode, stage channel rules, and premium claims.
