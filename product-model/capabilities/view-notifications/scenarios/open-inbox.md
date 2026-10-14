---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator opens Notifications",
      "kind": "actor",
      "actor": "delegator",
      "entities": [
        {
          "entity": "notification",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::notifications"
        }
      }
    },
    {
      "text": "The Product lists the Notifications newest first with the unread ones highlighted",
      "kind": "product",
      "actor": "delegator",
      "entities": [
        {
          "entity": "notification",
          "effect": "reads",
          "facts": [
            "Kind",
            "About",
            "From",
            "Created at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::notifications"
        }
      }
    },
    {
      "text": "The Product marks every Notification read",
      "kind": "product",
      "actor": "delegator",
      "entities": [
        {
          "entity": "notification",
          "effect": "changes",
          "from": "Unread",
          "to": "Read",
          "facts": []
        },
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Inbox last opened"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::notifications"
        }
      }
    }
  ]
}
---

# Open the inbox

## Trigger

The bell shows unread notifications.

## Outcome

The person sees what is new, highlighted as before the visit, and everything is now read.
