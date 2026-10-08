---
order: 760
icon: broadcast
---

# Radio & Trivia

Beyond individual track playback, Listune provides continuous live radio streaming and an interactive music trivia mini-game.

## World Radio Streaming

The `/radio` command (alias: `/fm`) connects your voice channel to global live radio broadcasts. Radio streams play continuously without requiring queue replenishment or track management.

```text
/radio
!radio
!fm
```

### Radio Capabilities

- **Categorized Station Directory**: Browse stations by country, music genre, or station name through Discord selection menus.
- **Continuous 24/7 Audio**: Ideal for community voice channels that want uninterrupted background music, chill hop, jazz, or international news broadcasts.
- **Web Player Synchronization**: The active radio station displays on the Web Player and Dashboard with live metadata whenever provided by the broadcast station.

## Music Trivia Mini-Game

Listune includes a music quiz system accessed through `/music trivia` (aliases: `/musictrivia`, `!mt`). This game streams short audio snippets into the voice channel while server members compete to identify the song title and artist.

```text
/music trivia mode:<mode> rounds:<rounds> time:<time> difficulty:<difficulty> genre:<genre> [playlist]
```

### Game Parameters

| Parameter | Type | Options / Valid Values | Description |
| --- | --- | --- | --- |
| `mode` | Required | Standard, Elimination, Fast-Track | Sets game rules and scoring mechanics. |
| `rounds` | Required | 5 to 25 | Total number of song snippets played during the match. |
| `time` | Required | 15s, 20s, 30s | Guessing window permitted per audio snippet. |
| `difficulty` | Required | Easy, Medium, Hard | Controls snippet length and popularity threshold of tracks. |
| `genre` | Required | Pop, Rock, 80s, 90s, Hip-Hop, Anime, EDM | Music category sampled by the trivia generator. |
| `playlist` | Optional | Custom Playlist ID | Overrides random genres to draw trivia questions from a specific custom playlist. |

### Scoring and Interaction

- The bot plays an audio snippet in the connected voice channel.
- Participants submit guesses using Discord Components V2 interactive buttons or chat responses.
- Points are awarded based on speed and accuracy.
- At the conclusion of all rounds, Listune generates a final leaderboard summarizing the winners and statistics.
