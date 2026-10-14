---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator opens My DRep",
      "kind": "actor",
      "actor": "delegator",
      "entities": [
        {
          "entity": "delegation",
          "effect": "reads",
          "facts": [
            "Delegated to",
            "Delegated since"
          ]
        },
        {
          "entity": "drep",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::my-drep"
        }
      }
    },
    {
      "text": "The Product counts the decided Governance actions since that epoch and the DRep's votes on them",
      "kind": "product",
      "actor": "delegator",
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
            "Rationale link",
            "Earlier votes"
          ]
        },
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "Voting power",
            "Delegators"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::my-drep"
        }
      }
    }
  ]
}
---

# See what happened since delegating

## Trigger

A delegator wants the longer view.

## Outcome

Every figure states its basis, counted from the epoch of the latest delegation certificate.

## Edge cases

- Until the start epoch is on record the page shows no figures and says so.
- For a default option the page lists up to ten decided actions and what the stake counted as on each.
