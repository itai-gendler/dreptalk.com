---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "post",
      "effect": "changes",
      "facts": [
        "Ups",
        "Downs",
        "Flags"
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
      "target": "src/lib/db/postFlags.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/postReactions.ts"
    }
  ]
}
---

# Only writers move a post's reaction and flag counts

Thumbs and flags come from writers, so only their reactions and flags change the counts.
