---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A DRep's profile or voting power changed on chain",
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
      "text": "The Product updates the DRep",
      "kind": "product",
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
            "Do not list",
            "Voting power",
            "Delegators",
            "Profile as of"
          ]
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

# Refresh profiles and voting power

## Trigger

The six-hourly run is due.

## Outcome

Profiles, voting power and delegator counts are current as of the run.

## Edge cases

- Profile documents beyond a run's budget are read on the following runs.
