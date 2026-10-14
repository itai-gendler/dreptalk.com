---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The DRep connects a wallet holding a different DRep key",
      "kind": "actor",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    },
    {
      "text": "The Product refuses to open the form",
      "kind": "product",
      "actor": "drep",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::signed-in::thread"
        }
      }
    }
  ]
}
---

# The wallet holds another DRep key

## Trigger

The connected wallet's DRep key is not the one the DRep signed in with.

## Outcome

The form does not open.

## Edge cases

- A script or multisig DRep can discuss but cannot answer a survey here.
- A survey whose question texts live off chain is listed with a note and cannot be answered.
