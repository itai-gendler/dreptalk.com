---
{
  "entities": [
    {
      "entity": "co-proposer-mandate",
      "shows": [
        "Expires at"
      ]
    },
    {
      "entity": "account",
      "collects": [
        "Display name"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/co-proposer/redeem.astro"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/components/RedeemCoProposer.tsx"
    }
  ]
}
---

# Co-proposer invite

Where the person holding an invite link accepts it with their own wallet.
