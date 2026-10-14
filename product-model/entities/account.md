---
{
  "relations": [
    {
      "entity": "device",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "notification",
      "verb": "receives",
      "cardinality": "one-to-many"
    },
    {
      "entity": "notification-channel",
      "verb": "connects",
      "cardinality": "one-to-many"
    },
    {
      "entity": "delegation",
      "verb": "follows",
      "cardinality": "one-to-one"
    },
    {
      "entity": "pairing-code",
      "verb": "approves",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/users.ts"
    }
  ]
}
---

# Account

What DRepTalk keeps for one person across the roles they sign in with. It holds the facts that belong to the person rather than to a role: their chosen name, their linked stake wallet and their notification choices. There is no password and no email address.

## Information kept

- **Display name** — the name shown where no on-chain name applies, such as the one a co-proposer picks
- **Linked stake address** — the stake wallet the account has proven, used to follow its delegation; never shown on any page
- **Push preferences** — which notification types reach browser push, one switch per type
- **Telegram preferences** — which notification types reach Telegram, one switch per type
- **Inbox last opened** — when the person last opened their notifications
- **Arrived through** — the drep.link the person came through when the account was created
