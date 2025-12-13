---
title: Troubleshooting & FAQs
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# FAQ

Find answers to the following common questions about Custom Rewards:

### Q. Can I reuse a Client Reward ID once archived?

Yes, IDs can be reused once the reward is archived or ended. Active rewards must have unique IDs.

### Q. Can I personalize reward points in the payload?

Yes. The payload includes a key called `credits` that carries the points or cashback value rewarded to the user.

### Q. What happens if the client webhook endpoint is unavailable?

CleverTap retries twice with a 3-second wait before marking as failed.

### Q. How are rewards tracked in system events?

All Custom Rewards trigger a single system event named *Webhook Rewarded*. The event includes a property indicating the reward type (Physical & Digital Reward or Self-managed Wallet Credits).

### Can I specify the reward quantity (for example, two movie tickets)?

Yes. Use the *Additional Parameters* section when configuring the promo campaign. You can add a key-value pair such as `"quantity": "2"` in the setup to indicate multiple rewards (for example, two vouchers or two movie tickets).
