---
{
  "relations": [
    {
      "entity": "thread",
      "verb": "covers",
      "cardinality": "one-to-many"
    },
    {
      "entity": "post",
      "verb": "covers",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/proposerGrants.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/proposers.md"
    }
  ]
}
---

# Co-proposer mandate

A proposer's authorization for one co-proposer, from the one-time invite link to the active mandate.

## Information kept

- **Invite link** — the one-time link that is the credential for accepting
- **Expires at** — seven days after the invite was created
- **Accepted at** — when the co-proposer accepted
- **Revoked at** — when the proposer revoked it

## States

### Pending

Invited; the link has not been used yet.

### Active

Accepted; the co-proposer writes on the proposer's behalf.

### Revoked

Ended by the proposer; posts written under it keep their badge.
