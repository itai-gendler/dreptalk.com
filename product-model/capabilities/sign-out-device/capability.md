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
      "target": "src/pages/api/auth/sessions/revoke.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src/lib/auth/session.ts#revokeSessionForUser"
    }
  ]
}
---

# Sign out a device

From the Devices list, a person signs out one of their own devices.
