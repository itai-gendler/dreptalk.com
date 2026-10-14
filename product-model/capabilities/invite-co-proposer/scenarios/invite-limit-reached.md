---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Proposer creates an invite",
      "kind": "actor",
      "actor": "proposer",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-proposers"
        }
      }
    },
    {
      "text": "The proposer already holds two pending or active mandates",
      "kind": "condition",
      "entities": [
        {
          "entity": "co-proposer-mandate",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "proposer",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-proposers"
        }
      }
    },
    {
      "text": "The Product refuses the invite",
      "kind": "product",
      "actor": "proposer",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-proposers"
        }
      }
    }
  ]
}
---

# The proposer already has two co-proposers

## Trigger

Two mandates are already pending or active.

## Outcome

No invite is created.
