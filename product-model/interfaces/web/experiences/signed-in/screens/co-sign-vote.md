---
{
  "entities": [
    {
      "entity": "multisig-vote",
      "shows": [
        "Governance action",
        "Choice",
        "Signatures",
        "Signatures required",
        "Expires at"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/drep/cosign/[id].astro"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/components/MultisigVotePanel.tsx"
    }
  ]
}
---

# Co-sign a multisig vote

Where a member of a multisig DRep signs a vote another member started, and submits it.
