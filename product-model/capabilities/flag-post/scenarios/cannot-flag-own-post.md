---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Post is the writer's own or written by the Product",
      "kind": "condition",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Kind"
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
      "text": "The DRep tries to flag it",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "flag",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    },
    {
      "text": "The Product refuses the flag",
      "kind": "product",
      "actor": "drep",
      "entities": [
        {
          "entity": "flag",
          "effect": "reads",
          "facts": []
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

# No flag on your own post or the Product's

## Trigger

The post is the writer's own or a system post.

## Outcome

Nothing is flagged.

## Edge cases

- Delegators and moderators without a writer role cannot flag.
