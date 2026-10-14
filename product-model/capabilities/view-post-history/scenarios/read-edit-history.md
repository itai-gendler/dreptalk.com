---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens the history of an edited Post",
      "kind": "actor",
      "actor": "visitor",
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
          "place": "web::post-history"
        }
      }
    },
    {
      "text": "The Visitor reads the earlier versions and the changes between them",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "post-version",
          "effect": "reads",
          "facts": [
            "Text",
            "Replaced at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::post-history"
        }
      }
    }
  ]
}
---

# Read what changed in a post

## Trigger

A reader wonders what an edited post said before.

## Outcome

The reader sees every version with the changes.

## Edge cases

- The history of a hidden post is shown only to its author and to moderators.
