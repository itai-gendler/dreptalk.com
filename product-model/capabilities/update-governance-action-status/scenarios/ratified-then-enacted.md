---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "An Active Governance action has been ratified on chain",
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
      "text": "The Product records Ratified and freezes its tallies",
      "kind": "product",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "changes",
          "from": "Active",
          "to": "Ratified",
          "facts": [
            "Decided epoch",
            "Data as of"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::thread"
        }
      }
    },
    {
      "text": "The Product keeps checking until the chain shows it enacted, then records Enacted",
      "kind": "product",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "changes",
          "from": "Ratified",
          "to": "Enacted",
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

# An action is ratified, then enacted

## Trigger

An enactable action reached its thresholds.

## Outcome

The action reads Ratified, then Enacted about an epoch later.
