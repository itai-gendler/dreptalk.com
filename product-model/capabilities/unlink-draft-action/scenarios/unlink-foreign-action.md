---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Proposer chooses \"Not your action? Unlink\" next to a connected Governance action on their draft",
      "kind": "actor",
      "actor": "proposer",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Title",
            "Type"
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
      "text": "The Product detaches the Governance action and marks it never to be linked to this draft again",
      "kind": "product",
      "actor": "proposer",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "changes",
          "facts": [
            "Draft link refused"
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
      "text": "The Product reopens the draft Thread for replies",
      "kind": "product",
      "actor": "proposer",
      "entities": [
        {
          "entity": "thread",
          "effect": "changes",
          "from": "Closed",
          "to": "Open",
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

# Detach someone else's action

## Trigger

Another proposer's action linked the draft.

## Outcome

The action is detached for good, and the draft reopens once no connected action remains.

## Edge cases

- When another action is still connected, the draft stays closed.
- An author whose writer role has lapsed can still unlink.
