---
{
  "domain": "voting-dashboard",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/pendingMultisigTx.ts"
    }
  ]
}
---

# Multisig vote

A vote by a native-script DRep that collects its members' signatures before it is submitted.

## Information kept

- **Governance action** — the action voted on
- **Choice** — Yes, No or Abstain
- **Rationale link** — the rationale anchor, if any
- **Signatures** — the member signatures collected so far
- **Signatures required** — what the script needs
- **Co-sign link** — the link the members open to sign
- **Expires at** — 36 hours after it was started
- **Transaction** — the submitted transaction

## States

### Collecting

Waiting for member signatures.

### Submitted

Signed by enough members and submitted.
