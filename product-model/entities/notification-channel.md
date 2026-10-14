---
{
  "domain": "notifications",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/notificationChannels.ts"
    }
  ]
}
---

# Notification channel

A browser push subscription or a Telegram chat connected to an account.

## Information kept

- **Channel** — Browser push or Telegram
- **Label** — the browser, or the Telegram username or first name
- **Last sent** — when something was last delivered to it
