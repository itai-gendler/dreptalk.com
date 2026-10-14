---
{
  "availability": [
    {
      "place": "web::signed-in"
    },
    {
      "place": "telegram-bot"
    }
  ],
  "domain": "notifications",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/api/notifications/telegram-link.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/notifications/telegramWebhook.ts#handleTelegramUpdate"
    }
  ]
}
---

# Connect Telegram

A signed-in person gets a one-time link from the notification settings and starts the DRepTalk bot with it in a private Telegram chat.
