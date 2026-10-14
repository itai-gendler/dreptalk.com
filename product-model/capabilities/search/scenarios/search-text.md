---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor enters words in Search",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::search"
        }
      }
    },
    {
      "text": "The Product lists the matching threads, posts, governance actions and DReps",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "thread",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Body"
          ]
        },
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::search"
        }
      }
    }
  ]
}
---

# Search for a topic

## Trigger

A reader looks for a discussion.

## Outcome

The reader sees matching threads, posts, actions and DReps.

## Edge cases

- Hidden and deleted posts are not found.
