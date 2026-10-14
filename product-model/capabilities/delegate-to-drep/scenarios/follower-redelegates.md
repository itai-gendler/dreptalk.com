---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator chooses Delegate on another DRep profile and signs the certificate with the followed wallet",
      "kind": "actor",
      "actor": "delegator",
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "Name"
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
      "text": "The Product records the expected change on the followed Delegation",
      "kind": "product",
      "actor": "delegator",
      "entities": [
        {
          "entity": "delegation",
          "effect": "changes",
          "facts": [
            "Delegated to",
            "Last checked"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::drep-profile"
        }
      }
    }
  ]
}
---

# A signed-in delegator re-delegates

## Trigger

A delegator moves to another DRep with the wallet it follows.

## Outcome

The followed Delegation points at the new DRep without a needless change notification.

## Edge cases

- When the wallet belongs to another account, the offer says that signing in with it switches accounts.
- A writer with no stake wallet linked is pointed to Settings, Account.
