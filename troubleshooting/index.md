---
order: 300
icon: alert
---

# Troubleshooting

This section covers common issues encountered by Discord users and server administrators, along with practical solutions.

## Playback and Audio Issues

### Playback is lagging, stuttering, or drops audio
- **Cause**: Temporary packet loss or Discord voice gateway routing latency.
- **Solution**: Execute the `/fix` command. The bot presents three recovery options:
  1. **Change Voice Region**: Switches the voice server RTC region to an alternate location to bypass routing congestion.
  2. **Reconnect**: Re-establishes the voice gateway socket without clearing the queue.
  3. **Recreate Player**: Re-initializes the audio session if the audio engine becomes desynchronized.

### Bot will not join the voice channel
- **Cause**: Missing channel permissions or voice channel user limits.
- **Solution**: Check channel settings in Discord. Ensure Listune has the **Connect** and **Speak** permissions in that channel. If the voice channel has a member limit that is full, grant the bot the **Move Members** permission so it can bypass channel caps.

### The bot left the voice channel unexpectedly
- **Cause**: Automatic inactivity leave timer (default: 90 seconds).
- **Solution**: On the Free tier, Listune automatically disconnects when playback ends and the queue is empty, or when all human listeners disconnect from the voice channel. To keep the bot in voice permanently, activate a Premium server plan and enable 24/7 mode with `/247 mode:enable`.

## Command and Interaction Issues

### The bot does not respond to commands in a specific channel
- **Cause**: Command channel restriction is enabled on the server.
- **Solution**: A server administrator may have restricted commands to specific channels using `/set channel`. Verify which channels are allowed, or have an administrator with Manage Server permissions review channel restrictions.

### "Only members with the DJ role can use this command"
- **Cause**: DJ Role mode is enabled on the server.
- **Solution**: When DJ mode is active, commands like `/skip`, `/pause`, `/volume`, and `/clearqueue` require the designated DJ role or Manage Server permissions, unless you are the original requester of the currently playing track.

### "Emoji search queries are not supported"
- **Cause**: Searching using only emojis triggers input validation safeguards.
- **Solution**: Enter a standard alphanumeric song title, artist name, or direct URL instead of emoji icons.

### "Queue limit reached" notice
- **Cause**: Free tier queue cap (default: 100 to 150 tracks).
- **Solution**: Use `/removedupes` to clear redundant songs, or upgrade to a Premium tier for expanded or unlimited queues.

### Direct Message delivery failed for `/grab`
- **Cause**: Your Discord privacy settings block Direct Messages from server members.
- **Solution**: In Discord, go to **User Settings > Privacy & Safety** and enable **Allow direct messages from server members** for that server.

## Discord Activity Issues

### Activity stuck loading or times out
- **Cause**: Discord client cached authorization error or launching from an unsupported context.
- **Solution**: Close the Activity frame and reopen it. Ensure you are launching the Activity from an active voice channel, 1-on-1 Direct Message, or Group DM call. Update your Discord client to the latest release.

## Dashboard and Premium Issues

### Settings are grayed out or locked on the web dashboard
- **Cause**: Missing Manage Server permission, or the feature requires Premium.
- **Solution**: Ensure your Discord account has the **Manage Server** permission in the guild. If the feature requires Premium (such as 24/7 mode or Custom Bot Profiles), verify that the server has been claimed using `/premium claim platform:patreon`.

### "No Patreon membership found" during `/premium claim`
- **Cause**: Patreon account is not connected to Discord or payment is still pending.
- **Solution**: Go to your Patreon profile, open **Settings > Connected Apps**, and confirm Discord is connected. Ensure your pledge is active, then rerun `/premium claim platform:patreon`.
