---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "An epoch ended in which a followed DRep voted",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "vote",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "drep",
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
      "text": "The Product writes each follower an epoch summary Notification",
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

# Summarize the DRep's epoch

## Trigger

An epoch ended in which the followed DRep voted.

## Outcome

The summary is in the inbox; push and Telegram carry it only when switched on.

## Edge cases

- Nothing is sent for an epoch without votes.
