---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "notification-channel",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "actors": [
        "drep",
        "spo",
        "cc-member",
        "proposer",
        "co-proposer",
        "delegator",
        "moderator"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/api/notifications/channels.ts"
    }
  ]
}
---

# Only signed-in people connect notification channels

A push subscription or a Telegram chat is connected to the signed-in person's account.
