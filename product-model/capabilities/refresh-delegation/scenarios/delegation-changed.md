---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A Tracked Delegation points somewhere new on chain",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "delegation",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::start-page"
        }
      }
    },
    {
      "text": "The Product updates the Delegation and notifies its delegator",
      "kind": "product",
      "entities": [
        {
          "entity": "delegation",
          "effect": "changes",
          "facts": [
            "Delegated to",
            "Delegated since",
            "Last checked"
          ]
        },
        {
          "entity": "notification",
          "effect": "creates",
          "to": "Unread",
          "facts": [
            "Kind",
            "About",
            "Created at"
          ]
        },
        {
          "entity": "delegator",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::start-page"
        }
      }
    }
  ]
}
---

# A delegation changed on chain

## Trigger

A followed stake address re-delegated outside DRepTalk.

## Outcome

The start page follows the new delegation and the delegator is notified.

## Edge cases

- A change the person made through DRepTalk is expected and sends no notification.
