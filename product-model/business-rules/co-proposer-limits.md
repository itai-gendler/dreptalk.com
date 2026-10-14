---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "invite-co-proposer"
    },
    {
      "type": "capability",
      "id": "accept-co-proposer-invite"
    },
    {
      "type": "entity",
      "id": "co-proposer-mandate"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/proposerGrants.ts#MAX_GRANTS_PER_PROPOSER"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/proposers.md"
    }
  ]
}
---

# A proposer has at most two co-proposers, and a wallet holds one mandate

Pending and active mandates together count toward the two. An invite works once, within seven days, and the proposer's own wallet cannot accept it.
