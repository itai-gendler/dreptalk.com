---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "vote",
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
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/api/vote/record.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/voting.md"
    }
  ]
}
---

# Only an active DRep votes through DRepTalk

Voting here is for a signed-in DRep whose registration is active; SPO and committee votes are cast outside DRepTalk and recorded by the Product from the chain.
