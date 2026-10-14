---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "multisig-vote",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "collects",
          "entity": "drep"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/api/drep/multisig/[id]/witness.ts"
    }
  ]
}
---

# Only the multisig DRep's own members sign and submit its vote

Signatures and submission come from members signed in as the same DRep, with keys of its script.
