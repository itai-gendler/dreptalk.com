---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep opens the co-sign link and checks the Multisig vote",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "multisig-vote",
          "effect": "reads",
          "facts": [
            "Governance action",
            "Choice",
            "Signatures",
            "Signatures required"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-sign-vote"
        }
      }
    },
    {
      "text": "The DRep signs with their member key",
      "kind": "actor",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-sign-vote"
        }
      }
    },
    {
      "text": "The Product checks the signature belongs to an authorized member and adds it",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "multisig-vote",
          "effect": "changes",
          "facts": [
            "Signatures"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-sign-vote"
        }
      }
    }
  ]
}
---

# Add your signature

## Trigger

A member receives the co-sign link.

## Outcome

The vote counts one more signature.
