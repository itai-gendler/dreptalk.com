---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "An Active info Governance action reached the end of its voting window",
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
      "text": "The Product records Closed",
      "kind": "product",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "changes",
          "from": "Active",
          "to": "Closed",
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

# An info action closes

## Trigger

An info action's voting window ended.

## Outcome

The action reads Closed; info actions never enact.
