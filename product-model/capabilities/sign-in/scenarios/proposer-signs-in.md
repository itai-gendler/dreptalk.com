---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor picks the Proposer role, connects a wallet and signs the challenge with its reward address",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "proposer",
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
      "text": "The Product confirms on chain that this reward address submitted at least one governance action",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "proposer",
          "effect": "reads",
          "facts": [
            "Reward address"
          ]
        },
        {
          "entity": "governance-action",
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
      "text": "The Product signs the device in as a proposer",
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
          "entity": "proposer",
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

# A proposer or co-proposer signs in with a reward address

## Trigger

A proposer, or a co-proposer the proposer authorized, wants to write.

## Outcome

The device is signed in as a proposer, or as a co-proposer writing for its proposer.

## Decision points

### Proposer or co-proposer

Did this reward address submit a governance action?

- It did → the device signs in as the proposer.
- It did not, but the address holds an active co-proposer mandate → the device signs in as a co-proposer writing for that proposer.
