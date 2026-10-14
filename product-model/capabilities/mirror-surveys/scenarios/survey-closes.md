---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "An Open Survey passed its closing epoch",
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
      "text": "The Product marks the Survey closed",
      "kind": "product",
      "entities": [
        {
          "entity": "survey",
          "effect": "changes",
          "from": "Open",
          "to": "Closed",
          "facts": [
            "Tally",
            "Participation count"
          ]
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

# A survey closes

## Trigger

The closing epoch passed.

## Outcome

The survey reads Closed; once finalized its figures come from the published tally artifact.
