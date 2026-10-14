---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens a DRep profile",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "Name",
            "Objectives",
            "Links",
            "Status",
            "Voting power",
            "Delegators",
            "Profile as of"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::drep-profile"
        }
      }
    },
    {
      "text": "The Visitor reads its votes and report card",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "vote",
          "effect": "reads",
          "facts": [
            "Choice",
            "Cast at"
          ]
        },
        {
          "entity": "drep",
          "effect": "reads",
          "facts": [
            "Report card"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::drep-profile"
        }
      }
    }
  ]
}
---

# Read a DRep's record

## Trigger

A delegator checks a DRep before delegating.

## Outcome

The reader sees how the DRep votes and explains itself.

## Edge cases

- A retired DRep stays viewable for its governance history and is marked retired.
