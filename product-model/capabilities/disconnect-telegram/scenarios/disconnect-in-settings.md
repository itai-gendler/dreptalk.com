---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator chooses Disconnect on the Telegram chat",
      "kind": "actor",
      "actor": "delegator",
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "reads",
          "facts": [
            "Label"
          ]
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
      "actor": "delegator",
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

# Disconnect from the settings

## Trigger

A person no longer wants Telegram messages.

## Outcome

The chat receives nothing more.
