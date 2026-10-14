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
      "target": "src/pages/api/drep/multisig/[id]/witness.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/pendingMultisigTx.ts#addPendingWitness"
    }
  ]
}
---

# Co-sign a multisig vote

A member of a multisig DRep opens the co-sign link and adds their signature to a vote another member started.
