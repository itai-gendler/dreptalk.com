---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep chooses to submit a Multisig vote with enough signatures",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "multisig-vote",
          "effect": "reads",
          "facts": [
            "Signatures",
            "Signatures required"
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
      "text": "The Product assembles the signatures into the transaction and the DRep's wallet signs and submits it",
      "kind": "product",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-sign-vote"
        }
      }
    },
    {
      "text": "The Product marks the Multisig vote submitted and shows the Vote as pending",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "multisig-vote",
          "effect": "changes",
          "from": "Collecting",
          "to": "Submitted",
          "facts": [
            "Transaction"
          ]
        },
        {
          "entity": "vote",
          "effect": "creates",
          "to": "Pending",
          "facts": [
            "Voter body",
            "Choice",
            "Cast at",
            "Transaction"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-sign-vote"
        }
      }
    }
  ]
}
---

# Submit a fully signed vote

## Trigger

The script's signature requirement is met.

## Outcome

The vote is submitted and shows as pending until the chain confirms it.
