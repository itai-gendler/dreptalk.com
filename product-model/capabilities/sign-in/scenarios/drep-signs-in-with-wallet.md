---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor picks the DRep role and connects a CIP-95 capable wallet",
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
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The Visitor signs the one-time challenge with their DRep key in the wallet",
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
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The Product derives the DRep ID from the signature and confirms on chain that it belongs to a registered, active DRep",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "DRep ID",
            "Status"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The Product signs the device in to the Account for that DRep, creating the Account at the first sign-in",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "device",
          "effect": "creates",
          "to": "Signed in",
          "facts": [
            "Label",
            "Signed in at",
            "Roles"
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
          "place": "web::public::sign-in"
        }
      }
    }
  ]
}
---

# A DRep signs in with a CIP-95 wallet

## Trigger

A DRep wants to write or vote on DRepTalk.

## Outcome

The device is signed in as the DRep and lands on the start page, or on the page that sent them to sign in.

## Decision points

### Returning or new

Does an Account for this DRep exist yet?

- It exists → the device signs in to it.
- It does not → the Product creates it first, then signs the device in.
