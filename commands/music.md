---
order: 690
icon: triangle-right
---

# Music Commands

Listune includes 34 music playback and queue management commands. All 34 commands support both Discord Slash Commands and text prefixes.

## Summary Table

| Command | Type | Aliases | Access | Description |
| --- | --- | --- | --- | --- |
| `/autoplay` | Slash & Prefix | None | Member | Toggles automatic playback of recommended songs when the queue finishes. |
| `/card` | Slash & Prefix | None | Member | Previews or switches the visual theme of the music player card. |
| `/clearqueue` | Slash & Prefix | None | Member | Empties all upcoming tracks from the queue without stopping the current track. |
| `/fix` | Slash & Prefix | `repair` | Member | Launches audio diagnostic tools to fix lag, switch voice region, or recreate player. |
| `/forcejoin` | Slash & Prefix | `fj` | Member | Forces the bot to connect to the user voice channel. |
| `/forward` | Slash & Prefix | None | Member | Skips ahead 10 seconds in the currently playing track. |
| `/grab` | Slash & Prefix | `save`, `yoink` | Member | Delivers current song details and an Add to Favorites button to your Direct Messages. |
| `/join` | Slash & Prefix | `j` | Member | Summons the bot into your current voice channel. |
| `/leave` | Slash & Prefix | `dc`, `disconnect` | Member | Disconnects the bot from voice and destroys the player session. |
| `/loop` | Slash & Prefix | None | Member | Cycles repeat mode between current song, entire queue, or disabled. |
| `/lyrics` | Slash & Prefix | `ly` | Member | Fetches and displays lyrics for the currently playing track. |
| `/music trivia` | Slash & Prefix | `mt`, `musictrivia` | Member | Launches an interactive multi-round music guessing trivia game. |
| `/nowplaying` | Slash & Prefix | `np` | Member | Displays live playback progress, duration, requester, and audio source. |
| `/pause` | Slash & Prefix | None | Member | Pauses the audio stream without dropping connection. |
| `/play` | Slash & Prefix | `p`, `pl`, `pp` | Member | Enqueues a song from search terms or direct web URLs. |
| `/playnext` | Slash & Prefix | None | Member | Pushes a track to the very front of the queue to play next. |
| `/previous` | Slash & Prefix | `pre` | Member | Replays the track that played immediately before the active song. |
| `/queue` | Slash & Prefix | `q` | Member | Shows the upcoming track list with pagination and total runtimes. |
| `/radio` | Slash & Prefix | `fm` | Member | Connects the voice channel to international live radio broadcast stations. |
| `/remove` | Slash & Prefix | `rm` | Member | Removes a single song at a specific queue position. |
| `/removedupes` | Slash & Prefix | `rmdupes`, `rd`, `cleandupes` | Member | Scans and deletes duplicate songs from the active queue. |
| `/removetracks` | Slash & Prefix | `rmtracks`, `rt` | Member | Removes all queued songs added by a specified user. |
| `/replay` | Slash & Prefix | None | Member | Restarts the current track from 0:00. |
| `/resume` | Slash & Prefix | None | Member | Resumes playback of a paused track. |
| `/rewind` | Slash & Prefix | None | Member | Rewinds playback by 10 seconds. |
| `/search` | Slash & Prefix | None | Member | Opens an interactive multi-tab browser for Songs, Artists, Albums, and Playlists. |
| `/seek` | Slash & Prefix | None | Member | Jumps directly to a specified timestamp in the active track. |
| `/shuffle` | Slash & Prefix | None | Member | Randomizes the ordering of all upcoming songs in the queue. |
| `/skip` | Slash & Prefix | None | Member | Skips the current track and starts the next queued song. |
| `/skipto` | Slash & Prefix | `sk` | Member | Jumps directly to a specific track index in the queue. |
| `/sleeptimer` | Slash & Prefix | `st`, `timer` | Member | Schedules an automatic playback stop after up to 120 minutes. |
| `/spotify` | Slash & Prefix | `sp` | Member | Connects and browses your linked Spotify library and playlists. |
| `/stop` | Slash & Prefix | None | Member | Halts audio playback, flushes the queue, and resets player state. |
| `/volume` | Slash & Prefix | `vol` | Member | Sets playback volume between 1 and 100. |

## Command Details

### `/autoplay`
- **Syntax**: `/autoplay` or `!autoplay`
- **Requirements**: Voice connection, active audio player.
- **Access**: Free (Member). When Autoplay is disabled by server managers in Guild Settings, this command is locked.
- **Notes**: Generates similar track recommendations when the current queue reaches the end. Enforces diversity controls with a limit of one track per artist.

### `/card`
- **Syntax**: `/card [theme:<name>]` or `!card [theme]`
- **Requirements**: Voice connection, active audio player.
- **Access**: Free (Member).
- **Notes**: Switches between 20 distinct visual canvas styles for now-playing track embeds.

### `/clearqueue`
- **Syntax**: `/clearqueue` or `!clearqueue`
- **Requirements**: Active queue with more than 1 song. Must share the same voice channel. DJ role restrictions apply if configured.
- **Access**: Free (Member).

### `/fix`
- **Syntax**: `/fix` or `!fix` (alias: `!repair`)
- **Requirements**: Active voice connection.
- **Access**: Free (Member).
- **Notes**: Renders an interactive diagnostic panel with three corrective actions:
  1. **Change Voice Region**: Rotates the Discord voice server RTC region to resolve routing lag.
  2. **Reconnect**: Re-establishes the voice socket connection without clearing the queue.
  3. **Recreate Player**: Re-initializes the Lavalink audio driver if the session is desynchronized.

### `/grab`
- **Syntax**: `/grab` or `!grab` (aliases: `!save`, `!yoink`)
- **Requirements**: Active playback. User must permit Direct Messages from server members in Discord privacy settings.
- **Access**: Free (Member).
- **Notes**: Sends an embed to the user Direct Messages with track metadata, artwork, source URL, and an interactive "Add to Favorites" button.

### `/play`
- **Syntax**: `/play search:<query_or_url>` or `!play <query_or_url>` (aliases: `!p`, `!pl`, `!pp`)
- **Arguments**:
  - `search` (Required, String): Song title, artist name, or direct URL.
- **Requirements**: User must be in a voice channel.
- **Access**: Free (Member). Free tier enforces a queue limit (default: 100 to 150 songs). Premium users receive expanded or unlimited queues.
- **Notes**: Supports live auto-completion inside Discord. Rejects queries made entirely of emojis.

### `/removedupes`
- **Syntax**: `/removedupes` or `!removedupes` (aliases: `!rmdupes`, `!rd`, `!cleandupes`)
- **Requirements**: Must share the same voice channel. Active queue.
- **Access**: Free (Member).
- **Notes**: Uses normalized URI and title-artist matching to strip redundant entries while preserving the first instance of each song.

### `/removetracks`
- **Syntax**: `/removetracks requester:<user>` or `!removetracks <@user>` (aliases: `!rmtracks`, `!rt`)
- **Arguments**:
  - `requester` (Required, User): The server member whose songs should be removed.
- **Requirements**: Must share the same voice channel. DJ role restrictions apply if configured.
- **Access**: Free (Member).

### `/search`
- **Syntax**: `/search query:<query>` or `!search <query>`
- **Arguments**:
  - `query` (Required, String): Search keywords.
- **Requirements**: Active voice connection.
- **Access**: Free (Member).
- **Notes**: Displays an interactive multi-tab browser with tabs for Songs, Artists, Albums, and Playlists.

### `/sleeptimer`
- **Syntax**: `/sleeptimer` or `!sleeptimer` (aliases: `!st`, `!timer`)
- **Requirements**: Active playback.
- **Access**: Free (Member).
- **Notes**: Displays an interactive modal allowing users to set a countdown from 1 to 120 minutes. At expiry, playback fades out cleanly and the bot handles channel leave rules.
