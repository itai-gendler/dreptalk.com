---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep chooses No on an open Governance action it voted Yes on and leaves the discussion copy unticked",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "vote",
          "effect": "reads",
          "facts": [
            "Choice"
          ]
        },
        {
          "entity": "governance-action",
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
      "text": "The DRep approves the transaction in the wallet",
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
      "text": "The Product shows the new Vote as pending, keeps the earlier one listed, and removes the earlier cross-posted rationale Post",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "vote",
          "effect": "changes",
          "from": "Confirmed",
          "to": "Pending",
          "facts": [
            "Choice",
            "Earlier votes",
            "Cast at",
            "Transaction"
          ]
        },
        {
          "entity": "post",
          "effect": "changes",
          "from": "Visible",
          "to": "Deleted",
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

# Change a vote while the action is open

## Trigger

A DRep votes again on an action it already voted on.

## Outcome

The later vote replaces the earlier one; a stale cross-post is replaced or removed.

## Edge cases

- Once an action closes, votes are final.
