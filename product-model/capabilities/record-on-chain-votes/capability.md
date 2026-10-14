---
{
  "availability": [
    {
      "place": "web::public"
    }
  ],
  "domain": "governance-actions",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/sync/phases/votes.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/drepVotes.ts#upsertVotes"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/drepVotes.ts#markStalePendingVotesFailed"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/governance/rationaleSync.ts#VOTE_RATIONALE_MIN_POWER_LOVELACE"
    }
  ]
}
---

# Record on-chain votes

On a schedule the Product reads every DRep, SPO and Constitutional Committee vote on the actions it mirrors, confirms the votes cast through DRepTalk, reads rationales and tells delegators how their DRep voted.
