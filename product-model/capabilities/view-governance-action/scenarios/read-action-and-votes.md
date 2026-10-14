---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens the Thread of a Governance action and reads its overview and status",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "thread",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": [
            "Title",
            "Type",
            "Abstract",
            "Motivation",
            "Rationale",
            "Authors",
            "References",
            "Proposer address",
            "Deposit",
            "Expiry epoch",
            "Tallies",
            "Thresholds",
            "Data as of"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::thread"
        }
      }
    },
    {
      "text": "The Visitor opens the votes and expands a Vote to read its Vote rationale and earlier votes",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "vote",
          "effect": "reads",
          "facts": [
            "Voter body",
            "Choice",
            "Earlier votes",
            "Counted",
            "Voting power"
          ]
        },
        {
          "entity": "vote-rationale",
          "effect": "reads",
          "facts": [
            "Text",
            "Address",
            "Readable"
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

# A visitor reads an action and its votes

## Trigger

A reader wants to understand an action before discussing it.

## Outcome

The reader knows what is decided, where it stands and why voters voted as they did.

## Edge cases

- A vote whose rationale document could not be read shows Rationale unavailable.
- Votes cast after ratification are listed and marked not counted.
- An action that links a Proposal Draft shows that it was discussed as a draft.
