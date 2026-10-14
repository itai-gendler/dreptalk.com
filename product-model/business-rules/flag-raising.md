---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "flag",
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
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/forum/handlers.ts#handleFlagPost"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/moderation.md"
    }
  ]
}
---

# Only writers flag posts

Writers flag posts; delegator sign-ins cannot.
