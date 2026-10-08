---
order: 390
icon: heart
---

# Patreon Integration

Patreon is the primary billing and membership platform used by Listune. Subscription tiers link directly to your Discord account through automated webhooks.

## Connecting Your Discord Account

To ensure your subscription is recognized immediately, your Discord account must be linked to Patreon prior to or upon subscribing:

1. Open **Patreon Settings** and navigate to **Connected Apps**.
2. Locate **Discord** and click **Connect**.
3. Authorize Patreon to identify your Discord User ID.
4. Visit the official Listune Patreon campaign page: [https://www.patreon.com/c/listune](https://www.patreon.com/c/listune).
5. Select your preferred tier:
   - [Personal Plan ($2/mo)](https://www.patreon.com/checkout/listune?rid=22189390)
   - [Guild Basic Plan ($3/mo)](https://www.patreon.com/checkout/listune?rid=10026039)
   - [Guild Plus Plan ($5/mo)](https://www.patreon.com/checkout/listune?rid=10067355)

## How Synchronization Works

- **Real-Time Webhooks**: When Patreon confirms your pledge, a webhook notifies the Listune backend. The bot records your Discord User ID and credits your account with the corresponding server quotas within seconds.
- **Support Server Role**: If you join the official Listune Support Server, you automatically receive the **Premium** role.
- **Renewal and Expiration**: Patreon subscriptions renew automatically every month. If a payment fails or a membership is cancelled, the quota expires at the end of the billing cycle, and any claimed servers gracefully return to standard limits.

## Ko-fi Support Alternative

Listune also accepts voluntary tips and supporter subscriptions through Ko-fi at [https://ko-fi.com/listune](https://ko-fi.com/listune). If you donate through Ko-fi, you can link your support using the transaction ID provided in your donation receipt.
