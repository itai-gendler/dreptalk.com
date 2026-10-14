---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/my-drep.astro"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/myDrep.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/my-drep.md"
    }
  ]
}
---

# View My DRep

A delegator reads, privately, what its DRep did since its latest delegation started: participation, rationale coverage, vote changes, the actions without a vote, and voting power then and now.
