---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "flag-post"
    },
    {
      "type": "capability",
      "id": "withdraw-flag"
    },
    {
      "type": "entity",
      "id": "post",
      "effect": "changes",
      "to": "Hidden"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/postFlags.ts#FLAG_HIDE_THRESHOLD"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/moderation.md"
    }
  ]
}
---

# Three flags from different writers hide a post

A post is hidden behind a placeholder once three different writers flagged it, and shown again, unchanged, when fewer than three flags remain. No single person can take a post down.
