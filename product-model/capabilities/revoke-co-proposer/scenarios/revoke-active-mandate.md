---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Proposer revokes an active co-proposer",
      "kind": "actor",
      "actor": "proposer",
      "entities": [
        {
          "entity": "co-proposer-mandate",
          "effect": "reads",
          "facts": [
            "Accepted at"
          ]
        },
        {
          "entity": "co-proposer",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-proposers"
        }
      }
    },
    {
      "text": "The Product revokes the Co-proposer mandate and ends the co-proposer's sessions under it",
      "kind": "product",
      "actor": "proposer",
      "entities": [
        {
          "entity": "co-proposer-mandate",
          "effect": "changes",
          "from": "Active",
          "to": "Revoked",
          "facts": [
            "Revoked at"
          ]
        },
        {
          "entity": "co-proposer",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-proposers"
        }
      }
    }
  ]
}
---

# Revoke an active co-proposer

## Trigger

A colleague should no longer write for the proposer.

## Outcome

The mandate is revoked and the co-proposer's access ends at once; earlier posts keep their badge.
