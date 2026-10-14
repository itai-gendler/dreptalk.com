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
      "type": "entity",
      "id": "notification"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/notifications/notify.ts"
    }
  ]
}
---

# A post notifies the people it mentions and the thread's other participants

Each person is notified once per post; edits notify nobody.
