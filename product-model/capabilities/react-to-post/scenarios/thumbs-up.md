---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The CC member chooses Thumbs up on another writer's Post",
      "kind": "actor",
      "actor": "cc-member",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
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
    },
    {
      "text": "The Product records the Reaction and updates the counts",
      "kind": "product",
      "actor": "cc-member",
      "entities": [
        {
          "entity": "reaction",
          "effect": "creates",
          "facts": [
            "Direction"
          ]
        },
        {
          "entity": "post",
          "effect": "changes",
          "facts": [
            "Ups"
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

# Give a thumbs up

## Trigger

A writer agrees with a post.

## Outcome

The post counts one more thumbs up.
