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
      "target": "src/lib/notifications/telegramWebhook.ts#handleTelegramUpdate"
    }
  ]
}
---

# Disconnect Telegram

A person disconnects a Telegram chat, from the settings or by sending /stop to the bot.
