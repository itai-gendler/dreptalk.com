---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A DRep registered on chain since the last run",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::dreps"
        }
      }
    },
    {
      "text": "The Product adds the DRep with its profile, and a drep.link built from its name",
      "kind": "product",
      "entities": [
        {
          "entity": "drep",
          "effect": "creates",
          "facts": [
            "DRep ID",
            "Name",
            "Objectives",
            "Links",
            "Image",
            "Status",
            "Voting power",
            "Delegators",
            "Profile as of"
          ]
        },
        {
          "entity": "drep-link",
          "effect": "creates",
          "facts": [
            "Short name"
          ],
          "with": "drep"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::dreps"
        }
      }
    }
  ]
}
---

# A newly registered DRep appears

## Trigger

A DRep registered since the last run.

## Outcome

The DRep has a profile, and a drep.link when its metadata names it.
