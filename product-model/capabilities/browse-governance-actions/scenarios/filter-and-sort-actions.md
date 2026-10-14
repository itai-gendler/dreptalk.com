---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens Governance Actions and picks Open and Closing soonest",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::governance-actions"
        }
      }
    },
    {
      "text": "The Product lists the open Governance actions by expiry epoch",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Title",
            "Type",
            "Expiry epoch",
            "Tallies"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::governance-actions"
        }
      }
    }
  ]
}
---

# Find the actions closing soonest

## Trigger

A reader wants to see which open actions need attention.

## Outcome

The reader sees the open actions, soonest to close first.

## Edge cases

- Trending counts each forum reply three times, adds the vote count on a logarithmic scale, halves every week without activity and sinks decided actions to the bottom.
- Recently decided orders by the decision epoch and lists only decided actions.
