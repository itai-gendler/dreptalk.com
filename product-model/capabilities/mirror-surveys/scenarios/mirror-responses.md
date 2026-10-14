---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The index holds new responses to a mirrored Survey",
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
      "text": "The Product records each Survey response and recounts the informational tally of DRep responses",
      "kind": "product",
      "entities": [
        {
          "entity": "survey-response",
          "effect": "creates",
          "facts": [
            "Answers",
            "Counted",
            "Transaction"
          ]
        },
        {
          "entity": "survey",
          "effect": "changes",
          "facts": [
            "Tally",
            "Participation count",
            "Excluded responses"
          ]
        },
        {
          "entity": "drep",
          "effect": "reads",
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

# Mirror new responses and the tally

## Trigger

The index saw new survey responses.

## Outcome

The card shows the responses counted, the excluded ones with reasons, and the informational tally.

## Edge cases

- While the survey is open the weighting uses the newest DRep voting power on record, so the figures move.
- Responses whose credential proof is not checked yet still count, provisionally.
