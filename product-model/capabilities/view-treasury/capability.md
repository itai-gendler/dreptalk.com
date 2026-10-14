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
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/treasury.astro"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "config/ncl-periods.ts"
    }
  ]
}
---

# View the treasury

Anyone follows enacted treasury withdrawals against the Net Change Limit of each budget period.
