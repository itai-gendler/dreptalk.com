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
      "target": "src/pages/notifications.astro"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/notifications.ts#markAllRead"
    }
  ]
}
---

# Open notifications

A signed-in person opens the inbox: replies, mentions, governance events and delegation news, newest first. Opening it marks everything read.
