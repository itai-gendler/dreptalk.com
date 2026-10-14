---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor waits longer than ten minutes without the code being approved",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "pairing-code",
          "effect": "reads",
          "facts": [
            "Expires at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The Product stops accepting the code and offers Get a new code",
      "kind": "product",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    }
  ]
}
---

# The pairing code expires

## Trigger

Nobody approved the code within ten minutes.

## Outcome

The phone stays signed out and offers a new code.
