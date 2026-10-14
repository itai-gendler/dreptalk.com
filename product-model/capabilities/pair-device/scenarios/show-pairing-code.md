---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor chooses Pair with desktop and Show pairing code in the installed app",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "pairing-code",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The Product shows a new Pairing code valid for ten minutes",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "pairing-code",
          "effect": "creates",
          "to": "Waiting",
          "facts": [
            "Code",
            "Device label",
            "Expires at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    }
  ]
}
---

# Show a pairing code on the phone

## Trigger

A person wants DRepTalk and push notifications on their phone.

## Outcome

The phone shows a code that waits for approval from a signed-in computer.

## Edge cases

- Pairing inside a mobile browser tab does not carry over to the installed app, whose storage is separate.
