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
      "target": "src/lib/forum/handlers.ts#handleFlagPost"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/postFlags.ts#flagPost"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/moderation.md"
    }
  ]
}
---

# Flag a post

A writer flags a post they consider abusive, spam or off-topic. Three flags from different writers hide it behind a placeholder.
