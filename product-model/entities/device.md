---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/session.ts"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/pair-a-device.md"
    }
  ]
}
---

# Device

A browser or phone signed in to an account, listed under Settings, Devices with the current one marked.

## Information kept

- **Label** — the browser and system the device signed in from
- **Signed in at** — when the device signed in
- **Last used** — when the device was last used, renewed at most every few hours
- **Roles** — the roles the device acts with, fixed when it signed in

## States

### Signed in

The device acts for the account.

### Signed out

The device was signed out, or its session ran out; it signs in again with a new signature or pairing code.
