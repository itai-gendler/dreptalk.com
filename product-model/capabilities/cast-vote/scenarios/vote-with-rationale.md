---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep chooses Yes on the Governance action, writes a rationale and ticks the box to also post it under the discussion",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Title",
            "Expiry epoch"
          ]
        },
        {
          "entity": "post",
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
      "text": "The Product hosts the Vote rationale at an address named by its hash and shows the link before signing",
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
      "text": "The Product shows the Vote as pending and posts the frozen rationale copy in the Thread",
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
        },
        {
          "entity": "post",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Body",
            "Kind",
            "Vote",
            "Posted at"
          ]
        },
        {
          "entity": "thread",
          "effect": "changes",
          "facts": [
            "Replies",
            "Last activity"
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

# Vote with a rationale and post it under the discussion

## Trigger

A DRep decides on an open action.

## Outcome

The vote shows at once as pending, the rationale is linked on chain, and a frozen copy is in the discussion.

## Edge cases

- The cross-post is off by default; without it no discussion post is made.
- A paired phone cannot vote; votes are signed from a wallet, on a computer or in a wallet's in-app browser.
- A rationale holds at most 60,000 characters.
