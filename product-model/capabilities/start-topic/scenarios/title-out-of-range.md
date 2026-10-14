---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep submits a title outside 3 to 200 characters",
      "kind": "actor",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::category"
        }
      }
    },
    {
      "text": "The Product refuses the thread",
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
          "place": "web::signed-in::category"
        }
      }
    }
  ]
}
---

# A title that is too short or too long

## Trigger

The title has fewer than 3 or more than 200 characters.

## Outcome

No thread is opened.

## Edge cases

- Five new threads per writer within ten minutes is the most the Product accepts.
- Governance Actions and Surveys take no threads from people.
