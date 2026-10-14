---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator turns off push for a browser",
      "kind": "actor",
      "actor": "delegator",
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "reads",
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

# Stop push on a device

## Trigger

A person no longer wants push on a browser.

## Outcome

That browser receives no more push notifications.
