---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator switches off mentions for browser push",
      "kind": "actor",
      "actor": "delegator",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Push preferences"
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
      "text": "The Product stores the choice",
      "kind": "product",
      "actor": "delegator",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Push preferences"
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

# Turn a kind off for a channel

## Trigger

Push notifications for mentions are too many.

## Outcome

Mentions no longer reach push; they still arrive in the inbox.

## Edge cases

- The epoch summary is off by default for push and Telegram; every other kind is on.
- The device-paired notice cannot be switched off.
