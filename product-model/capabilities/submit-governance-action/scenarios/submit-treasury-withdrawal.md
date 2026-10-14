---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Proposer picks Treasury withdrawal and adds up to 20 recipients with their amounts",
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
      "text": "The Product checks that every recipient is a registered stake address and shows the exact total",
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
      "text": "The Product runs the constitution's guardrails script against the withdrawal before the wallet signs",
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
    }
  ]
}
---

# Submit a treasury withdrawal the guardrails accept

## Trigger

A proposer asks the treasury to pay registered stake addresses.

## Outcome

The withdrawal is submitted after the guardrails script accepted it.

## Edge cases

- The transaction needs about 5 ada in plain-ada UTxOs as collateral.
- A staking parameter change offers the five staking parameters, blocks values outside the constitution's range or equal to the current one, and is checked by the guardrails script the same way.
