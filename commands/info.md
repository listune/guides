---
order: 660
icon: info
---

# Info Commands

Listune provides 14 information and community commands. All info commands support both Discord Slash Commands and text prefixes.

## Summary Table

| Command | Type | Aliases | Access | Description |
| --- | --- | --- | --- | --- |
| `/about` | Slash & Prefix | None | Member | Displays bot origin, lead developer, version, and official web links. |
| `/favorites` | Slash & Prefix | `fav`, `likes` | Member | Opens your personal collection of liked tracks with quick-play buttons. |
| `/global stats` | Slash & Prefix | `glstats` | Member | Displays ecosystem statistics across all servers, top global artists, and tracks. |
| `/guild stats` | Slash & Prefix | `gstats` | Member | Renders the server-specific top 10 played songs and top 10 played artists. |
| `/help` | Slash & Prefix | `h` | Member | Shows the complete command directory or detailed syntax for a specific command. |
| `/history` | Slash & Prefix | `hist`, `recent` | Member | Lists recently played songs with options to re-queue them instantly. |
| `/info` | Slash & Prefix | `stats`, `bs` | Member | Reports system runtime statistics: RAM usage, cluster uptime, nodes, and ping. |
| `/invite` | Slash & Prefix | `inv`, `addbot` | Member | Provides official OAuth2 invite URLs for Listune and its multi-bot instances. |
| `/privacy policy` | Slash & Prefix | `pp`, `priv` | Member | Displays the official Listune Privacy Policy summary and full documentation link. |
| `/profile` | Slash & Prefix | `pr` | Member | Displays a personalized card of user statistics, favorite tracks, and listening time. |
| `/rating` | Slash & Prefix | None | Member | Submits a star rating and review to help improve Listune. |
| `/report` | Slash & Prefix | None | Member | Submits a bug report directly to the official support server channels. |
| `/suggestions` | Slash & Prefix | `suggest`, `sgt` | Member | Submits a feature suggestion to the development team. |
| `/terms of services` | Slash & Prefix | `terms`, `tos` | Member | Displays the official Listune Terms of Service summary and full link. |

## Highlighted Commands

### `/help`
- **Syntax**: `/help [command:<name>]` or `!help [command]`
- **Notes**: Invoking `/help` without arguments presents an interactive categorized menu (Music, Filter, Playlist, Info, Settings). Specifying a command name displays exact argument requirements, aliases, and permissions.

### `/guild stats`
- **Syntax**: `/guild stats` or `!guildstats` (alias: `!gstats`)
- **Notes**: Pulls server-level historical records from the database, displaying:
  - Total tracks played in the guild
  - Cumulative listening time (days, hours, minutes)
  - Top 10 most played songs
  - Top 10 most played artists

### `/profile`
- **Syntax**: `/profile [user:<user>]` or `!profile [@user]`
- **Notes**: Generates an interactive profile card for yourself or another server member showing total listening duration, number of liked tracks, created playlists, and favorite genre.
