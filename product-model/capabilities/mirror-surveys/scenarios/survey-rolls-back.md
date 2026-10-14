---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "An Open Survey or its linking Governance action rolled back",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "survey",
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
      "text": "The Product marks the Survey unavailable and switches answering off",
      "kind": "product",
      "entities": [
        {
          "entity": "survey",
          "effect": "changes",
          "from": "Open",
          "to": "Unavailable",
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

# A survey's record rolls back

## Trigger

The survey's record, or the action linking it, rolled back.

## Outcome

The thread stays; the card says the record is gone and answering is off.

## Edge cases

- When the survey reappears and still qualifies, the next successful run restores it.
