---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "drep",
      "effect": "creates"
    },
    {
      "type": "entity",
      "id": "drep",
      "effect": "changes",
      "facts": [
        "Status",
        "Voting power",
        "Delegators",
        "Profile as of"
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
      "target": "src/lib/dreps/sync.ts"
    }
  ]
}
---

# DReps and their status come only from the chain

The Product adds DReps and sets their status, voting power and delegators from the chain only.
