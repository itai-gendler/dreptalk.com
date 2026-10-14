---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator chooses Sign out this device on its row",
      "kind": "actor",
      "actor": "delegator",
      "entities": [
        {
          "entity": "device",
          "effect": "reads",
          "facts": [
            "Label",
            "Last used"
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
      "text": "The Product signs that Device out",
      "kind": "product",
      "actor": "delegator",
      "entities": [
        {
          "entity": "device",
          "effect": "changes",
          "from": "Signed in",
          "to": "Signed out",
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

# Sign out a lost device

## Trigger

A person no longer wants one device signed in.

## Outcome

That device is signed out; revocation may take a moment to reach it.
