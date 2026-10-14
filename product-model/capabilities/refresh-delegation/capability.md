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
      "target": "src/lib/delegation/refresh.ts#refreshBulk"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/delegatorFollows.ts"
    }
  ]
}
---

# Refresh followed delegations

Once a day per account, and at every sign-in, the Product re-reads followed delegations from the chain and tells the delegator when theirs changed.
