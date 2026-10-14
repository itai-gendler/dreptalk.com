---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep chooses Flagged on a Post they flagged",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Flags"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    },
    {
      "text": "The Product withdraws the Flag",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "flag",
          "effect": "removes"
        },
        {
          "entity": "post",
          "effect": "changes",
          "facts": [
            "Flags"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    }
  ]
}
---

# Withdraw a flag

## Trigger

A writer reconsiders a flag.

## Outcome

The flag is withdrawn.
