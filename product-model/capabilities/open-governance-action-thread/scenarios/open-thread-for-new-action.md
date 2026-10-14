---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A new Governance action is on chain and its proposal document can be read and matches its hash",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "governance-action",
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
      "text": "The Product stores the Governance action and opens its Thread with an opening Post written from the proposal",
      "kind": "product",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "creates",
          "to": "Syncing",
          "facts": [
            "Action ID",
            "Type",
            "Title",
            "Abstract",
            "Motivation",
            "Rationale",
            "Authors",
            "References",
            "Proposer address",
            "Deposit",
            "Submitted epoch",
            "Expiry epoch",
            "On-chain changes"
          ]
        },
        {
          "entity": "thread",
          "effect": "creates",
          "to": "Open",
          "facts": [
            "Title",
            "Category",
            "Opened by",
            "Address"
          ],
          "with": "governance-action"
        },
        {
          "entity": "post",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Body",
            "Kind",
            "Posted at"
          ],
          "with": "thread"
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

# Open the thread of a new action

## Trigger

A new governance action appeared on chain.

## Outcome

The action has its thread, opened by the Product, within minutes.

## Edge cases

- The opening post is dated to the action's submission, not to when the Product found it.
