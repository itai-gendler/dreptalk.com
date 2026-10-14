---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "New Notifications wait for delivery",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "notification",
          "effect": "reads",
          "facts": [
            "Kind",
            "About"
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
      "text": "The Product sends each Notification channel one message bundling the new kinds its settings allow: up to three spelled out with a link, more as a count summary",
      "kind": "product",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Push preferences",
            "Telegram preferences"
          ]
        },
        {
          "entity": "notification-channel",
          "effect": "changes",
          "facts": [
            "Last sent"
          ]
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

# Deliver to push and Telegram

## Trigger

New notifications exist since the last delivery.

## Outcome

Each enabled channel receives the notifications its settings allow.

## Edge cases

- The device-paired notice is always delivered.
- Each channel advances past what it was sent, so nothing reaches it twice.
