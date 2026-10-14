---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Post is the writer's own or written by the Product",
      "kind": "condition",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Kind"
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
      "text": "The CC member tries to react",
      "kind": "actor",
      "actor": "cc-member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    },
    {
      "text": "The Product refuses the reaction",
      "kind": "product",
      "actor": "cc-member",
      "entities": [
        {
          "entity": "reaction",
          "effect": "reads",
          "facts": []
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

# No reaction on your own post or the Product's

## Trigger

The post is the writer's own, or the opening post of a governance action.

## Outcome

No reaction is recorded.
