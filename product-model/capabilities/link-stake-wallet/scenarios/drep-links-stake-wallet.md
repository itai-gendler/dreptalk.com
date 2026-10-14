---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep opens Settings, Account, connects the stake wallet and signs the one-time challenge with its reward address",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::account-settings"
        }
      }
    },
    {
      "text": "The Product verifies the signature and links the stake address to the Account",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Linked stake address"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::account-settings"
        }
      }
    },
    {
      "text": "The Product starts following the Delegation of that stake address",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "delegation",
          "effect": "creates",
          "to": "Looking up",
          "facts": [
            "Stake address"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::account-settings"
        }
      }
    }
  ]
}
---

# A DRep links the wallet that holds its own ada

## Trigger

A DRep wants to follow its personal delegation on the start page.

## Outcome

The stake wallet is linked and its Delegation is followed.
