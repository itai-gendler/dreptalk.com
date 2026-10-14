---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "governance-action",
      "effect": "creates"
    },
    {
      "type": "entity",
      "id": "governance-action",
      "effect": "changes",
      "facts": [
        "Tallies",
        "Thresholds",
        "Data as of",
        "Decided epoch"
      ]
    }
  ],
  "permits": [
    {
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/sync.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/tallySync.ts"
    }
  ]
}
---

# Governance actions, their status and tallies come only from the chain

Nobody creates a governance action or sets its status and tallies on DRepTalk; the Product mirrors them from the chain on its schedule.
