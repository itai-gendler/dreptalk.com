---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor picks the Delegator role, connects any CIP-30 wallet and signs the challenge with its stake key",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "delegator",
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
      "text": "The Product signs the device in read-only to the Account that owns this stake address, and starts following its Delegation",
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
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The Product reads the Delegation from the chain",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "delegation",
          "effect": "changes",
          "from": "Looking up",
          "to": "Tracked",
          "facts": [
            "Delegated to",
            "Last checked"
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

# A delegator signs in read-only

## Trigger

An ada holder wants to follow their DRep.

## Outcome

The device is signed in read-only, and the start page shows the delegation once it is read from the chain.

## Edge cases

- A wallet that reaches the Delegator sign-in for an account that is also a DRep still signs in read-only; writing needs the writer sign-in.
- When the chain cannot be read, the sign-in still succeeds and the Delegation stays Looking up.
