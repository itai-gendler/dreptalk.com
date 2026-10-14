---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens an invite link that is no longer pending",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::co-proposer-invite"
        }
      }
    },
    {
      "text": "The Product says the invite is unavailable",
      "kind": "product",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::co-proposer-invite"
        }
      }
    }
  ]
}
---

# A used or expired invite

## Trigger

The link was already used, withdrawn or is older than seven days.

## Outcome

Nothing is accepted.

## Edge cases

- The proposer's own wallet cannot accept its own invite.
- A wallet that already holds an active mandate cannot accept a second one.
