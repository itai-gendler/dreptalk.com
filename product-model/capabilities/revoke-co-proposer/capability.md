---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "co-proposers",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/api/auth/co-proposer/revoke.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/session.ts#revokeAllForGrant"
    }
  ]
}
---

# Revoke a co-proposer

A proposer ends an active co-proposer's mandate.
