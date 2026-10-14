---
{
  "entities": [
    {
      "entity": "notification",
      "shows": [
        "Kind",
        "About",
        "From",
        "Created at"
      ]
    },
    {
      "entity": "notification-channel",
      "shows": [
        "Channel",
        "Label",
        "Last sent"
      ]
    },
    {
      "entity": "account",
      "shows": [
        "Push preferences",
        "Telegram preferences"
      ],
      "collects": [
        "Push preferences",
        "Telegram preferences"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/notifications.astro"
    }
  ]
}
---

# Notifications

The inbox, with the notification settings and the push and Telegram channels.
