---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A deleted Post was deleted thirty days ago",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::citation"
        }
      }
    },
    {
      "text": "The Product erases the Post's text, its versions and its search entry",
      "kind": "product",
      "entities": [
        {
          "entity": "post",
          "effect": "changes",
          "from": "Deleted",
          "to": "Erased",
          "facts": [
            "Body"
          ]
        },
        {
          "entity": "post-version",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::citation"
        }
      }
    }
  ]
}
---

# Erase a post thirty days after deletion

## Trigger

Thirty days have passed since a post was deleted.

## Outcome

The post's text and versions are gone for good.
