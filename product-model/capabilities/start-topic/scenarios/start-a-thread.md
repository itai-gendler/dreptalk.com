---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep chooses to start a thread in a discussion category and writes a title and an opening post",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "thread",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "post",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::category"
        }
      }
    },
    {
      "text": "The Product opens the Thread with its opening Post and notifies the people mentioned in it",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "thread",
          "effect": "creates",
          "to": "Open",
          "facts": [
            "Title",
            "Category",
            "Opened by",
            "Address",
            "Replies",
            "Last activity",
            "Written under mandate"
          ]
        },
        {
          "entity": "post",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Body",
            "Kind",
            "Posted at",
            "Written under mandate"
          ],
          "with": "thread"
        },
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
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::category"
        }
      }
    },
    {
      "text": "The Product takes the DRep to the new Thread",
      "kind": "product",
      "actor": "drep",
      "entities": [
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

# Start a thread in a discussion category

## Trigger

A writer wants to raise something for discussion.

## Outcome

The thread is open and the writer lands on it.

## Edge cases

- A co-proposer's thread records the mandate it was written under, permanently.
