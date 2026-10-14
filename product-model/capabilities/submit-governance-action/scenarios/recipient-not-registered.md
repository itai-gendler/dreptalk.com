---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Proposer enters a recipient stake address that is not registered",
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
      "text": "The Product marks the row and keeps the action from being signed",
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

# A recipient is not a registered stake address

## Trigger

A recipient's stake address is not registered.

## Outcome

The action cannot be signed until the row is fixed or removed.
