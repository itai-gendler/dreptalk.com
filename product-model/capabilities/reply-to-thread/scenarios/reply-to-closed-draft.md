---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Thread is Closed because its draft is connected to a governance action",
      "kind": "condition",
      "entities": [
        {
          "entity": "thread",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "governance-action",
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
      "text": "The DRep tries to reply",
      "kind": "actor",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    },
    {
      "text": "The Product refuses the reply",
      "kind": "product",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    }
  ]
}
---

# A connected draft takes no replies

## Trigger

The Proposal Draft is connected to its governance action.

## Outcome

No reply is added; the draft points to the governance thread.
