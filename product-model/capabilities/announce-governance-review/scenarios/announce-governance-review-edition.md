---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A Governance Review edition went live that was not announced yet",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "governance-review-edition",
          "effect": "reads",
          "facts": [
            "Title"
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
      "text": "The Product writes every account a Notification about it and marks it announced",
      "kind": "product",
      "entities": [
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
          "entity": "governance-review-edition",
          "effect": "changes",
          "facts": [
            "Announced"
          ]
        },
        {
          "entity": "account",
          "effect": "reads",
          "facts": []
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

# Announce a new edition

## Trigger

A new edition was published.

## Outcome

Every account has a Governance Review notification.

## Edge cases

- A correction to an existing edition sends nothing.
- The Governance Review switch in the notification settings keeps it off push and Telegram.
