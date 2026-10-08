---
order: 780
icon: rows
---

# Queue & Playlists

Listune provides tools for managing the active voice channel queue and maintaining persistent personal playlists.

## Queue Management Commands

The server queue holds upcoming tracks in sequence. Listeners can inspect, reorder, clean up, and navigate through upcoming songs.

| Command | Syntax | Description |
| --- | --- | --- |
| `/queue` | `/queue [page]` | Displays upcoming songs with duration, title, and requester information. |
| `/shuffle` | `/shuffle` | Randomizes the sequence of upcoming tracks in the queue. |
| `/loop` | `/loop mode:<current\|all\|disable>` | Toggles repeat mode between single track loop, full queue loop, or disabled. |
| `/remove` | `/remove position:<number>` | Removes a single song at the specified queue index. |
| `/removedupes` | `/removedupes` | Scans the queue and removes duplicate tracks matching the same URI or title. |
| `/removetracks` | `/removetracks requester:<user>` | Batch removes all tracks requested by a specific server member. |
| `/clearqueue` | `/clearqueue` | Clears all upcoming tracks from the queue while keeping the active track playing. |
| `/playnext` | `/playnext search:<query>` | Inserts a track at the very top of the queue so it plays immediately after the current song. |
| `/skipto` | `/skipto position:<number>` | Skips directly to a specified track number in the queue, discarding preceding songs. |
| `/replay` | `/replay` | Restarts the current track from 0:00. |
| `/grab` | `/grab` | Sends current track metadata to your Direct Messages with a button to add it to your Favorites. |
| `/sleeptimer` | `/sleeptimer` | Opens an interactive modal to schedule playback stoppage after up to 120 minutes. |

## Personal Playlists

Every user can store personal playlists in the Listune database. These playlists persist across servers and can be loaded into any voice channel where you have command access.

### Playlist Command Directory

All custom playlist commands share the `/pl` root prefix:

- `/pl create name:<name> description:<description>`: Creates a new personal playlist and generates a unique playlist identifier.
- `/pl add id:<playlist_id> query:<url_or_name>`: Appends a track or URL to the designated playlist.
- `/pl remove id:<playlist_id> position:<number>`: Deletes a specific track entry from the playlist.
- `/pl all [page:<number>]`: Displays all playlists you own, including total track counts and creation dates.
- `/pl detail id:<playlist_id> [page:<number>]`: Lists every track stored inside the playlist with track lengths.
- `/pl play id:<playlist_id>`: Enqueues and begins playing the saved playlist in your current voice channel.
- `/pl savequeue id:<playlist_id>`: Snapshots all tracks in the active server queue and copies them into your personal playlist.
- `/pl editor id:<playlist_id>`: Adjusts public visibility and metadata for the playlist.
- `/pl delete id:<playlist_id>`: Permanently removes the playlist from the database.

## Favorites and Listening History

Listune tracks personal favorites and listening sessions independently:

- **Favorites (`/favorites`)**: View, play, or delete songs saved to your liked tracks collection. Songs can be added directly from Discord Components V2 buttons on player cards or via the `/grab` command.
- **History (`/history`)**: Displays recently played tracks with options to re-queue them instantly or add them to your saved playlists.
