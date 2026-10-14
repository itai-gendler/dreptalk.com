---
{
  "availability": [
    {
      "place": "web::public"
    },
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "dreps",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/components/DelegateDialog.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/delegation/trackingOffer.ts#trackingOffer"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/delegate-to-a-drep.md"
    }
  ]
}
---

# Delegate to a DRep

From a DRep's profile anyone delegates the voting power of their wallet to that DRep; the wallet signs and submits the certificate. Afterwards DRepTalk offers to follow the delegation.
