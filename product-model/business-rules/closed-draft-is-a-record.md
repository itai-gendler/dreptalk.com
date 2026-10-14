---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "reply-to-thread"
    },
    {
      "type": "capability",
      "id": "edit-post"
    },
    {
      "type": "capability",
      "id": "edit-topic-title"
    },
    {
      "type": "entity",
      "id": "thread"
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
      "target": "src/content/guides/get-feedback-on-a-proposal.md"
    }
  ]
}
---

# A connected draft takes no replies or edits

Once a Proposal Draft is connected to its governance action it stays a record of what was discussed before submission: no replies, post edits or title edits until it reopens.
