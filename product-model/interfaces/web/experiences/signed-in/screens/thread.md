---
{
  "entities": [
    {
      "entity": "thread",
      "shows": [
        "Title",
        "Category",
        "Opened by",
        "Address",
        "Title edited",
        "Replies",
        "Written under mandate"
      ],
      "collects": [
        "Title"
      ]
    },
    {
      "entity": "post",
      "shows": [
        "Body",
        "Kind",
        "Reply to",
        "Vote",
        "Ups",
        "Downs",
        "Flags",
        "Edited",
        "Written under mandate",
        "Posted at"
      ],
      "collects": [
        "Body",
        "Reply to"
      ]
    },
    {
      "entity": "governance-action",
      "shows": [
        "Action ID",
        "Type",
        "Title",
        "Abstract",
        "Motivation",
        "Rationale",
        "Authors",
        "References",
        "Proposer address",
        "Deposit",
        "Submitted epoch",
        "Expiry epoch",
        "Decided epoch",
        "On-chain changes",
        "Tallies",
        "Thresholds",
        "Data as of"
      ]
    },
    {
      "entity": "vote",
      "shows": [
        "Voter body",
        "Choice",
        "Cast at",
        "Earlier votes",
        "Counted",
        "Voting power"
      ],
      "collects": [
        "Choice"
      ]
    },
    {
      "entity": "vote-rationale",
      "shows": [
        "Text",
        "Address",
        "Readable"
      ],
      "collects": [
        "Text"
      ]
    },
    {
      "entity": "survey",
      "shows": [
        "Questions",
        "Eligible roles",
        "Closing epoch",
        "Sealed",
        "Tally",
        "Participation count",
        "Excluded responses",
        "Text loaded"
      ]
    },
    {
      "entity": "reaction",
      "shows": [
        "Direction"
      ]
    },
    {
      "entity": "flag",
      "shows": [
        "Raised by"
      ]
    },
    {
      "entity": "survey-response",
      "collects": [
        "Answers"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/t/[slug].astro"
    }
  ]
}
---

# Thread

One thread with its posts. A governance thread adds the action's overview, status, tallies, votes, on-chain data and history; a survey thread adds the survey card; a Proposal Draft lists the actions it is connected to.
