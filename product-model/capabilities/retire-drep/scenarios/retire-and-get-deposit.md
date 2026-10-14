---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep chooses Retire DRep in the Danger Zone",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "DRep ID",
            "Status"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::danger-zone"
        }
      }
    },
    {
      "text": "The DRep signs and submits the deregistration certificate in the wallet",
      "kind": "actor",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::danger-zone"
        }
      }
    },
    {
      "text": "The Product confirms the submission",
      "kind": "product",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::danger-zone"
        }
      }
    }
  ]
}
---

# Retire and get the deposit back

## Trigger

A DRep stops representing delegators.

## Outcome

The deregistration is submitted; after the next DRep sync the DRep reads Retired.

## Edge cases

- Everyone who delegated to the DRep loses that delegation.
