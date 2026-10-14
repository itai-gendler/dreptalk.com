---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "co-proposer-mandate",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "actors": [
        "proposer"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/coProposerManage.ts#requireGrantManager"
    }
  ]
}
---

# Only proposers invite co-proposers

A proposer signed in with its own on-chain identity invites co-proposers; co-proposers cannot invite further people.
