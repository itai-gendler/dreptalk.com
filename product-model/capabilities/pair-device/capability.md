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
      "target": "src/content/guides/pair-a-device.md"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/pairing.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/components/PairWithDesktop.tsx"
    }
  ]
}
---

# Pair a device

A phone or tablet, which has no wallet to sign with, shows a short code that a signed-in computer approves; the phone then signs itself in to the same account.
