---
{
  "kind": "primary",
  "routes": {
    "telegram": "Telegram"
  },
  "steps": [
    {
      "text": "The Delegator sends /stop to the bot",
      "kind": "actor",
      "actor": "delegator",
      "entities": [],
      "contexts": {
        "telegram": {
          "place": "telegram-bot"
        }
      }
    },
    {
      "text": "The Product removes the Notification channel and replies that the chat is disconnected",
      "kind": "product",
      "actor": "delegator",
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "removes"
        }
      ],
      "contexts": {
        "telegram": {
          "place": "telegram-bot"
        }
      }
    }
  ]
}
---

# Send /stop to the bot

## Trigger

A person wants to stop messages from inside Telegram.

## Outcome

The chat is disconnected and the bot confirms.
