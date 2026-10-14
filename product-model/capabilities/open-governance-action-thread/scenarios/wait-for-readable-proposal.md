---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A new Governance action's proposal document does not answer",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "governance-action",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::thread"
        }
      }
    },
    {
      "text": "The Product stores the Governance action without a thread and retries on later runs",
      "kind": "product",
      "entities": [
        {
          "entity": "governance-action",
          "effect": "creates",
          "to": "Syncing",
          "facts": [
            "Action ID",
            "Type",
            "Proposer address",
            "Deposit",
            "Submitted epoch",
            "Expiry epoch"
          ]
        },
        {
          "entity": "thread",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::thread"
        }
      }
    },
    {
      "text": "The Product opens the Thread with the real title once the document answers, or with a title built from the type and id after six attempts",
      "kind": "product",
      "entities": [
        {
          "entity": "thread",
          "effect": "creates",
          "to": "Open",
          "facts": [
            "Title",
            "Category",
            "Opened by",
            "Address"
          ]
        },
        {
          "entity": "post",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Body",
            "Kind",
            "Posted at"
          ],
          "with": "thread"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::thread"
        }
      }
    }
  ]
}
---

# Wait for a proposal document that cannot be read yet

## Trigger

The proposal document does not answer yet, typically a freshly pinned IPFS file.

## Outcome

The thread opens once the document answers, or on a fallback title after six attempts.

## Edge cases

- A document that arrives but fails its hash check, is not JSON or is too large is not retried; the thread opens on the fallback title.
