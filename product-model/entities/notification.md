---
{
  "domain": "notifications",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/db/notifications.ts"
    }
  ]
}
---

# Notification

An entry in a signed-in person's inbox; it can also reach their browser push and Telegram channels.

## Information kept

- **Kind** — reply, mention, governance action, DRep vote, DRep status, delegation change, epoch summary, DRep stats, rationale ready, Governance Review or device paired
- **About** — the thread, post, action, DRep or edition it points to
- **From** — who caused it, if anyone
- **Created at** — when it was created

## States

### Unread

Not seen yet.

### Read

Seen in the inbox.
