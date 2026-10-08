---
order: 800
icon: unmute
---

# Playback & Sources

Listune delivers high-fidelity audio streams powered by a Lavalink v4 driver with automatic node failover.

## Audio Processing Architecture

When a user initiates playback:

1. **Query Resolution**: The bot queries configured search providers (such as YouTube Music, Spotify, Apple Music, Deezer, Tidal, and SoundCloud) based on server preferences.
2. **Stream Routing**: Audio is retrieved by the Lavalink node and processed through real-time DSP audio filters (equalizers, pitch shifting, timescale transformations).
3. **Voice Delivery**: Processed frames are encrypted and streamed directly to Discord voice servers.

## Supported Streaming Services

Listune natively supports direct playback and playlist resolution from:

- **YouTube & YouTube Music**: Standard tracks, music videos, and public playlists.
- **Spotify**: Tracks, albums, artists, and playlists resolved through metadata matching.
- **Apple Music**: Individual songs, albums, and curated playlists.
- **SoundCloud**: Tracks, sets, and user playlists.
- **Deezer**: Single tracks and playlist collections.
- **Tidal**: Lossless-quality streams and albums.
- **Twitch**: Live stream audio feeds.
- **Direct HTTP Streams**: Raw audio streams (e.g. MP3, AAC, FLAC web radio streams).

## Detailed Guides

- [Play Queries](queries.md): How to submit text queries, artist searches, direct links, and playlists.
- [Queue & Playlists](queue-and-playlists.md): Managing queue orders, deduplication, custom playlists, favorites, and history.
- [Audio Filters](audio-filters.md): Applying 26 real-time audio filters, equalizers, and speed adjustments.
- [Radio & Trivia](radio-and-trivia.md): Exploring world radio broadcasts and interactive music trivia games.
