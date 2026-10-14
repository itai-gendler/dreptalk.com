---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "post",
      "effect": "creates"
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
    },
    {
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/forum/handlers.ts#handleCreatePost"
    }
  ]
}
---

# Only writers post

Posting is for active DReps, SPOs, CC members, proposers and co-proposers; delegators and moderators read. The Product writes the opening posts of governance and survey threads.
