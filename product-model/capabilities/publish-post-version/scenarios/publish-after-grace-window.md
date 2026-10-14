---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A public Post's grace window has closed and its current text has no version yet",
      "kind": "condition",
      "unattended": true,
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
          "place": "web::citation"
        }
      }
    },
    {
      "text": "The Product publishes the text as a Post version",
      "kind": "product",
      "entities": [
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
          "place": "web::citation"
        }
      }
    }
  ]
}
---

# Publish a version once the grace window closes

## Trigger

A post's grace window closed since the last run.

## Outcome

The post has a citable version.
