---
{
  "kind": "primary",
  "routes": {
    "main": "Website, then Telegram"
  },
  "steps": [
    {
      "text": "The Delegator chooses Connect Telegram and opens the link it gives",
      "kind": "actor",
      "actor": "delegator",
      "entities": [],
      "contexts": {
        "main": {
          "place": "web::signed-in::notifications"
        }
      }
    },
    {
      "text": "The Delegator sends the start message with the link code to the bot in a private chat",
      "kind": "actor",
      "actor": "delegator",
      "entities": [],
      "contexts": {
        "main": {
          "place": "telegram-bot"
        }
      }
    },
    {
      "text": "The Product connects the chat as a Notification channel and replies that it is connected",
      "kind": "product",
      "actor": "delegator",
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "creates",
          "facts": [
            "Channel",
            "Label"
          ]
        }
      ],
      "contexts": {
        "main": {
          "place": "telegram-bot"
        }
      }
    }
  ]
}
---

# Connect a Telegram chat

## Trigger

A person wants notifications in Telegram.

## Outcome

The chat is connected and listed in the settings with its name.
