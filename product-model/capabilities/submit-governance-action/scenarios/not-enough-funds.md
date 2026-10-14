---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Proposer connects a wallet holding less than the deposit and fee",
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
      "text": "The Product shows how much is missing",
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

# The wallet cannot pay the deposit

## Trigger

The wallet holds less than the deposit plus the fee.

## Outcome

Nothing is signed; the page says how much is missing.
