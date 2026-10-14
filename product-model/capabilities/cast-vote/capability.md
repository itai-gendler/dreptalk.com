---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "voting-dashboard",
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/voting.md"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/voting-on-multiple-actions.md"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/api/vote/record.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/components/VotePanel.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/voteLimits.ts#MAX_BATCH_VOTES"
    }
  ]
}
---

# Vote

A DRep votes Yes, No or Abstain on open governance actions and signs the vote in its own wallet, optionally with a rationale DRepTalk hosts and a copy posted under the discussion. A vote can be cast on the action's page or, for several actions in one transaction, from the voting dashboard.
