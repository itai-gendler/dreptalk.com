---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens the Thread",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "thread",
          "effect": "reads",
          "facts": [
            "Title",
            "Category",
            "Opened by"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::thread"
        }
      }
    },
    {
      "text": "The Visitor reads the posts and replies",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Body",
            "Kind",
            "Reply to",
            "Ups",
            "Downs",
            "Edited",
            "Written under mandate"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::thread"
        }
      }
    }
  ]
}
---

# A visitor reads a thread

## Trigger

A visitor opens a thread.

## Outcome

The visitor reads the posts; hidden posts show as placeholders.

## Edge cases

- A vote rationale post is marked frozen and links to its on-chain record.
- A post written under a co-proposer mandate shows the writer's name and the proposer they write for.
