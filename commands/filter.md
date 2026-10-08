---
order: 680
icon: filter
---

# Filter Commands

Listune includes 26 audio DSP filter commands. All filter commands support both Discord Slash Commands and text prefixes.

## Summary Table

| Command | Type | Aliases | Access | Description |
| --- | --- | --- | --- | --- |
| `/3d` | Slash & Prefix | None | Member | Toggles 360-degree spatial audio rotation. |
| `/bass` | Slash & Prefix | None | Member | Applies standard low-frequency acoustic enhancement. |
| `/bassboost` | Slash & Prefix | None | Member | Applies variable-level bass boost (`/bassboost [level]`). |
| `/china` | Slash & Prefix | None | Member | Applies an oriental pentatonic acoustic filter. |
| `/chipmunk` | Slash & Prefix | None | Member | Accelerates playback velocity and raises vocal pitch. |
| `/darthvader` | Slash & Prefix | None | Member | Lowers pitch and increases vocal resonance. |
| `/daycore` | Slash & Prefix | None | Member | Slows tempo and deepens pitch for daycore aesthetics. |
| `/doubletime` | Slash & Prefix | None | Member | Multiplies playback tempo for fast listening. |
| `/earrape` | Slash & Prefix | None | Member | High-gain acoustic saturation and heavy distortion. |
| `/equalizer` | Slash & Prefix | None | Member | Configures a 15-band graphic equalizer curve (`/equalizer [preset]`). |
| `/karaoke` | Slash & Prefix | None | Member | Attenuates center-channel vocal frequencies for singing along. |
| `/nightcore` | Slash & Prefix | None | Member | Simultaneously raises pitch and tempo for the nightcore style. |
| `/pitch` | Slash & Prefix | None | Member | Modifies audio pitch by a specific numeric multiplier (`/pitch <number>`). |
| `/pop` | Slash & Prefix | None | Member | Equalizer profile optimized for pop music vocal presence. |
| `/rate` | Slash & Prefix | None | Member | Directly adjusts the playback sample rate (`/rate <number>`). |
| `/reset filter` | Slash & Prefix | `reset` | Member | Resets all active audio filters and restores default flat sound. |
| `/slowmotion` | Slash & Prefix | None | Member | Reduces playback velocity for a relaxed rhythm. |
| `/soft` | Slash & Prefix | None | Member | Attenuates harsh high frequencies for softer background audio. |
| `/speed` | Slash & Prefix | None | Member | Adjusts playback speed continuously (`/speed <number>`). |
| `/superbass` | Slash & Prefix | None | Member | Applies heavy multi-stage bass equalization. |
| `/television` | Slash & Prefix | None | Member | Simulates narrow-band vintage television speakers. |
| `/treblebass` | Slash & Prefix | None | Member | Dual-shelf boost enhancing low sub-bass and high treble. |
| `/tremolo` | Slash & Prefix | None | Member | Creates periodic volume and amplitude fluctuations. |
| `/vaporwave` | Slash & Prefix | None | Member | Slows down tempo and shifts pitch down for vaporwave audio. |
| `/vibrate` | Slash & Prefix | None | Member | Rapid phase oscillation and high-frequency audio flutter. |
| `/vibrato` | Slash & Prefix | None | Member | Rhythmic pitch oscillation effect. |

## Usage and Requirements

### Common Requirements
- **Active Audio Player**: The bot must currently be connected and streaming in a voice channel.
- **Voice Channel Proximity**: The user must be in the same voice channel as the bot.
- **DJ Role Restrictions**: When the DJ Role system is enabled on the server, filter commands require the DJ role or the Discord **Manage Server** permission.

### Numeric Parameters

Several filter commands accept numeric multipliers or level indicators:

```text
/bassboost level:2
/speed number:1.25
/pitch number:0.9
/rate number:1.1
```

To cancel all active filters, execute `/reset filter` or `!reset`.
