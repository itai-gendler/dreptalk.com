---
{
  "domain": "surveys",
  "relations": [
    {
      "entity": "thread",
      "verb": "has",
      "cardinality": "one-to-one"
    },
    {
      "entity": "survey-response",
      "verb": "collects",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/cip-179-surveys.md"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/surveys.ts"
    }
  ]
}
---

# Survey

A CIP-179 survey published on chain that DReps may answer and that an imported governance action links. DRepTalk mirrors it from the Tessera index with a thread of its own and an informational tally.

## Information kept

- **Questions** — the questions and options from its on-chain definition
- **Eligible roles** — the roles allowed to answer
- **Closing epoch** — answers count through this epoch
- **Sealed** — whether answers stay encrypted until a reveal time
- **Tally** — the informational tally of DRep responses under the generic CIP-179 rules, with its basis
- **Participation count** — how many DRep responses were counted
- **Excluded responses** — responses left out of the count, with the reason for each
- **Text loaded** — whether its question texts are on chain; off-chain texts are not fetched

## States

### Open

Answers are accepted.

### Closed

The closing epoch has passed.

### Cancelled

Its owner withdrew it before it closed.

### Invalid definition

The index decided it cannot be tallied.

### Unavailable

Its record, or the action that links it, rolled back; answering is switched off.
