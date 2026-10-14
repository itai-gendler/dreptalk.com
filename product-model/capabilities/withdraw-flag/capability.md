---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "discussions",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/forum/handlers.ts#handleUnflagPost"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/postFlags.ts#unflagPost"
    }
  ]
}
---

# Withdraw a flag

A writer withdraws their flag; a hidden post returns unchanged once fewer than three flags remain.
