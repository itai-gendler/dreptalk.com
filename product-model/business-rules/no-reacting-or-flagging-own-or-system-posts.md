---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "react-to-post"
    },
    {
      "type": "capability",
      "id": "flag-post"
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
      "target": "src/lib/forum/handlers.ts#handleReactToPost"
    }
  ]
}
---

# Nobody reacts to or flags their own post or a post the Product wrote

A writer cannot react to or flag their own post, nor the opening post the Product writes for a governance action, which mirrors the action rather than taking a side.
