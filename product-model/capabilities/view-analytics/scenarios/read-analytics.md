---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens Analytics",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Type",
            "Tallies"
          ]
        },
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "Voting power",
            "Report card"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::analytics"
        }
      }
    }
  ]
}
---

# Read the analytics

## Trigger

A reader wants the big picture.

## Outcome

The reader sees how concentrated and how timely governance is.
