---
order: 880
icon: play
---

# Basic Usage

Once Listune is in your server, you can begin playing music using slash commands, prefix commands, or bot mentions.

## Starting Playback

1. Connect to any voice channel in your Discord server.
2. Open a text channel where Listune is permitted to send messages.
3. Type `/play` followed by your search query or a direct link.

For example:
```text
/play search:Rick Astley Never Gonna Give You Up
```

Listune will automatically join your voice channel, resolve the audio source, and begin streaming audio while posting the interactive player card in your text channel.

## Command Methods

Listune offers three distinct ways to execute commands:

=== Slash Commands
Slash commands are the recommended way to interact with Listune. Discord validates inputs in real time and provides auto-completion for song titles, radio stations, and playlist IDs.

```text
/play search:lofi hip hop radio
/queue page:1
/volume number:75
/skip
```

=== Prefix Commands
Prefix commands use a text prefix before the command name. The default prefix is `!`, though server managers can customize it using `/prefix` or through the web dashboard.

```text
!play lofi hip hop radio
!queue 1
!volume 75
!skip
```

=== Bot Mentions
Mentioning the bot acts in two distinct ways:

1. **Mention Help Card**: Sending `@Listune` by itself triggers the interactive welcome container. This container provides buttons for the Support Server, Documentation, and Web Dashboard, along with your server current prefix.
2. **Mention as Prefix**: You can use the bot mention in place of a text prefix:
```text
@Listune play lofi hip hop radio
@Listune queue
@Listune skip
```
===

## Primary Playback Controls

| Action | Slash Command | Prefix Command | Description |
| --- | --- | --- | --- |
| Play Music | `/play search:<query>` | `!play <query>` | Searches for a song or loads a direct URL into the queue. |
| Pause | `/pause` | `!pause` | Pauses audio playback without dropping the connection. |
| Resume | `/resume` | `!resume` | Resumes paused audio playback. |
| Skip Track | `/skip` | `!skip` | Skips the current song and plays the next queued track. |
| View Queue | `/queue [page]` | `!queue [page]` | Displays all upcoming songs with duration and requester. |
| Adjust Volume | `/volume <number>` | `!volume <number>` | Sets playback volume between 1 and 100. |
| Stop Playback | `/stop` | `!stop` | Stops audio, clears the entire queue, and resets the player. |
| Disconnect | `/leave` | `!leave` | Disconnects the bot from the voice channel immediately. |

## Inactivity and 24/7 Mode

When audio playback concludes and the queue is empty, or when all human listeners leave the voice channel, Listune starts an automatic leave timer (default: 90 seconds). This conserves server resources.

If your server has an active Premium plan, you can enable 24/7 mode with `/247`. In 24/7 mode, Listune remains in your designated voice channel continuously, ready to play music at any moment.
