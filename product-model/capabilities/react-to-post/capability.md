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
      "target": "src/lib/forum/handlers.ts#handleReactToPost"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/postReactions.ts#setReaction"
    }
  ]
}
---

# React to a post

A writer gives someone else's post a thumbs up or a thumbs down; one reaction per writer and post.
