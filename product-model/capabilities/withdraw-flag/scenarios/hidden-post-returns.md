---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep withdraws one of the three flags that hid a Post",
      "kind": "actor",
      "actor": "drep",
      "entities": [
        {
          "entity": "post",
          "effect": "reads",
          "facts": [
            "Flags"
          ]
        },
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
      "text": "The Product withdraws the Flag and shows the Post again",
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
          "from": "Hidden",
          "to": "Visible",
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

# A hidden post returns

## Trigger

The post was hidden by exactly three flags.

## Outcome

The post is shown again, unchanged.
