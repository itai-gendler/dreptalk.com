---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "edit-topic-title"
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
      "target": "src/lib/db/forum.ts#editTitle"
    }
  ]
}
---

# A thread's address never changes

The address is made from the first title and stays when the title is edited, so links never break; earlier titles are not kept.
