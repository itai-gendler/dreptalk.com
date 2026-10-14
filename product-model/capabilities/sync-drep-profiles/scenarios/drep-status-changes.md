---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A followed DRep is no longer registered",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::dreps"
        }
      }
    },
    {
      "text": "The Product marks the DRep retired and notifies the delegators who follow it",
      "kind": "product",
      "entities": [
        {
          "entity": "drep",
          "effect": "changes",
          "facts": [
            "Status"
          ]
        },
        {
          "entity": "notification",
          "effect": "creates",
          "to": "Unread",
          "facts": [
            "Kind",
            "About",
            "Created at"
          ]
        },
        {
          "entity": "delegator",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::dreps"
        }
      }
    }
  ]
}
---

# A followed DRep retires

## Trigger

A DRep that delegators follow left the registered set.

## Outcome

The DRep reads Retired and its followers are notified.
