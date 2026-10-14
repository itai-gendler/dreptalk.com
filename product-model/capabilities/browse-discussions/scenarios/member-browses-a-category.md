---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator opens a category from Discussions",
      "kind": "actor",
      "actor": "delegator",
      "entities": [
        {
          "entity": "thread",
          "effect": "reads",
          "facts": [
            "Title",
            "Opened by",
            "Replies",
            "Last activity"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::category"
        }
      }
    }
  ]
}
---

# A signed-in person opens a category

## Trigger

A signed-in person looks for a thread.

## Outcome

The person sees the category's threads.

## Edge cases

- The Surveys category exists only on a deployment that mirrors surveys.
