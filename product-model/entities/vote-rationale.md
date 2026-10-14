---
{
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/writing-a-vote-rationale.md"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/actionRationale.ts"
    }
  ]
}
---

# Vote rationale

The CIP-100 document explaining a vote. One written on DRepTalk is hosted here at an address that is its own hash; one linked by a vote cast elsewhere is read from the chain when the voter is large enough.

## Information kept

- **Text** — the rationale text
- **Address** — where the document is served, named by its blake2b-256 hash
- **Source** — written on DRepTalk or read from the voter's anchor
- **Readable** — whether the linked document could be read; otherwise the vote shows Rationale unavailable
