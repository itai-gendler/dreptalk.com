---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A Pending Vote has not appeared on chain after the authoritative sync",
      "kind": "condition",
      "unattended": true,
      "entities": [
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
      "text": "The Product marks the Vote failed and removes its cross-posted rationale Post",
      "kind": "product",
      "entities": [
        {
          "entity": "vote",
          "effect": "changes",
          "from": "Pending",
          "to": "Failed",
          "facts": []
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
          "place": "web::public::thread"
        }
      }
    }
  ]
}
---

# A vote never confirms

## Trigger

A vote cast here does not appear on chain in time.

## Outcome

The vote is marked failed and its cross-posted rationale leaves the discussion.
