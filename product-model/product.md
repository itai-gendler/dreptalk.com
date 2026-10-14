---
{
  "id": "dreptalk",
  "summary": "The public deliberation layer for Cardano governance: one thread per on-chain governance action, written in by wallet-verified DReps, SPOs, committee members and proposers, next to the live vote data.",
  "category": "governance",
  "tags": [
    "cardano",
    "governance",
    "forum",
    "voting"
  ],
  "authors": [
    {
      "name": "katomm",
      "url": "https://github.com/katomm"
    }
  ],
  "license": "Apache-2.0",
  "limitations": [
    "DRepTalk never holds keys: every vote, registration, delegation, survey answer and submitted action is signed and submitted by the person's own wallet.",
    "People sign in by signing a one-time challenge with a Cardano key; there are no passwords and no email addresses.",
    "Reading is public, but only wallet-verified governance roles write; delegators sign in read-only.",
    "On-chain data is never read live on a page; it comes from scheduled syncs and is shown with the time of its data.",
    "Members cannot delete posts; moderation is community flagging, and only the site operator deletes."
  ],
  "languages": [
    "en"
  ],
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "README.md",
      "title": "README"
    },
    {
      "kind": "doc",
      "role": "context",
      "target": "CONTRIBUTING.md",
      "title": "Contributing"
    }
  ]
}
---

# DRepTalk

DRepTalk is the public, wallet-authenticated deliberation layer for Cardano governance. Every on-chain governance action automatically gets a thread, and DReps, stake pool operators, Constitutional Committee members and proposers discuss it next to its votes, rationales and tallies. Each writer proves their on-chain role with a wallet signature; delegators sign in to follow their DRep and be notified. Around the threads sit the DRep directory, voting for DReps, CIP-179 surveys, analytics, the treasury, the per-epoch Governance Review and, on preprod, submitting new governance actions.

## Intent

The aim is a place where Cardano governance is discussed, voted and explained, next to the on-chain data it is about. Reading is public and writing is gated to on-chain roles, each proven by a wallet signature, so participation is accountable without custody of keys.
