---
{
  "availability": [
    {
      "place": "web::public"
    }
  ],
  "domain": "co-proposers",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/coProposerRedeem.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/proposerGrants.ts#redeemGrant"
    }
  ]
}
---

# Accept a co-proposer invite

The person holding an invite link picks a display name, connects their own wallet and signs a confirmation; no on-chain role or transaction is needed.
