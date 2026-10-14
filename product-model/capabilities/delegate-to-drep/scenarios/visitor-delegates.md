---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor chooses Delegate on the DRep profile and connects a wallet",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "Name",
            "Status"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::drep-profile"
        }
      }
    },
    {
      "text": "The Visitor signs and submits the certificate that delegates to this DRep in the wallet",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::drep-profile"
        }
      }
    },
    {
      "text": "The Product offers to sign in with the wallet that just delegated",
      "kind": "product",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::drep-profile"
        }
      }
    }
  ]
}
---

# Delegate without an account

## Trigger

A visitor chose a DRep.

## Outcome

The delegation is submitted; the Product offers to sign in with the delegating wallet to follow it.

## Edge cases

- A retired DRep has no Delegate button.
