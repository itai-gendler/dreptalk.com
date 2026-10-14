---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "thread",
      "effect": "changes",
      "facts": [
        "Replies",
        "Last activity"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "drep"
      ],
      "when": [
        {
          "entity": "drep",
          "fact": "Status",
          "is": "Active"
        }
      ]
    },
    {
      "actors": [
        "spo",
        "cc-member",
        "proposer",
        "co-proposer"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/forum.ts#createPost"
    }
  ]
}
---

# Only writers add to a thread's activity

Replies and cross-posted rationales update a thread's reply count and last activity.
