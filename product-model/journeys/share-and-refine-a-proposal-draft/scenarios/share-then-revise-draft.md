---
{
  "kind": "primary",
  "result": "achieved",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Proposer starts a thread in Proposal Drafts with the outline filled in",
      "kind": "actor",
      "capability": "start-topic",
      "actor": "proposer",
      "entities": [
        {
          "entity": "thread",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::category"
        }
      }
    },
    {
      "text": "The Product opens the draft Thread with its opening Post",
      "kind": "product",
      "capability": "start-topic",
      "actor": "proposer",
      "entities": [
        {
          "entity": "thread",
          "effect": "creates",
          "to": "Open",
          "facts": [
            "Title",
            "Category",
            "Opened by",
            "Address",
            "Replies",
            "Last activity",
            "Written under mandate"
          ]
        },
        {
          "entity": "post",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Body",
            "Kind",
            "Posted at",
            "Written under mandate"
          ],
          "with": "thread"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::signed-in::category"
        }
      }
    },
    {
      "text": "The Product takes the Proposer to the new draft",
      "kind": "product",
      "capability": "start-topic",
      "actor": "proposer",
      "entities": [
        {
          "entity": "thread",
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
      "text": "The Proposer edits the opening Post after the grace window to reflect the feedback",
      "kind": "actor",
      "capability": "edit-post",
      "actor": "proposer",
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
          "place": "web::signed-in::thread"
        }
      }
    },
    {
      "text": "The Product keeps the earlier text as a Post version and shows the post as edited",
      "kind": "product",
      "capability": "edit-post",
      "actor": "proposer",
      "entities": [
        {
          "entity": "post",
          "effect": "changes",
          "facts": [
            "Body",
            "Edited"
          ]
        },
        {
          "entity": "post-version",
          "effect": "creates",
          "facts": [
            "Text",
            "Address",
            "Published at"
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

# Share a draft, then revise it

## Trigger

A proposer wants feedback before paying the deposit.

## Outcome

The draft shows the revised proposal and every earlier version stays citable.
