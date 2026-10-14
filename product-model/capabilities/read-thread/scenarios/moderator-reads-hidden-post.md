---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator opens the Thread",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "thread",
          "effect": "reads",
          "facts": [
            "Title"
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
      "text": "The Moderator reads the text of a hidden Post",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Body",
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

# A moderator reads a hidden post

## Trigger

A moderator checks a post the community hid.

## Outcome

The moderator reads the hidden post's text.
