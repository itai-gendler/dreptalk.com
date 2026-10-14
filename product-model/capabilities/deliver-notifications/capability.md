---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "notifications",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/sync/phases/notifications.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/notifications/dispatch.ts#dispatchWebPush"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/notifications/fanout.ts#runFanout"
    }
  ]
}
---

# Deliver notifications

Every five minutes the Product fans governance events out to the accounts that receive them and delivers new notifications to each account's push and Telegram channels, as its settings allow.
