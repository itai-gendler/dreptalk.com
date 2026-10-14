---
{
  "entities": [
    {
      "entity": "delegation",
      "shows": [
        "Delegated to",
        "Delegated since"
      ]
    },
    {
      "entity": "drep",
      "shows": [
        "Name",
        "Status",
        "Voting power",
        "Delegators"
      ]
    },
    {
      "entity": "governance-action",
      "shows": [
        "Title",
        "Type",
        "Decided epoch"
      ]
    },
    {
      "entity": "vote",
      "shows": [
        "Choice",
        "Rationale link",
        "Earlier votes"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/my-drep.astro"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/my-drep.md"
    }
  ]
}
---

# My DRep

A delegator's private page on what their DRep, or their default option, did since their delegation started.
