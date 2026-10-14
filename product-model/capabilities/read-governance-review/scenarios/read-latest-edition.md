---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens the Governance Review and picks the newest edition",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "governance-review-edition",
          "effect": "reads",
          "facts": [
            "Epoch window",
            "Title"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::governance-review"
        }
      }
    },
    {
      "text": "The Visitor reads the edition, its sources and corrections",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "governance-review-edition",
          "effect": "reads",
          "facts": [
            "Article",
            "Sources",
            "Dataset",
            "Corrections"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::review-edition"
        }
      }
    }
  ]
}
---

# Read the latest edition

## Trigger

A reader wants to catch up on governance.

## Outcome

The reader knows what was decided, what moved and what is still open in that window.

## Edge cases

- Each edition reports the position at the end of its window; other pages may show newer data.
