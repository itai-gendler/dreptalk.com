---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "send-epoch-summary"
    },
    {
      "type": "capability",
      "id": "change-notification-settings"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/notificationChannels.ts#prefDefault"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/for-delegators.md"
    }
  ]
}
---

# An epoch summary reaches push and Telegram only when switched on

Every other notification kind reaches the channels by default; the summary always reaches the inbox.
