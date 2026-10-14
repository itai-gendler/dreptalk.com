---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Proposer edits the title of a Thread they opened",
      "kind": "actor",
      "actor": "proposer",
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
      "text": "The Product sets the new title and the edited marker, keeping the address",
      "kind": "product",
      "actor": "proposer",
      "entities": [
        {
          "entity": "thread",
          "effect": "changes",
          "facts": [
            "Title",
            "Title edited"
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

# Retitle your thread

## Trigger

The thread's author wants a better title.

## Outcome

The thread shows the new title marked as edited; links keep working.

## Edge cases

- Governance action and survey threads take their title from the chain and cannot be retitled.
