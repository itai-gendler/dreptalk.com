---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep signs with a stake wallet another Account already owns",
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
      "text": "The Product refuses to link it",
      "kind": "product",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::account-settings"
        }
      }
    }
  ]
}
---

# A stake wallet of another account is refused

## Trigger

The stake wallet already belongs to a different account.

## Outcome

Nothing is linked.
