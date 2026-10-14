---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens Discussions and reads the recent activity",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "thread",
          "effect": "reads",
          "facts": [
            "Title",
            "Category",
            "Last activity"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::discussions"
        }
      }
    },
    {
      "text": "The Visitor opens a category",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "thread",
          "effect": "reads",
          "facts": [
            "Title",
            "Replies",
            "Last activity"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::category"
        }
      }
    }
  ]
}
---

# A visitor browses the discussions

## Trigger

A visitor wants to see what is being discussed.

## Outcome

The visitor sees the threads of the category.
