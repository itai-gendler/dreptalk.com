---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "open-governance-action-thread"
    },
    {
      "type": "capability",
      "id": "unlink-draft-action"
    },
    {
      "type": "entity",
      "id": "governance-action",
      "facts": [
        "Draft link refused"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/draftLink.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/draftLinks.ts"
    }
  ]
}
---

# A draft connects to an action that names it among its first 20 references

Only a live Proposal Drafts thread of the same network connects, only once the action has its thread, and an action its draft's author detached never connects to that draft again.
