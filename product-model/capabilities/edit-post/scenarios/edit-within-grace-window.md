---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep edits their own Post within fifteen minutes of posting",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Body",
            "Posted at"
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
      "text": "The Product replaces the text silently",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "post",
          "effect": "changes",
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
    }
  ]
}
---

# Fix a typo right after posting

## Trigger

The writer edits within fifteen minutes of posting.

## Outcome

The text is replaced with no edited marker.
