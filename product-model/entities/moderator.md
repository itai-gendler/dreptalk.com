---
{
  "kind": "person",
  "acts": "external",
  "relations": [
    {
      "entity": "account",
      "verb": "uses",
      "cardinality": "one-to-one"
    }
  ],
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "README.md",
      "title": "README"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/roles.ts#isModerator"
    }
  ]
}
---

# Moderator

A person whose stake address the site operator lists as a moderator or admin. Moderators sign in with the ordinary stake-key wallet flow; the role adds no writing rights, only reading hidden posts and their history and detaching governance actions from Proposal Drafts.
