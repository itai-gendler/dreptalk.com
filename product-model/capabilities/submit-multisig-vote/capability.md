---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "voting-dashboard",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/api/drep/multisig/[id]/submit.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/api/drep/multisig/[id]/submitted.ts"
    }
  ]
}
---

# Submit a multisig vote

Once enough members signed, a member submits the vote; their wallet pays the fee.
