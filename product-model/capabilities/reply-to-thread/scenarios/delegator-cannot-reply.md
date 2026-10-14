---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator opens a Thread",
      "kind": "actor",
      "actor": "delegator",
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
      "text": "The Product offers no reply, since the account holds no writer role",
      "kind": "product",
      "actor": "delegator",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": []
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

# A delegator cannot write

## Trigger

A read-only account opens a thread.

## Outcome

No reply box is offered and nothing is posted.

## Edge cases

- A DRep whose registration is no longer active cannot post, react or flag unless it holds another writer role.
