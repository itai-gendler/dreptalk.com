---
{
  "availability": [
    {
      "place": "web::public"
    }
  ],
  "domain": "governance-actions",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/tallySync.ts#syncGovernanceTallies"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/thresholds.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/governance-statuses.md"
    }
  ]
}
---

# Update governance action status

On a schedule the Product reads each undecided action's tallies and lifecycle from the chain, evaluates every voting body against its threshold and moves the action to its new status.
