---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "open-governance-action-thread"
    },
    {
      "type": "entity",
      "id": "thread",
      "facts": [
        "Address"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/sync.ts#DEFERRED_TOPIC_MAX_ATTEMPTS"
    }
  ]
}
---

# A governance thread waits up to six runs for a readable proposal document

A thread opens on the action's real title once its proposal document answers; after six attempts, or when the document is unusable, it opens on a title built from the type and id, and its address keeps that title.
