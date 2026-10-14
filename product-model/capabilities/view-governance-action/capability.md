---
{
  "availability": [
    {
      "place": "web::public"
    },
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "governance-actions",
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/understanding-a-governance-action.md"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/view.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/thresholds.ts"
    }
  ]
}
---

# View a governance action

Anyone reads a governance action on its thread: what it proposes, where it stands, how each voting body is voting against its threshold, every vote with its rationale and earlier votes, the raw on-chain data and the history of its support.
