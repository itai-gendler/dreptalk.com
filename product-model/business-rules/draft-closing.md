---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "thread",
      "effect": "changes",
      "to": "Closed"
    }
  ],
  "permits": [
    {
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/draftLinks.ts#buildDraftLinkStatements"
    }
  ]
}
---

# Only the Product closes a draft

A Proposal Draft closes when the Product connects it to the governance action that names it.
