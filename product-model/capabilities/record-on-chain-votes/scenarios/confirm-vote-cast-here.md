---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A Pending Vote appears on chain",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "vote",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::thread"
        }
      }
    },
    {
      "text": "The Product confirms the Vote and notifies the DRep that its rationale is ready",
      "kind": "product",
      "entities": [
        {
          "entity": "vote",
          "effect": "changes",
          "from": "Pending",
          "to": "Confirmed",
          "facts": [
            "Voting power"
          ]
        },
        {
          "entity": "notification",
          "effect": "creates",
          "to": "Unread",
          "facts": [
            "Kind",
            "About",
            "Created at"
          ]
        },
        {
          "entity": "drep",
          "effect": "reads",
          "facts": []
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

# Confirm a vote cast through DRepTalk

## Trigger

A DRep's vote cast here appears on chain.

## Outcome

The vote is confirmed, and the DRep hears that its rationale is ready.
