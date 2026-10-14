---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Proposer opens Settings, Co-proposers and creates an invite",
      "kind": "actor",
      "actor": "proposer",
      "entities": [
        {
          "entity": "co-proposer",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-proposers"
        }
      }
    },
    {
      "text": "The Product creates a pending Co-proposer mandate with its invite link, valid for seven days",
      "kind": "product",
      "actor": "proposer",
      "entities": [
        {
          "entity": "co-proposer-mandate",
          "effect": "creates",
          "to": "Pending",
          "facts": [
            "Invite link",
            "Expires at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::co-proposers"
        }
      }
    }
  ]
}
---

# Create an invite link

## Trigger

A proposer wants a colleague to write for it.

## Outcome

A pending invite with a one-time link valid for seven days.

## Edge cases

- The link is the credential: anyone who opens it can claim the invite, so it is shared privately.
