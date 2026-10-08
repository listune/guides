---
order: 770
icon: sliders
---

# Audio Filters

Listune includes real-time digital signal processing (DSP) filters that transform voice channel audio without stopping playback or disconnecting from Discord.

## Filter Overview

Filters modify frequency response, playback velocity, musical pitch, and spatial acoustics on the fly. When a filter command is executed, the audio node recalibrates the DSP pipeline within milliseconds.

To remove any active filter and restore default audio settings, use:
```text
/reset filter
!reset
```

## Complete Filter List

| Filter Command | Syntax | Effect Description |
| --- | --- | --- |
| `/3d` | `/3d` | Simulates a 360-degree spatial audio rotation around the listener. |
| `/bass` | `/bass` | Applies standard low-frequency acoustic amplification. |
| `/bassboost` | `/bassboost [level]` | Multi-tier low-end boost with selectable intensity levels. |
| `/china` | `/china` | Distinctive pentatonic and oriental acoustic response. |
| `/chipmunk` | `/chipmunk` | High pitch and increased tempo for high-register vocals. |
| `/darthvader` | `/darthvader` | Lowers pitch and increases resonance for deep vocal processing. |
| `/daycore` | `/daycore` | Slows down tempo and lowers pitch for a heavy, spaced-out feel. |
| `/doubletime` | `/doubletime` | Multiplies playback speed for fast-tempo listening. |
| `/earrape` | `/earrape` | Heavy saturation and extreme high-gain acoustic distortion. |
| `/equalizer` | `/equalizer [preset]` | 15-band customizable graphic equalizer across frequency bands. |
| `/karaoke` | `/karaoke` | Isolates and attenuates center-channel vocal frequencies for singing along. |
| `/nightcore` | `/nightcore` | Increases speed and pitch simultaneously for the popular nightcore tempo. |
| `/pitch` | `/pitch <number>` | Adjusts musical key up or down without altering playback velocity. |
| `/pop` | `/pop` | Equalizer curve tailored to accentuate vocals and mids in pop tracks. |
| `/rate` | `/rate <number>` | Adjusts raw audio sample rate for digital resampling effects. |
| `/slowmotion` | `/slowmotion` | Reduces playback velocity for relaxed, slower rhythm. |
| `/soft` | `/soft` | Attenuates harsh high frequencies for gentle background listening. |
| `/speed` | `/speed <number>` | Modifies playback velocity continuously from half speed to double speed. |
| `/superbass` | `/superbass` | Applies intense multi-stage bass equalization. |
| `/television` | `/television` | Band-pass filter emulating old CRT television and radio speakers. |
| `/treblebass` | `/treblebass` | Dual shelf boost enhancing both deep lows and crisp highs. |
| `/tremolo` | `/tremolo` | Creates rhythmic amplitude modulation and volume pulsation. |
| `/vaporwave` | `/vaporwave` | Classic slowed-down, pitch-lowered vaporwave aesthetic. |
| `/vibrate` | `/vibrate` | Rapid micro-frequency phase vibration. |
| `/vibrato` | `/vibrato` | Periodic pitch modulation and oscillating frequency flutter. |
| `/reset filter` | `/reset filter` | Clears all active filters and returns playback to normal flat response. |

## Combining and Adjusting Parameters

Numeric filters such as `/speed`, `/pitch`, and `/rate` accept fractional inputs to fine-tune playback:

```text
/speed number:1.25
/pitch number:1.1
/bassboost level:2
```

Audio filters are also accessible directly from the Web Player interface and can be adjusted through the interactive Player Control dropdown when configured by server managers.
