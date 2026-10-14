---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens the Treasury and a budget period",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "net-change-limit-period",
          "effect": "reads",
          "facts": [
            "Ceiling",
            "Epochs",
            "Withdrawn",
            "Remaining",
            "Defining actions"
          ]
        },
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Title",
            "On-chain changes"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::treasury"
        }
      }
    }
  ]
}
---

# Check a budget period

## Trigger

A reader asks how much of the limit is spent.

## Outcome

The reader sees the ceiling, what was withdrawn and what remains.

## Edge cases

- The operative limit of each period is curated, because the info actions that set it never enact on chain.
