---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep flags a Post two other writers have flagged",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Flags"
          ]
        },
        {
          "entity": "flag",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    },
    {
      "text": "The Product records the Flag and hides the Post",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "flag",
          "effect": "creates",
          "facts": [
            "Raised by"
          ]
        },
        {
          "entity": "post",
          "effect": "changes",
          "from": "Visible",
          "to": "Hidden",
          "facts": [
            "Flags"
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

# The third flag hides the post

## Trigger

Two other writers already flagged the post.

## Outcome

The post is hidden behind a placeholder; its author and moderators can still read it.
