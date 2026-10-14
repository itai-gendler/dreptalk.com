---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "moderator"
    },
    {
      "type": "capability",
      "id": "read-thread"
    },
    {
      "type": "capability",
      "id": "unlink-draft-action"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "config/moderators.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "README.md",
      "title": "README"
    }
  ]
}
---

# Moderators are the stake addresses the site operator lists

The list is set by the operator outside the product and re-read at every sign-in; the moderator role adds no right to post, react or flag.
