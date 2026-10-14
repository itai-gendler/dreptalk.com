---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "erase-deleted-post"
    },
    {
      "type": "entity",
      "id": "post"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/postErasure.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/moderation.md"
    }
  ]
}
---

# A deleted post's text is erased thirty days after deletion

Deletion takes a post out of the forum at once; its text, every earlier version and its search entry are erased thirty days later. Members cannot delete posts.

## Rationale

The thirty days let abusive content still be dealt with after it was taken down.
