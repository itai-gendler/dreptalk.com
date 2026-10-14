---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "An Active enactable Governance action was removed on chain without expiring",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::thread"
        }
      }
    },
    {
      "text": "The Product records Dropped",
      "kind": "product",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "changes",
          "from": "Active",
          "to": "Dropped",
          "facts": [
            "Decided epoch"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::thread"
        }
      }
    }
  ]
}
---

# An action is dropped

## Trigger

A competing action of the same kind was enacted.

## Outcome

The action reads Dropped.
