---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator opens Settings, Devices and enters the code shown on the phone",
      "kind": "actor",
      "actor": "delegator",
      "entities": [
        {
          "entity": "pairing-code",
          "effect": "reads",
          "facts": [
            "Device label"
          ]
        },
        {
          "entity": "device",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::devices"
        }
      }
    },
    {
      "text": "The Delegator checks the device shown and confirms",
      "kind": "actor",
      "actor": "delegator",
      "entities": [
        {
          "entity": "device",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::devices"
        }
      }
    },
    {
      "text": "The Product approves the Pairing code for this account, capped at the roles this device holds, and adds a device-paired Notification",
      "kind": "product",
      "actor": "delegator",
      "entities": [
        {
          "entity": "pairing-code",
          "effect": "changes",
          "from": "Waiting",
          "to": "Approved",
          "facts": []
        },
        {
          "entity": "notification",
          "effect": "creates",
          "to": "Unread",
          "facts": [
            "Kind",
            "Created at"
          ]
        },
        {
          "entity": "account",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "device",
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

# Approve the code a phone shows

## Trigger

A person's phone shows a pairing code.

## Outcome

The code is approved and the account receives a device-paired notice.
