---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens DReps",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::dreps"
        }
      }
    },
    {
      "text": "The Product lists the registered DReps",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "Name",
            "Status",
            "Voting power",
            "Delegators"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::dreps"
        }
      }
    }
  ]
}
---

# Browse the DRep directory

## Trigger

A delegator looks for a DRep.

## Outcome

The reader sees DReps with their voting power and delegators.
