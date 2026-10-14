---
{
  "availability": [
    {
      "place": "web::administration"
    }
  ],
  "domain": "notifications",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/admin/notifications/[id]/test/route.ts"
    }
  ]
}
---

# Send a test notification

Send a test message through a channel. Success confirms the provider accepted it, not that a device received it.
