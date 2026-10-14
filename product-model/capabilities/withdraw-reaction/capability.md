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
      "target": "src/lib/forum/handlers.ts#handleClearReaction"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/postReactions.ts#clearReaction"
    }
  ]
}
---

# Withdraw a reaction

A writer takes back their thumbs up or thumbs down.
