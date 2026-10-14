---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The SPO chooses Reply on a post and writes the reply",
      "kind": "actor",
      "actor": "spo",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Body"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    },
    {
      "text": "The Product adds the reply under the top-level Post it answers",
      "kind": "product",
      "actor": "spo",
      "entities": [
        {
          "entity": "post",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Body",
            "Kind",
            "Reply to",
            "Posted at",
            "Written under mandate"
          ]
        },
        {
          "entity": "thread",
          "effect": "changes",
          "facts": [
            "Replies",
            "Last activity"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    },
    {
      "text": "The Product notifies the people mentioned and the other participants of the Thread",
      "kind": "product",
      "actor": "spo",
      "entities": [
        {
          "entity": "notification",
          "effect": "creates",
          "to": "Unread",
          "facts": [
            "Kind",
            "About",
            "From",
            "Created at"
          ]
        },
        {
          "entity": "thread",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    }
  ]
}
---

# Reply to a post

## Trigger

A writer answers someone in a thread.

## Outcome

The reply is in the thread and the participants are notified.

## Edge cases

- A reply to a reply attaches to that reply's own top-level post.
- Someone mentioned is notified once, as a mention, not again as a participant.
- Twenty posts per writer within ten minutes is the most the Product accepts.
