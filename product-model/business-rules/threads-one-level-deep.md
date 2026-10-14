---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "reply-to-thread"
    },
    {
      "type": "entity",
      "id": "post",
      "facts": [
        "Reply to"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/forum.ts#createPost"
    }
  ]
}
---

# Replies are one level deep

A reply answers the thread or one top-level post; a reply to a reply attaches to that reply's top-level post.
