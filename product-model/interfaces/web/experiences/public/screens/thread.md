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
      ]
    },
    {
      "entity": "vote-rationale",
      "shows": [
        "Text",
        "Address",
        "Readable"
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
