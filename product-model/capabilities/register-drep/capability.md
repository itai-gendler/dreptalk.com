---
{
  "availability": [
    {
      "place": "web::public"
    },
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "dreps",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/register-drep.astro"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/drepMetadataHandler.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/managing-your-drep.md"
    }
  ]
}
---

# Register as a DRep

Anyone with a CIP-95 wallet registers as a DRep: DRepTalk hosts the CIP-119 profile document and the wallet submits the registration, locking a refundable 500 ada deposit.
