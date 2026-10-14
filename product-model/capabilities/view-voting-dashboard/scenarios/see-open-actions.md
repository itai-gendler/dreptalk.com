---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep opens the Voting Dashboard",
      "kind": "actor",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::voting-dashboard"
        }
      }
    },
    {
      "text": "The Product lists the open Governance actions with the DRep's Vote on each and its voting record",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Title",
            "Type",
            "Expiry epoch"
          ]
        },
        {
          "entity": "vote",
          "effect": "reads",
          "facts": [
            "Choice",
            "Cast at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::voting-dashboard"
        }
      }
    }
  ]
}
---

# See what is waiting for a vote

## Trigger

A DRep checks the current ballot.

## Outcome

The DRep sees which open actions carry its vote and how long each stays open.
