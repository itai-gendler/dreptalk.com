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
      "target": "src/lib/forum/handlers.ts#handleEditPost"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/forum.ts#editPost"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/forum/editPolicy.ts#EDIT_GRACE_MS"
    }
  ]
}
---

# Edit a post

A writer edits their own post. Right after posting the edit is silent; after the grace window the earlier text is kept as a version and the post is marked edited.
