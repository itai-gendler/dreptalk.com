---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Post is a vote rationale",
      "kind": "condition",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Kind"
          ]
        },
        {
          "entity": "vote-rationale",
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
      "text": "The DRep looks for an edit control on it",
      "kind": "actor",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    },
    {
      "text": "The Product offers no edit for it",
      "kind": "product",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    }
  ]
}
---

# A vote rationale cannot be edited

## Trigger

The post is a cross-posted vote rationale.

## Outcome

Nothing changes; the post matches what was committed on chain.

## Edge cases

- A hidden post, a post in a closed draft and a post written under another mandate cannot be edited either.
