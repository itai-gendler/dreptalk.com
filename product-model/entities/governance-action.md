---
{
  "domain": "governance-actions",
  "relations": [
    {
      "entity": "thread",
      "verb": "has",
      "cardinality": "one-to-one"
    },
    {
      "entity": "vote",
      "verb": "receives",
      "cardinality": "one-to-many"
    },
    {
      "entity": "survey",
      "verb": "links",
      "cardinality": "many-to-many"
    }
  ],
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/governance-statuses.md"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/understanding-a-governance-action.md"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/governance.ts"
    }
  ]
}
---

# Governance action

An on-chain proposal put to the DReps, SPOs and Constitutional Committee. DRepTalk mirrors every action on its network with one thread each, its proposal document, its votes and its tallies, all as of the last sync.

## Information kept

- **Action ID** — the CIP-129 id and the transaction hash with index
- **Type** — info action, treasury withdrawal, parameter change, new constitution, committee update, hard fork initiation or motion of no confidence
- **Title** — from the proposal document, or a fallback built from the type and id
- **Abstract** — from the proposal document
- **Motivation** — from the proposal document
- **Rationale** — from the proposal document
- **Authors** — the names the proposal document declares, shown verbatim and unverified
- **References** — the links from the proposal document
- **Proposer address** — the reward address that posted the deposit and gets it back
- **Deposit** — the deposit locked by the action
- **Submitted epoch** — when the action was submitted
- **Expiry epoch** — the last epoch of its voting window
- **Decided epoch** — when it was ratified, enacted, expired, dropped or closed
- **On-chain changes** — the type-specific values the action would set
- **Tallies** — the yes share of the counted stake for each voting body
- **Thresholds** — the approval threshold for each voting body and whether it is met
- **Data as of** — when status and tallies were last synced
- **Trending score** — recent replies and votes, halving for every week without activity
- **Draft link refused** — set once the draft's author detached the action, so it is never linked to that draft again

## States

### Syncing

Found on chain; its status and tallies are not synced yet.

### Active

Voting is open.

### Ratified

Reached its thresholds and is queued for enactment.

### Enacted

Ratified and applied on chain.

### Expired

The voting window ended without ratification.

### Dropped

Removed without expiring, for example when a competing action was enacted.

### Closed

An info action whose voting window ended; info actions never enact.
