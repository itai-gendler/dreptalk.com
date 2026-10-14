---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens the invite link, picks a display name and connects their own wallet",
      "kind": "actor",
      "actor": "visitor",
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
          "place": "web::public::co-proposer-invite"
        }
      }
    },
    {
      "text": "The Visitor signs the one-time confirmation with the wallet's reward address",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::co-proposer-invite"
        }
      }
    },
    {
      "text": "The Product activates the mandate, keeps the chosen name where the Account has none, and signs the device in as a co-proposer",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "co-proposer-mandate",
          "effect": "changes",
          "from": "Pending",
          "to": "Active",
          "facts": [
            "Accepted at"
          ]
        },
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Display name"
          ]
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
          "entity": "co-proposer",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::co-proposer-invite"
        }
      }
    }
  ]
}
---

# Accept an invite with your own wallet

## Trigger

A colleague opens the invite link a proposer shared.

## Outcome

The mandate is active and the device is signed in as a co-proposer; later sign-ins go through the proposer sign-in.
