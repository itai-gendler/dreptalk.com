---
{
  "type": "web",
  "actors": [
    "visitor",
    "drep",
    "spo",
    "cc-member",
    "proposer",
    "co-proposer",
    "delegator",
    "moderator"
  ],
  "entryPoints": [
    {
      "web": "/"
    },
    {
      "web": "/ga/<governance action id>"
    },
    {
      "web": "/dreps/<DRep ID>"
    },
    {
      "web": "https://drep.link/<name>"
    }
  ],
  "languages": [
    "en"
  ],
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "README.md",
      "title": "README"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "src/content/guides/linking.md"
    }
  ]
}
---

# DRepTalk website

The public deliberation site for Cardano governance: governance actions with their threads, votes and tallies, discussions, DRep profiles, analytics, the treasury and the Governance Review, plus everything a signed-in DRep, SPO, CC member, proposer, co-proposer or delegator does.
