---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep opens Settings, drep.link and enters a new short name",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "drep-link",
          "effect": "reads",
          "facts": [
            "Short name",
            "Next change from"
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
      "text": "The Product makes it the drep.link and keeps the previous name redirecting for 180 days",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "drep-link",
          "effect": "changes",
          "facts": [
            "Short name",
            "Previous name",
            "Previous name redirects until",
            "Next change from"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::drep-link-settings"
        }
      }
    }
  ]
}
---

# Pick a new short name

## Trigger

A DRep wants a better short link.

## Outcome

The new link works at once and the old one redirects for 180 days.
