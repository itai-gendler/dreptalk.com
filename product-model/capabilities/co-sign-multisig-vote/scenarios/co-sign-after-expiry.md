---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep opens the co-sign link of an expired Multisig vote",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "multisig-vote",
          "effect": "reads",
          "facts": [
            "Expires at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-sign-vote"
        }
      }
    },
    {
      "text": "The Product refuses further signatures",
      "kind": "product",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-sign-vote"
        }
      }
    }
  ]
}
---

# The vote expired

## Trigger

More than 36 hours passed since the vote was started.

## Outcome

No signature is added.
