---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator chooses to send a test to a Notification channel",
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
      "text": "The Product sends a test message to it",
      "kind": "product",
      "actor": "delegator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::notifications"
        }
      }
    }
  ]
}
---

# Test a channel

## Trigger

A person wants to see that push works.

## Outcome

A test message arrives on that channel.

## Edge cases

- At most five tests per hour.
