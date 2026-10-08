---
order: 350
icon: check-circle
---

# Voting & Vote Lock

Listune is listed on Top.gg, the community directory for Discord bots. Voting supports the project and unlocks specific bot features for your account.

## Official Voting Link

You can cast your vote every 12 hours at:

- Direct Voting URL: [https://listune.app/topgg](https://listune.app/topgg)
- Official Top.gg Page: [https://top.gg/bot/928711702596423740/vote](https://top.gg/bot/928711702596423740/vote)

## What is Vote Lock?

Vote Lock is a conditional access mechanism. Certain optional bot features and commands (such as AI Music Assistant channels or voter-locked dashboard settings) can be configured to require an active vote record.

When an unvoted user attempts to invoke a vote-locked command or feature:
1. The bot intercepts the interaction and presents a notification card.
2. A direct **Vote on Top.gg** button is provided.
3. Once the user votes on Top.gg, the Top.gg webhook records the vote in the Listune database within seconds.
4. The user receives access for the next **12 hours**.

## Voting Rules and Frequency

- **12-Hour Validity**: Each vote remains valid in the Listune database for exactly 12 hours from the moment it is cast.
- **Top.gg Cooldown**: Top.gg enforces a 12-hour cooldown before the same user can vote again.
- **Vote Reminders**: Users can enable automatic vote reminder notifications on Top.gg to receive a ping when their voting cooldown expires.

## Bypassing Vote Locks

All users with an active **Premium** subscription (Personal, Guild Basic, or Guild Plus) automatically bypass all Vote Locks. Premium users do not need to vote on Top.gg to access any locked command or dashboard setting.
