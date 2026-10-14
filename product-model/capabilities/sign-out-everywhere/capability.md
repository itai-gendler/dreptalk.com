---
{
  "availability": [
    {
      "place": "web::signed-in"
    }
  ],
  "domain": "devices",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/pages/api/auth/logout-all.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/session.ts#revokeAllForUser"
    }
  ]
}
---

# Sign out everywhere

A person ends every session of their account at once, including the device they are on.
