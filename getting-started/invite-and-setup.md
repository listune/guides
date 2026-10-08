---
order: 890
icon: plug
---

# Inviting Listune

To use Listune in your Discord server, you must invite the bot through the official authorization link and ensure it receives the necessary Discord permissions.

## Official Invite Link

Always invite Listune through the official website redirect:

- Canonical Invite URL: [https://listune.app/invite](https://listune.app/invite)

Selecting this link directs you to the Discord OAuth2 application prompt where you select your target server. You must possess the **Manage Server** permission in that Discord guild to authorize new bots.

## Permission Breakdown

Listune requires specific permissions to join voice channels, stream audio, send interactive embeds, and manage command responses.

| Category | Permission | Purpose |
| --- | --- | --- |
| Text | View Channel | Read command messages and interaction triggers. |
| Text | Send Messages | Send track embeds, search results, and notifications. |
| Text | Embed Links | Render rich music cards, interactive controls, and queue tables. |
| Text | Read Message History | Check context and handle command pagination. |
| Text | Manage Messages | Clean up user command invocations and temporary notices. |
| Voice | Connect | Join your server voice or stage channels. |
| Voice | Speak | Stream audio through the voice connection. |
| Voice | Use Voice Activity | Maintain continuous voice transmission without push-to-talk. |
| Management | Manage Channels | Required only for automatic setup channels and voice channel status updates. |

:::info
If Listune lacks `Connect` or `Speak` permissions for a specific voice channel, playback will fail with a permission notice. Ensure channel-specific permission overrides do not block the bot.
:::
