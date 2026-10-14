---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep opens the Survey thread and connects the wallet holding its DRep key",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "survey",
          "effect": "reads",
          "facts": [
            "Questions",
            "Closing epoch",
            "Sealed"
          ]
        },
        {
          "entity": "thread",
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
      "text": "The Product checks that the wallet holds the same DRep key the DRep signed in with and opens the form",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "DRep ID"
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
      "text": "The DRep answers the questions and reads what signing puts on chain",
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
      "text": "The DRep signs and submits the answer in the wallet",
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
      "text": "The Product shows the transaction hash",
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

# Answer an open survey

## Trigger

A DRep wants to answer the survey linked to a proposal.

## Outcome

The transaction hash is shown with an explorer link; the counts move after the next mirror run.

## Edge cases

- Answering again while the survey is open replaces the earlier answer in full and costs another fee.
- An answer sent after the closing epoch is not counted, although its fee is spent.
- On a sealed survey the answers stay encrypted until the reveal time; the credential and role are public at once.
