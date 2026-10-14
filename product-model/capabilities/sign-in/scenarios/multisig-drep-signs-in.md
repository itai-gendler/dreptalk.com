---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor turns on \"This is a multisig / script DRep\", enters the script DRep ID and signs the challenge with one member key",
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
      "text": "The Product confirms on chain that the key is one of the script's authorized keys",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "DRep ID",
            "Script DRep"
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
      "text": "The Product signs the device in as that DRep",
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

# A member of a multisig DRep signs in

## Trigger

A member of a native-script DRep wants to act for that DRep.

## Outcome

The device is signed in as the script DRep.

## Edge cases

- A key on a Ledger or Trezor signs through the cardano-hw-cli command the page shows, and the Visitor pastes the file it writes.
