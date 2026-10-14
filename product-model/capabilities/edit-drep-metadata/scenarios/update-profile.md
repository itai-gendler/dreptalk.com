---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep opens Settings, Metadata and edits the prefilled profile",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "Name",
            "Objectives",
            "Motivations",
            "Qualifications",
            "Links",
            "Image",
            "Payment address",
            "Do not list"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::metadata-settings"
        }
      }
    },
    {
      "text": "The Product hosts the new profile document",
      "kind": "product",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::metadata-settings"
        }
      }
    },
    {
      "text": "The DRep signs and submits the update certificate in the wallet",
      "kind": "actor",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::metadata-settings"
        }
      }
    },
    {
      "text": "The Product applies the new profile to the DRep right away",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "drep",
          "effect": "changes",
          "facts": [
            "Name",
            "Objectives",
            "Motivations",
            "Qualifications",
            "Links",
            "Image",
            "Payment address",
            "Do not list"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::metadata-settings"
        }
      }
    }
  ]
}
---

# Update the profile

## Trigger

A DRep's profile is outdated.

## Outcome

The new profile shows on DRepTalk at once; wallets show it after their next sync.

## Edge cases

- Updates need no deposit, only the network fee.
- If the update never confirms, the next DRep sync restores the on-chain profile.
