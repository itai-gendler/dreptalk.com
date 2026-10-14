---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Proposer picks Info action and writes the title, abstract, motivation, rationale and references",
      "kind": "actor",
      "actor": "proposer",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::submit-governance-action"
        }
      }
    },
    {
      "text": "The Proposer links their Proposal Draft Thread and keeps Sign as author on with their name",
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
          "place": "web::signed-in::submit-governance-action"
        }
      }
    },
    {
      "text": "The Proposer opens Review, checks the action as its page will show it, and connects a wallet",
      "kind": "actor",
      "actor": "proposer",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::submit-governance-action"
        }
      }
    },
    {
      "text": "The Product shows the deposit beside the wallet's balance, publishes the metadata on IPFS and checks the published file against its hash",
      "kind": "product",
      "actor": "proposer",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::submit-governance-action"
        }
      }
    },
    {
      "text": "The Proposer signs and submits the transaction in the wallet",
      "kind": "actor",
      "actor": "proposer",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::submit-governance-action"
        }
      }
    },
    {
      "text": "The Product shows the transaction hash",
      "kind": "product",
      "actor": "proposer",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::submit-governance-action"
        }
      }
    }
  ]
}
---

# Submit an info action with a linked draft

## Trigger

A proposer is ready to put a discussed proposal on chain.

## Outcome

The transaction hash is shown; the action gets its thread once it is in a block.

## Edge cases

- The form is kept in the browser as it is typed, without wallet data.
- Motions of no confidence, hard forks, new constitutions and committee updates build on the last action of their kind, which the Product fills in.
