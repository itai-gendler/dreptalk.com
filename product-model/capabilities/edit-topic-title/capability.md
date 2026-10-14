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
      "target": "src/lib/forum/handlers.ts#handleEditTitle"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/forum.ts#editTitle"
    }
  ]
}
---

# Edit a thread title

The author of a thread in a discussion category changes its title; its address stays the same.
