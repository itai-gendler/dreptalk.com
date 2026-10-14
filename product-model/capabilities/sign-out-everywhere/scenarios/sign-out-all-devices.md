---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator chooses Sign out everywhere, including this device",
      "kind": "actor",
      "actor": "delegator",
      "entities": [
        {
          "entity": "device",
          "effect": "reads",
          "facts": [
            "Label"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::devices"
        }
      }
    },
    {
      "text": "The Product signs every Device of the account out",
      "kind": "product",
      "actor": "delegator",
      "entities": [
        {
          "entity": "device",
          "effect": "changes",
          "from": "Signed in",
          "to": "Signed out",
          "facts": []
        },
        {
          "entity": "account",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::devices"
        }
      }
    }
  ]
}
---

# Sign out every device

## Trigger

A device is lost or the person wants a clean slate.

## Outcome

Every device of the account is signed out.
