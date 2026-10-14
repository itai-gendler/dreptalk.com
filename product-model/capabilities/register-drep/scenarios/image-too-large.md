---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor adds an image larger than 256 KB",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::register-drep"
        }
      }
    },
    {
      "text": "The Product refuses the image",
      "kind": "product",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::register-drep"
        }
      }
    }
  ]
}
---

# A profile image that is too large

## Trigger

The image is not a JPG or PNG of at most 256 KB.

## Outcome

The image is refused; nothing is submitted.
