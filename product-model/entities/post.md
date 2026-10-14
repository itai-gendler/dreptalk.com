---
{
  "domain": "discussions",
  "relations": [
    {
      "entity": "post-version",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "reaction",
      "verb": "receives",
      "cardinality": "one-to-many"
    },
    {
      "entity": "flag",
      "verb": "receives",
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
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/moderation.md"
    }
  ]
}
---

# Post

One message in a thread: an opening post, a reply, or a vote rationale a DRep cross-posted when voting.

## Information kept

- **Body** — the Markdown text, with @mentions linked
- **Kind** — opening post, reply, or vote rationale
- **Reply to** — the top-level post a reply answers; threads are one level deep
- **Vote** — for a vote rationale, the Yes, No or Abstain it explains
- **Ups** — how many thumbs up it has
- **Downs** — how many thumbs down it has
- **Flags** — how many writers flagged it
- **Edited** — when it was last edited after its grace window
- **Written under mandate** — the co-proposer mandate it was written under, if any
- **Posted at** — when it was written

## States

### Visible

Shown in its thread.

### Hidden

Hidden behind a placeholder after three different writers flagged it; still stored.

### Deleted

Out of the forum; its text is kept for 30 days.

### Erased

Its text, every earlier version and its search entry are gone.
