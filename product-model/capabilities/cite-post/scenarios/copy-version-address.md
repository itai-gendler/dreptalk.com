---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor chooses Cite on a Post",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Body"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::thread"
        }
      }
    },
    {
      "text": "The Product lists every Post version newest first with its permanent address",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "post-version",
          "effect": "reads",
          "facts": [
            "Address",
            "Published at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::citation"
        }
      }
    },
    {
      "text": "The Visitor copies the address of one version",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "post-version",
          "effect": "reads",
          "facts": [
            "Address"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::citation"
        }
      }
    }
  ]
}
---

# Copy a version's permanent address

## Trigger

A DRep wants to quote a post in a vote rationale.

## Outcome

The reader has an address whose text never changes.

## Edge cases

- Cite appears once the post's grace window has closed.
- Vote rationales and the opening posts of governance actions already have their own permanent document and get no second one.
- A deleted post's versions answer Gone; a withheld post's versions answer not found until it returns.
