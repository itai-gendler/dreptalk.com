---
{
  "entities": [
    {
      "entity": "governance-action",
      "shows": [
        "Title",
        "Type",
        "Expiry epoch",
        "Tallies"
      ]
    },
    {
      "entity": "vote",
      "shows": [
        "Choice",
        "Cast at"
      ],
      "collects": [
        "Choice"
      ]
    },
    {
      "entity": "vote-rationale",
      "collects": [
        "Text"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/vote.astro"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/components/MultiVoteBar.tsx"
    }
  ]
}
---

# Voting Dashboard

A DRep's open governance actions with its own vote on each, and its voting record.
