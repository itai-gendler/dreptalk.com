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
      "target": "src/lib/forum/handlers.ts#handleDraftUnlink"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/draftLinks.ts#unlinkDraftAction"
    }
  ]
}
---

# Unlink a governance action from a draft

The author of a Proposal Draft, or a moderator, detaches a governance action that named the draft in its references without being the draft's action.
