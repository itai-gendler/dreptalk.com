---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The index rules an Open Survey untalliable",
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
      "text": "The Product marks the Survey as having an invalid definition",
      "kind": "product",
      "entities": [
        {
          "entity": "survey",
          "effect": "changes",
          "from": "Open",
          "to": "Invalid definition",
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

# The index rules a survey untalliable

## Trigger

The index decided the survey cannot be tallied.

## Outcome

The survey reads Invalid definition.
