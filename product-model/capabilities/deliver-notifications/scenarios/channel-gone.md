---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A Notification channel refuses delivery as gone",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::notifications"
        }
      }
    },
    {
      "text": "The Product removes the Notification channel",
      "kind": "product",
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::notifications"
        }
      }
    }
  ]
}
---

# A channel no longer exists

## Trigger

The browser subscription expired or the chat blocked the bot.

## Outcome

The channel is removed and nothing more is sent to it.
