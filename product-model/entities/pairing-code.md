---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/pairing.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/pair-a-device.md"
    }
  ]
}
---

# Pairing code

A short code a phone or tablet shows so a signed-in computer can sign it in without a key.

## Information kept

- **Code** — the short code shown on the phone
- **Device label** — the phone the code belongs to, shown to the approver
- **Expires at** — ten minutes after the code was shown

## States

### Waiting

Shown on the phone, waiting for approval.

### Approved

Approved from a signed-in computer.

### Used

The phone picked up the approval and signed itself in.
