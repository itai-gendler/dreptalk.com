---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor pastes a governance action id or a DRep ID",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "drep",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::search"
        }
      }
    },
    {
      "text": "The Product opens the matching Governance action thread or DRep profile",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Action ID"
          ]
        },
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "DRep ID"
          ]
        },
        {
          "entity": "thread",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::search"
        }
      }
    }
  ]
}
---

# Paste an on-chain id

## Trigger

A reader has a governance action id or a DRep ID.

## Outcome

The reader lands on that action's thread or DRep's profile.

## Edge cases

- An id that matches nothing on this network opens search with the id filled in.
