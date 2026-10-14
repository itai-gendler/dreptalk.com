---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator chooses Sign out",
      "kind": "actor",
      "actor": "delegator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in"
        }
      }
    },
    {
      "text": "The Product signs this Device out",
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
          "place": "web::signed-in"
        }
      }
    }
  ]
}
---

# Sign out of this device

## Trigger

A person is done on this device.

## Outcome

This device is signed out; others stay signed in.
