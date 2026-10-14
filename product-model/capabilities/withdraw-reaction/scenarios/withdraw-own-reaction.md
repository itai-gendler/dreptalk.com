---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The CC member chooses their current side again",
      "kind": "actor",
      "actor": "cc-member",
      "entities": [
        {
          "entity": "reaction",
          "effect": "reads",
          "facts": [
            "Direction"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    },
    {
      "text": "The Product removes the Reaction and updates the count",
      "kind": "product",
      "actor": "cc-member",
      "entities": [
        {
          "entity": "reaction",
          "effect": "removes"
        },
        {
          "entity": "post",
          "effect": "changes",
          "facts": [
            "Ups",
            "Downs"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    }
  ]
}
---

# Take back a reaction

## Trigger

A writer chooses the side they already chose.

## Outcome

The reaction is gone and the count drops.
