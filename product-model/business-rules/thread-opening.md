---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "thread",
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
      "target": "src/lib/forum/handlers.ts#handleCreateTopic"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/roles.ts#isWriter"
    }
  ]
}
---

# Only writers open threads

Opening a thread is for wallet-verified writers: active DReps, SPOs, CC members, proposers and co-proposers. The Product itself opens the thread of every governance action and mirrored survey.

## Rationale

Every writer is a wallet-verified governance participant, which is what keeps light moderation enough.
