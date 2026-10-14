---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "start-topic"
    },
    {
      "type": "capability",
      "id": "reply-to-thread"
    },
    {
      "type": "capability",
      "id": "edit-post"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/forum/postLimits.ts#maxPostBody"
    }
  ]
}
---

# A post holds up to 20,000 characters, a draft's opening post up to 150,000

Titles hold 3 to 200 characters. The opening post of a Proposal Draft may carry a full governance action text.
