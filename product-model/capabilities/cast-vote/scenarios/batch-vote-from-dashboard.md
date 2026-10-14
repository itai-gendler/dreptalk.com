---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep picks Yes, No or Abstain in the rows of several open Governance actions on the Voting Dashboard",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::voting-dashboard"
        }
      }
    },
    {
      "text": "The DRep opens Review & submit, adds one shared rationale and a custom one for a single action",
      "kind": "actor",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::voting-dashboard"
        }
      }
    },
    {
      "text": "The Product re-checks that every selected action still accepts votes and hosts each distinct Vote rationale once",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "vote-rationale",
          "effect": "creates",
          "facts": [
            "Text",
            "Address",
            "Source",
            "Readable"
          ]
        },
        {
          "entity": "vote",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::voting-dashboard"
        }
      }
    },
    {
      "text": "The DRep approves the one transaction in the wallet",
      "kind": "actor",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::voting-dashboard"
        }
      }
    },
    {
      "text": "The Product shows every Vote of the batch as pending",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "vote",
          "effect": "creates",
          "to": "Pending",
          "facts": [
            "Voter body",
            "Choice",
            "Rationale link",
            "Cast at",
            "Transaction"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::voting-dashboard"
        }
      }
    }
  ]
}
---

# Vote on several actions in one transaction

## Trigger

Several actions are open at once.

## Outcome

Every selected vote is cast in one transaction with one signature and one fee.

## Edge cases

- Selections and rationale drafts stay in the browser until the transaction is submitted.
- The bar warns when a selection would replace one of the DRep's earlier votes.
- An action that stopped accepting votes is removed from the batch with a notice before signing.
