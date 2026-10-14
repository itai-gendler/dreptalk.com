---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Delegator enters a code that is unknown or older than ten minutes",
      "kind": "actor",
      "actor": "delegator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::devices"
        }
      }
    },
    {
      "text": "The Product refuses the code",
      "kind": "product",
      "actor": "delegator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::devices"
        }
      }
    }
  ]
}
---

# An unknown or expired code is refused

## Trigger

The code entered does not match a waiting code.

## Outcome

Nothing is approved.

## Edge cases

- Attempts are limited per account and per network address within ten minutes.
