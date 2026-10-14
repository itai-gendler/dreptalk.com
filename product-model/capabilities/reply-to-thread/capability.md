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
      "target": "src/lib/forum/handlers.ts#handleCreatePost"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/forum.ts#createPost"
    }
  ]
}
---

# Reply

A writer replies in a thread, to the thread or to one post; threads are one level deep.
