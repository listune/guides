---
order: 380
icon: key
---

# Premium Redemption

Once you subscribe to a server-tier plan on Patreon or donate via Ko-fi, you activate Premium on your server using the bot in-chat commands.

## Activating a Server Slot

To assign one of your available server slots to a Discord guild:

1. Open any text channel in the target server where you have permission to send commands.
2. Execute the claim command:
```text
/premium claim platform:patreon
```
3. The bot checks your linked Patreon membership:
   - Validates that your account possesses available server quota (`usedQuota < maxQuota`).
   - Registers the server ID to your active supporter record.
   - Instantly applies Premium status to the guild.

All members in that server immediately gain access to 24/7 mode, unrestricted volume, full audio filters, expanded queues, and vote lock bypasses.

### Ko-fi Redemption

If your subscription was purchased through Ko-fi, specify `kofi` as the platform and include your Ko-fi transaction ID:
```text
/premium claim platform:kofi transaction_id:KFI-XXXX-XXXX
```

## Transferring or Reclaiming Server Slots

Server slots are not permanently locked to one guild. If you change servers or want to move your benefits:

1. In the server you wish to remove Premium from, execute:
```text
/premium unclaim platform:patreon
```
2. The bot removes the guild ID from your allocated list and restores 1 slot back to your available quota.
3. You can immediately claim a new server by running `/premium claim platform:patreon` in the new server.

## Checking Quota Status

If a claim attempt returns an error, verify the following:

- **Quota Full**: If you subscribed to Guild Basic (1 server) and have already claimed a server, you must unclaim the existing server before claiming a new one.
- **Account Disconnected**: Ensure your Discord account remains connected under Patreon Settings > Connected Apps.
- **Payment Verification**: Recent pledges may take up to 60 seconds to process through Patreon webhooks.
