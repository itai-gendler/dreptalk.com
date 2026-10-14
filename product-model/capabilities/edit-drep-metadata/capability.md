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
      "target": "src/pages/settings/metadata.astro"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/drepProfileApply.ts#applyDrepProfile"
    }
  ]
}
---

# Edit DRep metadata

A DRep changes its on-chain profile from a form prefilled with the current one; its wallet signs the update certificate and the profile here changes at once.
