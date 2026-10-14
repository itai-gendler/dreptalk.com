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
      "target": "src/pages/api/notifications/prefs.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/notificationChannels.ts#prefDefault"
    }
  ]
}
---

# Change notification settings

A signed-in person chooses, per channel, which kinds of notification reach browser push and Telegram.
