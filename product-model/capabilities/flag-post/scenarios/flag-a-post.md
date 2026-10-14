---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep chooses Flag on another writer's Post",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Flags"
          ]
        },
        {
          "entity": "flag",
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
      "text": "The Product records the Flag",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "flag",
          "effect": "creates",
          "facts": [
            "Raised by"
          ]
        },
        {
          "entity": "post",
          "effect": "changes",
          "facts": [
            "Flags"
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

# Flag a post

## Trigger

A writer finds a post abusive.

## Outcome

The post counts the flag.
