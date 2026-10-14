---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "view-my-drep"
    },
    {
      "type": "entity",
      "id": "delegation",
      "facts": [
        "Delegated since"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/myDrep.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/my-drep.md"
    }
  ]
}
---

# My DRep counts from the epoch of the latest delegation certificate

Re-delegating, even to the same DRep, restarts the count; a DRep registered later starts at its registration, and no figure appears without its basis.
