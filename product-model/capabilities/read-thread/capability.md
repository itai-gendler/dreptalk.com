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
  "domain": "discussions",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/t/[slug].astro"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/forum/postVisibility.ts"
    }
  ]
}
---

# Read a thread

Anyone reads a thread and its posts, each carrying its author's verified on-chain identity. A hidden post shows as a placeholder to everyone but its author and moderators.
