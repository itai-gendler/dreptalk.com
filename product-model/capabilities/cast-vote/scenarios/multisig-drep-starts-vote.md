---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep, signed in as a multisig DRep, chooses Abstain on an open Governance action",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Title"
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
      "text": "The Product stores a Multisig vote that collects signatures for 36 hours and shows its co-sign link",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "multisig-vote",
          "effect": "creates",
          "to": "Collecting",
          "facts": [
            "Governance action",
            "Choice",
            "Rationale link",
            "Signatures required",
            "Co-sign link",
            "Expires at"
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

# A multisig DRep starts a vote for co-signing

## Trigger

A member of a multisig DRep votes on an action.

## Outcome

The vote waits for the other members' signatures behind a co-sign link.
