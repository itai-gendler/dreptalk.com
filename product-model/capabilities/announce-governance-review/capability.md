---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "governance-review",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/reviewAnnouncements.ts#announceLatestEdition"
    }
  ]
}
---

# Announce a Governance Review edition

When a new edition goes live, the Product tells every account once, in the inbox and through push and Telegram. Runs on mainnet only.
