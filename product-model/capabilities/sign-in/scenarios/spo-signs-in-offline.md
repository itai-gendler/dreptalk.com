---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor picks the SPO role and copies the one-time challenge",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "spo",
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
      "text": "The Visitor signs the challenge offline with cardano-signer and pastes the signature and public key",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The Product matches the Calidus public key on chain to a registered pool",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "spo",
          "effect": "reads",
          "facts": [
            "Pool ID"
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
      "text": "The Product signs the device in to the Account for that pool",
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

# An SPO signs in with its Calidus key

## Trigger

An SPO wants to join the discussion; wallets cannot sign with a Calidus key.

## Outcome

The device is signed in as the SPO.

## Edge cases

- A CC member signs in the same way with the committee hot key; the Product confirms it is a currently authorized hot credential.
- A key-based DRep without a browser wallet can use the same offline path with its DRep key.
