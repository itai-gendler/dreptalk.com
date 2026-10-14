---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator turns on push for this browser and allows it",
      "kind": "actor",
      "actor": "delegator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::notifications"
        }
      }
    },
    {
      "text": "The Product connects the Notification channel for this browser",
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
        "web": {
          "place": "web::signed-in::notifications"
        }
      }
    }
  ]
}
---

# Allow push on this device

## Trigger

A person wants notifications on this browser or installed app.

## Outcome

This device receives push notifications.

## Edge cases

- On iPhone and iPad push needs DRepTalk added to the home screen.
