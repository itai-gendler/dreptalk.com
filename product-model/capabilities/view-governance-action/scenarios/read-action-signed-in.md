---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator opens the Thread of a Governance action",
      "kind": "actor",
      "actor": "delegator",
      "entities": [
        {
          "entity": "thread",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Title",
            "Type",
            "Abstract",
            "Motivation",
            "Rationale",
            "Authors",
            "References",
            "Proposer address",
            "Deposit",
            "Expiry epoch",
            "Tallies",
            "Thresholds",
            "Data as of"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    },
    {
      "text": "The Delegator reads the votes of each voting body",
      "kind": "actor",
      "actor": "delegator",
      "entities": [
        {
          "entity": "vote",
          "effect": "reads",
          "facts": [
            "Voter body",
            "Choice",
            "Counted"
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

# A signed-in person reads an action

## Trigger

A signed-in person opens an action.

## Outcome

The person sees the same facts, with the voting panel when they are a DRep.
