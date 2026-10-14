---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep edits their own Post after the grace window",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Body",
            "Edited"
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
      "text": "The Product keeps the earlier text as a Post version and publishes the new text as the next version",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "post",
          "effect": "changes",
          "facts": [
            "Body",
            "Edited"
          ]
        },
        {
          "entity": "post-version",
          "effect": "creates",
          "facts": [
            "Text",
            "Address",
            "Published at"
          ]
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

# Edit an older post

## Trigger

The writer edits after the grace window.

## Outcome

The post carries the new text and an edited marker; every earlier version stays citable.

## Edge cases

- Mentions added in an edit notify nobody.
