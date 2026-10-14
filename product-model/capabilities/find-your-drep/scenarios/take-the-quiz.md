---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor answers the questions drawn from decided Governance actions",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Title",
            "Abstract"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::find-your-drep"
        }
      }
    },
    {
      "text": "The Product ranks DReps by how their votes match the answers",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "Name",
            "Voting power"
          ]
        },
        {
          "entity": "vote",
          "effect": "reads",
          "facts": [
            "Choice"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::find-your-drep"
        }
      }
    }
  ]
}
---

# Take the matching quiz

## Trigger

A holder wants a DRep who votes like they would.

## Outcome

The holder sees DReps ranked by agreement, with a shareable result.

## Edge cases

- A DRep needs enough votes on the questions to be ranked.
