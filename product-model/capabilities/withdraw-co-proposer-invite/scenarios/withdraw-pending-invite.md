---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Proposer withdraws a pending invite",
      "kind": "actor",
      "actor": "proposer",
      "entities": [
        {
          "entity": "co-proposer-mandate",
          "effect": "reads",
          "facts": [
            "Expires at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-proposers"
        }
      }
    },
    {
      "text": "The Product removes the pending Co-proposer mandate",
      "kind": "product",
      "actor": "proposer",
      "entities": [
        {
          "entity": "co-proposer-mandate",
          "effect": "removes",
          "from": "Pending"
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

# Withdraw a pending invite

## Trigger

An invite was sent to the wrong person or is no longer needed.

## Outcome

The invite is gone and its link no longer works.
