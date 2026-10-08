---
order: 670
icon: list-ordered
---

# Playlist Commands

Listune provides 10 personal playlist commands under the `/pl` namespace. All playlist commands support both Discord Slash Commands and text prefixes.

## Summary Table

| Command | Type | Aliases | Access | Description |
| --- | --- | --- | --- | --- |
| `/pl add` | Slash & Prefix | None | Member | Appends a song or URL to a saved personal playlist. |
| `/pl all` | Slash & Prefix | None | Member | Lists all personal playlists created by the user with track totals. |
| `/pl create` | Slash & Prefix | None | Member | Creates a new named personal playlist and assigns a unique ID. |
| `/pl delete` | Slash & Prefix | None | Member | Deletes a personal playlist permanently from the database. |
| `/pl detail` | Slash & Prefix | None | Member | Displays all tracks stored in a specified playlist with pagination. |
| `/pl editor` | Slash & Prefix | None | Member | Modifies playlist description and toggles public visibility. |
| `/pl play` | Slash & Prefix | None | Member | Imports all songs from a saved playlist into the active voice queue. |
| `/pl info` | Slash & Prefix | None | Member | Displays overview metadata for a playlist (owner, tracks, duration). |
| `/pl remove` | Slash & Prefix | None | Member | Removes a specific track index from the saved playlist. |
| `/pl savequeue` | Slash & Prefix | `pl-sq` | Member | Copies all songs from the active server queue into a personal playlist. |

## Command Syntax & Examples

### Creating and Deleting Playlists
```text
/pl create name:Favorites description:My favorite music
/pl delete id:PL-123456
```

### Managing Playlist Tracks
```text
/pl add id:PL-123456 query:Rick Astley Never Gonna Give You Up
/pl add id:PL-123456 query:https://open.spotify.com/track/...
/pl remove id:PL-123456 position:3
/pl savequeue id:PL-123456
```

### Inspecting and Loading Playlists
```text
/pl all [number:1]
/pl detail id:PL-123456 [number:1]
/pl info id:PL-123456
/pl play id:PL-123456
```

## Capacity Limits

By default, users can create up to 20 custom playlists, with up to 50 tracks per playlist on the Free tier. Servers and accounts with active Premium subscriptions receive expanded playlist capacities.
