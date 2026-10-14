---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "New votes on a mirrored Governance action are on chain",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": []
        },
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
      "text": "The Product records each Vote and reads its Vote rationale when the voter holds at least 10,000 ada of voting weight",
      "kind": "product",
      "entities": [
        {
          "entity": "vote",
          "effect": "creates",
          "to": "Confirmed",
          "facts": [
            "Voter body",
            "Choice",
            "Rationale link",
            "Cast at",
            "Voting power",
            "Counted",
            "Transaction"
          ]
        },
        {
          "entity": "vote-rationale",
          "effect": "creates",
          "facts": [
            "Text",
            "Address",
            "Source",
            "Readable"
          ],
          "with": "vote"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::thread"
        }
      }
    },
    {
      "text": "The Product notifies the delegators who follow the DRep that it voted",
      "kind": "product",
      "entities": [
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
          "entity": "delegator",
          "effect": "reads",
          "facts": []
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

# Record votes cast on chain

## Trigger

Votes were cast on chain since the last run.

## Outcome

The votes appear on the action, and the voters' delegators are notified.

## Edge cases

- A later vote by the same voter replaces the earlier one, which stays listed as Changed or Revoted.
- A vote cast after the action was ratified is marked not counted.
