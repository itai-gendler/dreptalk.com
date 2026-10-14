---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The owner withdrew an Open Survey before it closed",
      "kind": "condition",
      "unattended": true,
      "entities": [
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
      "text": "The Product marks the Survey cancelled",
      "kind": "product",
      "entities": [
        {
          "entity": "survey",
          "effect": "changes",
          "from": "Open",
          "to": "Cancelled",
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

# A survey is cancelled

## Trigger

The owner withdrew the survey.

## Outcome

The survey reads Cancelled and its count says No count.
