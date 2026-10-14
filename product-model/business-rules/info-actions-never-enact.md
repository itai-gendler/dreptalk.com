---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "update-governance-action-status"
    },
    {
      "type": "entity",
      "id": "governance-action"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/tallySync.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/governance-statuses.md"
    }
  ]
}
---

# An info action closes instead of being ratified, expiring or being dropped

Info actions have no on-chain effect, so their status ends at Closed.
