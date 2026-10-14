---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator opens the start page",
      "kind": "actor",
      "actor": "delegator",
      "entities": [
        {
          "entity": "delegation",
          "effect": "reads",
          "facts": [
            "Delegated to"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::start-page"
        }
      }
    },
    {
      "text": "The Product shows the DRep, its latest confirmed votes and the open Governance actions it has not voted on",
      "kind": "product",
      "actor": "delegator",
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "Name",
            "Voting power",
            "Delegators"
          ]
        },
        {
          "entity": "vote",
          "effect": "reads",
          "facts": [
            "Choice",
            "Cast at"
          ]
        },
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Title",
            "Expiry epoch"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::start-page"
        }
      }
    }
  ]
}
---

# A delegator checks on its DRep

## Trigger

A delegator signs in.

## Outcome

The delegator sees whether its DRep is on top of the current ballot.

## Edge cases

- A delegation to Always abstain or Always no confidence is explained as a standing position with no votes to follow.
