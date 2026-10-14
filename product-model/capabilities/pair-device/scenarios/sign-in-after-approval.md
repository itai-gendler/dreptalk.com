---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor keeps the phone on its pairing code",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "pairing-code",
          "effect": "reads",
          "facts": [
            "Code"
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
      "text": "The Pairing code shown on the phone was approved from a signed-in computer",
      "kind": "condition",
      "entities": [
        {
          "entity": "pairing-code",
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
      "text": "The Product picks up the approval and signs the phone in with the approving account's roles",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "pairing-code",
          "effect": "changes",
          "from": "Approved",
          "to": "Used",
          "facts": []
        },
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

# The phone signs itself in once approved

## Trigger

The code was approved on a computer signed in to the account.

## Outcome

The phone is signed in to the account without handling a key.

## Edge cases

- A paired device can read, post and comment, but cannot vote, since it has no wallet to sign with.
