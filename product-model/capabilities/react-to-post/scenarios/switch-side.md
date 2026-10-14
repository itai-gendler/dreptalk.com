---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The CC member chooses Thumbs down on a Post they gave a thumbs up",
      "kind": "actor",
      "actor": "cc-member",
      "entities": [
        {
          "entity": "reaction",
          "effect": "reads",
          "facts": [
            "Direction"
          ]
        },
        {
          "entity": "post",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    },
    {
      "text": "The Product replaces the Reaction and updates both counts",
      "kind": "product",
      "actor": "cc-member",
      "entities": [
        {
          "entity": "reaction",
          "effect": "changes",
          "facts": [
            "Direction"
          ]
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

# Switch to the other side

## Trigger

A writer changes their mind.

## Outcome

The reaction moves to the other side.
