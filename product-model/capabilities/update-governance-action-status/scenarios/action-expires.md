---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "An Active enactable Governance action passed its expiry epoch",
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
      "text": "The Product records Expired",
      "kind": "product",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "changes",
          "from": "Active",
          "to": "Expired",
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

# An action expires

## Trigger

An enactable action's voting window ended without ratification.

## Outcome

The action reads Expired.
