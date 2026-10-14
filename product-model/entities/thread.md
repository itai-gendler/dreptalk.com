---
{
  "domain": "discussions",
  "relations": [
    {
      "entity": "post",
      "verb": "contains",
      "cardinality": "one-to-many"
    },
    {
      "entity": "governance-action",
      "verb": "drafts",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/forum.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "config/categories.ts"
    }
  ]
}
---

# Thread

A discussion in one category. People open threads in the discussion categories; the Product opens one thread per governance action and per mirrored survey. A thread in Proposal Drafts is a draft of a governance action discussed before it goes on chain.

## Information kept

- **Title** — set when the thread opens; editable by its author in discussion categories
- **Category** — Governance Actions, Proposal Drafts, Constitution and Guardrails, Budget and Treasury, General and Off-topic, or Surveys
- **Opened by** — the person who opened it, or the Product
- **Address** — the readable address made from the first title, which never changes
- **Title edited** — marks that the title changed; earlier titles are not kept
- **Replies** — how many posts it holds
- **Last activity** — when it was last posted in
- **Written under mandate** — the co-proposer mandate it was opened under, if any

## States

### Open

Takes replies and edits.

### Closed

A Proposal Draft connected to its governance action; it takes no replies or edits.
