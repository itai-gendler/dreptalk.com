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
      "target": "src/pages/posts/[id]/history.astro"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/forum/postHistory.ts"
    }
  ]
}
---

# View post history

Anyone opens the edited marker of a post to read every earlier version and what changed.
