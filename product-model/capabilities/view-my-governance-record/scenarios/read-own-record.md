---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep opens My governance record",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "Report card"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::my-governance-record"
        }
      }
    },
    {
      "text": "The Product lists the decided Governance actions without the DRep's Vote and its votes without a rationale",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Title",
            "Decided epoch"
          ]
        },
        {
          "entity": "vote",
          "effect": "reads",
          "facts": [
            "Choice",
            "Rationale link"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::my-governance-record"
        }
      }
    }
  ]
}
---

# Read your record

## Trigger

A DRep wants to improve its report card.

## Outcome

The DRep sees exactly which actions and votes pull its figures down.
