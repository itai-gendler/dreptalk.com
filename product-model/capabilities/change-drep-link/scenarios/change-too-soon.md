---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep enters a new short name within the cooldown",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "drep-link",
          "effect": "reads",
          "facts": [
            "Next change from",
            "Previous name redirects until"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::drep-link-settings"
        }
      }
    },
    {
      "text": "The Product refuses the change and says when it becomes possible",
      "kind": "product",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::drep-link-settings"
        }
      }
    }
  ]
}
---

# A change during the cooldown

## Trigger

The DRep changed its name less than 90 days ago, or its previous name still redirects.

## Outcome

Nothing changes; the page says when the next change is possible.

## Edge cases

- Switching back to the previous name is possible once the cooldown ends.
- Names must be 3 to 40 characters, not reserved, and not shaped like a DRep ID.
