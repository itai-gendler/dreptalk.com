---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A Syncing Governance action is due for its tally",
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
      "text": "The Product records its tallies and thresholds and marks it Active",
      "kind": "product",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "changes",
          "from": "Syncing",
          "to": "Active",
          "facts": [
            "Tallies",
            "Thresholds",
            "Data as of"
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

# An action gets its first tally

## Trigger

A Syncing action is due for its tally run.

## Outcome

The action is Active with tallies and thresholds shown as of the run.
