---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Proposer reviews a treasury withdrawal and goes to sign",
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
      "text": "The guardrails script rejects the action",
      "kind": "condition",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::submit-governance-action"
        }
      }
    },
    {
      "text": "The Product stops before the wallet signs and shows the rejection",
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

# The guardrails script rejects the action

## Trigger

The guardrails script rejects the withdrawal or parameter change.

## Outcome

Nothing is signed; the page says the script rejected it and shows its error under Details.

## Edge cases

- When the Product cannot confirm which guardrails script the constitution uses, nothing is published or signed.
