---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A Delegation is Looking up",
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
      "text": "The Product reads where it delegates and when the latest certificate was",
      "kind": "product",
      "entities": [
        {
          "entity": "delegation",
          "effect": "changes",
          "from": "Looking up",
          "to": "Tracked",
          "facts": [
            "Delegated to",
            "Delegated since",
            "Last checked"
          ]
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

# A delegation is read for the first time

## Trigger

A followed Delegation was still being looked up.

## Outcome

The Delegation is tracked.
