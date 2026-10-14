---
{
  "kind": "validation",
  "routes": {
    "main": "Website, then Telegram"
  },
  "steps": [
    {
      "text": "The Delegator sends the bot a start message with an expired link code",
      "kind": "actor",
      "actor": "delegator",
      "entities": [],
      "contexts": {
        "main": {
          "place": "telegram-bot"
        }
      }
    },
    {
      "text": "The Product replies that the link has expired",
      "kind": "product",
      "actor": "delegator",
      "entities": [],
      "contexts": {
        "main": {
          "place": "telegram-bot"
        }
      }
    }
  ]
}
---

# An expired link

## Trigger

The link code is no longer valid.

## Outcome

Nothing is connected; the bot says to get a fresh link from the settings.
