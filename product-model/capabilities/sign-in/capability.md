---
{
  "availability": [
    {
      "place": "web::public"
    }
  ],
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/signing-in.md"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/handlers.ts#handleVerify"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/resolveRole.ts"
    }
  ]
}
---

# Sign in

A person signs in by signing a one-time challenge with the Cardano key behind an on-chain governance identity, or with their stake wallet as a read-only delegator. There is no password and nothing is submitted on chain. The Product confirms the role on chain at every sign-in and signs the device in.
