---
{
  "type": "messaging",
  "actors": [
    "delegator"
  ],
  "languages": [
    "en"
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/notifications/telegramWebhook.ts#handleTelegramUpdate"
    }
  ]
}
---

# Telegram bot

The DRepTalk bot a signed-in person connects in a private Telegram chat to receive notifications there, and disconnects again with /stop.
