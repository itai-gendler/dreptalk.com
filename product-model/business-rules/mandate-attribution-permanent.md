---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "revoke-co-proposer"
    },
    {
      "type": "capability",
      "id": "edit-post"
    },
    {
      "type": "entity",
      "id": "post",
      "facts": [
        "Written under mandate"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/forum.ts#editPost"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/proposers.md"
    }
  ]
}
---

# Writing under a mandate keeps its attribution for good

A thread or post written under a co-proposer mandate shows the proposer it was written for, even after the mandate is revoked, and is edited only under that same mandate; a personal post is never edited under one.
